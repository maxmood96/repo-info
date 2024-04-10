## `postgres:bullseye`

```console
$ docker pull postgres@sha256:47a91b42de8bc1faeeb90647cdcdcab811e2be659f88123ec896829fbcd86553
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
$ docker pull postgres@sha256:4e171df642de35dc6deb1e1fc8d00e8a94d28c93ff3f12a40b986372af3634c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.0 MB (144961614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c0686a0dde6d2d77fe954cfe170f140684f17cc67f4a03079aca24e49b0ebe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 21 Feb 2024 00:46:13 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 21 Feb 2024 00:46:13 GMT
CMD ["bash"]
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV GOSU_VERSION=1.17
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV LANG=en_US.utf8
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_MAJOR=16
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_VERSION=16.2-1.pgdg110+2
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 21 Feb 2024 00:46:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Feb 2024 00:46:13 GMT
STOPSIGNAL SIGINT
# Wed, 21 Feb 2024 00:46:13 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 21 Feb 2024 00:46:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20333c6f31ac4229b5b8ce77282381381e7d1dc5b398c52a123bceac52f68b8c`  
		Last Modified: Wed, 10 Apr 2024 02:55:53 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186040651c97a1a0d59c94afab9e7bffe2616cf7d0b8c243a7424d69a5bad83f`  
		Last Modified: Wed, 10 Apr 2024 02:55:54 GMT  
		Size: 4.3 MB (4305787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e240f76f8fc7d9f27d68cdcc73f632b2e8bcd653980856fb9531f45f331b69`  
		Last Modified: Wed, 10 Apr 2024 02:55:54 GMT  
		Size: 1.5 MB (1472189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213c8153be0ac9932808e19ca353c84e6c2ebddc3efd6de44104c92124a4d203`  
		Last Modified: Wed, 10 Apr 2024 02:55:54 GMT  
		Size: 8.0 MB (8044262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c269e14d9973c23cac61eb08c09941e87bf18525b34e327984d2ed1d0038c8`  
		Last Modified: Wed, 10 Apr 2024 02:55:54 GMT  
		Size: 1.0 MB (1038377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21b8876507eb0515ecd4fc7b0b4a3a45fea82b0f296389d6b6228483a977dd8`  
		Last Modified: Wed, 10 Apr 2024 02:55:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e397c567af1a57ab9ce73836d5a037c1d8d9e0d642ee48ba26f6ac645526a430`  
		Last Modified: Wed, 10 Apr 2024 02:55:55 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0322ead07fa8c6c4f6cc030195efbb2d9b8dba7b0a8448af3342291df32a652d`  
		Last Modified: Wed, 10 Apr 2024 02:55:57 GMT  
		Size: 98.7 MB (98652497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67fc509c06b64d9d213989b6411fa592768fb83e8999a10e97053751bc71a21`  
		Last Modified: Wed, 10 Apr 2024 02:55:55 GMT  
		Size: 9.9 KB (9924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73301da916ba246310a4f20a81767ca29301169efb8a77513e1cfd10fc6aecd4`  
		Last Modified: Wed, 10 Apr 2024 02:55:55 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c608b7db135ca164f05ea2a174df3b5f46827a096378e9088f56f9c11318f5`  
		Last Modified: Wed, 10 Apr 2024 02:55:56 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1e37b6f7ff8f14eafe629a59c5b35f9a1eb3d91a337fb7385294ff6573a0f2`  
		Last Modified: Wed, 10 Apr 2024 02:55:57 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031b1749ad91ca7f8e15bf82622e312ac38024cd45f1c379b297d596dd375e06`  
		Last Modified: Wed, 10 Apr 2024 02:55:56 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:51616ade092fed220a0425f405fd20e41a51c55e571ad5634546ae4e714f993d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6019590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc6838232181dda29a706aa3c7b3fff2db1ce67196fda99012d4882b28d07cb2`

```dockerfile
```

-	Layers:
	-	`sha256:1ca8429d7011864cbe6454a9c5f1e705453f05bb192ec2ccfcfbbc591ed72d03`  
		Last Modified: Wed, 10 Apr 2024 02:55:54 GMT  
		Size: 6.0 MB (5965257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88177b72afe2b8a48aba6ffdb535fede8fa32512419d988a2740664153b94958`  
		Last Modified: Wed, 10 Apr 2024 02:55:54 GMT  
		Size: 54.3 KB (54333 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bullseye` - linux; arm variant v5

```console
$ docker pull postgres@sha256:4358de1838e112f7ff2355f552cd03f07780c6ae9d00bb91e275bc095efa403c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137880947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07a9d87b8256eba20e61f2e42091a793ca5abf51dd7e1c412fee61d28cfc2ff0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 21 Feb 2024 00:46:13 GMT
ADD file:90e7b77db704f73ce102dcbc0f6cbe5d778409a08ca0d29224ab736a76537669 in / 
# Wed, 21 Feb 2024 00:46:13 GMT
CMD ["bash"]
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV GOSU_VERSION=1.17
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV LANG=en_US.utf8
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_MAJOR=16
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_VERSION=16.2-1.pgdg110+2
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 21 Feb 2024 00:46:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Feb 2024 00:46:13 GMT
STOPSIGNAL SIGINT
# Wed, 21 Feb 2024 00:46:13 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 21 Feb 2024 00:46:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5f50de7913c8d45142222ead3575799095853dd5af08b7c42fe0f070c5947afc`  
		Last Modified: Tue, 12 Mar 2024 00:52:28 GMT  
		Size: 28.9 MB (28924563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c5856a3b8e5be1e224a1ee1a39380d90720f8d285f60b5f73cf2636a2e6547`  
		Last Modified: Tue, 12 Mar 2024 18:57:17 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe603521bf1e1374d518eab6b011bd2d01f948a4db807bea9340864cc1081c9`  
		Last Modified: Tue, 12 Mar 2024 18:57:17 GMT  
		Size: 4.0 MB (3986200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75534baff662f4ed7f1e8638408c9a0575f1fd50d81aead161579d895e2ae433`  
		Last Modified: Tue, 12 Mar 2024 18:57:17 GMT  
		Size: 1.4 MB (1449148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cdf6040f276d21d348411d17a84f26f827f995c88efc8315af29295107030fb`  
		Last Modified: Tue, 12 Mar 2024 18:57:18 GMT  
		Size: 8.0 MB (8044098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e43ebaae8506f6bbdba7cbb3ca9ac9c27dd929f3257083943db9f757f083aa`  
		Last Modified: Tue, 12 Mar 2024 18:57:18 GMT  
		Size: 1.0 MB (1034881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f806765887474afffb0f6bcf37df0b184d938e2a04f3a3511813c6898bc0d3a8`  
		Last Modified: Tue, 12 Mar 2024 18:57:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391b1037b13dd0ca600f70fc6e3285abb98ed9938a61546eea0fa191c3a5f94b`  
		Last Modified: Tue, 12 Mar 2024 18:57:19 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943fc7dad4e046a3ec4ba5ed36411072858c5928486bfdb81e23cbe67e2ed545`  
		Last Modified: Tue, 12 Mar 2024 18:57:21 GMT  
		Size: 94.4 MB (94421289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36dfa1d22736dd2ba25d5070f09d6eb6e133d7a40ec026c135653b4b4ea8d588`  
		Last Modified: Tue, 12 Mar 2024 18:57:19 GMT  
		Size: 9.9 KB (9926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44915fdb6a9b9d447b8828c53f65f70f2ab3e741c279d4adfaf10be063cc7cf8`  
		Last Modified: Tue, 12 Mar 2024 18:57:19 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3264e50ea9464b16e599ca658faf3468849b5f1d4add93a4a4e8b751e8addb1`  
		Last Modified: Tue, 12 Mar 2024 18:57:20 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6985798c59488d8f06e1e5a68bc53a9eb1a272f6b69e05a049a057163e5115f`  
		Last Modified: Tue, 12 Mar 2024 18:57:20 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9bd82148930e47710bd407d42a5d07df7090658062f4e91c50334c99d661343`  
		Last Modified: Tue, 12 Mar 2024 18:57:21 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:3ba2fd4fec72e35b40b46041df13eda3c8e608b3378cc35b6d23594520c3a96d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6036736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:726ad820b3a5457f750045e788dda1ac87230c70cc68a4bcc6460d05c7ab25d4`

```dockerfile
```

-	Layers:
	-	`sha256:b20c0c440ead1dd21c8b1b069656d01a1726afbe48c06b079cfc6dbfa1caf6e9`  
		Last Modified: Tue, 12 Mar 2024 18:57:17 GMT  
		Size: 6.0 MB (5982365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba0b12859f8ea07219f0750bfb2891009e05fefd5ef921e04495ddef4c6b769c`  
		Last Modified: Tue, 12 Mar 2024 18:57:17 GMT  
		Size: 54.4 KB (54371 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:3167850779c9f829f4c1bc3266cea6b50db68dd93ce0e29e70a7e05a42bb6304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.0 MB (132988631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9319c67fab53528ffb708d2bc9a0bbfec8f254e191e577ce815aa2a174eb42c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 21 Feb 2024 00:46:13 GMT
ADD file:f0436b046c7a5f796efae4d2d2be5a99ad212807e4aa49fc8cc372a4c4c8c4b0 in / 
# Wed, 21 Feb 2024 00:46:13 GMT
CMD ["bash"]
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV GOSU_VERSION=1.17
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV LANG=en_US.utf8
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_MAJOR=16
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_VERSION=16.2-1.pgdg110+2
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 21 Feb 2024 00:46:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Feb 2024 00:46:13 GMT
STOPSIGNAL SIGINT
# Wed, 21 Feb 2024 00:46:13 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 21 Feb 2024 00:46:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5b16029f28c496dabb357a7310d24f957046a925411ccd44eca962c03f85e38e`  
		Last Modified: Tue, 12 Mar 2024 01:04:23 GMT  
		Size: 26.6 MB (26582714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a326173843b66fc111333171528a9fe22768add050409d02b7485338ab16ab`  
		Last Modified: Wed, 13 Mar 2024 06:17:12 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6c614020d76a61e414a44ff02350496d6ee461c289fcad3c626cef742000c9`  
		Last Modified: Wed, 13 Mar 2024 06:17:13 GMT  
		Size: 3.6 MB (3598244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e4d69d393a0699c7bb05fd758a1672accec855a39e97efacea2a826e46af1c`  
		Last Modified: Wed, 13 Mar 2024 06:17:13 GMT  
		Size: 1.4 MB (1439222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac995ce0b360954d6352837e02032c5c81a6d9a94cf26aa66b578f0c43889dd5`  
		Last Modified: Wed, 13 Mar 2024 06:17:13 GMT  
		Size: 8.0 MB (8044085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dc9d78aa559bd1d226475d11f17e70ab88137542a9eee70869cdf713633a7f`  
		Last Modified: Wed, 13 Mar 2024 06:17:14 GMT  
		Size: 908.6 KB (908649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a394c7def46ff9da9f3ac32c6b6b15f9ae9c2ffc7adb5feb961ed75a83be373`  
		Last Modified: Wed, 13 Mar 2024 06:17:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc78a143fe24e6dabb0491e529d27d00cfd53dd1567665568a799999a9eb3a1`  
		Last Modified: Wed, 13 Mar 2024 06:17:14 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e8c5424c79c4b6ead972c17f3ac3808426946be8932ac794387d0d0798a4cf`  
		Last Modified: Wed, 13 Mar 2024 06:17:17 GMT  
		Size: 92.4 MB (92394951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b07d4cf316735db5fc8a101c0cc4a1eb58c615740da686b93b96eb1d73fec1`  
		Last Modified: Wed, 13 Mar 2024 06:17:15 GMT  
		Size: 9.9 KB (9929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1236cdd613fb213b55bdc6471c68416a61324cba950806611e212824c0ae2e5`  
		Last Modified: Wed, 13 Mar 2024 06:17:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea6e8bcea10bbd799f3ecd386d93305b847803d935fc8cd83fd24141542f846`  
		Last Modified: Wed, 13 Mar 2024 06:17:15 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b34b643b386a86d3d1becce7c5efda89c80a7c7a9cf3a49bce52cc9c104e9d9`  
		Last Modified: Wed, 13 Mar 2024 06:17:16 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c325f2762a263a94f1140bcffc4c872855f2ac1097b4d78f9edb92289d7f6d`  
		Last Modified: Wed, 13 Mar 2024 06:17:16 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:e07d7d351ff64bb4149e48375fe58ed11ae667d92f6080e9c09c18867236dd60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6036499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d17f9f1c8e826b6eb32ead6af2260f7e6f45b2f114e29ddb4e9997ced53bad06`

```dockerfile
```

-	Layers:
	-	`sha256:69b47eeb71d865f9a0b40c808737bad08f5e367a3d5049442c2b10a7249e6256`  
		Last Modified: Wed, 13 Mar 2024 06:17:13 GMT  
		Size: 6.0 MB (5982137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1555caadd938b5e2980ae4c250238b96411cddd7a44a9347543d1d1a3f856ea3`  
		Last Modified: Wed, 13 Mar 2024 06:17:12 GMT  
		Size: 54.4 KB (54362 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:d5619c4043dcbc6fbda54c042f578c2874b410058860c76a5db9fce3ccd68c7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.3 MB (141340111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b591f6aba8cb549640a4085f35c6fe473aed7a3441670e7305f3e8b49c38139`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 21 Feb 2024 00:46:13 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Wed, 21 Feb 2024 00:46:13 GMT
CMD ["bash"]
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV GOSU_VERSION=1.17
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV LANG=en_US.utf8
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_MAJOR=16
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_VERSION=16.2-1.pgdg110+2
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 21 Feb 2024 00:46:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Feb 2024 00:46:13 GMT
STOPSIGNAL SIGINT
# Wed, 21 Feb 2024 00:46:13 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 21 Feb 2024 00:46:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815fb7c177c5b4e57970154b0f8662e75fac841d750f99233914446fb70d4239`  
		Last Modified: Wed, 13 Mar 2024 03:54:09 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d330614a949481ad0d2fd9ed020bb7c87a2f3d37ef6088af3a14dc0324bb9b48`  
		Last Modified: Wed, 13 Mar 2024 03:54:10 GMT  
		Size: 4.3 MB (4309270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e4b3930a4d6aed0c0b8c6c9eef4df475d9408ea467dc865e625f0ff5e6c946`  
		Last Modified: Wed, 13 Mar 2024 03:54:10 GMT  
		Size: 1.4 MB (1404074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d9e6bb577d966ae8ea5936e66c8be0364b4fbc963cf39b52db94803e78698e`  
		Last Modified: Wed, 13 Mar 2024 03:54:10 GMT  
		Size: 8.0 MB (8044114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfc6fd417efe7ebd92094ec17b7ff8b3b3ba3a0f82986e835adff9b81ce6f47`  
		Last Modified: Wed, 13 Mar 2024 03:54:11 GMT  
		Size: 1.0 MB (1026592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de146e3dfe18a53e2119505dd9f3ad324d98aa02543bbe515ac2e162b148554`  
		Last Modified: Wed, 13 Mar 2024 03:54:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69aa322e1873ecb9ad41c7d04770a12b9c579eb42f715db79ee3b6eb60f70b6`  
		Last Modified: Wed, 13 Mar 2024 03:54:11 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7dca4b5e36067ef70882275f209c8717c61908994ad2b2b85c88c1b8bcd969`  
		Last Modified: Wed, 13 Mar 2024 03:54:15 GMT  
		Size: 96.5 MB (96464182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e1e2a1397cbb4f8f6b7712048bdd644525c60773631e973c4852c24025b8d3`  
		Last Modified: Wed, 13 Mar 2024 03:54:12 GMT  
		Size: 9.9 KB (9920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f59e443632129903e2dadbaf750052e5d3d64c83c8f8ce0247002d11eb29ae5b`  
		Last Modified: Wed, 13 Mar 2024 03:54:12 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13f5d22e087a81d1dbc06692ae0cdcceea978a48df260a2d62886ac84fe5632`  
		Last Modified: Wed, 13 Mar 2024 03:54:12 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70aeb197d69c12175686a8e7e8a9e36d6923c6797d768d36660bd95396e6b79a`  
		Last Modified: Wed, 13 Mar 2024 03:54:13 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd1e8615aa1ad85bc94b62effaaf63ec1f9250d66a07cca5b0281c2243f268f`  
		Last Modified: Wed, 13 Mar 2024 03:54:13 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:2c0e9aa122dad43a72ae276831aac6cb6b501a416b8982e0b32c2ceefd2cb1ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6025700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cdd3a0d4ee044a924d785ffd726cba5c983b1b5993d92f341f72d76dd79faf7`

```dockerfile
```

-	Layers:
	-	`sha256:cbc98c9347fa1e8b1c707531fcaefe4e9f4b86603658887f0270569832cdf61e`  
		Last Modified: Wed, 13 Mar 2024 03:54:10 GMT  
		Size: 6.0 MB (5971526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7fdf0acd0de40e39c3aa2b070a2465303b7154f86739c59b6dc7e66fef50133`  
		Last Modified: Wed, 13 Mar 2024 03:54:09 GMT  
		Size: 54.2 KB (54174 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bullseye` - linux; 386

```console
$ docker pull postgres@sha256:ffb0e1b0cf1b47e2cf0eb18a8d2ef9d0445acf4a24763213156427a559d33479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147681855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f476dbb9441ab4f64175e275e7d716a50f2b545012d9d6e27d71f365a25ebd62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 21 Feb 2024 00:46:13 GMT
ADD file:515cf6a96eea91239bc61e64b973eb555a9299d1053e3c6cb694d8bafa627086 in / 
# Wed, 21 Feb 2024 00:46:13 GMT
CMD ["bash"]
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV GOSU_VERSION=1.17
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV LANG=en_US.utf8
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_MAJOR=16
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_VERSION=16.2-1.pgdg110+2
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 21 Feb 2024 00:46:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Feb 2024 00:46:13 GMT
STOPSIGNAL SIGINT
# Wed, 21 Feb 2024 00:46:13 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 21 Feb 2024 00:46:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4276507bfa4980b432cd9334306e3335cf1bbc8e6dea45aad2ae9ec091223f03`  
		Last Modified: Tue, 12 Mar 2024 01:03:30 GMT  
		Size: 32.4 MB (32407589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88336346e1d8294260d0233caf8c0b5627b267f808ed39fa0e71c6f95244b84`  
		Last Modified: Tue, 12 Mar 2024 02:12:27 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d3e2be6724138e9765a5934c62325f000863ebf24805f3775eb806a2918ae0`  
		Last Modified: Tue, 12 Mar 2024 02:12:27 GMT  
		Size: 4.7 MB (4718004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1640831142b3feb6fd0f8573128d3e19e1f3edc268771f7bcb5055067f5bbf8d`  
		Last Modified: Tue, 12 Mar 2024 02:12:27 GMT  
		Size: 1.4 MB (1447739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd86428c42bfb329e0491b0f5396a3dbf5b52dba8938510ff5ab691cd635a99`  
		Last Modified: Tue, 12 Mar 2024 02:12:27 GMT  
		Size: 8.0 MB (8044138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd74aae9d46bcfee271bda6a844d6fa5e343c35a9421ad57074613bf6682bff`  
		Last Modified: Tue, 12 Mar 2024 02:12:28 GMT  
		Size: 1.0 MB (1028935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b645de77f56ba326de3bced9da0a96bd084eb0c131e923ccee63d8b3b2ea03`  
		Last Modified: Tue, 12 Mar 2024 02:12:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0963dd448be9dd88c85aa964f33ed218e825016f96187587eb555d0d6f36badf`  
		Last Modified: Tue, 12 Mar 2024 02:12:28 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e64ffc94f0a68fd7e400e74389ce14ab66ce3b1894e80717a0df1c8cf315f10`  
		Last Modified: Tue, 12 Mar 2024 02:12:31 GMT  
		Size: 100.0 MB (100014682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0849fd90df8d10c0e1488258d35e6b2c63d74ff52469ebe08b7c7d2eb1884d7`  
		Last Modified: Tue, 12 Mar 2024 02:12:29 GMT  
		Size: 9.9 KB (9925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0324b8002d1127d6849e414309b0aecfe584760402543857095f2771bacd81d`  
		Last Modified: Tue, 12 Mar 2024 02:12:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c81a56e78d383385f072a2dcbaef2235f30eb5477ca466e03c01edb2142f54`  
		Last Modified: Tue, 12 Mar 2024 02:12:29 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb93edb04046b472e41cf961d1db1d96a7eddfd72a15738fcd36bf85ef75a82c`  
		Last Modified: Tue, 12 Mar 2024 02:12:30 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2310351579894a361aefc394a4ff076f5f44eb76379b9291439e9d1f6f9294d2`  
		Last Modified: Tue, 12 Mar 2024 02:12:30 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:f56e14fd652b2f956966d548bb094aa305fa984b64faadb8fc311f67c104ccb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6033965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676b5e43e81dca65a5cc5284bc42a9366a7c02a4e1be732520491a4400e51447`

```dockerfile
```

-	Layers:
	-	`sha256:186282412f5282ea8b38e52490b338783247b865c221cb05877b323130970f73`  
		Last Modified: Tue, 12 Mar 2024 02:12:27 GMT  
		Size: 6.0 MB (5979672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1704cbaa7ba4e20e6ed3754b963c1bc113a05e219f9c35c021a200d23e0b31ba`  
		Last Modified: Tue, 12 Mar 2024 02:12:27 GMT  
		Size: 54.3 KB (54293 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bullseye` - linux; mips64le

```console
$ docker pull postgres@sha256:574cece48340e34a4e228810c2f5410c53fc8abc4a175daeda5086a1766c3c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.3 MB (139291861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f5388020d150536648778523589234f69f19d056cc92987b4766259ce2ae8e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 21 Feb 2024 00:46:13 GMT
ADD file:a42bb6c1ce6dd3579b82e6f04b91787c20ac276a10c0bc36d42b2b260789343b in / 
# Wed, 21 Feb 2024 00:46:13 GMT
CMD ["bash"]
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV GOSU_VERSION=1.17
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV LANG=en_US.utf8
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_MAJOR=16
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_VERSION=16.2-1.pgdg110+2
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 21 Feb 2024 00:46:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Feb 2024 00:46:13 GMT
STOPSIGNAL SIGINT
# Wed, 21 Feb 2024 00:46:13 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 21 Feb 2024 00:46:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ade123ee9f81df730fd8edfcb3e77a2032d0f4380f0cb466cccda650f64f9560`  
		Last Modified: Tue, 12 Mar 2024 01:18:36 GMT  
		Size: 29.6 MB (29640502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54851bdea03ced6c7d984157aa0a1a3e5e14bf168f106931a8aebe259495048`  
		Last Modified: Wed, 13 Mar 2024 18:22:28 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5508ef346d29eddc839ea0b226d1331621d8e7386dfb6ab193e5f66611225fa9`  
		Last Modified: Wed, 13 Mar 2024 18:22:29 GMT  
		Size: 4.3 MB (4306011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65c565e6fbfdd3733108ae5bc3bac5150d34b67ed2e46c53a8acea345b9a4be`  
		Last Modified: Wed, 13 Mar 2024 18:22:29 GMT  
		Size: 1.4 MB (1359319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a59769c3f4ac39fa453515ae2dedd944532564646a46364f05606c3a5af8705`  
		Last Modified: Wed, 13 Mar 2024 18:22:30 GMT  
		Size: 8.0 MB (8044527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003c99d0cde76ae67c4ceff51ae3cc75a89f60e636dfc88e1055c065bdb3cca3`  
		Last Modified: Wed, 13 Mar 2024 18:22:30 GMT  
		Size: 1.1 MB (1090275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa0af5563662108d043668dcf1f9360c35cbe0ecfb2b640b88b7682282d3501f`  
		Last Modified: Wed, 13 Mar 2024 18:22:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bfe25f808cba17124d0afaf87cf43e97b0657cb4df0977bea5fd4f7c7acb92`  
		Last Modified: Wed, 13 Mar 2024 18:22:31 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f73c6019d3f4161a2dc72b773deee8bd6bd07bb0f8d74319241ba933105cd5`  
		Last Modified: Wed, 13 Mar 2024 18:22:40 GMT  
		Size: 94.8 MB (94830457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8272087b1ec90d33ecff185894591fca40d9535e5c488063949741df0ac97c2`  
		Last Modified: Wed, 13 Mar 2024 18:22:31 GMT  
		Size: 9.9 KB (9924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3dccfdb533b971aa67498eec7438b6181888a63a2cc07dde30bcbdc4024cac`  
		Last Modified: Wed, 13 Mar 2024 18:22:31 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37aaacd92719716af54879088584c6909379b513a38cc97b75183b88f9934455`  
		Last Modified: Wed, 13 Mar 2024 18:22:32 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c601d616f75136dc8bef09bb11dfbfce687e1c490bf8e819559045a948ae7f0`  
		Last Modified: Wed, 13 Mar 2024 18:22:32 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e679e09b3a747637bdf0befad17b3b7373909418edef5cc37b8371f66b6537b7`  
		Last Modified: Wed, 13 Mar 2024 18:22:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:b3180c4f8f8b7a65acd3eb43090aa221929c834853716260efc549452bbc477f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 KB (54032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881a3db16773e8bb160db7f12270d0b2ced813d33e3f6bdb8de77bd885aef2a0`

```dockerfile
```

-	Layers:
	-	`sha256:56e86757289d751cef0c05c33456855d4adb4e93165b16a6f66eda9baad0ec2b`  
		Last Modified: Wed, 13 Mar 2024 18:22:28 GMT  
		Size: 54.0 KB (54032 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bullseye` - linux; ppc64le

```console
$ docker pull postgres@sha256:9a678789137a835f1ae5d794ae9325200acaed5e96178a5b871755f087d04018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155921443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec87e0185c7d5d7669e1b1ec0d2465f7542a34b7b918ccc1f7a5282379b2bda`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 21 Feb 2024 00:46:13 GMT
ADD file:0964343f3addae20bae700c2e575d45b636c3fe2dfed3d7d4b51961f487dad44 in / 
# Wed, 21 Feb 2024 00:46:13 GMT
CMD ["bash"]
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV GOSU_VERSION=1.17
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV LANG=en_US.utf8
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_MAJOR=16
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_VERSION=16.2-1.pgdg110+2
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 21 Feb 2024 00:46:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Feb 2024 00:46:13 GMT
STOPSIGNAL SIGINT
# Wed, 21 Feb 2024 00:46:13 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 21 Feb 2024 00:46:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2717318882616811ceb12e643b0407ce22b67c750fd90122b7150a1571991bed`  
		Last Modified: Tue, 12 Mar 2024 00:38:55 GMT  
		Size: 35.3 MB (35298007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd38cea8876d735deeab58b0615d93ba61b90cd8ecdaefbeca97cd9e9a8d1e7d`  
		Last Modified: Wed, 13 Mar 2024 06:18:14 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5014cc70c59aab029ab26912e043cd81c9b1aea129acd705162ec8df71a12911`  
		Last Modified: Wed, 13 Mar 2024 06:18:15 GMT  
		Size: 5.1 MB (5131934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74d831a47a203f36a05fc61fbf81c68298fefa9dc7003f6a594dee1c1380292`  
		Last Modified: Wed, 13 Mar 2024 06:18:15 GMT  
		Size: 1.4 MB (1393690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cada2c447a9d8c80024ecf0356d968167ae0d7f230d9b39139927db4efe0c44b`  
		Last Modified: Wed, 13 Mar 2024 06:18:15 GMT  
		Size: 8.0 MB (8044311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e004bfbf33e8deaeea9afdfe53c6e202959eec96cfb534de875bfce7ddef3a9`  
		Last Modified: Wed, 13 Mar 2024 06:18:15 GMT  
		Size: 1.2 MB (1197599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed55804b8908b751351fda13f35b40a329a18aed2f728bd4a8c8a5601dbca07b`  
		Last Modified: Wed, 13 Mar 2024 06:18:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205bfba9c66a95f91d53b569d0b9d4400d77d058d8305196d5e7997bc44586ce`  
		Last Modified: Wed, 13 Mar 2024 06:18:16 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bdfb93d54493dddac9721b7cd18f4710a64e2c32683f7c49fcaf6ca62dff3cc`  
		Last Modified: Wed, 13 Mar 2024 06:18:19 GMT  
		Size: 104.8 MB (104835127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2c7b0086016a64a2423b183aaae38b64d5eab5abc5c443437679e588d3aac9`  
		Last Modified: Wed, 13 Mar 2024 06:18:17 GMT  
		Size: 9.9 KB (9928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067bbe598838e838d9a6dad36d22ba2450978319ec24a3e67b6a5c92ce1981b2`  
		Last Modified: Wed, 13 Mar 2024 06:18:17 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203beb526693b39f5e638c6da95415ebc98ea5d6ee6ce47982eefc94a146e3eb`  
		Last Modified: Wed, 13 Mar 2024 06:18:17 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0521af93ecf5c78a11bbcb19e6edbb64f68aeee59a78f04d69a02297fa162315`  
		Last Modified: Wed, 13 Mar 2024 06:18:18 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3661ca94ea332b8f47608d658da1fac72f18ca6bfe275567fc00fc07a8a3fa2`  
		Last Modified: Wed, 13 Mar 2024 06:18:19 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:afbeb2c8b0fdb0e5c60b6bc523c2ceb2b564a44691ee29856f642aa4d62fa7cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6026623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4b43c4301425592a649fdd04d98b36274d558b1697ec3876a7e67c7aa1a2ac`

```dockerfile
```

-	Layers:
	-	`sha256:edbc07963eff519c5aedb507052fbac01ad10b1b9df22eac5e927e2722e9dc9a`  
		Last Modified: Wed, 13 Mar 2024 06:18:14 GMT  
		Size: 6.0 MB (5972397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89e440cb5ea49d3a55821dc7af8b61a6ea8bf1081bde1c90fb2c3b50916659df`  
		Last Modified: Wed, 13 Mar 2024 06:18:14 GMT  
		Size: 54.2 KB (54226 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bullseye` - linux; s390x

```console
$ docker pull postgres@sha256:db8b2b4a3958c4437b407be1e70471aaf208d8485388c87ffc649697b9458c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.3 MB (149333124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b6ea15412cd741fe2f75fba4d7f9fbe5dfccf95d153eb24dd2221f6bf2fd7de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 21 Feb 2024 00:46:13 GMT
ADD file:e121f5164f2335792d17befe564e4a4caf1dec33d5039c8245ce418144782215 in / 
# Wed, 21 Feb 2024 00:46:13 GMT
CMD ["bash"]
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV GOSU_VERSION=1.17
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV LANG=en_US.utf8
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_MAJOR=16
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_VERSION=16.2-1.pgdg110+2
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 21 Feb 2024 00:46:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Feb 2024 00:46:13 GMT
STOPSIGNAL SIGINT
# Wed, 21 Feb 2024 00:46:13 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 21 Feb 2024 00:46:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:840335d52e6c781c13aaaed8df36659831a5cb0747048da9bf578dd19a02b30e`  
		Last Modified: Tue, 12 Mar 2024 01:21:45 GMT  
		Size: 29.7 MB (29660245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd631e610a1c40ebde571592e93c7960a3fa32376cef605c515cfe18f12abd04`  
		Last Modified: Thu, 14 Mar 2024 04:13:10 GMT  
		Size: 1.7 KB (1683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d273bdc3c9e4469d5e7a0bb8b8b7f23b73a5c25d2474b800883123321ef47d`  
		Last Modified: Thu, 14 Mar 2024 04:13:10 GMT  
		Size: 4.2 MB (4195881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a55659f2cb951c9153bb7536bf70de6bd561cd0f8e374fc01ca894d7e9d29b`  
		Last Modified: Thu, 14 Mar 2024 04:13:10 GMT  
		Size: 1.4 MB (1437978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591bd53b644be9ae7684621bdbaa313f00d15c339cdf306e755fa8c3856e92ec`  
		Last Modified: Thu, 14 Mar 2024 04:13:11 GMT  
		Size: 8.1 MB (8098711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f55125936f68b969c4afb8a1a6233a9854b33419eb1c7bc07a187b450820421`  
		Last Modified: Thu, 14 Mar 2024 04:13:11 GMT  
		Size: 1.0 MB (1015276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2841e8230d515791c0be95d343870306101030cb9ef1a6dd3e88c43e8ef3eb5`  
		Last Modified: Thu, 14 Mar 2024 04:13:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8711898aaf938ebb75d471fa3f215e65103776136dc79026b3d2cdb1344a64`  
		Last Modified: Thu, 14 Mar 2024 04:13:12 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f927a0a26f477e4ab3e11ae934bfbe7fc802f71367219b470e6074793ccd84`  
		Last Modified: Thu, 14 Mar 2024 04:13:14 GMT  
		Size: 104.9 MB (104904267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152c91b4d2be8d43c14ec5f3dad3a84fd68adaa08dae1934d3d48979cb1b6abb`  
		Last Modified: Thu, 14 Mar 2024 04:13:12 GMT  
		Size: 9.9 KB (9925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a971b0bc320be1870d220da072c9d89426c374cb9b4d6498201979765a1f92a4`  
		Last Modified: Thu, 14 Mar 2024 04:13:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968f6d73b355cab4607237d1d98fabbafb192ef5bcfbcbf2675eb5a075ef5cbf`  
		Last Modified: Thu, 14 Mar 2024 04:13:13 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d074caba37bdfa2f2322254ed8ebfde5b2cd3f1e6f26929a3a40e5e942918571`  
		Last Modified: Thu, 14 Mar 2024 04:13:13 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a85f33267ef047951f89c667af206b89a2c7965c21c6ec2d3ef87db0e4c51fb`  
		Last Modified: Thu, 14 Mar 2024 04:13:14 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:a4e61884cc92ff7b9fc78bcf00c395556eea9ba3cd1bfad83445da510fccdb8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6018407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:999154ab099dd65c19d02afb7b348153364ce64d0654b3184d03e51c5921668e`

```dockerfile
```

-	Layers:
	-	`sha256:97af2253dd2bf950fac5ea4c44eb461d0aaa4b5fdd7220bab861e9008f3fe024`  
		Last Modified: Thu, 14 Mar 2024 04:13:10 GMT  
		Size: 6.0 MB (5964236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b3d3196a97c1a1aed52aa9b2676ad4b26af6eba01bac0af8ce53b1dda2d0d35`  
		Last Modified: Thu, 14 Mar 2024 04:13:10 GMT  
		Size: 54.2 KB (54171 bytes)  
		MIME: application/vnd.in-toto+json
