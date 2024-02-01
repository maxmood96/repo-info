## `postgres:16-bookworm`

```console
$ docker pull postgres@sha256:1392fac43b459bf1eb8a0dee037facc4d95f499e815b8fd5d4cbaf09033415e6
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
$ docker pull postgres@sha256:60c91e0203ae5ccca0a251953742752cd16a129db181bc15559cca71420b188c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.0 MB (152959510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75b7bff7c3ad1ae4468a2107724459061dc87d2176f8f02747a360c32b8c58b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 04 Jan 2024 21:52:40 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 04 Jan 2024 21:52:40 GMT
CMD ["bash"]
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV GOSU_VERSION=1.16
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV LANG=en_US.utf8
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_MAJOR=16
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_VERSION=16.1-1.pgdg120+1
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 04 Jan 2024 21:52:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jan 2024 21:52:40 GMT
STOPSIGNAL SIGINT
# Thu, 04 Jan 2024 21:52:40 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 04 Jan 2024 21:52:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d49150dabe2486c7b35dbe0ea864b690e079fa1b48ef77d1e4533d96b4051e7`  
		Last Modified: Fri, 12 Jan 2024 00:23:46 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d6a86d0fbff788e398befc7b6139bed448853e3a113ea6b2c6c97783f4d8a1`  
		Last Modified: Fri, 12 Jan 2024 00:23:46 GMT  
		Size: 4.5 MB (4533284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9385c30bce0478ebb3d7b8cd3ae66e9b211e980669bd0d67f3bb38b8bfaa40`  
		Last Modified: Fri, 12 Jan 2024 00:23:46 GMT  
		Size: 1.4 MB (1446015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550091272acc768f00ff9a7ae977f9c558f5d3364cd5f87fabcc452d6f677b0e`  
		Last Modified: Fri, 12 Jan 2024 00:23:46 GMT  
		Size: 8.1 MB (8066078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2720859ac49e9505ac9b95a3937053a3e0c2bb623b4bb6f49468c20ef7db8bc4`  
		Last Modified: Fri, 12 Jan 2024 00:23:47 GMT  
		Size: 1.2 MB (1195875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8091cf535458ca73ced6bb49c25ec769ae88608216e721e6bd1767d36138e3f`  
		Last Modified: Fri, 12 Jan 2024 00:23:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ca5fbd89cdb8212ec43875a45b14a9f1cfda38272896347251e76e0cc383fe`  
		Last Modified: Fri, 12 Jan 2024 00:23:47 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22fbbce47a56e5ceed3d8ec4a588a1adaed23a83c230645206ec26d961f876cd`  
		Last Modified: Fri, 12 Jan 2024 00:23:49 GMT  
		Size: 108.6 MB (108572098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b5e3b65b9594578082fe4f45b479c2de5782344f17d74b7e34a3184000bf28`  
		Last Modified: Fri, 12 Jan 2024 00:23:48 GMT  
		Size: 9.9 KB (9920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917e5b76e085bfd128b12de93138dc43366eefc6efe52bedea5d351a0612b50f`  
		Last Modified: Fri, 12 Jan 2024 00:23:48 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f21ce9572c6e1750cc335372d0d1c6a893da69e3064e7efc961237c5ba63538`  
		Last Modified: Fri, 12 Jan 2024 00:23:48 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea3941c8572e8e5721645ca86d9b9ddc868a5276c899e036d6da84fba9890ec`  
		Last Modified: Fri, 12 Jan 2024 00:23:49 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848fee03c0344030501221daea678a4869e5b9d4da9e4899d25b328bcc3c78a4`  
		Last Modified: Fri, 12 Jan 2024 00:23:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:d75fb3e8a4753c68a7ab34ebe8fef6b7a9c1daa76f202a9fc6fef45c9b844b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5005972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508a8e0f1d5a1c7a21edb987a0baea6c4d00e4c39f4b2603c7e985357057a7c5`

```dockerfile
```

-	Layers:
	-	`sha256:07565998ef8e006180ce8f6c8dad79f6479c3ab13e749c0903b76124f1a58ed1`  
		Last Modified: Fri, 12 Jan 2024 00:23:46 GMT  
		Size: 5.0 MB (4950740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46bab67e38d9182f5a0601980ebcac3c910388f02c9d832cb06b4ebcc6a59ad5`  
		Last Modified: Fri, 12 Jan 2024 00:23:46 GMT  
		Size: 55.2 KB (55232 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:c5f76d46d12230623ddccc341e3d11227258e07ce1c8a11f2d30e3a5aa15627a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.7 MB (145702508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45bf62eb2d063d2ed60fe9c20199c800ad61783623e3e71bf5b6b1715824bdc6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 04 Jan 2024 21:52:40 GMT
ADD file:2e234aad355a61f304982c134eb72c46730200cc475a400c78836ba8761cd52e in / 
# Thu, 04 Jan 2024 21:52:40 GMT
CMD ["bash"]
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV GOSU_VERSION=1.16
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV LANG=en_US.utf8
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_MAJOR=16
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_VERSION=16.1-1.pgdg120+1
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 04 Jan 2024 21:52:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jan 2024 21:52:40 GMT
STOPSIGNAL SIGINT
# Thu, 04 Jan 2024 21:52:40 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 04 Jan 2024 21:52:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7b3d38e58d48b1d7eb80e8663c89d5f32b423059b0dbee65b1dc132a6d707cff`  
		Last Modified: Thu, 11 Jan 2024 01:54:05 GMT  
		Size: 26.9 MB (26885480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0daff41643a0fa72522566af96a807b9d0c2858706e1cb4eed6293185faa7461`  
		Last Modified: Fri, 12 Jan 2024 23:04:26 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd063bd9f6e60c59c2e15d23fc927595a908fa058824ab0bbad5202d654e08a`  
		Last Modified: Fri, 12 Jan 2024 23:04:26 GMT  
		Size: 4.2 MB (4150631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa76578621e34371ad34e00afc5e1635250e7207d85b2b72f480e38a34ce5f1`  
		Last Modified: Fri, 12 Jan 2024 23:04:26 GMT  
		Size: 1.4 MB (1423683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c314126da956b5471a3e19ec5dad4c815cd78ade9db7705e67ec5d8cdf62d1`  
		Last Modified: Fri, 12 Jan 2024 23:04:26 GMT  
		Size: 8.1 MB (8066200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a4e530e6aa5d3ac192d5c343505818119c12aac84fc88398b5cdc0a4c74719`  
		Last Modified: Fri, 12 Jan 2024 23:04:27 GMT  
		Size: 1.2 MB (1194720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6e87ece566294dcd96ec57b001e4888813fc16ad78c736a4ca82ab264560ba`  
		Last Modified: Fri, 12 Jan 2024 23:04:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680b48c79af8efa8235b4e2b2d415cb8ec31264683157014db53ec427ac91f04`  
		Last Modified: Fri, 12 Jan 2024 23:04:27 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3ca62786a5bc7c3e32e2e6c31826a454f72b71b814263ad2c5d4bc3acb52a5`  
		Last Modified: Fri, 12 Jan 2024 23:04:31 GMT  
		Size: 104.0 MB (103961541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680dafca6c9c5f89c70aa6cb96c8fb53f8b85da04f2b7f023ec19b34371e339d`  
		Last Modified: Fri, 12 Jan 2024 23:04:28 GMT  
		Size: 9.9 KB (9931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9713f3bd693a412ba6fe90345a80d86c0a83aa96fb57972811abe93f88e6fa96`  
		Last Modified: Fri, 12 Jan 2024 23:04:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3a1f2b8ded3c7a782d1c5932ce9969b4e5e0c56639948a629d7cc91ae276bb`  
		Last Modified: Fri, 12 Jan 2024 23:04:29 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ca55de3d212383892c87980ca7436a51dead0b5ace17953fba8af8a2eb492f`  
		Last Modified: Fri, 12 Jan 2024 23:04:29 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a3e499c4a0d23aa8f4fb72862fbdd21466cf3e34dc92ac2864f2f5a71b8060`  
		Last Modified: Fri, 12 Jan 2024 23:04:29 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:2e5ab144d53df4c6a2f09467713fe25fcb348ba3c54869d257443d5d4acb0565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5021666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c057c90a983c754afa02640b484c8c5084d18bfbfc505d05d97f7568c140ca76`

```dockerfile
```

-	Layers:
	-	`sha256:dfbc2f1ebec4ae25d0c2dc2b5cd602f3cf37c42bae8b02b4f357b45f50a06a21`  
		Last Modified: Fri, 12 Jan 2024 23:04:26 GMT  
		Size: 5.0 MB (4966371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cae03c803523a157753059d8c08e8987373945d661dd832fcf07269e2edc823`  
		Last Modified: Fri, 12 Jan 2024 23:04:26 GMT  
		Size: 55.3 KB (55295 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:6441aa83a5158d075a6ac653b6af0db873a40caf640d8ba912aa6224b2d34f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140517195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a9b6397983a5829b1c9e141d9144cda80b19bf603aa7f481defd09271a2842b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 04 Jan 2024 21:52:40 GMT
ADD file:d365646158a0cbd9fd6557fb285ff54033d19efa44c8f46080998e8a603120a0 in / 
# Thu, 04 Jan 2024 21:52:40 GMT
CMD ["bash"]
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV GOSU_VERSION=1.16
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV LANG=en_US.utf8
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_MAJOR=16
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_VERSION=16.1-1.pgdg120+1
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 04 Jan 2024 21:52:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jan 2024 21:52:40 GMT
STOPSIGNAL SIGINT
# Thu, 04 Jan 2024 21:52:40 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 04 Jan 2024 21:52:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6e6fe5c6e33442e884612254cc97763ab9fa910c47faa20175f9edcaefda7316`  
		Last Modified: Thu, 11 Jan 2024 02:48:37 GMT  
		Size: 24.7 MB (24718126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e1e58565f82979750dfef91c94af4ff991772f8514853261ea0d7291b7f8e0`  
		Last Modified: Sat, 13 Jan 2024 10:53:24 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8c05aab40abb1822001ed88f8922f8bac0c7586e79337bd4090ae5ff9a84d5`  
		Last Modified: Sat, 13 Jan 2024 10:53:24 GMT  
		Size: 3.7 MB (3742356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27389aca32470807a99667a87625b777cbccb9c1dc7b73312705af9832877a29`  
		Last Modified: Sat, 13 Jan 2024 10:53:24 GMT  
		Size: 1.4 MB (1413415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46474b184044fecba121e7ea081a778812c8edc941fbf9082d39dd325bacfbc1`  
		Last Modified: Sat, 13 Jan 2024 10:53:25 GMT  
		Size: 8.1 MB (8066100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377d65f0a27fbd34c835c8f0592382a7b8535ffecc746f149bb6bf272fe569bc`  
		Last Modified: Sat, 13 Jan 2024 10:53:25 GMT  
		Size: 1.1 MB (1066742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6c2de310ddd7367d0482e994618b9562809c4bf951da597e9cbd92f2b2a9d5`  
		Last Modified: Sat, 13 Jan 2024 10:53:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa0b3b6423d2542152e7e4854b2aeea64c93e448d2ef33e5581686b17ebac13`  
		Last Modified: Sat, 13 Jan 2024 10:53:26 GMT  
		Size: 3.1 KB (3146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0285c9a29c9737eb7aab2894c7dcb4b345ce0143127b1557ca37bc66a7cabbfa`  
		Last Modified: Sat, 13 Jan 2024 10:53:29 GMT  
		Size: 101.5 MB (101490196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a8c114b4d700140a3fbf2ed0e63137672cd3802ea3ebeac8b30b4d612125ab`  
		Last Modified: Sat, 13 Jan 2024 10:53:26 GMT  
		Size: 9.9 KB (9930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f96de3810791560cef6bc466ebbb2a219c8ccb0c4281d883b6b19dd2f50272`  
		Last Modified: Sat, 13 Jan 2024 10:53:27 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee8a04044014258ed6e628dbcac830e14a33a9f15a5805750e972ff1238b9cc`  
		Last Modified: Sat, 13 Jan 2024 10:53:26 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0b457e5949e89d92592f91b830ee9ed4d51fb3b6bbd296d578a985cb0328db`  
		Last Modified: Sat, 13 Jan 2024 10:53:27 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe18a1543057bc5fbb7f22c4445415f5c01e019f66028f381b1f2693f60ea58`  
		Last Modified: Sat, 13 Jan 2024 10:53:28 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:3b1a3e63949b6fbfaf714c1714039212fd7cd3dcc25400ee41c40eb19246a651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5021584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc019237d184138bdf252fb52ebada990e2682cc18964f3a6b73170eb8d21516`

```dockerfile
```

-	Layers:
	-	`sha256:3f80680d75a76f50dd79a5cff293450a791f047f3c59579c4562b1ba8018f15b`  
		Last Modified: Sat, 13 Jan 2024 10:53:25 GMT  
		Size: 5.0 MB (4966289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0d5aaa7a502a514d56236c5c0d253f82df626a4f6c272c28270e85c961f0a45`  
		Last Modified: Sat, 13 Jan 2024 10:53:24 GMT  
		Size: 55.3 KB (55295 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:c24ad689a4df0101e3af801f4de7adea22c38cd383d6221981044b4c21947a2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.1 MB (151134823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:230cf55862f3e6a09449d81b3ef09d87f4d4b4adfa86cf43fd08f76a6c6adbde`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 04 Jan 2024 21:52:40 GMT
ADD file:70e4f0c71f88c97c8db279b998c10d4943954d304ff9f51875c3699a4dc5ee4e in / 
# Thu, 04 Jan 2024 21:52:40 GMT
CMD ["bash"]
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV GOSU_VERSION=1.16
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV LANG=en_US.utf8
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_MAJOR=16
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_VERSION=16.1-1.pgdg120+1
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 04 Jan 2024 21:52:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jan 2024 21:52:40 GMT
STOPSIGNAL SIGINT
# Thu, 04 Jan 2024 21:52:40 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 04 Jan 2024 21:52:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a5573528b1f0cf2f5d87c94fe0aee9d8967d5de98258be9303c3c6fa477824ec`  
		Last Modified: Thu, 11 Jan 2024 02:44:04 GMT  
		Size: 29.2 MB (29157335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc82172cf4e1da71de8f8e0c5446803279c008c9e77d109084bacff18ce16cd`  
		Last Modified: Fri, 12 Jan 2024 16:33:33 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e1eca8a6fb0229f065d444eb8b3bb8cee3f939ae1233f5d2fe46645596a5a9`  
		Last Modified: Fri, 12 Jan 2024 16:33:34 GMT  
		Size: 4.5 MB (4498668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1fc0a750a86381bccdb930d318163bf81d48ffa179824fe92ad5a9e81abedb`  
		Last Modified: Fri, 12 Jan 2024 16:33:34 GMT  
		Size: 1.4 MB (1377993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a271e86404871efc9808dc34eb0ceade900f92955e3898aa76ed8098f9adee`  
		Last Modified: Fri, 12 Jan 2024 16:33:34 GMT  
		Size: 8.1 MB (8066138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee9625544dd3153809df4202d741f737efe677f75ec7fc5e44a60eebf34364f`  
		Last Modified: Fri, 12 Jan 2024 16:33:35 GMT  
		Size: 1.1 MB (1108496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635c7a8eeff6dcc4a18ebcde0ec9275057f6aece5831d5bcbf15ea1d8e596712`  
		Last Modified: Fri, 12 Jan 2024 16:33:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf63625d5452eeed88ad37816c296820f1715de8d308416b6cedc2d509d99428`  
		Last Modified: Fri, 12 Jan 2024 16:33:37 GMT  
		Size: 3.1 KB (3138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d32355dc68b0b31cb6731d9bb3db3269508844b6a42b301974ea732282ba9c`  
		Last Modified: Fri, 12 Jan 2024 16:33:41 GMT  
		Size: 106.9 MB (106905951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f536aa26e61d13b527ee3a4025cacfa2ac581ade0fc14e5ff4ff3bc12a6f153`  
		Last Modified: Fri, 12 Jan 2024 16:33:37 GMT  
		Size: 9.9 KB (9922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218a04a996252ecfc2bb299ecc7b79db8843bc226f89bf0f4b6531d385df0b34`  
		Last Modified: Fri, 12 Jan 2024 16:33:38 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6fdf1d3bc629f6ce268373a09defa4faa1e5c2d82ba95f4fcbfd1a1f89b485`  
		Last Modified: Fri, 12 Jan 2024 16:33:38 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cc1b15465f4e08a40d7724596183bcf88d1c8257c237461190259fa6ae303a`  
		Last Modified: Fri, 12 Jan 2024 16:33:39 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc470d63629a1758ec88e27555c5f760bb084470db5df65ea7846a5aed041b3d`  
		Last Modified: Fri, 12 Jan 2024 16:33:39 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:2e839967422c39f217be8a9e750b7d66b8ae35cc45ad676caf7a46219d7bdd67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5011484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faf6a65f63ae1a8a0bb441f8c717e2cf24d5da976c6da4bf18360337f88dfc03`

```dockerfile
```

-	Layers:
	-	`sha256:4367a391d9c87e9a3d4768a11733c993bdf3fef1191ed3555a5c470a20f0ad3e`  
		Last Modified: Fri, 12 Jan 2024 16:33:34 GMT  
		Size: 5.0 MB (4956404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5737861d050014a5a3381e52651bf08e5449d424b4cd0a3f67be27977e7d552b`  
		Last Modified: Fri, 12 Jan 2024 16:33:33 GMT  
		Size: 55.1 KB (55080 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:132fbaa180790cebd92aa00aae73b0dbc6865d34cda2b70e7770e997a91e1e55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.5 MB (160482271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6b7a5e91f633524dfdb78621f0a77201380f806e7a62bce682de950a24835b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 04 Jan 2024 21:52:40 GMT
ADD file:540e2de73452bd162dd7f630bf29f60e7d2e4a7a5d32a495bedf8ad390b59d7f in / 
# Thu, 04 Jan 2024 21:52:40 GMT
CMD ["bash"]
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV GOSU_VERSION=1.16
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV LANG=en_US.utf8
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_MAJOR=16
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_VERSION=16.1-1.pgdg120+1
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 04 Jan 2024 21:52:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jan 2024 21:52:40 GMT
STOPSIGNAL SIGINT
# Thu, 04 Jan 2024 21:52:40 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 04 Jan 2024 21:52:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:34ef135b45f33052e8e5bca668f9a45a938944a9cf3fb73a46f54a7bf11f091b`  
		Last Modified: Wed, 31 Jan 2024 22:43:46 GMT  
		Size: 30.2 MB (30165018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d76940b3475b82008dc7bd11666a82908b6a3be55f18c51970c64a40bdda19b`  
		Last Modified: Thu, 01 Feb 2024 00:09:25 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe43c5b16aee57a59b9b4169c45ffaf0d55f1fc93debed5f16efcd04cb7c030c`  
		Last Modified: Thu, 01 Feb 2024 00:09:25 GMT  
		Size: 5.0 MB (4964271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6e72bd3e093224ef2d34a3df01ec860ff3d0b7c6c2b3cd5324780c059c20f7`  
		Last Modified: Thu, 01 Feb 2024 00:09:25 GMT  
		Size: 1.4 MB (1425215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66bcc6996b467877d52eb5dae80995077ef7884a2d0e504f9d07d08f76a66ca`  
		Last Modified: Thu, 01 Feb 2024 00:09:26 GMT  
		Size: 8.1 MB (8068693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43fa2068377d419c65945bb759e931e5ef0d8689e1186db658823283556f7d3`  
		Last Modified: Thu, 01 Feb 2024 00:09:26 GMT  
		Size: 1.1 MB (1136960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aaaf54f6d172e1d4a9083181c60cf3baac71e2c369b9f0f718f2fdafe5f295f`  
		Last Modified: Thu, 01 Feb 2024 00:09:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d37fe83db3350c2456a561f015f8bef44fe0fb10f1a5db2dfc715dadfa9241`  
		Last Modified: Thu, 01 Feb 2024 00:09:27 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a6bbbd8b4757d068488820787fc233b62247a6c87746c663385fcc19ce6126`  
		Last Modified: Thu, 01 Feb 2024 00:09:30 GMT  
		Size: 114.7 MB (114701852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d3ae6ca05415ef2a4be1293cc606cfbabecdeddfe1562e3220b18ca00dfbad`  
		Last Modified: Thu, 01 Feb 2024 00:09:27 GMT  
		Size: 9.9 KB (9930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea27d30efe7034364cba9f488a67f103015c9d70ff0b6a43f1fa51e963de691`  
		Last Modified: Thu, 01 Feb 2024 00:09:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b163308be6a2836583623d2c0cd8e8ee3ee73af2efb65be2ff0e3583724ba01`  
		Last Modified: Thu, 01 Feb 2024 00:09:28 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98cabcffbbf3e82ddddc65c5b79cfb8e3ae7ab07938087cc96bf937d5a841b07`  
		Last Modified: Thu, 01 Feb 2024 00:09:29 GMT  
		Size: 5.4 KB (5427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15de253dd621ba131938cf47929e0552b42f40aece953e6d7550710991ee77d`  
		Last Modified: Thu, 01 Feb 2024 00:09:29 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:eebb0dc8fed8edeaddc5f0ee0eb90010dc7df9a1006eda4e6c05a34f1c1438f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5019251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e18827194f437ef9f09035d71a9c8bba5ac8a78252e907586be8b33f5d7497d1`

```dockerfile
```

-	Layers:
	-	`sha256:ce9e5a2067544bfb100ba42f4a7c3a3f1b9da08a94a9e2db25705e65bdfdae36`  
		Last Modified: Thu, 01 Feb 2024 00:09:25 GMT  
		Size: 5.0 MB (4964080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb052e432ac95d714d0192a12cc1265d95801334af372e2b28602bc09bb813b1`  
		Last Modified: Thu, 01 Feb 2024 00:09:25 GMT  
		Size: 55.2 KB (55171 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:29e9ea5dcaeb7a7971d1cb2b9a02b4a4013db0741a1b57e51a7a181238190e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (149010022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:792cf4e5840b79fb7ccd71394e57374a884718bb9a83fa6fac86b03dfbfbbfb2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 04 Jan 2024 21:52:40 GMT
ADD file:61bc6da4a8a8247e6b88cf149051dbb04a6a5e6e1ffc5da16a85d1b4f24be297 in / 
# Thu, 04 Jan 2024 21:52:40 GMT
CMD ["bash"]
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV GOSU_VERSION=1.16
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV LANG=en_US.utf8
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_MAJOR=16
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_VERSION=16.1-1.pgdg120+1
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 04 Jan 2024 21:52:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jan 2024 21:52:40 GMT
STOPSIGNAL SIGINT
# Thu, 04 Jan 2024 21:52:40 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 04 Jan 2024 21:52:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4f1541106f1f6cee2d65a870d8d3fbbaef35e04dbcb8abaa9623a9f7137a6ae5`  
		Last Modified: Thu, 11 Jan 2024 02:22:46 GMT  
		Size: 29.1 MB (29121397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ad520a96a04a7b07ae7276068811e7be2f6b3c893f8f501148ab22d9123051`  
		Last Modified: Fri, 12 Jan 2024 18:49:07 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a8cc4e15a0bd2e0dd18cfdd871fb18c70de72a2c2047fc41b3974837f671a8`  
		Last Modified: Fri, 12 Jan 2024 18:49:07 GMT  
		Size: 4.5 MB (4474314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace438eed986509b8dd0ac0a74837725ffccc65a18f4366521a2bd66176032e2`  
		Last Modified: Fri, 12 Jan 2024 18:49:07 GMT  
		Size: 1.3 MB (1333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bea0096f07703dadc7534d077174838b5d57409c8d06d25102c14adf4bbf189`  
		Last Modified: Fri, 12 Jan 2024 18:49:08 GMT  
		Size: 8.1 MB (8066287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e8afb089fefbbd58eba4ead87c6b756393ef17db70551ccebcd6f5f23c3ab7`  
		Last Modified: Fri, 12 Jan 2024 18:49:08 GMT  
		Size: 1.2 MB (1182393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bf1fd380db0177f4a529c9948a1c7673692ec56a94240cdd73b908a9ca65e6`  
		Last Modified: Fri, 12 Jan 2024 18:49:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8bb5e025396c26c33053eeee6bdb542908a5aa743ab3dc208972d9416e3aab`  
		Last Modified: Fri, 12 Jan 2024 18:49:09 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141082f5b9244f2afc23c2c4feed2e52ab1067c7148fd18ec5d9d1a0fecefe24`  
		Last Modified: Fri, 12 Jan 2024 18:49:19 GMT  
		Size: 104.8 MB (104812003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b404c0df8016d29aeac268ba5335a04423e306b0ffa8f92f6bd3f3a5d461c852`  
		Last Modified: Fri, 12 Jan 2024 18:49:10 GMT  
		Size: 9.9 KB (9933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e880ffed8f24ee57986779b2155a6ea49ef3e42e8d23a8f8ae9602fa91d3b482`  
		Last Modified: Fri, 12 Jan 2024 18:49:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b664bce29a731783a7040e37df833b174f4b5351655b31e600a8a654fb94691c`  
		Last Modified: Fri, 12 Jan 2024 18:49:10 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18aa00eb462ef8d430ddbd3535089d1093045e3720f63f313d31b415da1b3ed`  
		Last Modified: Fri, 12 Jan 2024 18:49:11 GMT  
		Size: 5.4 KB (5425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c29a4e43e34594c0b5d7687bce21bd48a84054ae5a16c032c31ee1b0b6b375`  
		Last Modified: Fri, 12 Jan 2024 18:49:11 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:9cb2dc3263bee1342486f30fb3911ad2f9110b1b3a228a73ba44690cac1c49a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 KB (54959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a17af28a15aec732addcf4a2299ee530aec7b06ba146147ae119c80b22c624c4`

```dockerfile
```

-	Layers:
	-	`sha256:6b08304ffba3515ff5fb4ed6ec6b35ddf59f495eba9569bdb87350f465715db6`  
		Last Modified: Fri, 12 Jan 2024 18:49:07 GMT  
		Size: 55.0 KB (54959 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:b63d39363873a4141b4c36f9f1b1b71698f11593ae15135d5bf483a486b31e83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.3 MB (165283659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c8da6fa0b10e0bf4c1847571c3a3004e82485a22817423b7168f2287bb3660`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 04 Jan 2024 21:52:40 GMT
ADD file:fcbdad385ae78401c4f5aebfeed9ba8edc6adcc9870a328a756cef32458e50ca in / 
# Thu, 04 Jan 2024 21:52:40 GMT
CMD ["bash"]
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV GOSU_VERSION=1.16
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV LANG=en_US.utf8
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_MAJOR=16
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_VERSION=16.1-1.pgdg120+1
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 04 Jan 2024 21:52:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jan 2024 21:52:40 GMT
STOPSIGNAL SIGINT
# Thu, 04 Jan 2024 21:52:40 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 04 Jan 2024 21:52:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5d34c3dd8c95d308ec07fd694f24411653403413305af18811f2d53cc052f152`  
		Last Modified: Thu, 11 Jan 2024 02:39:25 GMT  
		Size: 33.1 MB (33120536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45e5348a348533919da0c9f6ab90e74b60b5e5ee1091ed60e311bb7917115bb`  
		Last Modified: Fri, 12 Jan 2024 14:08:38 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62883857cc12cd89e91cf5575f1057f573e26c164411982a89dd5aee36b797d5`  
		Last Modified: Fri, 12 Jan 2024 14:08:39 GMT  
		Size: 5.4 MB (5367937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cb6281d401abeaf482b2ba1d204204a08e6aaa87d007f75897e54c3d42b201`  
		Last Modified: Fri, 12 Jan 2024 14:08:39 GMT  
		Size: 1.4 MB (1368338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fab73a07e378a6daf6fd877790d897f69e81ea18a19433d34b310c7b52f8cfe`  
		Last Modified: Fri, 12 Jan 2024 14:08:39 GMT  
		Size: 8.1 MB (8066195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5feec01c41e06810fa6bc5edf1d97faa00734a06ca7672b3a2f2f21e3d4de7f`  
		Last Modified: Fri, 12 Jan 2024 14:08:40 GMT  
		Size: 1.3 MB (1283368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e63791e114ae2e34001ffc791919a793308d46333f66956492171fb40f84f5e`  
		Last Modified: Fri, 12 Jan 2024 14:08:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd78780608e34467c1b4c7dc42d41b8cf9b0368498b58d6827b90ece6e0d6d15`  
		Last Modified: Fri, 12 Jan 2024 14:08:40 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc7fe3b210ea6a79d6585807c992968737e1422847a771b1ce96a2bcb2823a3`  
		Last Modified: Fri, 12 Jan 2024 14:08:44 GMT  
		Size: 116.1 MB (116057033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020c92af16d6d6d6babce2062f3d9866e8655b973d3700c45afec6434caceb1e`  
		Last Modified: Fri, 12 Jan 2024 14:08:41 GMT  
		Size: 9.9 KB (9926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47e2eea70d2b3143ddb54fd53239f50c69a2f80d0e2c5c871986924edbfd95b`  
		Last Modified: Fri, 12 Jan 2024 14:08:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eeee0c4a51a349ebc54c4fa46fcbd27bab63be255024839b792024f05974644`  
		Last Modified: Fri, 12 Jan 2024 14:08:41 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c052029d235f7ea88becc719db3a975b729b0fdb73541cb9a53bd7e1dfcf81c5`  
		Last Modified: Fri, 12 Jan 2024 14:08:42 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b528fa25a9717437929d3a22dfd85ec6578424f3ae0f36c23e3bc1b7d066b067`  
		Last Modified: Fri, 12 Jan 2024 14:08:42 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:64772ecfb4e5c851fc5a9d3eeba5eaf44d02178b2c3be8ef7b17c31d4e8eb5d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5013119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e8769bd3250e5467ed17fccb9845ed57824e65ca6927943a96e4a2338f87de7`

```dockerfile
```

-	Layers:
	-	`sha256:8ba50e2a908379fac9d5173d50a5070f4ae04bdd79e496db210bed520855d04e`  
		Last Modified: Fri, 12 Jan 2024 14:08:39 GMT  
		Size: 5.0 MB (4957981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:706d13a469f8893d973a8ab1104586d11542f065b6e4d8a7b77b1518d2237535`  
		Last Modified: Fri, 12 Jan 2024 14:08:38 GMT  
		Size: 55.1 KB (55138 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:a66921e40581ad1e66f2e4a4d560d77c51275187e0c8b7f27d2e7c89b1d8fb76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.7 MB (158653706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b6143c76aae7301a813f2d0ae9dde14d57ba80ceb6296780a8e9a186cd88ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 04 Jan 2024 21:52:40 GMT
ADD file:65dbcebb09bfa0253ba47edc09622e132326164df51df5626ae3a06a0e5d179b in / 
# Thu, 04 Jan 2024 21:52:40 GMT
CMD ["bash"]
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV GOSU_VERSION=1.16
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV LANG=en_US.utf8
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_MAJOR=16
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_VERSION=16.1-1.pgdg120+1
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 04 Jan 2024 21:52:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jan 2024 21:52:40 GMT
STOPSIGNAL SIGINT
# Thu, 04 Jan 2024 21:52:40 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 04 Jan 2024 21:52:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a26174f024d942f0adb6db11b3ae9df606c112928e1b40e24779a0fdab24cb41`  
		Last Modified: Thu, 11 Jan 2024 01:50:51 GMT  
		Size: 27.5 MB (27491850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f78c938787e21daa4679a68403588f16235ab1790964f1a7832a223c681040`  
		Last Modified: Fri, 12 Jan 2024 14:27:04 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fabfaaa468c95dd3c91149470daaafe8e533c4f830f4102c0db7161e29e75d`  
		Last Modified: Fri, 12 Jan 2024 14:27:04 GMT  
		Size: 4.4 MB (4390595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5787b8c97ba87d24ebc8513f128fdb26526acdccfb59bfe6fecaabb29a46cded`  
		Last Modified: Fri, 12 Jan 2024 14:27:05 GMT  
		Size: 1.4 MB (1411882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408a26abbbbfeb74f240d4283dc08f3c52fad57f636641e7a558f90a787e33bc`  
		Last Modified: Fri, 12 Jan 2024 14:27:05 GMT  
		Size: 8.1 MB (8120192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b235a21f80e4a4630d016354a9fd66f71b085100a9b79ba027d7f294b982e15f`  
		Last Modified: Fri, 12 Jan 2024 14:27:05 GMT  
		Size: 1.1 MB (1096499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b45bcb4e62c58d7e9c43acaa8dd748789219f92f5488ca6f05cfa61b669d21b`  
		Last Modified: Fri, 12 Jan 2024 14:27:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:793ed250b77b384e9a642df76cfb14fe6bda87c14aac2fd5a3db31f9c59129c9`  
		Last Modified: Fri, 12 Jan 2024 14:27:06 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe0d42101bdc1ff4cea415ab662d8824a65e3ecab2f5d1d9b6d110153938c76`  
		Last Modified: Fri, 12 Jan 2024 14:27:08 GMT  
		Size: 116.1 MB (116122444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567d37ad210d771048b0bcb20eac830546a565aba06e99b73d2e35cc86a431fb`  
		Last Modified: Fri, 12 Jan 2024 14:27:06 GMT  
		Size: 9.9 KB (9923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2d21319bfd2bc1041a8c9b47aea2fc6017d18dec916393e25b3539f8402a40`  
		Last Modified: Fri, 12 Jan 2024 14:27:06 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a18ae1a9774b68c6672c1af091057393669b7754884ac6bcfaf822fb3bdeb4`  
		Last Modified: Fri, 12 Jan 2024 14:27:07 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8d4ef70f5702ea99828f685087c84e35b28e8ee9e8c56afc6154d231561415`  
		Last Modified: Fri, 12 Jan 2024 14:27:07 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765126a1e0b52326230b05e26b214154d4b3443fb2af48116ec823c7c3c7f1cc`  
		Last Modified: Fri, 12 Jan 2024 14:27:07 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:dce2719466810705b42492975611535934a314ffb39042bd56ccbb0e8d8241d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5004988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536c87088a23f6b3fe1d6f2be174035653ffab9e60eb47375f1ff88a44d80042`

```dockerfile
```

-	Layers:
	-	`sha256:6ec30e131a8cf71f18af6f8c76ddbe29085eebdcf52e2d0eba66b210b26d803e`  
		Last Modified: Fri, 12 Jan 2024 14:27:05 GMT  
		Size: 4.9 MB (4949922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff252c85a9627a5ddf26ae29e3d1645c4b922409a278eb9f33a0e7541e58df96`  
		Last Modified: Fri, 12 Jan 2024 14:27:04 GMT  
		Size: 55.1 KB (55066 bytes)  
		MIME: application/vnd.in-toto+json
