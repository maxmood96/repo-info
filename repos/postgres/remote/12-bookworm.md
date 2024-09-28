## `postgres:12-bookworm`

```console
$ docker pull postgres@sha256:aa8b61babf69488ddccb5c617462edf18842dc647d7dad50e2f186a0479400bc
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

### `postgres:12-bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:081117214c1a1e0e5338c0e457f783bf970fc508df316f8ac435b05b52bf5ad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.5 MB (148453231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb1fb8981959b137cb38510949d8d3924c0c781ba833c44b0b205b2eff14b4f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:22:52 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_MAJOR=12
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_VERSION=12.20-1.pgdg120+1
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:22:52 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:22:52 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7590b342caf0e29287e21d4ecd90abd58bd1cb62bcf84e566b9d29e3f9a5df48`  
		Last Modified: Fri, 27 Sep 2024 06:03:14 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb18e2728d682b586b6289071d26919cd7ef2662fd343243ea6ab90b18a73a24`  
		Last Modified: Fri, 27 Sep 2024 06:03:15 GMT  
		Size: 4.5 MB (4533694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22986b85c3ea7ae0439bd26db96ddba811d4bbf91b6b2ac672ef0ce7ee040a5a`  
		Last Modified: Fri, 27 Sep 2024 06:03:14 GMT  
		Size: 1.4 MB (1446628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab728509cf176064cc91852770511b5cb7a0bf4ac0e9479a1655667a4012ca0`  
		Last Modified: Fri, 27 Sep 2024 06:03:15 GMT  
		Size: 8.1 MB (8066305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73873b7d6c2e65f0e2da414fa1949b6a4b3c330ff044a47b55c4d47733a8bd86`  
		Last Modified: Fri, 27 Sep 2024 06:03:15 GMT  
		Size: 1.2 MB (1196060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5d8ce8b2b87cfd6371adf28507eaea5c6b2f4c89196682bcd71a3c40f7df42`  
		Last Modified: Fri, 27 Sep 2024 06:03:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e48e02fafbb7f076e59648b626d7dcbcf3c44203e1d4838670a3580aa9fd712`  
		Last Modified: Fri, 27 Sep 2024 06:03:15 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8697df0f38113f24976ae361825221b1db17efe19f9fdaf4393dc15e50255dd1`  
		Last Modified: Fri, 27 Sep 2024 06:03:17 GMT  
		Size: 104.1 MB (104064939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7631fc0f8cd381722f3793814aebf1f18bd210b5255dc996400fa5d3cea5a625`  
		Last Modified: Fri, 27 Sep 2024 06:03:16 GMT  
		Size: 9.0 KB (9011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65d8590c845218ed5b39ecba40d40d9fb7d684e0349592c8fe485ca8be6f625`  
		Last Modified: Fri, 27 Sep 2024 06:03:16 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa0d453b82230b128be757ebf956c853ad353b9e43df5e887fae543095dfdf7`  
		Last Modified: Fri, 27 Sep 2024 06:03:16 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405161c5b60aea969a29add6d5c19466e629f4115bd1ea31dedc4341327a1f84`  
		Last Modified: Fri, 27 Sep 2024 06:03:17 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5ab8bd4d28e1a3c7ef50b4e53b3d77695d709e376037492ece8d1f143fb908`  
		Last Modified: Fri, 27 Sep 2024 06:03:17 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:aeb5c3deb6742ba67e091d301bf3803479dd1c68af0211620c4edf9999ae070a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5654745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7012e579f7670c33abb2abf0cb80231ffd08c8de679a410ccb1da43bcb7337c8`

```dockerfile
```

-	Layers:
	-	`sha256:ad936bd0855922f3bc5a5e801cdaa4071d7c1e9bbdd35714a42638150f47672d`  
		Last Modified: Fri, 27 Sep 2024 06:03:15 GMT  
		Size: 5.6 MB (5600304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5c451f76e38f69b4faac3f3c72d87844f28027381c0f21f1d316455639284a6`  
		Last Modified: Fri, 27 Sep 2024 06:03:14 GMT  
		Size: 54.4 KB (54441 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:a531c9d975f754eb6470067fd69d97984a655df299a6ddfad305ce4a121389e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141164849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92c61bf3b3616955014b0dbb35da8e1ba5df88ff56506f1787038f221ceae82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:22:52 GMT
ADD file:91b876c600b7d3198bc98296224f6861440f56fcbd15a2188c95a8785b94061a in / 
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_MAJOR=12
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_VERSION=12.20-1.pgdg120+1
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:22:52 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:22:52 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:75a20c44e8becd141ba586ea413a1649251437a207502d4f8ad23d208f013e60`  
		Last Modified: Fri, 27 Sep 2024 03:21:44 GMT  
		Size: 26.9 MB (26887302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c6ea23909628e95a04f64c06b1b13eebd58d9f30c2461472e0fd1c95625882`  
		Last Modified: Fri, 27 Sep 2024 12:46:03 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cf5a39ea7a92b60bacf30a2ff06dc0257586469412c3750aa8e7e8d24013b7`  
		Last Modified: Fri, 27 Sep 2024 12:46:03 GMT  
		Size: 4.2 MB (4150914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9652982ab16c0fd7f2b19b22797765e0112bcc85ccfbce9d9c896800817166d`  
		Last Modified: Fri, 27 Sep 2024 12:46:03 GMT  
		Size: 1.4 MB (1423861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cac6f365cdea7c5c033fccf217977852d663b85fca3e0f387964725ed6eab2`  
		Last Modified: Fri, 27 Sep 2024 12:46:04 GMT  
		Size: 8.1 MB (8066414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2890a87d0918b7dc88391359a7e60e89a43b68c263899e83f0c79d285043c3d3`  
		Last Modified: Fri, 27 Sep 2024 12:46:04 GMT  
		Size: 1.2 MB (1194858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ebdb5a09ccbe681815ca6e8c740383a60ade1d5ca7ccd3727470bf53d2100da`  
		Last Modified: Fri, 27 Sep 2024 12:46:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6af01088a4c63d9d24095558b1c03e9b5721fa603f3e2a2b5b9c0b1c811d312`  
		Last Modified: Fri, 27 Sep 2024 12:46:04 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef7ccd22d0bcf4688332fb5b93714799a277c143c0a6dd6aee28d0941960801`  
		Last Modified: Fri, 27 Sep 2024 14:03:53 GMT  
		Size: 99.4 MB (99422158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be194c0b454e5e5e50134996cd130c4e5117812744fd62e0cfaf95e1e0b767d2`  
		Last Modified: Fri, 27 Sep 2024 14:03:50 GMT  
		Size: 9.0 KB (9021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbbb2ad4750eb4fa28747d2ea789dcf9c0e03c96db697b4855ca4012ca3ec66`  
		Last Modified: Fri, 27 Sep 2024 14:03:50 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d257c372c9cf0c26fec383198f569ad85ef5bde86166152f41497b21f3b034`  
		Last Modified: Fri, 27 Sep 2024 14:03:50 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5090aba2ceaea40e5f20cbe3075489b11dadc135ca6129b44732b1c872d50f51`  
		Last Modified: Fri, 27 Sep 2024 14:03:51 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15ba0563dee84a0f7e998aaeb40105711e66a1cf5fa47a0ab7cc30f1651c5bb`  
		Last Modified: Fri, 27 Sep 2024 14:03:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:e237738d70a476dc1dde69531baec24f1010ade21f0f0f902cdec90d800b8877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5668340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc829209cbf72d5ea01a2fa94f6d0a48f76f609508e2d2ae80fcaa8539a84c8`

```dockerfile
```

-	Layers:
	-	`sha256:12d429e8f7fb1f361965a00815b1fc6afbb1184af8b0a9236b40165a39de24af`  
		Last Modified: Fri, 27 Sep 2024 14:03:50 GMT  
		Size: 5.6 MB (5613692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f360ad45fa0f9a9dbd036e25f92621f57025d25b9ec98be6ba3915c8e39865fb`  
		Last Modified: Fri, 27 Sep 2024 14:03:50 GMT  
		Size: 54.6 KB (54648 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:8a5c0a82b61b91a9208d8367457ec2185547913e82a054ac4c12a76e16b6c475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (136012172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f33b2020cc5aef90ea6e98c930276bfb246c90b8163503b86ada28fdbc0e6a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:22:52 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_MAJOR=12
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_VERSION=12.20-1.pgdg120+1
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:22:52 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:22:52 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d39d2d96734dd6c7fab8068ba08f92c7cbc1c98f5894e1c25c2265db8f74a5`  
		Last Modified: Fri, 27 Sep 2024 13:19:22 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a22c508463eb866d2934abcd7fae9234d1932914b2986b18d2d3758cab849b`  
		Last Modified: Fri, 27 Sep 2024 13:19:22 GMT  
		Size: 3.7 MB (3742490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f5dd4f0fd99c6a3012452faaca1c7f98c7ab9c5fb902ab68355721421dfcbf`  
		Last Modified: Fri, 27 Sep 2024 13:19:22 GMT  
		Size: 1.4 MB (1413563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0666a7837552389500ae71853be89df7cc34d20e8d5504a056f763f2855fcf80`  
		Last Modified: Fri, 27 Sep 2024 13:19:23 GMT  
		Size: 8.1 MB (8066267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f162e5e3b3b23a992b39df4c6ca227d40dfd24548618a1b27edaae3f7b2c1cc`  
		Last Modified: Fri, 27 Sep 2024 13:19:23 GMT  
		Size: 1.1 MB (1066954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e04d94c3aff724f37298d31af669139c832234fb26aebfd50d54ebef6be80a`  
		Last Modified: Fri, 27 Sep 2024 13:19:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d780f92ccafa30779296e018d5d6148e75f89526330fc3bdf6e40d930801edd`  
		Last Modified: Fri, 27 Sep 2024 13:19:23 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac1419cbef242e69710c46b600f1f21ff3c1e9737e44eac074564c50fbf3e92`  
		Last Modified: Fri, 27 Sep 2024 15:52:47 GMT  
		Size: 97.0 MB (96985412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef77553377bb1e22a33ceb3f516bf57c0653f834c8381710328941f12038725`  
		Last Modified: Fri, 27 Sep 2024 15:52:44 GMT  
		Size: 9.0 KB (9019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791f8d2d99073282e2f3969bd617f95b79e0a53741ba36fde533be3714e04757`  
		Last Modified: Fri, 27 Sep 2024 15:52:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416c743dc66acbc6fbe61e1cc921c9d8d6f63122e0a0de883f4098c36bf72643`  
		Last Modified: Fri, 27 Sep 2024 15:52:44 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e899dec992495395a86069f175da79f22ab7be54cddafdc887f5953c11e9280`  
		Last Modified: Fri, 27 Sep 2024 15:52:45 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2ac67e0985a7b38463e4db10ccac3baa8e3f11ba48b65cb0e5b703a4054b7a`  
		Last Modified: Fri, 27 Sep 2024 15:52:45 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:f7002fc1b223cb58a3eb7227ecf6c4462189d17bac481934858835a0c9a2ef92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5668009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f197ff89394038d01d12b532066158e04900f1a5a843638a3361a53955224f7`

```dockerfile
```

-	Layers:
	-	`sha256:172aa897cacf05a7c85c645b833e34c2363cfbe5103448f5a45709e37e3a6a27`  
		Last Modified: Fri, 27 Sep 2024 15:52:44 GMT  
		Size: 5.6 MB (5613361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ec7aa1ec9861a0458d3fdae4903212b35db5b5be18d34bac11df0222b79b345`  
		Last Modified: Fri, 27 Sep 2024 15:52:44 GMT  
		Size: 54.6 KB (54648 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:cfa55bf235088d332529a17c7fb4cf5cc21d495c1d7e643983fa9fe75224781c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.7 MB (146686485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1193a2f9bbaceef7495e9dbf3b137eb1382b7725ace80d2bf7097c4b3a0707a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:22:52 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_MAJOR=12
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_VERSION=12.20-1.pgdg120+1
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:22:52 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:22:52 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c88e7faf79a34dd0af94058994e066483fb95ac60c57004716687e64f9bed5`  
		Last Modified: Fri, 27 Sep 2024 19:04:17 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86552d6a2e14fbce88d8ffa08a7f7e06dd4c6d7f208b84997c96c0f91053cba5`  
		Last Modified: Fri, 27 Sep 2024 19:04:18 GMT  
		Size: 4.5 MB (4499154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a986120aadb711cc1e9e8fbd5f2f62c7b123e0c329d6c1812be7bc38d03479b2`  
		Last Modified: Fri, 27 Sep 2024 19:04:18 GMT  
		Size: 1.4 MB (1378717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f6f593e3897cc85ba643ed6309995123ad8701a994700d1a796bb9ab0a1200`  
		Last Modified: Fri, 27 Sep 2024 19:04:18 GMT  
		Size: 8.1 MB (8066349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76441873964fa4a8d07dd408edfe47b022e2506a9fdabd6467f71cce1bd6c96a`  
		Last Modified: Fri, 27 Sep 2024 19:04:19 GMT  
		Size: 1.1 MB (1108704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00daffc086af223cc3083937b64cb98e4f5dbaae60aca84f869b695d9be65b4`  
		Last Modified: Fri, 27 Sep 2024 19:04:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e872bee6899bad3fe1acbb7e580e8381aa1f6a99b1e8d7b427011fe3beb076a`  
		Last Modified: Fri, 27 Sep 2024 19:04:19 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82256c976e762ecfa7418bba2d83ef8d6c32df337bb75d08c5f2f7aa2ba83d91`  
		Last Modified: Fri, 27 Sep 2024 19:20:25 GMT  
		Size: 102.5 MB (102457861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7903975a2515eb13575ac09cf92377f422be46f2882a284d4b4f58d1c00eafcc`  
		Last Modified: Fri, 27 Sep 2024 19:20:19 GMT  
		Size: 9.0 KB (9013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8becdcec6d28c95b22030b37cdf5e959cb361b66803d65b88dabf1cc60dc9d9a`  
		Last Modified: Fri, 27 Sep 2024 19:20:19 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ec399f2bd0f65c2103d2a63fde916412dc191b067c4ceb056037d42fff7979`  
		Last Modified: Fri, 27 Sep 2024 19:20:19 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8fe34947a75b66ca1dcb0215796604e355976e33f60d683c8773aa1a471c24`  
		Last Modified: Fri, 27 Sep 2024 19:20:20 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49f04f4ddecb7f69058fc2d689cc95d26640ac5a7155be8f4a87183f2b8d899`  
		Last Modified: Fri, 27 Sep 2024 19:20:20 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:7989a7bf1f4e9bac42275f9cf144eb3e2e6d962cc625dd80d03c5158c357765f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5661395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94de00102b5dde8fecdda0d337b147466eff12af0362df2204fde2f46437ea4a`

```dockerfile
```

-	Layers:
	-	`sha256:47031c9582dddffd24cee8cda3bb76b4bfc6c163f05b4a2bcd25395aae63a039`  
		Last Modified: Fri, 27 Sep 2024 19:20:19 GMT  
		Size: 5.6 MB (5606645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:694178b94239b8ceb821391e7db73f5b1507925307f62ba255a638c6a27e03c4`  
		Last Modified: Fri, 27 Sep 2024 19:20:19 GMT  
		Size: 54.8 KB (54750 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:9abeda28025779390762663498ab2e9a0df675a3c67e954a61fcf9e14fb398fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156404047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5717c7f29ec0ca4cc56165b10c8feb3de2427ba600e343d626073eed97ab10f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:22:52 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_MAJOR=12
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_VERSION=12.20-1.pgdg120+1
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:22:52 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:22:52 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a67673d8470a9ab2aa41442ef9e7e1b0191dccd77fcbfc63662e994465fd5b`  
		Last Modified: Fri, 27 Sep 2024 09:12:00 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57d565fae26101bca0104b82c64c2ae3138cbd9782cbe645294c208b345f054`  
		Last Modified: Fri, 27 Sep 2024 09:12:01 GMT  
		Size: 5.0 MB (4965047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ddaa89ca92b99a7ace388e2660ee76e034627e014e8ce17727323ca0977bd3`  
		Last Modified: Fri, 27 Sep 2024 09:12:00 GMT  
		Size: 1.4 MB (1422132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03eb426b5dfa5f966a650cae50cd6f24a4ab3e5119ff03e836724a5395a2d766`  
		Last Modified: Fri, 27 Sep 2024 09:12:01 GMT  
		Size: 8.1 MB (8066304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faca728e935619ac55f6c8522cc33cb09b204b3e25833bf5a6f270066ac8b9ba`  
		Last Modified: Fri, 27 Sep 2024 09:12:01 GMT  
		Size: 1.1 MB (1137147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1440560e84f725608578915a5eae61ab26d4d778c0617aaa2fae7bbbb94e73`  
		Last Modified: Fri, 27 Sep 2024 09:12:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf895fb4f47fb6d0486f6dce775192c0d39c9c5bb1a9dedc2d95d483afd7889`  
		Last Modified: Fri, 27 Sep 2024 09:12:01 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822f58605c10d5f39e4952f3b271c877d1eab495c518c6b0151972f72348ab45`  
		Last Modified: Fri, 27 Sep 2024 09:12:04 GMT  
		Size: 110.6 MB (110649854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9694984bfe0bdf99286d67877cd944f0b3944dce729beccda74e7e32692c92`  
		Last Modified: Fri, 27 Sep 2024 09:12:02 GMT  
		Size: 9.0 KB (9020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f396f012b4c1e1be34e220de1e9bd13594a6da862146740238c67d2a40d39a75`  
		Last Modified: Fri, 27 Sep 2024 09:12:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a33c4b8ccb4c09630e876d525d4caca87f5a3cc3a7a8d1925b387bcc0be75ae`  
		Last Modified: Fri, 27 Sep 2024 09:12:02 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fd94366720d9d1bf34756f06012acadd2c37785f17282acc8ea47b1419728a`  
		Last Modified: Fri, 27 Sep 2024 09:12:03 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff9d6e6d5a8781169982a421c23fb806fd7cb679e1e1f48a3bb4f70f3bd8c6a`  
		Last Modified: Fri, 27 Sep 2024 09:12:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:bfe299273350b8845c484f1a3829258aaa030cc2bc4ca1450f84475471134502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5666135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5dc5d2eaafa8b89b375a69f40fb1c533671f53f2f7e7eb969d29f67b750af8`

```dockerfile
```

-	Layers:
	-	`sha256:de90a6cc7e0fc573685c9bdb4a8467aa95f787e4b41f8d0e9e517c731ee7f957`  
		Last Modified: Fri, 27 Sep 2024 09:12:01 GMT  
		Size: 5.6 MB (5611745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64a2fff97daffa684ab3aa18a87cdcc6934e291da18ddac73acda6bbc0983c4b`  
		Last Modified: Fri, 27 Sep 2024 09:12:00 GMT  
		Size: 54.4 KB (54390 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:4253fc4de4805984d16256f4bcfe867ab08559a5d110b055be9e1c2520614edb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.9 MB (143906731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a70d7a65cc9726398475eed86b9b571753c98e012a56da0407755fd0289ba9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:22:52 GMT
ADD file:9ffa4d53a074e91efecf5e26e3b67077f46165e0d042c1e6cf1b93c531ed2bc4 in / 
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_MAJOR=12
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_VERSION=12.20-1.pgdg120+1
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:22:52 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:22:52 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:89502a0eae32ab684bc9df3d9922ee2874839b178a693286c4b866f5ca8e93f3`  
		Last Modified: Wed, 04 Sep 2024 22:24:11 GMT  
		Size: 29.1 MB (29125054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6816d65a3e4f8353643a7b128899349381df213efa9656f19c10a9b5ea808b4`  
		Last Modified: Thu, 05 Sep 2024 16:53:14 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2582c48faeb5f321bdf902ceaf70b33862248078e2e4c9787f83b98bd0c43fd5`  
		Last Modified: Thu, 05 Sep 2024 16:53:15 GMT  
		Size: 4.5 MB (4475058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3e8f22c29b2f27c213f3e56320bf54846e2737e061f819069f7809894322c0`  
		Last Modified: Thu, 05 Sep 2024 16:53:15 GMT  
		Size: 1.3 MB (1333759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04757d844a23c2a19dffb65588017e67356710f54d19ba6625eb9161a56ae52`  
		Last Modified: Thu, 05 Sep 2024 16:53:16 GMT  
		Size: 8.1 MB (8066466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cee2e1b1a6fa76e1bec8663034ad45ecc047698912407ef607416445f02309b`  
		Last Modified: Thu, 05 Sep 2024 16:53:16 GMT  
		Size: 1.2 MB (1182625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220e33cd4eaacd1b9c035697266946423133bd882349a6474f6ca67e49c77c9d`  
		Last Modified: Thu, 05 Sep 2024 16:53:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a7846879e7ce6da899c4a884930489c2259f94036b0d58b324e2e4b5879ddb`  
		Last Modified: Thu, 05 Sep 2024 16:53:17 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327951e1f94d170db9fda390442f2021988461878b82caa0bbf0f7d604d99081`  
		Last Modified: Thu, 05 Sep 2024 21:20:32 GMT  
		Size: 99.7 MB (99704421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7727caaa6f1fb2de9fb6b676832a2ee4c5f088c80a8e1bc2c8c172f5ff537a0c`  
		Last Modified: Thu, 05 Sep 2024 21:20:22 GMT  
		Size: 9.0 KB (9025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe31d37415c66f2b86639db8b8fcf3efbcd627f91f06f56e0211836013c686c`  
		Last Modified: Thu, 05 Sep 2024 21:20:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a849b86702f25e56c6e56b5e305ce1f18545a475cf2626ff7838747d8b9170bc`  
		Last Modified: Thu, 05 Sep 2024 21:20:22 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f917f9b6bec47d1e4e824646372d8b1adf8949a07be8babc3ade092e3e1e1c3e`  
		Last Modified: Thu, 05 Sep 2024 21:20:23 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c666f9ce69c8b921d493b024fc59be681ed273c400e0b9006af1ac2ee5a529`  
		Last Modified: Thu, 05 Sep 2024 21:20:23 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:745b6bccdfdd2c7a7d9c36dd11786df5ef6f48059ed0ce54c4cd3a8b227609ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 KB (54306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:730768436add5c2d5a353d8e841300967fe65a917241495bc72e308a245f0c56`

```dockerfile
```

-	Layers:
	-	`sha256:cb39c51f462ebbff4a4444b917731810ad3764cfce9fda09205069287d286af4`  
		Last Modified: Thu, 05 Sep 2024 21:20:22 GMT  
		Size: 54.3 KB (54306 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:131fd710eceda0d6ad04d4d5cadf072cac36216b076d3ba95f60a666977a6fe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160424832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b60da0e1fc990c19d5ce1cfbcadc65826fd345e5bca6f9cff7d048020818fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:22:52 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_MAJOR=12
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_VERSION=12.20-1.pgdg120+1
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:22:52 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:22:52 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf54cdb3c51234a200e3a5ea0b998d2697f1733d159674b2d59fd47da9244445`  
		Last Modified: Fri, 27 Sep 2024 22:28:17 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73c826b6f3a053b9527e8192429426da96e225f991578afaac9f17ae3e6b122`  
		Last Modified: Fri, 27 Sep 2024 22:28:17 GMT  
		Size: 5.4 MB (5368147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb16340d27ab05690ec0584c9807deb822e4fc432214b080a1ffe7d1a323fcd`  
		Last Modified: Fri, 27 Sep 2024 22:28:17 GMT  
		Size: 1.4 MB (1368568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71311acb7d188bc0ebb15a1a318aebcc0940c122ea4068301601bebad4193623`  
		Last Modified: Fri, 27 Sep 2024 22:28:18 GMT  
		Size: 8.1 MB (8066361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9f2dbbadd51375c292706713605a90574df14831465849b42dee1b7efec1c9`  
		Last Modified: Fri, 27 Sep 2024 22:28:18 GMT  
		Size: 1.3 MB (1283464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75167300b575090696c4ac208c0f19d409c71a9aba5b6433e69e19a2688b4d29`  
		Last Modified: Fri, 27 Sep 2024 22:28:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f6c4e0fd05ccfc4abe5c654cb666bb38899c21c4ea020fdcac2105b2476a1b`  
		Last Modified: Fri, 27 Sep 2024 22:28:18 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3c2ac167b410af730b165150be3225c7ea96ce5afbeda12981c70c2c6e0e1c`  
		Last Modified: Fri, 27 Sep 2024 22:35:51 GMT  
		Size: 111.2 MB (111196795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ce17529f42935b5b1452173a66b3334cf02de8989accaa682e063f4dd5a959`  
		Last Modified: Fri, 27 Sep 2024 22:35:48 GMT  
		Size: 9.0 KB (9016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6653608ea1d503ca97011b8354df8e6a0091e41dca86753f1070665cc4837b`  
		Last Modified: Fri, 27 Sep 2024 22:35:48 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36325b130a92434d24c6d53014082b65846b43ab09b3491593c758ca915a930b`  
		Last Modified: Fri, 27 Sep 2024 22:35:48 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524fc2d8d8acca527aa9c89951531b698f28080d783867a502d39d2a1f6a1ae4`  
		Last Modified: Fri, 27 Sep 2024 22:35:49 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2105412f39a8d31831b8577a28df91286f0aba6dbbdbfae5cbc1b7a388ff51d1`  
		Last Modified: Fri, 27 Sep 2024 22:35:49 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:aeff7fcf321d3d45aa0fd681df018e863dc68aed49534e8a478fcead0e6f7b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5662032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494f8f7240ca176aa61c5a04537160a965020f4198fe4ad969072e4b1742ee06`

```dockerfile
```

-	Layers:
	-	`sha256:cbadc3a90c9b89785d6fbba9e6b185d7f6577256bba417b933033bb5c2104c25`  
		Last Modified: Fri, 27 Sep 2024 22:35:48 GMT  
		Size: 5.6 MB (5607533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e810ccb86c3d5558a005b5f0aca75318af912698496adb5894510a99011f3947`  
		Last Modified: Fri, 27 Sep 2024 22:35:48 GMT  
		Size: 54.5 KB (54499 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:bf791b1995942015f2da57dd1bebe5806ef53a336e1fa9f34f3099d472222456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.9 MB (153857032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485d123c085bb314226a82bdca7941c7b1f8c168da6763fd5b57f465ff5600c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:22:52 GMT
ADD file:ee3c94adee604dbcaddf5d6c372b1f325a4443f66bd717dedf1ff7d9fb1ba116 in / 
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_MAJOR=12
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_VERSION=12.20-1.pgdg120+1
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:22:52 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:22:52 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:eca1e192de25fb56826ff7ed14b2e1532a49c27a08147a6249506eafd8ab4472`  
		Last Modified: Fri, 27 Sep 2024 02:47:22 GMT  
		Size: 27.5 MB (27490024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1d520b9a9ee5285c4270cc88cbbb8e5bc257213ae2140ccc073ec841b0f706`  
		Last Modified: Fri, 27 Sep 2024 15:27:34 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c8983de478016b32e2c145a386fac8ee381006eb0b61719536eac3ec333f6a`  
		Last Modified: Fri, 27 Sep 2024 15:27:34 GMT  
		Size: 4.4 MB (4391057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006718e1602ae92f7ab3999ca111386351cd2a5854bc2f0fec2c3f24d107c6b8`  
		Last Modified: Fri, 27 Sep 2024 15:27:34 GMT  
		Size: 1.4 MB (1412683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9cb4d66be19cd79ca495d5b66ad9554021cad9a8ed3f2fdd4db17fca094f043`  
		Last Modified: Fri, 27 Sep 2024 15:27:35 GMT  
		Size: 8.1 MB (8120493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57948d4a9af326497a193dfea3caadae37f5a2ce4e2788f989fb3c6373d5d1b`  
		Last Modified: Fri, 27 Sep 2024 15:27:35 GMT  
		Size: 1.1 MB (1096736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f52d75f1b72f3b0d72d67eae3e76667e797da2c8adb610cf1d2edcc241170c0`  
		Last Modified: Fri, 27 Sep 2024 15:27:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02c450ab117a5683efd8ffd8be44cea8c3b424a355ab477785c13980c86466d`  
		Last Modified: Fri, 27 Sep 2024 15:27:35 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266c8bc6ff3597a0662034cb9cf437cb6840a04d76880079a5501630f03118a1`  
		Last Modified: Fri, 27 Sep 2024 15:35:45 GMT  
		Size: 111.3 MB (111326707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4885dd79782bed0df82fc32f68fda83efb181d446c77b85b9f4da9026cd40902`  
		Last Modified: Fri, 27 Sep 2024 15:35:43 GMT  
		Size: 9.0 KB (9013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:798280862e8e2de01231139abc81514f3b2be555056229699079d1f3f6b9e9f8`  
		Last Modified: Fri, 27 Sep 2024 15:35:43 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b3857b6783299dd1a1a11bfcf39f452b99ead4e57bfb0d211a35df0ffffc6c`  
		Last Modified: Fri, 27 Sep 2024 15:35:43 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c878e23694a12bc78618548fe7de1b70b1eed2e7a3c204cbf3510508e1d4ed0b`  
		Last Modified: Fri, 27 Sep 2024 15:35:44 GMT  
		Size: 5.4 KB (5414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47bde8843828aea0eb677ed7b2c31a3a0919c82cac9d1a726543e63ee061c863`  
		Last Modified: Fri, 27 Sep 2024 15:35:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:7b963af2fdc6db1b6638ad9747188ee5917a7d7d9040fd548e8183c0b9041ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5654139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a5073d1388406b4c07c0748ffe6a8cfa96da0f3b85545e82e1d1516b52288c`

```dockerfile
```

-	Layers:
	-	`sha256:79c521b3d0ca5e32c6b6c547a1cffdbd6ed6cb354bd1244461e17c527891ba43`  
		Last Modified: Fri, 27 Sep 2024 15:35:43 GMT  
		Size: 5.6 MB (5599698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e6de343ef7eda0e3803cc27c71cf5718846ae444458c3fed6ec57b5d156a966`  
		Last Modified: Fri, 27 Sep 2024 15:35:43 GMT  
		Size: 54.4 KB (54441 bytes)  
		MIME: application/vnd.in-toto+json
