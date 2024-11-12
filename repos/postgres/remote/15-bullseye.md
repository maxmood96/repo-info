## `postgres:15-bullseye`

```console
$ docker pull postgres@sha256:e89e01b464adcb90e31f673359bb9fc91f293e2c770aadf5801a970e5bfc7539
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

### `postgres:15-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:e66a0985ee489b6f51612ce17027139117f99b6d3a9909f687010aa995a5d1c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.9 MB (142942863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c76bcd3a661bf7177a21d87b5aac274df303249c209cda0efa14b75f15bf0245`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:06:32 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_MAJOR=15
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_VERSION=15.8-1.pgdg110+1
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:06:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:06:32 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:06:32 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:06:32 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:06:32 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516e670f76defc23acb2c0dc7d9c467ff2e5db2afed9f63334355562ee57e3a6`  
		Last Modified: Tue, 12 Nov 2024 02:11:17 GMT  
		Size: 1.7 KB (1683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8202c7054c795bbcc9cee5362afd0cb1d8044003a9f63699c0cd3441cbb1a5d`  
		Last Modified: Tue, 12 Nov 2024 02:11:17 GMT  
		Size: 4.3 MB (4308171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4493463449f80d294d512c7f90b73145e2f0ba5b76996bfcd81a4efff303c16c`  
		Last Modified: Tue, 12 Nov 2024 02:11:17 GMT  
		Size: 1.5 MB (1472234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd6bd6b20be72bcb852384587b2147e26877395a53cdea4062614e810edff4b`  
		Last Modified: Tue, 12 Nov 2024 02:11:17 GMT  
		Size: 8.0 MB (8044556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8331472b7254ec296e3994e59586309e136dfd9c2e6d23a7f9afb7f8b0a8b3a4`  
		Last Modified: Tue, 12 Nov 2024 02:11:18 GMT  
		Size: 1.0 MB (1038332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbb847e60117ca506f0901d2199d64ca7b2cea28bdae28c68975b4cd9872a38`  
		Last Modified: Tue, 12 Nov 2024 02:11:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b148653b866bfccb513639a022d651ef4d79fded318e3ae861d6ea779f5ee5`  
		Last Modified: Tue, 12 Nov 2024 02:11:18 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb92aacfeb806e5f43bb11d01bb1019d77b9a9b7b7204643c4084d668f466a7a`  
		Last Modified: Tue, 12 Nov 2024 02:11:22 GMT  
		Size: 96.6 MB (96607389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c71022e4061e6b4901ddf753d04430ad77ab85555e4d9a2a7fff45acbea52b`  
		Last Modified: Tue, 12 Nov 2024 02:11:19 GMT  
		Size: 9.8 KB (9778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fbd3f077e2e659acf6a42ddefbb2a65e1fb401317dd516a80b1f62c99a7476`  
		Last Modified: Tue, 12 Nov 2024 02:11:19 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea15ef59043dc592ee7a1b08554ffdc955359a0b5bdbb7f7c9ba1c3c8a94f11`  
		Last Modified: Tue, 12 Nov 2024 02:11:19 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de9cd69634cd62d16b388d30174de64e2014aa709ff38cd7a36cf522090721b`  
		Last Modified: Tue, 12 Nov 2024 02:11:20 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c11f106b56c581fa83dcc8d802816112ff6c8f3e7e6fa9419ecbdedab5ff69b`  
		Last Modified: Tue, 12 Nov 2024 02:11:20 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:d90483a7801b4e068b56c4984b96bdc4a0b63b6582e546278b69095be7ddb9e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6005664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc7ece527e08579f1a5a0405e4a59cfcb629a4feb79cbeae4313e4044845704`

```dockerfile
```

-	Layers:
	-	`sha256:143e0ff7a1581fa35def95ab1eb6c7700c37a01b6ccc8e6266ed8ebe3ac06a66`  
		Last Modified: Tue, 12 Nov 2024 02:11:17 GMT  
		Size: 6.0 MB (5951684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:716dc91d55a6279cb2f94837d4236d6bb8150bc334f4db38b2e01974f0c114cd`  
		Last Modified: Tue, 12 Nov 2024 02:11:17 GMT  
		Size: 54.0 KB (53980 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:206882f697d6f52afd63e6f0c4abe1e38a0e6e1a80aaf4e966fc049c81948073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130889845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:323bacbf292ad3db279d83f7f1881e550cef495e1d9e3fe3d48400bc491ec247`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:06:32 GMT
ADD file:1a0a5d58e9eaa765a367c84b6a41097f2f807ca887b02e8a1a36fa504592a5e4 in / 
# Thu, 08 Aug 2024 17:06:32 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_MAJOR=15
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_VERSION=15.8-1.pgdg110+1
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:06:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:06:32 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:06:32 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:06:32 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:06:32 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:25eb86cb375819dcc30b18c185d2922f7f09900a247460cef95d47222230e7dc`  
		Last Modified: Thu, 17 Oct 2024 03:08:12 GMT  
		Size: 26.6 MB (26589555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de32be9c720a52367b74940afdb2d3e32862ccfc2147df092aa04adf6a42f26`  
		Last Modified: Thu, 17 Oct 2024 18:32:55 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ff15a87f66f6a908a6a576490ac34bf482409d26897b5135ebd6948998dd0f`  
		Last Modified: Thu, 17 Oct 2024 18:32:56 GMT  
		Size: 3.6 MB (3601804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ffc3f08141a457f9b4c53e40f5589900074e98aac2c94bd540d05315b969199`  
		Last Modified: Thu, 17 Oct 2024 18:32:56 GMT  
		Size: 1.4 MB (1439278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3822cf805c301d7318b7c57c3f006094cff7c26d51121b8fa2b0af8f43468a5`  
		Last Modified: Thu, 17 Oct 2024 18:32:56 GMT  
		Size: 8.0 MB (8044509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c36a59a85b06e2bd52d2ec2cb341155d250d3f2be1f9ac26b04df0c11e87acd2`  
		Last Modified: Thu, 17 Oct 2024 18:32:57 GMT  
		Size: 908.7 KB (908668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fbcffbce846085f1aeb1ca37200c908e3fec136a9e13d47da767b24f4c52ef`  
		Last Modified: Thu, 17 Oct 2024 18:32:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d07a02586715b0161df3cbe44f34958fd39fb7cc20fd8d25dd384432c3e9a3b`  
		Last Modified: Thu, 17 Oct 2024 18:32:57 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe92ad9912528edcd2abb61a912dba9a30f3625e0fdc50838fb50ced1cbce06`  
		Last Modified: Thu, 17 Oct 2024 19:32:39 GMT  
		Size: 90.3 MB (90285422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5884965e3da55d2c1c2fa0e9b19af6f439f7e1b1c3c9c3a4d1869c0d465e16e`  
		Last Modified: Thu, 17 Oct 2024 19:32:37 GMT  
		Size: 9.8 KB (9783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b03d7eeae5848fde80d0719f76be7402b8af44fab0970fee5df0cb53853cadb`  
		Last Modified: Thu, 17 Oct 2024 19:32:37 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de04374c4b7577ddf384bba70443a62fe25dec831e2bc5fb06eedb1bd0560f9e`  
		Last Modified: Thu, 17 Oct 2024 19:32:37 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242c957c162508505cc07cbabe263d38fbca725c5be7302cde66f6b320f40e07`  
		Last Modified: Thu, 17 Oct 2024 19:32:38 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6512dc9b7f68a3b0c761442b4ed972f5a6c6b599b32ec002fa4b45e054af0df5`  
		Last Modified: Thu, 17 Oct 2024 19:32:38 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:2e23ad88e2cedf9f14e36aaf317dcef790742d6fe5d904eb021262639e9bb17e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5998144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da4a67600be4a5033b7c12a95baa1a95ebd2670ba6046edc293792b32ccb4ef`

```dockerfile
```

-	Layers:
	-	`sha256:575510ccba5e95c4fa9a00e054cfb4e44c396706206d89f3f98f27101ae734e1`  
		Last Modified: Thu, 17 Oct 2024 19:32:37 GMT  
		Size: 5.9 MB (5944084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f651e14b2f1c77cb970c0c20d4c36f1cae57d15ad244bfc9591b2961b808529a`  
		Last Modified: Thu, 17 Oct 2024 19:32:37 GMT  
		Size: 54.1 KB (54060 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:6e37faaa4b9575461bcab8654ca9c148723b54d65ec62abed967e581af113885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.3 MB (139337542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be82ce56f7baa9c9fa296f2cc39b2d5b756e939bd02ee40960d4d00ed541070`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:06:32 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_MAJOR=15
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_VERSION=15.8-1.pgdg110+1
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:06:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:06:32 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:06:32 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:06:32 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:06:32 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625705541eb2c232ec6868052605994a58fd1783ec6af4d33d62324beabdd4ce`  
		Last Modified: Tue, 12 Nov 2024 09:10:50 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86ef8349dcde0e9538a12f2b24d39955b32259d90fd9226e4b09e83a23c6eea`  
		Last Modified: Tue, 12 Nov 2024 09:10:51 GMT  
		Size: 4.3 MB (4312806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408ba174abce076b100b1775066ae161d8f3c617fc9f8c9c5f24d6d9452e4822`  
		Last Modified: Tue, 12 Nov 2024 09:10:51 GMT  
		Size: 1.4 MB (1404090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1823cb8ddc148ec3c8dec960e1f98604509d055e771c71cd86a89084c02d09`  
		Last Modified: Tue, 12 Nov 2024 09:10:51 GMT  
		Size: 8.0 MB (8044346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4ea35053fdfd2a5d6a7dbf5900c78c319262391884c26e2fcc89dddee4be76`  
		Last Modified: Tue, 12 Nov 2024 09:10:52 GMT  
		Size: 1.0 MB (1026586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37385ec28429364a4917c18b2047c5afbbf75d0d2d92d13edaa098af60ce190d`  
		Last Modified: Tue, 12 Nov 2024 09:10:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c022894a4b9e1da9147eceeaa4898b06811b419e7f3efb2aefdf946bb2f7d4`  
		Last Modified: Tue, 12 Nov 2024 09:10:52 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e66567440cee83759bcf64b0de0a837e463592924215d1b94fca10be3cc73a`  
		Last Modified: Tue, 12 Nov 2024 09:27:42 GMT  
		Size: 94.4 MB (94437501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a169f1b7a12a284d8151cf313e546fde93407edd7ddbb202ec1a2d7ef5cd4aa`  
		Last Modified: Tue, 12 Nov 2024 09:27:38 GMT  
		Size: 9.8 KB (9779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746ae34e030e4f590a9042b2dcde7bfdee4ac3e1300cc5473cde7bfd1a7f1163`  
		Last Modified: Tue, 12 Nov 2024 09:27:38 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b6aa0aa59d9192729d4741da80fe3e029d115d0c8b757ba422f0afbc3bb69b`  
		Last Modified: Tue, 12 Nov 2024 09:27:38 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425f9d9417346d109e2693077675daf45f55fd9fa82c4062ceac28bed5846c68`  
		Last Modified: Tue, 12 Nov 2024 09:27:39 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8732155a88d431127d0cd6cacdb5aee4192ede5dc3e55c1deb65c30b64de680`  
		Last Modified: Tue, 12 Nov 2024 09:27:39 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:558d93a112c1a3a8c5726fef044cb6e89c87651bbcc6b64e844aac8f50b87468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6012199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4431739a3a44106f624441c38aa04a7bc7ac7f190ebe3d49c48fcc091bcdaa8`

```dockerfile
```

-	Layers:
	-	`sha256:38c022fdbc03cac3860b3583ac18375ec85dcc2e52d0ff738aba3a8dac607360`  
		Last Modified: Tue, 12 Nov 2024 09:27:39 GMT  
		Size: 6.0 MB (5957974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44638584c9a374c850017a9eaf65ebf5ed2dbe9c54cb787f6991c378d19ca9b6`  
		Last Modified: Tue, 12 Nov 2024 09:27:38 GMT  
		Size: 54.2 KB (54225 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:7f0d58fad668ca0fb67ea5ee29bcb248da08cdbf942f893c75b4cbce8d9ed380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.6 MB (145583693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c45ec5f6e239778f8e42d0daf800a9c663793280bdfbc65536562d3dc6fe203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:06:32 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_MAJOR=15
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_VERSION=15.8-1.pgdg110+1
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:06:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:06:32 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:06:32 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:06:32 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:06:32 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2aea24d0416284c8bc498d91bac1c90e2bf12b01e7867f799161bbb874a8323b`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 32.4 MB (32423351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33652125531f30215bc43b3c8b5fd48ce8d9f9e6d1f15c07d0cfd3f21e124250`  
		Last Modified: Tue, 12 Nov 2024 02:44:26 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2106933fc66f312f46756aee2940108dbfba93d3ea216317449f9083004881`  
		Last Modified: Tue, 12 Nov 2024 02:44:26 GMT  
		Size: 4.7 MB (4719669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a92ef941be28bfd3f37823fee2c4310a39899d87a610d5a94c1fc6836a4bd0`  
		Last Modified: Tue, 12 Nov 2024 02:44:26 GMT  
		Size: 1.4 MB (1447769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609e405e2dc378599d90888ccc41e1b255a9bd50406d5f84947bd810f9fc9d78`  
		Last Modified: Tue, 12 Nov 2024 02:44:26 GMT  
		Size: 8.0 MB (8044420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccffcb09f40bbc2a44f4d1bc3d2114d8b46b462278eb03e37d7cfd57614a975a`  
		Last Modified: Tue, 12 Nov 2024 02:44:27 GMT  
		Size: 1.0 MB (1028926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835d1d3c5f374219b5611f7f05e74722d083aba5338983bcdead4d2d74ac8553`  
		Last Modified: Tue, 12 Nov 2024 02:44:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1081a09865f01f751e26f9f9bd4322e63d0c2515c307538351d722b4cfad6ac2`  
		Last Modified: Tue, 12 Nov 2024 02:44:27 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98fb2f77272132e0309e9e9249c8777743abe04c25ee17d490f6daafacf4442`  
		Last Modified: Tue, 12 Nov 2024 02:44:30 GMT  
		Size: 97.9 MB (97898938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3bb5730b0988e748a85805183f2d578de087e8a3c27292c90bb4e44d3d4772`  
		Last Modified: Tue, 12 Nov 2024 02:44:28 GMT  
		Size: 9.8 KB (9782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f270bc57962869cc346a00e446f87daacc2d7e700b8c54990d5d9a6ebe4a1669`  
		Last Modified: Tue, 12 Nov 2024 02:44:28 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1f8c86ff6a4fa0970df1229f4a5cfbcfe7f4b2d46003387ae869b2aec05bc5`  
		Last Modified: Tue, 12 Nov 2024 02:44:28 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89890d7bd250649d49fc324b9d641163e6be373f3e1e3ceefc552d522a48ff87`  
		Last Modified: Tue, 12 Nov 2024 02:44:28 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d51be629a1f7f5aed9a3c9b7dd4ea7659074ab810beba70c3032d56385971a`  
		Last Modified: Tue, 12 Nov 2024 02:44:28 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:633d45ba49de6bee2325b04f7e66e006ae2244d03a8cc7567857c59feb36eef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6014708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4084a91cf2c2dc5fb91f522073c7f0361ea98fb3a20777acc1a645f7e937548e`

```dockerfile
```

-	Layers:
	-	`sha256:33c0bcb91167ae4e0107fc8e3aa6b3424e86866c93b906425c6ad40492d03ad0`  
		Last Modified: Tue, 12 Nov 2024 02:44:26 GMT  
		Size: 6.0 MB (5960772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1f2e025190b18813226cc721ca5af16ce33d3eef411e12cd3e08e33edcf37cd`  
		Last Modified: Tue, 12 Nov 2024 02:44:26 GMT  
		Size: 53.9 KB (53936 bytes)  
		MIME: application/vnd.in-toto+json
