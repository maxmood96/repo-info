## `postgres:14-bookworm`

```console
$ docker pull postgres@sha256:922d38d4ca73ba5bfa8140c50b0d1f45636ca7b4c20d90506c49e2be2d7911f5
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

### `postgres:14-bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:84d9c9651db9257160a8481e0604ec3fdc2318144be03d47f176edd6e0e63101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149382445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:365d502a72f32b9efc921dd7e5505362eef1f8e5aabfc1e3aba5e6889c49be5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 21 Nov 2024 20:09:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_MAJOR=14
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_VERSION=14.15-1.pgdg120+1
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:09:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:09:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:09:59 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:09:59 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:09:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c60893f59212a5e317c17fe1ef28c9ebb21b39ef2c3ae6a5966ab6fe47690c3`  
		Last Modified: Tue, 24 Dec 2024 22:15:17 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4681af49637eb39e1ef4378cb67aea767c2e6988504fb9df776faed71948e8`  
		Last Modified: Tue, 24 Dec 2024 22:15:17 GMT  
		Size: 4.5 MB (4533724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e485590999bad07a438054de210bd33b02821a2a4dd9a68108b6b4acae13ccd1`  
		Last Modified: Tue, 24 Dec 2024 22:15:17 GMT  
		Size: 1.4 MB (1446700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b594df41d23095af9876e7ef659a9c63fe08998166b56af34c3fd492cfdfd8`  
		Last Modified: Tue, 24 Dec 2024 22:15:17 GMT  
		Size: 8.1 MB (8066282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d304bad922997f167b8c839703708e015b258615d0c51c40583460f33b925d`  
		Last Modified: Tue, 24 Dec 2024 22:15:18 GMT  
		Size: 1.2 MB (1196080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ac8a7085778077f673bfe33cb857de3d2b4ac4695451c3c9db03c81f33a573`  
		Last Modified: Tue, 24 Dec 2024 22:15:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41295faaba7e672cf38c6ae30da2b7ef8774b727eba648e15b7dd0683ee6f2c`  
		Last Modified: Tue, 24 Dec 2024 22:15:18 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8bc7b60a38b33398c1583aff55043bd89422dc6efc818ab699a25ff0612a20f`  
		Last Modified: Tue, 24 Dec 2024 22:15:21 GMT  
		Size: 105.9 MB (105888237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69d252b29f7ba5ee882cc66345efa203cb4505b483b1ece6dee9ce7440ee9bb`  
		Last Modified: Tue, 24 Dec 2024 22:15:18 GMT  
		Size: 9.5 KB (9521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6fb314ec7e27b37711a5d69481cbb6fcbd1bf37610ff9431ce13dfc7df10bf8`  
		Last Modified: Tue, 24 Dec 2024 22:15:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216ec0214ff76445207e2093c88d57f008c51df2c29062f31759789ca7b969bd`  
		Last Modified: Tue, 24 Dec 2024 22:15:19 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d9289c27dc4bb754b588e8357d1b1a1fa5650261eab308ba4e142020e57fdba`  
		Last Modified: Tue, 24 Dec 2024 22:15:19 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6b1c025a5309a7d285572616401603871d323e6957d2123b343d6e90915469`  
		Last Modified: Tue, 24 Dec 2024 22:15:18 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:47cc85be63b632b53138ebc5fb4ac7fc25f4dc15203c8ab017d5e16c0fa4fb0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5710055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a00078b28bef6488596717791270ce88492c9e398470d44fd6dde97209be5400`

```dockerfile
```

-	Layers:
	-	`sha256:7f0478060b7be650edd20d50165f6d619f3599beb30bddc965f84ad40a4ed2c0`  
		Last Modified: Tue, 24 Dec 2024 22:15:17 GMT  
		Size: 5.7 MB (5655468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29cc2ecf7ec3e9be84aa441617368eb69fee257586f86184b15a9d5821f4c92c`  
		Last Modified: Tue, 24 Dec 2024 22:15:16 GMT  
		Size: 54.6 KB (54587 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:ffa6387c019a73a3e7edb9223c21b807f6ca33422ffa4a2b7c83874fdcc88907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141813384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca58df4c530a25c0446a4f9c6e8517c52e42e031cae7fd28f1c93f07ff9bd4e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 21 Nov 2024 20:09:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_MAJOR=14
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_VERSION=14.15-1.pgdg120+1
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:09:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:09:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:09:59 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:09:59 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:09:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:61230a432de02dc9fd57340d88179517d7f651caeb2a5e2fa6ec333d17ed65c5`  
		Last Modified: Tue, 24 Dec 2024 21:33:31 GMT  
		Size: 25.8 MB (25754907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c5c0f46e89699c50a8c0263d7e160dcc451a4f5a34817a19958bb11979bb47`  
		Last Modified: Wed, 25 Dec 2024 00:07:51 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5504e2bc18f3361b80074f5f24c78d533c83a99fc773632fcedc730b9cb46da9`  
		Last Modified: Wed, 25 Dec 2024 00:07:52 GMT  
		Size: 4.2 MB (4150922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41a08084d12214d26eaa8b5b9ecbec81800eb6334aed59c7fc65c65899104c6`  
		Last Modified: Wed, 25 Dec 2024 00:07:52 GMT  
		Size: 1.4 MB (1423850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb417ea830e889f93b0815a795c22be876d8d72f9099b6a2ed202c7f27531435`  
		Last Modified: Wed, 25 Dec 2024 00:07:52 GMT  
		Size: 8.1 MB (8066381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26b3663607f6d33c5a76174f7e3739874f31f218ad483bd52e11fbf1d7eaf6b`  
		Last Modified: Wed, 25 Dec 2024 00:07:53 GMT  
		Size: 1.2 MB (1194848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b8dc0048a6a8f13afa56d4c00070204f53f8882e7fcf122d351d6c0bd0f014`  
		Last Modified: Wed, 25 Dec 2024 00:07:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7355d6e11722e7cb2886865cd1e2e4ea9f81e34af2e107c80d04bc26a0ffb2b4`  
		Last Modified: Wed, 25 Dec 2024 00:07:53 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53af0d27eae80ed9598f869d6a8fc942d52107132e1296d7013584d558e4480`  
		Last Modified: Wed, 25 Dec 2024 00:55:14 GMT  
		Size: 101.2 MB (101202628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9369e94fa66bf05136dab5680e7998f3f407c2e81e2cda6be56c4b59f8ed5b84`  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd07ffd793cf5c4d817409e332d74f821c30149f5e8efbe63017ecede7122588`  
		Last Modified: Wed, 25 Dec 2024 00:55:11 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ad5ea27f1a1f395dbc85ebe27e704ebddf8de082b9f0780b55028ad344f7f1`  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0749fe798a47997ccbadc3cbd9639bd1ab9e0492c8fed589aa311c2082bfb2d`  
		Last Modified: Wed, 25 Dec 2024 00:55:12 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f2447a511428c3d3e5b440a51ba4796a2bc786dbb66ece00e6ebdacc792a3f`  
		Last Modified: Wed, 25 Dec 2024 00:55:12 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:29393d1d0de24dc5b179cef35c532545bc5cce9244e5405c212d705bcc7b06bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5723930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4c334f326bf521ed2f2e654a80c0d16b0c643499c148840f15bcf1058feb96`

```dockerfile
```

-	Layers:
	-	`sha256:2a186771df2f6c6876b30ed6743bbf733381bed2fa870bc9205fc3abb8916048`  
		Last Modified: Wed, 25 Dec 2024 00:55:11 GMT  
		Size: 5.7 MB (5669125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32ad0806001955f35507d73eccc0ecab791d3d6607effae400bdba7b4feb5b1b`  
		Last Modified: Wed, 25 Dec 2024 00:55:11 GMT  
		Size: 54.8 KB (54805 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:0e1fe6280221b620720cd1086a684ecc3c4fd452a69ede247b6606a13991f4c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136931622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2577bd523c7a830f837d4dafd77d7c7702bfe0ff4e7a589945ac6dc8406ed022`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 21 Nov 2024 20:09:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_MAJOR=14
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_VERSION=14.15-1.pgdg120+1
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:09:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:09:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:09:59 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:09:59 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:09:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:24f0da30a772db626789cda3e7b0911098d07574c40b30be943d43dec3ed685f`  
		Last Modified: Tue, 24 Dec 2024 21:33:51 GMT  
		Size: 23.9 MB (23933522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd104fc2aacfa50f0194aa93433975e3190d3e3f2d97d7c926e2b7475cfc4626`  
		Last Modified: Wed, 25 Dec 2024 00:46:58 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae52e17ad9a1a2db29f3f2c0c7c52671d807d2493a271e2502c69beaf602bb5`  
		Last Modified: Wed, 25 Dec 2024 00:46:59 GMT  
		Size: 3.7 MB (3742518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018493c358882b218cf4394ceaada5391f5195b9b3e4a35efd57466b6306e077`  
		Last Modified: Wed, 25 Dec 2024 00:46:59 GMT  
		Size: 1.4 MB (1413589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53077cb81df8a07a34ef0fc07a36ba29177ce933a1b2bfc6bf5ad13625c11de`  
		Last Modified: Wed, 25 Dec 2024 00:46:59 GMT  
		Size: 8.1 MB (8066259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35f33c297598762eeb1c2deb164cb0135b8559e7f43ac864ded8d6d6d2ab554`  
		Last Modified: Wed, 25 Dec 2024 00:46:59 GMT  
		Size: 1.1 MB (1066927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e4b8f5cc50c61e1034f7fd53bd4e35b9cde0692ff15b4950db484c8022adfb`  
		Last Modified: Wed, 25 Dec 2024 00:47:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aadd86baf84503a94e9bef9de85b734d8f7fe9baf0f5cd5671ef13845306966`  
		Last Modified: Wed, 25 Dec 2024 00:47:00 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4da6744765f9d2332bd5b308516296aabbf1317de2fe51013ed12a206a8ca59`  
		Size: 98.7 MB (98688963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c9c3807f18e3ec79d18df54858595fb3cbba6468f24e2712e1ad674651371f`  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb65530b13c39f865033bb386b595ba576782293255d071760f2d61138a7424`  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19850a8fb81dfc9de335228da7b90a003c0c5a1d8b9945ecd5c778047e4757bf`  
		Last Modified: Wed, 25 Dec 2024 02:15:38 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48bc8cb5488a2a40f09daae9d3934c9594b640207fecce9849d82d3897bb54d`  
		Last Modified: Wed, 25 Dec 2024 02:15:39 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72c5ac7b7056bc98c7b6b18b8fe25e95337ac45d73fffabc06dca7cca89d1ed`  
		Last Modified: Wed, 25 Dec 2024 02:15:39 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:3afbd42b0511f982da50c3a83318a82b166e024f275d178385402c5eaea70c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5723496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b3ee457f7f376b5ba0c89c69c9f00994a2cd65fc499a849790e7617a700d99`

```dockerfile
```

-	Layers:
	-	`sha256:7240456ca24a31be5b6216453c1b36de89660229354f0ce5235d2cfb7a49df86`  
		Last Modified: Wed, 25 Dec 2024 02:15:39 GMT  
		Size: 5.7 MB (5668696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82d2cb2e22a5228b1ae1b5e273beb0b860df1a688014aa164b9e8dd88968002b`  
		Last Modified: Wed, 25 Dec 2024 02:15:38 GMT  
		Size: 54.8 KB (54800 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:8cff0a408038772ef4575bb62fe777550cc7a8f1fd6010cdadc969c2493b7677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147402700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d2203ae5b47e83fe359bfd83702a5a0d739f237c2a7adee9f4a11330020d4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 21 Nov 2024 20:09:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_MAJOR=14
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_VERSION=14.15-1.pgdg120+1
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:09:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:09:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:09:59 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:09:59 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:09:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7479e21cda8af743d9d2726c4a5c92ecd79e7e3671f523bb00fa5632d108852`  
		Last Modified: Wed, 25 Dec 2024 01:01:07 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d05a1bcf69dc7b9507425bd5cdc6e8c1b67a5f76fd68bff224a61c0beb6a171`  
		Last Modified: Wed, 25 Dec 2024 01:01:08 GMT  
		Size: 4.5 MB (4499149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0028a78bc010e5435a0368b2221b3cc3e8e1f4426385ffd9ea5714c605a656`  
		Size: 1.4 MB (1378702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0ac4464edafe1d07e4c329a906389b769e1630a2db11a2cedd497fd3d5014d`  
		Last Modified: Wed, 25 Dec 2024 01:01:08 GMT  
		Size: 8.1 MB (8066309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcbbeda8df80166bc797457987dcb269a18c50689cca71a2cf044679d7396f2a`  
		Last Modified: Wed, 25 Dec 2024 01:01:09 GMT  
		Size: 1.1 MB (1108704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcccab3bbc5976c348a3475fb58276a34223ba8b4b1987e417ac52229207baf8`  
		Last Modified: Wed, 25 Dec 2024 01:01:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce387b6af688611f7812c0cd5b27134354be9d9b3776e2acbe18266a459d5bbb`  
		Last Modified: Wed, 25 Dec 2024 01:01:09 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a02b225a75a733fcaff33adb4c987bd7db9e771d06d151119a6c7fa875bff2a`  
		Last Modified: Wed, 25 Dec 2024 01:06:44 GMT  
		Size: 104.3 MB (104271266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea84261f61d8dca2eca25fde07275e42d707376667c22715e2adb93e533ff4d`  
		Last Modified: Wed, 25 Dec 2024 01:06:41 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4020f7952e8c9437d414f57c73979b1a8119fecb6c92c38bf7825beba6ebceb`  
		Last Modified: Wed, 25 Dec 2024 01:06:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce3b0675d9b0212d29278a33f6ee30acf051e48515efeda3460440449dc308c`  
		Last Modified: Wed, 25 Dec 2024 01:06:41 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595a080e06b33b75cac320fb58581942cac3e27eb747e0e8d1beadd4413f17fe`  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225c0462b7865c45d135d6a6ff656547d0c881dac030dae19d782806ed35374c`  
		Last Modified: Wed, 25 Dec 2024 01:06:42 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:11bc1cdc4706a6e0cb403e744531ea401824d97aabd0b18b24bd9f335cf01159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5716663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9581462aaa4dbc86c78e3f9120b77887e457aa0e45529d23ab64167f909e55d2`

```dockerfile
```

-	Layers:
	-	`sha256:92740187f050e97927ea5e9a59bd59cc7fd1f61c49b8a9295fc25107aeda78d0`  
		Last Modified: Wed, 25 Dec 2024 01:06:41 GMT  
		Size: 5.7 MB (5661807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a05f6997f38901e44e587aeee425f72f84ac094361ab718e0fb722febfcb8177`  
		Last Modified: Wed, 25 Dec 2024 01:06:41 GMT  
		Size: 54.9 KB (54856 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:0178f6f14ee88cabcc192e4fb8a832988d1f8abbf61fd80d0e996a3e8c418415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.4 MB (157355849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b56bff18abbd7cbe7f9e66a9f67a618a22c62ec2812ae09581ff7376b54dad6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 21 Nov 2024 20:09:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_MAJOR=14
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_VERSION=14.15-1.pgdg120+1
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:09:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:09:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:09:59 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:09:59 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:09:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2299cdab8229629633b1bdb488c3fc7be76db0fb83c2d1bf175f2c9018ab659b`  
		Last Modified: Tue, 24 Dec 2024 22:37:51 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bec1f9ab258b1197c871f3e8660bde1ba3cfd150d9cb56af6a804ad99720317`  
		Last Modified: Tue, 24 Dec 2024 22:37:52 GMT  
		Size: 5.0 MB (4965088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61602055b77c0b372ec5e89b8f8eae0e6dc19b9dd476ec0636ffbfaab41ecafc`  
		Size: 1.4 MB (1422147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b6e00d9f49b3034c15506594026db9aee76cfe2bc3d6c249211f45e63bf18d`  
		Last Modified: Tue, 24 Dec 2024 22:37:52 GMT  
		Size: 8.1 MB (8066311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551a3a6607dc34d92df7e49407c3c7281f6be57ad8b69bd3f3dd3bfe8e70ffc8`  
		Last Modified: Tue, 24 Dec 2024 22:37:52 GMT  
		Size: 1.1 MB (1137187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3349ebfc3bc83990c00bf8392a49ab64b9d986ca4eb4900489e3129dcbfd5ece`  
		Last Modified: Tue, 24 Dec 2024 22:37:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcfbca427456a00a72edc20b97b731fbd3d3db0b7a59a3d009913fa95f7cb216`  
		Last Modified: Tue, 24 Dec 2024 22:37:52 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a35d53e6a850d78b5b57e7d5e54a1402d3c4c1f86df2b85da2daf96d7d4ac24`  
		Last Modified: Tue, 24 Dec 2024 22:37:55 GMT  
		Size: 112.5 MB (112539879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0ff97f671d5e29478d51cc3663aaf87225ed9a0e8fb4f773cec7197061771d`  
		Last Modified: Tue, 24 Dec 2024 22:37:53 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7b1cc02210d6cdbe473265502deb851990591fda3600dc681a84da738b0445`  
		Last Modified: Tue, 24 Dec 2024 22:37:53 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80365432da96c41d75e4cce9e05e2570821257783a430077c286bd13994c6c26`  
		Last Modified: Tue, 24 Dec 2024 22:37:54 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aae3b0e74e0ef6811cdd34083b2a43345997a1608ae130be6d179f41241db00`  
		Last Modified: Tue, 24 Dec 2024 22:37:54 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffd052bc40a04e17f78775c96eb66f84a75bef7c48459063365b9900e66b5cf`  
		Last Modified: Tue, 24 Dec 2024 22:37:54 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:d20a6847f814bec6ac581e70644fd124cf7470b12def87fd75cadfb2cde27ad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5721696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb26e4f1e8752d8663b1709c1444a6499a4e906b98a055b01cf916d12740cd93`

```dockerfile
```

-	Layers:
	-	`sha256:07c66516b2b78c85a96b25dd7116b6edbda935ae308f850d3332d51e98961a71`  
		Size: 5.7 MB (5667163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e286b2c82ec9c71a680ca47efb7b7276d755b695691ef6a9f0cb6ddd7b7f9af4`  
		Last Modified: Tue, 24 Dec 2024 22:37:51 GMT  
		Size: 54.5 KB (54533 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:463542a070350885becf577aee5d1a3beb9f1f3e24c0c1b4374ccc66625c97c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.0 MB (145009355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48b5b4beb4189921e3ce75336710e6c8bb366392e220a0b2502ead8d1a0e1bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 21 Nov 2024 20:09:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1734912000'
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_MAJOR=14
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_VERSION=14.15-1.pgdg120+1
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:09:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:09:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:09:59 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:09:59 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:09:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8a9f899eb883b68bbb36209214842bc927b7c446aa0471f0b241ae7e76adb6e5`  
		Last Modified: Tue, 24 Dec 2024 21:33:38 GMT  
		Size: 28.5 MB (28505873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b9aed14ea6497e89eca3f0b46e593b2585ff9dd073d4b510a8c309ec0fd7b6d`  
		Last Modified: Wed, 25 Dec 2024 05:51:32 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:574779c9d077eb165da84341e8e8bd6c3e20848272fb554711af34fc149e689a`  
		Last Modified: Wed, 25 Dec 2024 05:51:32 GMT  
		Size: 4.5 MB (4475063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb93f8adb2151e7e9e2f281000d9919f517e649aa851f9d88690e4305a184f7`  
		Last Modified: Wed, 25 Dec 2024 05:51:32 GMT  
		Size: 1.3 MB (1333773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b21492879c0e67a1962882adac73c788f2dc5fc91ed3e4d8f7a8fdf4232aa58f`  
		Last Modified: Wed, 25 Dec 2024 05:51:33 GMT  
		Size: 8.1 MB (8066451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d087582d9ef3edd14e44f58ef28a724ae1ce2371b304062c2a36955b5eec52`  
		Size: 1.2 MB (1182605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ea7f1f78158aa37e1f8729c0b0d528087a69b4ee506eebb898118325530c14`  
		Last Modified: Wed, 25 Dec 2024 05:51:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f73b441dfd2157a39fab60e01bf46aa1da8f7095d7b3d37f196874ff7a5d2b`  
		Last Modified: Wed, 25 Dec 2024 05:51:33 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc45fbbcb3b4fabc98bc0012ed717be76ef7159bdf0fc828c291f4b50c0301d`  
		Last Modified: Wed, 25 Dec 2024 09:13:14 GMT  
		Size: 101.4 MB (101425739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea54ecdf480f26b6071e1f75199285eea3655fec53868550fb62af161afe6d6`  
		Last Modified: Wed, 25 Dec 2024 09:13:04 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94eebeb09ee9992bc074d17ca8af4e372955c60ddf0d72e8ce251632d63d6933`  
		Last Modified: Wed, 25 Dec 2024 09:13:04 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e816b181b67fe7733c093c9fa0be76c5ac242f8c947daffdd135a1269573e7df`  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f973c2bf0b188c027179791075c2b210b5270ff34550055f833648a1882ff4`  
		Last Modified: Wed, 25 Dec 2024 09:13:05 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6a530e80ec1ceb84bcc3f477495a5728faeba78bbfe147978f886d9fdbd781`  
		Last Modified: Wed, 25 Dec 2024 09:13:05 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:47eda9d72e92759813c7236913cb37f2b0db3f18a8e93dae4995a922a1df8133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 KB (54471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d874ac0c58b9ba3cbc9bb21b4f12904f13bd6864c2eb1a2aca857250e4c026a`

```dockerfile
```

-	Layers:
	-	`sha256:dcdc7c065f5f3a2f5a3ec1f3630bfc6aa7e3951eb12f2fb383089e9bb1c6aebf`  
		Last Modified: Wed, 25 Dec 2024 09:13:04 GMT  
		Size: 54.5 KB (54471 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:17cb765203af576775fc8b712d60266e9aa02fcd37cef048b355698c534ad8d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.4 MB (161351623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9640cf1b63abdc1c326451556635cf4d73ce143be880872a133d086167280bd5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 21 Nov 2024 20:09:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_MAJOR=14
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_VERSION=14.15-1.pgdg120+1
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:09:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:09:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:09:59 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:09:59 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:09:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Last Modified: Wed, 25 Dec 2024 00:32:48 GMT  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbeafe4a8ff43382a05a09d8b2f93e7f1e9334861540c89f78e2375d92b984eb`  
		Last Modified: Wed, 25 Dec 2024 05:38:45 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba456505d975bc57ffd4964694712c664262bd0f8fd51a87a2a8875e5362f84`  
		Last Modified: Wed, 25 Dec 2024 05:38:46 GMT  
		Size: 5.4 MB (5368158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed5f149deee53d2d9b74aac65bfcd924d3bbf39484072ae3732ca4186d9d55e`  
		Last Modified: Wed, 25 Dec 2024 05:38:45 GMT  
		Size: 1.4 MB (1368602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5862d679394d9b0a0e22e93413a2c34b088e5e8ff06f34e6e86cd83767480e`  
		Last Modified: Wed, 25 Dec 2024 05:38:46 GMT  
		Size: 8.1 MB (8066333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748bfabbd2c35935172b0e1c773fd58386b3d69ab51b67b791856d2cff13aef3`  
		Last Modified: Wed, 25 Dec 2024 05:38:46 GMT  
		Size: 1.3 MB (1283507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac34a224db4dc51fea89d30c1a7a8be48c643c4bf5ddf78adb1afb55775418e`  
		Last Modified: Wed, 25 Dec 2024 05:38:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbf2cbeeafaafd514fc56c7e7e137dcdc1b636c669c946dbe994678c403134e`  
		Last Modified: Wed, 25 Dec 2024 05:38:47 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8bff3e7f25552a5f39cdd22688ebf012cdb0a2dfdfab50eed54c8e7ff1af18`  
		Last Modified: Wed, 25 Dec 2024 05:43:53 GMT  
		Size: 113.2 MB (113181941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d004b3cf17020a6ad96827ed31a76d1304c2013d3885e70fd786e8db37f60d11`  
		Last Modified: Wed, 25 Dec 2024 05:43:50 GMT  
		Size: 9.5 KB (9523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5954ef6277aae1c3db6fc3ad7003f08d7ff30e8fcaa201334c03012e1fb58716`  
		Last Modified: Wed, 25 Dec 2024 05:43:50 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041b5c53b0d2c9dce929ba28985ed94d9d2188820dcd10a568d62f124c5f3acc`  
		Last Modified: Wed, 25 Dec 2024 05:43:50 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428d5ff245f512cc340b6d58a129a70a20454fc635aa6ed8c6145e3b6979a88d`  
		Last Modified: Wed, 25 Dec 2024 05:43:51 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46d4058edfcd3803ec774ccd10fdee2fcb51334568c8b7218c45f8c779d30ac`  
		Last Modified: Wed, 25 Dec 2024 05:43:51 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:7d48c0db082f31ef7f91a8ca3f39341f8a88ae1b028fc0f4202b5433e8961ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5717370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd90ec7ede52749fe0e76476fadcef60c3da8fece81a5aa42eacc4a3e195c1b`

```dockerfile
```

-	Layers:
	-	`sha256:bb4f1428c9877ef5bf19e858c9cc8d3e4decf325d995bffbdecef552cb05c85e`  
		Last Modified: Wed, 25 Dec 2024 05:43:50 GMT  
		Size: 5.7 MB (5662717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11fdeb9a7584fd4c90a2fdf9fd37808f602020441dd65b2c36b102b18b6cdba2`  
		Last Modified: Wed, 25 Dec 2024 05:43:50 GMT  
		Size: 54.7 KB (54653 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:62d251c561e75e31a3f00228781c040f34b92bd3f78620a6b0a9fe3f53398e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155181476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2548f5b4fcd5861a1b590cb23c9f09b9ab40c2c2791dcd5a93303507858c7935`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 21 Nov 2024 20:09:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_MAJOR=14
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_VERSION=14.15-1.pgdg120+1
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:09:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:09:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:09:59 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:09:59 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:09:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0e7e84bd4cca9e29f08dfac96d436e65bdd31929520e73147137b382fbc89b70`  
		Last Modified: Tue, 24 Dec 2024 21:33:49 GMT  
		Size: 26.9 MB (26878901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba32f000d1b4f78b8edf024cb0377fa89f44e1655de7fccea05048c424800f9`  
		Last Modified: Tue, 24 Dec 2024 23:48:23 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197d64fd8b3d03322c8aed80cc587df0fdadc0e2da415bb07878d3c0173ea5a5`  
		Last Modified: Tue, 24 Dec 2024 23:48:23 GMT  
		Size: 4.4 MB (4390988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06ea8686508c22fbd8b6935a9eb2e736a3f474cda70013f91a949660afe6699`  
		Last Modified: Tue, 24 Dec 2024 23:48:23 GMT  
		Size: 1.4 MB (1412671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674da2ed55b67ea5b4a3c0eb8de4cce3f08bffd965aed0ae73b1bcc8cd98a12b`  
		Last Modified: Tue, 24 Dec 2024 23:48:26 GMT  
		Size: 8.1 MB (8120416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da1c8e29b546c26241b6f4da70dfbb2a27e06983a39991edade37bbf94a59ca`  
		Last Modified: Tue, 24 Dec 2024 23:48:24 GMT  
		Size: 1.1 MB (1096715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cc88ca11d2e433e50d6f3b0e78ab5f667a8a9458239f972669541b814a5200`  
		Last Modified: Tue, 24 Dec 2024 23:48:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de32e4e7eaee0c381703208358befd3d61f01b6ebfd715194f7953862fc6b57`  
		Last Modified: Tue, 24 Dec 2024 23:48:24 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be1364282577d091369bd5eb041f949a351296bad488497930bc9c8631ba9f7`  
		Last Modified: Tue, 24 Dec 2024 23:52:39 GMT  
		Size: 113.3 MB (113261940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d70b4bffb7dec27e9bb6318b45c2ab035ad6b9622c5334dfc8d7895bf68392`  
		Last Modified: Tue, 24 Dec 2024 23:52:37 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8582f899bb762a29cd490496f096f782bb4964a8b69ced9d499c276ed45c383f`  
		Last Modified: Tue, 24 Dec 2024 23:52:37 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427686b0663af4e8e3ca1e59643b8d98eb0a37af0ff4a1938ecb1beb2a6868c0`  
		Last Modified: Tue, 24 Dec 2024 23:52:37 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f30aa52098e9f9fdbef8f7c447774deeebd64158f08d26b5ab5b5c1a3563282`  
		Size: 5.4 KB (5414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d901363932242ca5221d7948df62b4de1716790bdcc4826b0953a6241729878e`  
		Last Modified: Tue, 24 Dec 2024 23:52:37 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:5bb6a8e1b5d40cebf40a1087d149222e3c88c34f4f23f98dbfcced050324aa59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5709337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9429f2664eecff01975f02db42940c4b2e3f5dc65544cb7baff2138a29fefde`

```dockerfile
```

-	Layers:
	-	`sha256:e28b7752816966c1d4cf551a16badb798a554ca1a1c40ad21af08637b8c4572b`  
		Last Modified: Tue, 24 Dec 2024 23:52:37 GMT  
		Size: 5.7 MB (5654751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22b80e016fbe0d1c2e6e5f63b27cc1d000c2314ed0b97d83e3fb99239ee5d030`  
		Last Modified: Tue, 24 Dec 2024 23:52:36 GMT  
		Size: 54.6 KB (54586 bytes)  
		MIME: application/vnd.in-toto+json
