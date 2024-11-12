## `postgres:16-bookworm`

```console
$ docker pull postgres@sha256:c3c322487067ae4a37f5f2ad956f166e2a56b4885a6de53808e0ddadfbbe512b
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
$ docker pull postgres@sha256:9a70e4d1c03a5066080292db2dd95ee3965d3651316e21989fa0935afb8ce8ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.4 MB (153448130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b14e73a48cf2518aeb37e8b758a907473bcc72727297a7353a665afa069ef10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 26 Sep 2024 18:03:00 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV LANG=en_US.utf8
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PG_MAJOR=16
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PG_VERSION=16.4-1.pgdg120+2
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Sep 2024 18:03:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Sep 2024 18:03:00 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 18:03:00 GMT
STOPSIGNAL SIGINT
# Thu, 26 Sep 2024 18:03:00 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Sep 2024 18:03:00 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46eab5b44a357ff655ff055f57cbe93d7d24b2ce50af8285602c028adbc5bb7f`  
		Last Modified: Tue, 12 Nov 2024 02:10:46 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d302cc468dfc7fbc3c70541c31c6ee565e48869e2a3694aa46f904ab66adfa`  
		Last Modified: Tue, 12 Nov 2024 02:10:47 GMT  
		Size: 4.5 MB (4533728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e0882c90d98534e5843d98b5e21f299a0b874b6e1a7a74433b0d43228b8617`  
		Last Modified: Tue, 12 Nov 2024 02:10:47 GMT  
		Size: 1.4 MB (1446653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531ee2cf3c0c57c2a6c8682a28c71cc65fbaa11eb1d27df052c9506be30836bd`  
		Last Modified: Tue, 12 Nov 2024 02:10:47 GMT  
		Size: 8.1 MB (8066287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed54a7dee1d8c365566e120aa2a9eb952a4d51102fee8b9ce3ad5a524a17f6d5`  
		Last Modified: Tue, 12 Nov 2024 02:10:47 GMT  
		Size: 1.2 MB (1196089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c5c803443f51018d5a99f9dd11b49f94521b248380d1b334f62480014a0b0c`  
		Last Modified: Tue, 12 Nov 2024 02:10:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27c75a98748d914b8022be2b8a46d629685ee48aef2c7aa9408ccb19d0fb527`  
		Last Modified: Tue, 12 Nov 2024 02:10:48 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73cb4a42719dbb29228a389359bbeb8d33df422732f36024d803df8d1a07d52`  
		Last Modified: Tue, 12 Nov 2024 02:10:49 GMT  
		Size: 109.1 MB (109057138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83b68436f09a4b020538a7e3948a377feed7666dba5776b089ae93e5413cad2`  
		Last Modified: Tue, 12 Nov 2024 02:10:48 GMT  
		Size: 9.9 KB (9919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787d6bee95715af45ed03ba2afab59dc508245dedb7886a572c30b45b4a2c8c5`  
		Last Modified: Tue, 12 Nov 2024 02:10:48 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ff0988aaea9649fed1e97a14bc8d2552f0ac0848ca2e8cfcba19e43e8beb44`  
		Last Modified: Tue, 12 Nov 2024 02:10:48 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b82842ab81955836e0b1cf0a0b18a3c11c62c4d4af8d208d2d662052d78b5b8`  
		Last Modified: Tue, 12 Nov 2024 02:10:49 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e568a0dc8fbac53b655d0c0c65ce46f5ae33424315c5cdc35ab61b14bd447a7`  
		Last Modified: Tue, 12 Nov 2024 02:10:49 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:1a671c9cef1554678b4b7f3937cced17fffc1f65c6d9a1516bb4ba9a928dd551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5824028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc138f959fdac13fe8ab8b6164e45baa3791bcc182f6243803a9032b52f9a37`

```dockerfile
```

-	Layers:
	-	`sha256:c14d1b5b139979fbd3e18c32e5b14d5e6eb1c04bf013bb72160d15c09842f2af`  
		Last Modified: Tue, 12 Nov 2024 02:10:47 GMT  
		Size: 5.8 MB (5769450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cdfb525459b43bbdbfe50a6413fb108a3466619712014218784c3fda7e29bd1`  
		Last Modified: Tue, 12 Nov 2024 02:10:47 GMT  
		Size: 54.6 KB (54578 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:5b8f883735b765f2831f7903b253b55b71268d3e6cf9132f41d633f279733040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146179493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4c474493db59cff0213805d6581b0b05afa6008db3cbf9b4f2f0a41c76fedb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 26 Sep 2024 18:03:00 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV LANG=en_US.utf8
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PG_MAJOR=16
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PG_VERSION=16.4-1.pgdg120+2
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Sep 2024 18:03:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Sep 2024 18:03:00 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 18:03:00 GMT
STOPSIGNAL SIGINT
# Thu, 26 Sep 2024 18:03:00 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Sep 2024 18:03:00 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5ecbccf2cc6c4ffb179160d83e2f057a548b6aea719fc2b9b49c502da3d570e3`  
		Last Modified: Tue, 12 Nov 2024 00:55:10 GMT  
		Size: 26.9 MB (26890058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c9a75d6e7bb0b84fa3e3ed126da8e658c14423c6746bd4708bed0493f1152f`  
		Last Modified: Tue, 12 Nov 2024 04:56:02 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d576dac920716be0bdac71b91363bbe47b194b30453c870e3040401cdf27c139`  
		Last Modified: Tue, 12 Nov 2024 04:56:03 GMT  
		Size: 4.2 MB (4151053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8062b4ddee0ebd75cfc9c35c701133ed8e008d538120486da7f84f2a4f06334d`  
		Last Modified: Tue, 12 Nov 2024 04:56:03 GMT  
		Size: 1.4 MB (1423943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255ec96080c265c8341c4c683759a3f40690d07ef2f6b4b924ee2522c7cda429`  
		Last Modified: Tue, 12 Nov 2024 04:56:03 GMT  
		Size: 8.1 MB (8066447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4214ae3216be6a3aeb230779b6d350520da53667c5dc41d8ca7cca5ceb446e`  
		Last Modified: Tue, 12 Nov 2024 04:56:04 GMT  
		Size: 1.2 MB (1194867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15445246728e989cbdc1fbafdf1021e5230da619b5d4f1f0f1afb4056922061`  
		Last Modified: Tue, 12 Nov 2024 04:56:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37d7cc3ecd447669eb8e64205a144ec5677d1623d5375f69b8d57d1ce83c8d4`  
		Last Modified: Tue, 12 Nov 2024 04:56:04 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4d1315d5a94d8a7e78eab7d47ec7b11b298b6986726a39aa8eaeec526f4de0`  
		Last Modified: Tue, 12 Nov 2024 05:13:39 GMT  
		Size: 104.4 MB (104432879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4167286b75424d9a9b6d5a77092664b7ae5f5b34d85c2a8b57a7f322c6b0df3b`  
		Last Modified: Tue, 12 Nov 2024 05:13:36 GMT  
		Size: 9.9 KB (9923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57b15061f8c7a7c0fac6cc0178d3ef7d1822408ebb52fc43777a8041a2402be`  
		Last Modified: Tue, 12 Nov 2024 05:13:36 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173c8af903d2efb327c2895cf3d66c79b649e3a5d88ea6fcb5454d33b0dc7ecd`  
		Last Modified: Tue, 12 Nov 2024 05:13:36 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7ed43867c61dd3e4d3ac1cc1c2b1f00e8f5ac4e5f11134da7812bd6937a826`  
		Last Modified: Tue, 12 Nov 2024 05:13:37 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124dd3a83a6a1f44533dac3b44069d295fc521cefeb15d217f5b10a885363da5`  
		Last Modified: Tue, 12 Nov 2024 05:13:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:9872e0ffd80412140dcb7389649cf90b23cf354862655b906e0f01ee5c3718b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5840027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0817ec28ad907ce17ca60969ec7f24137a3b264a8aaf73ac4de4a251a476ab96`

```dockerfile
```

-	Layers:
	-	`sha256:369d81882d06ab0e010d5f53511838a6d758b05dbe331d436cca64caa2ae879e`  
		Last Modified: Tue, 12 Nov 2024 05:13:36 GMT  
		Size: 5.8 MB (5785230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c5450242a732227a5f9cdf590ec0daf4177a0e548404371de52438f031e87f7`  
		Last Modified: Tue, 12 Nov 2024 05:13:35 GMT  
		Size: 54.8 KB (54797 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:f8f0892a9148a20a1549f71dbd401c18c1061f61318b28fc945c95962b0a0fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140907768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c3c7c05c18cfc6e45d3f30901a41383bc40975b96f15bf3ab58b7a2c92f58f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 26 Sep 2024 18:03:00 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 26 Sep 2024 18:03:00 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV LANG=en_US.utf8
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PG_MAJOR=16
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PG_VERSION=16.4-1.pgdg120+2
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Sep 2024 18:03:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Sep 2024 18:03:00 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 18:03:00 GMT
STOPSIGNAL SIGINT
# Thu, 26 Sep 2024 18:03:00 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Sep 2024 18:03:00 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ce2863b6239d64258cb5259fe7c6662af1a6608de30cfbd083cbd8f2c4444a`  
		Last Modified: Thu, 17 Oct 2024 18:17:29 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca05ab1f003fb8509ac57a2e4c7d6878be5f1bea874573563d5b8f1c08ae5ad5`  
		Last Modified: Thu, 17 Oct 2024 18:17:30 GMT  
		Size: 3.7 MB (3742584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83f5906664d16faa0b6d62929bea3e5c74cad9286294ee54eb7117da1297007`  
		Last Modified: Thu, 17 Oct 2024 18:17:30 GMT  
		Size: 1.4 MB (1413641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c58f3f3af02b25f25b523ed0ea1fb442270ebf32158b3855452ba22389eaab`  
		Last Modified: Thu, 17 Oct 2024 18:17:30 GMT  
		Size: 8.1 MB (8066302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0aa0d5d266482ff233121591ef9a5eb2b155bb6cbca321c85bd71a5155470c`  
		Last Modified: Thu, 17 Oct 2024 18:17:31 GMT  
		Size: 1.1 MB (1066987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40edc6be753b3463eed28795acbc46b6f93f7f81ec0a582168c3755bb900e4e`  
		Last Modified: Thu, 17 Oct 2024 18:17:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42646e9542367c42cf1121b90465e4c66d80e11169ced1e36404b204b75a037c`  
		Last Modified: Thu, 17 Oct 2024 18:17:31 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e253066df64df1201ce1cecaaddfc4704e14602e579d1a67b305350de5ef1bf8`  
		Last Modified: Thu, 17 Oct 2024 18:48:33 GMT  
		Size: 101.9 MB (101879813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73c5a09b9abf1659512018f774487c9edc2766b070bae9c5d4b02de838fbb53`  
		Last Modified: Thu, 17 Oct 2024 18:48:30 GMT  
		Size: 9.9 KB (9923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d273e4ba2a5187412ca036f3a939e18dab041f8c7e224da967d139aa465ec070`  
		Last Modified: Thu, 17 Oct 2024 18:48:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081df9f2eece29d629e3653ecbeefbb3f28629e412b64a9f8041f9d86ab4f263`  
		Last Modified: Thu, 17 Oct 2024 18:48:31 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7aab1ed4aba19f274d25e11a214382f0dbb3aabacf191009d83891352279f7`  
		Last Modified: Thu, 17 Oct 2024 18:48:31 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf4642bd3fabe7f9200afa32e5cbe4ca39d33e9062a981434ffc4d1c68ae944`  
		Last Modified: Thu, 17 Oct 2024 18:48:31 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:d6615889b1ff82dc9a65eb5da2c8724d913e90e70a85c819d6fc767fd8508f48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5820903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a013d9878fffca111891321c45d178d1164ecf78339da6b0aff32f9b8689592a`

```dockerfile
```

-	Layers:
	-	`sha256:7ceefdee028edcc5bbd279df93154ba2092c413ca12e803eb42fd050035865cc`  
		Last Modified: Thu, 17 Oct 2024 18:48:30 GMT  
		Size: 5.8 MB (5766220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76d7ba541528d1ad6f9ef348252373c57047a4846fe63a3d9025611d0e6efe83`  
		Last Modified: Thu, 17 Oct 2024 18:48:30 GMT  
		Size: 54.7 KB (54683 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:f6a3e92973e341fb60ad892159e2089711f3ce3ba5a1ea99dff58d6aeb443241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151631144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:902c76d336c21f1cf7976e89935d137e712aa89dc245096beb839c9887faee4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 26 Sep 2024 18:03:00 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV LANG=en_US.utf8
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PG_MAJOR=16
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PG_VERSION=16.4-1.pgdg120+2
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Sep 2024 18:03:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Sep 2024 18:03:00 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 18:03:00 GMT
STOPSIGNAL SIGINT
# Thu, 26 Sep 2024 18:03:00 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Sep 2024 18:03:00 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab69d7a13052ab4c1c6c106b38b5789b911c218c839e653e05fb8b2122d5792`  
		Last Modified: Tue, 12 Nov 2024 09:09:27 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4716a73860da75029fe9430b1c4f94be3218b836db163adfb3cc48b5c2b93ee`  
		Last Modified: Tue, 12 Nov 2024 09:09:28 GMT  
		Size: 4.5 MB (4499129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620cd14150c219cefc32a5d2d2a28a9717c251a9764b8e2e46d6845d88b21e5c`  
		Last Modified: Tue, 12 Nov 2024 09:09:28 GMT  
		Size: 1.4 MB (1378690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d730e148c105da59c5f207752779797679cb3b7cc473b9123d7faff3ae7fce2`  
		Last Modified: Tue, 12 Nov 2024 09:09:28 GMT  
		Size: 8.1 MB (8066302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3ab4cc12dd5bf7b98c8040de1581b71f29d949c07e62a91f5d2cdc4f2871d4`  
		Last Modified: Tue, 12 Nov 2024 09:09:29 GMT  
		Size: 1.1 MB (1108703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2ae87b8c79be6182740ace38f245ff595752e49f5f57ac1044b3a17da644d9`  
		Last Modified: Tue, 12 Nov 2024 09:09:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb78c41da0aaaec5dcc8892cf07014b241a96eed14b6e64187aef2fc1ab620b`  
		Last Modified: Tue, 12 Nov 2024 09:09:29 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bbc2804eb4ec53ac24761ac4e00b5479e4d2cd754787cab66af26d483fc042`  
		Last Modified: Tue, 12 Nov 2024 09:18:42 GMT  
		Size: 107.4 MB (107400725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25e415bf74ff1b229555873a95f72703b08e1b8bd36b805523c809bd870a5f8`  
		Last Modified: Tue, 12 Nov 2024 09:18:40 GMT  
		Size: 9.9 KB (9918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25f1e19cf78b2ab85d0843dbd0dd459646c1beefe23c19c2e12030d641e774a`  
		Last Modified: Tue, 12 Nov 2024 09:18:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d382eece6dd302b29caa448cd8cb3543d66ac7c7322f659fe4f80bea044577b3`  
		Last Modified: Tue, 12 Nov 2024 09:18:40 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb1676baca68fabc8c4c04e0471293042c91a9a47c6205df86f7a5ff550bc9b`  
		Last Modified: Tue, 12 Nov 2024 09:18:41 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3372b268d51e9d806025768d9ddea1abd118dbd755cbb977aeb143bd80a2b4`  
		Last Modified: Tue, 12 Nov 2024 09:18:41 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:795c6164adaea444c74072a33e4efb68be64048f5e9158042a7afefa5cb318f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5830638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8a00677ff0855e373dcc1f40b7754f9d67e29ec5905d4d8334fad6715484568`

```dockerfile
```

-	Layers:
	-	`sha256:27d5ab52a659b1985729d7b7ea315e10818d7232d78edd1057b9de102ea1ff80`  
		Last Modified: Tue, 12 Nov 2024 09:18:40 GMT  
		Size: 5.8 MB (5775791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:933648d09442fc5e7ee2d7cb11a4cf025a8e95b71e156ee443fbd1c828203dad`  
		Last Modified: Tue, 12 Nov 2024 09:18:39 GMT  
		Size: 54.8 KB (54847 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:84a4ae6ff6a032cea7a775abee384320b720c0bc6773072917a87923c0dc1d49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161585519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9545af52b66a3fb69bc3290b22a52a9c1c39a5032504a18f67d6e35579763c9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 26 Sep 2024 18:03:00 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV LANG=en_US.utf8
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PG_MAJOR=16
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PG_VERSION=16.4-1.pgdg120+2
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Sep 2024 18:03:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Sep 2024 18:03:00 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 18:03:00 GMT
STOPSIGNAL SIGINT
# Thu, 26 Sep 2024 18:03:00 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Sep 2024 18:03:00 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7ee1f09256b44dcbf1fdceb1812168d85f16b3efac3344e077a5ad5b9b91a1`  
		Last Modified: Tue, 12 Nov 2024 02:23:57 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167652ef4dc736fbe6a4e2beca719a3f42e8b2b1f7bc10e9e8f6a9b42b5f607a`  
		Last Modified: Tue, 12 Nov 2024 02:23:58 GMT  
		Size: 5.0 MB (4965057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabdef9fd617bcf49e4b5d8e479fce7b23e94f9159e70e6b2f592691bbb561a1`  
		Last Modified: Tue, 12 Nov 2024 02:23:57 GMT  
		Size: 1.4 MB (1422150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a87ad0f7ec1277900aecaa79be9aa24ebefd26b31b87ef6981f87ab5bf7c8b0`  
		Last Modified: Tue, 12 Nov 2024 02:23:58 GMT  
		Size: 8.1 MB (8066285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acdc33c9199c4c2be3664fbdbfdb809520f1d4dfe65b4a0fc099e4b0bb87cef`  
		Last Modified: Tue, 12 Nov 2024 02:23:58 GMT  
		Size: 1.1 MB (1137168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963a430a752722396ecd0e7936a1c56b7903025f7fc857d21ce7312000c1a440`  
		Last Modified: Tue, 12 Nov 2024 02:10:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10f3f87aa32d86a6f6e1fb360c63615e595f1966aea4bf0fe7e2cd02ba48441`  
		Last Modified: Tue, 12 Nov 2024 02:23:59 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6080e5c36dc10fd48b9ea4d042225aac29639da4e9822757a06771510dee3413`  
		Last Modified: Tue, 12 Nov 2024 02:24:02 GMT  
		Size: 115.8 MB (115829164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceeda64eac3a9943cf70aad2feaa446c4427111f6165754e19799eadf56e0df1`  
		Last Modified: Tue, 12 Nov 2024 02:23:59 GMT  
		Size: 9.9 KB (9925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec5fc1b948ee3b8ad7339be923f6e999dd090ec065b1547adf4b312417f2924`  
		Last Modified: Tue, 12 Nov 2024 02:23:59 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aed36defe8d5264f9c7f73a3c03ab501aee15559ec9f30d3ddcb4c7887772b0`  
		Last Modified: Tue, 12 Nov 2024 02:24:00 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799316298257c3406b376b585579f21f857e26e8a1cd333ef875114b425d1c54`  
		Last Modified: Tue, 12 Nov 2024 02:24:00 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fe6c57ae9b3f2a0729099dd36b49afd360005ed87a2c1b5992b5365d319d56`  
		Last Modified: Tue, 12 Nov 2024 02:24:00 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:c2848c10c67f0fb61132eca0d82b790d519341695f27415fcaeb4232f159ecf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5837807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d967888fd47a9664bb769e64d0fb1f28ea69ed8225f6a5bce5bb6d9fc944624`

```dockerfile
```

-	Layers:
	-	`sha256:c1231a68bb878022d3d4f660414d5b2fe667883b75d7b05df25683bdf3723993`  
		Last Modified: Tue, 12 Nov 2024 02:23:57 GMT  
		Size: 5.8 MB (5783283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d00dbfc3ca82e876b339d7b0995b47862e3d7466d48a2a85348c37a67aeb585f`  
		Last Modified: Tue, 12 Nov 2024 02:23:57 GMT  
		Size: 54.5 KB (54524 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:4e932518fb75835c9245e9c6a99444cf3c4bf80385b84e958288d4fd7fdca96d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.9 MB (148866893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce87ecb0a51773ddafc600cde1d013fb13cb20bf405197f6aff48feb454cb7df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 26 Sep 2024 18:03:00 GMT
ADD file:6c11edc513b28b5a4034ee9c0d4cdcf019a82635ebb8a9e02732800fa457f683 in / 
# Thu, 26 Sep 2024 18:03:00 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV LANG=en_US.utf8
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PG_MAJOR=16
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PG_VERSION=16.4-1.pgdg120+2
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Sep 2024 18:03:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Sep 2024 18:03:00 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 18:03:00 GMT
STOPSIGNAL SIGINT
# Thu, 26 Sep 2024 18:03:00 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Sep 2024 18:03:00 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8f9d02f0305fc460f51690aebcb328c22e13a197228c0910e24b813db943a15b`  
		Last Modified: Thu, 17 Oct 2024 01:18:03 GMT  
		Size: 29.1 MB (29124779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8229a2b987c573ce24ec7945077cf94f45b4a93df0198919b64922db9c3d8e`  
		Last Modified: Fri, 18 Oct 2024 03:04:08 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a489944320ceb947ee507a596c278713aa6c35f4d279d0113f6974c16f35bcd`  
		Last Modified: Fri, 18 Oct 2024 03:04:09 GMT  
		Size: 4.5 MB (4475088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de62f1c89cab68b642617b5cafd8e41baac61f9645a7354c67920d5f17ad27b`  
		Last Modified: Fri, 18 Oct 2024 03:04:09 GMT  
		Size: 1.3 MB (1333805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057ffadde1b963c62db1ed441776e0a13abb6f376f7b12989b3f8dcf720fe931`  
		Last Modified: Fri, 18 Oct 2024 03:04:10 GMT  
		Size: 8.1 MB (8066484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df456abfb9c28297ff9a11730d0e8bed88a2748b1208c1083cc2a8bb4446f42`  
		Last Modified: Fri, 18 Oct 2024 03:04:10 GMT  
		Size: 1.2 MB (1182670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec8f00e859c32d94c35f3cfc73660226851eafc696f6b834bec9c4ee51bb6b5`  
		Last Modified: Fri, 18 Oct 2024 03:04:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234a24e0f4148cf6ec18bd7c5e0b0c4485e91eb339b11945f4639e671624e1bc`  
		Last Modified: Fri, 18 Oct 2024 03:04:10 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772aff70a574a94f7426653c63ccce0062303a6f30690891713ea91b054cbf0a`  
		Last Modified: Fri, 18 Oct 2024 04:15:31 GMT  
		Size: 104.7 MB (104663821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8133f21e9aa490285d248a71a70c24b9446ade3d4135255eb7412cdc40fd8bc`  
		Last Modified: Fri, 18 Oct 2024 04:15:20 GMT  
		Size: 9.9 KB (9921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6065ea2fcce34fba250b651b25f0eb634c5f306ffcd53f38211a80771295ea52`  
		Last Modified: Fri, 18 Oct 2024 04:15:21 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4457c59b42e5b7cd464bfdf0bb72928d9e16afbc3b23dca15122185d5f4b3b52`  
		Last Modified: Fri, 18 Oct 2024 04:15:21 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60087db7e54505c25e1c151d28d41a39a23e5c9eb6ff7cecd85683b1cdc393f`  
		Last Modified: Fri, 18 Oct 2024 04:15:22 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d4aa7dcee0c239685d7ac823bced9a0b4731a02b8c3ffb8ebcb5a85047499e`  
		Last Modified: Fri, 18 Oct 2024 04:15:22 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:9ff11c82270303fdab1212cbc20cebc39088bb5bcf657e57ff647ddba90623c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 KB (54341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4245f711ebb2264ddd6cde59cd1c628e95f6ea879516740b9cce186d9083147f`

```dockerfile
```

-	Layers:
	-	`sha256:550d5cd90c222916ab625b6ad39e527aa8b8defd43caae2771373596875d3e98`  
		Last Modified: Fri, 18 Oct 2024 04:15:20 GMT  
		Size: 54.3 KB (54341 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:d81e51087d9c14f6d2f29cf4d3fd0d20704ab11c43f6cfe46fecb9d23f25b809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.6 MB (165630210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ba4bf45f2c0aca54f1c638b0a7258cb5e8f923ce38efe8d81455d6af6c2422c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 26 Sep 2024 18:03:00 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV LANG=en_US.utf8
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PG_MAJOR=16
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PG_VERSION=16.4-1.pgdg120+2
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Sep 2024 18:03:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Sep 2024 18:03:00 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 18:03:00 GMT
STOPSIGNAL SIGINT
# Thu, 26 Sep 2024 18:03:00 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Sep 2024 18:03:00 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70eb90d7d5c11314f72e41413d38f889c2c3b6b1df1c13509e494536fb4a7474`  
		Last Modified: Tue, 12 Nov 2024 06:56:24 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601864a3c4064a6c4adf07836b13e484879205cf91110bf8b1b6ded160183abf`  
		Last Modified: Tue, 12 Nov 2024 06:56:25 GMT  
		Size: 5.4 MB (5368119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376a9b32bd536fe83df36c4042660efcbbf45bfe573830752f077b936f9fad63`  
		Last Modified: Tue, 12 Nov 2024 06:56:25 GMT  
		Size: 1.4 MB (1368648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ea5ae686b46fe56f40c695cd2cc65c4dff8508a97cad4d04806451012fb546`  
		Last Modified: Tue, 12 Nov 2024 06:56:25 GMT  
		Size: 8.1 MB (8066317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c53822aca86d381dd59f6a4f29b3167b4f0ef37c2cf227c5b02aa6db57a983e`  
		Last Modified: Tue, 12 Nov 2024 06:56:26 GMT  
		Size: 1.3 MB (1283485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79619e7ea9ad42fee1089a3e533609a0178f2d126f1333f383886ca02ffa79aa`  
		Last Modified: Tue, 12 Nov 2024 06:56:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dc5b07bdc69af89aa1396ead1be025dfd43f3145465c89fde5437a2eef12b5`  
		Last Modified: Tue, 12 Nov 2024 06:56:26 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add0fbc158311521ad1d2a2059a34da19a3836970d9b056bfe280117b14e4315`  
		Last Modified: Tue, 12 Nov 2024 07:06:13 GMT  
		Size: 116.4 MB (116398045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcff299ff9d80d04ace719977a74aa9919a68f588dcb0db7fd37806fdabd30b3`  
		Last Modified: Tue, 12 Nov 2024 07:06:09 GMT  
		Size: 9.9 KB (9921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86203ad20fc28f127c131b452cfa9d408e5d598dcf0e55f5710f681c3ecff3cb`  
		Last Modified: Tue, 12 Nov 2024 07:06:09 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1871d0637e1a7397c1ec88d143d8bda39128ba54a9eb0f16cc8080fb8b1bbf90`  
		Last Modified: Tue, 12 Nov 2024 07:06:09 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f8faed5d5737d95c0916a69a9be8ef242feae4a7e153ef86127c400e67d99b`  
		Last Modified: Tue, 12 Nov 2024 07:06:10 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00335543e4faed24dd1cd4ee5fa7af74a37bb6709f4cd2547dfd4ea1a33f999b`  
		Last Modified: Tue, 12 Nov 2024 07:06:10 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:df884d191789964f64b8f69e6644c8e80dfa1d4fed44444775efca614b97b924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5831321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cecd4d8e08d3c9bdb20a6cbef7bc40e0c5e94cd64e3c995945b38a99398bc06a`

```dockerfile
```

-	Layers:
	-	`sha256:ca3baf0abd20415bac275244c72fc2ac857cff3b7b870b2371d09f270af4bf72`  
		Last Modified: Tue, 12 Nov 2024 07:06:09 GMT  
		Size: 5.8 MB (5776679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:592b7590a779a9b7388e32d35d9a35e4b483b56e2f0614e3526c1cdfcc00231a`  
		Last Modified: Tue, 12 Nov 2024 07:06:08 GMT  
		Size: 54.6 KB (54642 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:0d1b2bf16b580982bd5f879b5180feac7f06540e1cf2bfe5cf6fbccfc484fd98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (158967611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ab317eac1c778efb1423af5a760fd2996c34c303294450f14eda534a7fb48d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 26 Sep 2024 18:03:00 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV LANG=en_US.utf8
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PG_MAJOR=16
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PG_VERSION=16.4-1.pgdg120+2
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Sep 2024 18:03:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Sep 2024 18:03:00 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 18:03:00 GMT
STOPSIGNAL SIGINT
# Thu, 26 Sep 2024 18:03:00 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Sep 2024 18:03:00 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12d5eb7003ab53b071fa65e3c4bdaf6e81e663753b614c23331de2fb77c28be`  
		Last Modified: Tue, 12 Nov 2024 07:30:48 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4804acc3c3f3ad0b659317fcc76e22e4bfab71b4af7702233415c8b83be65a90`  
		Last Modified: Tue, 12 Nov 2024 07:30:48 GMT  
		Size: 4.4 MB (4391039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f666d08df473b710b9352f09dd53c6995fd1b483175dd909f718156530953fd7`  
		Last Modified: Tue, 12 Nov 2024 07:30:48 GMT  
		Size: 1.4 MB (1412679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bedf4129e98367d02a2e978da16ee5e8be915fd7acaf957f1f722f236a247c`  
		Last Modified: Tue, 12 Nov 2024 07:30:48 GMT  
		Size: 8.1 MB (8120431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0a956114c91beb79dcc1abdb69e0cc300b2dc6a4c5c1f97884b44074f7645f`  
		Last Modified: Tue, 12 Nov 2024 07:30:49 GMT  
		Size: 1.1 MB (1096719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5000dba33ff2e5569ead76c5064bd9fab7fb2960c7ed1ec926ac116e975d0af`  
		Last Modified: Tue, 12 Nov 2024 07:30:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce0ebdd4ff0fae2866af2f32420891ddcfb731e002f78f22742b716468a6d94`  
		Last Modified: Tue, 12 Nov 2024 07:30:49 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98cb35a025fcc92e75c531a7b0f850ebe272d6f16e69c4dba69c04b9a992846c`  
		Last Modified: Tue, 12 Nov 2024 07:41:14 GMT  
		Size: 116.4 MB (116434866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08b391713845501e6ee2966edc737ebc5295736da3e7d362645103b583ace2d`  
		Last Modified: Tue, 12 Nov 2024 07:41:12 GMT  
		Size: 9.9 KB (9923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73cf177e08ee08769173320e07dc935b8b6f0f063c85dea1ea29e338fc0e0b35`  
		Last Modified: Tue, 12 Nov 2024 07:41:12 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e4575730f10cffa396dde76d12199f66ed3ec0aa4e8a469c8b85a2a6f6855c`  
		Last Modified: Tue, 12 Nov 2024 07:41:12 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fec16374ceb4508577cb42ad48bae3f7dfed3a20ed707b39f04a9adc6423f71`  
		Last Modified: Tue, 12 Nov 2024 07:41:12 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbda505c8a2c255b5d7d50ecfc35823c0abd58bb21d028386f4af9bbc78fa3ac`  
		Last Modified: Tue, 12 Nov 2024 07:41:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:c4182285edef0a589d857e7686625b1c1d08a47d4225cc5433c581ea80e6e0b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5823316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d6e4ae38dbe644641fdb0cfc50ad436891841e1d270391ff878d819733ca5a5`

```dockerfile
```

-	Layers:
	-	`sha256:0b51738c68ed50ad8d0af0964577dab3ad82bff418aa4efc12ba576b34ff4674`  
		Last Modified: Tue, 12 Nov 2024 07:41:11 GMT  
		Size: 5.8 MB (5768738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:823b9d0527562fbd2609bba89bf81e1ecceb53a2d3faddab6be47b68d2dc621a`  
		Last Modified: Tue, 12 Nov 2024 07:41:11 GMT  
		Size: 54.6 KB (54578 bytes)  
		MIME: application/vnd.in-toto+json
