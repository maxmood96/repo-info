## `postgres:17rc1-bookworm`

```console
$ docker pull postgres@sha256:9b4f634f50b7bf6129166ad8db3b12ded7df40aa86558ec937938e5fb620064d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `postgres:17rc1-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:8abcc464fccc4de55a5105f7c1317e7b39c846bb85ac979a3f94dcf8e004eafa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.2 MB (147241839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f06b59e446299d4e8851ec67717bca456d8fad493f9b828087f423e99f742c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:32 GMT
ADD file:c162e60b24ef6aed489ba1986f407fd9ab4ace659e0e3e6759ffac7eb0b7f770 in / 
# Wed, 04 Sep 2024 21:48:32 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV GOSU_VERSION=1.17
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV LANG=en_US.utf8
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_MAJOR=17
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_VERSION=17~rc1-1.pgdg120+1
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 05 Sep 2024 13:44:37 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
STOPSIGNAL SIGINT
# Thu, 05 Sep 2024 13:44:37 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 05 Sep 2024 13:44:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:44990bd21e0c5db65674bd030d12ea2461a14f2bb4007469bc2667c8535a8357`  
		Last Modified: Wed, 04 Sep 2024 21:51:32 GMT  
		Size: 26.9 MB (26887411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9ae4c474ed95cd628af882b052c523086cc21ddc0f24ca9b6f8eca4312960b`  
		Last Modified: Thu, 05 Sep 2024 05:48:45 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3023e0032654f8aed6b728bbe7febaffd2807f896f9f134715dc315c905eb3`  
		Last Modified: Thu, 05 Sep 2024 05:48:45 GMT  
		Size: 4.2 MB (4150914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db5800f5b661f501fdde83e66e50910fd6072841f01392ff5fd0a36aff48cf8`  
		Last Modified: Thu, 05 Sep 2024 05:48:45 GMT  
		Size: 1.4 MB (1423884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815cd609b0d2444b8d98a1915bf7cad5e755ec79d47470f84c541d7a31a1fbc6`  
		Last Modified: Thu, 05 Sep 2024 05:48:46 GMT  
		Size: 8.1 MB (8066403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a7cb2e0c74c89d4f114cd0a22f9d61d3e0ab92973ef09055b2bddf249bf984`  
		Last Modified: Thu, 05 Sep 2024 05:48:46 GMT  
		Size: 1.2 MB (1194866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085b70053bc41f4c2a8d0d5a7da4aa763d1367f13f8a570840911645523f2a15`  
		Last Modified: Thu, 05 Sep 2024 05:48:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be49688ae1ba33a431c4a7bc035a0f29ffaff6c7c9bc16bd0dea362b144f6c74`  
		Last Modified: Thu, 05 Sep 2024 05:48:46 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8dd12c42fe54ee8a48ddc160b27e649513b5808bfb2b0291c219e77cf590de`  
		Last Modified: Fri, 06 Sep 2024 21:16:48 GMT  
		Size: 105.5 MB (105497802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b668babf7dcebf795c247934f2e288b92306ae8abe394e04523843ca61b3de0`  
		Last Modified: Fri, 06 Sep 2024 21:16:44 GMT  
		Size: 10.2 KB (10238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ca4406f72040043f8d4504efcd1d14382f5c82d1602eb80d716a1a8bb26212`  
		Last Modified: Fri, 06 Sep 2024 21:16:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d1c99fd915f20e363456338c6e24794341157e6e1dbda273b9161006fe0a4d`  
		Last Modified: Fri, 06 Sep 2024 21:16:44 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09eadfefed086734d21ac10abd98663e22b0093421d769475dcdddf39c447802`  
		Last Modified: Fri, 06 Sep 2024 21:16:45 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd581d6db1e93649911a44341579605a09a78a51e0a7a96bd8ecb3df85394b81`  
		Last Modified: Fri, 06 Sep 2024 21:16:45 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17rc1-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:14292d45706f61b4bf9a92551d704594c78b12382a2ae9059befc673c05f770b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5833577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60de873a28ca87a414e43a58641bbef4f9dc82cd6a7e0e6cf38b94b37ab358c4`

```dockerfile
```

-	Layers:
	-	`sha256:386c8c8e28e9603a16c4dc70f7ba967b280071c1172fbfc071e3d08e87ae4d4a`  
		Last Modified: Fri, 06 Sep 2024 21:16:44 GMT  
		Size: 5.8 MB (5779532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf5cd06c622e3c544136afe5c08b5724a8ce785c76b59e6abea1e95717dec37b`  
		Last Modified: Fri, 06 Sep 2024 21:16:44 GMT  
		Size: 54.0 KB (54045 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17rc1-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:eeccab7b7360821735028b852babae74b06dac77837a63848ae5d20ce6014f17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141937189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c32729fe873d403d298ed5e30e97ce42005f3c76d17dd783ce0645e65e102e32`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 04 Sep 2024 21:58:08 GMT
ADD file:90772cdf7913d0ef1bf41e513a6205fa3195a1583476a536ec770e8381f77ac1 in / 
# Wed, 04 Sep 2024 21:58:08 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV GOSU_VERSION=1.17
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV LANG=en_US.utf8
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_MAJOR=17
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_VERSION=17~rc1-1.pgdg120+1
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 05 Sep 2024 13:44:37 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
STOPSIGNAL SIGINT
# Thu, 05 Sep 2024 13:44:37 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 05 Sep 2024 13:44:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:670631d7a00e03a2701d6b6aff29204afdeff4cd2da308462d92f5743156ede1`  
		Last Modified: Wed, 04 Sep 2024 22:01:44 GMT  
		Size: 24.7 MB (24718265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50662b3d2205bfde48c7c7ee492df609b20867a450a872a8e34fae1467209e84`  
		Last Modified: Thu, 05 Sep 2024 06:53:30 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bccbd6b6c11095d20b4078ffe578897cefad73d15b33fc0a3eec8093f041eb2`  
		Last Modified: Thu, 05 Sep 2024 06:53:30 GMT  
		Size: 3.7 MB (3742532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f537b63140972adb053d00e6965e0d19ac96f9fcf53cc647875e3499d7e072`  
		Last Modified: Thu, 05 Sep 2024 06:53:30 GMT  
		Size: 1.4 MB (1413612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818684dea80d219b3b50b12b97fd00572b2325ae91d47de8905c8fb5a0ddd9d4`  
		Last Modified: Thu, 05 Sep 2024 06:53:30 GMT  
		Size: 8.1 MB (8066297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efebd8ca0e3760211b0743352214ceaf97423c6db72d91fe0c68e34edb58328`  
		Last Modified: Thu, 05 Sep 2024 06:53:31 GMT  
		Size: 1.1 MB (1066972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f3b1200790e6e3387c0d7caaadab6f6b8ec7d7b34ec10f50f3dea452ba6b39`  
		Last Modified: Thu, 05 Sep 2024 06:53:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01488d49e7609eeb21c76d857556114a92d131aa883ce884d9e9bb1b7f8b9955`  
		Last Modified: Thu, 05 Sep 2024 06:53:31 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e9d0543229fc5ec729178381044b7ea8d6113848e3cae64a44ea751f25fa5b`  
		Last Modified: Fri, 06 Sep 2024 21:16:32 GMT  
		Size: 102.9 MB (102908944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82315a220b329f76d06a51dce6ab7fec447fd786bcad50841c84902272228a8`  
		Last Modified: Fri, 06 Sep 2024 21:16:29 GMT  
		Size: 10.2 KB (10246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709b5fbe498be4e9d61147328bb3155dfa493d39bbb28123aea00ab969e62e7b`  
		Last Modified: Fri, 06 Sep 2024 21:16:29 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac642ce956188c62dbaf66cd846e54360f2a93993ba2bc93fc13f418b48c1cc`  
		Last Modified: Fri, 06 Sep 2024 21:16:29 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39aecfe615d015f2aa589b06db2e5482a5bf607d55fe64ec7b0d630eda6401c2`  
		Last Modified: Fri, 06 Sep 2024 21:16:30 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56c5703895742f9661d9166e2f8a6241d7702bf0a94a168c405414d93a39091`  
		Last Modified: Fri, 06 Sep 2024 21:16:30 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17rc1-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:1386f46ce0ea68308493bdc604742fe78f7955005ce4c2481b188cba14298b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5833247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe5cfb360d4cedda5aeb24f51eef627ead16140d19fdf56765a2de91462edee1`

```dockerfile
```

-	Layers:
	-	`sha256:8d8a2d5a9e1d9cc41bdceb8658634d48b88511ad5a5ca3a0afc3235cbe1a6778`  
		Last Modified: Fri, 06 Sep 2024 21:16:29 GMT  
		Size: 5.8 MB (5779201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b53a2a0e5b3fec226eb15d7e166789f4456ad038468e0597d87bcf57f8d6709`  
		Last Modified: Fri, 06 Sep 2024 21:16:29 GMT  
		Size: 54.0 KB (54046 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17rc1-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:38a4dd56c5357bdf7aa3e063043383d6de5a0f7e63d32e8beecac9b256e575f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162675529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00b0b1a443af54e3a32e421d77cd9ea32599eae9d9538d469ca76aa1f3d57230`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:34 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Wed, 04 Sep 2024 22:44:34 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV GOSU_VERSION=1.17
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV LANG=en_US.utf8
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_MAJOR=17
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_VERSION=17~rc1-1.pgdg120+1
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 05 Sep 2024 13:44:37 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
STOPSIGNAL SIGINT
# Thu, 05 Sep 2024 13:44:37 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 05 Sep 2024 13:44:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6929aa670245b82c0d70e7f5dcac289c232127cc9b300670fbde3b92298d06`  
		Last Modified: Fri, 06 Sep 2024 21:00:28 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec50a74820e63b82ac31f9c6322a955531c85e065cb1c78a54fe44ef1793e60`  
		Last Modified: Fri, 06 Sep 2024 21:14:59 GMT  
		Size: 5.0 MB (4965081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e238c9d803f6c4b294d11a603af17d47f331754722bea76cb5ef7c6dcd8b14`  
		Last Modified: Fri, 06 Sep 2024 21:14:59 GMT  
		Size: 1.4 MB (1422124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d8a021da78aff6a778ec4a6c3b737294c6e216e2610742a4b270a715fe7eb6`  
		Last Modified: Fri, 06 Sep 2024 21:15:00 GMT  
		Size: 8.1 MB (8066266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac61e65af44ab15339b3a9f46e04966d300d6a3ad8f2f81f0681ddd071acb365`  
		Last Modified: Fri, 06 Sep 2024 21:15:00 GMT  
		Size: 1.1 MB (1137120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd96e97445a6409bb79703fe19d23f6f8f91d26e6fab8c7fa5d87a01fcabd4c`  
		Last Modified: Fri, 06 Sep 2024 21:15:00 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505e208804d7f1cf07b16ddb8ca95c2e06827391d6ab43fd24b5daf4993b1dc3`  
		Last Modified: Fri, 06 Sep 2024 21:15:00 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0319d851f43d81dcaa7fed73a592512767e0397198236acbb79297fab1974c25`  
		Last Modified: Fri, 06 Sep 2024 21:15:04 GMT  
		Size: 116.9 MB (116920078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2ba32f68a5ac9d843ab30e0d1777759ddea776d8a85ac69c612fa7e2c448ed`  
		Last Modified: Fri, 06 Sep 2024 21:15:01 GMT  
		Size: 10.2 KB (10246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338b3e4183799b8cbf1d887b91dc1bfcbf619f75b3b4e931f570daf0833130b8`  
		Last Modified: Fri, 06 Sep 2024 21:15:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c36b864645c6da09718d48f3e089f027280521f5ae1fc36d1d113b0ce1e25ba`  
		Last Modified: Fri, 06 Sep 2024 21:15:01 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:affdeb1d609bf79018f7328f7f46f63b9a558fe20350fd1aa2dd7cbcd6a1deb2`  
		Last Modified: Fri, 06 Sep 2024 21:15:01 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc3d59429708c22bc4d0f3be55eea34427a4691d89b6aac77bd1803312d7edd`  
		Last Modified: Fri, 06 Sep 2024 21:15:02 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17rc1-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:05c0fb10d034595ad61c6093ed48a647bb7bff0cffa83b6532950f629286b7bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5831419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c71d842859a5f6ca487f062919ae2504a7bbd33ada5951d7ab24a824fe8ee5c`

```dockerfile
```

-	Layers:
	-	`sha256:93ab36980584bf00d6236bd1d072670f91d72b8e90b1f3799e45fb6710611e69`  
		Last Modified: Fri, 06 Sep 2024 21:14:59 GMT  
		Size: 5.8 MB (5777611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:310e207a5dda22724e9c96de467c31e8afa200c1e2eb9dd19e5dc947d49b2639`  
		Last Modified: Fri, 06 Sep 2024 21:14:59 GMT  
		Size: 53.8 KB (53808 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17rc1-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:b7ec7abc8cd8b7a9e0729b4b5f82ac2f8171a78c3a10ee814b8102684c8a5242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166741008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9587d90f12fc88060dcd93ba8ed1f50171007131a78ad7a3af7a3350abffe44a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:52 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Wed, 04 Sep 2024 22:25:54 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV GOSU_VERSION=1.17
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV LANG=en_US.utf8
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_MAJOR=17
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_VERSION=17~rc1-1.pgdg120+1
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 05 Sep 2024 13:44:37 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
STOPSIGNAL SIGINT
# Thu, 05 Sep 2024 13:44:37 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 05 Sep 2024 13:44:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7091a65b3af01393bb237a0dd5e1eb6eb6722714679ff5876b084574dc17706`  
		Last Modified: Thu, 05 Sep 2024 03:09:50 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800ed3f152dd7bf42d96276af7a9d1ce719fd2a3bcef42118e305c36e12221e1`  
		Last Modified: Thu, 05 Sep 2024 03:09:51 GMT  
		Size: 5.4 MB (5368161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075f522e2a21fb72d03df834c71e2fbf45a6ec691eeae0decaa36ad2bc0652b0`  
		Last Modified: Thu, 05 Sep 2024 03:09:51 GMT  
		Size: 1.4 MB (1368567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6dd0b39792e48b0b4936cc2735903bd6daaa6f632a856cfefabf8c621eb16ef`  
		Last Modified: Thu, 05 Sep 2024 03:09:51 GMT  
		Size: 8.1 MB (8066345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8784a13cd11f3237242eb57895bd508e0f5d410cc1017caeced52945e8b97322`  
		Last Modified: Thu, 05 Sep 2024 03:09:52 GMT  
		Size: 1.3 MB (1283474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35aba7bcf3d315f55153104351b2edee8c0103834595bc782d25cbec20f5001b`  
		Last Modified: Thu, 05 Sep 2024 03:09:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f872029cf50f514a97ad2dc9fb914632e626f454e72f4795b87ad68dabc7f3`  
		Last Modified: Thu, 05 Sep 2024 03:09:52 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8645a7cab4f7f76cd93448bb6da029b300d09762bd91e339286b4c58868e8018`  
		Last Modified: Fri, 06 Sep 2024 20:58:42 GMT  
		Size: 117.5 MB (117511542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7dcdcc215148ad250d075bfcc13ba5bb8fe8fb2e445bdb7b2a115caa587a1b`  
		Last Modified: Fri, 06 Sep 2024 20:58:38 GMT  
		Size: 10.2 KB (10239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1aeffb850b4eb5165feb5a515c52beea08a36fb09f37eefa4f4202a31e84473`  
		Last Modified: Fri, 06 Sep 2024 20:58:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a83bbb65db9f980cbe2eea59356508c5544c329936cd2334698896dfb93d1f9`  
		Last Modified: Fri, 06 Sep 2024 20:58:38 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2aec56c0fa49c80d75bab021c2d623e98f2caeea18178a1d27227e864fd89d`  
		Last Modified: Fri, 06 Sep 2024 20:58:39 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a10c07c408e83e93561fd2ba30e9c0267a2f9f0a2bbdf1e4d7b3f222dab4e68`  
		Last Modified: Fri, 06 Sep 2024 20:58:39 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17rc1-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:8a8287124660af894b2ddc228134e600a46eb81d18be7ed8e4391d5950bedc11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5823265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eee0db992f24e89c837927e6a0c5d8c652504962821178b5d4d8ee5ad74263c`

```dockerfile
```

-	Layers:
	-	`sha256:a9aa83276841e486d5754e3f9c23f1c2c654508834ee2acc215d0b3207fb0ad1`  
		Last Modified: Fri, 06 Sep 2024 20:58:39 GMT  
		Size: 5.8 MB (5769368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cebb35c1270f2eb2fdfd35d9beb6c7715f8c01a9d39e8f27c51e62ea0849ee7f`  
		Last Modified: Fri, 06 Sep 2024 20:58:38 GMT  
		Size: 53.9 KB (53897 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17rc1-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:aca8cf7c2e4c880722435ef908016edb945554aab69a4cf16afd60779e81e568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.0 MB (160021210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9694532c3f0ea1e94db2b4b9d992162089fa9cf2aa6168977670d12340be1930`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 04 Sep 2024 21:42:50 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Wed, 04 Sep 2024 21:42:52 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV GOSU_VERSION=1.17
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV LANG=en_US.utf8
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_MAJOR=17
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_VERSION=17~rc1-1.pgdg120+1
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 05 Sep 2024 13:44:37 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
STOPSIGNAL SIGINT
# Thu, 05 Sep 2024 13:44:37 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 05 Sep 2024 13:44:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a71df81faca4120f677817bbd051e773830b054e72626158c76b4df335fa5f5`  
		Last Modified: Thu, 05 Sep 2024 05:04:02 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697d886823662fa64c552d6ec433809a3b77ca9bb1355ec5cba3160fa530a060`  
		Last Modified: Thu, 05 Sep 2024 05:04:03 GMT  
		Size: 4.4 MB (4391038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8a2ee793ee906d11de05d1a1778d1a245ff0121f2521f0fcbd8c5dbc63acbd`  
		Last Modified: Thu, 05 Sep 2024 05:04:03 GMT  
		Size: 1.4 MB (1412694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a43f4933e2b533e4734d02a6cf60a19522e291bd446eabfa1ecb8031471b1beb`  
		Last Modified: Thu, 05 Sep 2024 05:04:04 GMT  
		Size: 8.1 MB (8120458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29a493f58318811251ef710e6785725733972cd6f778208e7a7663b01cf0128`  
		Last Modified: Thu, 05 Sep 2024 05:04:03 GMT  
		Size: 1.1 MB (1096735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd2aad8c7ec9a88dee775539c06b9f365c7fdbec866fd84fe4d372a6dcc4d14`  
		Last Modified: Thu, 05 Sep 2024 05:04:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e0224b48d801dc7fd91c13ef65aac3ab8b4b00134811da28553542be3631fc`  
		Last Modified: Thu, 05 Sep 2024 05:04:04 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2226e8d1eab8144b3109fcee2fe068870ffdfbbc1cc108cc23a7691d50a551c5`  
		Last Modified: Fri, 06 Sep 2024 20:58:12 GMT  
		Size: 117.5 MB (117489403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5ca426b49cbe71a8d4452420b044e6d68ec705692a6c57c0112e4b1abe5718`  
		Last Modified: Fri, 06 Sep 2024 20:58:10 GMT  
		Size: 10.2 KB (10243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c5f66da210f0e150e02083e10c32acb382f8527a023e41ee78f1d96ca3a3e5`  
		Last Modified: Fri, 06 Sep 2024 20:58:10 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d124af686da520b82dadf4bf448fff6600b04429d0382ec8f80ffc0f722d0d1d`  
		Last Modified: Fri, 06 Sep 2024 20:58:10 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9dfff7e9c0e43c71ced1139127b326a5cb2cbded025e22c0aef8cd00700a79`  
		Last Modified: Fri, 06 Sep 2024 20:58:11 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0593750e448d30c4e739b7378b28caa0ff61be58e4019a9c1a24a732c80364`  
		Last Modified: Fri, 06 Sep 2024 20:58:11 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17rc1-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:ea7a5499e43670e65f810e395a6a59adf96df970136c1e3ef7a0e8843d8e4a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5815394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4052d5d2af24e24c7e8b2c3b0bd04f824bc251337ea41978f0983ec43964cc64`

```dockerfile
```

-	Layers:
	-	`sha256:90a2cfc65ff1b008f59203f09b67554f4d18ddbd9b8655da2fb2228d39829af6`  
		Last Modified: Fri, 06 Sep 2024 20:58:10 GMT  
		Size: 5.8 MB (5761545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bc9a6c5e3f856166dbbb97441add0728e16ec7f194275c9069f511b060093ca`  
		Last Modified: Fri, 06 Sep 2024 20:58:10 GMT  
		Size: 53.8 KB (53849 bytes)  
		MIME: application/vnd.in-toto+json
