## `postgres:13-bookworm`

```console
$ docker pull postgres@sha256:83f55aab9d011d36d32d56fe8d79e07ac64d12b36dad1fd334a2f8998ad72b03
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

### `postgres:13-bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:0240941582a0cdb5b6d86752b35d01b8e2c0221f54d9ce1a3afae308ba96d711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (151039373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b80c9941d38a20d7a53ecb0de2b2b388cc0768f0d8b648206e844c91eabcf64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV GOSU_VERSION=1.17
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV LANG=en_US.utf8
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PG_MAJOR=13
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PG_VERSION=13.22-1.pgdg12+1
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 03 Sep 2025 21:48:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 03 Sep 2025 21:48:27 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 21:48:27 GMT
STOPSIGNAL SIGINT
# Wed, 03 Sep 2025 21:48:27 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 03 Sep 2025 21:48:27 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c2a9181cfd26ca0861a859aaa69920d58707f2a1ba3bc7e2876fdacca9cd09`  
		Last Modified: Fri, 05 Sep 2025 21:46:45 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7abb2a25e6843e69ecfae4493562c2794e0d6ec0e44d752af9def3e18cc858`  
		Last Modified: Fri, 05 Sep 2025 21:46:46 GMT  
		Size: 4.5 MB (4533725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11310a5e59d4dbe56802fddef9355d312fa470c40dbc1a12f44de1ffa603dd2f`  
		Last Modified: Fri, 05 Sep 2025 21:46:46 GMT  
		Size: 1.4 MB (1446762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d1f6f932a03208e5ef6ee4af9cad69d87fe9f60c8c4123e67d73bf6980c9a5`  
		Last Modified: Fri, 05 Sep 2025 21:46:45 GMT  
		Size: 8.1 MB (8066306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3149ecc6b61657a7e01900d205913e622696f79d24f0d3fd53d6e2e5bdc15a54`  
		Last Modified: Fri, 05 Sep 2025 21:46:45 GMT  
		Size: 1.2 MB (1196136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812f8629a6fe23067feeb54a98a609e673f5e7959c810c0daa374c03c47a0c6d`  
		Last Modified: Fri, 05 Sep 2025 21:46:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d796a572482446c2e649a921dcc91496916425c50b7cca36a3d85c8f035b4af5`  
		Last Modified: Fri, 05 Sep 2025 21:46:49 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7990097d076c08687baab75e755da98ddc1ee9fa1bfbafd91160448fe50780`  
		Last Modified: Fri, 05 Sep 2025 21:47:13 GMT  
		Size: 107.5 MB (107545995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a96417d319cf5e231dcba6488e303b356f037baacd567574d4628291cb753ad`  
		Last Modified: Fri, 05 Sep 2025 21:46:49 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded31e88e046928aed2ca7cae5c33de1cd89b8cb0fc26397aa3705073acd2491`  
		Last Modified: Fri, 05 Sep 2025 21:46:49 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b3536a1345437de2cc26e859d160f973ab6351feac1d6db1696e4716f09d2f`  
		Last Modified: Fri, 05 Sep 2025 21:46:48 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80264f78f2fffcf80a2db8f9bf5d2d391b3eda7603dee9ddb2096af773468d04`  
		Last Modified: Fri, 05 Sep 2025 21:46:49 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6aa55a7f171c9342c260677b9aae018f8a3d6e61f9a3d5081aaeeb58cb0b21d`  
		Last Modified: Fri, 05 Sep 2025 21:46:49 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:ffee5f250ea8acd7168490beadd380dd23d61ea5360d2c6e4e1edf6564fa1171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5886591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f0f489b7d2ef57ddc0c151dd9af4a67f70790a7f47bd5e91e2c2957f0192aa`

```dockerfile
```

-	Layers:
	-	`sha256:8cf459a733003a80fbc1085e4edc2e84cfea4931b8a91e6b572447a3bb7f902b`  
		Last Modified: Fri, 05 Sep 2025 23:07:50 GMT  
		Size: 5.8 MB (5832867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:173a6e45555a86a9c3bf3fb04e0fdabef704af4c3c29286c7aa4c559d0325951`  
		Last Modified: Fri, 05 Sep 2025 23:07:51 GMT  
		Size: 53.7 KB (53724 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:cb5e066bfdc98a3e10610fe9253070f5b22ddd4983e716fecee6bbeea607cdcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (144032461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741f1a95af80db463756cbd44932d8349f4009b1b73e700e62fb9b546ae68119`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1754870400'
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV GOSU_VERSION=1.17
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV LANG=en_US.utf8
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PG_MAJOR=13
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PG_VERSION=13.22-1.pgdg12+1
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 03 Sep 2025 21:48:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 03 Sep 2025 21:48:27 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 21:48:27 GMT
STOPSIGNAL SIGINT
# Wed, 03 Sep 2025 21:48:27 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 03 Sep 2025 21:48:27 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:53f325cb4b149fb7bd7e6ed7f8dfc1c5a37b5d828d75b4e6ba65a5cfd25aec56`  
		Last Modified: Tue, 12 Aug 2025 20:45:02 GMT  
		Size: 25.8 MB (25762718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3306dfe5c386f28dfab9ab71e1a8fa0de78396be1ef2adfa4d4065db83bc5060`  
		Last Modified: Fri, 05 Sep 2025 22:16:06 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa525e8b4f2cf15534b844046d0dd73179f9f33a7bd3367c543e7cacb494c0fb`  
		Last Modified: Fri, 05 Sep 2025 22:16:06 GMT  
		Size: 4.2 MB (4150951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93434aa37f2d1c13406d5f3a05c3e482b3e63c8eadf25660bf71a26831426d1`  
		Last Modified: Fri, 05 Sep 2025 22:16:06 GMT  
		Size: 1.4 MB (1424016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7419890a2e19155081294fb22ceec212562a708fcba8c51d2fa7ed4688ed86`  
		Last Modified: Fri, 05 Sep 2025 22:16:08 GMT  
		Size: 8.1 MB (8066376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8373ed973f8a30c798c2e2adab74f3c76a152e64a233abedffab6a70038b18cb`  
		Last Modified: Fri, 05 Sep 2025 22:16:07 GMT  
		Size: 1.2 MB (1194866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3080feb21f043220665da502b88d0e2ee00534fc4fc0f5358ae06b31706cc4`  
		Last Modified: Fri, 05 Sep 2025 22:16:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754005ef519a31f4bf87589ab46d3eaf9ab89da8115d2ca35359d13f272e4275`  
		Last Modified: Fri, 05 Sep 2025 22:16:06 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01638adbcc5eac5468781541a6f61c906d630497a403f548cde887e2c01086d`  
		Last Modified: Fri, 05 Sep 2025 23:56:45 GMT  
		Size: 103.4 MB (103413341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5961e4768237cd6de5dcb637a099d260fc29ea34a5269509378ce3451063b453`  
		Last Modified: Fri, 05 Sep 2025 22:16:08 GMT  
		Size: 9.4 KB (9356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625876369162d7e321a1600c93e7ffb0c821b3dc03838c90c731ca8c3f199515`  
		Last Modified: Fri, 05 Sep 2025 22:16:08 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9e452672518ee50b421caa4bfbde348168e2ce71d3487f5ef24348c759a3d2`  
		Last Modified: Fri, 05 Sep 2025 22:16:04 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17be094664a325ef08f323f5052bfd48f98ded03c1f5669c364a00b24ae75c42`  
		Last Modified: Fri, 05 Sep 2025 22:16:04 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6c949238ac851b9657e224573db3364ae0af458594b1805aa447691fc9558e`  
		Last Modified: Fri, 05 Sep 2025 22:16:04 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:eb8a4a61cfd114f321deca93fe193f561d0c6e5622848e359185e1eb3d658cf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5902627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5458ed5ee6428f6a74ffc35551a035d50b279eed6c4524503dbcdb993e077a07`

```dockerfile
```

-	Layers:
	-	`sha256:107574f1b640a2f329dc0b146e227f28e62cfae271ebff84ff5d9e03e2b75c3f`  
		Last Modified: Fri, 05 Sep 2025 23:07:57 GMT  
		Size: 5.8 MB (5848696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4903cf149dc8ae3b04c3fce08c9442291235492dd1c5a8670a8bccb6596b9e35`  
		Last Modified: Fri, 05 Sep 2025 23:07:58 GMT  
		Size: 53.9 KB (53931 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:f1f67b66047f51a65405448adf17db4fbf73e7ef02ac449776ebf5cdf83c56fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139130766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40649c503b9ffac3807a6dfec2e60480b9e471e4b513aca8ba440ed01ab4d318`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_MAJOR=13
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_VERSION=13.22-1.pgdg12+1
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:07:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:07:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:07:16 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:07:16 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:07:16 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a8db185805c54c045d888f7030794ebee970355b2336287cac0a0e22638ffc98`  
		Last Modified: Tue, 12 Aug 2025 20:46:38 GMT  
		Size: 23.9 MB (23938929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6820cfb123948a92acbf96b230a0cdea26476a1d3d429aebc35cc9fc764b4a6d`  
		Last Modified: Tue, 12 Aug 2025 22:38:54 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3b99820b8a61186a81204f61ee925a3f4266ace75a824b4ebff77980b261a8`  
		Last Modified: Tue, 12 Aug 2025 22:38:55 GMT  
		Size: 3.7 MB (3742574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fba3f5dbe870838e10b49748bc06c909eaeb5ce71d28f86afbb30fb50686f3d`  
		Last Modified: Tue, 12 Aug 2025 22:38:55 GMT  
		Size: 1.4 MB (1413752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0991df6523048151c47c162c5ac7ecfc88bf25eeb426a1400cf0194426f20313`  
		Last Modified: Tue, 12 Aug 2025 22:38:56 GMT  
		Size: 8.1 MB (8066369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201deac0b306fa58e8dd8ac5df3e46479efee68548ea761125fc205f19c46d4a`  
		Last Modified: Tue, 12 Aug 2025 22:38:55 GMT  
		Size: 1.1 MB (1067038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8763abcb4c6fe6a574c1314ae0ac66ef89c57408280beea34653c3d252f5ae54`  
		Last Modified: Tue, 12 Aug 2025 22:38:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c55d99fc111b0443e24a20c7eaa4578a66b6eb57754d56f6704f35122015a32`  
		Last Modified: Tue, 12 Aug 2025 22:38:56 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b35c52ef89df0012d699614126fd8a0884b3b431d5625d28e90a10c55370a46`  
		Last Modified: Fri, 15 Aug 2025 00:08:43 GMT  
		Size: 100.9 MB (100881915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db763935bca88ff7600074f02cde8f209148ad7a25f4153e93be2c21c0c79f6`  
		Last Modified: Thu, 14 Aug 2025 21:50:03 GMT  
		Size: 9.4 KB (9354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf68a2b589ecf9386c9571b78646752334a76fd751da527dcca4d15ca2ca990`  
		Last Modified: Thu, 14 Aug 2025 21:50:07 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5267fd12f56de406a1c94c2c54e69b726e75ca513b28e6916b7d4e2074baa7`  
		Last Modified: Thu, 14 Aug 2025 21:50:09 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcdc8e8bff7d528aab1a90b599be9ad2ad04c4be7c801dc24f4b3a93d904a9a3`  
		Last Modified: Thu, 14 Aug 2025 21:50:13 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9f9c99feb1114229573c0243102b691d0ed39b5c2cb3726131385ab3823264`  
		Last Modified: Thu, 14 Aug 2025 21:50:17 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:9afb706d5125ca1efd36f977932bdad2bf5fa00b200b6c6b90ca1efdeae12620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5901887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492e8e74a5170dcdb08c0100cf59efa04f98c205240f813eaeb1531b108a8213`

```dockerfile
```

-	Layers:
	-	`sha256:f2feaf56c69b6e6c897ba3e817d8606d81566e2de10d0f102263319703e27b2b`  
		Last Modified: Thu, 14 Aug 2025 23:08:41 GMT  
		Size: 5.8 MB (5847959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64e2b3964b926d04fb42dc249a218207b510ae2037ab7b411a94123543b6cc54`  
		Last Modified: Thu, 14 Aug 2025 23:08:42 GMT  
		Size: 53.9 KB (53928 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:68b7197a83dbd34cd3f88178cdb02391fb9b07ecf1ad0bf891c8efa17e457da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (148966521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b924b56c1d742d9e033f8b2dfdb11263d55721d0cdfe306bb15904bd277fb3ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_MAJOR=13
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_VERSION=13.22-1.pgdg12+1
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:07:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:07:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:07:16 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:07:16 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:07:16 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f22bf4a69c67725a5d28659467a9f4119ed414adf8a1d433e11ad80206e7a29`  
		Last Modified: Thu, 14 Aug 2025 18:51:34 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361ee65475462ea3e8ee78a207e0ee11b503288d0fc59ca7e79ac316ec6acc04`  
		Last Modified: Thu, 14 Aug 2025 18:51:36 GMT  
		Size: 4.5 MB (4499189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d686f5a8767e8f7119f4019c78e95b41922a788f6adf346700ad86916e3f0d47`  
		Last Modified: Thu, 14 Aug 2025 18:51:36 GMT  
		Size: 1.4 MB (1378836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c4da94471816abaff082b723798940778c0d6e9ba39ca35822ae23757628b1`  
		Last Modified: Thu, 14 Aug 2025 18:51:37 GMT  
		Size: 8.1 MB (8066342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dd948fe7b916f24497e0aa4ac3ea5f654f2ec18fecaf144b35e44757fcc0f5`  
		Last Modified: Thu, 14 Aug 2025 18:51:37 GMT  
		Size: 1.1 MB (1108732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9e7f843ae66f3ff0fb7f0e9b43b16750e2dff4f3d8bb23e783ba6c4e9faa04`  
		Last Modified: Thu, 14 Aug 2025 18:51:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb81ba96e939b60e2849bd3e78c77085a5b656b0da6722c19eec786712cb1a7`  
		Last Modified: Thu, 14 Aug 2025 18:51:37 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0158f6234fffb6707295513c80d52a6f8c799f7dcffd3ed258e5197166565c0`  
		Last Modified: Thu, 14 Aug 2025 19:28:58 GMT  
		Size: 105.8 MB (105811236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2bc6d34f26c0e908b8b2f483644025b19dea2bbdb8508b96daed8e62c2dd28`  
		Last Modified: Thu, 14 Aug 2025 19:28:52 GMT  
		Size: 9.3 KB (9348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c0ec8e3710fd666328018c85e55104535f51553ede9b2ea61fdb2cadde90fc`  
		Last Modified: Thu, 14 Aug 2025 19:28:51 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a65a913f3f237742a08782e6b3fd3302d19d278d7b3fa3367ef3a01e43abad1`  
		Last Modified: Thu, 14 Aug 2025 19:28:51 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca285e7fde03c7a5800d78689065fe099b722b1ed325d609a1d9e9137648289`  
		Last Modified: Thu, 14 Aug 2025 19:28:52 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b0818658fce878cf357b1121aeef931895edcb824649bb068dce85afef116b`  
		Last Modified: Thu, 14 Aug 2025 19:28:54 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:e43bd33ac0e5fb169ab30be30088e487791052b78efe50221fc5d95a16d57736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5893152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f233385df3c27838f99be49d7838d9e442fe902239fb3d6b916afd605b61cbd7`

```dockerfile
```

-	Layers:
	-	`sha256:94b1637c69e92ccd09927695a79711ca9fb6387ac5d8ea6de469d34af2569556`  
		Last Modified: Thu, 14 Aug 2025 20:13:52 GMT  
		Size: 5.8 MB (5839182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28607da3c5a1debad7c3d1bfdaa18c065ee2e7ae8e3370883541c9619778b7b8`  
		Last Modified: Thu, 14 Aug 2025 20:13:53 GMT  
		Size: 54.0 KB (53970 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:3cd091ea3780ddfd404d1d261292a340ef5a1ad660edd503fbf39bf5e5049f35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159753273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4745eea5d3e17ac8fd3d290e065508e671443318c5c24ca0be8b2833f8ebcd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV GOSU_VERSION=1.17
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV LANG=en_US.utf8
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PG_MAJOR=13
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PG_VERSION=13.22-1.pgdg12+1
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 03 Sep 2025 21:48:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 03 Sep 2025 21:48:27 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 21:48:27 GMT
STOPSIGNAL SIGINT
# Wed, 03 Sep 2025 21:48:27 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 03 Sep 2025 21:48:27 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:de83e1b86bff46f07bde3b82cca8622aed0b900dbeec110f1205a282d10bae64`  
		Last Modified: Tue, 12 Aug 2025 20:46:35 GMT  
		Size: 29.2 MB (29212605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f1352279344c6078b55aaeeda1957e9972504efec3666c541c6889fe23672f`  
		Last Modified: Fri, 05 Sep 2025 21:46:47 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026827fcde21b9d023bc28b3c1199a7fdd52e6f163dc445576a31d3f6fe28c9b`  
		Last Modified: Fri, 05 Sep 2025 21:58:07 GMT  
		Size: 5.0 MB (4965145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bddc182da77ce61a77145e80c0a54de78ede75a6e8e69f1cd328f84c18284d`  
		Last Modified: Fri, 05 Sep 2025 21:58:05 GMT  
		Size: 1.4 MB (1422299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9b61289641498cc146ac2b7254a8849e7a79041240eef16d6918d5e3ae9f43`  
		Last Modified: Fri, 05 Sep 2025 21:58:06 GMT  
		Size: 8.1 MB (8066302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b7388952c1b0672f7331891dfab811ee50ed3340ebedc23537c5865ced8814`  
		Last Modified: Fri, 05 Sep 2025 21:58:05 GMT  
		Size: 1.1 MB (1137178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2d1408ba2d75227f5fe2c1f292411e966868b5c38e5750d8359c7bc0bf1558`  
		Last Modified: Fri, 05 Sep 2025 21:58:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949ba365622f9ee3273518521a2c5478a6e1992b8526ecbe8877ee68ac4a4dd3`  
		Last Modified: Fri, 05 Sep 2025 21:58:05 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0175622422d358f6f1eb975f10b915cfac3667e116205ad56e928d34ed79ed7`  
		Last Modified: Fri, 05 Sep 2025 21:58:25 GMT  
		Size: 114.9 MB (114929548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb42a73d8ec093ec3e59a095c5eb54d730452119fc021de6f446731ba1d0382`  
		Last Modified: Fri, 05 Sep 2025 21:58:05 GMT  
		Size: 9.4 KB (9355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067957459b861db15dc23ed1defdb37d27317e75c0953e5baace214b4665f359`  
		Last Modified: Fri, 05 Sep 2025 21:58:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3071106cca7e7f12054403c6c533d58b953681ba485256faea9f88a65b423735`  
		Last Modified: Fri, 05 Sep 2025 21:58:05 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7829298f69ba776ef9aad04c48af4888833648ece8d6497b2c1d693c75788d6b`  
		Last Modified: Fri, 05 Sep 2025 21:58:05 GMT  
		Size: 5.9 KB (5930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e401d189933b1b2f84d3a22c5cbd7a38b4265c7f493e5b4da3ccd4a0deaef8`  
		Last Modified: Fri, 05 Sep 2025 21:58:05 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:367c8447a63dd757eaafaea327282692a807bd7c0f85f41a01dcb16e910274f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5900507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b40b3fdb8129c906c3d0fbe2b10f692c3059d96a273b7bbc3d4a1bf1c0faf36`

```dockerfile
```

-	Layers:
	-	`sha256:b3ad08de842c652bc730e3553f250f067b42f8d4b6b5b2866367ecbeca254a69`  
		Last Modified: Fri, 05 Sep 2025 23:08:11 GMT  
		Size: 5.8 MB (5846827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f244f0137b59053833a2527b79007643f5e938e8c71becc1251a2444b85cbb2b`  
		Last Modified: Fri, 05 Sep 2025 23:08:12 GMT  
		Size: 53.7 KB (53680 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:6cfcb982fccf14948c6b41e90f6f7fe3e5f9e6a1e471f5c89751bf0eb3385df2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.9 MB (149902970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20b4b0dfbe56e8deb23a3f28a55bdf391e422dd8bd5e7c92b7cc416af847ab67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1754870400'
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_MAJOR=13
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_VERSION=13.22-1.pgdg12+1
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:07:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:07:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:07:16 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:07:16 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:07:16 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:83bd2d8e15bdca1c657f4e1229c9515648aa638816bf4ae6a4be5a7afaee3a81`  
		Last Modified: Tue, 12 Aug 2025 20:45:57 GMT  
		Size: 28.5 MB (28516923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29312da7268b11c0e420282a3de73777dd60323a6115c94e4770a3967d1008dd`  
		Last Modified: Thu, 14 Aug 2025 19:34:18 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadf75f6a42f2ec57e669503e79a92f31752f394516ac3907e5fb7ad2261db38`  
		Last Modified: Thu, 14 Aug 2025 19:34:19 GMT  
		Size: 4.5 MB (4475161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edb5cc62fc658d056d649cb284f0a020e6a6c0b57162be2680462937f71ab57`  
		Last Modified: Thu, 14 Aug 2025 19:34:19 GMT  
		Size: 1.3 MB (1333909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474838f47aaa89f71355146b0a39b988275244759ef97d0cf6e616a991c9027f`  
		Last Modified: Thu, 14 Aug 2025 19:34:19 GMT  
		Size: 8.1 MB (8066502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148e17ad67a5ccc4d969ff6abab8130942de3726b9e6fad6051c12601f1f8343`  
		Last Modified: Thu, 14 Aug 2025 19:34:19 GMT  
		Size: 1.2 MB (1182641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31de7c74bad6aba9b4e3ba53d1a4cfc29234f0d874650d8b3ecb0e3678aa8c07`  
		Last Modified: Thu, 14 Aug 2025 19:34:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5cba190353263630bff7d7d1f8db3bf41c59f3df3ef093a60839ff9e4950b3`  
		Last Modified: Thu, 14 Aug 2025 19:34:21 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb0aec2a4388cb86a7aa8cd7db3ff625777621a54e8b44cc1e5a436fa8a01485`  
		Last Modified: Fri, 15 Aug 2025 01:13:47 GMT  
		Size: 106.3 MB (106307637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e856142037866c69411bb4d28d997e37fb95ccc0e0560357bdba67f8b754571f`  
		Last Modified: Fri, 15 Aug 2025 01:13:42 GMT  
		Size: 9.4 KB (9358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398486ed3166f90115e976092fd18f6e8b53041a987d7ce786b7bcc491a06c4f`  
		Last Modified: Fri, 15 Aug 2025 01:13:43 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bf58e07e26208c6563d006a93446099735c7f31d1d732deb1a280560f22a70`  
		Last Modified: Fri, 15 Aug 2025 01:13:44 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d4588bb4b2ad2d8b7c6c479b673732bbe064cd04deebc533bf528e2f9fdb00`  
		Last Modified: Fri, 15 Aug 2025 01:13:44 GMT  
		Size: 5.9 KB (5930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3af39b730dde9c18031ff34f20bad381ed9fbcaea6379ceff5c3febcbb810ba`  
		Last Modified: Fri, 15 Aug 2025 01:13:45 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:648dcc405c3f32f1fc16584ce256f4d287363032bb70ae4ab4514130bc8fd2f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 KB (53591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a7c8c08247174d069c051aea73d2b40e955a1b3a39341425fbca9a24fd9175`

```dockerfile
```

-	Layers:
	-	`sha256:6e3a4169779c7a4be71e28e5aba780224232c244fb1f7c70569d23a6c9f711f3`  
		Last Modified: Fri, 15 Aug 2025 02:08:00 GMT  
		Size: 53.6 KB (53591 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:f9052c2eca47b2abe901409de97b66d5a62fbd1660fa2a957b8f915ae29a4d97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.6 MB (163551471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f8096062c113f1507d74b7d472b0b581a7efe0c340629c384a20925c26ff48`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_MAJOR=13
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_VERSION=13.22-1.pgdg12+1
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:07:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:07:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:07:16 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:07:16 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:07:16 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e71427bc966f27e4c045f76677200cc1cb8d57b75ba0d7ab977498c00e8d6a4`  
		Last Modified: Wed, 13 Aug 2025 11:23:54 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c88c8558d33d220ba0bd06a9aaa623bae8d2dc5226d907b7bea0495002b0d32`  
		Last Modified: Wed, 13 Aug 2025 15:35:10 GMT  
		Size: 5.4 MB (5368151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4541684e1bb8d6caaca0ac9f5d0cf566b2ef5226a534bd35fb5967ecbf66d244`  
		Last Modified: Wed, 13 Aug 2025 11:23:59 GMT  
		Size: 1.4 MB (1368729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f3c9c3e96a7afe0384ff2776211efbadf170ac27ffbd881765dd2568bbe5de`  
		Last Modified: Wed, 13 Aug 2025 15:35:11 GMT  
		Size: 8.1 MB (8066366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5ac7820ef53cc6fce6e86c3e89e9180a62df051f52f4f05f567ba757da2dd9`  
		Last Modified: Wed, 13 Aug 2025 11:24:05 GMT  
		Size: 1.3 MB (1283505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b039814790880fa88c0fe02fdcfc7406c540d2eeccdf1c8012cf811171ba3348`  
		Last Modified: Wed, 13 Aug 2025 12:12:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f05bb5a6b03e6da586b1e62ffbc88e07fc494b048054316cdb970e7f6adacb5`  
		Last Modified: Wed, 13 Aug 2025 11:24:14 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436883554db3569d05edd54eb9030bbad2e12ab5bd1f83cc9359b6ea667362e8`  
		Last Modified: Thu, 14 Aug 2025 19:59:51 GMT  
		Size: 115.4 MB (115371107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df2bb0e0d107af24613509b0cc55d8b573f97877a62a37c58865124ce6d91d5`  
		Last Modified: Thu, 14 Aug 2025 19:59:31 GMT  
		Size: 9.4 KB (9353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc258d3af1f29ddb828944b546457c7e084b489447659bfdb68561eee9419853`  
		Last Modified: Thu, 14 Aug 2025 19:59:31 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088e86414445b9f08c43742eb21601119af9d46b833d683229950d16aaf07e4f`  
		Last Modified: Thu, 14 Aug 2025 19:59:31 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac07ec876c67904f744c0abba1b2810f34fabfa5c5c26b3d0221dc43a19de66`  
		Last Modified: Thu, 14 Aug 2025 19:59:33 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8437915814041be150eab6c0189fcf511ac6fa652bde865500a3f22446a45a`  
		Last Modified: Thu, 14 Aug 2025 19:59:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:aec97dee1171a66164663a3a758e109948f726ba7c7cbc9768635c2dcadeb8a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5894026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2a84c72ea8efa8b3c4a959366d0f70a3644a00c8311d7ec12aeccf1da95934`

```dockerfile
```

-	Layers:
	-	`sha256:8e7cf19f1137583000087284d0c058b0eceea7d06c6815aa3c676cfbc6e68ab2`  
		Last Modified: Thu, 14 Aug 2025 20:08:47 GMT  
		Size: 5.8 MB (5840248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c31cf10714e7e64c42a7826325a40507c33fc4024e14dd8f6aa732debc19e975`  
		Last Modified: Thu, 14 Aug 2025 20:08:48 GMT  
		Size: 53.8 KB (53778 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:7cc832a72e1a98dd807f4f1722e7d897456a52347000d9eb54cd9e20978787d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160174922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f317f4a586082cf37a4b4cfe7679c1ae116a2d098b98d8d0b5ae96b261ff761e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_MAJOR=13
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_VERSION=13.22-1.pgdg12+1
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:07:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:07:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:07:16 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:07:16 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:07:16 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6c30648f10140423dedad94d980ec43d531a9cad0983059ff739bb9b52a33f`  
		Last Modified: Wed, 13 Aug 2025 11:43:34 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694ac9590e0ed955da24f366c054364cf8ba0c10685c2a11926f9130d96dd2ef`  
		Last Modified: Wed, 13 Aug 2025 11:43:34 GMT  
		Size: 4.4 MB (4391026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610383596c1fcdd9ad52eec420a313e89a0b3b8e9b9eec4a9c97875fa3199e0d`  
		Last Modified: Wed, 13 Aug 2025 11:43:34 GMT  
		Size: 1.4 MB (1412789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968418c0a002c3f87fa669b14de23f59d9a339200e3b6e12866ab5eaefe04843`  
		Last Modified: Wed, 13 Aug 2025 11:43:34 GMT  
		Size: 8.1 MB (8120490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c87bf03e6298d0eda03dad7a991ef95e36418ce316b1cab732a6c5aaf20b9c`  
		Last Modified: Wed, 13 Aug 2025 11:43:35 GMT  
		Size: 1.1 MB (1096806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e80fccf7e254e617a490a5e480bf0a7d998d006d09d137c184187e9db82e9c`  
		Last Modified: Wed, 13 Aug 2025 11:43:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0382bed70396ec99ad734fded83f746496510f544ac4570bbc14cf5ca09f924`  
		Last Modified: Wed, 13 Aug 2025 11:43:34 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4f072bcdcc0dd4b504bdb22873b29f8a09661a9a03fcec5251c7601b6e266e`  
		Last Modified: Thu, 14 Aug 2025 23:04:27 GMT  
		Size: 118.2 MB (118245790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ccb46a7221fcc30887893a54eb22059849a37ade495ea9143a8b3e8a19207ab`  
		Last Modified: Thu, 14 Aug 2025 23:04:17 GMT  
		Size: 9.4 KB (9354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba3ca78698647fae9a750e5dea322913dfc9953e09135303ce10adfe5ad880b`  
		Last Modified: Thu, 14 Aug 2025 23:04:17 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4926c0ab342c8404a7eb97768b0d9cd0877e2e93e81318fa252108343c18e3c3`  
		Last Modified: Thu, 14 Aug 2025 23:04:17 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0523e66eca57f201829d40ef166ad0c09b074105dd6ab0c00f410ed5226c6c0`  
		Last Modified: Thu, 14 Aug 2025 23:04:17 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e01fc7fba9b9bdf38d710964b2c8d29f86615b29a307b375b75a98f3c4d1d32`  
		Last Modified: Thu, 14 Aug 2025 23:04:17 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:d775df5c85c6d90cb0fb84044c6912fa44016025859c75eeff5d78c8dc4c333c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5897030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d13f62d11f66ddd2bc88e5e5f0c3e01f3511c047e06812118643d1163bd7e01`

```dockerfile
```

-	Layers:
	-	`sha256:6a352de924df3278c0d93921ee670f35ee809f6e05ddc02e327319e30fbc1c7e`  
		Last Modified: Thu, 14 Aug 2025 23:08:59 GMT  
		Size: 5.8 MB (5843307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbb5c8cf3229031aaf41c220852cf6fad4ce4be2c66598a94705bab8288d5197`  
		Last Modified: Thu, 14 Aug 2025 23:09:00 GMT  
		Size: 53.7 KB (53723 bytes)  
		MIME: application/vnd.in-toto+json
