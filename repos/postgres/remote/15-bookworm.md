## `postgres:15-bookworm`

```console
$ docker pull postgres@sha256:6293e062bb2dc8e041b66f855400d192fd5f48affb60ba4e376a2fac1e7a1aae
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
$ docker pull postgres@sha256:042f6c70531f37d6b2b1ceed0cfd02b15327add1189053c47f514076140d9b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.9 MB (152942327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb3aef95ec35cd53030537a4951594371e362271078d817838468bc0ae390a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:33:37 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 16 Mar 2026 22:33:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:33:48 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 22:33:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 22:33:52 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 16 Mar 2026 22:33:52 GMT
ENV LANG=en_US.utf8
# Mon, 16 Mar 2026 22:33:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:33:55 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 16 Mar 2026 22:33:55 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:33:55 GMT
ENV PG_MAJOR=15
# Mon, 16 Mar 2026 22:33:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Mon, 16 Mar 2026 22:33:55 GMT
ENV PG_VERSION=15.17-1.pgdg12+1
# Mon, 16 Mar 2026 22:34:51 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 16 Mar 2026 22:34:51 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 16 Mar 2026 22:34:51 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 16 Mar 2026 22:34:51 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 16 Mar 2026 22:34:51 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 16 Mar 2026 22:34:51 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 16 Mar 2026 22:34:51 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:34:51 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 16 Mar 2026 22:34:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:34:51 GMT
STOPSIGNAL SIGINT
# Mon, 16 Mar 2026 22:34:51 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 16 Mar 2026 22:34:51 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:308071462adeead29755aa392d093fe050ca61248538fbe49841434009ba1303`  
		Last Modified: Mon, 16 Mar 2026 22:34:29 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb61875e3d87aa1b0c336f72303fc4bd5af58a61a5b1c57f37583957c706a73e`  
		Last Modified: Mon, 16 Mar 2026 22:34:29 GMT  
		Size: 4.5 MB (4534214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b29bd3e087342c434293cec3dcfd43419809e098e77b09ec0677c1b5642ba21`  
		Last Modified: Mon, 16 Mar 2026 22:34:29 GMT  
		Size: 1.2 MB (1249541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1a80f7ea9bf2e78899467d2f9de6cce724539ed38d70e7025886439567c5df`  
		Last Modified: Mon, 16 Mar 2026 22:34:29 GMT  
		Size: 8.1 MB (8066484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46706ee5d448c952935bf108f87839ee216b593259da33cca99586559afe6c6c`  
		Last Modified: Mon, 16 Mar 2026 22:34:30 GMT  
		Size: 1.2 MB (1196402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14008c33708c61917d31b583701528a15c2b4397ce0d5b26455ccb3a7cc7582c`  
		Last Modified: Mon, 16 Mar 2026 22:34:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e63d36f0d5fbf2e6612d230bd9a647e81ced751d892eda783ef8c0967915d4`  
		Last Modified: Mon, 16 Mar 2026 22:34:30 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8574d473dee97227b08b0e318b7bf06bb1af45fe25fdda0aa30ec032cef8583`  
		Last Modified: Mon, 16 Mar 2026 22:35:13 GMT  
		Size: 109.6 MB (109638946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95266f8b4d831dabcb07b01796614ef4eeeee1b6a4eaf2f6edb52573b30d902`  
		Last Modified: Mon, 16 Mar 2026 22:35:10 GMT  
		Size: 9.8 KB (9777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab3f9a27af8f768b4379a27572ecbada79175986540c3b06d7194f2a6855c44`  
		Last Modified: Mon, 16 Mar 2026 22:35:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c8c030ed3ba797be6fa0f9c522367f5ab376ba942a29262d7d0ce2fa8f47ca`  
		Last Modified: Mon, 16 Mar 2026 22:35:10 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e26bf82e5af232030965eab795f16a818e4e17eb01d36143d33857bee86def5`  
		Last Modified: Mon, 16 Mar 2026 22:35:11 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c40507d19cfc6c0bf5f5b7c0a1bff5a18a915927b0c86a3255be27fab2e3a2`  
		Last Modified: Mon, 16 Mar 2026 22:35:11 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:0257821ced6996c51aa10b7f32d1b504a9bc49a4800c6d1ca1e6fdccb6b94a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5896644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565ff6bb61a7803bd54a9c17deaccbd27805914eab55cb2be6724196a8273b5d`

```dockerfile
```

-	Layers:
	-	`sha256:0a038eed3b9af582cc9a7ff4230d2329585fecde4fbde1c8ba735727242df921`  
		Last Modified: Mon, 16 Mar 2026 22:35:10 GMT  
		Size: 5.8 MB (5843348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fcc3905c51bd627a3486c84caab83adf4433748cc7fa09b25259e1029d28719`  
		Last Modified: Mon, 16 Mar 2026 22:35:10 GMT  
		Size: 53.3 KB (53296 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:795ce4c11651e1f28bc204d83714855e61e54493f3ce8e6160c8a453da3c72c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.9 MB (145886389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ab9a61f7308058bd53b2c9294237aac483b241a5e09c23881d428ef3ff7843f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:44:01 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 16 Mar 2026 22:44:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:18 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 22:44:18 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 22:44:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 16 Mar 2026 22:44:26 GMT
ENV LANG=en_US.utf8
# Mon, 16 Mar 2026 22:44:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 16 Mar 2026 22:44:32 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:32 GMT
ENV PG_MAJOR=15
# Mon, 16 Mar 2026 22:44:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Mon, 16 Mar 2026 22:44:32 GMT
ENV PG_VERSION=15.17-1.pgdg12+1
# Mon, 16 Mar 2026 23:12:09 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 16 Mar 2026 23:12:09 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 16 Mar 2026 23:12:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 16 Mar 2026 23:12:09 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 16 Mar 2026 23:12:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 16 Mar 2026 23:12:09 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 16 Mar 2026 23:12:09 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:12:09 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 16 Mar 2026 23:12:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:12:09 GMT
STOPSIGNAL SIGINT
# Mon, 16 Mar 2026 23:12:09 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 16 Mar 2026 23:12:09 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3f1e11847ee1bf3b5b4789698fd7943a2f92f317682fd98071438c59f096b12b`  
		Last Modified: Mon, 16 Mar 2026 21:51:51 GMT  
		Size: 25.8 MB (25765607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ef36273d9fa45dbd8c73489530f2c34dd7e376d9a5d8a84cd08c1c8bb05ae6`  
		Last Modified: Mon, 16 Mar 2026 22:57:04 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf471a819b71ced4adaadfbd0a8d906f730733bff405b86518bda82b98a8eb56`  
		Last Modified: Mon, 16 Mar 2026 22:57:04 GMT  
		Size: 4.2 MB (4151337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddee39686fcc2064ae9db5f23f121f28375f698e9e16bdfc8c6256e7366ebc16`  
		Last Modified: Mon, 16 Mar 2026 22:57:04 GMT  
		Size: 1.2 MB (1220138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f57b7279d9495fef9bcaf240e563d71c30f0da11b13d0207d72c31fd3d4595`  
		Last Modified: Mon, 16 Mar 2026 22:57:04 GMT  
		Size: 8.1 MB (8066574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7edbdb63be524b471856abba615bfd5433f8c73fb54c0e34b75b21bff7d983`  
		Last Modified: Mon, 16 Mar 2026 22:57:05 GMT  
		Size: 1.2 MB (1195080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc0561c9ed0bb2939f9453c721bb6a265d9a016aa36776c2cd4259b4bcc3fc1`  
		Last Modified: Mon, 16 Mar 2026 22:57:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6839a059aca6490a2913f6823e9e9714bec8cc887533fed5f2efe420155177e`  
		Last Modified: Mon, 16 Mar 2026 22:57:05 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90df86a03a659b231aeefe528ae48072464fda60f78221cdff188dc6041c5d3d`  
		Last Modified: Mon, 16 Mar 2026 23:12:30 GMT  
		Size: 105.5 MB (105467132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a844f421f1c84f42cbbf9b5780bbb3a21eed2adddddc38c7122e2443c88887`  
		Last Modified: Mon, 16 Mar 2026 23:12:27 GMT  
		Size: 9.8 KB (9784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc2a8d49c2148c3fbb3215b810727258c62ff3e0fd7bcfc9d79ee94e14776b3`  
		Last Modified: Mon, 16 Mar 2026 23:12:27 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d65cb8e99381369271121de9ca2780c2d17b7df1023de29ee2a2c79c903a89`  
		Last Modified: Mon, 16 Mar 2026 23:12:27 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a371a6854548069e63f6edba52c28eaec94261e2a6327792a0dab63b3fe31b28`  
		Last Modified: Mon, 16 Mar 2026 23:12:28 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081005dcd451a2bbd649946fb24b5ff4ffce2c7ce5c27ae002fc3b65330fecbf`  
		Last Modified: Mon, 16 Mar 2026 23:12:28 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:93ee10f2241e14abaf5b7b30d051e1be8c38cdb01d22205360e01661a8fea1a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5910952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b00052213982129e309506f4a8ede11986f0d742a1413c7a4b200c7a5a6e63`

```dockerfile
```

-	Layers:
	-	`sha256:b15b02fc39b52508b0748eaafb32f28b2ae9eb13cdeb35b9190517bdd0750131`  
		Last Modified: Mon, 16 Mar 2026 23:12:28 GMT  
		Size: 5.9 MB (5857449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18a6c2f37896393540c98e7eb3441487523dae948451068c9dca0fc2d009e407`  
		Last Modified: Mon, 16 Mar 2026 23:12:27 GMT  
		Size: 53.5 KB (53503 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:44147d8f60c48673a3c2730f5fbe688cf53338dd8f63e13422a8f1c262b8d0cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140947353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ca7f43e612ed3acfa8916eede0d60af8bed8587e517e7a91cb9b55292e4f20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:05:17 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 16 Mar 2026 23:05:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:05:30 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 23:05:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 23:05:35 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 16 Mar 2026 23:05:35 GMT
ENV LANG=en_US.utf8
# Mon, 16 Mar 2026 23:05:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:05:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 16 Mar 2026 23:05:40 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 23:05:40 GMT
ENV PG_MAJOR=15
# Mon, 16 Mar 2026 23:05:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Mon, 16 Mar 2026 23:05:40 GMT
ENV PG_VERSION=15.17-1.pgdg12+1
# Mon, 16 Mar 2026 23:19:32 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 16 Mar 2026 23:19:32 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 16 Mar 2026 23:19:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 16 Mar 2026 23:19:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 16 Mar 2026 23:19:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 16 Mar 2026 23:19:32 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 16 Mar 2026 23:19:32 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:19:32 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 16 Mar 2026 23:19:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:19:32 GMT
STOPSIGNAL SIGINT
# Mon, 16 Mar 2026 23:19:32 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 16 Mar 2026 23:19:32 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55991ea69ad5e39129b39106af7c435a81c2072a1a7e5d965144ac893a958995`  
		Last Modified: Mon, 16 Mar 2026 23:19:50 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e78ef659f69dec1ed4b643858f500e095d765718068fe4cf8157a79d591a6ac`  
		Last Modified: Mon, 16 Mar 2026 23:19:50 GMT  
		Size: 3.7 MB (3742670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca78c4bcd82c4e4229fd9cd63c75cbb9fc0dbe9d0fe967003fc46e4b7fe02fb`  
		Last Modified: Mon, 16 Mar 2026 23:19:50 GMT  
		Size: 1.2 MB (1215980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721c006d909fbed5b4dcc329dafc326152b0bae0c4bf2659d4a8f3b17bd91718`  
		Last Modified: Mon, 16 Mar 2026 23:19:50 GMT  
		Size: 8.1 MB (8066389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1a59514d8bd10774f3aeeb7fc2116629cfd74caa7f3b3a51f6a0c3c120012b`  
		Last Modified: Mon, 16 Mar 2026 23:19:51 GMT  
		Size: 1.1 MB (1067276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4e8c08fbf8761882a1ea11f3d843e5269308355c9c2ffd4172297bc6c487f9`  
		Last Modified: Mon, 16 Mar 2026 23:19:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e51f02d2a8c8d9e46c62738dd5f7ad74b651b0ef1e0e9bb1e2b9b4b44df5af`  
		Last Modified: Mon, 16 Mar 2026 23:19:51 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0bc4a794bea46dda53ecd8bed1ce201127eafc82b8fd958648bfff9ac98a11`  
		Last Modified: Mon, 16 Mar 2026 23:19:54 GMT  
		Size: 102.9 MB (102893166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:448ec9ac4ae72da36b591930c563422c40c20031998fc21be2625e56fe8e0ccc`  
		Last Modified: Mon, 16 Mar 2026 23:19:52 GMT  
		Size: 9.8 KB (9786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7b7b44b5d6cc273e6a9b037a0b931db835673dc3e500cb83ac126fa54fc7e0`  
		Last Modified: Mon, 16 Mar 2026 23:19:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185709110b04f2ca73b7d00df9a7afb5f21f5ae8ebea440f01fb255b7d86d45f`  
		Last Modified: Mon, 16 Mar 2026 23:19:52 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9188d6b1e1ca0d1dba4e5232c4a7d42e6106eb2a2f1d026eec182e884a6d50c`  
		Last Modified: Mon, 16 Mar 2026 23:19:53 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a86e5925db366fd22a8231705018b11594ddb33143fdd929c6adcbccf471c3b`  
		Last Modified: Mon, 16 Mar 2026 23:19:53 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:84ff77f64719867c5241081c535521e7492dc47686a94670c368f0e9fc407742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5910207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:773b67114aa31c761a345578693aa90dd72f4964bbd535fe9210f1af551ca1c3`

```dockerfile
```

-	Layers:
	-	`sha256:c5749bf8b04900e1a19eafecffbc38650ec138c3b2b79ce1a50c9f10410e2802`  
		Last Modified: Mon, 16 Mar 2026 23:19:50 GMT  
		Size: 5.9 MB (5856704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae8540d0485dfe2d8967033146bbb031327cd9aa7c21a14bae2ae0a8e9a0b8dd`  
		Last Modified: Mon, 16 Mar 2026 23:19:50 GMT  
		Size: 53.5 KB (53503 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:d52f07501e4de4458af9c212ece3a5518877d2812042de988175dd8c1d2977e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150939772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f1c7b926c20060ef54d486ee7f67c1277741d188fa5e3e3dd15ecbe2d4347cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:36:24 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 16 Mar 2026 22:36:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:36:35 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 22:36:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 22:36:40 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 16 Mar 2026 22:36:40 GMT
ENV LANG=en_US.utf8
# Mon, 16 Mar 2026 22:36:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:36:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 16 Mar 2026 22:36:44 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:36:44 GMT
ENV PG_MAJOR=15
# Mon, 16 Mar 2026 22:36:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Mon, 16 Mar 2026 22:36:44 GMT
ENV PG_VERSION=15.17-1.pgdg12+1
# Mon, 16 Mar 2026 22:36:57 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 16 Mar 2026 22:36:57 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 16 Mar 2026 22:36:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 16 Mar 2026 22:36:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 16 Mar 2026 22:36:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 16 Mar 2026 22:36:57 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 16 Mar 2026 22:36:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:36:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 16 Mar 2026 22:36:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:36:57 GMT
STOPSIGNAL SIGINT
# Mon, 16 Mar 2026 22:36:57 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 16 Mar 2026 22:36:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42a20880a79d253228af8a509bc4ee4c762a67b7bf646f07a5eb7c7f9422e3c`  
		Last Modified: Mon, 16 Mar 2026 22:37:16 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b28ab2a1d71a55e5b72e8fddc045a230dacabed791785a0b88cb43dabf6756`  
		Last Modified: Mon, 16 Mar 2026 22:37:16 GMT  
		Size: 4.5 MB (4519491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7279b37560c576c0a414803a8cfa1ee22512383144dc7a920761a8ad0721c7c3`  
		Last Modified: Mon, 16 Mar 2026 22:37:16 GMT  
		Size: 1.2 MB (1203295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30120808454b8d0144f9884274364dbc03b61224e729cde7bb26225a091ea735`  
		Last Modified: Mon, 16 Mar 2026 22:37:17 GMT  
		Size: 8.1 MB (8066489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8a0a1810b3300af96dd8cd9911a1733c6c7bdbd3ce57c4260e6b001e231532`  
		Last Modified: Mon, 16 Mar 2026 22:37:17 GMT  
		Size: 1.1 MB (1108984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37dac0e28c2bc52558512268abccb672ad2f47a598c96f5a8347820882a59b40`  
		Last Modified: Mon, 16 Mar 2026 22:37:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d79d8576b175f1c0fd45ade009f7d3bd6dbb0c2a7d1021296f666c98d86fd9a`  
		Last Modified: Mon, 16 Mar 2026 22:37:18 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb59c376ff34d523d53bee961cf68db8c39fe0347c24741f3e8a9ac7874f432`  
		Last Modified: Mon, 16 Mar 2026 22:37:20 GMT  
		Size: 107.9 MB (107904930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4d3e15ef032508e95af043d5fafd383701823739249b87f0c3abd86e3f9f3a`  
		Last Modified: Mon, 16 Mar 2026 22:37:19 GMT  
		Size: 9.8 KB (9778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad15183028abeca072d36f732f5fcbcb5597c9bf6e081cb224bb162aabe36a5a`  
		Last Modified: Mon, 16 Mar 2026 22:37:19 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee689c837f04e0f8ff2b8857a4b77974bf00240e8929bebe53e99460fdef340`  
		Last Modified: Mon, 16 Mar 2026 22:37:19 GMT  
		Size: 165.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af0a4d35d413ed22b582b1ce389bb2598fef3ee33e34b74d9d6adbd6582a66b`  
		Last Modified: Mon, 16 Mar 2026 22:37:20 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe835d7bf40728f47112283e0db6c20032bf4bff3c3bf4da0642d88592760366`  
		Last Modified: Mon, 16 Mar 2026 22:37:20 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:10ee6cf454478e565659b091319876af587825e0379df4c4cd7c5d6382f4cd60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5903199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36b1d2452005236fbd009791520286e28753ecdae372b69f0a1392c6456e64b`

```dockerfile
```

-	Layers:
	-	`sha256:7b53028580ef87caaa7d13566f3f035cba7a684689230376eb4023376312be50`  
		Last Modified: Mon, 16 Mar 2026 22:37:16 GMT  
		Size: 5.8 MB (5849659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63f5265b48915b7adda4d14d93b6de00ed397de96a5a3e50c6af4806b3f50eb2`  
		Last Modified: Mon, 16 Mar 2026 22:37:16 GMT  
		Size: 53.5 KB (53540 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:9fa4c18d0d41813883c106ee0192f8e92b64fe8a1487a650bb6238d3dec41aa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161647135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54eebf2088a83f5645d15773225756fb53d4825d62297a5931757990b623afae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:32:58 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 16 Mar 2026 22:33:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:33:09 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 22:33:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 22:33:13 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 16 Mar 2026 22:33:13 GMT
ENV LANG=en_US.utf8
# Mon, 16 Mar 2026 22:33:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:33:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 16 Mar 2026 22:33:16 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:33:16 GMT
ENV PG_MAJOR=15
# Mon, 16 Mar 2026 22:33:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Mon, 16 Mar 2026 22:33:16 GMT
ENV PG_VERSION=15.17-1.pgdg12+1
# Mon, 16 Mar 2026 22:42:46 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 16 Mar 2026 22:42:46 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 16 Mar 2026 22:42:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 16 Mar 2026 22:42:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 16 Mar 2026 22:42:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 16 Mar 2026 22:42:46 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 16 Mar 2026 22:42:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:42:47 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 16 Mar 2026 22:42:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:42:47 GMT
STOPSIGNAL SIGINT
# Mon, 16 Mar 2026 22:42:47 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 16 Mar 2026 22:42:47 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f649af5ed0883ac0b5027f768cbd9576b7bc8c76adac1eddeb4035e88b9258fe`  
		Last Modified: Mon, 16 Mar 2026 21:53:10 GMT  
		Size: 29.2 MB (29221681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea46623a09c9e79d9b3e31b5bb5de85b24f6d202391260c9e2b34fdf03da350`  
		Last Modified: Mon, 16 Mar 2026 22:43:04 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac6edc56a4693c01cb1439f4b7d90d51a2dc13d89d7f3aae6e4e9a55befd295`  
		Last Modified: Mon, 16 Mar 2026 22:43:04 GMT  
		Size: 5.0 MB (4966079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ec7fb5a1f75b2e66b68d5cf4c1ed3a7da3ae1dd47d833152714a387838f1be`  
		Last Modified: Mon, 16 Mar 2026 22:43:04 GMT  
		Size: 1.2 MB (1218641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5a5473e5a82f2aca49d7da1af1bee2ebbf3ecdf4706d68eccf9f923961c2c2`  
		Last Modified: Mon, 16 Mar 2026 22:43:05 GMT  
		Size: 8.1 MB (8066447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8467b077058d2b024b7ab101f0b0f0dd9503c2f720f01e64c56417cd0679950b`  
		Last Modified: Mon, 16 Mar 2026 22:43:05 GMT  
		Size: 1.1 MB (1137487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021f07c6beb0845e388770d0d09ad825412d4dbeba1f980ae10f54d0bdbdfd0e`  
		Last Modified: Mon, 16 Mar 2026 22:43:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f5991367bfa61bc2bf358ac6815fdfcd306002c4c0dddfccd1c88d0a4795e0`  
		Last Modified: Mon, 16 Mar 2026 22:43:05 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740aed49e26d48010adf4787c319077b901533753f2807f44d04bb004e7b2370`  
		Last Modified: Mon, 16 Mar 2026 22:43:09 GMT  
		Size: 117.0 MB (117016273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f6e371505c8b1085618675f3107d702021f45302ac1b99849727b552937aed`  
		Last Modified: Mon, 16 Mar 2026 22:43:06 GMT  
		Size: 9.8 KB (9784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7f1a7178b4807d115f59e7a81004aec0a5582ca469bc4f2d6392a59b024787`  
		Last Modified: Mon, 16 Mar 2026 22:43:06 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8a9fbb960a3f2e3ebd0c7f67b24127038fc400bd724b7a38c4601f33462db4`  
		Last Modified: Mon, 16 Mar 2026 22:43:07 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba454187760856c58b3f4672d913b9169241faa70a023bb43c4b59918457ca03`  
		Last Modified: Mon, 16 Mar 2026 22:43:08 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0d5d37c5e5e27b6d61d08b12d0de9bbda99ed49d65ae4d1d9dd3cb03436a18`  
		Last Modified: Mon, 16 Mar 2026 22:43:08 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:3edede641c145b6bc71672251f65ac7af5aa37544a52d7e5506a64654338cfb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b5e613ce42261f2fb10ed0cf3820d988a3e7eeab3ec086dd952e752e5aa0d3`

```dockerfile
```

-	Layers:
	-	`sha256:eb74f29af19f458917d350afc955157218485eba691e8b5e7d13c2c557d5702f`  
		Last Modified: Mon, 16 Mar 2026 22:43:04 GMT  
		Size: 5.9 MB (5855592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca8fb3d9530d7dd79cbbc2dbc1c76f3ad964a061c782ed1b4cc09017e62ba877`  
		Last Modified: Mon, 16 Mar 2026 22:43:04 GMT  
		Size: 53.3 KB (53252 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:a36a36325c4f62daaf3f6f3fe78f3a6f0bca822196af5dedda4f03ff63c05f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.8 MB (151755569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9795d02a89ef3788a5357fc70ec60365a9ea3c02cda7aeee5522697e2ea2d552`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 23:43:05 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 24 Feb 2026 23:43:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 23:44:15 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 23:44:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 23:44:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 24 Feb 2026 23:44:43 GMT
ENV LANG=en_US.utf8
# Tue, 24 Feb 2026 23:45:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 23:45:04 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 24 Feb 2026 23:45:07 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Feb 2026 23:45:07 GMT
ENV PG_MAJOR=15
# Tue, 24 Feb 2026 23:45:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 24 Feb 2026 23:45:07 GMT
ENV PG_VERSION=15.17-1.pgdg12+1
# Thu, 26 Feb 2026 23:57:28 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Feb 2026 23:57:30 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 23:57:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 23:57:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Feb 2026 23:57:34 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Feb 2026 23:57:34 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Feb 2026 23:57:35 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 23:57:37 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 23:57:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 23:57:37 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 23:57:37 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 23:57:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:00b501106805d55ebe605ff077d09c8c22aa2ccf0dd9ceffb2a21c5319633322`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 28.5 MB (28526197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a6f997a2bae9d6583f7a9d6141815e9b9041dff337d7ac153b3f46c5b805f5`  
		Last Modified: Wed, 25 Feb 2026 00:57:53 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd847e167f615e000df95c8ddbf4ec913956e8de429393c14d6579c8fa3b6eec`  
		Last Modified: Wed, 25 Feb 2026 00:57:53 GMT  
		Size: 4.5 MB (4475211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509b6c5cb25f9d256fb91972058d92c97ec72660257a5e4a0567b93d983683e4`  
		Last Modified: Wed, 25 Feb 2026 00:57:53 GMT  
		Size: 1.2 MB (1159230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d89b9e442925e9f99cc7d8126d286c933d9fa2af1dcd629bbe272d3991148e6`  
		Last Modified: Wed, 25 Feb 2026 00:57:54 GMT  
		Size: 8.1 MB (8066656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf9052eb778f8906ff20e40210c947a76e79676a164349c0d43640103061a45`  
		Last Modified: Wed, 25 Feb 2026 00:57:54 GMT  
		Size: 1.2 MB (1182880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6855c7d85646174eb68be28db5ef4c48412e69cc602e86bd03308406068383`  
		Last Modified: Wed, 25 Feb 2026 00:57:55 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b8fcdebfff3d96daa7d06b1c7d79991f36b897615adee4b706b0a3403cc991`  
		Last Modified: Wed, 25 Feb 2026 00:57:55 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70d6fa7d4c8c1fc3a28436f97c80486b670c8b45172e04c66ca0284a038ed38`  
		Last Modified: Thu, 26 Feb 2026 23:59:43 GMT  
		Size: 108.3 MB (108324866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2292d4ec60b6e7ad631f7d28a7da955112f42f898986bfc8f611941fee548b`  
		Last Modified: Thu, 26 Feb 2026 23:59:32 GMT  
		Size: 9.8 KB (9786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8861b076bfc2f2195512a594ef20d6b723309fa0660b106d2fb91a94e22792`  
		Last Modified: Thu, 26 Feb 2026 23:59:31 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d88a4a5d1a44f9c70b5f09c1d7333c956e5c007bbd40406d5023923f3ddb03`  
		Last Modified: Thu, 26 Feb 2026 23:59:31 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9dbb92b44a303b7fe7ebb57f8b808407672349adb6d2fce0f8358b04a93a78`  
		Last Modified: Thu, 26 Feb 2026 23:59:32 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385d3386c375dd4a7a77d6748a8fd84e309fde05ae3336a600fe236dd9c52672`  
		Last Modified: Thu, 26 Feb 2026 23:59:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:82c401468d9962f5f63f73bce15f3baff33a294d2cff3397fe1a9d5545b05012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 KB (53162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2638380ebcc0fbd0c28b61c596f1bdd758bbeb83a6b4faee4afb3b178b4cc043`

```dockerfile
```

-	Layers:
	-	`sha256:ca25a8cf2991647e9f3d5af22c5c29e8d9ac221df3a724903edd1985a0581248`  
		Last Modified: Thu, 26 Feb 2026 23:59:31 GMT  
		Size: 53.2 KB (53162 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:8f1b6284867864ec9dd9fd00a33fc5141f2e201a108311f78f3482bd9d90edba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.7 MB (165657741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c30b8a2ee126290a0a86a3d60474965f09fc7c36bf230cd62a94d2f63a52db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:58:45 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 24 Feb 2026 20:58:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:59:12 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 20:59:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 20:59:24 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 24 Feb 2026 20:59:24 GMT
ENV LANG=en_US.utf8
# Tue, 24 Feb 2026 20:59:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:59:33 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 24 Feb 2026 20:59:34 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Feb 2026 20:59:34 GMT
ENV PG_MAJOR=15
# Tue, 24 Feb 2026 20:59:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 24 Feb 2026 20:59:34 GMT
ENV PG_VERSION=15.17-1.pgdg12+1
# Thu, 26 Feb 2026 19:34:18 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:34:20 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:34:21 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:34:21 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Feb 2026 19:34:22 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Feb 2026 19:34:22 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Feb 2026 19:34:22 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:34:22 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:34:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:34:22 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:34:22 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:34:22 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3def25e912c223ee8b3899e5ca048b2439f856f438ac690293817fbc0291fb36`  
		Last Modified: Tue, 24 Feb 2026 18:41:49 GMT  
		Size: 32.1 MB (32078334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90fc91454a9561e6b11ad598da906c78edd30b499ff2234b49dd32562f2c327c`  
		Last Modified: Tue, 24 Feb 2026 21:01:12 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f53303ce4ed753a310b22dbdd2260f27925694aff49febb2da931d330f89bc`  
		Last Modified: Tue, 24 Feb 2026 21:01:12 GMT  
		Size: 5.4 MB (5368639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee621534fc9f66a74f75456ce763e23a22f0bc8cdc58a4cf5c532ec7ead1e2b`  
		Last Modified: Tue, 24 Feb 2026 21:01:12 GMT  
		Size: 1.2 MB (1208227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90aa3b04a3699b4d451ff19b898207a36991bb24bf9881e1da9dcb3840f656e8`  
		Last Modified: Tue, 24 Feb 2026 21:01:13 GMT  
		Size: 8.1 MB (8066558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943e3810ae0d32fbeb98071444fca03c119b767293f42d9aa091464e3b675fe7`  
		Last Modified: Tue, 24 Feb 2026 21:01:13 GMT  
		Size: 1.3 MB (1283663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbd92721995d8dfe36dd9311ada9eb9d7eb6474ce076a43abffcccfa4a272c7`  
		Last Modified: Tue, 24 Feb 2026 21:01:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e741e6e7c45af4f4d1a256134152099f5565df888582d1592322f7bfe7df5a`  
		Last Modified: Tue, 24 Feb 2026 21:01:15 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6ab97fce5c8bfff9167f53186560a535e0cd695154c3d63701a58b6c87a133`  
		Last Modified: Thu, 26 Feb 2026 19:35:14 GMT  
		Size: 117.6 MB (117631794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a1e36ad4bb959dd5bd22fd2324f2b0368f16d356796799eb3afd37779cd4a8`  
		Last Modified: Thu, 26 Feb 2026 19:35:10 GMT  
		Size: 9.8 KB (9780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046d89897d84fc86db338b45f5609f5e396f866e1dedd3dc96e35989b47d2191`  
		Last Modified: Thu, 26 Feb 2026 19:35:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c7ee09347395a9527e0b9d817820309eb5d48e4b9281506aaed0a744c54841`  
		Last Modified: Thu, 26 Feb 2026 19:35:10 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0200475cf77558aa19924a96cacae8de5b35d4a272d297214404f1c81f07a7c`  
		Last Modified: Thu, 26 Feb 2026 19:35:12 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6e049985ef38228a1abcea7966c38abd99b4bc2dbb8cde62502f083ac7b1ac`  
		Last Modified: Thu, 26 Feb 2026 19:35:12 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:d40434f66c18b601f1a7842f85c4007d28172efb4443cde7a076bab6cca5c1d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5904059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67d1fa3e01d877853450610d5e06426e5fdecd14e576da3e0486b8afb27dc674`

```dockerfile
```

-	Layers:
	-	`sha256:7aa089081ddfb209df989c755b4595a193d8cd5d649c4f6764a694af4fcd1e7b`  
		Last Modified: Thu, 26 Feb 2026 19:35:10 GMT  
		Size: 5.9 MB (5850709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bb2698a5751a09c59c0512dae3e5a7f3636fe7b81f6b5e3fe0aca0852f64e2d`  
		Last Modified: Thu, 26 Feb 2026 19:35:10 GMT  
		Size: 53.4 KB (53350 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:868a642b4f126787d6c1728a6bc894843794525389b5e7e9d20807106035f9f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.1 MB (162106247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d99f1d05b8a177fdcf7b06a013d1cecf407a2be8df71cbb55a433b2cae654a8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:06:41 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 16 Mar 2026 23:06:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:06:53 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 23:06:53 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 23:06:59 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 16 Mar 2026 23:06:59 GMT
ENV LANG=en_US.utf8
# Mon, 16 Mar 2026 23:07:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:07:02 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 16 Mar 2026 23:07:03 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 23:07:03 GMT
ENV PG_MAJOR=15
# Mon, 16 Mar 2026 23:07:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Mon, 16 Mar 2026 23:07:03 GMT
ENV PG_VERSION=15.17-1.pgdg12+1
# Mon, 16 Mar 2026 23:35:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 16 Mar 2026 23:35:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 16 Mar 2026 23:35:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 16 Mar 2026 23:35:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 16 Mar 2026 23:35:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 16 Mar 2026 23:35:12 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 16 Mar 2026 23:35:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:35:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 16 Mar 2026 23:35:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:35:13 GMT
STOPSIGNAL SIGINT
# Mon, 16 Mar 2026 23:35:13 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 16 Mar 2026 23:35:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f971a946f501019b7d025d943d39a1710e737577ec8101ad336f8933ccf8b2`  
		Last Modified: Mon, 16 Mar 2026 23:21:28 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276319bdc586d1987fc23023c8661bb41f84aa720a67c98849e42523c29b104f`  
		Last Modified: Mon, 16 Mar 2026 23:21:28 GMT  
		Size: 4.4 MB (4391205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca5d2d9aa5664d085887967b100f94ca5843d76a80767feb0b1a2bb1c5649f3`  
		Last Modified: Mon, 16 Mar 2026 23:21:28 GMT  
		Size: 1.2 MB (1222806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91174cb23f15048bf318f22a03e095c8af26b73dcef08fa1d56596fc1305c59c`  
		Last Modified: Mon, 16 Mar 2026 23:21:28 GMT  
		Size: 8.1 MB (8120727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91adf7122136fb26677c16d9d05b642a56106aec0de002c37d0b8298c099174c`  
		Last Modified: Mon, 16 Mar 2026 23:21:29 GMT  
		Size: 1.1 MB (1097064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441807e35600cec2024e9e4aa2b5bdac8d86b7c58b1dda3ad110af83c4eed7b5`  
		Last Modified: Mon, 16 Mar 2026 23:21:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80c53282092bcb54a070533bb12d2adf041fc7d2657f5104bf53e7a8dd161e2`  
		Last Modified: Mon, 16 Mar 2026 23:21:29 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56bfb2bb61e891d969ba7dea48d09acad8ea3c3f4bfff04a440413f8a8fd85be`  
		Last Modified: Mon, 16 Mar 2026 23:35:49 GMT  
		Size: 120.4 MB (120362408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53dad1a057331b0f990d69303c7126568109863eb3979ad1db3ef0552c1313a`  
		Last Modified: Mon, 16 Mar 2026 23:35:47 GMT  
		Size: 9.8 KB (9779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0cb1f8e5f976c4a29d601b7d97fe6af8db72f5c5269be61bcf02d8e4f6620a9`  
		Last Modified: Mon, 16 Mar 2026 23:35:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cad72ed163b8610bd40da55433b73db14fdc088837e5dac37fe71bcd459972`  
		Last Modified: Mon, 16 Mar 2026 23:35:47 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef0727a0591a0e49728c2cbb9c4a3f820449590f288781c7f51aa5ce0cb466b`  
		Last Modified: Mon, 16 Mar 2026 23:35:48 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0371c10b107a57bb110526fe2acba9ba57344cbb14efddf877ae62ba113dc9af`  
		Last Modified: Mon, 16 Mar 2026 23:35:48 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:c50cb4c28fdfa5ae99d346448c15c1a2137f85478087e4dec73ef22e1230f3c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc79cfdb22d1974da00a88b4e0043017a7f0832f43881cfd3808ee1414c06574`

```dockerfile
```

-	Layers:
	-	`sha256:fb0a23abd4856152a56a5380259833291c0e4f56b7a421ab392da2e07db4ee74`  
		Last Modified: Mon, 16 Mar 2026 23:35:47 GMT  
		Size: 5.9 MB (5852068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8459738b244aba5770f71c3453df5b521d4eba241fbf2e0c85705f0f2f4ebf59`  
		Last Modified: Mon, 16 Mar 2026 23:35:47 GMT  
		Size: 53.3 KB (53296 bytes)  
		MIME: application/vnd.in-toto+json
