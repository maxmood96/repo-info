## `postgres:16-bullseye`

```console
$ docker pull postgres@sha256:a7f7bf158aeee559243c3cab7325fe51563930dd872f7f2d6033a6c137ec928b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `postgres:16-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:62ca6de0d45426d4d2cea361f1692750dba73397a6c8b9f11bb0067233029420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149393695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef69d67b7a44787ba022d417a02897707f3c3c0fb177c4f66f3c70b368799f75`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 27 Feb 2025 00:53:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV GOSU_VERSION=1.17
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV LANG=en_US.utf8
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_MAJOR=16
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_VERSION=16.8-1.pgdg110+1
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 27 Feb 2025 00:53:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Feb 2025 00:53:12 GMT
STOPSIGNAL SIGINT
# Thu, 27 Feb 2025 00:53:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 27 Feb 2025 00:53:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:55147cbf65d4d152c070165835355b8ea7a090d48d81ba52cbeb9bbe8d629fc0`  
		Last Modified: Mon, 17 Mar 2025 22:17:31 GMT  
		Size: 30.3 MB (30253836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00600ce22c372db5845e2b4a316543e2ee36eb7bdc9bea99b0dbbc616fa160c1`  
		Last Modified: Mon, 17 Mar 2025 23:19:33 GMT  
		Size: 1.7 KB (1681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439bc713af0adb2c42c9ade81e3d2616a7b5590b5addb9d6bcf9833f2ac7d1f5`  
		Last Modified: Mon, 17 Mar 2025 23:19:33 GMT  
		Size: 4.3 MB (4308180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4b495ff8b66454ce6536b586afac1477d99e368ef1436a373f06c5769ab918`  
		Last Modified: Mon, 17 Mar 2025 23:19:33 GMT  
		Size: 1.5 MB (1472230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a596eec8cf9806c82b6d4054b73f9572fe7d196bd320e0e416524606468c410`  
		Last Modified: Mon, 17 Mar 2025 23:19:34 GMT  
		Size: 8.0 MB (8044480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99be509e8a0a3258704b98300abb879b0363387bae30f55b88dd91c6d2968102`  
		Last Modified: Mon, 17 Mar 2025 23:19:34 GMT  
		Size: 1.0 MB (1038348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8345b8357b4310616cbf494dafdb36e1155ef3376f2dd7c385cfd000f6cfb4`  
		Last Modified: Mon, 17 Mar 2025 23:19:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187c74d8f4bf7660e025ad62bf89683e37766bdb1e18c1f78562011d1e4a0fa1`  
		Last Modified: Mon, 17 Mar 2025 23:19:34 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1429229d45d0b7bf09f3345071ea40b4af07bf2d9e1a0248866ca042f937e81`  
		Last Modified: Mon, 17 Mar 2025 23:19:37 GMT  
		Size: 104.3 MB (104255808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4613f45e277e007ac82be662f68f3a9723e5bdae45eb2ebe55bb3ee8f5a8bc8b`  
		Last Modified: Mon, 17 Mar 2025 23:19:35 GMT  
		Size: 9.9 KB (9922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626031d6d49396e6a9cc8fb9630e4e736fdd0de86792f9a69faf1df2a84f7c79`  
		Last Modified: Mon, 17 Mar 2025 23:19:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee01808ad16332589a2795918969d3e0550542d24a0b24ad5277aa9ca38185b0`  
		Last Modified: Mon, 17 Mar 2025 23:19:35 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ee3d05e3baca1df742f55409013a49f8b5c8344475099d834767ae1428c326`  
		Last Modified: Mon, 17 Mar 2025 23:19:36 GMT  
		Size: 5.5 KB (5470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d2d5fc66a28e5597a199624217bf99ec95114a1f97b93a70b5909f6acb9f8a1`  
		Last Modified: Mon, 17 Mar 2025 23:19:36 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:527e05cb137c1527afbc9484506f3ffb57b9a4ebdc5a9d5cab34ee1dbe4a7bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6102260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e35fd673f9a7daad7eaf5e0b35239a6931502a0854e3621f69bb66ecfdfcb778`

```dockerfile
```

-	Layers:
	-	`sha256:04e25d36adaf46f2931077a98ad31d3061cdce57789c351a2228c8bbcfbb577e`  
		Last Modified: Mon, 17 Mar 2025 23:19:34 GMT  
		Size: 6.0 MB (6048778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eea826acc2f1135e55d8dabac676bb2099032aea34e29d5a51e013c2461156f`  
		Last Modified: Mon, 17 Mar 2025 23:19:33 GMT  
		Size: 53.5 KB (53482 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:ca0ad316b7aa5bd1f56f7775c9cb9ecac49b6ea63d6c92f536792f7c1df530e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137614175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c292ae4a203c2aa0633fb244399b1badc797a0800c2f2af28b7488c133c453b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1740355200'
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV GOSU_VERSION=1.17
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV LANG=en_US.utf8
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_MAJOR=16
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_VERSION=16.8-1.pgdg110+1
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 27 Feb 2025 00:53:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Feb 2025 00:53:12 GMT
STOPSIGNAL SIGINT
# Thu, 27 Feb 2025 00:53:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 27 Feb 2025 00:53:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b0ca501b624d9dae81049df15e1024733ee21141b25f8ca123d98e0d13df5d12`  
		Last Modified: Tue, 25 Feb 2025 01:31:18 GMT  
		Size: 25.5 MB (25535432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6204b706db4505b0d749e0d835ecbddd590f9fa27da4b9c5a692db9e0c03ea14`  
		Last Modified: Tue, 25 Feb 2025 05:02:00 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800a09efa9bf67a5bc2521ee16383eca0724ed0d84da6567ca79576dcbffd135`  
		Last Modified: Tue, 25 Feb 2025 05:02:01 GMT  
		Size: 3.6 MB (3601737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a493ae1f33759277362b97fbbe77c06ea34286ddf5fcf5bbb240a2e24ebddc44`  
		Last Modified: Tue, 25 Feb 2025 05:02:01 GMT  
		Size: 1.4 MB (1439258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01845e99e159242c0417adb0d7aac21e93428ba91032660691bbb726b812b2fe`  
		Last Modified: Tue, 25 Feb 2025 05:02:01 GMT  
		Size: 8.0 MB (8044637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f852b0bb6cd5d2096afce0fd3b3579928fadcc4ac7acd417df5011b93f6e0368`  
		Last Modified: Tue, 25 Feb 2025 05:02:02 GMT  
		Size: 908.7 KB (908701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c651445c8a497822fd0ba2afa2b5e18b75b616fbb5088b00084f76146dbcf9`  
		Last Modified: Tue, 25 Feb 2025 05:02:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752e78506a0db5d3fc118ceccddf5db9ea47674a847b7d530dd2e6d383dd2383`  
		Last Modified: Tue, 25 Feb 2025 05:02:02 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f1da78cd8291e3faed9bc71552591148a7de809fe0ba58819a7859ad1fb5cf`  
		Last Modified: Tue, 25 Feb 2025 05:32:05 GMT  
		Size: 98.1 MB (98063603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaa7fa8dc138913e5652550671738b3913f495655f112a7c99caa6af11da7db`  
		Last Modified: Tue, 25 Feb 2025 05:32:01 GMT  
		Size: 9.9 KB (9923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f073ee76d6532e3fe5d824e0a9bec541817e1066e1930de268c10a24f91f2680`  
		Last Modified: Tue, 25 Feb 2025 05:32:01 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764693f45e9a06d45335e48a3d008560f0dd270563d2a19eb0cf7897146b8407`  
		Last Modified: Tue, 25 Feb 2025 05:32:01 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0ddee0e7bc322ee8fe2afebf3c544390cdfd6570e65814181a89a50e93941d`  
		Last Modified: Fri, 28 Feb 2025 23:26:24 GMT  
		Size: 5.5 KB (5467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b15cc86eae406df118638e28de1f58e6102af3e55a9ce6c57ff7620968faf4`  
		Last Modified: Fri, 28 Feb 2025 23:26:24 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:05b2a60a5598a9bd1f06c98cb965bfeaab81c20a97432a788b9002c70f18b458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6117905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a124c7f24b9b778b18624a51f986b97745fe1b81e72c8b8a6457b67bf92a29`

```dockerfile
```

-	Layers:
	-	`sha256:7967a108e6b858727b5e18ef054f72023e8a209d99b8db58dd96ca92681c5d1f`  
		Last Modified: Fri, 28 Feb 2025 23:26:24 GMT  
		Size: 6.1 MB (6064235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddc336559c537085b58b6bd51f10bfab96c6e1398b2ec52e65017c6fc50f8f75`  
		Last Modified: Fri, 28 Feb 2025 23:26:24 GMT  
		Size: 53.7 KB (53670 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:6a2fae6af4454eeea0d393fbcd4f870c8636f00a1814a23786c384af0128036d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.4 MB (146400238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf00ce0189d4baddb5557833ff95cd4066c7ccfc322de5dba746d75fbb8bbc8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 27 Feb 2025 00:53:12 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV GOSU_VERSION=1.17
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV LANG=en_US.utf8
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_MAJOR=16
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_VERSION=16.8-1.pgdg110+1
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 27 Feb 2025 00:53:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Feb 2025 00:53:12 GMT
STOPSIGNAL SIGINT
# Thu, 27 Feb 2025 00:53:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 27 Feb 2025 00:53:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6eba8885c82049d690776150810f32585aca6c3eba49f692753434bdaee447ec`  
		Last Modified: Mon, 17 Mar 2025 22:18:52 GMT  
		Size: 28.7 MB (28745923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a220ac721ece58d300afceb9eccd2b98e13fe81b91d611b24ec03419a03a41`  
		Last Modified: Tue, 18 Mar 2025 05:22:27 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f426aff01f8ba34c5e8b92c500a7dee9ae88418440f0180f15a3216b5a2db0`  
		Last Modified: Tue, 18 Mar 2025 05:22:27 GMT  
		Size: 4.3 MB (4312826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa1eb7bf93390567bbea6bc26e6af756aead292491dddb464a792347c58b596`  
		Last Modified: Tue, 18 Mar 2025 05:22:27 GMT  
		Size: 1.4 MB (1404107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640ac0de34b0c3e24ea1b487fa0df3caf764b11d7633508d0c7d9f3c6fae7343`  
		Last Modified: Tue, 18 Mar 2025 05:22:27 GMT  
		Size: 8.0 MB (8044468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab648e86d38640c7d29dc4fd7b6f82cfa70ad38fa589f65b8703436447a9cdb`  
		Last Modified: Tue, 18 Mar 2025 05:22:28 GMT  
		Size: 1.0 MB (1026615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d250975a1d60a5f61f08ab2e129490f2f8955c4b42bd153274e8e0b44c06da1`  
		Last Modified: Tue, 18 Mar 2025 05:22:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f405878a6593f15db3b1610dd5fef7fd02e6af3be519c9cffd624659d61e47`  
		Last Modified: Tue, 18 Mar 2025 05:22:28 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd75ba23f0dc83fdfea8165c02c440d3b0bd2db930b05c88f725a8b5e8dbbdf6`  
		Last Modified: Tue, 18 Mar 2025 06:52:05 GMT  
		Size: 102.8 MB (102845481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e702934fcd130e31381ce50ff6af9a48e71b5f7f8e2fdd7f9fe43f95eb61b8`  
		Last Modified: Tue, 18 Mar 2025 06:52:02 GMT  
		Size: 9.9 KB (9919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1616275155dace666d7f6c4341668e1a0cb38053e0c0ea70f7778a6989879a3f`  
		Last Modified: Tue, 18 Mar 2025 06:52:02 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2021d6e86bf046b7275ef3c3e1c85b3f53012586a1e3fdd90c17de17877eab3e`  
		Last Modified: Tue, 18 Mar 2025 06:52:02 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30f859b9a480eff6e15e3fbb33d0d450c6323920bfbb2fd06c037cf7e215553`  
		Last Modified: Tue, 18 Mar 2025 06:52:03 GMT  
		Size: 5.5 KB (5471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c139778ade1aad8d8781fda1e91e48fc6d08fc9281289a9ba1d8ac43ab2ba4`  
		Last Modified: Tue, 18 Mar 2025 06:52:03 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:395c0bff61401dad7f0cf284b01e150af4241e7ee797f7385d4787059870222b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6108793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7acba3fcd5f378acb5c9ba432f2f142ca504182bde230dff37e97b4193c63046`

```dockerfile
```

-	Layers:
	-	`sha256:9fcd62e7068cb7e678b1702308832ff68e7b7114bc64582481df4677bbe8f96d`  
		Last Modified: Tue, 18 Mar 2025 06:52:02 GMT  
		Size: 6.1 MB (6055066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ecf16ee874270ed02f99ef4bd164489d0ee1d2ec0575c6bb2f219fd8ea326a3`  
		Last Modified: Tue, 18 Mar 2025 06:52:01 GMT  
		Size: 53.7 KB (53727 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:ae20a43f11012c53329c65ed7fc62a6a71ddf684932e4afb95c22e34ef4feb59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157579780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9131116746ab08eab3313fa7210f34d4b9cceab7523fc4df02223e89665cba4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 27 Feb 2025 00:53:12 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1742169600'
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV GOSU_VERSION=1.17
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV LANG=en_US.utf8
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_MAJOR=16
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_VERSION=16.8-1.pgdg110+1
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 27 Feb 2025 00:53:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Feb 2025 00:53:12 GMT
STOPSIGNAL SIGINT
# Thu, 27 Feb 2025 00:53:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 27 Feb 2025 00:53:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e83ba34877ecae8e583197e97ef35a452a1d1b81c406023bf40d3c79d5ba9025`  
		Last Modified: Mon, 17 Mar 2025 22:17:57 GMT  
		Size: 31.2 MB (31180337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24516e458957e00f297de6573b02e50651acce32728ffc3a93d5cc2d541eebdd`  
		Last Modified: Mon, 17 Mar 2025 23:45:01 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f6f25174371a5e5e66a7f087db4395037bec0020618670ca1b0694c2e35702`  
		Last Modified: Mon, 17 Mar 2025 23:45:01 GMT  
		Size: 4.7 MB (4719671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb54e05478d3aca1ffbecaea5f1eb84d0f1be845cd706d4a02ae6352c25df78f`  
		Last Modified: Mon, 17 Mar 2025 23:45:01 GMT  
		Size: 1.4 MB (1447755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa36275c78dc248b773d2eef8be078e38a391a278790742dcc590dfafa4809f`  
		Last Modified: Mon, 17 Mar 2025 23:45:02 GMT  
		Size: 8.0 MB (8044421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69d3d1d02f059ef71e0c87ca72f707fbc4e5c33cc07a941a7b0c2955966a0ff`  
		Last Modified: Mon, 17 Mar 2025 23:45:02 GMT  
		Size: 1.0 MB (1028920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed215408ffc9d8c6546c3965d40eb4361aa0a1a01f09021d13f65ea8ad29a3dc`  
		Last Modified: Mon, 17 Mar 2025 23:45:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12260922351ac091e5ae57899f5589016f2ea2fec49b0054e3747eeb9899624d`  
		Last Modified: Mon, 17 Mar 2025 23:45:02 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9df4df02e5d83316e59548f91bce74395afa5ebc74531030b2f1b71a4c36b2`  
		Last Modified: Mon, 17 Mar 2025 23:45:06 GMT  
		Size: 111.1 MB (111137865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86828e0fdc1a8a421c5b1e3e66be7fdb8e60ee308d79fb2a99f95008f200ba7c`  
		Last Modified: Mon, 17 Mar 2025 23:45:03 GMT  
		Size: 9.9 KB (9922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe1ac4c5dddd37e2e10272bd7484af0296fdaa677b233831b3ab430c2e385fb`  
		Last Modified: Mon, 17 Mar 2025 23:45:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a949e0c929be834b0111d193684cdee2efc70ca5366f483a1dcdbe91481e188`  
		Last Modified: Mon, 17 Mar 2025 23:45:04 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801542bcadb8e39693deacf603da51e116aafa83d74443773045f124acbc07b2`  
		Last Modified: Mon, 17 Mar 2025 23:45:04 GMT  
		Size: 5.5 KB (5473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9c134aba006f11ab9cbe5a7285d3fef540b5ff54fb3f0047c870a0eb1dc653`  
		Last Modified: Mon, 17 Mar 2025 23:45:04 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:89da52755e99ce5024d986a20c1049ce2f438675c66301a0fc8d5e35f901b59e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6115448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c176d3aa6a0ce4160d4f046018dc1c95063335dcf6e35f5958dc3683cb8d5fc`

```dockerfile
```

-	Layers:
	-	`sha256:888cc432f95b3b97268eb330244043b1afa695d2d1f5bf33fb3310ee1afce9e3`  
		Last Modified: Mon, 17 Mar 2025 23:45:01 GMT  
		Size: 6.1 MB (6062010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caf300ef933ca1694c70eab4f883bf06d15d9ffee13da1538a0c97c3c73f3c32`  
		Last Modified: Mon, 17 Mar 2025 23:45:01 GMT  
		Size: 53.4 KB (53438 bytes)  
		MIME: application/vnd.in-toto+json
