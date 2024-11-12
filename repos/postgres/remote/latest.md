## `postgres:latest`

```console
$ docker pull postgres@sha256:2838b352c95941267f50c7c17c0580d43d122a8b57c31976d58d46c3bc437b38
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

### `postgres:latest` - linux; amd64

```console
$ docker pull postgres@sha256:719d50f0df30ec51e85b11e858fe6002e35b89c9bcbeb630a5d7c04fc87d66b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154578062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb72c2c69f9f837d0e2a831b8e4772869a933dd8e81f4ddf19af1c97ab5c7fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 26 Sep 2024 18:19:57 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV LANG=en_US.utf8
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_MAJOR=17
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_VERSION=17.0-1.pgdg120+1
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Sep 2024 18:19:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 18:19:57 GMT
STOPSIGNAL SIGINT
# Thu, 26 Sep 2024 18:19:57 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Sep 2024 18:19:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd18d1b1f3cf4dfa29581499e08401a6c3accf7007c69305422d17b6d28579e`  
		Last Modified: Tue, 12 Nov 2024 02:10:30 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe013fcce988b34f6946f2ffb11aa822b5e6c2e822a4cbb20441327b18e889f`  
		Last Modified: Tue, 12 Nov 2024 02:10:31 GMT  
		Size: 4.5 MB (4533674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f0c600cf82459a72ec27aa77593608b06d1bb522f3c84342dd9b1f705f12f1`  
		Last Modified: Tue, 12 Nov 2024 02:10:31 GMT  
		Size: 1.4 MB (1446631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c903b2aeeef89d601ea6c16d8fb8e1112fd29c88ea6b092cdc125272f579df`  
		Last Modified: Tue, 12 Nov 2024 02:10:31 GMT  
		Size: 8.1 MB (8066251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49faa60cc715608a3b8b19c99cdf3800d76599c18984b75456bcc6e01130709b`  
		Last Modified: Tue, 12 Nov 2024 02:10:32 GMT  
		Size: 1.2 MB (1196068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744e496a897fc3012eb8c821c748efc7f26e57882a8b95168fe0f3364460af56`  
		Last Modified: Tue, 12 Nov 2024 02:10:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c689f809e57fd5194eb4d34eb3f4240dfd78cb6656b0c83d6e0ec1e2c06067`  
		Last Modified: Tue, 12 Nov 2024 02:10:32 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc6568b6a72f0fd2d3fceaa254dfe3594f7a390a70bd9c3ce9ae189623e02a9`  
		Last Modified: Tue, 12 Nov 2024 02:10:36 GMT  
		Size: 110.2 MB (110186881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e679d2c32d251e3bd6d11ea7448cec3c61ba3e967afe94dbd61e1642b66daf7`  
		Last Modified: Tue, 12 Nov 2024 02:10:33 GMT  
		Size: 10.2 KB (10239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4905c4cdeae12ddd63e55f7463043959577dbb1e67a902f147048ca84d8d4427`  
		Last Modified: Tue, 12 Nov 2024 02:10:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15266ecdce80e25ef051a55c76ee50b77cf9753905ba62d813629e0785ffe741`  
		Last Modified: Tue, 12 Nov 2024 02:10:33 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c10b51b83cace7b6538c5da1481e3d051e7cee57e4ca43d6aaa04e5b99fb7b`  
		Last Modified: Tue, 12 Nov 2024 02:10:34 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c636afee197a3dd8b4631ab11da25152ecf5c2fac0fcee2c45cc448904c84f1`  
		Last Modified: Tue, 12 Nov 2024 02:10:34 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:671f2b3b230be78ec81231e23120dc4df97c87d736497d6094d62cdfc7e1538b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5838467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26f37e421894ea19f497c0a011391bb90e7eadb1855ff90cf11e2910a9745f56`

```dockerfile
```

-	Layers:
	-	`sha256:a5d42538689deb63e3faf82e5075d42ff2216dc54ab4c866fea390732d7bc91e`  
		Last Modified: Tue, 12 Nov 2024 02:10:31 GMT  
		Size: 5.8 MB (5783276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c659ed4e957fbc3b36a73c8c987e990be3c3315fb1ba06a72f12d7cf69934fd8`  
		Last Modified: Tue, 12 Nov 2024 02:10:31 GMT  
		Size: 55.2 KB (55191 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; arm variant v5

```console
$ docker pull postgres@sha256:b85211af91e279ead05921434399f1ab623f79207516d95a0e2e64b7ab84ab5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.3 MB (147304463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80c3e1f18d9ac6b621a4b66eeb5e415b2e8bab586c28e43b5ea567b1cc79d764`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 26 Sep 2024 18:19:57 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV LANG=en_US.utf8
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_MAJOR=17
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_VERSION=17.0-1.pgdg120+1
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Sep 2024 18:19:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 18:19:57 GMT
STOPSIGNAL SIGINT
# Thu, 26 Sep 2024 18:19:57 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Sep 2024 18:19:57 GMT
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
	-	`sha256:aa20181fb1b2e02cc8888572dced40b9ccb9f194ed7662447429b6bb43dc1a79`  
		Last Modified: Tue, 12 Nov 2024 04:56:07 GMT  
		Size: 105.6 MB (105557537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f5e973c024e602d924122ddae3fee378a5f49b9d76d64810dc77965cd55dee`  
		Last Modified: Tue, 12 Nov 2024 04:56:05 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba22dcf9f0f3a40fd8d6b871f60c4b650fe9674831abed5b7c8c03f44739685`  
		Last Modified: Tue, 12 Nov 2024 04:56:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1dc44edefceb679baa821181574ee88487fea20cbc364c395a4443059c283d8`  
		Last Modified: Tue, 12 Nov 2024 04:56:05 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e02b77a521eed9d811669e0511cf8409e7863d785cfc3531133f3a13b91416`  
		Last Modified: Tue, 12 Nov 2024 04:56:06 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b011e3b6c429dfbe88475951d44542615580ef29bfa49b959ff6b98f979653d`  
		Last Modified: Tue, 12 Nov 2024 04:56:06 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:6a4561babc944781a3ac201fadad82ba416f5d045c95ffc7df78d3ca81864413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5856326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf12f37a7b1dece5bee5780cb151cc69cf9be627808a2ac59af80477cbdeb630`

```dockerfile
```

-	Layers:
	-	`sha256:0ebc236ee501708ba3bfcad53de8ac194e8dd2dc705e5e86e4a37f41255680c1`  
		Last Modified: Tue, 12 Nov 2024 04:56:03 GMT  
		Size: 5.8 MB (5800901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c5b97bd2cccc390c3aec0b9623ccd261969eabd1a33e31d8ec9ee4fbf2daa62`  
		Last Modified: Tue, 12 Nov 2024 04:56:02 GMT  
		Size: 55.4 KB (55425 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; arm variant v7

```console
$ docker pull postgres@sha256:59cd9c3b4197abbd663517c70c5b0d3050176a1e04ec3132378761fa5ea01065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (142003815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04134e7146a75735dcd3210e1263d93218445d90b89cb3fe49d3f4f3bb2aef8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 26 Sep 2024 18:19:57 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 26 Sep 2024 18:19:57 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV LANG=en_US.utf8
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_MAJOR=17
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_VERSION=17.0-1.pgdg120+1
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Sep 2024 18:19:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 18:19:57 GMT
STOPSIGNAL SIGINT
# Thu, 26 Sep 2024 18:19:57 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Sep 2024 18:19:57 GMT
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
	-	`sha256:373108670664a023a842e6d60139efd9ce388f5fb1bfdee5269c106b6f0b594c`  
		Last Modified: Thu, 17 Oct 2024 18:17:34 GMT  
		Size: 103.0 MB (102975548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9447a5b701ce36def5d068d5c52ae2fd46ba61a091e3002f7d90f1dcafc14727`  
		Last Modified: Thu, 17 Oct 2024 18:17:32 GMT  
		Size: 10.2 KB (10238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d1ec1965d1ce1cdb92c85d0ce583ca9cd273642246020b504e2c038646ee2e`  
		Last Modified: Thu, 17 Oct 2024 18:17:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2d566ea035b510eaf313ad959905bf3549a7fe04dcc1e8f21aae773f155ae1`  
		Last Modified: Thu, 17 Oct 2024 18:17:32 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10708c30e4b8829cf11ff70fa12b73af84f79b0f3c61bb96b37b378f93611700`  
		Last Modified: Thu, 17 Oct 2024 18:17:33 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5bdbc5c885910ccf6860af4796eecb89bf390e03d0502cbacc39ba6ab1fbb8`  
		Last Modified: Thu, 17 Oct 2024 18:17:33 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:8a41164b5debbf40cff4e8d0e0d3873794dd08ca2f97240a2003b110da82cbe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5837203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719dde74c89490328cf20af11d95325119fdd43f7a8cfb6a4d19119cf29cb3f4`

```dockerfile
```

-	Layers:
	-	`sha256:4c903648c3edab1d1462a958e993c0604cac088ca6fa8fb3bed5c4c85df5138e`  
		Last Modified: Thu, 17 Oct 2024 18:17:30 GMT  
		Size: 5.8 MB (5781891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac7253edb653e9bab5da994000cb3d2a9c9d223f166a703dc2ed8be64226efb1`  
		Last Modified: Thu, 17 Oct 2024 18:17:30 GMT  
		Size: 55.3 KB (55312 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:27750cd60e6cc4159181ad98a60fc7ff73449a8c6925687632e1d8be8ca99009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152748910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c9aa6ecd71d620c86c7e39ddc815ade359fe7e84ad47fc0a15ee4fdd0cae91d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 26 Sep 2024 18:19:57 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 26 Sep 2024 18:19:57 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV LANG=en_US.utf8
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_MAJOR=17
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_VERSION=17.0-1.pgdg120+1
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Sep 2024 18:19:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 18:19:57 GMT
STOPSIGNAL SIGINT
# Thu, 26 Sep 2024 18:19:57 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Sep 2024 18:19:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0dd2bf7a18016080f59a7ca20afcfd90b91b83dbe2f041cf829b175f8ed6417`  
		Last Modified: Thu, 17 Oct 2024 16:52:20 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecbc93de950e66abc2e48dcd67567fe8383702b3328af21a2dc72ad541ee30b`  
		Last Modified: Thu, 17 Oct 2024 16:52:21 GMT  
		Size: 4.5 MB (4499091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90646cadd7e608655d76f77b10a651de51ff7e45e8622c6be9155e37520bbc36`  
		Last Modified: Thu, 17 Oct 2024 16:52:21 GMT  
		Size: 1.4 MB (1378704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1dbef7dcaa1cabc44cc6659c4062b8fc5551dc57b9f3cb74f848092759b3516`  
		Last Modified: Thu, 17 Oct 2024 16:52:21 GMT  
		Size: 8.1 MB (8066287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7fdac227b96bb069a8114e3b8b41fe86c9e151bdabc4e73bd68643c5c49dffb`  
		Last Modified: Thu, 17 Oct 2024 16:52:22 GMT  
		Size: 1.1 MB (1108682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425a818d8223761585857cfa34430bf776e000e24eee1c9d6dd2631cded5b9a6`  
		Last Modified: Thu, 17 Oct 2024 16:52:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a40d31bfac2ea14b8ca0c6eaceef69b4fbe8241145ca06710903bc02fee8c5`  
		Last Modified: Thu, 17 Oct 2024 16:52:22 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e868621ffb41e6e31c6b89e532a771bf00fc6aac7348c3d388e4e45c90eb5a6d`  
		Last Modified: Thu, 17 Oct 2024 16:52:25 GMT  
		Size: 108.5 MB (108519247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ce5b6f352e341fb5aad1239ddc557dcc1a16a350131840a500f62350d0ceba`  
		Last Modified: Thu, 17 Oct 2024 16:52:23 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b732c95d024b00fb5410b246475f4fc118e95aeeaefa58a286cfe4c171daf14`  
		Last Modified: Thu, 17 Oct 2024 16:52:23 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc01759541cf752b4b560c707526751a322bbf4b5a85e2fcc98a027546d9ed1`  
		Last Modified: Thu, 17 Oct 2024 16:52:24 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6e84deecdbdea96d7e868cf1a450823400d457e4c2fbcddfb81bd44f486998`  
		Last Modified: Thu, 17 Oct 2024 16:52:24 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159c4494c27972d64510002308804cd79fa3c783d0aea629dc47aa7ff0c53467`  
		Last Modified: Thu, 17 Oct 2024 16:52:24 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:72c12b2528f7078bfa0d2908d0a96bc1b652c49caafa2815aa98cad3d23b020d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5826544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b82ed211d1c8ac9accad7a5488026a7b4e0f2a4cc6e6f0d997163ddc9534461c`

```dockerfile
```

-	Layers:
	-	`sha256:3dcb3642e418265ec4fcef8353c29ab6723ec0882e5efc230ab8c6210a903a04`  
		Last Modified: Thu, 17 Oct 2024 16:52:21 GMT  
		Size: 5.8 MB (5771174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88c2ff7d9bc69817de9d549fda52f3fc1e618bc988a7ab6cf13319bcd1928139`  
		Last Modified: Thu, 17 Oct 2024 16:52:21 GMT  
		Size: 55.4 KB (55370 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; 386

```console
$ docker pull postgres@sha256:dea42501d3ac8f9cfd2f37a3209416b99038419300c24f5ec101c63cde6bd5e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162744423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e725de66339e7d8c565e1bf5926528f2141abf82507fcf411e25fe9ce23a7a2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 26 Sep 2024 18:19:57 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV LANG=en_US.utf8
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_MAJOR=17
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_VERSION=17.0-1.pgdg120+1
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Sep 2024 18:19:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 18:19:57 GMT
STOPSIGNAL SIGINT
# Thu, 26 Sep 2024 18:19:57 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Sep 2024 18:19:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4aebdc3232d09b3d2a3e5719df16d280a8cad7d76fbf49df2378c069e07fec`  
		Last Modified: Tue, 12 Nov 2024 02:24:06 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3420bc5562d190765f67466df1be48538bac246f171686fcb7b87abb80041334`  
		Last Modified: Tue, 12 Nov 2024 02:24:07 GMT  
		Size: 5.0 MB (4965082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae72a4d8257cb7f95f1e7f8b53b90e27b9989db932e64761ef9fa98d8bb8bfc6`  
		Last Modified: Tue, 12 Nov 2024 02:24:07 GMT  
		Size: 1.4 MB (1422125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:368a20176e5db67a28fa3a115303f0311ed8c479dd44fae15780368533e5a7fe`  
		Last Modified: Tue, 12 Nov 2024 02:24:07 GMT  
		Size: 8.1 MB (8066277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7f356762c238d7cd7ac016b3d97474051d67ba353568fb5d2563014336bb40`  
		Last Modified: Tue, 12 Nov 2024 02:24:08 GMT  
		Size: 1.1 MB (1137132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c779b247076df7fd21e0619cb918d69966530688c969a328f7e8d646d6af24`  
		Last Modified: Tue, 12 Nov 2024 02:10:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92031d67896e402b0efe24b5a4c02766f7ff87867491f601b12ce1e1608efd0f`  
		Last Modified: Tue, 12 Nov 2024 02:10:35 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2854de9bbc7321170b9b72d29e442e1c5e08a22c3487aa459440d3b68516031f`  
		Last Modified: Tue, 12 Nov 2024 02:24:11 GMT  
		Size: 117.0 MB (116987792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09974882166892bf0e1244f6aa8b89897864f6846cd84dea1874f3f2ea60f383`  
		Last Modified: Tue, 12 Nov 2024 02:24:09 GMT  
		Size: 10.2 KB (10239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d800fb3dbf1570df97b06a5310734a00c40acd6a160582a47569e83ca7c4590`  
		Last Modified: Tue, 12 Nov 2024 02:23:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3f5f1738d17ab91373af1c95aee152706f76776140890b984c578e2c29e9d9`  
		Last Modified: Tue, 12 Nov 2024 02:24:09 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d244a70e1c4fa1a9d8c86a4e0f202220101bf5656a2615ff4721c71ce5e402c`  
		Last Modified: Tue, 12 Nov 2024 02:24:09 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f133468bc5ea908fd728ef799807531ce83939f007e4d1a5c8cfcd230d4ef11`  
		Last Modified: Tue, 12 Nov 2024 02:24:10 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:8cd2b461c897a95201e9789d417c1e3c4cdbcc05c04ce28d37ca57ef61b26f38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5854055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71f957c009de67bf6e632b36d4ad8f3c2e53df6ff4c11346deda14c3ae365ee2`

```dockerfile
```

-	Layers:
	-	`sha256:e22ac8724e4f38c3f37e39fc1022b1c16d7967ffb2753ff876ea53b81e244bcf`  
		Last Modified: Tue, 12 Nov 2024 02:24:07 GMT  
		Size: 5.8 MB (5798928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:907fcce604b527327fab6fbe2771ffff3c1b640d6f26e474db4ea5248cdf18ad`  
		Last Modified: Tue, 12 Nov 2024 02:24:06 GMT  
		Size: 55.1 KB (55127 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; mips64le

```console
$ docker pull postgres@sha256:8cb7bff9212583f1bb05e11a36d87a7c3f73774b74980c03a96bbef89d99e473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (149993114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3344c6fb25d9b9a21cda74ab0a0d4e358bcd5f17789e078bb133fea4b286f254`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 26 Sep 2024 18:19:57 GMT
ADD file:6c11edc513b28b5a4034ee9c0d4cdcf019a82635ebb8a9e02732800fa457f683 in / 
# Thu, 26 Sep 2024 18:19:57 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV LANG=en_US.utf8
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_MAJOR=17
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_VERSION=17.0-1.pgdg120+1
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Sep 2024 18:19:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 18:19:57 GMT
STOPSIGNAL SIGINT
# Thu, 26 Sep 2024 18:19:57 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Sep 2024 18:19:57 GMT
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
	-	`sha256:958e6c1af3232127114b10b1c5c2ab108aa6122698be305e46d5f41c5d19de89`  
		Last Modified: Fri, 18 Oct 2024 03:04:20 GMT  
		Size: 105.8 MB (105789718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758caff0a726a9e094c11d7326e0ea953182dcfd5abacf2eaa7531972561c652`  
		Last Modified: Fri, 18 Oct 2024 03:04:11 GMT  
		Size: 10.2 KB (10242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6347eb982ae079c2d78b1da3a506d23ce03638afc0a7d766ca04633ea1968fb5`  
		Last Modified: Fri, 18 Oct 2024 03:04:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f2395134d248d0acc1d48021bc2be405bd0e4f6c405ee5e19a4637b7ac5d6c`  
		Last Modified: Fri, 18 Oct 2024 03:04:11 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82461ccadf6ca3b1baf39ba3983561e9ea7864034a5f8010458d4b3c3bee31e6`  
		Last Modified: Fri, 18 Oct 2024 03:04:12 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65f4aa66346f23b79c7f36a760c5cccac3abe80416d869c2d70d0e5ce74b4fe`  
		Last Modified: Fri, 18 Oct 2024 03:04:12 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:63b575b486824e5e5eb9958964aa2d5924573c32f96d85d48bd67d9cee873ac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 KB (54972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7566664e2dbf31ede0d0c33dabc92582ebdec59d691f1b92c6edcee9b390b3aa`

```dockerfile
```

-	Layers:
	-	`sha256:5b8c8bac032ad9b44192907d14ff85a62172ec285497f5d61812fc7799cafbd6`  
		Last Modified: Fri, 18 Oct 2024 03:04:08 GMT  
		Size: 55.0 KB (54972 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; ppc64le

```console
$ docker pull postgres@sha256:6399a24d017802cdaec00fe93b60dde57dd3491aa393bd554c226ec52b50bb8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166811337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:557a71ac5cac29f06b005da725c818545c534b23cc9f13a2bef4305e660cfb92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 26 Sep 2024 18:19:57 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV LANG=en_US.utf8
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_MAJOR=17
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_VERSION=17.0-1.pgdg120+1
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Sep 2024 18:19:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 18:19:57 GMT
STOPSIGNAL SIGINT
# Thu, 26 Sep 2024 18:19:57 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Sep 2024 18:19:57 GMT
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
	-	`sha256:5678f44619a4cb0109b9a4e0c82532ccb955458e83122d7c9d6b6c698211cd90`  
		Last Modified: Tue, 12 Nov 2024 06:56:31 GMT  
		Size: 117.6 MB (117578859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5921a3fb1b2a951e86fdd89214c23bfa6b12c7a0834e136fb46b29c85335b0c`  
		Last Modified: Tue, 12 Nov 2024 06:56:27 GMT  
		Size: 10.2 KB (10237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b964aef296977417585e10c6ec1ff8966aaa449f0c02337f78dd8ba9c8dbe65`  
		Last Modified: Tue, 12 Nov 2024 06:56:27 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a09354db5ddd07bcfcf50bb65bef6f3141755ca1dd8988af56caa21c272402`  
		Last Modified: Tue, 12 Nov 2024 06:56:27 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68497f048e5fa9bee13eba3c7417b2ac30b9c5d906b7cd363aa02f46bca3b0df`  
		Last Modified: Tue, 12 Nov 2024 06:56:28 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b58667eeda235c1a5258c43cfa4d258f13fada49361d1e7085542352f4d2c0c`  
		Last Modified: Tue, 12 Nov 2024 06:56:28 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:19853618cfa224546a85f498ec1d1b361028858a3fb7c1cbfd78225791e6465a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5845786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a86c4b4739bbdae0eb87588e0a1c7ce2766df3cb55966ff57465d79870069b`

```dockerfile
```

-	Layers:
	-	`sha256:81cfb50f6aa0f42fa5f0b243358b55be8a1a661e97c961b1c1432578a2ae54bb`  
		Last Modified: Tue, 12 Nov 2024 06:56:25 GMT  
		Size: 5.8 MB (5790517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cedca434dad53b43c1a7734b3380fecdc44b233109ee97d5aa01aee9f4f6783d`  
		Last Modified: Tue, 12 Nov 2024 06:56:24 GMT  
		Size: 55.3 KB (55269 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; s390x

```console
$ docker pull postgres@sha256:79e3982b71cc53f85692612f6fb7ec886fdb7d2b4e13c4c9848313570f232632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.1 MB (160108598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4481c92f51ca9007fc93b43cad1d2cf7a1728a832227bb0da3c1c17e60ee7a30`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 26 Sep 2024 18:19:57 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV LANG=en_US.utf8
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_MAJOR=17
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_VERSION=17.0-1.pgdg120+1
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Sep 2024 18:19:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 18:19:57 GMT
STOPSIGNAL SIGINT
# Thu, 26 Sep 2024 18:19:57 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Sep 2024 18:19:57 GMT
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
	-	`sha256:0c8d3fe36deace495e425294fb81cc9f7d850f01710c0c297671aae7b8768aba`  
		Last Modified: Tue, 12 Nov 2024 07:30:51 GMT  
		Size: 117.6 MB (117575542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4296c50272bd93dfd67bc4136975ac42f15b95b1994f662c6fce5a1574a8ac3`  
		Last Modified: Tue, 12 Nov 2024 07:30:50 GMT  
		Size: 10.2 KB (10234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96061097208edf17f6c3ed0306200283e63fa1ac70e8e3a79e0899206d9576a8`  
		Last Modified: Tue, 12 Nov 2024 07:30:50 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8f53079ad3ba55223f7ad8edd52d137871f624011301d8a66ea36376e27465`  
		Last Modified: Tue, 12 Nov 2024 07:30:50 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6d456c334e5ca214227e461bc46f88c34e44503eb0cbb4d888851113eba07c`  
		Last Modified: Tue, 12 Nov 2024 07:30:50 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80b8cfce68ce03cde7246f63d33e245c455806a3422231f1d63927ff6cde7b1`  
		Last Modified: Tue, 12 Nov 2024 07:30:50 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:8a99781b54776fdd41540c4c885a0f0f3d41d31a1d137aa8fcba6d37a41c6476
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5837754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd70be1a7b4433d27fc1074b1c0b57da36063a6a9714abd959898c371f3cbed`

```dockerfile
```

-	Layers:
	-	`sha256:3c94937744ec45c31b562f32361c1d581887892b26374ef27238952c00bf66a2`  
		Last Modified: Tue, 12 Nov 2024 07:30:48 GMT  
		Size: 5.8 MB (5782564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a595c6fc28c23bab48f1ff8f47a062d3360b71d0af464a1d3b09bf2ff1a1591b`  
		Last Modified: Tue, 12 Nov 2024 07:30:48 GMT  
		Size: 55.2 KB (55190 bytes)  
		MIME: application/vnd.in-toto+json
