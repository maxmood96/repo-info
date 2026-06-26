## `postgres:19beta1`

```console
$ docker pull postgres@sha256:a6bdd01b51b115f446a03135f9395575b3eb6ba90a92bfb692da82088f8820f8
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

### `postgres:19beta1` - linux; amd64

```console
$ docker pull postgres@sha256:7b1995b5d3f205e91c60f327e56d9a4434981ba2b041bdf3de9c06410f0af086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.6 MB (163642734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0df9a84bc4d9008b2b42b660e3ba280e36692826d74a829273a78b1c2a4b6616`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:32:15 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 24 Jun 2026 01:32:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:32:27 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 01:32:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 01:32:32 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 24 Jun 2026 01:32:32 GMT
ENV LANG=en_US.utf8
# Wed, 24 Jun 2026 01:32:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:32:35 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 24 Jun 2026 01:32:36 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 01:32:36 GMT
ENV PG_MAJOR=19
# Wed, 24 Jun 2026 01:32:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/19/bin
# Wed, 24 Jun 2026 01:32:36 GMT
ENV PG_VERSION=19~beta1-1.pgdg13+1
# Wed, 24 Jun 2026 01:32:56 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 24 Jun 2026 01:32:56 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 24 Jun 2026 01:32:56 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 24 Jun 2026 01:32:56 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Wed, 24 Jun 2026 01:32:56 GMT
VOLUME [/var/lib/postgresql]
# Wed, 24 Jun 2026 01:32:56 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:32:56 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 24 Jun 2026 01:32:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:32:56 GMT
STOPSIGNAL SIGINT
# Wed, 24 Jun 2026 01:32:56 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 24 Jun 2026 01:32:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed599bc3be5829e62ca3077b7500de5ffd073d329b534028976e3a936e81e8e2`  
		Last Modified: Wed, 24 Jun 2026 01:33:16 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913eb393276d1b3c50690397810bfb6c3ad86e2621ae5cce3e9809d244cc006f`  
		Last Modified: Wed, 24 Jun 2026 01:33:16 GMT  
		Size: 6.4 MB (6443045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd94f0e6a9bcd580f46dfa54b5d5b3579f01467df01f6c96f983445d90895b48`  
		Last Modified: Wed, 24 Jun 2026 01:33:16 GMT  
		Size: 1.3 MB (1256761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faaa0bd3524f08e52ac1a0df1a86832e451a21f6a17febf00655d6db3318ba8d`  
		Last Modified: Wed, 24 Jun 2026 01:33:17 GMT  
		Size: 8.2 MB (8203916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2360cdced1c8f395b82ec32c67692ffaa960c66e2844401c5dc3c08feb1222`  
		Last Modified: Wed, 24 Jun 2026 01:33:18 GMT  
		Size: 1.3 MB (1311643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d664b3bb2bbcfcffad7bf44ef8fc43eef993bea2e1625cfc328b0e68edac53`  
		Last Modified: Wed, 24 Jun 2026 01:33:18 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:854223614a48fbad425017a7e2993245664fb74e0667465c513d081666841358`  
		Last Modified: Wed, 24 Jun 2026 01:33:18 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce7511ca8cc43b2a9649f60582f9b696a6715d0a6035bf16de5dacc54a6154d`  
		Last Modified: Wed, 24 Jun 2026 01:33:21 GMT  
		Size: 116.6 MB (116609702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853f01c0d61862bc6c853c2fcb260b104cee7546a2b72dd70e41c0a1213bba44`  
		Last Modified: Wed, 24 Jun 2026 01:33:19 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfcc527f1c3aa72eee4a6fa045b8d9e72026ff1bd8832559213a98e1231de4db`  
		Last Modified: Wed, 24 Jun 2026 01:33:19 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:446e5e357cf148f5ceb746f445fcadfb6fd506d3c0fb0a608d109383f1235dfc`  
		Last Modified: Wed, 24 Jun 2026 01:33:20 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb431b480bf1f5af7d9a89b1f133a263c805dae855b32aaf153bd4fca096937`  
		Last Modified: Wed, 24 Jun 2026 01:33:21 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1` - unknown; unknown

```console
$ docker pull postgres@sha256:659686ca397f62d47be5eddd690c9858597d6f0a44913529fb8aa4880b3d3937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6049169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3371ea3035c77407307015e2b8a96844ecc3c4eeaf9a61c3b501003c7c8a2b92`

```dockerfile
```

-	Layers:
	-	`sha256:3aaf4cf96d7bee38ab5a92ce63fcc8448687949a4da6b2e84c7fc6a490a0a418`  
		Last Modified: Wed, 24 Jun 2026 01:33:17 GMT  
		Size: 6.0 MB (5997885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c97529c3193d5cf9a23d962dee5a97fc5b9e7e614bad1f786a737c33f86bc262`  
		Last Modified: Wed, 24 Jun 2026 01:33:16 GMT  
		Size: 51.3 KB (51284 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1` - linux; arm variant v5

```console
$ docker pull postgres@sha256:b89eda3df0483585239f369f4c637571df14835461e0dca923830972ffcac567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92008547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dd88b81fbbda871fd4c64283e7fb651f1cca2f48325afcb515970d30ced79f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:41:35 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 24 Jun 2026 01:41:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:41:54 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 01:41:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 01:42:02 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 24 Jun 2026 01:42:02 GMT
ENV LANG=en_US.utf8
# Wed, 24 Jun 2026 01:42:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:09 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 24 Jun 2026 01:42:10 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 01:42:10 GMT
ENV PG_MAJOR=19
# Wed, 24 Jun 2026 01:42:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/19/bin
# Wed, 24 Jun 2026 01:42:10 GMT
ENV PG_VERSION=19~beta1-1.pgdg13+1
# Wed, 24 Jun 2026 01:55:39 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 24 Jun 2026 01:55:39 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 24 Jun 2026 01:55:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 24 Jun 2026 01:55:39 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Wed, 24 Jun 2026 01:55:39 GMT
VOLUME [/var/lib/postgresql]
# Wed, 24 Jun 2026 01:55:39 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:55:39 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 24 Jun 2026 01:55:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:55:39 GMT
STOPSIGNAL SIGINT
# Wed, 24 Jun 2026 01:55:39 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 24 Jun 2026 01:55:39 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:da43bc6a07a9cd7cc23faa538adc0797482747316b5a85b9f3f94ed17f6c1a2a`  
		Last Modified: Wed, 24 Jun 2026 00:28:12 GMT  
		Size: 28.0 MB (27959221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e27174a4d38e510084e2ad0fe6a035632b117140a586e9a8fab621e6f122969`  
		Last Modified: Wed, 24 Jun 2026 01:55:52 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d19e2ac4d4f4819e1babd0a15d0cf069f813c9d89964cb57927bcf370031f4`  
		Last Modified: Wed, 24 Jun 2026 01:55:52 GMT  
		Size: 5.9 MB (5932373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e751ac5b8688bda6eee88da7eab2b90a70f1fed68933fd23c6af2c5b10ee014`  
		Last Modified: Wed, 24 Jun 2026 01:55:52 GMT  
		Size: 1.2 MB (1227517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04259096cd05e1c061fd5510b2b5cd57fc2aa597f40af5f6d005bdf2cb9bc88`  
		Last Modified: Wed, 24 Jun 2026 01:55:52 GMT  
		Size: 8.2 MB (8204329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582c958ffa663e0a4a6c43dc9f65c300104e86194d344d52089c6ee5652788f8`  
		Last Modified: Wed, 24 Jun 2026 01:55:53 GMT  
		Size: 1.3 MB (1317331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9f04198776d57de3babe926c1099641d243426666655b12395640287d10877`  
		Last Modified: Wed, 24 Jun 2026 01:55:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27dd71b98044c9ecaa3efc144a0e304c8002cc2a1c63d06acbdbccc48add242c`  
		Last Modified: Wed, 24 Jun 2026 01:55:53 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d76adada2e485d9800cb1d583317f60cdb76435e7cd0636698b8ec292d967d`  
		Last Modified: Wed, 24 Jun 2026 01:55:55 GMT  
		Size: 47.3 MB (47335526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83493e786a84c2eb2d2ea45138279490d5058ed932bfbbcafdc9d9ebb222884`  
		Last Modified: Wed, 24 Jun 2026 01:55:54 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4671fa17ac4a345afac51ee5f9955ac43f393a6e7b552cc22a93522dcab0449`  
		Last Modified: Wed, 24 Jun 2026 01:55:54 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb645620673100e8a1601c87b31e68a487dc408cb72237568841d7b6622ab37`  
		Last Modified: Wed, 24 Jun 2026 01:55:55 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d49df2b2bd37cb342a26f7fb8971fc5b948a6b4abc1e0f6fd848ac3c610464`  
		Last Modified: Wed, 24 Jun 2026 01:55:56 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1` - unknown; unknown

```console
$ docker pull postgres@sha256:8eac34751ede00b744325c95810b2f635131635d7125a08006df79c8794ba568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5179601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a04c2a662f8ad330a59a2d5f997675ab7e20bd8cd2498f7580b91bef352274d`

```dockerfile
```

-	Layers:
	-	`sha256:325a5a7cd90c6e23af8bbb7fb3195b069acaaaf077935b978593164d305733ac`  
		Last Modified: Wed, 24 Jun 2026 01:55:52 GMT  
		Size: 5.1 MB (5128129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2c8ed5a9b5f3ea3ef2c8057bb74da5a1953710405a748327b9b11f04137f17d`  
		Last Modified: Wed, 24 Jun 2026 01:55:52 GMT  
		Size: 51.5 KB (51472 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1` - linux; arm variant v7

```console
$ docker pull postgres@sha256:a023e8301caa5962bdce22ffa7bcb47e6d2da1300813bb016c2106cf1e386590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88282269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:880ef0021baadaa23bcf8890493d0f46fc16db8d6c6f4f591f97f618d8220030`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:44:30 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 24 Jun 2026 01:44:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:44:45 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 01:44:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 01:44:52 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 24 Jun 2026 01:44:52 GMT
ENV LANG=en_US.utf8
# Wed, 24 Jun 2026 01:44:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:44:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 24 Jun 2026 01:44:58 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 01:44:58 GMT
ENV PG_MAJOR=19
# Wed, 24 Jun 2026 01:44:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/19/bin
# Wed, 24 Jun 2026 01:44:58 GMT
ENV PG_VERSION=19~beta1-1.pgdg13+1
# Wed, 24 Jun 2026 01:57:16 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 24 Jun 2026 01:57:16 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 24 Jun 2026 01:57:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 24 Jun 2026 01:57:16 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Wed, 24 Jun 2026 01:57:16 GMT
VOLUME [/var/lib/postgresql]
# Wed, 24 Jun 2026 01:57:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:57:16 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 24 Jun 2026 01:57:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:57:16 GMT
STOPSIGNAL SIGINT
# Wed, 24 Jun 2026 01:57:16 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 24 Jun 2026 01:57:16 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:81c84b0273952340067af970e1fe77a42ea83b4ed1a53319e258d5f1077848f0`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 26.2 MB (26211051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da25d34c7dad73e043ac25d3b2e8b2c4e8aa6dca41c89fbc323eb0e9d6e0145c`  
		Last Modified: Wed, 24 Jun 2026 01:57:28 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c81f2a4257636c6917a312280fc456884e23becb9db66442e8608e0ccebdc9`  
		Last Modified: Wed, 24 Jun 2026 01:57:29 GMT  
		Size: 5.5 MB (5497337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc8b7f215fd43a214aa6eebf8e134cfcd6a19c89ecfde1226c0815089c31606`  
		Last Modified: Wed, 24 Jun 2026 01:57:28 GMT  
		Size: 1.2 MB (1222426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11cb9f29157a2b09ffbbb7b60a1c26a7b72e0c6a1a95b5da4f43b86194427d3`  
		Last Modified: Wed, 24 Jun 2026 01:57:29 GMT  
		Size: 8.2 MB (8204070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b058a1db6185ab24361928196d2b663450d3b5c5a0a66544d11ad6ed66605d56`  
		Last Modified: Wed, 24 Jun 2026 01:57:29 GMT  
		Size: 1.2 MB (1172637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9159e9af82782c5c5d9a3bb7eeb5e03a8e157727af05792931c43c8c39937f4`  
		Last Modified: Wed, 24 Jun 2026 01:57:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a380848034e93202cec3c7689a2a81c470e0fa98d75df0bf05f10e5ba502a79c`  
		Last Modified: Wed, 24 Jun 2026 01:57:30 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853ff66b1d7d8d6092ee9e5e76a8362191479641ff2fd914b1252b34ee839145`  
		Last Modified: Wed, 24 Jun 2026 01:57:31 GMT  
		Size: 45.9 MB (45942478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04993bea28d9028bc30feadb86bd55ebfa5dd668044da1c78819cd2b51a32859`  
		Last Modified: Wed, 24 Jun 2026 01:57:31 GMT  
		Size: 21.4 KB (21432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954fde3af89f9ed2968a6cbae48af6e155773286106b8cb9f839e9a8e451d125`  
		Last Modified: Wed, 24 Jun 2026 01:57:31 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380de6e4606481d3046cd93041b904276c1174633beb65ac84fcb28f767c8e6b`  
		Last Modified: Wed, 24 Jun 2026 01:57:32 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718109e124dca3844a746be5d1bdb8c03c68b01418ac60f44f82f55f62c1ab77`  
		Last Modified: Wed, 24 Jun 2026 01:57:32 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1` - unknown; unknown

```console
$ docker pull postgres@sha256:4d63f8a2fe8e56a6d7f418603015409fcc22e96020130df00d54c6e27b252bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5178907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aad247a1d60ee52f4af164e3504b62d02fc76561a5e1a2e376fd7d881ecc194`

```dockerfile
```

-	Layers:
	-	`sha256:5c018931043eea49006859fc9c235847b75f8ef5573cbd7bdb128ccc82910721`  
		Last Modified: Wed, 24 Jun 2026 01:57:29 GMT  
		Size: 5.1 MB (5127434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b12bf7c6d8a67b104511c343bac5a4c45cb307ec2364b82faae5d1eb54b39d6`  
		Last Modified: Wed, 24 Jun 2026 01:57:28 GMT  
		Size: 51.5 KB (51473 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:6851a292aa5445526c7d4f1340a53858dd093c5e13e42b21778d398aa666cce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.2 MB (162206670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d35b55dca02f157e53402f1822463f739f8fc587a0dac578e0bd63ec7f412a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:34:33 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 24 Jun 2026 01:34:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:34:46 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 01:34:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 01:34:51 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 24 Jun 2026 01:34:51 GMT
ENV LANG=en_US.utf8
# Wed, 24 Jun 2026 01:34:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:34:55 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 24 Jun 2026 01:34:55 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 01:34:55 GMT
ENV PG_MAJOR=19
# Wed, 24 Jun 2026 01:34:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/19/bin
# Wed, 24 Jun 2026 01:34:55 GMT
ENV PG_VERSION=19~beta1-1.pgdg13+1
# Wed, 24 Jun 2026 01:35:18 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 24 Jun 2026 01:35:18 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 24 Jun 2026 01:35:18 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 24 Jun 2026 01:35:18 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Wed, 24 Jun 2026 01:35:18 GMT
VOLUME [/var/lib/postgresql]
# Wed, 24 Jun 2026 01:35:18 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:35:18 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 24 Jun 2026 01:35:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:35:18 GMT
STOPSIGNAL SIGINT
# Wed, 24 Jun 2026 01:35:18 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 24 Jun 2026 01:35:18 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984fde83aabd68afa22e905d25a6089a433fae9fa6bb22a294280f74cd47bde5`  
		Last Modified: Wed, 24 Jun 2026 01:35:38 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7811ac9c53626821d5efdab21e9feb9a897d9886e008bc44c0530dc19d158c55`  
		Last Modified: Wed, 24 Jun 2026 01:35:39 GMT  
		Size: 6.2 MB (6235088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02469ff3041d518ea56a335104c2c52a8b1fbc36d29a226fbd0b040a35a21ab9`  
		Last Modified: Wed, 24 Jun 2026 01:35:38 GMT  
		Size: 1.2 MB (1209605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3641aa2c0bf3bbc7d4689c8698f8b5405e15e1f2b26436367245913d5b290032`  
		Last Modified: Wed, 24 Jun 2026 01:35:38 GMT  
		Size: 8.2 MB (8204026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f2d8f08e720f7f3c246aa20e1b6697057bc67007accdc7cb3cd09aafc70555`  
		Last Modified: Wed, 24 Jun 2026 01:35:40 GMT  
		Size: 1.2 MB (1220586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71fdb1fc8bc8b198f642d5d86a64e39ac2686cf0c11831a2e12728f1757fa0ab`  
		Last Modified: Wed, 24 Jun 2026 01:35:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36c7db37db274fc63aa3cd0370be584072a18eb63cd8e5ca2d90ac83732755c`  
		Last Modified: Wed, 24 Jun 2026 01:35:40 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbea82ac897a6a16b434f24e8769a8d87f46842fc8c5820b1e6986b5c03f9da2`  
		Last Modified: Wed, 24 Jun 2026 01:35:43 GMT  
		Size: 115.2 MB (115156565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa6d391aee0297b718fdecc9b5f1db74a5f769f2b7b5f69f68c384d4fdc43c0`  
		Last Modified: Wed, 24 Jun 2026 01:35:41 GMT  
		Size: 21.4 KB (21417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ddff54e52bf205a15572195394058226cf72876d4bf50d1b27c59435f775c3`  
		Last Modified: Wed, 24 Jun 2026 01:35:41 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74048b48db4582adcbcb9954a3cca29454325afbadf2b610ae4b06b87e704ebb`  
		Last Modified: Wed, 24 Jun 2026 01:35:42 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b22c585c5b218679c583be2cbb5325e38c349f9fc9059eaf292862f47360f3f`  
		Last Modified: Wed, 24 Jun 2026 01:35:42 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1` - unknown; unknown

```console
$ docker pull postgres@sha256:3baa246bb3a9c40d5e7910bbfb2963b749d8470f61ae62eaf175715bbb74fb86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6055715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:231893db1652158da561a8b7d0d69df5190136ab6dee280f2431bfca9eb6f1cc`

```dockerfile
```

-	Layers:
	-	`sha256:739ee80944f70f72258b743cb4ce7606a396e2e0172d0c91df768a3953ebb675`  
		Last Modified: Wed, 24 Jun 2026 01:35:39 GMT  
		Size: 6.0 MB (6004202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0e4fcc86969936b1ad066a7826cc1383701cc1978b5647e546449cf56a7ced3`  
		Last Modified: Wed, 24 Jun 2026 01:35:38 GMT  
		Size: 51.5 KB (51513 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1` - linux; 386

```console
$ docker pull postgres@sha256:d4f3537d01345aa29e7df788c632ede8f6085bea8a41eba0140fedbb1169142c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.2 MB (98195975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb30e9745dbe4bc4780fdbec289d2845555c0d1dbd7dee72e9bde59e821dcc1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:29:14 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 24 Jun 2026 01:29:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:29:27 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 01:29:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 01:29:33 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 24 Jun 2026 01:29:33 GMT
ENV LANG=en_US.utf8
# Wed, 24 Jun 2026 01:29:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:29:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 24 Jun 2026 01:29:37 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 01:29:37 GMT
ENV PG_MAJOR=19
# Wed, 24 Jun 2026 01:29:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/19/bin
# Wed, 24 Jun 2026 01:29:37 GMT
ENV PG_VERSION=19~beta1-1.pgdg13+1
# Wed, 24 Jun 2026 01:39:35 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 24 Jun 2026 01:39:36 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 24 Jun 2026 01:39:36 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 24 Jun 2026 01:39:36 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Wed, 24 Jun 2026 01:39:36 GMT
VOLUME [/var/lib/postgresql]
# Wed, 24 Jun 2026 01:39:36 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:39:36 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 24 Jun 2026 01:39:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:39:36 GMT
STOPSIGNAL SIGINT
# Wed, 24 Jun 2026 01:39:36 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 24 Jun 2026 01:39:36 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:984d3baa100eb8c4d7c83b7c23b4748e508aa6ed5903297f02be90a681f52d41`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 31.3 MB (31301210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4260f448a888e93f9fdc3b5b03335266232ad5c64ccc6fa48b74159d68542798`  
		Last Modified: Wed, 24 Jun 2026 01:39:48 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb632dfe3e7df245c2ecf699e7e11eaad2bb2147ffe61dcc148f4a36f9d605a`  
		Last Modified: Wed, 24 Jun 2026 01:39:49 GMT  
		Size: 6.6 MB (6631403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216bdfda595de3fcc3a8a9992a57537d09c8d88ecaf46db36faea992bff1996b`  
		Last Modified: Wed, 24 Jun 2026 01:39:48 GMT  
		Size: 1.2 MB (1225821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad88560201f77a0cc468a69e50f30eef14ae6844d628351eff8c4986bbfc10d2`  
		Last Modified: Wed, 24 Jun 2026 01:39:49 GMT  
		Size: 8.2 MB (8204104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d7a510e7ba01f41ba9311318f9c0d4ed4fba6a5dde06d21cee6a1b2adc210a`  
		Last Modified: Wed, 24 Jun 2026 01:39:50 GMT  
		Size: 1.3 MB (1308296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58bee90281d813e4125a19b916ff28e9ae08d70feec4288402bc0778fabae964`  
		Last Modified: Wed, 24 Jun 2026 01:39:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd96a6c7a4d2173e67b1515edc4ffeb53e68d7076ab7c98296b1e44dae080b2`  
		Last Modified: Wed, 24 Jun 2026 01:39:50 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5546302f04e1c1212a91dfe0f3117eacaec0ebafa052d854f4673ef62b55bf21`  
		Last Modified: Wed, 24 Jun 2026 01:39:53 GMT  
		Size: 49.5 MB (49492890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b96f90aff769041ba2c2a3786afd8fbd0d8f899a91a3d4a246ec66631ea507e`  
		Last Modified: Wed, 24 Jun 2026 01:39:51 GMT  
		Size: 21.4 KB (21418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2227b1596116bb014711cb21eb09e64e7eb13a50a1ece5a15df0f5e819151c5b`  
		Last Modified: Wed, 24 Jun 2026 01:39:51 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46035fb9d16bc136e4449d04d08aa8e63c0046474bd35b1a77b97e1fc84c793c`  
		Last Modified: Wed, 24 Jun 2026 01:39:51 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f1695589ea6ecbea182b27b5a6084fd40a5a5afd43c2b619cef5c05bf89cdd`  
		Last Modified: Wed, 24 Jun 2026 01:39:52 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1` - unknown; unknown

```console
$ docker pull postgres@sha256:ab2e92164861dcd4835e87399f71611f555940cbf37c2dfb9368139be1006233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5174751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f2d8416fb422bb8abb4c2b0dcf1c88c9e32144b0ccf06faa604681aefdabc8d`

```dockerfile
```

-	Layers:
	-	`sha256:e537594e755216234acad642fb4d85c4a82bcacce9c61ed78d7aa953b4d9ad8e`  
		Last Modified: Wed, 24 Jun 2026 01:39:49 GMT  
		Size: 5.1 MB (5123514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:822cb8ef751894aad688c3e492930ac24911cdb031d4e65ab431fb83a9477443`  
		Last Modified: Wed, 24 Jun 2026 01:39:48 GMT  
		Size: 51.2 KB (51237 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1` - linux; ppc64le

```console
$ docker pull postgres@sha256:cc2ffefe2d2f0a051734ae92e02991b0d6b2b17b2b71d02e1a8f870e9274cc75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176125933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8946fc7c24c5da420e02533664b429cf144685045c222426dd7d3716be98e57`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 03:02:27 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 24 Jun 2026 03:02:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 03:02:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 03:02:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 03:03:05 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 24 Jun 2026 03:03:05 GMT
ENV LANG=en_US.utf8
# Wed, 24 Jun 2026 03:03:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 03:03:19 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 24 Jun 2026 03:03:21 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 03:03:21 GMT
ENV PG_MAJOR=19
# Wed, 24 Jun 2026 03:03:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/19/bin
# Wed, 24 Jun 2026 03:03:21 GMT
ENV PG_VERSION=19~beta1-1.pgdg13+1
# Wed, 24 Jun 2026 03:04:03 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 24 Jun 2026 03:04:04 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 24 Jun 2026 03:04:04 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 24 Jun 2026 03:04:04 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Wed, 24 Jun 2026 03:04:04 GMT
VOLUME [/var/lib/postgresql]
# Wed, 24 Jun 2026 03:04:04 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 03:04:05 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 24 Jun 2026 03:04:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 03:04:05 GMT
STOPSIGNAL SIGINT
# Wed, 24 Jun 2026 03:04:05 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 24 Jun 2026 03:04:05 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:639e1c13483ea279c94219be2736856262d8dd2efeff3e6d309f11a66aba21fb`  
		Last Modified: Wed, 24 Jun 2026 00:30:29 GMT  
		Size: 33.6 MB (33606388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986ec99518a807bfad5f7f46ab0d7169e6bb8464c56530a6857da4833bcf42a0`  
		Last Modified: Wed, 24 Jun 2026 03:04:48 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b235d4ec390c403864dac84f73f8717b274ee67ad58efd50aa20676e32950ab`  
		Last Modified: Wed, 24 Jun 2026 03:04:49 GMT  
		Size: 7.1 MB (7076761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097461e8a5ef2da1a84e8b66d0907cb5d87f6f558b864dbccab0f456fe833694`  
		Last Modified: Wed, 24 Jun 2026 03:04:48 GMT  
		Size: 1.2 MB (1214756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38e02605252f06f6ad4fd846fa34fd2c8bfce121536074a31620b544092b0a1`  
		Last Modified: Wed, 24 Jun 2026 03:04:49 GMT  
		Size: 8.2 MB (8204060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5c026a4459463a6e5145ad624a4164b37786a4e4dd7bf9759e4e855d64bcc3`  
		Last Modified: Wed, 24 Jun 2026 03:04:50 GMT  
		Size: 1.4 MB (1394880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566c45b1c57ad093b48578c726e36fc3978d088b4357bba48905f926320f23c0`  
		Last Modified: Wed, 24 Jun 2026 03:04:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2db7823b7c0860e15b3f9662e8a0370ef70f939cbbb9d59e62f37739e85d1cc`  
		Last Modified: Wed, 24 Jun 2026 03:04:51 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4136eb6a9fcf392517d5b671c7d4a9251b054b493b461511a926f52df2f78ef`  
		Last Modified: Wed, 24 Jun 2026 03:04:53 GMT  
		Size: 124.6 MB (124596847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4bfba71207612e3e1587d98bd7e32b516dabbe4535505bece5139dd6863685`  
		Last Modified: Wed, 24 Jun 2026 03:04:51 GMT  
		Size: 21.4 KB (21409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964eb404ea94378306a88c98b48324768cd16b7394c4f9c8dc72e68d43b35985`  
		Last Modified: Wed, 24 Jun 2026 03:04:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606db1a88294c74e4917b0b4cce1bedc7f74de9af623542572cd88a9427487fb`  
		Last Modified: Wed, 24 Jun 2026 03:04:52 GMT  
		Size: 6.1 KB (6092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0eb1bb3d9a238f225042b9097083fc63f3bf5d822287899b3b7f128abb6d0d`  
		Last Modified: Wed, 24 Jun 2026 03:04:53 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1` - unknown; unknown

```console
$ docker pull postgres@sha256:f6fd7e518fb0c10e6f7e4e8ea5c36c5e69157c322f95ab567a4c238fe82173ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6055845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa001cceefd69b85c5d0633e94fb63a5a8c757da0d41ab688ce323fcaf7a9d7d`

```dockerfile
```

-	Layers:
	-	`sha256:ccaa99f963af70f1731a62c9b19e5384af0f551a497ed5565f9ae8fe54744a47`  
		Last Modified: Wed, 24 Jun 2026 03:04:49 GMT  
		Size: 6.0 MB (6004509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667f61d1c00c89372477ef612851e97044ba1bdbdefca771842c9a2328d3d575`  
		Last Modified: Wed, 24 Jun 2026 03:04:49 GMT  
		Size: 51.3 KB (51336 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1` - linux; riscv64

```console
$ docker pull postgres@sha256:48e07a88a265a6865aadcdf2b0d0a4a05b02a7b3926b4c23a129d03d6bd89a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93378292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f500a6f6a162d776049b03fb8731064aafeb33076e9c66a545efaaa20faec5d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1782172800'
# Thu, 25 Jun 2026 17:20:07 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 25 Jun 2026 17:21:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jun 2026 17:22:04 GMT
ENV GOSU_VERSION=1.19
# Thu, 25 Jun 2026 17:22:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 25 Jun 2026 17:23:05 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 25 Jun 2026 17:23:05 GMT
ENV LANG=en_US.utf8
# Thu, 25 Jun 2026 17:23:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jun 2026 17:23:47 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Jun 2026 17:23:49 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 25 Jun 2026 17:23:49 GMT
ENV PG_MAJOR=19
# Thu, 25 Jun 2026 17:23:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/19/bin
# Thu, 25 Jun 2026 17:23:49 GMT
ENV PG_VERSION=19~beta1-1.pgdg13+1
# Fri, 26 Jun 2026 19:23:49 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 26 Jun 2026 19:23:50 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 26 Jun 2026 19:23:51 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 26 Jun 2026 19:23:51 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Fri, 26 Jun 2026 19:23:51 GMT
VOLUME [/var/lib/postgresql]
# Fri, 26 Jun 2026 19:23:51 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 26 Jun 2026 19:23:51 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 26 Jun 2026 19:23:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Jun 2026 19:23:51 GMT
STOPSIGNAL SIGINT
# Fri, 26 Jun 2026 19:23:51 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 26 Jun 2026 19:23:51 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:58bface994ba631e609596a2ca5032d9d75de27f1b6476034b581e226205adab`  
		Last Modified: Wed, 24 Jun 2026 03:41:42 GMT  
		Size: 28.3 MB (28282378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6adbcc74bc464c350395b0ed6c1768df2fe221b068feb6158693ad4ec07cd00e`  
		Last Modified: Fri, 26 Jun 2026 19:26:26 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d34ed43918633e51bd4b0dfe515e8421bf7b4d99c7a97135953368b017f8e34f`  
		Last Modified: Fri, 26 Jun 2026 19:26:28 GMT  
		Size: 6.3 MB (6293016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75577e804f36a67f7f9edf858af5711ac30d48485a836696cb03b019ecd36ac3`  
		Last Modified: Fri, 26 Jun 2026 19:26:26 GMT  
		Size: 1.2 MB (1202088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7531413cc31124ad057b4194a1eb2086a683b6b4d169970cf67852cdf74c7eb`  
		Last Modified: Fri, 26 Jun 2026 19:26:29 GMT  
		Size: 8.2 MB (8203759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f9b21c12f76de08f6c105f2b2e8ba8d94e03c0a18063b3314a7d36fd79db64`  
		Last Modified: Fri, 26 Jun 2026 19:26:28 GMT  
		Size: 1.4 MB (1402395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f5cd849b9c5cab9341c5d47ce0147c065a4a959e62f1844d1fa79d44437dd3`  
		Last Modified: Fri, 26 Jun 2026 19:26:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4834cab7a2c6eca063fcf59846c4f1194e5de56dcc92340991a3bbb7949a5b83`  
		Last Modified: Fri, 26 Jun 2026 19:26:30 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4cdf0e35046a8eb3579b9848c559d612f0c84711b807b551fd2378da067d1f2`  
		Last Modified: Fri, 26 Jun 2026 19:26:37 GMT  
		Size: 48.0 MB (47962384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8552d27ef9375c09a6e6b28d5129556feaa048c3233af330d9ea24f660c2d748`  
		Last Modified: Fri, 26 Jun 2026 19:26:30 GMT  
		Size: 21.4 KB (21428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d855a8015c757d4d7b65bbee453c7c39dddca948abd6b2c2ddba4c9a16e9142a`  
		Last Modified: Fri, 26 Jun 2026 19:26:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc53fdc51b744bbed27eda974dfe583a401128abb1139c89776848f265cf6e67`  
		Last Modified: Fri, 26 Jun 2026 19:26:31 GMT  
		Size: 6.1 KB (6101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17fff3b4a893ff4157428fb161c8dacbb824f561b91cf7a611df38db1d5b2918`  
		Last Modified: Fri, 26 Jun 2026 19:26:31 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1` - unknown; unknown

```console
$ docker pull postgres@sha256:e9f5f31e7cfb4d3b0c4df63c4c1ee8997a32dd42e31ddcc25e5567d73a42b5ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5169739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac0f31bbb11d750ed19f0da0441b3415d89db0655a69570d9522da31a7572d81`

```dockerfile
```

-	Layers:
	-	`sha256:47f097ab407a1a982223a44d5c7456238d9cf3bb55d129a59b9fc4a71150f93c`  
		Last Modified: Fri, 26 Jun 2026 19:26:28 GMT  
		Size: 5.1 MB (5118410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c86575780f2d5030bc66e085276f7c27c58c55b5b596dba79a7d20ecb58068ab`  
		Last Modified: Fri, 26 Jun 2026 19:26:25 GMT  
		Size: 51.3 KB (51329 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1` - linux; s390x

```console
$ docker pull postgres@sha256:9f0c185864327670239e39ad7a1a891eb49f1940f6239c9cc63ab0c471174ab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.3 MB (178325215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa0ff3f7331c703ea2a8f6999bb08f150864ac5047780811101a966efcaa802`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:57:59 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 24 Jun 2026 01:58:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:58:12 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 01:58:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 01:58:19 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 24 Jun 2026 01:58:19 GMT
ENV LANG=en_US.utf8
# Wed, 24 Jun 2026 01:58:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:58:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 24 Jun 2026 01:58:24 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 01:58:24 GMT
ENV PG_MAJOR=19
# Wed, 24 Jun 2026 01:58:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/19/bin
# Wed, 24 Jun 2026 01:58:24 GMT
ENV PG_VERSION=19~beta1-1.pgdg13+1
# Wed, 24 Jun 2026 02:12:38 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 24 Jun 2026 02:12:38 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 24 Jun 2026 02:12:38 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 24 Jun 2026 02:12:38 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Wed, 24 Jun 2026 02:12:38 GMT
VOLUME [/var/lib/postgresql]
# Wed, 24 Jun 2026 02:12:38 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:12:38 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 24 Jun 2026 02:12:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:12:38 GMT
STOPSIGNAL SIGINT
# Wed, 24 Jun 2026 02:12:38 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 24 Jun 2026 02:12:38 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b6a0af2ceb4b698210b8776157288a3fb06e46aaf75d641139449fcc50ce430d`  
		Last Modified: Wed, 24 Jun 2026 00:28:43 GMT  
		Size: 29.9 MB (29851381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f8b3edc75b49ced11dab27f4148cad3479e0ca4d1bef3a3372749607386048`  
		Last Modified: Wed, 24 Jun 2026 02:13:10 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9af1a36d970a9aa144153569a33418a335c9f9fa39e21a0cc4822586b42480`  
		Last Modified: Wed, 24 Jun 2026 02:13:11 GMT  
		Size: 6.4 MB (6408505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67240597dd615f7661bbea5c29258b345c44ac1ab6bb6353553953f634b3b31c`  
		Last Modified: Wed, 24 Jun 2026 02:13:10 GMT  
		Size: 1.2 MB (1230274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe0ebce0cd5e64ec821f7bc63f955b565a014c44a3e15ddbf8fb5de3b298b72`  
		Last Modified: Wed, 24 Jun 2026 02:13:11 GMT  
		Size: 8.3 MB (8258957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b62f6fa5bb2b55a8c5023e16a41664043d46f4d418a482eb291c58f249ad3f7`  
		Last Modified: Wed, 24 Jun 2026 02:13:12 GMT  
		Size: 1.4 MB (1398189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e3b23c8c098994d89f5ec00fd029fe0265f484d55050145dd15dc6dc11ad6d`  
		Last Modified: Wed, 24 Jun 2026 02:13:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5a3c3534096eaaed44cd33e5dc26c06d3585042dbe09953547256135f24b66`  
		Last Modified: Wed, 24 Jun 2026 02:13:12 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63e8fcb745b23841ae589af259dfd965533a2e1955fcb8178f7b3d696c30ead`  
		Last Modified: Wed, 24 Jun 2026 02:13:15 GMT  
		Size: 131.1 MB (131145644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73228b3594d9b53bab861d17b94d3fbf67ba8de72931de694a52e4725f16e329`  
		Last Modified: Wed, 24 Jun 2026 02:13:13 GMT  
		Size: 21.4 KB (21424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9e58745f29c9129e10960b0aed0f11fc5f89cdf7cfb81f14d82846ab79229e`  
		Last Modified: Wed, 24 Jun 2026 02:13:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceea84a81a7612bbfad943f6a8e10dea5ea8e72e54a58515242f5417a34e65d4`  
		Last Modified: Wed, 24 Jun 2026 02:13:13 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5265ffa140974a80343cbc0f406a1f0e0c009e7b325cfe99fb368ad83c86a1`  
		Last Modified: Wed, 24 Jun 2026 02:13:14 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1` - unknown; unknown

```console
$ docker pull postgres@sha256:af3986f663fdbd44d85b54e4c200b38c15495fb510ccdb06d7dcfc7d90ff00e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6065839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a951dc05cac117605c35cf1c9268462e3e20152ed70845012a48f5d2a5efd31`

```dockerfile
```

-	Layers:
	-	`sha256:3a882dcc3c3ca4b71f7faa7c2d721f2b444add5fbd75ecc0fd0a58ba0acd52ac`  
		Last Modified: Wed, 24 Jun 2026 02:13:11 GMT  
		Size: 6.0 MB (6014555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eb51d1e246cc38278ba57b13aa6d6815fb2c9d6c28a6113ab91a5966d0d6deb`  
		Last Modified: Wed, 24 Jun 2026 02:13:10 GMT  
		Size: 51.3 KB (51284 bytes)  
		MIME: application/vnd.in-toto+json
