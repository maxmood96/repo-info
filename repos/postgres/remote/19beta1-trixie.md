## `postgres:19beta1-trixie`

```console
$ docker pull postgres@sha256:f9ccf22a6b8f2b8b0c43635e74bdb1921cdfba42ccf67d35ef6445aab705b3e1
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `postgres:19beta1-trixie` - linux; amd64

```console
$ docker pull postgres@sha256:c9043a803f73c1dbcfd8a97d77f9731dac94cbb1ec3ee230682b1a745bb49495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.6 MB (163642368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0d7abf9b41b6dc336f0ca9cbbacf4de81677dbf6b0fa136b311e1973daa4ff5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:33:17 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 11 Jun 2026 00:33:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:33:30 GMT
ENV GOSU_VERSION=1.19
# Thu, 11 Jun 2026 00:33:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 11 Jun 2026 00:33:35 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 11 Jun 2026 00:33:35 GMT
ENV LANG=en_US.utf8
# Thu, 11 Jun 2026 00:33:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:33:38 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Jun 2026 00:33:39 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:33:39 GMT
ENV PG_MAJOR=19
# Thu, 11 Jun 2026 00:33:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/19/bin
# Thu, 11 Jun 2026 00:33:39 GMT
ENV PG_VERSION=19~beta1-1.pgdg13+1
# Thu, 11 Jun 2026 00:33:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 11 Jun 2026 00:33:59 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 11 Jun 2026 00:33:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 11 Jun 2026 00:33:59 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Thu, 11 Jun 2026 00:33:59 GMT
VOLUME [/var/lib/postgresql]
# Thu, 11 Jun 2026 00:33:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:33:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 11 Jun 2026 00:33:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:33:59 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jun 2026 00:33:59 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 11 Jun 2026 00:33:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149f41ed741d14af03a9c152c85181ec13e330e1f54a5d9e353ecb25a8fe36b4`  
		Last Modified: Thu, 11 Jun 2026 00:34:19 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a905fda4b70bac4474095d8b4289b85ec1bafd5521074936df0349e043de7d`  
		Last Modified: Thu, 11 Jun 2026 00:34:19 GMT  
		Size: 6.4 MB (6443046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6db4dcac3c505718e132463d748f0bc3c74024dfb9fb6e059222b51b506bcc4`  
		Last Modified: Thu, 11 Jun 2026 00:34:19 GMT  
		Size: 1.3 MB (1256735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256cfbc699d78cb7595ae51bc1afa40b2ab30ac36f0ccd41cfda47e92a75ae8c`  
		Last Modified: Thu, 11 Jun 2026 00:34:19 GMT  
		Size: 8.2 MB (8203883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39a4afcda73f579b00f534f0f31ff164775d0419983ee175388b2545cf1c9b1`  
		Last Modified: Thu, 11 Jun 2026 00:34:20 GMT  
		Size: 1.3 MB (1311630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328ac4b2731926170cee035b3cffc3c64d7047b3d0eb939316ea1c6bd0516509`  
		Last Modified: Thu, 11 Jun 2026 00:34:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0df2a411db23112bb6231315998e2ca00cf09eb1df0db1b2dfc54c41d5e585`  
		Last Modified: Thu, 11 Jun 2026 00:34:20 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9bc3a10442ffc3b4de2317047f6fbc01281a3304849987e84ff8791079514e`  
		Last Modified: Thu, 11 Jun 2026 00:34:24 GMT  
		Size: 116.6 MB (116609411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c163fb4943ab45b419c0919db9b83a93566e6413d3073389bb0242fc085d9fd9`  
		Last Modified: Thu, 11 Jun 2026 00:34:22 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134e1544d46e780acd559a852ad9a63d22059a26ce2c17b805b36f34a0253930`  
		Last Modified: Thu, 11 Jun 2026 00:34:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddae59d4a6e1d892824c0b653aebefe688845a985fc7eec7ad218361d38974e8`  
		Last Modified: Thu, 11 Jun 2026 00:34:22 GMT  
		Size: 6.1 KB (6095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711c7c16a314122f34d96668a6e7ac3e76596f71039bc2b88c1be7d17e1e1dc5`  
		Last Modified: Thu, 11 Jun 2026 00:34:23 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:e3875aeeb23aba8acfbe2516b935d0e8fa4496a5c462833d110af11b8c86c34b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6049169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01dcd724f833829e796b2319ee6403f8c79db6c8f28917beca00066ac3fc16da`

```dockerfile
```

-	Layers:
	-	`sha256:1832401a77ec9a52a4c991bd2f61dff13e24767691d6b15456a2f92d838f75e3`  
		Last Modified: Thu, 11 Jun 2026 00:34:19 GMT  
		Size: 6.0 MB (5997885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:020f4f2032552c5c3925eb279ea3176955af36931e16e5bcaec1f1c010728aa6`  
		Last Modified: Thu, 11 Jun 2026 00:34:19 GMT  
		Size: 51.3 KB (51284 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-trixie` - linux; arm variant v5

```console
$ docker pull postgres@sha256:df1daab6b596366b74ae4e9be7bc33689a778ad13798e7e7d36b56a05c452dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92008438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588f27e9eef78e6bd4f5f7be2a48dd388d52e27e01aafaed8863e89d6907112b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:44:33 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 11 Jun 2026 00:44:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:44:54 GMT
ENV GOSU_VERSION=1.19
# Thu, 11 Jun 2026 00:44:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 11 Jun 2026 00:45:03 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 11 Jun 2026 00:45:03 GMT
ENV LANG=en_US.utf8
# Thu, 11 Jun 2026 00:45:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:10 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Jun 2026 00:45:10 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:45:10 GMT
ENV PG_MAJOR=19
# Thu, 11 Jun 2026 00:45:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/19/bin
# Thu, 11 Jun 2026 00:45:10 GMT
ENV PG_VERSION=19~beta1-1.pgdg13+1
# Thu, 11 Jun 2026 00:58:57 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 11 Jun 2026 00:58:57 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 11 Jun 2026 00:58:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 11 Jun 2026 00:58:57 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Thu, 11 Jun 2026 00:58:57 GMT
VOLUME [/var/lib/postgresql]
# Thu, 11 Jun 2026 00:58:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:58:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 11 Jun 2026 00:58:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:58:57 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jun 2026 00:58:57 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 11 Jun 2026 00:58:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ed883f3fd95b7edef302d7ca9520eefdae280af081509bd7e9e5b5ff8f4cda7c`  
		Last Modified: Wed, 10 Jun 2026 23:41:17 GMT  
		Size: 28.0 MB (27959200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3863145ec3b151db18418627e2a013c1902c2646ec9ccfaf4ecd96e7266a78`  
		Last Modified: Thu, 11 Jun 2026 00:59:10 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3549a8ef6e60392015dc87bf26cb594b2c069ebfbc03936ae5935445a38067f4`  
		Last Modified: Thu, 11 Jun 2026 00:59:10 GMT  
		Size: 5.9 MB (5932394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbfa3da65b1e20e116d53585cf773a885e30cf8f0c7ee6053585b1402b20174`  
		Last Modified: Thu, 11 Jun 2026 00:59:10 GMT  
		Size: 1.2 MB (1227565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a407df95c27d0b109c36784567a1e3beef928bb008cb5126dcaff7fe92a4aa51`  
		Last Modified: Thu, 11 Jun 2026 00:59:10 GMT  
		Size: 8.2 MB (8204335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db3431630afe119993cac668bec1d06e67b63fa4e1da6905c4edb5c26747672`  
		Last Modified: Thu, 11 Jun 2026 00:59:11 GMT  
		Size: 1.3 MB (1317344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a710538e88f460478f145f03acfc6b5cae1f80de3f73169ed09e525fe54cdbb0`  
		Last Modified: Thu, 11 Jun 2026 00:59:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fc7d2d98098b680bcd002d90e5dd7579b69ec22c891b878a17139131d98186`  
		Last Modified: Thu, 11 Jun 2026 00:59:11 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bb3b4c744557e7a8d86137a35df11110ffeb8604dd3e55a3d8320e66e42f34`  
		Last Modified: Thu, 11 Jun 2026 00:59:13 GMT  
		Size: 47.3 MB (47335355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e953b1b10aa66cee4fef5940576972bfbf795a34498fd83a8e0c1a18e508f169`  
		Last Modified: Thu, 11 Jun 2026 00:59:12 GMT  
		Size: 21.4 KB (21413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8a9f0d5360b422c873267421dd09765e42e02eebbc8bcd507147b3b6f6029b`  
		Last Modified: Thu, 11 Jun 2026 00:59:13 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784518753e1d26ef1df6a43c96b48a1ab4cdf799e20ef302ca8c88d57d97ba87`  
		Last Modified: Thu, 11 Jun 2026 00:59:13 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec16b71a3a5e07052dbf5a9c4ae2c2fb3631b1db0236dc78859fda984483b0ae`  
		Last Modified: Thu, 11 Jun 2026 00:59:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:07097126146f08499e7eefaea29ee4d7435088cea9714b99956edb8d354a8ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5179602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c23d84ed56e0970fde3b13bdc8679e7bc88688099b8803e92f6a043976214d0`

```dockerfile
```

-	Layers:
	-	`sha256:d2c1daaef0b828c5b73b2263c729e4f197e596f4eb1e406271ebc48b52dbffbd`  
		Last Modified: Thu, 11 Jun 2026 00:59:10 GMT  
		Size: 5.1 MB (5128129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df5d554c37b2faeda918a45fad0ac49b565e137f5e1fd351cf28adaa60f4a4ed`  
		Last Modified: Thu, 11 Jun 2026 00:59:10 GMT  
		Size: 51.5 KB (51473 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-trixie` - linux; arm variant v7

```console
$ docker pull postgres@sha256:6c6743b41044a04842c3ffd1e68d51dcdb134af9db4848b7d2066839c63b11ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88282359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37ffc50f46578f581dadabc61fcd7d2b1442a335d7f40072557bae48d19262b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:46:46 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 11 Jun 2026 00:46:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:03 GMT
ENV GOSU_VERSION=1.19
# Thu, 11 Jun 2026 00:47:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 11 Jun 2026 00:47:10 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 11 Jun 2026 00:47:10 GMT
ENV LANG=en_US.utf8
# Thu, 11 Jun 2026 00:47:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Jun 2026 00:47:15 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:47:15 GMT
ENV PG_MAJOR=19
# Thu, 11 Jun 2026 00:47:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/19/bin
# Thu, 11 Jun 2026 00:47:15 GMT
ENV PG_VERSION=19~beta1-1.pgdg13+1
# Thu, 11 Jun 2026 00:59:47 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 11 Jun 2026 00:59:47 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 11 Jun 2026 00:59:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 11 Jun 2026 00:59:47 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Thu, 11 Jun 2026 00:59:47 GMT
VOLUME [/var/lib/postgresql]
# Thu, 11 Jun 2026 00:59:48 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:59:48 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 11 Jun 2026 00:59:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:59:48 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jun 2026 00:59:48 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 11 Jun 2026 00:59:48 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4bd6ddea06d5009ee47ddb0f254a2569aff0230c005869ebd416b20295d945c0`  
		Last Modified: Wed, 10 Jun 2026 23:42:34 GMT  
		Size: 26.2 MB (26211004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97603e6dc37aea860afe37b37888ac0e5d484cff92b3ece063171e2f22b7ae6`  
		Last Modified: Thu, 11 Jun 2026 01:00:00 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21292ff823b8a9ac51b706b3586bc5d7ab9f09f827ebeda53afc02686f1fb012`  
		Last Modified: Thu, 11 Jun 2026 01:00:00 GMT  
		Size: 5.5 MB (5497334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2c42239a078370c16e2bce80178d70cfe203818e5627d1927a46fee395103d`  
		Last Modified: Thu, 11 Jun 2026 01:00:00 GMT  
		Size: 1.2 MB (1222450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb0a3b3a8d2df6126ab067265ce33d45e955873b6480a90b034c5fe28913d46`  
		Last Modified: Thu, 11 Jun 2026 01:00:00 GMT  
		Size: 8.2 MB (8204110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc17354c43256b75cde4000f1f222bd208e14ab4a529322d190172bf6bcc74c4`  
		Last Modified: Thu, 11 Jun 2026 01:00:01 GMT  
		Size: 1.2 MB (1172654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e21e65e125ac07ee53ee5f649822906795e85f29fcdbde9a94a418d344ad9aa`  
		Last Modified: Thu, 11 Jun 2026 01:00:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b084f31edec69aecd0295112ec3aad314991c8da426b3c8f412f96e18c6ec0d8`  
		Last Modified: Thu, 11 Jun 2026 01:00:01 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722d079247e2ead196421b87728193c68c711d2af0d7a0f7c846c1435883af0d`  
		Last Modified: Thu, 11 Jun 2026 01:00:04 GMT  
		Size: 45.9 MB (45942551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fb4eb8f9f894bfb79f9f9dad94833e0bba2bc99117615553998e4114803055`  
		Last Modified: Thu, 11 Jun 2026 01:00:03 GMT  
		Size: 21.4 KB (21425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8675d4b861538d8e95d30c322607510d07213b92a1eae1e60eeb362579736e9e`  
		Last Modified: Thu, 11 Jun 2026 01:00:04 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc69265294fdd4859110c9e8aab7363400c6c364573e8761057252d17fe48e9`  
		Last Modified: Thu, 11 Jun 2026 01:00:04 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898eb4a760e039d3ee8784303fc123210370f4a0df19eb3f782ac42734c20219`  
		Last Modified: Thu, 11 Jun 2026 01:00:05 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:c8da04c04c71237fdf400f1e16f09153219f326b7633c0bee8dfc738e9a5246e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5178907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccd348e864c38adbccd5e1a0a013f6fcf4c617b3cc4067b33f78869173e87343`

```dockerfile
```

-	Layers:
	-	`sha256:e3c964c8647c4ec77d6a98da8e736b19d230c3e67536192b98bbec96bc50a9e4`  
		Last Modified: Thu, 11 Jun 2026 01:00:00 GMT  
		Size: 5.1 MB (5127434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce75e547ac01c9276e801a41b7be49707d9556e51a70f12ef4911a76c9d60ba6`  
		Last Modified: Thu, 11 Jun 2026 01:00:00 GMT  
		Size: 51.5 KB (51473 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-trixie` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:814bc4db94bbe72b88ac42b2e5d0d11d216553d75c570a7e14add1e0c7e0a94d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.2 MB (162206165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48880507b320060932dbc29dbfbe5bb88d6383b5040b8bc36233d638b17f5a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:35:15 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 11 Jun 2026 00:35:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:35:30 GMT
ENV GOSU_VERSION=1.19
# Thu, 11 Jun 2026 00:35:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 11 Jun 2026 00:35:35 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 11 Jun 2026 00:35:35 GMT
ENV LANG=en_US.utf8
# Thu, 11 Jun 2026 00:35:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:35:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Jun 2026 00:35:40 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:35:40 GMT
ENV PG_MAJOR=19
# Thu, 11 Jun 2026 00:35:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/19/bin
# Thu, 11 Jun 2026 00:35:40 GMT
ENV PG_VERSION=19~beta1-1.pgdg13+1
# Thu, 11 Jun 2026 00:36:02 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 11 Jun 2026 00:36:02 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 11 Jun 2026 00:36:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 11 Jun 2026 00:36:03 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Thu, 11 Jun 2026 00:36:03 GMT
VOLUME [/var/lib/postgresql]
# Thu, 11 Jun 2026 00:36:03 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:36:03 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 11 Jun 2026 00:36:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:36:03 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jun 2026 00:36:03 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 11 Jun 2026 00:36:03 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf107e9ced296b2cf7b764ac39772fc84832350a08f96a457d5e3279a3168f2`  
		Last Modified: Thu, 11 Jun 2026 00:36:22 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c3acb06f50e2aef98ba17051a0816784c1428699e417402716f1dbafdad4b2`  
		Last Modified: Thu, 11 Jun 2026 00:36:23 GMT  
		Size: 6.2 MB (6235173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9cfaff3447e48d82e5b8092a32f6650af7467102a07bc785bf46b0d89e2a2e`  
		Last Modified: Thu, 11 Jun 2026 00:36:22 GMT  
		Size: 1.2 MB (1209596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a70aabb22c1c15cca9b6b98e4fe1f97a2a3b68d450c724f9203d75a4a647a64`  
		Last Modified: Thu, 11 Jun 2026 00:36:23 GMT  
		Size: 8.2 MB (8204061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1839ffb73fec6c7b63a6c127cc17b193a9db85fe80c3c26fb260b695163de9c`  
		Last Modified: Thu, 11 Jun 2026 00:36:23 GMT  
		Size: 1.2 MB (1220601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea1edd0577deb996d310427e3acfae2aac86fbedd6890d542e6ce1ad2c4e13c`  
		Last Modified: Thu, 11 Jun 2026 00:36:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ee1976a32ff9342938829c9cb94c48c8e7566914b95bee4bff6aeeab9ce64b`  
		Last Modified: Thu, 11 Jun 2026 00:36:24 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eead0285510edda6d9ff7a3e373abe833d1ff6ca594afbc4783bfa4240473df3`  
		Last Modified: Thu, 11 Jun 2026 00:36:27 GMT  
		Size: 115.2 MB (115155953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9cf1b301aaadf41fb7def73a790510e37418f8ccfed684428e1cf88185f17f`  
		Last Modified: Thu, 11 Jun 2026 00:36:25 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815f7407646f692a375ccf35c959e1a7b7a6b0ca29f54a6eadc88be3c57d6488`  
		Last Modified: Thu, 11 Jun 2026 00:36:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e654c6f3f22ea5c40c3aca94b98fab67586d70ae53c82405a3641d2d8393cf`  
		Last Modified: Thu, 11 Jun 2026 00:36:26 GMT  
		Size: 6.1 KB (6095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a427ee75a3dff3d35e25bd451ba2e6264dd704e939cf77d2ddafeca86ddc844`  
		Last Modified: Thu, 11 Jun 2026 00:36:26 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:568794ee7801c3e99c7d4093a6146e7c3766c17c1aad2ec316feca0aa6382da7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6055716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:988017a5576a545932c3cea14ba5ba352ac3af0e423201ce59889e5b536b0c7d`

```dockerfile
```

-	Layers:
	-	`sha256:1eb5cf05af7fd875c299e7e484c7ef786197eecd6f25b750fb7dad72bdb5f9b3`  
		Last Modified: Thu, 11 Jun 2026 00:36:23 GMT  
		Size: 6.0 MB (6004202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5b2d034ea67c7b8cd78e2427b17c99a61b65557756d0c03d8629b4463a04e77`  
		Last Modified: Thu, 11 Jun 2026 00:36:22 GMT  
		Size: 51.5 KB (51514 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-trixie` - linux; 386

```console
$ docker pull postgres@sha256:2efea73af624a34e145340effc3d0f3d8d583e1dfe4135ec5b0e61bfd00de88f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.2 MB (98196339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe54ab09db7d1f494d717c239624afcbcf39a688a4c25b44fd71af2733f20ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:30:27 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 11 Jun 2026 00:30:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:30:43 GMT
ENV GOSU_VERSION=1.19
# Thu, 11 Jun 2026 00:30:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 11 Jun 2026 00:30:49 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 11 Jun 2026 00:30:49 GMT
ENV LANG=en_US.utf8
# Thu, 11 Jun 2026 00:30:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:30:53 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Jun 2026 00:30:53 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:30:53 GMT
ENV PG_MAJOR=19
# Thu, 11 Jun 2026 00:30:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/19/bin
# Thu, 11 Jun 2026 00:30:53 GMT
ENV PG_VERSION=19~beta1-1.pgdg13+1
# Thu, 11 Jun 2026 00:41:11 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 11 Jun 2026 00:41:11 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 11 Jun 2026 00:41:11 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 11 Jun 2026 00:41:11 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Thu, 11 Jun 2026 00:41:11 GMT
VOLUME [/var/lib/postgresql]
# Thu, 11 Jun 2026 00:41:11 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:41:11 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 11 Jun 2026 00:41:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:41:11 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jun 2026 00:41:11 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 11 Jun 2026 00:41:11 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:720f951a68f4f9ab464e52b53cf88cfb86bc876b3f00956d000420777ab93c0c`  
		Last Modified: Wed, 10 Jun 2026 23:40:30 GMT  
		Size: 31.3 MB (31301194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc421d1215109c28dfba0cdb1fc34b8a24eeafb2c9b53ac993bde9501cec913`  
		Last Modified: Thu, 11 Jun 2026 00:41:24 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5f9af2a917e9925f48c6a2dfe93a783353e817445aceaa1049f4904b31b347`  
		Last Modified: Thu, 11 Jun 2026 00:41:24 GMT  
		Size: 6.6 MB (6631442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317fd97929a7a2927a6f9a38d5d9d9a7e5fe425226263baacd39a469a480109c`  
		Last Modified: Thu, 11 Jun 2026 00:41:24 GMT  
		Size: 1.2 MB (1225880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0274fdd90af9eb86eb90d423200bb8172a0ed4ab8b63a248a1ceb4c7676a03`  
		Last Modified: Thu, 11 Jun 2026 00:41:24 GMT  
		Size: 8.2 MB (8204092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95bdc126530c964db2e2a23dfdf752f9eb4e178edc91e90cd838f8f92488fedb`  
		Last Modified: Thu, 11 Jun 2026 00:41:26 GMT  
		Size: 1.3 MB (1308280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e7c6e240ad8b26b04c029176586c0285ace2a7166907c47a231eb0f978e98c`  
		Last Modified: Thu, 11 Jun 2026 00:41:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43430ce0dfa05fe6c6de06d7ddbfd18f9e58e0cb8b989f581dd5f2aea7fa32be`  
		Last Modified: Thu, 11 Jun 2026 00:41:25 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0853f1a39278bfdbb59ff2cc482fa359bb7be8dc6fedd395003f5b071186f118`  
		Last Modified: Thu, 11 Jun 2026 00:41:28 GMT  
		Size: 49.5 MB (49493200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76bc1c651b56365ebf19f5d8154cc86a4b6ca6c735cabf3d3e31194f55f19d2c`  
		Last Modified: Thu, 11 Jun 2026 00:41:27 GMT  
		Size: 21.4 KB (21417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0536785cd1986cd0922db0c360a5cca878e1f8611b249d0031202bb4ebe633`  
		Last Modified: Thu, 11 Jun 2026 00:41:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b9b9737e691b911bd36ade153ac337e976202eedcd04048339311d92fc2add`  
		Last Modified: Thu, 11 Jun 2026 00:41:27 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ea4b09c06b7b0ca591b02495652ebe2c66a3a977e50d031b54e0fd88d2a7b6`  
		Last Modified: Thu, 11 Jun 2026 00:41:28 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:61e041e5fdff3ae3861b58377c499267c86bcfa87039eb8d84746aec0bab955d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5174751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23f8a5926ef9cfcd375ad357362e8ab55f3f769af906710fe978846b3108c726`

```dockerfile
```

-	Layers:
	-	`sha256:333002557e0a368b4c1e935e7f5a4e3ad093c9641e61f3882fc504242179699c`  
		Last Modified: Thu, 11 Jun 2026 00:41:24 GMT  
		Size: 5.1 MB (5123514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db87d1d80aadcf8c1195edd49a79a3b3d8aa8a0afc49b1fb487c68b22b320eb0`  
		Last Modified: Thu, 11 Jun 2026 00:41:24 GMT  
		Size: 51.2 KB (51237 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-trixie` - linux; ppc64le

```console
$ docker pull postgres@sha256:a04af75da7b8294991eeb9de0b647a959de85ff00e1839fae4ca7d848302e23b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176125661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9806b60c6a2905bcf73197409462c70b41fad0121a780cabc8874db62945aa71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 04:22:16 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 11 Jun 2026 04:22:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 04:22:45 GMT
ENV GOSU_VERSION=1.19
# Thu, 11 Jun 2026 04:22:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 11 Jun 2026 04:22:57 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 11 Jun 2026 04:22:57 GMT
ENV LANG=en_US.utf8
# Thu, 11 Jun 2026 04:23:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 04:23:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Jun 2026 04:23:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 04:23:06 GMT
ENV PG_MAJOR=19
# Thu, 11 Jun 2026 04:23:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/19/bin
# Thu, 11 Jun 2026 04:23:06 GMT
ENV PG_VERSION=19~beta1-1.pgdg13+1
# Thu, 11 Jun 2026 04:23:52 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 11 Jun 2026 04:23:52 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 11 Jun 2026 04:23:53 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 11 Jun 2026 04:23:53 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Thu, 11 Jun 2026 04:23:53 GMT
VOLUME [/var/lib/postgresql]
# Thu, 11 Jun 2026 04:23:53 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 04:23:53 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 11 Jun 2026 04:23:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 04:23:53 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jun 2026 04:23:53 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 11 Jun 2026 04:23:53 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e93abe7480356a6fc8ce6943b71e051b601733a1b3eec3b84b51ba066f7ebb`  
		Last Modified: Thu, 11 Jun 2026 04:24:34 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e50b953d51df1ad75aa8423fe4c0b925ff04cb0f00fc9bf7d832470c0113811`  
		Last Modified: Thu, 11 Jun 2026 04:24:34 GMT  
		Size: 7.1 MB (7076806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b50b5ff568aaa483897ee3a1d850dd075b9e6655d095d44de11470d6f8fc009`  
		Last Modified: Thu, 11 Jun 2026 04:24:34 GMT  
		Size: 1.2 MB (1214789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd8cddd4d91d1f798bf8f04a08fd19f0142e2c39271c68c2550b9e9fd0cc832`  
		Last Modified: Thu, 11 Jun 2026 04:24:35 GMT  
		Size: 8.2 MB (8204074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93bda34c5d2b40061a1e23c1b4ffa3a2ae3eaf4b9cb20d75b9698f949074d325`  
		Last Modified: Thu, 11 Jun 2026 04:24:36 GMT  
		Size: 1.4 MB (1394935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7053b7edc10475c2c4219fcbafcdaa68460b254fc0f37b9ce94c177fb20f36a2`  
		Last Modified: Thu, 11 Jun 2026 04:24:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc5c991fdba4277fa6991ebe8b974a0fa349af5e7830ce228f1bfac146a2248`  
		Last Modified: Thu, 11 Jun 2026 04:24:36 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e82055c16584e4d6dc5b19f2ab83ccd3f55c4986c59c074b95b02d5833db8bf`  
		Last Modified: Thu, 11 Jun 2026 04:24:39 GMT  
		Size: 124.6 MB (124596475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9db9e375b9a4cc14185787d2685150e5ed5480f1a0d38d58827cbd9403dde9c`  
		Last Modified: Thu, 11 Jun 2026 04:24:37 GMT  
		Size: 21.4 KB (21408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6942adb7664628c63190ba2c8fb0912f80fccadf6ec7f9adc2f931504ab35d67`  
		Last Modified: Thu, 11 Jun 2026 04:24:38 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98de1c59182d4dacee4b70817a629e2bffb18eee093d1a03a28d523dfc7b2d7`  
		Last Modified: Thu, 11 Jun 2026 04:24:38 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec3b1141ba943f9e7110f0405ab16448ef842b1ebb41e076e6eec84748fb68a`  
		Last Modified: Thu, 11 Jun 2026 04:24:39 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:70cb45d5ac0de27cf3868b0d542ec80c647f4dd23eaccca71720bb5cfe98c3b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6055845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4fa98e54d01b5aa51545ab8abe446afe09ae9d702c7241086c0964db7f944e`

```dockerfile
```

-	Layers:
	-	`sha256:6730536cca1c8165d4048b8af8e221e40cd7060e0b99a5669750498d05ac41c6`  
		Last Modified: Thu, 11 Jun 2026 04:24:34 GMT  
		Size: 6.0 MB (6004509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dc910b6b3f50667c618db098faa5e783582489617ad6d86691f9752183d0fe2`  
		Last Modified: Thu, 11 Jun 2026 04:24:34 GMT  
		Size: 51.3 KB (51336 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-trixie` - linux; riscv64

```console
$ docker pull postgres@sha256:3f42e923dfd25f6de327932c61c45bd0c1495dae82b6cda13058a09d3d4fdd2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93373848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b80975e88651d0e1845e9c6a665be56fd40052f5bd1056863719faa3fe8d59f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Thu, 21 May 2026 02:50:07 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 May 2026 02:51:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 May 2026 02:52:03 GMT
ENV GOSU_VERSION=1.19
# Thu, 21 May 2026 02:52:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 May 2026 02:53:05 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 21 May 2026 02:53:05 GMT
ENV LANG=en_US.utf8
# Thu, 21 May 2026 02:53:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jun 2026 08:35:48 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 06 Jun 2026 08:35:49 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 06 Jun 2026 08:35:49 GMT
ENV PG_MAJOR=19
# Sat, 06 Jun 2026 08:35:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/19/bin
# Sat, 06 Jun 2026 08:35:49 GMT
ENV PG_VERSION=19~beta1-1.pgdg13+1
# Sat, 06 Jun 2026 10:46:56 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Sat, 06 Jun 2026 10:46:56 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 06 Jun 2026 10:46:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 06 Jun 2026 10:46:57 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Sat, 06 Jun 2026 10:46:57 GMT
VOLUME [/var/lib/postgresql]
# Sat, 06 Jun 2026 10:46:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 10:46:58 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 06 Jun 2026 10:46:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Jun 2026 10:46:58 GMT
STOPSIGNAL SIGINT
# Sat, 06 Jun 2026 10:46:58 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 06 Jun 2026 10:46:58 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff80fab2ceef62152f851f145dff3e1b25c48ee0dc516ea3c5f794f1de277e4a`  
		Last Modified: Thu, 21 May 2026 04:57:58 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ebf27cb3c66e3558679585eb0ce15e35dffeb04046d13139cfa9828b8aecbe8`  
		Last Modified: Thu, 21 May 2026 04:58:00 GMT  
		Size: 6.3 MB (6293113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6e1d6536f4a123cdebd63843f1424aa7930dccbf70ff78c5840e6f97d7db65`  
		Last Modified: Thu, 21 May 2026 04:57:58 GMT  
		Size: 1.2 MB (1202056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3c1ee862684d21c2fb3519828f08b7512c7907ca5be82aefb1f418bc2b9541`  
		Last Modified: Thu, 21 May 2026 04:58:01 GMT  
		Size: 8.2 MB (8203742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0d86390b30ab815ee7aa2d1e66b827fd12b514cc6ac7eff4c2abf72df3b699`  
		Last Modified: Thu, 21 May 2026 04:58:01 GMT  
		Size: 1.4 MB (1402363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae38be4fff78abdb0c0e2378162f5c3da78eb9a1deee38905ebc3c567505af7`  
		Last Modified: Sat, 06 Jun 2026 10:49:26 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc44bde68b10a90f30acefbbc215d67ce320a4b10d8c550cce2594a7563cab8`  
		Last Modified: Sat, 06 Jun 2026 10:49:26 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3c7b5dcf3bfbb8dee953537e64a355dfc98db43bfcc37c1ea1c6b5c990d4dd`  
		Last Modified: Sat, 06 Jun 2026 10:49:34 GMT  
		Size: 48.0 MB (47962717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48944586491fe11dd39fc6a338c5e983e7e2d3822412a4d3a071efccb1ffa797`  
		Last Modified: Sat, 06 Jun 2026 10:49:26 GMT  
		Size: 21.4 KB (21424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a88e4e4fce589f326731ecc16dc5ebb97fa0e95622e77b0c143bd636f8e479d`  
		Last Modified: Sat, 06 Jun 2026 10:49:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c3be94a21cb220b095fd897d95f0f17fb85de7ba074d3f64a2817b9866b576`  
		Last Modified: Sat, 06 Jun 2026 10:49:27 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385ac1c2d9a8075caa080f90692b02c84c5862adae2cd763c3371c8611b9bbeb`  
		Last Modified: Sat, 06 Jun 2026 10:49:28 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:84a980770136463aa4f350480b1cd8a481d50f7bcc7d4667df609914ff34b433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5169723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5f5d75f297dbbadcdd00cec4df12b5dfcde88d84172582d8c82a8caccc60cb`

```dockerfile
```

-	Layers:
	-	`sha256:3eee072fd644effadf2900704f587e286489d7d9f4bfbca0204374248444f9dc`  
		Last Modified: Sat, 06 Jun 2026 10:49:27 GMT  
		Size: 5.1 MB (5118392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fee4bc697f667380fe870bbf009900a9f28c80d20ea240f05184908db38f730d`  
		Last Modified: Sat, 06 Jun 2026 10:49:26 GMT  
		Size: 51.3 KB (51331 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-trixie` - linux; s390x

```console
$ docker pull postgres@sha256:33a854040ec89de353a4f180d2399a0e920b3f9ead3d6aefd5611464c5160a0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.3 MB (178324156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f9123aaf2f5a7d5c988ad2c645e48af1a2c27af27d142fee5dc094c0ca9421`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:58:49 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 11 Jun 2026 00:58:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:59:02 GMT
ENV GOSU_VERSION=1.19
# Thu, 11 Jun 2026 00:59:02 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 11 Jun 2026 00:59:07 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 11 Jun 2026 00:59:07 GMT
ENV LANG=en_US.utf8
# Thu, 11 Jun 2026 00:59:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:59:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Jun 2026 00:59:12 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:59:12 GMT
ENV PG_MAJOR=19
# Thu, 11 Jun 2026 00:59:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/19/bin
# Thu, 11 Jun 2026 00:59:12 GMT
ENV PG_VERSION=19~beta1-1.pgdg13+1
# Thu, 11 Jun 2026 01:12:47 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 11 Jun 2026 01:12:47 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 11 Jun 2026 01:12:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 11 Jun 2026 01:12:47 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Thu, 11 Jun 2026 01:12:47 GMT
VOLUME [/var/lib/postgresql]
# Thu, 11 Jun 2026 01:12:47 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 01:12:47 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 11 Jun 2026 01:12:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 01:12:47 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jun 2026 01:12:47 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 11 Jun 2026 01:12:47 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2915c4a1da6ba1b5bdd1dff2922470fb42439fbc4aaeb0d4583be34c20f4928d`  
		Last Modified: Thu, 11 Jun 2026 01:13:18 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4c357e6cade9d027438084d6a03ffa68e4c73be534ae8495b66c5679c7e894`  
		Last Modified: Thu, 11 Jun 2026 01:13:19 GMT  
		Size: 6.4 MB (6408449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2ea20c618ff0ba3fe7c87d3096e2468025fd6479d5ee837915833393f855ad`  
		Last Modified: Thu, 11 Jun 2026 01:13:18 GMT  
		Size: 1.2 MB (1230281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29041be68bbe8c2d12e6c94fa87befb9fec508ed40ea5399c9a4d09e50fe1fc0`  
		Last Modified: Thu, 11 Jun 2026 01:13:19 GMT  
		Size: 8.3 MB (8258963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066e5fb9d56eef945c4370a23076bb39b6dc4f5a48068916742ea67392b0a055`  
		Last Modified: Thu, 11 Jun 2026 01:13:20 GMT  
		Size: 1.4 MB (1398236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f9aab3dfa17802d7f871671d99a6fb7e990f0c0d0f1f92d8d361de716084c9`  
		Last Modified: Thu, 11 Jun 2026 01:13:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a44f6bed2f8bf0cef40d26f3fb11d402aa700bd5caee563b557f24a9c2f22df2`  
		Last Modified: Thu, 11 Jun 2026 01:13:20 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c526f7385b063751bca683849420ebe61991115c2340e597015317de875125`  
		Last Modified: Thu, 11 Jun 2026 01:13:23 GMT  
		Size: 131.1 MB (131144619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9bc6072e67dc8b310b97af63357746a6cf5598ae262b0caea57dc47341306e`  
		Last Modified: Thu, 11 Jun 2026 01:13:21 GMT  
		Size: 21.4 KB (21421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0387423a9a8441a90db28a268cf87777f59c36ee219bdf91d027775ecbea29`  
		Last Modified: Thu, 11 Jun 2026 01:13:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3181c2743db8d9c48aaca02e24e640bf90fc2f5e8bdd9c89135daee03a5620ad`  
		Last Modified: Thu, 11 Jun 2026 01:13:21 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b9616f3d2422b982c1b512614c7bde72198005ebb5025ca43ac4f22be041c20`  
		Last Modified: Thu, 11 Jun 2026 01:13:22 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:ec6428b12557062a0578d2d649f6373b635dadc5ca70ca87998380d2811a6b4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6065838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6a1e1e796374ee1bdf7a8a780821c937167ae7c5bf908e6f8e40a66242485b`

```dockerfile
```

-	Layers:
	-	`sha256:95e266b25b25b67191b09e08d5523cf093d62b4ad6b6218ad301d069bc24125b`  
		Last Modified: Thu, 11 Jun 2026 01:13:19 GMT  
		Size: 6.0 MB (6014555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c8b452dcaa2c4116433c8186960a8451938d36cbf276b03cc253ab1f4d4d597`  
		Last Modified: Thu, 11 Jun 2026 01:13:19 GMT  
		Size: 51.3 KB (51283 bytes)  
		MIME: application/vnd.in-toto+json
