## `postgres:19beta1`

```console
$ docker pull postgres@sha256:1b6357f5a18336ff97624b4df0b8ea9b1ee7d41cd21f2386104da8e2ac0d233e
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
$ docker pull postgres@sha256:0bff3fb0c26d507ca8ca423b56b21eb74cdc12fabaf404cf9f3c3a7a178b32bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.6 MB (163636781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1125da2106fcec587a21eef0a01129a4bb328578ac2645a48d1a056ea85cd3b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Sat, 06 Jun 2026 00:20:20 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sat, 06 Jun 2026 00:20:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jun 2026 00:20:32 GMT
ENV GOSU_VERSION=1.19
# Sat, 06 Jun 2026 00:20:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 06 Jun 2026 00:20:36 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Sat, 06 Jun 2026 00:20:36 GMT
ENV LANG=en_US.utf8
# Sat, 06 Jun 2026 00:20:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jun 2026 00:20:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 06 Jun 2026 00:20:39 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 06 Jun 2026 00:20:39 GMT
ENV PG_MAJOR=19
# Sat, 06 Jun 2026 00:20:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/19/bin
# Sat, 06 Jun 2026 00:20:39 GMT
ENV PG_VERSION=19~beta1-1.pgdg13+1
# Sat, 06 Jun 2026 00:20:58 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Sat, 06 Jun 2026 00:20:58 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 06 Jun 2026 00:20:58 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 06 Jun 2026 00:20:58 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Sat, 06 Jun 2026 00:20:58 GMT
VOLUME [/var/lib/postgresql]
# Sat, 06 Jun 2026 00:20:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 00:20:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 06 Jun 2026 00:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Jun 2026 00:20:59 GMT
STOPSIGNAL SIGINT
# Sat, 06 Jun 2026 00:20:59 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 06 Jun 2026 00:20:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5f258f1e05439474ba82d5cf3f75a5fecdd8183b66b0b8acc0f79dd45333d9`  
		Last Modified: Sat, 06 Jun 2026 00:21:18 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a90edd3a87aae0a9727377a9cfe9735d099ec6b432be6f7f0a4f650eb585d0`  
		Last Modified: Sat, 06 Jun 2026 00:21:18 GMT  
		Size: 6.4 MB (6443067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd339afe356e94f2ea9f32a044e174e216984284b2f23d17a629108f1da565f`  
		Last Modified: Sat, 06 Jun 2026 00:21:18 GMT  
		Size: 1.3 MB (1256762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949944b886bfc5b799d136a4b8050ccadc64dde4f5981bcc4d89f3bd7958bd96`  
		Last Modified: Sat, 06 Jun 2026 00:21:18 GMT  
		Size: 8.2 MB (8203822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f144fcd8e8988bf465a1f648663565b87a45e8b718d403588a881898117dbad`  
		Last Modified: Sat, 06 Jun 2026 00:21:19 GMT  
		Size: 1.3 MB (1311637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1018a5990779c64529fb500ffac88a8ee06f55a05842f2e8694f16ab24cc6a98`  
		Last Modified: Sat, 06 Jun 2026 00:21:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7896f5cd78f1bed7162464e9fdbc8918edf2a891b9d31a5c0599de0d47a4d4ce`  
		Last Modified: Sat, 06 Jun 2026 00:21:19 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd06501f82702b7fbb36d005b19acaaf0fdad4dde9fb90ab8724671fbaa7882`  
		Last Modified: Sat, 06 Jun 2026 00:21:23 GMT  
		Size: 116.6 MB (116609305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5927d7c85ac6e750dc56f53406925a561d46f6d66fb2d7ad58263b2d065ef857`  
		Last Modified: Sat, 06 Jun 2026 00:21:21 GMT  
		Size: 21.4 KB (21425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14093fec7b93dacf816388d02c83cf088cee0c4693842b00603049ec7af6fe31`  
		Last Modified: Sat, 06 Jun 2026 00:21:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f20ac1c082312d237788a57115063f32c08be292aed932e334c9bcd8c142af3`  
		Last Modified: Sat, 06 Jun 2026 00:21:21 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3891a839edbe533806ea30d8f9aa06fea186e8d04f1b2ab4bca6c7454e93eebf`  
		Last Modified: Sat, 06 Jun 2026 00:21:22 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1` - unknown; unknown

```console
$ docker pull postgres@sha256:f2d8237797fa71415a3004d40705000bfec16eb83bb16b0dcb7f02444f2c717f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6049169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d22ce4eb984c1fbfff8d57ae87828355cbb8cd83b7aa7564db830f4f7555a12f`

```dockerfile
```

-	Layers:
	-	`sha256:3c412504fc6158810d6a70e47ec6b6226512c96fc78a372873f157a874e37644`  
		Last Modified: Sat, 06 Jun 2026 00:21:18 GMT  
		Size: 6.0 MB (5997885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b539899a444c1882d101d0cebadff2445dd2c8b0cab1a94e9661d0b8ba22826`  
		Last Modified: Sat, 06 Jun 2026 00:21:17 GMT  
		Size: 51.3 KB (51284 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1` - linux; arm variant v5

```console
$ docker pull postgres@sha256:9b1d63bb6d6069b9986d36f4881e02ea4e84baf8ee1422d28a7aa8db4430b2d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92002990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a64669af90b92ffd4c4e9f26274a35a4f7595c723ede9aa379baab388750f03`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Sat, 06 Jun 2026 00:22:55 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sat, 06 Jun 2026 00:23:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jun 2026 00:23:16 GMT
ENV GOSU_VERSION=1.19
# Sat, 06 Jun 2026 00:23:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 06 Jun 2026 00:23:24 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Sat, 06 Jun 2026 00:23:24 GMT
ENV LANG=en_US.utf8
# Sat, 06 Jun 2026 00:23:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jun 2026 00:23:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 06 Jun 2026 00:23:32 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 06 Jun 2026 00:23:32 GMT
ENV PG_MAJOR=19
# Sat, 06 Jun 2026 00:23:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/19/bin
# Sat, 06 Jun 2026 00:23:32 GMT
ENV PG_VERSION=19~beta1-1.pgdg13+1
# Sat, 06 Jun 2026 00:37:42 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Sat, 06 Jun 2026 00:37:42 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 06 Jun 2026 00:37:42 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 06 Jun 2026 00:37:42 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Sat, 06 Jun 2026 00:37:42 GMT
VOLUME [/var/lib/postgresql]
# Sat, 06 Jun 2026 00:37:42 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 00:37:42 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 06 Jun 2026 00:37:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Jun 2026 00:37:42 GMT
STOPSIGNAL SIGINT
# Sat, 06 Jun 2026 00:37:42 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 06 Jun 2026 00:37:42 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:37dea77b903ae642229487445fa64e20dcf83d60070467f9c7581fb71a2dd8a8`  
		Last Modified: Tue, 19 May 2026 22:36:45 GMT  
		Size: 28.0 MB (27953869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c85a50b617c7f0f49212fbea9d9fc45d69115421dfdd385babe565c0dd3a7a`  
		Last Modified: Sat, 06 Jun 2026 00:37:55 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0c688ca4cd542df322eebc41a2bfcbdfad9502a2fed82f002ff3013e459a04`  
		Last Modified: Sat, 06 Jun 2026 00:37:56 GMT  
		Size: 5.9 MB (5932355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6d37e91b198c10169087385ef22853ea83a535accf62e92f907f88b0a4a787`  
		Last Modified: Sat, 06 Jun 2026 00:37:55 GMT  
		Size: 1.2 MB (1227539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e48ecc5f4a0c09c1967538288bf74e149d7d822761c6c553983df08734d1be`  
		Last Modified: Sat, 06 Jun 2026 00:37:56 GMT  
		Size: 8.2 MB (8204233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39625d0ddb0fe97d2b4239f6a6418d4a0c39bfdffd5b514e56f6a2f3fdb2627c`  
		Last Modified: Sat, 06 Jun 2026 00:37:56 GMT  
		Size: 1.3 MB (1317265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6ebab08ad967c683bc3969ad09433e45e4f18496c38dbfb313fd6db6b3d1db`  
		Last Modified: Sat, 06 Jun 2026 00:37:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a145e8858b78ee964a3cf5acc35762771dcabaa6f91231c89b69230bfe00490`  
		Last Modified: Sat, 06 Jun 2026 00:37:57 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1f8b0d11cc3c96d1122c46ce779c5e75c0a5642be1ba908d106b64229b9951`  
		Last Modified: Sat, 06 Jun 2026 00:37:58 GMT  
		Size: 47.3 MB (47335468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6010100342a060db71d5c028fb7b5b4255ff2e71dd608ac6c4df1b47a77a0f`  
		Last Modified: Sat, 06 Jun 2026 00:37:58 GMT  
		Size: 21.4 KB (21421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b58f43c7776fc5f85201dcaf70a3b5267b2e51e96b98c8d39225b47933785d`  
		Last Modified: Sat, 06 Jun 2026 00:37:58 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0a7c7956c605ebb46d6f7844118f63c39ef6c00a4f3ec7e6850dad45f63153`  
		Last Modified: Sat, 06 Jun 2026 00:37:58 GMT  
		Size: 6.1 KB (6100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007052c22766b3fbd9e12ff670b203abb8505f5caa85e426fc0960035dae723a`  
		Last Modified: Sat, 06 Jun 2026 00:37:59 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1` - unknown; unknown

```console
$ docker pull postgres@sha256:877f0562dbf157e9cda83c821cd5526e5a9969442cabb1959eabe89dd58eb23c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5179602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5e47f5ff371080bcf5b69f88f6694bee87fc315484e3089db569b00be78b0d9`

```dockerfile
```

-	Layers:
	-	`sha256:b08e2380881f202f98f96bbe9965d0637f318b3703874a0adaf5c9bd862825e1`  
		Last Modified: Sat, 06 Jun 2026 00:37:56 GMT  
		Size: 5.1 MB (5128129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0f14935c85532cecb4858c6ed0caeb2b3bb2a94b8df82033c100c1d20a0e986`  
		Last Modified: Sat, 06 Jun 2026 00:37:55 GMT  
		Size: 51.5 KB (51473 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1` - linux; arm variant v7

```console
$ docker pull postgres@sha256:1c7c82bde1b178ae56b876eb2357a852fa17d808734432ea038366e170c95c18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88276928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b444a4ff7287702c1231680e74643b2be022f0daa2dd085e1350fc7769fe27`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Sat, 06 Jun 2026 00:26:52 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sat, 06 Jun 2026 00:26:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jun 2026 00:27:07 GMT
ENV GOSU_VERSION=1.19
# Sat, 06 Jun 2026 00:27:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 06 Jun 2026 00:27:15 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Sat, 06 Jun 2026 00:27:15 GMT
ENV LANG=en_US.utf8
# Sat, 06 Jun 2026 00:27:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jun 2026 00:27:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 06 Jun 2026 00:27:20 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 06 Jun 2026 00:27:20 GMT
ENV PG_MAJOR=19
# Sat, 06 Jun 2026 00:27:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/19/bin
# Sat, 06 Jun 2026 00:27:20 GMT
ENV PG_VERSION=19~beta1-1.pgdg13+1
# Sat, 06 Jun 2026 00:39:57 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Sat, 06 Jun 2026 00:39:57 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 06 Jun 2026 00:39:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 06 Jun 2026 00:39:57 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Sat, 06 Jun 2026 00:39:57 GMT
VOLUME [/var/lib/postgresql]
# Sat, 06 Jun 2026 00:39:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 00:39:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 06 Jun 2026 00:39:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Jun 2026 00:39:57 GMT
STOPSIGNAL SIGINT
# Sat, 06 Jun 2026 00:39:57 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 06 Jun 2026 00:39:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae573d6dce59d0bc21c9ac8411157d7a4db431a47c3a94118382d3cc548b8fc9`  
		Last Modified: Sat, 06 Jun 2026 00:40:10 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31028a2cb408934995aad73be7e42be8d8cf10922acbb914ae5614a38e9d59d9`  
		Last Modified: Sat, 06 Jun 2026 00:40:10 GMT  
		Size: 5.5 MB (5497315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a341ab697d66ffec250a9af4a45784296621c18cdeed5ebdbbf2cea6b902e5`  
		Last Modified: Sat, 06 Jun 2026 00:40:10 GMT  
		Size: 1.2 MB (1222375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b963d8d85f12eb21ef05ee1b8be2952b58816fce06f169694abc1380b484af`  
		Last Modified: Sat, 06 Jun 2026 00:40:10 GMT  
		Size: 8.2 MB (8204116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59ea46c5a16514265bdd7b59a951a19f22ae86287f5a58ea4cbc5eca8b11d30`  
		Last Modified: Sat, 06 Jun 2026 00:40:11 GMT  
		Size: 1.2 MB (1172646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388d45d7ad5de27d1c3c600d166662cccf098b32aebaf340bffa872725dbd4ff`  
		Last Modified: Sat, 06 Jun 2026 00:40:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb86fecfcacbd0fc1326033895e068048721a9e7a77d693456ebd34ba3af5868`  
		Last Modified: Sat, 06 Jun 2026 00:40:12 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550d6b22acefc45a3811081e3c4d1dc7131d7edeea2b75a1611b8be619db47fc`  
		Last Modified: Sat, 06 Jun 2026 00:40:13 GMT  
		Size: 45.9 MB (45942371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c88a21587c646a3befc78aff3b4a7e4a1f4fa8a26d7077456cd3a82278b5c1`  
		Last Modified: Sat, 06 Jun 2026 00:40:13 GMT  
		Size: 21.4 KB (21434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962307fa134611f8258ceb4592133d821bfb4fe7d9e6e6dd4681d1df450609a6`  
		Last Modified: Sat, 06 Jun 2026 00:40:13 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a5e1eeef06e9dd54e0f3793c8f037632130b62329b3a7df535fb29dffbb6b7`  
		Last Modified: Sat, 06 Jun 2026 00:40:13 GMT  
		Size: 6.1 KB (6100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6577ee927ab4f38ba46a12657d38a9c57c8c890970db416dd80575f2b82c4d5`  
		Last Modified: Sat, 06 Jun 2026 00:40:14 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1` - unknown; unknown

```console
$ docker pull postgres@sha256:e6199891854a7f5fb1cd851354451bc0842feb7d64e9adca6a2e1089c7159128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5178907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba3aaaec306aa2b5097b3103c979857f291092d1a90adc8341aa508a4217af74`

```dockerfile
```

-	Layers:
	-	`sha256:04d140cdb3080f0160870c255bd147414fa7d9334025f4aa9e80e227aa98e6b4`  
		Last Modified: Sat, 06 Jun 2026 00:40:10 GMT  
		Size: 5.1 MB (5127434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfce7c9098959fb90f0d8bad90ec32d194677668a0bc20736011c7cd4bb0616a`  
		Last Modified: Sat, 06 Jun 2026 00:40:10 GMT  
		Size: 51.5 KB (51473 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:7f5c216d8da410307d8498e53191b529f22ca2289d75724c315e6387ff39e82c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.2 MB (162198851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979981c6375e467943abe0579e95d9edad0c5bac22b6a13cc5711618d3755443`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Sat, 06 Jun 2026 00:21:41 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sat, 06 Jun 2026 00:21:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jun 2026 00:21:54 GMT
ENV GOSU_VERSION=1.19
# Sat, 06 Jun 2026 00:21:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 06 Jun 2026 00:22:00 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Sat, 06 Jun 2026 00:22:00 GMT
ENV LANG=en_US.utf8
# Sat, 06 Jun 2026 00:22:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jun 2026 00:22:04 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 06 Jun 2026 00:22:05 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 06 Jun 2026 00:22:05 GMT
ENV PG_MAJOR=19
# Sat, 06 Jun 2026 00:22:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/19/bin
# Sat, 06 Jun 2026 00:22:05 GMT
ENV PG_VERSION=19~beta1-1.pgdg13+1
# Sat, 06 Jun 2026 00:22:54 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Sat, 06 Jun 2026 00:22:54 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 06 Jun 2026 00:22:54 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 06 Jun 2026 00:22:54 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Sat, 06 Jun 2026 00:22:54 GMT
VOLUME [/var/lib/postgresql]
# Sat, 06 Jun 2026 00:22:54 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 00:22:54 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 06 Jun 2026 00:22:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Jun 2026 00:22:54 GMT
STOPSIGNAL SIGINT
# Sat, 06 Jun 2026 00:22:54 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 06 Jun 2026 00:22:54 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917b378e3cef405c0dab79526bc8ff5350f67fbda9e63c0924b85f60a5620e4a`  
		Last Modified: Sat, 06 Jun 2026 00:23:14 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f725fba48054ef685829aece95913f81789583b6d37fdec6cde382ab8011de46`  
		Last Modified: Sat, 06 Jun 2026 00:23:14 GMT  
		Size: 6.2 MB (6235147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e0cf979808397d326a194050d1d85b6e91602f930bf7d57c5dc2412c394f7c`  
		Last Modified: Sat, 06 Jun 2026 00:23:14 GMT  
		Size: 1.2 MB (1209544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991ec0d7b7135bd4a8680c80c6397cfdc62dd346850ac6e2513a4aeba6c78422`  
		Last Modified: Sat, 06 Jun 2026 00:23:14 GMT  
		Size: 8.2 MB (8204009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b138441671b136d65a44cbdbedfea7a164193b5556b6b48435291b4440ed4d60`  
		Last Modified: Sat, 06 Jun 2026 00:23:15 GMT  
		Size: 1.2 MB (1220567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936588442905795a2d18a99d70d6364a3c193b5462dde88f93a0a9dfcafbc4a8`  
		Last Modified: Sat, 06 Jun 2026 00:23:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88cedadd6a1313a923d13d3b1ea7531910a277deb190e3fc5879071b3f0facf`  
		Last Modified: Sat, 06 Jun 2026 00:23:15 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c0ee7cc0cbce061cc36b00a719ace236721376c68d8dd6d37c13647f170d74`  
		Last Modified: Sat, 06 Jun 2026 00:23:19 GMT  
		Size: 115.2 MB (115155396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdea416faffb75db10db54d7c57dbac3d80e322eef3bb7d72feff6a04caef488`  
		Last Modified: Sat, 06 Jun 2026 00:23:16 GMT  
		Size: 21.4 KB (21424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27a414fa7b0e58c5d4ffea610951ba0f831c0c27029e0256eba51f2abc6aee8`  
		Last Modified: Sat, 06 Jun 2026 00:23:17 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd027b08eb2e0bc9fe7760253bc767e40f73225521b33dd200f23b56f9db10a2`  
		Last Modified: Sat, 06 Jun 2026 00:23:17 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a0416a9cb29d7bbe9359d2e23cc363dcf56cd58016bf3d8d2521bec02e604b`  
		Last Modified: Sat, 06 Jun 2026 00:23:18 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1` - unknown; unknown

```console
$ docker pull postgres@sha256:c1acb17095906d6da324db2c19cedf839bb3fd3bae5615bb652d9ecb3c992775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6055716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84a878e90261338981fdc04306799f2c0070fd8295e78a0298d08713c66618c`

```dockerfile
```

-	Layers:
	-	`sha256:8dbaa3643145599fe99adeedfabce82c888077011a6fe5b7906fa62501eaeaf4`  
		Last Modified: Sat, 06 Jun 2026 00:23:14 GMT  
		Size: 6.0 MB (6004202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e710835657807eb0e029c0cc66f056a4df7012e6e16cc5e6fbb0fed285ef750`  
		Last Modified: Sat, 06 Jun 2026 00:23:13 GMT  
		Size: 51.5 KB (51514 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1` - linux; 386

```console
$ docker pull postgres@sha256:3c40b28459d0b7369e16b374551798852c5a086e1ec113cd544e57d5b22e776d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.2 MB (98190422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71ca6f72b69f7f52bac8991185d599be9807737cf9d310213f373024688cf9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Sat, 06 Jun 2026 00:21:19 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sat, 06 Jun 2026 00:21:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jun 2026 00:21:33 GMT
ENV GOSU_VERSION=1.19
# Sat, 06 Jun 2026 00:21:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 06 Jun 2026 00:21:38 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Sat, 06 Jun 2026 00:21:38 GMT
ENV LANG=en_US.utf8
# Sat, 06 Jun 2026 00:21:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jun 2026 00:21:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 06 Jun 2026 00:21:43 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 06 Jun 2026 00:21:43 GMT
ENV PG_MAJOR=19
# Sat, 06 Jun 2026 00:21:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/19/bin
# Sat, 06 Jun 2026 00:21:43 GMT
ENV PG_VERSION=19~beta1-1.pgdg13+1
# Sat, 06 Jun 2026 00:30:43 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Sat, 06 Jun 2026 00:30:43 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 06 Jun 2026 00:30:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 06 Jun 2026 00:30:43 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Sat, 06 Jun 2026 00:30:43 GMT
VOLUME [/var/lib/postgresql]
# Sat, 06 Jun 2026 00:30:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 00:30:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 06 Jun 2026 00:30:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Jun 2026 00:30:43 GMT
STOPSIGNAL SIGINT
# Sat, 06 Jun 2026 00:30:43 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 06 Jun 2026 00:30:43 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:05ced853378773a7168a29bae2e2f29a846f0a56beb260fd47a509a5e4ac966a`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 31.3 MB (31295335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0225f82e2ea3120f738e4ed6236e5ddd1283822aa66cbd247554f1dc55a2ae14`  
		Last Modified: Sat, 06 Jun 2026 00:30:55 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f91751e54447505807d97fc8cb885ee44c3f770bc2c1abfd91d7453dc8cdd4`  
		Last Modified: Sat, 06 Jun 2026 00:30:55 GMT  
		Size: 6.6 MB (6631420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b821d71afabd98a9293fd0e5e7c4fca462336b3afbbe81bdcbc7902601c0e675`  
		Last Modified: Sat, 06 Jun 2026 00:30:55 GMT  
		Size: 1.2 MB (1225844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788c8bed497606f9b9e3042774c52e9aedb442619f5f2b5d23e814f616f8491e`  
		Last Modified: Sat, 06 Jun 2026 00:30:55 GMT  
		Size: 8.2 MB (8204066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915786cded0b9b407510c654a1d39521757bf676e9ad6bc85a85c0e0e5e92bd0`  
		Last Modified: Sat, 06 Jun 2026 00:30:56 GMT  
		Size: 1.3 MB (1308267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fcd58506afabdc16e2892f81b7a8b903b65036393d6acf7b35de1ef8a0801c`  
		Last Modified: Sat, 06 Jun 2026 00:30:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7819efe573f1427e02b6d7f5f29f26e520fd63854dafb3379196f100d745d307`  
		Last Modified: Sat, 06 Jun 2026 00:30:57 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28df6ee32dfa481179a16176cf6c8606a247e5f53e6d4e1800e6fa7771c7a4df`  
		Last Modified: Sat, 06 Jun 2026 00:30:58 GMT  
		Size: 49.5 MB (49493228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc3129af57f4811f5db35cb47076edffc1adeb8b4730d459b696c8990025a82`  
		Last Modified: Sat, 06 Jun 2026 00:30:58 GMT  
		Size: 21.4 KB (21421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ffd43e9d42b10d57cf220e9b7f8aa72ebbfbca078787e080dea5740bf9d5bd`  
		Last Modified: Sat, 06 Jun 2026 00:30:58 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9b7071e979552a126c2ebd1f9d30f736586a803f5e2464496c889698044c65`  
		Last Modified: Sat, 06 Jun 2026 00:30:58 GMT  
		Size: 6.1 KB (6100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513b2f2837a38124912a9be3f8a484a1c9cecc73a6d6d91e368ebc0f68c9d3ac`  
		Last Modified: Sat, 06 Jun 2026 00:30:59 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1` - unknown; unknown

```console
$ docker pull postgres@sha256:fbc66e28c3a55897da1f12aeaf9e2353c6c2f3833128caac0689d481eb08baa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5174751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6e5581aba28b2a9138a4a28acf0e8e2835ac7876c498619fdaac93383cffca`

```dockerfile
```

-	Layers:
	-	`sha256:596a647460f01200e3dc272f6e66d3a02dbc809983ded845b9327ccb694566df`  
		Last Modified: Sat, 06 Jun 2026 00:30:55 GMT  
		Size: 5.1 MB (5123514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae4de285aa40ee5db93366311ef439d6aef26e7d6a18a4b73219fb2b06acabd8`  
		Last Modified: Sat, 06 Jun 2026 00:30:55 GMT  
		Size: 51.2 KB (51237 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1` - linux; ppc64le

```console
$ docker pull postgres@sha256:df12c0e8041cedf2a990502e2aad7282ccbb2b9456743f0935aa5276a1d17a22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176119370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16766260f0a31165e74a2bf0e8cdae66e2082c85d3d34daeb43ba451feeadb5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Sat, 06 Jun 2026 01:04:43 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sat, 06 Jun 2026 01:04:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jun 2026 01:05:11 GMT
ENV GOSU_VERSION=1.19
# Sat, 06 Jun 2026 01:05:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 06 Jun 2026 01:05:21 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Sat, 06 Jun 2026 01:05:21 GMT
ENV LANG=en_US.utf8
# Sat, 06 Jun 2026 01:05:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jun 2026 01:05:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 06 Jun 2026 01:05:30 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 06 Jun 2026 01:05:30 GMT
ENV PG_MAJOR=19
# Sat, 06 Jun 2026 01:05:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/19/bin
# Sat, 06 Jun 2026 01:05:30 GMT
ENV PG_VERSION=19~beta1-1.pgdg13+1
# Sat, 06 Jun 2026 01:06:11 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Sat, 06 Jun 2026 01:06:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 06 Jun 2026 01:06:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 06 Jun 2026 01:06:13 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Sat, 06 Jun 2026 01:06:13 GMT
VOLUME [/var/lib/postgresql]
# Sat, 06 Jun 2026 01:06:14 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 01:06:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 06 Jun 2026 01:06:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Jun 2026 01:06:15 GMT
STOPSIGNAL SIGINT
# Sat, 06 Jun 2026 01:06:15 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 06 Jun 2026 01:06:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65fb76d3442e74499cb63951a7a179a4bac0a5f1f704daca58d4fafd2399c1c`  
		Last Modified: Sat, 06 Jun 2026 01:07:00 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef8873ac40fbe5b3462709339f416b5bbee6ed43d8254d2369b1989cc820556`  
		Last Modified: Sat, 06 Jun 2026 01:07:01 GMT  
		Size: 7.1 MB (7076776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7a65fe0819261f305238823b2f4cf2d8a72f5208f8044809784755f85c7ab8`  
		Last Modified: Sat, 06 Jun 2026 01:07:00 GMT  
		Size: 1.2 MB (1214739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e35d68da6b68cfe12c445d220bb904ece5775ce6004e6192f6fb31108c3075`  
		Last Modified: Sat, 06 Jun 2026 01:07:00 GMT  
		Size: 8.2 MB (8204051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c36950cc3b138cd315dedcd19172fb6997391ba5fb8d5ba24ed38f3cad9e37`  
		Last Modified: Sat, 06 Jun 2026 01:07:01 GMT  
		Size: 1.4 MB (1394895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221bb0ab4f32f71dfaede138522c382d46593438dda54e539061693bf950072e`  
		Last Modified: Sat, 06 Jun 2026 01:07:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6a9167ddadcd7b098769163a14327c15764d5b33b9d91e64b223cce2d3ce29`  
		Last Modified: Sat, 06 Jun 2026 01:07:02 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d441d3801540cfd3ea02276b562ed180df44d1a7ab35a2ac388ee54eb8240b`  
		Last Modified: Sat, 06 Jun 2026 01:07:06 GMT  
		Size: 124.6 MB (124596205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d9b7c2eea8a99353f1d622e6831a61e6d727d9450a03b752ccb84b8b67733d`  
		Last Modified: Sat, 06 Jun 2026 01:07:03 GMT  
		Size: 21.4 KB (21409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec6198904cce6be8d65bcb351982ad769ff9c74cc598891299636ceb837c0047`  
		Last Modified: Sat, 06 Jun 2026 01:07:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1a9876ab709bea25395877c543a1bf62b464f003240662c32da13470c2c30d`  
		Last Modified: Sat, 06 Jun 2026 01:07:03 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e0bd402340247793f4af0b10b701f0fd276933b6853b6899285c66759ed65d`  
		Last Modified: Sat, 06 Jun 2026 01:07:04 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1` - unknown; unknown

```console
$ docker pull postgres@sha256:68f70d178fafe562834d5c7eaa910844027cc5101a9fa58b7b5fa27fadd189e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6055845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:770588c542b9f01cac392ea3eccae043d872de0d03511cd82354cedcb2403328`

```dockerfile
```

-	Layers:
	-	`sha256:1bfd1a404592fe432f7d332a15dbeb86e8483da3db1a8a770d304a6318fc61fb`  
		Last Modified: Sat, 06 Jun 2026 01:07:00 GMT  
		Size: 6.0 MB (6004509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c7c077bae938314bf15b2b2c091a7a615970383c94a0d36efc936ab7d5dac32`  
		Last Modified: Sat, 06 Jun 2026 01:07:00 GMT  
		Size: 51.3 KB (51336 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1` - linux; riscv64

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

### `postgres:19beta1` - unknown; unknown

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

### `postgres:19beta1` - linux; s390x

```console
$ docker pull postgres@sha256:5510cab3c9545dba3d93a2e3bb4cd16e2671519beac93a998c90a07485999b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.3 MB (178324389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d0a11f21b13c6cd9a22159e4455984c8e0af644f2bd28dd5fcfa6146214380`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Sat, 06 Jun 2026 00:30:40 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sat, 06 Jun 2026 00:30:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jun 2026 00:30:54 GMT
ENV GOSU_VERSION=1.19
# Sat, 06 Jun 2026 00:30:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 06 Jun 2026 00:30:59 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Sat, 06 Jun 2026 00:30:59 GMT
ENV LANG=en_US.utf8
# Sat, 06 Jun 2026 00:31:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jun 2026 00:31:04 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 06 Jun 2026 00:31:05 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 06 Jun 2026 00:31:05 GMT
ENV PG_MAJOR=19
# Sat, 06 Jun 2026 00:31:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/19/bin
# Sat, 06 Jun 2026 00:31:05 GMT
ENV PG_VERSION=19~beta1-1.pgdg13+1
# Sat, 06 Jun 2026 00:45:19 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Sat, 06 Jun 2026 00:45:19 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 06 Jun 2026 00:45:19 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 06 Jun 2026 00:45:19 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Sat, 06 Jun 2026 00:45:19 GMT
VOLUME [/var/lib/postgresql]
# Sat, 06 Jun 2026 00:45:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 00:45:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 06 Jun 2026 00:45:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Jun 2026 00:45:20 GMT
STOPSIGNAL SIGINT
# Sat, 06 Jun 2026 00:45:20 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 06 Jun 2026 00:45:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e41e17993e3f5d3cd5214fb7c9ffd539d55eaa26b9a9e130d22d8e919cb98a`  
		Last Modified: Sat, 06 Jun 2026 00:45:51 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf1b545667da33031a3ca37c0cfa5a1c08d158a8b719b043c8d69a52602d976`  
		Last Modified: Sat, 06 Jun 2026 00:45:51 GMT  
		Size: 6.4 MB (6408520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4fdc11fcac472e43a49e823fdd849da4dc2f41f16399aced8a75bfdc102c18`  
		Last Modified: Sat, 06 Jun 2026 00:45:51 GMT  
		Size: 1.2 MB (1230268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f4daf999a2b2d944e948f37877352ded0e6186ea163eac19066b0404fff3b9`  
		Last Modified: Sat, 06 Jun 2026 00:45:51 GMT  
		Size: 8.3 MB (8258955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89cc597e0b4c15e43ce8faad55fb9de2d742021787ef730ac2d08eb1642e273`  
		Last Modified: Sat, 06 Jun 2026 00:45:52 GMT  
		Size: 1.4 MB (1398216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29fe8a311028319f919ddf1e3735b4b21549b1e53ff459f66c72102b5b0aa646`  
		Last Modified: Sat, 06 Jun 2026 00:45:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04359c10495fbcd10d97a9dd3bff0c776752dddb4ef7c5e18e096aee09c6cf3`  
		Last Modified: Sat, 06 Jun 2026 00:45:52 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d6eb1b47e513d289051428044a638dea45186bd17e99eb1971954670b96808`  
		Last Modified: Sat, 06 Jun 2026 00:45:55 GMT  
		Size: 131.2 MB (131150243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4dbf49f223d5db78fdc05e8de91bb17e3086e02bb0d7bd5f45192ae5001998`  
		Last Modified: Sat, 06 Jun 2026 00:45:53 GMT  
		Size: 21.4 KB (21426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7878134ca1bc7a460a5383556606d74026108b71cbd41b0c0c1788d0147e278d`  
		Last Modified: Sat, 06 Jun 2026 00:45:53 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b110e4f64767740f32371736db6daf023cdb12403569334abc504945759b922e`  
		Last Modified: Sat, 06 Jun 2026 00:45:53 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272e3767d4687d0322b911129b87f64712ec4eec43fab9e6f2cf57c2ecec9e80`  
		Last Modified: Sat, 06 Jun 2026 00:45:54 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1` - unknown; unknown

```console
$ docker pull postgres@sha256:50d805031004a7e58d392360ef7379bf886b733ae54a31d104e55a26e4b0eaec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6065839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9d1184f44fc876100dad0072ae0f9cce45a75c9ba188ed800afb26a113ec359`

```dockerfile
```

-	Layers:
	-	`sha256:5a8e80c3cf8c18e4ec99a0ddd6949bb0e5d4c2f5184d494ba7f323438c7ef268`  
		Last Modified: Sat, 06 Jun 2026 00:45:51 GMT  
		Size: 6.0 MB (6014555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:145fcc2a3b9cf760cc484c845f923422241de3148249b45e9fa6a2fd5f0aa553`  
		Last Modified: Sat, 06 Jun 2026 00:45:51 GMT  
		Size: 51.3 KB (51284 bytes)  
		MIME: application/vnd.in-toto+json
