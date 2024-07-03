## `postgres:17beta2-bookworm`

```console
$ docker pull postgres@sha256:148cf704666f792196a37cee28051fb7f0be7e4b4e3e3ae1f42c6bf5428369f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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
	-	linux; s390x
	-	unknown; unknown

### `postgres:17beta2-bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:43d557fea201c9f2675499116b17a0a54d40fd0e8388b75b8d0c1afa504431c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154418484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9031ef916c6a8eea0888585591dd769da6e9d01286222e17a329ee635654b3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 02 Jul 2024 00:03:06 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV LANG=en_US.utf8
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_MAJOR=17
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_VERSION=17~beta2-1.pgdg120+1
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 02 Jul 2024 00:03:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 00:03:06 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19ea388c2bec872f26052268f23911378f5fc22ac81e9995cc3d3e61d69e36c`  
		Last Modified: Tue, 02 Jul 2024 22:06:58 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c50ad8240853980ca761e6b3fb8f73b91e904f3ab012422d0c53675d120f641`  
		Last Modified: Tue, 02 Jul 2024 22:06:58 GMT  
		Size: 4.5 MB (4533692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b5015146a051f69f54dd23e640b37b8b27f6580564e1ab240c1ba2e88e3244`  
		Last Modified: Tue, 02 Jul 2024 22:06:58 GMT  
		Size: 1.4 MB (1446649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517054fbb7cfb11ab7aa7b23101f0024f77321aa70f7448e1119960cfeb0d422`  
		Last Modified: Tue, 02 Jul 2024 22:06:58 GMT  
		Size: 8.1 MB (8066219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b54b1126e4b1b72524cbb615071a0ae08374db66cdd3ea9de0408831f357b4`  
		Last Modified: Tue, 02 Jul 2024 22:06:59 GMT  
		Size: 1.2 MB (1196028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140ec7a1eb743527f5b4cc26add6755313bb0312d11780c258bb511466176a20`  
		Last Modified: Tue, 02 Jul 2024 22:06:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4ab75c5128b54fc1455a55e447fe6bcd4953bdd693e80f96fed7e915d2daed`  
		Last Modified: Tue, 02 Jul 2024 22:06:59 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341918a1557ad5daca4dad347c101d9afd5925cfa98013600674f4bbb1a203a7`  
		Last Modified: Tue, 02 Jul 2024 22:07:01 GMT  
		Size: 110.0 MB (110029060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4466a16e5cbb92c30220be91afc0bd33e40b71039561a41604bd5f86073c93`  
		Last Modified: Tue, 02 Jul 2024 22:07:00 GMT  
		Size: 10.2 KB (10238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43b5a58d9d319fcf264aecbecb3b48fcd6f97451032e23ce76e88c7e4fd82ca`  
		Last Modified: Tue, 02 Jul 2024 22:07:00 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79766f3d718d511a93c6a1450b7e7ec2df948011804a5bf7e65f6bf012e02136`  
		Last Modified: Tue, 02 Jul 2024 22:07:00 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1344052c07c34788effdf9ff603e8505f56317ca9a313bd3b6fde3c29f36b47`  
		Last Modified: Tue, 02 Jul 2024 22:07:01 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb48a067d3bfef88e3d7b408862739fbbf273fb2e8ab072e81d873ac4a5c652`  
		Last Modified: Tue, 02 Jul 2024 22:07:01 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta2-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:40c88deed609ba1b7b91b69daca472536cbcbf381e5dc4f5378d6c511a0a7a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5782014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43e851b5f645e4595bf5fcf8ef4c4874cfc72bceb1d0a61acde4b94f2f0af277`

```dockerfile
```

-	Layers:
	-	`sha256:baaf86825baff84541eb537dc72ec03e1c1043e4458bd6251d71add670a9d031`  
		Last Modified: Tue, 02 Jul 2024 22:06:58 GMT  
		Size: 5.7 MB (5728064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c501808843401aba13a4390963ff430380a4745a6b0254677f2cdc854e0d0599`  
		Last Modified: Tue, 02 Jul 2024 22:06:58 GMT  
		Size: 54.0 KB (53950 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta2-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:89fd8687fb247a0eea2c8f20204933692c57db1850db410d65b4ef0d028d7a1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.1 MB (147128622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a87a33e5ebe2165272932d41eb8c1158dcbe6ddc6a4294fa3ee9c83b283afaf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 02 Jul 2024 00:03:06 GMT
ADD file:acd64fd8017b050fbd1031cf3a9abb59fd15c600649b9467c16029cc6bfd11d5 in / 
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV LANG=en_US.utf8
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_MAJOR=17
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_VERSION=17~beta2-1.pgdg120+1
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 02 Jul 2024 00:03:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 00:03:06 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a8f08669f346f00b060b912e835bd6c163fca9818f070c730d6ffcc249497315`  
		Last Modified: Tue, 02 Jul 2024 00:51:30 GMT  
		Size: 26.9 MB (26887286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59b3a9e9882faa9d7e907cd2cf39b4e5a9bb175421289db1354c98b8b0a18fb`  
		Last Modified: Tue, 02 Jul 2024 16:40:40 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0c327a9fd1068afec744374a2b6aa34d1d645864d5112abf481501763d7117`  
		Last Modified: Tue, 02 Jul 2024 16:40:41 GMT  
		Size: 4.2 MB (4150894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52faa661dbdeeb2aea59010aff6247dcc3800dd9f33f5d8133059fcd240b5b3b`  
		Last Modified: Tue, 02 Jul 2024 16:40:41 GMT  
		Size: 1.4 MB (1423896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dce04a3a04913df4602890ba20f6b6cfc7705c8c882194e9b854aefd0008b3a`  
		Last Modified: Tue, 02 Jul 2024 16:40:41 GMT  
		Size: 8.1 MB (8066339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0be4e27d08771531138ab8f59b7d7cd571b6a494e51770d10f4c40c97356053`  
		Last Modified: Tue, 02 Jul 2024 16:40:42 GMT  
		Size: 1.2 MB (1194832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7963b6f6da8949a382df274dc92805b28274f6337c3f2d541561920a0e5e2564`  
		Last Modified: Tue, 02 Jul 2024 16:40:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853af3d287f4af2be571fc5ef2c2031736521d765ffdd736b515afa8d3e4c7a1`  
		Last Modified: Tue, 02 Jul 2024 16:40:42 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b00a66311b341a9a013b60f4d07fbab3a08b4b45afb7f8e21f1fe572e275cef`  
		Last Modified: Wed, 03 Jul 2024 00:46:15 GMT  
		Size: 105.4 MB (105384806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d6f62e176a1cf8cb281bc413ff789a759e1f57683c7ab6dac0a3f77394ad4b`  
		Last Modified: Wed, 03 Jul 2024 00:46:12 GMT  
		Size: 10.2 KB (10245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6a8154c868adcdeeee7c0f2bea12eb429954b60fccff29c3f0fe34f5d313ef`  
		Last Modified: Wed, 03 Jul 2024 00:46:12 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485f367619e6b15d10732cb193be789c70b922d98c590a0f82d03b92a2f77f98`  
		Last Modified: Wed, 03 Jul 2024 00:46:12 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de658e79ffc2ac5fdf7d3a440ca1bfa0f03b1b7ce72c85edd00846db5de16999`  
		Last Modified: Wed, 03 Jul 2024 00:46:13 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc55d49158b502ff643cb4c7e75d8832306eb1369f66cb0fa6caf2d6c1ab3ef3`  
		Last Modified: Wed, 03 Jul 2024 00:46:13 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta2-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:2eb81e61f3ba93e19429e5386a39e17fad89377299605f9b7659b2f97af425d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5799304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d307a4f5fd2cedc79435a76c88b886515d327951cf0ed40e196c4ba65d23019b`

```dockerfile
```

-	Layers:
	-	`sha256:344b54737b63e54ff1ba3e0d1c05d46e76fd9d86f4b8e8b97eeeb5d75cb0d8d8`  
		Last Modified: Wed, 03 Jul 2024 00:46:12 GMT  
		Size: 5.7 MB (5745159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc61b0e78262bab651d2523ef715b5c4f4544de737a495415eaf8b18c8b51531`  
		Last Modified: Wed, 03 Jul 2024 00:46:12 GMT  
		Size: 54.1 KB (54145 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta2-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:e36666ed4d82df13853d2537e4e66179b4f1323045a7c6e1ed8a571b1333832f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141812537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4750fb7856e5475acba2866e89ca1e1a86b87333d4fcfa3ef3dd0c6614d94da7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 02 Jul 2024 00:03:06 GMT
ADD file:f2c0623bafe70d6e2d8748c6de4eeb93699054f8d34e62c6257b940d4e24e44d in / 
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV LANG=en_US.utf8
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_MAJOR=17
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_VERSION=17~beta2-1.pgdg120+1
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 02 Jul 2024 00:03:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 00:03:06 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:60ec5feb0c17c4f910ca5d3cefbda7bcc1ca066b4482707262696f589dabdcb5`  
		Last Modified: Tue, 02 Jul 2024 01:03:20 GMT  
		Size: 24.7 MB (24718170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e53fefa8d3101e8a0bc5507c0ed94188031a17bf91adbe954428c0b6f880853`  
		Last Modified: Tue, 02 Jul 2024 17:38:54 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251bd0b144b23ad8519d1545774347c063500a775048339f08c87693a7ae0c7f`  
		Last Modified: Tue, 02 Jul 2024 17:38:55 GMT  
		Size: 3.7 MB (3742501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f571c6eedd852ab2a112721e041ac867e8ced9fb15cc28b617bb198dc0a5f27c`  
		Last Modified: Tue, 02 Jul 2024 17:38:54 GMT  
		Size: 1.4 MB (1413606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb95199544118710e4791e822acf08bbf353a975c760b67c8111a2a29ff22e2`  
		Last Modified: Tue, 02 Jul 2024 17:38:55 GMT  
		Size: 8.1 MB (8066234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a277d9c240de0214fe297baa3515bf4f5c57d1d424049c5189ef53db00ed45`  
		Last Modified: Tue, 02 Jul 2024 17:38:56 GMT  
		Size: 1.1 MB (1066926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe0362f9a814b36c0a770f7a004b754bab98fdaec66820ca93c16d857f5c2c5`  
		Last Modified: Tue, 02 Jul 2024 17:38:55 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54ace98cde34cf746c337772c1769e483b6fe872a6632851debeee76df4f7ed`  
		Last Modified: Tue, 02 Jul 2024 17:38:56 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f39fe8b8a113fc17b3d2ffa0f72c0b1a90fbc61d0e833fb7254f703c6415fac`  
		Last Modified: Wed, 03 Jul 2024 04:40:16 GMT  
		Size: 102.8 MB (102784537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2ab008a91afdbe6ccdcea1950dc282ee728ab9d273526160b05979ececa78f`  
		Last Modified: Wed, 03 Jul 2024 04:40:13 GMT  
		Size: 10.2 KB (10241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88fc97c11cdbd7fd3e8d3660d691a84225fc89fb553b81f13433528c834a9f21`  
		Last Modified: Wed, 03 Jul 2024 04:40:13 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2deef30ff369b93cd038ea2492d51a9bd00441164d5edd24954aebe325a5e876`  
		Last Modified: Wed, 03 Jul 2024 04:40:13 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460b70b95ff7b2fb190fff0d9598b7f04ea786e85a5cede438a5cae37a1c47af`  
		Last Modified: Wed, 03 Jul 2024 04:40:14 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4542c7cfb49156b0eb9dc5f30cc3de844727ceafc1b3e47149201eb3945ac41`  
		Last Modified: Wed, 03 Jul 2024 04:40:14 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta2-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:2359ab0de8ab7cd0b2cfb17c7081fef18e502265c822edde7d7be6135d0823ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5799117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63425f7e51a087b83e92bd49e03175c3346f12b79dc36444b5f92ec35f5529cc`

```dockerfile
```

-	Layers:
	-	`sha256:3653f33b5c4227c4edbce5373d6d21be084005d9082e7ea914778b670ca7e893`  
		Last Modified: Wed, 03 Jul 2024 04:40:13 GMT  
		Size: 5.7 MB (5744971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8ff62c1e6740cb427000b83d2d1c84ef742424d51cca61f004c5fc2707a114b`  
		Last Modified: Wed, 03 Jul 2024 04:40:13 GMT  
		Size: 54.1 KB (54146 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta2-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:b52cebbc6d0d452f835719e7f331a723102b780cb702d59d8b7beca19b624265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152585963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f3a34c9b775826931a002e3b054844cb7f01841a6555c364751a4554b88bc89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 02 Jul 2024 00:03:06 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV LANG=en_US.utf8
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_MAJOR=17
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_VERSION=17~beta2-1.pgdg120+1
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 02 Jul 2024 00:03:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 00:03:06 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e8f452626a5ccee4d38885b3c7abbc5a24fc91da8bf6d0090bca8c08c89917`  
		Last Modified: Tue, 02 Jul 2024 19:34:03 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5ffe8e37fb800a5ebcee96f4b496950c85cb79336dc4357ab75a233fa38f4a`  
		Last Modified: Tue, 02 Jul 2024 19:34:04 GMT  
		Size: 4.5 MB (4499208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf69853ae1785d5c0197e614a76cd27d916350886ae4cfe9e621148c0467a903`  
		Last Modified: Tue, 02 Jul 2024 19:34:04 GMT  
		Size: 1.4 MB (1378712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4774f812fbe5e337d3a549344352854c2893bb1719ac1b72ae13ff5c68a3ec`  
		Last Modified: Tue, 02 Jul 2024 19:34:04 GMT  
		Size: 8.1 MB (8066267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40ac180fe1177ed56d6fff78982cd56f02a1aa4d6f4ddca0a1e5006729db29b`  
		Last Modified: Tue, 02 Jul 2024 19:34:05 GMT  
		Size: 1.1 MB (1108672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe791d1413b7a0db4b682de4057e89e9f2039fc2911fdaea504e3f614ff4d90`  
		Last Modified: Tue, 02 Jul 2024 19:34:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3454c459cd32fa0070b58e83027c170d2b2b98018ccfb1e3d623486fda01757`  
		Last Modified: Tue, 02 Jul 2024 19:34:05 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01dd9bf6e7a87a992c1072bd5a3407dee79fa78e28b939eb053e9994863be20`  
		Last Modified: Wed, 03 Jul 2024 03:55:08 GMT  
		Size: 108.4 MB (108355966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f4a89c51f7b7968361e52a406ffe5f45f5d1e7f9d3b6f80008ec1fef8495e4`  
		Last Modified: Wed, 03 Jul 2024 03:55:05 GMT  
		Size: 10.2 KB (10241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26139869428810b116828bd1e6c2d975532148e16603e53f9241727e4209006`  
		Last Modified: Wed, 03 Jul 2024 03:55:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4cbd7879a70c9a50c5063c867133632c697b19440cacf28144bdde187cf45d`  
		Last Modified: Wed, 03 Jul 2024 03:55:05 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9c653bd9e552fc3f5b4e2252f8135b03324ed321b9c8af068371a53976630a`  
		Last Modified: Wed, 03 Jul 2024 03:55:06 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e385b6b07e5b5a65ad839b5d0fa7602bd695f9e464827c2ee24faacb1d637459`  
		Last Modified: Wed, 03 Jul 2024 03:55:06 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta2-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:fe0932e7117e5fc3fa4dcfe3d5becaea1c3a29ae8e6c85399d82790ca34a7537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5788616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c25417da5ca10e191785354772443e4a0bffbe939e774536e20a3072f1231762`

```dockerfile
```

-	Layers:
	-	`sha256:e36fbf716e91fdf943832976673e580ba62a029ce12dce89f646a8d537d37fc4`  
		Last Modified: Wed, 03 Jul 2024 03:55:05 GMT  
		Size: 5.7 MB (5734381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b877bedee724c7ac969818a5d110c3292a0956953b785238a058fd804a5a512f`  
		Last Modified: Wed, 03 Jul 2024 03:55:04 GMT  
		Size: 54.2 KB (54235 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta2-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:32e9fe0c0b547aac76211a6480bd3765aef0b587be957c5df3456c3535695824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162575183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d09c1520b7ec9b4ecfe850f102a4c78b9593adea597ddbae32e37030500f80f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 02 Jul 2024 00:03:06 GMT
ADD file:833af11e99172b5d823c96481bc09ac63041d36ae1212658673bdc5b134499d7 in / 
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV LANG=en_US.utf8
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_MAJOR=17
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_VERSION=17~beta2-1.pgdg120+1
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 02 Jul 2024 00:03:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 00:03:06 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b9519b4198cfa047c0958f7cde32a32d32c6ae3486aea1aefc60e08ecf59449b`  
		Last Modified: Tue, 02 Jul 2024 00:42:41 GMT  
		Size: 30.1 MB (30144275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3ae3540165abd7737f57e9ae7ead261d5922596a736f0155b36275a37fab48`  
		Last Modified: Tue, 02 Jul 2024 22:21:09 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ea06566ade0eca906529ff0786f288f8b67b28aa1ca846754ed10aa766d513`  
		Last Modified: Tue, 02 Jul 2024 22:21:10 GMT  
		Size: 5.0 MB (4965046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e254b46d823ba326ada8f50418b9b04c27d1ee9997efc9fd680b37648f6e39aa`  
		Last Modified: Tue, 02 Jul 2024 22:21:10 GMT  
		Size: 1.4 MB (1422149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582a847e3fe77aaf22def2dece8b20b79644d9b9a8f0a339a2c55eed67b56b3c`  
		Last Modified: Tue, 02 Jul 2024 22:21:10 GMT  
		Size: 8.1 MB (8066261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f218449232749ff831042a295bbcef1aa7f70dab9bfc305d4b58bbffc5a07e`  
		Last Modified: Tue, 02 Jul 2024 22:21:11 GMT  
		Size: 1.1 MB (1137163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30c53f91282df4986686f0e69b90a0e73651d6779bc10f290e2930a426a83ea`  
		Last Modified: Tue, 02 Jul 2024 22:21:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8768285c98495dac4b4beb0022196e9eb15a207a98cfa07d0025a998dcc3342e`  
		Last Modified: Tue, 02 Jul 2024 22:21:11 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5e981c5855ca50646a020cd80b4a9e05c2808f126d79ba2e394bcff8522042`  
		Last Modified: Tue, 02 Jul 2024 22:21:15 GMT  
		Size: 116.8 MB (116819719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1624a093056c53360eafb1497b98ad4ae2a99a115518b44f4e7631bdaf431d1`  
		Last Modified: Tue, 02 Jul 2024 22:21:12 GMT  
		Size: 10.2 KB (10246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6e55e3140bf256bdc491f79f4b679adb536408141e0b8b629816026f684c47`  
		Last Modified: Tue, 02 Jul 2024 22:21:12 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96bfc9c2723e55ed988f6d054f57b1830cf57ab37445fc2c5cb2454db89acf54`  
		Last Modified: Tue, 02 Jul 2024 22:21:12 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1b1b7bfe84c97fa839bb73ae51bc9560467ad0ef3bc30fb7fc3ea949c44497`  
		Last Modified: Tue, 02 Jul 2024 22:21:13 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a70962fb5078056bd6b80a894e667f872b18f1cadb4af2fa491c32ccd05818b`  
		Last Modified: Tue, 02 Jul 2024 22:21:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta2-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:7845a1e4f981b298b1b79632588696a63daf9797c3c78cec3a6dabd945d43dbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5797147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d4b4f5cbc1b63f9e499de7bc4dc66d67fbd28ae13027288f6821f78ab4bfe3d`

```dockerfile
```

-	Layers:
	-	`sha256:eb9fca93848d524f0d0eb17520cc8dfff8e5e235a07faa50971594782cfebfe6`  
		Last Modified: Tue, 02 Jul 2024 22:21:10 GMT  
		Size: 5.7 MB (5743238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:434ad023b23f9fcf519616b0d5a0203762b660d1cf5db0eb1c16b0d93c8921c6`  
		Last Modified: Tue, 02 Jul 2024 22:21:10 GMT  
		Size: 53.9 KB (53909 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta2-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:7343b75d6331fcc1530fed88058c5cfde0107ac0032b27f542c9c8b27c5864de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159935171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f670bcbc00855d740813a9c5460357d575c0594dd203ef2dcbb2c59b36eca126`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 02 Jul 2024 00:03:06 GMT
ADD file:e13e277230efdcc9e4a44bd7a459bf0e65b04440b6bbf292da87f61b4c9ae2fc in / 
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV LANG=en_US.utf8
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_MAJOR=17
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_VERSION=17~beta2-1.pgdg120+1
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 02 Jul 2024 00:03:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 00:03:06 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:407bad4d6e39c8adb6cf98fb11c1bd255ae53204b7059378e0c0f6f76fa3c585`  
		Last Modified: Tue, 02 Jul 2024 00:48:33 GMT  
		Size: 27.5 MB (27490090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8a71948d86c6476b11b03a3ea2a95e21e3693226ea72328ae7dedf03a1fc35`  
		Last Modified: Tue, 02 Jul 2024 08:30:40 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a2e75547f8774b9c8149023948457ce542e5a2e2e61c8c43fb9d4f1953789f`  
		Last Modified: Tue, 02 Jul 2024 08:30:41 GMT  
		Size: 4.4 MB (4390962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b44b5d87690af91260b379c6cba06ffdc18065455215fbe801c42e8cd922924`  
		Last Modified: Tue, 02 Jul 2024 08:30:40 GMT  
		Size: 1.4 MB (1412649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc27b527b2b5661cc83da3e3f8557b11946181aa9b487aac80fd914335bbed62`  
		Last Modified: Tue, 02 Jul 2024 08:30:41 GMT  
		Size: 8.1 MB (8120432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2176ea6ea6e28caf3aa368822939b17a6b887e75a009bbaacb3188e6f4b2e9`  
		Last Modified: Tue, 02 Jul 2024 08:30:41 GMT  
		Size: 1.1 MB (1096716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c12438e4e00cd611e479a010b1d8e419c787cc33704c4f49c9bced295c45cb8`  
		Last Modified: Tue, 02 Jul 2024 08:30:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6d246dc183b24c06f0ae1dd745485fe787dd09e20aa59f769e0d7878ba5e1e`  
		Last Modified: Tue, 02 Jul 2024 08:30:42 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00823aaa2023b9c3b249d5fbb468289b9193d46e7265fe7d17ef11c739ec65a`  
		Last Modified: Wed, 03 Jul 2024 03:23:18 GMT  
		Size: 117.4 MB (117403760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763272d1a8277e561d97af67eed36d81fbd658ce6557ac3f5dadd243b8048ec3`  
		Last Modified: Wed, 03 Jul 2024 03:23:16 GMT  
		Size: 10.2 KB (10239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9849f74f5d41c5f008133c827845408c1e51145623fc4fbca4d0835f65462d`  
		Last Modified: Wed, 03 Jul 2024 03:23:16 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1630459a1f80f6fb9d8fbdb51f52e61c2f5ec1bd4e793f52f70fbdfaa0cbd7`  
		Last Modified: Wed, 03 Jul 2024 03:23:16 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a884cd83744ffb0a0a51e9c464dd68f7b71b50039383d2ce1893294ce19686b`  
		Last Modified: Wed, 03 Jul 2024 03:23:17 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09266f502cf8526cdb2d9aec98f4dd0ca858c8bc35a339efd679667aa0ffe4c0`  
		Last Modified: Wed, 03 Jul 2024 03:23:17 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta2-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:0f4d3efabbf2b3f5c975f11f63a77aaa994b542472389c47f06c986dfb2300d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5781408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6727f5ccda976dce6ba8834613554c2a445a5e195132e90a105b4386002edc2e`

```dockerfile
```

-	Layers:
	-	`sha256:db192008098407cdb5ecab597a35abc7c1fc196e7e919c4617fe0b28345c67df`  
		Last Modified: Wed, 03 Jul 2024 03:23:17 GMT  
		Size: 5.7 MB (5727458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:658ce13003c260289b5948151b56ba5284a282cd6afa8ef1bededf6b9644554e`  
		Last Modified: Wed, 03 Jul 2024 03:23:16 GMT  
		Size: 54.0 KB (53950 bytes)  
		MIME: application/vnd.in-toto+json
