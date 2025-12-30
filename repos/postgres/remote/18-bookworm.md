## `postgres:18-bookworm`

```console
$ docker pull postgres@sha256:97835bf538e4f7e0697d38a6d09463e7b52bee3eec236417d41e3e865425dd84
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
$ docker pull postgres@sha256:cdcd213fb7ebe21142413c3fd8d507235ad62d9ef18c4f3f6005369ce483301a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157057692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f026528ac214d0fcbda2b6cf76b8f7788b8a1263d50b4490dc08af3cc3199164`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:36:32 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 29 Dec 2025 23:36:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:36:43 GMT
ENV GOSU_VERSION=1.19
# Mon, 29 Dec 2025 23:36:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 29 Dec 2025 23:36:47 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 29 Dec 2025 23:36:47 GMT
ENV LANG=en_US.utf8
# Mon, 29 Dec 2025 23:36:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:36:50 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 29 Dec 2025 23:36:51 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 29 Dec 2025 23:36:51 GMT
ENV PG_MAJOR=18
# Mon, 29 Dec 2025 23:36:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 29 Dec 2025 23:36:51 GMT
ENV PG_VERSION=18.1-1.pgdg12+2
# Mon, 29 Dec 2025 23:37:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 29 Dec 2025 23:37:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 29 Dec 2025 23:37:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 29 Dec 2025 23:37:06 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 29 Dec 2025 23:37:06 GMT
VOLUME [/var/lib/postgresql]
# Mon, 29 Dec 2025 23:37:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:37:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 29 Dec 2025 23:37:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:37:06 GMT
STOPSIGNAL SIGINT
# Mon, 29 Dec 2025 23:37:06 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 29 Dec 2025 23:37:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10149150dbe6967cd17afca76d79eb1f1678578d42a3001240462eed3f33f1d1`  
		Last Modified: Mon, 29 Dec 2025 23:37:36 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a050f3666f8757368daf8c22622610f81961003dc9dc69023c4db6f15b1271`  
		Last Modified: Mon, 29 Dec 2025 23:37:36 GMT  
		Size: 4.5 MB (4534095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d9454cc93c9fdd1e5fd6c18b85d286e3d74095cd275a066b72cabda3cc3aece`  
		Last Modified: Mon, 29 Dec 2025 23:37:36 GMT  
		Size: 1.2 MB (1249537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fca0461b6cc832aa76b743d3595736b5d85ef3127358839295ca08fa9380cc`  
		Last Modified: Mon, 29 Dec 2025 23:37:37 GMT  
		Size: 8.1 MB (8066410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ba37c95763a97c450aa15a159a817dcefb69c3e397311f4add6fcb350eb88a`  
		Last Modified: Mon, 29 Dec 2025 23:37:36 GMT  
		Size: 1.2 MB (1196403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ebe9e4d731335a08789acd3f44ed153efbbd580f297c946331fb2f1c99da99`  
		Last Modified: Mon, 29 Dec 2025 23:37:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914b9e5e834619c94614f67a53771146798c3cdf3f9c470b1e4116031afa80b5`  
		Last Modified: Mon, 29 Dec 2025 23:37:36 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e43411118765746d95bc19ac9dbce438019f430a80263736caedf6d4aa65da2`  
		Last Modified: Mon, 29 Dec 2025 23:37:44 GMT  
		Size: 113.8 MB (113753155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e5900d8d77218fab99f5b67aa585efd7c22043d7b50269a6b47c55c80d6734`  
		Last Modified: Mon, 29 Dec 2025 23:37:36 GMT  
		Size: 19.1 KB (19087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e03d128b958301df192b871b3862fbf0af7c19c6707711517627ce8117de7a`  
		Last Modified: Mon, 29 Dec 2025 23:37:36 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762073fe227ed0f0dbb6ee3c8e0b6d9c7ef1eb2fec25672b63ccb3d681692421`  
		Last Modified: Mon, 29 Dec 2025 23:37:35 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6404f071ad7b3bc265dab1aa32c4617040cf7423c5a406edadb03420e7252243`  
		Last Modified: Mon, 29 Dec 2025 23:37:35 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:ad2f13eeae8adf239d7822ec62f4ab78a17e0cfd8a513754fa1b35bb3af42893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6208076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469c52281d5cfd2d8e659eece2785aabeabc983ec8341e6ceb31825f0f38cef0`

```dockerfile
```

-	Layers:
	-	`sha256:72405775d430eae8183ec0260cd0b454d87c492b47d8822f7a34d71d1fd7a2f8`  
		Last Modified: Tue, 30 Dec 2025 03:15:13 GMT  
		Size: 6.2 MB (6156487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9d4444d8d78b487e452de559d5d4c65baa1c5a1101f660b35bfaff1788ef170`  
		Last Modified: Tue, 30 Dec 2025 03:15:14 GMT  
		Size: 51.6 KB (51589 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:f00bd3c7ff5932258df8ae5865a88d2c8bf25a78163af5b807fc37a1375eda69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.2 MB (87152117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a24b0d00cab59541006fc8e9e9e88ca3a43583bfa6cea5f25bf15b9fa547f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:53:50 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 29 Dec 2025 23:53:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:54:07 GMT
ENV GOSU_VERSION=1.19
# Mon, 29 Dec 2025 23:54:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 29 Dec 2025 23:54:15 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 29 Dec 2025 23:54:15 GMT
ENV LANG=en_US.utf8
# Mon, 29 Dec 2025 23:54:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:54:21 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 29 Dec 2025 23:54:21 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 29 Dec 2025 23:54:21 GMT
ENV PG_MAJOR=18
# Mon, 29 Dec 2025 23:54:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 29 Dec 2025 23:54:21 GMT
ENV PG_VERSION=18.1-1.pgdg12+2
# Tue, 30 Dec 2025 00:06:46 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 30 Dec 2025 00:06:46 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Dec 2025 00:06:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Dec 2025 00:06:46 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 30 Dec 2025 00:06:46 GMT
VOLUME [/var/lib/postgresql]
# Tue, 30 Dec 2025 00:06:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 00:06:47 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Dec 2025 00:06:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Dec 2025 00:06:47 GMT
STOPSIGNAL SIGINT
# Tue, 30 Dec 2025 00:06:47 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Dec 2025 00:06:47 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:cdd01b66e4b6599d6f59fe75d883783e8ddfc67db8fda967c6ce250da575cc0b`  
		Last Modified: Mon, 29 Dec 2025 22:25:33 GMT  
		Size: 25.8 MB (25757576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20751ebf7b7ed4a5eef2bc2e8d2088488808e6d071f54ced9d9c187c8a3a98c`  
		Last Modified: Tue, 30 Dec 2025 00:07:08 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fad423f026b4cb74443d9b15bf832825d395a9c85020fa37995186d23886cc`  
		Last Modified: Tue, 30 Dec 2025 00:07:09 GMT  
		Size: 4.2 MB (4151215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc9020cb759108148339ea675faef6e80a7b719e481e3bbb6549afdb6293321`  
		Last Modified: Tue, 30 Dec 2025 00:07:09 GMT  
		Size: 1.2 MB (1220042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbbfab53dcc7209e1f28974656986edcbfb09c78394b59c7796e5a3459b676b`  
		Last Modified: Tue, 30 Dec 2025 00:07:09 GMT  
		Size: 8.1 MB (8066595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294bc00cb15c60853161ae9684e61ad40429fd8d4696c5b93b6f40fc84c87408`  
		Last Modified: Tue, 30 Dec 2025 00:07:09 GMT  
		Size: 1.2 MB (1195042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daba7583ac70f602d3fe4627ca3e3115d65f576e870612b778e8a9d8fd85f1ce`  
		Last Modified: Tue, 30 Dec 2025 00:07:09 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5304841265495ce67b048cbfb6edeebba91b5bb8d3a06045d93aafe4fabe1fa`  
		Last Modified: Tue, 30 Dec 2025 00:07:09 GMT  
		Size: 3.1 KB (3138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9706c4a5c31dfae04e24495f25f1ccad947d6b5a1094ee51e3047a16a722fbda`  
		Last Modified: Tue, 30 Dec 2025 00:07:12 GMT  
		Size: 46.7 MB (46731985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0209ee162af6f696b93f5340d36b7018b80f7c9eb9a58441b329c7be502acfe`  
		Last Modified: Tue, 30 Dec 2025 00:07:09 GMT  
		Size: 19.1 KB (19088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9898631e1c3a724adb80058c9eb157126402de19da1024e2eb5b6df97859d74a`  
		Last Modified: Tue, 30 Dec 2025 00:07:09 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd16153cfdcd1fcfa23f86166f9f491496be637429f3177fb58d8bc56a7adbc`  
		Last Modified: Tue, 30 Dec 2025 00:07:09 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056c4dd32e5e51513543695c1f84cab6163c021a951d3884fedcf058e6c6e484`  
		Last Modified: Tue, 30 Dec 2025 00:07:09 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:e73fa05bd3bd3c2a26acba52ed5f01ab8b264bd44c2d60554ed30cb8ad48df18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5368793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:696d996f4bef9e979cee0dcf6219ad8f863bb3349be095cc7b1d842abf6e0a28`

```dockerfile
```

-	Layers:
	-	`sha256:9dea58df2914f7a6cae1f49433309ea725c9dfc7bd74483aa0f83216e1f3aea0`  
		Last Modified: Tue, 30 Dec 2025 03:15:20 GMT  
		Size: 5.3 MB (5317006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dacea509e877237fc25fec14a9df1a2ba4fe759b83be08bd638c5daa6b1fe55a`  
		Last Modified: Tue, 30 Dec 2025 03:15:21 GMT  
		Size: 51.8 KB (51787 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:1086ab02abcfb142f8e02a11ba0c49b8b1e6a4f741f32d88bc16eb7c7de94bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83276959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72692a9ee8acac69eb5b2dde1424f0be998bb2134c03a36d4209d44db57d69d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:55:35 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 29 Dec 2025 23:55:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:55:48 GMT
ENV GOSU_VERSION=1.19
# Mon, 29 Dec 2025 23:55:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 29 Dec 2025 23:55:54 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 29 Dec 2025 23:55:54 GMT
ENV LANG=en_US.utf8
# Mon, 29 Dec 2025 23:55:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:55:58 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 29 Dec 2025 23:55:59 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 29 Dec 2025 23:55:59 GMT
ENV PG_MAJOR=18
# Mon, 29 Dec 2025 23:55:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 29 Dec 2025 23:55:59 GMT
ENV PG_VERSION=18.1-1.pgdg12+2
# Tue, 30 Dec 2025 00:07:29 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 30 Dec 2025 00:07:29 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Dec 2025 00:07:29 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Dec 2025 00:07:29 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 30 Dec 2025 00:07:29 GMT
VOLUME [/var/lib/postgresql]
# Tue, 30 Dec 2025 00:07:29 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 00:07:29 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Dec 2025 00:07:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Dec 2025 00:07:29 GMT
STOPSIGNAL SIGINT
# Tue, 30 Dec 2025 00:07:29 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Dec 2025 00:07:29 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3733e79b87ec6af3c60809fa9882f5d220b1e1fc2459b7d6a5b3167dc8eb7155`  
		Last Modified: Mon, 29 Dec 2025 22:25:04 GMT  
		Size: 23.9 MB (23934053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8655732384451e5d3d678c604c55a39a258694485244484c7f8fe7d40d51da98`  
		Last Modified: Tue, 30 Dec 2025 00:07:51 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1517117205dbf824afb4cd8ae5ee800885fa6527a7ae3ca9848411d6d5d5363`  
		Last Modified: Tue, 30 Dec 2025 00:07:59 GMT  
		Size: 3.7 MB (3742697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37e7d4c7e36a5a31be4919155bfcdc7d6ec3e98e44eb75ae0c0e54bd9209da6`  
		Last Modified: Tue, 30 Dec 2025 00:07:51 GMT  
		Size: 1.2 MB (1215970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dbcfef8a42f7dbf0927ec29573b40e551643a17862f69f2f091caf72cb24b42`  
		Last Modified: Tue, 30 Dec 2025 00:07:52 GMT  
		Size: 8.1 MB (8066386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d189d7c11ca3a4ffd40a159a099493b1af33b4b522d5e71850895e6204e31b`  
		Last Modified: Tue, 30 Dec 2025 00:07:52 GMT  
		Size: 1.1 MB (1067214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34aad41fcbb9ebee881d9dabe1795403ad884fda9b5e4d8220f1f5ecaf1a9cc0`  
		Last Modified: Tue, 30 Dec 2025 00:07:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49fb1339aff2600eb00ff78cf6fad9d9cf97cdc984aa5340eefb94cc84116284`  
		Last Modified: Tue, 30 Dec 2025 00:07:51 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb18ed214ada595dbecb18f21be1164f5718842621cf5fb8f2722a5b44abb2a`  
		Last Modified: Tue, 30 Dec 2025 00:07:55 GMT  
		Size: 45.2 MB (45220967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e370049beec2c352f9044c997d5292a27b88a8eda935ea8db345748667b71d24`  
		Last Modified: Tue, 30 Dec 2025 00:07:51 GMT  
		Size: 19.1 KB (19092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfb8db26d21b38daf832b0fb5e0d09f328b64b3cf255bc19bfe9ce718b9ce7c`  
		Last Modified: Tue, 30 Dec 2025 00:07:51 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c355e5947cfba367b0d17aced0c6754f3b8b96e05d1ae0b2d0cb1cd1e1a26e35`  
		Last Modified: Tue, 30 Dec 2025 00:07:51 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a5ce08bb9238676212867742c6035699c3da35b487109f8e50b056a7b0cf69`  
		Last Modified: Tue, 30 Dec 2025 00:07:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:00b18d0e81b1ccdb6fae51c774b9aad3ec3158d15f693823c600fc250374ee1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5368042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9b442b9f2cc2f746d3fc927568234e565167cf5b96561bd30506a26cd965a38`

```dockerfile
```

-	Layers:
	-	`sha256:72e979cfb25484e3ce858b395586b83d4a71bb244503e65a695496bb65613101`  
		Last Modified: Tue, 30 Dec 2025 03:15:26 GMT  
		Size: 5.3 MB (5316257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f21e118b8019aab1b79eafd29f18afee387b65b026987e050c27ed97bf535307`  
		Last Modified: Tue, 30 Dec 2025 03:15:26 GMT  
		Size: 51.8 KB (51785 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:962ff8a5fe8af40072324f70621c11864caa2e35f1f9a9ebf58a087efd4c36e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.0 MB (155018856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c636744e7853c467915a0dd1decd38c2c99629e0b6fe278fc3ca10f5bfeb0108`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:40:03 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 29 Dec 2025 23:40:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:40:15 GMT
ENV GOSU_VERSION=1.19
# Mon, 29 Dec 2025 23:40:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 29 Dec 2025 23:40:20 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 29 Dec 2025 23:40:20 GMT
ENV LANG=en_US.utf8
# Mon, 29 Dec 2025 23:40:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:40:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 29 Dec 2025 23:40:24 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 29 Dec 2025 23:40:24 GMT
ENV PG_MAJOR=18
# Mon, 29 Dec 2025 23:40:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 29 Dec 2025 23:40:24 GMT
ENV PG_VERSION=18.1-1.pgdg12+2
# Mon, 29 Dec 2025 23:40:39 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 29 Dec 2025 23:40:40 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 29 Dec 2025 23:40:40 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 29 Dec 2025 23:40:40 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 29 Dec 2025 23:40:40 GMT
VOLUME [/var/lib/postgresql]
# Mon, 29 Dec 2025 23:40:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:40:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 29 Dec 2025 23:40:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:40:40 GMT
STOPSIGNAL SIGINT
# Mon, 29 Dec 2025 23:40:40 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 29 Dec 2025 23:40:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62377989d063f84ac55cf5dad98fdee7c92e01bca07e1aabcef2970cb40bd141`  
		Last Modified: Mon, 29 Dec 2025 23:41:09 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4359e1d91567262308a6800c36afbd9c69063a7f83e6de0cb4338a2572b851c`  
		Last Modified: Mon, 29 Dec 2025 23:41:09 GMT  
		Size: 4.5 MB (4519846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772cb4f02b7f81277cdf6b7ebec92cb2d6b8c7a01e09e12f4d2aff7d0c914d74`  
		Last Modified: Mon, 29 Dec 2025 23:41:09 GMT  
		Size: 1.2 MB (1203279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc0345bf019975e822c6cd74262b56d65504f63c8a4f44e5a19e952629d520b`  
		Last Modified: Mon, 29 Dec 2025 23:41:10 GMT  
		Size: 8.1 MB (8066440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c1b7a04cfa8409ff0d76856d7eace5d7b0d4721d1d7c79b77dc162990e20d7c`  
		Last Modified: Mon, 29 Dec 2025 23:41:09 GMT  
		Size: 1.1 MB (1108944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a8bbc0027807db0d16eb799bd970837c1385737e8b92de3006caeb05ba669b`  
		Last Modified: Mon, 29 Dec 2025 23:41:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0835a052023d191ddc48f435f8ea4037231e5d6691587c79b03c6fe0231780c6`  
		Last Modified: Mon, 29 Dec 2025 23:41:09 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5584087af830961aa4ce49fba929bb08d79dfd519663a9431a5096890d3ebce1`  
		Last Modified: Mon, 29 Dec 2025 23:41:19 GMT  
		Size: 112.0 MB (111988482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4004c14e5c4d9f81efa8b8bf8760016292d6a8afe72983491a2730baf5b6b56f`  
		Last Modified: Mon, 29 Dec 2025 23:41:09 GMT  
		Size: 19.1 KB (19083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4495582b0b94ee206b1d26271c9df4933985f7bc8b8e17d2b5798b6677a91ccf`  
		Last Modified: Mon, 29 Dec 2025 23:41:09 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf4c6420856e934eb10fd922186aadf2e36fab6f5a8cf0c5c2ac5ce98aadf2b`  
		Last Modified: Mon, 29 Dec 2025 23:41:18 GMT  
		Size: 5.8 KB (5835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca2814103fc9e82e79a3f5b6d57ef85eaacea70fc06790bc4f8f9d1e9e77054`  
		Last Modified: Mon, 29 Dec 2025 23:41:09 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:a694a972d11dac0dd9639f16b4c61c49761c9b9bd13ad16f72eedd8df4539cf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6214643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4dfd11d4be8641e95864c9056ad265d5ed790cf54ffb94cfad57f2fadd085ad`

```dockerfile
```

-	Layers:
	-	`sha256:38a5908b8023b53cb421dae3e4a999d8f40550864c78fd18aa7d87dddd03e344`  
		Last Modified: Tue, 30 Dec 2025 03:15:32 GMT  
		Size: 6.2 MB (6162812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3579a531ec6e20017336ee32ade831aec837997f800e440df2b9ab87861e952a`  
		Last Modified: Tue, 30 Dec 2025 03:15:32 GMT  
		Size: 51.8 KB (51831 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:50eb2fb67c82ce144a3c231942e5942100eebab49986e2a71dd8ded73cedfe81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.9 MB (93932707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acccb319c4a97c1ff83c6838e656843a28487f008012517c29c6b5129932ee5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:32:33 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 29 Dec 2025 23:32:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:32:46 GMT
ENV GOSU_VERSION=1.19
# Mon, 29 Dec 2025 23:32:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 29 Dec 2025 23:32:50 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 29 Dec 2025 23:32:50 GMT
ENV LANG=en_US.utf8
# Mon, 29 Dec 2025 23:32:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:32:53 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 29 Dec 2025 23:32:54 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 29 Dec 2025 23:32:54 GMT
ENV PG_MAJOR=18
# Mon, 29 Dec 2025 23:32:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 29 Dec 2025 23:32:54 GMT
ENV PG_VERSION=18.1-1.pgdg12+2
# Mon, 29 Dec 2025 23:41:18 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 29 Dec 2025 23:41:18 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 29 Dec 2025 23:41:18 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 29 Dec 2025 23:41:18 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 29 Dec 2025 23:41:18 GMT
VOLUME [/var/lib/postgresql]
# Mon, 29 Dec 2025 23:41:18 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:41:18 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 29 Dec 2025 23:41:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:41:18 GMT
STOPSIGNAL SIGINT
# Mon, 29 Dec 2025 23:41:18 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 29 Dec 2025 23:41:18 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f67520a70f469d560f84fd587586b5b9a9f46691d2f4b10c88544b5d21f5fe06`  
		Last Modified: Mon, 29 Dec 2025 22:24:46 GMT  
		Size: 29.2 MB (29209773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae3dbf423f72c92d0aa4386c8b460e8ddae27df4cc8faa5f8dff8a6cf3ee621`  
		Last Modified: Mon, 29 Dec 2025 23:41:39 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076324618e8ee0dd8cd4c2b39a4ce1eed4255667a61befcb737135152bbdcf95`  
		Last Modified: Mon, 29 Dec 2025 23:41:40 GMT  
		Size: 5.0 MB (4965380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fc2f4de02cd8272f176320ba4ca8c1bd6f792b84fe5da3a30a0ed337bb74e4`  
		Last Modified: Mon, 29 Dec 2025 23:41:40 GMT  
		Size: 1.2 MB (1218648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64999465fa2d19f75b18e1eee4ec5d614f542fc45412c1b5326b248a047416f`  
		Last Modified: Mon, 29 Dec 2025 23:41:40 GMT  
		Size: 8.1 MB (8066418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb77a79ac03b15039a5b8ed8704f2a1dd1778106ea0d74b2c62389d54b15ae6`  
		Last Modified: Mon, 29 Dec 2025 23:41:40 GMT  
		Size: 1.1 MB (1137420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492bd62eb31a692129c0e229a6599d1af9633ede0425435998378cd975d59eaa`  
		Last Modified: Mon, 29 Dec 2025 23:41:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22706ee760e359a9d3b16bb2f0a56c22e60fdfd8ab8d73af861bc36f24b0bfbb`  
		Last Modified: Mon, 29 Dec 2025 23:41:39 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7329871e67ad61b32e04ed1f2270f599ceb611c858ea25c92757db8bab1ca95`  
		Last Modified: Mon, 29 Dec 2025 23:41:43 GMT  
		Size: 49.3 MB (49305408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c213664e87967d8e3726a1d4b6c64d05ae17515e47b19226148080d28834e685`  
		Last Modified: Mon, 29 Dec 2025 23:41:39 GMT  
		Size: 19.1 KB (19084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b2fd756711e252c32699aa3246fe77053d1e14acea36ae53e82ff65a176cc3`  
		Last Modified: Mon, 29 Dec 2025 23:41:38 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8372aaf813b5f22d657a421e87f4569b9cf2a3c97916c2a0227307a9770700c`  
		Last Modified: Mon, 29 Dec 2025 23:41:40 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee8e66ad5c32e78f1ed83c4af90547ecc206be4edad06d216ae5d260803ca2a`  
		Last Modified: Mon, 29 Dec 2025 23:41:39 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:e147ab7cf8bae457a7ad43c144e8b592b94d6e21216f32acbde53c8e1d9fa33e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5363110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5611d421250050892c9d9f1029517e74aa9583b32407e2747f85e259f65976`

```dockerfile
```

-	Layers:
	-	`sha256:df99a219a97f5232322eac5c1c60d2022bf75411b48e58d9c5bace873ac6ca12`  
		Last Modified: Tue, 30 Dec 2025 03:15:38 GMT  
		Size: 5.3 MB (5311572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5129b0e90e8ab3960a837ff4f17c63e398607a19041d5f1472a8fda8f6584b7`  
		Last Modified: Tue, 30 Dec 2025 03:15:39 GMT  
		Size: 51.5 KB (51538 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:670930d0a9e4bfd4f8a96f62f7e22d10a9e94780dced5e9f8ea9da14af97dd5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155916313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d17a622a8842c2e15a407a963b0f5b559fad53019b754aaa11fa57bb5f34431e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 05:16:51 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Dec 2025 05:17:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 05:17:57 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Dec 2025 05:17:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Dec 2025 05:18:22 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 30 Dec 2025 05:18:22 GMT
ENV LANG=en_US.utf8
# Tue, 30 Dec 2025 05:18:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 05:18:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Dec 2025 05:18:43 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 05:18:43 GMT
ENV PG_MAJOR=18
# Tue, 30 Dec 2025 05:18:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 30 Dec 2025 05:18:43 GMT
ENV PG_VERSION=18.1-1.pgdg12+2
# Tue, 30 Dec 2025 06:29:39 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 30 Dec 2025 06:29:41 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Dec 2025 06:29:42 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Dec 2025 06:29:42 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 30 Dec 2025 06:29:42 GMT
VOLUME [/var/lib/postgresql]
# Tue, 30 Dec 2025 06:29:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 06:29:45 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Dec 2025 06:29:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Dec 2025 06:29:45 GMT
STOPSIGNAL SIGINT
# Tue, 30 Dec 2025 06:29:45 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Dec 2025 06:29:45 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f479f5e9b924c5f7ef1d8b31a2c87cbd2a63c9fdc99e9e0c0cea7eae009e308c`  
		Last Modified: Mon, 29 Dec 2025 22:38:39 GMT  
		Size: 28.5 MB (28513809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca417b7ae950ff7970ad040b45abc24df944012e1756024d3f91656523cc30f8`  
		Last Modified: Tue, 30 Dec 2025 06:32:09 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8058603eaabaaed3c93fdfec7c2d4b77840d6fd5a151130f1c783e2de499479e`  
		Last Modified: Tue, 30 Dec 2025 06:32:09 GMT  
		Size: 4.5 MB (4475462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a676f9edcbcd2bb6defaca57cf7604e1ff4d96eb528e323ef74cd849bff4a90`  
		Last Modified: Tue, 30 Dec 2025 06:32:09 GMT  
		Size: 1.2 MB (1159183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f809eb30e7653bd1a9ce23c5ce36a429632d6088fa3f0348dd87900860b29e76`  
		Last Modified: Tue, 30 Dec 2025 06:32:09 GMT  
		Size: 8.1 MB (8066647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41385bcf55cc88174fc97e7d3019c5f94b8e8e5d4aa5c374766ad43452190273`  
		Last Modified: Tue, 30 Dec 2025 06:32:09 GMT  
		Size: 1.2 MB (1182926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a35a2d513dc5e6c316ef29fe04efa4c84517f5bf54fe460b95b551a22c3c0dc`  
		Last Modified: Tue, 30 Dec 2025 06:32:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:651c58be512fb2ee6b868cc910f9dbe2572916717b1affd127f4442c7a46a68f`  
		Last Modified: Tue, 30 Dec 2025 06:32:09 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4758d761e77766b8b14a2c2ffca316473bb64de22e230b98e82f1c25ff8d8b`  
		Last Modified: Tue, 30 Dec 2025 06:32:15 GMT  
		Size: 112.5 MB (112488613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe192ea16e2da06e57da1f36b2a5a8bd87e10786cd17f4d4031648c910e3189`  
		Last Modified: Tue, 30 Dec 2025 06:32:09 GMT  
		Size: 19.1 KB (19088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56a6aa65a7e89698a4bee2648f58b7872e66d3921dff7ae33a7b4a041c275eb`  
		Last Modified: Tue, 30 Dec 2025 06:32:09 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75179768a5e577fcf19d1a3b7808af19c59999cca6cd074b9575709068f2be4b`  
		Last Modified: Tue, 30 Dec 2025 06:32:09 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2268948a058355c6ed44ff90293de0f066cd05909a02516e1f9a2d26cb80fc6c`  
		Last Modified: Tue, 30 Dec 2025 06:32:09 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:027350c8739d2af5bdd91a177304605e4c288747b3b177680d5a3638a0be8ad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 KB (51461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77fe02a4e2d8c0d0e9c2c5acbcaf90b62d398688d9710eb293da9dfdb44b19c`

```dockerfile
```

-	Layers:
	-	`sha256:7b0a5f4b5d416868bba57637735c825737e850f79d11f5c78e73c9215393d194`  
		Last Modified: Tue, 30 Dec 2025 09:09:02 GMT  
		Size: 51.5 KB (51461 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:8e07e89cdb0a39c74a9a397902331dcfb823fff82cb410429b5873e5df8ffde5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.9 MB (169939893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:818e5bf20637d80f18107d55984cfdd2764912b8dcd69e3f16e84b56f24afebe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 03:02:46 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Dec 2025 03:02:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 03:03:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Dec 2025 03:03:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Dec 2025 03:03:22 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 30 Dec 2025 03:03:22 GMT
ENV LANG=en_US.utf8
# Tue, 30 Dec 2025 03:03:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 03:03:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Dec 2025 03:03:30 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 03:03:30 GMT
ENV PG_MAJOR=18
# Tue, 30 Dec 2025 03:03:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 30 Dec 2025 03:03:30 GMT
ENV PG_VERSION=18.1-1.pgdg12+2
# Tue, 30 Dec 2025 03:04:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 30 Dec 2025 03:04:13 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Dec 2025 03:04:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Dec 2025 03:04:13 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 30 Dec 2025 03:04:13 GMT
VOLUME [/var/lib/postgresql]
# Tue, 30 Dec 2025 03:04:14 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 03:04:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Dec 2025 03:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Dec 2025 03:04:15 GMT
STOPSIGNAL SIGINT
# Tue, 30 Dec 2025 03:04:15 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Dec 2025 03:04:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b7648f01f6858fc79caf032b4b9ed2f7e43e57f4621dc8cb36e84eb86399065b`  
		Last Modified: Tue, 30 Dec 2025 01:48:36 GMT  
		Size: 32.1 MB (32068844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8993cd576de63224175e2761513dac215150adcfd4397bd3d184de000db7f4`  
		Last Modified: Tue, 30 Dec 2025 03:05:10 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b32758d6de47fa496deec7238c75b37c97200b172a6808ca5de2c077bd488c7`  
		Last Modified: Tue, 30 Dec 2025 03:05:16 GMT  
		Size: 5.4 MB (5368513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488f1e8e76948ecd39b7aeead94f475539765a470c59ca8bef5788154f7c9729`  
		Last Modified: Tue, 30 Dec 2025 03:05:10 GMT  
		Size: 1.2 MB (1208180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c7ff6285c058d7fc3f1ea7a8f7d6c0eb9a90bfa212b60ca622fc14d7c8a2c8`  
		Last Modified: Tue, 30 Dec 2025 03:05:11 GMT  
		Size: 8.1 MB (8066536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cca05c3c74429ec7a9217ebaeedae6d89bde26f2e14a244c5d68d4fcb790078`  
		Last Modified: Tue, 30 Dec 2025 03:05:10 GMT  
		Size: 1.3 MB (1283676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f471299bd3ad24fe063c5ba0b3616af479e9a1a90966448e7c24050671b6a00`  
		Last Modified: Tue, 30 Dec 2025 03:05:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:446965b8fe7d7401776520ac6e95f2a321aa4c51d5d2bb7df64fc8dcc4b97162`  
		Last Modified: Tue, 30 Dec 2025 03:05:11 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5894d5a4f25b63af530aa1a5ba1576a70b2e9b2beca184f86c8d33481c6cc15e`  
		Last Modified: Tue, 30 Dec 2025 03:05:19 GMT  
		Size: 121.9 MB (121914490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa3c2fa403be6662ca13a76f9d79f40b5fa5eb7a2c8288cf6214dc3a645affb`  
		Last Modified: Tue, 30 Dec 2025 03:05:11 GMT  
		Size: 19.1 KB (19079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed550937168a419f9f34e7315494e052e1ad487adc9b093f4362be9413a7b3e`  
		Last Modified: Tue, 30 Dec 2025 03:05:11 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b5ed835651c7a67a336c5ba46240ccd1e2e62fb367c80859add51190fc76df`  
		Last Modified: Tue, 30 Dec 2025 03:05:11 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd80c11bb87d62ac446b251034b1c0651b6c58a36722d5e1199441e5ccd8550`  
		Last Modified: Tue, 30 Dec 2025 03:05:11 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:1ae1bd9c3386b1c06727bbba15f5694a3eb3655075c5086ab3a54d75d6016a39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6215520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891080b4796869874e5b111f3b14be3f8a5cd5dedd34de407d770beefee77649`

```dockerfile
```

-	Layers:
	-	`sha256:259f13efec4e782dc1c1a72b41c480bc9b895ee9df46a4501ab9b83370946715`  
		Last Modified: Tue, 30 Dec 2025 03:15:46 GMT  
		Size: 6.2 MB (6163872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c82b4139b80c2b1b33bd24b92efc10e7eeed02fb9cec90a953b2a5338dbf8120`  
		Last Modified: Tue, 30 Dec 2025 03:15:47 GMT  
		Size: 51.6 KB (51648 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:4cbae7d6340db5844eb45e055b0b747557632acc0d4b2d660fddd1e747b78aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.4 MB (166358444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85888d5d5672b59ef8262804d221593da07f1884b23949d0b61d5f87f3327ae2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:04:48 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Dec 2025 00:04:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:04:58 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Dec 2025 00:04:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Dec 2025 00:05:03 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 30 Dec 2025 00:05:03 GMT
ENV LANG=en_US.utf8
# Tue, 30 Dec 2025 00:05:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:05:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Dec 2025 00:05:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:05:06 GMT
ENV PG_MAJOR=18
# Tue, 30 Dec 2025 00:05:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 30 Dec 2025 00:05:06 GMT
ENV PG_VERSION=18.1-1.pgdg12+2
# Tue, 30 Dec 2025 00:17:09 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 30 Dec 2025 00:17:09 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Dec 2025 00:17:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Dec 2025 00:17:09 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 30 Dec 2025 00:17:09 GMT
VOLUME [/var/lib/postgresql]
# Tue, 30 Dec 2025 00:17:09 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 00:17:09 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Dec 2025 00:17:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Dec 2025 00:17:09 GMT
STOPSIGNAL SIGINT
# Tue, 30 Dec 2025 00:17:09 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Dec 2025 00:17:09 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:908a8b9619550bcbaa302a1a1375bffd68fb4bab6330d7a965b0b9e3f3896a0a`  
		Last Modified: Mon, 29 Dec 2025 22:25:40 GMT  
		Size: 26.9 MB (26884397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3871b04fd556bf546f070d934db142337040c1511e3993155fbfe1b2a7634d`  
		Last Modified: Tue, 30 Dec 2025 00:17:45 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1303fd135aad89b8d91f902fbef72ed6fdbeb6351644459e25d6322ffe14d0`  
		Last Modified: Tue, 30 Dec 2025 00:17:48 GMT  
		Size: 4.4 MB (4391255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9960e9421284b4e4c1cddb972620b3cfa5b331c1e3b52afd2bee3e61e79823`  
		Last Modified: Tue, 30 Dec 2025 00:17:48 GMT  
		Size: 1.2 MB (1222775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834d6a67d8c312fbeaa4966b7fca2ac3a01aa64799d22e62942c344fe7fb5872`  
		Last Modified: Tue, 30 Dec 2025 00:17:50 GMT  
		Size: 8.1 MB (8120678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf097523e0ea86c1a1ff5c409711fe4bb849dcbcac72b6bfe02962792645ce6`  
		Last Modified: Tue, 30 Dec 2025 00:17:48 GMT  
		Size: 1.1 MB (1097019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee70bc9d86212c0129070cc2ca91a0321633eba41b89348f26af97d30fd1751`  
		Last Modified: Tue, 30 Dec 2025 00:17:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ac5a99bff7b91244fb12dca5ac4fb3c0d5d156c69101dae56543ab345b224d`  
		Last Modified: Tue, 30 Dec 2025 00:17:48 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d24765d0a0d3129a297bc7ea9b9dc4d5d7f8cf1399f11e59ee8cb6896977855`  
		Last Modified: Tue, 30 Dec 2025 00:18:00 GMT  
		Size: 124.6 MB (124612654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeecd3574d80e66c3aa10969d386776e8918fcfd420421cb5990965aecd2f917`  
		Last Modified: Tue, 30 Dec 2025 00:17:48 GMT  
		Size: 19.1 KB (19091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3a47d912b753da16b61b09febbefcf3fc8db55e0e278744671e1d996a1e5db`  
		Last Modified: Tue, 30 Dec 2025 00:17:48 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ab63cb5957da33ca8afa417e25d1a527b7f5a45a90947403016024061064c1`  
		Last Modified: Tue, 30 Dec 2025 00:17:48 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b68cb4a2d0cbeb8aa77ad999b781b9f4a22e726be39cc0245a672513b2b566`  
		Last Modified: Tue, 30 Dec 2025 00:17:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:1cb50f0d92b6a629537e8335ea42025971d1a9ff039261cdeae69293252b6551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6222735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f3a5250269869e7c9cc41f097b2627750d326307c646666098c1a71da06258f`

```dockerfile
```

-	Layers:
	-	`sha256:923e63f04fd16ea77a630875e7e806df9002c539405b5fa83c332b9c997ed68a`  
		Last Modified: Tue, 30 Dec 2025 03:15:52 GMT  
		Size: 6.2 MB (6171145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06a63d3b8ef5a35ac6d7c0390d2cc864da8fde84b606fd8bad383b6ca0434b44`  
		Last Modified: Tue, 30 Dec 2025 03:15:53 GMT  
		Size: 51.6 KB (51590 bytes)  
		MIME: application/vnd.in-toto+json
