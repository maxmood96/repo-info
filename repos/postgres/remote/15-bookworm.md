## `postgres:15-bookworm`

```console
$ docker pull postgres@sha256:a1e2ed7bd88c2b548da4709480c5b26ffbd1ea344d1614861ff0a0af6783d2d4
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

### `postgres:15-bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:e4713195170af4a1661a205512186d3cdb0c80a21a93d572fafdad303b2fbf48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151259776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b11af774b629c3b903c6c1cfa5d4e0915bb3dab041aa3946ef12cf1e20e835ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 12 Feb 2024 19:12:29 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Mon, 12 Feb 2024 19:12:29 GMT
CMD ["bash"]
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
ENV GOSU_VERSION=1.16
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
ENV LANG=en_US.utf8
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
ENV PG_MAJOR=15
# Mon, 12 Feb 2024 19:12:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Mon, 12 Feb 2024 19:12:29 GMT
ENV PG_VERSION=15.6-1.pgdg120+2
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 12 Feb 2024 19:12:29 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 12 Feb 2024 19:12:29 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Feb 2024 19:12:29 GMT
STOPSIGNAL SIGINT
# Mon, 12 Feb 2024 19:12:29 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 12 Feb 2024 19:12:29 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992c3cda2b1723d0b3e51cbc5b8e65fc690a9010e52ccb33d4a036fa9800d11a`  
		Last Modified: Tue, 13 Feb 2024 01:58:44 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a35a0941f71a32bc1f35216f49424d27f2de2defd8501700f5d46f946ddc1d3`  
		Last Modified: Tue, 13 Feb 2024 01:58:44 GMT  
		Size: 4.5 MB (4533432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5008e6b22411e00752e11b53a98454b0a663d2a57a06b7ec1ae58e731fb147fc`  
		Last Modified: Tue, 13 Feb 2024 01:58:44 GMT  
		Size: 1.4 MB (1446200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b748b60d7b8221fed081765b1ca1bbf0fba0e4a21a147ee9566cdf61f781f6`  
		Last Modified: Tue, 13 Feb 2024 01:58:44 GMT  
		Size: 8.1 MB (8066224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7dd426d9c3c623ee4fed89fa78a0f331e95b5cf082c2ccc3a081f70d1a1514`  
		Last Modified: Tue, 13 Feb 2024 01:58:45 GMT  
		Size: 1.2 MB (1196028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00767100b5b5e9413aacfa6b1693b8e4c4b8a29a6444d8db1b6d87e5296cecf0`  
		Last Modified: Tue, 13 Feb 2024 01:58:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d555127a7a111b6c2c195d36605b51a26b14de5d10bd1f7d0d1e81947f268f`  
		Last Modified: Tue, 13 Feb 2024 01:58:45 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb2fc34223e1602ef51615062a641880362b6d43a992ebd348a948a5b3b2ac4`  
		Last Modified: Tue, 13 Feb 2024 01:58:47 GMT  
		Size: 106.9 MB (106873711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37fd6fddcc91c67cb0c5427528743b70f3e034c249769fb7c252ac6870ea0714`  
		Last Modified: Tue, 13 Feb 2024 01:58:45 GMT  
		Size: 9.8 KB (9770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa92d99e0c6f6ab0fc155cbbf9d67f454d5c21f7b941ae3522553fa1b11a95a`  
		Last Modified: Tue, 13 Feb 2024 01:58:46 GMT  
		Size: 129.0 B  
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

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:7d7ca0047ae0d1eb9caaa84bde6abeafec730d7c3d823e2dd6d0ed0ad17e227c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4950368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cecb29d542d91034d54a4278047b3cd1bd9f344ccbd8a82954690a46bc2bea58`

```dockerfile
```

-	Layers:
	-	`sha256:8df42afd5873525083c5ced414ab9eba4e9d7151c3fd9eb0d206d9a9e4616e60`  
		Last Modified: Tue, 13 Feb 2024 01:58:44 GMT  
		Size: 4.9 MB (4895743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f78526069d3c11df8b3fd84f106e86d2e2adc4e0ddc6fc20f68c99ff756b6cce`  
		Last Modified: Tue, 13 Feb 2024 01:58:44 GMT  
		Size: 54.6 KB (54625 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:8b6fd5506388839aea58d468454db063d045cf45a9e047b937bb75599eb42cd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.9 MB (143945456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e99e4d8ba62429a5930039ec54ffa90dc2d4eeb62c801d25611e6f0116fa94ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 12 Feb 2024 19:12:29 GMT
ADD file:468c16fc087244db1784e8f07bec3a1a417cd85172afa7dc960c2d1ecd1f37bc in / 
# Mon, 12 Feb 2024 19:12:29 GMT
CMD ["bash"]
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
ENV GOSU_VERSION=1.16
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
ENV LANG=en_US.utf8
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
ENV PG_MAJOR=15
# Mon, 12 Feb 2024 19:12:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Mon, 12 Feb 2024 19:12:29 GMT
ENV PG_VERSION=15.6-1.pgdg120+2
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 12 Feb 2024 19:12:29 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 12 Feb 2024 19:12:29 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Feb 2024 19:12:29 GMT
STOPSIGNAL SIGINT
# Mon, 12 Feb 2024 19:12:29 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 12 Feb 2024 19:12:29 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e0d489e60efeee042d73afc4d45ad77014188c0ac8941f9ba5f15760d2288c3a`  
		Last Modified: Tue, 13 Feb 2024 01:13:30 GMT  
		Size: 26.9 MB (26883902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ea0b0e7670aea8015785787fce52735329103a2d1df2c9abd1867261873ecc`  
		Last Modified: Tue, 13 Feb 2024 22:48:33 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca10a6275e365e3a7c4bf95fedd13ae8f4ab527acd4fb619f169574436fcd6b`  
		Last Modified: Tue, 13 Feb 2024 22:48:34 GMT  
		Size: 4.2 MB (4150724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988d19a7bcf4478b200e95015d773db4c9ab9e01635bef72ea6b7cbbe5269f65`  
		Last Modified: Tue, 13 Feb 2024 22:48:33 GMT  
		Size: 1.4 MB (1423772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cdc97b174e240f6129f20c381100f957deeb8444b39108fb201c771a363b8bb`  
		Last Modified: Tue, 13 Feb 2024 22:48:34 GMT  
		Size: 8.1 MB (8066360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e60ad6fb99d69af0c734978930805d284538c6521c4b83d2817e6ced87eb28`  
		Last Modified: Tue, 13 Feb 2024 22:48:35 GMT  
		Size: 1.2 MB (1194807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72809ae367f602f3c6b101d8a3061c4ad45ed968b75478ccf13b952ca6e408c`  
		Last Modified: Tue, 13 Feb 2024 22:48:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91666c8da4ce630dadb500c805b546aee5128d69aff5adb04f007dfb59b3a89`  
		Last Modified: Tue, 13 Feb 2024 22:48:35 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00581ecc2816bc5bde4b21dee1a481df5e2ea7fff0c40438de9b59f73521ea2e`  
		Last Modified: Tue, 13 Feb 2024 23:35:01 GMT  
		Size: 102.2 MB (102205800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34080c61236620b24397d75be7fdd0a6eef305a1296e34b02146408bfdd644de`  
		Last Modified: Tue, 13 Feb 2024 23:34:59 GMT  
		Size: 9.8 KB (9776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4c3a07127894a85c163ce1138d6e05b9e337e6c36fa884b8db5ad75aea935c`  
		Last Modified: Tue, 13 Feb 2024 23:34:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbcbbb74af098b3bc49eded99c9026a16b2fbe258bee452231725f832411f1ed`  
		Last Modified: Tue, 13 Feb 2024 23:34:59 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e54db71eb48b5d2e47ba914d9285919ce93909b034e8134106999cd2a58056`  
		Last Modified: Tue, 13 Feb 2024 23:34:59 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987c882e69db160d7d078475ec88360bf30dc3664841b0e3bdbb26b630b6db3b`  
		Last Modified: Tue, 13 Feb 2024 23:35:00 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:f1d0e3196f9e727bb555db812b7fd60a24caa8b960746e545000156ac1a45be2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4960873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0aadbf9ab2aa9ed8ed8643b2a33d082b7c6fc100e743d624e01334c38bccae5`

```dockerfile
```

-	Layers:
	-	`sha256:31db12d3754ed938a8ce035d0aad81b4e98370a5c81034c02fb6b630f15412e9`  
		Last Modified: Tue, 13 Feb 2024 23:34:58 GMT  
		Size: 4.9 MB (4906203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:018318bb5c6c1b652dfbd39641d011c7a7410dfa1e018601391af97a39dcf7d6`  
		Last Modified: Tue, 13 Feb 2024 23:34:58 GMT  
		Size: 54.7 KB (54670 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:90fca643f8da982a27f6053579106cb8f7de792c1a07297c06b3a494f7c462f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.2 MB (139161173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf681668242dbe4b27386da4220e85d1c17cec5cb4fc4d8e4ea2e8b6af3ee15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:20 GMT
ADD file:d6072ced9736ca566086eea2514cf12faccec9859bbd93e83950ad51f6827e8c in / 
# Wed, 31 Jan 2024 22:44:20 GMT
CMD ["bash"]
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
ENV GOSU_VERSION=1.16
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
ENV LANG=en_US.utf8
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
ENV PG_MAJOR=15
# Mon, 12 Feb 2024 19:12:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Mon, 12 Feb 2024 19:12:29 GMT
ENV PG_VERSION=15.6-1.pgdg120+2
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 12 Feb 2024 19:12:29 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 12 Feb 2024 19:12:29 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Feb 2024 19:12:29 GMT
STOPSIGNAL SIGINT
# Mon, 12 Feb 2024 19:12:29 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 12 Feb 2024 19:12:29 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:404006a0fd99beed6ef1a9502692bd5005ae8c3b9d36a9b48654f7dfaacfb2c5`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 24.7 MB (24741565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a70dc692e9443904c6069756eb156b90f67f2e2c99918eaebc5cfe1f007c1aa`  
		Last Modified: Fri, 02 Feb 2024 03:03:30 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2090feeb63cbb6332dee960b9803500ff3e6ae9b6b950b4f6b746456d0fd55ad`  
		Last Modified: Fri, 02 Feb 2024 03:03:31 GMT  
		Size: 3.7 MB (3742397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2dd583392beb505f2e9bc09e7cfde0f8875381fa4f16c002093c9716062837d`  
		Last Modified: Fri, 02 Feb 2024 03:03:31 GMT  
		Size: 1.4 MB (1416970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107f785849d75f92900ffb600a7b9175a0addd5dc8980f018bed254ee23b9690`  
		Last Modified: Fri, 02 Feb 2024 03:03:32 GMT  
		Size: 8.1 MB (8068718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211c3edde7d4cf123a87f977cd07a61b3911ede96782fa7f4c401f2c224b1706`  
		Last Modified: Fri, 02 Feb 2024 03:03:32 GMT  
		Size: 1.1 MB (1066815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd8534794dcf1606fde4783bb9b117c99e7494da2a36f72831584fb4f073f9b`  
		Last Modified: Fri, 02 Feb 2024 03:03:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6743540547fb2fa57104883757041f926ed2e54a20f513ab1450cc90f8ecf614`  
		Last Modified: Fri, 02 Feb 2024 03:03:32 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c49894ef8ca77b9de726236bd8711b8c177dfcf95b313d92f2e9f439cb3d081`  
		Last Modified: Tue, 13 Feb 2024 00:32:23 GMT  
		Size: 100.1 MB (100104582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7c1e13cb6a2cf512b71f566b9c705f0fe6dad5c83b210be7bf6fa026906397`  
		Last Modified: Tue, 13 Feb 2024 00:32:19 GMT  
		Size: 9.8 KB (9791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d4bdb6d072b21468b3e7687d797c418e0884db51818acc83190f42ce98e440`  
		Last Modified: Tue, 13 Feb 2024 00:32:19 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca578612b8381de956d29692e39afea7785e1f32ddd81107faf013d8319348d`  
		Last Modified: Tue, 13 Feb 2024 00:32:19 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5845d7db460decb284d58f09e314e810321b8c63d1033e9baae94f876e1364fd`  
		Last Modified: Tue, 13 Feb 2024 00:32:20 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ab9d8f555568783456d7f890252655308b8abd1fe12dddb856b30b1d26dcc5`  
		Last Modified: Tue, 13 Feb 2024 00:32:21 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:66de604b842dc2610b13419b04e8dbc90c96dec22af26daeb19f125c5188250c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4960743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c1a9efc12642e4cff9d49c6daea25a598acf8e4b67bc638d6bfb5c2f661441`

```dockerfile
```

-	Layers:
	-	`sha256:88292ed4ea10b025eb7d677afcff964cbb1ba416ab990076479b0e57fd3a2df9`  
		Last Modified: Tue, 13 Feb 2024 00:32:20 GMT  
		Size: 4.9 MB (4906073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3be93927f7394c4f0c680e49637a9d67e2763855b633a8314f15413e560ec8b1`  
		Last Modified: Tue, 13 Feb 2024 00:32:19 GMT  
		Size: 54.7 KB (54670 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:442671beb80862c68857738dc97f2aea517dfd3b2e1824af138d7979c4824754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.5 MB (149485620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e38128c00449776b7e4c3002e9d3cc4c59c30e63838b44780419976c16dfcf6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 12 Feb 2024 19:12:29 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Mon, 12 Feb 2024 19:12:29 GMT
CMD ["bash"]
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
ENV GOSU_VERSION=1.16
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
ENV LANG=en_US.utf8
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
ENV PG_MAJOR=15
# Mon, 12 Feb 2024 19:12:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Mon, 12 Feb 2024 19:12:29 GMT
ENV PG_VERSION=15.6-1.pgdg120+2
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 12 Feb 2024 19:12:29 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 12 Feb 2024 19:12:29 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Feb 2024 19:12:29 GMT
STOPSIGNAL SIGINT
# Mon, 12 Feb 2024 19:12:29 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 12 Feb 2024 19:12:29 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926c64b890ad3e280473310f439d2f2aea933be44c67eb3bcb41bdb1bbd4c4cf`  
		Last Modified: Wed, 14 Feb 2024 07:32:05 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca757527cc4e639ac5ec5d1d5393acd54c238d1a4017f14ffa6e36d86f0ad76`  
		Last Modified: Wed, 14 Feb 2024 07:32:06 GMT  
		Size: 4.5 MB (4498899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffbe79d4ccf8b20e6bcdc64f652c1c6ce6527a7ba3e9f5ffc14152936818fbd`  
		Last Modified: Wed, 14 Feb 2024 07:32:05 GMT  
		Size: 1.4 MB (1378163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948961f25f1c405c47b16481b1e29402f8bbb57399f2c2e3a397cbf44621af35`  
		Last Modified: Wed, 14 Feb 2024 07:32:06 GMT  
		Size: 8.1 MB (8066335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de342bb9830910fbe1e7d63176676e06e6cf3ca5edaf40a39e5cfe17388009ef`  
		Last Modified: Wed, 14 Feb 2024 07:32:06 GMT  
		Size: 1.1 MB (1108635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3793b15c294c77a56ef1c0ba5fbb1a03ed52d99f87dd3710350486cc98b78a0b`  
		Last Modified: Wed, 14 Feb 2024 07:32:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75dcc1faad83c7a25153110fb658d2c6a20d08959c3d599dd9df456bf489ea34`  
		Last Modified: Wed, 14 Feb 2024 07:32:07 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d705f0464bc8fba6c0ac8fb1836bf80fe54ae2bebb0329e1e15be5708b1eea`  
		Last Modified: Wed, 14 Feb 2024 07:34:29 GMT  
		Size: 105.3 MB (105257122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc648dfb1ae3d8fa1d54529cd7d61e65f79373cbd79254b1b99cb01b215ac5c`  
		Last Modified: Wed, 14 Feb 2024 07:34:26 GMT  
		Size: 9.8 KB (9776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9793f4b16bf39c6781b8e17671c27f7c5439faf9c630d43abcdfb9bba81f5b6`  
		Last Modified: Wed, 14 Feb 2024 07:34:26 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d82c333540fbd5b2158f9f50669ac02c6fcf84456aea8dfcb2ce8f67ee7e19c`  
		Last Modified: Wed, 14 Feb 2024 07:34:26 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3108c8ab7232d4cbf5551d0cc682a5e5ea31f460cf93c6235e20c0daf44769d9`  
		Last Modified: Wed, 14 Feb 2024 07:34:27 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548a706f1899b4ff1b07812c547d6181eb930e24f20a7c551b0f67a5f1cc0ed4`  
		Last Modified: Wed, 14 Feb 2024 07:34:27 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:f3bd466f63f29e90779b2f9cdc93575fc02544e6b7a84537e66d743e9377d628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4955871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cabc8847f30da57d4d31dff4f68aa19af60965d375a2e681d431d180a95d647f`

```dockerfile
```

-	Layers:
	-	`sha256:bfc890d883b6d48271c1a7db0f04133c025429becb16b0062a80cf8021c7c410`  
		Last Modified: Wed, 14 Feb 2024 07:34:25 GMT  
		Size: 4.9 MB (4901403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6a7b7aba191c3f418570101db7f70d32bfaaccd0ab5bdfabd722c55ef59057d`  
		Last Modified: Wed, 14 Feb 2024 07:34:25 GMT  
		Size: 54.5 KB (54468 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:cecfa5410d0a563c6793e6c033629706f3c838b91ab904ce41fe24970d1a1b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159292108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7e734f2b8e98fd2cbe77249f8b68703bff5eeba848a65d297737b034fadf2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 12 Feb 2024 19:12:29 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Mon, 12 Feb 2024 19:12:29 GMT
CMD ["bash"]
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
ENV GOSU_VERSION=1.16
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
ENV LANG=en_US.utf8
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
ENV PG_MAJOR=15
# Mon, 12 Feb 2024 19:12:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Mon, 12 Feb 2024 19:12:29 GMT
ENV PG_VERSION=15.6-1.pgdg120+2
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 12 Feb 2024 19:12:29 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 12 Feb 2024 19:12:29 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Feb 2024 19:12:29 GMT
STOPSIGNAL SIGINT
# Mon, 12 Feb 2024 19:12:29 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 12 Feb 2024 19:12:29 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21523211d4827e09e67b44ace7bd046e2cb433ce6434e97b5f05436bc0eb47c4`  
		Last Modified: Tue, 13 Feb 2024 02:11:18 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d95b942cfc1d9ce1314fd03d925bbee9b4c8dccaddbf67f7558278771d7f816`  
		Last Modified: Tue, 13 Feb 2024 02:11:19 GMT  
		Size: 5.0 MB (4964362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e368d2b8daba69ff558a08928187dccf5933d0f5c104b8baf7795136209f650`  
		Last Modified: Tue, 13 Feb 2024 02:11:18 GMT  
		Size: 1.4 MB (1421765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:449992108bb04cb330e04e7b98c95c4d4afbc6c46d7f8aa8352a38eed3349828`  
		Last Modified: Tue, 13 Feb 2024 02:11:19 GMT  
		Size: 8.1 MB (8066259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b62b826a414261acfbcc4620ea5885766d752619734a24aa7c34ca009dd8b3`  
		Last Modified: Tue, 13 Feb 2024 02:11:19 GMT  
		Size: 1.1 MB (1137107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f6781fbd8ae110a6a3185a41f9a7723bffe544882be389419900fbba8c4040`  
		Last Modified: Tue, 13 Feb 2024 02:11:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d70da4531a2f8d1e1910a7dfe0e7a8d894f7f4298ac1ba018540a3a0c37518`  
		Last Modified: Tue, 13 Feb 2024 02:11:20 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9649254b0594e172fd35a2b6549fb0b17b2a017e5c02f35e83060e46ebae38ab`  
		Last Modified: Tue, 13 Feb 2024 02:11:24 GMT  
		Size: 113.5 MB (113540712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a1bc3429852b5b021d4e834f7a4e57cb9caa67c07e51dd1bac27b30b07d3b9`  
		Last Modified: Tue, 13 Feb 2024 02:11:20 GMT  
		Size: 9.8 KB (9777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39fdb00f49a73042dfb25b81e9268f0822c0068e083002b0e1b41f79322325e0`  
		Last Modified: Tue, 13 Feb 2024 02:11:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed29033f6183ba10db70f10b91a24e99c5c9dfba329ddfcfbb2b9f8eb07346c2`  
		Last Modified: Tue, 13 Feb 2024 02:11:21 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104e0bd7f01d56fa10b17704d37816b6115d03c327de0e9b714db87b8016e9b1`  
		Last Modified: Tue, 13 Feb 2024 02:11:22 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619dc26c5985d66d3f3e5dc6d3e08ec42c679a7edde9ba89418a2e6cf3d4d495`  
		Last Modified: Tue, 13 Feb 2024 02:11:22 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:61257c90692c66e1e7f51df1ee69c33de940f5f1ce4fb7bff622760aac0f25b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4958512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f39b3ffe3310915ab536421e4fe6f4d318b91797061a884ad10d63b5887bb1b`

```dockerfile
```

-	Layers:
	-	`sha256:ec515c957943e40eb0ca17832d4be553087adf18680aec883a7a834e7dc565b6`  
		Last Modified: Tue, 13 Feb 2024 02:11:18 GMT  
		Size: 4.9 MB (4903938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6db2792fdbf4b56a093fcf5628fa120ba1d0f663eebef3cd6218c8fb267b5e76`  
		Last Modified: Tue, 13 Feb 2024 02:11:18 GMT  
		Size: 54.6 KB (54574 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:e0e8e4fc99f5e9c22e69324d7e677a5504907df3c0f58ff5d6a459a650a6bd58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.7 MB (146651442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653a8c851e1945cc6ee0ce8a77ca809cb6299032fab02dd2b906f629d54722ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 12 Feb 2024 19:12:29 GMT
ADD file:7b0bbeed7888e49f58bdffd816596bc88b87bd4a3761c5a2590f3123c077899b in / 
# Mon, 12 Feb 2024 19:12:29 GMT
CMD ["bash"]
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
ENV GOSU_VERSION=1.16
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
ENV LANG=en_US.utf8
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
ENV PG_MAJOR=15
# Mon, 12 Feb 2024 19:12:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Mon, 12 Feb 2024 19:12:29 GMT
ENV PG_VERSION=15.6-1.pgdg120+2
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 12 Feb 2024 19:12:29 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 12 Feb 2024 19:12:29 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Feb 2024 19:12:29 GMT
STOPSIGNAL SIGINT
# Mon, 12 Feb 2024 19:12:29 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 12 Feb 2024 19:12:29 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:78ede1ea2c0b185708583060a40bd2aeddee7b533566b4df729e98e5e5de458b`  
		Last Modified: Tue, 13 Feb 2024 02:15:10 GMT  
		Size: 29.1 MB (29119092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56171fe936c6b25b6e67f412e05d01490e9ce71d9e38dd05402df936f3abdb5f`  
		Last Modified: Wed, 14 Feb 2024 18:54:59 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758cfc974d09063935b449905db40f0ae4857a1afdced0e14a438847fb83de8a`  
		Last Modified: Wed, 14 Feb 2024 18:55:00 GMT  
		Size: 4.5 MB (4474419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8724f859beb4c236f992331b9f83fff8688e2b79c198fea0f641d84a58363797`  
		Last Modified: Wed, 14 Feb 2024 18:55:00 GMT  
		Size: 1.3 MB (1333553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d9c11f1c678b2436420a3e07990deffeb86977c7dcc5f1ef91b044759cb3ad0`  
		Last Modified: Wed, 14 Feb 2024 18:55:01 GMT  
		Size: 8.1 MB (8066441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04bb055783199c101c8da24e55f8488e31c9a94569c1043da636c3842a5fa02`  
		Last Modified: Wed, 14 Feb 2024 18:55:01 GMT  
		Size: 1.2 MB (1182595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b12d3d7935a70abadad1f881054dcae05098206da48785d270ef1c063eeada`  
		Last Modified: Wed, 14 Feb 2024 18:55:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78530ea48860c5e1c7365d1b2554825cc041e375a644db42e0eeb2cea3dd6a06`  
		Last Modified: Wed, 14 Feb 2024 18:55:02 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97188485ab307550f3bddfae0fa3e8c6064d14600ec28b1900447cc5641fe595`  
		Last Modified: Wed, 14 Feb 2024 21:18:38 GMT  
		Size: 102.5 MB (102455230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934a3630daf68dea1f0c15915c18e7f4a2b177f555966dc73c00947519e8d362`  
		Last Modified: Wed, 14 Feb 2024 21:18:28 GMT  
		Size: 9.8 KB (9780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c11b8e7ec71781c910b4fe2c622ef3aac194b957cf5d11b2dc48ba7b031162`  
		Last Modified: Wed, 14 Feb 2024 21:18:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f19978f42d8f480669ab5cc7b6f2c68e056eb60b383663deedf77e4accb273`  
		Last Modified: Wed, 14 Feb 2024 21:18:28 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f28af5cd92f48fbf2035f6433346e27422377e94c35a86bbe3698964581274`  
		Last Modified: Wed, 14 Feb 2024 21:18:29 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19dd480a1f41e0ed146b0bd1f66b71142a810055bcfdbf5258dfbd2101ea9d4b`  
		Last Modified: Wed, 14 Feb 2024 21:18:30 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:bdedf797e01ea55cfe03f07d22bb1b4f3f1fb17d918bc8e195cb869730aec120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 KB (54333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6a2a8e2fa512caf060f2584b85057fc322d5ba05b52222426c678a13aff5d9`

```dockerfile
```

-	Layers:
	-	`sha256:99530f03d87e508df7abd8882b8244ee779d09ca812c9dd612a2d7f52ab59444`  
		Last Modified: Wed, 14 Feb 2024 21:18:27 GMT  
		Size: 54.3 KB (54333 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:a3c073209fb5497c8bd7a855201d195ecb07a2e41ee8aa34834e04df79e0b2c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163445203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4efbb5de74a12f4bae16a242a7d1e97cc1b3e77c4e71ccace1300cad74f66d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 12 Feb 2024 19:12:29 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Mon, 12 Feb 2024 19:12:29 GMT
CMD ["bash"]
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
ENV GOSU_VERSION=1.16
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
ENV LANG=en_US.utf8
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
ENV PG_MAJOR=15
# Mon, 12 Feb 2024 19:12:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Mon, 12 Feb 2024 19:12:29 GMT
ENV PG_VERSION=15.6-1.pgdg120+2
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 12 Feb 2024 19:12:29 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 12 Feb 2024 19:12:29 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 12 Feb 2024 19:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Feb 2024 19:12:29 GMT
STOPSIGNAL SIGINT
# Mon, 12 Feb 2024 19:12:29 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 12 Feb 2024 19:12:29 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd2881d71e211f5fd3ecf1f293d90e384c26c6985deb1a1f12b50ce18d148ed`  
		Last Modified: Wed, 14 Feb 2024 03:34:07 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd497aa07c70675c6dc14ae607f791fb94eef6054113d7e387591b0f06eb4ef0`  
		Last Modified: Wed, 14 Feb 2024 03:34:07 GMT  
		Size: 5.4 MB (5368101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac794d2e4a2efa5bc712d62ec33a8e273d3b6b21f933c6e188369b839ff5c51`  
		Last Modified: Wed, 14 Feb 2024 03:34:07 GMT  
		Size: 1.4 MB (1368483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a557ab96c433b491fecb537d90783282a6c30f6b739808884a07c1849c81ce37`  
		Last Modified: Wed, 14 Feb 2024 03:34:08 GMT  
		Size: 8.1 MB (8066365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4853b48fd279ea9197e0de8b5be518c1a5b8747fec373d57a6dc7d1cf73c5fb4`  
		Last Modified: Wed, 14 Feb 2024 03:34:08 GMT  
		Size: 1.3 MB (1283519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb72fb069928ca90f07937e19a087768b49392566b2b92a793b896ffca415e3`  
		Last Modified: Wed, 14 Feb 2024 03:34:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b51de8ea37018cf49f65728922902d15e7a2ea1750fafc3a81e438cb347eef`  
		Last Modified: Wed, 14 Feb 2024 03:34:09 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a984d88676be517d7257d97d3f96c8c51725eed343323d9948993ae4f3f3a7`  
		Last Modified: Wed, 14 Feb 2024 03:41:40 GMT  
		Size: 114.2 MB (114219727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361862c5b4c9d51224e75d7c83d29550c4d5ee83ed68b2f82ce5af6a25ef8e5c`  
		Last Modified: Wed, 14 Feb 2024 03:41:37 GMT  
		Size: 9.8 KB (9776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88a2390d3a0a5e7cc211e2c3d2c9ab34258534ecf72f93d37a8b7aa2579c45f`  
		Last Modified: Wed, 14 Feb 2024 03:41:37 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cbdcdfa1d962a8cb5db5759f117eb5df678a929027004c954eecdd95f1231c`  
		Last Modified: Wed, 14 Feb 2024 03:41:37 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215ab9c5b5c36577a3250eb7f1122582e05e4f093ae65e1b19ab975d42d3c93b`  
		Last Modified: Wed, 14 Feb 2024 03:41:38 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d039bdfbcc4cec5e9f79c7b2b4eab8cffcd126e321e54e9524be7e29d6449c`  
		Last Modified: Wed, 14 Feb 2024 03:41:38 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:9c89776459c89ae8217a2cffb3a16015ec6c2e8c2eb1759404fd32fcddc95ae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4957490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93d00caae36bbce257cd3fa272ee9a9d466107a759482e3db0e09a88fa343d1a`

```dockerfile
```

-	Layers:
	-	`sha256:76d1357fdcb9b608b709e6ed588e2a8d6605ef37f334082dfb0f676fda4cb34a`  
		Last Modified: Wed, 14 Feb 2024 03:41:37 GMT  
		Size: 4.9 MB (4902972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cab1928ee76b7006881a16524f0d812aa0e0dd8d3c056c282044faddf2d0173c`  
		Last Modified: Wed, 14 Feb 2024 03:41:36 GMT  
		Size: 54.5 KB (54518 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:19701874ac2bbbb65e1170a895556064648265cfc08c6fad812784f2836a8d49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.7 MB (156658062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7788a172a7c1c4418b5cf30c2bf355a44b964f8eb24220f2de39e51d858a5bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 04 Jan 2024 21:52:40 GMT
ADD file:d543e4bc70d0d1d81c594a97289d7f2b4925d86461644cf881890997abfb6ead in / 
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
ENV PG_VERSION=15.5-1.pgdg120+1
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
	-	`sha256:84abfb784f629f520e19ebd281090b7f1b3b78ff96b3be919578a053d2708ad5`  
		Last Modified: Wed, 31 Jan 2024 23:29:10 GMT  
		Size: 27.5 MB (27513479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ebaf1e2854aa44f14e7255cf6b3c9224bec168d8f04bc034c6bd9be8657038`  
		Last Modified: Wed, 07 Feb 2024 07:37:28 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2344d8214aa5bca7df7df9e71b92fa9a5edfe44017185bcc0ec521a66125f005`  
		Last Modified: Wed, 07 Feb 2024 07:37:28 GMT  
		Size: 4.4 MB (4390612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7665699d77ba8123b3db4282477f3806915ff4a90dc6c2a4b0e1c480354ccd0`  
		Last Modified: Wed, 07 Feb 2024 07:37:28 GMT  
		Size: 1.4 MB (1415117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61097bc9bd0214d1f63463bd5dc372ad88fa310b31ef3cdd08ef1109cf59df7`  
		Last Modified: Wed, 07 Feb 2024 07:37:28 GMT  
		Size: 8.1 MB (8122904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8b69f95a58a0743c1f14cfdf4970d9403e2b8203eca0cdaeefa0f893fb24b3`  
		Last Modified: Wed, 07 Feb 2024 07:37:29 GMT  
		Size: 1.1 MB (1096511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da06ef3a6eafda0295bb417794e019582520af20e9e67bc718155f64dd71d8da`  
		Last Modified: Wed, 07 Feb 2024 07:37:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6696e321975221c6dcd1d8cd992ca40f50159a6275f025a283de3585cda60511`  
		Last Modified: Wed, 07 Feb 2024 07:37:29 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01052ae360bc763124c3b73f7dfb7f1d6befd414f7d32e7fecf10ddf8d728c71`  
		Last Modified: Wed, 07 Feb 2024 08:26:47 GMT  
		Size: 114.1 MB (114099326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc41dc0704182f605c2c0353f5e2a23a7712526bb915416025b6fa7533bb0651`  
		Last Modified: Wed, 07 Feb 2024 08:26:45 GMT  
		Size: 9.8 KB (9785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfd50902b16831b22e9418e9701ff7bba5008e90ab6958835d375306e31ab9e`  
		Last Modified: Wed, 07 Feb 2024 08:26:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4caebc46f60638d564b0ecd7a2394697042d46ab5d99d0122449b0bd3a01ee4a`  
		Last Modified: Wed, 07 Feb 2024 08:26:46 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffdbb1d71051f526ad28d1392cc413069f8a3fade9c3d59604ba92d3eee8e280`  
		Last Modified: Wed, 07 Feb 2024 08:26:46 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ddebec79784c28ecea868e0bdf11edb47bf838f24940d93871e5471a52da6a9`  
		Last Modified: Wed, 07 Feb 2024 08:26:46 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:07338f5cf5ceaf476cd5b7e1c2fc45ef0c409b54d488604b88961b4a772f5dd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4949305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af9363863036e60e64e4088750764e878d6054e95b822711ddce7770c1f493a`

```dockerfile
```

-	Layers:
	-	`sha256:ffc3e1a4f76a5a55076f0b5a29e19893c1d79638632e41b71490557635603fe1`  
		Last Modified: Wed, 07 Feb 2024 08:26:45 GMT  
		Size: 4.9 MB (4894847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:600591a08bec81ac5027077ba7725f097d2d461223d1204c8ec2db358df374e3`  
		Last Modified: Wed, 07 Feb 2024 08:26:45 GMT  
		Size: 54.5 KB (54458 bytes)  
		MIME: application/vnd.in-toto+json
