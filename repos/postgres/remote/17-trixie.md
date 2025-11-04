## `postgres:17-trixie`

```console
$ docker pull postgres@sha256:1da445c15f55eb86a84b2aaaf552465c48eb5cdbaa316c368a2480b1c0b39051
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

### `postgres:17-trixie` - linux; amd64

```console
$ docker pull postgres@sha256:8259ff12af407097391726fc01ee4b6aefad91777849d51e491d95c46f8ccc63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161116131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:680650095fe6845bcbedf252687ac19de3d5973fd868e6c5c639c42856a40dfe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Oct 2025 18:23:03 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
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
ENV PG_MAJOR=17
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PG_VERSION=17.6-2.pgdg13+1
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2448e4057c349aafcb0d4655ec0a84d53acd1ef6a8545abe48c61f6e4e36e581`  
		Last Modified: Wed, 22 Oct 2025 17:42:15 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f401357b4b788b0e6fe0346a3ec054a2d2e0686f9e60d34bc7804e1a3abaeee`  
		Last Modified: Wed, 22 Oct 2025 17:42:16 GMT  
		Size: 6.4 MB (6436580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6dee24bc8dbe0e41a67b61a1fac17be078a603539f2182f96c0c6439356b825`  
		Last Modified: Wed, 22 Oct 2025 17:42:16 GMT  
		Size: 1.3 MB (1256572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cca9c68843bd625ce5f3db2975accc06f1776ff90ce674ba80ec94ee4605cf`  
		Last Modified: Wed, 22 Oct 2025 17:42:17 GMT  
		Size: 8.2 MB (8203682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef69903c3d378adc8e9a95b7776125669ce75dc7c54e828b4e2ca25575eefc26`  
		Last Modified: Wed, 22 Oct 2025 17:42:16 GMT  
		Size: 1.3 MB (1311455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d3b3abadea62e1f1cffa6d157dfe196a5bdf92dc6ab23dfff929d377174165`  
		Last Modified: Wed, 22 Oct 2025 17:42:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabe707e1eeaf44d354f09d739d9fbc78a0761a6fce30d5b7a1351f697d26930`  
		Last Modified: Wed, 22 Oct 2025 17:42:16 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197734e8d983b0d262c8d2d2bb2af35b3f89c7a881493f90ebf02eabd35ab6c0`  
		Last Modified: Wed, 22 Oct 2025 17:42:28 GMT  
		Size: 114.1 MB (114108592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903f11cf87bbb1b9d24f811d049fa9701272cb7b548eb7360830b2707bd16553`  
		Last Modified: Wed, 22 Oct 2025 17:42:16 GMT  
		Size: 10.3 KB (10342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f9274b533cad116dc03133dfabdb0b3a8fbff66f1274918048ae4189653a02`  
		Last Modified: Wed, 22 Oct 2025 17:42:16 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de651ade5c4520c1900d33e2770ca7fabe9b46ee634bdec213373f38534920b`  
		Last Modified: Wed, 22 Oct 2025 17:42:16 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0febede0a299d275b50eb8e2d0f5d19efddd6f17ab2de55a67476d0ab362dd1`  
		Last Modified: Wed, 22 Oct 2025 17:42:16 GMT  
		Size: 6.1 KB (6078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f048522a36ca462e762fc9633b12326ce0521ce8be1e6ce7446009bc06d6da8a`  
		Last Modified: Wed, 22 Oct 2025 17:42:16 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:3c17f82e4b215685fac52773c56fc58b7a9ed29f8d43bb2a975b6f1c1be403f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5780263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85de5aa943453f11c07975af59246633c9c9d050c61f6b43ba594f3f1f8a6bc1`

```dockerfile
```

-	Layers:
	-	`sha256:ec8f4fab80a573a54e193166f294a6cc3cc85739212c738a5b4b88015fecc512`  
		Last Modified: Wed, 22 Oct 2025 20:16:38 GMT  
		Size: 5.7 MB (5726360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e128dab550509682e6df2bf96cdb2e6895c2bcc9a2c5db4021f86009aea73691`  
		Last Modified: Wed, 22 Oct 2025 20:16:39 GMT  
		Size: 53.9 KB (53903 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-trixie` - linux; arm variant v5

```console
$ docker pull postgres@sha256:c3eb92f94b482b36ecc9112fe1f2163273a7d4696a65ed079ee7cfbce016c204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155144905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bbb308677e773daaef1a4e5d8f87df39f63ff925d2dff2dbebbc87692adba73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:00:47 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Nov 2025 01:00:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:01:07 GMT
ENV GOSU_VERSION=1.19
# Tue, 04 Nov 2025 01:01:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 01:01:16 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 04 Nov 2025 01:01:16 GMT
ENV LANG=en_US.utf8
# Tue, 04 Nov 2025 01:01:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:01:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Nov 2025 01:01:23 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:01:23 GMT
ENV PG_MAJOR=17
# Tue, 04 Nov 2025 01:01:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 04 Nov 2025 01:01:23 GMT
ENV PG_VERSION=17.6-2.pgdg13+1
# Tue, 04 Nov 2025 01:18:29 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 04 Nov 2025 01:18:29 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Nov 2025 01:18:29 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Nov 2025 01:18:29 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Nov 2025 01:18:29 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 04 Nov 2025 01:18:29 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Nov 2025 01:18:29 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:18:29 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Nov 2025 01:18:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:18:29 GMT
STOPSIGNAL SIGINT
# Tue, 04 Nov 2025 01:18:29 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Nov 2025 01:18:29 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:453afc2258d7bc5729fed5672fb95bafa092e30a933b4377a12034be940a671b`  
		Last Modified: Tue, 04 Nov 2025 00:13:12 GMT  
		Size: 27.9 MB (27946438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2cc3517ac80be3700895178e1ab7ec5797af83b522564e745ec7443adf8681`  
		Last Modified: Tue, 04 Nov 2025 01:18:59 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf43e61c9c1aab4986987e1aaf59041d658339e9570b26c7a10c5d4253e1561`  
		Last Modified: Tue, 04 Nov 2025 01:19:01 GMT  
		Size: 5.9 MB (5928923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2684c82f4435ca08e9f6a3a1331cccf42873cf96dec8380474624056ac58e68f`  
		Last Modified: Tue, 04 Nov 2025 01:18:59 GMT  
		Size: 1.2 MB (1227353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473f66d33033ff9d354f1332ea286928b20a360cfed948ab1394e5a47ab19e78`  
		Last Modified: Tue, 04 Nov 2025 01:19:00 GMT  
		Size: 8.2 MB (8204087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb0b4582c0f9a54bf4fbac9119ad2511f4c789ead1eb9b200f54f5ae8f40b8c`  
		Last Modified: Tue, 04 Nov 2025 01:18:59 GMT  
		Size: 1.3 MB (1317128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53b9e928e5b9526775f5c455b21e8f48f6df212bc7ed83ad1552ec536950f53`  
		Last Modified: Tue, 04 Nov 2025 01:18:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b5e3e3f0871d173d97c968c288857b3f26ec40cf1e4e19fe7f432a4a381410`  
		Last Modified: Tue, 04 Nov 2025 01:18:59 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4fd8aad49e6197a35288e9c7627ee4b7f0cb165b83706cc9d004592d1170277`  
		Last Modified: Tue, 04 Nov 2025 01:19:11 GMT  
		Size: 110.5 MB (110499670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6bfba0a6e7739fdd72fd1bc47570b5669e1560b7e27ad50b1a4c05b82afde5a`  
		Last Modified: Tue, 04 Nov 2025 01:18:59 GMT  
		Size: 10.3 KB (10329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96cc26d1e9a1af9d46e83afcb0ee595f596cf7ee4e8ac7cc0c69fc59ca83f91`  
		Last Modified: Tue, 04 Nov 2025 01:18:59 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b45f9f52be9d4dbb89c3a888f6707b1254b1060feac46dc152ed7a0e6219a9c`  
		Last Modified: Tue, 04 Nov 2025 01:18:59 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32624f2b33e7bb2b2d4413ab352c042543760871357502e191ca7f3a4b4b312d`  
		Last Modified: Tue, 04 Nov 2025 01:18:59 GMT  
		Size: 6.1 KB (6080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05bfa4b57072c1e32633f5429556e37cf39fa8f4a8108c860b0c5271de75f79b`  
		Last Modified: Tue, 04 Nov 2025 01:18:59 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:fc49d93cfebd978bb8cf3852bffd8eb045f0b7262ca71940670aa3c76b4fb40e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5795361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14f39af71125af8ba17e534395139195994d0cb496e0f2577c5474ccb1d3091`

```dockerfile
```

-	Layers:
	-	`sha256:5d011d04698d6453364b43454a859deb1ed4ea7bb06d5fdc111c855dd7325ae2`  
		Last Modified: Tue, 04 Nov 2025 09:11:00 GMT  
		Size: 5.7 MB (5741278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:269fb9514dfbf28e07f65e04913c9f844e420f83213099ee1fdc4a1b01da1825`  
		Last Modified: Tue, 04 Nov 2025 09:11:01 GMT  
		Size: 54.1 KB (54083 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-trixie` - linux; arm variant v7

```console
$ docker pull postgres@sha256:3462e8abb0c0375f8a4f68145eeedf919d37aeefef7eb7f3032c857116e1f913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.2 MB (150176403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c549db078017ac4b694d17de911556384f039e199096b3b91d5a822411ca4d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Oct 2025 18:23:03 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
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
ENV PG_MAJOR=17
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PG_VERSION=17.6-2.pgdg13+1
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15db1d552b25e8a8b42af2d8f8d9d71cadedbcaccc96a3a42587ab6a7fd9869`  
		Last Modified: Wed, 22 Oct 2025 17:52:38 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ebc40b4e85d705462bafec2767c9eeb962bd6dfb9034c9712455afb695b220f`  
		Last Modified: Wed, 22 Oct 2025 17:54:49 GMT  
		Size: 5.5 MB (5496745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff450a9809ef979dea3ab3226520d07452a5f15e5bf5a8d9e4e2c504d1ade6d1`  
		Last Modified: Wed, 22 Oct 2025 17:54:49 GMT  
		Size: 1.2 MB (1222218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a122ff1c663fe55b5a13a9318dcc0a081b784866b167f34b59a31555c5d2c03`  
		Last Modified: Wed, 22 Oct 2025 17:54:49 GMT  
		Size: 8.2 MB (8203884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26294284f60acd33979cfc7d225442ab47c6c2913d353b50cecc4cc2a646189d`  
		Last Modified: Wed, 22 Oct 2025 17:54:49 GMT  
		Size: 1.2 MB (1172433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f6b1eb8f7e34f75eeab77e5b139b15150bb07a1801e5f31c8645864c193b3c`  
		Last Modified: Wed, 22 Oct 2025 17:54:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82fb00e81d4dca08cad3158f3df1ced168a0afa005e242981824c276ea4018d7`  
		Last Modified: Wed, 22 Oct 2025 17:54:48 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988f1899a0d2fb915090387deea440c79d909551e4a2de300ca0148ed4e6471c`  
		Last Modified: Wed, 22 Oct 2025 17:54:57 GMT  
		Size: 107.8 MB (107846890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa482897d3c98da349d132a5b0e59f2f95f613c7d4975f3f6677ae2463ebc038`  
		Last Modified: Wed, 22 Oct 2025 17:54:48 GMT  
		Size: 10.4 KB (10354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c002dbd38fc3d3885b7de39db139fd4790a3ecb0636e2fd31138d911549e8804`  
		Last Modified: Wed, 22 Oct 2025 17:54:48 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c7661393c547b8bd3baf730517624c4c5a7972393b3866854564fc2062e38f`  
		Last Modified: Wed, 22 Oct 2025 17:54:48 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051237e9936db006a38a76ecbc3d551d8e731036455b687ab2d87aeff8b58981`  
		Last Modified: Wed, 22 Oct 2025 17:54:49 GMT  
		Size: 6.1 KB (6079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7d76dd7e5b8ab49461983912bdd7b949997a32db24142da70f0126b891f795`  
		Last Modified: Wed, 22 Oct 2025 17:54:49 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:8e720311551720a1a9e4b179173d75ec2f4b14a6430eddd0d89139dc6e381e9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5794709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b267906b2581b8543d7a9300bda4301a7ca54eeebd84cc26414de48196c80eb`

```dockerfile
```

-	Layers:
	-	`sha256:c4254cc313396bc7b0400d35bbeb46153e9e6d6a1d8d3f999f0d90bb8d39ad98`  
		Last Modified: Wed, 22 Oct 2025 20:16:51 GMT  
		Size: 5.7 MB (5740583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:938ccca4b19edc9a0224fb5af7addd594c4ca990fc622776159c172307a35c7f`  
		Last Modified: Wed, 22 Oct 2025 20:16:52 GMT  
		Size: 54.1 KB (54126 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-trixie` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:3c4c2af9c754f13bfc21a17b7277980951b0972503b6cc5b4afff347364b2622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159745905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72f060ede28c7859451d22580b796e41fa6207250a8b21971dcf4ed35a37320d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Oct 2025 18:23:03 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
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
ENV PG_MAJOR=17
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PG_VERSION=17.6-2.pgdg13+1
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73bdf82d978e810c33b48b0cdbe8dd39e3c1ff4bd2a4064aba321bf85fdaa1b`  
		Last Modified: Wed, 22 Oct 2025 17:40:16 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a53801ef2ab502b5b101d5e58f6bb542f90327830dfb001c781b9e2785904b2`  
		Last Modified: Wed, 22 Oct 2025 17:40:16 GMT  
		Size: 6.2 MB (6231835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8bdfc61c57edd955163aac957d69f41beafefa186a725c26bea6e75c75f871d`  
		Last Modified: Wed, 22 Oct 2025 17:40:16 GMT  
		Size: 1.2 MB (1209346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb705d98db09328e50dcf36814b4b765a43431364410006aa05149ae3d1ac22d`  
		Last Modified: Wed, 22 Oct 2025 17:40:16 GMT  
		Size: 8.2 MB (8203821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3350540738f4de4da0f54808ed4f0a72d94a1c9180563d91ec3411be3af25642`  
		Last Modified: Wed, 22 Oct 2025 17:40:15 GMT  
		Size: 1.2 MB (1220397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7b423b4d5e65d228538350873fcefeb11f37937fcfd04d6ee262b10c37fb93`  
		Last Modified: Wed, 22 Oct 2025 17:40:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271a5af27896fa930377c34a03a169875e42c7475942c273f39d5909f45b0c44`  
		Last Modified: Wed, 22 Oct 2025 17:40:15 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6fae2438ed375c91fdf10a1a1b74e58fb29ddd09ccc55e5ab4eb67b52d2166`  
		Last Modified: Wed, 22 Oct 2025 17:40:28 GMT  
		Size: 112.7 MB (112717067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09eec2805020c15dbdc42752b7bb491959cec4d738c5bd08a21ff8b728c63031`  
		Last Modified: Wed, 22 Oct 2025 17:40:15 GMT  
		Size: 10.3 KB (10330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205794db97ec717f94c2f1853fc82d5d6e07dcb4a5ca508334ef500e2ef6f3cc`  
		Last Modified: Wed, 22 Oct 2025 17:40:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1451592e3ff028ee0834fe57f93b79d6c975e87d55babac841fd8fa1181331f9`  
		Last Modified: Wed, 22 Oct 2025 17:40:15 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b2221d0fc975db9c06f946f240a6c91bc891c92db4ca87b8a4426d3ff26076`  
		Last Modified: Wed, 22 Oct 2025 17:40:15 GMT  
		Size: 6.1 KB (6075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075cc1dfa1feac2f1da7b65004f9db1ade325718791cdb22a20196a2d57016aa`  
		Last Modified: Wed, 22 Oct 2025 17:40:15 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:51315f9c632fa0e2e717c063e3eb48d77beb78ca73dc50aa9292f075ee968d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5786878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:010e392160fe1e5fff0c6a0366195f05146513b64f866193ad3b4553e7cad1a0`

```dockerfile
```

-	Layers:
	-	`sha256:d7190f17a7b3d624655d957efd078f37716f3c7b558a138dea78a205d636cb34`  
		Last Modified: Wed, 22 Oct 2025 20:16:57 GMT  
		Size: 5.7 MB (5732706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57cc815b3b16e51f66a018a1e016f8fb63b23a15623a26087cd70c17259a5e6f`  
		Last Modified: Wed, 22 Oct 2025 20:16:58 GMT  
		Size: 54.2 KB (54172 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-trixie` - linux; 386

```console
$ docker pull postgres@sha256:a00d9fd5c6b2abda56dd2b7e3ef27cf993261a45bcd9c043450c4a5c029f5000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170299739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f18f49efb82dc7c000e7d2d27cfe23cea88696fc5430800c64f3639a5c8ad98d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Oct 2025 18:23:03 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
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
ENV PG_MAJOR=17
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PG_VERSION=17.6-2.pgdg13+1
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0883c19957398f88b27b79cb5313c4204dfdd6101d21627dfb1b0d539fa286f3`  
		Last Modified: Wed, 22 Oct 2025 17:40:35 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc36bfcbf99d51c8dc6e952495d396a13182b83eaddff4db73a7d7cecb54c6ad`  
		Last Modified: Wed, 22 Oct 2025 17:51:38 GMT  
		Size: 6.6 MB (6629453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286dff577b343e2df0c88b154d7da286a9547f5dc770448eee770c4808d803c4`  
		Last Modified: Wed, 22 Oct 2025 17:51:38 GMT  
		Size: 1.2 MB (1225651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549e0a41afd34b690c926c903173c2368ad32b0ff24329e3b1b34f725264c9b2`  
		Last Modified: Wed, 22 Oct 2025 17:51:39 GMT  
		Size: 8.2 MB (8203868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79217f0076cb1a7fcfa71f7f272938335a5f9218cbc1d1af5c1fc85d4711fb9`  
		Last Modified: Wed, 22 Oct 2025 17:51:38 GMT  
		Size: 1.3 MB (1308103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09d68c457697db31e209574b62b00f3a871e85fd898e988cff49a9f3f8bbb9b`  
		Last Modified: Wed, 22 Oct 2025 17:51:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48f75240c8b1daa78107b49546d998c78c17c33c31ec872fb796f067f44fc66`  
		Last Modified: Wed, 22 Oct 2025 17:51:38 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9b9fbb35955de23f8676129d3efe99d78603910eb31375f9d6785e06326eb5`  
		Last Modified: Wed, 22 Oct 2025 17:51:49 GMT  
		Size: 121.6 MB (121616711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9397fdf7e20bf540d16f0f1b4f74367d7996f3df7114e2e6d3ce4829d85e9a6c`  
		Last Modified: Wed, 22 Oct 2025 17:51:38 GMT  
		Size: 10.3 KB (10335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93ab8a0a885cc07fd5f8282278dcf2ee89c0b8592bb2fde559a74359298ca39`  
		Last Modified: Wed, 22 Oct 2025 17:51:39 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420b0c5d85f47f0525dbdd471786836c1fab5362652645c7203738bd7f2041e6`  
		Last Modified: Wed, 22 Oct 2025 17:51:39 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb0fb30f59c8d6c97419c898820a4f59e738933a5449f7dd61876b4fbbe7ca1`  
		Last Modified: Wed, 22 Oct 2025 17:51:37 GMT  
		Size: 6.1 KB (6080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d29cad82040348f97d4cbb958f6126869b865b398e40a0f62043d41c5658a3`  
		Last Modified: Wed, 22 Oct 2025 17:51:37 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:809da1451c4d732195885690a12c5a359477bcd45d797dea204c93d632696cf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5794018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:117ae20ef2bf99db33b3126f8dddf2402a41ab93f22d5cf732a7c984123ecf99`

```dockerfile
```

-	Layers:
	-	`sha256:e303fd539ec630e050e63c0d21b2fd4f47eff33d3d8c4c013fed1ed4b3095243`  
		Last Modified: Wed, 22 Oct 2025 20:17:04 GMT  
		Size: 5.7 MB (5740171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48c19394d65251717a7db4456a684be9bde2df673da00067cea05bbfc307fa37`  
		Last Modified: Wed, 22 Oct 2025 20:17:05 GMT  
		Size: 53.8 KB (53847 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-trixie` - linux; ppc64le

```console
$ docker pull postgres@sha256:20873ba8ad19904a2db66720b58ce87f79852553fb4c9b33d93dbb706753e0c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.5 MB (173453929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83fb882ce51628a89bf2e6bd4c7cb465ee7a24ee82b7bb3d612d7eddf239f406`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 05:28:29 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Nov 2025 05:28:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 05:28:58 GMT
ENV GOSU_VERSION=1.19
# Tue, 04 Nov 2025 05:28:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 05:29:08 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 04 Nov 2025 05:29:08 GMT
ENV LANG=en_US.utf8
# Tue, 04 Nov 2025 05:29:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 05:29:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Nov 2025 05:29:16 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 05:29:16 GMT
ENV PG_MAJOR=17
# Tue, 04 Nov 2025 05:29:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 04 Nov 2025 05:29:16 GMT
ENV PG_VERSION=17.6-2.pgdg13+1
# Tue, 04 Nov 2025 05:34:48 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 04 Nov 2025 05:34:48 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Nov 2025 05:34:49 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Nov 2025 05:34:49 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Nov 2025 05:34:49 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 04 Nov 2025 05:34:49 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Nov 2025 05:34:50 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 05:34:51 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Nov 2025 05:34:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 05:34:51 GMT
STOPSIGNAL SIGINT
# Tue, 04 Nov 2025 05:34:51 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Nov 2025 05:34:51 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6817b6703cb75bdc729c8ede685ed38f44a4184e4e4d51559386d59d72eb257b`  
		Last Modified: Tue, 04 Nov 2025 05:31:03 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f490ad0a24773bfe9acb4c8cb70636d88d35af427ff1aac539e93fca45bbbb`  
		Last Modified: Tue, 04 Nov 2025 05:31:04 GMT  
		Size: 7.1 MB (7075842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c7d07c82d0b904418ce0647f7740a4f0bd9f68113d52b854e593e5deb473a8`  
		Last Modified: Tue, 04 Nov 2025 05:31:03 GMT  
		Size: 1.2 MB (1214643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef72c60312e96a4f77b06baf4174b5b218065751fe0d6c1bb2ddee4315f0965a`  
		Last Modified: Tue, 04 Nov 2025 05:31:05 GMT  
		Size: 8.2 MB (8203897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142efaa2871a984549c89ca109f2a8b2e6cefa9e473a2b2f6c58e15036ed3236`  
		Last Modified: Tue, 04 Nov 2025 05:31:03 GMT  
		Size: 1.4 MB (1394708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c725c78eef3c2a165b671043ed07da8f6b159ac56f63d28b00b3a10f7f7ec0be`  
		Last Modified: Tue, 04 Nov 2025 05:31:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf12ea6639a8a7bf71289dc415727da3f95280fe4233abac84bea2d0704b6527`  
		Last Modified: Tue, 04 Nov 2025 05:31:03 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ff579563aa3b6c6ae504dc5ccf01bfd6dbfcb49b226d4efc6aa78670ae5234`  
		Last Modified: Tue, 04 Nov 2025 05:35:53 GMT  
		Size: 121.9 MB (121944874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df99d04381d0bb55554a44eab2776aa35a9c2cf4459a05d5ba3616881ca4f48`  
		Last Modified: Tue, 04 Nov 2025 05:35:46 GMT  
		Size: 10.3 KB (10338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb8df16f0829b5e80f81181619f2cc70491eb90c42386fc891b6f7b396e67a7a`  
		Last Modified: Tue, 04 Nov 2025 05:35:46 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ccb6cf0d2f11a76c0c420a64906dd5fbf3cba2360a6af712b20f353197f585f`  
		Last Modified: Tue, 04 Nov 2025 05:35:46 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db220634e24a4f88d396e7957fb1ececc116af77a64dbbc68b90c9bbd3abca0`  
		Last Modified: Tue, 04 Nov 2025 05:35:46 GMT  
		Size: 6.1 KB (6077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a390b228972cfb331496ed891e3b3e9b7aa4503d30179d3f210cbaf182c633e`  
		Last Modified: Tue, 04 Nov 2025 05:35:46 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:24da36e2964bb95edb10682173e9039df5f9c44a138f12dc0119f0dce5239b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5786899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad7be42da8704e81986f7133c106b230976e1f8ea049482e9507fbbef8d67109`

```dockerfile
```

-	Layers:
	-	`sha256:e228d074ed556adca7fb70e1ac5c70b2d21c0d3451e05c31368bf05fafe149be`  
		Last Modified: Tue, 04 Nov 2025 09:11:16 GMT  
		Size: 5.7 MB (5732973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d05c5b93a6c9cf075793e4f53a54879b273477ef9e328149128157b5f1af27dc`  
		Last Modified: Tue, 04 Nov 2025 09:11:17 GMT  
		Size: 53.9 KB (53926 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-trixie` - linux; riscv64

```console
$ docker pull postgres@sha256:83dee71f4c7e965cc88fdb3a0f8a3ea3db2193f4a1903a80a311e45af514e9a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 MB (92185026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03168a7e14ead3083c8e1ceb1dc65652949c597c71cd067f55edf962bfe6e949`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Oct 2025 18:23:03 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
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
ENV PG_MAJOR=17
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PG_VERSION=17.6-2.pgdg13+1
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9adff4a179b9fe91b9f15b2dc9b98bf13f6bd73026e8adafc003200ff4ce44f1`  
		Last Modified: Wed, 22 Oct 2025 07:43:55 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200d06b9a5432c81900eb717e8f64f41557ca1d50eea4d1437901ae684688ba4`  
		Last Modified: Wed, 22 Oct 2025 07:43:55 GMT  
		Size: 6.3 MB (6291294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034271ddbd25d251a136a1b3cd58a2afad5c42501617c6f3589df7eb31d7eb57`  
		Last Modified: Wed, 22 Oct 2025 07:43:55 GMT  
		Size: 1.2 MB (1201922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6227f719f4c8788701a2c3ecfd26e17753f53ef1064be8631a140fbcb89e7c28`  
		Last Modified: Wed, 22 Oct 2025 07:43:55 GMT  
		Size: 8.2 MB (8203561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ea035a8f71d660e4020de05d9777ec52394d907e6b7d28c7d817ec09fd0030`  
		Last Modified: Wed, 22 Oct 2025 07:43:55 GMT  
		Size: 1.4 MB (1402196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f31d0e78680834398d35967ceca0da016e7fca57876699f978631fcd90b557`  
		Last Modified: Wed, 22 Oct 2025 07:43:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548a458eab1846771dcaff6277ef6428e8b3883bc3b09c4646df76499a6c8651`  
		Last Modified: Wed, 22 Oct 2025 07:43:55 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3534da3d7aea8bb8a6939804b67328c4f46cb2ed0999f5eab592a4cc03b2b70`  
		Last Modified: Wed, 22 Oct 2025 09:54:57 GMT  
		Size: 46.8 MB (46789074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38fe9670630f0425e9eacb5505c038b333033ac82031b599f3d57b871e461c0`  
		Last Modified: Wed, 22 Oct 2025 09:54:53 GMT  
		Size: 10.3 KB (10344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8129a67bebb34cab5ae46d32a42d5e31c3c984c171e274ae47ccd124e75e4fae`  
		Last Modified: Wed, 22 Oct 2025 09:54:53 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da50ec78ddb6902c2f03778bee15ba7cf34ed836ab13b3d536ef38205b779015`  
		Last Modified: Wed, 22 Oct 2025 09:54:53 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0b09eea23707c40454cbae611e80b7f87d93442ec3d32f6158052e40d49f01`  
		Last Modified: Fri, 24 Oct 2025 09:58:56 GMT  
		Size: 6.1 KB (6077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc46697dbf1763c3142360b5229caa560bcfe9e1acbaf9ccdf1166ae6f45ad3`  
		Last Modified: Fri, 24 Oct 2025 09:58:57 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:09e6a4d93b4638f1e5e8236543681293d128759c9209cb9cf011dfc97ecdfff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299c133225e9caff4927eeb82dfd2212c0099d1786e9440e13660dd966054080`

```dockerfile
```

-	Layers:
	-	`sha256:fe62fc367a11b0fb25253d3619793dfffa30d0addc58b271dfa7c325b901c05f`  
		Last Modified: Fri, 24 Oct 2025 11:08:43 GMT  
		Size: 5.1 MB (5083636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6db2f54bcf0dd1a97542b0e10660ff70439d694b34eeadd4baf1503785721b6`  
		Last Modified: Fri, 24 Oct 2025 11:08:44 GMT  
		Size: 54.0 KB (53961 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-trixie` - linux; s390x

```console
$ docker pull postgres@sha256:83f98b667a02d1f12acf7411cf12f1c863e3cdbc138f8d420badc2276457ae62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.7 MB (175686120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:049357839382ec2d8e3a743e68f929b592babbbe46069a3cefc9b36105cc062a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 08:27:40 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Nov 2025 08:27:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 08:27:54 GMT
ENV GOSU_VERSION=1.19
# Tue, 04 Nov 2025 08:27:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 08:27:59 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 04 Nov 2025 08:27:59 GMT
ENV LANG=en_US.utf8
# Tue, 04 Nov 2025 08:28:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 08:28:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Nov 2025 08:28:03 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 08:28:03 GMT
ENV PG_MAJOR=17
# Tue, 04 Nov 2025 08:28:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 04 Nov 2025 08:28:03 GMT
ENV PG_VERSION=17.6-2.pgdg13+1
# Tue, 04 Nov 2025 08:53:09 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 04 Nov 2025 08:53:10 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Nov 2025 08:53:10 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Nov 2025 08:53:10 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Nov 2025 08:53:10 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 04 Nov 2025 08:53:10 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Nov 2025 08:53:10 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 08:53:10 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Nov 2025 08:53:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 08:53:10 GMT
STOPSIGNAL SIGINT
# Tue, 04 Nov 2025 08:53:10 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Nov 2025 08:53:10 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5277ec6f1c414b484db9fecc0de77c602e71fee039360fe110650cb6890929`  
		Last Modified: Tue, 04 Nov 2025 08:41:15 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bdb34bb3e2a5ce0cae8e52551c685fcd8a7788df7db7a1dacc2dba0485da423`  
		Last Modified: Tue, 04 Nov 2025 08:41:15 GMT  
		Size: 6.4 MB (6408741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5944ce8ab4406ba39b9a721554f0500abbb457a4135eca29aa30d6d9b6cd0181`  
		Last Modified: Tue, 04 Nov 2025 08:41:15 GMT  
		Size: 1.2 MB (1229847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4065048143b841bc109b3f36e52f213361de57f8d57e33ebb995b779ef564aa`  
		Last Modified: Tue, 04 Nov 2025 08:41:15 GMT  
		Size: 8.3 MB (8258764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9870370b0442159a69dcb66a3326acf087e6588d12f2a75fed7bc4b91d58d0`  
		Last Modified: Tue, 04 Nov 2025 08:41:15 GMT  
		Size: 1.4 MB (1398013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ee11469e556709ea343bdedb60914171686d2d59c00ac49fa1ea2b680291cb`  
		Last Modified: Tue, 04 Nov 2025 08:41:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab28319756ac85bb250fcfd214d93036f6975220cb83316adadd9f83f687c51`  
		Last Modified: Tue, 04 Nov 2025 08:41:15 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c196b32753c1a6500c6ee936f8b9b636ab801db6c0373597e66363ffd82cdd`  
		Last Modified: Tue, 04 Nov 2025 09:11:57 GMT  
		Size: 128.5 MB (128532041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566592a82abdb55c07de9d442f1bdf8537863333db4618e2a3d3cb71f0e1a12d`  
		Last Modified: Tue, 04 Nov 2025 08:54:00 GMT  
		Size: 10.3 KB (10343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1fad987200501b6b494da2b1828a9cc4e7c664bf5da61873da3664818b5daeb`  
		Last Modified: Tue, 04 Nov 2025 08:54:00 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49cf978f1b95c32b1a4f2225a82c9739209ec54759967c4086a1c6e4e70291a`  
		Last Modified: Tue, 04 Nov 2025 08:54:00 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec10d450bee732ed68d7f454620e4b4fab9a98f38a1095ee875f40ef09c8b7eb`  
		Last Modified: Tue, 04 Nov 2025 08:54:00 GMT  
		Size: 6.1 KB (6078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd58d422ebca2b54ca1b2aad9a065ac62a044f88968b13d23e493fe33db630f1`  
		Last Modified: Tue, 04 Nov 2025 08:54:01 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:e0aeb7b2fc5727126f5d3f5a771a7caf8af444c3573ed1b3595adfd106d0655e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5795169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e8a9ce929859907a404aa447f4e7daa7ac9009274221e4a9e67a93c5e04042d`

```dockerfile
```

-	Layers:
	-	`sha256:24ef3af7f075038ab609db45e4f711df1332b53fd7c5dd35d48ac1f1fd32fa50`  
		Last Modified: Tue, 04 Nov 2025 09:11:25 GMT  
		Size: 5.7 MB (5741309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c28c14f7436383b52fbc1536a37f9a350ac6b5ffa1db75de1e4c2039e72a087f`  
		Last Modified: Tue, 04 Nov 2025 09:11:26 GMT  
		Size: 53.9 KB (53860 bytes)  
		MIME: application/vnd.in-toto+json
