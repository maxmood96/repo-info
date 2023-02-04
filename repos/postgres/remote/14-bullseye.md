## `postgres:14-bullseye`

```console
$ docker pull postgres@sha256:9b2fa49092604854a942d104013e155ba71ba5b54fd68ae61eec750bd5f735bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `postgres:14-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:fdb107ea31ce66775b1ae23f645dc0f73d8016219ce5b818ed6b155ced75e888
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.0 MB (137966693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134818c929c8a7b6a13de269c437c1186b100cf50a89b6e1ca67a20129452b4f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 08:53:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 Jan 2023 08:53:21 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 01 Feb 2023 04:28:19 GMT
ENV GOSU_VERSION=1.16
# Wed, 01 Feb 2023 04:28:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 01 Feb 2023 04:28:34 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 01 Feb 2023 04:28:35 GMT
ENV LANG=en_US.utf8
# Wed, 01 Feb 2023 04:28:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 04:28:39 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 01 Feb 2023 04:28:40 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 01 Feb 2023 04:29:18 GMT
ENV PG_MAJOR=14
# Wed, 01 Feb 2023 04:29:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Wed, 01 Feb 2023 04:29:18 GMT
ENV PG_VERSION=14.6-1.pgdg110+1
# Wed, 01 Feb 2023 04:29:36 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 01 Feb 2023 04:29:37 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 01 Feb 2023 04:29:37 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 01 Feb 2023 04:29:38 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 01 Feb 2023 04:29:38 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 01 Feb 2023 04:29:38 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 01 Feb 2023 04:29:38 GMT
COPY file:d4c2ceee202d1390df115217c6e567abc1da7a31572f20a840d966332148ebe4 in /usr/local/bin/ 
# Wed, 01 Feb 2023 04:29:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Feb 2023 04:29:39 GMT
STOPSIGNAL SIGINT
# Wed, 01 Feb 2023 04:29:39 GMT
EXPOSE 5432
# Wed, 01 Feb 2023 04:29:39 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8dbd2beab503e312b0f0341b437039f4090f835dae29451e65bf79d8c7bd38f`  
		Last Modified: Wed, 11 Jan 2023 08:56:49 GMT  
		Size: 4.4 MB (4414922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d9dc9d0fbd73c8984f36476ef54033071d59aa7b734ca940eb016b21c1d197`  
		Last Modified: Wed, 11 Jan 2023 08:56:47 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f8df119080ef4f020014420407bb099cff39efacfb185b4ff31ab4c263911d`  
		Last Modified: Wed, 01 Feb 2023 04:31:46 GMT  
		Size: 1.5 MB (1471387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4adc97fdfa40059d7627a9f0da949f7b4f46b4ee6faf14f662caf4a39d58e28f`  
		Last Modified: Wed, 01 Feb 2023 04:31:46 GMT  
		Size: 8.0 MB (8045262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b101c784ba96bab7e670ef80f5069caf1ba085c6e3c0e622ea2cf318403787bf`  
		Last Modified: Wed, 01 Feb 2023 04:31:44 GMT  
		Size: 1.3 MB (1261177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:776d6095adf6688022cb269a6ab70b40adc84e75f3bd67b48be03d12e8dee048`  
		Last Modified: Wed, 01 Feb 2023 04:31:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe093395f4abd627585e4a75fd2c335fac652d6e85aa51be3e7842e5e6b5526`  
		Last Modified: Wed, 01 Feb 2023 04:31:44 GMT  
		Size: 3.2 KB (3198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706bb750549b65fb6c1b1991a45f221a9143a87385623223c7ac97550fb03062`  
		Last Modified: Wed, 01 Feb 2023 04:32:29 GMT  
		Size: 91.4 MB (91357185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a988004619f9774aaca3371173ba8c2d5e6d0e7c1b26f6fc281774b44c8e1f54`  
		Last Modified: Wed, 01 Feb 2023 04:32:16 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b2f345e9534930e19193bc830a432cb5397ca3bda255ce95585ae79944d789`  
		Last Modified: Wed, 01 Feb 2023 04:32:16 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b24f7c5c8b1c696176190ae18d8eac0d772f21bfd1753440230ed48d6f61695`  
		Last Modified: Wed, 01 Feb 2023 04:32:16 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0cce3e4db2416db8984b6d8c9de35ad43ae65501315da65993a61ae9e5812a`  
		Last Modified: Wed, 01 Feb 2023 04:32:16 GMT  
		Size: 4.8 KB (4780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:14-bullseye` - linux; arm variant v5

```console
$ docker pull postgres@sha256:36813adfe9d7f5cbca4c1ed2db81537e65518e384fb9f84ccf66e62e0fe3588b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.2 MB (131230970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfefad8773466bc1438a7c214a1a7543f2340d1a79ea02ac7fffc2b4eaa9ead7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 04 Feb 2023 02:46:38 GMT
ADD file:ce468627e54d8d1c839cea8ab62e505f612298fd97d50e189293fcfcc6af03a5 in / 
# Sat, 04 Feb 2023 02:46:38 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 10:06:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 04 Feb 2023 10:06:41 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Sat, 04 Feb 2023 10:06:41 GMT
ENV GOSU_VERSION=1.16
# Sat, 04 Feb 2023 10:06:53 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 04 Feb 2023 10:07:01 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Sat, 04 Feb 2023 10:07:01 GMT
ENV LANG=en_US.utf8
# Sat, 04 Feb 2023 10:07:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 10:07:08 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 04 Feb 2023 10:07:09 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Sat, 04 Feb 2023 10:23:51 GMT
ENV PG_MAJOR=14
# Sat, 04 Feb 2023 10:23:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Sat, 04 Feb 2023 10:23:52 GMT
ENV PG_VERSION=14.6-1.pgdg110+1
# Sat, 04 Feb 2023 10:39:55 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Sat, 04 Feb 2023 10:39:57 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Sat, 04 Feb 2023 10:39:58 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Sat, 04 Feb 2023 10:39:58 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sat, 04 Feb 2023 10:39:59 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Sat, 04 Feb 2023 10:39:59 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 04 Feb 2023 10:39:59 GMT
COPY file:d4c2ceee202d1390df115217c6e567abc1da7a31572f20a840d966332148ebe4 in /usr/local/bin/ 
# Sat, 04 Feb 2023 10:39:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 04 Feb 2023 10:40:00 GMT
STOPSIGNAL SIGINT
# Sat, 04 Feb 2023 10:40:00 GMT
EXPOSE 5432
# Sat, 04 Feb 2023 10:40:00 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:83735a64f458d40820e4310d632e8bb1dc888f6c25114496be3ce431b5f21d5d`  
		Last Modified: Sat, 04 Feb 2023 02:51:43 GMT  
		Size: 28.9 MB (28898637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff93d69700c7471875d2be886638201e09648dea040af9bd57bec560f2b80c2c`  
		Last Modified: Sat, 04 Feb 2023 11:26:28 GMT  
		Size: 4.1 MB (4096397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d70be376ca899a24d3934b02e7a1e8bb0e65748c7894053d73f417b530b1c9`  
		Last Modified: Sat, 04 Feb 2023 11:26:27 GMT  
		Size: 1.8 KB (1756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a101817cd9a69573a0ebac713f9eafe9ff390742a254663807b0b6ced3c8c065`  
		Last Modified: Sat, 04 Feb 2023 11:26:27 GMT  
		Size: 1.4 MB (1448626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7bb8f60356ab322fc6eeed6b15cf10a48520ea628af2873754c97c3aae9c81`  
		Last Modified: Sat, 04 Feb 2023 11:26:27 GMT  
		Size: 8.0 MB (8045148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b131161016b63febaef9c2489f6fd8f057f834feeec8801196487d7cf864444`  
		Last Modified: Sat, 04 Feb 2023 11:26:25 GMT  
		Size: 1.3 MB (1257285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46aff044b4b7c5ce594fd6aa9ffee134ddaba249a026cf5f149c7ba0c2563a48`  
		Last Modified: Sat, 04 Feb 2023 11:26:25 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d787e0cc60536190ef6a25fa725d88d11280b5737265ae793ebd2557bedc4200`  
		Last Modified: Sat, 04 Feb 2023 11:26:25 GMT  
		Size: 3.2 KB (3169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc33e5e57e67f275931c4d55f62188b89f62133c1010f00d987380adecba0e3`  
		Last Modified: Sat, 04 Feb 2023 11:27:21 GMT  
		Size: 87.5 MB (87465214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652e88fff279309efa9944a90d8fb8a50236485087a37a8662bb4ceb96c0bf75`  
		Last Modified: Sat, 04 Feb 2023 11:27:05 GMT  
		Size: 9.5 KB (9543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678ffbd7934114860a217ab13741ad7e7dc9d2f1aed8c54b8bf5e2ed1c4724ed`  
		Last Modified: Sat, 04 Feb 2023 11:27:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34df6d27f9b1d64d393a1d5c37b318dfc374f2c2055e60205be3a215fec0d3a2`  
		Last Modified: Sat, 04 Feb 2023 11:27:05 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b7dd2ccb4d7af9df4d43932d9448f644150591fbb5cfd06d6755a8aebacc83`  
		Last Modified: Sat, 04 Feb 2023 11:27:05 GMT  
		Size: 4.8 KB (4779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:14-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:fb5229b3642011a22ae182d7ccd7ae93a1ba248e685e882049f4cce28d8d667e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125887806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8777d388c2e676e6423406e47c30176c47e1d2e9f5d0812fa16f7aa4b3531b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 11 Jan 2023 04:00:36 GMT
ADD file:3fb94bfd628f3ebd91db74501bd297a817977cc066664f0fa342442b3352e0be in / 
# Wed, 11 Jan 2023 04:00:37 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 19:36:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 Jan 2023 19:36:07 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 31 Jan 2023 22:07:08 GMT
ENV GOSU_VERSION=1.16
# Tue, 31 Jan 2023 22:07:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 31 Jan 2023 22:07:24 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 31 Jan 2023 22:07:25 GMT
ENV LANG=en_US.utf8
# Tue, 31 Jan 2023 22:07:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 22:07:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 31 Jan 2023 22:07:31 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 31 Jan 2023 22:22:00 GMT
ENV PG_MAJOR=14
# Tue, 31 Jan 2023 22:22:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 31 Jan 2023 22:22:00 GMT
ENV PG_VERSION=14.6-1.pgdg110+1
# Tue, 31 Jan 2023 22:35:47 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 31 Jan 2023 22:35:48 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 31 Jan 2023 22:35:49 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 31 Jan 2023 22:35:49 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 31 Jan 2023 22:35:49 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 31 Jan 2023 22:35:50 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 31 Jan 2023 22:35:50 GMT
COPY file:d4c2ceee202d1390df115217c6e567abc1da7a31572f20a840d966332148ebe4 in /usr/local/bin/ 
# Tue, 31 Jan 2023 22:35:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Jan 2023 22:35:50 GMT
STOPSIGNAL SIGINT
# Tue, 31 Jan 2023 22:35:50 GMT
EXPOSE 5432
# Tue, 31 Jan 2023 22:35:50 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:330ad28688ae3fa5f3b241fef3efd076299bec9874e0597b1c16dcf8a165a53d`  
		Last Modified: Wed, 11 Jan 2023 04:07:49 GMT  
		Size: 26.6 MB (26559488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:085be26168de547bec03f87ac64282ad6a584c8812133cd1c3458abf965dc34c`  
		Last Modified: Wed, 11 Jan 2023 20:48:20 GMT  
		Size: 3.7 MB (3717155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189056b2ca03557033060e94fbc300fcb122039a7559c2526181f9779629b1e4`  
		Last Modified: Wed, 11 Jan 2023 20:48:19 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afb61aa4c12f63f6a713595a492dde6dff1273f7679ef053b0b8af701767bf2`  
		Last Modified: Tue, 31 Jan 2023 23:17:16 GMT  
		Size: 1.4 MB (1438672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b35a302b189e9a3db93a78aebda6b7417d25f32a35a7fd1b024fa5255dad4d8`  
		Last Modified: Tue, 31 Jan 2023 23:17:17 GMT  
		Size: 8.0 MB (8045155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55871759cd35032696826a1d6449ce8b22ca0874858c5997def44fb6cc7f0912`  
		Last Modified: Tue, 31 Jan 2023 23:17:14 GMT  
		Size: 1.1 MB (1131196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4264c4bc576aa41537ac2282814a530e33178e5ce19c4666286095652b27fa`  
		Last Modified: Tue, 31 Jan 2023 23:17:14 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df32530e9d5a10e1ccdfddb9987040c083900ad67fc09fa664a410d97d72094`  
		Last Modified: Tue, 31 Jan 2023 23:17:15 GMT  
		Size: 3.2 KB (3171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac47466a1eb384f8e9f85456e604e5b62ac638342bbcf1de72df74c29635ff7e`  
		Last Modified: Tue, 31 Jan 2023 23:18:13 GMT  
		Size: 85.0 MB (84976464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba74928d4e2196d1bbfd6aa1636657ab975e0a34bf91d473369c2d10f2c0b6e`  
		Last Modified: Tue, 31 Jan 2023 23:17:58 GMT  
		Size: 9.5 KB (9545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85bc54d22f97fdc6226e0995e0600bd30c465c3d94023a070b03375846c688b1`  
		Last Modified: Tue, 31 Jan 2023 23:17:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412b280f4cc4b7c4ee4570738d4f42f6967a579aa3494dc6784e93773d5c0cac`  
		Last Modified: Tue, 31 Jan 2023 23:17:58 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce443b6c868858cfe6c46527c581d3082e68b0e4cb7b512f7a4e824f6611bc5`  
		Last Modified: Tue, 31 Jan 2023 23:17:58 GMT  
		Size: 4.8 KB (4783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:14-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:edca999f54c5666c9cecda32e36e16f16321a6dcb67da7c8833e7582deab1ca9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133058577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8965da136fb8c9feb9ec2031ea434a656f8fae2afb10a4a377c9541539944578`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:37 GMT
ADD file:f613775c59ebd3ca219dc6bbad83115eb74bbbc1980ca4b63e7cb8ab3fa364e4 in / 
# Sat, 04 Feb 2023 06:17:37 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 13:25:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 04 Feb 2023 13:25:17 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Sat, 04 Feb 2023 13:25:17 GMT
ENV GOSU_VERSION=1.16
# Sat, 04 Feb 2023 13:25:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 04 Feb 2023 13:25:32 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Sat, 04 Feb 2023 13:25:32 GMT
ENV LANG=en_US.utf8
# Sat, 04 Feb 2023 13:25:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 13:25:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 04 Feb 2023 13:25:37 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Sat, 04 Feb 2023 13:26:01 GMT
ENV PG_MAJOR=14
# Sat, 04 Feb 2023 13:26:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Sat, 04 Feb 2023 13:26:01 GMT
ENV PG_VERSION=14.6-1.pgdg110+1
# Sat, 04 Feb 2023 13:26:17 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Sat, 04 Feb 2023 13:26:19 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Sat, 04 Feb 2023 13:26:19 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Sat, 04 Feb 2023 13:26:19 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sat, 04 Feb 2023 13:26:20 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Sat, 04 Feb 2023 13:26:20 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 04 Feb 2023 13:26:20 GMT
COPY file:d4c2ceee202d1390df115217c6e567abc1da7a31572f20a840d966332148ebe4 in /usr/local/bin/ 
# Sat, 04 Feb 2023 13:26:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 04 Feb 2023 13:26:20 GMT
STOPSIGNAL SIGINT
# Sat, 04 Feb 2023 13:26:20 GMT
EXPOSE 5432
# Sat, 04 Feb 2023 13:26:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f79f8cc5c20d534298dd6317333f38b7691da6d66e063ff10699727982c852be`  
		Last Modified: Sat, 04 Feb 2023 06:21:25 GMT  
		Size: 30.0 MB (30044792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:738e41444ccc1793c822694e11bfc3c2c4dff73e1776c524b0c394473fca0ee4`  
		Last Modified: Sat, 04 Feb 2023 13:28:24 GMT  
		Size: 4.4 MB (4416187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:714a7ea9e9fbbb1b54589616d058bdaddf008e97dab522f0e8a8b4bf85f4c466`  
		Last Modified: Sat, 04 Feb 2023 13:28:23 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:487612a90945fee63cb817b5b701744317b2bbb71de72f1455b73541c6ba9dcb`  
		Last Modified: Sat, 04 Feb 2023 13:28:23 GMT  
		Size: 1.4 MB (1403208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039cd64a8d6fc697c9499be365a437faac43b82ee3df2c7aca1ad2a7b6d608df`  
		Last Modified: Sat, 04 Feb 2023 13:28:22 GMT  
		Size: 8.0 MB (8045165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b00482c5d86ccea6a836605f9a1b7d43fd9ee06be0be3b13098e3ed62c5497`  
		Last Modified: Sat, 04 Feb 2023 13:28:21 GMT  
		Size: 1.2 MB (1249160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7413c2ab6643c2d5be9916b4830ee7ee9a839ec3b3ab62ef97d8a0f4b87d0eb8`  
		Last Modified: Sat, 04 Feb 2023 13:28:21 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209f1869e3afb49cd84436f8a8cfc67416ac6897750998bb73f1dbeaee48c443`  
		Last Modified: Sat, 04 Feb 2023 13:28:21 GMT  
		Size: 3.2 KB (3202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd13eeb7729db88ad7530b37ae5445f19152f3e44f1e6f96176ce2d17ca5b98`  
		Last Modified: Sat, 04 Feb 2023 13:29:00 GMT  
		Size: 87.9 MB (87880269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604fff3c78af362d0c74a8287f84c1527efffa4143bb139b76dc6f0f85ae0413`  
		Last Modified: Sat, 04 Feb 2023 13:28:51 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7292c35063d90109ed7857cb125e07e20ffe13daa7e74cac83ea87dfd80e5579`  
		Last Modified: Sat, 04 Feb 2023 13:28:51 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5448d48757b249116f4ab6620fb4727771ba980fe00a627d1084e0b014d059`  
		Last Modified: Sat, 04 Feb 2023 13:28:51 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d5b08e561735a2db8fb2a6f90bc1c418e1e2e5066795b7b6a4727ff73e33c0f`  
		Last Modified: Sat, 04 Feb 2023 13:28:51 GMT  
		Size: 4.8 KB (4777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:14-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:98ca6024e77894f584ce3dceeed3d14831af0e65ebaacec439cdbee2287ebe5a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139586021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c980ec4ee124518d92feb24f75019ed7e75e6eb574c7d90fd973d76cbcd6980`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 04 Feb 2023 07:49:22 GMT
ADD file:82af884aad6a87f5b309a7418aa1df69f92180a39818ae6d77d37d072cb6fecb in / 
# Sat, 04 Feb 2023 07:49:22 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 15:50:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 04 Feb 2023 15:50:50 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Sat, 04 Feb 2023 15:50:51 GMT
ENV GOSU_VERSION=1.16
# Sat, 04 Feb 2023 15:51:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 04 Feb 2023 15:51:08 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Sat, 04 Feb 2023 15:51:09 GMT
ENV LANG=en_US.utf8
# Sat, 04 Feb 2023 15:51:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 15:51:15 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 04 Feb 2023 15:51:17 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Sat, 04 Feb 2023 16:05:19 GMT
ENV PG_MAJOR=14
# Sat, 04 Feb 2023 16:05:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Sat, 04 Feb 2023 16:05:21 GMT
ENV PG_VERSION=14.6-1.pgdg110+1
# Sat, 04 Feb 2023 16:18:31 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Sat, 04 Feb 2023 16:18:31 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Sat, 04 Feb 2023 16:18:32 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Sat, 04 Feb 2023 16:18:33 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sat, 04 Feb 2023 16:18:34 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Sat, 04 Feb 2023 16:18:35 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 04 Feb 2023 16:18:37 GMT
COPY file:d4c2ceee202d1390df115217c6e567abc1da7a31572f20a840d966332148ebe4 in /usr/local/bin/ 
# Sat, 04 Feb 2023 16:18:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 04 Feb 2023 16:18:38 GMT
STOPSIGNAL SIGINT
# Sat, 04 Feb 2023 16:18:39 GMT
EXPOSE 5432
# Sat, 04 Feb 2023 16:18:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:fb99e0a97d653ef9acb2bdac0d1d10a8655b789bd4e8924c4a1c4a2af8adbb4a`  
		Last Modified: Sat, 04 Feb 2023 07:55:04 GMT  
		Size: 32.4 MB (32375772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d5562e9108729c139eb383e4115735aba6ad598c8fa06979180d9026829d66`  
		Last Modified: Sat, 04 Feb 2023 16:58:45 GMT  
		Size: 4.6 MB (4607396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4adb8c7271ee68926c23f48a6b4e2da428541c992988b9033506a14667596d8`  
		Last Modified: Sat, 04 Feb 2023 16:58:43 GMT  
		Size: 1.6 KB (1639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1901d99798f1eca342d20c76078bc08e164ccbf96e931c132e5a5f3bd7d4de73`  
		Last Modified: Sat, 04 Feb 2023 16:58:43 GMT  
		Size: 1.4 MB (1446463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7edb0ae75f911791beadf04785124e449b0f26301a53be52fcaed1f71ad5d031`  
		Last Modified: Sat, 04 Feb 2023 16:58:43 GMT  
		Size: 8.0 MB (8043333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347120c75ac26a044d443c46e5a5aaa024c9bcb6ed5072a01f3de2ecce76de8e`  
		Last Modified: Sat, 04 Feb 2023 16:58:42 GMT  
		Size: 1.0 MB (1027959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f0a2c440e0252704000f30eea5a3997c6a692309d6c653c8a353941424a201`  
		Last Modified: Sat, 04 Feb 2023 16:58:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:467311549dffa7f2472aad4b7747ee89a72a99e2ff6af0dd918e098c6a16c44a`  
		Last Modified: Sat, 04 Feb 2023 16:58:41 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b091cccd6ad9129ceab69d203dada58f8200797cb92b0813174866371626ef`  
		Last Modified: Sat, 04 Feb 2023 16:59:33 GMT  
		Size: 92.1 MB (92065577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199cd75c7071c2074c6495a1b06f8c34a52e446324b6d4652940b9c6b3b25402`  
		Last Modified: Sat, 04 Feb 2023 16:59:21 GMT  
		Size: 9.5 KB (9535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319a17dc0a88677c51e523c445315be63621ec2e79b848f776fe2bbe8da2dafb`  
		Last Modified: Sat, 04 Feb 2023 16:59:21 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea501f6ac2c14aca9b3052166e69cbb717f9b1a7c57b72f1b9a6202a53ea4eb1`  
		Last Modified: Sat, 04 Feb 2023 16:59:21 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8977385e2ca513894ca7799939b22725ce68299fb03e9c9d9b3e9334280c5fd2`  
		Last Modified: Sat, 04 Feb 2023 16:59:21 GMT  
		Size: 4.8 KB (4786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:14-bullseye` - linux; mips64le

```console
$ docker pull postgres@sha256:641522ad1a8bb7db101ab5d88494fcdd164b6f19ea527c6b7695efcaf4e13d7b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132353941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:627ac5389bb9fec230b1ab601dc4f8f0ea4dd754cada049c6e5b236d98e4a53e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 04 Feb 2023 06:20:15 GMT
ADD file:03d6cf2d45a21e59975a1d17c6ca9fc83bb7a0da235873315c9c7940245beb1e in / 
# Sat, 04 Feb 2023 06:20:19 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 11:24:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 04 Feb 2023 11:24:34 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Sat, 04 Feb 2023 11:24:36 GMT
ENV GOSU_VERSION=1.16
# Sat, 04 Feb 2023 11:25:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 04 Feb 2023 11:25:38 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Sat, 04 Feb 2023 11:25:40 GMT
ENV LANG=en_US.utf8
# Sat, 04 Feb 2023 11:25:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 11:26:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 04 Feb 2023 11:26:09 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Sat, 04 Feb 2023 12:27:58 GMT
ENV PG_MAJOR=14
# Sat, 04 Feb 2023 12:28:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Sat, 04 Feb 2023 12:28:03 GMT
ENV PG_VERSION=14.6-1.pgdg110+1
# Sat, 04 Feb 2023 13:27:24 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Sat, 04 Feb 2023 13:27:31 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Sat, 04 Feb 2023 13:27:37 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Sat, 04 Feb 2023 13:27:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sat, 04 Feb 2023 13:27:46 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Sat, 04 Feb 2023 13:27:49 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 04 Feb 2023 13:27:52 GMT
COPY file:d4c2ceee202d1390df115217c6e567abc1da7a31572f20a840d966332148ebe4 in /usr/local/bin/ 
# Sat, 04 Feb 2023 13:27:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 04 Feb 2023 13:27:59 GMT
STOPSIGNAL SIGINT
# Sat, 04 Feb 2023 13:28:03 GMT
EXPOSE 5432
# Sat, 04 Feb 2023 13:28:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:aedd2a952aead0f89a308f23f44377263665bf76192d5542abd66473ea799d44`  
		Last Modified: Sat, 04 Feb 2023 06:28:25 GMT  
		Size: 29.6 MB (29619892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0563ff2a7376bd58df5a0d8093dbc2e3bffeae967406a030310572635689a0e5`  
		Last Modified: Sat, 04 Feb 2023 16:16:34 GMT  
		Size: 4.2 MB (4196257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce02eeaa75426698c696b6dabfed79f4275e8150b96fa3774a5962e72a3a1ca`  
		Last Modified: Sat, 04 Feb 2023 16:16:28 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bff052a7306d89ba1344b451f95617def7de3609c7e5425929a778dc725cf33`  
		Last Modified: Sat, 04 Feb 2023 16:16:30 GMT  
		Size: 1.4 MB (1358187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a12537cf5fa2e5906b6aa71aee12df4b287d64fcfbb184674a305f40a41806c`  
		Last Modified: Sat, 04 Feb 2023 16:16:34 GMT  
		Size: 8.0 MB (8043901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd02c90ca7e1eaaaa702370aa75417b717d85480622cb2ae394f75ef4ace0321`  
		Last Modified: Sat, 04 Feb 2023 16:16:27 GMT  
		Size: 1.1 MB (1089523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8225be314e3ccf262601382c1874bc44519601135c22fc7019e5dac929c35cb7`  
		Last Modified: Sat, 04 Feb 2023 16:16:26 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2546d28433ce76edeba75cdaae0529bf10b4feff8c6753916ed4543416898c19`  
		Last Modified: Sat, 04 Feb 2023 16:16:26 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864c8a7d6213862769345157596644e340a9e102d79ff42c78665326e92a1755`  
		Last Modified: Sat, 04 Feb 2023 16:18:43 GMT  
		Size: 88.0 MB (88026653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab3db6f6dd3c89b0d42fa72a7cbdcc88678f6d9f4338acb84403fd0b6d1f243`  
		Last Modified: Sat, 04 Feb 2023 16:17:46 GMT  
		Size: 9.5 KB (9541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c818e2bad18d0a66f5f537745bcccf705cfe092aade6b21383258aaee17b5a83`  
		Last Modified: Sat, 04 Feb 2023 16:17:46 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d951ea146bad0540e7a41c3da3b2f19e3a8abe1c042a1606c366d2e3384452`  
		Last Modified: Sat, 04 Feb 2023 16:17:46 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f0ef4c43a2f3e83cd44439cd7fc7c5a24c7748c2141664dc410de8ee78eeeb`  
		Last Modified: Sat, 04 Feb 2023 16:17:46 GMT  
		Size: 4.8 KB (4783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:14-bullseye` - linux; ppc64le

```console
$ docker pull postgres@sha256:1e1bbecd84d8dbdcc1bdc5db836a882015c6872d3e6e039e13b71efa102878ae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.0 MB (147045785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34a27d6242281719beaa19b29a77b64b90ed9a4527cf58b868fc71c164bcb92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 11 Jan 2023 03:49:30 GMT
ADD file:3c7553fb5eda606d574ff6c08bc2213f9e6a68910043fe3087e4c1a04b65a18e in / 
# Wed, 11 Jan 2023 03:49:32 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 06:49:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 Jan 2023 06:49:11 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 01 Feb 2023 01:47:03 GMT
ENV GOSU_VERSION=1.16
# Wed, 01 Feb 2023 01:47:18 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 01 Feb 2023 01:47:29 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 01 Feb 2023 01:47:30 GMT
ENV LANG=en_US.utf8
# Wed, 01 Feb 2023 01:47:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 01:47:39 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 01 Feb 2023 01:47:42 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 01 Feb 2023 01:48:47 GMT
ENV PG_MAJOR=14
# Wed, 01 Feb 2023 01:48:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Wed, 01 Feb 2023 01:48:48 GMT
ENV PG_VERSION=14.6-1.pgdg110+1
# Wed, 01 Feb 2023 01:49:22 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 01 Feb 2023 01:49:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 01 Feb 2023 01:49:27 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 01 Feb 2023 01:49:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 01 Feb 2023 01:49:29 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 01 Feb 2023 01:49:29 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 01 Feb 2023 01:49:30 GMT
COPY file:d4c2ceee202d1390df115217c6e567abc1da7a31572f20a840d966332148ebe4 in /usr/local/bin/ 
# Wed, 01 Feb 2023 01:49:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Feb 2023 01:49:31 GMT
STOPSIGNAL SIGINT
# Wed, 01 Feb 2023 01:49:31 GMT
EXPOSE 5432
# Wed, 01 Feb 2023 01:49:31 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bbf81328aca90b7ddb122fc175443f5323674a9e51bbb00d5b1d683ef0b858f4`  
		Last Modified: Wed, 11 Jan 2023 03:55:33 GMT  
		Size: 35.3 MB (35268773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334917a809fcfe9ca525536b58efc53e0a20fbf889658115088cc82766eda6e3`  
		Last Modified: Wed, 11 Jan 2023 06:56:54 GMT  
		Size: 5.2 MB (5222785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34d923f3c92f56c3b8869933bf845d477a56c32ef5b54694cff0e0e1465929c`  
		Last Modified: Wed, 11 Jan 2023 06:56:51 GMT  
		Size: 1.8 KB (1799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e15dd7f032c61eaeabe998468afdec64ba00ab89a0e26ef3c171d65a25dde29`  
		Last Modified: Wed, 01 Feb 2023 01:54:16 GMT  
		Size: 1.4 MB (1393211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02f7f8adf2e55041797234321816dff7af1750fc582d22cffff9fa749c40a40`  
		Last Modified: Wed, 01 Feb 2023 01:54:16 GMT  
		Size: 8.0 MB (8045217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7afc0143ed7eea99efc3f0d57ae9a242d20320894479699d4f919c89f5d8dde6`  
		Last Modified: Wed, 01 Feb 2023 01:54:14 GMT  
		Size: 1.4 MB (1420129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e2c069fa06a4fcb4ad3ddedf4cf2f67975bddde97842e36cafed9e90feae4b`  
		Last Modified: Wed, 01 Feb 2023 01:54:14 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30376ccd06a4b00f633689fb487662be96651172009becec1bb20dd31b7457ff`  
		Last Modified: Wed, 01 Feb 2023 01:54:14 GMT  
		Size: 3.2 KB (3202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2f8a33a862095fef8f13c5714196459f68db334652ea511761b14db8eae3bf`  
		Last Modified: Wed, 01 Feb 2023 01:55:29 GMT  
		Size: 95.7 MB (95675873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daddab568307989631c85f4d49e108326bd418d5aed930726019fa637857cc3b`  
		Last Modified: Wed, 01 Feb 2023 01:55:06 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:046969b55c8edca03b64b4a417c546475e2852da2dc8ab88d1243876b4d767db`  
		Last Modified: Wed, 01 Feb 2023 01:55:06 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5210576385aaec16a2e913fb4f2d459a160692a634ba70e37f613679b1b92b79`  
		Last Modified: Wed, 01 Feb 2023 01:55:06 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df06078ba257611299b2d7e502b07455b750d891263b96b3fa37239a0dae8437`  
		Last Modified: Wed, 01 Feb 2023 01:55:06 GMT  
		Size: 4.8 KB (4782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:14-bullseye` - linux; s390x

```console
$ docker pull postgres@sha256:4dca096432138db82103f659bc4160f3da18c8a59b9ecc3790f1e67f1c826b92
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.2 MB (85211019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f38f7d9606615f269ad9cf9df6a5ab5401fced65345febb965019735e5c12da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 04 Feb 2023 04:06:15 GMT
ADD file:29a3ecb38611dbbb6f45b2d10ad3cee60c0198429376f999e9a397f9c405820e in / 
# Sat, 04 Feb 2023 04:06:17 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 08:10:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 04 Feb 2023 08:10:02 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Sat, 04 Feb 2023 08:10:02 GMT
ENV GOSU_VERSION=1.16
# Sat, 04 Feb 2023 08:10:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 04 Feb 2023 08:10:13 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Sat, 04 Feb 2023 08:10:14 GMT
ENV LANG=en_US.utf8
# Sat, 04 Feb 2023 08:10:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 08:10:18 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 04 Feb 2023 08:10:19 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Sat, 04 Feb 2023 08:17:43 GMT
ENV PG_MAJOR=14
# Sat, 04 Feb 2023 08:17:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Sat, 04 Feb 2023 08:17:43 GMT
ENV PG_VERSION=14.6-1.pgdg110+1
# Sat, 04 Feb 2023 08:24:45 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Sat, 04 Feb 2023 08:24:48 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Sat, 04 Feb 2023 08:24:48 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Sat, 04 Feb 2023 08:24:48 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sat, 04 Feb 2023 08:24:49 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Sat, 04 Feb 2023 08:24:49 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 04 Feb 2023 08:24:49 GMT
COPY file:d4c2ceee202d1390df115217c6e567abc1da7a31572f20a840d966332148ebe4 in /usr/local/bin/ 
# Sat, 04 Feb 2023 08:24:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 04 Feb 2023 08:24:50 GMT
STOPSIGNAL SIGINT
# Sat, 04 Feb 2023 08:24:50 GMT
EXPOSE 5432
# Sat, 04 Feb 2023 08:24:50 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7c6fe4d1ef15da79055e0a71952e1a38f799d4f36e9acebdb1ec1512651b39f1`  
		Last Modified: Sat, 04 Feb 2023 04:10:27 GMT  
		Size: 29.6 MB (29629678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69b877532e531bf9e0aa813b26733ceda5700b726c5f1638b9f2ca7ca30e4bb`  
		Last Modified: Sat, 04 Feb 2023 08:46:53 GMT  
		Size: 4.3 MB (4302202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40fecc1968f3dc322909a5084bd524e8d8e105e6235f8814ed5e00d5703f6149`  
		Last Modified: Sat, 04 Feb 2023 08:46:52 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8382a5e3dbf07ed5cd4bdddf8bf0bf579bbf35a4fac9ff92342061f2e0a35283`  
		Last Modified: Sat, 04 Feb 2023 08:46:52 GMT  
		Size: 1.4 MB (1436943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8227d9564ea98d3753efc85d18e1b99bd5c00ddb23b4b46c19dcdf3e6cd6037`  
		Last Modified: Sat, 04 Feb 2023 08:46:53 GMT  
		Size: 8.1 MB (8099206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5b5e7506716d092b4417adc5b0a17b87479bf070c0c1c69e1e62f66fa3dfa8`  
		Last Modified: Sat, 04 Feb 2023 08:46:51 GMT  
		Size: 1.2 MB (1237918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47c658ca9f7ac63c7babed3a8bfab340b6aa6625cb4e3024ab95de5b95a6ba62`  
		Last Modified: Sat, 04 Feb 2023 08:46:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e7ec9cfc0af3de6249eb2afdaf48f8f12b93ff2975c3aa2820b7675f73f992`  
		Last Modified: Sat, 04 Feb 2023 08:46:51 GMT  
		Size: 3.2 KB (3194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f996f2b4acfe66cd7526eb51396ed6376cd19d7e19adfc4f13bf932e5e5b94c`  
		Last Modified: Sat, 04 Feb 2023 08:47:19 GMT  
		Size: 40.5 MB (40485278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8466e692592f005537a4aff5f0b0fa2a65de6a0aafbf86e0a394a77596c80cc6`  
		Last Modified: Sat, 04 Feb 2023 08:47:14 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a911273b12428e015228d07108cba9270acff59ff12a2bb01e12aaee77fb24dc`  
		Last Modified: Sat, 04 Feb 2023 08:47:14 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db89ea3dd243c75fc631ce3aebf75587a313ff74f42f9c75ed899faec5d33f8`  
		Last Modified: Sat, 04 Feb 2023 08:47:14 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e0721aba0256d6a905d76eaca53b2dd1d54550b83395f5fc551b8d6dd048f6`  
		Last Modified: Sat, 04 Feb 2023 08:47:14 GMT  
		Size: 4.8 KB (4782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
