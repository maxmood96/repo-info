## `postgres:15-bullseye`

```console
$ docker pull postgres@sha256:9c26847a062e233c658505454949be28f2fe4ec0478688ed6a66a566ef3928c3
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

### `postgres:15-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:dc80fad72faa669b26d2a6d0d291a13f7e6f637882107c721d309c97d7f0d067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.9 MB (138940957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7bca1f2988a91a6f21b4566b7c1d8057ed77e3f741cc0a3d96c3d15877d24c4`
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
ENV PG_MAJOR=15
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_VERSION=15.5-1.pgdg110+1
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
	-	`sha256:ee1d05a9d46581585290ee07a3a001a9a8f5fb17c2a828c8475230e23d5e677b`  
		Last Modified: Fri, 12 Jan 2024 00:23:58 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10681b015f791467b4b734b617e466a7f8e68390e45d6e1d891d0130d632c9fa`  
		Last Modified: Fri, 12 Jan 2024 00:23:59 GMT  
		Size: 4.3 MB (4305804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4230757a1ba9b153f02d92099d3b8ab5b81cca0e5704aeb032a6eeaeb0b92cab`  
		Last Modified: Fri, 12 Jan 2024 00:23:59 GMT  
		Size: 1.5 MB (1473292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00550a4d4759fe6ffa15aa45a29cd4d0ab6adadd6f888119c2d38a4160c6231c`  
		Last Modified: Fri, 12 Jan 2024 00:23:59 GMT  
		Size: 8.0 MB (8045951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f42a7815ef170dc216f02ddb90dab9b52a0e7094737281ffafa656b3177684`  
		Last Modified: Fri, 12 Jan 2024 00:24:00 GMT  
		Size: 1.0 MB (1038370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014b6fd98c57561a2737d06e95027cd4daa0dee023283c13e1993dccd1b842a0`  
		Last Modified: Fri, 12 Jan 2024 00:24:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cc33cd1646233c137d6aa4163a99ae7276cf7f0a7c02435f925bea8e7b4af8`  
		Last Modified: Fri, 12 Jan 2024 00:24:00 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e229178d21ec19ac9714298e10a260dee2c90d4b7be020d49f68e162e7fdb21a`  
		Last Modified: Fri, 12 Jan 2024 00:24:03 GMT  
		Size: 92.6 MB (92638962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bc8fa06a7b8cbbafa8bf18f19c3e19323996b270cb12202a12924fedeb8af8`  
		Last Modified: Fri, 12 Jan 2024 00:24:01 GMT  
		Size: 9.8 KB (9778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038351f66f10f996955ee8f073e809a12a58504223d7e4589fe8bc0c5ee10cd6`  
		Last Modified: Fri, 12 Jan 2024 00:24:01 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddde39904034fb14486b6f16d328400246ba960b6bae7989560ac508bcdc0626`  
		Last Modified: Fri, 12 Jan 2024 00:24:01 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88491262f7bc393199c6592e29a00e4ebe261140977f33f9c948f01a058af4c5`  
		Last Modified: Fri, 12 Jan 2024 00:24:02 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e140f34449da5c5c55573a83d558113ee3d856f7749f5ed166da8c65c0908671`  
		Last Modified: Fri, 12 Jan 2024 00:24:02 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:fdb812e352a74330c194d8c50e2d1d0076c1319d16096175ede2d5896f9e8cf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5061341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d654427d48300603f0d18a45bbe1189916e0d1d4b7a0367fa5c7efc9e62dd355`

```dockerfile
```

-	Layers:
	-	`sha256:60df5ce2f2992d2a462b02b7c2d5b2be32f731af1caa3cdb2053ed037d76d983`  
		Last Modified: Fri, 12 Jan 2024 00:23:59 GMT  
		Size: 5.0 MB (5007314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57aa35f922f538b5c8be7c6161ce7a3de0be575dfe4c0fadfc1c7de9c95c4c5b`  
		Last Modified: Fri, 12 Jan 2024 00:23:58 GMT  
		Size: 54.0 KB (54027 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bullseye` - linux; arm variant v5

```console
$ docker pull postgres@sha256:90c1d049cfc57d0e2e83918c8050aa11e19bcfb864ed0e60874500ba923819cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.2 MB (132159308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f487e8a1f4c4f7b3395cf519dc4e442080f43a064eab24e33fed53bfe2a54c1a`
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
ENV PG_MAJOR=15
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_VERSION=15.5-1.pgdg110+1
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
	-	`sha256:221b8a0afe467736e3d064d1a4bcdf0bae40795dfd710766db33a366cdb886cc`  
		Last Modified: Sat, 13 Jan 2024 00:31:07 GMT  
		Size: 88.7 MB (88699773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd6e35f36adbcdeb4104db592cc481e9497dd62ed78e7f258d1f65efad8b8ef`  
		Last Modified: Sat, 13 Jan 2024 00:31:04 GMT  
		Size: 9.8 KB (9785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d57551c44b47d62a73e2b84192fe0b7fa9f7582acb2d6a082f8a643a9af531`  
		Last Modified: Sat, 13 Jan 2024 00:31:04 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d239d50a1f77894fa40da655dc9ee575de2b38b19ad7ed17533b4b60e3778d45`  
		Last Modified: Sat, 13 Jan 2024 00:31:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f6d365120be3e317e236a853ad513b8086ad67b9e468ad6ab36a38ebc012ae`  
		Last Modified: Sat, 13 Jan 2024 00:31:05 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0535e3b8387468f6bca06471dad9b9c59be1c6dc79421655022f41286619f4c`  
		Last Modified: Sat, 13 Jan 2024 00:31:05 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:da1870ec1ea150770f2d320e18108c3d7bf6bd878b17d387c848f549fe3d4b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5071829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:499817e5a8ed56e06018c0a51d1d07066c9fae64a54fa318e3c9ddb9fdca877e`

```dockerfile
```

-	Layers:
	-	`sha256:c1092fd2848657f24a4e177302f10f91624e7a1dc8a058eef696dab51945a32c`  
		Last Modified: Sat, 13 Jan 2024 00:31:03 GMT  
		Size: 5.0 MB (5017775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45e1d90a196aeb18cd836ebfd0d632e8eba7bfc0cbc74f70f4fd7c412417160b`  
		Last Modified: Sat, 13 Jan 2024 00:31:03 GMT  
		Size: 54.1 KB (54054 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:6114a5eeae400cdc1a5ff624fc2fb249caa38b4fe92cb3c05ceec1ed6e6d26cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126791177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ede970b43c65d5cb790cad80954e4d96e300ff73ecefd09aa27956713067149`
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
ENV PG_MAJOR=15
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_VERSION=15.5-1.pgdg110+1
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
	-	`sha256:6b75fe9a6c270ce4fc5e4fc12c2fab3c155195fee999bc02d16bf26d692cad7f`  
		Last Modified: Sat, 13 Jan 2024 12:35:33 GMT  
		Size: 86.2 MB (86197468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de72a42904036eb5b32470c3f09a7f28db97d222bef2e7d562ca6c2081c1b5a`  
		Last Modified: Sat, 13 Jan 2024 12:35:30 GMT  
		Size: 9.8 KB (9782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c5e0f0489fef965ba22a97c9b0927ce8e629856c94ce9d59aaabf3883fb076`  
		Last Modified: Sat, 13 Jan 2024 12:35:30 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c54bc93b9b459363dba5e6418961a997a6fc3a91ea9942cb604217928a42315`  
		Last Modified: Sat, 13 Jan 2024 12:35:30 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5450ac640a9c7ba3a2935e1108a92f44db54171851dea820894ca226d468101`  
		Last Modified: Sat, 13 Jan 2024 12:35:31 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c161450326ef1431f5ac140dedf1398ff2b442d33fed2d1c044552e1e6b05f`  
		Last Modified: Sat, 13 Jan 2024 12:35:31 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:7d5655654478e7d29e8eddf819be8cbedb0854f06805d7d3ed3c3acf7e9526d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5071701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c5156cfae4a9bc3ee8a34f1644affd2370ecd20d0d18266892b01851723038`

```dockerfile
```

-	Layers:
	-	`sha256:c008a0420074035dac326a38c7cc7a32761e67b8974c80903af23d6ec6e0c583`  
		Last Modified: Sat, 13 Jan 2024 12:35:29 GMT  
		Size: 5.0 MB (5017653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:faa9c0b57ef2274a97b201f37c3c8716853939cdd5d193af3b838f68bc4bbd72`  
		Last Modified: Sat, 13 Jan 2024 12:35:29 GMT  
		Size: 54.0 KB (54048 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:5f41ee3e40508657d47ff7a670418a384e1f6fbbd6eccb4482f9f5e1da723fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134025143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d3d198deeacece76afffcfbbc6c83df0678bff9df43ef68798c6f79347c2edf`
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
ENV PG_MAJOR=15
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_VERSION=15.5-1.pgdg110+1
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
	-	`sha256:b85f8da11425c655dd097b846a5a94c1acd7b6898c30fac89e9e40a07b1f3c3a`  
		Last Modified: Fri, 12 Jan 2024 16:36:35 GMT  
		Size: 89.2 MB (89153368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40366c61c28b6129a7e07d8d156cf17d9924d24398e797536b3d5dc1c0d23bc8`  
		Last Modified: Fri, 12 Jan 2024 16:36:32 GMT  
		Size: 9.8 KB (9779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02af7b788a1edcfc3fbf02ecb02b884065a814b2bdea2bc079c6af3d9f97970c`  
		Last Modified: Fri, 12 Jan 2024 16:36:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbaab188bb5de27d898b4d1e1ccb574ac6b423dc7578c0835f4b1fbd0fd42cf`  
		Last Modified: Fri, 12 Jan 2024 16:36:33 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e548f67bc87405734650bdf724bff3a7659e8638639a011996efd00cf7b97dd3`  
		Last Modified: Fri, 12 Jan 2024 16:36:34 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01957835092dc98ed821983b925c52b1cfb2a4cfe1fb870dc9c227280faffa2c`  
		Last Modified: Fri, 12 Jan 2024 16:36:34 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:e2f10c011050256d3505b0209520c20936f1f837dc2d991e35c21b4aefdbb302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5066810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a685dcecc30f60a71c0e4ad03df659d6ae51877d43327686201e740548adcd`

```dockerfile
```

-	Layers:
	-	`sha256:65c93a882bbe79d737f615a72b737dbb081723bd45ac9676875eddfc8b8caeeb`  
		Last Modified: Fri, 12 Jan 2024 16:36:32 GMT  
		Size: 5.0 MB (5012945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fe51157ae384893f023bd4d5db0f159d3d7cb241b24d31bb19200e3f00d9159`  
		Last Modified: Fri, 12 Jan 2024 16:36:32 GMT  
		Size: 53.9 KB (53865 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:d7b0c6c46c42b66e4ca7303ef9dd3783568edba7563214a10f5009f896931e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (140995381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799531bb02065c7a9802801b7052abaaa361c299eb37f59df9a416479ef1f4e3`
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
ENV PG_MAJOR=15
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_VERSION=15.5-1.pgdg110+1
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
	-	`sha256:266f77afe976652545102584a3379f2394c6cec2af1896e61dd1dc5f92bb0bb7`  
		Last Modified: Thu, 01 Feb 2024 00:08:19 GMT  
		Size: 1.7 KB (1670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72fc5e3a20cebaf4bbda46982bfc390b6b1e82e30711421b4352172a2c7b40ee`  
		Last Modified: Thu, 01 Feb 2024 00:08:20 GMT  
		Size: 4.7 MB (4718033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1115d0a9ccaa36ea434f6baa175589696d53f85d7967a8612b9490803006287`  
		Last Modified: Thu, 01 Feb 2024 00:08:20 GMT  
		Size: 1.4 MB (1449169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48cf1a721f22d57e0e6af5ed8e9cddc06dae3ead90aaf9d7336b6d899cce05fd`  
		Last Modified: Thu, 01 Feb 2024 00:08:20 GMT  
		Size: 8.0 MB (8045915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9e2bea9c59ab929fc585e5474352054264af626cee85bdb301ed6c9cbe51cb`  
		Last Modified: Thu, 01 Feb 2024 00:08:21 GMT  
		Size: 1.0 MB (1028930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb48ac499de43f106e8b57b798d8d904d9b6392dee4e388514653e72853a8a3`  
		Last Modified: Wed, 31 Jan 2024 23:56:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744b1685b238b0c882e8bb0403d63e91b5cfe6078b2212f64e29d0e95748c115`  
		Last Modified: Wed, 31 Jan 2024 23:56:36 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6233552f9188853fabccc0966b16ea1b01f50b2ce68e848938e3dcea9bc52c7`  
		Last Modified: Thu, 01 Feb 2024 00:08:24 GMT  
		Size: 93.3 MB (93330202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8581308aca6fe9a320bf8e49e1a2e5d96c009ff105fc04c20e88a18a90ed64`  
		Last Modified: Thu, 01 Feb 2024 00:08:22 GMT  
		Size: 9.8 KB (9785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115ae3d1a988a50d41dde1752bf8c283a79e3387fd3e903bd5bdc4ee256e22aa`  
		Last Modified: Thu, 01 Feb 2024 00:07:24 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c7c3069ac86d525cc81f9b944808a96ea8b76a5e00c03f94502984803ce8cf`  
		Last Modified: Thu, 01 Feb 2024 00:08:22 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b975874e53d8fa10e79c00e0e277de8ac6131863056a00d23212a128b62f9c`  
		Last Modified: Thu, 01 Feb 2024 00:08:22 GMT  
		Size: 5.4 KB (5426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fd94f94ab2b1baab5cda8ed118b961c16a92b282beb25e2841cd109fcc1378`  
		Last Modified: Thu, 01 Feb 2024 00:08:23 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:57c7e3ef1634aa70134a4c317086fd8dcb21a0f3b40380b9a67d3d154ac46bc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5068867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e436f2be6c4ead37b3b828af1b3f30db60ae32b7dc84885bb914125f385accc`

```dockerfile
```

-	Layers:
	-	`sha256:f8041a06ea54b14bffa232461e8034f7fb9e8170eaa9abeaeb21ec58cf09be75`  
		Last Modified: Thu, 01 Feb 2024 00:08:20 GMT  
		Size: 5.0 MB (5014883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17a44d38ae7840d22db0495c8928ed7ed0cc10280cf6626af94f906ca651cf92`  
		Last Modified: Thu, 01 Feb 2024 00:08:20 GMT  
		Size: 54.0 KB (53984 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bullseye` - linux; mips64le

```console
$ docker pull postgres@sha256:753441fda9e639d81bf55999ea64d6d993c9a695ab9adeba42d5967b537ab60c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133687107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e342535a49ea1d7d62cdb0280cbf9aea8159fcac5391f5b14a392aab46bec6`
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
ENV PG_MAJOR=15
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_VERSION=15.5-1.pgdg110+1
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
	-	`sha256:745ddf1f9825021c065754d5acf8816545b60b4d06064091a86bbb4ddc964fa1`  
		Last Modified: Fri, 12 Jan 2024 22:25:19 GMT  
		Size: 89.2 MB (89226975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faae510ac315e81d7ce0ab8af31cb5eb58c1246488cb6d8b99a36ebafc78d02b`  
		Last Modified: Fri, 12 Jan 2024 22:25:10 GMT  
		Size: 9.8 KB (9788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27137211bbe241f6b4012677dae7a7f190f8b68a84fb27d33a0422f7670a162a`  
		Last Modified: Fri, 12 Jan 2024 22:25:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8530a14cd33272c2ed7666e15d708b2b33afceb2819c2cbb0aa54fc4ab67732b`  
		Last Modified: Fri, 12 Jan 2024 22:25:11 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7700d6837195d966fb9cc59178108d171769eba9925efc0124404231bcf77a`  
		Last Modified: Fri, 12 Jan 2024 22:25:11 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d6b3ddde81d0acfcbed4e7892014019264fee390b5254d84a1869143a01024`  
		Last Modified: Fri, 12 Jan 2024 22:25:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:c3992e52cf00f6c55200470b104f87206df027e9ca75c2123643a945673b48fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 KB (53717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1e421bf033e7ed91a4aac642ddc83de9539c1f393895075fd3cc3b64e48883`

```dockerfile
```

-	Layers:
	-	`sha256:a119873d829a1a1ebd276b83edc23eb6404095dc5394da7d83a9548e1c24e2f3`  
		Last Modified: Fri, 12 Jan 2024 22:25:09 GMT  
		Size: 53.7 KB (53717 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bullseye` - linux; ppc64le

```console
$ docker pull postgres@sha256:086a0017c829abc942d34d4720b15d2151f5e40db27f2ad6fa0ec7dfc85b751e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.0 MB (148049135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67bc38a097df13775875724cd3dbbba4c22eebc144901bd8c96dfe512f138198`
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
ENV PG_MAJOR=15
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_VERSION=15.5-1.pgdg110+1
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
	-	`sha256:d60a2381f1f8c78b607013da8cebd70683d1e90b62f989c435281e7b7f1323be`  
		Last Modified: Fri, 12 Jan 2024 14:14:52 GMT  
		Size: 97.0 MB (96964188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7380b3b14b72ffc9c007420bde8903cb6cec4d2f9d2314251c0160407bf0a9e`  
		Last Modified: Fri, 12 Jan 2024 14:14:48 GMT  
		Size: 9.8 KB (9781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf720ca5886c818c67b1b582a83e1a3b5f597c1f57bd95d496ac8f1bacf16994`  
		Last Modified: Fri, 12 Jan 2024 14:14:48 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828da91680d9941eee65217bf3c44dca32908d526a6e5ffe26636140cddd234d`  
		Last Modified: Fri, 12 Jan 2024 14:14:48 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ff5e6bdf2b2a1033675ff540efb84b731640bdfb454f9cb17d24a89820d1f9`  
		Last Modified: Fri, 12 Jan 2024 14:14:49 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552e2909e395cd55b45fac9c3923544d9164e7558f8e6bbf954ee27aab7204ec`  
		Last Modified: Fri, 12 Jan 2024 14:14:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:cad852c42bfcec4dacf726f7fbeb99372890714005a1d5658e7ab4a04667ed59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5068356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:339d445672a0ff6f41e1a68ac9dd9d918460e26ff3f72bd784ee7973088ad9cd`

```dockerfile
```

-	Layers:
	-	`sha256:fede220bfa59d534ec2ce1129bcc7241a595e28437689acff7fec61613415e2c`  
		Last Modified: Fri, 12 Jan 2024 14:14:48 GMT  
		Size: 5.0 MB (5014448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91a7341c9b06b9f6c8a6223fc9d7a3c7919c3acd92cb412c1f604ecf4e97fa6d`  
		Last Modified: Fri, 12 Jan 2024 14:14:47 GMT  
		Size: 53.9 KB (53908 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bullseye` - linux; s390x

```console
$ docker pull postgres@sha256:fabfb52ac6319c1dc2432d3c18db3ebafe1c038fe3bdb9aa6767c8308df777a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142553371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:388b1753b7b4556429e612948a1e905e93ade4bec4ec26ac06016ec42bd4b0b5`
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
ENV PG_MAJOR=15
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_VERSION=15.5-1.pgdg110+1
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
	-	`sha256:b7c3d12fa0ce7676acd593670bb4e168ca6804e37a0e396ffe4bda09eaefc5c3`  
		Last Modified: Fri, 12 Jan 2024 14:32:26 GMT  
		Size: 98.1 MB (98126037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3070a7af04284b6689f30bb42bd96cf68fc6e399c1363bb21d8288cd91913d95`  
		Last Modified: Fri, 12 Jan 2024 14:32:24 GMT  
		Size: 9.8 KB (9782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc79b83589eaa4a93a072e25e4c6baf24dc22c3d09e8826de235facced36b710`  
		Last Modified: Fri, 12 Jan 2024 14:32:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f2681b749b72a46e161600b9058d9c39c5899560c244f08c9cefba27ab037e`  
		Last Modified: Fri, 12 Jan 2024 14:32:24 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12aa0226f2db17d4eb2f92d88f48669b48a83d6156b9ba0028c0897f3c490d5`  
		Last Modified: Fri, 12 Jan 2024 14:32:25 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1676cc000b9db0faae058019c112d06729d91344870328866faf3fe05df9b669`  
		Last Modified: Fri, 12 Jan 2024 14:32:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:34243a435768e0721aa668a8e932cd0b4a0bd1844f8b5ba16b06949c5b1ee9f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5060153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb3e9dd04c1fa689ef380040d12a87c0f6323aa96f997befe24afe213809bea5`

```dockerfile
```

-	Layers:
	-	`sha256:d59fc01e12cadac2df061fd1dfb39ff53d01bcf082d4e7ae3f70b25486d2f7f6`  
		Last Modified: Fri, 12 Jan 2024 14:32:24 GMT  
		Size: 5.0 MB (5006293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c32403a85c3c917c5836af6729dc445cbac50ba32b1ab5c0db022a3ce46efbd`  
		Last Modified: Fri, 12 Jan 2024 14:32:24 GMT  
		Size: 53.9 KB (53860 bytes)  
		MIME: application/vnd.in-toto+json
