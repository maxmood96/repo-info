## `postgres:latest`

```console
$ docker pull postgres@sha256:7aba8c66107ee218ddbaacb30eae46d774bf5e34ab77a917be819b4e227493c4
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
$ docker pull postgres@sha256:41da01536bc3ae26308cefb0c57235e7488001360bdb15191eb0b7955b570299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.4 MB (162352309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1892662ab56773f96746107054fcfec3d7cd32d39a34fabec4a57f66bd15524`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:15:33 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 19 May 2026 23:15:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:15:44 GMT
ENV GOSU_VERSION=1.19
# Tue, 19 May 2026 23:15:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 19 May 2026 23:15:48 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 19 May 2026 23:15:48 GMT
ENV LANG=en_US.utf8
# Tue, 19 May 2026 23:15:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:15:51 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 19 May 2026 23:15:52 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:15:52 GMT
ENV PG_MAJOR=18
# Tue, 19 May 2026 23:15:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 19 May 2026 23:15:52 GMT
ENV PG_VERSION=18.4-1.pgdg13+1
# Tue, 19 May 2026 23:16:07 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 19 May 2026 23:16:07 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 19 May 2026 23:16:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 19 May 2026 23:16:07 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 19 May 2026 23:16:07 GMT
VOLUME [/var/lib/postgresql]
# Tue, 19 May 2026 23:16:07 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:16:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 19 May 2026 23:16:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 23:16:08 GMT
STOPSIGNAL SIGINT
# Tue, 19 May 2026 23:16:08 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 19 May 2026 23:16:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da70ae85cfc17a8f7e6df938c2f030edd51c5a487dfc5564f1099553a292cd2`  
		Last Modified: Tue, 19 May 2026 23:16:27 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d007497f293c358abea16cd8c4d9b89213ff7e7fc5e048eca3a7eddfc32c168`  
		Last Modified: Tue, 19 May 2026 23:16:27 GMT  
		Size: 6.4 MB (6443077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e30f1af2eaf6303ecc4be386f71ba20362d2e5f571df2554fd289c2eafa226c`  
		Last Modified: Tue, 19 May 2026 23:16:27 GMT  
		Size: 1.3 MB (1256782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03be55d5ab4481850c4e21fe3fdf34cf9afcd8f4cf8049dd422656e15e9a7477`  
		Last Modified: Tue, 19 May 2026 23:16:27 GMT  
		Size: 8.2 MB (8203870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61b753ab936ad1d71e8bd95bd4cf9236733c0992bfb8eaaa126d89955b66b83`  
		Last Modified: Tue, 19 May 2026 23:16:28 GMT  
		Size: 1.3 MB (1311605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca2487a2d311ee0980a7b68deb4024437a81d0a181702ac9db4f372d777fdc2`  
		Last Modified: Tue, 19 May 2026 23:16:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cfc50f93c878b4a98a6acc781dc036bca1184457787d5c7609e543ff469c723`  
		Last Modified: Tue, 19 May 2026 23:16:29 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d454463c51b755d792dbc20885756c529c10f9de9f7992f4b0b36395fefb8ae4`  
		Last Modified: Tue, 19 May 2026 23:16:31 GMT  
		Size: 115.3 MB (115326876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f99fd2a8a25c7aabb69e4c93023a695840dc6a4f1f962f12c19e9d935e57c1`  
		Last Modified: Tue, 19 May 2026 23:16:29 GMT  
		Size: 19.3 KB (19330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f93b17e79df699e9e4dfd3da3d5cac4b29299913e83507e2104f9e4fb94d28c`  
		Last Modified: Tue, 19 May 2026 23:16:30 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732b1f237736ef16ec36e6b00c56b2bec432b33dfe30e94baa2502f0f879f95b`  
		Last Modified: Tue, 19 May 2026 23:16:30 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eab7b05d783b0b7bf8a26cb6bf2a2e6305bb3d8f73e11d14c8df9799d6f6582`  
		Last Modified: Tue, 19 May 2026 23:16:31 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:a22ea5f97521e0efa9987e2bc9a2c76c637722182c868bbb31a049a5766a62bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6009289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd614ce49f5a9934d39467c55160ec9858b762e3215770d0f22d5974fe89c0b5`

```dockerfile
```

-	Layers:
	-	`sha256:d52c4da08c7cfbece5e8cd6c41d67d44c5c4d22dcdf906789b7cfe3806fd7558`  
		Last Modified: Tue, 19 May 2026 23:16:27 GMT  
		Size: 6.0 MB (5956831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:412e7df169d157e8d2ad06dbbb9d939d3f3f66459002bea083dcf1e7856509fd`  
		Last Modified: Tue, 19 May 2026 23:16:27 GMT  
		Size: 52.5 KB (52458 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; arm variant v5

```console
$ docker pull postgres@sha256:b26be9a33486f2911f68a160d4df26aa3ff6cdd3ac3988cf664f48bfda96a722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91492843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a60da82da85f36d90dc830ed0da5950446f858887c7d520288c484babfb3a3c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:24:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 19 May 2026 23:24:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:24:28 GMT
ENV GOSU_VERSION=1.19
# Tue, 19 May 2026 23:24:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 19 May 2026 23:24:36 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 19 May 2026 23:24:36 GMT
ENV LANG=en_US.utf8
# Tue, 19 May 2026 23:24:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:24:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 19 May 2026 23:24:43 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:24:43 GMT
ENV PG_MAJOR=18
# Tue, 19 May 2026 23:24:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 19 May 2026 23:24:43 GMT
ENV PG_VERSION=18.4-1.pgdg13+1
# Tue, 19 May 2026 23:37:47 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 19 May 2026 23:37:47 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 19 May 2026 23:37:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 19 May 2026 23:37:47 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 19 May 2026 23:37:47 GMT
VOLUME [/var/lib/postgresql]
# Tue, 19 May 2026 23:37:47 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:37:47 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 19 May 2026 23:37:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 23:37:47 GMT
STOPSIGNAL SIGINT
# Tue, 19 May 2026 23:37:47 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 19 May 2026 23:37:47 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:37dea77b903ae642229487445fa64e20dcf83d60070467f9c7581fb71a2dd8a8`  
		Last Modified: Tue, 19 May 2026 22:36:45 GMT  
		Size: 28.0 MB (27953869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d433221719dd9e62a0f7816a4359b03832a253e360f390fbdcdd04a3747e03`  
		Last Modified: Tue, 19 May 2026 23:38:00 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19bdea52729aba7ced197c9d8e5dbda5632aebc9d72d33147b5699722ad8f15d`  
		Last Modified: Tue, 19 May 2026 23:38:00 GMT  
		Size: 5.9 MB (5934285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bfba22f380e06f12f01c62356b98d921a0223ce9d4b3e8312684f405494b293`  
		Last Modified: Tue, 19 May 2026 23:38:00 GMT  
		Size: 1.2 MB (1227549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c68b0d346400bd43798bdfa77d97f5899e858950c2761c76ab338ffb1228a4`  
		Last Modified: Tue, 19 May 2026 23:38:00 GMT  
		Size: 8.2 MB (8204211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a881e54df0f344aee4a8c4c7326765023de40045d019ff94a4296ae2aeba7f11`  
		Last Modified: Tue, 19 May 2026 23:38:01 GMT  
		Size: 1.3 MB (1317326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f9187b86ceca8e7ddde0cd3f8c2b2d11c9575031d71477b82c0a2662d1a56d`  
		Last Modified: Tue, 19 May 2026 23:38:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d01d2906e0cd35a9437156ef0a7d322c6cfc90e7b9789ae2a6816b2cf40424`  
		Last Modified: Tue, 19 May 2026 23:38:02 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30242a3b3c821cc449039733ad8fcf74b5e4202a3d5d2c5b7edb0f96c5e5b39d`  
		Last Modified: Tue, 19 May 2026 23:38:03 GMT  
		Size: 46.8 MB (46825442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9187ab7697a06ea36c7d3a3543b501f22699611071ad3053ddf0a47d0261577`  
		Last Modified: Tue, 19 May 2026 23:38:02 GMT  
		Size: 19.3 KB (19322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d972d52867f8a1a269c69ed81f80cb2273137407aece4eae6cb013ed05652d`  
		Last Modified: Tue, 19 May 2026 23:38:03 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb5665e83203e85659b77e75ef9597ded7d10fa60bab4c9c303ac4e789d5389`  
		Last Modified: Tue, 19 May 2026 23:38:03 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611ac8bb8409fab89b8d0ad81c26c6d62c1757ccb00ce5d006f0aab542986558`  
		Last Modified: Tue, 19 May 2026 23:38:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:b04a62807c5a961198d06eff7732c6d95f2304bacbfdc9745da91a9e3eda0ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5172653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d729a7c5e9c2a9376f576e940528f9e0ef9c6f8c42711d6731f22a7a09a403e2`

```dockerfile
```

-	Layers:
	-	`sha256:269f436802e16ea4752520f4167f3155a32aa18e7122dd3e7c467887aafcf45d`  
		Last Modified: Tue, 19 May 2026 23:38:00 GMT  
		Size: 5.1 MB (5119974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:419e40efdf547b130bba04b37a4af6014c55405d1adb82147bdae533353eff3a`  
		Last Modified: Tue, 19 May 2026 23:38:00 GMT  
		Size: 52.7 KB (52679 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; arm variant v7

```console
$ docker pull postgres@sha256:4cad39ce702f3bb98933ddd6b730634ea71d80c675db146f337cb05afca653cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87800242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58ccc01eaccb78052cde86ebca63404874ad91983c567bdf9bf5e1efa1af0d70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:28:35 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 19 May 2026 23:28:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:28:51 GMT
ENV GOSU_VERSION=1.19
# Tue, 19 May 2026 23:28:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 19 May 2026 23:28:58 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 19 May 2026 23:28:58 GMT
ENV LANG=en_US.utf8
# Tue, 19 May 2026 23:29:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:29:02 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 19 May 2026 23:29:03 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:29:03 GMT
ENV PG_MAJOR=18
# Tue, 19 May 2026 23:29:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 19 May 2026 23:29:03 GMT
ENV PG_VERSION=18.4-1.pgdg13+1
# Tue, 19 May 2026 23:40:56 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 19 May 2026 23:40:56 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 19 May 2026 23:40:56 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 19 May 2026 23:40:56 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 19 May 2026 23:40:56 GMT
VOLUME [/var/lib/postgresql]
# Tue, 19 May 2026 23:40:56 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:40:56 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 19 May 2026 23:40:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 23:40:56 GMT
STOPSIGNAL SIGINT
# Tue, 19 May 2026 23:40:56 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 19 May 2026 23:40:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250c6891cd274a54c8097abdc246e0e88f27dab4aa0aab94141a1a4815a4a6fd`  
		Last Modified: Tue, 19 May 2026 23:41:08 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62650414d97c2ac9640731a029add3900c63ae6b1568d4e2561036c5f04d142c`  
		Last Modified: Tue, 19 May 2026 23:41:09 GMT  
		Size: 5.5 MB (5497158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000cd4795e854d5effe26f06443f62b3de7df6cba580c6c7e74a01c5b22aa891`  
		Last Modified: Tue, 19 May 2026 23:41:08 GMT  
		Size: 1.2 MB (1222422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7b7b246df481f57917497cbe364cf36100eab28f955853eb56da174b92b2af`  
		Last Modified: Tue, 19 May 2026 23:41:09 GMT  
		Size: 8.2 MB (8204131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199ae6c0df13f37229d0959c1755637bcd9f6630e26579116292f3836e508d9c`  
		Last Modified: Tue, 19 May 2026 23:41:09 GMT  
		Size: 1.2 MB (1172652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a3bd198fd34599ee7c4553f16fd1089841ba73d8ce3f1ba72d923808f77785`  
		Last Modified: Tue, 19 May 2026 23:41:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5624faca2af10789204e8977551d7b8cd8cbee6bb2ee1f9d78aaf22b6b2452`  
		Last Modified: Tue, 19 May 2026 23:41:10 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91cd7bbd95bac112a7431d7fc95d1cd2f862b56c32bf79fabd22ef57e413267c`  
		Last Modified: Tue, 19 May 2026 23:41:11 GMT  
		Size: 45.5 MB (45467870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:befb235d941f4becfdc0760219ebfd067afb1196472ceb54183933cdb6570d27`  
		Last Modified: Tue, 19 May 2026 23:41:11 GMT  
		Size: 19.3 KB (19341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d18ce49ccb77940eda1aa99b9b7e8a15ea23efcae657a6d223d685ac5e396a2`  
		Last Modified: Tue, 19 May 2026 23:41:11 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b640aec9781e6f43d63122ce564dc118e2e207c9a8e2bae150933c1bb81d30cf`  
		Last Modified: Tue, 19 May 2026 23:41:11 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c3462d03e33843a00f3b86037ad96b06d82a637ab98910b4b2d8efa036d853`  
		Last Modified: Tue, 19 May 2026 23:41:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:67360d37240827c96f97b4364a3d5fb47716ab71a297c9754bdd3f59406c6abb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5171958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ffe0866c8ded7a50ce483efe3929fde4008808b84de413ac3202d32dcbf266c`

```dockerfile
```

-	Layers:
	-	`sha256:68157ff396ea11c9489cc6f8847fb810c23c9dcdfc69290332564ae0dbf5ce43`  
		Last Modified: Tue, 19 May 2026 23:41:09 GMT  
		Size: 5.1 MB (5119279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc8a8844ca8c849095e85c250eea019e1e6fb420dee184eafb345bda06783269`  
		Last Modified: Tue, 19 May 2026 23:41:08 GMT  
		Size: 52.7 KB (52679 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:f6902dfddea256a7bf788aefabbf10e5305ea348693caa4c741795559044001a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160955411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd55af5fa3946c2639af63958ae0b317b150ab0c90d379bd718d3b3349f6ba10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:17:24 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 19 May 2026 23:17:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:17:37 GMT
ENV GOSU_VERSION=1.19
# Tue, 19 May 2026 23:17:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 19 May 2026 23:17:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 19 May 2026 23:17:43 GMT
ENV LANG=en_US.utf8
# Tue, 19 May 2026 23:17:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:17:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 19 May 2026 23:17:47 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:17:47 GMT
ENV PG_MAJOR=18
# Tue, 19 May 2026 23:17:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 19 May 2026 23:17:47 GMT
ENV PG_VERSION=18.4-1.pgdg13+1
# Tue, 19 May 2026 23:18:04 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 19 May 2026 23:18:04 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 19 May 2026 23:18:04 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 19 May 2026 23:18:04 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 19 May 2026 23:18:04 GMT
VOLUME [/var/lib/postgresql]
# Tue, 19 May 2026 23:18:04 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:18:05 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 19 May 2026 23:18:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 23:18:05 GMT
STOPSIGNAL SIGINT
# Tue, 19 May 2026 23:18:05 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 19 May 2026 23:18:05 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d42e6947396dc3a3e053f0552cd7db9128a3231575b63bb445ba801fd6196b`  
		Last Modified: Tue, 19 May 2026 23:18:24 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f64b82520a75d2e24fa41d59cc70c46e67e04026f856416e5b2d4a2c199716`  
		Last Modified: Tue, 19 May 2026 23:18:24 GMT  
		Size: 6.2 MB (6235505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e86f6b8bd4b14dd6a0dcd150061520ed43e2d2ffc7d0906b8db65e1845589a3`  
		Last Modified: Tue, 19 May 2026 23:18:24 GMT  
		Size: 1.2 MB (1209591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6014830c5e6d97e276d1e4ece3ba5c03baad3d5ffdf2858f87774394cb0c1742`  
		Last Modified: Tue, 19 May 2026 23:18:24 GMT  
		Size: 8.2 MB (8204034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55963178907b22586d2a83e6e6c743ca4b97e10f3467d8169889e2ca758def5a`  
		Last Modified: Tue, 19 May 2026 23:18:25 GMT  
		Size: 1.2 MB (1220567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0d9985687d3d304f160e39b80ddfe97f928dc8a692633c17a6e8027bd07783`  
		Last Modified: Tue, 19 May 2026 23:18:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce720ec930b7116adc09d5398b7d8e9cf7211e540ee9360d00955a4007d3ffd`  
		Last Modified: Tue, 19 May 2026 23:18:26 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a19057306bee1b752b1f78c420d4990983764f286f385b476507f3976b2b83`  
		Last Modified: Tue, 19 May 2026 23:18:28 GMT  
		Size: 113.9 MB (113913632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8668cf528ee0ce1a46243e87789db90620a37781fb0042077482a51b991d5f5`  
		Last Modified: Tue, 19 May 2026 23:18:27 GMT  
		Size: 19.3 KB (19327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fde3e4485e3d4ca4f09219f5ef014b9e7e5907d4ff13227c2653d93c6dd2b20`  
		Last Modified: Tue, 19 May 2026 23:18:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30f8e8e47ac902ee5852f61905f75290d6e62bc2b832e8a1cec3e03fe511b7f`  
		Last Modified: Tue, 19 May 2026 23:18:27 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b859742db43296a73c99bae2e10c6eafeed533a27a11ba1ad3df6f877379e5ad`  
		Last Modified: Tue, 19 May 2026 23:18:28 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:8c2615fed099f417be871b7e11c2aa01729865f7b78c3459d45af42a94127d79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6015932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac48a4d8fc6bc311803335f9546018f3866ca4462c6e7b87b31ec506385ba470`

```dockerfile
```

-	Layers:
	-	`sha256:78ed726c460a0ff606d6f828ea5d69e6a2fb9c5b12486803524f1669d6065dc4`  
		Last Modified: Tue, 19 May 2026 23:18:24 GMT  
		Size: 6.0 MB (5963196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3da9a3e23e53f9fc02f0ee78be0836d047b62b5d1d92796a3d159c000e42333`  
		Last Modified: Tue, 19 May 2026 23:18:24 GMT  
		Size: 52.7 KB (52736 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; 386

```console
$ docker pull postgres@sha256:6491a703d8705e7547aa0b170f2e6ccae7abc2622603a96ea61ddfea1a7b4248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.6 MB (97616711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0050dc6aab9f0dc1db669ffb0a529d8684e64540d53883144bbdbdbf7980069`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:11:02 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 19 May 2026 23:11:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:11:17 GMT
ENV GOSU_VERSION=1.19
# Tue, 19 May 2026 23:11:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 19 May 2026 23:11:22 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 19 May 2026 23:11:22 GMT
ENV LANG=en_US.utf8
# Tue, 19 May 2026 23:11:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:11:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 19 May 2026 23:11:27 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:11:27 GMT
ENV PG_MAJOR=18
# Tue, 19 May 2026 23:11:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 19 May 2026 23:11:27 GMT
ENV PG_VERSION=18.4-1.pgdg13+1
# Tue, 19 May 2026 23:20:17 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 19 May 2026 23:20:18 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 19 May 2026 23:20:18 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 19 May 2026 23:20:18 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 19 May 2026 23:20:18 GMT
VOLUME [/var/lib/postgresql]
# Tue, 19 May 2026 23:20:18 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:20:18 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 19 May 2026 23:20:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 23:20:18 GMT
STOPSIGNAL SIGINT
# Tue, 19 May 2026 23:20:18 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 19 May 2026 23:20:18 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:05ced853378773a7168a29bae2e2f29a846f0a56beb260fd47a509a5e4ac966a`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 31.3 MB (31295335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31d23a9a666492437f7e320506acb0eaa6a25a56e1bfca252f4e5ae15de6136`  
		Last Modified: Tue, 19 May 2026 23:20:31 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbd10c075ba57c46a36b5bbbfbaccc546bfc3ede955a1505a53378ea7429e70`  
		Last Modified: Tue, 19 May 2026 23:20:31 GMT  
		Size: 6.6 MB (6631419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74be5be402fba126a4c7fa02b5047e65e06fa9ba686e6f078b587089b235c489`  
		Last Modified: Tue, 19 May 2026 23:20:31 GMT  
		Size: 1.2 MB (1225840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51eaec0397ec4deadaa7cc078849c0284f980319973d9d37a077121c333a32e3`  
		Last Modified: Tue, 19 May 2026 23:20:31 GMT  
		Size: 8.2 MB (8204078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad998cb18d95b6d34a87afd86bf30aaf307a27299d0c26d143869436e58cd37e`  
		Last Modified: Tue, 19 May 2026 23:20:32 GMT  
		Size: 1.3 MB (1308282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09cf6e1422f6462600a607a40ce0b399b9ac11daee673c254b9df3e29892d4d`  
		Last Modified: Tue, 19 May 2026 23:20:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd73de82e58e6dd1c5e25bdd99c358cbc4d2cbdba06c664004847a66bc6bcc6`  
		Last Modified: Tue, 19 May 2026 23:20:32 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49609f5c83e5705f8eaa39f8046a9c9fb8064e1fd7d223be1e2a4c5c43a8abcc`  
		Last Modified: Tue, 19 May 2026 23:20:34 GMT  
		Size: 48.9 MB (48921593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618185101b90fe4bb30f99d8583d31fc183b2894c7d9477016a159e0e52aaee2`  
		Last Modified: Tue, 19 May 2026 23:20:33 GMT  
		Size: 19.3 KB (19324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c352e7d345fb9ed231a2a1d61349db0b1485a66793620911f585c0ae54d1d9`  
		Last Modified: Tue, 19 May 2026 23:20:33 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e910611b3ed97229fc1f022f3dd3e7fdc1ec22f699a0d2da8837f20d96493234`  
		Last Modified: Tue, 19 May 2026 23:20:34 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff22d1f138cdc5d1b95a2d8c146321bd1ba0d83f2f3f1dbcfc32827b5052aae`  
		Last Modified: Tue, 19 May 2026 23:20:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:66ca7a7fa4e015910f1f68db1ff64fefd6e23e96bf62fb0568359f7335cd6ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5167698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d791b5a7202e25e6773d7bb49c3d9189aad859f197448a2fa8ddf4091c2e7e6`

```dockerfile
```

-	Layers:
	-	`sha256:95da6d6f06dad583366b979784ffc91b446cff3e8143059398bf4ca12b2b0f0c`  
		Last Modified: Tue, 19 May 2026 23:20:31 GMT  
		Size: 5.1 MB (5115307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f85a6d5bbb4cde8ebf2ad92abda9a8ae6d13446f3702bd50e93aed1637c6a919`  
		Last Modified: Tue, 19 May 2026 23:20:31 GMT  
		Size: 52.4 KB (52391 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; ppc64le

```console
$ docker pull postgres@sha256:f11448819cfae9597bb40e77fa1385e62abd42f180989186d0a9cc49b7220d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174766008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e4e9f5d6e66551bf8092d2bc523dda107cc6bd06483f95a9a84d7e2e896c67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:52:18 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 20 May 2026 00:52:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:52:47 GMT
ENV GOSU_VERSION=1.19
# Wed, 20 May 2026 00:52:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 20 May 2026 00:52:57 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 20 May 2026 00:52:57 GMT
ENV LANG=en_US.utf8
# Wed, 20 May 2026 00:53:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:53:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 20 May 2026 00:53:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 20 May 2026 00:53:06 GMT
ENV PG_MAJOR=18
# Wed, 20 May 2026 00:53:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Wed, 20 May 2026 00:53:06 GMT
ENV PG_VERSION=18.4-1.pgdg13+1
# Wed, 20 May 2026 00:53:50 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 20 May 2026 00:53:51 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 20 May 2026 00:53:51 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 20 May 2026 00:53:51 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 20 May 2026 00:53:51 GMT
VOLUME [/var/lib/postgresql]
# Wed, 20 May 2026 00:53:51 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 20 May 2026 00:53:51 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 20 May 2026 00:53:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 00:53:51 GMT
STOPSIGNAL SIGINT
# Wed, 20 May 2026 00:53:51 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 20 May 2026 00:53:51 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058b47d60c3c36623902dd53cdd673ce9b93583318e52744c4f1c8fcee2210d3`  
		Last Modified: Wed, 20 May 2026 00:54:39 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c6200d019c69189d0cef55392b9d5f243922994526471f68eb529e6cea6849`  
		Last Modified: Wed, 20 May 2026 00:54:40 GMT  
		Size: 7.1 MB (7076746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123e9dad4ecf44cd33cca69d25aa161600fedac0adfc03523b3b4dbfff65d670`  
		Last Modified: Wed, 20 May 2026 00:54:39 GMT  
		Size: 1.2 MB (1214730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62d4bbb20eaa83d2a85b1f102e15ff2cb6785ca81fdda9b6487c13403ea8879`  
		Last Modified: Wed, 20 May 2026 00:54:40 GMT  
		Size: 8.2 MB (8204050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cabd8a34059cfd4179cb9b138029133ff5ac88145fbf412d16f6df32a0ee94`  
		Last Modified: Wed, 20 May 2026 00:54:40 GMT  
		Size: 1.4 MB (1394900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addd7512ebbc0491a92f74f3bc573c6005f782856ff8fc3c078b46196125f6b8`  
		Last Modified: Wed, 20 May 2026 00:54:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecb1e0239a2c6cca5794b42475503acd64e3dc81fc4796fc6d94c839b3f5d73`  
		Last Modified: Wed, 20 May 2026 00:54:41 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8526576c6c487dc802e21b5a153cdb20a75c4d655b2a757d59944d58499b8065`  
		Last Modified: Wed, 20 May 2026 00:54:45 GMT  
		Size: 123.2 MB (123244955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c24884d0d046dca3dd1b37c5833717fe3ea36b4026b51d83359d847facfeca4`  
		Last Modified: Wed, 20 May 2026 00:54:42 GMT  
		Size: 19.3 KB (19332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d12f4692fe8e7a3de39e06149046e1757c806eca88832cc4151c1b6f630bd5d`  
		Last Modified: Wed, 20 May 2026 00:54:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40cbff527dbc0503d0e2d8b6b17f9afb85c789d8a13516b4d8e7442232928e4`  
		Last Modified: Wed, 20 May 2026 00:54:42 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:badda34b8818679b2ea8295c82bb5209960919962643b553bb34d535c694d139`  
		Last Modified: Wed, 20 May 2026 00:54:43 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:3de6a211b956d7c7f245cf0b30e0e071e00a67a5761aa401e075c775ae30a3a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6016013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ab15bf426269ed215a86b29557b836245dd517674a7d0c36a885e4548a32211`

```dockerfile
```

-	Layers:
	-	`sha256:84859dc96ca65a2ab678abe1025f613d94990617360225c4e278c7895f988985`  
		Last Modified: Wed, 20 May 2026 00:54:40 GMT  
		Size: 6.0 MB (5963479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9887ae55c7675eb28c93d4e7e3edb534809a5e4a9a2d8910321d6e0499d46fb`  
		Last Modified: Wed, 20 May 2026 00:54:39 GMT  
		Size: 52.5 KB (52534 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; riscv64

```console
$ docker pull postgres@sha256:c7824c664a3d1e07ce3968815412419d378f51b6ab4d3d3b3b8ef1eb6f617c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.9 MB (92900391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12783d717e9aa359b291da0b2c51a71eb74a7623b543457fc837dcd7b886b70e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Sun, 10 May 2026 12:21:48 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sun, 10 May 2026 12:22:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 10 May 2026 12:23:42 GMT
ENV GOSU_VERSION=1.19
# Sun, 10 May 2026 12:23:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 10 May 2026 12:24:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Sun, 10 May 2026 12:24:43 GMT
ENV LANG=en_US.utf8
# Sun, 10 May 2026 12:25:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 10 May 2026 12:25:25 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 May 2026 12:25:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Sun, 10 May 2026 12:25:26 GMT
ENV PG_MAJOR=18
# Sun, 10 May 2026 12:25:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Sun, 10 May 2026 12:25:26 GMT
ENV PG_VERSION=18.4-1.pgdg13+1
# Sat, 16 May 2026 00:23:58 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Sat, 16 May 2026 00:23:58 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 16 May 2026 00:23:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 16 May 2026 00:23:59 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Sat, 16 May 2026 00:23:59 GMT
VOLUME [/var/lib/postgresql]
# Sat, 16 May 2026 00:23:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 16 May 2026 00:23:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 16 May 2026 00:23:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2026 00:23:59 GMT
STOPSIGNAL SIGINT
# Sat, 16 May 2026 00:23:59 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 16 May 2026 00:23:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988dc2de045f11813ef1359f5abe174ba62914438fb92d75cab7c65a9647aed2`  
		Last Modified: Sun, 10 May 2026 14:30:04 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88bf149e5f1637f24cdc4c472d6e4ca943279612e0d39c8e267125e4ebbe141c`  
		Last Modified: Sun, 10 May 2026 14:30:06 GMT  
		Size: 6.3 MB (6293378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22405ed7ddeb3ddb041a0d46f2314cf33a0b76a8a467e9c2d55a2a69b23735f5`  
		Last Modified: Sun, 10 May 2026 14:30:04 GMT  
		Size: 1.2 MB (1202046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f1d93a3e38e95a376c71494a9b760c3874601da3ad347a9397e5584a2fdba3b`  
		Last Modified: Sun, 10 May 2026 14:30:08 GMT  
		Size: 8.2 MB (8203592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b5d68446e4a2a25f4140c2073abfa1f378e16bf8336f3f58606a91b20d9af9`  
		Last Modified: Sun, 10 May 2026 14:30:06 GMT  
		Size: 1.4 MB (1402374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b4166483991e8893bbf63a352298792c54bd94c781e40f75ac232b27f4550f`  
		Last Modified: Sun, 10 May 2026 14:30:06 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4ab377a5216f4b915710db64b9dca4fa85382b9e3963c6a789da9f27fd014d`  
		Last Modified: Sun, 10 May 2026 14:30:07 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f040252e6a224f7cab81ef06238130f38eee61197b2c9a5eed03c085b682999e`  
		Last Modified: Sat, 16 May 2026 00:26:33 GMT  
		Size: 47.5 MB (47488588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f86ee632d0d41d34afee970545d3766a00f08bcf6e95baec45e5d5d09aa47b4`  
		Last Modified: Sat, 16 May 2026 00:26:26 GMT  
		Size: 19.3 KB (19339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d331b8333df1ccd4d5fa72d1ed076438d7bb66a327581c5ec923725056ef6b3`  
		Last Modified: Sat, 16 May 2026 00:26:26 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830f560b8f2088e791754bcdee469d3720fa68b8320b7f7202572b101076ddd1`  
		Last Modified: Sat, 16 May 2026 00:26:26 GMT  
		Size: 6.1 KB (6100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939309e14bd28d1484557775de1f5e4837f114fc22edb65c4c6e7a7e5c920dd6`  
		Last Modified: Sat, 16 May 2026 00:26:27 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:65898cb1e17e92e7c0a3af5a47e304a2f4f3f917fe637557d3d4c6c9bd829ceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5162734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4b232ab5414f9ef51bf83eca1060fa99894aa6521d39fd4b33b1d1e04a235ef`

```dockerfile
```

-	Layers:
	-	`sha256:f77e2c6a0e3c56b805b14b250f3d2755d40ae3f1bbb4a7dd9e00f5998d335b30`  
		Last Modified: Sat, 16 May 2026 00:26:27 GMT  
		Size: 5.1 MB (5110205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ac1ca749a440820fcf733d81ca82a3ef4fea57ed55e38ed9f151fb336e9fa4b`  
		Last Modified: Sat, 16 May 2026 00:26:25 GMT  
		Size: 52.5 KB (52529 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; s390x

```console
$ docker pull postgres@sha256:3b1499947d6749b3148bae0fe398bbd4bcc2373359f2714f5a7e7c2645ff7bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (176988711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49d3a437715f1d1818d6ae09b12292e3a952d286c7d0cf3df4768ca1d01d98b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:40:13 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 19 May 2026 23:40:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:40:27 GMT
ENV GOSU_VERSION=1.19
# Tue, 19 May 2026 23:40:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 19 May 2026 23:40:33 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 19 May 2026 23:40:33 GMT
ENV LANG=en_US.utf8
# Tue, 19 May 2026 23:40:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:40:38 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 19 May 2026 23:40:39 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:40:39 GMT
ENV PG_MAJOR=18
# Tue, 19 May 2026 23:40:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 19 May 2026 23:40:39 GMT
ENV PG_VERSION=18.4-1.pgdg13+1
# Tue, 19 May 2026 23:54:11 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 19 May 2026 23:54:11 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 19 May 2026 23:54:11 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 19 May 2026 23:54:11 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 19 May 2026 23:54:11 GMT
VOLUME [/var/lib/postgresql]
# Tue, 19 May 2026 23:54:11 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:54:11 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 19 May 2026 23:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 23:54:11 GMT
STOPSIGNAL SIGINT
# Tue, 19 May 2026 23:54:11 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 19 May 2026 23:54:11 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8310d78eca048636ac7fe6d8860e3e5dc349db7fc09332003a920e1532da3f4`  
		Last Modified: Tue, 19 May 2026 23:54:41 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f629815d552e7eaa5fda05e618e4b7f10de15eae1fdbdd3f3eed9ca5149cf39a`  
		Last Modified: Tue, 19 May 2026 23:54:42 GMT  
		Size: 6.4 MB (6408661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d27157d070fd03d36ad92d6ffb07741d157a85a35f81dec35befbf39b40c285`  
		Last Modified: Tue, 19 May 2026 23:54:41 GMT  
		Size: 1.2 MB (1230215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1b2304936713177dfd9a7e108109a09dc240314fae72da2316d2fa7f3a93f9`  
		Last Modified: Tue, 19 May 2026 23:54:42 GMT  
		Size: 8.3 MB (8258967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c273d1e48bf4bc998249745dc3a2cfbfd3274c35e1d8bab47f4ff4d26cbda734`  
		Last Modified: Tue, 19 May 2026 23:54:42 GMT  
		Size: 1.4 MB (1398212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efc7f7e48d8f5241f4b9613a196cc6b3d23ffab0ef68938f73e1ffd372d544a`  
		Last Modified: Tue, 19 May 2026 23:54:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac9ba8be49db68efb649772ea6a8d4b919fa9f0d55ed7ce2c5edc43cde8998f`  
		Last Modified: Tue, 19 May 2026 23:54:43 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4700cca167ffd3534c47225b93a8be9e3308d3c4bd479240ba46dba48a24f1`  
		Last Modified: Tue, 19 May 2026 23:54:45 GMT  
		Size: 129.8 MB (129816566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156f63538d346dede5b9cc3517f03505b1d15856c140fedfaabf82e7db0ce676`  
		Last Modified: Tue, 19 May 2026 23:54:43 GMT  
		Size: 19.3 KB (19328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2686e5bae200c51908e16218f5671cf5caf26e3c1eeb56c14955bcba8c70df86`  
		Last Modified: Tue, 19 May 2026 23:54:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616a843caf7fa7201e6038394a597fdf005934df3a406429ebb5db864de17825`  
		Last Modified: Tue, 19 May 2026 23:54:44 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5f0e91743910b82eaf28a133c6decd2b50159b2ffa073c98cce9c8e5d1f255`  
		Last Modified: Tue, 19 May 2026 23:54:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:2c5bfacc497cd849e5a6142e77ae62b07037519e87be45d8ba9301be745c4865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6025959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc00afa339b0c72819c43cbf14feb89ddac71b6366ef6c8a78bfd13b18a7ac85`

```dockerfile
```

-	Layers:
	-	`sha256:38233c73f6ca81cc6d99de6c4c538656fa78fa1fef425eb8694851c74301c260`  
		Last Modified: Tue, 19 May 2026 23:54:42 GMT  
		Size: 6.0 MB (5973501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4844ad63f5f2936bc89d10f149d714a8449a1a996ea04e0c25c0d671a3b886c3`  
		Last Modified: Tue, 19 May 2026 23:54:41 GMT  
		Size: 52.5 KB (52458 bytes)  
		MIME: application/vnd.in-toto+json
