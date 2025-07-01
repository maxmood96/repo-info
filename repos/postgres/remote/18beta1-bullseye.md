## `postgres:18beta1-bullseye`

```console
$ docker pull postgres@sha256:5d48acb92784cccf6a88c664f728b4a6a07848ef641c2f9c9ca1a9d2deeb773b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `postgres:18beta1-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:4de77ecf85c467caf6dcf960656adb8dc11b97da91b51684c6077aede1e92acc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149416932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c65c4f821020eeb34f9f459ed40f160409e79db48c38ce112f5e144344699edd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 09 Jun 2025 21:23:06 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV GOSU_VERSION=1.17
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV LANG=en_US.utf8
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PG_MAJOR=18
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PG_VERSION=18~beta1-1.pgdg110+1
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 09 Jun 2025 21:23:06 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
VOLUME [/var/lib/postgresql]
# Mon, 09 Jun 2025 21:23:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jun 2025 21:23:06 GMT
STOPSIGNAL SIGINT
# Mon, 09 Jun 2025 21:23:06 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 09 Jun 2025 21:23:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd9497ecd1f83b4e6acb6672c0a0f4076c2dc91cbfd7a2a15a8150f29e6ef54`  
		Last Modified: Tue, 01 Jul 2025 02:22:02 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c162a114cb32615da09de325511213aec79998a596dfbb85889eb4b522a15dac`  
		Last Modified: Tue, 01 Jul 2025 02:22:03 GMT  
		Size: 4.3 MB (4308211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aff227300c51e3848941d2979c95e4b9ed0b187248ebdc54e62bc099dfebaf1`  
		Last Modified: Tue, 01 Jul 2025 02:22:03 GMT  
		Size: 1.5 MB (1473617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc2b014a01ccb5485bba60914570f2f571b6f695e112f3c9a594012de1f4e69`  
		Last Modified: Tue, 01 Jul 2025 02:22:04 GMT  
		Size: 8.0 MB (8045877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508ddc3b8f5df6a841ab79894d647b592419d1014a848befdba3aa625f6bce2c`  
		Last Modified: Tue, 01 Jul 2025 02:22:03 GMT  
		Size: 1.0 MB (1038395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5103bfadacce8d2b6891d5b1dd49302557df042cc333ff5b941d6f5721e1600c`  
		Last Modified: Tue, 01 Jul 2025 02:22:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a99c5a05d1d796f93d3a860b1d6800024d5ad64f387c18e3fee602526fed07`  
		Last Modified: Tue, 01 Jul 2025 02:22:04 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e04ab29d79770664821ef821e9d574813a8e9c9bc53a90d2a34e80e3b69137`  
		Last Modified: Tue, 01 Jul 2025 02:22:09 GMT  
		Size: 104.3 MB (104264317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364af41749a7b9978029db3430ca05cd16238bec6f63d6e815576a6ef8a4e1f3`  
		Last Modified: Tue, 01 Jul 2025 02:22:03 GMT  
		Size: 19.1 KB (19104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e3fb9c3ee1da30d1b467d64431c3c99a7fab256b5e2d681b3b5af2f1af94e1`  
		Last Modified: Tue, 01 Jul 2025 02:22:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c972afe92a763c517bbc25c3d077e951c0a88e5cc475f28be0634d48982a76b1`  
		Last Modified: Tue, 01 Jul 2025 02:22:04 GMT  
		Size: 179.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b46c181944ba96732022fbef6d25839291655b13c268584dd458039f39088b`  
		Last Modified: Tue, 01 Jul 2025 02:22:04 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b644c4f4c10df64d53630e63a4970e48a2b99ca6b54bfb10d21195925cca9962`  
		Last Modified: Tue, 01 Jul 2025 02:22:03 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta1-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:2f86876f75403cd9d5975df551842f367cb727bdcf9ed1fe186b1cefa0b51be2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6528832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa76266d57e0f901fea67312f726e1ce7633091e435b733eeca5851972b63d0`

```dockerfile
```

-	Layers:
	-	`sha256:64afdf2c67a9794ef8761419b892e0a6f6ecf5201391409f10568db90c3249f0`  
		Last Modified: Tue, 01 Jul 2025 05:11:42 GMT  
		Size: 6.5 MB (6474665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47ed616f266932b0955a190e775513dab6f129b34cfe07a99d33bf4a636d4cfd`  
		Last Modified: Tue, 01 Jul 2025 05:11:43 GMT  
		Size: 54.2 KB (54167 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18beta1-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:b2ab1ac050728b13a50ac41258b29dc512cbf42407f5a7922988efb7c1d6c127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.9 MB (80904479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9726d407f15cf5445f77116713dff8d183d054154a6abac875be828f5a1ee37`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 09 Jun 2025 21:23:06 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1749513600'
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV GOSU_VERSION=1.17
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV LANG=en_US.utf8
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PG_MAJOR=18
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PG_VERSION=18~beta1-1.pgdg110+1
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 09 Jun 2025 21:23:06 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
VOLUME [/var/lib/postgresql]
# Mon, 09 Jun 2025 21:23:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jun 2025 21:23:06 GMT
STOPSIGNAL SIGINT
# Mon, 09 Jun 2025 21:23:06 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 09 Jun 2025 21:23:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:254beacf3f323cf99977d539dcb720dc371b362af3a11b68a1c46f29aa86d29f`  
		Last Modified: Tue, 10 Jun 2025 22:48:19 GMT  
		Size: 25.5 MB (25544195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9abe736d79e05f6cffecc0489bd1925ce7cc5f9671168cbf7867aa77313d971d`  
		Last Modified: Wed, 11 Jun 2025 02:25:07 GMT  
		Size: 1.7 KB (1681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d9397c415d07185281508dbfde76f00630943770be20437cc820991f8ec21a`  
		Last Modified: Wed, 11 Jun 2025 02:25:08 GMT  
		Size: 3.6 MB (3601820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1a1bf96ba3a9651841503cf2b69eee23230d91c9126b1234cc229031dfea69`  
		Last Modified: Wed, 11 Jun 2025 02:25:08 GMT  
		Size: 1.4 MB (1440899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2025e835f5ed5e2604a37406d717ed5a637e9d92206db7c4a8cf1d65438ab5b6`  
		Last Modified: Wed, 11 Jun 2025 02:25:09 GMT  
		Size: 8.0 MB (8045875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff99a2f3dce50e4137487f6eff81dc15728ca8800ca80b7dae2b06fec7760202`  
		Last Modified: Wed, 11 Jun 2025 02:25:10 GMT  
		Size: 908.7 KB (908668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2116d5e376bdceb6d9777f3d1726c44c6a3794040d3f15b49f2a4bde1a67793d`  
		Last Modified: Wed, 11 Jun 2025 02:25:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362f39dd9579f18412778f736f45f79de6eb0f211f150b4d55a14a370325c7ec`  
		Last Modified: Wed, 11 Jun 2025 02:35:08 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faade6b63f72f8130dea8af14dd1cacc3120495851a8ed5f4634248e1c34d072`  
		Last Modified: Wed, 11 Jun 2025 12:00:14 GMT  
		Size: 41.3 MB (41332548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453eac95777a537586f05ab2d209f29f801b5ab99958b4ea94c67b68f89a9e2c`  
		Last Modified: Wed, 11 Jun 2025 02:35:11 GMT  
		Size: 19.1 KB (19112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a71b7809729d16687eccc738aa7d9bea17259e513868c335688b07105c1654`  
		Last Modified: Wed, 11 Jun 2025 02:35:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d39dccfd02b9658bfa13ee9c2e52bad3cf78c8df0b0b62b4dca0a13b83a799`  
		Last Modified: Wed, 11 Jun 2025 02:35:17 GMT  
		Size: 180.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:910184ae81f3348d0a6a801b0866c73f598657565d6ef5f5e8b4a19e6fca9dba`  
		Last Modified: Wed, 11 Jun 2025 02:35:19 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e52b48897375e7f31882bfad49c916f25df4f37b8f8eb72b71ace9b0992a86`  
		Last Modified: Wed, 11 Jun 2025 02:35:21 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta1-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:ff207881c7d1f2b9984c2c4fc781f21e735be36992c5b273237da878cc30196f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5683904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58e0c14c42bb29d6ef25c5ae6a1efc4abf2d77cacf8f67d879d916da410d56a`

```dockerfile
```

-	Layers:
	-	`sha256:849b079a1ac9ea792b844a270d0260edb3e920f2c6a3b294777fc366eb6162a2`  
		Last Modified: Wed, 11 Jun 2025 05:11:13 GMT  
		Size: 5.6 MB (5629559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d2fafa74914554cc31fd5fd2969f6d83d9a7d5a44dd6b94a89d4a097eff776b`  
		Last Modified: Wed, 11 Jun 2025 05:11:14 GMT  
		Size: 54.3 KB (54345 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18beta1-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:90b4584a7e46361040dd39d89712c5945d8d6e2699cc3d1ebdca149491724e6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.4 MB (146420054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:475b5cfcf71632b0555c3a99d2c809cf153079c54fb134cb4e49e0693290c95c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 09 Jun 2025 21:23:06 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV GOSU_VERSION=1.17
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV LANG=en_US.utf8
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PG_MAJOR=18
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PG_VERSION=18~beta1-1.pgdg110+1
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 09 Jun 2025 21:23:06 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
VOLUME [/var/lib/postgresql]
# Mon, 09 Jun 2025 21:23:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jun 2025 21:23:06 GMT
STOPSIGNAL SIGINT
# Mon, 09 Jun 2025 21:23:06 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 09 Jun 2025 21:23:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1efb2a16e6255fa81193190b623ba0668ffa777ab1de41ac5c5d2d2060a47784`  
		Last Modified: Wed, 11 Jun 2025 00:07:31 GMT  
		Size: 28.7 MB (28744185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d1aa8b14d6c2340d79f9dcc5c7d981e9e2449c2ca1ddd3b841ba02a9ec9f67`  
		Last Modified: Wed, 11 Jun 2025 02:17:16 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ab99dfee393772b9d00749ba3a527c73c1a985bb2fed2a057c33d6f424c5c3`  
		Last Modified: Wed, 11 Jun 2025 02:17:18 GMT  
		Size: 4.3 MB (4312799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d3d84fd8c9d70058c8e0b4b31de85d5043cda15864068cea6f88d0a4f7be0e`  
		Last Modified: Wed, 11 Jun 2025 02:17:16 GMT  
		Size: 1.4 MB (1405929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10877f2d7984dcfc3fb405a8f9308383ef014de0f5c75bcdc758568a3d5ac16d`  
		Last Modified: Wed, 11 Jun 2025 02:17:18 GMT  
		Size: 8.0 MB (8045717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935055b822914944b70a0083990ace46c79f323e5b48a04fa6930405a9c3dc8f`  
		Last Modified: Wed, 11 Jun 2025 02:17:18 GMT  
		Size: 1.0 MB (1026587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c81c0a4b897271c0a3da28c0825c4f12588599be36b9dcaaa7f853fdbf25578`  
		Last Modified: Wed, 11 Jun 2025 02:17:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f71f395644070dac7f893864d14036e82819689dd49412df9b843b9befd09fe`  
		Last Modified: Wed, 11 Jun 2025 02:17:18 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb70be45ee0110b6274b91478629b3e16f4462390cc5fa356d7e1ba916cc378a`  
		Last Modified: Wed, 11 Jun 2025 02:17:23 GMT  
		Size: 102.9 MB (102854363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99c632da84c3633d11b52deb0942d34da991a3684bb86ee7aad1397c8de9cc5`  
		Last Modified: Wed, 11 Jun 2025 02:17:19 GMT  
		Size: 19.1 KB (19106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d9bce9c40ba9ef20236dca3f43c0b5134d12090367290bd6bce36262c90dae`  
		Last Modified: Wed, 11 Jun 2025 02:17:19 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c295350ba57ae13937d99f8920b6407d6b38bcba9d6d6190ce5b2f96a826218`  
		Last Modified: Wed, 11 Jun 2025 02:17:19 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6681ffd334e64649216a4ef793aa23a97c6112e55ea61832035470debbd99a08`  
		Last Modified: Wed, 11 Jun 2025 02:17:19 GMT  
		Size: 5.9 KB (5926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba9292e10ec3edf919fc1be27729f5facd0d9610818ee9a13518f7e0f0ced07`  
		Last Modified: Wed, 11 Jun 2025 02:17:20 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta1-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:9873bdbbe5eb5fad82bdcfad6cbec51c937eee95b87029cd391e65a9d71324bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6535306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a77a8b44098cc8c11eb1b0f09d0fe3c91304530d8402d90e03244c18884966da`

```dockerfile
```

-	Layers:
	-	`sha256:e991368591840f3a96edc5bcf8f057411143291ae05ab800fffdd7a7729d4fdf`  
		Last Modified: Wed, 11 Jun 2025 05:11:20 GMT  
		Size: 6.5 MB (6480906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d53651ebb902f4b818669574251bba71a349a0f6df643dd5e0617c1a3679bff8`  
		Last Modified: Wed, 11 Jun 2025 05:11:21 GMT  
		Size: 54.4 KB (54400 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18beta1-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:b5fbe7b598b43e1e57639268b1385c0000973122d771077349bd2d4135c2cf90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (91042934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa787732a67e56036b42c4b692a8623aab4d6c8f02c9db3e60256da0a570a36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 09 Jun 2025 21:23:06 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1751241600'
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV GOSU_VERSION=1.17
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV LANG=en_US.utf8
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PG_MAJOR=18
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PG_VERSION=18~beta1-1.pgdg110+1
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 09 Jun 2025 21:23:06 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
VOLUME [/var/lib/postgresql]
# Mon, 09 Jun 2025 21:23:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jun 2025 21:23:06 GMT
STOPSIGNAL SIGINT
# Mon, 09 Jun 2025 21:23:06 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 09 Jun 2025 21:23:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:40be1da6146972d9df50a98eef7b5c0f729cd95a3a38782418f354f3b9355a9a`  
		Last Modified: Tue, 01 Jul 2025 01:14:57 GMT  
		Size: 31.2 MB (31189680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd75f44dfbda6758bf2487ae9645eebff9213987db530c541cf0f54bb516829c`  
		Last Modified: Tue, 01 Jul 2025 02:29:21 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3eac085904da0332bb2efbb8b7c911450319f00a8f5c2300d9c6426fbc768d`  
		Last Modified: Tue, 01 Jul 2025 02:29:22 GMT  
		Size: 4.7 MB (4719715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f311d5548706c199f9b05df3eea2be940f80bac488e56857b2c608a9b8b294`  
		Last Modified: Tue, 01 Jul 2025 02:29:22 GMT  
		Size: 1.4 MB (1449339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124dd04dc659286486409d46f525eb642d13d8d8043560d61213ca04cae5c574`  
		Last Modified: Tue, 01 Jul 2025 02:29:22 GMT  
		Size: 8.0 MB (8045776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3aa31b70dc9deb2bbed0f2789f08122a45333bc4b7ce5415cc972da844561bd`  
		Last Modified: Tue, 01 Jul 2025 02:29:22 GMT  
		Size: 1.0 MB (1028934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404ad9cc37fea801cbf20f508534e689ee9b94f1f3ff72797266b2d66773c5f7`  
		Last Modified: Tue, 01 Jul 2025 02:29:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e78323059dd591f89280ba250e3886a6c889ff6c038e3eb154f7864a96a64f`  
		Last Modified: Tue, 01 Jul 2025 02:29:21 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb26992da632845b228d3c52644b2e045698095232de5b439c7008ecf610d64`  
		Last Modified: Tue, 01 Jul 2025 02:29:24 GMT  
		Size: 44.6 MB (44579028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967d1e216d4ba17a249d8e163f671dd10376187532409b27ebf3bd1b4dbebee7`  
		Last Modified: Tue, 01 Jul 2025 02:29:21 GMT  
		Size: 19.1 KB (19110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d6e8a8fb72f50f1297f6ec5f98a0ceeeedd7d5ba69f9e61e9ad6a25def75d9`  
		Last Modified: Tue, 01 Jul 2025 02:29:21 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658834858dd46c62f6a18cbf8c89814eaf2c262a05ce1a73598c4537170126a6`  
		Last Modified: Tue, 01 Jul 2025 02:29:22 GMT  
		Size: 180.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e27591054aec676f52d8c9d40eff37ce8eab21d6cc91037c6c46e5dc8fb36cf`  
		Last Modified: Tue, 01 Jul 2025 02:29:22 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f579a65719ffa6a9150680bd4288b5f7216a0a86629dc401c83981fa7a90eb`  
		Last Modified: Tue, 01 Jul 2025 02:29:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta1-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:8d3c842c49f3ae92494426f3493924e9d9ecaed1768b207963140e691aefd039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5678335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95064f1ed11a70a00d4608524039cd054caf4f3046e3001cf9577a83ff413b2e`

```dockerfile
```

-	Layers:
	-	`sha256:37317c4eaafdae67e3df84e45ba04bb22e3d85b99f9fde32a2fbe9107103589c`  
		Last Modified: Tue, 01 Jul 2025 05:12:07 GMT  
		Size: 5.6 MB (5624213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fb3d6fab4e3140b90929ad9e40e71cda3c971db8657bb1f1c42bf38aae0e8eb`  
		Last Modified: Tue, 01 Jul 2025 05:12:08 GMT  
		Size: 54.1 KB (54122 bytes)  
		MIME: application/vnd.in-toto+json
