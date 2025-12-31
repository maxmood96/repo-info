## `postgres:latest`

```console
$ docker pull postgres@sha256:bfe50b2b0ddd9b55eadedd066fe24c7c6fe06626185b73358c480ea37868024d
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

### `postgres:latest` - linux; amd64

```console
$ docker pull postgres@sha256:c333057ef41ae33af97a75ca7534b82aa12963cf5afc9c97954de21f06bcbaa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.2 MB (162205902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3580042f864be93d92ef7a79b075a691f69f7bd8500ea8e489f94dda8a1cd70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:36:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 29 Dec 2025 23:36:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:36:18 GMT
ENV GOSU_VERSION=1.19
# Mon, 29 Dec 2025 23:36:18 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 29 Dec 2025 23:36:22 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 29 Dec 2025 23:36:22 GMT
ENV LANG=en_US.utf8
# Mon, 29 Dec 2025 23:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:36:25 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 29 Dec 2025 23:36:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 29 Dec 2025 23:36:26 GMT
ENV PG_MAJOR=18
# Mon, 29 Dec 2025 23:36:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 29 Dec 2025 23:36:26 GMT
ENV PG_VERSION=18.1-1.pgdg13+2
# Mon, 29 Dec 2025 23:36:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 29 Dec 2025 23:36:40 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 29 Dec 2025 23:36:40 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 29 Dec 2025 23:36:40 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 29 Dec 2025 23:36:40 GMT
VOLUME [/var/lib/postgresql]
# Mon, 29 Dec 2025 23:36:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:36:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 29 Dec 2025 23:36:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:36:40 GMT
STOPSIGNAL SIGINT
# Mon, 29 Dec 2025 23:36:40 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 29 Dec 2025 23:36:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9172e24e2f38f6706a13f55f64655f1bd1c20f83b01c8be9b0e68e2a77263a20`  
		Last Modified: Mon, 29 Dec 2025 23:37:09 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96e97bb6a7e46b779a48286025034573b27602b208050992ece5f835f7382d9`  
		Last Modified: Mon, 29 Dec 2025 23:37:09 GMT  
		Size: 6.4 MB (6436654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d949714b3761f3d266d2f2597f8a198879365b3c73a0220a827593ce9a13223`  
		Last Modified: Mon, 29 Dec 2025 23:37:09 GMT  
		Size: 1.3 MB (1256659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220a79c3dc48239a6ab1f4fc6c6bd1a1efe642074cf66355cd6564969e74b6e9`  
		Last Modified: Mon, 29 Dec 2025 23:37:10 GMT  
		Size: 8.2 MB (8203752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd9f01fbe3015665093b02bcecf4aa962ee9a3bd7918d7f9696250d80e4d24a`  
		Last Modified: Mon, 29 Dec 2025 23:37:09 GMT  
		Size: 1.3 MB (1311506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4346024d450e6fdd1c2eab43c32de59dc806a853280ea08e865c8478c50ce094`  
		Last Modified: Mon, 29 Dec 2025 23:37:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923097c4091206a763ecfc7e4513da5b5068ec355074467a633aa4b4f72e83a7`  
		Last Modified: Mon, 29 Dec 2025 23:37:09 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af774b3ad5749ff073883899f2678f30139d588d9af5e2b13bf55c3ec8d10edc`  
		Last Modified: Mon, 29 Dec 2025 23:37:16 GMT  
		Size: 115.2 MB (115191041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc8979f5730ad97bb88c9d54745b5ff8cc30e29784bdfb3cdda9db8e61f49ff`  
		Last Modified: Mon, 29 Dec 2025 23:37:09 GMT  
		Size: 19.2 KB (19184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2968aa50182dcae16d066fbdb6b103a6b0852f60d134894d52cacdeec2e86b46`  
		Last Modified: Mon, 29 Dec 2025 23:37:09 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9532f2df07c43dd3feef78f749ee6528cf06f0d198b08bdefb85087952c73856`  
		Last Modified: Mon, 29 Dec 2025 23:37:15 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be82039e7017e1c18301d6b60fea20c6dd6ae97e56f7d7e6038004036258522`  
		Last Modified: Mon, 29 Dec 2025 23:37:08 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:9057b6e39032f383499623e882a70bd9ef6be7839406ec1627b46b10f4a1fafe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6008930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d6e1bfb4b06ed48006e9cc2d808d495134bb66b4d79c94e880c29dc725415e6`

```dockerfile
```

-	Layers:
	-	`sha256:5b97b047e2b9e23476a32dae87041d9efbcef1a179650a8c4fc54d29767e6620`  
		Last Modified: Tue, 30 Dec 2025 03:14:37 GMT  
		Size: 6.0 MB (5956473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16f737298e204e4b9a16b32c5fa0cf387ddf3f4b81c379d2f3880da06576d5ea`  
		Last Modified: Tue, 30 Dec 2025 03:14:38 GMT  
		Size: 52.5 KB (52457 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; arm variant v5

```console
$ docker pull postgres@sha256:e515237384761a3383b7a20d8829cf92652471e6fc5833870537d315edcf6ec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.4 MB (91396926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6660d243bfaa3be58e2f61b793d006c221a53bca5fcabb9ce0fe6de47d399f53`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:52:15 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 29 Dec 2025 23:52:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:52:37 GMT
ENV GOSU_VERSION=1.19
# Mon, 29 Dec 2025 23:52:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 29 Dec 2025 23:52:45 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 29 Dec 2025 23:52:45 GMT
ENV LANG=en_US.utf8
# Mon, 29 Dec 2025 23:52:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:52:53 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 29 Dec 2025 23:52:54 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 29 Dec 2025 23:52:54 GMT
ENV PG_MAJOR=18
# Mon, 29 Dec 2025 23:52:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 29 Dec 2025 23:52:54 GMT
ENV PG_VERSION=18.1-1.pgdg13+2
# Tue, 30 Dec 2025 00:06:13 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 30 Dec 2025 00:06:13 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Dec 2025 00:06:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Dec 2025 00:06:13 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 30 Dec 2025 00:06:13 GMT
VOLUME [/var/lib/postgresql]
# Tue, 30 Dec 2025 00:06:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 00:06:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Dec 2025 00:06:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Dec 2025 00:06:13 GMT
STOPSIGNAL SIGINT
# Tue, 30 Dec 2025 00:06:13 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Dec 2025 00:06:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b99a8d8dab982a1a4ea341e66b178b14c0f373c2cd90ac46a67308a4f43c82ae`  
		Last Modified: Mon, 29 Dec 2025 22:27:09 GMT  
		Size: 27.9 MB (27944146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e850f62a6257da652b7369522fe607d0d78f4c48c02f42867e3017c68f2e2219`  
		Last Modified: Tue, 30 Dec 2025 00:06:37 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd376745726a267c1ce7f3184998639a1685ea72859dada65433bde5c167ed5`  
		Last Modified: Tue, 30 Dec 2025 00:06:37 GMT  
		Size: 5.9 MB (5929065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe4fef3ee4ab0f232dbcddd6497c28f0153abcd225a56cd3f3a09fe63dafbe1`  
		Last Modified: Tue, 30 Dec 2025 00:06:37 GMT  
		Size: 1.2 MB (1227402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75351a52f89f00ffb50fe56afabbdcc9737fb30781ed8b4eabcbec9a03f9ef5`  
		Last Modified: Tue, 30 Dec 2025 00:06:38 GMT  
		Size: 8.2 MB (8204158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28d05e776b81b11b8ad9a330341a67fe2dad5d5b8f873d2db7d04e9f0a814b0`  
		Last Modified: Tue, 30 Dec 2025 00:06:37 GMT  
		Size: 1.3 MB (1317181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d573d44d4e62c5a82b1c4a75d100364c5a4d5d8bb2c028e346ba8d4b3e05cc4`  
		Last Modified: Tue, 30 Dec 2025 00:06:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8be8b725526b42fe31a04308221dfb1cdd003936427d8cf047bb0e3c5030619`  
		Last Modified: Tue, 30 Dec 2025 00:06:37 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2c4068b9b91c60b83749e9b53eb6d499c1e7cbe7aaa400110768e8a0cf11b9`  
		Last Modified: Tue, 30 Dec 2025 00:06:39 GMT  
		Size: 46.7 MB (46745217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a56bcfd69ab1275e226c3f33382a0ede1e09d78543ded5a29b8f7e4c024b960`  
		Last Modified: Tue, 30 Dec 2025 00:06:36 GMT  
		Size: 19.2 KB (19179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23be6d2cb86133dd6c40dafebbf1db405ed8980a4f5367d21e11b78b7fdfc159`  
		Last Modified: Tue, 30 Dec 2025 00:06:36 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff85275dc3b1b9342ec5ab78951512974c9f37b891537ab106e34d7b136f101`  
		Last Modified: Tue, 30 Dec 2025 00:06:37 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e6d549ce4d8bc89decf62091b421d8eeff7581bbf27b109d0aa62d7a050d10`  
		Last Modified: Tue, 30 Dec 2025 00:06:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:2bd24822b6e37473d590b2872bcaa8c80d9916d2a38069794c90878490deabaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5172295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ddbcaa2172b7a05a5f7db55562b38896b111c71cf63cf1dacd0bed4d0073c9c`

```dockerfile
```

-	Layers:
	-	`sha256:990efba2c84f85a6b3155384538c9eb4a324cd0c94cde743929f20cc69ac4349`  
		Last Modified: Tue, 30 Dec 2025 03:14:43 GMT  
		Size: 5.1 MB (5119616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c1db56f1ff7ba35ea185e405c3541feec9076a74a754531bc8342b6bdcb8df6`  
		Last Modified: Tue, 30 Dec 2025 03:14:44 GMT  
		Size: 52.7 KB (52679 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; arm variant v7

```console
$ docker pull postgres@sha256:464712d8f4851cf6419df76d346eb807e468eb625f3b30c8694a8a6ce3e4e5ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87718000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a218f7e01c399aa6518f517dc0b2581dbe90cd4be249129f0ef556fc2c725369`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:54:14 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 29 Dec 2025 23:54:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:54:30 GMT
ENV GOSU_VERSION=1.19
# Mon, 29 Dec 2025 23:54:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 29 Dec 2025 23:54:38 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 29 Dec 2025 23:54:38 GMT
ENV LANG=en_US.utf8
# Mon, 29 Dec 2025 23:54:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:54:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 29 Dec 2025 23:54:44 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 29 Dec 2025 23:54:44 GMT
ENV PG_MAJOR=18
# Mon, 29 Dec 2025 23:54:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 29 Dec 2025 23:54:44 GMT
ENV PG_VERSION=18.1-1.pgdg13+2
# Tue, 30 Dec 2025 00:06:49 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 30 Dec 2025 00:06:49 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Dec 2025 00:06:49 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Dec 2025 00:06:49 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 30 Dec 2025 00:06:49 GMT
VOLUME [/var/lib/postgresql]
# Tue, 30 Dec 2025 00:06:49 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 00:06:49 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Dec 2025 00:06:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Dec 2025 00:06:49 GMT
STOPSIGNAL SIGINT
# Tue, 30 Dec 2025 00:06:49 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Dec 2025 00:06:49 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8776ab36f241a8d0a3a854da69e3b14bca77549521ddf151231917ee7c8fcb`  
		Last Modified: Tue, 30 Dec 2025 00:07:15 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4e13a8b079abba3e235376698242657fc6d9bf3d15fcccf32b904a877ec0b2`  
		Last Modified: Tue, 30 Dec 2025 00:07:15 GMT  
		Size: 5.5 MB (5496848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4af8275c77b847da67b5b48a72110d7f0aff0cd8e49cf4d89b5babfa40698e6`  
		Last Modified: Tue, 30 Dec 2025 00:07:15 GMT  
		Size: 1.2 MB (1222284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a7f8c3d992f4a88df885758a1fec9ea0c1e6b741faaf951715bdb9bbb3219c`  
		Last Modified: Tue, 30 Dec 2025 00:07:16 GMT  
		Size: 8.2 MB (8203959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e99f946ea126429af012ab003f339ea356180731a51c342a3f737ac8c1ab60b`  
		Last Modified: Tue, 30 Dec 2025 00:07:15 GMT  
		Size: 1.2 MB (1172467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2c6fdddb8a8aacee36f7aaafe9a537bf252ebbb0426a23225ae077ca584b72`  
		Last Modified: Tue, 30 Dec 2025 00:07:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191184b4cba26733f5b786788dc4e01854bd8a1e4a92e9d58eab3c5598d981c6`  
		Last Modified: Tue, 30 Dec 2025 00:07:15 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ffc850d64fc70c9a0ebf42bb587b45621452b62a2528851786e6eeef24aeb9`  
		Last Modified: Tue, 30 Dec 2025 00:07:18 GMT  
		Size: 45.4 MB (45382661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673d8fdfc765dcab0f747c8db7f8e74f25514ed7210864fc9c9a54e174bdd8e3`  
		Last Modified: Tue, 30 Dec 2025 00:07:14 GMT  
		Size: 19.2 KB (19196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a913c2d96125d8635613c690379a5b03d88e0f2dc2aa23a6f6d7734ea5f07e`  
		Last Modified: Tue, 30 Dec 2025 00:07:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4f53fc5b0637e6ed915b13b5f0dccd74ceddb4d3ddaa07d501e097af84707b`  
		Last Modified: Tue, 30 Dec 2025 00:07:15 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d05961897c68f0d588c03b8e1c15980c6aeff9de7a8654574488f6de10636e`  
		Last Modified: Tue, 30 Dec 2025 00:07:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:e2507afc6cefa51bfc346cda689157b6c7f028b6a16a35f07f9534231c42bfb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5171597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d8168648e637fd5222398cef375b48a9c5051a17b63f4189825f8b48c7132a`

```dockerfile
```

-	Layers:
	-	`sha256:cf0de7cf40fee1797b4778e748f5fb8cbb5255d9e26f1d74e33ef8906d644f3b`  
		Last Modified: Tue, 30 Dec 2025 03:14:50 GMT  
		Size: 5.1 MB (5118921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dc4370bf068ac37579923c083ba78eece79764e45ae9efd0e73e55851d1015b`  
		Last Modified: Tue, 30 Dec 2025 03:14:50 GMT  
		Size: 52.7 KB (52676 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:6802045a43b1abc51a0acb8203b08eb59a671920de0793452d68de84b6790e99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160813724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12dd9870a01e7c8587eeacc68c76013a4d273eaa5c78cbe81aeeeca6ea0f8b3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:39:42 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 29 Dec 2025 23:39:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:39:56 GMT
ENV GOSU_VERSION=1.19
# Mon, 29 Dec 2025 23:39:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 29 Dec 2025 23:40:01 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 29 Dec 2025 23:40:01 GMT
ENV LANG=en_US.utf8
# Mon, 29 Dec 2025 23:40:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:40:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 29 Dec 2025 23:40:05 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 29 Dec 2025 23:40:05 GMT
ENV PG_MAJOR=18
# Mon, 29 Dec 2025 23:40:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 29 Dec 2025 23:40:05 GMT
ENV PG_VERSION=18.1-1.pgdg13+2
# Mon, 29 Dec 2025 23:40:23 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 29 Dec 2025 23:40:23 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 29 Dec 2025 23:40:23 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 29 Dec 2025 23:40:23 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 29 Dec 2025 23:40:23 GMT
VOLUME [/var/lib/postgresql]
# Mon, 29 Dec 2025 23:40:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:40:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 29 Dec 2025 23:40:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:40:23 GMT
STOPSIGNAL SIGINT
# Mon, 29 Dec 2025 23:40:23 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 29 Dec 2025 23:40:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876e05b0003d000a2a3906ea4bc9dde98e17926a5331a909da1021fa0abd7951`  
		Last Modified: Mon, 29 Dec 2025 23:40:54 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79af5418d01e74a3d4b0de92896cd82d5f937dd58c269f6705e2878f99e9633b`  
		Last Modified: Mon, 29 Dec 2025 23:40:55 GMT  
		Size: 6.2 MB (6231997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936d50ef2dd1b8e585bd77051eb344ce85de9632e11f6c6e92859bbb00afcbd8`  
		Last Modified: Mon, 29 Dec 2025 23:40:54 GMT  
		Size: 1.2 MB (1209480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948eb52cd9a369390f58e8054c406772aa1d68a06df3b65d2b1e6805e015f05d`  
		Last Modified: Mon, 29 Dec 2025 23:40:55 GMT  
		Size: 8.2 MB (8203922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ede6fa8de0c2ca2d9e6b97a9028cb92a51a6e4fa54b434d604fc2c4add006d0`  
		Last Modified: Mon, 29 Dec 2025 23:40:55 GMT  
		Size: 1.2 MB (1220465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41bf09d406a30a2696bc3ef906a08c9e602d02ab76ba3faa720b89898c13256c`  
		Last Modified: Mon, 29 Dec 2025 23:40:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803f571f3f58068b92261efaa1356a3f9f2749dedc28dcea91c4b0122b0238bd`  
		Last Modified: Mon, 29 Dec 2025 23:40:54 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ac7ed1200a4c254db9fab1694c407b649fbcb49a40992fe5d08942de3bdfcd`  
		Last Modified: Mon, 29 Dec 2025 23:41:02 GMT  
		Size: 113.8 MB (113779468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb6881936911d74f5c5b700368d11e5596460e61fbff303b8dcfa6f15c9184b`  
		Last Modified: Mon, 29 Dec 2025 23:40:54 GMT  
		Size: 19.2 KB (19185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0010ea57a154e97932128932be668211e44a53eb1dcec37da88d0f70883f453b`  
		Last Modified: Mon, 29 Dec 2025 23:40:54 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baaf29a813fe41d9a5601915092ee4ac726ba6b1447abfaf89c2508c4797662f`  
		Last Modified: Mon, 29 Dec 2025 23:40:54 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f602b784015adc1bc74c3087ab0f03f668504d93067f32f3494b3a95831b08c`  
		Last Modified: Mon, 29 Dec 2025 23:40:54 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:d79f59c24c1297b9f1c24780159648bf2120f6a4a7df6069fa3bccfd162a8544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6015582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b85d915b66b643594cecbafe6452b1ea79e039c9644ec36c86bdaf3a91aa92`

```dockerfile
```

-	Layers:
	-	`sha256:af316f2fab01f8ca962180b50aeba858fcc9b2ce923b1487243b5a536643ce6d`  
		Last Modified: Tue, 30 Dec 2025 01:46:23 GMT  
		Size: 6.0 MB (5962846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11e343508d8470cea08298ff3fafe6fee3fcac6b0c175832c892ef7c3dbaa76d`  
		Last Modified: Tue, 30 Dec 2025 01:46:22 GMT  
		Size: 52.7 KB (52736 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; 386

```console
$ docker pull postgres@sha256:6eb02c75bd39e35f0df4223a718a2b30fb54af6ee8ead07d1ca6dcd09d8746b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97511508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74af6a5a2e9f51a662f2463577d25b1b0ee59dce2d943d594a366b94343658b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:32:33 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 29 Dec 2025 23:32:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:32:47 GMT
ENV GOSU_VERSION=1.19
# Mon, 29 Dec 2025 23:32:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 29 Dec 2025 23:32:52 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 29 Dec 2025 23:32:52 GMT
ENV LANG=en_US.utf8
# Mon, 29 Dec 2025 23:32:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:32:55 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 29 Dec 2025 23:32:56 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 29 Dec 2025 23:32:56 GMT
ENV PG_MAJOR=18
# Mon, 29 Dec 2025 23:32:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 29 Dec 2025 23:32:56 GMT
ENV PG_VERSION=18.1-1.pgdg13+2
# Mon, 29 Dec 2025 23:41:25 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 29 Dec 2025 23:41:25 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 29 Dec 2025 23:41:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 29 Dec 2025 23:41:25 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 29 Dec 2025 23:41:25 GMT
VOLUME [/var/lib/postgresql]
# Mon, 29 Dec 2025 23:41:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:41:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 29 Dec 2025 23:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:41:25 GMT
STOPSIGNAL SIGINT
# Mon, 29 Dec 2025 23:41:25 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 29 Dec 2025 23:41:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:796ffff142a3158a5c48a8d81b8b722c5cf4889d5e22da70bdd13a6459d6e40b`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 31.3 MB (31293100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae3dbf423f72c92d0aa4386c8b460e8ddae27df4cc8faa5f8dff8a6cf3ee621`  
		Last Modified: Mon, 29 Dec 2025 23:41:39 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fed57127c0638ffe9d35cd63809396a456d99b0cd0fc626f74aefa2d3b639c`  
		Last Modified: Mon, 29 Dec 2025 23:41:48 GMT  
		Size: 6.6 MB (6629549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6262b9f7dade4b7895ad073308bc2c63e9fd43053e45a1e4fd94b3742f18bca4`  
		Last Modified: Mon, 29 Dec 2025 23:41:47 GMT  
		Size: 1.2 MB (1225707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa92cbad8996ac67570a35846e3ed0c7353327c387b51f32e84e3d0040a3ff09`  
		Last Modified: Mon, 29 Dec 2025 23:41:47 GMT  
		Size: 8.2 MB (8203974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d48f67bedf4819f3e0abc51a246d9a7a9cf6be7bbcf5d3c6df20cf842d02109`  
		Last Modified: Mon, 29 Dec 2025 23:41:47 GMT  
		Size: 1.3 MB (1308149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7399790067765deae8415e38848a64abb31e7c1334aba526e351fd259385ffe`  
		Last Modified: Mon, 29 Dec 2025 23:41:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad9eace4ecdf35d04e0257ec63c1d3622404a17305f562edb3f27760d37c8ee`  
		Last Modified: Mon, 29 Dec 2025 23:41:47 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621fee2e4ad6736a7b28797e51528d60097bd463667f5dedc9e79beecfab79ee`  
		Last Modified: Mon, 29 Dec 2025 23:41:50 GMT  
		Size: 48.8 MB (48821271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb53b51b9244d5574070a643b9a30e133909be3c5bbc07202915c6f336e16bb`  
		Last Modified: Mon, 29 Dec 2025 23:41:46 GMT  
		Size: 19.2 KB (19181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8a708b88d2a3c6b40623dea010660d1dcc70b57a4fa67ca00f934f811c25be`  
		Last Modified: Mon, 29 Dec 2025 23:41:46 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618040a412cdcb6499fd252027c5cf0be087355528910177686dd9337e996f61`  
		Last Modified: Mon, 29 Dec 2025 23:41:46 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8a1f317a9c3321dee27307312b97775120693bf717c90e5c39218a8833a2bd`  
		Last Modified: Mon, 29 Dec 2025 23:41:46 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:15e817476dc64222604e82b2b9f41c25f80829d120f653474f3b330cb891b2c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5167340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29dbea55b515225fc6b4ab858f37d8200727084b1aa29bfa8aa329e5eb5d8831`

```dockerfile
```

-	Layers:
	-	`sha256:893e9967a173bf5df9ffc4216e01bca9f0a061192289ed2d2b7411c20e9803c7`  
		Last Modified: Tue, 30 Dec 2025 03:14:59 GMT  
		Size: 5.1 MB (5114949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe648be8cda5ca5cffb5b7e0731d1171e41b1a4be3ab38ea2bebb83a97ecffd2`  
		Last Modified: Tue, 30 Dec 2025 03:15:00 GMT  
		Size: 52.4 KB (52391 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; ppc64le

```console
$ docker pull postgres@sha256:56014f544f8821260451e88ec8582214ccefcfa8512dcafa6863034c7856bb7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.6 MB (174627100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d086d48f58051eb84d47c026012b0babf098d46ff154ba03ab9856cac3188b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 17:21:44 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Dec 2025 17:21:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 17:22:15 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Dec 2025 17:22:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Dec 2025 17:22:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 30 Dec 2025 17:22:26 GMT
ENV LANG=en_US.utf8
# Tue, 30 Dec 2025 17:22:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 17:22:34 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Dec 2025 17:22:35 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 17:22:35 GMT
ENV PG_MAJOR=18
# Tue, 30 Dec 2025 17:22:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 30 Dec 2025 17:22:35 GMT
ENV PG_VERSION=18.1-1.pgdg13+2
# Tue, 30 Dec 2025 17:23:16 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 30 Dec 2025 17:23:16 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Dec 2025 17:23:17 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Dec 2025 17:23:17 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 30 Dec 2025 17:23:17 GMT
VOLUME [/var/lib/postgresql]
# Tue, 30 Dec 2025 17:23:17 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 17:23:18 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Dec 2025 17:23:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Dec 2025 17:23:18 GMT
STOPSIGNAL SIGINT
# Tue, 30 Dec 2025 17:23:18 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Dec 2025 17:23:18 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:34b56ab3c5579c93222f3403d640c7a7f19044e9e46a2d1c6b1da60bde918efc`  
		Last Modified: Tue, 30 Dec 2025 15:11:02 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4cd81b05c23469a350d322cb21f72123ba1d44e14d4440a283c5ee71814ef4`  
		Last Modified: Tue, 30 Dec 2025 17:24:15 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a30a2253ec4f0760447e76ba6721a8ef7596d865576424958de60868aa4cf2`  
		Last Modified: Tue, 30 Dec 2025 17:24:15 GMT  
		Size: 7.1 MB (7075910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0352d674c68184a954a5bf64beb9e2a7829730c2de8504f9cb8bec8f1297d3`  
		Last Modified: Tue, 30 Dec 2025 17:24:15 GMT  
		Size: 1.2 MB (1214682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5dc94c962d0003f472d053414d1ba57bbce83d60615728e29f782e289789574`  
		Last Modified: Tue, 30 Dec 2025 17:24:16 GMT  
		Size: 8.2 MB (8203984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386d1981a551614af17220e531d937e6399e976e5342c521c6e6e002ec809d9e`  
		Last Modified: Tue, 30 Dec 2025 17:24:15 GMT  
		Size: 1.4 MB (1394824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d315fcc0c298b4a56e4f1143510ee8c105410308bed29c895fba9ec2a9b18586`  
		Last Modified: Tue, 30 Dec 2025 17:24:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8b9ee641caf35f9243eef9c10e80c2389b513cd66c1dc39a50291500f237f4`  
		Last Modified: Tue, 30 Dec 2025 17:24:15 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e257830db51c6bc2905be015961d9ffac7dcf4aff4e2cd46f0e9f750e5fe6ef`  
		Last Modified: Tue, 30 Dec 2025 17:24:27 GMT  
		Size: 123.1 MB (123111048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b04b6dc854eada48fa3b13a89c203e2538f980ae59ba81fbd9e97a969101deb`  
		Last Modified: Tue, 30 Dec 2025 17:24:15 GMT  
		Size: 19.2 KB (19184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66a300e55dd88604e56bb17b10064ffa7f0a211e853abb2eab75f3b67c4c1b0`  
		Last Modified: Tue, 30 Dec 2025 17:24:15 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428edf9448039a959f7519d606eddb8578d9bd004ebef5da15e8ab38fa21f7d1`  
		Last Modified: Tue, 30 Dec 2025 17:24:16 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a725f8a8e0616a4c0f031fafe02a4d8d3109628df82d32e5a071c29ce8387cab`  
		Last Modified: Tue, 30 Dec 2025 17:24:16 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:5f41a12e4803ba0d2aecfa22b71ce34332ba410404df674bcbc81852097fa005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6015655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc446253a369a97808b526e4e268640939df1c424879d991b7f9ed326474e8e7`

```dockerfile
```

-	Layers:
	-	`sha256:89622c7784d13f8d57d4910039d901f0b3d27a37a17ae67485ac76c815661f3b`  
		Last Modified: Tue, 30 Dec 2025 18:09:50 GMT  
		Size: 6.0 MB (5963121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6913468cf7be6039530213dc90c187838b6809892d954e7189f800fb45a16917`  
		Last Modified: Tue, 30 Dec 2025 18:09:51 GMT  
		Size: 52.5 KB (52534 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; riscv64

```console
$ docker pull postgres@sha256:3483d44dccd1a12a7c43e61fc1e5e2a026377fa1c9728c89c19c2d7ba88ff3e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92795577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21766b5dae8eeeb4e070809d081a7603d39357cab766970a0a7417e6a3bf1cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Wed, 31 Dec 2025 01:09:46 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 31 Dec 2025 01:10:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Dec 2025 01:11:38 GMT
ENV GOSU_VERSION=1.19
# Wed, 31 Dec 2025 01:11:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 31 Dec 2025 01:12:37 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 31 Dec 2025 01:12:37 GMT
ENV LANG=en_US.utf8
# Wed, 31 Dec 2025 01:13:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Dec 2025 01:13:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 31 Dec 2025 01:13:18 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 31 Dec 2025 01:13:18 GMT
ENV PG_MAJOR=18
# Wed, 31 Dec 2025 01:13:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Wed, 31 Dec 2025 01:13:18 GMT
ENV PG_VERSION=18.1-1.pgdg13+2
# Wed, 31 Dec 2025 03:16:01 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 31 Dec 2025 03:16:02 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 31 Dec 2025 03:16:02 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 31 Dec 2025 03:16:02 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 31 Dec 2025 03:16:02 GMT
VOLUME [/var/lib/postgresql]
# Wed, 31 Dec 2025 03:16:02 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 31 Dec 2025 03:16:03 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 31 Dec 2025 03:16:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Dec 2025 03:16:03 GMT
STOPSIGNAL SIGINT
# Wed, 31 Dec 2025 03:16:03 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 31 Dec 2025 03:16:03 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e70644e1c09f8e035d52f884531a7fd757a338e9fc82c3df70e6ea742f3f8d`  
		Last Modified: Wed, 31 Dec 2025 03:18:54 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5d9c8bb5d8629d6a733e124d23e3279af6396cad87aede4113ead652bc91ac`  
		Last Modified: Wed, 31 Dec 2025 03:18:54 GMT  
		Size: 6.3 MB (6291325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1caec3152eff7c8d79f440391af043fcc9bd9d042b004ad0b2d21cb93a4b73ab`  
		Last Modified: Wed, 31 Dec 2025 03:18:54 GMT  
		Size: 1.2 MB (1201915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4962a2e0dc0a8e3514297eb06f8d97aedc52572c2643a0373594a541e725ad35`  
		Last Modified: Wed, 31 Dec 2025 03:18:55 GMT  
		Size: 8.2 MB (8203621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306e759ea1f4577acb671ce8388eb9c8aade4af0fc33d9c06c6bf52fd096fa97`  
		Last Modified: Wed, 31 Dec 2025 03:18:54 GMT  
		Size: 1.4 MB (1402241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a422cab0904301076eacc31fd289d89c712925611b7fcc4abef5a27034fa1f`  
		Last Modified: Wed, 31 Dec 2025 03:18:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49014b439d452cc891588c4fcf6687fc5883506ab8a3368c86f9968353e4647`  
		Last Modified: Wed, 31 Dec 2025 03:18:54 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebcf23a0d2a8970aaa20020964fb6595772cd7e847d32ec1861640fdbb9a7e3b`  
		Last Modified: Wed, 31 Dec 2025 03:18:57 GMT  
		Size: 47.4 MB (47393574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b30da880f84380bf79ed68a35277186482e424f28718cd08e329a77f11ed1f`  
		Last Modified: Wed, 31 Dec 2025 03:18:54 GMT  
		Size: 19.2 KB (19192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ce45448a527d6dd64e72333c128b29491cfe882edf57fd02323819bf9cebcd`  
		Last Modified: Wed, 31 Dec 2025 03:18:54 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da575d48d06f8cd7cd6d4b4f2cdf0f9002eae6159a5d55a19690c057ad6c59d`  
		Last Modified: Wed, 31 Dec 2025 03:18:52 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2101f4415f9ab5edf818feab547852f9d814d568cce71ce61a31846d40e7d840`  
		Last Modified: Wed, 31 Dec 2025 03:18:53 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:daf99d8a3e1dda3629d145e55a5309ff1c239d4b8a81e7628b10c6b05ce5db8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5162418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20aecaf39d5d3d37376461680f39abffbc10f65623c737a577d77da244970254`

```dockerfile
```

-	Layers:
	-	`sha256:2c46852d78d1ec44b4f47ea2a2e945b1af054064dbf19212fab2bcf73a653696`  
		Last Modified: Wed, 31 Dec 2025 06:08:51 GMT  
		Size: 5.1 MB (5109889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee2a123ea5a20bbe4f2deed7e1c9d1fd532d0cd400db1427a054f7343a310604`  
		Last Modified: Wed, 31 Dec 2025 06:08:51 GMT  
		Size: 52.5 KB (52529 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; s390x

```console
$ docker pull postgres@sha256:5fa423f0248a7b4a20b09fc5776c580fe3638a6239265f2e306304b9d370066d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.8 MB (176849724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd70ac58461eee85b5680ffd522aeab2b9887cc1ff6d449fa83d917b79fa9ca7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:04:05 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Dec 2025 00:04:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:04:19 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Dec 2025 00:04:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Dec 2025 00:04:24 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 30 Dec 2025 00:04:24 GMT
ENV LANG=en_US.utf8
# Tue, 30 Dec 2025 00:04:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:04:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Dec 2025 00:04:29 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:04:29 GMT
ENV PG_MAJOR=18
# Tue, 30 Dec 2025 00:04:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 30 Dec 2025 00:04:29 GMT
ENV PG_VERSION=18.1-1.pgdg13+2
# Tue, 30 Dec 2025 00:16:39 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 30 Dec 2025 00:16:40 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Dec 2025 00:16:40 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Dec 2025 00:16:40 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 30 Dec 2025 00:16:40 GMT
VOLUME [/var/lib/postgresql]
# Tue, 30 Dec 2025 00:16:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 00:16:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Dec 2025 00:16:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Dec 2025 00:16:40 GMT
STOPSIGNAL SIGINT
# Tue, 30 Dec 2025 00:16:40 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Dec 2025 00:16:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c9a83915f7d4b9d7fbe5dceeedd49718d2702fd67d78b63a38ec344f3fbfcc41`  
		Last Modified: Mon, 29 Dec 2025 22:27:07 GMT  
		Size: 29.8 MB (29834418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03bd633819322cb11cc9513c226982c942eac3e48bfea2d0beb19c3ebd3e150`  
		Last Modified: Tue, 30 Dec 2025 00:17:22 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015fcb425b0e0871d518edcad4b32033422d0610ee48d41f3288482f4fec20f5`  
		Last Modified: Tue, 30 Dec 2025 00:17:23 GMT  
		Size: 6.4 MB (6408815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92c8bb518bee6ea32d2d42baa957da796efc96dc7ced791f56e79c49a0295c5`  
		Last Modified: Tue, 30 Dec 2025 00:17:22 GMT  
		Size: 1.2 MB (1230094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8535702b3710c6fcd3201da506474e2b1283cf1944f25e878d3fd583f7677efd`  
		Last Modified: Tue, 30 Dec 2025 00:17:23 GMT  
		Size: 8.3 MB (8258860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d63ed103a386eaf5a068332156cd65d9319160774cf86554445beccd47ee9ad`  
		Last Modified: Tue, 30 Dec 2025 00:17:22 GMT  
		Size: 1.4 MB (1398084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2dd9df4f9a1797f74af4c2cdd546b3644f6a67e7f305b3faa9f6dfbff69a69`  
		Last Modified: Tue, 30 Dec 2025 00:17:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f900bfe654117b3bae9e4f7f94414bf575d933fd78fd8dc60edada8ee0c14818`  
		Last Modified: Tue, 30 Dec 2025 00:17:22 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabf5c323b6d214b240abecf6d5232ea760119badf79cfe621ba0c7458aa1c2b`  
		Last Modified: Tue, 30 Dec 2025 00:17:32 GMT  
		Size: 129.7 MB (129689691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75aeffb6420aedf6d36d43fc66fd3b4e97861eede0973a8821fb0687ed9b21e`  
		Last Modified: Tue, 30 Dec 2025 00:17:22 GMT  
		Size: 19.2 KB (19186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37cc1aef33c37c744ec7dae906e567de54d080caf4ed0d16c03877b150aa3923`  
		Last Modified: Tue, 30 Dec 2025 00:17:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488eee5d793bc9183e26eba37b264bc82c002047c2b06ab797ca688c64a551ae`  
		Last Modified: Tue, 30 Dec 2025 00:17:23 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7df89b26295c37416918e16f360f2926bad271a9e79ba4170b883d02e9a9be`  
		Last Modified: Tue, 30 Dec 2025 00:17:23 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:e4addc54e0c5e7e52b9c93bc7ab17e2e94805661612e20474b15308689b4e41d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6025601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:402f6028d62f8521fbda87ab2f557a28ab0ab5d6491ad4d20995697b31d1f2d7`

```dockerfile
```

-	Layers:
	-	`sha256:b2a43f378312e676af28fd89b0d0458724c251c8f497be0da76b2c14bbb28bb1`  
		Last Modified: Tue, 30 Dec 2025 03:15:13 GMT  
		Size: 6.0 MB (5973143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bb7c607a3ae40148860bb5a39ee23d472ccdfd9a5e99665b814aca8c529efb8`  
		Last Modified: Tue, 30 Dec 2025 03:15:14 GMT  
		Size: 52.5 KB (52458 bytes)  
		MIME: application/vnd.in-toto+json
