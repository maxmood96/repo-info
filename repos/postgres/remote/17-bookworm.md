## `postgres:17-bookworm`

```console
$ docker pull postgres@sha256:a361dee4f2fc44864038d239e87a409901124828c75993c172ed5914e8fec805
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
$ docker pull postgres@sha256:102594a97342ea7ff17e6657db147574944a83c20643b4e116acec9b6ccc9621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156096922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ca68e400d39abaee156031ccd6ffae4c5df695d59037d246b7182032bc7e71b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:34:57 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 11 Jun 2026 00:35:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:35:09 GMT
ENV GOSU_VERSION=1.19
# Thu, 11 Jun 2026 00:35:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 11 Jun 2026 00:35:14 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 11 Jun 2026 00:35:14 GMT
ENV LANG=en_US.utf8
# Thu, 11 Jun 2026 00:35:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:35:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Jun 2026 00:35:17 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:35:17 GMT
ENV PG_MAJOR=17
# Thu, 11 Jun 2026 00:35:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 11 Jun 2026 00:35:17 GMT
ENV PG_VERSION=17.10-1.pgdg12+1
# Thu, 11 Jun 2026 00:35:29 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 11 Jun 2026 00:35:29 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 11 Jun 2026 00:35:29 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 11 Jun 2026 00:35:29 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 11 Jun 2026 00:35:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 11 Jun 2026 00:35:30 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 11 Jun 2026 00:35:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:35:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 11 Jun 2026 00:35:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:35:30 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jun 2026 00:35:30 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 11 Jun 2026 00:35:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a947e693491227e060b1b397702501f4e486f26b6f863c71431285d1de9d6e9`  
		Last Modified: Thu, 11 Jun 2026 00:35:50 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03be56ac3ff2cf371eabf48eca6c8113aa305a529b960763d41ce80b3af17fd`  
		Last Modified: Thu, 11 Jun 2026 00:35:51 GMT  
		Size: 4.5 MB (4534260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423aa4457e687da6e55dfdf291b1a4898c99b6c25407b3eb0a5283a2ac0aef36`  
		Last Modified: Thu, 11 Jun 2026 00:35:50 GMT  
		Size: 1.2 MB (1249509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578b03bc2adefe00adbd18d23305463e968c3716316a140f6792679524a02a93`  
		Last Modified: Thu, 11 Jun 2026 00:35:51 GMT  
		Size: 8.1 MB (8066489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733b0e8d24afc60b35122fdb47a0d2bb5fb856e461414088e8d641f4255f32a2`  
		Last Modified: Thu, 11 Jun 2026 00:35:51 GMT  
		Size: 1.2 MB (1196380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152e821831462b1c0820a9e35d12dca71932c18f95531411151e2d59af8d2001`  
		Last Modified: Thu, 11 Jun 2026 00:35:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d78c343a5491a0e3d39dc4777f829639ea1f98d5d27f8c43191527328affa6`  
		Last Modified: Thu, 11 Jun 2026 00:35:52 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0ca4f658b9033bc7cdc9d5e56864fbd3649339bc042db113284062fae9762a`  
		Last Modified: Thu, 11 Jun 2026 00:35:55 GMT  
		Size: 112.8 MB (112791370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dee1c4ba28bbd434efe8a63d2d61faefd6486a733e648049feaff592dd5d67`  
		Last Modified: Thu, 11 Jun 2026 00:35:53 GMT  
		Size: 10.3 KB (10295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b5ce0a7507307129c7d2e0e30ab1855e6545229ad0976176d7917a5e34266a`  
		Last Modified: Thu, 11 Jun 2026 00:35:53 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcc936d0dac6094028f5a1fa8c1b59fb792a29d56591bb284787e534d72a8cb`  
		Last Modified: Thu, 11 Jun 2026 00:35:54 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e599f5967330c66fa5340c203cfbb6a9d27af9f871ad99543e6cadb252bfb8`  
		Last Modified: Thu, 11 Jun 2026 00:35:55 GMT  
		Size: 6.1 KB (6094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556f8f514660025148be077d65487586ae94aac61f76dbf99c3db2112501d3a1`  
		Last Modified: Thu, 11 Jun 2026 00:35:55 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:87366576aea44bd289b005ec03d578dbcf9b4c4208a82c9fb2f9f544da8641b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5980809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eb03f69854651d20cbd809ddd5a9468ebc0981471bf0787a1ee88462200a4a6`

```dockerfile
```

-	Layers:
	-	`sha256:6130f35a1ba975c575ac04474e0c6e48277b9b8c60e5e2cb56a4bd7eb29c1fb1`  
		Last Modified: Thu, 11 Jun 2026 00:35:51 GMT  
		Size: 5.9 MB (5927508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ac874e3e76ab593a1f5014f2ac8d1d0557fa94bfdfe4aa147ad7e5fbf5c718e`  
		Last Modified: Thu, 11 Jun 2026 00:35:50 GMT  
		Size: 53.3 KB (53301 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:ba5cf21809efac86088d5bcb509acbe6a24c3c169c3763dae288a43639f478c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149130961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3066e3fa1018dea12f8e82b8a1f2e0d50d73087087f9087a538e4e78adf59bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:47:50 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 11 Jun 2026 00:47:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:48:08 GMT
ENV GOSU_VERSION=1.19
# Thu, 11 Jun 2026 00:48:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 11 Jun 2026 00:48:15 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 11 Jun 2026 00:48:15 GMT
ENV LANG=en_US.utf8
# Thu, 11 Jun 2026 00:48:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:48:21 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Jun 2026 00:48:21 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:48:21 GMT
ENV PG_MAJOR=17
# Thu, 11 Jun 2026 00:48:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 11 Jun 2026 00:48:21 GMT
ENV PG_VERSION=17.10-1.pgdg12+1
# Thu, 11 Jun 2026 01:04:31 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 11 Jun 2026 01:04:31 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 11 Jun 2026 01:04:31 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 11 Jun 2026 01:04:31 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 11 Jun 2026 01:04:31 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 11 Jun 2026 01:04:31 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 11 Jun 2026 01:04:31 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 01:04:31 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 11 Jun 2026 01:04:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 01:04:31 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jun 2026 01:04:31 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 11 Jun 2026 01:04:31 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:99eb1512995af32b91c63bcd418e886af77e3c7ca088226161af558763425461`  
		Last Modified: Wed, 10 Jun 2026 23:38:28 GMT  
		Size: 25.8 MB (25773188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5d7ae8b920d5480731067014dec0d4e5ef7d47f797d0be7e5ae964dcaa05d7`  
		Last Modified: Thu, 11 Jun 2026 01:04:50 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c0859497719717aa6b13177b5bbf2f8f679077aa65a41cafcab6a3165933cc`  
		Last Modified: Thu, 11 Jun 2026 01:04:51 GMT  
		Size: 4.2 MB (4151335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696e9ae9d5e176f32ad8040691141d26538780cfd20d06de833e25207d286037`  
		Last Modified: Thu, 11 Jun 2026 01:04:50 GMT  
		Size: 1.2 MB (1220102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce621e86d3f74e81eefd38b878191ce3c7f3d6b9f3f31d973b49c89ffc5df37`  
		Last Modified: Thu, 11 Jun 2026 01:04:51 GMT  
		Size: 8.1 MB (8066588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47a43adbbde733ebca83b79817192ab4c3d86be6ae6d70184ac367902bfaf2c`  
		Last Modified: Thu, 11 Jun 2026 01:04:52 GMT  
		Size: 1.2 MB (1195127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5206962b7e5c6cb0de42292168e41de5fe9b572fbec63269fb0e414e9cc3f84d`  
		Last Modified: Thu, 11 Jun 2026 01:04:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444cf297213662688f57166a269d204e3ac6af4549db817df1c3e98e62bb0e00`  
		Last Modified: Thu, 11 Jun 2026 01:04:52 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e105230611a229cf0bf33ace05e4dcbf784b2c0caf2220531abdefbdab8bdb7a`  
		Last Modified: Thu, 11 Jun 2026 01:04:56 GMT  
		Size: 108.7 MB (108703324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8fa7ecfbadca92385be49c8b23eac25c9483f30e809282317c94d8796db032`  
		Last Modified: Thu, 11 Jun 2026 01:04:53 GMT  
		Size: 10.3 KB (10298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221c0367560adefefc042fd7561a90e6fc34891edea4d8eaa1b8150792f3e0ce`  
		Last Modified: Thu, 11 Jun 2026 01:04:53 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61704b94b7e27499db87d2b6ab63d1db011e5ff985c73026084c4bd0070b881b`  
		Last Modified: Thu, 11 Jun 2026 01:04:54 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871bb829b6b71ece3b2a6c41ce41309f702e3b84c7e3f62effb828e3c0eb9f9e`  
		Last Modified: Thu, 11 Jun 2026 01:04:55 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8255afc57fa58fe2550d7c36083663bdf407e355bb2e31c0fc5cf149b212e4`  
		Last Modified: Thu, 11 Jun 2026 01:04:55 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:7afeb9d0ffdd6715ff804759642c5dce9de45797bc17953a635ee85c07835568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5999333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b5f5d4e47816e96c949b3d064eaea27b5c4e7389575d3f4c7b766f23f265313`

```dockerfile
```

-	Layers:
	-	`sha256:ea52547a6d751e156b4c4c19096601af7902d353f3e81b3a8cf398168ec83bc9`  
		Last Modified: Thu, 11 Jun 2026 01:04:51 GMT  
		Size: 5.9 MB (5945825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb3669c97de6b07804746f7a25435fbfc3a7eae4482539e7885fe1979ae7e9d6`  
		Last Modified: Thu, 11 Jun 2026 01:04:50 GMT  
		Size: 53.5 KB (53508 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:f0dadb14545ef56ed492a7307d12a2066a9c9b4d666e205f3e0ead49b88d4523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144127536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f95328ef3327cc46d166339ae053431562adc5a755f41c73000525a8c98306c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:00:33 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 11 Jun 2026 01:00:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:00:47 GMT
ENV GOSU_VERSION=1.19
# Thu, 11 Jun 2026 01:00:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 11 Jun 2026 01:00:52 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 11 Jun 2026 01:00:52 GMT
ENV LANG=en_US.utf8
# Thu, 11 Jun 2026 01:00:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:00:56 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Jun 2026 01:00:56 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 01:00:56 GMT
ENV PG_MAJOR=17
# Thu, 11 Jun 2026 01:00:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 11 Jun 2026 01:00:56 GMT
ENV PG_VERSION=17.10-1.pgdg12+1
# Thu, 11 Jun 2026 01:15:45 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 11 Jun 2026 01:15:45 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 11 Jun 2026 01:15:45 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 11 Jun 2026 01:15:45 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 11 Jun 2026 01:15:45 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 11 Jun 2026 01:15:45 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 11 Jun 2026 01:15:45 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 01:15:45 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 11 Jun 2026 01:15:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 01:15:45 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jun 2026 01:15:45 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 11 Jun 2026 01:15:45 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8ae2378435d99f39097aa4fd0d6c58c08445becca3153d53205b2cc5054b09c2`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 23.9 MB (23944473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbbb655004e9c96408c547089490dae0a45036adc3bc0485fdaeab10ad48b8d`  
		Last Modified: Thu, 11 Jun 2026 01:16:04 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437c70c128538fa5a4e6cc62927ab475ca4f9a0a8f32e1c579a4ce8dd988aa65`  
		Last Modified: Thu, 11 Jun 2026 01:16:04 GMT  
		Size: 3.7 MB (3742667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a1aef3c2e8a4c3516d015939cae200e78157cdaa36c55a65071ee66076efac`  
		Last Modified: Thu, 11 Jun 2026 01:16:04 GMT  
		Size: 1.2 MB (1216011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c62a28e8bed099251ebff3e9012b15dcedadbaf8c5b85ff8fadb0da55e03153`  
		Last Modified: Thu, 11 Jun 2026 01:16:04 GMT  
		Size: 8.1 MB (8066429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:180eef8f1a4c1b4c6beaae5aa383be23b4b3e34277784f1bba7e882245c404c6`  
		Last Modified: Thu, 11 Jun 2026 01:16:05 GMT  
		Size: 1.1 MB (1067278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5196a2d248fdc32b4b4023e769f973a313e9353c8aac2839920b96240f1f73e`  
		Last Modified: Thu, 11 Jun 2026 01:16:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a538c03866a6671738c339916f889c8333a2d9e1eef8876dba48c27fd3a9def1`  
		Last Modified: Thu, 11 Jun 2026 01:16:05 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5054909ac063ea8b089344d0f64f91a6fe28416cbb54c4c3aa21c1ef6182c161`  
		Last Modified: Thu, 11 Jun 2026 01:16:08 GMT  
		Size: 106.1 MB (106069378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe8eff3969eafc29943944abead3dcab35133b8a1e3c0819af9489d799843a1`  
		Last Modified: Thu, 11 Jun 2026 01:16:07 GMT  
		Size: 10.3 KB (10300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa94f2900bd8b568f5003f98d4ffc73495710ded017fc5a0045f56269fec9553`  
		Last Modified: Thu, 11 Jun 2026 01:16:07 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229193684a5c0f67e6f013ac67db4ee03f8ce54d539cd047a94943f0a29100ff`  
		Last Modified: Thu, 11 Jun 2026 01:16:07 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e33689379b0e2509046ea0f0cfbde5f6b1ebc5734bc3ef6a2d41c6fcf426c94`  
		Last Modified: Thu, 11 Jun 2026 01:16:08 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f654acb61178ce25b1d185e502a8dd61cc8b07d82f173353de4b4202dd87f0f7`  
		Last Modified: Thu, 11 Jun 2026 01:16:08 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:0353a7b455382b535d4736f0c0e9a0ca2045ce4f1d14d177592bd3d33505e4b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5998587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565e694cd453cd91ca3f10afdc9e5d130dbb92aa2ee99bc874265ce18b3e04ae`

```dockerfile
```

-	Layers:
	-	`sha256:008dab5ae0c86165b7608f22e1a61797e80a14da6b29ab6fd3d472dbcb21f4d1`  
		Last Modified: Thu, 11 Jun 2026 01:16:04 GMT  
		Size: 5.9 MB (5945080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2225bf94f2eb697af339988ec44e2c54bd0d146ef6e90eae64f3c1275b63b8f`  
		Last Modified: Thu, 11 Jun 2026 01:16:04 GMT  
		Size: 53.5 KB (53507 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:9d08b9992171b42bc227fb2ed47b3d8d963a9a44cbb3811cf6b695423663cb41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154128453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da8c3e55a6b678cd4cc9cc4a9ace990ab0ba11a51bcf62a83a6ba6bb341e4c1a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:36:30 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 11 Jun 2026 00:36:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:36:41 GMT
ENV GOSU_VERSION=1.19
# Thu, 11 Jun 2026 00:36:41 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 11 Jun 2026 00:36:46 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 11 Jun 2026 00:36:46 GMT
ENV LANG=en_US.utf8
# Thu, 11 Jun 2026 00:36:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:36:49 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Jun 2026 00:36:49 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:36:49 GMT
ENV PG_MAJOR=17
# Thu, 11 Jun 2026 00:36:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 11 Jun 2026 00:36:49 GMT
ENV PG_VERSION=17.10-1.pgdg12+1
# Thu, 11 Jun 2026 00:37:01 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 11 Jun 2026 00:37:01 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 11 Jun 2026 00:37:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 11 Jun 2026 00:37:01 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 11 Jun 2026 00:37:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 11 Jun 2026 00:37:01 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 11 Jun 2026 00:37:01 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:37:01 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 11 Jun 2026 00:37:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:37:01 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jun 2026 00:37:01 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 11 Jun 2026 00:37:01 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a00a9b35ae38d7c121be03aa165571e683d219e0f2f26ff447c78987ba76f4f`  
		Last Modified: Thu, 11 Jun 2026 00:37:21 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd6db56ef2cf33ff512a7af2a28f43ca648263490d11c18130a8d0c9c8186b4`  
		Last Modified: Thu, 11 Jun 2026 00:37:21 GMT  
		Size: 4.5 MB (4519569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:702fcce4cfb42cdb9e5b8de2ae3ba3da1843b60c78b6adc2c3937e72ebb5b135`  
		Last Modified: Thu, 11 Jun 2026 00:37:21 GMT  
		Size: 1.2 MB (1203312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b8dd3045b440d73b49088f08704ff3272d170bf3df65c9358260f1e07734ed`  
		Last Modified: Thu, 11 Jun 2026 00:37:21 GMT  
		Size: 8.1 MB (8066498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fae9e2d3ad38d68d0d88d8e9c0ac959e2e5ce29d2acb675750f71e03fbf432c`  
		Last Modified: Thu, 11 Jun 2026 00:37:22 GMT  
		Size: 1.1 MB (1109059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ca214cbaa9e479572d806d7d746002f210cbac432e00e40ba8d4dea444bf8b`  
		Last Modified: Thu, 11 Jun 2026 00:37:22 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7e1f46a919df3ac54a0a90bd8af37224c2d6f0e9e98568efdd56c03246f8d3`  
		Last Modified: Thu, 11 Jun 2026 00:37:23 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71af2b814a1cd0da6d83a934ce06451cab26b1dddede066ccdd638c83f26463`  
		Last Modified: Thu, 11 Jun 2026 00:37:26 GMT  
		Size: 111.1 MB (111086423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33b4b5a94c5ca092d727582242dcc2ddac71e523e1701b6fb9dac248fe68dbc`  
		Last Modified: Thu, 11 Jun 2026 00:37:24 GMT  
		Size: 10.3 KB (10294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca8d64e5817ae11896610d16e3de24bec7a585ff110706b6498bd92dc98092d`  
		Last Modified: Thu, 11 Jun 2026 00:37:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923e4f9c32265b025689ba0b34b87191914ac85ba8fec59b259f3adc39a72452`  
		Last Modified: Thu, 11 Jun 2026 00:37:24 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf079f36aa6a1913de2aed179e43bead9566e3807d803362d91eb775ea2e0cc`  
		Last Modified: Thu, 11 Jun 2026 00:37:25 GMT  
		Size: 6.1 KB (6092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616c4c09641368014a2a79c332a72a3d603138b5ae71834d402d874931cb8576`  
		Last Modified: Thu, 11 Jun 2026 00:37:25 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:62d39510ee79d6c423729c1db8c4f574d25b560980579d87fba4acf3a26a3ec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5987365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:807865e1dc8d0588ad4cbbf9604a3e75889afc9d57d6e671c036772c35868bb5`

```dockerfile
```

-	Layers:
	-	`sha256:7303dbde032f27bdf84f3d220db6b486715126f312e6a4c8d6fdebdd6a58d768`  
		Last Modified: Thu, 11 Jun 2026 00:37:21 GMT  
		Size: 5.9 MB (5933819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a973315a9947c04b07e9146e2ffa9a1d3be2906f422edfa60e2c51d399c97d7`  
		Last Modified: Thu, 11 Jun 2026 00:37:21 GMT  
		Size: 53.5 KB (53546 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:b14df2fa134627164b058a1d26977d7a1314a415c73500c368c949b51d438e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.0 MB (164994517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf2536770b5d83a81f8f4ab6c89a1224f68e49d068a750bcabcb6a8464df0ad9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:32:05 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 11 Jun 2026 00:32:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:32:16 GMT
ENV GOSU_VERSION=1.19
# Thu, 11 Jun 2026 00:32:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 11 Jun 2026 00:32:20 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 11 Jun 2026 00:32:20 GMT
ENV LANG=en_US.utf8
# Thu, 11 Jun 2026 00:32:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:32:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Jun 2026 00:32:24 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:32:24 GMT
ENV PG_MAJOR=17
# Thu, 11 Jun 2026 00:32:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 11 Jun 2026 00:32:24 GMT
ENV PG_VERSION=17.10-1.pgdg12+1
# Thu, 11 Jun 2026 00:43:02 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 11 Jun 2026 00:43:02 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 11 Jun 2026 00:43:02 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 11 Jun 2026 00:43:02 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 11 Jun 2026 00:43:02 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 11 Jun 2026 00:43:02 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 11 Jun 2026 00:43:02 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:43:02 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 11 Jun 2026 00:43:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:43:02 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jun 2026 00:43:02 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 11 Jun 2026 00:43:02 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:707460b758530d4476f3fefff30544db7cf8dbd98838ccc3533bc05e79016be4`  
		Last Modified: Wed, 10 Jun 2026 23:40:00 GMT  
		Size: 29.2 MB (29225762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505cb8d48ef4bdd0cb3b081265503c0be45cda26ed6d7caa071fe6eed80403f4`  
		Last Modified: Thu, 11 Jun 2026 00:43:21 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ddde968f92909b01ea3bd4894308eaacc5fd062f5476076184e2bc4d2478f5`  
		Last Modified: Thu, 11 Jun 2026 00:43:21 GMT  
		Size: 5.0 MB (4966113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8937f2bd1f8cd4b2d93aa119fe91b1b6432f778756984dd790365c8080c4173e`  
		Last Modified: Thu, 11 Jun 2026 00:43:21 GMT  
		Size: 1.2 MB (1218676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026e690d796d98b92e74a46de5948d6cc26e83374542283df6d92b29891695ea`  
		Last Modified: Thu, 11 Jun 2026 00:43:21 GMT  
		Size: 8.1 MB (8066466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ebd3f5cf3acfdfde7e8c7abffca9837e1098879508f32dfba11e0a7b92bf7dd`  
		Last Modified: Thu, 11 Jun 2026 00:43:23 GMT  
		Size: 1.1 MB (1137464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfa9e32f829d28a70ef14b248e2a1ea9572116a96345f757c7cd061206ab5b9`  
		Last Modified: Thu, 11 Jun 2026 00:43:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba4a6cbf876dead63ec017457af3058b02b7611adb57647806d1ea15cc408b2`  
		Last Modified: Thu, 11 Jun 2026 00:43:23 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab77d3a84ae394e596f39bd5e0b39aadf75eb72254b15999ae7b0e527b3495ee`  
		Last Modified: Thu, 11 Jun 2026 00:43:26 GMT  
		Size: 120.4 MB (120358737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6979982af9f8f697aaa78cb38e41dccfc60ce29b0fba460431b2f92464b343`  
		Last Modified: Thu, 11 Jun 2026 00:43:24 GMT  
		Size: 10.3 KB (10299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016c9c7c672ee3b9ca098258cda100aeaf1d610d2de9225d3ffd2036a6c52f11`  
		Last Modified: Thu, 11 Jun 2026 00:43:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90dd75959ce3cd744529e0f0403c8418fdfe4e048df714d38d0f59f5381b0d45`  
		Last Modified: Thu, 11 Jun 2026 00:43:24 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ee969d12e791d6423870b3c2d02b013d9cf967e33d1c3fdb956cd0b9794399`  
		Last Modified: Thu, 11 Jun 2026 00:43:25 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cab1fc9c7371c2d043ab0396c7171b11069f5a7a70be7201a898ddddbf0b9f`  
		Last Modified: Thu, 11 Jun 2026 00:43:25 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:7a72020af750af646809eea2f6d115e316252b7492cb357be13a50d3084013af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5997225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ef17b17f2a2fad650f20334e0afb15492f5e52d2d414c4486999db7f673ce35`

```dockerfile
```

-	Layers:
	-	`sha256:f7e0c013421ced277f89ba121dce3e13bad6dff132f41f023d603c762c3b9fce`  
		Last Modified: Thu, 11 Jun 2026 00:43:21 GMT  
		Size: 5.9 MB (5943968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a36cd13178c844bb7ea6f89a5230bceb417ab10f7b2cd27ffae54087480f2a9`  
		Last Modified: Thu, 11 Jun 2026 00:43:21 GMT  
		Size: 53.3 KB (53257 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:20f60f3811b87af4f284591507f2653b234ed7148ad639a262c97ccfdb02a0e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.0 MB (154978390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a84f9d36ea536a6624f5cddc64a1a0799a9f07ffae6f47539aa88058d953d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 03:47:32 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 20 May 2026 03:48:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 03:48:39 GMT
ENV GOSU_VERSION=1.19
# Wed, 20 May 2026 03:48:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 20 May 2026 03:49:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 20 May 2026 03:49:06 GMT
ENV LANG=en_US.utf8
# Wed, 20 May 2026 03:49:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 03:49:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 20 May 2026 03:49:29 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 20 May 2026 03:49:29 GMT
ENV PG_MAJOR=17
# Wed, 20 May 2026 03:49:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Wed, 20 May 2026 03:49:29 GMT
ENV PG_VERSION=17.10-1.pgdg12+1
# Wed, 20 May 2026 06:12:52 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 20 May 2026 06:12:55 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 20 May 2026 06:12:56 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 20 May 2026 06:12:56 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 20 May 2026 06:12:58 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 20 May 2026 06:12:58 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 20 May 2026 06:13:00 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 20 May 2026 06:13:02 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 20 May 2026 06:13:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 06:13:02 GMT
STOPSIGNAL SIGINT
# Wed, 20 May 2026 06:13:02 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 20 May 2026 06:13:02 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:83efaacc11aede9fdd3dcef1c025f5df70c81553b815dfb44caceaf1fa9eba75`  
		Last Modified: Tue, 19 May 2026 22:35:42 GMT  
		Size: 28.5 MB (28522504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eab0ac5538ed0c0ccb817c384f2da276651cb900c4ee7f52230d296d7319ecf`  
		Last Modified: Wed, 20 May 2026 05:02:21 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3f24330c464e9c9a34b9c04f2af74377fb284ba681aecf1eaca7b0c8d5b376`  
		Last Modified: Wed, 20 May 2026 05:02:22 GMT  
		Size: 4.5 MB (4475198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98381d3276d839839fdcebfcf33bf865cf90eaf43ccf575978aa617c4059ff4`  
		Last Modified: Wed, 20 May 2026 05:02:21 GMT  
		Size: 1.2 MB (1159226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbabcffa59b806ff40b6d0aca34bf8d4642e4fe8a0529111a0a19fcc23d24a8f`  
		Last Modified: Wed, 20 May 2026 05:02:22 GMT  
		Size: 8.1 MB (8066669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec23172ba38a0ef878da18a9628307ee3ba06cb2002c4d210fac8bf8332c862`  
		Last Modified: Wed, 20 May 2026 05:02:23 GMT  
		Size: 1.2 MB (1182959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8236c98d68c2505862cb68f376e64638cb6a31d152042da0346a097dd0953ac8`  
		Last Modified: Wed, 20 May 2026 05:02:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6d4c1168ae55abd4742068cc060fc7424f84ae4123ad2c8ba118f837a61bd0`  
		Last Modified: Wed, 20 May 2026 05:02:23 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a13236a3a09bdda56680ba1e043013930e9869d26486bce8814f5c62cec5b97`  
		Last Modified: Wed, 20 May 2026 06:15:09 GMT  
		Size: 111.6 MB (111550529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd7b06cb7ba205c0a575074408fc4e7eb770dab3a134ef88db9a0176e691209`  
		Last Modified: Wed, 20 May 2026 06:14:58 GMT  
		Size: 10.3 KB (10298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e6a4a154d3266c908c17c50a9382e48c250f4a017268136ce0d995ce462d24`  
		Last Modified: Wed, 20 May 2026 06:14:58 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8a898a5a36c471915c5b1817f31bbc8b1441fa32b66395975ecf20c4bbc342`  
		Last Modified: Wed, 20 May 2026 06:14:58 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914ff27ae5a725cd9263a8a95e10ac1f4b6e206102b7615e9f448955d6a8bd1e`  
		Last Modified: Wed, 20 May 2026 06:14:59 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c89885917a909aa1dfb9fc689c3bbc1fabb43e4a5f734f9bad35aa79181a7de`  
		Last Modified: Wed, 20 May 2026 06:14:59 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:749ef9acbfbf0a87bdfd4aefef5afed990271219dd37c1fe8a5c245ec0252354
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 KB (53167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eba383564aa916b84a08094cac02c07071ad37b8213577ab66af560a8658604`

```dockerfile
```

-	Layers:
	-	`sha256:61d4fd733cef1a1177f4d59d3fb7e9d51d93c531db023c9deba2d926f7aa60d8`  
		Last Modified: Wed, 20 May 2026 06:14:57 GMT  
		Size: 53.2 KB (53167 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:bfb84ca726a0ab98d0bec5d1df30bb62c54a6ed1c574e8b54232bc0957a16c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.0 MB (168954058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92d9751e5ad49f143b5351acfb4042a5100c1c7d45ac467a32539fb567a27d05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 04:24:53 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 11 Jun 2026 04:25:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 04:25:14 GMT
ENV GOSU_VERSION=1.19
# Thu, 11 Jun 2026 04:25:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 11 Jun 2026 04:25:23 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 11 Jun 2026 04:25:23 GMT
ENV LANG=en_US.utf8
# Thu, 11 Jun 2026 04:25:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 04:25:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Jun 2026 04:25:31 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 04:25:31 GMT
ENV PG_MAJOR=17
# Thu, 11 Jun 2026 04:25:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 11 Jun 2026 04:25:31 GMT
ENV PG_VERSION=17.10-1.pgdg12+1
# Thu, 11 Jun 2026 04:29:01 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 11 Jun 2026 04:29:02 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 11 Jun 2026 04:29:02 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 11 Jun 2026 04:29:02 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 11 Jun 2026 04:29:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 11 Jun 2026 04:29:03 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 11 Jun 2026 04:29:03 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 04:29:03 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 11 Jun 2026 04:29:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 04:29:03 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jun 2026 04:29:03 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 11 Jun 2026 04:29:03 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:23f7cdee3ef2598b081c2b848fee95730a7ab2b1cc5b726c72dcb8c2fe3632f7`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 32.1 MB (32081941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9879978988d3514916adbb0e2d83185ae5bd8c8d0b8c65f0be2d53ba96bfa7c8`  
		Last Modified: Thu, 11 Jun 2026 04:26:47 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ea0380ce54b8d13335a48ef988ec86e91b21fcc1e842cda5e67de076d30f45`  
		Last Modified: Thu, 11 Jun 2026 04:26:48 GMT  
		Size: 5.4 MB (5368652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2467c481adaec6c7c016d4400a90964a0c95a9e2e53cb55f6162cd82b54af0`  
		Last Modified: Thu, 11 Jun 2026 04:26:47 GMT  
		Size: 1.2 MB (1208199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b6bfa79d3857d5a20416feaf6e46abc27c0a7e730f4656e0a617059df2960b`  
		Last Modified: Thu, 11 Jun 2026 04:26:48 GMT  
		Size: 8.1 MB (8066524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ce9565433b149801f0155b1840aa9aa755fc09b6329a68b351a67d87af82f4`  
		Last Modified: Thu, 11 Jun 2026 04:26:48 GMT  
		Size: 1.3 MB (1283632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b009d3d2307709cc92dfb72deb0105d5270a35feb1fc8cf28f4fd61c4c26f4d`  
		Last Modified: Thu, 11 Jun 2026 04:26:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3b066eb70f2b5963e0a2adeb18c1dbb057037c113b667965d5800b009296d8`  
		Last Modified: Thu, 11 Jun 2026 04:26:49 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea92a6a107848379dd01e373bd64363bc396375467d774f252385a65ce1c0f9`  
		Last Modified: Thu, 11 Jun 2026 04:29:45 GMT  
		Size: 120.9 MB (120923808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f054a05dda795adf0c5081e084e813faf861d4fcbfa00fd6c8fc8928058300bd`  
		Last Modified: Thu, 11 Jun 2026 04:29:42 GMT  
		Size: 10.3 KB (10295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41221f0e7dee3e981b3fe8245ea273a6b2b26e65f3aa0ec6e0df931b28488cb`  
		Last Modified: Thu, 11 Jun 2026 04:29:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dca1b9bee1ae63e14b92b984fbcdb1f020864ff89ce3dbb1e8a8e3d51c78297`  
		Last Modified: Thu, 11 Jun 2026 04:29:42 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d186dcc124dac0be9696d05505b77e2c10480051292fb57e3853cb7644191d`  
		Last Modified: Thu, 11 Jun 2026 04:29:43 GMT  
		Size: 6.1 KB (6095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca9f666d7465d4b7b130752f8b51331bbc84ea31ffa133b9696a1a7d4864454`  
		Last Modified: Thu, 11 Jun 2026 04:29:43 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:9a9eb2cec7adff0014f7243274003e5881aba9b9b33460a3f00ac70941d24417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5988224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc13c9186117760d1a836a4cf66670f4ae4cfba0d9317f32c5cd99fa1ba53e1`

```dockerfile
```

-	Layers:
	-	`sha256:b2b32d2323d75a6ab42881c0ba81b6d0d3aae5058a5d09280d204c1f840b2608`  
		Last Modified: Thu, 11 Jun 2026 04:29:42 GMT  
		Size: 5.9 MB (5934869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6df364b89f81257aff4cbb6b348f2aaf2c3a0f9ca63cc5dcb5b75d22d2e54e58`  
		Last Modified: Thu, 11 Jun 2026 04:29:42 GMT  
		Size: 53.4 KB (53355 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:d1ffcdeb35380f5042ade15e216ea273eb8f656b262b55eb06e6a07ac852c992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.4 MB (165380382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2933163a7de93e345dac2860dd7bed38747c4744cab7c9d36d8839c6c3591c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:59:24 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 11 Jun 2026 00:59:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:59:36 GMT
ENV GOSU_VERSION=1.19
# Thu, 11 Jun 2026 00:59:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 11 Jun 2026 00:59:40 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 11 Jun 2026 00:59:40 GMT
ENV LANG=en_US.utf8
# Thu, 11 Jun 2026 00:59:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:59:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Jun 2026 00:59:44 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:59:44 GMT
ENV PG_MAJOR=17
# Thu, 11 Jun 2026 00:59:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 11 Jun 2026 00:59:44 GMT
ENV PG_VERSION=17.10-1.pgdg12+1
# Thu, 11 Jun 2026 01:25:56 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 11 Jun 2026 01:25:56 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 11 Jun 2026 01:25:56 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 11 Jun 2026 01:25:56 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 11 Jun 2026 01:25:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 11 Jun 2026 01:25:57 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 11 Jun 2026 01:25:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 01:25:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 11 Jun 2026 01:25:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 01:25:57 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jun 2026 01:25:57 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 11 Jun 2026 01:25:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256856daca460d474058bbaaf343d95b94b242476ba57e5561c2dbaacc68a10a`  
		Last Modified: Thu, 11 Jun 2026 01:13:27 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46266781f1d701ec23814c9788269c80d9f4970404deb86715c84b6c4bee3f1`  
		Last Modified: Thu, 11 Jun 2026 01:13:27 GMT  
		Size: 4.4 MB (4391192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda1f03d35381a384dea45bf89b875c84b3d9d4991d21e99bd8ddba13b0d5744`  
		Last Modified: Thu, 11 Jun 2026 01:13:27 GMT  
		Size: 1.2 MB (1222855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbaa75644cbc9a3945799750334bb22cbca884cf974cda42884bee435fa58cd`  
		Last Modified: Thu, 11 Jun 2026 01:13:27 GMT  
		Size: 8.1 MB (8120747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9075d9e459ac2c125621db426e5e6fcf1de8076f016eb2f9b131e97c6be72cf`  
		Last Modified: Thu, 11 Jun 2026 01:13:28 GMT  
		Size: 1.1 MB (1097070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39bfb330678301b1cda4b0f6cd3f01c8977615ed437e8c1d53f573f50eeb3948`  
		Last Modified: Thu, 11 Jun 2026 01:13:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f72d2e2ef4b672169c21b1047ee515cbf365fe997aac5ade80f76e5033feed`  
		Last Modified: Thu, 11 Jun 2026 01:13:28 GMT  
		Size: 3.1 KB (3138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91de5509368fae52fb122696f73f01e1fc800b9dfa17ea10c428972a3d3899c`  
		Last Modified: Thu, 11 Jun 2026 01:26:30 GMT  
		Size: 123.6 MB (123633707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e1434b26fc17e1a11f31ea29f0375fd4ba195fb9c7247ade5aeca8b7ab6bc7`  
		Last Modified: Thu, 11 Jun 2026 01:26:28 GMT  
		Size: 10.3 KB (10301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e240e28691e287e55b5811cf0498d4bff2302dba9ea54980a74094926bcd78`  
		Last Modified: Thu, 11 Jun 2026 01:26:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bf45a810d06e815ebd29214ce580317d103e820d04116f3c68f3eefab0d0533`  
		Last Modified: Thu, 11 Jun 2026 01:26:28 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833f914ff445fac8f04336e3131cfa0bfeea16b942bbd3cb9ca537ba100d2c9c`  
		Last Modified: Thu, 11 Jun 2026 01:26:29 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e28878d0d321494d49b0e38ea31dd340955a22de7bb15843018946eb057dd4`  
		Last Modified: Thu, 11 Jun 2026 01:26:29 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:ed93de19970bd8ab7cff1b4e1d5a56ec9226dde7dca011371a38bae133377d94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5993745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f428c850441d517bed7be2057a69d0978bb4c47372cd604c6ecc4e558c6b4ad`

```dockerfile
```

-	Layers:
	-	`sha256:371ac0c7985c27196c317d260e754b87aa63a2c613a1161a7cf28a98982ad492`  
		Last Modified: Thu, 11 Jun 2026 01:26:28 GMT  
		Size: 5.9 MB (5940444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:985b740acaad4702079ca34edd3cccf1ea62376dcd04d309c5f84d22ef33a9de`  
		Last Modified: Thu, 11 Jun 2026 01:26:28 GMT  
		Size: 53.3 KB (53301 bytes)  
		MIME: application/vnd.in-toto+json
