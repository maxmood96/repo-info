## `postgres:16-bookworm`

```console
$ docker pull postgres@sha256:b7a6dc699779d21c30b016faa2c1facb37ccdc56ceafd27eb70d7816b12b7f2e
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

### `postgres:16-bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:de3f8ec47fa7cde1a4a32519a48100aee8db920cc6b33e7afa8c13e972c46fe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.0 MB (154997279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b129144af90db992aeadfda1d2d6793a8cf4ed877e7f307d27ee11ac3afda83`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 19:17:54 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:17:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:18:05 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:18:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:18:10 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 14 Nov 2025 19:18:10 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:18:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:18:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:18:14 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 14 Nov 2025 19:18:14 GMT
ENV PG_MAJOR=16
# Fri, 14 Nov 2025 19:18:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Fri, 14 Nov 2025 19:18:14 GMT
ENV PG_VERSION=16.11-1.pgdg12+1
# Fri, 14 Nov 2025 19:18:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:18:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:18:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:18:27 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:18:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:18:27 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:18:27 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:18:27 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:18:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:18:27 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:18:27 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:18:27 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c4956c224dac432c2dff80a28a89aecb4063ade3a2273f89dd2c3299034b96`  
		Last Modified: Fri, 14 Nov 2025 19:19:09 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36bdc1779a1600b2c9cf4e51e9fff730c2bda27add8ded970394c59910024e0`  
		Last Modified: Fri, 14 Nov 2025 19:19:10 GMT  
		Size: 4.5 MB (4534104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d65e0e59d8bce336a87025baf26fff56811cc1bf94ce88000158227b5b9b2da`  
		Last Modified: Fri, 14 Nov 2025 19:19:09 GMT  
		Size: 1.2 MB (1249492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8cba7d30ba6d3e8032f55f2ccaea1bcbbe0c8ee7747416d14c5eadf332331f3`  
		Last Modified: Fri, 14 Nov 2025 19:19:09 GMT  
		Size: 8.1 MB (8066471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6a8f55a61cd6cfe6cf8e3769b55a678ba930a2f766a827b50d3a6c1c6ed6da`  
		Last Modified: Fri, 14 Nov 2025 19:19:09 GMT  
		Size: 1.2 MB (1196406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8438d895aa4200e8e017a198ece65ac57cc0c1cfbe22f1ca8323746e4f109d34`  
		Last Modified: Fri, 14 Nov 2025 19:19:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60acc70d7b69e4882a8f2cc052ba437d60eabe8160795485102b5eee4b1794f4`  
		Last Modified: Fri, 14 Nov 2025 19:19:08 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2f8a89c730294fdfcdc95953404aa16167d5b10e35f555f034d26b4f9f79ab`  
		Last Modified: Fri, 14 Nov 2025 19:19:22 GMT  
		Size: 111.7 MB (111701569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3a01bd6b03d41a15d1568d7f90825607a87526c562f5211a86acad138f6991`  
		Last Modified: Fri, 14 Nov 2025 19:19:09 GMT  
		Size: 9.9 KB (9920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8780632cce8ad0a018d9fe9a206876c7d8f8941ac52837513590ce75d434b11`  
		Last Modified: Fri, 14 Nov 2025 19:19:08 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12ba42e856a72e8c76a2c4fe376c5b31bb7ab73829eb14fb95a60c09c587ecd`  
		Last Modified: Fri, 14 Nov 2025 19:19:09 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7a84b72b6cf58fb68c712edee004a8deed85517a511dbbc05c5dd2f60075a5`  
		Last Modified: Fri, 14 Nov 2025 19:19:09 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b24badbd635ae310b723c8348c62fe560211134f7f697acc822954cb395f662`  
		Last Modified: Fri, 14 Nov 2025 19:19:09 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:021e87983bd7bcda390c3965b2137d81eb9617ed878e33f5eb8d19cc8c657624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5962842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a692da51e64711e8f143547944dad5a531d92cf8ec3c24431c0ca91a2ce734e9`

```dockerfile
```

-	Layers:
	-	`sha256:a29db31a7dbb94d40db9acb4281111bfb21ab1a78e22bf64aa664705ddf49a84`  
		Last Modified: Fri, 14 Nov 2025 21:14:11 GMT  
		Size: 5.9 MB (5909546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:779da23ffabe719623bdf88897d731ae8a590f71fd7659cff6698ce621e35877`  
		Last Modified: Fri, 14 Nov 2025 21:14:11 GMT  
		Size: 53.3 KB (53296 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:99fcd8b4eba8ae43c664db89d776fd80000188cb19cb8dfc5b4cac17bf5727fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.0 MB (148013060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d70dac6dbb8050dfc02c56d2664663e1acff01dfa356335394ae490db0f468b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 19:20:34 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:20:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:20:50 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:20:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:20:57 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 14 Nov 2025 19:20:57 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:21:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:21:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:21:04 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 14 Nov 2025 19:21:04 GMT
ENV PG_MAJOR=16
# Fri, 14 Nov 2025 19:21:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Fri, 14 Nov 2025 19:21:04 GMT
ENV PG_VERSION=16.11-1.pgdg12+1
# Fri, 14 Nov 2025 19:48:22 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:48:22 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:48:23 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:48:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:48:23 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:48:23 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:48:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:48:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:48:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:48:23 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:48:23 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:48:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:def4b77141116a067c72a4f39eb9fa70634fe918be6e3df3cf0bc46323be22c7`  
		Last Modified: Tue, 04 Nov 2025 00:12:34 GMT  
		Size: 25.8 MB (25757661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6583851563050769ee9d66e953595803d0660b93501f859dd0e4e834c50af15d`  
		Last Modified: Fri, 14 Nov 2025 19:33:23 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57837587cccf38cee37d36508883fadea3a1bc45ca9f676d6332d4e4482a640e`  
		Last Modified: Fri, 14 Nov 2025 19:33:24 GMT  
		Size: 4.2 MB (4151199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4234ab4d68babd468e42864e5d626fca698892d57c366f86d6edcb725a0543c5`  
		Last Modified: Fri, 14 Nov 2025 19:33:24 GMT  
		Size: 1.2 MB (1220023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ab2854fe8852acd87f4e247a98470a46ca1dce3936a7f11c53357d07c221fd`  
		Last Modified: Fri, 14 Nov 2025 19:33:24 GMT  
		Size: 8.1 MB (8066546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8adec54aacb827f25be150e2908c0b61935ea35908844f61351f7d3a71381b`  
		Last Modified: Fri, 14 Nov 2025 19:33:24 GMT  
		Size: 1.2 MB (1195048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69afa08689788200ad601332c147cc264897187f00acf99386ddd37dcdcb449b`  
		Last Modified: Fri, 14 Nov 2025 19:33:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68386c1c0b54a25e093c27669e9fbcd81164ef652f7a998b35d2a3279c94c73`  
		Last Modified: Fri, 14 Nov 2025 19:33:23 GMT  
		Size: 3.1 KB (3147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f6c94e72fe0ba2955af1083aa249cdabf329154c08b17604330bff26a2a6d6`  
		Last Modified: Fri, 14 Nov 2025 20:09:34 GMT  
		Size: 107.6 MB (107601905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07b6ebc2b8274f304bb39d30a174566c480e51bf0275de6268a75ee6fcf448c`  
		Last Modified: Fri, 14 Nov 2025 20:09:25 GMT  
		Size: 9.9 KB (9929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610cb3f5d1339e41fd6f0879771627739852fceb62a97daf6115003dd14daf36`  
		Last Modified: Fri, 14 Nov 2025 20:09:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f942000549c6997fb5535fdc3958e58f253aaea18bf0426e8cdc02b3d1f6e8c3`  
		Last Modified: Fri, 14 Nov 2025 20:09:25 GMT  
		Size: 165.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd7ce092ceac4fb089cb29ac00a16ffb23eec5fd82fac721a64bab75fb601ac`  
		Last Modified: Fri, 14 Nov 2025 20:09:25 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c89c92df49638de55c82a64b7bf08bfdd142608afaca45fefc4fcf73661b94`  
		Last Modified: Fri, 14 Nov 2025 20:09:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:72cfedcab762792297bb21c05e63dd2032585f4317d6f11eece631d203dca50b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5981145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c99b022d8a79c736db11f4f989f169a225fe8e3baf3c9f39b9b6869a59b36b`

```dockerfile
```

-	Layers:
	-	`sha256:85ebd6a98eb9bfd18e29863bb5bb6e077e5ce32142a140417f8796e210410dce`  
		Last Modified: Fri, 14 Nov 2025 21:14:18 GMT  
		Size: 5.9 MB (5927643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da0cec99eeddf27ed52a061d3cd1c72d83c7a46e76fec2cb3c971cdbcd3d9c38`  
		Last Modified: Fri, 14 Nov 2025 21:14:19 GMT  
		Size: 53.5 KB (53502 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:9ccbd42cec48335d66e466f280a39509e2518e7b5472f31c63d91097ad9ca427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143061149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05eb9e97e5c4e705838d8847e523066082162040f52604489e380e7f503956db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 19:40:58 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:41:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:41:12 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:41:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:41:18 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 14 Nov 2025 19:41:18 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:41:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:41:22 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:41:22 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 14 Nov 2025 19:41:22 GMT
ENV PG_MAJOR=16
# Fri, 14 Nov 2025 19:41:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Fri, 14 Nov 2025 19:41:22 GMT
ENV PG_VERSION=16.11-1.pgdg12+1
# Fri, 14 Nov 2025 19:55:43 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:55:43 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:55:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:55:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:55:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:55:43 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:55:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:55:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:55:44 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:55:44 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:55:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:dae611a010be6eab1cdff516b7db8214a5d92b74372702ade8cd5e6bb793dfdd`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 23.9 MB (23934126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd4dbedfce4b831cdcac49d212348161567c932105799d27992396d3635db35`  
		Last Modified: Fri, 14 Nov 2025 19:56:12 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e8dd7ec59c7c62d727a044beac2c600f123626c35464a433f628da7993ab54`  
		Last Modified: Fri, 14 Nov 2025 19:56:12 GMT  
		Size: 3.7 MB (3742642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bdf504f965f6d56e70081dfa3ed4c4da7128afc6e7572a25ef5dae513389c9`  
		Last Modified: Fri, 14 Nov 2025 19:56:12 GMT  
		Size: 1.2 MB (1215982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3099367a7ff2bba53cfeab5fe6a0469d6bf51508b2788a206e1a3ba97556233f`  
		Last Modified: Fri, 14 Nov 2025 19:56:12 GMT  
		Size: 8.1 MB (8066408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92501614059fc89db8d7c4dfc3bac83c9f319d4ce73a5d1d6bd79f54b979ca1`  
		Last Modified: Fri, 14 Nov 2025 19:56:12 GMT  
		Size: 1.1 MB (1067264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e0980ce632c3b9e2afd02fed219310237fff01f516c2273ed8e52a54bcc547`  
		Last Modified: Fri, 14 Nov 2025 19:56:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d449c4a1435f1805cf3188433f084c0c3cf9a88c1a34378a99d49cffe4a2d44`  
		Last Modified: Fri, 14 Nov 2025 19:56:11 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffcf3fd7a501111c984416734d7ad2f98548cacc01a28ce81b3df407ad020f89`  
		Last Modified: Fri, 14 Nov 2025 19:56:18 GMT  
		Size: 105.0 MB (105014056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b4597ec9cc1a41507e7fe0e58f168daa2df6b2344c3be35d56beaf9c3e5adf`  
		Last Modified: Fri, 14 Nov 2025 19:56:12 GMT  
		Size: 9.9 KB (9927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8d8179afa4b848f3ad3ece50bf7046b5f0f1aeb398255ce1e325fa8dd6106f`  
		Last Modified: Fri, 14 Nov 2025 19:56:12 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64839fa4cdb6b56e0e959487c1601ee5a10dad1173930a1036ef0e12fb39f724`  
		Last Modified: Fri, 14 Nov 2025 19:56:11 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4a5c5fd2fd1ce725f380a9a44afdbdf384ff1cdd698352e0b2ec449aa0b744`  
		Last Modified: Fri, 14 Nov 2025 19:56:11 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0de2604bfe83f0e15c5e462afeae1579aeae147845676ff3f17b25236fb638a`  
		Last Modified: Fri, 14 Nov 2025 19:56:11 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:775a4abff5e902bd7761aa8b0b3d1d3b35479b2da98812b6040d426384968716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5980401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be89fbadd2fee6bd61daf42aee597ddf5e435812a507514b96e714edf64e583`

```dockerfile
```

-	Layers:
	-	`sha256:c9efd5a0b823f7d0c4371e73a387f93603365cac23a80609d6816be942a2d2ed`  
		Last Modified: Fri, 14 Nov 2025 21:14:25 GMT  
		Size: 5.9 MB (5926898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3d9a78ef704efbb2ba2515f713be7c358dc651a0a2ae2fd1779ccd513c562db`  
		Last Modified: Fri, 14 Nov 2025 21:14:26 GMT  
		Size: 53.5 KB (53503 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:f1da3d416da075792c78dd08e75286be388da53bd743061b8aae96f4a2ce0f9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.0 MB (152985347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ccd242a2f9f26b392abaf2c7e947fece76e9b84ea952d1b0c042f4bdbe6c8db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 19:18:31 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:18:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:18:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:18:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:18:50 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 14 Nov 2025 19:18:50 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:18:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:18:53 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:18:54 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 14 Nov 2025 19:18:54 GMT
ENV PG_MAJOR=16
# Fri, 14 Nov 2025 19:18:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Fri, 14 Nov 2025 19:18:54 GMT
ENV PG_VERSION=16.11-1.pgdg12+1
# Fri, 14 Nov 2025 19:19:08 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:19:08 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:19:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:19:09 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:19:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:19:09 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:19:09 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:19:09 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:19:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:19:09 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:19:09 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:19:09 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc7a22fb0061115604a4cbe62d898a91e73dbf2acaae73b1c323203d1a89a80`  
		Last Modified: Fri, 14 Nov 2025 19:19:40 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25153ce3c101af4710165dc1c694eee6721417497ec398d362716e571b4a25ba`  
		Last Modified: Fri, 14 Nov 2025 19:19:40 GMT  
		Size: 4.5 MB (4519767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9889f2e03ff2b8690de91cb14228824587feb529bd2405cb3c356bd92fc4f7`  
		Last Modified: Fri, 14 Nov 2025 19:19:40 GMT  
		Size: 1.2 MB (1203241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8a9ba71895df4f148b347f5560f240efe0c4df38ab3b5dc642915219e3c3cc`  
		Last Modified: Fri, 14 Nov 2025 19:19:41 GMT  
		Size: 8.1 MB (8066445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e6ea7bc0fbcfee3cd88ed800baa8a0261d53846a58ff5398c5058e095c7539`  
		Last Modified: Fri, 14 Nov 2025 19:19:40 GMT  
		Size: 1.1 MB (1108976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f992d4fdce490df33287772e92b3fca5960a360c7755f503a0aff6264e22419`  
		Last Modified: Fri, 14 Nov 2025 19:19:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7871dbb2829779681e459952745a239057d0d0bb9e5c71daa6d3b1f25b71190`  
		Last Modified: Fri, 14 Nov 2025 19:19:40 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2b871039ad37084c9f080bdae0c49b7e676804a2c475e7cfe6625ea4972cc6`  
		Last Modified: Fri, 14 Nov 2025 19:19:52 GMT  
		Size: 110.0 MB (109963870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c122ab6cd88bac52ddc3e20f5dc8996c82eef1f4832e12e09977de88b8983d7a`  
		Last Modified: Fri, 14 Nov 2025 19:19:41 GMT  
		Size: 9.9 KB (9922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e274b8614011bffb580665cf1425b58cff23d18374a482a90c26d6333c3894a`  
		Last Modified: Fri, 14 Nov 2025 19:19:43 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccf143e9a5fcf296d67ad219e6868e7f364c8341e71ff9b7f2ab5734ac86f27`  
		Last Modified: Fri, 14 Nov 2025 19:19:41 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596366fa61486c2b0835d437719c623e577060ba3df8cf5595ecb0b4f1a7434c`  
		Last Modified: Fri, 14 Nov 2025 19:19:40 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b4da7e64bdc848fe1c6e330d6f278f79020895fbad5d1630ae7fcd08046ed5`  
		Last Modified: Fri, 14 Nov 2025 19:19:41 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:778ae2031beddcf347773b4ab6ff7312fb748b3a8e44cd39a3b98408e7418e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5969398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a425283285967d14187587c02b90b34c69ad4369402431206c6a7acb992fe420`

```dockerfile
```

-	Layers:
	-	`sha256:c44f9ec259f94b928dd5ba9bb7fb9214105ff37bd16ae43c5cfe9dc14402154d`  
		Last Modified: Fri, 14 Nov 2025 21:14:31 GMT  
		Size: 5.9 MB (5915857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53c52b9bed77ad0a20524d86cbbf2a7c34473039830ec2fc6ca36f8c1b34fe36`  
		Last Modified: Fri, 14 Nov 2025 21:14:32 GMT  
		Size: 53.5 KB (53541 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:29d604ea584cdf9fffd5b89df5140f1a267f2a3d5bc7361908baed4153f4160e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.8 MB (163785225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037f75d8fbf8fad53319d063f9ec5415f46f3a45a4873ebc7e1bf1f0c116d9c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 19:19:26 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:19:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:19:37 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:19:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:19:42 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 14 Nov 2025 19:19:42 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:19:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:19:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:19:45 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 14 Nov 2025 19:19:45 GMT
ENV PG_MAJOR=16
# Fri, 14 Nov 2025 19:19:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Fri, 14 Nov 2025 19:19:45 GMT
ENV PG_VERSION=16.11-1.pgdg12+1
# Fri, 14 Nov 2025 19:29:53 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:29:53 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:29:54 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:29:54 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:29:54 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:29:54 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:29:54 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:29:54 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:29:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:29:54 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:29:54 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:29:54 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e0dafb38d1608fdb0908090be60250d2f739b5a9191857a4c4a74ebd3ef3b814`  
		Last Modified: Tue, 04 Nov 2025 00:12:54 GMT  
		Size: 29.2 MB (29209846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe787a3431f3ee663793442a1607d0cf8e5db997f5fb9988003cd68db1f565b`  
		Last Modified: Fri, 14 Nov 2025 19:30:24 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e1b5094c8dea2edc7d2993a55186c1fa9528ef1e17f372d4c42adad09f522a`  
		Last Modified: Fri, 14 Nov 2025 19:30:25 GMT  
		Size: 5.0 MB (4965332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b76f34dcac0829a846274f4659a91e1e41f533d977358815b5a5fcc02ef3e3`  
		Last Modified: Fri, 14 Nov 2025 19:30:24 GMT  
		Size: 1.2 MB (1218605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6491151e9d0c8926730c7978d1a4b3324240c0b9d5d527035574fe13b86b6f43`  
		Last Modified: Fri, 14 Nov 2025 19:30:25 GMT  
		Size: 8.1 MB (8066428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ee9ec53a97045053dbbbad8dade881ae759a306ef8fc07c3befdf58a0fd388`  
		Last Modified: Fri, 14 Nov 2025 19:30:24 GMT  
		Size: 1.1 MB (1137420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c42e8f05199a8da8f9f3529c37dbac5dd5116f9058ff5eb0bf9715853d1658`  
		Last Modified: Fri, 14 Nov 2025 19:22:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810672cbbe382e3c58e4c7ce1da672f3535a2525c78412f20023899169ad0e04`  
		Last Modified: Fri, 14 Nov 2025 19:30:24 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27118c43d7d19b80020bda46d116b5afb2d28cee0cafdc28bedc779c218ac41`  
		Last Modified: Fri, 14 Nov 2025 19:30:41 GMT  
		Size: 119.2 MB (119166920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9481b245d84447f461f8f0ac2ec57daa544fa3630fa41d36b8bf439a59d263da`  
		Last Modified: Fri, 14 Nov 2025 19:30:24 GMT  
		Size: 9.9 KB (9929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33fa167b7ec68aadf98273ad3b9e5b2430a2989fbd9f814001fc6a897715d704`  
		Last Modified: Fri, 14 Nov 2025 19:30:25 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ccbc87ffd683e44565a0b0a06fc2297afd38d331caa1e38378165325855601e`  
		Last Modified: Fri, 14 Nov 2025 19:30:24 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7970e91ee8f4241ae74ed1febd9d329cecf016e6f8bead98eec0378f462243`  
		Last Modified: Fri, 14 Nov 2025 19:30:25 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2664f026dec0cb391d7c90b732fb702774414cad425059c719a7286a04e58ee`  
		Last Modified: Fri, 14 Nov 2025 19:30:24 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:e759b920daed7d8d86c24c7deef3b54e1dcd0e5495c234b35a1fe7993c825d08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5979038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9502011d4ef8899208263848cf007dcc4f8437fa947b270cd8891312adeb317e`

```dockerfile
```

-	Layers:
	-	`sha256:5d0e665ae3592b11d2b17a25a794726afc7bdbe6dbb528407f7b225473c82c18`  
		Last Modified: Fri, 14 Nov 2025 21:14:38 GMT  
		Size: 5.9 MB (5925786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0078bfa396cd956857e8c29288a3c1af036787b46dbbe8d1be732722a920881`  
		Last Modified: Fri, 14 Nov 2025 21:14:39 GMT  
		Size: 53.3 KB (53252 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:cdba0a0da8acba22f81b34622872599a83adc107e58d43e2dfb391283a24a374
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.9 MB (153858023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2b730e64c52c4f01b9982e33bad8a8b581ea3814e5575ac700c4beca3a7d043`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1762202650'
# Thu, 13 Nov 2025 21:05:11 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Nov 2025 21:05:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 21:06:17 GMT
ENV GOSU_VERSION=1.19
# Thu, 13 Nov 2025 21:06:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Nov 2025 21:06:42 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 13 Nov 2025 21:06:42 GMT
ENV LANG=en_US.utf8
# Thu, 13 Nov 2025 21:06:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 21:07:00 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 21:07:02 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 21:07:02 GMT
ENV PG_MAJOR=16
# Thu, 13 Nov 2025 21:07:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 13 Nov 2025 21:07:02 GMT
ENV PG_VERSION=16.11-1.pgdg12+1
# Fri, 14 Nov 2025 00:41:28 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 14 Nov 2025 00:41:31 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 00:41:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 00:41:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 00:41:34 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 00:41:34 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 20:30:38 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 20:30:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 20:30:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 20:30:40 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 20:30:40 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 20:30:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:86a398000765b1c4b7c071dc9cc165bf6a4cd12fe05016be099c4927b331abf2`  
		Last Modified: Tue, 04 Nov 2025 00:11:46 GMT  
		Size: 28.5 MB (28513928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5897551a2552577c61ce4f6d3e050bbbbd0995790b8b73fd7cdc49d9b055ca0d`  
		Last Modified: Thu, 13 Nov 2025 22:20:56 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b9405847d098fc620886493e72f0e5dcfa97b75cd6a9d59224eadd9cf8bf61`  
		Last Modified: Thu, 13 Nov 2025 22:20:57 GMT  
		Size: 4.5 MB (4475523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86912819250b1edacb6275958b1d6055f3687a17efc34555ca245fa2a3f316a9`  
		Last Modified: Thu, 13 Nov 2025 22:20:56 GMT  
		Size: 1.2 MB (1159224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015e6a2dc648c577e7ac47c1e80d70878a92c9f27c134326e965177da8792833`  
		Last Modified: Thu, 13 Nov 2025 22:20:58 GMT  
		Size: 8.1 MB (8066657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa007178d718a756ccdfbeb8c247a03eda9ad3dc8be24dd059f059232f3a6add`  
		Last Modified: Thu, 13 Nov 2025 22:20:56 GMT  
		Size: 1.2 MB (1182940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690eb075c7ebd3f7bcca7651222ff06cc5008a2d145c481e10ab2a986b8028bd`  
		Last Modified: Thu, 13 Nov 2025 22:20:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4975fe054767ad80c6798f32c109fc8599d39e4529f526f5ebc589b754ed5120`  
		Last Modified: Thu, 13 Nov 2025 22:20:56 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a82a9aebf81ce983bc4ae71f336d87f8f3670706c34837bf4a03f9bfd5bec7`  
		Last Modified: Fri, 14 Nov 2025 00:44:03 GMT  
		Size: 110.4 MB (110439074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f15695dba45940eef7f7ed0d0bdc65046d19fd4b7b22154651f77dabde6f4cfb`  
		Last Modified: Fri, 14 Nov 2025 00:43:55 GMT  
		Size: 9.9 KB (9926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0a4503a5992d7f76dbbbfcc3af82d556f3b506e67948a03843366c2e912655`  
		Last Modified: Fri, 14 Nov 2025 00:43:55 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ab33694cd0d0535a01a348bdea4d2b33ac6e4ff568e567205d75f71122118b`  
		Last Modified: Fri, 14 Nov 2025 00:43:55 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8795f48e9ac7abe173fc6071ab0830683494e30428433b46a3b87baadde13f3e`  
		Last Modified: Fri, 14 Nov 2025 20:31:15 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24ebb752020391a6c5731784d018cadcedae68456980f6d1e61a5c0b967d680`  
		Last Modified: Fri, 14 Nov 2025 20:31:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:df38623a24e1874491afffb3b502fd6cef6db4e4b15edf846cc8ab2b33e1ad88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 KB (53162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c28ff4e15a1ae45eab49628a1e119c9ded2f949bb929ae7454d14af3b2ab14`

```dockerfile
```

-	Layers:
	-	`sha256:b67ee821466f8d185e561dc433c1a9d7ba32a642e6415483e4dcbeba3722947a`  
		Last Modified: Fri, 14 Nov 2025 21:14:43 GMT  
		Size: 53.2 KB (53162 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:4981b564c16634ef3c5320535e4cefb95d85e430c82d95611272994bd905780d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167757874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2257242a2682441eb6d0e991b14db43a04975dd906053c774b29c9ccc04856e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Thu, 13 Nov 2025 21:06:20 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Nov 2025 21:06:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 21:06:41 GMT
ENV GOSU_VERSION=1.19
# Thu, 13 Nov 2025 21:06:41 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Nov 2025 21:06:49 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 13 Nov 2025 21:06:49 GMT
ENV LANG=en_US.utf8
# Thu, 13 Nov 2025 21:06:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 21:06:55 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 21:06:56 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 21:06:56 GMT
ENV PG_MAJOR=16
# Thu, 13 Nov 2025 21:06:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 13 Nov 2025 21:06:56 GMT
ENV PG_VERSION=16.11-1.pgdg12+1
# Thu, 13 Nov 2025 21:28:48 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 13 Nov 2025 21:28:48 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Nov 2025 21:28:49 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Nov 2025 21:28:49 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Nov 2025 21:28:49 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Nov 2025 21:28:49 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:33:37 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:33:37 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:33:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:33:37 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:33:37 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:33:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2442ae4ed78d32124d4f8b92ec0b1caf0e12483bafbd1803659dc391d3600616`  
		Last Modified: Tue, 04 Nov 2025 00:13:59 GMT  
		Size: 32.1 MB (32068905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb270615848954e048e023b4b3b91e35e7f942e570ac7859868c4a059ec785b`  
		Last Modified: Thu, 13 Nov 2025 21:08:29 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb722f1eaf84fd544360fca60ec8af94a1d3385ecafb0ce33f4645c4d8795f79`  
		Last Modified: Thu, 13 Nov 2025 21:08:30 GMT  
		Size: 5.4 MB (5368424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ac73f938bede2d8d0b71d2112ae0b4578cc125ae15b73533d4293440924a5d`  
		Last Modified: Thu, 13 Nov 2025 21:08:29 GMT  
		Size: 1.2 MB (1208142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e9b5369d12206889008e433fbe718a7c4cf0a7785d73c27651f608c39e2caf`  
		Last Modified: Thu, 13 Nov 2025 21:08:30 GMT  
		Size: 8.1 MB (8066503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36cc7c5ad06e2d4ea662fc5f43fae09d9e0795a386f62f9c1baec5fe27db15d8`  
		Last Modified: Thu, 13 Nov 2025 21:08:29 GMT  
		Size: 1.3 MB (1283606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad27fffb2fea9f82aeb115bdd927b81c260f90ac97f28644937b05f4e1b4135a`  
		Last Modified: Thu, 13 Nov 2025 21:08:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1a67fbbadbbb6c9a29d8a12ffe01107d9283b5139ef0e881c9cfb2675710f6`  
		Last Modified: Thu, 13 Nov 2025 21:08:29 GMT  
		Size: 3.1 KB (3146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40fb01248cad7507606a48208f651dc6fc70bfb9c1c5bc9f4583d9c3df6e50b7`  
		Last Modified: Thu, 13 Nov 2025 21:29:52 GMT  
		Size: 119.7 MB (119741622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8783d1838cf7e5fa567eaf4da7b870f73fd0d585a1c06a9e45d421cd19fd6a`  
		Last Modified: Thu, 13 Nov 2025 21:29:42 GMT  
		Size: 9.9 KB (9924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12aa6e733b467788b5a99688b1837e947b5a8078002f49c295dc8b8006490faa`  
		Last Modified: Thu, 13 Nov 2025 21:29:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf10bdd3a9cef5a493112015bc8227d4aec0a6d8c208cf548a39c119965f4fe`  
		Last Modified: Thu, 13 Nov 2025 21:29:42 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c438328a75d6a2b1fcb8586e6e7afd4fe48bc19cef37b8a86dc851dc0f3c63`  
		Last Modified: Fri, 14 Nov 2025 19:34:19 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05719d0c55a4875bca10dfcb20088ddd74ef00db26fd437195c9d28157b0707`  
		Last Modified: Fri, 14 Nov 2025 19:34:19 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:6cedff4792cdc1320a5bfca7113c57a6c4bcb926cdf9ec57377606446f297e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5970257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ba32d6bf1670c819a5385d27a3a94aa08cdd49ee52dca8601ef5d4f36c6ec6`

```dockerfile
```

-	Layers:
	-	`sha256:e93d87afa311d340eb2b2c32a29f4e2dfe2a6d5a3d918ebfd5a10dadd1ca3be7`  
		Last Modified: Fri, 14 Nov 2025 21:14:47 GMT  
		Size: 5.9 MB (5916907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd6ff787cecff04a8f67b291bf162582d560b7da71db61a4b6b1a0cc40804b3e`  
		Last Modified: Fri, 14 Nov 2025 21:14:48 GMT  
		Size: 53.4 KB (53350 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:79208cd0a99cf20ec3491b541b3c7812f81fe95e8c0c6002b95d858f6c566fd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.2 MB (164228238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c420f3271df6da7d677abccfccc01cb6d90e17ca8130fd123e8889925ace67ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 01:13:37 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 01:13:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:13:48 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 01:13:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 01:13:53 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 14 Nov 2025 01:13:53 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 01:13:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:13:56 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 01:13:56 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 14 Nov 2025 01:13:56 GMT
ENV PG_MAJOR=16
# Fri, 14 Nov 2025 01:13:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Fri, 14 Nov 2025 01:13:56 GMT
ENV PG_VERSION=16.11-1.pgdg12+1
# Fri, 14 Nov 2025 19:47:02 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:47:02 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:47:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:47:03 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:47:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:47:03 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:47:03 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:47:03 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:47:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:47:03 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:47:03 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:47:03 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147120a275748d7cfba32c7910cfdd1921b82567283d3f4872b29d3332df0cb9`  
		Last Modified: Fri, 14 Nov 2025 01:26:42 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c4dbe2517a4fe7544130e6b0f0c1fdb94aca456f3aac1d7c02b5ed01f5cd44`  
		Last Modified: Fri, 14 Nov 2025 01:26:42 GMT  
		Size: 4.4 MB (4391284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6596bc653f8082ee398adac92ec9eeeb716e58a3ff8dc430e86ab5a62e379f53`  
		Last Modified: Fri, 14 Nov 2025 01:26:42 GMT  
		Size: 1.2 MB (1222779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85dfd95f329d9b74ae2398d490dec8eb6362df90f950e7dfd6f7b8fcca8ba92c`  
		Last Modified: Fri, 14 Nov 2025 01:26:43 GMT  
		Size: 8.1 MB (8120661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe45344ee09474fa4b6ee71a5418dc97a3568680ceeb233e3cce2390bf5c976`  
		Last Modified: Fri, 14 Nov 2025 01:26:42 GMT  
		Size: 1.1 MB (1097014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3440c5db601ce3b77d5499d0b8bae3d7b2e8fa0bb886209b43bf5f0dac95a1e6`  
		Last Modified: Fri, 14 Nov 2025 01:26:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44adc8c24a16e584037f1d62236ba2c26a6a40b5d7d6d65244a9f196c29e4839`  
		Last Modified: Fri, 14 Nov 2025 01:26:42 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69a03f88bbe37504d375ff5b47c10754cf0bbf3ae9c6c4db23a21360f25db5f`  
		Last Modified: Fri, 14 Nov 2025 19:48:03 GMT  
		Size: 122.5 MB (122491274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f077b559b6f1ac1b925a563edd2a4eb49506045ec0e913b97ed0217ee700acd3`  
		Last Modified: Fri, 14 Nov 2025 19:47:55 GMT  
		Size: 9.9 KB (9928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee1cb08edb9841a31fb5eff98c39d8a43e64e709e860a52194115ee6d0f282e`  
		Last Modified: Fri, 14 Nov 2025 19:47:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46607f088105323410d1657e07d70336226c3b5218549dbfb17ff04c8053ef06`  
		Last Modified: Fri, 14 Nov 2025 19:47:55 GMT  
		Size: 165.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50f571ffa3b61369663208e82efd33de27fae3879a68ef690e98cc61707fa6a`  
		Last Modified: Fri, 14 Nov 2025 19:47:55 GMT  
		Size: 5.8 KB (5843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b945af84f6dd148b106dc94e5e8cb6a8db6de324c3898d95ba5a71d0dbb4aece`  
		Last Modified: Fri, 14 Nov 2025 19:47:55 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:8a29b9eace5c220d625ac5cdb86233983cc755e4172ce0b5efd94c319e490834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5975558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0624290da3d949212f01c08f13351ec9226ee1a89f9bc6daa9c4e0fb3a709c7`

```dockerfile
```

-	Layers:
	-	`sha256:6357db4627f8a7e83291c8edb11052d0ced0c516d8dda45b9425787a10630f05`  
		Last Modified: Fri, 14 Nov 2025 21:14:55 GMT  
		Size: 5.9 MB (5922262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:216323b27c8e1b952d599c7bf2df80d6750a95c0f7c91d95cc5c675c42942c58`  
		Last Modified: Fri, 14 Nov 2025 21:14:56 GMT  
		Size: 53.3 KB (53296 bytes)  
		MIME: application/vnd.in-toto+json
