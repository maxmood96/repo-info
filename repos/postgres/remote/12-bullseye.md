## `postgres:12-bullseye`

```console
$ docker pull postgres@sha256:d69571130f85280528caed96c9b189e1d32e2be7642bf366a1da6424740febed
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

### `postgres:12-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:52a305224fc8b49381e735508536e8bf0e46148b926ebb9bad52053c11259b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (136044945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0c8f8ccd849395007f40aa1bb2a99148bca0096a63c7604a4de9c1956d94ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 04 Jan 2024 21:52:40 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
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
ENV PG_MAJOR=12
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_VERSION=12.17-1.pgdg110+1
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16f583b63d320dcb0b3306b1ab3b412471d361b1c1c960461113d3fc91838df`  
		Last Modified: Fri, 12 Jan 2024 00:24:13 GMT  
		Size: 1.7 KB (1683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c392dcf26e8170c1afc95e85dddb43e1b5965dd380e677b9accb6af8fed212c9`  
		Last Modified: Fri, 12 Jan 2024 00:24:13 GMT  
		Size: 4.3 MB (4305835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48ed369e9cd62e6005033b40b5684fce7919ffd295b7ab9766f30c0a30324d5`  
		Last Modified: Fri, 12 Jan 2024 00:24:13 GMT  
		Size: 1.5 MB (1473286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5099a86ab9f68368a8b90438235e744c8702db6301dc86350133fb7749a9880`  
		Last Modified: Fri, 12 Jan 2024 00:24:14 GMT  
		Size: 8.0 MB (8045932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d33c22b20433e4ea5a33256419d60f94867b15e159a049f97157be9a2060d6c`  
		Last Modified: Fri, 12 Jan 2024 00:24:14 GMT  
		Size: 1.0 MB (1038369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281d14e2657452d2afafddd393a360c6b8019e4e2a9c6a427b4258f66c53caac`  
		Last Modified: Fri, 12 Jan 2024 00:24:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e526003408bb29052529ff64f39b18eab42621c6b87ab0aaec6a7b46396eb1`  
		Last Modified: Fri, 12 Jan 2024 00:24:14 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37c21d0c9bf3c3e97a7b20cb6d6fc62ee4043b12f0c1cefbe1f4cdc7477188f`  
		Last Modified: Fri, 12 Jan 2024 00:24:18 GMT  
		Size: 89.7 MB (89743703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64dae0609ee82ff5b01f0fee8bb0b6d7ac3f3563f44897091c512c8299cf1ea7`  
		Last Modified: Fri, 12 Jan 2024 00:24:15 GMT  
		Size: 9.0 KB (9023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ee792b3263bf882593101ad22a60b720e2cfb9de431ef462bfa9a4f313ee56`  
		Last Modified: Fri, 12 Jan 2024 00:24:16 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4403c77a008ab10e7822608c3131c15f613b849a9303f59fc0ad250eddeeb9fd`  
		Last Modified: Fri, 12 Jan 2024 00:24:16 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ffde6cea65e60357f5bc847d96b315545192bc86b66d152b8247e009d0180d3`  
		Last Modified: Fri, 12 Jan 2024 00:24:17 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa02dfd332df6eab3f192d9b2e000f244dc1fa5d3a933f787edb269c720d8d2f`  
		Last Modified: Fri, 12 Jan 2024 00:24:17 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:8ca4084e278c35b48a1751ecaa0e7502a9d6dda00fcb595bbcef9f68ae8b5b38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4989785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6dc6794904768116b729c0d5c7bf6bbd3f1cf5a7967e2c63e3c1d1263348bb`

```dockerfile
```

-	Layers:
	-	`sha256:cbc509d848cbbf765d8f66360a14a7c2dd3ad56f3c0ee162beb45efccb1c9f9e`  
		Last Modified: Fri, 12 Jan 2024 00:24:14 GMT  
		Size: 4.9 MB (4935748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1980191589f2b005e0ae33485fab2ab758a8ebf9f3d5e54d7f61473a121363c1`  
		Last Modified: Fri, 12 Jan 2024 00:24:13 GMT  
		Size: 54.0 KB (54037 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bullseye` - linux; arm variant v5

```console
$ docker pull postgres@sha256:26acc61ed70a7e0d58e2e8744eaf461e11a8847be4f73e46fae0346fa7fdf11f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129246838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feff7a30188c5eb9d0850774df911f3318936089dbd657b816b6f44290c8c799`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 04 Jan 2024 21:52:40 GMT
ADD file:771e145a148ba6b03341b2263d20ecc38b89c367acc660ed985638987faa0ae5 in / 
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
ENV PG_MAJOR=12
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_VERSION=12.17-1.pgdg110+1
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:05919bd913f54ba9a5204c51fd89eb54126c4f3f9bf6f1f53f67bd19652a4d14`  
		Last Modified: Thu, 11 Jan 2024 01:54:52 GMT  
		Size: 28.9 MB (28921224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ecfc3a1186cdbe088ecc150da136b2aa7105711a5d20e226c902346d22bfe1`  
		Last Modified: Fri, 12 Jan 2024 23:41:08 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc9a607f4ae56cb1c9c3ba5a800694619e3b0bebbdb60517f1abc797dc48715`  
		Last Modified: Fri, 12 Jan 2024 23:41:09 GMT  
		Size: 4.0 MB (3986206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6726a4c33e1bf380b648f17bd0a8b3c4a0a64d86f1e5fbb3dc60c51c96b346d2`  
		Last Modified: Fri, 12 Jan 2024 23:41:08 GMT  
		Size: 1.5 MB (1450767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0bcd6899b7786c9aa550c02d039309f01ceb1e89be12befec2f6f82c6bcc50`  
		Last Modified: Fri, 12 Jan 2024 23:41:09 GMT  
		Size: 8.0 MB (8045823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553b784013a89333aee0d9bf64c188944cd679bc637409970f898ff7fec8b035`  
		Last Modified: Fri, 12 Jan 2024 23:41:10 GMT  
		Size: 1.0 MB (1034893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477f6d94cea24848de3c6193059f29fcf0fc82284ee965370c3189161fd8ebde`  
		Last Modified: Fri, 12 Jan 2024 23:41:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41fbe4eb2a0f7b4800e84f29b54d49715012ab12717fc4f3842b287ee245fa9`  
		Last Modified: Fri, 12 Jan 2024 23:41:10 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807ddc1e8ecba41bb8a23d08e7d8c600edea6b67df0dafcb304c3c4633bc8399`  
		Last Modified: Sat, 13 Jan 2024 03:10:13 GMT  
		Size: 85.8 MB (85788066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38caab87a682c910e721bb7afe8657fd79f97dbc31d72d87e973a68ff93c6114`  
		Last Modified: Sat, 13 Jan 2024 03:10:10 GMT  
		Size: 9.0 KB (9023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a653bc40c424590de4f73b7b15d706e26d182876a032317629ab92ce151ecfca`  
		Last Modified: Sat, 13 Jan 2024 03:10:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6d10c8ab3b0be7c61a4595feeedff7a0b0fc75e24178b48664665e9311af9e`  
		Last Modified: Sat, 13 Jan 2024 03:10:11 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac258dffee745b803d7244309d2933604f3dd157c4b59be3c42007af929a0f59`  
		Last Modified: Sat, 13 Jan 2024 03:10:11 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b68638f2f2d1fb7059120511b2f25cf520aa62e6b95af67a44bb82db92e091`  
		Last Modified: Sat, 13 Jan 2024 03:10:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:5e7f68b7f7fae5e084f6879bba1e1b43511d000ca191c2287353760ac694ad02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5001320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f044efd3c04414d42b1cd01567f75b2c2684924dabfc520deee6932ceb53f1eb`

```dockerfile
```

-	Layers:
	-	`sha256:5ce1ac543ab614a1ae4aeeaecc93f4d0193c1dff4d6937f5ca1b8e1f9435b339`  
		Last Modified: Sat, 13 Jan 2024 03:10:11 GMT  
		Size: 4.9 MB (4947252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42d5452e3e133c70e7f485e961c3fd859960bf56bd864c24da900f3752ed57f0`  
		Last Modified: Sat, 13 Jan 2024 03:10:10 GMT  
		Size: 54.1 KB (54068 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:cdd1236abc84223d49f4bd95e8d1c655c68831a9ba76273ba54f9ebdedc4a674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.0 MB (123996037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77f558263b48bc6c78001b724f71e67a7fd8dc2912d54c54c5b01c354ddebfd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 04 Jan 2024 21:52:40 GMT
ADD file:1a36d919bfcbaa6b981b71ce99d777d303e69c2d6cb1924992e5a9cd811c11c5 in / 
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
ENV PG_MAJOR=12
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_VERSION=12.17-1.pgdg110+1
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:d976170654fe1bc717306b8bf14dc57d20e331b13e4797bc137e6911aa745a8a`  
		Last Modified: Thu, 11 Jan 2024 02:49:26 GMT  
		Size: 26.6 MB (26578974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d489586cbd07ec5fdc06281232e736aba26f7f1d7bf418d0e1b44969535d5ca2`  
		Last Modified: Sat, 13 Jan 2024 11:29:45 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:747ceaaec02c42ed18cb94d9a9eef6100a68bea88eb10936bc4836736915ad2b`  
		Last Modified: Sat, 13 Jan 2024 11:29:45 GMT  
		Size: 3.6 MB (3598373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc832a229385a25892f5b1b9e67c094b993aefa431b8b5701f9366e179afc4e`  
		Last Modified: Sat, 13 Jan 2024 11:29:45 GMT  
		Size: 1.4 MB (1441004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0deea33e841e2f4e8c51f977f93af62399d8ea5c3513ec55ce0c0bf582e9eec`  
		Last Modified: Sat, 13 Jan 2024 11:29:45 GMT  
		Size: 8.0 MB (8045989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f079a9ecc7de55430058221e0bda865d52605998ca4844679e1c91e86f094b`  
		Last Modified: Sat, 13 Jan 2024 11:29:46 GMT  
		Size: 908.8 KB (908750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e624caf19f8dba3b19d0683e42cd5685d64a33ef5c3694eadd03a83c0f3e5da`  
		Last Modified: Sat, 13 Jan 2024 11:29:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b8e84a59b3d51a7bf575cc96113bf9a2ddb2ad13a593adb45153b67f0a7d21`  
		Last Modified: Sat, 13 Jan 2024 11:29:46 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37d26227cea4a2467f91a1db8e13594cc5c808deb0a8b47baf881e1aa2a1dad`  
		Last Modified: Sat, 13 Jan 2024 16:04:52 GMT  
		Size: 83.4 MB (83403083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd79ed25bcc389cb27d9b9de58da23e0bc16c5272e3aa543ac354449347e67f5`  
		Last Modified: Sat, 13 Jan 2024 16:04:50 GMT  
		Size: 9.0 KB (9027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3026aece7a50fdf1e0a1d8c66ddfed44d04a6a24b79bd91a03ad8d2eb402249`  
		Last Modified: Sat, 13 Jan 2024 16:04:50 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592800f21b7aaea31218e5026fec8d566c9ebbfe566167e7a72b5b6a9fac140a`  
		Last Modified: Sat, 13 Jan 2024 16:04:50 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a816d030727b097677ef0c13907f1226cbc853fab7a69ed62cb17649a056eb9`  
		Last Modified: Sat, 13 Jan 2024 16:04:51 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd4656ad28321d2a715951d55d2cad51387162980c83a4b6d7bae30da016f24`  
		Last Modified: Sat, 13 Jan 2024 16:04:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:360e8abfc37e592517f8766f902a58d94efd4f6279a759ecddca61af4f5c17e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5001189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fed578bbc1ab71da3732d935614c49adc26cc0ae728cb0c95c780af6fca93c2`

```dockerfile
```

-	Layers:
	-	`sha256:1a7627f749063b6cf4f8e692df57decb6f28fc8e3f2054db66d64d36e6a06095`  
		Last Modified: Sat, 13 Jan 2024 16:04:50 GMT  
		Size: 4.9 MB (4947130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05b5fcd0ef22d58e1bd4038ce8431f5ffbec341b2b9948bd3ff98153a52f340a`  
		Last Modified: Sat, 13 Jan 2024 16:04:49 GMT  
		Size: 54.1 KB (54059 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:f1d9bd035437af986ccffd3d8c25f1e1e04029232cf80fd5a8ac75e18a66fb31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.2 MB (131160247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d4c87f240558b227f7a3ad6efe2fa8a87e78e5f81a5cad5a5909d2c94b01872`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 04 Jan 2024 21:52:40 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
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
ENV PG_MAJOR=12
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_VERSION=12.17-1.pgdg110+1
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd04a5b220e5e72942a5fed1546db8418f5b1122dcf298d7282a70a523b70b5c`  
		Last Modified: Fri, 12 Jan 2024 16:34:53 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8334da49cb91b2905cecd82042bca0bd07318c91768d29d4651569d1ed227bcc`  
		Last Modified: Fri, 12 Jan 2024 16:34:54 GMT  
		Size: 4.3 MB (4309248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f7e678cb6006f90a7d4e2b248bc09f12f1e1d3d4665c483fa699e42e38c1a5`  
		Last Modified: Fri, 12 Jan 2024 16:34:53 GMT  
		Size: 1.4 MB (1405367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e80f0daf214aa319e9cf00a68057b77db8faac3e10a47e7442719961a906c12`  
		Last Modified: Fri, 12 Jan 2024 16:34:54 GMT  
		Size: 8.0 MB (8045890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bab5cf7125e54abe925e2e9908bb551cb09dd59b3630fb199ca4268e7b46d56`  
		Last Modified: Fri, 12 Jan 2024 16:34:55 GMT  
		Size: 1.0 MB (1026637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3445db0186aa3a0b5d55cae563c20bf9a7188d8d7b813bc164ce1db00df27d40`  
		Last Modified: Fri, 12 Jan 2024 16:34:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e88f26a372302a9e82866d18787e31107b18ce6e246917992713ed112b48c9`  
		Last Modified: Fri, 12 Jan 2024 16:34:55 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653c5edb5414c99e93d2fc1a418a3b416eca269e6cfa1def05fe40d38638467a`  
		Last Modified: Fri, 12 Jan 2024 16:41:30 GMT  
		Size: 86.3 MB (86289228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22fe865db83021e082331c45befa399120eb91fca9ede0d8d2e900ce5cfc29f`  
		Last Modified: Fri, 12 Jan 2024 16:41:26 GMT  
		Size: 9.0 KB (9021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c4615cadc58182ddea5dd4ffdfe52d460280f65cf334a7e0d2b93e1718821e`  
		Last Modified: Fri, 12 Jan 2024 16:41:26 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5c49eab82ea96e687fbc74cdf9e18e90f7c12ca8cf1a965f663b98e6064b6d`  
		Last Modified: Fri, 12 Jan 2024 16:41:26 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2463893ae4d72e98c7948ca125a441d31bd6b27dacdf979b0fb21f07459eda0`  
		Last Modified: Fri, 12 Jan 2024 16:41:27 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea15d5df813dba480f829fa8b6286c63d9052604d5fde965d5046c29f63a5e2`  
		Last Modified: Fri, 12 Jan 2024 16:41:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:25c4b7dab05d8c906f710fcd492b43453fb5f8bb5e673060638b2becc1301b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4995256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce68df39d36542bd48338a1ef6ae78671e3d46317997ec940dcb22ba480652fa`

```dockerfile
```

-	Layers:
	-	`sha256:32a2a06ae856831e5a7b8c60c14f7fa6efd136d8eb60bebdd01a138f5729cb91`  
		Last Modified: Fri, 12 Jan 2024 16:41:27 GMT  
		Size: 4.9 MB (4941379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5588882a8d7db7d929b1e259e23362b0dec5106ed4d89c679ef08a6efb254205`  
		Last Modified: Fri, 12 Jan 2024 16:41:26 GMT  
		Size: 53.9 KB (53877 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:57c3fe6267ade1620466639117ee1f50f0a16a96078acda313ee0bcbf03b3024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.0 MB (138004738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:835671d36b232818afaeacc974cd7ab10c9071769b2c1c45c63512854bee7ce0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 04 Jan 2024 21:52:40 GMT
ADD file:0e0961062de8ea0706118b883ee7638aae4465761dec06896f1bd28b9fb4b516 in / 
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
ENV PG_MAJOR=12
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_VERSION=12.17-1.pgdg110+1
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:854acbf4b2df9e625a11c0e67025dce58b41d948bb7e5d4d5e708e25489f6e8f`  
		Last Modified: Wed, 31 Jan 2024 22:44:37 GMT  
		Size: 32.4 MB (32402507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9e2e28435fc762653cffec7633b76e3a04b9303a1fede187805e74e2ca001b`  
		Last Modified: Thu, 01 Feb 2024 00:07:21 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af08951a591a6153239dbc0ed51b09572ce2f172c547bcc3219d1377e2749e0c`  
		Last Modified: Thu, 01 Feb 2024 00:07:22 GMT  
		Size: 4.7 MB (4717991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5b0f5d01492a50c29c813d0b75daeeba0f646edbdc20415376ebfc340abb5b`  
		Last Modified: Thu, 01 Feb 2024 00:07:22 GMT  
		Size: 1.4 MB (1449149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b220eec71d7573fbb19dd191381b6849f20a816e7223da142accae73e341ecfa`  
		Last Modified: Thu, 01 Feb 2024 00:07:22 GMT  
		Size: 8.0 MB (8045923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cf092f7d9a451d139120ef71f45c4ea47679e2d4015512b6f91e3137e6c74e`  
		Last Modified: Thu, 01 Feb 2024 00:07:22 GMT  
		Size: 1.0 MB (1028936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef40ed6c3c62fa81c718bae0bb1242e3028b51dea6fca1302a9752ba85da5660`  
		Last Modified: Thu, 01 Feb 2024 00:07:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078d853f7f11865b09390745fd6f64118f0294f9c7a18f7857b45a01fa495efe`  
		Last Modified: Thu, 01 Feb 2024 00:07:23 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac861321787bb4d011ed56707a8a019518f1d0b3f585346a8f9d41aebc1c664b`  
		Last Modified: Thu, 01 Feb 2024 00:07:26 GMT  
		Size: 90.3 MB (90340364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdf04ac53f7652bf741aee140d900cd1eca1d3e93e96c5a8bd309c025db44f8`  
		Last Modified: Thu, 01 Feb 2024 00:07:24 GMT  
		Size: 9.0 KB (9026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115ae3d1a988a50d41dde1752bf8c283a79e3387fd3e903bd5bdc4ee256e22aa`  
		Last Modified: Thu, 01 Feb 2024 00:07:24 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a8e3fbff51ff0398e732597762f4e65f4eec38bd8fbbb74f6ac5ba99178b45`  
		Last Modified: Thu, 01 Feb 2024 00:07:25 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485e42cdeb93a1c6e10f93c4c8e5a9c5ece7cd57bd9b1e8df0ba23b6bd127db6`  
		Last Modified: Thu, 01 Feb 2024 00:07:25 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865207f358794807c662686127677cec45a3c61ae996f574e507b533a6f69a88`  
		Last Modified: Thu, 01 Feb 2024 00:07:25 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:2d01179dd204e0da6aab77ed6e3cf4f6d7c4174d0c9fbe49f22f4750075e903a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4998357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0c8ce2d5ee22548615558d809eef03d7b657e708979bb6517296aaf8f23098e`

```dockerfile
```

-	Layers:
	-	`sha256:03182f1254cf22374f2982092e0873e85ba07bf9a90eeef77f8c60942c7de572`  
		Last Modified: Thu, 01 Feb 2024 00:07:21 GMT  
		Size: 4.9 MB (4944360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1db8018bf4ea68089c8fb0a3505028ff56168c31401f5b6dde98c0769ee7e688`  
		Last Modified: Thu, 01 Feb 2024 00:07:21 GMT  
		Size: 54.0 KB (53997 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bullseye` - linux; mips64le

```console
$ docker pull postgres@sha256:a596fe417a3e61b179a831227358961341f2d4423cc7daec40d46a5acd207b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130852482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64bfdceab186bd310df5c9289579aa72a8a6dfadf4da33653fe8f4996b2bf18b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 04 Jan 2024 21:52:40 GMT
ADD file:45b54e9ac99d4bf84139a07fe13fb123e60dcc91036e007820f717e6ef708912 in / 
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
ENV PG_MAJOR=12
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_VERSION=12.17-1.pgdg110+1
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:ba6b58b3ef4d7a81d629337604645ba2efe91a5e812edd9e2fa732c0647f6f3c`  
		Last Modified: Thu, 11 Jan 2024 02:24:20 GMT  
		Size: 29.6 MB (29636033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fedd32844fc536eeb613a73b00887440c0ba98766c1cf33e3f6cb9a22957032`  
		Last Modified: Fri, 12 Jan 2024 20:03:10 GMT  
		Size: 1.7 KB (1680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e3f7502c24260448de6c5ee7a4227337ce5f7d81adc26a2557eb3bda5dc19f`  
		Last Modified: Fri, 12 Jan 2024 20:03:11 GMT  
		Size: 4.3 MB (4306018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d659dbe6424a799d5a0f335a368489ddf89dd687e030a383f40af14cb9ce43d`  
		Last Modified: Fri, 12 Jan 2024 20:03:10 GMT  
		Size: 1.4 MB (1360894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b05692d78b282dcc8938d9e04fd4a17e2f9a2b39b740be5cba77aca482fb9f`  
		Last Modified: Fri, 12 Jan 2024 20:03:11 GMT  
		Size: 8.0 MB (8046287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b59a6570e07ef7f6bf91d3a3657c2c334fd0dbc40de38ccb79ceca9e6dae18a`  
		Last Modified: Fri, 12 Jan 2024 20:03:11 GMT  
		Size: 1.1 MB (1090267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3323fdbde163faea68a753223d5672641e1690f4175caa547a0b5476de4ed499`  
		Last Modified: Fri, 12 Jan 2024 20:03:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029931f2f6d08512e548b33bcb227a7bcab27efda52759d5866732b2075c272b`  
		Last Modified: Fri, 12 Jan 2024 20:03:12 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aedc46678dbddca300e4b202daae9feb2a72dc4ee4fef0f14d7bea89edadff99`  
		Last Modified: Sat, 13 Jan 2024 05:46:46 GMT  
		Size: 86.4 MB (86393106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ad168cbc8e33edba7f9fc7fc0bd5bc1e2cc9858b4f720d8b24f37ce0c2e3a6`  
		Last Modified: Sat, 13 Jan 2024 05:46:37 GMT  
		Size: 9.0 KB (9033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecfb9464efc1853b6eccac6137eb3df9ff3ff53a5414d43ee36c67293269dec1`  
		Last Modified: Sat, 13 Jan 2024 05:46:37 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69966774ae023eafe4413f9547f23e18f9a5844344b43fd8294bf8e1d3c6d584`  
		Last Modified: Sat, 13 Jan 2024 05:46:37 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc26fcf7a63dea7ad2f73b23e9e8dada2962a982e67b2d1da9fdf22fe3d2d2d`  
		Last Modified: Sat, 13 Jan 2024 05:46:38 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4301b54c4b174c93b0c53340642806bee56172311116709e6c8db09c4eb8e031`  
		Last Modified: Sat, 13 Jan 2024 05:46:38 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:3b760b4054af1bf7f60a0bde0709dfb3455eae0c8cb2d362bc3086a166ee5643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 KB (53728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dba83773c2c178d563ba12b6d45a2a5923a07c645084cbe082b93b8b140c1cd5`

```dockerfile
```

-	Layers:
	-	`sha256:a46915c742693c37589d65e64732cfcd61397839123fa105473d69c7fbb690f5`  
		Last Modified: Sat, 13 Jan 2024 05:46:37 GMT  
		Size: 53.7 KB (53728 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bullseye` - linux; ppc64le

```console
$ docker pull postgres@sha256:ac2e61202a6ec27a91c77ad1488d5d47bc116dd6c783dea127d3b1bd5e265c14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.0 MB (144998408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25efa46bda56d0c1407ccd338d7f25a32a1df664bbdea8c84e816ca2234dcdcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 04 Jan 2024 21:52:40 GMT
ADD file:577ec786dad9a86344b678e69a7f514c3deede7cc45d9b3c9088449060272d55 in / 
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
ENV PG_MAJOR=12
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_VERSION=12.17-1.pgdg110+1
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:4c9dbec0f2ecfefcce502a32967ad48a18396e58a4950f972d672b4d95c84bcc`  
		Last Modified: Thu, 11 Jan 2024 02:40:16 GMT  
		Size: 35.3 MB (35293800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7320e40316e83835365d6bc4b86b0c40ebf8e8a253fb0d24497757bb16dc0f`  
		Last Modified: Fri, 12 Jan 2024 14:11:50 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f38bb18486d7f190fa9c68e7722d23cc6dd1b874c21184fb10fdaed1883892`  
		Last Modified: Fri, 12 Jan 2024 14:11:52 GMT  
		Size: 5.1 MB (5131988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970497d7dab5162dc526fd22b57be24601fed76a5aeaeb829410e7c05be3bb5f`  
		Last Modified: Fri, 12 Jan 2024 14:11:51 GMT  
		Size: 1.4 MB (1394945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d75ae680acd425f5b9ab7ee4f6dc1509b9ad14ee0926a714aeaecf4dd685a0b`  
		Last Modified: Fri, 12 Jan 2024 14:11:51 GMT  
		Size: 8.0 MB (8046007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2021bc69cd7936af4ebbf5bfba7a6e67e545e684cfda88047a53cc6467277252`  
		Last Modified: Fri, 12 Jan 2024 14:11:52 GMT  
		Size: 1.2 MB (1197581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5505785b7d97a82996605f09502bd7efb648fba359f64ac21fc824be471fb93`  
		Last Modified: Fri, 12 Jan 2024 14:11:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6ecee0f8c9f1ffe62023bc7d1fd792e516f3bebebe860e014853a8042a9c6c`  
		Last Modified: Fri, 12 Jan 2024 14:11:53 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af1b8bf5503673f4d0bb4ce3c2f7619b2310320cdce742f6c259a3797ee9c188`  
		Last Modified: Fri, 12 Jan 2024 14:23:24 GMT  
		Size: 93.9 MB (93914222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8516d0ed545608695089c98b99d907c857213985130a24dcb1ea1682e4055cd6`  
		Last Modified: Fri, 12 Jan 2024 14:23:20 GMT  
		Size: 9.0 KB (9023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69caa3b18478516593d1c7e503745a723d5cfb50013c2d340cd1490e7c0ea110`  
		Last Modified: Fri, 12 Jan 2024 14:23:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e99ee5cb8bec7c003701c04860be1934fd99ab78b7c1ed457f0d5b35ecc65b3`  
		Last Modified: Fri, 12 Jan 2024 14:23:20 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5a13d4e292c10a6a7330b705dcd761f4e8e868dbee2b97f40af12c61302f87`  
		Last Modified: Fri, 12 Jan 2024 14:23:21 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1c86808014aff07aabbe64f23191578a4cc9976c3e6ed1bc79872ee5e6020e`  
		Last Modified: Fri, 12 Jan 2024 14:23:21 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:406aede1cbbb47ad95eba91114d1e4b0cf8b67280dba14ff5b6cdbe1e472b62a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4996800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c2bec36a96ef8b3374fc3eed55184f7670306b3db75ad7a481bbb7497067e1c`

```dockerfile
```

-	Layers:
	-	`sha256:869d142fe9760af5f69dc6a36a29792b6c723125f14583d578cf77e4265e8d82`  
		Last Modified: Fri, 12 Jan 2024 14:23:20 GMT  
		Size: 4.9 MB (4942882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:765d0939cc05eaa519de02c8cd2e425a8c0ee6b72cb64d4917053de497db9334`  
		Last Modified: Fri, 12 Jan 2024 14:23:20 GMT  
		Size: 53.9 KB (53918 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bullseye` - linux; s390x

```console
$ docker pull postgres@sha256:075354ba00020450356fd8a2d183c16965f75b0e187a8fecef57a8890f857a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139689404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0dea2d8931aca0f0c7bb9b45f3736915f770db051c911749f83d33ed9477700`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 04 Jan 2024 21:52:40 GMT
ADD file:77a92d4e9397475a6c68f4341baba607a7c875bc6e252de3e096482dd074f8ca in / 
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
ENV PG_MAJOR=12
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_VERSION=12.17-1.pgdg110+1
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:a8470cec8ee9510bf45556c756635d84eb3cbc0220b52812522196008c6b0d3e`  
		Last Modified: Thu, 11 Jan 2024 01:51:19 GMT  
		Size: 29.7 MB (29656884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47330ce14937b58fcacedba1705518d5b5c06692221b523057d1c260c8531b1a`  
		Last Modified: Fri, 12 Jan 2024 14:30:14 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0caf29b4fc0e3020d8e36fa1e3ba1062d1f7a3d62aa1e7261c65ab01cf887214`  
		Last Modified: Fri, 12 Jan 2024 14:30:14 GMT  
		Size: 4.2 MB (4195878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ac9434e09dbdd6d861d35be28eceb12ec3dd65065314332ad3eceecc4f379c`  
		Last Modified: Fri, 12 Jan 2024 14:30:14 GMT  
		Size: 1.4 MB (1439049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a95e365913d944b2d0615142546c4a2e36eea32b1c122eb9e3caa5500b5872`  
		Last Modified: Fri, 12 Jan 2024 14:30:14 GMT  
		Size: 8.1 MB (8099634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae9ee85bc00a08a97ea33d76f365c313dfcf1aa345e4fa2fb6723c2052e69f1`  
		Last Modified: Fri, 12 Jan 2024 14:30:15 GMT  
		Size: 1.0 MB (1015264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80edfb137f2d0861c069cfd70559fc31bd072060b41d34c6770e2c762673d84`  
		Last Modified: Fri, 12 Jan 2024 14:30:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df2fdd8b84a5275b404877c1d5790c18d4f42168e39d26cedb78e3595208889`  
		Last Modified: Fri, 12 Jan 2024 14:30:15 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e2905c63f66cb012ad8c6b985eb0e5e1d9bafb41e468fee79480530e300260`  
		Last Modified: Fri, 12 Jan 2024 14:38:49 GMT  
		Size: 95.3 MB (95262830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f948c7e3d16b7026f8259a108299048b7c40f246927643018e2842742b8b119f`  
		Last Modified: Fri, 12 Jan 2024 14:38:47 GMT  
		Size: 9.0 KB (9023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cc8f00cf4529ae16586fe84b7973dc14ee1e98f06f317c0d702c0098dff30a`  
		Last Modified: Fri, 12 Jan 2024 14:38:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b99f2ec111cfd668794709289cfffc40b73b2d36040b2799c5e0692de0b2c1c`  
		Last Modified: Fri, 12 Jan 2024 14:38:47 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2bb3a01c7b834e3ed899bace8ac1b020afaf768afa6a06c034ab3ddba70664`  
		Last Modified: Fri, 12 Jan 2024 14:38:48 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623429219c17ef9573ccb835b6349d9d75d4321dc647ec616ab8c0c4dbde65b9`  
		Last Modified: Fri, 12 Jan 2024 14:38:48 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:bcb984409528a1d09ffeadcfbf81853aca61d6639124e5a34691f08f53d3347e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4988597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17a6bee5df469852ea0dda2789c73ae7742b1d0c61339afd194c90823b30bbc2`

```dockerfile
```

-	Layers:
	-	`sha256:218c010892bbd2e920ba7bc385c3312782394e6e3fbb00e737e48441715b12db`  
		Last Modified: Fri, 12 Jan 2024 14:38:47 GMT  
		Size: 4.9 MB (4934727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e68f56236cebf8feb6f58593eaf713782faac0a09b86979643148de1e42bf844`  
		Last Modified: Fri, 12 Jan 2024 14:38:47 GMT  
		Size: 53.9 KB (53870 bytes)  
		MIME: application/vnd.in-toto+json
