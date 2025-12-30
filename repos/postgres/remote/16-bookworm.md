## `postgres:16-bookworm`

```console
$ docker pull postgres@sha256:f4e5027f3f2946bd12c2364a4b6107eeaafbff630ef0aab634abd6135455a751
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

### `postgres:16-bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:aabf42d57c343e4b27101c55550469db623091da35a3449f4693f9db3b1180b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.0 MB (154997215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85cacf63af6fbd04233ba70a4f7b50c9117e5f26b59da38136832ad683a6ce7b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:37:33 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 29 Dec 2025 23:37:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:37:43 GMT
ENV GOSU_VERSION=1.19
# Mon, 29 Dec 2025 23:37:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 29 Dec 2025 23:37:47 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 29 Dec 2025 23:37:47 GMT
ENV LANG=en_US.utf8
# Mon, 29 Dec 2025 23:37:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:37:50 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 29 Dec 2025 23:37:50 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 29 Dec 2025 23:37:50 GMT
ENV PG_MAJOR=16
# Mon, 29 Dec 2025 23:37:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Mon, 29 Dec 2025 23:37:50 GMT
ENV PG_VERSION=16.11-1.pgdg12+1
# Mon, 29 Dec 2025 23:38:01 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 29 Dec 2025 23:38:01 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 29 Dec 2025 23:38:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 29 Dec 2025 23:38:01 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 29 Dec 2025 23:38:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 29 Dec 2025 23:38:01 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 29 Dec 2025 23:38:01 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:38:02 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 29 Dec 2025 23:38:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:38:02 GMT
STOPSIGNAL SIGINT
# Mon, 29 Dec 2025 23:38:02 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 29 Dec 2025 23:38:02 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782801a9d1dfffbe864f85d4b18a3250c64cb679495258c181e81a393d5d7234`  
		Last Modified: Mon, 29 Dec 2025 23:38:31 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d146464ccd743959afc9ac45424fc23e30f245aed13646a57b4f58a75d586de6`  
		Last Modified: Mon, 29 Dec 2025 23:38:32 GMT  
		Size: 4.5 MB (4534043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf4a5ac3ee97f45715b6bf2672944e583c0ed9318abd8203b98c4686ceb5da8`  
		Last Modified: Mon, 29 Dec 2025 23:38:31 GMT  
		Size: 1.2 MB (1249473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b759b6b7cdcecdefb02911231b19e3cb1c3465c51e1771504b82966176177de`  
		Last Modified: Mon, 29 Dec 2025 23:38:32 GMT  
		Size: 8.1 MB (8066411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638817d04b35fbde0d2e1a6f5e6897018f1c7e21b8758a1cc7c22bc1bce88550`  
		Last Modified: Mon, 29 Dec 2025 23:38:31 GMT  
		Size: 1.2 MB (1196387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff3bb3595737cdf71caf6bc2b25f85c4f1895807f42b9f8f24d0faf78cce01d`  
		Last Modified: Mon, 29 Dec 2025 23:38:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264226f2af0eb1b1d70b69ba53a4a695c130af00797f5c4fa1602a87068b4511`  
		Last Modified: Mon, 29 Dec 2025 23:38:31 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315b978676ae5a4b2580d9aa0d9fff71c3a016f11d4df6b87a52bc0fb0ee0c54`  
		Last Modified: Mon, 29 Dec 2025 23:38:37 GMT  
		Size: 111.7 MB (111701816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516cabc6b49bf964c9ae0ae822b5694b8dfaeb5fe6a9537d7241fa14580fe3f7`  
		Last Modified: Mon, 29 Dec 2025 23:38:31 GMT  
		Size: 9.9 KB (9920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3faf08f2515132f90a48e7c456da194cab845bcfe0276ce8a9c334eeef1fcd6f`  
		Last Modified: Mon, 29 Dec 2025 23:38:31 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd512119e25503a324c7114413a1e88854529f9755f29355b29aff89e692e8da`  
		Last Modified: Mon, 29 Dec 2025 23:38:30 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bda0ecc775ebe4a90e0d7c2002d8ef9b89cfd965e64ee69bcb9334bbf822aa4`  
		Last Modified: Mon, 29 Dec 2025 23:38:30 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bdd7bb28a81637a017b42242868b744cbb6b6841a76c6f309475f78ce1fa5d`  
		Last Modified: Mon, 29 Dec 2025 23:38:30 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:147dacc1a331e28278fdfc8c2855d1c3c30f4b8d5e2c0172545e435957e7fccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5962841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:793468a8831c6dfc05b4b4af00583df1d2d58ecc7643f4fd12df65a428fd2fef`

```dockerfile
```

-	Layers:
	-	`sha256:bea4fd8e7f2f6059a54fdd9bb95873c7d22834a12bf7d5b3c82456d77d4dc4bb`  
		Last Modified: Tue, 30 Dec 2025 03:11:42 GMT  
		Size: 5.9 MB (5909546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78902c7be7a393626e92058f456c229e1bb5b44800ffc56efea096304e0f1da2`  
		Last Modified: Tue, 30 Dec 2025 03:11:43 GMT  
		Size: 53.3 KB (53295 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:ccf0d881ea805d0c9fdeea7788c0cc618df9fc514a688d3cafd270b1640bb4a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.0 MB (148010909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a366941086fa4b8eb0378b58a0ffbb27a93c2ceb3ec192ab0b1e28357c53c88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:56:05 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 29 Dec 2025 23:56:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:56:22 GMT
ENV GOSU_VERSION=1.19
# Mon, 29 Dec 2025 23:56:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 29 Dec 2025 23:56:29 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 29 Dec 2025 23:56:29 GMT
ENV LANG=en_US.utf8
# Mon, 29 Dec 2025 23:56:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:56:34 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 29 Dec 2025 23:56:35 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 29 Dec 2025 23:56:35 GMT
ENV PG_MAJOR=16
# Mon, 29 Dec 2025 23:56:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Mon, 29 Dec 2025 23:56:35 GMT
ENV PG_VERSION=16.11-1.pgdg12+1
# Tue, 30 Dec 2025 00:11:25 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 30 Dec 2025 00:11:25 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Dec 2025 00:11:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Dec 2025 00:11:25 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Dec 2025 00:11:26 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 30 Dec 2025 00:11:26 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Dec 2025 00:11:26 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 00:11:26 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Dec 2025 00:11:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Dec 2025 00:11:26 GMT
STOPSIGNAL SIGINT
# Tue, 30 Dec 2025 00:11:26 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Dec 2025 00:11:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:cdd01b66e4b6599d6f59fe75d883783e8ddfc67db8fda967c6ce250da575cc0b`  
		Last Modified: Mon, 29 Dec 2025 22:25:33 GMT  
		Size: 25.8 MB (25757576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60c2f03771c1cb3ac50191334860c0314b8ac9e272ea886d206ea8ee2949212`  
		Last Modified: Tue, 30 Dec 2025 00:11:55 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4c99e1a376f3f91490c66a9179421f2e59166804333fa8c3c4644d50d48453`  
		Last Modified: Tue, 30 Dec 2025 00:11:55 GMT  
		Size: 4.2 MB (4151196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c18c864aa31c4d7fa3088524bc6c77ae5216b09686d7bbcb460a2458136063`  
		Last Modified: Tue, 30 Dec 2025 00:11:55 GMT  
		Size: 1.2 MB (1220041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae239219046aa8e83942d598e7473f500ba7da0de4b10f8bd477dd3d0925378a`  
		Last Modified: Tue, 30 Dec 2025 00:11:55 GMT  
		Size: 8.1 MB (8066525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63b059d74521551f1a939e8a53e46ceb104ced1e7e68fc2080c4b2525cbe9a1`  
		Last Modified: Tue, 30 Dec 2025 00:11:55 GMT  
		Size: 1.2 MB (1195004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0315129b13688489eac9794828d84a35b0184ad0f5d6e475668680f32a102a3c`  
		Last Modified: Tue, 30 Dec 2025 00:11:55 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8801bc5e5fd3cc45b0e7e8b707b52ce83f6a48b426e2378f9da2927357a17ca8`  
		Last Modified: Tue, 30 Dec 2025 00:11:55 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d5166548e95ddfd46d0515154eeb1a60c0c0343e159ebbb441ad1174db4bf7`  
		Last Modified: Tue, 30 Dec 2025 00:12:07 GMT  
		Size: 107.6 MB (107599901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12bf71c0475af4b83c5e7a5e86de43d588125c39b47fe950c9751923343fd23e`  
		Last Modified: Tue, 30 Dec 2025 00:11:55 GMT  
		Size: 9.9 KB (9924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0e8fd457af5c1ca5d75ae472cebbf4b953ba80766fb68c82c4951fd48a5b9d`  
		Last Modified: Tue, 30 Dec 2025 00:11:55 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54ab3aa605d981a249e44e3d2d8948580eb2847b3533ffc6df29f204891cde2`  
		Last Modified: Tue, 30 Dec 2025 00:11:55 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02265133aae3e46bf6bd3b4bfa15f0f9aa858ef306d58853016f8eef7e963b00`  
		Last Modified: Tue, 30 Dec 2025 00:11:55 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9827e239fddd3f50e343a86d928e8fe50bc870523d461870adb3776b082208`  
		Last Modified: Tue, 30 Dec 2025 00:12:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:f4357b31a5dd8cbd541c43b411a4e80a4e9754761c687e37ef961214408904e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5981145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c0649716661d68d62008f9267202e2202e55075fc9f2a51473539d2e4fffdc`

```dockerfile
```

-	Layers:
	-	`sha256:2ded495f6fe130361ffcafd06bb23aa02bb85b741c72f47a060d61e4c5735b4e`  
		Last Modified: Tue, 30 Dec 2025 03:11:48 GMT  
		Size: 5.9 MB (5927643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89d43d5ebf506d9678df3589fc6277cdbbad76e4e449a448347f4c9c6ff52d13`  
		Last Modified: Tue, 30 Dec 2025 03:11:49 GMT  
		Size: 53.5 KB (53502 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:c54d2a2da651b4f43af8abebfc746e2bb705990a11ec38cefeb6933e77ce345a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143069218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a826776dafb37e5213f31caa3a5924b44ea7f2be577adb091abd0452a9a21b36`
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
ENV PG_MAJOR=16
# Mon, 29 Dec 2025 23:55:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Mon, 29 Dec 2025 23:55:59 GMT
ENV PG_VERSION=16.11-1.pgdg12+1
# Tue, 30 Dec 2025 00:22:50 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 30 Dec 2025 00:22:51 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Dec 2025 00:22:51 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Dec 2025 00:22:51 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Dec 2025 00:22:51 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 30 Dec 2025 00:22:51 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Dec 2025 00:22:51 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 00:22:51 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Dec 2025 00:22:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Dec 2025 00:22:51 GMT
STOPSIGNAL SIGINT
# Tue, 30 Dec 2025 00:22:51 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Dec 2025 00:22:51 GMT
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
	-	`sha256:941f5728f9102848654a8df6a4b8543f31dd7e846afd8f24764d90d650a9af7b`  
		Last Modified: Tue, 30 Dec 2025 00:23:26 GMT  
		Size: 105.0 MB (105022236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8449976e1a5f37463f9a5579df6528fab83e35f30d171d9db055a9ce900fdf3`  
		Last Modified: Tue, 30 Dec 2025 00:23:18 GMT  
		Size: 9.9 KB (9918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b30eff49c5033711ba6d7724dcc60392e6165a156915f9210e992d4889446c`  
		Last Modified: Tue, 30 Dec 2025 00:23:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b56c321481d9d27cbfa4e61da4a490aac134d2a61fdedb15ef0eade11a461c1`  
		Last Modified: Tue, 30 Dec 2025 00:23:18 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec5c54af7bda9ac1bab07787e5ecb369ffde16bd4882e9c0a781d6d0caf0f04`  
		Last Modified: Tue, 30 Dec 2025 00:23:20 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3b0bf41baeb0b38744e8c81852ed922ae1517f0a22f929f804d91cf62b0f61`  
		Last Modified: Tue, 30 Dec 2025 00:23:18 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:136b2983f95bd6d68f0bccca6bfb658e5f67c8875ef58d4b4def0e23a83db728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5980401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d969f01ca9804cd2dc0b0573206389c659445a3a5eaf64fb8588ce7ab88ec80`

```dockerfile
```

-	Layers:
	-	`sha256:531362b2bf77875cdb908c92ae167beb2d1f890b8d12ccf3be0c4e404df5f70c`  
		Last Modified: Tue, 30 Dec 2025 03:11:54 GMT  
		Size: 5.9 MB (5926898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5728f874cd5874c6bf3bdc087f9be17319ae5cd73e43ae9a064eb5148344f277`  
		Last Modified: Tue, 30 Dec 2025 03:11:55 GMT  
		Size: 53.5 KB (53503 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:3762871714d180c54824fcf3881a2b1e38cf86195533a216867c7a0484d51b95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.0 MB (152985238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4798b5c8f078eb09998925508ac4e66b2a93e19ad58ac119ce5d00de35c9471`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:40:30 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 29 Dec 2025 23:40:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:40:42 GMT
ENV GOSU_VERSION=1.19
# Mon, 29 Dec 2025 23:40:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 29 Dec 2025 23:40:47 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 29 Dec 2025 23:40:47 GMT
ENV LANG=en_US.utf8
# Mon, 29 Dec 2025 23:40:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:40:50 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 29 Dec 2025 23:40:51 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 29 Dec 2025 23:40:51 GMT
ENV PG_MAJOR=16
# Mon, 29 Dec 2025 23:40:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Mon, 29 Dec 2025 23:40:51 GMT
ENV PG_VERSION=16.11-1.pgdg12+1
# Mon, 29 Dec 2025 23:41:03 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 29 Dec 2025 23:41:03 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 29 Dec 2025 23:41:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 29 Dec 2025 23:41:03 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 29 Dec 2025 23:41:04 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 29 Dec 2025 23:41:04 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 29 Dec 2025 23:41:04 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:41:04 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 29 Dec 2025 23:41:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:41:04 GMT
STOPSIGNAL SIGINT
# Mon, 29 Dec 2025 23:41:04 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 29 Dec 2025 23:41:04 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa19b916d154cb9bfaea250caa1b464d95d68545103b7cef873bfd4411185f3b`  
		Last Modified: Mon, 29 Dec 2025 23:41:32 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4429ed9e3516868439e9baffb57e5115a2afed9f02b0a95832410d1dfd5453e`  
		Last Modified: Mon, 29 Dec 2025 23:41:32 GMT  
		Size: 4.5 MB (4519803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149b6f9ea48d3e18da4dbb09f7ce0e6f40f263352af7ba1dfe2e7d1e40b1b273`  
		Last Modified: Mon, 29 Dec 2025 23:41:34 GMT  
		Size: 1.2 MB (1203258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15fe32db1bbc3adb697d6ad8dbaa9b0bf072673be117bf14cdf983410c9fc1ed`  
		Last Modified: Mon, 29 Dec 2025 23:41:33 GMT  
		Size: 8.1 MB (8066476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52ab647ca18df1f9d065fb7c7d7932be34c75aee3875ee0cedaabcab1ed4989`  
		Last Modified: Mon, 29 Dec 2025 23:41:32 GMT  
		Size: 1.1 MB (1108976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4de01ea1128ceafe62dc3e65732e4a57699f32e8919895b6a5e189583b6157`  
		Last Modified: Mon, 29 Dec 2025 23:41:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf76c04ed1ec854e678d630de72793ecf635265f7b2b83a3b9a6be029fe6a017`  
		Last Modified: Mon, 29 Dec 2025 23:41:40 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c2152dba038baa8209282575d8015eec5ab77b60699381d37fc2af2821d390`  
		Last Modified: Mon, 29 Dec 2025 23:41:42 GMT  
		Size: 110.0 MB (109963860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787166f724f57e4cac77d2e4458addbf66c1c921f37b338988df498e0f8e499c`  
		Last Modified: Mon, 29 Dec 2025 23:41:33 GMT  
		Size: 9.9 KB (9917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9aa95dea37b255fb10d65470139722e37e332b1b62f3fb6a2a7ef3d20a5de35`  
		Last Modified: Mon, 29 Dec 2025 23:41:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e3161f0ffd611d240dc254328c7ba26ad04488ade40cf61ac2e327654de846`  
		Last Modified: Mon, 29 Dec 2025 23:41:33 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa7451dc44a7b5486b204882c4fc36bc07def5b8ebc58e4559d54a3f925559a`  
		Last Modified: Mon, 29 Dec 2025 23:41:33 GMT  
		Size: 5.8 KB (5835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe3983b8a36c2248d93e87f571e4fe740fe93ccbdbf510491845baa7d7bc56f`  
		Last Modified: Mon, 29 Dec 2025 23:41:33 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:524e4fff7f0dcbfa7053c9872bd16347fda039826f22f9be3dc34693fbc2bcd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5969398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1efc87a23c14f6fbdbf2c2f2be6bb60f447648aec5b61516920dd0ba5e70ad5`

```dockerfile
```

-	Layers:
	-	`sha256:8ff43481363d2892a8581a7c5404f2f4943276ece206c1b9fc71d234de8942a0`  
		Last Modified: Tue, 30 Dec 2025 03:12:02 GMT  
		Size: 5.9 MB (5915857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa70990e9ab147ce6182d969e2c9ef85dbf0774e936ede6dd6ce2e41a33fde93`  
		Last Modified: Tue, 30 Dec 2025 03:12:03 GMT  
		Size: 53.5 KB (53541 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:7aceaa2d375c63f70136bf2899ef17631c6771d6ce4f24cff447577443ca1541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.8 MB (163789277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411b79bc9b0bcf29b909bb41f33b8735d665a9d02a1de5a750d5bdc3149ce5da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:34:14 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 29 Dec 2025 23:34:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:34:26 GMT
ENV GOSU_VERSION=1.19
# Mon, 29 Dec 2025 23:34:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 29 Dec 2025 23:34:31 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 29 Dec 2025 23:34:31 GMT
ENV LANG=en_US.utf8
# Mon, 29 Dec 2025 23:34:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:34:35 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 29 Dec 2025 23:34:35 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 29 Dec 2025 23:34:35 GMT
ENV PG_MAJOR=16
# Mon, 29 Dec 2025 23:34:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Mon, 29 Dec 2025 23:34:35 GMT
ENV PG_VERSION=16.11-1.pgdg12+1
# Mon, 29 Dec 2025 23:46:09 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 29 Dec 2025 23:46:09 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 29 Dec 2025 23:46:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 29 Dec 2025 23:46:09 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 29 Dec 2025 23:46:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 29 Dec 2025 23:46:09 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 29 Dec 2025 23:46:09 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:46:10 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 29 Dec 2025 23:46:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:46:10 GMT
STOPSIGNAL SIGINT
# Mon, 29 Dec 2025 23:46:10 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 29 Dec 2025 23:46:10 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f67520a70f469d560f84fd587586b5b9a9f46691d2f4b10c88544b5d21f5fe06`  
		Last Modified: Mon, 29 Dec 2025 22:24:46 GMT  
		Size: 29.2 MB (29209773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5938a99a867414d377109a1a72a5c9ab0bd0f1cd70a11c4205771e8d1efd1e60`  
		Last Modified: Mon, 29 Dec 2025 23:46:40 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7fd85a783cace66d0338dad6b88356f307c0e60fd4c828a412d3d6a6081466`  
		Last Modified: Mon, 29 Dec 2025 23:46:40 GMT  
		Size: 5.0 MB (4965366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c019358a886c1e0a1729ef2d2c4adee1754fccfbfddb57b1c244d43dfb97962`  
		Last Modified: Mon, 29 Dec 2025 23:46:41 GMT  
		Size: 1.2 MB (1218647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ff690f4ba562cd5cfe660fe8a87823fe6ec05048545a2108bd94a1299a0fa5`  
		Last Modified: Mon, 29 Dec 2025 23:46:41 GMT  
		Size: 8.1 MB (8066420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035d427d87b5dba2c28d5b963eac64edeb87356329b567ba3b02fde68251e6ad`  
		Last Modified: Mon, 29 Dec 2025 23:46:41 GMT  
		Size: 1.1 MB (1137442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0a806634141f4c6f034f0597bb56cbc44e2401b951d5a8a3a2152b0659e193`  
		Last Modified: Mon, 29 Dec 2025 23:46:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1798d8b71764a0c526066d8370676ca4f71161054579b32e7a2e8d92e41ca1`  
		Last Modified: Mon, 29 Dec 2025 23:46:41 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45a1c956b041141423d04c7199dc2450f6169750ffa08f1be5427c77883d6e0`  
		Last Modified: Mon, 29 Dec 2025 23:46:51 GMT  
		Size: 119.2 MB (119170967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2118b0367684f1601037c2b82453b9a9ff3edc40157170773adb4f962e00d13a`  
		Last Modified: Mon, 29 Dec 2025 23:46:41 GMT  
		Size: 9.9 KB (9922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcbdf6d3b7f6c82c580c5579b6682500401ceff4b95b34f1e60272eb74f068e`  
		Last Modified: Mon, 29 Dec 2025 23:46:41 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86845349e473cdb021c8512edf55754bca482d541517c4ef93f536c2150737e4`  
		Last Modified: Mon, 29 Dec 2025 23:46:39 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490a0e4fc20bcdf024d3d6d759d5dba46d36ed58f60c64425170d12d43c8949e`  
		Last Modified: Mon, 29 Dec 2025 23:46:39 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5d58172719bab4b554f13b54219e0cba2d38c45a13a8d0d6acf13d51d33a91`  
		Last Modified: Mon, 29 Dec 2025 23:46:39 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:8da952ca3cfa19921bbba1fcb60831747b7e67632fd8877e53c28e48c3beed5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5979038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9410b0dbb42ec6018c6bbee8840189de4d01eaf0c38ecb77b1a3688538ab3707`

```dockerfile
```

-	Layers:
	-	`sha256:2b0dc1dc62bc15384e2cce9f06af0ba4713677e224af13676eabc8279087c8f3`  
		Last Modified: Tue, 30 Dec 2025 03:12:08 GMT  
		Size: 5.9 MB (5925786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9f4e8bcd81309ff9280a05aefbb575128d7671052e4b5577e322428b7a4a3e8`  
		Last Modified: Tue, 30 Dec 2025 03:12:09 GMT  
		Size: 53.3 KB (53252 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:ca245ddd33edf47320fcdfc34a8eb84bfe557a1fb697e17d7510e2d8174a85a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.9 MB (153854414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e03d003fff9f4930b23bf31dd0616856cbd67083ba328d6babf12bbe3197633a`
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
ENV PG_MAJOR=16
# Tue, 09 Dec 2025 08:37:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Tue, 09 Dec 2025 08:37:09 GMT
ENV PG_VERSION=16.11-1.pgdg12+1
# Tue, 09 Dec 2025 12:10:54 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 09 Dec 2025 12:10:56 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 09 Dec 2025 12:10:58 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 09 Dec 2025 12:10:58 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 09 Dec 2025 12:11:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 09 Dec 2025 12:11:00 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 09 Dec 2025 12:11:01 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 12:11:03 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 09 Dec 2025 12:11:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 12:11:03 GMT
STOPSIGNAL SIGINT
# Tue, 09 Dec 2025 12:11:03 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 09 Dec 2025 12:11:03 GMT
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
	-	`sha256:a7a09b9dad989436370c4f289ed41820f1068171da6ab294a3d03b57f6649716`  
		Last Modified: Tue, 09 Dec 2025 12:13:32 GMT  
		Size: 110.4 MB (110435610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a52cb28e9cde0df8df1de284fa3fa2c91cbb0e9b7bfea12be370fd78648db8`  
		Last Modified: Tue, 09 Dec 2025 12:13:25 GMT  
		Size: 9.9 KB (9925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a673c21e661d006dfa5c89b21cb6eb875483aca6e2070f496e0cc58c853e3680`  
		Last Modified: Tue, 09 Dec 2025 12:13:25 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964a9dcd59e8073ec8e1db9cb8365716bfe02fec3360613b6c4656c9cffcabea`  
		Last Modified: Tue, 09 Dec 2025 12:13:26 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee88d63f38bfa5f689f6b89477abab53e7a7aad4c02e457e3a885e988050bd8`  
		Last Modified: Tue, 09 Dec 2025 12:13:25 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e5326b9c0f7f89e4b74fdd8790fff8774af1fd049864cdb659578ca2274b0c`  
		Last Modified: Tue, 09 Dec 2025 12:13:25 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:ec7efe173ba8dc45ce3336dc5574a488b156d275ee3891fed877f8669b820433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 KB (53162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d9e44ae2686139d40e4c8bc3961c49349cef73dbc57f7f6b0dbb45891742000`

```dockerfile
```

-	Layers:
	-	`sha256:87cac7d63c2c53bb801e0f16aee571fa1b06c050d19fe215e8c7d7f1cdc7107e`  
		Last Modified: Tue, 09 Dec 2025 16:06:09 GMT  
		Size: 53.2 KB (53162 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:f8224752aa2c367336905046acfb854923e7754148f79ca185e863cdbb02deee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167757778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0d610c2260ce83c25e599784a563b83cf65ed4fa8dc67caf676e36ef0872db`
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
ENV PG_MAJOR=16
# Tue, 09 Dec 2025 14:06:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Tue, 09 Dec 2025 14:06:42 GMT
ENV PG_VERSION=16.11-1.pgdg12+1
# Tue, 09 Dec 2025 14:10:33 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 09 Dec 2025 14:10:33 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 09 Dec 2025 14:10:34 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 09 Dec 2025 14:10:34 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 09 Dec 2025 14:10:34 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 09 Dec 2025 14:10:34 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 09 Dec 2025 14:10:35 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 14:10:35 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 09 Dec 2025 14:10:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 14:10:35 GMT
STOPSIGNAL SIGINT
# Tue, 09 Dec 2025 14:10:35 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 09 Dec 2025 14:10:35 GMT
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
	-	`sha256:96426cb8c8010ff9149132441ac5a009fa90fcd706356157656f67b5819171c5`  
		Last Modified: Tue, 09 Dec 2025 14:11:49 GMT  
		Size: 119.7 MB (119741371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48049ce75203bc877ecbac51ef6f2e2553dc7b5858693757df2416f5a691c8b9`  
		Last Modified: Tue, 09 Dec 2025 14:11:35 GMT  
		Size: 9.9 KB (9921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f882cf8845a51f374f49c99afe58f9c00c12f7195c8b61facc52a345a6f68d`  
		Last Modified: Tue, 09 Dec 2025 14:11:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd0fafd64325ab74d9e4e697037f2bf17a0e02aa25c52730fad0a2b6d3139a1`  
		Last Modified: Tue, 09 Dec 2025 14:11:35 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97fda32490b2e7b48ecd2ba21511954b84868fc35e80020a93aff142de79a990`  
		Last Modified: Tue, 09 Dec 2025 14:11:35 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94315724a57cf1198f30b57eaff4c9f86ceb5144fb0cb54d48cdac78f1467117`  
		Last Modified: Tue, 09 Dec 2025 14:11:35 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:ef0feec1130a928dac8fdc77c7217e12f70f4526d91a927316340f56c92aeaf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5970257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96aed50ef0db69cfe85e13a38b17aeaaf784d2b1ed32f8fcf0c5a1db70c1f138`

```dockerfile
```

-	Layers:
	-	`sha256:786bc63352f14ff42b2e852c39700f2034f5bc6e779e93f741e625b76ff0f4df`  
		Last Modified: Tue, 09 Dec 2025 18:08:43 GMT  
		Size: 5.9 MB (5916907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9f63f3cb88a5f565e0ec11911fab68626223a3594f1772374a5ed045e9dc30f`  
		Last Modified: Tue, 09 Dec 2025 18:08:44 GMT  
		Size: 53.4 KB (53350 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:419174de9b9a8341ea852280b9739c4981e455037d153234eb7b3b31046965ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.2 MB (164224373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b7dfb5feec72c7492a9d3c99df0699536755fd468eb9507cf039bdd4d1771c`
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
ENV PG_MAJOR=16
# Tue, 30 Dec 2025 00:05:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Tue, 30 Dec 2025 00:05:06 GMT
ENV PG_VERSION=16.11-1.pgdg12+1
# Tue, 30 Dec 2025 00:29:55 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 30 Dec 2025 00:29:55 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Dec 2025 00:29:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Dec 2025 00:29:55 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Dec 2025 00:29:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 30 Dec 2025 00:29:55 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Dec 2025 00:29:55 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 00:29:55 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Dec 2025 00:29:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Dec 2025 00:29:55 GMT
STOPSIGNAL SIGINT
# Tue, 30 Dec 2025 00:29:55 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Dec 2025 00:29:55 GMT
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
	-	`sha256:e24e53f497d9eb0894d4e140c6e80bb72ccdc9e75507b1f68b27917356482929`  
		Last Modified: Tue, 30 Dec 2025 00:30:44 GMT  
		Size: 122.5 MB (122487582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3daebea07caef5a90d67fe9531c6b6fba006201dbb8239ff69c97eca60c49b96`  
		Last Modified: Tue, 30 Dec 2025 00:30:31 GMT  
		Size: 9.9 KB (9923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945c94c10aae08ebd29b6b4680c747da382c5ebd1fe31e3073b852298d91a489`  
		Last Modified: Tue, 30 Dec 2025 00:30:31 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81bbd963f9bfa3a49e5a3234f719ca3e5e828c816f363588b47989920c6d04ac`  
		Last Modified: Tue, 30 Dec 2025 00:30:31 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fd7c8bffabf7e50175de955eda36af982066a4d4d1dbf165bad63ab2909094`  
		Last Modified: Tue, 30 Dec 2025 00:30:31 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26881f0d8559705b1f497d1490142345a21f5ea30ba86f8b382b60a1b4519dfa`  
		Last Modified: Tue, 30 Dec 2025 00:30:31 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:89acac5c4cba67cfe09629748dce1f802660cb923f839216a7b5739e1470eab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5975558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d07445aacc3e356061fdb295e9a6ff57362f0daf24d423068e768fb9cefd00`

```dockerfile
```

-	Layers:
	-	`sha256:249279be9a3aa84e502817667b126c7ad1b75ef7902a2dd2a43523267d852334`  
		Last Modified: Tue, 30 Dec 2025 03:12:20 GMT  
		Size: 5.9 MB (5922262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea81435fffb8534fa1a857d4bd89edd02a29da0a9b72df38b319a1dd7034d452`  
		Last Modified: Tue, 30 Dec 2025 03:12:21 GMT  
		Size: 53.3 KB (53296 bytes)  
		MIME: application/vnd.in-toto+json
