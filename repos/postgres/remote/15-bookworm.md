## `postgres:15-bookworm`

```console
$ docker pull postgres@sha256:589b8defb116f348c9bc29677736e669c4c6ed3f0f16b0376c26b6e10e406b48
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

### `postgres:15-bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:66ac7c0445725cad65b7859de817d3befb53873d6a7504fc3bc8b0f1e55318d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.9 MB (152942587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf12e8645493f853a1ca16556c0f8d39968954ad6628b9d8d69c8167edb27f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:32:54 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 22 Apr 2026 01:32:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:33:03 GMT
ENV GOSU_VERSION=1.19
# Wed, 22 Apr 2026 01:33:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Apr 2026 01:33:07 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 22 Apr 2026 01:33:07 GMT
ENV LANG=en_US.utf8
# Wed, 22 Apr 2026 01:33:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:33:09 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 22 Apr 2026 01:33:10 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:33:10 GMT
ENV PG_MAJOR=15
# Wed, 22 Apr 2026 01:33:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Wed, 22 Apr 2026 01:33:10 GMT
ENV PG_VERSION=15.17-1.pgdg12+1
# Wed, 22 Apr 2026 01:33:21 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 22 Apr 2026 01:33:21 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 22 Apr 2026 01:33:21 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 22 Apr 2026 01:33:21 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 22 Apr 2026 01:33:21 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 22 Apr 2026 01:33:21 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 22 Apr 2026 01:33:21 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:33:21 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 22 Apr 2026 01:33:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:33:21 GMT
STOPSIGNAL SIGINT
# Wed, 22 Apr 2026 01:33:21 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 22 Apr 2026 01:33:21 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc06f3bec977b84358b6f444f1a857c28dcc92d4286ce00374bf1fdd70ed47a3`  
		Last Modified: Wed, 22 Apr 2026 01:33:39 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4687a900418500a49eeabfe767b31467aec363964082c2d4b4261690a763558f`  
		Last Modified: Wed, 22 Apr 2026 01:33:40 GMT  
		Size: 4.5 MB (4534209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2417a0e3ae5a1b8d5575249a41254a79ffbe8658df903437ff57a6a554d2cf96`  
		Last Modified: Wed, 22 Apr 2026 01:33:39 GMT  
		Size: 1.2 MB (1249492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce97f8b02c07dd9b37d0bb720ccb8fab64ec1495af2d85b175d00e5f7db9bb03`  
		Last Modified: Wed, 22 Apr 2026 01:33:40 GMT  
		Size: 8.1 MB (8066490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbc69f348d202055e1a072c1211c534e0376c6a2ca1c13bfa659474c61344ed`  
		Last Modified: Wed, 22 Apr 2026 01:33:40 GMT  
		Size: 1.2 MB (1196388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1cc88a000ae0883b72ba181d018bc3f379fbb0b72a47f4c232fb1b100ce993`  
		Last Modified: Wed, 22 Apr 2026 01:33:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e6420a078246b9419f5b34c9aafb6cf9db9d774532e671e9d32368752e6593`  
		Last Modified: Wed, 22 Apr 2026 01:33:41 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f65fb23abd2de54772cc3d6600d202b3096bee14fe816999b618795f8f1b40`  
		Last Modified: Wed, 22 Apr 2026 01:33:44 GMT  
		Size: 109.6 MB (109638977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e441687532480e34fdb9ae3a6ada4b218f13520fb910a64265c2245bea84f81c`  
		Last Modified: Wed, 22 Apr 2026 01:33:42 GMT  
		Size: 9.8 KB (9783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d522b22bb91bba3313bd16a66e48398f4ad97fbc2a56a7066fb9c78e768cca74`  
		Last Modified: Wed, 22 Apr 2026 01:33:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e42b200dde3be7cc7f936579a9e9e57da30420a2a9932674ba72d8bc58769c3`  
		Last Modified: Wed, 22 Apr 2026 01:33:42 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4666c7058d512812c3a72368f76e490a631c12ae3bef81e02bba22dde03ffde`  
		Last Modified: Wed, 22 Apr 2026 01:33:43 GMT  
		Size: 6.1 KB (6095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435c2066b94d58771787a4a2f3c35a2ed655e43133e5e690e13bf01371ed82d8`  
		Last Modified: Wed, 22 Apr 2026 01:33:43 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:582d8f66aa7aa529e8e9c228edc64c0c7444c36ad0f677b84b046d2deeac7d04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5896644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9c9c12ed41efdb99aa4258f760e0f597f5fcb99d50a96d00e1ba8eb98f02c6`

```dockerfile
```

-	Layers:
	-	`sha256:c09d673c52e658893009f22aa2ae8b531fc7589a4cda9e7cc33d2b5c4e318211`  
		Last Modified: Wed, 22 Apr 2026 01:33:40 GMT  
		Size: 5.8 MB (5843348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbef9550b9863323a387b513e4f5c3d1a0586a79e4c7108f9d71ea1e238e62a3`  
		Last Modified: Wed, 22 Apr 2026 01:33:39 GMT  
		Size: 53.3 KB (53296 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:d63a840b00c80ad2d73b2a43d029f59a1c310026276998d3e262c80d4802a792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.9 MB (145885084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31cc9632a2344de52f300a94f4138f43998a3e8f1f3b252a70b5d797c07c26c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:27:26 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 07 Apr 2026 02:27:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:42 GMT
ENV GOSU_VERSION=1.19
# Tue, 07 Apr 2026 02:27:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 07 Apr 2026 02:27:49 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 07 Apr 2026 02:27:49 GMT
ENV LANG=en_US.utf8
# Tue, 07 Apr 2026 02:27:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:27:54 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 07 Apr 2026 02:27:55 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:27:55 GMT
ENV PG_MAJOR=15
# Tue, 07 Apr 2026 02:27:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 07 Apr 2026 02:27:55 GMT
ENV PG_VERSION=15.17-1.pgdg12+1
# Tue, 07 Apr 2026 02:42:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 07 Apr 2026 02:42:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 07 Apr 2026 02:42:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 07 Apr 2026 02:42:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 07 Apr 2026 02:42:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 07 Apr 2026 02:42:07 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 07 Apr 2026 02:42:07 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 02:42:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 07 Apr 2026 02:42:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 02:42:07 GMT
STOPSIGNAL SIGINT
# Tue, 07 Apr 2026 02:42:07 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 07 Apr 2026 02:42:07 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4748d6bbb5a5b9e671dcabe2f909bdd7514f760a5cfdcd37d5b04627424120f2`  
		Last Modified: Tue, 07 Apr 2026 00:10:57 GMT  
		Size: 25.8 MB (25765667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f90f9e196c29915a64379837b22b08336be602712ab652ef44211409ae34a9`  
		Last Modified: Tue, 07 Apr 2026 02:42:25 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728f08d8920485e160c2a022965ac35e0ef23b6bd7749f84979c1037fddea41a`  
		Last Modified: Tue, 07 Apr 2026 02:42:25 GMT  
		Size: 4.2 MB (4151297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa82ba1a48ece38e68dd1d6810ce1c9fa2734b17ee1c38fe2a99b2692f0a2a36`  
		Last Modified: Tue, 07 Apr 2026 02:42:25 GMT  
		Size: 1.2 MB (1220086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1aef35d58bd3c5644919e74269a2d9cb4b059ae80d56e5bd1e4ff12d4e5cfb2`  
		Last Modified: Tue, 07 Apr 2026 02:42:25 GMT  
		Size: 8.1 MB (8066574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1443c7314f30eaaa740f801ecbd27cd6795a477bbfa60d59569af291cbd51736`  
		Last Modified: Tue, 07 Apr 2026 02:42:26 GMT  
		Size: 1.2 MB (1195064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0d0d457aa6bc3e031abd56e7537f70737b002f7bb00f439be42183d7ce6eba`  
		Last Modified: Tue, 07 Apr 2026 02:42:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e62472eea40e00a725fe693fad2615c384cb3826eb515afe6949f9e6fa204e`  
		Last Modified: Tue, 07 Apr 2026 02:42:26 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3861dd2fa6f238685a685a7a70a0258cb6657f6878b86cff0f9f9c13383561bb`  
		Last Modified: Tue, 07 Apr 2026 02:42:29 GMT  
		Size: 105.5 MB (105465859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3227a9335151c06be408280beeaf6e526ce9ea8cd8a27d1d1804e6c289aafbb`  
		Last Modified: Tue, 07 Apr 2026 02:42:28 GMT  
		Size: 9.8 KB (9790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743ce4a703a847cd9d2493a3c18dd5d894dd6160bfc185f6eba5f832976e04e9`  
		Last Modified: Tue, 07 Apr 2026 02:42:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec827b427c6627df1c6aef6572ec86db498accdd88100b1b8ad5244fc8e49726`  
		Last Modified: Tue, 07 Apr 2026 02:42:28 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56204b43d5836b1c8cb02d403d8a46e0bccba841d6d0f20b621442ff25782a95`  
		Last Modified: Tue, 07 Apr 2026 02:42:29 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f07ef21e5612cbaa9541f3a50e85ba49bcf83b2f7c18c7ae3b0c8c868ba8c22`  
		Last Modified: Tue, 07 Apr 2026 02:42:29 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:b11482fc5835c069ac1a32bd4505fffc77748955fb5eb0750cc5dd91b3da6e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5910949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:104eadde571ae96a598e4c64e6eacf1aa6b42251d302f3ac3f68484e507c2c4e`

```dockerfile
```

-	Layers:
	-	`sha256:a94782182795af1e151eac8aa0370028dd8355882ca8307ccada650e51a0265e`  
		Last Modified: Tue, 07 Apr 2026 02:42:25 GMT  
		Size: 5.9 MB (5857449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bba01ec0d9b1651a4c728c3cfde6fe3fb29679caef85205901427d59a754583`  
		Last Modified: Tue, 07 Apr 2026 02:42:25 GMT  
		Size: 53.5 KB (53500 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:4d47f96ce60e05a0ba53170af63a6ab1b060f8e86014f4ea709784b9bf7f58ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (140964121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f0797a2623fe5edd6263b68443b9d3cf2ac45133d79b564c05329891395aa21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:45:01 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 07 Apr 2026 01:45:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:45:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 07 Apr 2026 01:45:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 07 Apr 2026 01:45:20 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 07 Apr 2026 01:45:20 GMT
ENV LANG=en_US.utf8
# Tue, 07 Apr 2026 01:45:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:45:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 07 Apr 2026 01:45:24 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:45:24 GMT
ENV PG_MAJOR=15
# Tue, 07 Apr 2026 01:45:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 07 Apr 2026 01:45:24 GMT
ENV PG_VERSION=15.17-1.pgdg12+1
# Tue, 07 Apr 2026 01:59:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 07 Apr 2026 01:59:40 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 07 Apr 2026 01:59:40 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 07 Apr 2026 01:59:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 07 Apr 2026 01:59:40 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 07 Apr 2026 01:59:40 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 07 Apr 2026 01:59:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:59:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 07 Apr 2026 01:59:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:59:40 GMT
STOPSIGNAL SIGINT
# Tue, 07 Apr 2026 01:59:40 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 07 Apr 2026 01:59:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:dabf2c04988ff47a9777c2e6aee85c1e347525704928c5c1a366fae1fb63fea2`  
		Last Modified: Tue, 07 Apr 2026 00:58:55 GMT  
		Size: 23.9 MB (23941461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e98dc76c458f7f4952358551edd02079ed973c62a3f4befb3100176cfe482d`  
		Last Modified: Tue, 07 Apr 2026 01:59:58 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8f3eb86b7e2cb86b422b15e33768f733dc37d8b1e7ffc0aa7aba1b458fd3f6`  
		Last Modified: Tue, 07 Apr 2026 01:59:58 GMT  
		Size: 3.7 MB (3742702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4ba32f7ba14ea8671571614bbe28026224601afaf097511c655c5ca5338677`  
		Last Modified: Tue, 07 Apr 2026 01:59:58 GMT  
		Size: 1.2 MB (1216018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690f33cda4d5225e92d1e9007651c7f456c394ecf9bad37f7659042ad4545c42`  
		Last Modified: Tue, 07 Apr 2026 01:59:58 GMT  
		Size: 8.1 MB (8066466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acc1e76ced445c416d5154f5406801208c9c8d90ea109c32035b294f4e4e9d6`  
		Last Modified: Tue, 07 Apr 2026 01:59:59 GMT  
		Size: 1.1 MB (1067272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69829db95387460f49087e6dfa382b66e017a09e74ddcde5fa0cf842a1ff653e`  
		Last Modified: Tue, 07 Apr 2026 01:59:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ba0789fd2c43676612d0b2ccf9b7545929fa5de8990552ddc6494477dbc151`  
		Last Modified: Tue, 07 Apr 2026 02:00:00 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abdda17f8989c53fde3912405602beee90454a4c09499cbe71524d601f8870d7`  
		Last Modified: Tue, 07 Apr 2026 02:00:02 GMT  
		Size: 102.9 MB (102909665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3951efd37e630951ae1929b053f2a95f349142a788715f226c33939a795babf`  
		Last Modified: Tue, 07 Apr 2026 02:00:00 GMT  
		Size: 9.8 KB (9786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84b5c6c999b44b3bbce668479ab718a84b2623fa458547ec4b19ff7767145f2`  
		Last Modified: Tue, 07 Apr 2026 02:00:01 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67104a58be07c0015c0b55fef32795fd7f42d6ee7edce90563cffa3ffb5ed632`  
		Last Modified: Tue, 07 Apr 2026 02:00:01 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364ac9bb4a47bec8221653d1c8757cf4c9491e3852143250cd87fba5aee5aa4f`  
		Last Modified: Tue, 07 Apr 2026 02:00:02 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c834a4a2d30be39b1080d2cd6c8b984f579430d3b4a202a3ba5d30583b041e4`  
		Last Modified: Tue, 07 Apr 2026 02:00:02 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:d79a1d927dfb620dddeef1527c134ec56fe7f4625ef9861a5a90053db1b06321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5910207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e9a7be6f89cd367fda60b1800e44426dca4e9b2c10fc76d414de38edffdcef`

```dockerfile
```

-	Layers:
	-	`sha256:318cd97c435d6e700bccca7808a593b4c6c13b5c5871952b5712d926147669ec`  
		Last Modified: Tue, 07 Apr 2026 01:59:58 GMT  
		Size: 5.9 MB (5856704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6c5a572a26c0a334816ae734a6e36f395cf177732e37de88b07c4bcad6399a8`  
		Last Modified: Tue, 07 Apr 2026 01:59:58 GMT  
		Size: 53.5 KB (53503 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:9ad6d612b6b66d7be057fef78045fc22ad6739f7313ee180ab57da522cdbab2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150938828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a27488e9abca0b306c691c4b82f41b8af2a3e24c791324ca49f891469eda57`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:35:44 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 22 Apr 2026 01:35:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:35:54 GMT
ENV GOSU_VERSION=1.19
# Wed, 22 Apr 2026 01:35:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Apr 2026 01:35:59 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 22 Apr 2026 01:35:59 GMT
ENV LANG=en_US.utf8
# Wed, 22 Apr 2026 01:36:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:36:02 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 22 Apr 2026 01:36:03 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:36:03 GMT
ENV PG_MAJOR=15
# Wed, 22 Apr 2026 01:36:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Wed, 22 Apr 2026 01:36:03 GMT
ENV PG_VERSION=15.17-1.pgdg12+1
# Wed, 22 Apr 2026 01:36:14 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 22 Apr 2026 01:36:15 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 22 Apr 2026 01:36:15 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 22 Apr 2026 01:36:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 22 Apr 2026 01:36:15 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 22 Apr 2026 01:36:15 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 22 Apr 2026 01:36:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:36:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 22 Apr 2026 01:36:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:36:15 GMT
STOPSIGNAL SIGINT
# Wed, 22 Apr 2026 01:36:15 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 22 Apr 2026 01:36:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f725e43f1520c2e611732a7eedde2acf293fb906406ff01a1db586c94d973053`  
		Last Modified: Wed, 22 Apr 2026 01:36:33 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d827c6aa00677f9d4c1735eee1eb5354bfdf1c0f9ac47750b870a56c16a5537`  
		Last Modified: Wed, 22 Apr 2026 01:36:34 GMT  
		Size: 4.5 MB (4519569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20a774fc92713da3cf67ead677c43f27eef6fc3ec57d63e7268ed854a5f01d9`  
		Last Modified: Wed, 22 Apr 2026 01:36:34 GMT  
		Size: 1.2 MB (1203314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35e2ae1c9d05a53c254f5e1a3db1ca4ba0387bda52a57d2e1429ac31380b871`  
		Last Modified: Wed, 22 Apr 2026 01:36:34 GMT  
		Size: 8.1 MB (8066478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a890661374a43e6e6e39d086dfa7d4cc8b64bcde9e1bfa18b01ca0af52981c48`  
		Last Modified: Wed, 22 Apr 2026 01:36:35 GMT  
		Size: 1.1 MB (1109042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9d6c443ef7d3a84a63c49cb293c3b4ef9ded98d18805cbb67a020e514cf0e4`  
		Last Modified: Wed, 22 Apr 2026 01:36:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac23af118899523f2f42fba696b4e4c9c926c1c5ecfdfb3090d1fa8f439e8b65`  
		Last Modified: Wed, 22 Apr 2026 01:36:35 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8351dd07f55becf4fe9643bc9ac79c33a616afc25f5134b2e6d324bb3792fa98`  
		Last Modified: Wed, 22 Apr 2026 01:36:38 GMT  
		Size: 107.9 MB (107903531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559d8fe1beb0d72620932d9cce8cd4a056d8fc94e835570bb3eb8580ef7a6d86`  
		Last Modified: Wed, 22 Apr 2026 01:36:36 GMT  
		Size: 9.8 KB (9779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be18b935455782697221315166e7e4bd7f94985ae2dbbe90c15505f274457402`  
		Last Modified: Wed, 22 Apr 2026 01:36:36 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adec4e5a8e2a32810df365b9649e5379891ead32a257918e4d1942ac6528f4d0`  
		Last Modified: Wed, 22 Apr 2026 01:36:36 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7724273df2f67e82cf17311019ff9fe1b19d3fa135b0fa8896fa49d18d300c6`  
		Last Modified: Wed, 22 Apr 2026 01:36:37 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f1f0d1751265d8581c8d1059ee9df4ce8d2d2078ff511c1959bf8813bcd0b6`  
		Last Modified: Wed, 22 Apr 2026 01:36:38 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:7c9dc9b852d4b5013eb6e93a307c6c550de1c438dcf822ab162ea2e8c6e82040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5903200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1053d5f599467d1e5c12f55ec91ec14f24ac2061c5f429843e511c80a3615798`

```dockerfile
```

-	Layers:
	-	`sha256:839b6941dab870880760b1d46f87305a818d20c858d8818fe833bced70d1f247`  
		Last Modified: Wed, 22 Apr 2026 01:36:34 GMT  
		Size: 5.8 MB (5849659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10c07a71c2c1fe001b7ae74c80fc4a0e40ca9c1330ef04b99c1645a9a410988a`  
		Last Modified: Wed, 22 Apr 2026 01:36:34 GMT  
		Size: 53.5 KB (53541 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:6d5a43380086d28841984ca30c65f69ebafd686c492bc03630f89cf0cbfb5859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161645418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdaf6568dfe052d5a82192754ae5e76a7bfc73dd5c5361642f33975336889817`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:36:32 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 07 Apr 2026 01:36:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:36:44 GMT
ENV GOSU_VERSION=1.19
# Tue, 07 Apr 2026 01:36:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 07 Apr 2026 01:36:48 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 07 Apr 2026 01:36:48 GMT
ENV LANG=en_US.utf8
# Tue, 07 Apr 2026 01:36:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:36:51 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 07 Apr 2026 01:36:52 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:36:52 GMT
ENV PG_MAJOR=15
# Tue, 07 Apr 2026 01:36:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 07 Apr 2026 01:36:52 GMT
ENV PG_VERSION=15.17-1.pgdg12+1
# Tue, 07 Apr 2026 01:46:51 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 07 Apr 2026 01:46:51 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 07 Apr 2026 01:46:51 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 07 Apr 2026 01:46:51 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 07 Apr 2026 01:46:51 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 07 Apr 2026 01:46:51 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 07 Apr 2026 01:46:51 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:46:51 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 07 Apr 2026 01:46:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:46:51 GMT
STOPSIGNAL SIGINT
# Tue, 07 Apr 2026 01:46:51 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 07 Apr 2026 01:46:51 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2686573d3309fb5ec86398e0f20a729a351a259d4d793edf6cb41a0ef910fccb`  
		Last Modified: Tue, 07 Apr 2026 00:10:58 GMT  
		Size: 29.2 MB (29221768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ed955f00003bdfb31821b5a92374166e9ca632201674466692d08b0199fa10`  
		Last Modified: Tue, 07 Apr 2026 01:47:10 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d08a030ad4f8a47260feacfac12cd38352ad6597841106031600efee0f764d2`  
		Last Modified: Tue, 07 Apr 2026 01:47:10 GMT  
		Size: 5.0 MB (4966077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52abfef346ca2f698276dd0e6e9f615d950f0ee768e8cce83fadf1810bf8bf7`  
		Last Modified: Tue, 07 Apr 2026 01:47:10 GMT  
		Size: 1.2 MB (1218636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4075362520e83b02947a0a5b73298ea40f52d5fd491740e6dcd81a49e7dc74`  
		Last Modified: Tue, 07 Apr 2026 01:47:10 GMT  
		Size: 8.1 MB (8066452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6a83e8a39593b8bc724c02b90fed6d4b4506f7383adf77dddfad0385888a1c`  
		Last Modified: Tue, 07 Apr 2026 01:47:11 GMT  
		Size: 1.1 MB (1137457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fc2be1dad638abe060aa3b4e8862b22fd4f267d1ba5aca5ad40a13ee393253`  
		Last Modified: Tue, 07 Apr 2026 01:47:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303bd4454fd5d2fc5783e5370a55628c5716af22bfb3838af48fa2b20cfd7f9c`  
		Last Modified: Tue, 07 Apr 2026 01:47:11 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c05d3045bd5cd3e07a022a5a3aa7c10572f1f569b1ccbe85cb1274fa6ec47dc`  
		Last Modified: Tue, 07 Apr 2026 01:47:15 GMT  
		Size: 117.0 MB (117014492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94104b9604fe557e098905d066121e61e86cef05ab766fab5c9d204c1a9eb31`  
		Last Modified: Tue, 07 Apr 2026 01:47:12 GMT  
		Size: 9.8 KB (9788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08685746b26ff5832b50fb3f584b6910b1b1643c9ba464bc83bbcef447c91b1c`  
		Last Modified: Tue, 07 Apr 2026 01:47:13 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441a3ba3eb0afb0329cc4435404c79ee67d2a01584877dec3e4c949b8d0e823e`  
		Last Modified: Tue, 07 Apr 2026 01:47:12 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c7e8f0158102f89330cb3be7cdbc795fac16fa88f58793bba976a835dfbabc`  
		Last Modified: Tue, 07 Apr 2026 01:47:13 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12326def43930124b667290b26e144e548d3b98b2c831a87c5b5addeb87a621`  
		Last Modified: Tue, 07 Apr 2026 01:47:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:ffabe416e973a8662e74d5972b0b2fe2b59d27b81202a90a5dbf4165489435eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23daa4744c2ad44dfff56ca4f2562fb25bbc6e4315da0e5495545f92c6d7c851`

```dockerfile
```

-	Layers:
	-	`sha256:7cdb51f8697ffacb513cffbece3fa665626143fa9c5383266db4da2fb833062d`  
		Last Modified: Tue, 07 Apr 2026 01:47:10 GMT  
		Size: 5.9 MB (5855592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dedd3bb0c7cf121dc8b562ee85fc3818a365d535e21e9dfb29ab24479926fbc3`  
		Last Modified: Tue, 07 Apr 2026 01:47:10 GMT  
		Size: 53.3 KB (53252 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:0d872e94d68d11965e28b149bcc5f828d5b01e6a9250f9cdd46bd5469509ad5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.7 MB (151749527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5194132360dc10fea299adc430422ff943c2d07a0606b0237baaa341a4f1ccd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 08:36:10 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 07 Apr 2026 08:36:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 08:37:18 GMT
ENV GOSU_VERSION=1.19
# Tue, 07 Apr 2026 08:37:18 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 07 Apr 2026 08:37:45 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 07 Apr 2026 08:37:45 GMT
ENV LANG=en_US.utf8
# Tue, 07 Apr 2026 08:38:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 08:38:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 07 Apr 2026 08:38:08 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 08:38:08 GMT
ENV PG_MAJOR=15
# Tue, 07 Apr 2026 08:38:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 07 Apr 2026 08:38:08 GMT
ENV PG_VERSION=15.17-1.pgdg12+1
# Tue, 07 Apr 2026 13:18:15 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 07 Apr 2026 13:18:18 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 07 Apr 2026 13:18:19 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 07 Apr 2026 13:18:19 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 07 Apr 2026 13:18:21 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 07 Apr 2026 13:18:21 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 07 Apr 2026 13:18:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 13:18:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 07 Apr 2026 13:18:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 13:18:25 GMT
STOPSIGNAL SIGINT
# Tue, 07 Apr 2026 13:18:25 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 07 Apr 2026 13:18:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7377a524ccdc918cca6272a35a48618805ffa8fb443fe7f687971509cb1f8d53`  
		Last Modified: Tue, 07 Apr 2026 00:10:05 GMT  
		Size: 28.5 MB (28526285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8577deaa1ee6306b521ee5d84ddaf65f0450bfb69e5e2e10ace88d337c6cba4f`  
		Last Modified: Tue, 07 Apr 2026 09:51:03 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2193f14079132665de93d8fc43dbccb2d7e4a15aa9874d91ad7b6e9774f5548b`  
		Last Modified: Tue, 07 Apr 2026 09:51:04 GMT  
		Size: 4.5 MB (4475247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa9d1210a9eb3ea5aff9a27d0fed962b67d985e781ebf9b4aeae64f122914c0`  
		Last Modified: Tue, 07 Apr 2026 09:51:03 GMT  
		Size: 1.2 MB (1159244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e47fef44ca5ddd3d584b459d7fa9e53ad74dda9d20319868217ecaefd5e4ead`  
		Last Modified: Tue, 07 Apr 2026 09:51:04 GMT  
		Size: 8.1 MB (8066561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64e531094ee8eda299eb99703ce16f6ccb0dec62e0d8395c5229bdf89943ae6`  
		Last Modified: Tue, 07 Apr 2026 09:51:04 GMT  
		Size: 1.2 MB (1182905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66a1323700edb806f7d1852762ef08ab512cd2cb6d3d752c4ce5cc357bab520`  
		Last Modified: Tue, 07 Apr 2026 09:51:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c09b94ca6add0648b12298fad493162ceca74e3a56abda4b44871cf3d96266d`  
		Last Modified: Tue, 07 Apr 2026 09:51:05 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c616eed96003f2fe63ac8fe7e6f6fa70dff5348bbf63f1227538097cdd13e6`  
		Last Modified: Tue, 07 Apr 2026 13:20:30 GMT  
		Size: 108.3 MB (108318736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0a68051352f6a733795df85af1304bc9957fe9d332e1adb4eab0003b530fd1`  
		Last Modified: Tue, 07 Apr 2026 13:20:19 GMT  
		Size: 9.8 KB (9789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:793005f982dad630e4c1b5edf318f3be208d6c33a249c723372bc2d651338de9`  
		Last Modified: Tue, 07 Apr 2026 13:20:19 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd158b7c4a030144192cf0134242a2e9436163d54845d00764adc9087931b4d`  
		Last Modified: Tue, 07 Apr 2026 13:20:19 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4cfd9c2f7c4476e8d7034db392b3cec57ff4e51723b09757acce386cb76e386`  
		Last Modified: Tue, 07 Apr 2026 13:20:20 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4d3fa0c8e1ecdd9beed133019d1a402ab179b5190270fd6723b3109c904d95`  
		Last Modified: Tue, 07 Apr 2026 13:20:20 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:2892e6e372517a8a953f86ea7bd3e4073ec1fb76a5e92be4f7ea190bd073a575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 KB (53162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:325874f12d783541b3ab737ccdd2af40236df14ac101c37d770f337551e227df`

```dockerfile
```

-	Layers:
	-	`sha256:46bf2b061c3cf0b1eb6f3ca4424ae392ad2c47dcd66bae3fc27e89a12a19ba61`  
		Last Modified: Tue, 07 Apr 2026 13:20:18 GMT  
		Size: 53.2 KB (53162 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:024c409c61b832f2c41864aa9d2ba65535b0645d03e0b43b40ee333a308ba93b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.7 MB (165657655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4138f8f6d1116a4d50ab241f549c63f2292ac102c9d139c8c42b0e30d4bb4bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 04:01:02 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 07 Apr 2026 04:01:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:01:34 GMT
ENV GOSU_VERSION=1.19
# Tue, 07 Apr 2026 04:01:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 07 Apr 2026 04:01:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 07 Apr 2026 04:01:43 GMT
ENV LANG=en_US.utf8
# Tue, 07 Apr 2026 04:01:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:01:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 07 Apr 2026 04:01:53 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 04:01:53 GMT
ENV PG_MAJOR=15
# Tue, 07 Apr 2026 04:01:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 07 Apr 2026 04:01:53 GMT
ENV PG_VERSION=15.17-1.pgdg12+1
# Tue, 07 Apr 2026 08:32:47 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 07 Apr 2026 08:32:47 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 07 Apr 2026 08:32:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 07 Apr 2026 08:32:47 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 07 Apr 2026 08:32:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 07 Apr 2026 08:32:47 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 07 Apr 2026 08:32:48 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 08:32:48 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 07 Apr 2026 08:32:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 08:32:48 GMT
STOPSIGNAL SIGINT
# Tue, 07 Apr 2026 08:32:48 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 07 Apr 2026 08:32:48 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b1c56220ca211bc9d02f1ed5c589465809676b6ab2cef705f1e2fb8e9726de76`  
		Last Modified: Tue, 07 Apr 2026 00:09:42 GMT  
		Size: 32.1 MB (32078464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c73a4e80f8eee9e890cb47bedd35d02c67ef5bcca2b473c6d3e00a80965b06a`  
		Last Modified: Tue, 07 Apr 2026 04:04:12 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7947f119f83a299b47ca573148739e01949d18cbaa9318e7ab4a40e85e5823df`  
		Last Modified: Tue, 07 Apr 2026 04:04:13 GMT  
		Size: 5.4 MB (5368665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f2363b8d0c3c8477a5c830c8f04da66b6b2dbe1de9983fe4475a83363c62b90`  
		Last Modified: Tue, 07 Apr 2026 04:04:13 GMT  
		Size: 1.2 MB (1208247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73441d3fd6b801869bfe2128fece0f8cfd3dae11351c3d17ba334f6a60758933`  
		Last Modified: Tue, 07 Apr 2026 04:04:13 GMT  
		Size: 8.1 MB (8066577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b825f5e783521a55f9a2725ca3ae6863c9ebc88d6eeb23db6ad9f4a50720cb7f`  
		Last Modified: Tue, 07 Apr 2026 04:04:14 GMT  
		Size: 1.3 MB (1283671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255852130442a8dd66f03e76d6c53fb783681b9f0b0f0deb8976c69d771ebc43`  
		Last Modified: Tue, 07 Apr 2026 04:04:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b958c25dd0ceaa8626e0e80c7b5ef496a8edd59a35e667fc15c63e5053d77b`  
		Last Modified: Tue, 07 Apr 2026 04:04:14 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa00ba32e421e0e6a3bb3122a42be24599a7983ac3c45b79eb43716de9b4c024`  
		Last Modified: Tue, 07 Apr 2026 08:33:31 GMT  
		Size: 117.6 MB (117631502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28cceb727eeab81624b24d987581955bb469dfd41cdce1794477605bdf7d692`  
		Last Modified: Tue, 07 Apr 2026 08:33:28 GMT  
		Size: 9.8 KB (9782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b3a16eb383062a2f2f1f34f8df6395ef159399135ba4bbfbd90746868f17ae`  
		Last Modified: Tue, 07 Apr 2026 08:33:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0711356b3ae244a0a7009fb937753662bce65191847384f2aa60a8f09b8830`  
		Last Modified: Tue, 07 Apr 2026 08:33:28 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44dac0abb372317f633faa6bba129ec329a2812bbdfd686d6bcb12f38b10ca49`  
		Last Modified: Tue, 07 Apr 2026 08:33:29 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba76fa0d48f74d9664abfea6b54613645e35d4a0cce1a768d0be34b460ba4aa0`  
		Last Modified: Tue, 07 Apr 2026 08:33:29 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:0e61035b78fa8b745c522d68e2db0724ae58833ec2b8ee7248a0270dbd6d4452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5904059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c27e6c66427ad25bc11edc59f412a455181e97ca7c36efec60284dc947416c4`

```dockerfile
```

-	Layers:
	-	`sha256:fed47efab4f8263066d081ac9c9458eada2ea9f0a12076d2873283542626d81a`  
		Last Modified: Tue, 07 Apr 2026 08:33:28 GMT  
		Size: 5.9 MB (5850709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bdd659cb43f223150d50561047f0f04247205959c3eb058e1791a9daed5c2f1`  
		Last Modified: Tue, 07 Apr 2026 08:33:28 GMT  
		Size: 53.4 KB (53350 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:665d23c6176cde0fcf4d9b9005bd23c53f12acd2d127eddcf4b9ed4a1077204c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.1 MB (162117367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdbf25307ce41236fa03a45e11cc522791d7821f043c055eaff14727366216b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:00:00 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 22 Apr 2026 02:00:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:00:11 GMT
ENV GOSU_VERSION=1.19
# Wed, 22 Apr 2026 02:00:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Apr 2026 02:00:16 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 22 Apr 2026 02:00:16 GMT
ENV LANG=en_US.utf8
# Wed, 22 Apr 2026 02:00:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:00:19 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 22 Apr 2026 02:00:20 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 02:00:20 GMT
ENV PG_MAJOR=15
# Wed, 22 Apr 2026 02:00:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Wed, 22 Apr 2026 02:00:20 GMT
ENV PG_VERSION=15.17-1.pgdg12+1
# Wed, 22 Apr 2026 02:25:37 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 22 Apr 2026 02:25:37 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 22 Apr 2026 02:25:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 22 Apr 2026 02:25:37 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 22 Apr 2026 02:25:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 22 Apr 2026 02:25:37 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 22 Apr 2026 02:25:37 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:25:37 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 22 Apr 2026 02:25:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 02:25:37 GMT
STOPSIGNAL SIGINT
# Wed, 22 Apr 2026 02:25:37 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 22 Apr 2026 02:25:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11da21923a7acd15c1bdc4fbec7f740d72dea4f15ee29682c5075b48e4731af`  
		Last Modified: Wed, 22 Apr 2026 02:13:33 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5019c6e9a6ba2a6831822eddec4e8628136f5f0da21287c4bec5f5ac60d27c`  
		Last Modified: Wed, 22 Apr 2026 02:13:33 GMT  
		Size: 4.4 MB (4391207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d06d09259474456a9c6c928f6a0f6c5eadef1292744167164fc15a4f6d7f0e`  
		Last Modified: Wed, 22 Apr 2026 02:13:33 GMT  
		Size: 1.2 MB (1222828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b30b6ccae26c5a9705301e389499ddab4a8c4d99173b87daf3cc88d8dd46b5`  
		Last Modified: Wed, 22 Apr 2026 02:13:34 GMT  
		Size: 8.1 MB (8120740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c40ab67ca7705d789061a75a9efa56262fb3189f4dad4f5014de7e780000523`  
		Last Modified: Wed, 22 Apr 2026 02:13:35 GMT  
		Size: 1.1 MB (1097047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254f0aa1369bcebcb46e22c1c49cdfc25af56e49cdb023acac0e660a8caaa5b9`  
		Last Modified: Wed, 22 Apr 2026 02:13:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d90107c41a6ca028187f3a1e701989b071339c2976701facfa96680609a8ab5`  
		Last Modified: Wed, 22 Apr 2026 02:13:35 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d75314f10adfefd26fbc8069fdbff72d5471397d93990e9367dc70c78125d9d`  
		Last Modified: Wed, 22 Apr 2026 02:26:12 GMT  
		Size: 120.4 MB (120373195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35809deb915bcab8e06f3eee5b236e5341d128198a99a28a8e118729ca71db0`  
		Last Modified: Wed, 22 Apr 2026 02:26:09 GMT  
		Size: 9.8 KB (9784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862c00ca5af86d8d0a2979daeb77cbe68bf8e8e8d711a4b1ac8b7d554b0bc933`  
		Last Modified: Wed, 22 Apr 2026 02:26:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7494dfa367dd0086d981c2490dd950edc5e7406c18cf5d6e919f4d692254be`  
		Last Modified: Wed, 22 Apr 2026 02:26:09 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92afc4a0c67d8d0caa91adfbdbcfd5d482954bcabc1ada22d11cb879b986f97d`  
		Last Modified: Wed, 22 Apr 2026 02:26:10 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63105888dd129097c35d970d26700f2e6a6ca9d3290ccce26a99e1fd4e4eed25`  
		Last Modified: Wed, 22 Apr 2026 02:26:10 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:1a492572dc979910f1554880a086a7624191c4b9c5bb5f2fc0afc5e88c971ba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f1a1f41b7876c0f0480d3fa280a1f74941c5c5dc6cd5352a439d56f20f6f741`

```dockerfile
```

-	Layers:
	-	`sha256:bbb896bbe76ed9785884c246aebe935e72de61818532d20cf8dc63148eb2b195`  
		Last Modified: Wed, 22 Apr 2026 02:26:09 GMT  
		Size: 5.9 MB (5852068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85b43b6e17c29eb5a732ad178aa8a709361b5ea5337da9e690782dd8e6ee2c2e`  
		Last Modified: Wed, 22 Apr 2026 02:26:09 GMT  
		Size: 53.3 KB (53296 bytes)  
		MIME: application/vnd.in-toto+json
