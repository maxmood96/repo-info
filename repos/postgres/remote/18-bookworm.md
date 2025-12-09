## `postgres:18-bookworm`

```console
$ docker pull postgres@sha256:4bda5f6c48fd7b8cb4da5c5288f8e01cb4db38863c5e7c375fa87b4a2742aba0
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

### `postgres:18-bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:36ea14a25ca28492cbe33ee35a27de1cf9ef2ede2a575d1181629cfc4a3dab1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157057575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe09e734f4c4a95bc3e18a6360901fc880d43c8f7026dec94943ad3825cdb85c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:02:10 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 08 Dec 2025 23:02:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:02:23 GMT
ENV GOSU_VERSION=1.19
# Mon, 08 Dec 2025 23:02:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Dec 2025 23:02:28 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 08 Dec 2025 23:02:28 GMT
ENV LANG=en_US.utf8
# Mon, 08 Dec 2025 23:02:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:02:31 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Dec 2025 23:02:32 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:02:32 GMT
ENV PG_MAJOR=18
# Mon, 08 Dec 2025 23:02:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 08 Dec 2025 23:02:32 GMT
ENV PG_VERSION=18.1-1.pgdg12+2
# Mon, 08 Dec 2025 23:02:47 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 08 Dec 2025 23:02:47 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 08 Dec 2025 23:02:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 08 Dec 2025 23:02:47 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 08 Dec 2025 23:02:47 GMT
VOLUME [/var/lib/postgresql]
# Mon, 08 Dec 2025 23:02:47 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:02:47 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 08 Dec 2025 23:02:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:02:47 GMT
STOPSIGNAL SIGINT
# Mon, 08 Dec 2025 23:02:47 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 08 Dec 2025 23:02:47 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181dba553b298a7e16b8c63034c09af91ef0042476bc8f69b0e3f97aa8c280ad`  
		Last Modified: Mon, 08 Dec 2025 23:03:18 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a764cb3797b04b9360f196c186cba6f6da2100ffa4d1808ea987e7870f9dd22`  
		Last Modified: Mon, 08 Dec 2025 23:03:18 GMT  
		Size: 4.5 MB (4534103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9270c04f295b0b038436965f6dc54fbf3cd99442eece5ffdb026a8fd17e0265`  
		Last Modified: Mon, 08 Dec 2025 23:03:18 GMT  
		Size: 1.2 MB (1249505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383e32669f2a0c797a2277960f780471803af874c01f2a85afbb71cd59e0cd92`  
		Last Modified: Mon, 08 Dec 2025 23:03:19 GMT  
		Size: 8.1 MB (8066478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edefe7b1623b96f717dd8736adb1bd737e478611f4bfe69b40be0c30a31af9bf`  
		Last Modified: Mon, 08 Dec 2025 23:03:18 GMT  
		Size: 1.2 MB (1196412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499256b18824d7e6a794b3542e19e18e41a5242e0c138efdcdd5403e1197fb74`  
		Last Modified: Mon, 08 Dec 2025 23:03:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b16fb1577abe65c2c4a37460869310c68b7dedf3995f989cfb599d87bd40c1`  
		Last Modified: Mon, 08 Dec 2025 23:03:18 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080ea083aa379a1cded33ae90742c9bff2439fd549ed9c07e49a5a1edc5c7b58`  
		Last Modified: Mon, 08 Dec 2025 23:03:29 GMT  
		Size: 113.8 MB (113753003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677d1004905877383ce61af58e554973ccced93a90e6cf0182528669e6281cf2`  
		Last Modified: Mon, 08 Dec 2025 23:03:18 GMT  
		Size: 19.1 KB (19079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31bdc613a4d857698c353fa213989128df868ffb8d640d12212b542a261eb66`  
		Last Modified: Mon, 08 Dec 2025 23:03:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7a96a6ae2a284509b97335f69b84fac7733a9082c6b58f9bbf87cbbd89dc38`  
		Last Modified: Mon, 08 Dec 2025 23:03:20 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0508b796e86aa0b82b5aa5f203bbfa14cde7b8f5331a8185081caea0a3b59488`  
		Last Modified: Mon, 08 Dec 2025 23:03:19 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:e4e6c75a372dbea5166c1c8b9756a7fb7900a18c4eb640b78d839128e8bcc239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6208076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b35c86a64e697979f2d14ea2b1699c8e4f87354948492e2f12bdcb7912f38c2d`

```dockerfile
```

-	Layers:
	-	`sha256:eb1e3b64a9e1168bdf6316d158681060e6b79119aaaba94dc0329c8d7b1d2e59`  
		Last Modified: Tue, 09 Dec 2025 00:11:02 GMT  
		Size: 6.2 MB (6156487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ada74586c103595e81f54f68820c2d11dc2db3bb8a23e63dfbac8ab1d71fdbfa`  
		Last Modified: Tue, 09 Dec 2025 00:11:03 GMT  
		Size: 51.6 KB (51589 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:c91da1dd832d0ca6819e7f6e375aa295ccd7efa2153f5e40820e7fd7a7c95080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.2 MB (87151970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef4e2a05cae0f571b026692c7856457d8003c5fe94f4e14b1f156d0655403bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:23:44 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 08 Dec 2025 23:23:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:24:02 GMT
ENV GOSU_VERSION=1.19
# Mon, 08 Dec 2025 23:24:02 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Dec 2025 23:24:09 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 08 Dec 2025 23:24:09 GMT
ENV LANG=en_US.utf8
# Mon, 08 Dec 2025 23:24:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:24:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Dec 2025 23:24:16 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:24:16 GMT
ENV PG_MAJOR=18
# Mon, 08 Dec 2025 23:24:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 08 Dec 2025 23:24:16 GMT
ENV PG_VERSION=18.1-1.pgdg12+2
# Mon, 08 Dec 2025 23:36:43 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 08 Dec 2025 23:36:43 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 08 Dec 2025 23:36:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 08 Dec 2025 23:36:43 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 08 Dec 2025 23:36:43 GMT
VOLUME [/var/lib/postgresql]
# Mon, 08 Dec 2025 23:36:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:36:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 08 Dec 2025 23:36:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:36:43 GMT
STOPSIGNAL SIGINT
# Mon, 08 Dec 2025 23:36:43 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 08 Dec 2025 23:36:43 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:20ca79728ab9e4eb574872cf271bd965c51cf4e8ac84660ef17b281a3aeb750e`  
		Last Modified: Mon, 08 Dec 2025 22:16:26 GMT  
		Size: 25.8 MB (25757588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18021fc7241623fadeb5cd0935694226a64a48676c5d825286aa42839cd9f634`  
		Last Modified: Mon, 08 Dec 2025 23:37:04 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866e60be16179cc1dc5ff2b2d9383f78ecb0a42eb3116f1b6d2cf64026e8379e`  
		Last Modified: Mon, 08 Dec 2025 23:37:05 GMT  
		Size: 4.2 MB (4151182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85dea9709c0cc91ccc09bd88070ff8e7835fb029e1b7a8155bc481c0fbbdb66c`  
		Last Modified: Mon, 08 Dec 2025 23:37:04 GMT  
		Size: 1.2 MB (1220045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9611d7e618917a835310540491b2678ffadea33010c69b1ddcd832955489247`  
		Last Modified: Mon, 08 Dec 2025 23:37:04 GMT  
		Size: 8.1 MB (8066549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1daccd900a30ea6898f46e44b15e600496fdad14b32d0bb0fe6bed91d6d61e2`  
		Last Modified: Mon, 08 Dec 2025 23:37:04 GMT  
		Size: 1.2 MB (1195030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b662385d8beb2e386e1f1af655e29a7d56f88f427c89a2b3a912bc4ea2d53018`  
		Last Modified: Mon, 08 Dec 2025 23:37:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bcb87a679d581d2d853ea9723fbc7890541a0d6d3975c6f347f666adc10986`  
		Last Modified: Mon, 08 Dec 2025 23:37:04 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03cb4fed6efdb343d33a2364aae30393eeaca2e758bcfb3eb381d444fbfe70c`  
		Last Modified: Mon, 08 Dec 2025 23:37:08 GMT  
		Size: 46.7 MB (46731915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4fef07a7dc16108668f5e6121daf67e47b175e749d3120d69295448d46aee2`  
		Last Modified: Mon, 08 Dec 2025 23:37:05 GMT  
		Size: 19.1 KB (19089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01031dfd17e68486829e7e61ca3f6ad866f2d2492d54e9be17117da5f9af45c`  
		Last Modified: Mon, 08 Dec 2025 23:37:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558a45ca73b9bea90fe7e5609e9f5226b9e9478687d1952552307b0ffe43b699`  
		Last Modified: Mon, 08 Dec 2025 23:37:04 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046d2edc9290b89105b551dfe2031c473305edbf7f87f51f1d3fccd4b9546fb9`  
		Last Modified: Mon, 08 Dec 2025 23:37:04 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:1a4d13b92ce369e7d75989646538514d770d8c72c610d5ba0e2c71c397d0d948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5368792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f5928ad82b1970196bce2eff89538bbace03c7c6223d79ae017d55bb25aa3ca`

```dockerfile
```

-	Layers:
	-	`sha256:9f3f3512afda363794708c3793aa8a57ec31e4729752570dd75695477da0c539`  
		Last Modified: Tue, 09 Dec 2025 03:12:48 GMT  
		Size: 5.3 MB (5317006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed7ce6d5c71dc4d730b2745951d8848d64cb7f510a584a17d0ad462661233c86`  
		Last Modified: Tue, 09 Dec 2025 03:12:49 GMT  
		Size: 51.8 KB (51786 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:1123f7b8610b4c38c71e31f91859b623aac0e0c7b0d0b0bdd29019556a6615e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83276901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea12d7d90b7d1564a4ad078ba70f4f80f2954e9100e916b7ce0eff86a0a809a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:37:28 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 08 Dec 2025 23:37:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:37:43 GMT
ENV GOSU_VERSION=1.19
# Mon, 08 Dec 2025 23:37:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Dec 2025 23:37:49 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 08 Dec 2025 23:37:49 GMT
ENV LANG=en_US.utf8
# Mon, 08 Dec 2025 23:37:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:37:53 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Dec 2025 23:37:53 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:37:53 GMT
ENV PG_MAJOR=18
# Mon, 08 Dec 2025 23:37:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 08 Dec 2025 23:37:53 GMT
ENV PG_VERSION=18.1-1.pgdg12+2
# Mon, 08 Dec 2025 23:49:49 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 08 Dec 2025 23:49:49 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 08 Dec 2025 23:49:49 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 08 Dec 2025 23:49:49 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 08 Dec 2025 23:49:49 GMT
VOLUME [/var/lib/postgresql]
# Mon, 08 Dec 2025 23:49:49 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:49:50 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 08 Dec 2025 23:49:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:49:50 GMT
STOPSIGNAL SIGINT
# Mon, 08 Dec 2025 23:49:50 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 08 Dec 2025 23:49:50 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e12d446114182318769a6ca4adfc14d21fbb73f898de1d765662812d9f21c3a6`  
		Last Modified: Mon, 08 Dec 2025 22:16:03 GMT  
		Size: 23.9 MB (23934020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e916e1e2b574d48fe4d17f2f55f051c3988982922f58e684856670a96f50b769`  
		Last Modified: Mon, 08 Dec 2025 23:50:24 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75dab41cf845ddd0bd6e2c34218d17e76608688c0ced571bd269218c398e0ba`  
		Last Modified: Mon, 08 Dec 2025 23:50:24 GMT  
		Size: 3.7 MB (3742630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa83cd5fe8e42a34ce0c73df78aec82f551ec252065b519337d9dd19215072fe`  
		Last Modified: Mon, 08 Dec 2025 23:50:24 GMT  
		Size: 1.2 MB (1215981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef887ac3389d563e6a40761a6728cfb36b37817d3626e896ad4e10d8d112a7`  
		Last Modified: Mon, 08 Dec 2025 23:50:25 GMT  
		Size: 8.1 MB (8066389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2abc2551a12c2667538fc5875c67271ddcfe2dec7443e9900cf522541bea67`  
		Last Modified: Mon, 08 Dec 2025 23:50:24 GMT  
		Size: 1.1 MB (1067258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a4d39907f8def56f25bb21bb52ae2d36a8e01c66adf27ff82ee957671f18e9`  
		Last Modified: Mon, 08 Dec 2025 23:50:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d205946325bda99bed307f89b84c0093bd90eea13899ba4707bc2716a4870634`  
		Last Modified: Mon, 08 Dec 2025 23:50:24 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2577fc68213f145c7fc2a2e6a159f7d6d01dd157407908c1a06a9f7698b0750a`  
		Last Modified: Mon, 08 Dec 2025 23:50:30 GMT  
		Size: 45.2 MB (45220967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801e3242211ca357abffa4cd49b35a0f5b8a86e965121eb50a4409592c8f8dde`  
		Last Modified: Mon, 08 Dec 2025 23:50:24 GMT  
		Size: 19.1 KB (19086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9888fad3051e20567bbe687ce20028758adeb0bfab5c57a96a8891248ecd88`  
		Last Modified: Mon, 08 Dec 2025 23:50:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6473df2fce0b8d78222d231f1c5cf770a2ca2f9592c94a73ab575b1c63c20b54`  
		Last Modified: Mon, 08 Dec 2025 23:50:25 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e0043e0793ca858f9bb512653f19e0364b571d780ad807371a09306a1c8a45`  
		Last Modified: Mon, 08 Dec 2025 23:50:24 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:b399f8479f48476f122eb8daf1380da224523c5f68b087fae4cf16e15c412c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5368042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b775d5336b4f58038be454e430f222c44de067482c82915abb343d4c48da2efa`

```dockerfile
```

-	Layers:
	-	`sha256:ef13ba905c0250fbc7d55ea11bbd7d21a6bcccaa98b72b419fd827954a25d33a`  
		Last Modified: Tue, 09 Dec 2025 03:12:54 GMT  
		Size: 5.3 MB (5316257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96f4ee9d638d19410dcc795e7fc1fc3011b75b86807a9a2594c175f83d8143a4`  
		Last Modified: Tue, 09 Dec 2025 03:12:55 GMT  
		Size: 51.8 KB (51785 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:687c761587322d8c68a1baad706a5dab88305685f2c3fa871c3e08d78b93f319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.0 MB (155019202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00b1675dfbb063fad8b89487c9be8e4b6ac1fcd2669c03a991d29847634cba60`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:05:40 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 08 Dec 2025 23:05:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:05:51 GMT
ENV GOSU_VERSION=1.19
# Mon, 08 Dec 2025 23:05:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Dec 2025 23:05:56 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 08 Dec 2025 23:05:56 GMT
ENV LANG=en_US.utf8
# Mon, 08 Dec 2025 23:05:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:06:00 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Dec 2025 23:06:00 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:06:00 GMT
ENV PG_MAJOR=18
# Mon, 08 Dec 2025 23:06:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 08 Dec 2025 23:06:00 GMT
ENV PG_VERSION=18.1-1.pgdg12+2
# Mon, 08 Dec 2025 23:06:17 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 08 Dec 2025 23:06:18 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 08 Dec 2025 23:06:18 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 08 Dec 2025 23:06:18 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 08 Dec 2025 23:06:18 GMT
VOLUME [/var/lib/postgresql]
# Mon, 08 Dec 2025 23:06:18 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:06:18 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 08 Dec 2025 23:06:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:06:18 GMT
STOPSIGNAL SIGINT
# Mon, 08 Dec 2025 23:06:18 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 08 Dec 2025 23:06:18 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dec8597fc9a51d1e0f57053f625036bb37587dd9ac76f2e34b0c12df27e86cf`  
		Last Modified: Mon, 08 Dec 2025 23:06:47 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435f1ce1604d15b90b53ff47f4a2665ae9abb1476f0bcf7a3c6766d9596412d3`  
		Last Modified: Mon, 08 Dec 2025 23:06:47 GMT  
		Size: 4.5 MB (4519820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c50393527466be14d52e45ebe266aa6bc1e3f30d943fd3106873d0353d185d0`  
		Last Modified: Mon, 08 Dec 2025 23:06:47 GMT  
		Size: 1.2 MB (1203227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05c91f4b5ea08814806fd69fe98a01b55bc45da92f708be31f64b7af9ae7fc5`  
		Last Modified: Mon, 08 Dec 2025 23:06:48 GMT  
		Size: 8.1 MB (8066459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a326b33c168a1ae6f8374244df889425ff91f68fadcad1ebc5411c5615258908`  
		Last Modified: Mon, 08 Dec 2025 23:06:47 GMT  
		Size: 1.1 MB (1108957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8919aaa3475822f0fabda9d5bceb1d2732596d0d4e4444d850983f81713317`  
		Last Modified: Mon, 08 Dec 2025 23:06:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8146abf1dff1895aa088e437616e4b4e16f7d3dc04bdf9372982f10732b4ae0c`  
		Last Modified: Mon, 08 Dec 2025 23:06:47 GMT  
		Size: 3.1 KB (3138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfb9c3db61f2b78f31097e4a7ca6a754847124c7f78186ae925992cd271f281`  
		Last Modified: Mon, 08 Dec 2025 23:06:58 GMT  
		Size: 112.0 MB (111988862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8eb2cf7a2dd49363f4b380f7706497717d09f25e22f698efedd3da2c146d9e`  
		Last Modified: Mon, 08 Dec 2025 23:06:47 GMT  
		Size: 19.1 KB (19080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c6fdfe850f648d50f0200086b55537b3d57c67c0cf9a00fbbb3dccb3da8389`  
		Last Modified: Mon, 08 Dec 2025 23:06:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fad3e9ec6e0a2d34e03823513854f054b10dd37aa33e3258d1db7f2d38497ce`  
		Last Modified: Mon, 08 Dec 2025 23:06:47 GMT  
		Size: 5.8 KB (5835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2d457458a52d3c6f2830172e8a5c014748a4184058dbdf081d6f00a78b3b09`  
		Last Modified: Mon, 08 Dec 2025 23:06:47 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:4c257fcda73bad68d44d479a6b9cc5b0ae120ddfe56eef497b26377a16f374c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6214644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6af49941df207e1c3c961807baa4712cfea97c7da7cfbd3b0e1ca20e8b22dd`

```dockerfile
```

-	Layers:
	-	`sha256:186a0afccb23f73b7649d76d33723ae521e10b0c4f2fcb1350639c4f601ae832`  
		Last Modified: Tue, 09 Dec 2025 00:11:18 GMT  
		Size: 6.2 MB (6162812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba9d34935ef72f36df85843aa44ba1cc5900fa61eeffb407c201abeca1638efa`  
		Last Modified: Tue, 09 Dec 2025 00:11:19 GMT  
		Size: 51.8 KB (51832 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:83c233e45ed503ee9d8ba0987ca7e52660755eb531eec6b5e85d85ec487fe858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.9 MB (93933229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:602a01a215968470d1e86d0ec27367418e9ccd409789b90dbf3b362760f05782`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:01:04 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 08 Dec 2025 23:01:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:01:16 GMT
ENV GOSU_VERSION=1.19
# Mon, 08 Dec 2025 23:01:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Dec 2025 23:01:21 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 08 Dec 2025 23:01:21 GMT
ENV LANG=en_US.utf8
# Mon, 08 Dec 2025 23:01:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:01:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Dec 2025 23:01:25 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:01:25 GMT
ENV PG_MAJOR=18
# Mon, 08 Dec 2025 23:01:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 08 Dec 2025 23:01:25 GMT
ENV PG_VERSION=18.1-1.pgdg12+2
# Mon, 08 Dec 2025 23:10:35 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 08 Dec 2025 23:10:35 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 08 Dec 2025 23:10:35 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 08 Dec 2025 23:10:35 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 08 Dec 2025 23:10:35 GMT
VOLUME [/var/lib/postgresql]
# Mon, 08 Dec 2025 23:10:36 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:10:36 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 08 Dec 2025 23:10:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:10:36 GMT
STOPSIGNAL SIGINT
# Mon, 08 Dec 2025 23:10:36 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 08 Dec 2025 23:10:36 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e28a7f622a043206041afc8ed0d2b3d1b9bbffe3b724b994051e9d6dbc2f8a1e`  
		Last Modified: Mon, 08 Dec 2025 22:16:30 GMT  
		Size: 29.2 MB (29209729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d622cee000e047efbeaed171605089ca3dedda266e01d3a6ea900a6d76da076`  
		Last Modified: Mon, 08 Dec 2025 23:10:58 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d20e759901ca8fb1cd9da28f1997025d68b2b6370b575111266b4d7c2c134e`  
		Last Modified: Mon, 08 Dec 2025 23:10:59 GMT  
		Size: 5.0 MB (4965358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f7795136696a7c8db81eac64a984cbc9e73a6b1b8c39d1537d63205e5a239e`  
		Last Modified: Mon, 08 Dec 2025 23:10:59 GMT  
		Size: 1.2 MB (1218620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ded47cff083f7c5cbd1fb9a7636fad7e4e28baf3005154be67c9cf7fa07b22a`  
		Last Modified: Mon, 08 Dec 2025 23:11:04 GMT  
		Size: 8.1 MB (8066441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f72bcbf412bc643bfb77840aa13916522cc948e429f008de4c0d861cfcb81d`  
		Last Modified: Mon, 08 Dec 2025 23:10:59 GMT  
		Size: 1.1 MB (1137420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404c42669808730763ab5a5120d536c6b71afb7a9ea1b3be6e05a30349bc559e`  
		Last Modified: Mon, 08 Dec 2025 23:10:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8492c4c64b08b264e7b845e6ab00ea1dc0279e9db3b1a746020058c5061748ec`  
		Last Modified: Mon, 08 Dec 2025 23:10:58 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c777e8addc44fe4da825c5982feff312e17332ab6d43d3873ba5a630ad6e60e`  
		Last Modified: Mon, 08 Dec 2025 23:11:02 GMT  
		Size: 49.3 MB (49306012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f4df1357ef7537c1062bacb73121db57d0335b16e932319a7d7d958f9900f2`  
		Last Modified: Mon, 08 Dec 2025 23:10:58 GMT  
		Size: 19.1 KB (19082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1040adf92d3e5d032cfda37430da75f1d721efdbc04bb6cff0dda3273bae066`  
		Last Modified: Mon, 08 Dec 2025 23:10:58 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa9307bd4c027c91dc600c014b30f6fdf20f12673e17d23010cb0fb0fe199ea`  
		Last Modified: Mon, 08 Dec 2025 23:10:58 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c156efcec756ee90acccb05ac7ac233a8e0ac6aa802af95853f878214ad39a`  
		Last Modified: Mon, 08 Dec 2025 23:10:58 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:ccdd0839de6fb93d0c939fb2ab4c9f613f464c268795ca66e820e6ebe4a53797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5363110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f9acf53c433dfe43bd2ce17c473819141dfa44769c740a8bdf295e2809cf03c`

```dockerfile
```

-	Layers:
	-	`sha256:e71e4bf6850b2792ed9b4066b062842516f8a2abb0595db05e02ab0975ceb1b0`  
		Last Modified: Tue, 09 Dec 2025 03:13:04 GMT  
		Size: 5.3 MB (5311572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4ab3490b6e07d58bdca1827582bb5eab2fdeac8464c36d7e074c3223e0c734d`  
		Last Modified: Tue, 09 Dec 2025 03:13:05 GMT  
		Size: 51.5 KB (51538 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:d4fb73627a10aecb5f01d6f9d59d919ddd8c8e99e654c33847d6cd5b43793451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155915442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd416d7e4d2210202d89a13d02fdcb06d4fe7ddd955f20a7a3cde6f9009d9e34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 08:35:18 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 09 Dec 2025 08:35:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 08:36:23 GMT
ENV GOSU_VERSION=1.19
# Tue, 09 Dec 2025 08:36:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 09 Dec 2025 08:36:48 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 09 Dec 2025 08:36:48 GMT
ENV LANG=en_US.utf8
# Tue, 09 Dec 2025 08:37:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 08:37:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 09 Dec 2025 08:37:09 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 09 Dec 2025 08:37:09 GMT
ENV PG_MAJOR=18
# Tue, 09 Dec 2025 08:37:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 09 Dec 2025 08:37:09 GMT
ENV PG_VERSION=18.1-1.pgdg12+2
# Tue, 09 Dec 2025 09:48:13 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 09 Dec 2025 09:48:15 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 09 Dec 2025 09:48:17 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 09 Dec 2025 09:48:17 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 09 Dec 2025 09:48:17 GMT
VOLUME [/var/lib/postgresql]
# Tue, 09 Dec 2025 09:48:18 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 09:48:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 09 Dec 2025 09:48:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 09:48:20 GMT
STOPSIGNAL SIGINT
# Tue, 09 Dec 2025 09:48:20 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 09 Dec 2025 09:48:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b2b054f3a77e8800c8f5fad5ed6594164acd9d6bbb1409af308aa485c7352cac`  
		Last Modified: Mon, 08 Dec 2025 22:15:08 GMT  
		Size: 28.5 MB (28513802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d47dc8acc85e561a2b57f777018cb1cea2c388e433fae54bb69a230e01e7bf6`  
		Last Modified: Tue, 09 Dec 2025 09:50:43 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded2023525854da28133834b4d009a7b2461ff6da6a300aa50ca4e83bdc07201`  
		Last Modified: Tue, 09 Dec 2025 09:50:43 GMT  
		Size: 4.5 MB (4475494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fdccfe6df3d4b77476b8e6b837791063e36a5343f2741e514f74019e786b0da`  
		Last Modified: Tue, 09 Dec 2025 09:50:43 GMT  
		Size: 1.2 MB (1159212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae81cada0dbdd36e2f3ce856568dd67817b9419e45715e907952c70b153112c2`  
		Last Modified: Tue, 09 Dec 2025 09:50:43 GMT  
		Size: 8.1 MB (8066677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f610dc6ee7fcf349dc925fcb88038f9c027d70deb2c0048dfcef02f4d0300fbe`  
		Last Modified: Tue, 09 Dec 2025 09:50:43 GMT  
		Size: 1.2 MB (1182943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17a35b4a2a9c8c58153919fc2323fe2e2f2554ab27b544e125279494971f11d`  
		Last Modified: Tue, 09 Dec 2025 09:50:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696281a9f2a21529623361fa823bf678235f4122aa4a80f78e7068017da7b04c`  
		Last Modified: Tue, 09 Dec 2025 09:50:43 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41135fb148a1b374962ccce12faa433717170bf3c6b101aee48884d995ddc28f`  
		Last Modified: Tue, 09 Dec 2025 09:50:56 GMT  
		Size: 112.5 MB (112487643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeea97a7963c482622dad6763baf4f3e56f799a4e93e6508a535f97d785bd526`  
		Last Modified: Tue, 09 Dec 2025 09:50:43 GMT  
		Size: 19.1 KB (19088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79da0dc9ee9c6894ae9937cd97e3e6232085a6e3202c2220bdd209aa3ea51668`  
		Last Modified: Tue, 09 Dec 2025 09:50:43 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df57da1c823eb177b05212682302e8e1f18bdc2e5568adc5226a2ce6e9ff9299`  
		Last Modified: Tue, 09 Dec 2025 09:50:42 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e6d50016be942868fcbdf18fc7e4637091045f9811a0a1219e84bde24d71a3`  
		Last Modified: Tue, 09 Dec 2025 09:50:42 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:58b3735389bc72247942518c03776e6a550b84561957bc3843eee442eb097e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 KB (51462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cfa56de0aa43e7ab720d965d4b1e54a79d2935a980e1dbf86941f927903eed3`

```dockerfile
```

-	Layers:
	-	`sha256:c7e5fc1b701c463ecc3eda205828811a4eef0d43c187464cb9fb025b71c8d272`  
		Last Modified: Tue, 09 Dec 2025 12:09:00 GMT  
		Size: 51.5 KB (51462 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:7e8c363c2cf80b502df89bcb653a52e9c39413d966bbc8c322efa65103786389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.9 MB (169940057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1f560367916f30fc8b87247ecfcdc2a535932d3e98a665a1ffbc00b65dd6b3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 14:06:00 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 09 Dec 2025 14:06:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 14:06:26 GMT
ENV GOSU_VERSION=1.19
# Tue, 09 Dec 2025 14:06:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 09 Dec 2025 14:06:35 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 09 Dec 2025 14:06:35 GMT
ENV LANG=en_US.utf8
# Tue, 09 Dec 2025 14:06:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 14:06:41 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 09 Dec 2025 14:06:42 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 09 Dec 2025 14:06:42 GMT
ENV PG_MAJOR=18
# Tue, 09 Dec 2025 14:06:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 09 Dec 2025 14:06:42 GMT
ENV PG_VERSION=18.1-1.pgdg12+2
# Tue, 09 Dec 2025 14:07:23 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 09 Dec 2025 14:07:24 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 09 Dec 2025 14:07:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 09 Dec 2025 14:07:24 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 09 Dec 2025 14:07:24 GMT
VOLUME [/var/lib/postgresql]
# Tue, 09 Dec 2025 14:07:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 14:07:26 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 09 Dec 2025 14:07:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 14:07:26 GMT
STOPSIGNAL SIGINT
# Tue, 09 Dec 2025 14:07:26 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 09 Dec 2025 14:07:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:85c696326521b18996e4f030a7e27e2c57ad4956710f12ec3011da2c017e09ad`  
		Last Modified: Tue, 09 Dec 2025 09:15:52 GMT  
		Size: 32.1 MB (32068845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1242fbf5439ce7c9e3a77980c5b6e8bafeb45c33f149e270bb88cd9ec1f4c67e`  
		Last Modified: Tue, 09 Dec 2025 14:08:34 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c53d034afcbdd6f654d9fe1aaeef703493ef065a5ae05bcada4329686328a6`  
		Last Modified: Tue, 09 Dec 2025 14:08:34 GMT  
		Size: 5.4 MB (5368546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37ed3cd8227300b056f550d1b12ae037f670a1985bdb9c38a6a073d9a0857a9`  
		Last Modified: Tue, 09 Dec 2025 14:08:34 GMT  
		Size: 1.2 MB (1208196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ad4f65c6983b761b5dfcf5c82c2e08ea5816ce7aa74697b372208808f5d5ba`  
		Last Modified: Tue, 09 Dec 2025 14:08:34 GMT  
		Size: 8.1 MB (8066521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5abf9fe0835cfd8dd1de603db21ab5d44448a5232262d4dfd62b6a2e37ae0b81`  
		Last Modified: Tue, 09 Dec 2025 14:08:34 GMT  
		Size: 1.3 MB (1283631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0185ec9f7edb70a06ffe3de0ec8b66fde15435a482585c9f9c2878586b3bf22f`  
		Last Modified: Tue, 09 Dec 2025 14:08:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26d941e8b8881b4c06c365213698d3d5d5110a3d0a234b835f43b884d1b5b79`  
		Last Modified: Tue, 09 Dec 2025 14:08:34 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db33f5a8faa14951e350eca8fc15ef1cae1d33ec005c5b01898ea172c3036b21`  
		Last Modified: Tue, 09 Dec 2025 14:08:41 GMT  
		Size: 121.9 MB (121914651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a36180ccfa1526a1f469beb4a21b8169306a7da405ad78d15acd437c230d69`  
		Last Modified: Tue, 09 Dec 2025 14:08:34 GMT  
		Size: 19.1 KB (19089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723a5b06d2f9114e21d395a55d641a90a1ba5ae785f311382a4c0984871e70cd`  
		Last Modified: Tue, 09 Dec 2025 14:08:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede2bc07afbc9a042e42695743f9f6bd5b55dff94edde38214924c040419e7c4`  
		Last Modified: Tue, 09 Dec 2025 14:08:34 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c972516742ca9d2d5eb82d46b74b8980c89c79d139a809e95c40795dfe8fadec`  
		Last Modified: Tue, 09 Dec 2025 14:08:35 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:24e5ba627e635036a372cbc76ef436e66b5612a88a82e04e07fdbba05e369938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6215520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc140b703e07d6a1b3fb111d54bd8a584bed85631c70d2f41453ae2e550c53c`

```dockerfile
```

-	Layers:
	-	`sha256:be939be38e318d24ad166af8a3abc25c8b7f30aec40178c06badc65ca73954c8`  
		Last Modified: Tue, 09 Dec 2025 18:09:34 GMT  
		Size: 6.2 MB (6163872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e150ae5703a125a84f1e0809c6334f83d55e79834cf24dc592f852cf66aeee7`  
		Last Modified: Tue, 09 Dec 2025 18:09:35 GMT  
		Size: 51.6 KB (51648 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:f3a56ec8f820cf05228086073c251fab2325b9f048fc5850125104e650273d17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.4 MB (166369356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a20ecf632bda50cc29fd5f190a0c19b7f72777d8cb11fdb76a8d52866de60e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:37:48 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 08 Dec 2025 23:37:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:38:00 GMT
ENV GOSU_VERSION=1.19
# Mon, 08 Dec 2025 23:38:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Dec 2025 23:38:04 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 08 Dec 2025 23:38:04 GMT
ENV LANG=en_US.utf8
# Mon, 08 Dec 2025 23:38:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:38:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Dec 2025 23:38:08 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:38:08 GMT
ENV PG_MAJOR=18
# Mon, 08 Dec 2025 23:38:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 08 Dec 2025 23:38:08 GMT
ENV PG_VERSION=18.1-1.pgdg12+2
# Mon, 08 Dec 2025 23:49:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 08 Dec 2025 23:49:59 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 08 Dec 2025 23:49:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 08 Dec 2025 23:49:59 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 08 Dec 2025 23:49:59 GMT
VOLUME [/var/lib/postgresql]
# Mon, 08 Dec 2025 23:49:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:49:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 08 Dec 2025 23:49:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:49:59 GMT
STOPSIGNAL SIGINT
# Mon, 08 Dec 2025 23:49:59 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 08 Dec 2025 23:49:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:00a29f44cb5b31bbcf043ec5426ee1c018bb26435350712cb5e48d56c6d95792`  
		Last Modified: Mon, 08 Dec 2025 22:15:04 GMT  
		Size: 26.9 MB (26884429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725cf3e4bfa36eb2b8eddb47675bb249f0ca3eefe6068b41e37fa647a565ca78`  
		Last Modified: Mon, 08 Dec 2025 23:51:45 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899e4551cb8c25e22e5439deaa5f9a2bfebb42c27d9dfe13b32e42e03fa534a6`  
		Last Modified: Mon, 08 Dec 2025 23:51:46 GMT  
		Size: 4.4 MB (4391344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96440795729f516ea449176989238797f5d4bbd3ae8757a77a04ba941d036e72`  
		Last Modified: Mon, 08 Dec 2025 23:51:45 GMT  
		Size: 1.2 MB (1222829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11b91c535a77489ba0daa9b0dedc7794397bb2a6e2e99b524e50faab62e117d`  
		Last Modified: Mon, 08 Dec 2025 23:51:46 GMT  
		Size: 8.1 MB (8120716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e54f30d6e3687a8c5c94bb3d140fbff52ef5d03601cc11bc041fd6646b48d9`  
		Last Modified: Mon, 08 Dec 2025 23:51:46 GMT  
		Size: 1.1 MB (1097045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022fc848c95d0b9b39608c17b09d6af19633141f1d64c5be5afb6b0a2d5436b6`  
		Last Modified: Mon, 08 Dec 2025 23:51:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7bec706c26a025fb818d05790ea0e361eabcad789c5b1a0fdb616a7e33d8f29`  
		Last Modified: Mon, 08 Dec 2025 23:51:46 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4355d4b39dd1163e4b223efeb733b3267acdb5c497d72616ef1c22218d807db`  
		Last Modified: Tue, 09 Dec 2025 00:20:25 GMT  
		Size: 124.6 MB (124623337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12998a22c35c7b1b201ce201d663a421d4ca9a3571f546cb2b790e8a44bcc898`  
		Last Modified: Tue, 09 Dec 2025 00:20:17 GMT  
		Size: 19.1 KB (19087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7993a3935a415a0e393014731a8fbc0758e4de5f13a973aad9e83f77550b9a61`  
		Last Modified: Tue, 09 Dec 2025 00:20:17 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ff010e22959b6827d28d3bf9f0d1c6c7f7becd9840a5ce9dc2a028542b58ec`  
		Last Modified: Tue, 09 Dec 2025 00:20:17 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f07187a35ad81485b2dda444161076057f9b02ee5be0ad503c58f2bcb3deb6`  
		Last Modified: Tue, 09 Dec 2025 00:20:17 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:eab783024859dffbde0b894c03ba2dc9d2687fed536348bb58457688bfdef739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6222735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c01d892b689292624ecdfec37d8d40d5fddff91d26f3fe7e358c860a228c9f8`

```dockerfile
```

-	Layers:
	-	`sha256:aaddd1e3a3a6d0154f63971f8bd74427c62c28b261b35eccc4a4858396b91efb`  
		Last Modified: Tue, 09 Dec 2025 04:58:41 GMT  
		Size: 6.2 MB (6171145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46c14be7548c819b6809c8442beb54b07add33677abbbc0b312c9af1b80a797a`  
		Last Modified: Tue, 09 Dec 2025 04:58:41 GMT  
		Size: 51.6 KB (51590 bytes)  
		MIME: application/vnd.in-toto+json
