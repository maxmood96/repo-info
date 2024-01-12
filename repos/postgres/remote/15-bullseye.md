## `postgres:15-bullseye`

```console
$ docker pull postgres@sha256:870b3124a64cab57e73241692ce1569fb515ab8b9585e47c08458736cadd07ed
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
$ docker pull postgres@sha256:3d75990e3ed8986de70edddca9599023a0d8b9cbbf8410148823b8390edf7c1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.2 MB (132164259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c765e2356312db9cfabeafbbfad2be1dc02390337cb3ce6134bcea6c0d071ab6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 19 Dec 2023 01:55:38 GMT
ADD file:831966ecbc1ad85566dda1f3580cd9306cc099069cd418506e8befd03c296d1c in / 
# Tue, 19 Dec 2023 01:55:38 GMT
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
	-	`sha256:fdebea600ba5b47ddd94c41d9d687679a030fdad563a3490945a5433dae01d54`  
		Last Modified: Tue, 19 Dec 2023 01:59:22 GMT  
		Size: 28.9 MB (28921283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5998e1e18cd7818d27c94752e2d22db37826d44e11596aa1f838652c2711a701`  
		Last Modified: Fri, 05 Jan 2024 02:49:38 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234d9bf89252d125ce689173ee6f4fd501ced987cd728797e4c09187cd2219a5`  
		Last Modified: Fri, 05 Jan 2024 02:49:39 GMT  
		Size: 4.0 MB (3986362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359c6b518e813716e68156b6962ac9e11b3626807320bca0b829e6418b45e2f1`  
		Last Modified: Fri, 05 Jan 2024 02:49:38 GMT  
		Size: 1.5 MB (1450834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea348f7dadb3e98a5f88e70d22429b9f23fae8a68739ca2fae508c6d31bdf253`  
		Last Modified: Fri, 05 Jan 2024 02:49:39 GMT  
		Size: 8.0 MB (8045860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e290d666e3c68e1cb4d15350e196adc79aaf605cf49e39578265205ba5841b`  
		Last Modified: Fri, 05 Jan 2024 02:49:40 GMT  
		Size: 1.0 MB (1034956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79964b3313cb8ae93c86130d273435a00efd2c8630c0d8043950d1e7996fa3a8`  
		Last Modified: Fri, 05 Jan 2024 02:49:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14999c5f25cfb5837d1a1f7b66de0590fb361e8666ce57c140d67a5c122f593b`  
		Last Modified: Fri, 05 Jan 2024 02:49:40 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb62d66fb98da3aba4459fbc9e930165f987a24f1bf4676ae6960388e2617657`  
		Last Modified: Fri, 05 Jan 2024 03:38:04 GMT  
		Size: 88.7 MB (88704338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a646be982a1c6ce77806d5972c633bcf47f6e17b23c193279ef8f663c72ab6b7`  
		Last Modified: Fri, 05 Jan 2024 03:38:02 GMT  
		Size: 9.8 KB (9788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6ab4ea1d29303eb18acd88171ec151ccc281143146667e93e1ee57f56106cd`  
		Last Modified: Fri, 05 Jan 2024 03:38:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1750ebed35c5a9fe377cc637b30a2f14d2e0cd9314766c4b730eb2a6af028293`  
		Last Modified: Fri, 05 Jan 2024 03:38:02 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416974624aa9df5ed591d5425a5be14baf8302b08261555f75f9dd2f3bb10593`  
		Last Modified: Fri, 05 Jan 2024 03:38:03 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2416586deb73c11daedfce2f7ad11f261c4bb7977163c6021359f5f9badac3a`  
		Last Modified: Fri, 05 Jan 2024 03:38:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:9a122238f047db67239274066baeb6b9b819195a3ebd131a6ac9efccf89d5fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5071832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:756e4330e6db47f08d77054ecbbf33387ffa7440d6287f6a34f404e41ba0d3e7`

```dockerfile
```

-	Layers:
	-	`sha256:289537060249c7d95921bec9568da262c3438c18c193b5d3728e9b341a1bc2a9`  
		Last Modified: Fri, 05 Jan 2024 03:38:01 GMT  
		Size: 5.0 MB (5017775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53f12e74e5970cfc03a4b29e4691b8b3de88e1cf85e46899c407e5fd2ddf910d`  
		Last Modified: Fri, 05 Jan 2024 03:38:01 GMT  
		Size: 54.1 KB (54057 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:5a17aecd12784de67660160a5b4207af96319c9822e97f6264f62a12615d3697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126790575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd52c7b2b09c9b11ac0fa2d9c122f0d82f6a59496ee01dd5da3ddb62e1caf9f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 19 Dec 2023 02:08:09 GMT
ADD file:496e70a34ff4dabb4eefdf40e4e2f0563bea0c120bb43206f8f52ab5a887b637 in / 
# Tue, 19 Dec 2023 02:08:09 GMT
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
	-	`sha256:19ccf4d6cc6956e4a5522352be94632923aa376a9939a4f45428a4f304c73bc8`  
		Last Modified: Tue, 19 Dec 2023 02:12:33 GMT  
		Size: 26.6 MB (26578972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d975cd1debbe8fce1375d195625188b9f85a471a910b6d8c377217e4f54240bc`  
		Last Modified: Wed, 20 Dec 2023 01:28:19 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf12cc793b0b3f127a223672a9c73635e0727de9b1166520b6309acd37dfe0b`  
		Last Modified: Fri, 05 Jan 2024 03:17:59 GMT  
		Size: 3.6 MB (3598363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a67ebbfa8a4bb5f6ebe3760dc2b4a17b65f306e1593719f48076598908b81ef`  
		Last Modified: Fri, 05 Jan 2024 03:17:59 GMT  
		Size: 1.4 MB (1440970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff2ad3c75dc0d3e73b0cb2a61ff150c2f7137746c693329f8a2de4d6fbd279e`  
		Last Modified: Fri, 05 Jan 2024 03:17:59 GMT  
		Size: 8.0 MB (8046000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479e676439f922ae6ff84de6553c461646d33d2c4e82e4a07d8d1b3774747b2e`  
		Last Modified: Fri, 05 Jan 2024 03:17:59 GMT  
		Size: 908.8 KB (908753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e2afae5f60d1cb8e28e23a703efcfdce20158823444300030a648b6b56399a`  
		Last Modified: Fri, 05 Jan 2024 03:18:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9084ae3771528c357178dd45142a07ca72f8be87d238914573bf4f451f1c686`  
		Last Modified: Fri, 05 Jan 2024 03:18:00 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a42b120d83197c298ca8d70cc4ca8e0d3665d7739020ffc1c7319cd48ab526`  
		Last Modified: Fri, 05 Jan 2024 04:05:21 GMT  
		Size: 86.2 MB (86196880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817496ae6f92ec5c08bfa026d157afe4bd459f54571233d6ac9dc83d011c6bbd`  
		Last Modified: Fri, 05 Jan 2024 04:05:19 GMT  
		Size: 9.8 KB (9790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ab1c7d10490d1fb8acc128cc1f27a0a83402c3860712949d242a5013052618`  
		Last Modified: Fri, 05 Jan 2024 04:05:19 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818af47f8265e1636760ce07cf005efb7d406ebf60c38a8376147c6ae979bf89`  
		Last Modified: Fri, 05 Jan 2024 04:05:19 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c3ca6118ded6d1b047df21e77dcc0d6fd74f3717a0e9441ceb5f671d099c5d`  
		Last Modified: Fri, 05 Jan 2024 04:05:20 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0edb1dbe953f1843f7df888623047babc06e79f854980fa754bd21f9c700deb6`  
		Last Modified: Fri, 05 Jan 2024 04:05:20 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:e3cbc68ed96306e5f69f58beed9d5eba895f0fb32752b0852de16f8df42d852e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5071701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:726a12c971b3fed85cf1f5e776a0242bdd4b29eb7ef9925a1e39341db89455e9`

```dockerfile
```

-	Layers:
	-	`sha256:9532827219fa8e29281b435028831d4c10eda2b18899d0f69d59816ee218fccb`  
		Last Modified: Fri, 05 Jan 2024 04:05:18 GMT  
		Size: 5.0 MB (5017653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:313ce5af3cb58541661f5ca16fd4e26c30dae345ff202fe470a4e55eb6874e9c`  
		Last Modified: Fri, 05 Jan 2024 04:05:18 GMT  
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
$ docker pull postgres@sha256:178980371ffdd3ab774d441c491632f3e06aaa8064542c6f005e9577ad791d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (140992842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d51c359c0eff1b0c7256fb6930a1d858649a2c3ee3d0eef5e97c1210c9277ed7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 04 Jan 2024 21:52:40 GMT
ADD file:ed1ce84cc05c621c3311366a5ef8f9ed36bdff95d75ee1564c10e7a20f993b61 in / 
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
	-	`sha256:d19cbf7b148868960150824d1e6f8ebc5f6d7542a422061491e92178f7db879b`  
		Last Modified: Thu, 11 Jan 2024 02:44:06 GMT  
		Size: 32.4 MB (32402672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c195757c92c14c33706b52afa0404a6fef39066c2ae4e1cff0268308cb727fdd`  
		Last Modified: Fri, 12 Jan 2024 00:35:40 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f993a72e941c05d8cb17cc22354d42fd06bdbea1d0892a1c05ee094fd1e840`  
		Last Modified: Fri, 12 Jan 2024 00:35:40 GMT  
		Size: 4.7 MB (4717994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d2931840b1d3c11efdda80decf5d529fd027eb5de36b4f8e19bf8b17d7b830`  
		Last Modified: Fri, 12 Jan 2024 00:35:40 GMT  
		Size: 1.4 MB (1449103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50645c97884b5e70b5b2a1c488f195e37fc6e405800846c51087020d90d51538`  
		Last Modified: Fri, 12 Jan 2024 00:35:40 GMT  
		Size: 8.0 MB (8045872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de82ffa01af5abb76bedee4a9209102d605d5e8d797ead104af4ecd67d2531b`  
		Last Modified: Fri, 12 Jan 2024 00:35:41 GMT  
		Size: 1.0 MB (1028907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ce9dcbec097bd79b0720c9ac905966fc8604aca1e6e5ffdc039eee9ad13726`  
		Last Modified: Fri, 12 Jan 2024 00:35:41 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ce2aa4dd64651e086ae8e56524555ba38a3e554a097b1a863ad146d8798589`  
		Last Modified: Fri, 12 Jan 2024 00:35:41 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690daa73df8e6191fdfb9c0ed0a9a58f90359e234b21837ccddbac1e86bcc32a`  
		Last Modified: Fri, 12 Jan 2024 00:35:44 GMT  
		Size: 93.3 MB (93327683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0646ad413ef8059fa2f516ef6735e717d47c7fbcdf0a6108fb0cf5374dad824c`  
		Last Modified: Fri, 12 Jan 2024 00:35:42 GMT  
		Size: 9.8 KB (9775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a251f494dffa32334352993cb01850ac3ae3c4d4da9c17a5cd7ce2d603de59`  
		Last Modified: Fri, 12 Jan 2024 00:35:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba50453b69754e3b0a03d67dfc7b50f01252f1fb7e82ceb19e78179b75eb472`  
		Last Modified: Fri, 12 Jan 2024 00:35:43 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e32d4700524b8427cc2a47c1a3c552c60c390d9e47b151646e4482b3f7033d0`  
		Last Modified: Fri, 12 Jan 2024 00:35:44 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea1a5e92f37c298ab2d65c4fc28ff4b49b492d1543e1c8e57141d635e6cee45`  
		Last Modified: Fri, 12 Jan 2024 00:35:44 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:7b4f36dd4922fce9e4ae109da345f6146dc4e83f6056f4baf8fe9c1194405aee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5068869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e474e3d51bc6e4ebaf6ee13ff4ad361d873aee90e313acb436d24c3d47de99`

```dockerfile
```

-	Layers:
	-	`sha256:0f8e526e3c1841f02e66c40ab084039d532bb6a21dca36a729df1bed8dc3a923`  
		Last Modified: Fri, 12 Jan 2024 00:35:40 GMT  
		Size: 5.0 MB (5014883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:726b218dea9e0d95224b78ec35631209d7c5594f8cdbf544e5277fb670db497f`  
		Last Modified: Fri, 12 Jan 2024 00:35:39 GMT  
		Size: 54.0 KB (53986 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bullseye` - linux; mips64le

```console
$ docker pull postgres@sha256:59948e5cae4f8802d034647ec977af0d7f0a0352deeddaa123fa9c80b2230c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133688411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feec278e846e63de253bbb30a0724533311849952b549af61cab91961c4ccd65`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 19 Dec 2023 02:14:50 GMT
ADD file:dcc77071aa6c677714230fd845d154c00ba6ba34a78f8f1073c224e90f17f543 in / 
# Tue, 19 Dec 2023 02:14:54 GMT
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
	-	`sha256:f9454980ac665cb2d7641130c738c2054ef7a7516386fc6742b46b5b60dd93ad`  
		Last Modified: Tue, 19 Dec 2023 02:26:03 GMT  
		Size: 29.6 MB (29635982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207177edcd6dbe8ce328379ab3be9fe9aa42304ee8a45049feefe410b6422fdf`  
		Last Modified: Fri, 05 Jan 2024 04:21:24 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73dc0d7338f12deddda8d0e3601a87d88f3c9fae3f15e827c8e43bf44decb84d`  
		Last Modified: Fri, 05 Jan 2024 04:21:25 GMT  
		Size: 4.3 MB (4306012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2664d0f9306e39c55028b002816a44b0584c2b99232a1fe76a3b52b4441d8d9`  
		Last Modified: Fri, 05 Jan 2024 04:21:25 GMT  
		Size: 1.4 MB (1360864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9b3fb4d44bbd8f1396f306f5f8c0d02ca9947b7c4ea56b82ac74372e8fbdf1`  
		Last Modified: Fri, 05 Jan 2024 04:21:26 GMT  
		Size: 8.0 MB (8046275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03c063791a4903d29f880a0030f2401016874570674b8d2291ebadda8c4d4ca`  
		Last Modified: Fri, 05 Jan 2024 04:21:26 GMT  
		Size: 1.1 MB (1090271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2c34d966da355997b66a8f82c598920ef1b06f15020157dfacd76bdd2d549d`  
		Last Modified: Fri, 05 Jan 2024 04:21:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c92402b8b1c83ce792ffc2c67a7fc0c28c799348c7c2bef1edae9310b89ad7`  
		Last Modified: Fri, 05 Jan 2024 04:21:26 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825a4232a3737ca01fd849c2fe416325840bb5a1276595e8ebe092aa8c65ac4e`  
		Last Modified: Fri, 05 Jan 2024 06:34:03 GMT  
		Size: 89.2 MB (89228365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fba4d4a3fa0e510d4321c68a677012024e4d80a255e6452849108eb60cbb28`  
		Last Modified: Fri, 05 Jan 2024 06:33:54 GMT  
		Size: 9.8 KB (9794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdaec7bd6c87e512aaf06eee8973ecdb909dbf435058414ad382c8c7fe607c56`  
		Last Modified: Fri, 05 Jan 2024 06:33:54 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825f7c4684fd25c08707dbeae4e1f511e03ff290ed94a8e40c330ad2bd0092df`  
		Last Modified: Fri, 05 Jan 2024 06:33:54 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed2a3e9b80b43977819682169fb723df8b6fdc9900578e307d85260db5c1591`  
		Last Modified: Fri, 05 Jan 2024 06:33:55 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ca37768877c2c5b89b8b4a82900f8a4dd16846f1903b2d3a334be5b4b8eba0`  
		Last Modified: Fri, 05 Jan 2024 06:33:55 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:a326913804fc9e1eb9168be27b340a6ead369020f619397da6182b8c2b6f2c8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 KB (53717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab8f93db070498ec93479406749af2f9d3a47b913bb544a9ba03d22a1a1961af`

```dockerfile
```

-	Layers:
	-	`sha256:ccfb1b251e64519190d95780ff089c9b243cf528b4cf4c530f94ee9efd21bdb1`  
		Last Modified: Fri, 05 Jan 2024 06:33:53 GMT  
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
