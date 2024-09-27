## `postgres:12-bullseye`

```console
$ docker pull postgres@sha256:82156837dd098064762621ae9cad5028887d8cf7a1fe33b6bfdebb3e8ef33f80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `postgres:12-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:980648f865d792e06fd023c32708af302aee309c0bbe7649b13686f0d9ea042e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140055379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4f64b9681c83ed13f9d21999bee84261f86b63746845677ea3b29eaabb1427a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:22:52 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
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
ENV PG_VERSION=12.20-1.pgdg110+1
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8a499c24facfec1656d89988f45f5e7a3e794178ffbbe2937abe2be862f94c`  
		Last Modified: Fri, 27 Sep 2024 06:03:15 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674de784cb59e09c3507a8a21b5af47816536a87dfddc4f0a22d62f0b2d3feeb`  
		Last Modified: Fri, 27 Sep 2024 06:03:15 GMT  
		Size: 4.3 MB (4308140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7367bd047a10964ec5912deee43edad5b10a22cd0246302cb7ff284d3fa4a052`  
		Last Modified: Fri, 27 Sep 2024 06:03:15 GMT  
		Size: 1.5 MB (1472209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cebf1db0dad62b1aaca5496767602eba6e9eebdfd50bec8dff03c4f4dd2d885`  
		Last Modified: Fri, 27 Sep 2024 06:03:15 GMT  
		Size: 8.0 MB (8044412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab37d6c302784a1b612b43acb9eb9c74e9ffce2fed8db6f36af5b4599663032`  
		Last Modified: Fri, 27 Sep 2024 06:03:16 GMT  
		Size: 1.0 MB (1038346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5d8ce8b2b87cfd6371adf28507eaea5c6b2f4c89196682bcd71a3c40f7df42`  
		Last Modified: Fri, 27 Sep 2024 06:03:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b70089fd7f077d44a9e4591e2ff2d62fb8dbf4db783533d118121e637e5b66d`  
		Last Modified: Fri, 27 Sep 2024 06:03:16 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60edbcea6e4713b54c88620dbd9d1d79407612fb31fe646cd500a11742d49bb`  
		Last Modified: Fri, 27 Sep 2024 06:03:17 GMT  
		Size: 93.7 MB (93743826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b187989767550ddd52867fd659e2aef809ddbc1e3d19b18fdf17cbaeeade081`  
		Last Modified: Fri, 27 Sep 2024 06:03:16 GMT  
		Size: 9.0 KB (9014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475ad8bcff8e9c29d1f8c174096590ceab2ecc5aa42e044259462be7f1060b86`  
		Last Modified: Fri, 27 Sep 2024 06:03:17 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1ee0a6af8769114bfe6f3fff3c3a5761d55a8e3adacb9fb8abc177c7a48230`  
		Last Modified: Fri, 27 Sep 2024 06:03:17 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43aad222cc601282e7ecc65e0a1d9742b4dca5dd4de4b031bbb54bdfe703ee02`  
		Last Modified: Fri, 27 Sep 2024 06:03:17 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238e426a201a7a79851a09235e96e24f177b26bf30d3eff4bc0c61dd640feca5`  
		Last Modified: Fri, 27 Sep 2024 06:03:17 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:c47bcd860cbddf02710ff1363aa0c1b84e5233241478d038284c8d00affebba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5901590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e74142d76a16e08db7aff616cc255376599254a2f73e02da235b6611c06d8c4d`

```dockerfile
```

-	Layers:
	-	`sha256:0812a13d68aa1f462f329cb0c7d17e5091bf781da27e44551d7a06a2c1895786`  
		Last Modified: Fri, 27 Sep 2024 06:03:15 GMT  
		Size: 5.8 MB (5847749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81aaa8d5cdff2a83a5814d8b20eed08e3f8d79a8cb435a855ac7b844391fb085`  
		Last Modified: Fri, 27 Sep 2024 06:03:15 GMT  
		Size: 53.8 KB (53841 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bullseye` - linux; arm variant v5

```console
$ docker pull postgres@sha256:b207f276b18ad0e3b875df38e49d96c1b5d471bd70a9ad02d1811058595df4b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.9 MB (132912782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d69ecf915d64b6ff89f75a3f48ca20c16c3c47df118255b975e915b935ae1c59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:22:52 GMT
ADD file:b6f3f19f4bd2bf78068380b3cd10d72519ced99a2b5abe830b4729df341dcfdf in / 
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
ENV PG_VERSION=12.20-1.pgdg110+1
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:eb58dd05d71179dcd2ecf0ec8338e7ff114cd5be9c0806a025a8205ee48b13ed`  
		Last Modified: Thu, 05 Sep 2024 08:36:38 GMT  
		Size: 89.4 MB (89447941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b51233c0e2f8f1f6d3364b497e52cc6b656d249d4fb0a566b98a5fe681c4b64`  
		Last Modified: Thu, 05 Sep 2024 08:36:35 GMT  
		Size: 9.0 KB (9026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b981f9fd55f0a9f9596ce03ad64af90b41611db1fec75d0f68330755cce41cf`  
		Last Modified: Thu, 05 Sep 2024 08:36:35 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3a515be53589275271288995bc0dfb776bab2a520ac4c49a7ca96669677862`  
		Last Modified: Thu, 05 Sep 2024 08:36:35 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378791001d7d3c662b5263d3cfe85a5b7f2f0a41348ddd998eb0132dce1a73ed`  
		Last Modified: Thu, 05 Sep 2024 08:36:36 GMT  
		Size: 5.4 KB (5425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20b90b5bd62476ecc653583d689affae084ad2710f55e70ebd962ef3bb305bb`  
		Last Modified: Thu, 05 Sep 2024 08:36:36 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:9e15fe67ce8f033dce93ad8c987c5b3f1be775b6bbe6df881e8e1b8c24e68927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5914412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33833b9a4bc993cee92f3614975f94ac96949862b57f7c36c39eefa18456a491`

```dockerfile
```

-	Layers:
	-	`sha256:cf130a28c1aa520583f3f06b29ebcc3ecbfe1a05d21dad57fe0197e05b2d51d5`  
		Last Modified: Thu, 05 Sep 2024 08:36:35 GMT  
		Size: 5.9 MB (5860374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a4b9dd5d75b7cc81cbade9d0372e33041dd5eeb339ac4b15a81bd80309cdd33`  
		Last Modified: Thu, 05 Sep 2024 08:36:35 GMT  
		Size: 54.0 KB (54038 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:70d7843cf69465bd6b738f34a32f1fdd791dccc07c56c6155824252a7c513468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128107205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb02b36c487d77e2e5d1020a0a5fa2ad9789210bb5dccfde0793edb9c7ff98a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:22:52 GMT
ADD file:9017833b3f74675db45d0ac4f67e9ea2e05e58da02c851ea580aa49f0b310c64 in / 
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
ENV PG_VERSION=12.20-1.pgdg110+1
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:ea6a6c5151e68b5b8e6387d29b1e945e29ac292dcf4f3458fa71a33db9e1aa51`  
		Last Modified: Fri, 27 Sep 2024 05:17:51 GMT  
		Size: 26.6 MB (26589312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f7ee9aa8542dd002b04e55a6816f5bf5cbb0158a4cb741a5b026c444f3cd68`  
		Last Modified: Fri, 27 Sep 2024 13:35:17 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d92d01c1ba353d80b8b90c070c0cd8e9aad8011e305d8e11261b9b70178c2ba`  
		Last Modified: Fri, 27 Sep 2024 13:35:18 GMT  
		Size: 3.6 MB (3601646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ac53483c20be8e3dc37018657fa7da71cc2fe704d4a8584f5bed780f6f95bf`  
		Last Modified: Fri, 27 Sep 2024 13:35:18 GMT  
		Size: 1.4 MB (1439197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc13a593572aad175dadc94e74d94c092854fff01df09ebccb3510c741f7d0e`  
		Last Modified: Fri, 27 Sep 2024 13:35:18 GMT  
		Size: 8.0 MB (8044380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241c86160ff5e1ba60a1c7604eb26405626ab6fda5c4380b9805a59ad97c7109`  
		Last Modified: Fri, 27 Sep 2024 13:35:19 GMT  
		Size: 908.7 KB (908657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e465cd3063172bb3e815c998a8336034bbf814952b3e1af5cdaaaadf22f42d3`  
		Last Modified: Fri, 27 Sep 2024 13:35:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244049feac44bfcaa4ae84b09a618357b8decd08d5f3628de436d48f8af0833b`  
		Last Modified: Fri, 27 Sep 2024 13:35:19 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13ce6ae8108f3bcd99ddd4f080a594037c5018121bcbbf0899cbffaac4670f8`  
		Last Modified: Fri, 27 Sep 2024 16:06:15 GMT  
		Size: 87.5 MB (87504168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262ae67ee8cf03c31130971337a8359a2a78a59be089c113d9d9675ac1d07630`  
		Last Modified: Fri, 27 Sep 2024 16:06:12 GMT  
		Size: 9.0 KB (9020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf8663622789d7e9ca678e85dc384b9122e02c7af188d6f29960d74b85bc3cb`  
		Last Modified: Fri, 27 Sep 2024 16:06:12 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec777c681cf2388925365d6118554d76109fc08851fb67aa6a560899ad333bfb`  
		Last Modified: Fri, 27 Sep 2024 16:06:12 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a9a69a40986f7685c1724b97bfa4e35d15c4302be2acca598e5b7153a608f8`  
		Last Modified: Fri, 27 Sep 2024 16:06:13 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b23755ecedc64d8e1191ca498c4e0557f2e1ca029cb6c2bdcc6f920795cba02`  
		Last Modified: Fri, 27 Sep 2024 16:06:13 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:5389c5263f4cadf703fe85c91393d0046cd4e1aecfe6bf5b4e1dbcb731b705e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5914045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09ee02f973feb1c4063f7aea48eba93118472714e056df6a88d9df8f29451146`

```dockerfile
```

-	Layers:
	-	`sha256:31a65922352dd94c101bb109772ae16e58afced7f5e7b6d84020cf6f4a788f30`  
		Last Modified: Fri, 27 Sep 2024 16:06:12 GMT  
		Size: 5.9 MB (5860016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:656a4ae8a4dabcd7f9b481e677234acde29d198c5824e948f1016026c8c6a414`  
		Last Modified: Fri, 27 Sep 2024 16:06:12 GMT  
		Size: 54.0 KB (54029 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:2c2993777bd5a78ba8e7dbce3067180188552f3dbe80e3a3d3bb22a10097ff2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136498683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1613d332c7e246439e8bde4009f8759291edfe250251e76070114319bef70a2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:22:52 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
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
ENV PG_VERSION=12.20-1.pgdg110+1
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4d435480769061fce76dcf29c4861bab3e49a37bbca3753981efcaf2b8972f`  
		Last Modified: Fri, 27 Sep 2024 19:05:36 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc3b62378842b599f0fbae4205b2ae2cf07da365179b99b9237f72f564bda87`  
		Last Modified: Fri, 27 Sep 2024 19:05:37 GMT  
		Size: 4.3 MB (4312746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db4cf39e8570f778921a4af200004283dc8a53c7a1a7c9a4c86144bc0d19996b`  
		Last Modified: Fri, 27 Sep 2024 19:05:37 GMT  
		Size: 1.4 MB (1404151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2834286179aaad945f6567c9bf89b871eaaa864bc7723554dd671e851e07fd71`  
		Last Modified: Fri, 27 Sep 2024 19:05:37 GMT  
		Size: 8.0 MB (8044335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68007a3219b210af3b8f6244783ec225ff909486d766af1078437765b2c59f46`  
		Last Modified: Fri, 27 Sep 2024 19:05:38 GMT  
		Size: 1.0 MB (1026605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9441dbae15794bec4ea60e6bcb0a7918188dbc0d546c1e676b20097178d70dd`  
		Last Modified: Fri, 27 Sep 2024 19:05:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9759db2035bb92733699320db4147e40c8f0a7fa9e1824e57430a7f5333cb835`  
		Last Modified: Fri, 27 Sep 2024 19:05:38 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878d04c5e74fe8cbbd752cd7bd6e9982dba59203bc27bec51a8b9267fe9f3fa6`  
		Last Modified: Fri, 27 Sep 2024 19:21:15 GMT  
		Size: 91.6 MB (91615835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04cefd298100a6332a3bb253a18b0265aa62db042b3351dc513bb16402b4c0d`  
		Last Modified: Fri, 27 Sep 2024 19:21:13 GMT  
		Size: 9.0 KB (9016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb184f8e1ef555b68ed63110cd8a85e03a618efabdb8b0bc5e5a7a52f60f8cc7`  
		Last Modified: Fri, 27 Sep 2024 19:21:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42978c408e23cc4765d713d341d447eceb0b526bd0b3c8ee1df6a1dfa55b503a`  
		Last Modified: Fri, 27 Sep 2024 19:21:13 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f0e6d508d476b93deb70992cdf3658c167d942dadbbed4bb06dc0510349700`  
		Last Modified: Fri, 27 Sep 2024 19:21:14 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155d91333a383d81d41daf5e1485f0b456a1815dafc50ba404c82fe310ebbfb8`  
		Last Modified: Fri, 27 Sep 2024 19:21:14 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:bf4be1fb1aba7718b57512acc8761c005ce5465d4f407380008e1e4c36d94c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a9e18c27a410d7f629be01a78a0389e68b91e5b1cfd7792d18207b58da3bb9`

```dockerfile
```

-	Layers:
	-	`sha256:fa4f2486334e00a8ae10ee0811a5018bdeebaca27c3aaf6d8dd160e4f9dcb052`  
		Last Modified: Fri, 27 Sep 2024 19:21:13 GMT  
		Size: 5.9 MB (5854039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80e54430c736b667c88ee28615921268d92d8e898e5176a8f55600ed25334995`  
		Last Modified: Fri, 27 Sep 2024 19:21:13 GMT  
		Size: 54.1 KB (54126 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:305b527537beb18a633c7aff832650e3668a066fe7f4f18f3f313f6257dd2a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142607888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7518a91b9fd729610397db695e96b67c2aa2cd1cd449abadde599d15d55833f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:22:52 GMT
ADD file:176ca55c782e88e529d56f56999487b261e37eaa9b59fcfdf2b400ed60a31a55 in / 
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
ENV PG_VERSION=12.20-1.pgdg110+1
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:5306a3a8e6d3817e237e681e3f75f332f8a6ba35c1f365dcff9af549d9f45234`  
		Last Modified: Fri, 27 Sep 2024 07:27:50 GMT  
		Size: 32.4 MB (32413499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f3806064ad19011aacbc994441381158e8118dc572c73c97ccab50f8d100b0`  
		Last Modified: Fri, 27 Sep 2024 09:11:05 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d521e5b3e71f4c46c832ff7aadab4082faa731d6e38d7171732d2be1bfdf50`  
		Last Modified: Fri, 27 Sep 2024 09:11:05 GMT  
		Size: 4.7 MB (4719658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3331173ae6a7ffc4c8f46d636b3bb9be7134287167f7f051eb2a769e78f315b`  
		Last Modified: Fri, 27 Sep 2024 09:11:05 GMT  
		Size: 1.4 MB (1447811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10c0e25b43d62c22125d5cab65744ccbb816f2fbd12c67ff892175c61fd7d85`  
		Last Modified: Fri, 27 Sep 2024 09:11:06 GMT  
		Size: 8.0 MB (8044321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725436626ab6364f6161ea7d51452f8e7ed9cb1af6cd368f6f52b2eba5b4b5d4`  
		Last Modified: Fri, 27 Sep 2024 09:11:06 GMT  
		Size: 1.0 MB (1028938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1951ad3b64a24acfd4ee9d864de7975c5f4375871d962d5f960b02654b8ef44`  
		Last Modified: Fri, 27 Sep 2024 09:11:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3dabb8a2231b842ca6615a9a1ed515e375f20955b812999d8dcd51e6e1fee9`  
		Last Modified: Fri, 27 Sep 2024 09:11:06 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7187f1e665c47300006f53f6873ab9db48153ab9f5df460d9430ecc1af802d51`  
		Last Modified: Fri, 27 Sep 2024 09:11:12 GMT  
		Size: 94.9 MB (94933809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1390b65f90b1a020c4fc03c7acb3141838e260cdd072b6f3a4ad244dc1108ae2`  
		Last Modified: Fri, 27 Sep 2024 09:11:07 GMT  
		Size: 9.0 KB (9017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f8158b612d102fa8e32ff9510a96527ea80fdb3334593eff1bfbf3df253893`  
		Last Modified: Fri, 27 Sep 2024 09:11:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1450160c48ff2f43f85e41469d409616fbd57651866db072d676d2555f8501a1`  
		Last Modified: Fri, 27 Sep 2024 09:11:07 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f055dcd9826776b7c0b7d1ece4fbeb03c5c2e7c3f6d1f499017f945fb12946c`  
		Last Modified: Fri, 27 Sep 2024 09:11:08 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988ff5ab198c920527d8a4a81bfce757a36d1cb8af5b728f5555e5b5b45bc532`  
		Last Modified: Fri, 27 Sep 2024 09:11:08 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:39b67c0efaf6a1ff9c158deb6481a0b550919337105ea362658cc57ec8b6f810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5911507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30921515893896963fa6fb23c5f14251729f77c8befa925e56fbe85d3f957c57`

```dockerfile
```

-	Layers:
	-	`sha256:b159dbe9bad70d9780981ae7c351ad3a0193e38eed0f2e64a91a2738189f619e`  
		Last Modified: Fri, 27 Sep 2024 09:11:06 GMT  
		Size: 5.9 MB (5857707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbafd56cf0cfe9bd37fb2bbce7ef0144df397e1376dd5c01d715c36b63b182ef`  
		Last Modified: Fri, 27 Sep 2024 09:11:05 GMT  
		Size: 53.8 KB (53800 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bullseye` - linux; ppc64le

```console
$ docker pull postgres@sha256:f566c573faef1106cbf5093ba689198a11fa886bcf9ee33eb88d895f0d975ab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.8 MB (150818109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c35c182dd2208adbe8c67d18aa868ce5838c452571ac847bcdfbb33ba3b6495`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:22:52 GMT
ADD file:1dd1fe717176cf8c20fe5b4fd39ce7f79d39d2aec08c436f3ade914e61d5d17b in / 
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
ENV PG_VERSION=12.20-1.pgdg110+1
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:d707bb7aae242f1d09f79521fe5f270d586f9dffc7621fd108c3901d6d8b3e24`  
		Last Modified: Thu, 05 Sep 2024 03:27:18 GMT  
		Size: 99.7 MB (99725497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501a0ad7ecda7a83c235c17af0496d45bdbfc53f9e6da36a54229ee45e51c17d`  
		Last Modified: Thu, 05 Sep 2024 03:27:14 GMT  
		Size: 9.0 KB (9021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e71ba3a3fde9ed73f2c76945d173ff66cf430a254976111dcc548cc0c04cd5`  
		Last Modified: Thu, 05 Sep 2024 03:27:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63ff9d405e93aa6ab5c1209bb2387b088362a1c1e6664f6b7904be894bc1244`  
		Last Modified: Thu, 05 Sep 2024 03:27:14 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a353928048abb77adfc31a188e30ae170b179cd7f748138abfed3ba57be5158`  
		Last Modified: Thu, 05 Sep 2024 03:27:15 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b57d64e232bd9a89b30d940ff9a47b4a19ec72ec0e0c3cae3f13dc975475d3`  
		Last Modified: Thu, 05 Sep 2024 03:27:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:33decb68f64e69ced676adbd52d523eecea1f5190d2cbd2c4aa7eda19e010094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f920ebdc70b4fc1f836c14a2d3ebadc3ec2e9816eb926b9cd33f0f0cfb380c7b`

```dockerfile
```

-	Layers:
	-	`sha256:db63adba5c4eef273f40ecf7a9f71d52d327094384412ef303641730af282481`  
		Last Modified: Thu, 05 Sep 2024 03:27:14 GMT  
		Size: 5.9 MB (5854868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec458d72ea82daead93f1a180e21436c5814c501312a1931838982e1c176ff8e`  
		Last Modified: Thu, 05 Sep 2024 03:27:13 GMT  
		Size: 53.9 KB (53889 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bullseye` - linux; s390x

```console
$ docker pull postgres@sha256:c059ee00e4e1e8c991c8b0e7ec7ae6b0b3eb94c44aa8143e3b7b6d262fa9b1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144338801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf020212f9eda49e0b3c3161fe98086277fbcd452420ee331b68fd9d8b6f5c5c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:22:52 GMT
ADD file:301629b0d8ae489e6705aa09fa33dae1617ec0882c0376c2a9b5ec18197190f0 in / 
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
ENV PG_VERSION=12.20-1.pgdg110+1
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:27f5b62d7f564f989ce6b72c60d55746a44b529a03a9e20af06204d7736c122c`  
		Last Modified: Thu, 05 Sep 2024 05:17:05 GMT  
		Size: 99.9 MB (99903067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75766bbaec200078c60e2650a6cc5a3c5371e65b3cb789cb6f6fd0c9fda5776d`  
		Last Modified: Thu, 05 Sep 2024 05:17:02 GMT  
		Size: 9.0 KB (9020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8afa91290e5dde00bd28d1de28503d34a2b8fd61eadecfd3f7c911e6186724a`  
		Last Modified: Thu, 05 Sep 2024 05:17:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d700583b6117da723348b1113f484b3fd8b8b1a127a5d5acd08216e066f19be4`  
		Last Modified: Thu, 05 Sep 2024 05:17:02 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06eb0a969bf4c4f709f8e7a8c179ff452e4197ffcc1cee4edc37b50e493c9677`  
		Last Modified: Thu, 05 Sep 2024 05:17:03 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd0efb1ef95a4740859921f8bf3510afd8423e73f3614cced91cf9b11932ec10`  
		Last Modified: Thu, 05 Sep 2024 05:17:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:64efd241f341fba05b7005ac8f4f23e4d964c2783afc47e380dfc0c77c6b2017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5900552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ae2a76f95cda37c60b39ec66bfa6298fe6e7d5350cd7df3d2408cf1a10c2b2`

```dockerfile
```

-	Layers:
	-	`sha256:2db10d53d4b68c71461789982ed1c0b08916e0f32424c617e9250e4496c97e0a`  
		Last Modified: Thu, 05 Sep 2024 05:17:02 GMT  
		Size: 5.8 MB (5846713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07a1767cb23ec77d8c82fe77048149f0496cfd79d8f0e760fb6fdefc5fe5238f`  
		Last Modified: Thu, 05 Sep 2024 05:17:02 GMT  
		Size: 53.8 KB (53839 bytes)  
		MIME: application/vnd.in-toto+json
