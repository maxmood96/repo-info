## `postgres:15-bookworm`

```console
$ docker pull postgres@sha256:69c679b1889a50217027a9b3fef86dd5ca4f744869f18b05bbf64106b8cb45cd
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
$ docker pull postgres@sha256:bdc41bb1e867c47363d8e70da707cd481b630cf02e55ab483ce71feb685a0037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.9 MB (152888452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae2091e79919e9e2623ed5e7fe6a89ba158aca6d8fedfa4fb893069b5d9448d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Oct 2025 18:23:03 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENV GOSU_VERSION=1.19
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENV LANG=en_US.utf8
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PG_MAJOR=15
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PG_VERSION=15.14-1.pgdg12+1
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 15 Oct 2025 18:23:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 15 Oct 2025 18:23:03 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Oct 2025 18:23:03 GMT
STOPSIGNAL SIGINT
# Wed, 15 Oct 2025 18:23:03 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 15 Oct 2025 18:23:03 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c1d07d458db9ccaf4723ec91f591635694ff1dc3bd2a0c3e6b5baa395c5068`  
		Last Modified: Wed, 22 Oct 2025 17:43:14 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9e3a3e06c73ccde367af1b02e6c55fcd48ff094df24433ba557e9e9002581e`  
		Last Modified: Wed, 22 Oct 2025 17:43:15 GMT  
		Size: 4.5 MB (4534000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2d68e5f0acecfc8be10fda2c362ec5b3ddc1017f07960381f9f9685c59b02d`  
		Last Modified: Wed, 22 Oct 2025 17:43:14 GMT  
		Size: 1.2 MB (1249480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55942864272a60be11d635407bd915598a411511cd90b8af87cdcc0aa6c2461b`  
		Last Modified: Wed, 22 Oct 2025 17:43:15 GMT  
		Size: 8.1 MB (8066496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7f29c5dc66b91b82b17a26bcc651dc1deffcaf1e9c7e7018213d33ff3b7479`  
		Last Modified: Wed, 22 Oct 2025 17:43:14 GMT  
		Size: 1.2 MB (1196373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2378fb4ee2701efe67b1f5739a702164e2d731edbfbaac0495576781aaa17d71`  
		Last Modified: Wed, 22 Oct 2025 17:43:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba5f32ffb87e6c1ab6a00298af060c08314f44e57092acb3171adf0676900cf`  
		Last Modified: Wed, 22 Oct 2025 17:43:14 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10a92d9ae1168fe282bb96d787ec27ba92d93ac4b0a24ff463efe21b3e30f8e`  
		Last Modified: Wed, 22 Oct 2025 17:43:25 GMT  
		Size: 109.6 MB (109593020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d1b5f6132681cdbdef334386b755d2f2b48dc7f86a7c858063c9c26b143a52`  
		Last Modified: Wed, 22 Oct 2025 17:43:14 GMT  
		Size: 9.8 KB (9777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3efacb9a972d9daec65854975108cf82c27e06b31369086eb199ae187bf29c0a`  
		Last Modified: Wed, 22 Oct 2025 17:43:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bfde3de72cc25dd2c0c986d52db1ee17db02c40a01de2d96e591ff1348c0e8`  
		Last Modified: Wed, 22 Oct 2025 17:43:14 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b241b2c75d4b496b4877622b74839997637cc69cd082025c5bfa5dcbeda0808`  
		Last Modified: Wed, 22 Oct 2025 17:43:14 GMT  
		Size: 6.1 KB (6078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6fded3c8ea0aad518d8d58c0db67364797ad3198193acfde76b2815d48e66c`  
		Last Modified: Wed, 22 Oct 2025 17:43:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:4396c0bc2193bfe4be2a2c905b8f1bcd685ee6f00d9069f4244d3e874a28d077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5896677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727e766083103f05ee5449088ee21b4ebc3ff6cb453e2658c783329d0e9e3524`

```dockerfile
```

-	Layers:
	-	`sha256:24088426c06ee01dc66fccf233dbec0d1f969aef60f07d1b223cc9d310fb5e5d`  
		Last Modified: Wed, 22 Oct 2025 20:13:36 GMT  
		Size: 5.8 MB (5843338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c02cde715d6c3aeed1b1763b7304a20eb49af1bb0bdf3f0b08d042f11d992496`  
		Last Modified: Wed, 22 Oct 2025 20:13:37 GMT  
		Size: 53.3 KB (53339 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:cbf6741a32e6c2723510c2d3f53bfab775048a0886969cdc0bfcfa563ceb969c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.8 MB (145823239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a30b3a7087caa2450ef5127c325c3e83def7ca796667e6a02f02f24150bc380a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 01:19:02 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Nov 2025 01:19:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:19:18 GMT
ENV GOSU_VERSION=1.19
# Tue, 04 Nov 2025 01:19:18 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 01:19:25 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 04 Nov 2025 01:19:25 GMT
ENV LANG=en_US.utf8
# Tue, 04 Nov 2025 01:19:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:19:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Nov 2025 01:19:31 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:19:31 GMT
ENV PG_MAJOR=15
# Tue, 04 Nov 2025 01:19:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 04 Nov 2025 01:19:31 GMT
ENV PG_VERSION=15.14-1.pgdg12+1
# Tue, 04 Nov 2025 01:33:54 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 04 Nov 2025 01:33:54 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Nov 2025 01:33:54 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Nov 2025 01:33:54 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Nov 2025 01:33:54 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 04 Nov 2025 01:33:54 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Nov 2025 01:33:54 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:33:54 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Nov 2025 01:33:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:33:54 GMT
STOPSIGNAL SIGINT
# Tue, 04 Nov 2025 01:33:54 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Nov 2025 01:33:54 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:def4b77141116a067c72a4f39eb9fa70634fe918be6e3df3cf0bc46323be22c7`  
		Last Modified: Tue, 04 Nov 2025 00:12:34 GMT  
		Size: 25.8 MB (25757661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ed6a55981ad169bbb4df2c64c402e3ced78365c4ed236e77d91b2fe9f50a4f`  
		Last Modified: Tue, 04 Nov 2025 01:34:25 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68009d11cff971314b948d45e26cadc8c625bff4a0c53f8524fd3e0f22eeabb`  
		Last Modified: Tue, 04 Nov 2025 01:34:26 GMT  
		Size: 4.2 MB (4151198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99135c3c73dc06aa8bc91fcab137114c173922ff4598ac69857529e556364f2b`  
		Last Modified: Tue, 04 Nov 2025 01:34:25 GMT  
		Size: 1.2 MB (1220045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4703a95bbb38377c941db3e9a6ffac18c3137c44fff10b48a9871355fa76b80`  
		Last Modified: Tue, 04 Nov 2025 01:34:26 GMT  
		Size: 8.1 MB (8066533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae6bb2effbd66d1ca39ecc98bf76b1258792c63b6d60787f88b1c137b489332`  
		Last Modified: Tue, 04 Nov 2025 01:34:25 GMT  
		Size: 1.2 MB (1195017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859b46957c9002b18b71b23adfa36b79b36315feb92cd7cc7404bccbfb989e7f`  
		Last Modified: Tue, 04 Nov 2025 01:34:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4bbd29790aecd8b9e133aae55abdb5aa02588a0e72d93de7281b227693bd57`  
		Last Modified: Tue, 04 Nov 2025 01:34:25 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7e981e1a1fafaf0f247f4044254302788a718e1229059078b5e7f182a75b78`  
		Last Modified: Tue, 04 Nov 2025 01:34:33 GMT  
		Size: 105.4 MB (105412028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7ef654800d9191ab4001dfb9f1d40436c25b8a8c970b3bbdf6e2389c7fc25c`  
		Last Modified: Tue, 04 Nov 2025 01:34:26 GMT  
		Size: 9.8 KB (9776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7b064ef20200c1a6809747289bb481a44b6eeb7600d75fda3795df84a5a8cd`  
		Last Modified: Tue, 04 Nov 2025 01:34:26 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247162284c0f0fab28779ae74594738d55c4b736e6997796f4c48a69a6078dfb`  
		Last Modified: Tue, 04 Nov 2025 01:34:25 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509aeda32314a832b9c8029e602636d3a002824bc4b2a3c97a7dab59ae43d533`  
		Last Modified: Tue, 04 Nov 2025 01:34:25 GMT  
		Size: 6.1 KB (6079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c125b948880422e1440c1fc74fd9f3d9d228b1abafb41fa53f0b9f872c3f755`  
		Last Modified: Tue, 04 Nov 2025 01:34:25 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:5d4bb7f80e80aa3e2475ca7213af44d2353208163b93345666ebfbd22c14e02d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5910941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfaea271803b92c3af8208298a951867edbd0098b7db12462342b85ae52717a8`

```dockerfile
```

-	Layers:
	-	`sha256:45abbf90a1a8c249c3f1d34045075fc649aaa2822fb84c668c348111b9b5dddc`  
		Last Modified: Tue, 04 Nov 2025 09:09:37 GMT  
		Size: 5.9 MB (5857439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5d9a9289d6e5944163c6c350914eecdd9401a35357b12955799d12cdc585a5b`  
		Last Modified: Tue, 04 Nov 2025 09:09:37 GMT  
		Size: 53.5 KB (53502 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:42615492c3bee8bbf7321235f9583e88501a71e8de4207567188df9b50fa6e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140913635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9916fa92ebfb90638c28e2a204df426a251c7667218b148f7bfe3f7b1d13b2be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Oct 2025 18:23:03 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENV GOSU_VERSION=1.19
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENV LANG=en_US.utf8
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PG_MAJOR=15
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PG_VERSION=15.14-1.pgdg12+1
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 15 Oct 2025 18:23:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 15 Oct 2025 18:23:03 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Oct 2025 18:23:03 GMT
STOPSIGNAL SIGINT
# Wed, 15 Oct 2025 18:23:03 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 15 Oct 2025 18:23:03 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4f520125372ffa3e5f64f19eebfdfce1c8314446e9e3ab2629f5c13cacbd8345`  
		Last Modified: Tue, 21 Oct 2025 00:20:18 GMT  
		Size: 23.9 MB (23934023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273ffece88b524b37a5d4054254df7a46105227ff52196e20b468239023f527b`  
		Last Modified: Wed, 22 Oct 2025 18:20:47 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36cbb8eebedea66302ed6e375ca79e184e0447a6d906a08d4e81d08e79ef1d7f`  
		Last Modified: Wed, 22 Oct 2025 18:20:47 GMT  
		Size: 3.7 MB (3742680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751a0c377f04b221a8b16fa37b14d088ecd3cf1d55677372edf32e3467abaaa6`  
		Last Modified: Wed, 22 Oct 2025 18:20:47 GMT  
		Size: 1.2 MB (1216003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789785de60f331019a4397e15f5a66919c6ba7844056ba0afc700b803e2a06dc`  
		Last Modified: Wed, 22 Oct 2025 18:20:48 GMT  
		Size: 8.1 MB (8066476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa216a2675fc1fdb5252f62d96e456f748087236a69b7413a516be6ff4a2183`  
		Last Modified: Wed, 22 Oct 2025 18:20:47 GMT  
		Size: 1.1 MB (1067222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e1789fd64930f9700bf5df353518d5eb069e3dd08bf4890c21628019b94493`  
		Last Modified: Wed, 22 Oct 2025 18:20:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85737b35d58738a5deea243cff640dfbf91a1ed93d673c696cac10fc4c485358`  
		Last Modified: Wed, 22 Oct 2025 18:20:47 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2baba9ffcb3094c65f2b3d2e39499c9d91e5aa19fd78fc690b289ec83dc8be2f`  
		Last Modified: Wed, 22 Oct 2025 18:20:57 GMT  
		Size: 102.9 MB (102866465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa81962d330ccf62fad65a62bee18baf80f3344fd3e95e5ee662e0c487c2a7a5`  
		Last Modified: Wed, 22 Oct 2025 18:20:47 GMT  
		Size: 9.8 KB (9781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b9c9ba9002594ad548fe6a647dfb547eb970ac015e80c9ac51b5700143d00d2`  
		Last Modified: Wed, 22 Oct 2025 18:20:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f103cfb57f5ebc09d717f8dfcbfdd0e35f635d4e6ff2443285268268f89e6a40`  
		Last Modified: Wed, 22 Oct 2025 18:20:47 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca04a1c7dee9862d9dcb9020e0144dbbe4d40a98c9baf1e1d6bdd36359bda4a`  
		Last Modified: Wed, 22 Oct 2025 18:20:47 GMT  
		Size: 6.1 KB (6081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2667cbc21e42915817078774b90ab5f6d79ac28f283a9480474eae247db4c57`  
		Last Modified: Wed, 22 Oct 2025 18:20:53 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:884158a0c9cadc27d1543446cc8fdad9488ab30821841bbbe561fd0f2579fefc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5910240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:684c03356820214d1f2df7e15b8856b0485f01da6aff9cdd3dd726149a55cc70`

```dockerfile
```

-	Layers:
	-	`sha256:cee65329c76d116d33a23fefa75efc7b08d7560d93a8b310a982edb81e49b33e`  
		Last Modified: Wed, 22 Oct 2025 20:13:49 GMT  
		Size: 5.9 MB (5856694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4b288bad6ec3bc8e76296f7c0f349d1fec68b5419ee7ad4d554286a57f72f41`  
		Last Modified: Wed, 22 Oct 2025 20:13:50 GMT  
		Size: 53.5 KB (53546 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:134b57141c5f84f9fb7142a77aa8cc2c48d88822a21007559d5af3c11f87c33d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150882372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e94c7256011ed43382fe7c070ec6a3c6c9dea623f2e321fe06a03ded8e882e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Oct 2025 18:23:03 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENV GOSU_VERSION=1.19
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENV LANG=en_US.utf8
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PG_MAJOR=15
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PG_VERSION=15.14-1.pgdg12+1
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 15 Oct 2025 18:23:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 15 Oct 2025 18:23:03 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Oct 2025 18:23:03 GMT
STOPSIGNAL SIGINT
# Wed, 15 Oct 2025 18:23:03 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 15 Oct 2025 18:23:03 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695877f834fb03f7d95d77591dadb36356ae627ac28acb9542de45c43e461588`  
		Last Modified: Wed, 22 Oct 2025 17:40:15 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e92404c1088d43cda975ccf025706ca5bc4ab3a409d6699e3afe5f78cd9228`  
		Last Modified: Wed, 22 Oct 2025 17:40:15 GMT  
		Size: 4.5 MB (4519773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2af509a4c6b0bf21e43baaaa4c06067ca59eb923c5eeaf68aa79dfaa912c03b`  
		Last Modified: Wed, 22 Oct 2025 17:40:15 GMT  
		Size: 1.2 MB (1203235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c3d6c088ceecc2cc1c2271d424d20ecf63e5874c59330afcc41f7b98448fb2`  
		Last Modified: Wed, 22 Oct 2025 17:40:16 GMT  
		Size: 8.1 MB (8066518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2961caabde6eef487dd53f2771434d22a9596a8685f6209848ce68748a431e`  
		Last Modified: Wed, 22 Oct 2025 17:40:15 GMT  
		Size: 1.1 MB (1108949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2fb1523fbf172692f2fa2c305aafcd5806d518fbc9281f2f7c07bf6373277f`  
		Last Modified: Wed, 22 Oct 2025 17:40:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f162d3ac8c785e6cbaf83257109ee89e40d06842616272ecf68e2134f8bbfb59`  
		Last Modified: Wed, 22 Oct 2025 17:40:15 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91c192dd67aea864a0de0de0980851d5fcd933bf6e6b549f82cab311627fc85`  
		Last Modified: Wed, 22 Oct 2025 17:41:07 GMT  
		Size: 107.9 MB (107860941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0594737db3113e829505f5469b58e0230395f7983f2c39b63d8b50a09f055181`  
		Last Modified: Wed, 22 Oct 2025 17:40:55 GMT  
		Size: 9.8 KB (9778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d4c7815fd12f2713621d8b624816b854f0e7d8cc948cdf7096902e172caa8d`  
		Last Modified: Wed, 22 Oct 2025 17:40:55 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fffe660deb38f2e84e3c563baed11c236a8cda97f9633644a7654c2fd74c8ff`  
		Last Modified: Wed, 22 Oct 2025 17:40:55 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c38e4a9cf917c19fd543bf582bad2852cd42edd34a025dc8f28c8f9b8d4f6a`  
		Last Modified: Wed, 22 Oct 2025 17:40:55 GMT  
		Size: 6.1 KB (6079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfc0cb99fcea96e598ab590435335ae12b4a579d233db6154b0ba3e2b309011`  
		Last Modified: Wed, 22 Oct 2025 17:40:55 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:0192c2607040747a795ea204f98fa9b875c001c855680678c5da4ffb7d8fc0a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5903233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf64adef4e76e52e012baca355cc960cff6ec91601a7ece6287eea8f77c946a`

```dockerfile
```

-	Layers:
	-	`sha256:18e601740745ddf5f8e5714599727660ae01c606227f21999f250a84d1fa699d`  
		Last Modified: Wed, 22 Oct 2025 20:13:57 GMT  
		Size: 5.8 MB (5849649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c02ba7cf067e98a8037245dde6a914c281afd8cac38b543124ebf53e6a1055c`  
		Last Modified: Wed, 22 Oct 2025 20:13:58 GMT  
		Size: 53.6 KB (53584 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:b789ea69a0578a335aeee60c12c3d30674cc096c73d0aeb81641879b5b36b1ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161592224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:587a44411486bae551a9d02ab5d2df1c94c16fe6965bf2f6e1728870aff3e535`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Oct 2025 18:23:03 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1760918400'
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENV GOSU_VERSION=1.19
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENV LANG=en_US.utf8
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PG_MAJOR=15
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PG_VERSION=15.14-1.pgdg12+1
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 15 Oct 2025 18:23:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 15 Oct 2025 18:23:03 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Oct 2025 18:23:03 GMT
STOPSIGNAL SIGINT
# Wed, 15 Oct 2025 18:23:03 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 15 Oct 2025 18:23:03 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9af2454a4583e64377534c708d303465636c37f3e4623cd4ad3bce1a1fedbfca`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 29.2 MB (29209678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24076bc7ebba634a9a75ded07cf060a20d358a50780c25fb6e5aa863216c7d68`  
		Last Modified: Wed, 22 Oct 2025 17:54:53 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1116a7afbff7ad085a2c150ee347fa8a6a072a574d3fdefc5d5fce07a36565`  
		Last Modified: Wed, 22 Oct 2025 17:54:54 GMT  
		Size: 5.0 MB (4965349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497b6f1c87ce6129e002455dc51c0eec4b09ad7f8058e6d012a25f1a1a211791`  
		Last Modified: Wed, 22 Oct 2025 17:54:54 GMT  
		Size: 1.2 MB (1218611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637ee6f44d5c6bb3d07894fff9face7fe1b1e0813f3a0036f07605c2c413f021`  
		Last Modified: Wed, 22 Oct 2025 17:54:54 GMT  
		Size: 8.1 MB (8066489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffda615409c369aa851f1979ac628dc5cec97ec89abf8b8f9b3d54a18bd06944`  
		Last Modified: Wed, 22 Oct 2025 17:54:54 GMT  
		Size: 1.1 MB (1137439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ba1977fdfb38b639493e3c72894dc36974daa57143fc7c8253d3fa80d93a3f`  
		Last Modified: Wed, 22 Oct 2025 17:54:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59087add834beb7b285d65dcf0c7366e31461d4787e2f88ded51efeac2a5365`  
		Last Modified: Wed, 22 Oct 2025 17:54:53 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05f114ce6bf891b6e2f85205c0366b74615a1a71d3ea4e57587866fbef48048`  
		Last Modified: Wed, 22 Oct 2025 17:55:13 GMT  
		Size: 117.0 MB (116973891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a616934781238a63f0c0720cc7243398d4de09c0aef7ba89730e51cf7f9b92bd`  
		Last Modified: Wed, 22 Oct 2025 17:54:53 GMT  
		Size: 9.8 KB (9782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d28cfe4173ff4bfcaa2606d52376100e8b8b0cbe76074a3209b025ab650f28f`  
		Last Modified: Wed, 22 Oct 2025 17:54:53 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72c471b7b9c97b5068235d657f4a61badd79bf0b177ddc3d7e078c3f328d260`  
		Last Modified: Wed, 22 Oct 2025 17:54:52 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ecf875c508d34883e9f79436edcec139c9e8fde49e959b9b0cf8b0293fe7e3`  
		Last Modified: Wed, 22 Oct 2025 17:54:52 GMT  
		Size: 6.1 KB (6080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9aafd94fd8e5ee94f1a6384ca6250f7c12b074a07e005556dbee1b8f636a65`  
		Last Modified: Wed, 22 Oct 2025 17:54:53 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:46512e8cb6f7251a3dc009307640b14a3f0c5ec9229b7e83a0858d3c8ebb7eec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ca81c8b92e864030ec5cb95830c12390ab128316e3939677d48286fe8e5f4c`

```dockerfile
```

-	Layers:
	-	`sha256:ddb3dc4e6f6f365b670d3b585ec03318d944810fb36f815b9e9c280f62ef22d1`  
		Last Modified: Wed, 22 Oct 2025 20:14:03 GMT  
		Size: 5.9 MB (5855582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e9f3b40f0cc3cadfcb45be12e92128fc5ed4cedc2fe2ab03f4b73d60ebd9914`  
		Last Modified: Wed, 22 Oct 2025 20:14:04 GMT  
		Size: 53.3 KB (53295 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:ae3e92c22dfda011a88e4acdd7e3c15c6dd40c680ffc1b54afd5620e5ef5508d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.7 MB (151697031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:052bd38375317f84d0e58c340b0c433b468e744127527ce34890bb3b2afedb4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Oct 2025 18:23:03 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1760918400'
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENV GOSU_VERSION=1.19
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENV LANG=en_US.utf8
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PG_MAJOR=15
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PG_VERSION=15.14-1.pgdg12+1
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 15 Oct 2025 18:23:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 15 Oct 2025 18:23:03 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Oct 2025 18:23:03 GMT
STOPSIGNAL SIGINT
# Wed, 15 Oct 2025 18:23:03 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 15 Oct 2025 18:23:03 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:67737a113ff8fe4461be953b475f1930d91e20d222e9a1f4e55ddb9bf4c2c6de`  
		Last Modified: Tue, 21 Oct 2025 00:19:57 GMT  
		Size: 28.5 MB (28513717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638082f5bdd46e1dc03e02cf23d1dbf9eb0243cee2673878adaeea6ff101c669`  
		Last Modified: Tue, 21 Oct 2025 11:14:17 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a832a624b6912c079cd14c8dbc78f05f84f8c63fb6ff50c1481959a4041ccb`  
		Last Modified: Tue, 21 Oct 2025 11:14:17 GMT  
		Size: 4.5 MB (4475441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2058c367c9a389dc08789fd036afda0c19262f918f661b1b2fcc967583e5e63b`  
		Last Modified: Tue, 21 Oct 2025 11:14:17 GMT  
		Size: 1.2 MB (1159187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a64915f74595c0753d83fc085d15fb295947b596778b96ef167c37e2d9d346`  
		Last Modified: Tue, 21 Oct 2025 11:14:18 GMT  
		Size: 8.1 MB (8066688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ec43a9850817d3646e4c7cb31bb4c68028986d39f10feacbec0eafd7b778d6`  
		Last Modified: Tue, 21 Oct 2025 11:14:17 GMT  
		Size: 1.2 MB (1182884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd529c052140a9fa8c938256943d9a9b6dbb304d55c9ea9ee326fc6f9e3b3c06`  
		Last Modified: Tue, 21 Oct 2025 11:14:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc87168a9ddb8a1d3a0edef3403aee3ed1af5b953f23f3ced72f712c0cd5393`  
		Last Modified: Tue, 21 Oct 2025 11:14:17 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3773fa7434c49d77e6db1680532d312e1c4bda1f24a2757b09e7c41cd9fc99cd`  
		Last Modified: Wed, 22 Oct 2025 22:22:25 GMT  
		Size: 108.3 MB (108278339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903cb39527316e812b1b535138399b014a12e1ecf12ed235e5f4d43be2ef050c`  
		Last Modified: Wed, 22 Oct 2025 22:22:16 GMT  
		Size: 9.8 KB (9786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a99240f56bbbf644a012ff08997b4b267cd727cf60d05e5e3217d1503590de`  
		Last Modified: Wed, 22 Oct 2025 22:22:17 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f443b779654b2bbfade0b6d1aaf2ebaec42adb55c7013aca19ba11308644c9e4`  
		Last Modified: Wed, 22 Oct 2025 22:22:17 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4cd96acaf970ffe11ac925a8eb477da55a62c1bda7784a0fe19fe446a0493d`  
		Last Modified: Wed, 22 Oct 2025 22:22:17 GMT  
		Size: 6.1 KB (6081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4281edc0ce60604402352504be9f9c6bc73ba660cd4b3bbbb2ac46798aa37f`  
		Last Modified: Wed, 22 Oct 2025 22:22:17 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:086fe562e3a366ae65a4c43b9f831c25b8add1df759458e47ed5ebf3c1f03e5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 KB (53204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4962f037debc1578a090ac8c08bdd30d35020da95b2fc24dee0fca5687c186a`

```dockerfile
```

-	Layers:
	-	`sha256:b3f010a8965fd78c9e50a5d03bc9c57149be6183a11c7edb686d7792492bfdb1`  
		Last Modified: Thu, 23 Oct 2025 02:09:55 GMT  
		Size: 53.2 KB (53204 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:a845f93016c10e95d5a0d9324a5ad476c8a60177db3a0329abd298e2c9a96b9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.6 MB (165611838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d86a0c5c4c6140e05f60b91b3168e48a328a6624939e2830d3e6ddab3cf30573`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 05:31:31 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Nov 2025 05:31:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 05:31:55 GMT
ENV GOSU_VERSION=1.19
# Tue, 04 Nov 2025 05:31:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 05:32:04 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 04 Nov 2025 05:32:04 GMT
ENV LANG=en_US.utf8
# Tue, 04 Nov 2025 05:32:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 05:32:11 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Nov 2025 05:32:12 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 05:32:12 GMT
ENV PG_MAJOR=15
# Tue, 04 Nov 2025 05:32:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 04 Nov 2025 05:32:12 GMT
ENV PG_VERSION=15.14-1.pgdg12+1
# Tue, 04 Nov 2025 05:43:43 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 04 Nov 2025 05:43:44 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Nov 2025 05:43:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Nov 2025 05:43:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Nov 2025 05:43:45 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 04 Nov 2025 05:43:45 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Nov 2025 05:43:45 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 05:43:45 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Nov 2025 05:43:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 05:43:45 GMT
STOPSIGNAL SIGINT
# Tue, 04 Nov 2025 05:43:45 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Nov 2025 05:43:45 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2442ae4ed78d32124d4f8b92ec0b1caf0e12483bafbd1803659dc391d3600616`  
		Last Modified: Tue, 04 Nov 2025 00:13:59 GMT  
		Size: 32.1 MB (32068905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9103551c5ae3de0bf7412fc3c3b589558b7a201cbb70143c80bd2b0f61436dea`  
		Last Modified: Tue, 04 Nov 2025 05:33:51 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d8d801e7df0e946c6ef493f47fde8298f346b4857822e8cc845ec2dace394c`  
		Last Modified: Tue, 04 Nov 2025 05:33:52 GMT  
		Size: 5.4 MB (5368449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804b885fd04fae73183839df1808db9272d0431ae0f0928bd6b382d946151cde`  
		Last Modified: Tue, 04 Nov 2025 05:33:51 GMT  
		Size: 1.2 MB (1208164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b3fc93c49f7cc3807da4615adc099c2bb10e0cb4118ef25ee5f6b9a5e558ce`  
		Last Modified: Tue, 04 Nov 2025 05:33:52 GMT  
		Size: 8.1 MB (8066533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a273919551517ff19ec39b648f56896c0ad54a2bd41122a406872dd4765d5d2e`  
		Last Modified: Tue, 04 Nov 2025 05:33:51 GMT  
		Size: 1.3 MB (1283653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ecc47ad06fcbf1282127b790eac31a18c8f9f33a45e576e3a31d852677b9a7`  
		Last Modified: Tue, 04 Nov 2025 05:33:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0009da3bc6b84521bd539e23e6eb6607d2c54baf338648051dba9320134fc83d`  
		Last Modified: Tue, 04 Nov 2025 05:33:51 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d848277bce12c3b4e7d482cfc131f41eb4cbfaaf780b1c055e65e24de7d754bf`  
		Last Modified: Tue, 04 Nov 2025 05:45:04 GMT  
		Size: 117.6 MB (117595376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d34a1134b870d871d99f0dc920fc62cd060796b9cd8588c7003baed664e067`  
		Last Modified: Tue, 04 Nov 2025 05:44:40 GMT  
		Size: 9.8 KB (9774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d1a11e778c9ead405734d64e5ff6a90d5a9a7091e2bedff6939dafe7f7ee98`  
		Last Modified: Tue, 04 Nov 2025 05:44:40 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96290f77a48ba64b65959516cbb2609e0e78bfbd4810d7731355f66eafab9784`  
		Last Modified: Tue, 04 Nov 2025 05:44:40 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7dcbc279e69af1420f49c6486bc1b4e0533cebcd5f2362737cdbb21aa5cee13`  
		Last Modified: Tue, 04 Nov 2025 05:44:40 GMT  
		Size: 6.1 KB (6076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d8a0bf553a67e80e383c7e3fe722c81ad164f9b99e1a20471100786b6f7095`  
		Last Modified: Tue, 04 Nov 2025 05:44:40 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:233a69e381a80a9517dddbc9ad3eebbe99e30313597c22339b8328f706f736d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5904049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ebde014ede802eb063c86cd104be89a4dca5d82428fae15b688a37bf654457`

```dockerfile
```

-	Layers:
	-	`sha256:99d414dc4ae49ec69c3f51da355ed509094a7f45b3719eedf01586be90a7913f`  
		Last Modified: Tue, 04 Nov 2025 10:23:15 GMT  
		Size: 5.9 MB (5850699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc98406165cb71327dca93c678469a285aba59fa380a0f8e54ed3c8afbdef40e`  
		Last Modified: Tue, 04 Nov 2025 10:23:15 GMT  
		Size: 53.4 KB (53350 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:fa9d79ad513443fe1d54157f2779aa8cf02fbdc103d7f2926c575521c20ebd18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.1 MB (162064664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0801939550f2ab3679d2a49f12e50d56de3a66b4426b6f79444ad104bd62568`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 01:51:20 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Nov 2025 01:51:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:51:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 04 Nov 2025 01:51:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 01:51:36 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 04 Nov 2025 01:51:36 GMT
ENV LANG=en_US.utf8
# Tue, 04 Nov 2025 01:51:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:51:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Nov 2025 01:51:40 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:51:40 GMT
ENV PG_MAJOR=15
# Tue, 04 Nov 2025 01:51:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 04 Nov 2025 01:51:40 GMT
ENV PG_VERSION=15.14-1.pgdg12+1
# Tue, 04 Nov 2025 02:39:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 04 Nov 2025 02:39:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Nov 2025 02:39:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Nov 2025 02:39:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Nov 2025 02:39:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 04 Nov 2025 02:39:13 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Nov 2025 02:39:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 02:39:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Nov 2025 02:39:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 02:39:13 GMT
STOPSIGNAL SIGINT
# Tue, 04 Nov 2025 02:39:13 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Nov 2025 02:39:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be232883d651408831817911bfa9e7aa97a9c1c16f0d9f51c1e4ba7b41472bac`  
		Last Modified: Tue, 04 Nov 2025 02:04:32 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23b66b64a9cdc4ee49f93ae5b45cc117b88ef644c87e9f7b7233ad03f1df1e6`  
		Last Modified: Tue, 04 Nov 2025 02:04:32 GMT  
		Size: 4.4 MB (4391266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7150046113cc44e28b1ef06ab4fbcccba24aaa77b823e94e7ddc78b90768e77`  
		Last Modified: Tue, 04 Nov 2025 02:04:32 GMT  
		Size: 1.2 MB (1222763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803591ef6beb1305b4de9cb08ea0a5a7155ba4c21ab320b03dd2534e3cc8350c`  
		Last Modified: Tue, 04 Nov 2025 02:04:33 GMT  
		Size: 8.1 MB (8120685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feaa31f35ea72d07928eb7499fc5efc4246391480d5cb584d9d0697eed9f4177`  
		Last Modified: Tue, 04 Nov 2025 02:04:32 GMT  
		Size: 1.1 MB (1097009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d55137c99bd935b934b11785cb06835fd3dab3bbeab391582d16418c871865a`  
		Last Modified: Tue, 04 Nov 2025 02:04:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a18c5bf9206e23832e577d19e87876f15f4e9d70196bbc3e360ccc62fdb32e`  
		Last Modified: Tue, 04 Nov 2025 02:04:33 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7802496d82b73c2b3795a50e2ec4fa3c4543f566cbaad4ddbd9e7ea09502f4`  
		Last Modified: Tue, 04 Nov 2025 02:40:27 GMT  
		Size: 120.3 MB (120327627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190b66c7959aa2825c2d1bb4811564555678dd5f1002aa96cfcec6089bebeb2d`  
		Last Modified: Tue, 04 Nov 2025 02:40:13 GMT  
		Size: 9.8 KB (9783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34f86996ba5cd184f630b475d2689e29e68ec51b414793b0f61c84f2d3822b9`  
		Last Modified: Tue, 04 Nov 2025 02:40:13 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03119650d3ecedbc63ca13904df349ae06bb903f3e1fc69f4164fa59127afb49`  
		Last Modified: Tue, 04 Nov 2025 02:40:13 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8a0e68a526b7871e7b3ad0c8fcca067eaaffeb84509438d2dcb915617f406c`  
		Last Modified: Tue, 04 Nov 2025 02:40:13 GMT  
		Size: 6.1 KB (6077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6298249aba3e33e82e5d78c667e73245c8a758aa7f85ec3a16cf16c6b54745f7`  
		Last Modified: Tue, 04 Nov 2025 02:40:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:d9bc58c56e88070ee5610ba82cecb5bffe09d7bceaaabae8c33e65d50eb9c53e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf98dc10115ab640295803ab9d1e26e9a5fb0b38b92a9aa199d7d0188aef673`

```dockerfile
```

-	Layers:
	-	`sha256:5567240e261ccf54cffb35403194c9fc7e002307f21a43294fcc5f664c0011f3`  
		Last Modified: Tue, 04 Nov 2025 10:23:16 GMT  
		Size: 5.9 MB (5852058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8512618a5ecc0aaa3f16b26670c289fbc8334e0ad1028d18965aa91075333ed8`  
		Last Modified: Tue, 04 Nov 2025 10:23:15 GMT  
		Size: 53.3 KB (53295 bytes)  
		MIME: application/vnd.in-toto+json
