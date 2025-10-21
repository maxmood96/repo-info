## `postgres:17-bookworm`

```console
$ docker pull postgres@sha256:9fd154da53417da7e1fe71d95a4a9073dc9e9b88ffe0bfc1dbd056d1ab3d0a9f
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

### `postgres:17-bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:c062998bef1b483101bdc1826cd2d8746f0c6a0614d9ce7a41816f33c2eae553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (156014731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8d02d21cb2e8be5e9a6bbf09669f89768758618bde2da4f349777f9f71a2a9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 25 Sep 2025 18:02:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV GOSU_VERSION=1.19
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV LANG=en_US.utf8
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PG_MAJOR=17
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PG_VERSION=17.6-2.pgdg12+1
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 25 Sep 2025 18:02:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 25 Sep 2025 18:02:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Sep 2025 18:02:43 GMT
STOPSIGNAL SIGINT
# Thu, 25 Sep 2025 18:02:43 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 25 Sep 2025 18:02:43 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38248541ec29b12e8ff8bcb87f0443d83c89eadaf0f7823911c7e894b922b052`  
		Last Modified: Tue, 21 Oct 2025 01:39:44 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecddd27211c77196d473d8f0b8f7746f1c3c4b1a78e419cf6ac9262ff4bde0a3`  
		Last Modified: Tue, 21 Oct 2025 01:39:44 GMT  
		Size: 4.5 MB (4534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a96d164f9fe57a086f52bd1126512089ab0a465ddb1c103e21c4bc532da5d2b`  
		Last Modified: Tue, 21 Oct 2025 01:39:44 GMT  
		Size: 1.2 MB (1249492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59c03759fd65342054e347ccbea8bf7d09449791b91ede76810556fd1656ca4`  
		Last Modified: Tue, 21 Oct 2025 01:39:46 GMT  
		Size: 8.1 MB (8066494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28bcf1497eb46717dd2a5e4b0b525126a152c033a8ec843bd351cceaabe3387`  
		Last Modified: Tue, 21 Oct 2025 01:39:45 GMT  
		Size: 1.2 MB (1196354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f382d04fe42ea75e04186e4c8c0ed77dd05bdd2ac7172228124cb3fe3b7d431`  
		Last Modified: Tue, 21 Oct 2025 01:39:43 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502bc3fca981b0d83d868b089a2b530e8fbc10f2514dc9a810375a7a27d51f87`  
		Last Modified: Tue, 21 Oct 2025 01:39:45 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1bba192256f6a9c8c3ea4f8a16a4824fa49435a8dabeace780b51827caadf4`  
		Last Modified: Tue, 21 Oct 2025 01:39:56 GMT  
		Size: 112.7 MB (112718940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f86d94209dc5715b76fb410c10bc6397acfdf8287190a668f4bd2e77eae1f1`  
		Last Modified: Tue, 21 Oct 2025 01:39:46 GMT  
		Size: 10.2 KB (10238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e556df0ef0911c53de5f17ea912c7b97da1a439cfc05b0e6d482ffc4032c9667`  
		Last Modified: Tue, 21 Oct 2025 01:39:46 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34712e63b2aa91d1780a6fc618c80ec4f80878336d32554a8244a73a3986bf6a`  
		Last Modified: Tue, 21 Oct 2025 01:39:46 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db184d4c280ea345008c830fb8bbdf4b170d32cd328cd135e2d6256b03e0b91d`  
		Last Modified: Tue, 21 Oct 2025 01:39:46 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f68be46801e35682d873ae176a275100b5f60aa7c93522aab6f916904db332`  
		Last Modified: Tue, 21 Oct 2025 01:39:46 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:9fcfb5d57a802327926547fca07dcefdf59317c94121122229b8ea599ffed7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5980789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c1e356c2323cc5ceb0f47cc7619d4f5ea94f4a91c3d5442d48eaa45ebb5c11`

```dockerfile
```

-	Layers:
	-	`sha256:d4d14319572973c3c432dd6a92197b74673ff1f7c79e5ec0efa4074815a4e5f5`  
		Last Modified: Tue, 21 Oct 2025 11:11:51 GMT  
		Size: 5.9 MB (5927456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84fc44bf8acded58957f23b75190cc7a9e4052ede91fbf06e36954512b44bcee`  
		Last Modified: Tue, 21 Oct 2025 11:11:52 GMT  
		Size: 53.3 KB (53333 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:262020b95696cd505a6d82b370dd1ee0f43e44dea86f13dd653a3ac68fabd397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (149040498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a953d73381facd892cb3a1659ffab840e6db2f1a4a66387bfc00fccc66c9d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 25 Sep 2025 18:02:43 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1760918400'
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV GOSU_VERSION=1.19
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV LANG=en_US.utf8
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PG_MAJOR=17
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PG_VERSION=17.6-2.pgdg12+1
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 25 Sep 2025 18:02:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 25 Sep 2025 18:02:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Sep 2025 18:02:43 GMT
STOPSIGNAL SIGINT
# Thu, 25 Sep 2025 18:02:43 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 25 Sep 2025 18:02:43 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f982c9691d15a93fba0c1226ca85169d870439f0b6119d1ec61ec73d2a7dc8c3`  
		Last Modified: Tue, 21 Oct 2025 00:19:59 GMT  
		Size: 25.8 MB (25757495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a20143c0b4e56b14cd6e0fa14722713c5f90b86b2ed8b4491ed6c311b5b5862`  
		Last Modified: Tue, 21 Oct 2025 02:15:49 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627d47a56f35023b685b2b99358ba7c8d4f3d2bac1d99bf3bb662dc29ef1967e`  
		Last Modified: Tue, 21 Oct 2025 02:15:49 GMT  
		Size: 4.2 MB (4151201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f308ed01bc015fdcdc87c904c2692276d29e163da0067aa5e4a1d8881b186daf`  
		Last Modified: Tue, 21 Oct 2025 02:15:49 GMT  
		Size: 1.2 MB (1220061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a61a7f0508fd3783c7f4c11cdeac24c27a58848e03249ae908768966c308fe9`  
		Last Modified: Tue, 21 Oct 2025 02:15:49 GMT  
		Size: 8.1 MB (8066613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b8bac614e9fe46d72c1783ae6fabcdbe0537e6ecfb99d89291029e6958c9ea`  
		Last Modified: Tue, 21 Oct 2025 02:15:49 GMT  
		Size: 1.2 MB (1195027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5addc97b9c4aebf3bad2f043a8e8f12bf838923092720288883100672c57f90`  
		Last Modified: Tue, 21 Oct 2025 02:15:49 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b823ba534eb55e3643d9e4093965429854a83b39abeb71c5a4b078f92840cc9`  
		Last Modified: Tue, 21 Oct 2025 02:15:49 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b105a82f950ff175059f0797929ce3987383b9a0848e4b8ffa00b99ce0f569`  
		Last Modified: Tue, 21 Oct 2025 02:15:54 GMT  
		Size: 108.6 MB (108629034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20839d1f44d52d075475db64f56fe52bd06b61a952f2b0b80fae444a5a2795c8`  
		Last Modified: Tue, 21 Oct 2025 02:15:49 GMT  
		Size: 10.2 KB (10238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ea2f06adbcadce02a9095e7b83cedc301b2a0b57e8bcb4cf47b033403e1930`  
		Last Modified: Tue, 21 Oct 2025 02:15:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bba8f6a77ad6716780203f5d860e26435f011f3448210587c0702d69dda78c1`  
		Last Modified: Tue, 21 Oct 2025 02:15:50 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188e78aa529c5a313263afb29c84e09c6bc89d9517fbaa48e2b9bf2e70378097`  
		Last Modified: Tue, 21 Oct 2025 02:15:51 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f019a09c26d08552669206c8c3138cefb78e0f8edc9f2e873a44af46a582a536`  
		Last Modified: Tue, 21 Oct 2025 02:15:50 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:904e8b94b45702912cf414f7affcd798701da948f47c75ad0863b8997e267383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5999311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e0944fb26823ba677889d4b2aa1b5f7ffa5331115c04e93aa4bbd7f1741e72`

```dockerfile
```

-	Layers:
	-	`sha256:e4f0af563243ac68348d6f89e54ce8011c36a7062f812f96ab0e0e441ceb25e8`  
		Last Modified: Tue, 21 Oct 2025 08:12:52 GMT  
		Size: 5.9 MB (5945771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c04cfd577963f85c8eca4fa05ab7d009a63dc12f191b89270f6fac748603a82c`  
		Last Modified: Tue, 21 Oct 2025 08:12:52 GMT  
		Size: 53.5 KB (53540 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:d589519aecdd1e76a27819862f14be63433f075ee31ed0d59b894a2af5719f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (144041928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2c130dfc7c0aa7db917080b8b98ee32cf9cd105fe17298d7a6995bc2d0b6cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 25 Sep 2025 18:02:43 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV GOSU_VERSION=1.19
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV LANG=en_US.utf8
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PG_MAJOR=17
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PG_VERSION=17.6-2.pgdg12+1
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 25 Sep 2025 18:02:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 25 Sep 2025 18:02:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Sep 2025 18:02:43 GMT
STOPSIGNAL SIGINT
# Thu, 25 Sep 2025 18:02:43 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 25 Sep 2025 18:02:43 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4f520125372ffa3e5f64f19eebfdfce1c8314446e9e3ab2629f5c13cacbd8345`  
		Last Modified: Tue, 21 Oct 2025 00:20:18 GMT  
		Size: 23.9 MB (23934023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2934f1d57eda898666d95bb6c35a88c82c2240960b81f84857c64680ebd782c`  
		Last Modified: Tue, 21 Oct 2025 02:30:44 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb7f0c2524d51e56345169f3033a594b2e02c3098599a756e60b400adaf0b1e`  
		Last Modified: Tue, 21 Oct 2025 02:30:44 GMT  
		Size: 3.7 MB (3742680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f085134908afe169f85f458d9a6485a2c1cf2508e29cc53d664a93e15b9a922`  
		Last Modified: Tue, 21 Oct 2025 02:30:44 GMT  
		Size: 1.2 MB (1215963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749d3e8b14e6f4b52b6f2e2785f562c1ffd169d7005b04c149bd945d0ec115f1`  
		Last Modified: Tue, 21 Oct 2025 02:30:44 GMT  
		Size: 8.1 MB (8066434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3348b679a21eba0314929b88cf16368cc6835cfcdce318a2d2e0e8332a90b674`  
		Last Modified: Tue, 21 Oct 2025 02:30:44 GMT  
		Size: 1.1 MB (1067209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfef4df1460bacea0780aff2a77e426c0a25a84c4d17ddad5db9b582c7156f8d`  
		Last Modified: Tue, 21 Oct 2025 02:30:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2770095cc68e97a5f290bc0f5f87b3e1ea9443d51c6b616436f9b8983a527f4b`  
		Last Modified: Tue, 21 Oct 2025 02:30:44 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfebcb7b2ea748a844e0afd8f551447a0c0f5b170ce3706a5538276544a7eaf`  
		Last Modified: Tue, 21 Oct 2025 02:30:52 GMT  
		Size: 106.0 MB (105994549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bc25ed4f39183f92d485937516b1874bc3bce2aba4e58979b61c3744047ab9`  
		Last Modified: Tue, 21 Oct 2025 02:30:44 GMT  
		Size: 10.2 KB (10239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158e03777f9ef5d351ee92831c909645962c5651676871ee5fe7537eb693e9ba`  
		Last Modified: Tue, 21 Oct 2025 02:30:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9bce464441696d1a03e5ffcc8691a88b92dcb08712f4801f50ed4ca9637ef6f`  
		Last Modified: Tue, 21 Oct 2025 02:30:45 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7f21fbf248ccbbe54a1dd4f2630c67e1a65d1f03b46995e374e27bb731b4d5`  
		Last Modified: Tue, 21 Oct 2025 02:30:45 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb082eb10e167f1a9b2875693a01153b898164a0202a4a4adc8c065818a824e2`  
		Last Modified: Tue, 21 Oct 2025 02:30:45 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:3d4ec00bab659a52467280ab284b76ca7e8a0c3189874b36cfb5310713524037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5998565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:434ebd164ef74a1a41775b9038a2738bad14355d5e4e4587a37e5335271bbe5f`

```dockerfile
```

-	Layers:
	-	`sha256:4be447a98890cdaad1d415466c2b3f5c076f9b20d20beb53833b01c7d87ff6fd`  
		Last Modified: Tue, 21 Oct 2025 08:12:58 GMT  
		Size: 5.9 MB (5945026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7a3806f1a53d7488e26129d7380d645dfef7b7e0d2879b1a6f30dc057666193`  
		Last Modified: Tue, 21 Oct 2025 08:12:59 GMT  
		Size: 53.5 KB (53539 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:b290eb3f714605bc559624fd1e84e830902fda38e4efa13229cc9bb67f641b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (154014261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a8fb2609e2954177d1cbdab275866d97df8aa4e31ff3aa1babb72817f13cdf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 25 Sep 2025 18:02:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV GOSU_VERSION=1.19
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV LANG=en_US.utf8
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PG_MAJOR=17
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PG_VERSION=17.6-2.pgdg12+1
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 25 Sep 2025 18:02:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 25 Sep 2025 18:02:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Sep 2025 18:02:43 GMT
STOPSIGNAL SIGINT
# Thu, 25 Sep 2025 18:02:43 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 25 Sep 2025 18:02:43 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a08c15c89a6b8f8ec0ad0246202bda518827730fd8fa7ad923e293c3db4a4e6`  
		Last Modified: Tue, 21 Oct 2025 01:43:40 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c92cd2f344a71ffb590700a43ca0a226cdde5c948efb0d8a06ef536df80fe9f`  
		Last Modified: Tue, 21 Oct 2025 01:43:40 GMT  
		Size: 4.5 MB (4519813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ca47c5d53484d880937dd226393cb3f37a5e2da3ed6fe4b72dddbd296672bb`  
		Last Modified: Tue, 21 Oct 2025 01:43:40 GMT  
		Size: 1.2 MB (1203264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d451a90b3a7e25986c47e1027f0ac645193631e8c5795f200fb259ec932c106e`  
		Last Modified: Tue, 21 Oct 2025 01:43:41 GMT  
		Size: 8.1 MB (8066520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcb7eaf7ef8d832c4a19a0640fad0bb1cb9060c9665f8b51c190bc2c9329eef`  
		Last Modified: Tue, 21 Oct 2025 01:43:40 GMT  
		Size: 1.1 MB (1108968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4393d4cf3ee5d98e43fa0a3a93a4d3b4c65b5669d5dfe37a718a951e84a9dad3`  
		Last Modified: Tue, 21 Oct 2025 01:43:40 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1244860fc24b266f4975ca919c4472650a43bb321b8e3139531b64892f0ab2dd`  
		Last Modified: Tue, 21 Oct 2025 01:43:40 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeacf1173fd8fd658ad66d395e7d98dfdfb852330d305c7f4fe4a3938e6257c3`  
		Last Modified: Tue, 21 Oct 2025 01:43:54 GMT  
		Size: 111.0 MB (110992447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beea8e874ba2cb02a6d6018f0abfd72e63cfd8455664190bc00d4671a9df5f6e`  
		Last Modified: Tue, 21 Oct 2025 01:43:40 GMT  
		Size: 10.2 KB (10231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eddd98a3ed345114b0f8ed13775f9e6dc21c1ea2d77e2fd29357f512af12ef06`  
		Last Modified: Tue, 21 Oct 2025 01:43:40 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525b10ba715a368d89ecb27ce5d3a79095e841e6b404cbe4b04352f4249999cc`  
		Last Modified: Tue, 21 Oct 2025 01:43:40 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73905a4b88eae2ef1fd2b325be50b143d7d67d8b5a9a68aea955cdce1ea132d9`  
		Last Modified: Tue, 21 Oct 2025 01:43:41 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2cdda88aca6399ed974a0f222c1fdde1e2db999a5eb9dc4302d16866c110dc`  
		Last Modified: Tue, 21 Oct 2025 01:43:41 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:7d8277dc29a03050ecc8ea683d5be7125b725da3c435b9764657043038b6c860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5987345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d31f9d4232846e991a65368a8da412fb98cd571155f422c8b33ec9a5cb0b27`

```dockerfile
```

-	Layers:
	-	`sha256:bb32ea4943be72e6b4ff3f8db18ee505e774ab3927a550b76790bd173d9d5ca3`  
		Last Modified: Tue, 21 Oct 2025 11:12:04 GMT  
		Size: 5.9 MB (5933767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cec7c3b7433f76b29e8ae9559429f4546510a3be649719746f8e35b54b83ec2c`  
		Last Modified: Tue, 21 Oct 2025 11:12:05 GMT  
		Size: 53.6 KB (53578 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:1171c137c3c6219799ea3ba084ba230f6e3e6291a2432561bb3bc656237a45cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.9 MB (164874475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7802120426ce7ee01bc7a6801eaa3bf94e1ee4460f6f6481f5138bc4cf39935`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 25 Sep 2025 18:02:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1760918400'
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV GOSU_VERSION=1.19
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV LANG=en_US.utf8
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PG_MAJOR=17
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PG_VERSION=17.6-2.pgdg12+1
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 25 Sep 2025 18:02:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 25 Sep 2025 18:02:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Sep 2025 18:02:43 GMT
STOPSIGNAL SIGINT
# Thu, 25 Sep 2025 18:02:43 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 25 Sep 2025 18:02:43 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9af2454a4583e64377534c708d303465636c37f3e4623cd4ad3bce1a1fedbfca`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 29.2 MB (29209678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c983b8d8487fdb7df349004a5d637e84f055bb51621e90a8ba90de5ec15254b`  
		Last Modified: Tue, 21 Oct 2025 01:50:24 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62134dfea3b16e13a23d75d25e3c222cdad4a51960afb39d1c84b0c50c232c67`  
		Last Modified: Tue, 21 Oct 2025 01:50:24 GMT  
		Size: 5.0 MB (4965352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf15298d479b3092110500e54f9bc5e15e14b18b20ba39276ef1be02a3b072ae`  
		Last Modified: Tue, 21 Oct 2025 01:50:24 GMT  
		Size: 1.2 MB (1218630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f225a33a3385c6e33fc1f4b4066143132b73f2e0a5bd7dfaa87ed78fea9851a`  
		Last Modified: Tue, 21 Oct 2025 01:50:25 GMT  
		Size: 8.1 MB (8066487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853a79b1b5ecbc7650ef77b1adcf2ad55891c60d4174e5691bb4c16f89d3040a`  
		Last Modified: Tue, 21 Oct 2025 01:50:24 GMT  
		Size: 1.1 MB (1137401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36201a563b7fbea32b0826d3b2b30e8411db0d479b924e8431b90159412308d0`  
		Last Modified: Tue, 21 Oct 2025 01:50:24 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25c99370e71b3349d6895e2915514019bac84d6d5403533f05b6db94464c866`  
		Last Modified: Tue, 21 Oct 2025 01:50:24 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7caeb2b225bd326e3ecbcd48aa098a97c5142d0e8b018ff49f309020fb680355`  
		Last Modified: Tue, 21 Oct 2025 01:50:35 GMT  
		Size: 120.3 MB (120255858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a760cd55a73cc6d35f324607d900e4b9d67a3b25e042999242d39de4389ea70f`  
		Last Modified: Tue, 21 Oct 2025 01:50:24 GMT  
		Size: 10.2 KB (10242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33286c0a12e488308df4b29a6d2a476d32de819430c05f2a7d0e77e7d05d199e`  
		Last Modified: Tue, 21 Oct 2025 01:50:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d9b194c3b143ac868df29c1a9da0bc4838d90f50933f7f7fa2694d70165605`  
		Last Modified: Tue, 21 Oct 2025 01:50:25 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43efa9cf05f6a032baa28c70054c330c3cb41eadda3d37db27ed497c2421fa0`  
		Last Modified: Tue, 21 Oct 2025 01:50:25 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6c0e6c8289ed5dd46a010ea6492aa2fd6cacf1b1cc4dcc271420a5a8bccf4b`  
		Last Modified: Tue, 21 Oct 2025 01:50:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:31cc9ddd7da8d18daa7c57885b45f3c751e431bf87b9241fa28f6fb304f7289f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5997203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c3581ac1de4e354d3c2adfe94b10b6fa66ca62781b7083e3b948f4f87ef44b`

```dockerfile
```

-	Layers:
	-	`sha256:597a518bd40a6a46268c0da6cb8189cb4734d0f39c5f266069fc27ab1b27e96c`  
		Last Modified: Tue, 21 Oct 2025 11:12:09 GMT  
		Size: 5.9 MB (5943914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:782e4b4b3643be0d7b9fda833d9996db7219ddc0a6c72bbd994acd1c314a860d`  
		Last Modified: Tue, 21 Oct 2025 11:12:10 GMT  
		Size: 53.3 KB (53289 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:8c388c6aa2ec0d8fd8ff5b364588d64c1af98fa242219442ab30fc2c5e109753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.9 MB (154881054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66221fc1f8b389ce9ef3519bd2edee7ad5c30c3f78ee88f036abe99fc3856b6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 25 Sep 2025 18:02:43 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1760918400'
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV GOSU_VERSION=1.19
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV LANG=en_US.utf8
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PG_MAJOR=17
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PG_VERSION=17.6-2.pgdg12+1
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 25 Sep 2025 18:02:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 25 Sep 2025 18:02:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Sep 2025 18:02:43 GMT
STOPSIGNAL SIGINT
# Thu, 25 Sep 2025 18:02:43 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 25 Sep 2025 18:02:43 GMT
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
	-	`sha256:6fc6e41415917b9535667ef1052d0ff74eb6b2c00ac558354ebf5d6447ed936e`  
		Last Modified: Tue, 21 Oct 2025 12:26:24 GMT  
		Size: 111.5 MB (111462058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b98fd2fb79255f4653caaf74835c3781c50a93cbf820c963a58699f9fcea15f`  
		Last Modified: Tue, 21 Oct 2025 12:26:15 GMT  
		Size: 10.2 KB (10244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b81324c216fb5b22002e174fa1553ec2981b519ea43e7c5632d51f1821c54a`  
		Last Modified: Tue, 21 Oct 2025 12:26:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e22906f9fb689234bbac5215aee618b2a30863d5fbb2eab746c740d924f8b192`  
		Last Modified: Tue, 21 Oct 2025 12:26:15 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e84255609707f4d10068b1cc14dd414d951c9349ec27fb556da214693a4020`  
		Last Modified: Tue, 21 Oct 2025 12:26:15 GMT  
		Size: 5.9 KB (5930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b31fea62426b14f92b954317db8dd639521609b828eaa30b926bf81e0dc3bf`  
		Last Modified: Tue, 21 Oct 2025 12:26:15 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:0942be01b3a117f7537ca957ecdace49dedb3eba095ffcd62f4d9d8cc5e31033
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 KB (53199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be929ff65f8c19a59a91ea26489317e7b00d2e2194b1d47edacd1f02d252ac80`

```dockerfile
```

-	Layers:
	-	`sha256:07dacf67f1a178f1eeafa473c10c86eafe1f485d4e5e9c238b45d55fa748621e`  
		Last Modified: Tue, 21 Oct 2025 14:09:30 GMT  
		Size: 53.2 KB (53199 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:86b1a85c390793d5081fba69ee0af02d2da34c251952bdf4711d7c6503dcfc87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.8 MB (168834523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d29a14c56d419639e700b3cc9223444c685672f02f2779873da9f442e67139`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 25 Sep 2025 18:02:43 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1760918400'
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV GOSU_VERSION=1.19
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV LANG=en_US.utf8
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PG_MAJOR=17
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PG_VERSION=17.6-2.pgdg12+1
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 25 Sep 2025 18:02:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 25 Sep 2025 18:02:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Sep 2025 18:02:43 GMT
STOPSIGNAL SIGINT
# Thu, 25 Sep 2025 18:02:43 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 25 Sep 2025 18:02:43 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5a28d569c39dc949a4743122d7b5ec2d2e0664f1276c801bf984a711d80f2a1d`  
		Last Modified: Tue, 21 Oct 2025 03:26:43 GMT  
		Size: 32.1 MB (32068780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b696225b8b1f2c384d658e9bfe9c57053a8668118d549d3b36da48b6963075`  
		Last Modified: Tue, 21 Oct 2025 06:43:27 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a355fa6dc1d1bb059af61333ce6498fc31ae06df0d851330b2f8b540dfeb63e2`  
		Last Modified: Tue, 21 Oct 2025 06:43:28 GMT  
		Size: 5.4 MB (5368479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bd5bba6ec7a0a6fb95ab8cfa7c66966882e07fbe48a05ef522f88873add047`  
		Last Modified: Tue, 21 Oct 2025 06:43:28 GMT  
		Size: 1.2 MB (1208156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae8ac2c42c9f6594b8d8e1e3d130443d58a4aa43fe466ee3d2cdf1ab9826e35`  
		Last Modified: Tue, 21 Oct 2025 06:43:29 GMT  
		Size: 8.1 MB (8066567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9efe0b9f191c41e1b3ed2ec19364d0ea27eb33b7293ee3977c6982e6b2ddf6`  
		Last Modified: Tue, 21 Oct 2025 06:43:28 GMT  
		Size: 1.3 MB (1283638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47fdfb2477182cd6e7d2f31bd55ac647bc86d5926f2af2104859007788ef824`  
		Last Modified: Tue, 21 Oct 2025 06:43:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6517610580277e06311705631cfff65685fe85d637c330e6c783231df1f27885`  
		Last Modified: Tue, 21 Oct 2025 06:43:28 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d8e5880eab1fcd2360c34e8cef30bf937a25c42eafc00c3ca4526a3d1ab00f`  
		Last Modified: Tue, 21 Oct 2025 06:45:38 GMT  
		Size: 120.8 MB (120817837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacb85909a2e868bc21e5cd7b9577eac5a3c6ccfc54751831a0b7b194eaeb4b2`  
		Last Modified: Tue, 21 Oct 2025 06:45:27 GMT  
		Size: 10.2 KB (10234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea40011833b17d638581b6d3e819288e650140d23791b038fcbbef07f336731`  
		Last Modified: Tue, 21 Oct 2025 06:45:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85cbe5f8bee92be938612f0d6a56fc12ccfa98b05f3df1b211d858559bb2791b`  
		Last Modified: Tue, 21 Oct 2025 06:45:27 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c079731e02d2ec2a261ae0b98fc97cd4e89a2b71a12342e10ac3046ebbded4`  
		Last Modified: Tue, 21 Oct 2025 06:45:27 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a653a16175463184a77d3a72f65d0b4c9c66e48f5f81c42a06fc0acf58875eae`  
		Last Modified: Tue, 21 Oct 2025 06:45:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:1259908fff3722d43cdbf51a57cafd3a87fd755f13edde366ce2c94193a70c24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5988204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62864c5a0dabfc031f20bb0147979ec54d741720259d560a0e76d8be5d258bc8`

```dockerfile
```

-	Layers:
	-	`sha256:b562e4b8feb4d4789de2732fda1225ea4dd9d51bb2600870600f23df7a7be0be`  
		Last Modified: Tue, 21 Oct 2025 08:13:19 GMT  
		Size: 5.9 MB (5934817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33dc936a156afa238904464d554cb02465c5c65269ad007c3d17e79088a7cf35`  
		Last Modified: Tue, 21 Oct 2025 08:13:19 GMT  
		Size: 53.4 KB (53387 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:4b4cadb6499b266858a5e6c3fbb7a09c0037ebb1bf5d9519fdff3fef88be3b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.3 MB (165271438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b630f3e05baca6cd8181a899ddb92432598de8a2819e4944497e9e647f8f2752`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 25 Sep 2025 18:02:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1760918400'
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV GOSU_VERSION=1.19
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV LANG=en_US.utf8
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PG_MAJOR=17
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PG_VERSION=17.6-2.pgdg12+1
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 25 Sep 2025 18:02:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 25 Sep 2025 18:02:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Sep 2025 18:02:43 GMT
STOPSIGNAL SIGINT
# Thu, 25 Sep 2025 18:02:43 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 25 Sep 2025 18:02:43 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:43b0f588b497b17691a3547afa4ae41853829cffde6930e6425ddae4a3f89278`  
		Last Modified: Tue, 21 Oct 2025 00:21:28 GMT  
		Size: 26.9 MB (26884356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbbc89cdc3fa353d60c43720bdf82075de4d3d7f0c44e66ac1b936214316d444`  
		Last Modified: Tue, 21 Oct 2025 07:23:34 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d7249199a8c59bf88d79fa9c61d376c678a3c1a60e23e170e566a5cc9ab8c7`  
		Last Modified: Tue, 21 Oct 2025 07:23:35 GMT  
		Size: 4.4 MB (4391275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c02569f5117362eed5934e5a8537c9759666479f38aee5570fc7bd6338204d`  
		Last Modified: Tue, 21 Oct 2025 07:23:34 GMT  
		Size: 1.2 MB (1222762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7e09a52b74d07c6d7262b55ff861bdf77a70790b5631805536145cd535dc37`  
		Last Modified: Tue, 21 Oct 2025 07:23:35 GMT  
		Size: 8.1 MB (8120688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aafd5b4f001f9f0cc10818e81029d9ec019069ba0717d9e6308c03f42a55c021`  
		Last Modified: Tue, 21 Oct 2025 07:23:34 GMT  
		Size: 1.1 MB (1097053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439e0ba2429cb6a6a63bd4f85444525c2a3b76154a9bf2f4cd09d0d487da83ce`  
		Last Modified: Tue, 21 Oct 2025 07:23:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23e7113b9d219e589f496eab5023a0c2a5e25205b21fe9bd05307057561e514`  
		Last Modified: Tue, 21 Oct 2025 07:23:34 GMT  
		Size: 3.1 KB (3138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba22f4d804ca6b17e4194ef8dbf07cd53e46795055565cb7ba08bfb4f9e762b9`  
		Last Modified: Tue, 21 Oct 2025 12:07:16 GMT  
		Size: 123.5 MB (123534237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301e35b5060951abce2c0b831657d2f7d129128f160145adba20473b994d93f2`  
		Last Modified: Tue, 21 Oct 2025 08:13:21 GMT  
		Size: 10.2 KB (10241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968c72459c5b3cbd597329dbf68ee691f2f8587b108bca2c7a627133f92422c1`  
		Last Modified: Tue, 21 Oct 2025 08:13:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b192ee7cef3312db487046351b80da95b4db8fe0450de3ca5c7540c049e68861`  
		Last Modified: Tue, 21 Oct 2025 08:13:21 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def4df712f81ca74cc3f451ebdcd8ccc121690b44d2963b02d050b3211b5b6f8`  
		Last Modified: Tue, 21 Oct 2025 08:13:22 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d56d225ef0a4bea39c939c1c299b395d232fc698a6763e935643ac9d265f59`  
		Last Modified: Tue, 21 Oct 2025 08:13:22 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:63e5370f9d00044897cc7cd55759ed55cc90f385deba24519ec5771f0fe91dcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5993723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbcd499c178492a646d34aed7192c483c500475c4632f823fed4f1975403c5ad`

```dockerfile
```

-	Layers:
	-	`sha256:70f4c8eeefac89610b2d620024f39ba3cdc8b191ecd968aef321729a98b4add2`  
		Last Modified: Tue, 21 Oct 2025 11:12:21 GMT  
		Size: 5.9 MB (5940390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6d6bf3d5dd890929a249533a978ba22592beedccff3b624208a78b100feadc4`  
		Last Modified: Tue, 21 Oct 2025 11:12:22 GMT  
		Size: 53.3 KB (53333 bytes)  
		MIME: application/vnd.in-toto+json
