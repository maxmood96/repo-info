## `postgres:15-bookworm`

```console
$ docker pull postgres@sha256:9c4f9d01c7b034b48bf91bfbc601c715e0ef88e379b95d8ab55fe59a5ad939c0
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
$ docker pull postgres@sha256:13c97a6f2aa0f1483ce55513c5c0528051005c86da72c8ca84778ea0eabaf352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151330049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f77c5a59ad583a37bf03a692a7eeb4d2a3684745155695358bc5a16e4a63516`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:44:17 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 09 May 2024 18:44:17 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV PG_MAJOR=15
# Thu, 09 May 2024 18:44:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 09 May 2024 18:44:17 GMT
ENV PG_VERSION=15.7-1.pgdg120+1
# Thu, 09 May 2024 18:44:17 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:44:17 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:44:17 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:44:17 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:44:17 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:44:17 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268fb554018fb57780689a9adf97763316178d313dcee40821132ac00cd2e2e8`  
		Last Modified: Thu, 13 Jun 2024 18:24:20 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99953dbc0e049ce11110a813f2244eaad9b293aadc7b7988f4f5ce23b3ce6a2`  
		Last Modified: Thu, 13 Jun 2024 18:24:21 GMT  
		Size: 4.5 MB (4533726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec644a5562df63843b3d7932c08aba4b2bfc0c38b4350740ae3d132db99913e5`  
		Last Modified: Thu, 13 Jun 2024 18:24:21 GMT  
		Size: 1.4 MB (1449926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b3633ef3dc26bdb93a6bbaf890a7b6cc0ec2cb4388b4885f34b9f6e9a7cab9`  
		Last Modified: Thu, 13 Jun 2024 18:24:20 GMT  
		Size: 8.1 MB (8068885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bcaade78f8f8f46b67269e6b994a3d28b1745a1abe2f9fcc31759b03f2d273c`  
		Last Modified: Thu, 13 Jun 2024 18:24:21 GMT  
		Size: 1.2 MB (1196096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27a57b6d3a6ed591ed6ee46506a64a18cd66a2dba7a31291c9a98832b711e24`  
		Last Modified: Thu, 13 Jun 2024 18:24:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de500326540557af671594180194e8b77ce3d29f875fd152056a7173a6ffb9a5`  
		Last Modified: Thu, 13 Jun 2024 18:24:22 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7ad6c21ee94b95e6c26a44d45c4a3ba87098e83ffba567d73a2ea41696e231`  
		Last Modified: Thu, 13 Jun 2024 18:24:23 GMT  
		Size: 106.9 MB (106910882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259be144ed3776d4a2d4a0e21de124ca8d79f030c0dc2e72776c68c80942d0ed`  
		Last Modified: Thu, 13 Jun 2024 18:24:22 GMT  
		Size: 9.8 KB (9775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6febd76974e0a6d0ceb8e5da9962f6ed504f03ea8b0dbbe9da78d620a5d36ad`  
		Last Modified: Thu, 13 Jun 2024 18:24:23 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5c51699243b0d547bae63ea3a1f7e9250dcd48fe4422699b1d1fca02403057`  
		Last Modified: Thu, 13 Jun 2024 18:24:23 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861bc5810e64ce243e23948749d42c5687272442c6b62c375110496dc16f3002`  
		Last Modified: Thu, 13 Jun 2024 18:24:23 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d922d3c7d7b8afe1fe70de95aa6584d6d2d1ea752aa896e7c26ceec7b29efc4`  
		Last Modified: Thu, 13 Jun 2024 18:24:23 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:040e195b76cb04fcee7e65b47d2549b30c380b1a5b1f2a2c2001707e39f04ae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5709705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee65396cb8d846c5a26d07a6b6a186ceeb384312cb3fcdb571d9ff41480c8988`

```dockerfile
```

-	Layers:
	-	`sha256:6447d48f078c7ef2e150940cd823fc7f5abebb5870da6fd740f611fd04011d39`  
		Last Modified: Thu, 13 Jun 2024 18:24:20 GMT  
		Size: 5.7 MB (5655194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16903c847c21ac30767e716cc5eef2287aaecb26b17e464ef47f4c9468a6120c`  
		Last Modified: Thu, 13 Jun 2024 18:24:20 GMT  
		Size: 54.5 KB (54511 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:da8565a5f24798a7cb63b4b32bec728442aa650045dd211e3ea8c5d30e4fd0de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (144002999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15232c26ecbfb7cb3394e0cea7a65d9688cbd4c558fd70c505a0e8b23148abe9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:44:17 GMT
ADD file:9ca492786bcb3648d90c47fc2dba3c8239eea7a0689f6a17ee25a9f5129aabd5 in / 
# Thu, 09 May 2024 18:44:17 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV PG_MAJOR=15
# Thu, 09 May 2024 18:44:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 09 May 2024 18:44:17 GMT
ENV PG_VERSION=15.7-1.pgdg120+1
# Thu, 09 May 2024 18:44:17 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:44:17 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:44:17 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:44:17 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:44:17 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:44:17 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d50583018de0ccbb239bef29dd375ae0ea018644d67a37b4fc29bec08b3b1a33`  
		Last Modified: Thu, 13 Jun 2024 00:51:38 GMT  
		Size: 26.9 MB (26909975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76f93fe24faf9bdd2823e7ed0fa9bf1ae89c6d82d81309c0044fbd05c272b8b`  
		Last Modified: Thu, 13 Jun 2024 20:27:17 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2160d7118cc9f8e23b3033ea807d4e87947c45bfb8bcea73028027aa765329`  
		Last Modified: Thu, 13 Jun 2024 20:27:18 GMT  
		Size: 4.2 MB (4150952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5efce1143a2d44abdd1810dd3dfeb14c4ee36f79dc41476601665c7c40a2f54`  
		Last Modified: Thu, 13 Jun 2024 20:27:18 GMT  
		Size: 1.4 MB (1427070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e623323d67613018c639686712853eb77cd588d64ced98a25fd20512f43b1e6`  
		Last Modified: Thu, 13 Jun 2024 20:27:18 GMT  
		Size: 8.1 MB (8068972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee6b3c3492fbdef9666e4379393f2c59aff2ab2278dcc38c611ebe869696083`  
		Last Modified: Thu, 13 Jun 2024 20:27:19 GMT  
		Size: 1.2 MB (1194853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58d2e67789ab63ba29790eec6bd56fe19d33551de322ceaa5f0bbf489a10b4f`  
		Last Modified: Thu, 13 Jun 2024 20:27:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e906e2ab7c56d77757417a3a48d2ba73236b668f3ef3ffe2788196fea729bb`  
		Last Modified: Thu, 13 Jun 2024 20:27:19 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f437fa9c158732de9f7bf6994ab039bf69c6a3827501ba5eb1eba3f3e5091c31`  
		Last Modified: Thu, 13 Jun 2024 21:33:10 GMT  
		Size: 102.2 MB (102231066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e501ba5c688423dfc8642edaa65b615fb83ac61274a02dc025f8b95eaeabf65`  
		Last Modified: Thu, 13 Jun 2024 21:33:06 GMT  
		Size: 9.8 KB (9783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa34a5fa2cb0da7f7cf11b73ecf0d16cabb4e499557382242b89365663c71198`  
		Last Modified: Thu, 13 Jun 2024 21:33:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8aafea27f1bff70c0c080b86d942d804c923b2c9ba70d8f30bb8005e1257958`  
		Last Modified: Thu, 13 Jun 2024 21:33:06 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ee063925f45e92e646a16bad57aeb7f01c87c3efac3606658a0443564e5047`  
		Last Modified: Thu, 13 Jun 2024 21:33:07 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788c82ea3c30168f67bb867d17df870716ace3bcd397a4e30d3618aaf297cbec`  
		Last Modified: Thu, 13 Jun 2024 21:33:07 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:1900629fc35a6c34cb0e75726d14fe287334a0cf9f84de2551d4bfbbc021cfe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5721342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd9b52b69f6af993693055edb9657bab8e625895c5acee56cf5d2f067cca6039`

```dockerfile
```

-	Layers:
	-	`sha256:7a9895b719b1205c2a7d7492ce8c34cec9401a4982594cac0f43bf8fe6d1305d`  
		Last Modified: Thu, 13 Jun 2024 21:33:07 GMT  
		Size: 5.7 MB (5666618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be1df7f271b478aa89443bb48c387e071562c117ed9e1c39149e99368e41c0eb`  
		Last Modified: Thu, 13 Jun 2024 21:33:06 GMT  
		Size: 54.7 KB (54724 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:ee619f7119f6fda8ec30f35524b0f83861d5020323925918c7dd0d18a20ebe0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138750699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2856c0780b6980691b6bc192f93dab5a2c5b22c2cd463f9650464f4b8e468267`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:44:17 GMT
ADD file:4c737c0a5e5b59fcbe2bc42dca815263159a1e1d16789ebeee086933aac4649a in / 
# Thu, 09 May 2024 18:44:17 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV PG_MAJOR=15
# Thu, 09 May 2024 18:44:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 09 May 2024 18:44:17 GMT
ENV PG_VERSION=15.7-1.pgdg120+1
# Thu, 09 May 2024 18:44:17 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:44:17 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:44:17 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:44:17 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:44:17 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:44:17 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:12af5edb53b85c10582c3e3d437561cc626437f48928a30456a99941d87706e3`  
		Last Modified: Thu, 13 Jun 2024 01:01:38 GMT  
		Size: 24.7 MB (24740215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493051253236caea97f219fd70aa5f22f8b46248ff1d3c3d3188d73ce0784a40`  
		Last Modified: Fri, 14 Jun 2024 01:16:01 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6804256b124e139d9f0115e1d42291cc23b80dce76de35fd5698c162eaf1dbf0`  
		Last Modified: Fri, 14 Jun 2024 01:16:01 GMT  
		Size: 3.7 MB (3742521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b531feac03289045c14b775e7e96c3ede9f3a2d05e3b6dd1e733009cf1bbb62`  
		Last Modified: Fri, 14 Jun 2024 01:16:01 GMT  
		Size: 1.4 MB (1417097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66c7bb29e6b93b045ad24872cfa94249282a9726a9f006f38918a121c5ba9be`  
		Last Modified: Fri, 14 Jun 2024 01:16:02 GMT  
		Size: 8.1 MB (8068841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b345cb504203c27252fd77886ea537ccbba6a85470442aae2a7829f01b742d27`  
		Last Modified: Fri, 14 Jun 2024 01:16:02 GMT  
		Size: 1.1 MB (1066956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d104bf8bcc118bb31c29d3d8a68c778d2cb3ff3581269130a6cdcbe82a263ed7`  
		Last Modified: Fri, 14 Jun 2024 01:16:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe06d964e32afda897c71c4829462b2d98aa14cf05e4ce8a1821876e9adb65c`  
		Last Modified: Fri, 14 Jun 2024 01:16:02 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34fb09a0b130c34b3c828039ec97acf3846364e4552242b461df11ad6870f01a`  
		Last Modified: Fri, 14 Jun 2024 02:17:09 GMT  
		Size: 99.7 MB (99694955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c9b4a0ffc9d92790924736f83b270a258e2dee11b5e2784e9efe683c5a325e`  
		Last Modified: Fri, 14 Jun 2024 02:17:06 GMT  
		Size: 9.8 KB (9785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58f2cbb266aca9abf5e409317d8327209b048814dddfe8270b2257421e96bc4`  
		Last Modified: Fri, 14 Jun 2024 02:17:06 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc55aa1bb80c813d63e006a732a31edf5e48ea08c363a2d639e72cb4a8dc1cc`  
		Last Modified: Fri, 14 Jun 2024 02:17:06 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc6943c6b7be79bf7a772a849cb6d33f3ac9ac571fe613ee63adbc706a34742`  
		Last Modified: Fri, 14 Jun 2024 02:17:07 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94cd8082451b52316983e557908981d725085c9c4b01de9a40a94d4c448fc6bc`  
		Last Modified: Fri, 14 Jun 2024 02:17:07 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:fa3333c3e9e5ae37c85dedbd5907a5a087240fa4b2bfdf7958758238bf2a0159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5721148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:945c4dc494951397c1d94cf8d1f193252707503509ae54b58668506b33a1d74f`

```dockerfile
```

-	Layers:
	-	`sha256:01603e4bf5f9eaa8a01ffdb1b92763b983734b457753911dc46b7d7d90f46101`  
		Last Modified: Fri, 14 Jun 2024 02:17:06 GMT  
		Size: 5.7 MB (5666430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfc7ee98b1e516be746b370ff109f4531d0aac7f038d7c5618859d69f5354e32`  
		Last Modified: Fri, 14 Jun 2024 02:17:05 GMT  
		Size: 54.7 KB (54718 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:5417ff67fa8c1d593987d75347f47f2a376d9937baca43490168aefa2d4e44dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.5 MB (149535512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f67bbaee4b1402186c33c9dc4a1f9967cf5717ae905115e27833d07956a25aa8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:44:17 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Thu, 09 May 2024 18:44:17 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV PG_MAJOR=15
# Thu, 09 May 2024 18:44:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 09 May 2024 18:44:17 GMT
ENV PG_VERSION=15.7-1.pgdg120+1
# Thu, 09 May 2024 18:44:17 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:44:17 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:44:17 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:44:17 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:44:17 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:44:17 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059b5c43db4127d3c84a4caee54092e336d3ba62e208c915e1644fb73a7c5e2f`  
		Last Modified: Fri, 14 Jun 2024 00:40:58 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac4aa6c99e9f11007d4c9ef96a1b0dd6aa1ba9b32bb8f1eed1577047f513928`  
		Last Modified: Fri, 14 Jun 2024 00:40:58 GMT  
		Size: 4.5 MB (4499134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f695f6dafe22ec09a8d465915c3f2df31da965a38406fe775765c9a6d6e5af46`  
		Last Modified: Fri, 14 Jun 2024 00:40:58 GMT  
		Size: 1.4 MB (1382260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3531e6d72caa83e1e23ae04b0c519b1174a47e2c737f6f4bf8e2822a9acae84c`  
		Last Modified: Fri, 14 Jun 2024 00:40:59 GMT  
		Size: 8.1 MB (8068931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8460f5c0f01056e728f9f916df72baeae6eb09bf8e6c86f8964a9822b8008cb5`  
		Last Modified: Fri, 14 Jun 2024 00:40:59 GMT  
		Size: 1.1 MB (1108679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c419f8ddd2fbd2e547a8b11791240d264a925a69a36bc442567489c2755fd853`  
		Last Modified: Fri, 14 Jun 2024 00:40:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54f6c55c74f6700f1cea329574b215d9662b08548c98081dabb64ac7caffaf8`  
		Last Modified: Fri, 14 Jun 2024 00:40:59 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd6fd21148dd25e5fde6691bee6dcb9e47f3ac023c99c69790cd31aa8adf365`  
		Last Modified: Fri, 14 Jun 2024 00:56:07 GMT  
		Size: 105.3 MB (105276739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78bcf256d9929e8fbde12bb419b8d91dba60160a60012ca3f39c86e0778bf491`  
		Last Modified: Fri, 14 Jun 2024 00:56:04 GMT  
		Size: 9.8 KB (9780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833883e73286cdc1eaa115e4fe5ba3d3b32d34f793f0644899b0bc6ef892f636`  
		Last Modified: Fri, 14 Jun 2024 00:56:04 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2d90bec67409ab7b2e5a7289b280a3524e6ae99b334bc5ef95aa4872fcfc9e`  
		Last Modified: Fri, 14 Jun 2024 00:56:04 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b62a4a71e1cf40b7a30461fcbffd76e680d116217d1dbe8c9a5e2498d28a97`  
		Last Modified: Fri, 14 Jun 2024 00:56:06 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c34f45f552cfc52fc180fa9433d428c3750859e1390f334cc5752750e1053c`  
		Last Modified: Fri, 14 Jun 2024 00:56:05 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:f8e2b37e5eae5191298c4c961346b6ff51c4a63aa5a2036a9f8161585b51b026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5716355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec9b1ef27715d9b7752a31f5aca12bdbb38fab7aa621658efb08ee686534954`

```dockerfile
```

-	Layers:
	-	`sha256:8b188d91bcaa43372e8beda83925279cd9f6acc0c72397b6b6353eef915d770c`  
		Last Modified: Fri, 14 Jun 2024 00:56:05 GMT  
		Size: 5.7 MB (5661535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d04df55a2c6efd640c2583e1fe06667a421974cb489c890b9eca8655e5d821f6`  
		Last Modified: Fri, 14 Jun 2024 00:56:04 GMT  
		Size: 54.8 KB (54820 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:393ec2880fd4455066b08715d1c2133a5bcf80b0d771c6e9eeea6a49bc189357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159335149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccb6cd165048618fe66166001e6cbe331c8303297f6537600314fe3b3dd486b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:44:17 GMT
ADD file:d68e899424fb360eaf2a6f2f35e06dc87f5841c13cce853d3e0710f969583d10 in / 
# Thu, 09 May 2024 18:44:17 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV PG_MAJOR=15
# Thu, 09 May 2024 18:44:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 09 May 2024 18:44:17 GMT
ENV PG_VERSION=15.7-1.pgdg120+1
# Thu, 09 May 2024 18:44:17 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:44:17 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:44:17 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:44:17 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:44:17 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:44:17 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7adb06274fdba91ff3ec0873bc068b9a785bd5e3ff48e6f1d9e855048f1f0a66`  
		Last Modified: Thu, 13 Jun 2024 00:43:23 GMT  
		Size: 30.2 MB (30162659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707c40cf0f45050a4e226089a3065a81f0c5dc80c0d3e02fb39bdd1c7d0a606f`  
		Last Modified: Thu, 13 Jun 2024 02:14:02 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e846f16d11b89dab9919a97405fe1dbf56234967531cdf13c951b733135fcc5e`  
		Last Modified: Thu, 13 Jun 2024 02:14:03 GMT  
		Size: 5.0 MB (4965013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153d4e557c47445eaaea8d113f3bf64e4073d31930a1b6b07777141a8f4c6912`  
		Last Modified: Thu, 13 Jun 2024 02:14:02 GMT  
		Size: 1.4 MB (1425567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda0cbf2bda07017f0ff847355ef90783e98c6a80b06260a43e6b8a004071d6b`  
		Last Modified: Thu, 13 Jun 2024 02:14:03 GMT  
		Size: 8.1 MB (8068913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07230f98fc54aec4909710187467b79be8f76ec5cc43740c5916e8801fe1e2ab`  
		Last Modified: Thu, 13 Jun 2024 02:14:03 GMT  
		Size: 1.1 MB (1137138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2effa40444a8a115fc63e24f248990aa7ed0136f2ffa92fdc6b50ad32eba04d2`  
		Last Modified: Thu, 13 Jun 2024 02:12:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9902fb69ed7f544415e5720b8138b494536c29663883681aed28e93299df381c`  
		Last Modified: Thu, 13 Jun 2024 02:12:16 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d8e7d744a9d63e8b5aee0e72c8802167cd02f160357c7459cce8e283441321`  
		Last Modified: Thu, 13 Jun 2024 02:14:07 GMT  
		Size: 113.6 MB (113555748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c7cd80ff012ffa5664be3537773b37c2a332b2f25c1818dba567049fdd956bd`  
		Last Modified: Thu, 13 Jun 2024 02:14:04 GMT  
		Size: 9.8 KB (9786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f24aa164296eacbbfc61599c22ecb7ffb89e9bd77aa00cbbb54d9d9b3a81d2`  
		Last Modified: Thu, 13 Jun 2024 02:14:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6fe754b44940b76866d883777aeb7e233759eeaa8ded8e847f9a58cf5b4f38`  
		Last Modified: Thu, 13 Jun 2024 02:14:05 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827906b167968f69d8945a6a309b82c1dcca89155e8e029f899b491f4aea2bcc`  
		Last Modified: Thu, 13 Jun 2024 02:14:05 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a871def6e9552eab2e806e12bf43267dc2f77453633a9829cd47985f237a252`  
		Last Modified: Thu, 13 Jun 2024 02:14:05 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:e3bf460867df69d8a7f5fd7006bf4da131fde4810feeae7627711eb0eb509ac6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5719131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df95455b2bbc256e1c4b35c7bca92676c78230befe9b92c991d339d10dd97fd5`

```dockerfile
```

-	Layers:
	-	`sha256:d6408e9c0ece56e242d644a7e80eaa2d22a8b8444871458bb06a9659cd983c0a`  
		Last Modified: Thu, 13 Jun 2024 02:14:03 GMT  
		Size: 5.7 MB (5664671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e36b11f14c2f7e56016ada8cc0ca87f5c720e4724ea82d181a59e4869e237632`  
		Last Modified: Thu, 13 Jun 2024 02:14:02 GMT  
		Size: 54.5 KB (54460 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:e625ea5d325b29ae9ef6fe51592fff0483229428759c2975b4b2bc26454dc1b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.7 MB (146690920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66f0185d964e45c1f349ab55535fd551e05f4450fc185aa034a286f6543abc6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:44:17 GMT
ADD file:a92da94a28279478b2eae11dcdcd2913fc06af02498a5515cc3f288668d74e43 in / 
# Thu, 09 May 2024 18:44:17 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV PG_MAJOR=15
# Thu, 09 May 2024 18:44:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 09 May 2024 18:44:17 GMT
ENV PG_VERSION=15.7-1.pgdg120+1
# Thu, 09 May 2024 18:44:17 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:44:17 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:44:17 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:44:17 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:44:17 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:44:17 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6ccc6628d3cdcda935b3b60cb54fa578d669965454d9cf39de3df9c1276132b7`  
		Last Modified: Tue, 14 May 2024 01:22:19 GMT  
		Size: 29.1 MB (29143688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee99d44e1a2a38d3f0ea99728eb5d543f3a58d4f87764d7b6d8c5d4dcd60c3a`  
		Last Modified: Wed, 15 May 2024 06:13:06 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6001f74096b78911bc028b40ebb35a3333ca2508a3305350118f5a8f47823670`  
		Last Modified: Wed, 15 May 2024 06:13:06 GMT  
		Size: 4.5 MB (4475100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdee96ab4aa2f94d2b0fd6fe42b0d9d3d751a8a7c0648a33822d3b6e6d31e56a`  
		Last Modified: Wed, 15 May 2024 06:13:06 GMT  
		Size: 1.3 MB (1337130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff34223f28c6fc17569c01dffe96ebebfccd831a35e0fd4b363a54a465c62c5f`  
		Last Modified: Wed, 15 May 2024 06:13:07 GMT  
		Size: 8.1 MB (8069077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa5c61838f2b740e18249c538f25d78abda6e100a964c461baacdf2f55c763e`  
		Last Modified: Wed, 15 May 2024 06:13:07 GMT  
		Size: 1.2 MB (1182639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d7d9e782f2e6fbe180afc7afea7a2e7f94a05356a95478ee2d2a539a534b07`  
		Last Modified: Wed, 15 May 2024 06:13:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bacd64a9f9782260675c34cbcf4057aeff92b035c40ee4bde29eb899991b864c`  
		Last Modified: Wed, 15 May 2024 06:13:08 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116806766233dd9557f1a782b4250e9796064879e27afeaaf4fc8e9750c238cd`  
		Last Modified: Wed, 15 May 2024 08:33:49 GMT  
		Size: 102.5 MB (102463175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5d349514d1ec19ae4e0b545e2900072a64ee5815fe4f3b92d2e2818df4ed47`  
		Last Modified: Wed, 15 May 2024 08:33:39 GMT  
		Size: 9.8 KB (9785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d90ba1730f2afb46b12777bb66b278a512f3bcca63cf70919b483320318f5f`  
		Last Modified: Wed, 15 May 2024 08:33:40 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae2cf02946fa17dcec0b9867067d689b25b51f6972ee2ca79cfd18fd2eea51c`  
		Last Modified: Wed, 15 May 2024 08:33:39 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4c4cead265c97d44285b79833a8b8ee01fdae81c1734a7e887ba62366448eb`  
		Last Modified: Wed, 15 May 2024 08:33:40 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134a33513862280c8bffdcd81351bca14d83bc36a94b58ddb75b7f20361fcbd0`  
		Last Modified: Wed, 15 May 2024 08:33:40 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:fc5107ffd7e6d851addda485ab77251f2fde0569fe088fa6fe735f907e9143a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 KB (54333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa11df0afc9fe5af5b4f5220ce496138467a834c9ae4dd32d68d05442b29a8d`

```dockerfile
```

-	Layers:
	-	`sha256:1a6f33671917e489f6cd7de24f3172d24e28944d518f41451be924455604abb8`  
		Last Modified: Wed, 15 May 2024 08:33:39 GMT  
		Size: 54.3 KB (54333 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:1093dd5c0b02f4decbc33f95b2b3844d994b699c890e01d46859514ac36a3d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.5 MB (163487322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6c2b63fec34a7c7907fd2809cb71702c881d825bd1753b3747f28632b7fc4bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:44:17 GMT
ADD file:26d639147c70c8e3b876ab5c2950b7b7e7c654b878e69cf7a82a7cbdfdb31024 in / 
# Thu, 09 May 2024 18:44:17 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV PG_MAJOR=15
# Thu, 09 May 2024 18:44:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 09 May 2024 18:44:17 GMT
ENV PG_VERSION=15.7-1.pgdg120+1
# Thu, 09 May 2024 18:44:17 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:44:17 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:44:17 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:44:17 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:44:17 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:44:17 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c4f33295caca163b437a6dc1ad770a1f2d84b4d5e78e832bbe0fb2f064aeccfd`  
		Last Modified: Thu, 13 Jun 2024 01:21:30 GMT  
		Size: 33.1 MB (33141195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ce3d2e2dd26ed2ee971fce30509b03a268266ef6661c37ab01b06aaea977a2`  
		Last Modified: Fri, 14 Jun 2024 04:50:50 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0b107b67b75a99675cecac40b78e0a03b27dc41c4e72a49011d730ff9a626f`  
		Last Modified: Fri, 14 Jun 2024 04:50:50 GMT  
		Size: 5.4 MB (5368230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b29592030092edd9c2d4f6377bb04280475e56b1a15e8a23fe33476cdcccfba`  
		Last Modified: Fri, 14 Jun 2024 04:50:50 GMT  
		Size: 1.4 MB (1371299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758aab932f37bd7ede2c247f8f364e06293cf29a6abf480c14c410dac0022d26`  
		Last Modified: Fri, 14 Jun 2024 04:50:51 GMT  
		Size: 8.1 MB (8068982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f494893d635f3afc4b0d6f82c1b3c1e22012e631b18d4efdf8b212308cbdce3`  
		Last Modified: Fri, 14 Jun 2024 04:50:51 GMT  
		Size: 1.3 MB (1283497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430ea084ff79461737d3396dad9f8b949252d1052c00c14b93f7f10986c8792d`  
		Last Modified: Fri, 14 Jun 2024 04:50:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f6a3290a408bdea48295cf53e8024a783f6f98f692b9240df81035056e3a07`  
		Last Modified: Fri, 14 Jun 2024 04:50:52 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9366e2eba0dfd043b9a747b6073e58f524a77e06f6ce061fb09b805d4b525f58`  
		Last Modified: Fri, 14 Jun 2024 04:57:51 GMT  
		Size: 114.2 MB (114234006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4cfb8a1cc5d9004af2186260e071725f4aef6385327d4226d1d6ae9b8d9c9f`  
		Last Modified: Fri, 14 Jun 2024 04:57:47 GMT  
		Size: 9.8 KB (9780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319a651fbb8a9e018aa7bc0851071e1665f65370715576d7682220ffd1e01dea`  
		Last Modified: Fri, 14 Jun 2024 04:57:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d148dcbe890f5ef6d3b4116ea64c1a5b4b46b62020f73bd96288b5353c6d6e8b`  
		Last Modified: Fri, 14 Jun 2024 04:57:47 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52875b9a0c00262bfda41bcc5ef75830021556e69f0de70912fa13a66f929e14`  
		Last Modified: Fri, 14 Jun 2024 04:57:49 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131a12bf097826fdf50cf41982b7b9650a709b5fddaab45d043aa41c1bfc16a1`  
		Last Modified: Fri, 14 Jun 2024 04:57:49 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:30bd24dba71972ec79e47ffdea1908fc6551cf81942b8875fc8e269ac9924a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5716994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f98b58836a56430db89c442b1016a29137b25f702d7891bcb59c9e86f860e84`

```dockerfile
```

-	Layers:
	-	`sha256:c6b64a9f891e7939fd6678a7b7a2874969773d25c83f344d9cc2c1d41282204b`  
		Last Modified: Fri, 14 Jun 2024 04:57:48 GMT  
		Size: 5.7 MB (5662423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04971879c2f5dea1b695415673bd8a5aacebbf76d7d262e4623a00c71fad9fe0`  
		Last Modified: Fri, 14 Jun 2024 04:57:47 GMT  
		Size: 54.6 KB (54571 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:4aa03beb790b121fb3970e9ee1aac7545ae422d2cda72f45f3dd8f499340faed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.8 MB (156836246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83aea2a5ee079f69ebb8fa76201028ac9ddc4957e73ad6c754998838cdffe7cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:44:17 GMT
ADD file:e4d9e24430546fda3cf8c73efdaa45b6bf1014a23d4d3c0247fe341b3ee9212a in / 
# Thu, 09 May 2024 18:44:17 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV PG_MAJOR=15
# Thu, 09 May 2024 18:44:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 09 May 2024 18:44:17 GMT
ENV PG_VERSION=15.7-1.pgdg120+1
# Thu, 09 May 2024 18:44:17 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:44:17 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:44:17 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:44:17 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:44:17 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:44:17 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:06561002b4f942b877c60f94bd44315c2e0580cc0ae30f060660bdbcdae21d6e`  
		Last Modified: Thu, 13 Jun 2024 00:47:43 GMT  
		Size: 27.5 MB (27512459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df718a21529484d825e8d34c404257a0546286e7a7caaafa5e6aa3c284858359`  
		Last Modified: Thu, 13 Jun 2024 12:22:12 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab19acd660b1d3121eadb9baf4f00251f6bad0be1f21e5546e9a7bbdf7c25f0f`  
		Last Modified: Thu, 13 Jun 2024 12:22:12 GMT  
		Size: 4.4 MB (4391035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec53b5378db13907773971770802e5cd432e139b9ca53f853835ada5cff2134b`  
		Last Modified: Thu, 13 Jun 2024 12:22:12 GMT  
		Size: 1.4 MB (1415933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f148609caa08348b01404906d68e5fac6a87cf8be9296e80c1478c47b119a32`  
		Last Modified: Thu, 13 Jun 2024 12:22:13 GMT  
		Size: 8.1 MB (8123196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4a29b13525c5cab1218d23d20c299a8d1311c5619fb9a8586f2cdba6ec7dda`  
		Last Modified: Thu, 13 Jun 2024 12:22:13 GMT  
		Size: 1.1 MB (1096730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b9b3dab45f719c1cfa9a9942b491b3d6577a1e12d3c44ec54edb4ba4bf475c`  
		Last Modified: Thu, 13 Jun 2024 12:22:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce605bd25ed1e30eab9e389d318038b16d3f7fea277774f1e329cce643e81f83`  
		Last Modified: Thu, 13 Jun 2024 12:22:13 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c910b25ec502cecfd618fc131d97b030179dc52ed41824a6db0b32fe64a92330`  
		Last Modified: Thu, 13 Jun 2024 12:29:30 GMT  
		Size: 114.3 MB (114276787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5bf9263dc8472861841ed45124b00a3c7c848c041ddbbf65d099199a11de98`  
		Last Modified: Thu, 13 Jun 2024 12:29:28 GMT  
		Size: 9.8 KB (9782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bffef2b322ca2c3ed575b5c38cf23d45b46dd20ddba11329bb4d8740d82e29ad`  
		Last Modified: Thu, 13 Jun 2024 12:29:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de549eb1821d795432b1d41b817f5a250d5d1279aa1f4b5e6b7abf9f6822f8ed`  
		Last Modified: Thu, 13 Jun 2024 12:29:28 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28c3e93765808b7fcf432ab0ec4cd30b60d2095887146211d7b4426c12510bc`  
		Last Modified: Thu, 13 Jun 2024 12:29:28 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e190ce517c3d3b273e8b94072021fdb583d84559e62c49e8db2a3df1316056`  
		Last Modified: Thu, 13 Jun 2024 12:29:28 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:3a5682ed8c27904e8454bc674ef9b8b537dd2ca8558afe3c915aa253a7f9b271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5709099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85673ba6773061c20998c7c1b55e4933d2e3a87f1601c8249ee1100873e7efc`

```dockerfile
```

-	Layers:
	-	`sha256:14a7301c11f305749b33e1e47e4e08c85bdb2045905ab842de7120efbdead545`  
		Last Modified: Thu, 13 Jun 2024 12:29:28 GMT  
		Size: 5.7 MB (5654588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ecb6708e473c74f60e81c7610720e10942738c79555a9219d2ef001793280b6`  
		Last Modified: Thu, 13 Jun 2024 12:29:27 GMT  
		Size: 54.5 KB (54511 bytes)  
		MIME: application/vnd.in-toto+json
