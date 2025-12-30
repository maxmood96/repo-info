## `postgres:17-bookworm`

```console
$ docker pull postgres@sha256:b842a9c7c420ed1313ee7c8440ef44da718c8fda05bfd1caf034ed4667cb645a
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
$ docker pull postgres@sha256:1c1647e6ffe0254ddd3f29ccc1dc427e9145cf1025eb16618883e49132b06eb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (156016782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ec021260e93aee356e4e86fe9807874ae79f5c1b2755a70e454f1a4a90366f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:37:00 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 29 Dec 2025 23:37:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:37:12 GMT
ENV GOSU_VERSION=1.19
# Mon, 29 Dec 2025 23:37:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 29 Dec 2025 23:37:16 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 29 Dec 2025 23:37:16 GMT
ENV LANG=en_US.utf8
# Mon, 29 Dec 2025 23:37:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:37:19 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 29 Dec 2025 23:37:20 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 29 Dec 2025 23:37:20 GMT
ENV PG_MAJOR=17
# Mon, 29 Dec 2025 23:37:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Mon, 29 Dec 2025 23:37:20 GMT
ENV PG_VERSION=17.7-3.pgdg12+1
# Mon, 29 Dec 2025 23:37:33 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 29 Dec 2025 23:37:33 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 29 Dec 2025 23:37:33 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 29 Dec 2025 23:37:33 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 29 Dec 2025 23:37:33 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 29 Dec 2025 23:37:33 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 29 Dec 2025 23:37:33 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:37:34 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 29 Dec 2025 23:37:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:37:34 GMT
STOPSIGNAL SIGINT
# Mon, 29 Dec 2025 23:37:34 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 29 Dec 2025 23:37:34 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be56d59d653131f004c1362246df8f7e2a475182d26102295b499bf09939f645`  
		Last Modified: Mon, 29 Dec 2025 23:38:02 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc057f792b73a0c6ddae84f25fba325db53b75b8184900fb05447c779fe07ae`  
		Last Modified: Mon, 29 Dec 2025 23:38:03 GMT  
		Size: 4.5 MB (4534099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b9523d1a8f1becca17b7eac8757c250f217911d814f85a2b8a9609156a5b05`  
		Last Modified: Mon, 29 Dec 2025 23:38:02 GMT  
		Size: 1.2 MB (1249514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f459942ba3621f22587cfb9a0bf958cd280f67d8537bb760d9271c59a2cbb176`  
		Last Modified: Mon, 29 Dec 2025 23:38:04 GMT  
		Size: 8.1 MB (8066447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e3feac14d36ac3847e4066fdd77243ce7385d5e9d1ca0be576eddb88865e08`  
		Last Modified: Mon, 29 Dec 2025 23:38:03 GMT  
		Size: 1.2 MB (1196412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3a9b2a059d438de82b26793c3bae40815e6f830fb9d5588b790193b164a019`  
		Last Modified: Mon, 29 Dec 2025 23:38:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26400b2379c7ed5cc0e4d3ad5800a315f17e8644aa4d90f6f0a3fb214d03ce9`  
		Last Modified: Mon, 29 Dec 2025 23:38:04 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99562acfbe2da923f36c0ea0c51b9dc643337b4611c3886572047bae133ee647`  
		Last Modified: Mon, 29 Dec 2025 23:38:10 GMT  
		Size: 112.7 MB (112720909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9341537ce710e8d36890d58ef85a22ad9518de895a25a85bcaaad1b0ff212831`  
		Last Modified: Mon, 29 Dec 2025 23:38:02 GMT  
		Size: 10.2 KB (10237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfce8036844b6cb608eda821015d44084fbb60046c4f2c300b284d71b89f126b`  
		Last Modified: Mon, 29 Dec 2025 23:38:02 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5773fb4a9d720a72a10fe96c0b6293e84ae2ed76754e3e6d2de5bb46a34a8196`  
		Last Modified: Mon, 29 Dec 2025 23:38:03 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3efabc308a47f6718e3a67c8e89f227330797cda1da722095564d5497a35cc15`  
		Last Modified: Mon, 29 Dec 2025 23:38:03 GMT  
		Size: 5.8 KB (5835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb69b566c1e308b46ee4287a8e8b35bde92f6c17c0dfab2277e76bd5004a9fb`  
		Last Modified: Mon, 29 Dec 2025 23:38:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:5fbc7f87295f226d11d81f46bdf71c310cd6410f6aa7576a591afcd28afa1415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5980746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebed61b85b355635d152f17584b97376f985679978d949abec4c82eaeb0bd6c3`

```dockerfile
```

-	Layers:
	-	`sha256:6d3c664863f18901bde766dd76cb849e0a4180e384106ee75dce28950c7947d3`  
		Last Modified: Tue, 30 Dec 2025 03:13:43 GMT  
		Size: 5.9 MB (5927456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6678a093e606c7bdb9dbb877383b5a880fb7cdbd04427301e42f3066659a4007`  
		Last Modified: Tue, 30 Dec 2025 03:13:44 GMT  
		Size: 53.3 KB (53290 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:52f4aa57ce94f06888851ac630a625d3c0314d88d7e81c032e0b56744397c701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (149043618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8191796453fb2f05ff8db0deca5f97976fbc7638a372e554e5f4a977a1add7d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:54:14 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 29 Dec 2025 23:54:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:54:31 GMT
ENV GOSU_VERSION=1.19
# Mon, 29 Dec 2025 23:54:31 GMT
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
ENV PG_MAJOR=17
# Mon, 29 Dec 2025 23:54:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Mon, 29 Dec 2025 23:54:44 GMT
ENV PG_VERSION=17.7-3.pgdg12+1
# Tue, 30 Dec 2025 00:10:30 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 30 Dec 2025 00:10:30 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Dec 2025 00:10:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Dec 2025 00:10:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Dec 2025 00:10:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 30 Dec 2025 00:10:30 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Dec 2025 00:10:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 00:10:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Dec 2025 00:10:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Dec 2025 00:10:30 GMT
STOPSIGNAL SIGINT
# Tue, 30 Dec 2025 00:10:30 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Dec 2025 00:10:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:cdd01b66e4b6599d6f59fe75d883783e8ddfc67db8fda967c6ce250da575cc0b`  
		Last Modified: Mon, 29 Dec 2025 22:25:33 GMT  
		Size: 25.8 MB (25757576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8776ab36f241a8d0a3a854da69e3b14bca77549521ddf151231917ee7c8fcb`  
		Last Modified: Tue, 30 Dec 2025 00:07:15 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a58cd6fcf2d81b9ca057832eddec0e51beb2e1b012e9bfff4144c961e579fe`  
		Last Modified: Tue, 30 Dec 2025 00:11:00 GMT  
		Size: 4.2 MB (4151185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b42a0934e92b656d37903ca0890c7437cfbb58b567ee8ef0cae04bb56e3ee70`  
		Last Modified: Tue, 30 Dec 2025 00:11:00 GMT  
		Size: 1.2 MB (1220044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dddc4a137634cc9f1e69f5d85cfe613aef549be0eba9525d4c6a816ca8b956e`  
		Last Modified: Tue, 30 Dec 2025 00:11:01 GMT  
		Size: 8.1 MB (8066541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c161af63bd45f89b9137323d21e13b327a80009c65764d0a8b8dd8fa7b7ad023`  
		Last Modified: Tue, 30 Dec 2025 00:10:59 GMT  
		Size: 1.2 MB (1195029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2c6fdddb8a8aacee36f7aaafe9a537bf252ebbb0426a23225ae077ca584b72`  
		Last Modified: Tue, 30 Dec 2025 00:07:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191184b4cba26733f5b786788dc4e01854bd8a1e4a92e9d58eab3c5598d981c6`  
		Last Modified: Tue, 30 Dec 2025 00:07:15 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469dd5dd8a23ee01171e7d862c2a629e6751d6769632ffe456663833cf147ac0`  
		Last Modified: Tue, 30 Dec 2025 00:11:07 GMT  
		Size: 108.6 MB (108632252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ce1f29a3b31fe1fc545652b2c09da5b1381101c79945ec55df9509a2f97de2`  
		Last Modified: Tue, 30 Dec 2025 00:10:59 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4b537cb35ca71a5a9875ceb318036667adf76033a51f08bcddedcf3c4d1621`  
		Last Modified: Tue, 30 Dec 2025 00:10:59 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e161b5466efbfa5989dc187e645d934ff70ecd5342bf30dd5957c0d2cf0ce0b8`  
		Last Modified: Tue, 30 Dec 2025 00:11:01 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bc029ce86b7e9defe11bcf47f231e163b6e3268eee65f3eae33740f0fdc965`  
		Last Modified: Tue, 30 Dec 2025 00:10:59 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7763d557b91f4c79d7252d72a9ad1e1c098ea14c6470585279d1fcbda0029c6`  
		Last Modified: Tue, 30 Dec 2025 00:11:00 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:af7d8c025ebf044f8b0e53b44dc9fc506c47b8b5b1ebe9ebe421deb5307e1c5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5999268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b9203b24c4955f7570ec09306998f057f7dbfbc62ee2372a5d809ccc39b8f5c`

```dockerfile
```

-	Layers:
	-	`sha256:2693de257acd9e7073d7cbcd6c477790b0063090a277dc5c2e92bcb953d59534`  
		Last Modified: Tue, 30 Dec 2025 03:14:01 GMT  
		Size: 5.9 MB (5945771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7c45ba0c6b490c25149f9540bf1bcacedd89513adbaee914f88ce7eae80e8bc`  
		Last Modified: Tue, 30 Dec 2025 03:14:02 GMT  
		Size: 53.5 KB (53497 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:5dedbf2d20216cdd563da8e866082cd5711e8c72b9005e82ac77b03166d39626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144056808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acc14d8fccb0a7d012360575bc27302bfa39cab0f6396488913f0bba652fd431`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:57:36 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 29 Dec 2025 23:57:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:57:49 GMT
ENV GOSU_VERSION=1.19
# Mon, 29 Dec 2025 23:57:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 29 Dec 2025 23:57:55 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 29 Dec 2025 23:57:55 GMT
ENV LANG=en_US.utf8
# Mon, 29 Dec 2025 23:57:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:57:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 29 Dec 2025 23:57:59 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 29 Dec 2025 23:57:59 GMT
ENV PG_MAJOR=17
# Mon, 29 Dec 2025 23:57:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Mon, 29 Dec 2025 23:57:59 GMT
ENV PG_VERSION=17.7-3.pgdg12+1
# Tue, 30 Dec 2025 00:13:00 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 30 Dec 2025 00:13:00 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Dec 2025 00:13:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Dec 2025 00:13:00 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Dec 2025 00:13:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 30 Dec 2025 00:13:00 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Dec 2025 00:13:00 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 00:13:00 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Dec 2025 00:13:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Dec 2025 00:13:00 GMT
STOPSIGNAL SIGINT
# Tue, 30 Dec 2025 00:13:00 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Dec 2025 00:13:00 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3733e79b87ec6af3c60809fa9882f5d220b1e1fc2459b7d6a5b3167dc8eb7155`  
		Last Modified: Mon, 29 Dec 2025 22:25:04 GMT  
		Size: 23.9 MB (23934053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d78ce8302283086832564a9937e5853b23a651ed9bcb8489a660c542dbeec9`  
		Last Modified: Tue, 30 Dec 2025 00:13:29 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a8b5e17ebbda1768569c39fe98d08644305edd5a209a473e2b27c9ed40335d`  
		Last Modified: Tue, 30 Dec 2025 00:13:29 GMT  
		Size: 3.7 MB (3742662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5258eb90c40bfefe40f259055e1008961f13c881e17e82e62326f6bedd31d7f6`  
		Last Modified: Tue, 30 Dec 2025 00:13:29 GMT  
		Size: 1.2 MB (1215952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4944a2fe03c0150b536f4caada272fe09622859709a088ad83ed5c1f7c654c43`  
		Last Modified: Tue, 30 Dec 2025 00:13:30 GMT  
		Size: 8.1 MB (8066448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b107bb911776c6b1f30efd64ab08d2240f47063e5fbbacc26cf4749f86f72f`  
		Last Modified: Tue, 30 Dec 2025 00:13:29 GMT  
		Size: 1.1 MB (1067251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf86b00e96a6ce8e8d7a962f2580c4f97359f9d0a253b3dc64dd63561cff64d7`  
		Last Modified: Tue, 30 Dec 2025 00:13:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9162ffbd4dfdef0a2d5ec2c4a63ee253e17f5aada39937b2a0510f3bc153200`  
		Last Modified: Tue, 30 Dec 2025 00:13:29 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cfb7aa8f3a42eee9a421228a269d0cd5a78797f96e4c4a153c859fe613e469a`  
		Last Modified: Tue, 30 Dec 2025 00:13:42 GMT  
		Size: 106.0 MB (106009461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b2c35d37ecb5c530e67c93fb48642feb25578d0c9f9e6f123b963d6db5c03a`  
		Last Modified: Tue, 30 Dec 2025 00:13:29 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0bf9f7d8f4382c034c958c3e6d8ab3e7ee5652f884a4a8a35aac364731bcc0`  
		Last Modified: Tue, 30 Dec 2025 00:13:29 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d3bd56a9ed7840b45bdad51ecd7983a3302ae8f4d06d4e6db68b3f80648877`  
		Last Modified: Tue, 30 Dec 2025 00:13:29 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c226da8adf4d9dca3b66ae978a3fbc0194d9a202a0a7aedab18c8ec858c7c24`  
		Last Modified: Tue, 30 Dec 2025 00:13:30 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6c11c5d0617ce38613ba10221ce73421d352e00fad979fd2b0a354b976f034`  
		Last Modified: Tue, 30 Dec 2025 00:13:30 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:5f2b2e0b74be29625b198c9c325f540aff1f66f4e2910b142fa9ad6eaaa2c61d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5998523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:294081172ed2b0052ce41480474eac742e574dabae51a6f96859cf96f1db3abd`

```dockerfile
```

-	Layers:
	-	`sha256:f8ca04c8c3d3102e466d1e845ed7f5b300d0704de7d824950163f2c5c07bc17d`  
		Last Modified: Tue, 30 Dec 2025 03:14:07 GMT  
		Size: 5.9 MB (5945026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3bb532fb6329ca746516f9109f43cc068cde09bc0d865888a207b324bf678d8`  
		Last Modified: Tue, 30 Dec 2025 03:14:08 GMT  
		Size: 53.5 KB (53497 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:a4184c406d40d6ec5c62a821a283f3d380e79776246973cf262f0008a188f5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (154015168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0093a91992cc527d309b48a4ac7456985d6c2508100185bfddb55fae87bfa9b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:40:30 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 29 Dec 2025 23:40:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:40:41 GMT
ENV GOSU_VERSION=1.19
# Mon, 29 Dec 2025 23:40:41 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 29 Dec 2025 23:40:46 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 29 Dec 2025 23:40:46 GMT
ENV LANG=en_US.utf8
# Mon, 29 Dec 2025 23:40:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:40:49 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 29 Dec 2025 23:40:50 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 29 Dec 2025 23:40:50 GMT
ENV PG_MAJOR=17
# Mon, 29 Dec 2025 23:40:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Mon, 29 Dec 2025 23:40:50 GMT
ENV PG_VERSION=17.7-3.pgdg12+1
# Mon, 29 Dec 2025 23:41:02 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 29 Dec 2025 23:41:02 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 29 Dec 2025 23:41:02 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 29 Dec 2025 23:41:02 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 29 Dec 2025 23:41:02 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 29 Dec 2025 23:41:02 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 29 Dec 2025 23:41:03 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:41:03 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 29 Dec 2025 23:41:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:41:03 GMT
STOPSIGNAL SIGINT
# Mon, 29 Dec 2025 23:41:03 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 29 Dec 2025 23:41:03 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa19b916d154cb9bfaea250caa1b464d95d68545103b7cef873bfd4411185f3b`  
		Last Modified: Mon, 29 Dec 2025 23:41:32 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8260a1fd5f074980f85b9971af2673456121b9d17389202c9c29b9d05d8e8e00`  
		Last Modified: Mon, 29 Dec 2025 23:41:32 GMT  
		Size: 4.5 MB (4519801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9866b342abeedf6488925d2b7aa7107b841eb2caabb4cd827ff3de4803daa766`  
		Last Modified: Mon, 29 Dec 2025 23:41:32 GMT  
		Size: 1.2 MB (1203226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296b4612d6f2bff9cf5b4d83fe643001de7b8961836062021f28f3f2069f29c2`  
		Last Modified: Mon, 29 Dec 2025 23:41:33 GMT  
		Size: 8.1 MB (8066469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3475a28d254c943197144d1568ff7ca2a7740332d811ecc45f92d36f9ef603f9`  
		Last Modified: Mon, 29 Dec 2025 23:41:32 GMT  
		Size: 1.1 MB (1108968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe133c084829e8528bffa092dc609ab78244bd6f14fea0978098137279d2863d`  
		Last Modified: Mon, 29 Dec 2025 23:41:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9832ff66a6b32bd086c7f77696ef5bdf9f04477e46af29a8a5a31c39f3ee21de`  
		Last Modified: Mon, 29 Dec 2025 23:41:32 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf5322e2f0fcfc73f19bd0183768f34249aef7e2bfa162f85ceee038b9557b2`  
		Last Modified: Mon, 29 Dec 2025 23:41:43 GMT  
		Size: 111.0 MB (110993520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fd41bb81379ef1b521ecf2d691e7e39191f9b8fc0c5994ec85cfe3ae6efb51`  
		Last Modified: Mon, 29 Dec 2025 23:41:32 GMT  
		Size: 10.2 KB (10232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776b935e076433673ae08f8ec1f25bfda58069e39ef8e0b2a4a62682fb410a70`  
		Last Modified: Mon, 29 Dec 2025 23:41:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f609b8df816a3d80e883c818d1f7ebc52b060065047f2bb53324a59a3e168fd`  
		Last Modified: Mon, 29 Dec 2025 23:41:33 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a951d49e586cbeade8a702e643e653a564fc21b1ffe5190cee061ad9ecee4cbd`  
		Last Modified: Mon, 29 Dec 2025 23:41:38 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35de89b8299eb6b98589b121cb0649cb1b1ecf87bacc23adf9974f3952c38711`  
		Last Modified: Mon, 29 Dec 2025 23:41:34 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:f8e8141c5be6b3fc0ab8bb6f76c1819563a9506fa217a4917eec036b1605f16b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5987302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8b74b61e66c4d8b6225a155fbdf5cb63787e9fe96155a79313e0c2b81c64685`

```dockerfile
```

-	Layers:
	-	`sha256:1ef34ee9e99784b2b4b470320490550a183c435651b96a282f91f65a81874fc6`  
		Last Modified: Tue, 30 Dec 2025 03:14:13 GMT  
		Size: 5.9 MB (5933767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0177515dc4bc3bd0ff1fcda5af79ff688e9dad114b51bd352ffc2b6eee194920`  
		Last Modified: Tue, 30 Dec 2025 03:14:14 GMT  
		Size: 53.5 KB (53535 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:f09349d9a32ddb606d0d1f468b292d63538aeafcfcba03a01903a01f026301c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.9 MB (164891363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:983c891c9d336a3615b200701e208d5668d4522e8f20c93813fc960b2b8e0efc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:33:32 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 29 Dec 2025 23:33:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:33:44 GMT
ENV GOSU_VERSION=1.19
# Mon, 29 Dec 2025 23:33:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 29 Dec 2025 23:33:48 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 29 Dec 2025 23:33:48 GMT
ENV LANG=en_US.utf8
# Mon, 29 Dec 2025 23:33:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:33:51 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 29 Dec 2025 23:33:52 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 29 Dec 2025 23:33:52 GMT
ENV PG_MAJOR=17
# Mon, 29 Dec 2025 23:33:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Mon, 29 Dec 2025 23:33:52 GMT
ENV PG_VERSION=17.7-3.pgdg12+1
# Mon, 29 Dec 2025 23:44:48 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 29 Dec 2025 23:44:48 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 29 Dec 2025 23:44:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 29 Dec 2025 23:44:48 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 29 Dec 2025 23:44:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 29 Dec 2025 23:44:48 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 29 Dec 2025 23:44:49 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:44:49 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 29 Dec 2025 23:44:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:44:49 GMT
STOPSIGNAL SIGINT
# Mon, 29 Dec 2025 23:44:49 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 29 Dec 2025 23:44:49 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f67520a70f469d560f84fd587586b5b9a9f46691d2f4b10c88544b5d21f5fe06`  
		Last Modified: Mon, 29 Dec 2025 22:24:46 GMT  
		Size: 29.2 MB (29209773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef6747ac61902a6df833d316d1701b69c088da0a03ead112d351ee8f39c4f14`  
		Last Modified: Mon, 29 Dec 2025 23:45:16 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc09525fd29f21bb4610da4a70ef8a40e6ea5cf35913c5e44a82ba1972364d15`  
		Last Modified: Mon, 29 Dec 2025 23:45:17 GMT  
		Size: 5.0 MB (4965432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3884589cee6a0dc12b139eedf6ca451c0b77d0a5b7564ee5571b64514aa4a2ba`  
		Last Modified: Mon, 29 Dec 2025 23:45:16 GMT  
		Size: 1.2 MB (1218667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c8c3fc2c20b4b50ef2812ebcd53740e2803e32fc5975ae21d87644565cfebd`  
		Last Modified: Mon, 29 Dec 2025 23:45:17 GMT  
		Size: 8.1 MB (8066418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dcd6f5c86acf4c2ca6139002f7907b1db3430ce5bb38980d04bb274bc8de0da`  
		Last Modified: Mon, 29 Dec 2025 23:45:16 GMT  
		Size: 1.1 MB (1137420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d637ae41d162c560b4f629ecb1153cea92507f5641c37a6ce282a2fdabd4cb1`  
		Last Modified: Mon, 29 Dec 2025 23:45:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e08df27c15ba859ce6fbef98882e42da40379444821d88ad0e565961f8103b`  
		Last Modified: Mon, 29 Dec 2025 23:45:16 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b536e57975959812635d5aefed10c3e204703a7c5aab1eefc921d70bfda75728`  
		Last Modified: Mon, 29 Dec 2025 23:45:25 GMT  
		Size: 120.3 MB (120272663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7255e8c09c5def0f20922da63f6b145d3aa632b790e37ac14c8bcfd7e88910cf`  
		Last Modified: Mon, 29 Dec 2025 23:45:16 GMT  
		Size: 10.2 KB (10237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff74ed5ad1c93afc5042a839c6ec7f41e04b8aa949cd9d5032777b9b06c0a89e`  
		Last Modified: Mon, 29 Dec 2025 23:45:16 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e024c28a6e7f128cf245781690a3a7ba230ff9867ba910bd35323b413d2683`  
		Last Modified: Mon, 29 Dec 2025 23:45:18 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adff3e240e5206d0515265d0ae7091a25f0e6b3d9495ae6e255aa86073b8a25`  
		Last Modified: Mon, 29 Dec 2025 23:45:18 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eddcff777c51e0a8d2d9cf7bc8313ddadcff7e71cfcff7c8ecf657d2312ab319`  
		Last Modified: Mon, 29 Dec 2025 23:45:18 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:f029b8f77aab8b2c3e33f2116d912d4411d542df90cc03c840b1c6e73bd1dd22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5997160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2cdbbc4ca376b33e8678d87eed92b47722a52b2c36b1da847b5698f080e5ff`

```dockerfile
```

-	Layers:
	-	`sha256:51659a7a4ad45ec85658672812fe1be9bcbcf74c40ad424b4130ca9f34a8a249`  
		Last Modified: Tue, 30 Dec 2025 03:14:21 GMT  
		Size: 5.9 MB (5943914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e610049e11c36f0c229014c7d4933dcd48a1a704bdbd90a00a50d876a96d3f7e`  
		Last Modified: Tue, 30 Dec 2025 03:14:21 GMT  
		Size: 53.2 KB (53246 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:41a66e7b42d40b35b47bba6ea0fe3ac055791543b7ba27dad1e58a9b68ab1784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.9 MB (154896964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a213b53229e4044eb86be24396956f0881d159f81d29cf564e7f6565aff1c9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 05:16:51 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Dec 2025 05:17:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 05:17:57 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Dec 2025 05:17:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Dec 2025 05:18:22 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 30 Dec 2025 05:18:22 GMT
ENV LANG=en_US.utf8
# Tue, 30 Dec 2025 05:18:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 05:18:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Dec 2025 05:18:43 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 05:18:43 GMT
ENV PG_MAJOR=17
# Tue, 30 Dec 2025 05:18:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 30 Dec 2025 05:18:43 GMT
ENV PG_VERSION=17.7-3.pgdg12+1
# Tue, 30 Dec 2025 07:42:10 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 30 Dec 2025 07:42:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Dec 2025 07:42:14 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Dec 2025 07:42:14 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Dec 2025 07:42:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 30 Dec 2025 07:42:16 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Dec 2025 07:42:17 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 07:42:19 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Dec 2025 07:42:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Dec 2025 07:42:19 GMT
STOPSIGNAL SIGINT
# Tue, 30 Dec 2025 07:42:19 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Dec 2025 07:42:19 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f479f5e9b924c5f7ef1d8b31a2c87cbd2a63c9fdc99e9e0c0cea7eae009e308c`  
		Last Modified: Mon, 29 Dec 2025 22:38:39 GMT  
		Size: 28.5 MB (28513809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca417b7ae950ff7970ad040b45abc24df944012e1756024d3f91656523cc30f8`  
		Last Modified: Tue, 30 Dec 2025 06:32:09 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8058603eaabaaed3c93fdfec7c2d4b77840d6fd5a151130f1c783e2de499479e`  
		Last Modified: Tue, 30 Dec 2025 06:32:09 GMT  
		Size: 4.5 MB (4475462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a676f9edcbcd2bb6defaca57cf7604e1ff4d96eb528e323ef74cd849bff4a90`  
		Last Modified: Tue, 30 Dec 2025 06:32:09 GMT  
		Size: 1.2 MB (1159183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f809eb30e7653bd1a9ce23c5ce36a429632d6088fa3f0348dd87900860b29e76`  
		Last Modified: Tue, 30 Dec 2025 06:32:09 GMT  
		Size: 8.1 MB (8066647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41385bcf55cc88174fc97e7d3019c5f94b8e8e5d4aa5c374766ad43452190273`  
		Last Modified: Tue, 30 Dec 2025 06:32:09 GMT  
		Size: 1.2 MB (1182926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a35a2d513dc5e6c316ef29fe04efa4c84517f5bf54fe460b95b551a22c3c0dc`  
		Last Modified: Tue, 30 Dec 2025 06:32:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:651c58be512fb2ee6b868cc910f9dbe2572916717b1affd127f4442c7a46a68f`  
		Last Modified: Tue, 30 Dec 2025 06:32:09 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09acc03af420ce869698e9ecc565bc8f3511b3f551571ea3475d85e0db2d71ff`  
		Last Modified: Tue, 30 Dec 2025 07:44:45 GMT  
		Size: 111.5 MB (111477945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd54ffde5dc845ada00113fbf500fdcf7b63279687fe9a0127a49c73ac9cdaa`  
		Last Modified: Tue, 30 Dec 2025 07:44:32 GMT  
		Size: 10.2 KB (10241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86155a5947bf4714dabfccc9e7f67a1a01aa07630e3a0c9e8136494df042a25`  
		Last Modified: Tue, 30 Dec 2025 07:44:33 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e131af8d19333e051ae1c470326790b3f7a49704d30db18c797399284b02c77`  
		Last Modified: Tue, 30 Dec 2025 07:44:33 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deed9ca1ae7c9a38842c23489ce3a803b16671f89cd42be9a7db75d8dee2100b`  
		Last Modified: Tue, 30 Dec 2025 07:44:43 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6b682a5ddb67b504352c0bbfb48677f3555423bf4cd6904e5c3dcb7a81fc78`  
		Last Modified: Tue, 30 Dec 2025 07:44:33 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:fc6a5d419ecf4a26d565854aff161a63f9d1a33ffe4bcf847a6561a5ed9fd392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 KB (53156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84d07008d8a32bb5faee1bb01dfc92cb8521a3c77b8f352e64ba93f653b3f16`

```dockerfile
```

-	Layers:
	-	`sha256:af825f76200d966842f5c862b1881a5c85c4d65f0ae36b2162ec8a73a1f7b95a`  
		Last Modified: Tue, 30 Dec 2025 09:08:39 GMT  
		Size: 53.2 KB (53156 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:def0cb8c8d7112e1081c99bb82da9118da0aca7f6b6a2b85d2b9c6435d018115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.8 MB (168836105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb3381906aaf748f0bac1c96a754c887086aeaafe2bf46ced545db8fc22d3aa4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 03:02:46 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Dec 2025 03:02:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 03:03:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Dec 2025 03:03:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Dec 2025 03:03:22 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 30 Dec 2025 03:03:22 GMT
ENV LANG=en_US.utf8
# Tue, 30 Dec 2025 03:03:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 03:03:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Dec 2025 03:03:30 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 03:03:30 GMT
ENV PG_MAJOR=17
# Tue, 30 Dec 2025 03:03:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 30 Dec 2025 03:03:30 GMT
ENV PG_VERSION=17.7-3.pgdg12+1
# Tue, 30 Dec 2025 03:06:00 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 30 Dec 2025 03:06:01 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Dec 2025 03:06:02 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Dec 2025 03:06:02 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Dec 2025 03:06:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 30 Dec 2025 03:06:03 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Dec 2025 03:06:05 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 03:06:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Dec 2025 03:06:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Dec 2025 03:06:06 GMT
STOPSIGNAL SIGINT
# Tue, 30 Dec 2025 03:06:06 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Dec 2025 03:06:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b7648f01f6858fc79caf032b4b9ed2f7e43e57f4621dc8cb36e84eb86399065b`  
		Last Modified: Tue, 30 Dec 2025 01:48:36 GMT  
		Size: 32.1 MB (32068844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8993cd576de63224175e2761513dac215150adcfd4397bd3d184de000db7f4`  
		Last Modified: Tue, 30 Dec 2025 03:05:10 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b32758d6de47fa496deec7238c75b37c97200b172a6808ca5de2c077bd488c7`  
		Last Modified: Tue, 30 Dec 2025 03:05:16 GMT  
		Size: 5.4 MB (5368513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488f1e8e76948ecd39b7aeead94f475539765a470c59ca8bef5788154f7c9729`  
		Last Modified: Tue, 30 Dec 2025 03:05:10 GMT  
		Size: 1.2 MB (1208180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c7ff6285c058d7fc3f1ea7a8f7d6c0eb9a90bfa212b60ca622fc14d7c8a2c8`  
		Last Modified: Tue, 30 Dec 2025 03:05:11 GMT  
		Size: 8.1 MB (8066536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cca05c3c74429ec7a9217ebaeedae6d89bde26f2e14a244c5d68d4fcb790078`  
		Last Modified: Tue, 30 Dec 2025 03:05:10 GMT  
		Size: 1.3 MB (1283676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f471299bd3ad24fe063c5ba0b3616af479e9a1a90966448e7c24050671b6a00`  
		Last Modified: Tue, 30 Dec 2025 03:05:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:446965b8fe7d7401776520ac6e95f2a321aa4c51d5d2bb7df64fc8dcc4b97162`  
		Last Modified: Tue, 30 Dec 2025 03:05:11 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77cd8d00b2c5628e4360281a8c429dc955d97539b6afb9e2f362c2673f3edbf8`  
		Last Modified: Tue, 30 Dec 2025 03:07:10 GMT  
		Size: 120.8 MB (120819379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9442c35094b4647553a05de5c94d364ce3714231ec068bf26591759f71040d79`  
		Last Modified: Tue, 30 Dec 2025 03:07:01 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9551d6d8034f328419b2b8a70154f47619f0ef298ae4510ee83db0268248e4`  
		Last Modified: Tue, 30 Dec 2025 03:07:01 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873dda26d13dca725bf90fc556a36675f43651928b86bf3bf981ef8e1d601c41`  
		Last Modified: Tue, 30 Dec 2025 03:07:01 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def70342619efe504fd68fb3349af0801f47c560cb936c84868539283f2f5440`  
		Last Modified: Tue, 30 Dec 2025 03:07:01 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140fd1b8afb647a4193ecf8c7c2007544145b70e6a72defb7172b02b3adddc78`  
		Last Modified: Tue, 30 Dec 2025 03:07:01 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:368d79262ce15757c674e590bdf2ad748eea292d6890d213c1dd97ba79b58d93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5988161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a29a58718a03e2daddefa918c41485eeb2d9e808e1dc6450d89b45c7437944a4`

```dockerfile
```

-	Layers:
	-	`sha256:a8fd49c7f3608697431da42bd56316179fd91bf15fe0753104cec78fdccfd300`  
		Last Modified: Tue, 30 Dec 2025 03:14:30 GMT  
		Size: 5.9 MB (5934817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f223205753f783ba4b0db00c33b99e239a8f5b7cf6b5248d4bff101544cf88f`  
		Last Modified: Tue, 30 Dec 2025 03:14:30 GMT  
		Size: 53.3 KB (53344 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:bdf5c18c7868870943a8a92c03e31d4889c13ce4dbdba490ac62a565bc2d4d46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.3 MB (165299549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce1661b754a4797be3ed724f95abf31dcc1d214551799c192ae3446e00f3f911`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:06:14 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Dec 2025 00:06:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:06:25 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Dec 2025 00:06:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Dec 2025 00:06:29 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 30 Dec 2025 00:06:29 GMT
ENV LANG=en_US.utf8
# Tue, 30 Dec 2025 00:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:06:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Dec 2025 00:06:32 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:06:32 GMT
ENV PG_MAJOR=17
# Tue, 30 Dec 2025 00:06:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 30 Dec 2025 00:06:32 GMT
ENV PG_VERSION=17.7-3.pgdg12+1
# Tue, 30 Dec 2025 00:18:16 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 30 Dec 2025 00:18:17 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Dec 2025 00:18:17 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Dec 2025 00:18:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Dec 2025 00:18:17 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 30 Dec 2025 00:18:17 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Dec 2025 00:18:17 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 00:18:17 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Dec 2025 00:18:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Dec 2025 00:18:17 GMT
STOPSIGNAL SIGINT
# Tue, 30 Dec 2025 00:18:17 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Dec 2025 00:18:17 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:908a8b9619550bcbaa302a1a1375bffd68fb4bab6330d7a965b0b9e3f3896a0a`  
		Last Modified: Mon, 29 Dec 2025 22:25:40 GMT  
		Size: 26.9 MB (26884397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb093f9deac517140ab39eb3b348f003f62dfb1dafeadbadb034710e8634e22`  
		Last Modified: Tue, 30 Dec 2025 00:18:58 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953df64371fe4409302c205cfc6579659baa5eb312339be84cb9609aaec6679e`  
		Last Modified: Tue, 30 Dec 2025 00:18:59 GMT  
		Size: 4.4 MB (4391229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490ddef0f5d915c746ab524cb88ea9c974a167ec04075163f939a669633f95f5`  
		Last Modified: Tue, 30 Dec 2025 00:18:58 GMT  
		Size: 1.2 MB (1222772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fbec28192a3869b0bf5862eda5a910f93024068591ea351effcd0278383abf`  
		Last Modified: Tue, 30 Dec 2025 00:18:59 GMT  
		Size: 8.1 MB (8120676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9baa2d8d8e645941be0f7f4131614ca802f37fb9c01a853565ca4b8f38b92255`  
		Last Modified: Tue, 30 Dec 2025 00:18:59 GMT  
		Size: 1.1 MB (1097023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f484c9594aef302d399b477aa8bc579b83faf3088b138c10cc37b2afca2b274`  
		Last Modified: Tue, 30 Dec 2025 00:18:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6fbe69e0c8de97bd6734911439802d6c8e66d1e6de295ce55b76d117faee54`  
		Last Modified: Tue, 30 Dec 2025 00:18:59 GMT  
		Size: 3.1 KB (3138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc1be6b8c0cbd57655c11c3893b863c35e95114f50fd4235e53fc3843622f42`  
		Last Modified: Tue, 30 Dec 2025 00:19:16 GMT  
		Size: 123.6 MB (123562469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c64aa2f181476be1727a4444fd8cdb4b23f28dfaa18f6987062a01564831387`  
		Last Modified: Tue, 30 Dec 2025 00:18:59 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1f5f31357261fcff3039b066221da027495e36b0bba64a577d4ae0520a7681`  
		Last Modified: Tue, 30 Dec 2025 00:18:59 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4613a9749cfbac3bfd3261415e915e307bf1e700b71b555ef376af51dbb6c8`  
		Last Modified: Tue, 30 Dec 2025 00:18:59 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070604a12e3ff6d44c2872ed115bb0ba48c7105555fe2605b2867c0121be827e`  
		Last Modified: Tue, 30 Dec 2025 00:18:59 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb7f098f09b41fcf9b4719cb5b0ec21d9f21c2b25e1c1967ed708416e15bc75`  
		Last Modified: Tue, 30 Dec 2025 00:18:59 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:934570e4384b6cda46abcda3674d041318b5fddfa18f1557a6bb04f84a0fc465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5993680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8580a89d98c400928a9d8d7af855136aad461169eb8e2d91cd1d9c5d5f3a62ff`

```dockerfile
```

-	Layers:
	-	`sha256:1e90ffa994b4274af1f40cfa3b3bafc1433144bcee9b590227450adbad62cd6a`  
		Last Modified: Tue, 30 Dec 2025 03:14:32 GMT  
		Size: 5.9 MB (5940390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e04fab2cf017f5f08946f06451c8e5a6c756528f2af0c61f1ae85fe9e99fcdf7`  
		Last Modified: Tue, 30 Dec 2025 03:14:33 GMT  
		Size: 53.3 KB (53290 bytes)  
		MIME: application/vnd.in-toto+json
