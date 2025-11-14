## `postgres:17-bookworm`

```console
$ docker pull postgres@sha256:921ba1b84a46af0acca974e9ddc33f3ae5feb7dd3f888b3a3ae05814fbc68117
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
$ docker pull postgres@sha256:5da02d1bc1d7178bc67344fe98ab15f584540e5e5a730b8308cd00fe10080f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (156016757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247a7ecfa4ebe985f739c1aaef7017ef5d0631032f292b45209b04b237ca315c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 19:19:10 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:19:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:19:21 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:19:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:19:25 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 14 Nov 2025 19:19:25 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:19:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:19:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:19:28 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 14 Nov 2025 19:19:28 GMT
ENV PG_MAJOR=17
# Fri, 14 Nov 2025 19:19:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Fri, 14 Nov 2025 19:19:28 GMT
ENV PG_VERSION=17.7-3.pgdg12+1
# Fri, 14 Nov 2025 19:19:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:19:40 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:19:40 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:19:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:19:40 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:19:40 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:19:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:19:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:19:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:19:40 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:19:40 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:19:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d97173786cdac79a26275c035c0ec91cdb76ff17eab18c7ff9728ba0addcf3`  
		Last Modified: Fri, 14 Nov 2025 19:20:11 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8bb52cc3ae3e0ea19fd9f2c7fd76027ff8997b47a0f1dbc183d036b0d02f9e`  
		Last Modified: Fri, 14 Nov 2025 19:20:11 GMT  
		Size: 4.5 MB (4534015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42717bffc43c4bc7dbbb989cca5cbb7496e12802d53fffad03e6f6d5172a4f3`  
		Last Modified: Fri, 14 Nov 2025 19:20:10 GMT  
		Size: 1.2 MB (1249519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5441f1c76b6ecbb90da460ed2400f7541292a6dca36c05b39c37556437f6c2`  
		Last Modified: Fri, 14 Nov 2025 19:20:12 GMT  
		Size: 8.1 MB (8066409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab58684c57979fbd0ce92a1e4793d4bcdfb65b452a51147499b1bda9645057a`  
		Last Modified: Fri, 14 Nov 2025 19:20:11 GMT  
		Size: 1.2 MB (1196368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a8eeade6c553b345920f877fd1df7b1bf951c4d50d7471780f4c9b4852410c`  
		Last Modified: Fri, 14 Nov 2025 19:20:11 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa7cbb3170d4142449d5875bec2e722bc75abae90992dd8cc14a2e5651f0b53`  
		Last Modified: Fri, 14 Nov 2025 19:20:10 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fb46d20cd7c85101f0e43c30fba88e54138c22e13b091b35f95d1e6fb17384`  
		Last Modified: Fri, 14 Nov 2025 19:20:21 GMT  
		Size: 112.7 MB (112720904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17aa4381b0d9bdb320b9113fb446c2431f19887f5d25908f8d99ac92fa1637b4`  
		Last Modified: Fri, 14 Nov 2025 19:20:11 GMT  
		Size: 10.2 KB (10238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319152189f3ea973e0b2494b05d6b47d862364c89f33a41377e70dabd48eb31a`  
		Last Modified: Fri, 14 Nov 2025 19:20:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c06df08e517331d4d8ed3a5c167ef1b57dfef7c2e5c749a23e913c3c212c4e`  
		Last Modified: Fri, 14 Nov 2025 19:20:10 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecca510992f5469ec11b3e1a57776b19e40b32d07db4db9501ffd564800fb35d`  
		Last Modified: Fri, 14 Nov 2025 19:20:11 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ef054814f6ed31b655501a8dab1b42f35c7f6c33a4796f6394ab02b8f60b0f`  
		Last Modified: Fri, 14 Nov 2025 19:20:11 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:dff00dbe5bc81c20fd99a1f6b4ff2119700b6177b792fa11dc82cd0851eb2ad9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5980746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc3ab39f65d5fe3a5a3b9e07f56265750d0818401b2efa97d9ca7898ec5d48a8`

```dockerfile
```

-	Layers:
	-	`sha256:e8afebe18cf03a75b64277841eee3e8b7834fd0c4f0a88f0d2073a86e3cf9496`  
		Last Modified: Fri, 14 Nov 2025 21:16:33 GMT  
		Size: 5.9 MB (5927456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bd9c8b53891b9f9c7f26074e005efa4aab14069a5856fe58cca26e5885bcde8`  
		Last Modified: Fri, 14 Nov 2025 21:16:34 GMT  
		Size: 53.3 KB (53290 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:34b79d4c891c26ba239a38071c1c3511ff4851c2e27f29e816aa4c4eef958bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (149044560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc86282c29af17672f2130c0adff4bea6f4137fef91dbe6ed597357b27f2339c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 19:32:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:32:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:32:23 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:32:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:32:29 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 14 Nov 2025 19:32:29 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:32:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:32:35 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:32:36 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 14 Nov 2025 19:32:36 GMT
ENV PG_MAJOR=17
# Fri, 14 Nov 2025 19:32:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Fri, 14 Nov 2025 19:32:36 GMT
ENV PG_VERSION=17.7-3.pgdg12+1
# Fri, 14 Nov 2025 19:47:56 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:47:57 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:47:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:47:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:47:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:47:57 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:47:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:47:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:47:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:47:57 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:47:57 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:47:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:def4b77141116a067c72a4f39eb9fa70634fe918be6e3df3cf0bc46323be22c7`  
		Last Modified: Tue, 04 Nov 2025 00:12:34 GMT  
		Size: 25.8 MB (25757661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b528453493c2cc37863e8e5a739e081c78c312f326bf3ef2bdafe099eea3182e`  
		Last Modified: Fri, 14 Nov 2025 19:48:33 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffbf26f8869aa16399753c4c5b2827ef88c544048616d809cc7c7cca4303f9e`  
		Last Modified: Fri, 14 Nov 2025 19:48:33 GMT  
		Size: 4.2 MB (4151222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb064a0b8ca77304a460984c5dfd86388491044268c9141b4c2511360aab223`  
		Last Modified: Fri, 14 Nov 2025 19:48:33 GMT  
		Size: 1.2 MB (1220077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e152a8db0fd36a9f1ea66d9e96d89516f08a0e1e4fa9ef935792666759cc8ab`  
		Last Modified: Fri, 14 Nov 2025 19:48:34 GMT  
		Size: 8.1 MB (8066552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eca893309571633fe5458f9150d7ca19637e5ab23bedcf941a8e96a6ab63629`  
		Last Modified: Fri, 14 Nov 2025 19:48:33 GMT  
		Size: 1.2 MB (1195036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6961c9489f0f4ba86b190395d467a11be831bf03cfc1988597c0fb18731fa608`  
		Last Modified: Fri, 14 Nov 2025 19:48:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eef1345344765e22998d93585860de6b877e9c1ea9484afcbe6819262a8ae12`  
		Last Modified: Fri, 14 Nov 2025 19:48:33 GMT  
		Size: 3.1 KB (3146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3b87f6277aa52bfa0de729939d9c2640984a1f697fc5b50d552d07d48f3cdc`  
		Last Modified: Fri, 14 Nov 2025 19:48:51 GMT  
		Size: 108.6 MB (108633017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91fe171d1fa39dd5161bfd5b5a05ae7f80ddb22a5fe46adc70e830cb4734d659`  
		Last Modified: Fri, 14 Nov 2025 19:48:33 GMT  
		Size: 10.2 KB (10243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fedfb899db4b7ae3f331ea844e423e7d7b53d36e940f310d0744012a25844ca`  
		Last Modified: Fri, 14 Nov 2025 19:48:33 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ab8998ce67f9133075f222de1f297bd2cf1939ed89655943e52125785ceb3e`  
		Last Modified: Fri, 14 Nov 2025 19:48:33 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1456ab937e29c351dba199813f4c225813f0aa65438e00efbee7548666dff9`  
		Last Modified: Fri, 14 Nov 2025 19:48:34 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751e7187553f1231672d1537e7a4fdb4feb35cee7a7b6040d267360fcc9ab0ee`  
		Last Modified: Fri, 14 Nov 2025 19:48:34 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:a2b7d27dbcd7b43b1d659b87208fae0df7a99ab9f45fd21735bd62186e80c117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5999268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d205bbf8ffd50950f08552187d650d224019f9790ede163dc97b5f384bc6542b`

```dockerfile
```

-	Layers:
	-	`sha256:96ca455e712b57758d4f862792b0b4c0f26d2c28f193047b6159d1749319990a`  
		Last Modified: Fri, 14 Nov 2025 21:16:39 GMT  
		Size: 5.9 MB (5945771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e2c7eec84e9e5c1dfa51f860b5753527c39657fa4a2016df3ad018f79faf48e`  
		Last Modified: Fri, 14 Nov 2025 21:16:40 GMT  
		Size: 53.5 KB (53497 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:af2c2d02c441870f0639a7bb5ee250a5099a2ddbeb4c7a8082991f26f4efd61c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144062441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1772b9e8ad1e0105a0fa2d4385a5f27fdf0f5890b1a1781bd262651524ee17d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 19:22:44 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:22:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:22:57 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:22:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:23:03 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 14 Nov 2025 19:23:03 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:23:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:23:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:23:08 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 14 Nov 2025 19:23:08 GMT
ENV PG_MAJOR=17
# Fri, 14 Nov 2025 19:23:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Fri, 14 Nov 2025 19:23:08 GMT
ENV PG_VERSION=17.7-3.pgdg12+1
# Fri, 14 Nov 2025 19:49:38 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:49:39 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:49:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:49:39 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:49:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:49:39 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:49:39 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:49:39 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:49:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:49:39 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:49:39 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:49:39 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:dae611a010be6eab1cdff516b7db8214a5d92b74372702ade8cd5e6bb793dfdd`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 23.9 MB (23934126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f938f8fa2e74fd1797642b36eb1eaa82f84b121d463a1877fc11f4dbd7051e`  
		Last Modified: Fri, 14 Nov 2025 19:34:49 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32192eee72583a220f92e6b20624e8c5e54f39fcd4d2868fea051345cbac464a`  
		Last Modified: Fri, 14 Nov 2025 19:34:49 GMT  
		Size: 3.7 MB (3742621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17b6491688748b24c9be0c13cd25cdb6a89955f998dfcf9015394d24ac84a50`  
		Last Modified: Fri, 14 Nov 2025 19:34:49 GMT  
		Size: 1.2 MB (1215946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8918a8f710f2ee816680f8feb56a3d1588b1d28960965b68364da61966fec4cc`  
		Last Modified: Fri, 14 Nov 2025 19:34:50 GMT  
		Size: 8.1 MB (8066396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3b56d27d2534bf60a5d8fc2c737dff996ce6fd389e34dc9e5492058f89d21f`  
		Last Modified: Fri, 14 Nov 2025 19:34:49 GMT  
		Size: 1.1 MB (1067230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb6a12119f803b7e40ec7293563f54d66bfd591b71c51b799c6fa9f994e57e5`  
		Last Modified: Fri, 14 Nov 2025 19:34:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:504b209e972547b6f8c6f00853f6c5c4e461b95f1596810ee4abf1f3ea835a88`  
		Last Modified: Fri, 14 Nov 2025 19:34:49 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e812f1207e447cf516674f1b27497f3335f3957e2b5297f3519525ceb14263`  
		Last Modified: Fri, 14 Nov 2025 19:50:14 GMT  
		Size: 106.0 MB (106015135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a294b2d2c066ac3723e79430569721dfe430c9ed9ce69e4da1f7bdc80cb9c8e`  
		Last Modified: Fri, 14 Nov 2025 19:50:05 GMT  
		Size: 10.2 KB (10243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b817a75257235378803e97626f67c88eb4686c531fc38ca19bb4e98187896de`  
		Last Modified: Fri, 14 Nov 2025 19:50:05 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5f2d30d8b3f0ab498e65c772db8ac8073900e6e7ed14cd59179729c05e5044`  
		Last Modified: Fri, 14 Nov 2025 19:50:05 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca088ca3e9f7402fe54ac1cacc1354e592039d1210fe213cbc3dde63c2db80d`  
		Last Modified: Fri, 14 Nov 2025 19:50:05 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd6d4d4da2140ce3421a3bea9bab3f5978f3d7cdd4aea25ffb604b0d0125d41`  
		Last Modified: Fri, 14 Nov 2025 19:50:05 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:37a1015699477e521c9a92f6aea05346c9471713068ce0f59f6b028ebe910a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5998522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f072a4004904bce194380bb9a1295764642395ef8664ec45dbbea695e57e781f`

```dockerfile
```

-	Layers:
	-	`sha256:23456f0b9d4267d9b535149f40ba078a8d74cf8f2d76c12cfba095be7c243953`  
		Last Modified: Fri, 14 Nov 2025 21:16:46 GMT  
		Size: 5.9 MB (5945026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d39538d8325f19827a0bbec10ad7ab1d9df148d487cac23ea33912c7b9119ce`  
		Last Modified: Fri, 14 Nov 2025 21:16:47 GMT  
		Size: 53.5 KB (53496 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:e1523dcbec4451b0c7fde45a1e068991b739908461dcaca454792737782da9a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (154015116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9080d7353797810fd5df59ec26afc5ee3fe2515750ce7f48e9ddfe29346ed08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 19:18:32 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:18:37 GMT
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
# Fri, 14 Nov 2025 19:18:53 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 14 Nov 2025 19:18:53 GMT
ENV PG_MAJOR=17
# Fri, 14 Nov 2025 19:18:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Fri, 14 Nov 2025 19:18:53 GMT
ENV PG_VERSION=17.7-3.pgdg12+1
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
	-	`sha256:040e4b8bba569865d8707869b62e973bd300fbb26452dcefbb852b62eebf0cad`  
		Last Modified: Fri, 14 Nov 2025 19:19:40 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350040fc66b7ec8ac2805f3b1986954b94046af24af0404dadd529a752af0e9f`  
		Last Modified: Fri, 14 Nov 2025 19:19:40 GMT  
		Size: 4.5 MB (4519837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1465d96194a8e7200c6bf4802bc0141b50a649996e4a786c255f9c72dc4e56`  
		Last Modified: Fri, 14 Nov 2025 19:19:40 GMT  
		Size: 1.2 MB (1203277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa1f58376e5638b6f0d20b4f1d22491be60156711b86b431442277205d95467`  
		Last Modified: Fri, 14 Nov 2025 19:19:40 GMT  
		Size: 8.1 MB (8066471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4fc449f26d93b1b27e8f3df3d8dc3d5fcc3d3dbbb694bd71d594cfbc145b86`  
		Last Modified: Fri, 14 Nov 2025 19:19:40 GMT  
		Size: 1.1 MB (1108986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f992d4fdce490df33287772e92b3fca5960a360c7755f503a0aff6264e22419`  
		Last Modified: Fri, 14 Nov 2025 19:19:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2667b699fd69ff0862614b60c753fa21405fdd21fd63264c317c180cf83634b`  
		Last Modified: Fri, 14 Nov 2025 19:19:40 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1188d2db4a0ac7b937b54f98e52a308f68e3b1f7197143c995c9ff4bf80172dc`  
		Last Modified: Fri, 14 Nov 2025 19:19:59 GMT  
		Size: 111.0 MB (110993178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3806eaa55c59ba00d7731b4ad7cd2fb598316621b1892dc7d8083ff9dc267053`  
		Last Modified: Fri, 14 Nov 2025 19:19:40 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920b012e09eec22348b88bcb28522888887e3b67afdfb64d843262539bc93dfa`  
		Last Modified: Fri, 14 Nov 2025 19:19:40 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c71bc2e3d5f11e73892da63b0f63f57cce0e8788a4c186595f07d0f99ef934f`  
		Last Modified: Fri, 14 Nov 2025 19:19:41 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a83460a36505b4640bbcc2fc5b7bf37fe4b810764dbd911d3338a3476673fc`  
		Last Modified: Fri, 14 Nov 2025 19:19:41 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b4da7e64bdc848fe1c6e330d6f278f79020895fbad5d1630ae7fcd08046ed5`  
		Last Modified: Fri, 14 Nov 2025 19:19:41 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:75ca2a7ca938b7902b09b20e80154c546e7c35cebb77db5aea28cb2524b816e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5987302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8089e84203614b2813986b8dd49b347bcd329f7cebe8360c7ca5f770e22b4973`

```dockerfile
```

-	Layers:
	-	`sha256:7fd6565e25d886cab272023dd2dc360d9a7d8e763b149eaac90a3802d13f2e42`  
		Last Modified: Fri, 14 Nov 2025 21:16:52 GMT  
		Size: 5.9 MB (5933767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdef19254f0b8cc6a1f0719547519f261da8d4f73f6178455ba7ce8cbb098987`  
		Last Modified: Fri, 14 Nov 2025 21:16:53 GMT  
		Size: 53.5 KB (53535 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:7c4f652447c4d592043cb31a0c7a367d717f7402ec407735597902a9b80a82cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.9 MB (164887119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16dcc46d8b810aab42c961b167d60d36e7f0e53236e9ac4df8369a1c8017c960`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 19:19:23 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:19:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:19:33 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:19:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:19:37 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 14 Nov 2025 19:19:37 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:19:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:19:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:19:41 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 14 Nov 2025 19:19:41 GMT
ENV PG_MAJOR=17
# Fri, 14 Nov 2025 19:19:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Fri, 14 Nov 2025 19:19:41 GMT
ENV PG_VERSION=17.7-3.pgdg12+1
# Fri, 14 Nov 2025 19:30:03 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:30:03 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:30:04 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:30:04 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:30:04 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:30:04 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:30:04 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:30:04 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:30:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:30:04 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:30:04 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:30:04 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e0dafb38d1608fdb0908090be60250d2f739b5a9191857a4c4a74ebd3ef3b814`  
		Last Modified: Tue, 04 Nov 2025 00:12:54 GMT  
		Size: 29.2 MB (29209846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727e079d64d0a29c2bed64ebf9f5ea06715aee8cf8bf0f508f9b161672c94f8b`  
		Last Modified: Fri, 14 Nov 2025 19:29:01 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d5da86839ec850780059dbd29f5367d3dbbbbcab493e64c4c5c244c715efbe3`  
		Last Modified: Fri, 14 Nov 2025 19:30:34 GMT  
		Size: 5.0 MB (4965356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce7fd3ce2e3e5641c4151e99222c98f5d36f2f5ae579d817dd3dbbb02a633c8`  
		Last Modified: Fri, 14 Nov 2025 19:30:33 GMT  
		Size: 1.2 MB (1218614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e775dbb80d7fba32183307d7353fc6b17f2ec355cdb8eef4fd8ee88a3b122d`  
		Last Modified: Fri, 14 Nov 2025 19:30:33 GMT  
		Size: 8.1 MB (8066397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a54063eeba25070973287dd6c098d83603d0ddcf5ee1dabf7ba4517d3e83abc`  
		Last Modified: Fri, 14 Nov 2025 19:30:33 GMT  
		Size: 1.1 MB (1137400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975b3e5a4a881ca8ac3fbc71cab30528d07d3a1c38263e1fa7e1618cb2d0c4c6`  
		Last Modified: Fri, 14 Nov 2025 19:29:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fde6312145b45e8cd43dc3a9f97d7b5c8680a12d871bf7dbad43d7bcae931c2`  
		Last Modified: Fri, 14 Nov 2025 19:30:33 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c979a2876b670f7ed7d49a4b5e7d0ac0f6b6d3600262c3ef4956c6096cce1d27`  
		Last Modified: Fri, 14 Nov 2025 19:30:53 GMT  
		Size: 120.3 MB (120268520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9a645c20ff22ff69252390f1226ede1f7f8791701fe0d808559a57e9bd26bd`  
		Last Modified: Fri, 14 Nov 2025 19:30:33 GMT  
		Size: 10.2 KB (10242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96b210b1872bd7503041a52d386e3143d1274d06fb49d5319801726c9c86286`  
		Last Modified: Fri, 14 Nov 2025 19:30:33 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ff8ce90ec2ccae746fdb5a63be4f92b1527936fd5d3c4d90e69042125d93f2`  
		Last Modified: Fri, 14 Nov 2025 19:30:33 GMT  
		Size: 165.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65630427a680281db151c5a226678f31c6667518d43f0ac95230ec4d70a01178`  
		Last Modified: Fri, 14 Nov 2025 19:30:33 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377de80a473e257e9bf0cb607365184a79a23b0a1a298d8d93492cb5144626f7`  
		Last Modified: Fri, 14 Nov 2025 19:30:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:d43fd85b7257594f0d774bc46ec839903f299103bea072a298c80dae6f183d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5997160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb2d664fa8506e234d0f423ad6d2e4691c85255a3910b7f0aa244c89b0255519`

```dockerfile
```

-	Layers:
	-	`sha256:ad9df48395a39e274da7fe3a8a61d010b3ac75d2660696e1a127d7296905b8a9`  
		Last Modified: Fri, 14 Nov 2025 21:17:00 GMT  
		Size: 5.9 MB (5943914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c00169124293c95011651b2d393ab33b5707065c6971c1662cb7e5b5e4cd2554`  
		Last Modified: Fri, 14 Nov 2025 21:17:01 GMT  
		Size: 53.2 KB (53246 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:8920e2574668f255161445adc208ebf53d2ecf32cc56c8bb207b95f6dc5eb9e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.9 MB (154896631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7066b4b213a02b73af2db9719a7e8973a51ce5abdd755130f44762498401846`
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
ENV PG_MAJOR=17
# Thu, 13 Nov 2025 21:07:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 13 Nov 2025 21:07:02 GMT
ENV PG_VERSION=17.7-3.pgdg12+1
# Thu, 13 Nov 2025 23:31:21 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 13 Nov 2025 23:31:23 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Nov 2025 23:31:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Nov 2025 23:31:25 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Nov 2025 23:31:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Nov 2025 23:31:27 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 20:29:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 20:29:45 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 20:29:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 20:29:45 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 20:29:45 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 20:29:45 GMT
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
	-	`sha256:0269ad42fa2af63aa50b35d322fe106ea806c014754592d381e951263a18f9f8`  
		Last Modified: Thu, 13 Nov 2025 23:33:59 GMT  
		Size: 111.5 MB (111477362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d30227eadb47c1a6ec5851bc4ec60c03ddf49055abd9539f80b27559666bad1`  
		Last Modified: Thu, 13 Nov 2025 23:33:44 GMT  
		Size: 10.2 KB (10245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74aba0b8b30c870c7ee1d4fc2549c724f70ca03e25bec3c8bd862e6863fceda2`  
		Last Modified: Thu, 13 Nov 2025 23:33:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2659501f47d465cf285c0ed841631441043e0d83f7fd5cccdbe980a036f940`  
		Last Modified: Thu, 13 Nov 2025 23:33:44 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965d2a1d5d00bac210e3a93ca4c2f95edf42d0907ee823605a059889f5880057`  
		Last Modified: Fri, 14 Nov 2025 20:30:19 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90241d9b0d6a6bfefbe328d3b56c3d871fc207de1d8c5f93656848d5bf78a1e5`  
		Last Modified: Fri, 14 Nov 2025 20:30:19 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:c54672babfbfe7c70de860404d740d602f5ee1eb4360b4ec59ff0a538ac9ae38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 KB (53156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b38d30cf777413bff7d27390d3bdd6b1c143aa48d7b898aeaada5e98cdb88f7b`

```dockerfile
```

-	Layers:
	-	`sha256:787cadbdae0bc1f766840d033cba5c43161295c896f8035223a3e767ce8f2c5c`  
		Last Modified: Fri, 14 Nov 2025 21:17:06 GMT  
		Size: 53.2 KB (53156 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:91644f0470ae63fd6e9979053bd8cca5783b2160d1538ee566c46a49ad630daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.8 MB (168835814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04443aa9dfed3ef45d4a6070b0a1027fb1bde2eb02cdc8f806e90394ddc9339a`
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
ENV PG_MAJOR=17
# Thu, 13 Nov 2025 21:06:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 13 Nov 2025 21:06:56 GMT
ENV PG_VERSION=17.7-3.pgdg12+1
# Thu, 13 Nov 2025 21:18:23 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 13 Nov 2025 21:18:24 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Nov 2025 21:18:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Nov 2025 21:18:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Nov 2025 21:18:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Nov 2025 21:18:25 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:32:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:32:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:32:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:32:08 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:32:08 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:32:08 GMT
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
	-	`sha256:5dc65498a99b84f9f517dceb59200c293f33f3353ef850894ee57b0b088bfbcc`  
		Last Modified: Thu, 13 Nov 2025 21:19:26 GMT  
		Size: 120.8 MB (120819245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ff920552e1c84b41a97edae5d257fa59a2b17d846be60cef66d46ba87e7554`  
		Last Modified: Thu, 13 Nov 2025 21:19:17 GMT  
		Size: 10.2 KB (10241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50c373604ccfa4b48fe99e6f06d54777f37cec6a74d989704812d6538733bf8`  
		Last Modified: Thu, 13 Nov 2025 21:19:17 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11ee8d3601d53c6ae56d78430a904e59de1332f4f46f256ca15690fe0787b72`  
		Last Modified: Thu, 13 Nov 2025 21:19:17 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2be38359c79c6a95a021f66531ec44107cc3d23c720a7e9d46486e9c0ef09a`  
		Last Modified: Fri, 14 Nov 2025 19:32:53 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8d6731fed629c64f53dbc22f6cccb54b3a63b60021a416840fcee4b8dbd33f`  
		Last Modified: Fri, 14 Nov 2025 19:32:53 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:adb3a36f6194b6ffdaced08027c777db58f33206fb2e130670dbfbfb010302a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5988161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5f0bbeeefaebbd1234f7fa2813ba7e640ba3ba594bd3d87438fdcd0fa4e3116`

```dockerfile
```

-	Layers:
	-	`sha256:283c109657712b64e3fc19a7599234a804c21354c3e278082f488dd0b8e08c14`  
		Last Modified: Fri, 14 Nov 2025 21:17:10 GMT  
		Size: 5.9 MB (5934817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f9404b93c34ff75ea891dc6e4b4bbaa68f68fca7260110f69413c695c56ba7d`  
		Last Modified: Fri, 14 Nov 2025 21:17:11 GMT  
		Size: 53.3 KB (53344 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:076b833f9ab0b4954b67bc407f95fbe05f7d211ac9a47da824c8bbb60af61640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.3 MB (165304484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b06711f5cb0dd43761bacb10789a5dd8e131fdea793bacfe208e63101db9f8fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 01:06:18 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 01:06:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:06:29 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 01:06:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 01:06:33 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 14 Nov 2025 01:06:33 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 01:06:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:06:36 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 01:06:37 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 14 Nov 2025 01:06:37 GMT
ENV PG_MAJOR=17
# Fri, 14 Nov 2025 01:06:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Fri, 14 Nov 2025 01:06:37 GMT
ENV PG_VERSION=17.7-3.pgdg12+1
# Fri, 14 Nov 2025 19:33:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:33:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:33:26 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:33:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:33:26 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:33:26 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:33:26 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:33:26 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:33:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:33:26 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:33:26 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:33:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f8fa7c9be40e65c6864a8067075ec5b333329c2a64af66826dd5ac9227bbb7`  
		Last Modified: Fri, 14 Nov 2025 01:20:20 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20aee8139c54cf291aecadb44b89451118714e2196939c90b774dec33e567b27`  
		Last Modified: Fri, 14 Nov 2025 01:20:21 GMT  
		Size: 4.4 MB (4391303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74fb3c76a11d58811e75513137736de479edf26bb633dede480ec83c00ff5782`  
		Last Modified: Fri, 14 Nov 2025 01:20:21 GMT  
		Size: 1.2 MB (1222780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f92f27a0f2e926eed87d09ada3e43f3d25f045220cc9b8fbf4d24c4209869a`  
		Last Modified: Fri, 14 Nov 2025 01:20:22 GMT  
		Size: 8.1 MB (8120665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0522a54daed1b0ec3734c45eec7150c8c4b9fd9096be1a57a695ed6ada4134`  
		Last Modified: Fri, 14 Nov 2025 01:20:21 GMT  
		Size: 1.1 MB (1097023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0aeac068244937cecae3d66002544be8f25d6b576886c2db71f3e7ed6e8f82`  
		Last Modified: Fri, 14 Nov 2025 01:20:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c286a97ecfb3938dd38e57b6779ef0b5c261fccfc81873eb3c40258d0bbeac81`  
		Last Modified: Fri, 14 Nov 2025 01:20:21 GMT  
		Size: 3.1 KB (3146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204010812a9cc0b59dd8e86932454126399842ebae988ffcc0b8ed951311866d`  
		Last Modified: Fri, 14 Nov 2025 19:34:19 GMT  
		Size: 123.6 MB (123567171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c125c62dd3162b3ca28967167108531b4d4c8908308264fec42e73e653fd9901`  
		Last Modified: Fri, 14 Nov 2025 19:34:08 GMT  
		Size: 10.2 KB (10245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3058314a3877463a4508985fd60f161c511b2ca84e21377d452a68ca876ac93a`  
		Last Modified: Fri, 14 Nov 2025 19:34:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28aa7796f7d083b30db6937473b7a89e6d26040d6952cd7c5a749cd44228d9cc`  
		Last Modified: Fri, 14 Nov 2025 19:34:09 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80113feff7db427b5e9dc71c380edb06749183e3b9e2e10ff652d9cfb59aa0d0`  
		Last Modified: Fri, 14 Nov 2025 19:34:08 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca145c0bd45e69312f80b221a5848713df0c77a7fb5e9a7967f87266d641b204`  
		Last Modified: Fri, 14 Nov 2025 19:34:09 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:67cfbe7f2ab5feb8c2071e25fd1d717f85da971ff37c1ebb148522b68eb0cc34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5993680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c59575376ebdc414c91ffda20a1663e70f6b0c804f25109e1adcb17c520fceb4`

```dockerfile
```

-	Layers:
	-	`sha256:b0a86ac174ce57d72ce545ce359c7edc59f156201ed939c362dc7cabfb104691`  
		Last Modified: Fri, 14 Nov 2025 21:17:16 GMT  
		Size: 5.9 MB (5940390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f236417ffcd2f36197387c5346edbbf4bb656f7cfe7825266b5a49bc39a30e0c`  
		Last Modified: Fri, 14 Nov 2025 21:17:17 GMT  
		Size: 53.3 KB (53290 bytes)  
		MIME: application/vnd.in-toto+json
