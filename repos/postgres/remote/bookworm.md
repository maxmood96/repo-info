## `postgres:bookworm`

```console
$ docker pull postgres@sha256:80630f83606d8db77d30b3851b16a9f78be2d0d4dda6f7b82a1fdca5ebe3acba
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

### `postgres:bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:4b2a518e377fe4cbb67168b8043724634f144cbad35a306c6bab44fced4ec2c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157126431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c67953c3a90a3a846b72e6cd2cfa418b0487e06156ed470dbbeaeb4cac09178`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:33:02 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 08 May 2026 19:33:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:33:13 GMT
ENV GOSU_VERSION=1.19
# Fri, 08 May 2026 19:33:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 May 2026 19:33:17 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 08 May 2026 19:33:17 GMT
ENV LANG=en_US.utf8
# Fri, 08 May 2026 19:33:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:33:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 May 2026 19:33:21 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:33:21 GMT
ENV PG_MAJOR=18
# Fri, 08 May 2026 19:33:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Fri, 08 May 2026 19:33:21 GMT
ENV PG_VERSION=18.3-1.pgdg12+1
# Fri, 08 May 2026 19:33:35 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 08 May 2026 19:33:35 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 08 May 2026 19:33:35 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 08 May 2026 19:33:35 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 08 May 2026 19:33:35 GMT
VOLUME [/var/lib/postgresql]
# Fri, 08 May 2026 19:33:35 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:33:35 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 08 May 2026 19:33:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:33:35 GMT
STOPSIGNAL SIGINT
# Fri, 08 May 2026 19:33:35 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 08 May 2026 19:33:35 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047252d203fc9f963e60a2f82ed198f6ac1a7fd5022852eda0c80b83cae9d3bd`  
		Last Modified: Fri, 08 May 2026 19:33:55 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:285c515ff12e3af3dcaf8c46dae3afacf0cd8bf3605963f33bf7769626ed921a`  
		Last Modified: Fri, 08 May 2026 19:33:55 GMT  
		Size: 4.5 MB (4534215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04bac481cf959c7f2252eb9d4fa287f73a5cd140f38e2102debcdb8ff3065ec`  
		Last Modified: Fri, 08 May 2026 19:33:55 GMT  
		Size: 1.2 MB (1249506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2f8983bdebf0b7564e99a757464d27b67a26dbc3265f40c71d2932618d686d`  
		Last Modified: Fri, 08 May 2026 19:33:55 GMT  
		Size: 8.1 MB (8066446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928cbc530e9bcbca5d0e3dce94b38d83e22baea1d79fc70453de2ca00bffe3f2`  
		Last Modified: Fri, 08 May 2026 19:33:56 GMT  
		Size: 1.2 MB (1196388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d7c0b1553c6f6316fc6308f598952b8f5b37329cbc52d72d67006c5f04716c`  
		Last Modified: Fri, 08 May 2026 19:33:56 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef11daf919659d0d6e3a1058ade593fcb88761bdf175aef515632a7d66417cf9`  
		Last Modified: Fri, 08 May 2026 19:33:57 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dab6177213d106b539dee1958243e9c49096756c6834620542c39d2d4ba42a4`  
		Last Modified: Fri, 08 May 2026 19:34:04 GMT  
		Size: 113.8 MB (113813525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73f5647695fb420b075bba4452af3bd1ce26847dc461c087c18798afcf9617c`  
		Last Modified: Fri, 08 May 2026 19:33:58 GMT  
		Size: 19.2 KB (19227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1186127d05fbc8be8cfeb273a8731b9eff042fb03e3c8078878fdbd6dc8d0d`  
		Last Modified: Fri, 08 May 2026 19:33:58 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73bb36f2399258efb15c6a279a8d62bd2cd65666d8f5ae0ffe3a601369c8e21`  
		Last Modified: Fri, 08 May 2026 19:33:58 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142af709c9ab7060a27d794b1e8ec16696c255ead065e1b4b02d411bf47f18b2`  
		Last Modified: Fri, 08 May 2026 19:33:59 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:1ade40c63e02344c09d4141d5b5e0e239421b4a2af9c97597d3c1d52b15ef5ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6208087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c49857cff42adf856bce2e5bf5d5f3f1dce365388288aa53aa042c1a077fbebd`

```dockerfile
```

-	Layers:
	-	`sha256:30cbd0864e2c6efd888cf4702063b39ba97b498480d004ac116f85eb449ab5f3`  
		Last Modified: Fri, 08 May 2026 19:33:55 GMT  
		Size: 6.2 MB (6156497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbcc4f3f0f66bbe9e44f39cb745248f0b2677c97300783802e520787c8ebd030`  
		Last Modified: Fri, 08 May 2026 19:33:55 GMT  
		Size: 51.6 KB (51590 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:7d00e52d8725786863e2776e4a9e5dfa3d20863d99765151feba5bde1099008b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.2 MB (87224273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ece736b549b56b8721959e1530fe2a7f2d9b0f19845d26ff92618f4c32ac6fea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:39:34 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 08 May 2026 20:39:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:39:51 GMT
ENV GOSU_VERSION=1.19
# Fri, 08 May 2026 20:39:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 May 2026 20:39:58 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 08 May 2026 20:39:58 GMT
ENV LANG=en_US.utf8
# Fri, 08 May 2026 20:40:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:40:04 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 May 2026 20:40:04 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 20:40:04 GMT
ENV PG_MAJOR=18
# Fri, 08 May 2026 20:40:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Fri, 08 May 2026 20:40:04 GMT
ENV PG_VERSION=18.3-1.pgdg12+1
# Fri, 08 May 2026 20:52:08 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 08 May 2026 20:52:08 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 08 May 2026 20:52:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 08 May 2026 20:52:08 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 08 May 2026 20:52:08 GMT
VOLUME [/var/lib/postgresql]
# Fri, 08 May 2026 20:52:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:52:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 08 May 2026 20:52:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 20:52:08 GMT
STOPSIGNAL SIGINT
# Fri, 08 May 2026 20:52:08 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 08 May 2026 20:52:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0496e5b1fd9475851f8b3578080061a05ea61be300ea5a278a4a08a883855adc`  
		Last Modified: Fri, 08 May 2026 18:33:05 GMT  
		Size: 25.8 MB (25765670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d17ba87d03e9701820f4b5b5a33336ee6a4a2ba2154d42849e8656327d0da4`  
		Last Modified: Fri, 08 May 2026 20:52:21 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b249452bfd186ed253b19b685e3609f76a471495f0b933b81b90591b1000b6`  
		Last Modified: Fri, 08 May 2026 20:52:21 GMT  
		Size: 4.2 MB (4151320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35cd3aafec837f6e64d349d7215f4849089088c7d92ac7fe5759a31e9b047fee`  
		Last Modified: Fri, 08 May 2026 20:52:21 GMT  
		Size: 1.2 MB (1220284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d444d2673808ef40837747a33b73a53da98070ccddcbe6949a6a27ed6f5eb05f`  
		Last Modified: Fri, 08 May 2026 20:52:22 GMT  
		Size: 8.1 MB (8066589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571df963865d1f6b712ecaa37fb86b55b8c5d155cd13a7dc4687c834af336db4`  
		Last Modified: Fri, 08 May 2026 20:52:22 GMT  
		Size: 1.2 MB (1195084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72c2f03fee0499d559c2913f418991a0e60c6ae586fc9b636ebe625badd6157`  
		Last Modified: Fri, 08 May 2026 20:52:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05a2bff7e9a906b366567752dfcbfd5549bac11bbcd136a292b8c72d5331d2b`  
		Last Modified: Fri, 08 May 2026 20:52:22 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79b4b22df2c1145c36051789886619e6379d720457745780b1a8d858bb56c53`  
		Last Modified: Fri, 08 May 2026 20:52:24 GMT  
		Size: 46.8 MB (46795256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a405ecc0667a85fb3adcd82ddf8d83ab87fcab12ea066bf43ad9a8bb4af337d`  
		Last Modified: Fri, 08 May 2026 20:52:23 GMT  
		Size: 19.2 KB (19233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5352796a1117ed3ece6b32ecf567cb500935d0712a7052774c4ff13cf47191`  
		Last Modified: Fri, 08 May 2026 20:52:24 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb2a51bb959a4baaaa242607b502ed7805f85d4aaecfe562886bfe69d18e718`  
		Last Modified: Fri, 08 May 2026 20:52:24 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deba4a6080cf81867131aedafc4565a0cb5acd37f30ff442868995a5fdb75801`  
		Last Modified: Fri, 08 May 2026 20:52:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:1695b4efd4386e5401fcfa0e301b9bb8f87ff072433d875691e6f4a106e29131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5368802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48b83145ace5a7016ffad1832ed6be582000a42923542d1918dbca533d4a487d`

```dockerfile
```

-	Layers:
	-	`sha256:162f71799024613fe744f54512e241499f8698fc6112a73afeb002c3c8701a3c`  
		Last Modified: Fri, 08 May 2026 20:52:21 GMT  
		Size: 5.3 MB (5317016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e361e2316ee048a4b40069583a867af4e876c9df8ea24cf78f87f13bba198330`  
		Last Modified: Fri, 08 May 2026 20:52:21 GMT  
		Size: 51.8 KB (51786 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:a384d07d9616a994923df739d4de1208e08d71244f6bd7337fd5ae060dc5e353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83344506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:311eefa2114f2b1d9f42b9aa05ab4ee0ed7439bd073d446104e33000a7b0d340`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:27:28 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 08 May 2026 19:27:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:27:42 GMT
ENV GOSU_VERSION=1.19
# Fri, 08 May 2026 19:27:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 May 2026 19:27:47 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 08 May 2026 19:27:47 GMT
ENV LANG=en_US.utf8
# Fri, 08 May 2026 19:27:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:27:51 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 May 2026 19:27:52 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:27:52 GMT
ENV PG_MAJOR=18
# Fri, 08 May 2026 19:27:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Fri, 08 May 2026 19:27:52 GMT
ENV PG_VERSION=18.3-1.pgdg12+1
# Fri, 08 May 2026 19:39:27 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 08 May 2026 19:39:27 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 08 May 2026 19:39:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 08 May 2026 19:39:27 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 08 May 2026 19:39:27 GMT
VOLUME [/var/lib/postgresql]
# Fri, 08 May 2026 19:39:27 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:39:27 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 08 May 2026 19:39:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:39:27 GMT
STOPSIGNAL SIGINT
# Fri, 08 May 2026 19:39:27 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 08 May 2026 19:39:27 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1c5a0b31b39e45b38b0c73a2e506eb60bb1de512092b4765e565207648f55da2`  
		Last Modified: Fri, 08 May 2026 18:37:03 GMT  
		Size: 23.9 MB (23941406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401def594a39c3b21b7a73fb16262502b1cb29f40141182a4af137575b42b359`  
		Last Modified: Fri, 08 May 2026 19:39:40 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5558df4f6ebcecbeba732f19d613b36aa8fa500a550b4c120c683d396f024df`  
		Last Modified: Fri, 08 May 2026 19:39:40 GMT  
		Size: 3.7 MB (3742706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a060bf7fccfbdd896405b273eb3973f438aaed43aa859aab9c4faa62fb107d6`  
		Last Modified: Fri, 08 May 2026 19:39:40 GMT  
		Size: 1.2 MB (1216145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb82630bec148eb49b679fcd241a83b547496eae50cf4cdf9b0913f886d9194`  
		Last Modified: Fri, 08 May 2026 19:39:40 GMT  
		Size: 8.1 MB (8066508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e557dbd412d11ea443455067a6250a3cb875dc8491fe45f975efa4573c059d`  
		Last Modified: Fri, 08 May 2026 19:39:41 GMT  
		Size: 1.1 MB (1067268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c29aa59cd267bf12c80df1e2d83fbb425a5e9ee2bdfd8785d3250530d5e13c`  
		Last Modified: Fri, 08 May 2026 19:39:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5005802dd46ab01764ec343fa7e33ddc62f924e78a98354347b363a9c4c28f9`  
		Last Modified: Fri, 08 May 2026 19:39:41 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01c0ce7ee68e23ab278fbac7ba24f2792b3ca7acfa068eecd348e02653fc6b0`  
		Last Modified: Fri, 08 May 2026 19:39:43 GMT  
		Size: 45.3 MB (45280408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6d868b6d98902e2ab40e63f94176eab260e78d5d12857173bfa14e5897994d`  
		Last Modified: Fri, 08 May 2026 19:39:43 GMT  
		Size: 19.2 KB (19230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdf9eedbcdcd645b44cd5ed4082c604ea1ca1251ccf800a87d59d5cfa1cb939`  
		Last Modified: Fri, 08 May 2026 19:39:42 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02644dfee497b27b1ece59ad179753e3ed6dcfccde54afd5e9c43ec71ce230fc`  
		Last Modified: Fri, 08 May 2026 19:39:43 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc18d94f491176315ea70c6f4730a5da0cec844b6b26d499e1ca8f6269f60610`  
		Last Modified: Fri, 08 May 2026 19:39:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:8368a690f26987ca4aeb1f79c6cca60e3f60c237681dc875a2e63a4b23cb976a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5368054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88982397e5dcdd861ce01a9dc36ffc2548b532576eba54dfb8a48f5e0aaa4bea`

```dockerfile
```

-	Layers:
	-	`sha256:bd6441e2cf1901738761b173d560db6bef5fd2ab765e03f056dbfde9a2f7edd5`  
		Last Modified: Fri, 08 May 2026 19:39:40 GMT  
		Size: 5.3 MB (5316267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:446242dd7c882385983244dfcf792b61fdff6e5127ea8ab3118addbf86d71a51`  
		Last Modified: Fri, 08 May 2026 19:39:40 GMT  
		Size: 51.8 KB (51787 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:ed505e49589d964cc84644252c6de3bddc41ad8f53d9c508a5179810fd4935bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155112725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0984215845c9203725ec1049ec2b1bdd2e8f5e0eeb4a82cfea4d9928a952ad40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:33:36 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 08 May 2026 19:33:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:33:47 GMT
ENV GOSU_VERSION=1.19
# Fri, 08 May 2026 19:33:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 May 2026 19:33:52 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 08 May 2026 19:33:52 GMT
ENV LANG=en_US.utf8
# Fri, 08 May 2026 19:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:33:54 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 May 2026 19:33:55 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:33:55 GMT
ENV PG_MAJOR=18
# Fri, 08 May 2026 19:33:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Fri, 08 May 2026 19:33:55 GMT
ENV PG_VERSION=18.3-1.pgdg12+1
# Fri, 08 May 2026 19:34:10 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 08 May 2026 19:34:10 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 08 May 2026 19:34:10 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 08 May 2026 19:34:10 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 08 May 2026 19:34:10 GMT
VOLUME [/var/lib/postgresql]
# Fri, 08 May 2026 19:34:10 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:34:10 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 08 May 2026 19:34:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:34:10 GMT
STOPSIGNAL SIGINT
# Fri, 08 May 2026 19:34:10 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 08 May 2026 19:34:10 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9fbfc04c3832dd2cc66ec77614e74ed9153d52f4cf3ce47758444aea623b1ed`  
		Last Modified: Fri, 08 May 2026 19:34:29 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce68cede4f6fd13698b7709503d2b70b657a558709825eb241c828a16d39c569`  
		Last Modified: Fri, 08 May 2026 19:34:29 GMT  
		Size: 4.5 MB (4519520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f70eddaca1a6f017d95fc9f9e40fbcbc530ec9e6d2c25899b891d58e9272b9`  
		Last Modified: Fri, 08 May 2026 19:34:29 GMT  
		Size: 1.2 MB (1203292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd497e82fc74783793f75a602afe719b46bccc66a0882b4326ac88e9c2d60ec`  
		Last Modified: Fri, 08 May 2026 19:34:29 GMT  
		Size: 8.1 MB (8066487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3283ff06f54f739efae158800997e3faa4d1744b277f328503fd3bed0506819b`  
		Last Modified: Fri, 08 May 2026 19:34:30 GMT  
		Size: 1.1 MB (1109008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa53580300b99122a18fcc08551dd35001c7b9e6abb4c2f6dec20862c19a3498`  
		Last Modified: Fri, 08 May 2026 19:34:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a8c43de120c778030e6ed270548afb0627e0add4b7e2d74b697bee72ed934c`  
		Last Modified: Fri, 08 May 2026 19:34:30 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accf81bbd9c3dd0b9f99bd78f5bb10d7e9fcb6a0961cb31f43f959483e47d373`  
		Last Modified: Fri, 08 May 2026 19:34:35 GMT  
		Size: 112.1 MB (112068187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0748545376ad6eb727ec76e701ee84dbd18de772208c95e70eb15ef4adf719dd`  
		Last Modified: Fri, 08 May 2026 19:34:32 GMT  
		Size: 19.2 KB (19230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5982a935189e37b4a01f48e813db2ee59d43a63f3ebac48707b558bc0bc2b5`  
		Last Modified: Fri, 08 May 2026 19:34:31 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f812c7ac467db71729a117e27162d6fd0aafb25425e5f00de9b538ed836c3040`  
		Last Modified: Fri, 08 May 2026 19:34:32 GMT  
		Size: 6.1 KB (6095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2067a2131a4be1ea111922a850d8973ddf1ec6b205ca9e2888a9e38352193371`  
		Last Modified: Fri, 08 May 2026 19:34:33 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:212bb862eba5827e44ffb96790825e59ddbe0cd2d9d1d4f97159b51a8c78a019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6214654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cbb2b6f74bc137aaa0c2b9744d8bd27b17dfea8e875460c21eb71cbb627ba36`

```dockerfile
```

-	Layers:
	-	`sha256:7bded5af4ab39b677412696a08e8fd7b543822100e8640836dce501a87ebf65d`  
		Last Modified: Fri, 08 May 2026 19:34:29 GMT  
		Size: 6.2 MB (6162822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2468fde52b9d8e458aeebf76a2693efdc0e1e4292811e8132db9d97d4c9e8443`  
		Last Modified: Fri, 08 May 2026 19:34:29 GMT  
		Size: 51.8 KB (51832 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; 386

```console
$ docker pull postgres@sha256:e9f5d3502f4a3764e77701d33fdc37cbf833f207098c83fad057c1471732d673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (93998469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b42847f71ca2b3ffb977e0b18fbdfc6694ececc04ce84748b35a2c7232c0944a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:29:39 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 08 May 2026 19:29:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:29:52 GMT
ENV GOSU_VERSION=1.19
# Fri, 08 May 2026 19:29:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 May 2026 19:29:57 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 08 May 2026 19:29:57 GMT
ENV LANG=en_US.utf8
# Fri, 08 May 2026 19:30:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:30:00 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 May 2026 19:30:01 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:30:01 GMT
ENV PG_MAJOR=18
# Fri, 08 May 2026 19:30:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Fri, 08 May 2026 19:30:01 GMT
ENV PG_VERSION=18.3-1.pgdg12+1
# Fri, 08 May 2026 19:39:42 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 08 May 2026 19:39:42 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 08 May 2026 19:39:42 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 08 May 2026 19:39:42 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 08 May 2026 19:39:42 GMT
VOLUME [/var/lib/postgresql]
# Fri, 08 May 2026 19:39:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:39:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 08 May 2026 19:39:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:39:43 GMT
STOPSIGNAL SIGINT
# Fri, 08 May 2026 19:39:43 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 08 May 2026 19:39:43 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d90092c8edd324a692787fd4188906e71211941e12cf7df45f29d2b706aba9ab`  
		Last Modified: Fri, 08 May 2026 18:30:44 GMT  
		Size: 29.2 MB (29221767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5478fd511b963fd4c1b9d33b41fe496fb4193fcde6f1ab3c9c163c2bee7213`  
		Last Modified: Fri, 08 May 2026 19:39:56 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7f98b992ad83cedac3515331cb9797e01611d503a7c9fd71aa5e396ec4ab55`  
		Last Modified: Fri, 08 May 2026 19:39:56 GMT  
		Size: 5.0 MB (4966089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b59e1f910094e37de0995891e6b52d7381ac57bb4cb727fa701e67665fa6119`  
		Last Modified: Fri, 08 May 2026 19:39:56 GMT  
		Size: 1.2 MB (1218639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60dc9aa1c109e077c1605704b0d2592dafdd5dc24cf7c12845df2aef17f7d45`  
		Last Modified: Fri, 08 May 2026 19:39:56 GMT  
		Size: 8.1 MB (8066457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc990c143e97c2c319511821bfa33cdb9bdc98b3f9eab6645fd624f7c9d1dc0`  
		Last Modified: Fri, 08 May 2026 19:39:57 GMT  
		Size: 1.1 MB (1137493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64440a7ab269291bd92340b6cfa69416c8626e5c5b31f6f461a6919fdada818`  
		Last Modified: Fri, 08 May 2026 19:39:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52a610f7d41767ea7a2c37675113d83d88cbe046a4671d264d4f28454603457`  
		Last Modified: Fri, 08 May 2026 19:39:57 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8cd8096452a9e97b49e4a836afdbe858e14a0161408d6df7581b582c22c4c49`  
		Last Modified: Fri, 08 May 2026 19:39:59 GMT  
		Size: 49.4 MB (49357957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40450cd1585e09b800be901539a9cd4375ca060d51d44528a8832bead46fe24a`  
		Last Modified: Fri, 08 May 2026 19:39:58 GMT  
		Size: 19.2 KB (19230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86fad5b5600855114b76dd7405268fbc5e63761a47ae1d2e0d2bfc2e05a01c5d`  
		Last Modified: Fri, 08 May 2026 19:39:58 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac02da8b7afa184889e7a4c7d4fbabb988b762519295cc84af189f2c1b514a4`  
		Last Modified: Fri, 08 May 2026 19:39:59 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4389f3d61da8faee44e44c3727fe5223b577627c97f9db64d82f271204e728c6`  
		Last Modified: Fri, 08 May 2026 19:39:59 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:a40e0269958972bbeb5426992b3b20521ceded46f0df772988fa1d48a11e8e04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5363120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a464ca5880a78f932ce45400e0fc8ceca875053d71ac2021a26f9df5a996eee6`

```dockerfile
```

-	Layers:
	-	`sha256:2fb0e1d1b910ce5d58bf4f753d47d0d4c92d0a8f1a06e1d0a4db7439e75cad3f`  
		Last Modified: Fri, 08 May 2026 19:39:56 GMT  
		Size: 5.3 MB (5311582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:027ee5cc5fedb068b752728f6179c37fad6f13c93b5af5a64080c0305c8ca6ba`  
		Last Modified: Fri, 08 May 2026 19:39:55 GMT  
		Size: 51.5 KB (51538 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:3d41f6470a2af63342343f928eb8b65118bf383b5da1558b213500fbb6101ae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (155992534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2377033dfa7fab0e93710e3ac1cfa7c14fc9be8e8d286ece48388274b9fcef90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 00:06:05 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sat, 09 May 2026 00:06:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 00:07:14 GMT
ENV GOSU_VERSION=1.19
# Sat, 09 May 2026 00:07:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 09 May 2026 00:07:42 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Sat, 09 May 2026 00:07:42 GMT
ENV LANG=en_US.utf8
# Sat, 09 May 2026 00:08:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 00:08:02 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 09 May 2026 00:08:05 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 09 May 2026 00:08:05 GMT
ENV PG_MAJOR=18
# Sat, 09 May 2026 00:08:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Sat, 09 May 2026 00:08:05 GMT
ENV PG_VERSION=18.3-1.pgdg12+1
# Sat, 09 May 2026 01:20:34 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Sat, 09 May 2026 01:20:36 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 09 May 2026 01:20:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 09 May 2026 01:20:37 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Sat, 09 May 2026 01:20:37 GMT
VOLUME [/var/lib/postgresql]
# Sat, 09 May 2026 01:20:39 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 09 May 2026 01:20:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 09 May 2026 01:20:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 09 May 2026 01:20:40 GMT
STOPSIGNAL SIGINT
# Sat, 09 May 2026 01:20:40 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 09 May 2026 01:20:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8e1a6f4f5a9e9628f902e3c8df639d1691d7f1000dc904f820155d1b9b2fa2ff`  
		Last Modified: Fri, 08 May 2026 18:20:04 GMT  
		Size: 28.5 MB (28526280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd791120c9d0fd5ae541f4efa02eac6975d5d521dc7713c7c0a5580ce265c4a`  
		Last Modified: Sat, 09 May 2026 01:22:41 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eadbfdae50a5c8aa838603ee76bf9e1fc8ec6b440308f4db99142611dc5993e1`  
		Last Modified: Sat, 09 May 2026 01:22:42 GMT  
		Size: 4.5 MB (4475224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b923703b3af581ebee9e4272469b019a1b7c32026c82e2e5bceb9fe34f99e7b`  
		Last Modified: Sat, 09 May 2026 01:22:41 GMT  
		Size: 1.2 MB (1159237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b79102effcd09fd07d148fe64add7df15e3fd82ad665383ab1497a3dbb472c`  
		Last Modified: Sat, 09 May 2026 01:22:42 GMT  
		Size: 8.1 MB (8066715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1edfe569d18ce1b4a1ff0a80ffb62bdb50d73a0907b94ba210053462a9123ca`  
		Last Modified: Sat, 09 May 2026 01:22:42 GMT  
		Size: 1.2 MB (1182949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a94ef0e8381b9e5f5762910a868bf0ff569db77c3db867fb3fb03a4b4f12cda`  
		Last Modified: Sat, 09 May 2026 01:22:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3144afc30e2cc8cbb96a6cbb6e4779570c8f8913d38f069dca79e86d70e260c4`  
		Last Modified: Sat, 09 May 2026 01:22:43 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab04929f04dc78b7fe266bdec19032346a8bac5e8ef42d79c24ff28b121a2786`  
		Last Modified: Sat, 09 May 2026 01:22:55 GMT  
		Size: 112.6 MB (112552045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c157c06b60593669abe39208a80ec34587deb89262881363bb1f173cef899505`  
		Last Modified: Sat, 09 May 2026 01:22:44 GMT  
		Size: 19.2 KB (19240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef38ab1017631bcfc2eb598ccef72838015396f563a36e1e7426e5e17b83b8b`  
		Last Modified: Sat, 09 May 2026 01:22:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3027e856bb827c65cbee265155b2bb363a7b850e9ebfe1e095d7a9982a8ed0`  
		Last Modified: Sat, 09 May 2026 01:22:45 GMT  
		Size: 6.1 KB (6101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7313867de04ede1c79f001778436a78d2e2c13b262b5be94c0e85043085f918e`  
		Last Modified: Sat, 09 May 2026 01:22:45 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:7ee2dff2982d4cafa1877ae901a943362ea80e0bafd6edfcff6cd8ca40cebc34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 KB (51462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d71156eb93ebddf754d4d1cbf7196923c1cc84fe53b3a03564c079cab96a38`

```dockerfile
```

-	Layers:
	-	`sha256:f27bd5af6e0568daeda9dbdba2d5c88b89667ecb4051b5df2a257160ca51069c`  
		Last Modified: Sat, 09 May 2026 01:22:41 GMT  
		Size: 51.5 KB (51462 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:532b7be7d698cb4f59f2bff3351d451ec6e5fc1cbf5a33fdad08997fdb6c8fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.0 MB (170033346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15de79364d9139d4a1b040ec493aa65d0e0108541ab50469fe3f414ddc63ebf6`
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
ENV PG_MAJOR=18
# Fri, 08 May 2026 22:07:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Fri, 08 May 2026 22:07:29 GMT
ENV PG_VERSION=18.3-1.pgdg12+1
# Fri, 08 May 2026 22:08:02 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 08 May 2026 22:08:03 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 08 May 2026 22:08:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 08 May 2026 22:08:03 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 08 May 2026 22:08:03 GMT
VOLUME [/var/lib/postgresql]
# Fri, 08 May 2026 22:08:03 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 22:08:04 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 08 May 2026 22:08:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 22:08:04 GMT
STOPSIGNAL SIGINT
# Fri, 08 May 2026 22:08:04 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 08 May 2026 22:08:04 GMT
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
	-	`sha256:65d1e5a474dc42f3d145666723cd66fa77586e65851aeb99a57dd84cc9e7e519`  
		Last Modified: Fri, 08 May 2026 22:08:47 GMT  
		Size: 122.0 MB (121997853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b02085a9b66afd4d427f7bbbfcb7bde41753049caf3c8e2cbd374074d61554`  
		Last Modified: Fri, 08 May 2026 22:08:44 GMT  
		Size: 19.2 KB (19234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1727d64eb8c4933d2a3c11feb2a149261b94a9fba8c8106c69f0c996146f72`  
		Last Modified: Fri, 08 May 2026 22:08:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4882f4526ef034add120559f84ee48a358b33594517072f327e82e58984e2248`  
		Last Modified: Fri, 08 May 2026 22:08:45 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289ab05cca94dc338f77f6a8c4556ba00078a3ca9b2985e43d83187f590bbcb8`  
		Last Modified: Fri, 08 May 2026 22:08:45 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:bb1c6628abbfb406910534b2e4143d8d580ece4d67da6182ea4dc8d584d3ced1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6215530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fa3050ed2520bc45814f6213178233af1a740779b82b4277227853a5a194cf0`

```dockerfile
```

-	Layers:
	-	`sha256:8ea64744f3059a4a34bde6cac5347ba0247677a90a0e70a8e284953ec63ee418`  
		Last Modified: Fri, 08 May 2026 22:08:42 GMT  
		Size: 6.2 MB (6163882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d98234a1b5bf9e07f659fbe7ed9e25409cff4d75dd5594a23329e4e4921ce6f`  
		Last Modified: Fri, 08 May 2026 22:08:42 GMT  
		Size: 51.6 KB (51648 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:1ee549939a9cadd6df56c9eda74a05d9018b369b37d4053bf7a1b35a2a040d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.4 MB (166428829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1695fc0cba6b881956d2bd8c49538108d6b3b2c5562239ddee239875ad176dfb`
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
ENV PG_MAJOR=18
# Fri, 08 May 2026 20:10:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Fri, 08 May 2026 20:10:24 GMT
ENV PG_VERSION=18.3-1.pgdg12+1
# Fri, 08 May 2026 20:26:44 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 08 May 2026 20:26:45 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 08 May 2026 20:26:45 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 08 May 2026 20:26:45 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 08 May 2026 20:26:45 GMT
VOLUME [/var/lib/postgresql]
# Fri, 08 May 2026 20:26:45 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:26:45 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 08 May 2026 20:26:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 20:26:45 GMT
STOPSIGNAL SIGINT
# Fri, 08 May 2026 20:26:45 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 08 May 2026 20:26:45 GMT
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
	-	`sha256:bb3d6ea0ef86b6d475452f67d441169de3318c75a2135c9377dfd3be0c204026`  
		Last Modified: Fri, 08 May 2026 20:27:24 GMT  
		Size: 124.7 MB (124674827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a831c787ffe96705c3504fabf8bcf3764460cc5bdc8fa889226d36964e05ff30`  
		Last Modified: Fri, 08 May 2026 20:27:23 GMT  
		Size: 19.2 KB (19230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2bd8c94f59b5924aead9a97a78030a98e736d6bdc7c89ce020d13fb1834384`  
		Last Modified: Fri, 08 May 2026 20:27:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445155c4d5a14cc12d09f6b29827618732c66f6629f5ae984b4ca6d85b623d36`  
		Last Modified: Fri, 08 May 2026 20:27:23 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570ae86bcbe9f47e4d8572b98dc566328e0af746792ae9680ef886f11e3cbe68`  
		Last Modified: Fri, 08 May 2026 20:27:24 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:435dd73cf1440ae0204276316f7367c802917e68646d5153cd421d2f3c881ce2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6222745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49f7a50b51bb4a023bfa244abb05429c3752262628628931b039f9b7aefad7c8`

```dockerfile
```

-	Layers:
	-	`sha256:ab3dac9371183a5c8ba3f72588a2eef12a416a44a6b13a26ab65fb9d5743ba0a`  
		Last Modified: Fri, 08 May 2026 20:27:21 GMT  
		Size: 6.2 MB (6171155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:653c8415358609be2922e73759482c44056bbe633d9f664c548092196befc8b5`  
		Last Modified: Fri, 08 May 2026 20:27:20 GMT  
		Size: 51.6 KB (51590 bytes)  
		MIME: application/vnd.in-toto+json
