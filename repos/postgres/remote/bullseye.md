## `postgres:bullseye`

```console
$ docker pull postgres@sha256:9f2fd97cddf02056135f2a7f3959df6b636e050cf8bf70430643ca0d2ff14051
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

### `postgres:bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:77b5131f934f16c293c4f23979f0c01ef678b195808348cf8f093733838902ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.0 MB (144955720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e67f49d970f86d31e93a11d848ca4cd7a5705f941f7a916086b02144cacfb8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 12 Feb 2024 19:15:38 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Mon, 12 Feb 2024 19:15:38 GMT
CMD ["bash"]
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
ENV GOSU_VERSION=1.16
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
ENV LANG=en_US.utf8
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
ENV PG_MAJOR=16
# Mon, 12 Feb 2024 19:15:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Mon, 12 Feb 2024 19:15:38 GMT
ENV PG_VERSION=16.2-1.pgdg110+2
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 12 Feb 2024 19:15:38 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 12 Feb 2024 19:15:38 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Feb 2024 19:15:38 GMT
STOPSIGNAL SIGINT
# Mon, 12 Feb 2024 19:15:38 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 12 Feb 2024 19:15:38 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77cf33a56a6530d3f3ab5f8a346e15a7beb26c6f9a980c09db759d310b72bb03`  
		Last Modified: Tue, 13 Feb 2024 01:58:43 GMT  
		Size: 1.7 KB (1683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b54282b50ea001f3bedb5feca562e4e11c0a844bab9063bf0c2f9def9e7b71b`  
		Last Modified: Tue, 13 Feb 2024 01:58:43 GMT  
		Size: 4.3 MB (4305888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69d37e8f6fdb64786ac3e49f4fa4d35c50547de1aeb590062386d2417668f2c`  
		Last Modified: Tue, 13 Feb 2024 01:58:43 GMT  
		Size: 1.5 MB (1471787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6fcdf9837c3dc705cb18994943efd1dd10dccac9c2c633c854a3b124055490`  
		Last Modified: Tue, 13 Feb 2024 01:58:43 GMT  
		Size: 8.0 MB (8044038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309d802244185c0f1358dca41b31978f313960e0b1f36f38a132b1dcbdc5ae8c`  
		Last Modified: Tue, 13 Feb 2024 01:58:44 GMT  
		Size: 1.0 MB (1038369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00767100b5b5e9413aacfa6b1693b8e4c4b8a29a6444d8db1b6d87e5296cecf0`  
		Last Modified: Tue, 13 Feb 2024 01:58:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76fde63969be03e7d2dfa04dcae7041217606f5a83ecba96b91073486dfa61cd`  
		Last Modified: Tue, 13 Feb 2024 01:58:44 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971936bd70d35a206071376a7a1becc73d9d3435412e9091743c2ffebcc3ef9a`  
		Last Modified: Tue, 13 Feb 2024 01:58:46 GMT  
		Size: 98.7 MB (98652466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b5646f23796f2ac4ecfa8f89dce313765ba998eca3054b0c3336834e172ec0c`  
		Last Modified: Tue, 13 Feb 2024 01:58:45 GMT  
		Size: 9.9 KB (9914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a31aaac7d0b6d946156fd35a611bf224689cce678b29aaae897fa3cd5e859b`  
		Last Modified: Tue, 13 Feb 2024 01:58:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ba6a640840aeae236e1d594981581627a407dadb5311a646138372f8f9be76`  
		Last Modified: Tue, 13 Feb 2024 01:58:46 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426382df61af4c509894f334eee61a83eb84ef7a9f3bf9b33a859af42eb432cd`  
		Last Modified: Tue, 13 Feb 2024 01:58:46 GMT  
		Size: 5.4 KB (5413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220457fdf6e9f102fe7a854a1b9b4005d621b59c5b8957ab1ccb3e460f4bea8b`  
		Last Modified: Tue, 13 Feb 2024 01:58:47 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:b00aa19f66fd149a6b2bc1eb05ab7571786fe7af78c015473a42e5bcbffea629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5208332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aad16f7b0fb50047a239c6282370b846b2f53e045cc43466142c789d6f535b2`

```dockerfile
```

-	Layers:
	-	`sha256:c4e30ec219a3e4e5d23e0741a10ded2828e1293eb2cb096c990f35f327e805a9`  
		Last Modified: Tue, 13 Feb 2024 01:58:43 GMT  
		Size: 5.2 MB (5153999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:988baf94536902a990c3e35fd96bc25cc6b852611dd3760e2f3694f11406b837`  
		Last Modified: Tue, 13 Feb 2024 01:58:43 GMT  
		Size: 54.3 KB (54333 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bullseye` - linux; arm variant v5

```console
$ docker pull postgres@sha256:37d25416df9083763627c8f2f585b98e216be79ec3b97f158f31f1044cc53aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137879826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2139ea9a3569f10a5d2f8d12f5587441cf55bd40c8fea706e37fe71ac9fab5c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 12 Feb 2024 19:15:38 GMT
ADD file:2900145429df7cd46dd4818f44636aff96d0ef5335d5eb8cd5ed3106caa8b031 in / 
# Mon, 12 Feb 2024 19:15:38 GMT
CMD ["bash"]
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
ENV GOSU_VERSION=1.16
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
ENV LANG=en_US.utf8
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
ENV PG_MAJOR=16
# Mon, 12 Feb 2024 19:15:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Mon, 12 Feb 2024 19:15:38 GMT
ENV PG_VERSION=16.2-1.pgdg110+2
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 12 Feb 2024 19:15:38 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 12 Feb 2024 19:15:38 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Feb 2024 19:15:38 GMT
STOPSIGNAL SIGINT
# Mon, 12 Feb 2024 19:15:38 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 12 Feb 2024 19:15:38 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:237c1c7c36842faaa132f240658a3f42b8e6adb150f7850dc25fb4b50ed242ba`  
		Last Modified: Tue, 13 Feb 2024 01:14:18 GMT  
		Size: 28.9 MB (28924482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1236d0a5c3d9dbd7d2404f4ac1a010b57e12a320dbb3300fa84fb31d45669d`  
		Last Modified: Tue, 13 Feb 2024 23:07:56 GMT  
		Size: 1.7 KB (1673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b55d60842b4bb8e79bafcef2db8b104b1be57ba2cbd233caff6cfa38d2b18b8`  
		Last Modified: Tue, 13 Feb 2024 23:07:57 GMT  
		Size: 4.0 MB (3986248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057e03c38c6d55c1c14888c4860b085ae664acd448e75f0d82ce0f0d89a43930`  
		Last Modified: Tue, 13 Feb 2024 23:07:57 GMT  
		Size: 1.4 MB (1449151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c590e64b2116cca854e4e4e794efd0a54ccfc6774fb4d85ff0cfe43ae9cc4b`  
		Last Modified: Tue, 13 Feb 2024 23:07:57 GMT  
		Size: 8.0 MB (8044109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1bcda3a50c7d7b7cb5484d1f87857fb08dd495fc486b8fcfb7edabcda15326c`  
		Last Modified: Tue, 13 Feb 2024 23:07:57 GMT  
		Size: 1.0 MB (1034923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ba7c974f079b0a97581d738ebaedec0f1dd82917a0758f9b6c2f1b05f68d33`  
		Last Modified: Tue, 13 Feb 2024 23:07:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2a77cea0506ccdcc7fdd925d122419c29c11c232722f78e12f18afb35a6d8c`  
		Last Modified: Tue, 13 Feb 2024 23:07:58 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c91adaaa3b22d849e501e5f736646d68186ff3aa9dd0b880eb53d680635dbcf`  
		Last Modified: Tue, 13 Feb 2024 23:08:01 GMT  
		Size: 94.4 MB (94420166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61e32fcbc13f40cba2ae117dc1d0d1e55b24e642c5b8a04fb5a4d07853058db`  
		Last Modified: Tue, 13 Feb 2024 23:07:59 GMT  
		Size: 9.9 KB (9922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a87899f44c0fb03409d985a7eff6e81d0bab4f0f50ca502c17d93187a499eb`  
		Last Modified: Tue, 13 Feb 2024 23:07:59 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70de5ca5a4cd451ab524b89e61a38aec30fa1bbb468f24a921dc7375a272b2c1`  
		Last Modified: Tue, 13 Feb 2024 23:07:59 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d3795ac33c4594208b820c67490d885955c2df98ab029307b17058a539f426`  
		Last Modified: Tue, 13 Feb 2024 23:08:00 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82df2cccca12b70a9ce6af509b84f0373091bf524ba8e28c2f1ff7d314885dc5`  
		Last Modified: Tue, 13 Feb 2024 23:08:00 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:5d851b273a03d230bef1626b36b6a762994d7257d644e3fd7277c3bff11ed63d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5223994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e1fb4ee88e33c3c637bbcf7ea2bc7c69aa12c1c49bc306021cbfc0f6c66c67`

```dockerfile
```

-	Layers:
	-	`sha256:0d31f91d8528cd5059bde527af66f6f0dd733f8345a1fc7385dd3100b42a425a`  
		Last Modified: Tue, 13 Feb 2024 23:07:57 GMT  
		Size: 5.2 MB (5169623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b5ddf0758dc3c401c7ab39fbfcf02c00eb5940a660c93684f59263950d56c0a`  
		Last Modified: Tue, 13 Feb 2024 23:07:56 GMT  
		Size: 54.4 KB (54371 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:041e52f087497337be6ed45ee6aba75a5554b3e7f7f04496df557266e064562b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.9 MB (138865228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456bbbe26a526d7670356db597bbaebc7adbe3aab772a6701260cd614c1fcb4e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:42 GMT
ADD file:65b9e2efdf2b09faf0d5ea0e2e00984ff3c8cf89b7959287bc6ca54c7772801d in / 
# Wed, 31 Jan 2024 22:44:42 GMT
CMD ["bash"]
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
ENV GOSU_VERSION=1.16
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
ENV LANG=en_US.utf8
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
ENV PG_MAJOR=16
# Mon, 12 Feb 2024 19:15:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Mon, 12 Feb 2024 19:15:38 GMT
ENV PG_VERSION=16.2-1.pgdg110+2
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 12 Feb 2024 19:15:38 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 12 Feb 2024 19:15:38 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Feb 2024 19:15:38 GMT
STOPSIGNAL SIGINT
# Mon, 12 Feb 2024 19:15:38 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 12 Feb 2024 19:15:38 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4de6a546d77461a35cb9514c6432142adfb72460cf04bac21bd261d66c288476`  
		Last Modified: Wed, 31 Jan 2024 22:49:36 GMT  
		Size: 26.6 MB (26579212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b580fd79e49d15b95712f117989584ccd8245e65191f1dfbd0ede638c5a38ded`  
		Last Modified: Fri, 02 Feb 2024 04:04:03 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f49b3fa04a0340b10325926222fd5582c4f4934808fc24db3f674d58ec14da5`  
		Last Modified: Fri, 02 Feb 2024 04:04:04 GMT  
		Size: 3.6 MB (3598324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3edfdc2d0dab4c606057c30ea95c2e60b10b65a113b31be918f944ca9d920a9c`  
		Last Modified: Fri, 02 Feb 2024 04:04:04 GMT  
		Size: 1.4 MB (1440986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca46ef2f60bf0e2ad162d598a95d47cce6ffa4cb980ec0a4ec599890623fb35`  
		Last Modified: Fri, 02 Feb 2024 04:04:04 GMT  
		Size: 8.0 MB (8045891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782ccc1a834fa8fbe420383808fb818a8928242553f4f58a8064fb47d68608db`  
		Last Modified: Fri, 02 Feb 2024 04:04:05 GMT  
		Size: 908.7 KB (908697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3b7b6d5909a2744b273277c0621645228c2f6ce949831738dfd72ee04bbf5c`  
		Last Modified: Fri, 02 Feb 2024 04:04:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71ea72386dbbf58703a45b5268eefaf596bfc9ef67c0098f5298eb63f42e6a9`  
		Last Modified: Fri, 02 Feb 2024 04:04:05 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ede5c9fd1c57b3f665936e8138fa970a2e4fd10fe9f49ce1a5eb3bad5a808f`  
		Last Modified: Mon, 12 Feb 2024 23:47:49 GMT  
		Size: 98.3 MB (98271345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304f115bad67b3f66fa75d84bf655ea273714b307f61af1d1dbee294f991f6f6`  
		Last Modified: Mon, 12 Feb 2024 23:47:46 GMT  
		Size: 9.9 KB (9931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ffc818ed10326a4be9f4f1002ffc2efba7e0ce81971cf55e249ac9181cea76`  
		Last Modified: Mon, 12 Feb 2024 23:47:46 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1851fa9226a614c1fa8b6f7dcd862f55c2baa40ce2c53eabba28840e61c02c`  
		Last Modified: Mon, 12 Feb 2024 23:47:46 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e93c476b012585d097e35cebc57008e89aa6ccbd0465578e2a1ce847788eed8`  
		Last Modified: Mon, 12 Feb 2024 23:47:47 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44408bbdfcfa1f02e42355d014ff94a5edc70ca2222c995d141f9d5b8696fc6a`  
		Last Modified: Mon, 12 Feb 2024 23:47:47 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:1015bf953c4a3c72831113fe3fc0bf92f8452fd854070dc63178c8a986c17e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5133200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b4874b36140135c369850634f815e143fabfa61bb098e36ad3488487998e31a`

```dockerfile
```

-	Layers:
	-	`sha256:5e388df34a145b3dba3cbeee8ec7395c1d668e7583a8737575411c327fa3aa17`  
		Last Modified: Mon, 12 Feb 2024 23:47:47 GMT  
		Size: 5.1 MB (5078838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7e7a28df3c7484d01e88c778cfac61c8e2ed9e78d4f6ede473262ce850859ac`  
		Last Modified: Mon, 12 Feb 2024 23:47:46 GMT  
		Size: 54.4 KB (54362 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:5f1956e5fb611bd5a17aa3b53487bc882c9fccbd0cf71379dc00eccf87eec8a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.3 MB (141339450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d42c34bf9440651274e0803e28880a176214c9763298452fac8bfba53bcbbe7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 12 Feb 2024 19:15:38 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Mon, 12 Feb 2024 19:15:38 GMT
CMD ["bash"]
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
ENV GOSU_VERSION=1.16
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
ENV LANG=en_US.utf8
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
ENV PG_MAJOR=16
# Mon, 12 Feb 2024 19:15:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Mon, 12 Feb 2024 19:15:38 GMT
ENV PG_VERSION=16.2-1.pgdg110+2
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 12 Feb 2024 19:15:38 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 12 Feb 2024 19:15:38 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Feb 2024 19:15:38 GMT
STOPSIGNAL SIGINT
# Mon, 12 Feb 2024 19:15:38 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 12 Feb 2024 19:15:38 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f377b685f9e110633951ed4489949788a6c78de3f282f590e03fb5d54e548a94`  
		Last Modified: Wed, 14 Feb 2024 07:33:34 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c328df1d90ea1feadc8dd2e155df9bd28789609e9dc64357f2be2f80abd83a0d`  
		Last Modified: Wed, 14 Feb 2024 07:33:34 GMT  
		Size: 4.3 MB (4309281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953d1af9f2bc6f31028d4dae9db5153c3e39bcd89a5ea0521f134e6946377eee`  
		Last Modified: Wed, 14 Feb 2024 07:33:34 GMT  
		Size: 1.4 MB (1403560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3831bf79ad1e510e6dbd37d57dc2cff1769fff3104edd05ce89ab25dcda19f`  
		Last Modified: Wed, 14 Feb 2024 07:33:35 GMT  
		Size: 8.0 MB (8044003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b26592f7347d7c51e6944273140337bd247259557c9a385e466d95f46c93f4`  
		Last Modified: Wed, 14 Feb 2024 07:33:36 GMT  
		Size: 1.0 MB (1026590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ea78c2425345daadc9770010934c9ec53e2ea2da7b255dacb0c4b5991b7ab5`  
		Last Modified: Wed, 14 Feb 2024 07:33:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375aed027cdb1ae68547c758be6a98f428af8e12dceb329429825f241f2b9a43`  
		Last Modified: Wed, 14 Feb 2024 07:33:36 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3e87f2b14c2156c0424734bae371a500dfe3e1e40aed0ff4ffebcd09425f86`  
		Last Modified: Wed, 14 Feb 2024 07:33:38 GMT  
		Size: 96.5 MB (96464175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afff42eda50b4d79285d31ac2535f2dccdd1b6b1437eef278f7c15631566c46`  
		Last Modified: Wed, 14 Feb 2024 07:33:37 GMT  
		Size: 9.9 KB (9919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6c2bae7e46c35b811d233ba46b133959ed60ce632062073442266da29993c5`  
		Last Modified: Wed, 14 Feb 2024 07:33:37 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7acd229b3cd9bb51107f4279d1c74ddc02eee9b99d932825bdcb39e4fb136a`  
		Last Modified: Wed, 14 Feb 2024 07:33:37 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362f6adfc4185d9962e4ead2337c847e97faf279c2186823307dde4095dbc0b4`  
		Last Modified: Wed, 14 Feb 2024 07:33:38 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f00a9e29f289a0bcf03c8bad41359d466158028d2e60c8349991a452ba87e3a`  
		Last Modified: Wed, 14 Feb 2024 07:33:38 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:288a61be1034cb89879df4fa3f7b3b006c9610bfeee0e152239db6ab2eafd17f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5213806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced7baf58031580d56ff67f23f51913922f39f04846edd788b49522c8ea530f3`

```dockerfile
```

-	Layers:
	-	`sha256:400a07311b468d29cfd21db62f99c7d2e79b0cff5ddad247e97cb8fd294c3e18`  
		Last Modified: Wed, 14 Feb 2024 07:33:34 GMT  
		Size: 5.2 MB (5159632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:288c4bcb6c780ec76134a832be0b2edf40541524394e29dca2ee70f4e2bc3183`  
		Last Modified: Wed, 14 Feb 2024 07:33:34 GMT  
		Size: 54.2 KB (54174 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bullseye` - linux; 386

```console
$ docker pull postgres@sha256:78d9493cba03f0d7792de9d8f26bbadc080a280493e9db5ebbb449005e4db08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147682226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8215263eda9e508e2b1bf0aba697231128423ac12824525c5626a658842ebf35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 12 Feb 2024 19:15:38 GMT
ADD file:9eaee5af136d095dc1dac0ffce0fde09d8f1bd02ff7cb65ee67e00b2a66f34f7 in / 
# Mon, 12 Feb 2024 19:15:38 GMT
CMD ["bash"]
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
ENV GOSU_VERSION=1.16
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
ENV LANG=en_US.utf8
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
ENV PG_MAJOR=16
# Mon, 12 Feb 2024 19:15:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Mon, 12 Feb 2024 19:15:38 GMT
ENV PG_VERSION=16.2-1.pgdg110+2
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 12 Feb 2024 19:15:38 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 12 Feb 2024 19:15:38 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Feb 2024 19:15:38 GMT
STOPSIGNAL SIGINT
# Mon, 12 Feb 2024 19:15:38 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 12 Feb 2024 19:15:38 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1ac8173b08d16f9f136fb0e3ee39999cef7495f924ecb43f3ca4a4eea267cc88`  
		Last Modified: Tue, 13 Feb 2024 00:44:36 GMT  
		Size: 32.4 MB (32407443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74a431c92200b9bb3161aedbaa162dad75d7f645b965d92df591b437c98e09c`  
		Last Modified: Tue, 13 Feb 2024 02:10:53 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a210a21295962eefea8263a270b6638a0fca85d28d79b42a24001203b5095e`  
		Last Modified: Tue, 13 Feb 2024 02:10:54 GMT  
		Size: 4.7 MB (4718007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2a4b244e26cb5c49053f9e6eb34c54c40759228b6fea9a54539a7b0a4fd7e0`  
		Last Modified: Tue, 13 Feb 2024 02:10:53 GMT  
		Size: 1.4 MB (1447364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e1bc3debb2e3db184c365e5d0f80f7242a150c16699c6038a971f23063f799`  
		Last Modified: Tue, 13 Feb 2024 02:10:54 GMT  
		Size: 8.0 MB (8044085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d255d1d01cf7f22f7d399a9caaf2a8441878d5bc21c95070fb86b54a6d88af5e`  
		Last Modified: Tue, 13 Feb 2024 02:10:55 GMT  
		Size: 1.0 MB (1028907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63bce7cf9927ed2b9029b68aabf1bdcf98c16b5fbacbd6efbf8866706d02cd5`  
		Last Modified: Tue, 13 Feb 2024 01:59:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666a13cbe08ecc13c89de7db52320b99c5bd97274ea8b4231fad9298705fdea2`  
		Last Modified: Tue, 13 Feb 2024 02:10:55 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bfa1590d7b8ec27d0c0db7a9f5f17e815f7abf6e02d33ce216cb1edf774fdf8`  
		Last Modified: Tue, 13 Feb 2024 02:11:00 GMT  
		Size: 100.0 MB (100015667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1dd99efca306d5923fa5beec066fe2aa70d55b0634a0f55df5960b278c1e3b`  
		Last Modified: Tue, 13 Feb 2024 02:10:56 GMT  
		Size: 9.9 KB (9917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0bba00abc3e7ebf313534ab21df3f246613ba7fb270f76115cad9e367fc41a7`  
		Last Modified: Tue, 13 Feb 2024 02:10:56 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218b22922c2269bc48e2d2097963a17d5631bc8f21d3baef239c85f88e745714`  
		Last Modified: Tue, 13 Feb 2024 02:10:56 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466d86b83b53d08988d082ed0b9aded9293b61d007eb0e1d6dc74ac037514398`  
		Last Modified: Tue, 13 Feb 2024 02:10:57 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c9f43a0bbc90908d6df0c069021e0c7fa8a0cebe93387040ebfcd277e86c323`  
		Last Modified: Tue, 13 Feb 2024 02:10:57 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:a7e0ef5a52855e5958be66556d537dc6a1c726b65a4a16ec08ef710c9ffcca47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5221011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55218844c5bfde2164f16044e0d00ef66802654379266509e7118f36b160a514`

```dockerfile
```

-	Layers:
	-	`sha256:1e52b4fc5094a971335e6294580d7adaf858daba9659797f8653bcaf134de7f5`  
		Last Modified: Tue, 13 Feb 2024 02:10:53 GMT  
		Size: 5.2 MB (5166718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3fd5f3680b7cd318fa4d52bde64bf25733826534c71c58be3e51471c6194331`  
		Last Modified: Tue, 13 Feb 2024 02:10:53 GMT  
		Size: 54.3 KB (54293 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bullseye` - linux; mips64le

```console
$ docker pull postgres@sha256:8c815320385db5bdef16cdc17ea2ec025f071177774dd02167309e6f4eced4e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.3 MB (139294766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232719db8e6657f0a61ebe4fc4c4c09632e0c79d03ea2ebbea210ec8aa4a8294`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 12 Feb 2024 19:15:38 GMT
ADD file:aec249f679ecc1ccad460833afd79f8f10ccd9378d1275ed1f23fa98cf3f99b6 in / 
# Mon, 12 Feb 2024 19:15:38 GMT
CMD ["bash"]
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
ENV GOSU_VERSION=1.16
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
ENV LANG=en_US.utf8
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
ENV PG_MAJOR=16
# Mon, 12 Feb 2024 19:15:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Mon, 12 Feb 2024 19:15:38 GMT
ENV PG_VERSION=16.2-1.pgdg110+2
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 12 Feb 2024 19:15:38 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 12 Feb 2024 19:15:38 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Feb 2024 19:15:38 GMT
STOPSIGNAL SIGINT
# Mon, 12 Feb 2024 19:15:38 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 12 Feb 2024 19:15:38 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c99d8d33768bdc2aba62f6b3cc956b807c30b43339ac2ffa3db52a47112dd416`  
		Last Modified: Tue, 13 Feb 2024 02:16:36 GMT  
		Size: 29.6 MB (29640432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a849fcac53047c6a6acdc95c4277c2be55f05911a6ad56a8046c4a9a26974ac2`  
		Last Modified: Wed, 14 Feb 2024 20:10:02 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86c4720db1b11d6b2ccbca3df28b0cc228514a7ae1fed2253a93d4c21149be7`  
		Last Modified: Wed, 14 Feb 2024 20:10:02 GMT  
		Size: 4.3 MB (4306009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84f0b230c1022fc59e7f48167f30edcf1a786694dd23f8662535790ddc91985`  
		Last Modified: Wed, 14 Feb 2024 20:10:02 GMT  
		Size: 1.4 MB (1359125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefb58385796b7974e72ab37f9936b0e4d54e8ff7b40d32d177ca27b99fd4089`  
		Last Modified: Wed, 14 Feb 2024 20:10:03 GMT  
		Size: 8.0 MB (8044524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc8161e15c26a63b7dc8145f9a0b6f07f56073ae6866e87ad5c48ddbf1a8321a`  
		Last Modified: Wed, 14 Feb 2024 20:10:04 GMT  
		Size: 1.1 MB (1090288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73db0c123e6878c8e540b29d18ef260c9d7c967916a1d08321240e9bafd76b7`  
		Last Modified: Wed, 14 Feb 2024 20:10:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1079861ffc1fa950d08a7043336b9115b32e2f839bc377b44fb6b40a69ec4acc`  
		Last Modified: Wed, 14 Feb 2024 20:10:04 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba23de10beaf1d22a23706f96e3fde3d05a34d4733a4a7f26041613e2ea54086`  
		Last Modified: Wed, 14 Feb 2024 20:10:14 GMT  
		Size: 94.8 MB (94833624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1f92a1eae3fcc33267d1c2280197bea3d1ace9b1480fecfa91686fb89a8d66`  
		Last Modified: Wed, 14 Feb 2024 20:10:05 GMT  
		Size: 9.9 KB (9923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df99b90510badf008bfc1ec93cf359c870b56fbfae54ec6ab69f330726827f07`  
		Last Modified: Wed, 14 Feb 2024 20:10:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8067e685e9ef13a38ed00c6c0786b6e6ba13b49151fc270c1199bfd7ed742b40`  
		Last Modified: Wed, 14 Feb 2024 20:10:05 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc23ae40d1f0020b28da34ff6de593e031b69e7cd8c0dd4815b0b7be6b663ed`  
		Last Modified: Wed, 14 Feb 2024 20:10:06 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2177cc81cde4c9a25d081bfb796775b88785716431a432368c8f509048979568`  
		Last Modified: Wed, 14 Feb 2024 20:10:06 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:55625e75362ac0b68e6e56e6abcd6b7f92c5a2307e50bcb7d3c2858cf9a312a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 KB (54032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4bb5279437ebe4ebc8157870710c68c95738e647cc060ef614d7067aa8332e5`

```dockerfile
```

-	Layers:
	-	`sha256:b0c220b2bc47998a7339155ecc0bcd5b5581e7e04f8a8dafda376735a6d04f27`  
		Last Modified: Wed, 14 Feb 2024 20:10:01 GMT  
		Size: 54.0 KB (54032 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bullseye` - linux; ppc64le

```console
$ docker pull postgres@sha256:b4addd83fad1799d0de53221932d0538bd6ef7b2d0a2bf6ff2320a37e01da9cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155921189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44ef8d8c866d1fce354f9e67d22c50d022726dc1923cdcf60ea8ff43b71c903f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 12 Feb 2024 19:15:38 GMT
ADD file:f8e53a63f5fbfb32b4bac66dc2b16f2e2d101e5feb6cd9e3b6d3065fb8aee14d in / 
# Mon, 12 Feb 2024 19:15:38 GMT
CMD ["bash"]
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
ENV GOSU_VERSION=1.16
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
ENV LANG=en_US.utf8
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
ENV PG_MAJOR=16
# Mon, 12 Feb 2024 19:15:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Mon, 12 Feb 2024 19:15:38 GMT
ENV PG_VERSION=16.2-1.pgdg110+2
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 12 Feb 2024 19:15:38 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 12 Feb 2024 19:15:38 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Feb 2024 19:15:38 GMT
STOPSIGNAL SIGINT
# Mon, 12 Feb 2024 19:15:38 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 12 Feb 2024 19:15:38 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5c87ba6a2e42f083a6cfdea0d3b1b3bc977a5065ff0087fdbf4fc8dbc7982a38`  
		Last Modified: Tue, 13 Feb 2024 00:44:50 GMT  
		Size: 35.3 MB (35297799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c1746d13079825e197182c79ec2c8a2135831a249be716ae4520181648a265`  
		Last Modified: Wed, 14 Feb 2024 03:39:19 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eab50b99e32ce86dbdd461ab3fe2aa7efa4f356a638e0baa1d9341efbfcc92d`  
		Last Modified: Wed, 14 Feb 2024 03:39:20 GMT  
		Size: 5.1 MB (5131984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3f1ead899fca5f8cf490206be6b3ddbbbfddd19d4bc50a8334227b8905cb7c`  
		Last Modified: Wed, 14 Feb 2024 03:39:20 GMT  
		Size: 1.4 MB (1393565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56cffa70231b833a13ef18fbb7ebea977eaa01ec5f68446aba7c7444849c85c8`  
		Last Modified: Wed, 14 Feb 2024 03:39:20 GMT  
		Size: 8.0 MB (8044234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8daa922a916f7526f9d0bf26e16154af53d09e5cb3f9587b2542eff4110e9742`  
		Last Modified: Wed, 14 Feb 2024 03:39:21 GMT  
		Size: 1.2 MB (1197634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd019bd346b0440efbcb07dd9afe47253363945f07aa7c6027ab6fcf33ca49`  
		Last Modified: Wed, 14 Feb 2024 03:39:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1611064f7c98aeaa3efa83ef48e78ba291c7fd4b65156384538e438e7c740a`  
		Last Modified: Wed, 14 Feb 2024 03:39:22 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5f0b4cd41a200657a99853b39128d846eb94a86095606b613acc0ec3a9543c`  
		Last Modified: Wed, 14 Feb 2024 03:39:25 GMT  
		Size: 104.8 MB (104835208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb804aa7be59ef069a372621af64193e88088403664d315dc338534b98b2b25e`  
		Last Modified: Wed, 14 Feb 2024 03:39:22 GMT  
		Size: 9.9 KB (9923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e663293f6228a542f41a34cad27552f9a60e2023ec9ed29056a58e71ee1a52f3`  
		Last Modified: Wed, 14 Feb 2024 03:39:22 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9074eed7617836e23246c9d773c3fe6e0bfd2e09be8253b020da0ed4c4729d`  
		Last Modified: Wed, 14 Feb 2024 03:39:23 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3616f8c3055e11803e0f4931c92f933b67871613e6c46305bc2b5f155f42bd0`  
		Last Modified: Wed, 14 Feb 2024 03:39:23 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b862cb3c44f5566a19cf0264e6b7dda7f45d92f6535c9b5fbea9200ba16f437c`  
		Last Modified: Wed, 14 Feb 2024 03:39:24 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:f01a1e75bb4488ba0f44b98347ce5f581985c28a851fa76aad96ac47b2e5f6cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5d3b4d27f9aa994a7e183b4e961bac69f131459b7f71c418f0c5f9a83727676`

```dockerfile
```

-	Layers:
	-	`sha256:0fde91d0cd1fa3940ea0f5be67e0b1c2267f76ac0f94fd283fd880208f322eb2`  
		Last Modified: Wed, 14 Feb 2024 03:39:20 GMT  
		Size: 5.2 MB (5161139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb7277af7e75827d615c9e8b7a197e4ca68f60a5be88d05b056b854e120c8f6a`  
		Last Modified: Wed, 14 Feb 2024 03:39:19 GMT  
		Size: 54.2 KB (54226 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bullseye` - linux; s390x

```console
$ docker pull postgres@sha256:9f16ec4579f911f2c1f9065d7a7f0c2397e190b4fe7c3b6d2da1e8c737a5dc9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.3 MB (149332194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e808eb615bfae84cce2c4daf2e310e39ed57f411b46f708da3c8dba2115c042`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 12 Feb 2024 19:15:38 GMT
ADD file:08d247ddc5feae7a34870daaf7096c41de9c1bb9fc04bc305db02fe94b34d2e5 in / 
# Mon, 12 Feb 2024 19:15:38 GMT
CMD ["bash"]
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
ENV GOSU_VERSION=1.16
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
ENV LANG=en_US.utf8
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
ENV PG_MAJOR=16
# Mon, 12 Feb 2024 19:15:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Mon, 12 Feb 2024 19:15:38 GMT
ENV PG_VERSION=16.2-1.pgdg110+2
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 12 Feb 2024 19:15:38 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 12 Feb 2024 19:15:38 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 12 Feb 2024 19:15:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Feb 2024 19:15:38 GMT
STOPSIGNAL SIGINT
# Mon, 12 Feb 2024 19:15:38 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 12 Feb 2024 19:15:38 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2ac5fae051fa0d97737a12baa9ac705d62ae16e9a4ae39eed54e3f977616ce05`  
		Last Modified: Tue, 13 Feb 2024 01:30:53 GMT  
		Size: 29.7 MB (29660168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67fde6c7c99c7969bf0b048d75c95d0630c55cbd1ad0affb04d98e8c5845887`  
		Last Modified: Thu, 15 Feb 2024 14:26:16 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770c49e4cd26f71b339282c61f17a880fa5c4622aac4ef9fbf1db5e6fcea542f`  
		Last Modified: Thu, 15 Feb 2024 14:26:16 GMT  
		Size: 4.2 MB (4195920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c8a12c7746dcd587e1a7bdfbaae6e170b94432e295709aafe95aa03c265015`  
		Last Modified: Thu, 15 Feb 2024 14:26:17 GMT  
		Size: 1.4 MB (1437495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9a6c7c9a357a3fb4344dd25a0a664bbe6c2d409a57b2bd624348a98b4475c9`  
		Last Modified: Thu, 15 Feb 2024 14:26:16 GMT  
		Size: 8.1 MB (8098694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69783d1e9fcd0d9d5a5706d0197f2fd4ed29936061aca59523c09587aaee43fb`  
		Last Modified: Thu, 15 Feb 2024 14:26:17 GMT  
		Size: 1.0 MB (1015235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8094a5d8f89301df4049b21c509bf75fba8dd90904ade691842575ee6443904a`  
		Last Modified: Thu, 15 Feb 2024 14:26:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd66c56529f067cf95113f245050ba8fa310bf4e32adeb0c0617882426c44ba4`  
		Last Modified: Thu, 15 Feb 2024 14:26:17 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afee4bf13f2e30166f4bb161397499a8e7bc613e2b0301d5af106f91ad8d93df`  
		Last Modified: Thu, 15 Feb 2024 14:26:20 GMT  
		Size: 104.9 MB (104903931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73c9f1133f5fbdf5505421a0003dfeab7c8a0467642dcc04bfbf8936cf8c221`  
		Last Modified: Thu, 15 Feb 2024 14:26:18 GMT  
		Size: 9.9 KB (9912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb766f824be4d4961c0db07de0738d705c189d25ace922c486cc756f43301254`  
		Last Modified: Thu, 15 Feb 2024 14:26:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593f7dfb9594fabbbb58e32c73eb88a5bc3f1296fb24c6089a9fc1fd2aa1a069`  
		Last Modified: Thu, 15 Feb 2024 14:26:18 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371f26f14aa8a507563bbf9dcaaa3093e312da1ffc4a3e94a3d194d3b80fb98b`  
		Last Modified: Thu, 15 Feb 2024 14:26:19 GMT  
		Size: 5.4 KB (5413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f08fbb1240981a05038cbd96cdffb9491ca29c0dc4359c42ece099ffc5397f1`  
		Last Modified: Thu, 15 Feb 2024 14:26:19 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:434b5fbba05a22a53a4c8e3bc8127ea5b5e57bcb2cd008b4fda54025c803ad38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5207150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6c7e693c4ef2409b93e382d6b7f939d2f18f8d1708b6d6d8830b019b4d1889`

```dockerfile
```

-	Layers:
	-	`sha256:f56909cc306a9cdd51cac96872d28bdcbacd6e83d43bb85758340315c9563070`  
		Last Modified: Thu, 15 Feb 2024 14:26:16 GMT  
		Size: 5.2 MB (5152978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f65a1ce33f1b46ced05a8939c9d73961e771c4098ee222b426dca26bdbab317d`  
		Last Modified: Thu, 15 Feb 2024 14:26:16 GMT  
		Size: 54.2 KB (54172 bytes)  
		MIME: application/vnd.in-toto+json
