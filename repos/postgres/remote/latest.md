## `postgres:latest`

```console
$ docker pull postgres@sha256:a2282ad0db623c27f03bab803975c9e3942a24e974f07142d5d69b6b8eaaf9e2
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

### `postgres:latest` - linux; amd64

```console
$ docker pull postgres@sha256:367432dc4409b2d993a72666105b1bd45de0bac8ddd9f41ece7c0e641597d2d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.9 MB (152870348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:391a00ec7cac4b8dcfb9f9341f3b34c1ad624ea2b16ce8ca3e9d848fdb650753`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:37 GMT
ADD file:d261a6f6921593f1e0b3f472ab1b1822e2c6deb0b369200f0b3370556bfad017 in / 
# Tue, 21 Nov 2023 05:21:37 GMT
CMD ["bash"]
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
ENV GOSU_VERSION=1.16
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
ENV LANG=en_US.utf8
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
ENV PG_MAJOR=16
# Thu, 07 Dec 2023 22:39:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 07 Dec 2023 22:39:53 GMT
ENV PG_VERSION=16.1-1.pgdg120+1
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 07 Dec 2023 22:39:53 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 07 Dec 2023 22:39:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Dec 2023 22:39:53 GMT
STOPSIGNAL SIGINT
# Thu, 07 Dec 2023 22:39:53 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 07 Dec 2023 22:39:53 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1f7ce2fa46ab3942feabee654933948821303a5a821789dddab2d8c3df59e227`  
		Last Modified: Tue, 21 Nov 2023 05:25:58 GMT  
		Size: 29.1 MB (29149908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0c088137b81ddb77e670944f1b6e045e9550a01888b8685542a8b2aab54df7`  
		Last Modified: Fri, 08 Dec 2023 22:12:32 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11be68f68a2e4d0a4189bc0bbf19917ac941a0c20a070b16b7219d6bc69552e1`  
		Last Modified: Fri, 08 Dec 2023 22:12:32 GMT  
		Size: 4.4 MB (4422623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f13c4e1d962d0d66022ec0721c0f23bcdfc0f99aa3ffa773f54dc0a691e48c`  
		Last Modified: Fri, 08 Dec 2023 22:12:32 GMT  
		Size: 1.4 MB (1448507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43187fdc5ebc2295dd36d0442173177187de01931b2faa35ee22b26b00f8bd64`  
		Last Modified: Fri, 08 Dec 2023 22:12:32 GMT  
		Size: 8.1 MB (8067871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84cb0803492cd27747b947acabe4d4c7d5bad6b0857e5d06b05859d2035f7c9`  
		Last Modified: Fri, 08 Dec 2023 22:12:33 GMT  
		Size: 1.2 MB (1195077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50a897e2632497badf03fe0e7d6b042a4674a2d4a3c3d205ca25a0b19a5cbc3`  
		Last Modified: Fri, 08 Dec 2023 22:12:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc6d5552c5250fa73e5a42b8bd3945b25b1e005cc3a2dae57d173f1a00ec350`  
		Last Modified: Fri, 08 Dec 2023 22:12:33 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8161286a3f116bb5c6276a39769ea7377a663acc594c44a1337c71832587e62`  
		Last Modified: Fri, 08 Dec 2023 22:12:37 GMT  
		Size: 108.6 MB (108566930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36f0ab546afcea80d28291d8e5dc1909ec560e59d2a3a034c437f44e8f92146`  
		Last Modified: Fri, 08 Dec 2023 22:12:34 GMT  
		Size: 9.9 KB (9923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a71678092b63da46f68b635db7b0623f04ed846424dbf3f95e90ebee52dcff`  
		Last Modified: Fri, 08 Dec 2023 22:12:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c23bdcac53834864ee4de0629d7a3bf8250d63d230d97716fa9e81f4ba1dc00`  
		Last Modified: Fri, 08 Dec 2023 22:12:34 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16648961c6612a942a07fc0189e17ca4e76e8a0de41745195de2027ea6ebfe0b`  
		Last Modified: Fri, 08 Dec 2023 22:12:35 GMT  
		Size: 4.8 KB (4782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:f567d94bcb8db3931c991c3809804e51a05a458a51b7b43b7fde4e8063b54d04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4996701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e211e4078b6b63710dfd6edecd5ea31f67e7b9f5923871269dc548651e0e6614`

```dockerfile
```

-	Layers:
	-	`sha256:aaeae7e7c2570deaf81fed0ba2f096526282892480b44754f5d76d59d12b3278`  
		Last Modified: Fri, 08 Dec 2023 22:12:31 GMT  
		Size: 4.9 MB (4945339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b369276b648eded92ced66b63283d1b61bf9d92ec525534c3633737ee09a579f`  
		Last Modified: Fri, 08 Dec 2023 22:12:31 GMT  
		Size: 51.4 KB (51362 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; arm variant v5

```console
$ docker pull postgres@sha256:f15adcc7d39d60fefcd7fffe6d69635e282dd606a7473ebdf9292a00d1a0c8cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.7 MB (145684641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a81691fa31f2cd0e05705bb84ec855983835a36f906437afdfecb639cd709de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 21 Nov 2023 05:00:51 GMT
ADD file:1ae8e5ac45b11d01083680b765e1fcfef9f7938f89d6f424572126fa946d8cdf in / 
# Tue, 21 Nov 2023 05:00:52 GMT
CMD ["bash"]
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
ENV GOSU_VERSION=1.16
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
ENV LANG=en_US.utf8
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
ENV PG_MAJOR=16
# Thu, 07 Dec 2023 22:39:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 07 Dec 2023 22:39:53 GMT
ENV PG_VERSION=16.1-1.pgdg120+1
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 07 Dec 2023 22:39:53 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 07 Dec 2023 22:39:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Dec 2023 22:39:53 GMT
STOPSIGNAL SIGINT
# Thu, 07 Dec 2023 22:39:53 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 07 Dec 2023 22:39:53 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f476aef5b6e1122850e68c81ef06fc2df17e968961b060483b4d2fb33018aae3`  
		Last Modified: Tue, 21 Nov 2023 05:03:55 GMT  
		Size: 26.9 MB (26922153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749be5ef15818a6d009a4eeb567fd6b3341f668dbd0778f344ba9ac1c3434090`  
		Last Modified: Fri, 08 Dec 2023 23:49:50 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cfc5a4bde01ce112826bedc5094d77282fddbd8697063c504bb035e5a7ffe1`  
		Last Modified: Fri, 08 Dec 2023 23:49:50 GMT  
		Size: 4.0 MB (4040489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c818e7cc03f89d1edf7b7dcac145dffa73298e87bc608f0d0ced470844da8c2b`  
		Last Modified: Fri, 08 Dec 2023 23:49:50 GMT  
		Size: 1.4 MB (1426052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bacdb34348a9747d38a6db8c6fc635b82fcd09258f03a97cc16f830544eb4c1c`  
		Last Modified: Fri, 08 Dec 2023 23:49:51 GMT  
		Size: 8.1 MB (8067982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd985847be75937a28a261fb141a6b83f7a3a2869d7cb9802a97e494b1206bf2`  
		Last Modified: Fri, 08 Dec 2023 23:49:51 GMT  
		Size: 1.2 MB (1193963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0ede3e8380dbd67add822320acc1014151fd90bd8285565e2e4b17b21adbab`  
		Last Modified: Fri, 08 Dec 2023 23:49:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69cc4363f64d85c4f58f7ab91a533f7153e4b8a7707c5ce1495298d29bb76468`  
		Last Modified: Fri, 08 Dec 2023 23:49:52 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5bb1d2d1b56891beea050c9c6686cde4adde8520c1ab4aee03557f581bde093`  
		Last Modified: Fri, 08 Dec 2023 23:49:55 GMT  
		Size: 104.0 MB (104014560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7755ece6f57cda454efcbc827980bc076ce2bc085ca6691a9c4a1f00660b8db`  
		Last Modified: Fri, 08 Dec 2023 23:49:52 GMT  
		Size: 9.9 KB (9929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa7060c041531275905460aaa69e25117ac42cad7ac6a82dc6f5c3d0deea805`  
		Last Modified: Fri, 08 Dec 2023 23:49:53 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224a73e1ccb758ce4f29d1e45228fdbaddb65eacac5a74275bcc81796ab131c9`  
		Last Modified: Fri, 08 Dec 2023 23:49:53 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e30d4a0ed9082a244e66eea7baffed7f5675a91e46c0daa859c18e2624ebd0`  
		Last Modified: Fri, 08 Dec 2023 23:49:53 GMT  
		Size: 4.8 KB (4787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:3caa5a8ae48cd1b9f20858ea316075d8814b022977d55733caa988e96f274722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 KB (51196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de77c23971266e624f9234e6b07e952e0ecfd504da2785b988f284b77389c719`

```dockerfile
```

-	Layers:
	-	`sha256:d12f8f4dc59327fe96680c4f74986cf6dc3b2bbaabcffe813ca36ad6fbf7432e`  
		Last Modified: Fri, 08 Dec 2023 23:49:50 GMT  
		Size: 51.2 KB (51196 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; arm variant v7

```console
$ docker pull postgres@sha256:3ee00f72d0d11fe2fff2236cd388e97617e5f137c2431bea136c16c53b29dc10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140513421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8a65077084f146ef798174c1191307e3d7dc93c5c8077251cf55263cbd21c72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 21 Nov 2023 03:57:43 GMT
ADD file:b693944382a95fa47622fde77eb98f0cdeafa40261e7334bd355e00f650b6632 in / 
# Tue, 21 Nov 2023 03:57:43 GMT
CMD ["bash"]
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
ENV GOSU_VERSION=1.16
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
ENV LANG=en_US.utf8
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
ENV PG_MAJOR=16
# Thu, 07 Dec 2023 22:39:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 07 Dec 2023 22:39:53 GMT
ENV PG_VERSION=16.1-1.pgdg120+1
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 07 Dec 2023 22:39:53 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 07 Dec 2023 22:39:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Dec 2023 22:39:53 GMT
STOPSIGNAL SIGINT
# Thu, 07 Dec 2023 22:39:53 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 07 Dec 2023 22:39:53 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b4ce590529bbcf84326048a22fce76fcfcb5c60af5519debd7935a74c1e9126e`  
		Last Modified: Tue, 21 Nov 2023 04:01:50 GMT  
		Size: 24.7 MB (24748925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21f4aebb739ffe9e0940e28d247a8da2f821a7f31a7802ddbeec56c29d382fe`  
		Last Modified: Wed, 22 Nov 2023 01:33:09 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8cff5cb7280b5e856a5c26b4275967808fa3cd8f286358a620731f3890ddf5`  
		Last Modified: Wed, 22 Nov 2023 01:33:09 GMT  
		Size: 3.6 MB (3645045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1afbab58653c806dee1842134bc232fc8cc4443e53a1fe16a5c8e0585e94bce`  
		Last Modified: Wed, 22 Nov 2023 01:33:09 GMT  
		Size: 1.4 MB (1416140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b3f0fa04d232a3c3ce72e77065c901b3902f976c0029d8a166a9035f5c3bb2`  
		Last Modified: Sat, 09 Dec 2023 05:37:40 GMT  
		Size: 8.1 MB (8067932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e59493675a5375d463b6e5328bd150d0f19c59eb446ca5a1fcc643d0210d59a`  
		Last Modified: Sat, 09 Dec 2023 05:37:39 GMT  
		Size: 1.1 MB (1065978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e280b4019edf92089c2093350fcc13ea707026f191d4b42dc860f3c8d08874`  
		Last Modified: Sat, 09 Dec 2023 05:37:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16f8fa83f99c03bc7c7e540ed27c4ed91ffd63085a00fe5dafad7d2fec0db7e`  
		Last Modified: Sat, 09 Dec 2023 05:37:39 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f195cba75b6011178cee21f8d57790c0daca4ab460431016e78867c0fa256bf1`  
		Last Modified: Sat, 09 Dec 2023 05:37:44 GMT  
		Size: 101.5 MB (101549956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e9e84dd5672f8c439dfb3e4f2dc92f236861af84b0351d51c1bde6766a52e83`  
		Last Modified: Sat, 09 Dec 2023 05:37:40 GMT  
		Size: 9.9 KB (9933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3efb4749a219be3fcf749707ee44f9d83ec332670873eed3982f038baf1d0cf2`  
		Last Modified: Sat, 09 Dec 2023 05:37:40 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e99090926904e93e53ab1dfedd4a618460a6033170ebac339c68011a89c1c2c`  
		Last Modified: Sat, 09 Dec 2023 05:37:41 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595addb1f838f714ff1379456088b7c5d2fe76823666750fa1380c387eca3ea6`  
		Last Modified: Sat, 09 Dec 2023 05:37:41 GMT  
		Size: 4.8 KB (4787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:efebbdcec302bcfdb8d874b1f3a84c8ed06e3237b2b29299d68e831b589886df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5012299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d44ad1a661f43172f17b61ee13b899a4be380503f620078df796d2526ac91066`

```dockerfile
```

-	Layers:
	-	`sha256:aa1ec125f06b6549579a962bc7a98d788906f11e3d6f45caba3f9d1c2a84a7b4`  
		Last Modified: Sat, 09 Dec 2023 05:37:39 GMT  
		Size: 5.0 MB (4960888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0df995bacd49d9e6eddadb6b7822d703198d904b8736fdad2654f3961d1d7ae7`  
		Last Modified: Sat, 09 Dec 2023 05:37:39 GMT  
		Size: 51.4 KB (51411 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:3d6a1b8e4b062e8cdaf9ed6fd8b70d11c4fea34457b4568762f21a76ecc06ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.1 MB (151050131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e94111c791ed44a10847467e1fb9e1cd01003d83def68e7b4fc790d3df0d740`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:06 GMT
ADD file:869c7d0747a17c53715581a2e862992eb8516c7f45f167821dfa80966a4870d1 in / 
# Tue, 21 Nov 2023 06:27:06 GMT
CMD ["bash"]
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
ENV GOSU_VERSION=1.16
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
ENV LANG=en_US.utf8
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
ENV PG_MAJOR=16
# Thu, 07 Dec 2023 22:39:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 07 Dec 2023 22:39:53 GMT
ENV PG_VERSION=16.1-1.pgdg120+1
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 07 Dec 2023 22:39:53 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 07 Dec 2023 22:39:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Dec 2023 22:39:53 GMT
STOPSIGNAL SIGINT
# Thu, 07 Dec 2023 22:39:53 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 07 Dec 2023 22:39:53 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2c6d21737d8318aa15c4cc838475029a5efc36c0429e3d8da80d97d0b96d9aaf`  
		Last Modified: Tue, 21 Nov 2023 06:30:30 GMT  
		Size: 29.2 MB (29179277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cceff339129572dbb692e7aa1ed4221a7ffc75cf59151c83b04ff8dc59e069c`  
		Last Modified: Wed, 22 Nov 2023 11:51:51 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205f857684f5cbc32a359894eac031b9e3228e9e600f87a016db9921226bf202`  
		Last Modified: Wed, 22 Nov 2023 11:51:51 GMT  
		Size: 4.4 MB (4383844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cba82cb23b34b9baa62d2db06ae15164a9877c18aa858187007c9aecdc11f25`  
		Last Modified: Wed, 22 Nov 2023 11:51:51 GMT  
		Size: 1.4 MB (1380715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4803766e4d1fd9337fa99584a3f977783a291a1b0946306bf4dfb5a3088d2c49`  
		Last Modified: Sat, 09 Dec 2023 06:33:21 GMT  
		Size: 8.1 MB (8068014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f0ec34e7211c28e9e49e1aeb75a41eb0082c8f207e4602922ce44a008536fa`  
		Last Modified: Sat, 09 Dec 2023 06:33:21 GMT  
		Size: 1.1 MB (1107771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:446b4885cd3990649fd2bdd013f0e90cc7639745d75a5616df9ee0da2e608d99`  
		Last Modified: Sat, 09 Dec 2023 06:33:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7bd820ae0a820816c978ad1e6780598cb96aedc56117afe661b71b84d85b75`  
		Last Modified: Sat, 09 Dec 2023 06:33:21 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59656b694bd132522f38577db97117da42f5dae5d668bf2bf1b50b21585271f6`  
		Last Modified: Sat, 09 Dec 2023 06:33:25 GMT  
		Size: 106.9 MB (106911080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b57c0e9c7850f106a38b2d1d52dce24be2259ef0fc7c678dac2a53f677793e3`  
		Last Modified: Sat, 09 Dec 2023 06:33:22 GMT  
		Size: 9.9 KB (9924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1fd2992003fb9492d6023a0297f943ae2148ec718043753d0310af0f93b096`  
		Last Modified: Sat, 09 Dec 2023 06:33:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a156e5981d7d38001408e8eedd55f3f4d0c6f77f6880c4e136a6189b7b7138`  
		Last Modified: Sat, 09 Dec 2023 06:33:23 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10cb21bd9a17d9e2d76183810ae3ed9c05eb5e6c17cdf0346fea983a6eb817b`  
		Last Modified: Sat, 09 Dec 2023 06:33:23 GMT  
		Size: 4.8 KB (4784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:6169329dcedf2e966c5b3f1cd1f215196c672797c1ee8132264cbeca15c033d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5002212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc2f22a49537a4c46223423a07d8c7ea212550d1dcb4997cdd09aa4a969e951d`

```dockerfile
```

-	Layers:
	-	`sha256:1f59fc92d93d8f5253a0fcc9d48a802edca6cbcaf0198d29e406e538ca5c3b89`  
		Last Modified: Sat, 09 Dec 2023 06:33:21 GMT  
		Size: 5.0 MB (4951003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a65bd677e9f53e53bdfa9f924e5c7c6a9f723c830f55a4bbe44d1b64b7a58495`  
		Last Modified: Sat, 09 Dec 2023 06:33:21 GMT  
		Size: 51.2 KB (51209 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; 386

```console
$ docker pull postgres@sha256:03eef6d50f4dba45c2b60374cf8e8177d4ca1e4a2bed11ab5c7f4c490c15491f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157835603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d57ee2757365dcd2377cc2687c36530ffb49af3b2ae20f5a8b11fee08a8109b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 14 Sep 2023 18:21:14 GMT
ADD file:0c94521fdd9c0a4fdeeb9aad23e68cd053fba0dcd7c3af550aefa79377816e31 in / 
# Thu, 14 Sep 2023 18:21:14 GMT
CMD ["bash"]
# Thu, 14 Sep 2023 18:21:14 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
ENV GOSU_VERSION=1.16
# Thu, 14 Sep 2023 18:21:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8 # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
ENV LANG=en_US.utf8
# Thu, 14 Sep 2023 18:21:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
ENV PG_MAJOR=16
# Thu, 14 Sep 2023 18:21:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 14 Sep 2023 18:21:14 GMT
ENV PG_VERSION=16.0-1.pgdg120+1
# Thu, 14 Sep 2023 18:21:14 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Sep 2023 18:21:14 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA" # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Sep 2023 18:21:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Sep 2023 18:21:14 GMT
STOPSIGNAL SIGINT
# Thu, 14 Sep 2023 18:21:14 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Sep 2023 18:21:14 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:98bdfce9af831c2a0d0bfcca812d0039cd1666986550f552b4b4c625bd5aa31c`  
		Last Modified: Wed, 01 Nov 2023 00:43:26 GMT  
		Size: 30.2 MB (30164042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb6f41839eb2a87ef2dffd17343aa5ddc05b97c522918e943d78d47cddcdede`  
		Last Modified: Wed, 01 Nov 2023 01:21:46 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f3287b79b8e0c64a2515238159cc4b56f2eaed7641825f950c1d914f30faeb`  
		Last Modified: Wed, 01 Nov 2023 01:21:46 GMT  
		Size: 4.8 MB (4844453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec4bc8f6e5898fe7a3966ce909f46ab4e0df9bbdc1d423068849f511dfa8cc0`  
		Last Modified: Wed, 01 Nov 2023 01:21:46 GMT  
		Size: 1.4 MB (1424527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f690361a3214cd03da3488f25f2c1208100f0846a42fae85d4dd151510f70d6a`  
		Last Modified: Wed, 01 Nov 2023 01:21:47 GMT  
		Size: 8.1 MB (8067937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89d6c39dcf3764ecfa3fa09854205c72830f74726dafdbe207811b2fecaa0f0`  
		Last Modified: Wed, 01 Nov 2023 01:21:47 GMT  
		Size: 1.1 MB (1136190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fd6a304af6288214e0e3822448a99f3e51ac21bdec693c051d04a4b71daf2b`  
		Last Modified: Wed, 01 Nov 2023 01:21:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939c952ec8773ec2d7ac33c8d3d7b4910ebb1696e2b816d25fb142b947a4b5b8`  
		Last Modified: Wed, 01 Nov 2023 01:21:48 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbee1af947ebd8571fb4063bfc6a5a994a1073c667244508625d98d0dc0997e9`  
		Last Modified: Wed, 01 Nov 2023 01:21:55 GMT  
		Size: 112.2 MB (112179020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2d5fd0ee494e42cd225c4474d9e3f528a4a39c4a5e19a48609a0d194866164`  
		Last Modified: Wed, 01 Nov 2023 01:21:48 GMT  
		Size: 9.9 KB (9931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1bad1d03f59c75f3298a1cb40af270730bbad8891ffdef388dc62947d38cf0`  
		Last Modified: Wed, 01 Nov 2023 01:21:48 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ff3b03393dc5eef858678a585691eedeab8cdce20a90d1073bf6d31eec5d72`  
		Last Modified: Wed, 01 Nov 2023 01:21:49 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c467916b185a75dbe7f48a83b65f9223e54827f8cc48cd4d4f03f2f15dc7022`  
		Last Modified: Wed, 01 Nov 2023 01:21:49 GMT  
		Size: 4.8 KB (4784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:2808278f9dffa2efe1259b3730de4d2c6c7dd6d9c1ba2b8e17dd76fcc22e6b4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 KB (50955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b4cf8cee0adb4afb5891e7eb6f9f6bcbd766a0dfcc6fe3ac246ae15660473a`

```dockerfile
```

-	Layers:
	-	`sha256:e746b284e291cc3a88304abd22171f857e17d10f88c9579714d9dbf4b928c81a`  
		Last Modified: Wed, 01 Nov 2023 01:21:46 GMT  
		Size: 51.0 KB (50955 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; mips64le

```console
$ docker pull postgres@sha256:6aa3932a24ea1cbed0bade2aaf85a53ce8d3068b298993be5e339511482e5a13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.9 MB (148928814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4401029e86030cfd105eba800a2a44d7ad8f4e03273c167ab09b4e2dcef17d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 21 Nov 2023 04:09:50 GMT
ADD file:e093749192323dc72b60a8440ddba26c415586f618b5e107fa264ba5eb2ca7ba in / 
# Tue, 21 Nov 2023 04:09:54 GMT
CMD ["bash"]
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
ENV GOSU_VERSION=1.16
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
ENV LANG=en_US.utf8
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
ENV PG_MAJOR=16
# Thu, 07 Dec 2023 22:39:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 07 Dec 2023 22:39:53 GMT
ENV PG_VERSION=16.1-1.pgdg120+1
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 07 Dec 2023 22:39:53 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 07 Dec 2023 22:39:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Dec 2023 22:39:53 GMT
STOPSIGNAL SIGINT
# Thu, 07 Dec 2023 22:39:53 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 07 Dec 2023 22:39:53 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ebdff2138fee4a3ec27560ab1353dc51c12c2608ff721f5db3d24104872b702a`  
		Last Modified: Tue, 21 Nov 2023 04:20:35 GMT  
		Size: 29.1 MB (29141984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c1e134b14c81c56b4ed9988dbb37bdc67bf94402900423ac3f735173216a11`  
		Last Modified: Sat, 09 Dec 2023 06:56:33 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9b50b308a3a7a18a0df16dc82ad5b232646ea0c13a6aaa5d1b37c8c4f8c4b3`  
		Last Modified: Sat, 09 Dec 2023 06:56:34 GMT  
		Size: 4.4 MB (4355816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293341dc1fd0cffe25edf4988e7305459c5d0ac855bcc36bbb515db3b59cebf6`  
		Last Modified: Sat, 09 Dec 2023 06:56:34 GMT  
		Size: 1.3 MB (1336007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc127975ccd48b6aa03b42019eaf34e8f3d69b05608ddf54d9fdec47298589e9`  
		Last Modified: Sat, 09 Dec 2023 06:56:35 GMT  
		Size: 8.1 MB (8068128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7273ee0da7a4c8d9d72dc651d9d08c04d78692b9d8196dddd16823d7e354b0bc`  
		Last Modified: Sat, 09 Dec 2023 06:56:34 GMT  
		Size: 1.2 MB (1181559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7e7825a0d13c8a3286b9667149efcf5d7fda0e5022c3bc6c7b38fdc8b275ed`  
		Last Modified: Sat, 09 Dec 2023 06:56:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03fec3314d1fe7ef1147f42d6045fdd0bc2ecfe4a7fe36712bcb76914ba3ee5`  
		Last Modified: Sat, 09 Dec 2023 06:56:35 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebcb884af73951748d4767e42f46963af755a078002ebbf95092bbad95946bb`  
		Last Modified: Sat, 09 Dec 2023 06:56:52 GMT  
		Size: 104.8 MB (104825871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bbf2a6112275e51248d393e74d9b43feac0043dff464b8440674ba38af54626`  
		Last Modified: Sat, 09 Dec 2023 06:56:36 GMT  
		Size: 9.9 KB (9928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b64da4ac50daa43a8d9dc8ca3289d0c9e1d54b01927334f887f0cf2f401709`  
		Last Modified: Sat, 09 Dec 2023 06:56:36 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721133fac96df8ed66df168ebc38b967149b6ea10e538aae260f93e9c8e72240`  
		Last Modified: Sat, 09 Dec 2023 06:56:36 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d583c8c88f94eba08a9e0ae584dc663e11ad84b8ccaa055dd9d3be717c084ad0`  
		Last Modified: Sat, 09 Dec 2023 06:56:37 GMT  
		Size: 4.8 KB (4792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:337cfe0998cd8b4be4f33f47c139e2bf5c4600a5fb02fcba34045d9cd3b7fce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 KB (51085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0820125fb9981dfa7a30178c2a075ad31f67cb230ccb8dbfde23990e75c54691`

```dockerfile
```

-	Layers:
	-	`sha256:b881ee2ffd35ee2515f00260fe3687ce3afd43de7886eaedccb9cee5fe913063`  
		Last Modified: Sat, 09 Dec 2023 06:56:33 GMT  
		Size: 51.1 KB (51085 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; ppc64le

```console
$ docker pull postgres@sha256:6f10398897aad809d9baad2a1653446cb6e686f2004db74015ade7a5a0bb12de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.2 MB (165179676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7baec2497d97d1eddaab032c4c885558472dce6a1054afaacd9a275e3dea17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 21 Nov 2023 04:24:14 GMT
ADD file:8b22a531b6611a1e63dfc20e4e2931592e2d821bd4b64c4b2810bb9a36640c02 in / 
# Tue, 21 Nov 2023 04:24:16 GMT
CMD ["bash"]
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
ENV GOSU_VERSION=1.16
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
ENV LANG=en_US.utf8
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
ENV PG_MAJOR=16
# Thu, 07 Dec 2023 22:39:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 07 Dec 2023 22:39:53 GMT
ENV PG_VERSION=16.1-1.pgdg120+1
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 07 Dec 2023 22:39:53 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 07 Dec 2023 22:39:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Dec 2023 22:39:53 GMT
STOPSIGNAL SIGINT
# Thu, 07 Dec 2023 22:39:53 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 07 Dec 2023 22:39:53 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c570d04e61d8e35a3c8f12179d048d701451f97f9cf2099ea3e3738512dbf062`  
		Last Modified: Tue, 21 Nov 2023 04:28:58 GMT  
		Size: 33.1 MB (33141607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2e1444eb5768a9f1452aad0278ed3b46e23bd0ddcdd4834e4c0c3f04f7a564`  
		Last Modified: Tue, 21 Nov 2023 23:54:59 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa03b72cb005f7e4b1680abe9b55b766463104336988c455382e20b7bd83ffe`  
		Last Modified: Tue, 21 Nov 2023 23:54:59 GMT  
		Size: 5.2 MB (5239246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cb219c2b2f2937086d88d617001b3022093e4bdb6b1b0f88c97f0800c1b221`  
		Last Modified: Tue, 21 Nov 2023 23:54:59 GMT  
		Size: 1.4 MB (1370020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e462d13c06b51d7c908aa6cbc93b2bcde82212de9ccd7ad886f35c9d16c328`  
		Last Modified: Sat, 09 Dec 2023 04:38:48 GMT  
		Size: 8.1 MB (8068028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a417abce6335440f9a1599a71d0db83ce4ffbbe505d6ff49ade43aef04ebc9f5`  
		Last Modified: Sat, 09 Dec 2023 04:38:47 GMT  
		Size: 1.3 MB (1282773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a832690b60f7957430cfe884b1c46be35fefa8f118a01692c8d54479bf785db`  
		Last Modified: Sat, 09 Dec 2023 04:38:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0b051ef9bdd2b6276bf8538b01573ca9ee44b7c0574696cb1f83ab2945c330`  
		Last Modified: Sat, 09 Dec 2023 04:38:47 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71aab70a79b1c5ad0863d54fb6778ebf3373c23b730885a3d4542240d7776e2e`  
		Last Modified: Sat, 09 Dec 2023 04:38:52 GMT  
		Size: 116.1 MB (116058561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297b8032b8180db55a7e8354e85e466a2f9b7c8c6788e5f0f7e2d8d5726c969e`  
		Last Modified: Sat, 09 Dec 2023 04:38:48 GMT  
		Size: 9.9 KB (9930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c354bdda0d050884bb6b78fea791304a9e9ff9372d70fac1a80587211045f24`  
		Last Modified: Sat, 09 Dec 2023 04:38:49 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9397fe4980773671aa93c96ac9089d4e7affddcb68d34c7dcec584ab006165a`  
		Last Modified: Sat, 09 Dec 2023 04:38:49 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b239db0f1a442487c9f7f81c11ef48781ba64e232241039e84313138cb6bad7`  
		Last Modified: Sat, 09 Dec 2023 04:38:50 GMT  
		Size: 4.8 KB (4786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:d823ee7638a23810de1b220a393e5ba3a18dadd657c92f8ef36066b77ea0c1e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5003845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419804ad45ef5fa84725e95bb4d228da16d687545813820b5c1e2b129e150221`

```dockerfile
```

-	Layers:
	-	`sha256:3b9f7ab20b3dc24d7c1a10f83b0b368ad5815fbe6aa016d5890e6bc6a0878ecc`  
		Last Modified: Sat, 09 Dec 2023 04:38:47 GMT  
		Size: 5.0 MB (4952580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b2a8c51c8ca916f5fe61a08663589988c89cad837ef347555e53974d08f7795`  
		Last Modified: Sat, 09 Dec 2023 04:38:47 GMT  
		Size: 51.3 KB (51265 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; s390x

```console
$ docker pull postgres@sha256:b1fb5d81d729723c6a8ee8dabe67184266c389523d11071cd42c6d45d14a13cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.6 MB (158577130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5ff3efd6d712142e6c8112b8e0115ff8a8628111d3acf968b9d6987fe89ed30`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 21 Nov 2023 05:04:35 GMT
ADD file:c33fa9fdde73983850798b6eb1cd062e0398109d1d773e6a937fead7475c8efc in / 
# Tue, 21 Nov 2023 05:04:41 GMT
CMD ["bash"]
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
ENV GOSU_VERSION=1.16
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
ENV LANG=en_US.utf8
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
ENV PG_MAJOR=16
# Thu, 07 Dec 2023 22:39:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 07 Dec 2023 22:39:53 GMT
ENV PG_VERSION=16.1-1.pgdg120+1
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 07 Dec 2023 22:39:53 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 07 Dec 2023 22:39:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Dec 2023 22:39:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Dec 2023 22:39:53 GMT
STOPSIGNAL SIGINT
# Thu, 07 Dec 2023 22:39:53 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 07 Dec 2023 22:39:53 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6daa625e5a040476e253e7acd0befa74254a4865ec836d6334a544d82a21d4be`  
		Last Modified: Tue, 21 Nov 2023 05:10:21 GMT  
		Size: 27.5 MB (27512885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89216ae53f720b4da9522deb1c8896d66a743dbc83d0ab5356ccf6bf6c0ad8e4`  
		Last Modified: Tue, 21 Nov 2023 18:22:46 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd1123ed4c50e7e0d7ff3fb10d11792421107339b8201d7dea2bde635cf5d86`  
		Last Modified: Tue, 21 Nov 2023 18:22:46 GMT  
		Size: 4.3 MB (4278291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d8142ebc194d7418f51ad332e0a79f3e1a575f2503f46b4f93cb085d5812f4`  
		Last Modified: Tue, 21 Nov 2023 18:22:46 GMT  
		Size: 1.4 MB (1414350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb75167d761f2f5cd3eda298ae7213b097f3939d9f064e76e43755a32a78e5b`  
		Last Modified: Sat, 09 Dec 2023 01:59:18 GMT  
		Size: 8.1 MB (8122273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a818c801adb9fe2619494f02d44d6bfd8553ce331001dbda8e792ce893c841`  
		Last Modified: Sat, 09 Dec 2023 01:59:18 GMT  
		Size: 1.1 MB (1095731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08942158f77ced9b1b87c5d52551306d38aca1c61950b8e882fcfb119ae163c7`  
		Last Modified: Sat, 09 Dec 2023 01:59:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5ccd328d41b41c2308349b20b876d2982ab878c7c1317a470f85fe0e36ad67`  
		Last Modified: Sat, 09 Dec 2023 01:59:17 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afdab71c7afc458d2efb7518c725137dcde83d1a193cfd08dc77312f10ea92fe`  
		Last Modified: Sat, 09 Dec 2023 01:59:21 GMT  
		Size: 116.1 MB (116134164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e890fd13cce648c5ccbd58c2bac0238578135cc27acb77c979110cd7cba0888a`  
		Last Modified: Sat, 09 Dec 2023 01:59:18 GMT  
		Size: 9.9 KB (9928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f6a8764810c9eb9304274cf23bb53f72b495b61973422cfbb884adf6930204`  
		Last Modified: Sat, 09 Dec 2023 01:59:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f0da0d2f81e23c9a5a3a9faac326132985d1ea0c408ac4662b3c2aa9d54860`  
		Last Modified: Sat, 09 Dec 2023 01:59:19 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a16cedccfc77b4a847b18973fde2cf86372cc1b3cd694f27c4236098fd688a1`  
		Last Modified: Sat, 09 Dec 2023 01:59:19 GMT  
		Size: 4.8 KB (4786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:1c2e8a07665342cf9f2b70963b4937bf464da3f28aa4a8938040563b60e22b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4995716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ae8dd008a3f7f8adc17fa387146513c130a4dccc6cf7adc797a49d8b62387f`

```dockerfile
```

-	Layers:
	-	`sha256:6b1496714562bc56ade7e4782ea56b1d119122a71139f472c53a14ca95a6f71b`  
		Last Modified: Sat, 09 Dec 2023 01:59:18 GMT  
		Size: 4.9 MB (4944521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9753bceca497c54a2f0a3647358c7bcf168923356889d593d30666731dbe5f7`  
		Last Modified: Sat, 09 Dec 2023 01:59:17 GMT  
		Size: 51.2 KB (51195 bytes)  
		MIME: application/vnd.in-toto+json
