## `postgres:12-bookworm`

```console
$ docker pull postgres@sha256:390e7fc48f59403666da257b45b132c8e3e35aeb2d2df291e91e3e18336eaee3
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
$ docker pull postgres@sha256:1d9e2e7c7e8944f1cff1aced43c1e6371d239d7c2e40a3e6a71abaab5d1f060a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.5 MB (148451778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c90280ff3e1f597e86d58caf32968440ff8f01346077ea6064eba3015f46c4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:02:23 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 09 May 2024 18:02:23 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV PG_MAJOR=12
# Thu, 09 May 2024 18:02:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Thu, 09 May 2024 18:02:23 GMT
ENV PG_VERSION=12.19-1.pgdg120+1
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:02:23 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:02:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:02:23 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:02:23 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:02:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6fd2e12bb178bfd25de077c3159c09efc573ff9212fc0d98337dcb5c6452617`  
		Last Modified: Thu, 13 Jun 2024 18:30:11 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ea6cd19b24cc265f079861d69ffa7a572d743b644388dea6f59d57063d7a305`  
		Last Modified: Thu, 13 Jun 2024 18:30:12 GMT  
		Size: 4.5 MB (4533665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2acef64df177251f89885a9dd9be41f14d8c607afb6544498259c1e5053c03a`  
		Last Modified: Thu, 13 Jun 2024 18:30:12 GMT  
		Size: 1.4 MB (1449904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce3fd80098eb637fed88efa0f5b18905a890a7ef2422ac2dd617816212b400b`  
		Last Modified: Thu, 13 Jun 2024 18:30:13 GMT  
		Size: 8.1 MB (8068871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709014c13463f58d02273944dfeff0d6e2cd462790baf8b2a227e18b383de034`  
		Last Modified: Thu, 13 Jun 2024 18:30:13 GMT  
		Size: 1.2 MB (1196076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5262396c7d64c1617de4bdaf6f4593a14ccf204c07fffc4a66e8a8bdd0e1e9e7`  
		Last Modified: Thu, 13 Jun 2024 18:30:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c8dd17d179f89efeab07cf6e205cf9e7cdbbc13313b0c4516ee6499e0a2e45`  
		Last Modified: Thu, 13 Jun 2024 18:30:14 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464684d6f1792e7c78002c1e54e828b2d4fe7ec97c328e8c4246ae163fff86b9`  
		Last Modified: Thu, 13 Jun 2024 18:30:17 GMT  
		Size: 104.0 MB (104033491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8081b1ab2727aba19e3465ac042b5635377bda09bd9fceb67002e4c1516a8da`  
		Last Modified: Thu, 13 Jun 2024 18:30:14 GMT  
		Size: 9.0 KB (9017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0d79b15de9d63169fab53b9ea4c2a335132c8224dbe92df870d470a43569b4`  
		Last Modified: Thu, 13 Jun 2024 18:30:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d079fd838ef51a19d7d2b6f151f7327274dfd4001a66abf9503854922f26bc9`  
		Last Modified: Thu, 13 Jun 2024 18:30:15 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bba15418729563f628c301696562449abbe76e151b81dec671578610331f7d2`  
		Last Modified: Thu, 13 Jun 2024 18:30:15 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19869ced22ecf32a84b9a170b3d9536455fbdd5aaf542564ab7dc0ab81fe3003`  
		Last Modified: Thu, 13 Jun 2024 18:30:16 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:ba845ee00743ec07f6e1bf5a311e39dcfd2a04f5fd49bb12ca5960dc53a6c507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5624696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c35b5c9c332dd073b569b30dc45f133d4c8738d3633a0e2c670fdbab4f13153`

```dockerfile
```

-	Layers:
	-	`sha256:8c73590d87916f050e17472f8c9c854806def249940325b35b79a64290aafce5`  
		Last Modified: Thu, 13 Jun 2024 18:30:12 GMT  
		Size: 5.6 MB (5570172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:893c76cc030fc9f2cee8f536f5221082504ce27d3f565a00451699a382feb170`  
		Last Modified: Thu, 13 Jun 2024 18:30:12 GMT  
		Size: 54.5 KB (54524 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:b2a73aa104fab8a717522b62d7cac2bcf9f2dd38ebb31be53d6ff1afaf168f8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141182716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddfb06faec5b19b0e77a1e30a3baa50c227104c1aefecd21630c545ad3429714`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:02:23 GMT
ADD file:9ca492786bcb3648d90c47fc2dba3c8239eea7a0689f6a17ee25a9f5129aabd5 in / 
# Thu, 09 May 2024 18:02:23 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV PG_MAJOR=12
# Thu, 09 May 2024 18:02:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Thu, 09 May 2024 18:02:23 GMT
ENV PG_VERSION=12.19-1.pgdg120+1
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:02:23 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:02:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:02:23 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:02:23 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:02:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d50583018de0ccbb239bef29dd375ae0ea018644d67a37b4fc29bec08b3b1a33`  
		Last Modified: Thu, 13 Jun 2024 00:51:38 GMT  
		Size: 26.9 MB (26909975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76f93fe24faf9bdd2823e7ed0fa9bf1ae89c6d82d81309c0044fbd05c272b8b`  
		Last Modified: Thu, 13 Jun 2024 20:27:17 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2160d7118cc9f8e23b3033ea807d4e87947c45bfb8bcea73028027aa765329`  
		Last Modified: Thu, 13 Jun 2024 20:27:18 GMT  
		Size: 4.2 MB (4150952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5efce1143a2d44abdd1810dd3dfeb14c4ee36f79dc41476601665c7c40a2f54`  
		Last Modified: Thu, 13 Jun 2024 20:27:18 GMT  
		Size: 1.4 MB (1427070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e623323d67613018c639686712853eb77cd588d64ced98a25fd20512f43b1e6`  
		Last Modified: Thu, 13 Jun 2024 20:27:18 GMT  
		Size: 8.1 MB (8068972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee6b3c3492fbdef9666e4379393f2c59aff2ab2278dcc38c611ebe869696083`  
		Last Modified: Thu, 13 Jun 2024 20:27:19 GMT  
		Size: 1.2 MB (1194853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58d2e67789ab63ba29790eec6bd56fe19d33551de322ceaa5f0bbf489a10b4f`  
		Last Modified: Thu, 13 Jun 2024 20:27:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e906e2ab7c56d77757417a3a48d2ba73236b668f3ef3ffe2788196fea729bb`  
		Last Modified: Thu, 13 Jun 2024 20:27:19 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df59284993a96a118098652a35b2ed33ff1c7636102b908be65061d5bb8d6c67`  
		Last Modified: Thu, 13 Jun 2024 23:02:48 GMT  
		Size: 99.4 MB (99411541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58ca09f6efdde784444387be6bc60c6fbe125e9765260fe7cb0ca5c67820f03`  
		Last Modified: Thu, 13 Jun 2024 23:02:44 GMT  
		Size: 9.0 KB (9024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46aace2ef153296920b80d26180593f3821c98312091372b755b7c7915a31f6d`  
		Last Modified: Thu, 13 Jun 2024 23:02:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3ccfb59287c54e470ada55319b1ff7eae7ed51e1cc07787166d65973931c87`  
		Last Modified: Thu, 13 Jun 2024 23:02:45 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f1ab959a46500f0f31cb4c7373f52c82c998983768d0521d81dc85b747646b`  
		Last Modified: Thu, 13 Jun 2024 23:02:46 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440d97fca7675edc0481d6d7a1b74bea05996fac779a4d4aa1a764fcec9aaf0a`  
		Last Modified: Thu, 13 Jun 2024 23:02:46 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:059e7fa189b1884699c1e9a2b5f40aebcccb7644b42088af297413d32d4e7495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5638005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f93d6578643b17548736c85dccc997754b458a6489ab0bfe8f9513eb589ce4`

```dockerfile
```

-	Layers:
	-	`sha256:25c5d5cb8ee2569c48d4f6a936d6935fbb45229cdf9dbdbff302b19f3ebb3d17`  
		Last Modified: Thu, 13 Jun 2024 23:02:45 GMT  
		Size: 5.6 MB (5583274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed59ffedc30ba2230b5963b04a98286ffeabd645a964199afb5bd42e8801502e`  
		Last Modified: Thu, 13 Jun 2024 23:02:44 GMT  
		Size: 54.7 KB (54731 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:7e9a8d6698861995fb03c4ff1236231caab8db5a4e80dbc7a00f4954452f3eab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (136030412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a87bab7e46a9ec3db7102afa8060634b220b7e6bb87b60fcc67482a6d35a12ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:02:23 GMT
ADD file:4c737c0a5e5b59fcbe2bc42dca815263159a1e1d16789ebeee086933aac4649a in / 
# Thu, 09 May 2024 18:02:23 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV PG_MAJOR=12
# Thu, 09 May 2024 18:02:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Thu, 09 May 2024 18:02:23 GMT
ENV PG_VERSION=12.19-1.pgdg120+1
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:02:23 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:02:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:02:23 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:02:23 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:02:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:12af5edb53b85c10582c3e3d437561cc626437f48928a30456a99941d87706e3`  
		Last Modified: Thu, 13 Jun 2024 01:01:38 GMT  
		Size: 24.7 MB (24740215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493051253236caea97f219fd70aa5f22f8b46248ff1d3c3d3188d73ce0784a40`  
		Last Modified: Fri, 14 Jun 2024 01:16:01 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6804256b124e139d9f0115e1d42291cc23b80dce76de35fd5698c162eaf1dbf0`  
		Last Modified: Fri, 14 Jun 2024 01:16:01 GMT  
		Size: 3.7 MB (3742521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b531feac03289045c14b775e7e96c3ede9f3a2d05e3b6dd1e733009cf1bbb62`  
		Last Modified: Fri, 14 Jun 2024 01:16:01 GMT  
		Size: 1.4 MB (1417097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66c7bb29e6b93b045ad24872cfa94249282a9726a9f006f38918a121c5ba9be`  
		Last Modified: Fri, 14 Jun 2024 01:16:02 GMT  
		Size: 8.1 MB (8068841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b345cb504203c27252fd77886ea537ccbba6a85470442aae2a7829f01b742d27`  
		Last Modified: Fri, 14 Jun 2024 01:16:02 GMT  
		Size: 1.1 MB (1066956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d104bf8bcc118bb31c29d3d8a68c778d2cb3ff3581269130a6cdcbe82a263ed7`  
		Last Modified: Fri, 14 Jun 2024 01:16:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe06d964e32afda897c71c4829462b2d98aa14cf05e4ce8a1821876e9adb65c`  
		Last Modified: Fri, 14 Jun 2024 01:16:02 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fea4d8d112ca039943e326b8e9dfebf3a819a4c8ca66d8d9f614b8dad6cfcf5`  
		Last Modified: Fri, 14 Jun 2024 03:40:29 GMT  
		Size: 97.0 MB (96975429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e151c1bf6a14be5f28ce9282e2d004de70ecb5446d35cfc79ba0861ce28ac8e`  
		Last Modified: Fri, 14 Jun 2024 03:40:26 GMT  
		Size: 9.0 KB (9021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029bca0fcaea87356bd888bcc5b1ce3b608db3c025301cb7e04ea1627040d064`  
		Last Modified: Fri, 14 Jun 2024 03:40:26 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f131a3dd3dd23c615f357b18bcc8c2671d594c9370592b3c4cb9533de74d045a`  
		Last Modified: Fri, 14 Jun 2024 03:40:26 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2628c8eb247884a5d2713deff33f4a9c9ddcf70e28a05b46e15b51d40af0a6a4`  
		Last Modified: Fri, 14 Jun 2024 03:40:27 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e612318d89609e309ff1862aa4568a878edef0486d91c50436c958f6c618ee81`  
		Last Modified: Fri, 14 Jun 2024 03:40:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:83c642cbb848fd7ed6d85254d953d1d5bad545b5376b92364d45bec209c54b65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5637817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9375fde89985f2e024968812a37eda6e431496ee0de04bbcdf16f380d5cff69`

```dockerfile
```

-	Layers:
	-	`sha256:e25275f015a204537fb457f47e933885b6377c19b474090081417d1432155095`  
		Last Modified: Fri, 14 Jun 2024 03:40:26 GMT  
		Size: 5.6 MB (5583086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88cc73db0531371bbd07862568829c9459a8ad172bf42a6e604641ebbfc4f91b`  
		Last Modified: Fri, 14 Jun 2024 03:40:26 GMT  
		Size: 54.7 KB (54731 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:597e6b079fdf64aac94e8bbe55957547fb077c66648954a24558525dd977ef73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.7 MB (146688961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a52fa1ec854b319783506991ebbfbff79bc4f8a391cbc09be73809256fffe00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:02:23 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Thu, 09 May 2024 18:02:23 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV PG_MAJOR=12
# Thu, 09 May 2024 18:02:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Thu, 09 May 2024 18:02:23 GMT
ENV PG_VERSION=12.19-1.pgdg120+1
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:02:23 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:02:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:02:23 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:02:23 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:02:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059b5c43db4127d3c84a4caee54092e336d3ba62e208c915e1644fb73a7c5e2f`  
		Last Modified: Fri, 14 Jun 2024 00:40:58 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac4aa6c99e9f11007d4c9ef96a1b0dd6aa1ba9b32bb8f1eed1577047f513928`  
		Last Modified: Fri, 14 Jun 2024 00:40:58 GMT  
		Size: 4.5 MB (4499134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f695f6dafe22ec09a8d465915c3f2df31da965a38406fe775765c9a6d6e5af46`  
		Last Modified: Fri, 14 Jun 2024 00:40:58 GMT  
		Size: 1.4 MB (1382260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3531e6d72caa83e1e23ae04b0c519b1174a47e2c737f6f4bf8e2822a9acae84c`  
		Last Modified: Fri, 14 Jun 2024 00:40:59 GMT  
		Size: 8.1 MB (8068931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8460f5c0f01056e728f9f916df72baeae6eb09bf8e6c86f8964a9822b8008cb5`  
		Last Modified: Fri, 14 Jun 2024 00:40:59 GMT  
		Size: 1.1 MB (1108679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c419f8ddd2fbd2e547a8b11791240d264a925a69a36bc442567489c2755fd853`  
		Last Modified: Fri, 14 Jun 2024 00:40:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54f6c55c74f6700f1cea329574b215d9662b08548c98081dabb64ac7caffaf8`  
		Last Modified: Fri, 14 Jun 2024 00:40:59 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414f2433a842f387ad8c9102e2feed644f1b67086b02abbfb49b965eb1cfa887`  
		Last Modified: Fri, 14 Jun 2024 01:01:08 GMT  
		Size: 102.4 MB (102430949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685dc4594efcb39fc785f3ef6d8aa83df3e0e5e351fa1d1bf087588132f3f861`  
		Last Modified: Fri, 14 Jun 2024 01:01:05 GMT  
		Size: 9.0 KB (9018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8589575005dd40a308fa69c31fedef440881b386ef4df3a85a019b9b2646db2`  
		Last Modified: Fri, 14 Jun 2024 01:01:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34aeee549ee99e37300d012792b810c0793c99aa11a58e51f2d1587447f0846`  
		Last Modified: Fri, 14 Jun 2024 01:01:05 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95867d3b307d48bf96c9b29fbed083eb04435774c7ce8adafa2964d71aef64bd`  
		Last Modified: Fri, 14 Jun 2024 01:01:06 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5080f3ceef303778b81a08569b37aa00793548d427d2a65b61197b9e9df108`  
		Last Modified: Fri, 14 Jun 2024 01:01:07 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:aa0f2f962e7e68a0af584991b890563f2b20c0c0265d4559c7570a38f46177dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5631346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19dba7fc1bcc4f457951ec214e04a5d8d4c04ecd20c3fcc3eb46125c2a93039e`

```dockerfile
```

-	Layers:
	-	`sha256:f1fefb1da3dd8339ffab4ae3f7b69d63112637effca86d5515e36dd3e031eaf1`  
		Last Modified: Fri, 14 Jun 2024 01:01:05 GMT  
		Size: 5.6 MB (5576513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:364991f19ea8309c66f9e5e4f934a14b9be46270b7fc984192e7dbfda04ac729`  
		Last Modified: Fri, 14 Jun 2024 01:01:05 GMT  
		Size: 54.8 KB (54833 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:3ff7376a2b5661a34063bd2ab4986733bf325748f7872759b444806172e5fe4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156383925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6eaef814b6568c400aef27281d8d1b1ca04853eb53c3c8f94aeb7678108498`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:02:23 GMT
ADD file:d68e899424fb360eaf2a6f2f35e06dc87f5841c13cce853d3e0710f969583d10 in / 
# Thu, 09 May 2024 18:02:23 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV PG_MAJOR=12
# Thu, 09 May 2024 18:02:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Thu, 09 May 2024 18:02:23 GMT
ENV PG_VERSION=12.19-1.pgdg120+1
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:02:23 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:02:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:02:23 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:02:23 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:02:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7adb06274fdba91ff3ec0873bc068b9a785bd5e3ff48e6f1d9e855048f1f0a66`  
		Last Modified: Thu, 13 Jun 2024 00:43:23 GMT  
		Size: 30.2 MB (30162659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb6895722a221b732a42adccea75ca485c1516998105ceabe59c6ba647d4b5f`  
		Last Modified: Thu, 13 Jun 2024 02:12:28 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cdc92f511ab77c37ae58dcbd0d17c351d9d660012e0d719d6d16cb6061e50f`  
		Last Modified: Thu, 13 Jun 2024 02:12:28 GMT  
		Size: 5.0 MB (4965085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2ba71655da750dfc5252f6db06e96499b7716fb266afe423912a99d8498f8a`  
		Last Modified: Thu, 13 Jun 2024 02:12:28 GMT  
		Size: 1.4 MB (1425617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de66ffb3d2396ae6f617d4527aa783f8c3913251e5966cdff0ea20f8e705f0d2`  
		Last Modified: Thu, 13 Jun 2024 02:12:29 GMT  
		Size: 8.1 MB (8068911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01d5a7ea14d02e211312704d500386db76ac1d22e6f23bf43ee40a79c73d192`  
		Last Modified: Thu, 13 Jun 2024 02:12:29 GMT  
		Size: 1.1 MB (1137166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47449466a52686cd91b89f1bc9017c124bbab6d417607d2a7df81e1123b970a`  
		Last Modified: Thu, 13 Jun 2024 02:12:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad215e446f0744bdba6d05d3b7af21052e57c9c41a765878b7ea4b41b32b336`  
		Last Modified: Thu, 13 Jun 2024 02:12:29 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e66eaf23625093105f520a3d7b33749cac6c78c54fe333d81fe659ffb5ebc7d`  
		Last Modified: Thu, 13 Jun 2024 02:12:32 GMT  
		Size: 110.6 MB (110605142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f0d176bae3080e6e504d867d26db8f07a2d67e5079a03e470aac90287cfe20`  
		Last Modified: Thu, 13 Jun 2024 02:12:30 GMT  
		Size: 9.0 KB (9022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96cc07e0f986bcd6ff8dd2cf09fffe4e5ba865bb9d15af113ed7b8a554b568da`  
		Last Modified: Thu, 13 Jun 2024 02:12:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e9348232a5db4c77aaad4454afff72abc7a9004e2b58a2414c855a254494e8`  
		Last Modified: Thu, 13 Jun 2024 02:12:30 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977d3e1544a345dfbf266fd378d2e3d83d906095ed015608ee6c00e5945e77b6`  
		Last Modified: Thu, 13 Jun 2024 02:12:31 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadcfd97fbe9918229548f8778284964090b303d223d30bffa43e9e3364cc447`  
		Last Modified: Thu, 13 Jun 2024 02:12:31 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:200058091f2b7c144a746768a8a96f19bf6cb421363c6d035ebc11d2d9f80095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5635800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee02cb2127de5c823e5d02087bfc9a8050702b9e32929d91de534873335d3f25`

```dockerfile
```

-	Layers:
	-	`sha256:ea7a02898b77026f0cf2190b50a891d433e20cf0b29dfc723fa9d00cd73fec67`  
		Last Modified: Thu, 13 Jun 2024 02:12:28 GMT  
		Size: 5.6 MB (5581327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f4f5819dd7e2540ec1ce6601ef3cfe46d5b5f526f596b7e0742f8c9db271dd8`  
		Last Modified: Thu, 13 Jun 2024 02:12:27 GMT  
		Size: 54.5 KB (54473 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:748b163bc85aa5ab93a6c706ded13b9b61d0e45faf286306098dcb2755b79c53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.9 MB (143915931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c3683b2e6588d4bdb78921f01267228b0e7457b48d40ac985c5751af690a9cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:02:23 GMT
ADD file:a92da94a28279478b2eae11dcdcd2913fc06af02498a5515cc3f288668d74e43 in / 
# Thu, 09 May 2024 18:02:23 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV PG_MAJOR=12
# Thu, 09 May 2024 18:02:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Thu, 09 May 2024 18:02:23 GMT
ENV PG_VERSION=12.19-1.pgdg120+1
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:02:23 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:02:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:02:23 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:02:23 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:02:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6ccc6628d3cdcda935b3b60cb54fa578d669965454d9cf39de3df9c1276132b7`  
		Last Modified: Tue, 14 May 2024 01:22:19 GMT  
		Size: 29.1 MB (29143688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca7ca5be5bd0a7b12cf1de9bdbbb595db188733fdb7c12d2154117a760a408e`  
		Last Modified: Wed, 15 May 2024 13:11:04 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e909d43c3f6bdd4be1ba36770e0ed624351d0416a8ca74a6f639f311e9054b6`  
		Last Modified: Wed, 15 May 2024 13:11:05 GMT  
		Size: 4.5 MB (4475045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a15af61ea75ceda9589ef7d5f9058d35d8a3965118622206da86a87ba21618`  
		Last Modified: Wed, 15 May 2024 13:11:05 GMT  
		Size: 1.3 MB (1337094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe00d0ac5956310274d2985b0a3c77af877b3779a2c6240cf89586720dc4bbc`  
		Last Modified: Wed, 15 May 2024 13:11:06 GMT  
		Size: 8.1 MB (8069092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571b3cda5307aee2b09abd52b1952421399ecf3a6589465b061b131a6416243e`  
		Last Modified: Wed, 15 May 2024 13:11:06 GMT  
		Size: 1.2 MB (1182602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56572b0970ce5c953a09028442aa0d32390dc0b2f149602322aec52bb677820a`  
		Last Modified: Wed, 15 May 2024 13:11:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13558ebe6fc60c64a9c3e74bda614b4c77fbb8d003658db7b01d28101eabd500`  
		Last Modified: Wed, 15 May 2024 13:11:06 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88bca10f6650ebbcfbdc1e333666d445236f901fa9ebeb13432d7fa119d2a18a`  
		Last Modified: Wed, 15 May 2024 15:17:03 GMT  
		Size: 99.7 MB (99689052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f99fa9ef8daef0a728a0a97bdefbee5252f7a0c5cb6544d44d0c10c784c7a6c`  
		Last Modified: Wed, 15 May 2024 15:16:53 GMT  
		Size: 9.0 KB (9028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d3c4d8c9aadbd7b9e27335df3a2193ba72fa618ada8676b8496f67f698859a`  
		Last Modified: Wed, 15 May 2024 15:16:53 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6042ad977a08138ef10b5a61ed45d404c3cee4fd5b01a3dac0a116b1e6a7c63e`  
		Last Modified: Wed, 15 May 2024 15:16:53 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216a9a6a0869ddb0aefef8392f5a8c474c1514aeb95eb8769ffd09fbe15bccf1`  
		Last Modified: Wed, 15 May 2024 15:16:54 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742ccdb7ef24280b9a699359184be7e328569b8f6ec07850d9e55b6178d01768`  
		Last Modified: Wed, 15 May 2024 15:16:54 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:b210cf0292bec80f7978dc1dcd3c665b968d90d050c9cdb9bdd142212ccd05b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 KB (54340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bce20aeb63f8d6c7fed0dcb7c236185bf61562385f81db3462e4adc9ee07f2a`

```dockerfile
```

-	Layers:
	-	`sha256:6cdce29b8cb81efb64a9fcf2bb1aaaf322cb7a2d8d041e917abfb00833627455`  
		Last Modified: Wed, 15 May 2024 15:16:52 GMT  
		Size: 54.3 KB (54340 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:734a881dd793d6e4fac8b6c66df846312cbcfc6beae2499c240a71df9e858e6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160419376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b6aeb3d4eff96f9f93bc8d5ecde78435f5530ba0c28c05276ce66d2d26f62c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:02:23 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Thu, 09 May 2024 18:02:23 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV PG_MAJOR=12
# Thu, 09 May 2024 18:02:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Thu, 09 May 2024 18:02:23 GMT
ENV PG_VERSION=12.19-1.pgdg120+1
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:02:23 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:02:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:02:23 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:02:23 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:02:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679533ebd7a290ad3f9e86a947131de8ce2263568b3b2f9dce2426af3c1d9d71`  
		Last Modified: Tue, 14 May 2024 15:38:31 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cc75436997df176c438cc3c32f068ef7ef32a430fe088f60f3b14b8799d027`  
		Last Modified: Tue, 14 May 2024 15:38:32 GMT  
		Size: 5.4 MB (5368171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec7a9c9e28d59d671b303a8ed215dec5c617d085941712041975a6de179576e`  
		Last Modified: Tue, 14 May 2024 15:38:32 GMT  
		Size: 1.4 MB (1371225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8baf0005c66072b15b907340892649f395b58750a2727a4138c8d62fc30b9ef2`  
		Last Modified: Tue, 14 May 2024 15:38:32 GMT  
		Size: 8.1 MB (8068963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21384c66fa8ad2af30496f67140f8e068f2ceb2a2d789837e2384593cfca9fd9`  
		Last Modified: Tue, 14 May 2024 15:38:33 GMT  
		Size: 1.3 MB (1283486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1c0befeb421a5453649797a027f09baad45dc7c996e3486da49f4e9879286e`  
		Last Modified: Tue, 14 May 2024 15:38:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46725b9093668cd05b0dc9eb9f0aba3b982b3a9434680e5c3303df5b96960ec1`  
		Last Modified: Tue, 14 May 2024 15:38:33 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a0206b844bc15578e47ff9dc31667321973042a20a0d95cccd47aab5b439cd`  
		Last Modified: Tue, 14 May 2024 15:51:19 GMT  
		Size: 111.2 MB (111167026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70b1be3e968d96a9feda09f0f028406e6ff0275bf99dcc90aebe22681c36d27`  
		Last Modified: Tue, 14 May 2024 15:51:14 GMT  
		Size: 9.0 KB (9023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518e685b726a0432858f8fbdc5a53b86f0f631d675f62aa4d2455964bd0dc2fe`  
		Last Modified: Tue, 14 May 2024 15:51:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d647b502f944211b6065aca3856fefbd87554bb81f6b9ecea9f81ce5536486`  
		Last Modified: Tue, 14 May 2024 15:51:14 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e547bb4e9ae925617de0727af239d1850524ce776d5a0e97444f3c802e1dcb60`  
		Last Modified: Tue, 14 May 2024 15:51:15 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5362a6315d84fe44f22c226645f1dcae21baac36bcc88cd28038adf0b0c6a6b6`  
		Last Modified: Tue, 14 May 2024 15:51:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:9f55d8a26bb1366a35e1d5dd1f343a7b1894c902d656d648e2464813fd58c896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5631937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ffc4c5eb0da2c7ec897af64458ed1d7032df34b4f466fd19fae1f58405f607`

```dockerfile
```

-	Layers:
	-	`sha256:870ace534a959b6e9efa88075780d69c1a696ba2dadb437c7e44c9c8a3de6fad`  
		Last Modified: Tue, 14 May 2024 15:51:15 GMT  
		Size: 5.6 MB (5577402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a9a5da330ecfda2ae945d43de5af7939c9ac50bf25562e998acbbe759d37e62`  
		Last Modified: Tue, 14 May 2024 15:51:14 GMT  
		Size: 54.5 KB (54535 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:021c9a001735b25b46506eca2e595733b4777b0b0708d8ba883a0b32bfd73ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.9 MB (153882624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fffe30db95f55406ae1011664abb33a7d89190b5345c7a03f9d1adf551998cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:02:23 GMT
ADD file:e4d9e24430546fda3cf8c73efdaa45b6bf1014a23d4d3c0247fe341b3ee9212a in / 
# Thu, 09 May 2024 18:02:23 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV PG_MAJOR=12
# Thu, 09 May 2024 18:02:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Thu, 09 May 2024 18:02:23 GMT
ENV PG_VERSION=12.19-1.pgdg120+1
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:02:23 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:02:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:02:23 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:02:23 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:02:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:06561002b4f942b877c60f94bd44315c2e0580cc0ae30f060660bdbcdae21d6e`  
		Last Modified: Thu, 13 Jun 2024 00:47:43 GMT  
		Size: 27.5 MB (27512459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df718a21529484d825e8d34c404257a0546286e7a7caaafa5e6aa3c284858359`  
		Last Modified: Thu, 13 Jun 2024 12:22:12 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab19acd660b1d3121eadb9baf4f00251f6bad0be1f21e5546e9a7bbdf7c25f0f`  
		Last Modified: Thu, 13 Jun 2024 12:22:12 GMT  
		Size: 4.4 MB (4391035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec53b5378db13907773971770802e5cd432e139b9ca53f853835ada5cff2134b`  
		Last Modified: Thu, 13 Jun 2024 12:22:12 GMT  
		Size: 1.4 MB (1415933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f148609caa08348b01404906d68e5fac6a87cf8be9296e80c1478c47b119a32`  
		Last Modified: Thu, 13 Jun 2024 12:22:13 GMT  
		Size: 8.1 MB (8123196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4a29b13525c5cab1218d23d20c299a8d1311c5619fb9a8586f2cdba6ec7dda`  
		Last Modified: Thu, 13 Jun 2024 12:22:13 GMT  
		Size: 1.1 MB (1096730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b9b3dab45f719c1cfa9a9942b491b3d6577a1e12d3c44ec54edb4ba4bf475c`  
		Last Modified: Thu, 13 Jun 2024 12:22:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce605bd25ed1e30eab9e389d318038b16d3f7fea277774f1e329cce643e81f83`  
		Last Modified: Thu, 13 Jun 2024 12:22:13 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2f2b4ec4d06e6d166abf065d5251b8b0361be121b5acfbc01b0eca387f65a6`  
		Last Modified: Thu, 13 Jun 2024 12:36:12 GMT  
		Size: 111.3 MB (111323932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f479281bb27bb5d89ec0619a49e3473b77ef467243f00bc1bef2039d123d49`  
		Last Modified: Thu, 13 Jun 2024 12:36:10 GMT  
		Size: 9.0 KB (9017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf149a662d8edbb8a4d87a553b524e8e23697a3e1b5ecafdef7c7334358f04a`  
		Last Modified: Thu, 13 Jun 2024 12:36:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a0fa0ef910d5502797d65ee417b532262a6ef9be3f2b4e6749c369be0eecc5`  
		Last Modified: Thu, 13 Jun 2024 12:36:10 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a610c99dff7323e9818d32dcec5d902defdf2b4abf06260d9832472bada8aec`  
		Last Modified: Thu, 13 Jun 2024 12:36:10 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a3902a6fca6fbbf506f4b3113124552fc701bd796935560229d40b88a5c03e`  
		Last Modified: Thu, 13 Jun 2024 12:36:10 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:baa54a6f59e2133e1cf5e409b394e346173a7c02514cebf0135abd6981171d06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5624090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c41820acf2d1498ab625962ac89f20681df4a198a09eb33c569975d633413907`

```dockerfile
```

-	Layers:
	-	`sha256:28a63df3c145613c55a3cd3a9579851416a05f68dc86791b07b27c8c213caf37`  
		Last Modified: Thu, 13 Jun 2024 12:36:10 GMT  
		Size: 5.6 MB (5569566 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e02c12657d38a9e5e2884775b7b7f3a487f7dadd5eec7e3c1ee6b0d905ab9c1`  
		Last Modified: Thu, 13 Jun 2024 12:36:09 GMT  
		Size: 54.5 KB (54524 bytes)  
		MIME: application/vnd.in-toto+json
