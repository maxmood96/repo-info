## `postgres:16-bookworm`

```console
$ docker pull postgres@sha256:5cbc20689cd4b9416f3e84ce6bd07dfa0314bd0385cb7a5083d946b90052388b
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
$ docker pull postgres@sha256:57c55aefb81a937d21171b7c2266264b5552cb1a4f90459bbdfc417a36883a4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.0 MB (155038644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0a399de9424c2e689fa7c7e89620b83cc37b6c7a9e19eda8883df623ccb26be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:33:21 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 08 May 2026 19:33:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:33:32 GMT
ENV GOSU_VERSION=1.19
# Fri, 08 May 2026 19:33:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 May 2026 19:33:37 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 08 May 2026 19:33:37 GMT
ENV LANG=en_US.utf8
# Fri, 08 May 2026 19:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:33:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 May 2026 19:33:40 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:33:40 GMT
ENV PG_MAJOR=16
# Fri, 08 May 2026 19:33:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Fri, 08 May 2026 19:33:40 GMT
ENV PG_VERSION=16.13-1.pgdg12+1
# Fri, 08 May 2026 19:33:52 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 08 May 2026 19:33:52 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 08 May 2026 19:33:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 08 May 2026 19:33:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 08 May 2026 19:33:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 08 May 2026 19:33:52 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 08 May 2026 19:33:52 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:33:52 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 08 May 2026 19:33:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:33:52 GMT
STOPSIGNAL SIGINT
# Fri, 08 May 2026 19:33:52 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 08 May 2026 19:33:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8748e0f0e19a700d254f00d06841ca3bedac0cdcb61fde3086c42e88d9a7d2`  
		Last Modified: Fri, 08 May 2026 19:34:12 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd9aa235a7fcb405d5e2d64ef769e5e3c2a33fc9ce3c4d41f686af3ba78b070`  
		Last Modified: Fri, 08 May 2026 19:34:12 GMT  
		Size: 4.5 MB (4534255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a11cb02794604d3fe0e96a70d144cf1a14c8c101c12320c0fbde434d52c4d55`  
		Last Modified: Fri, 08 May 2026 19:34:12 GMT  
		Size: 1.2 MB (1249546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a90f5711b608892db66205a3106db948051eca93790d4c289a233efcdb7b37`  
		Last Modified: Fri, 08 May 2026 19:34:12 GMT  
		Size: 8.1 MB (8066463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70088c6ecf2ed406d1a0c75011834376ae8c97fb839e5551b556127bb89655d`  
		Last Modified: Fri, 08 May 2026 19:34:13 GMT  
		Size: 1.2 MB (1196386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2fb47bde63f507ee1a9ba958041398e2d756761ac60006fb579d6d3b3fa501`  
		Last Modified: Fri, 08 May 2026 19:34:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e362a5f4dff0a3fde91651a5d3b4624047ae2787e49fdb32e536d25a941720`  
		Last Modified: Fri, 08 May 2026 19:34:14 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad4d86849e8464ac0cd6a8ba8e8f9f84435930e7d1cbc9362c00004fff413eb`  
		Last Modified: Fri, 08 May 2026 19:34:17 GMT  
		Size: 111.7 MB (111734738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f9cbb7e3d721ae8fffce65fc73d9d25832c891e72f2978f54a240afeea7f8e`  
		Last Modified: Fri, 08 May 2026 19:34:15 GMT  
		Size: 10.0 KB (9967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16857e6e29566e3b79cc3f47ad919d279895f25f4c3f329130844300d3810c3a`  
		Last Modified: Fri, 08 May 2026 19:34:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344ec23c63fbca2b1fc62150ea3139799d9d2b1b869319fa1e06b35e60c1b1f8`  
		Last Modified: Fri, 08 May 2026 19:34:15 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f05bec41aaff3393199b90b62a83cb02cce6671100668f285188be38b21616`  
		Last Modified: Fri, 08 May 2026 19:34:16 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef57ae80bcbfec1847433f29b38fcfd17222b149106ce8241623bd8433f63e7`  
		Last Modified: Fri, 08 May 2026 19:34:16 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:52fb696a9de436b5f78cc45f78ba302302d8ffd03cfe0edd61b4ef1b7275b869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5962852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569fac9d295023781081d9010c444ae912ddc0793ad3b44f4ba4e49e5e188def`

```dockerfile
```

-	Layers:
	-	`sha256:520885d2fd51590ff0d71011921491fc69f4ab79e2ba847bbe897f40d0267a4f`  
		Last Modified: Fri, 08 May 2026 19:34:12 GMT  
		Size: 5.9 MB (5909556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9460568d60cd2bf7f22f3736ca42773f50a3676bade81f1a89a9b8bf2d446bd8`  
		Last Modified: Fri, 08 May 2026 19:34:12 GMT  
		Size: 53.3 KB (53296 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:cf4d1e4dd539b42ecda95b9cb8edf22c7bad71ab8c1c3a669fd25ae0f4802259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.1 MB (148053918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ca77c131cf223dfcbfc0b9a1489d124f7f5f07a89c3b92c6ec948b471cd64ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:41:14 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 08 May 2026 20:41:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:41:30 GMT
ENV GOSU_VERSION=1.19
# Fri, 08 May 2026 20:41:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 May 2026 20:41:36 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 08 May 2026 20:41:36 GMT
ENV LANG=en_US.utf8
# Fri, 08 May 2026 20:41:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:41:42 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 May 2026 20:41:42 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 20:41:42 GMT
ENV PG_MAJOR=16
# Fri, 08 May 2026 20:41:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Fri, 08 May 2026 20:41:42 GMT
ENV PG_VERSION=16.13-1.pgdg12+1
# Fri, 08 May 2026 20:56:19 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 08 May 2026 20:56:19 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 08 May 2026 20:56:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 08 May 2026 20:56:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 08 May 2026 20:56:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 08 May 2026 20:56:20 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 08 May 2026 20:56:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:56:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 08 May 2026 20:56:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 20:56:20 GMT
STOPSIGNAL SIGINT
# Fri, 08 May 2026 20:56:20 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 08 May 2026 20:56:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0496e5b1fd9475851f8b3578080061a05ea61be300ea5a278a4a08a883855adc`  
		Last Modified: Fri, 08 May 2026 18:33:05 GMT  
		Size: 25.8 MB (25765670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6473c132b40c6a4690034661d29c1309518ad263c9c6ffad30b99503e97ae3`  
		Last Modified: Fri, 08 May 2026 20:56:39 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb6e22fa207eefcd65fbb3530c4ac96afc23b3e93b36541ab91080f6081d064`  
		Last Modified: Fri, 08 May 2026 20:56:39 GMT  
		Size: 4.2 MB (4151320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf0cb0a0b3dc811c4531394b5339cd419532421ddeb12af2512c48c83c12ae7`  
		Last Modified: Fri, 08 May 2026 20:56:39 GMT  
		Size: 1.2 MB (1220307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df81c60a93e1fba92a22c2119a57950e354dd74cfc679cc980d735facc307e2`  
		Last Modified: Fri, 08 May 2026 20:56:40 GMT  
		Size: 8.1 MB (8066602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ff00a106eeffddabe006f8c673c2d2150358a3b83310adda0c5f5d9a5fc977`  
		Last Modified: Fri, 08 May 2026 20:56:40 GMT  
		Size: 1.2 MB (1195085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5525059b9fbfbdfc4329b4d70000e040352b035495343a4e39d178587837b61c`  
		Last Modified: Fri, 08 May 2026 20:56:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc8803d7f5b06b0a840316fb04b2efb3242c987e10b7094e27d46aa57f0e83c`  
		Last Modified: Fri, 08 May 2026 20:56:40 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09f4550aeb9893ff09db3908cab78b4722403c9321a3b4993d85e1e39ba8b2a`  
		Last Modified: Fri, 08 May 2026 20:56:44 GMT  
		Size: 107.6 MB (107633958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1596184e74c9efbc7c72b941c878c38e0ac3093a2e511a4e688f5d4b1d9e8628`  
		Last Modified: Fri, 08 May 2026 20:56:42 GMT  
		Size: 10.0 KB (9972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77253812edecea766d0aa4721e60d32e85087b80df9815959c0fbf51ecc566bc`  
		Last Modified: Fri, 08 May 2026 20:56:42 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82982be5d97012ff33dd2be9307987903bbafda2f1071ea6405ef59381a27b10`  
		Last Modified: Fri, 08 May 2026 20:56:42 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782ed1344929968d4621bfc0f1061a870a4f41b8e868e9f809279742e0cdef1a`  
		Last Modified: Fri, 08 May 2026 20:56:43 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1457c36b455c288ec14884c03676c6163a2b375c0d3476eb63dbbc68c0847f44`  
		Last Modified: Fri, 08 May 2026 20:56:43 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:86b1bfb7979c88be26741832f053a315d726e13e950f08bf308a3878c1c2c403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5981154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff3726ac8f273b757e26d7c7863800827f3ed148e2c2468bb6c09b5c813b0fb`

```dockerfile
```

-	Layers:
	-	`sha256:3fc88d9d81cc5b5f1ebf75b3e1a5373debf1a28661fd8ca8f670c31d3ac04457`  
		Last Modified: Fri, 08 May 2026 20:56:39 GMT  
		Size: 5.9 MB (5927653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1b48e14d9021bc112202c5d0b88e8912b6c7c9ab9f181708c88e16cfc8dad3c`  
		Last Modified: Fri, 08 May 2026 20:56:39 GMT  
		Size: 53.5 KB (53501 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:42419be381540f7e65ec9d7cfb06ebff9b8e90d7b7f25a711e6d0993e1b40ac8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143093116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45419dff7af41dddcce3bc4c1964872eb89770a584a515286ad6b98896c57813`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:29:08 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 08 May 2026 19:29:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:29:20 GMT
ENV GOSU_VERSION=1.19
# Fri, 08 May 2026 19:29:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 May 2026 19:29:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 08 May 2026 19:29:26 GMT
ENV LANG=en_US.utf8
# Fri, 08 May 2026 19:29:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:29:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 May 2026 19:29:30 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:29:30 GMT
ENV PG_MAJOR=16
# Fri, 08 May 2026 19:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Fri, 08 May 2026 19:29:30 GMT
ENV PG_VERSION=16.13-1.pgdg12+1
# Fri, 08 May 2026 19:43:49 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 08 May 2026 19:43:49 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 08 May 2026 19:43:49 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 08 May 2026 19:43:49 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 08 May 2026 19:43:49 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 08 May 2026 19:43:49 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 08 May 2026 19:43:49 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:43:49 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 08 May 2026 19:43:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:43:49 GMT
STOPSIGNAL SIGINT
# Fri, 08 May 2026 19:43:49 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 08 May 2026 19:43:49 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1c5a0b31b39e45b38b0c73a2e506eb60bb1de512092b4765e565207648f55da2`  
		Last Modified: Fri, 08 May 2026 18:37:03 GMT  
		Size: 23.9 MB (23941406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7771b277c829c885335f437ca05aa44428d494fc8801c5d1114b89488b609a27`  
		Last Modified: Fri, 08 May 2026 19:44:07 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c62cc0230b9c5c6e9a181993610c8e91e30e530c07e0f9985eb73d859272588`  
		Last Modified: Fri, 08 May 2026 19:44:07 GMT  
		Size: 3.7 MB (3742715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc27a7195d25947d598ac4dfdc21ea2af4d2b559f71d02c16ef42a1740d9176d`  
		Last Modified: Fri, 08 May 2026 19:44:07 GMT  
		Size: 1.2 MB (1216149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c996730013c96ba1140f1831004ed4d2f5e32bda01ee1fb610ee5454523824`  
		Last Modified: Fri, 08 May 2026 19:44:08 GMT  
		Size: 8.1 MB (8066428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0ed96a0b2e16dbe0e2cbaed1e91b9804f1320d0a744cae561901c78a54422a`  
		Last Modified: Fri, 08 May 2026 19:44:09 GMT  
		Size: 1.1 MB (1067273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e068cfa0e9ceae88d608b54186da0ddfdfbe198b63881593c6ae7f1a5ce30d36`  
		Last Modified: Fri, 08 May 2026 19:44:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0400b56a0a4376f7ef1d65044f4f4224443e05b65929fd86d2586878b70507f`  
		Last Modified: Fri, 08 May 2026 19:44:09 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32d4d1a573dd48e8c770c610f3eb59baa08b94c63cf0c1b41e8f105cec1cb3f`  
		Last Modified: Fri, 08 May 2026 19:44:12 GMT  
		Size: 105.0 MB (105038161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df1fb6bce719e1880a9fbe1e88aac822ac9e69391d57524456a41db161453d6`  
		Last Modified: Fri, 08 May 2026 19:44:10 GMT  
		Size: 10.0 KB (9976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c946d3b2b1eb206a64ec0e7ee62b8732b31ba650e1dfe2dfbc07bce2e7afd16`  
		Last Modified: Fri, 08 May 2026 19:44:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6acaef96f961fdd95708492bd7ef31151515598edef869b32eb6d943626ac4`  
		Last Modified: Fri, 08 May 2026 19:44:10 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e90cef78f8d8ceba5a7f5ecfc798e874b88c52814c20571a6a49cbad9f9e09`  
		Last Modified: Fri, 08 May 2026 19:44:11 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64e732f96a10a5decece651814031ab3264167e8df4cad456c3c2591c326b09`  
		Last Modified: Fri, 08 May 2026 19:44:11 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:31acc1dba75b2bee3c15b23104a77c0c4a57e19a45af37dd93fcd09f285aeaa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5980411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a12196ad3144a77b7a3d8fc96d8fe3f99b5cd89e829d2469f93c453abc911e9`

```dockerfile
```

-	Layers:
	-	`sha256:dd42b5fda862e98345a8d6e9442ee81f502e7884b48b8d357f59d1d9c75d06af`  
		Last Modified: Fri, 08 May 2026 19:44:07 GMT  
		Size: 5.9 MB (5926908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d5958da65c17c68384aa87544a30f2a31bbda9470594742c856e814f8996ded`  
		Last Modified: Fri, 08 May 2026 19:44:07 GMT  
		Size: 53.5 KB (53503 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:494df59df434a3a83b698c01d0ae28d486d68e9675877d3341287f054a653be2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.0 MB (153021703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:477b63deb3e45f99ebf7a3970807e145173d026c55e16b4ef85f74ce5074460e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:34:34 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 08 May 2026 19:34:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:34:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 08 May 2026 19:34:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 May 2026 19:34:49 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 08 May 2026 19:34:49 GMT
ENV LANG=en_US.utf8
# Fri, 08 May 2026 19:34:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:34:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 May 2026 19:34:53 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:34:53 GMT
ENV PG_MAJOR=16
# Fri, 08 May 2026 19:34:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Fri, 08 May 2026 19:34:53 GMT
ENV PG_VERSION=16.13-1.pgdg12+1
# Fri, 08 May 2026 19:35:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 08 May 2026 19:35:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 08 May 2026 19:35:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 08 May 2026 19:35:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 08 May 2026 19:35:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 08 May 2026 19:35:06 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 08 May 2026 19:35:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:35:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 08 May 2026 19:35:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:35:06 GMT
STOPSIGNAL SIGINT
# Fri, 08 May 2026 19:35:06 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 08 May 2026 19:35:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2394ba5fe6a2f623809c2263f7ba4345ef5e1c874ce851b8b16b8fe209d62b5d`  
		Last Modified: Fri, 08 May 2026 19:35:25 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0de3d39e9af43604233fb3ba3f088693425c4dc36cb68ab0fd3b009a007034`  
		Last Modified: Fri, 08 May 2026 19:35:25 GMT  
		Size: 4.5 MB (4519513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868d24919a0077eb607bda5bfe6aaac1668185ed402e5b828f12e84fa4c91718`  
		Last Modified: Fri, 08 May 2026 19:35:25 GMT  
		Size: 1.2 MB (1203301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357b26d4b4f16f5b8dd58f3f63a6c0df3ef2dfba2af4b44ad80351b0e57567e6`  
		Last Modified: Fri, 08 May 2026 19:35:26 GMT  
		Size: 8.1 MB (8066477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d119a67c2c6259f0f152461564972254067a2c4addb5189cf61ce41b7818d882`  
		Last Modified: Fri, 08 May 2026 19:35:26 GMT  
		Size: 1.1 MB (1109008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62f9eb2a271495b7db812cacf6f9032accf9729b2ebeef1b8a02e50f34ee65e`  
		Last Modified: Fri, 08 May 2026 19:35:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6839103a8eef9b074e86fa499b02c362c99a9cd2e23423d97ff59d17e8e4414d`  
		Last Modified: Fri, 08 May 2026 19:35:27 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f1adbfc48bec330e30e4fe972ef9b65ce37dc1d7701d541d53c8ed1fba31af`  
		Last Modified: Fri, 08 May 2026 19:35:30 GMT  
		Size: 110.0 MB (109986262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e01db0645f5f290729ba8a54eee73018cd758e36be599e2ce10edab5f8a9d24`  
		Last Modified: Fri, 08 May 2026 19:35:28 GMT  
		Size: 10.0 KB (9969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf399f3b3d42ee6e49a366a1d735ba8775ff989bc5c9dcd2b2db10921a21d8e`  
		Last Modified: Fri, 08 May 2026 19:35:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb481bdca055a7e08c46ff4f6382016a5a2a080478489fdd07df1a20af57d889`  
		Last Modified: Fri, 08 May 2026 19:35:28 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc0d5a7223adf3f0894b1c31444cce99081c2ec4d190fcee06987af734f6661`  
		Last Modified: Fri, 08 May 2026 19:35:29 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622121d0d4a94b33672b98f1f6a35fe99e2a2564edfb95d6e6475a4b34219b27`  
		Last Modified: Fri, 08 May 2026 19:35:29 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:8372cc8ea563f34bace836c7a6536c44c043d920bdb497e4e7e6276c9c150c95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5969408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7358551cdf8772ad1e8b5e4b11a1f82922b48cc744649d198873a7899f87e6b`

```dockerfile
```

-	Layers:
	-	`sha256:74f6a56e8e832f8239a93ed99e2c372f8454636e2c21fd0c8ff9c7df1e47fc32`  
		Last Modified: Fri, 08 May 2026 19:35:26 GMT  
		Size: 5.9 MB (5915867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf4c59beb66416c7cdc48795bbef0bf327b4ee8c6f8d34eff6231b82d4df7c27`  
		Last Modified: Fri, 08 May 2026 19:35:25 GMT  
		Size: 53.5 KB (53541 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:3c5139f0c68c974fb5f73ec14bdf3b8c4102c285ab5d5fa7541900b91f1735ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.8 MB (163828130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cda207cda6961459b266c1db7b6ef3ce3e3c4487289fa910b7028d586aa45ed5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:32:04 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 08 May 2026 19:32:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:32:17 GMT
ENV GOSU_VERSION=1.19
# Fri, 08 May 2026 19:32:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 May 2026 19:32:22 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 08 May 2026 19:32:22 GMT
ENV LANG=en_US.utf8
# Fri, 08 May 2026 19:32:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:32:25 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 May 2026 19:32:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:32:26 GMT
ENV PG_MAJOR=16
# Fri, 08 May 2026 19:32:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Fri, 08 May 2026 19:32:26 GMT
ENV PG_VERSION=16.13-1.pgdg12+1
# Fri, 08 May 2026 19:43:49 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 08 May 2026 19:43:50 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 08 May 2026 19:43:50 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 08 May 2026 19:43:50 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 08 May 2026 19:43:50 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 08 May 2026 19:43:50 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 08 May 2026 19:43:50 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:43:50 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 08 May 2026 19:43:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:43:50 GMT
STOPSIGNAL SIGINT
# Fri, 08 May 2026 19:43:50 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 08 May 2026 19:43:50 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d90092c8edd324a692787fd4188906e71211941e12cf7df45f29d2b706aba9ab`  
		Last Modified: Fri, 08 May 2026 18:30:44 GMT  
		Size: 29.2 MB (29221767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206383b9708f0dbc0bddbf52dd4f621eb4d288e4de7d402dcf03eafab5741167`  
		Last Modified: Fri, 08 May 2026 19:44:10 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d87e2eb56d956b5acefc27abc96f35c731f03208d919f0bf7aa6c7c34128de8`  
		Last Modified: Fri, 08 May 2026 19:44:11 GMT  
		Size: 5.0 MB (4966154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c65083d575774035b2bd2a04abfcbd65d172613039c94da678d92ec14e78e43`  
		Last Modified: Fri, 08 May 2026 19:44:10 GMT  
		Size: 1.2 MB (1218673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfb5bbec1d475853c4dae6d5582b4168cd1a8580def37f2bb1f11e57751b769`  
		Last Modified: Fri, 08 May 2026 19:44:11 GMT  
		Size: 8.1 MB (8066471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8f64d56e79a9d0f8b8d4ceb82824182b40cb4f3757a20535db7564934cf3ba`  
		Last Modified: Fri, 08 May 2026 19:44:11 GMT  
		Size: 1.1 MB (1137493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4afd8b9f69c744d0a632af2cc848b0cb45c3ea2fd3e4478fbde20e75e17bc8f`  
		Last Modified: Fri, 08 May 2026 19:44:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6306e36a4055bb10c607e4f54473106077e73c7b61764acc24491cae0ab571a5`  
		Last Modified: Fri, 08 May 2026 19:44:12 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d444f427e7cfad7bc18bbc7861e9a268ce2cd2e7583042b73f3db115d5b136a0`  
		Last Modified: Fri, 08 May 2026 19:44:16 GMT  
		Size: 119.2 MB (119196596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda81c9f305c5c64c4b9610670808d2ecf97e996cbdcba6fa1fc35435d16558a`  
		Last Modified: Fri, 08 May 2026 19:44:13 GMT  
		Size: 10.0 KB (9970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed79927929b69caeb29659c6d5f31012e822687f0906b3caa85a99cd88e0a80`  
		Last Modified: Fri, 08 May 2026 19:44:13 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4d77eb8027e4eb9cdee691d2da9ed1fedf906869700ca9962b052e07aca2e1`  
		Last Modified: Fri, 08 May 2026 19:44:13 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec6f1538ca7b1ba4164ceff4b77d18be074a08734554c6cbc102d056564c52e`  
		Last Modified: Fri, 08 May 2026 19:44:14 GMT  
		Size: 6.1 KB (6100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf670405a911173f1437a7c4ae95bde9441aba3df12cb29b68bbc38acb0b174`  
		Last Modified: Fri, 08 May 2026 19:44:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:b8fb5b891de63e01f5477f77d2e01d82002193af679804eddc11792325430ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5979048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b4f6693f3ea9c707ea2b9e8916274aa683ad334f5fd1fa188fbaf8a9cbe4d79`

```dockerfile
```

-	Layers:
	-	`sha256:cab02b5a6754edd1d9a7bd5e18a68f05052f99caa0a2388e1918c6080f8d68d2`  
		Last Modified: Fri, 08 May 2026 19:44:11 GMT  
		Size: 5.9 MB (5925796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3aca0bb006ede40311cb318948d4c7a649fb326b801fa971393a9693e8bb91f7`  
		Last Modified: Fri, 08 May 2026 19:44:10 GMT  
		Size: 53.3 KB (53252 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:56600f3ccba67f3af404e1267c0ff495ef3218616a6313c5784678ec8643c133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.9 MB (153905907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1b869ec5eeae66ba1b0b7fe8fac788fcc90e1607dc86cda791da8cef664751`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 07:10:31 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 22 Apr 2026 07:11:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 07:11:42 GMT
ENV GOSU_VERSION=1.19
# Wed, 22 Apr 2026 07:11:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Apr 2026 07:12:10 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 22 Apr 2026 07:12:10 GMT
ENV LANG=en_US.utf8
# Wed, 22 Apr 2026 07:12:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 07:12:31 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 22 Apr 2026 07:12:33 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 07:12:33 GMT
ENV PG_MAJOR=16
# Wed, 22 Apr 2026 07:12:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Wed, 22 Apr 2026 07:12:33 GMT
ENV PG_VERSION=16.13-1.pgdg12+1
# Wed, 22 Apr 2026 10:46:51 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 22 Apr 2026 10:46:53 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 22 Apr 2026 10:46:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 22 Apr 2026 10:46:55 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 22 Apr 2026 10:46:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 22 Apr 2026 10:46:57 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 22 Apr 2026 10:46:58 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 10:47:00 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 22 Apr 2026 10:47:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 10:47:00 GMT
STOPSIGNAL SIGINT
# Wed, 22 Apr 2026 10:47:00 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 22 Apr 2026 10:47:00 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1bdc534ce4a1e0d7ff161c131dd4f30a3e0afa362f1cd64aaaf83f0d7b346bfc`  
		Last Modified: Wed, 22 Apr 2026 01:26:21 GMT  
		Size: 28.5 MB (28526265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b23087cb6164c5baede5f0b58942609b1d2e984c90cb0e1550699188851a859`  
		Last Modified: Wed, 22 Apr 2026 08:25:43 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac16282694b6f6b51fb726802ef171244d8c0c3ccf33b831aaefd3065400f1bb`  
		Last Modified: Wed, 22 Apr 2026 08:25:44 GMT  
		Size: 4.5 MB (4475225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f87c24db2efa4ebc447965e614aa656b8aa728f3dd61c411e2061f29ded1360`  
		Last Modified: Wed, 22 Apr 2026 08:25:43 GMT  
		Size: 1.2 MB (1159221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5738ae8dbf29019acb67c3cf9ed5cf68bad522384714efa0a2f9878d99c023f`  
		Last Modified: Wed, 22 Apr 2026 08:25:44 GMT  
		Size: 8.1 MB (8066656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10d84d51ba40139d8c3cadc934b639fb067807bf933d0f19a09158d93fe8524`  
		Last Modified: Wed, 22 Apr 2026 08:25:44 GMT  
		Size: 1.2 MB (1182923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb134c034bf1a9d288fa66f2176919e7dcf9202e73a24d63f4ad9f600ee674e`  
		Last Modified: Wed, 22 Apr 2026 08:25:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e08c7de82ead266db979d60e3c9146a8cd3d572449aab30f810debda150d42`  
		Last Modified: Wed, 22 Apr 2026 08:25:45 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69af03d19785f94c4b0b3247b2c833e9d8de96a06ca4d7ab0f1bbc75e9fd7559`  
		Last Modified: Wed, 22 Apr 2026 10:49:05 GMT  
		Size: 110.5 MB (110474640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efbd26ac6406427e53d3cb638dbca25bce21a86bddbd510b9d073a2cc0b2172`  
		Last Modified: Wed, 22 Apr 2026 10:48:54 GMT  
		Size: 10.0 KB (9968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499b92a47ed7e17f42de0be4d967727a49ab48539d3f3d4d9ee19cde329f15dc`  
		Last Modified: Wed, 22 Apr 2026 10:48:54 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feced719aaa5a63c3c897f765308502a97bf45fb42b5093d8f5284b15f802eed`  
		Last Modified: Wed, 22 Apr 2026 10:48:54 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f084b6fb5ee742f09ec3946e922f7109e6ab0fc0a000fda6c8bc16e81d94252`  
		Last Modified: Wed, 22 Apr 2026 10:48:55 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139c627ac70519fbff50fc2635c8180a3b974df0923c9d13fc059491af5d6437`  
		Last Modified: Wed, 22 Apr 2026 10:48:55 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:72f6ccff6a26900dc6cb229cc8b8e541b6b70babea02b88a006c8b93bb82d177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 KB (53162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:776631e1e612dd00d366ec2be6cee8d1f0d3e46896318acd36b23479a5bab09c`

```dockerfile
```

-	Layers:
	-	`sha256:f01dc0978ca97a4e3bf81c1af93541e600eea25df1bbc4e6508056349a4b30fd`  
		Last Modified: Wed, 22 Apr 2026 10:48:53 GMT  
		Size: 53.2 KB (53162 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:da6fa7c8a039f83b8654a1adc0ebcbcc93cdd9e1d69861ab714e6c0fb8f79667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167788480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf4a2777575ac592ca662ac1ef2dee409f94cf50a07e4f72b0b4a5e139e78deb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 22:06:52 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 08 May 2026 22:07:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:07:13 GMT
ENV GOSU_VERSION=1.19
# Fri, 08 May 2026 22:07:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 May 2026 22:07:21 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 08 May 2026 22:07:21 GMT
ENV LANG=en_US.utf8
# Fri, 08 May 2026 22:07:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:07:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 May 2026 22:07:29 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 22:07:29 GMT
ENV PG_MAJOR=16
# Fri, 08 May 2026 22:07:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Fri, 08 May 2026 22:07:29 GMT
ENV PG_VERSION=16.13-1.pgdg12+1
# Fri, 08 May 2026 22:10:54 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 08 May 2026 22:10:55 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 08 May 2026 22:10:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 08 May 2026 22:10:55 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 08 May 2026 22:10:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 08 May 2026 22:10:55 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 08 May 2026 22:10:55 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 22:10:56 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 08 May 2026 22:10:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 22:10:56 GMT
STOPSIGNAL SIGINT
# Fri, 08 May 2026 22:10:56 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 08 May 2026 22:10:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0e29ea7436ed4beb1c38bcfee44589407e49fc690669b42b35db33a9588e820a`  
		Last Modified: Fri, 08 May 2026 19:44:06 GMT  
		Size: 32.1 MB (32078453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5eb32d4435eca1a6b3ca4902a373ba25f5297f05de0d149a0709a90b7ec1759`  
		Last Modified: Fri, 08 May 2026 22:08:42 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd7517567a07b79c6a9914a7b25506a363f17fb5401752c73d6f34e594309f5`  
		Last Modified: Fri, 08 May 2026 22:08:42 GMT  
		Size: 5.4 MB (5368597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc1be6e226cae2878d88644a13fc0a2c6745aceada5dee6fe1e55a1f4924aac`  
		Last Modified: Fri, 08 May 2026 22:08:42 GMT  
		Size: 1.2 MB (1208225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2a4f5fbc8e702eb075177bc8edb10be5d7f54953f645b4cf915a5ea8dc0f33`  
		Last Modified: Fri, 08 May 2026 22:08:42 GMT  
		Size: 8.1 MB (8066517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a767e16edf602eaf29e66ea14d171f425c0fe9fd18185b67b8c93271f3d2c8d3`  
		Last Modified: Fri, 08 May 2026 22:08:43 GMT  
		Size: 1.3 MB (1283630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e1aa66ae5559097568ba79a7894b072af66b6a1d9544c5cbb610d20c033760`  
		Last Modified: Fri, 08 May 2026 22:08:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8341b75bac864b473b052c616c8e7e99c2af8703dd7aec0eaf858b591842bc18`  
		Last Modified: Fri, 08 May 2026 22:08:44 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db08aafd31b223b8226efdbf7417cc6338d01b8c032ef0b7aa61c0868db0abe`  
		Last Modified: Fri, 08 May 2026 22:11:47 GMT  
		Size: 119.8 MB (119762091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8e05444f5ece56d7971e3c32177a15fcb5bbfca32c7b3762bf424b12a18e1f`  
		Last Modified: Fri, 08 May 2026 22:11:39 GMT  
		Size: 10.0 KB (9970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19085a191d2d528570349782a123af6f64bb7e9f92817a917c5f6080d6fc93df`  
		Last Modified: Fri, 08 May 2026 22:11:39 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c8cdaae574aa8ddc16b5dac5c9caeadd878edc5c019a7bef3ce5fd95ecb403`  
		Last Modified: Fri, 08 May 2026 22:11:39 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e9ba7a8912400b09c0e844e517431ee52dcfec9bd2cf88de2894d9a1e2d725`  
		Last Modified: Fri, 08 May 2026 22:11:40 GMT  
		Size: 6.1 KB (6093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925250f482b84832ad993cb2c6fee2dcc33984b0de68ba51c501099cecb19820`  
		Last Modified: Fri, 08 May 2026 22:11:40 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:3c24ef7e431364f1874badf046a3d714313a880a3a919b54a0eab0c65cbec9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5970267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30069ef27e5a7ffb963f604c175d91c166ae4151163571bd76bf584d05c99243`

```dockerfile
```

-	Layers:
	-	`sha256:c29cb1ac5cb8fe789144fd4ecbb4ec4aba960582e6cdcc557af86491503a30fc`  
		Last Modified: Fri, 08 May 2026 22:11:39 GMT  
		Size: 5.9 MB (5916917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0df43806bea4e4ad02dbafc2650938dcf49beb7345c532081e00d820271b2e2f`  
		Last Modified: Fri, 08 May 2026 22:11:39 GMT  
		Size: 53.4 KB (53350 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:8f4b6cc69d258ebb89973eda5083499233c16786e6643e6c2bf71c20178e3616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164267621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb2f01e5de492a3463cfbb4a325e9cb340b8aaf675e2c397673837360e531124`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:09:36 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 08 May 2026 20:09:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:10:08 GMT
ENV GOSU_VERSION=1.19
# Fri, 08 May 2026 20:10:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 May 2026 20:10:17 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 08 May 2026 20:10:17 GMT
ENV LANG=en_US.utf8
# Fri, 08 May 2026 20:10:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:10:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 May 2026 20:10:24 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 20:10:24 GMT
ENV PG_MAJOR=16
# Fri, 08 May 2026 20:10:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Fri, 08 May 2026 20:10:24 GMT
ENV PG_VERSION=16.13-1.pgdg12+1
# Fri, 08 May 2026 20:42:49 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 08 May 2026 20:42:49 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 08 May 2026 20:42:49 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 08 May 2026 20:42:49 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 08 May 2026 20:42:49 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 08 May 2026 20:42:49 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 08 May 2026 20:42:49 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:42:49 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 08 May 2026 20:42:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 20:42:49 GMT
STOPSIGNAL SIGINT
# Fri, 08 May 2026 20:42:49 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 08 May 2026 20:42:49 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204b870d6fb6f324cac69e2dc3f77c282d05602967e604d2f33965cba0d635d8`  
		Last Modified: Fri, 08 May 2026 20:27:21 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5ab83cefe8347b2f43c5918b6212b9d269a55efd1928d66318347794892879`  
		Last Modified: Fri, 08 May 2026 20:27:20 GMT  
		Size: 4.4 MB (4391372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6583a3676d3a3569baabe46bd88fbf602ed21094feab0da984de4e6304b83ac6`  
		Last Modified: Fri, 08 May 2026 20:27:21 GMT  
		Size: 1.2 MB (1222932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420c685a29ab37d2b09935266e0307ab612a6d5e53a2756588ac40d5026c75a5`  
		Last Modified: Fri, 08 May 2026 20:27:21 GMT  
		Size: 8.1 MB (8120845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb9bf671e27e2eacdce43a2e44f61eb0af9a2fb7bc60df7287238b3f20c8c50`  
		Last Modified: Fri, 08 May 2026 20:27:22 GMT  
		Size: 1.1 MB (1097190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3097b9e40f971ea0488cbabdfb53e7b228c558da35b79f5d9fc3fe95d0468d00`  
		Last Modified: Fri, 08 May 2026 20:27:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb797ac9c521650d560c327fdfc0fc615fd4fb98f35c2d4f3b863cd8b1e1ad2`  
		Last Modified: Fri, 08 May 2026 20:27:22 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa09348aac91fd20325b830e857e2b3b38dc76f2a8ba970142185ac9d5b39631`  
		Last Modified: Fri, 08 May 2026 20:43:26 GMT  
		Size: 122.5 MB (122522706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6371abfdc76cd6385969d99b201cccd30129fc9a38880db33f05f435a3c97c`  
		Last Modified: Fri, 08 May 2026 20:43:24 GMT  
		Size: 10.0 KB (9975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721aac4f7514174dd78773b3778b5669fcde5708066cee4f0922d9d3db817d57`  
		Last Modified: Fri, 08 May 2026 20:43:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbda620d145962664ce52f31548b336b1ee5a3592e775eef05c94a85a9135b0a`  
		Last Modified: Fri, 08 May 2026 20:43:24 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dadc57a7d44ff82847d76a1d10d6f7ee1aa71c0c4ee65dc4a3e5099ec3023429`  
		Last Modified: Fri, 08 May 2026 20:43:25 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a9ed4d6b648d26246e3793b0d60dc2d5f3b37c4b864573f648438da7a1a97a`  
		Last Modified: Fri, 08 May 2026 20:43:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:8e5169ea202ccb2e58e886477b8c976b98196f1b5174e2f2fd9d076cbd13b812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5975568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4600d78dc46f22e8893b320d6aa1d0159be77d232411e7d90385afd3031aa1`

```dockerfile
```

-	Layers:
	-	`sha256:3864a7637123c342fc09d66574fdeb27f4329f48898d727cb4fe5629cd650bb7`  
		Last Modified: Fri, 08 May 2026 20:43:24 GMT  
		Size: 5.9 MB (5922272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31b263b488c1d40c8b10c0a14732bea4aa3e84bb58257f990008309b9544f50b`  
		Last Modified: Fri, 08 May 2026 20:43:24 GMT  
		Size: 53.3 KB (53296 bytes)  
		MIME: application/vnd.in-toto+json
