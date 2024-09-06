## `postgres:16-bullseye`

```console
$ docker pull postgres@sha256:515059eda28298fec5e406b4b324efa36fd3057259843608f84185035ddebe9b
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

### `postgres:16-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:b1cde2af83ff0149843d13a5626a7958526fb5144cbc475efdb236b994b9f182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.0 MB (145043627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09106e69d5c3594aa96edd11aa3830a73d1f5e063133c8a3d76f5fd5aca30d5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:20:28 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_MAJOR=16
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_VERSION=16.4-1.pgdg110+1
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:20:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:20:28 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:20:28 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b85298a8b2127acf97f498283bce8fefab8dedf6b417740896163e02c643de8`  
		Last Modified: Wed, 04 Sep 2024 23:09:02 GMT  
		Size: 1.7 KB (1680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95c9279f30b65c6fdee50e93464f72427a406218d4e38a8d4f5334315825cdc`  
		Last Modified: Wed, 04 Sep 2024 23:09:02 GMT  
		Size: 4.3 MB (4308206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6313bf914f342b25e7e606d546e56831837ab8a29b8c62adf881e4bf755366d3`  
		Last Modified: Wed, 04 Sep 2024 23:09:02 GMT  
		Size: 1.5 MB (1472242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c169fcc9f8efe0ae227186f8e5a5a1ce5fbcf69792fa0601969412597104a4`  
		Last Modified: Wed, 04 Sep 2024 23:09:02 GMT  
		Size: 8.0 MB (8044415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c4beea2171ed4f23d0df0f723c441494ef874ac0f84345c1a8ab223294dba3a`  
		Last Modified: Wed, 04 Sep 2024 23:09:03 GMT  
		Size: 1.0 MB (1038368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd2333708a2535baa754a3f983d940333fd16a13404e5b16b2e719fa0c05a5f`  
		Last Modified: Wed, 04 Sep 2024 23:09:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835bd264582eb6e327411337666d0d4712a71212aae5b5032db26ccc0f6dd4fc`  
		Last Modified: Wed, 04 Sep 2024 23:09:03 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f994d0fdd079e036be6a6b7eee9a643c4d86a16f70b4aa4b7600860e040c00`  
		Last Modified: Wed, 04 Sep 2024 23:09:04 GMT  
		Size: 98.7 MB (98730954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46dad05ce1d2b39bd38640770c5b5ebea383b7e7faf5080f0b63f2ea81c7fa9b`  
		Last Modified: Wed, 04 Sep 2024 23:09:03 GMT  
		Size: 9.9 KB (9925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0d6d069b8317f335dbe51d8c28467141debf3f73025a85ef4b64a5b46f534f`  
		Last Modified: Wed, 04 Sep 2024 23:09:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6f1725d57b993d5af22d2a0e4f7634fd30c6f0f65ec5ebdae5b366a0895b54`  
		Last Modified: Wed, 04 Sep 2024 23:09:04 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18ef075dda28fbadc9fd710b6c68e7e8628d24f3020adf209207ff78b518f06`  
		Last Modified: Wed, 04 Sep 2024 23:09:03 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e833a193ea76ad0ecd7684119765f27ba8c565c961dcf7889d435fe9a78418c2`  
		Last Modified: Wed, 04 Sep 2024 23:09:04 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:8c4eeb423a1a57e6236a76fa502ade307ef366ecaca89a74502b89e4c65d6797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6051034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5204b81f906c64b05ec954e49abba5c9beeebc6fd208803a645f573906b194a`

```dockerfile
```

-	Layers:
	-	`sha256:e9fa932abd3fb95ba679e0c8372ff1b011a10c216f2b5acb5fd42b70bb7c8458`  
		Last Modified: Wed, 04 Sep 2024 23:09:02 GMT  
		Size: 6.0 MB (5996894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd37ad8e2cc702da54d6fbf07eb51be6a1c2471368c4739c60e48d54bb0e93d4`  
		Last Modified: Wed, 04 Sep 2024 23:09:02 GMT  
		Size: 54.1 KB (54140 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bullseye` - linux; arm variant v5

```console
$ docker pull postgres@sha256:710ee50dc8ee2a9166c41291765e953d943b4c970594f30e27a97ab99b998c46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.0 MB (137964793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c676ed647752ada2e3fec32d3d7e853dff6440dacdbc7f88420ae1ce8aca9da9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:20:28 GMT
ADD file:b6f3f19f4bd2bf78068380b3cd10d72519ced99a2b5abe830b4729df341dcfdf in / 
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_MAJOR=16
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_VERSION=16.4-1.pgdg110+1
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:20:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:20:28 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:20:28 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c8ed7888c72e20491bc1a05ae8b473757ca4d400de33029eab69bacfb9dd933b`  
		Last Modified: Wed, 04 Sep 2024 21:52:15 GMT  
		Size: 28.9 MB (28924911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff08d14835d2a8416c4df6e3dd9e317c595ade6582b069f140f08286cdbad6e`  
		Last Modified: Thu, 05 Sep 2024 06:06:12 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f652cee625fb7c902694dfb64a4dcbd644862142e4dfc68893dd60dd62f5c5`  
		Last Modified: Thu, 05 Sep 2024 06:06:13 GMT  
		Size: 4.0 MB (3991654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d02501ed234a0a5d8e7cbd6a3b78af584bd0c2c5a2559d08ee15ba7e5f06830`  
		Last Modified: Thu, 05 Sep 2024 06:06:13 GMT  
		Size: 1.4 MB (1449215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9160d82cccd2166396d8525cd76bfc39ac2c6a06230e6c5b4fb2a4b6e736dd`  
		Last Modified: Thu, 05 Sep 2024 06:06:13 GMT  
		Size: 8.0 MB (8044317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5cb92b5411bcffbc1c9ab1ecc57e17994310a00f9727277ec63f3e3cca4bf2`  
		Last Modified: Thu, 05 Sep 2024 06:06:13 GMT  
		Size: 1.0 MB (1034881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52386f3c03837e7199651cb1044a0ed933f4fae098f20975ad8db2eb6262efd`  
		Last Modified: Thu, 05 Sep 2024 06:06:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d037fe4403f7b5c213daecbfb442898d0fca3592426a40bf38cd34bacc6ae7ce`  
		Last Modified: Thu, 05 Sep 2024 06:06:14 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d932cd36de636f416fa0d2bae01ad70547644c12b13ebf618c1d835d82fcede`  
		Last Modified: Thu, 05 Sep 2024 06:38:28 GMT  
		Size: 94.5 MB (94499046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2b1bf7476808ab1c9121cd301fc8294304e6217419e3f7646be3317d534f21`  
		Last Modified: Thu, 05 Sep 2024 06:38:25 GMT  
		Size: 9.9 KB (9931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6aead6b2592d48d39775e653ac5e4c4770099af8bfcc4a9f257bd9b122bba57`  
		Last Modified: Thu, 05 Sep 2024 06:38:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed9ac65d78443817dbabd99185886cd1771ecca36bfecab6cf731dffa7ad9a5`  
		Last Modified: Thu, 05 Sep 2024 06:38:25 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c98916ca277f8838b43f80e88a5fbddc0ea7cc90d6c87cf8e5cabe57b853fa1`  
		Last Modified: Thu, 05 Sep 2024 06:38:26 GMT  
		Size: 5.4 KB (5425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4992b66025c0d89ea928933e04ec11da803e92a76dac43fb411033560d6329b`  
		Last Modified: Thu, 05 Sep 2024 06:38:26 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:754d59d2e5f2e4b706e63224a34bc13e855841dc842883b29f094068f00b20b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6068633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffbd1383a3a5c6db430d4e7812efc2868a6baae020486ef352c7a0781ac30952`

```dockerfile
```

-	Layers:
	-	`sha256:479f66e61b8ec74b61fc657e60a059c833854faaf3380ce7b84510742ef261ab`  
		Last Modified: Thu, 05 Sep 2024 06:38:25 GMT  
		Size: 6.0 MB (6014288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85ac7bda981ec0adb418201524795bb425e17dbc72beda11fbb6ec43c0017c25`  
		Last Modified: Thu, 05 Sep 2024 06:38:24 GMT  
		Size: 54.3 KB (54345 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:8f765672cc6b24a056b2f2f1afac4b3cf0d5d9cf0966466665e7bcc73191bc03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133078226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad555d6ec9a9a3f3173957b9aba1e6d4bf5f7a4bac5fcb93012829df7ac828e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:20:28 GMT
ADD file:c451ece1244c14bce110ffbe6906867ce12f8e88234988b0edba91009a9dbbf8 in / 
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_MAJOR=16
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_VERSION=16.4-1.pgdg110+1
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:20:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:20:28 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:20:28 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f572303598915f7fb61cc4b47f7207c9ee64d52b9db5fc03ee133ec2dd679347`  
		Last Modified: Wed, 04 Sep 2024 22:02:25 GMT  
		Size: 26.6 MB (26589615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5e9c606d8528311a46a30cb82519938c43b33c4e1f31162ab88efcc0dd0f15`  
		Last Modified: Thu, 05 Sep 2024 07:11:28 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2970a29d8de911f08d48442531c9307bf0ae742938b71d029a754342b919a541`  
		Last Modified: Thu, 05 Sep 2024 07:11:29 GMT  
		Size: 3.6 MB (3601649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b66db6d98ea73837923d726df3338ff4973e9c5bd1b7514f22394af905dd9b4`  
		Last Modified: Thu, 05 Sep 2024 07:11:29 GMT  
		Size: 1.4 MB (1439215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770e958c632b7100f93874e6d8edcf6a0e7bfebd2df344b16f5d3ec2a0f0f714`  
		Last Modified: Thu, 05 Sep 2024 07:11:29 GMT  
		Size: 8.0 MB (8044293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c42f090ffe7dc7637ee220b14061287b2fc4c983da82a663fcd24defc85954`  
		Last Modified: Thu, 05 Sep 2024 07:11:30 GMT  
		Size: 908.6 KB (908647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9846d37a8dad8e0ac73680041abcd9790c9deee18bc1d3cdc6986e340820abf`  
		Last Modified: Thu, 05 Sep 2024 07:11:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b909d375e13dbdd2a339a93e951b8c697bb1f0a9622446bdac7ce891a6eba51`  
		Last Modified: Thu, 05 Sep 2024 07:11:30 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ba5dc0a298ba2d0135955cc07608c2c45b2e5fde07a3a7b6af4432539785f4`  
		Last Modified: Thu, 05 Sep 2024 07:42:45 GMT  
		Size: 92.5 MB (92474043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a6083498e5e52de35be3300f64c810282c18ff6879255b6378720276d76d1a`  
		Last Modified: Thu, 05 Sep 2024 07:42:43 GMT  
		Size: 9.9 KB (9930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd04c0ed00889aa9e26368884e0bd48ede8f4a6ed14ddca307709a24c3af240f`  
		Last Modified: Thu, 05 Sep 2024 07:42:43 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b801a3f962bec3cb9fdd7c1cb5ee1963c48530e15c77990ce0aabf1888e8ab3`  
		Last Modified: Thu, 05 Sep 2024 07:42:44 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02dab368fa0f51f5308062114c5ed169b1a79d5a8e59c5229b55175e22d3fbd`  
		Last Modified: Thu, 05 Sep 2024 07:42:44 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3bdfbe0e76470e2a530c9200034104e7e3c73d0d8ebe48dd2a5a200039c687c`  
		Last Modified: Thu, 05 Sep 2024 07:42:44 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:ff5905c56c0f51ae5c4a1730abf9f8afe09c9f482b2b611fde8e1a0686051d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6068253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbd838ab30608976cb187cc5e0b9b50e1c761db969bf124e9a737d52d867589`

```dockerfile
```

-	Layers:
	-	`sha256:2d4f4b80837fe1aa9bd21078f6c8ec52cdbe95cede634b441edccb53f0dc1d9c`  
		Last Modified: Thu, 05 Sep 2024 07:42:42 GMT  
		Size: 6.0 MB (6013917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32ab2a8e6c9419b3a37d3c1875ee35267d925565ee2d68c35270d2f35d4c4d07`  
		Last Modified: Thu, 05 Sep 2024 07:42:42 GMT  
		Size: 54.3 KB (54336 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:99623484d2e4972371a89e3a66e0983bb65179771773dc7569c3bdb95714f5ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141429143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34d40ef738c9e9e074f4227515aa0d1598906b7ca7c7c1045a8f748157a3aead`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:20:28 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_MAJOR=16
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_VERSION=16.4-1.pgdg110+1
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:20:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:20:28 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:20:28 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2b01cc9b32ef6de1409283ddcbd829b65619e9afccb9d845e9af6bd1be7682`  
		Last Modified: Thu, 05 Sep 2024 16:08:52 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d485dfa76d8a734e194bcb59e9ee5bb65a041a82c13828a230a1c91683a7fd`  
		Last Modified: Thu, 05 Sep 2024 16:08:53 GMT  
		Size: 4.3 MB (4312704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6040b61bcd643bc0d338f3e6058c46a5dac0014fdebdac5b925cc65ff559e5c4`  
		Last Modified: Thu, 05 Sep 2024 16:08:52 GMT  
		Size: 1.4 MB (1404108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656cf2221a1bacb5afca55670af2b9e25a3b9b85529b9f075f5d02924d81ab97`  
		Last Modified: Thu, 05 Sep 2024 16:08:53 GMT  
		Size: 8.0 MB (8044220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da18785bd70d991fdca6bd8d565be084603c5fd8faf6cdae863b104c12afabf`  
		Last Modified: Thu, 05 Sep 2024 16:08:53 GMT  
		Size: 1.0 MB (1026577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd478cc402fa0416b0b01d600dab85704795d3397553868789ae087c6378448`  
		Last Modified: Thu, 05 Sep 2024 16:08:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0278feac55966f4a0f947226fd7a64d6ac31b04b711b476f70d347a8b65fa9ac`  
		Last Modified: Thu, 05 Sep 2024 16:08:54 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef5244adee8fc029aadb89ec85c6eca5374989c4d6bca8f44837ef11ac8337e`  
		Last Modified: Thu, 05 Sep 2024 16:08:57 GMT  
		Size: 96.5 MB (96546401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb55f6f072ba4c15b8461273401ba1ecede3c73363af1b254492e9ce2043d665`  
		Last Modified: Thu, 05 Sep 2024 16:08:54 GMT  
		Size: 9.9 KB (9925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c510dd56415693ec8faf0dd241d604635a4e9f5c51588eaa25857afc42c000`  
		Last Modified: Thu, 05 Sep 2024 16:08:55 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57f446126fef378a82d05bb746fc24c7856b0af585dceb9f7cb5e717a0304c2`  
		Last Modified: Thu, 05 Sep 2024 16:08:55 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0914e61a3aed336840730df1e6ea62bfbf7f07a561a8cb25d2d58470521fad11`  
		Last Modified: Thu, 05 Sep 2024 16:08:55 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c58370d296281f2a302410e761a5ea330d2050f878494ff5a0f2e4104bba44`  
		Last Modified: Thu, 05 Sep 2024 16:08:55 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:44b2cd216af69943173a8af210d0091193b943968801851e6688c5457689c093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6057633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:669602c43ffa9e9cee24f809be04b135800713fb5b4e8a5d4c4db60bd78de5e1`

```dockerfile
```

-	Layers:
	-	`sha256:f32aa9f354a2cc977815a976bc0976954af6e46c1af3525bf1367f0f2bff8617`  
		Last Modified: Thu, 05 Sep 2024 16:08:53 GMT  
		Size: 6.0 MB (6003196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e04c016c3249798503be14bc00b81be202d307c9a642d6bea0a77912962c39f`  
		Last Modified: Thu, 05 Sep 2024 16:08:52 GMT  
		Size: 54.4 KB (54437 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:fe152877c3df99094fdea3a22775ba42d6df0a45c5c4834f2c9e089b690a3b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.8 MB (147771282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22037f1fb8f455c44443e476b100e1c911ba3482f9834f034c539ca79f4649b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:20:28 GMT
ADD file:9177ff00c3abd0afc64f577295a060d88f4daed1042f024f7cfcfcd8cb1da9b8 in / 
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_MAJOR=16
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_VERSION=16.4-1.pgdg110+1
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:20:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:20:28 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:20:28 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2e34c6adf259f6e5265d64b5a01b92c3cc93548f22be8c1ccc578b7e9babb30c`  
		Last Modified: Wed, 04 Sep 2024 22:48:51 GMT  
		Size: 32.4 MB (32413314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7324cbcf02cc3c966bb1e462301956bc10f53da58e5a1815eb0b77925c3657`  
		Last Modified: Thu, 05 Sep 2024 00:21:17 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b359351a7d6048dddbcc1796a0b1a13e4beaf0b5d66f649a16238f6d39b972d5`  
		Last Modified: Thu, 05 Sep 2024 00:21:17 GMT  
		Size: 4.7 MB (4719617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b9b3d88b4a40b4020d4086b357b5e2e335292b14c8854017325934a14663ac`  
		Last Modified: Thu, 05 Sep 2024 00:21:17 GMT  
		Size: 1.4 MB (1447732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa3953ef5cc7a70e3a244ce79d697bfbb4b52773d826a7fb31e05182bac59e2`  
		Last Modified: Thu, 05 Sep 2024 00:21:17 GMT  
		Size: 8.0 MB (8044274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723b6f633986c419583f3a0038d44a913edabe771895ab266e5f76bb5400a0aa`  
		Last Modified: Thu, 05 Sep 2024 00:21:18 GMT  
		Size: 1.0 MB (1028891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e334986206a66238aed2abf4fcfe65aac68c98a825de55a0f076206d4f6026ed`  
		Last Modified: Thu, 05 Sep 2024 00:19:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5bd27728b8fab97c9a7c924d7265aad4c1c7375541723156bbd2a955fb67c0`  
		Last Modified: Thu, 05 Sep 2024 00:21:18 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e6dcff34cc5079c32f74658f429e36b02ce921cf6c5cdee2543e3f4e1aa50c`  
		Last Modified: Thu, 05 Sep 2024 00:21:21 GMT  
		Size: 100.1 MB (100096695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322512917e12cc29ba0f1216e46f6b4892596ee12726d6d0fab604258f3d0305`  
		Last Modified: Thu, 05 Sep 2024 00:21:19 GMT  
		Size: 9.9 KB (9916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd17b5f2035ffb3725151764ad0846d9eaa36a89f2abd467e5fe3614ab460271`  
		Last Modified: Thu, 05 Sep 2024 00:21:19 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f067dc43cdae548e7a86025d5c4fe15aaebf787bc5899a99c9959f6b43d3c296`  
		Last Modified: Thu, 05 Sep 2024 00:21:17 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b1d7380ad74ff7f3fa9dbb70c163d8b312e467d63a1e86f7bc78ee72b3bdae`  
		Last Modified: Thu, 05 Sep 2024 00:21:20 GMT  
		Size: 5.4 KB (5425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76efc3d01674697e19070a013af5e560fb7ca3e09be2e8be8374cff2c821f946`  
		Last Modified: Thu, 05 Sep 2024 00:21:20 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:bea5a07fd88338138d5eb5d946bd88f3699a9541a9d0ad50b4672ce325164396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6065695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8f04ebd83b47f6a3eae72330976da5f66e577711bb5ab16f683c69e21c04c6`

```dockerfile
```

-	Layers:
	-	`sha256:1378d6172df380837cfab2414cc1742d94d09497edc2db231722a83a269c1629`  
		Last Modified: Thu, 05 Sep 2024 00:21:17 GMT  
		Size: 6.0 MB (6011595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f82d4e718c201fb47ca7e479a58185fdaec1df2699a0a2d18fb5a1ae58cee7c`  
		Last Modified: Thu, 05 Sep 2024 00:21:17 GMT  
		Size: 54.1 KB (54100 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bullseye` - linux; mips64le

```console
$ docker pull postgres@sha256:db6db2f60c5e7481b26ccb8345545e972cbbaa79358b6eb29715c124fbbf31bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139376589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c7858e7df4fec07bcd17471b9484292971ca70a0a7aaee0161497ea0414860e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:20:28 GMT
ADD file:d4b92daa2701c7af077c4c89b2b1f5a97cfc6389c09e049b3bdaa36454653bbd in / 
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_MAJOR=16
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_VERSION=16.4-1.pgdg110+1
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:20:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:20:28 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:20:28 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:15b8bd5d9ec350cbe23bbccddd5284b3cc9139e037500a63a02025354518d5c8`  
		Last Modified: Tue, 13 Aug 2024 00:23:52 GMT  
		Size: 29.6 MB (29646095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8756e4bf324c450320a08e19331208ae564f36a011174c89af8cb49a53f60c21`  
		Last Modified: Wed, 14 Aug 2024 06:08:12 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80efd2830b090c4732a7cdc9cc81ab571e02a44d3d1437948c71657571e9925a`  
		Last Modified: Wed, 14 Aug 2024 06:08:12 GMT  
		Size: 4.3 MB (4308324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc775a138ac985753fc78bfa32a171a019ed026a41738516b80442dcb0bf0b18`  
		Last Modified: Wed, 14 Aug 2024 06:08:12 GMT  
		Size: 1.4 MB (1359373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd6a47bae0895d43a00e4068c39d18d5630c457b64a3370f0f96284bb42423d`  
		Last Modified: Wed, 14 Aug 2024 06:08:13 GMT  
		Size: 8.0 MB (8044717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30aae077fa3abd7258a46d4e7c2e634a6f65e59687ca05718c7c1736b0a65ce9`  
		Last Modified: Wed, 14 Aug 2024 06:08:13 GMT  
		Size: 1.1 MB (1090275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb13c1ba77f878e041e12823e8b6dc6ea9d93bd7ecab70a97d379b65f470109`  
		Last Modified: Wed, 14 Aug 2024 06:08:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a98d98bab3c64f344d2e50547954cbd619d9e47596137358497a0ae3457d01`  
		Last Modified: Wed, 14 Aug 2024 06:08:13 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1923a6a8fab6ffeacb325fecb474b65267e9b21478961809dbe7e7df14887201`  
		Last Modified: Wed, 14 Aug 2024 08:25:35 GMT  
		Size: 94.9 MB (94907039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a6377183eba665fbd6089aba5523e72e08592af334159716521edecc204ba5`  
		Last Modified: Wed, 14 Aug 2024 08:25:26 GMT  
		Size: 9.9 KB (9921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762a6754b4ecac08cbacb0037dbd39bd974c7d2a662729e575ac1255ec4f62c0`  
		Last Modified: Wed, 14 Aug 2024 08:25:26 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9af9e6a56d8a736406fedb6b08b75f71e9530da8cad3f73767c4f0a6eb436e4`  
		Last Modified: Wed, 14 Aug 2024 08:25:26 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445d23d1b842059a8a0ce5fc77dde6d8f529a56735b4a668897ec0cecef3f0d4`  
		Last Modified: Wed, 14 Aug 2024 08:25:27 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acc682edefac19507726c3298b37405993c6e6a095f2a5ba6dbbfe085007793`  
		Last Modified: Wed, 14 Aug 2024 08:25:27 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:a341a0afed8d59def871b844ed43177c4da298f5f33e0cab15b9d55a6a2b8bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 KB (54001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8848d38d8a62de1420e21a94686de5c2ac33312866a921feb8bd25b957d907a`

```dockerfile
```

-	Layers:
	-	`sha256:370610a8b754bff77297f8523d08b4a62c896808dc33448b9a8eb7caf89f3cbd`  
		Last Modified: Wed, 14 Aug 2024 08:25:26 GMT  
		Size: 54.0 KB (54001 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bullseye` - linux; ppc64le

```console
$ docker pull postgres@sha256:f433b26aa365c8f710a9ea4f7a35b9ffd05e0e98954694c15c5e01c5219563f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (156020493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdcd96d1f4103724b909074e1c8791a1141c09008d67b97432e16561552b1d7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:20:28 GMT
ADD file:1dd1fe717176cf8c20fe5b4fd39ce7f79d39d2aec08c436f3ade914e61d5d17b in / 
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_MAJOR=16
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_VERSION=16.4-1.pgdg110+1
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:20:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:20:28 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:20:28 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:713e780b10a0e4075bf4372f97f67566ba30b5cc32dd0bf565177796f5503d7b`  
		Last Modified: Wed, 04 Sep 2024 22:30:58 GMT  
		Size: 35.3 MB (35299274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb03920874bebaac0313c066da6e1292d051b9bdbd1123d8de0e41a668ccb72e`  
		Last Modified: Thu, 05 Sep 2024 03:12:11 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac3e8856a34a137abae04f17f55e1b3d6a2886709cab091647f4fef7897631a`  
		Last Modified: Thu, 05 Sep 2024 03:12:12 GMT  
		Size: 5.1 MB (5137806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dadd44eafb3401af71118033b6cb1bb2e472a4eab258f5ebe20b1b035cbf2d4b`  
		Last Modified: Thu, 05 Sep 2024 03:12:12 GMT  
		Size: 1.4 MB (1393635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae1bc84e0e01888ba16e6babb838cd471e00ecaf928ea1e7beef6406a4b936f`  
		Last Modified: Thu, 05 Sep 2024 03:12:12 GMT  
		Size: 8.0 MB (8044494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db835f9f21dfc6fca2b1aa1d9ed5199d68a03bf4a8742ffe7bc912bee54c791`  
		Last Modified: Thu, 05 Sep 2024 03:12:13 GMT  
		Size: 1.2 MB (1197541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f8cb26e1532c0e800af9f9dd22391dda36b40c2d8934633184af9cea8decbe`  
		Last Modified: Thu, 05 Sep 2024 03:12:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a67336446e997e452360d45b8b18e766a00beff49071b72280c2101482cb427`  
		Last Modified: Thu, 05 Sep 2024 03:12:13 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345f4c80e6de993238f0bc30a7ca3356feb295e4950f0e1645bc926a08076ef3`  
		Last Modified: Thu, 05 Sep 2024 03:15:12 GMT  
		Size: 104.9 MB (104926985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af015aa43cd04e0e476ae4b8fa5112154bd7de1deefc0b7230e46fd60fab6e47`  
		Last Modified: Thu, 05 Sep 2024 03:15:09 GMT  
		Size: 9.9 KB (9919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363134152c2148729a4e4c90795cbf115c1a96d5f0458f59268397b128f41bc3`  
		Last Modified: Thu, 05 Sep 2024 03:15:09 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21cf7d0ed465fdc01582ba1c32fa562bdbf41d6d461b09d2d1ac70407b99d92`  
		Last Modified: Thu, 05 Sep 2024 03:15:09 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ea0fa359083b24e417ca035eece6973524b560cfa2240f21688933f6380ec6a`  
		Last Modified: Thu, 05 Sep 2024 03:15:10 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff0552aeef3ec3fe6b477111c1b405d8db277f0a849495d17f363a083bfedf7`  
		Last Modified: Thu, 05 Sep 2024 03:15:10 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:ca6c79b4bb228097ebcac862d2cb772a3c570e7f1e42fd2be145d6769c224f98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6058231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993b53ce1db0cce26cd9654ff9dbddf766176f541176dd038b7e10102afd22c3`

```dockerfile
```

-	Layers:
	-	`sha256:2978e8f5a15a3ba51697d9b474f2123201f70376465e2e3ce3ef67b802a16350`  
		Last Modified: Thu, 05 Sep 2024 03:15:09 GMT  
		Size: 6.0 MB (6004032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95a3dcffcfae205b4953ac85ce4906ae6671bca3e408a827877278690587c03d`  
		Last Modified: Thu, 05 Sep 2024 03:15:08 GMT  
		Size: 54.2 KB (54199 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bullseye` - linux; s390x

```console
$ docker pull postgres@sha256:e9789a27140da231431a09a3d7a89c09e3a89b3a2c516ce56fd95fd65c0ba774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149425714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1518a0e47b9cfd21280685a4cba8afd985549ef511312aa3fe7c002866f48701`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:20:28 GMT
ADD file:301629b0d8ae489e6705aa09fa33dae1617ec0882c0376c2a9b5ec18197190f0 in / 
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_MAJOR=16
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_VERSION=16.4-1.pgdg110+1
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:20:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:20:28 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:20:28 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ffc4ad031bdde6abf6ae0c4570ad3e4d72f747634c83ee773ce85b5582490bad`  
		Last Modified: Wed, 04 Sep 2024 21:48:09 GMT  
		Size: 29.7 MB (29663447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa74617b6306779ebd9fe52758d2400e81a4c82d80b8c0dd2d87dc02c9187ef`  
		Last Modified: Thu, 05 Sep 2024 05:05:36 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95d1b5d7b1f1d66b6dcf47f49733f151a45df9fc346b7fb40c378aebc629f4a`  
		Last Modified: Thu, 05 Sep 2024 05:05:36 GMT  
		Size: 4.2 MB (4200347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69982ab84b3d7a587c8efaadc9f9082799de1c9183067e379dfb94e9a77af86`  
		Last Modified: Thu, 05 Sep 2024 05:05:36 GMT  
		Size: 1.4 MB (1437973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0ab37ef9cd03d0f26514d5b7d51f3ff5b8c87dd84895233863040b15a688dc`  
		Last Modified: Thu, 05 Sep 2024 05:05:37 GMT  
		Size: 8.1 MB (8098858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29c31483b2b4e9ac50de84964c4b8c92a50c4939ac41224cd8fbde23826d786`  
		Last Modified: Thu, 05 Sep 2024 05:05:37 GMT  
		Size: 1.0 MB (1015252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41e8be03ee08a804c131ea8a9344f92b2d99929f458b23e9745b939edcb267a`  
		Last Modified: Thu, 05 Sep 2024 05:05:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ddf8031b775ba82af170e0d5e20c4cf9b27c8e7e983ce8e74a142542dffa1a7`  
		Last Modified: Thu, 05 Sep 2024 05:05:37 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f3f9e743d87eb16dbf4231f623cf523a38d92f58eb697d35746f8bae3c73cd`  
		Last Modified: Thu, 05 Sep 2024 05:07:55 GMT  
		Size: 105.0 MB (104989078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485e282c51fa0a01f8cf63247dc34a88973dc04cb54497bd7d8930c861883444`  
		Last Modified: Thu, 05 Sep 2024 05:07:52 GMT  
		Size: 9.9 KB (9921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b019387b182c9a4b49dadda80e1bc3676dae2a847bffc2a686c0fc437c2fd646`  
		Last Modified: Thu, 05 Sep 2024 05:07:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65dba47ec90eaa278e2649ffaca97d63d4998630dbeafba7077f746fd40dcc7c`  
		Last Modified: Thu, 05 Sep 2024 05:07:52 GMT  
		Size: 165.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1851b8cda5bc04f05f9fd2068388db69c6dace12f788aaf2695e6aa2f27bb7f`  
		Last Modified: Thu, 05 Sep 2024 05:07:53 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626333fac1121528e9460eaaa77a5aa95ae715b6e64fac9294933daa7f4ecbf2`  
		Last Modified: Thu, 05 Sep 2024 05:07:53 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:cb3278b7435c17e1efd0cd9ee640c400193db65914f6634112759edad51be100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6050015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d9e81219cb47819e5ee69a341702f511d071f2480e932a87f2a4f1c5f1394d`

```dockerfile
```

-	Layers:
	-	`sha256:76cccf0003ae2f38d37d6bf7b23cb9d96d8ce7e01338a8ddd38156394c08a7fd`  
		Last Modified: Thu, 05 Sep 2024 05:07:52 GMT  
		Size: 6.0 MB (5995871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae3423462f6dcd629dadb10ed628036db1e2126dbca5adfb5b3a736cff85e68d`  
		Last Modified: Thu, 05 Sep 2024 05:07:52 GMT  
		Size: 54.1 KB (54144 bytes)  
		MIME: application/vnd.in-toto+json
