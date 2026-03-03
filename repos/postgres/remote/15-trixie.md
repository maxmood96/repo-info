## `postgres:15-trixie`

```console
$ docker pull postgres@sha256:f30e3de0ac9cc938dac627ef2231099867c694b5f949fadb924c8c977428c399
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

### `postgres:15-trixie` - linux; amd64

```console
$ docker pull postgres@sha256:ae94f99e5e8b250260ba89e2b04a54d85ece7aa942a161c2994f38ecd06aa6d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.0 MB (158034412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d743cd41504b6e2a0699afb9af94eac4403e7b93a60b06fa92d9ef5732d06d58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 19:28:26 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Feb 2026 19:28:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 19:28:38 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Feb 2026 19:28:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Feb 2026 19:28:42 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Feb 2026 19:28:42 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 19:28:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 19:28:45 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:28:47 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Feb 2026 19:28:47 GMT
ENV PG_MAJOR=15
# Thu, 26 Feb 2026 19:28:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 26 Feb 2026 19:28:47 GMT
ENV PG_VERSION=15.17-1.pgdg13+1
# Thu, 26 Feb 2026 19:28:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:28:59 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:28:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:28:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Feb 2026 19:28:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Feb 2026 19:28:59 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Feb 2026 19:29:00 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:29:00 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:29:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:29:00 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:29:00 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:29:00 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c725cebedaa00ec3d975dd5e1453f659c0f599c3e324318379dd1a4a2273f15`  
		Last Modified: Thu, 26 Feb 2026 19:29:19 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2358c04556d27e9d10599383e0193c761a13a288ad367d4d31708f9110d9016`  
		Last Modified: Thu, 26 Feb 2026 19:29:20 GMT  
		Size: 6.4 MB (6441232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae50de223a45f3df86cd785ae3f9a18359061d1ec28349edbafec22b9111af2`  
		Last Modified: Thu, 26 Feb 2026 19:29:19 GMT  
		Size: 1.3 MB (1256766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6de334a9157f5020718f0969132397c3216b4f3d789f0aaa3b8f43efbc4948c`  
		Last Modified: Thu, 26 Feb 2026 19:29:20 GMT  
		Size: 8.2 MB (8203783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67266521af9d5dff09b9a9cb09599c8a0cde1c2af916339a67f8ef4f9647bee1`  
		Last Modified: Thu, 26 Feb 2026 19:29:20 GMT  
		Size: 1.3 MB (1311630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd349cbbb730f35b75e2d37c1173407ddc072644eb0f28d1e7a151173352bf2a`  
		Last Modified: Thu, 26 Feb 2026 19:29:18 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b480546e671bc553c90c7e9a27a1876a602bcc49fb44d133a8b0451b0e8e7116`  
		Last Modified: Thu, 26 Feb 2026 19:29:20 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9526eade8e14a14e5207714f9da987d0091cb6710e156e2b8211d8264ca6b7`  
		Last Modified: Thu, 26 Feb 2026 19:29:23 GMT  
		Size: 111.0 MB (111021737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8ddeccdf2d28a0aff9fa5a6bc103ecfa6ad0c72dc561a9f0575c231d5e48ee`  
		Last Modified: Thu, 26 Feb 2026 19:29:21 GMT  
		Size: 9.9 KB (9878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c010f1448fe4810c684c4a3adea7b77c9382786f723bbb215b219ea65fe286`  
		Last Modified: Thu, 26 Feb 2026 19:29:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f080c6a4c94ccbedf21bff7a4f83c894c30ecb1bfe35950f7f6ff21ca9aec203`  
		Last Modified: Thu, 26 Feb 2026 19:29:22 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01de8c32e6c7d16be18d8c981f1d55694cd199d16bc98cf0c93f04721389d31`  
		Last Modified: Thu, 26 Feb 2026 19:29:22 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e180f475c84dacae62f92df5d2b78fd1d084d311c31cd773e999a155389b231`  
		Last Modified: Thu, 26 Feb 2026 19:29:22 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:4996089ce62d94c70940a27edefd4a55e8daf12769187912731e3893791b92b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5696380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f626897a7352730db8a042d609f9468166745c8d3a5e0728a12b2f022e99ae`

```dockerfile
```

-	Layers:
	-	`sha256:0ec1a9a918373c0058739e149facfccaba8f67ea33ab821e0e440f36daaba1a6`  
		Last Modified: Thu, 26 Feb 2026 19:29:20 GMT  
		Size: 5.6 MB (5642516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a34778c227a8138371ef73e5473489084fb7c18f0e7963d52c5b75ef5460440`  
		Last Modified: Thu, 26 Feb 2026 19:29:19 GMT  
		Size: 53.9 KB (53864 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; arm variant v5

```console
$ docker pull postgres@sha256:a616fa56a4dd979bf92f4f1607adce62d3fc45517258665544b69c2cfa58588c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152080556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d9aaad1e860929b7ef7add35af2ce0fc3398c701de83bb39e5223743869011e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 19:15:51 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Feb 2026 19:16:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 19:16:13 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Feb 2026 19:16:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Feb 2026 19:16:21 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Feb 2026 19:16:21 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 19:16:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 19:16:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:16:29 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Feb 2026 19:16:29 GMT
ENV PG_MAJOR=15
# Thu, 26 Feb 2026 19:16:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 26 Feb 2026 19:16:29 GMT
ENV PG_VERSION=15.17-1.pgdg13+1
# Thu, 26 Feb 2026 19:45:45 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:45:45 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:45:45 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:45:45 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Feb 2026 19:45:45 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Feb 2026 19:45:45 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Feb 2026 19:45:45 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:45:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:45:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:45:46 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:45:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:45:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f659b68534a399b6c2ec6cad7e375b54c5f1396df8bf0ba0f17bb2abc9e14af`  
		Last Modified: Thu, 26 Feb 2026 19:29:50 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f2339590d8a7345ac971defc97ef20d1a7e2e21af5445151fc2719a98ed5fb`  
		Last Modified: Thu, 26 Feb 2026 19:29:50 GMT  
		Size: 5.9 MB (5932418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d342497ab0886c49e45ae30397b71bcceec4cbdd3c5194b8a0d90f3ff07a8a2d`  
		Last Modified: Thu, 26 Feb 2026 19:29:50 GMT  
		Size: 1.2 MB (1227515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80538fd2c25ae5b4c6604999d9b6b3d90e2c24cd57d7235eeab03e073f71c3c`  
		Last Modified: Thu, 26 Feb 2026 19:29:51 GMT  
		Size: 8.2 MB (8204272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1539e11634098169d4c37a30365fbc976e8b67ec9903f3ccb9045b0957812d`  
		Last Modified: Thu, 26 Feb 2026 19:29:51 GMT  
		Size: 1.3 MB (1317346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f49a617cd6ef8e5a9ce60302957ed655c110de09d5d659352db865c8c4aa15d`  
		Last Modified: Thu, 26 Feb 2026 19:29:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b76a378fa77bca080dc9ab300cf70f63e40e94727728e18d3c298b54bd435a`  
		Last Modified: Thu, 26 Feb 2026 19:29:51 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5d8948170873b0432853d968d1a5cbe69feabd4f584617e704c41833124292`  
		Last Modified: Thu, 26 Feb 2026 19:46:07 GMT  
		Size: 107.4 MB (107430759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa5722fd1a4977ad62d7ca3e8c6b2b26e4d3624527518bf4edd116684578325`  
		Last Modified: Thu, 26 Feb 2026 19:46:03 GMT  
		Size: 9.9 KB (9882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443418c7425714338ba9b48541d8e614294721c89529e430db071625d12eff89`  
		Last Modified: Thu, 26 Feb 2026 19:46:04 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9d67ef463de55fc45dfccee661acb28d2e3c4281b143053c0b1d91c7131bc4`  
		Last Modified: Thu, 26 Feb 2026 19:46:03 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4725bea65ba01fcaa6762e078d47d16bb55a5a029bfa25a708ee2c7037a7ad5b`  
		Last Modified: Thu, 26 Feb 2026 19:46:05 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c196d4c216b9b6268c2b8d2a8d28a83b4eebaae727ffcb68d5c1a01ec15862`  
		Last Modified: Thu, 26 Feb 2026 19:46:05 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:2ab2546ba2be6da33aa2552ec083c6a0b00038886743ad4d2dc1f93d3d9f6f86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5713240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e99a9e45395e7a4dffcb87bc02af0816f374696f89c298cef7236f07bdd4878`

```dockerfile
```

-	Layers:
	-	`sha256:21c825c25e18ec71ab50c17528b654924004d2af8e893d6b7d4ed999dd89dcae`  
		Last Modified: Thu, 26 Feb 2026 19:46:04 GMT  
		Size: 5.7 MB (5659154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e6446817f9685e569eb131281304306f91bf11b28e601781e7a5036822bb906`  
		Last Modified: Thu, 26 Feb 2026 19:46:03 GMT  
		Size: 54.1 KB (54086 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; arm variant v7

```console
$ docker pull postgres@sha256:a0a3228dd0660fd21b7b41796bea3a5c51b56c9b4939b50fed53f03b141aa5ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.1 MB (147136675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bb27daea1a06cb4285d5d057ebfd18125f9089ebff4266da5db3a836fd4b909`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 19:40:30 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Feb 2026 19:40:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 19:40:46 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Feb 2026 19:40:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Feb 2026 19:40:53 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Feb 2026 19:40:53 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 19:40:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 19:40:58 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:40:58 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Feb 2026 19:40:58 GMT
ENV PG_MAJOR=15
# Thu, 26 Feb 2026 19:40:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 26 Feb 2026 19:40:58 GMT
ENV PG_VERSION=15.17-1.pgdg13+1
# Thu, 26 Feb 2026 19:55:09 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:55:09 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:55:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:55:09 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Feb 2026 19:55:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Feb 2026 19:55:09 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Feb 2026 19:55:09 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:55:09 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:55:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:55:09 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:55:09 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:55:09 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2982733f90392b07723bc8a1a4ce2fb1131e64c8d7ee55cad0a7ee773dcd253c`  
		Last Modified: Thu, 26 Feb 2026 19:55:27 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ce504174bfe8041c5996d6093a5e00975cacb5dd07f681270ec6515c673f85`  
		Last Modified: Thu, 26 Feb 2026 19:55:28 GMT  
		Size: 5.5 MB (5496564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f9ddf58367beaa76de922bae1ff69ef41b4f46730aa54e456bc93cc22b19bf`  
		Last Modified: Thu, 26 Feb 2026 19:55:28 GMT  
		Size: 1.2 MB (1222374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf844de0f4e1465d029df6ae1a10d4ff77c5fcf1c7bb631ccbeafa259a526ce4`  
		Last Modified: Thu, 26 Feb 2026 19:55:28 GMT  
		Size: 8.2 MB (8204003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3baf879f1a04e0991a4f5873f4727862bf6097b776137bf0d81a978a8f9f5d96`  
		Last Modified: Thu, 26 Feb 2026 19:55:29 GMT  
		Size: 1.2 MB (1172594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655d121eb8ca16b93a25f904f49a10d41e8d924e3a625f31ed76c716aa27f187`  
		Last Modified: Thu, 26 Feb 2026 19:55:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b299f694bb63cc2c8818c1cd5211e8fde17226a0dafbe0450019d1b069beb0`  
		Last Modified: Thu, 26 Feb 2026 19:55:29 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f5a77946a9833c6d4e3010b7073dffeff5debac49188bb994f40147aed6cdd`  
		Last Modified: Thu, 26 Feb 2026 19:55:33 GMT  
		Size: 104.8 MB (104806751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afda1a951070a7a14392166975bcd4c26e7ee9017d44f6f36f6d0a5b8b296fa`  
		Last Modified: Thu, 26 Feb 2026 19:55:30 GMT  
		Size: 9.9 KB (9894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85dc5219fc55b16b9a51eaba4764596d5d72af17f280cb49c150ab78f05f88ef`  
		Last Modified: Thu, 26 Feb 2026 19:55:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5e463a34f958a4916f02c9d1b3878b0e0849d5b246e6fa7158bccd5655587a`  
		Last Modified: Thu, 26 Feb 2026 19:55:31 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a510eeb344db5a26d40194bba91d9f2331c28dbf5e490e62a036000d26a80f2`  
		Last Modified: Thu, 26 Feb 2026 19:55:31 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea67dbf39c9c4a81ec69e9225d4354c77f00c55351dea384617b8f1a8751ff24`  
		Last Modified: Thu, 26 Feb 2026 19:55:31 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:09f19e3ecb942ef4698e21b39b53cce412b73299094c5b83df10abbd67a7188d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5712546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c6d3dd6ef45823f285dd6e1c5d5ce877292156594b7f66381d087f2dc79fbb`

```dockerfile
```

-	Layers:
	-	`sha256:11953f12eba7df8de8a31718b00d44583bb1e5b0ff709ce162c54b2090074cfc`  
		Last Modified: Thu, 26 Feb 2026 19:55:28 GMT  
		Size: 5.7 MB (5658459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ca7b7db8756af9a69cb7573efe247ff3dff6b1f6d8a579c55b509a371584b6b`  
		Last Modified: Thu, 26 Feb 2026 19:55:27 GMT  
		Size: 54.1 KB (54087 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:c5e4f1f70d5a5afc5e2bebea1ce71b8805f44938b22a822718ae3ef06051e115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.7 MB (156663737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e044a3419af0767e83de2c5a631f4ae563fd35af595fce4cecb45ccff4b40c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 19:22:35 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Feb 2026 19:22:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 19:22:48 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Feb 2026 19:22:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Feb 2026 19:22:54 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Feb 2026 19:22:54 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 19:22:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 19:22:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:22:58 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Feb 2026 19:22:58 GMT
ENV PG_MAJOR=15
# Thu, 26 Feb 2026 19:22:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 26 Feb 2026 19:22:58 GMT
ENV PG_VERSION=15.17-1.pgdg13+1
# Thu, 26 Feb 2026 19:26:45 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:26:46 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:26:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:26:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Feb 2026 19:26:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Feb 2026 19:26:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Feb 2026 19:26:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:26:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:26:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:26:46 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:26:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:26:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a06368a31120e74d838276e7271b18978163e9a2703d54965c5c6ef7d1203b`  
		Last Modified: Thu, 26 Feb 2026 19:23:30 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e9a8f049cefdd0e0818b63d0686b8290bb9926da9b29e0fb0c973c85ac7118`  
		Last Modified: Thu, 26 Feb 2026 19:23:31 GMT  
		Size: 6.2 MB (6234090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07feb1330a04d32f9b854b1a0f3f2d78ec8f0f96c0d25416e30d3dc8a4ce5ddd`  
		Last Modified: Thu, 26 Feb 2026 19:23:30 GMT  
		Size: 1.2 MB (1209609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606ff205966ce0957dd25649543e0bccdcea279125056176d6f65c71dbaea291`  
		Last Modified: Thu, 26 Feb 2026 19:23:31 GMT  
		Size: 8.2 MB (8203963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d332b92d7389eb40a20411b2d27443d28c847c97d16d369621e1c7ab4f42359`  
		Last Modified: Thu, 26 Feb 2026 19:23:32 GMT  
		Size: 1.2 MB (1220595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00df52df9af7871763b55851962f445dadb779a933e0db24c1e3a525a55d8401`  
		Last Modified: Thu, 26 Feb 2026 19:23:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2093ff109bf9feb2bb840add794d73ab83026bdf3f71c1e4c5e0d5ba810562d`  
		Last Modified: Thu, 26 Feb 2026 19:23:32 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331a806bfc4ff9d0e7ba151b6ea4e041f6a25ea245207a63848f058bb36a081d`  
		Last Modified: Thu, 26 Feb 2026 19:27:07 GMT  
		Size: 109.6 MB (109634749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70967bed2ef22cdb862eff34f1752a054f9a472bc607a4ba4959026055444dbe`  
		Last Modified: Thu, 26 Feb 2026 19:27:04 GMT  
		Size: 9.9 KB (9886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736f3fae741872e2bba18930261ee8c6d240e0e55da7dfb80984202794bb82ab`  
		Last Modified: Thu, 26 Feb 2026 19:27:04 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41337a8e0550cd933fca6cc385312de7c14ac65fe97719a248249c2e0c2f6019`  
		Last Modified: Thu, 26 Feb 2026 19:27:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef1be38ed448c129693f5c06eac38a9e46a6619ef7e2c9dec328e3e88933094`  
		Last Modified: Thu, 26 Feb 2026 19:27:05 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ffc14736fe69237ae21dd9c81773f55598efd682076c550b2090dea9d6ffd4`  
		Last Modified: Thu, 26 Feb 2026 19:27:05 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:b965785b53f9b7af5b947389933c6747bb18bc9b6c0e188e562082e4acb453cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5702995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:999be43e168dc0d03fbfe71b7ebc248264ff5524121bbff5d55f88a41fcde378`

```dockerfile
```

-	Layers:
	-	`sha256:8d05d602ae9f234f482a5a6db3f80e32aac7da24e442a9a5a10a72f14229da8b`  
		Last Modified: Thu, 26 Feb 2026 19:27:04 GMT  
		Size: 5.6 MB (5648862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f9479a8dcb6e0dc04a1586c8127c5a32f7020f550e2a89f98dfab528b1d9fc8`  
		Last Modified: Thu, 26 Feb 2026 19:27:04 GMT  
		Size: 54.1 KB (54133 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; 386

```console
$ docker pull postgres@sha256:087b60e4987f313e00220957009a1ad57c76b26ed6d6919e5d9b047d5048a757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.1 MB (167131877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc269fcebf1e5d0370fac1d48a0f2315733e036ed08430f99346e862271d479`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 19:19:59 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Feb 2026 19:20:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 19:20:14 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Feb 2026 19:20:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Feb 2026 19:20:19 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Feb 2026 19:20:19 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 19:20:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 19:20:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:20:23 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Feb 2026 19:20:23 GMT
ENV PG_MAJOR=15
# Thu, 26 Feb 2026 19:20:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 26 Feb 2026 19:20:23 GMT
ENV PG_VERSION=15.17-1.pgdg13+1
# Thu, 26 Feb 2026 19:31:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:31:40 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:31:40 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:31:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Feb 2026 19:31:40 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Feb 2026 19:31:40 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Feb 2026 19:31:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:31:41 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:31:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:31:41 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:31:41 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:31:41 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84bd3a408c9af9f2b4d754a082372a36ea432ee87d5e7a1bd58e4d1a1316b5b`  
		Last Modified: Thu, 26 Feb 2026 19:32:01 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4048be36438ad439a79f3c9f31f4ec75df7fb6390578474be1305f36e08949cd`  
		Last Modified: Thu, 26 Feb 2026 19:32:01 GMT  
		Size: 6.6 MB (6631489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28c7f0cb5fec2a2a3a813287bca933df447350faac4fbb7f6070beac7ce0e00`  
		Last Modified: Thu, 26 Feb 2026 19:32:01 GMT  
		Size: 1.2 MB (1225821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee8a4d82cb29a063865df58164d19ed038cce8443d872b88e0cf01613c869cf`  
		Last Modified: Thu, 26 Feb 2026 19:32:01 GMT  
		Size: 8.2 MB (8203962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ea5aedcd3a9c15b1e0a092edf0b921edf07e49c9740e83fb70aab99f2520f20`  
		Last Modified: Thu, 26 Feb 2026 19:32:02 GMT  
		Size: 1.3 MB (1308257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81597b820d0f54cefb060ba21cf5660eb1328e407ed701935de03c8b42bf7006`  
		Last Modified: Thu, 26 Feb 2026 19:32:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2c00684190aed8106cb46ec0a82133158eca68e4c91d3ff719004b819670da`  
		Last Modified: Thu, 26 Feb 2026 19:32:03 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08182a548822328888d4b821afac63c25bd9be0789c3f38631544b5b4de4c26`  
		Last Modified: Thu, 26 Feb 2026 19:32:05 GMT  
		Size: 118.4 MB (118447795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565e074c409d9228d80ca80b2dec68618c4c517d1d195ba2930cc3b2ea03f282`  
		Last Modified: Thu, 26 Feb 2026 19:32:04 GMT  
		Size: 9.9 KB (9884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8f2650d03a6f6c576858b9fdbff760a0dacb1a29308179c9bc4c153332894a`  
		Last Modified: Thu, 26 Feb 2026 19:32:04 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe18175f787670fda3f939329ddddcce29c1b02a38c3e73edbdcc8f504599366`  
		Last Modified: Thu, 26 Feb 2026 19:32:03 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab11787dbef41106454cc7a77e295414aae35f049eb5f6d6e4aa91099a24d73`  
		Last Modified: Thu, 26 Feb 2026 19:32:05 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114e8a0ae0a1d6332d0c0958dcdcc048acbdbe4bc848815d4acd2273d8316526`  
		Last Modified: Thu, 26 Feb 2026 19:32:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:cc80e556388607a933de91691d1cd826e8c44e73b209dac92d1e735a82cb5002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5711857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d44b25d3d98f5cc6cc07f027066cf925c4f96c52136826311b94483a110b39`

```dockerfile
```

-	Layers:
	-	`sha256:bdff86eee832b78e812b8e380ed806d95be48910c2423c06cba30c1ccde38aaf`  
		Last Modified: Thu, 26 Feb 2026 19:32:01 GMT  
		Size: 5.7 MB (5658047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e0dced0b33e3eae5af9115c537aae9ad7ade76dc52d8a816ff074e8daf2da19`  
		Last Modified: Thu, 26 Feb 2026 19:32:01 GMT  
		Size: 53.8 KB (53810 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; ppc64le

```console
$ docker pull postgres@sha256:df1f5b01c75323962d5985e506544d9ddf807ec79e0896deda25acc0e6a81da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170288108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90d6d0fbe737507c125e171190675566670f8fcbd0f4a82eaf0c1121e2ef705`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:56:07 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 24 Feb 2026 20:56:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:56:39 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 20:56:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 20:56:50 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 24 Feb 2026 20:56:50 GMT
ENV LANG=en_US.utf8
# Tue, 24 Feb 2026 20:56:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:56:58 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 24 Feb 2026 20:56:59 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Feb 2026 20:56:59 GMT
ENV PG_MAJOR=15
# Tue, 24 Feb 2026 20:56:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 24 Feb 2026 20:56:59 GMT
ENV PG_VERSION=15.17-1.pgdg13+1
# Thu, 26 Feb 2026 19:34:05 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:34:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:34:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:34:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Feb 2026 19:34:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Feb 2026 19:34:06 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Feb 2026 19:34:07 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:34:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:34:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:34:07 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:34:07 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:34:07 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40248b5208b48e0e9ebc31dab2059dabe20332fc4bb1ec45dc8aa5e1fe9c9128`  
		Last Modified: Tue, 24 Feb 2026 20:58:26 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c07d0d1d47bd4056b39ca321d6f1599c262f4e7e7c61fed95bf692a7bf355e7`  
		Last Modified: Tue, 24 Feb 2026 20:58:27 GMT  
		Size: 7.1 MB (7076565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a5f2e35019a76aefee22e397b204520a3f66e4951f57efda4751593a483c29`  
		Last Modified: Tue, 24 Feb 2026 20:58:26 GMT  
		Size: 1.2 MB (1214767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f7a05acca236351baa0b2518676e18567e268cc12c1981ad8b6855176339bb`  
		Last Modified: Tue, 24 Feb 2026 20:58:27 GMT  
		Size: 8.2 MB (8204004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3d66a30c54a599dce72a82fee964c52aa01d586db4c938507314a62bc3af48`  
		Last Modified: Tue, 24 Feb 2026 20:58:27 GMT  
		Size: 1.4 MB (1394901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa754634ead0b3025f44ae8a7a31e0f8b0c32d9914c15de96605223c7d32c45`  
		Last Modified: Tue, 24 Feb 2026 20:58:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c258d92643098feeef8976aec5642f3ca772b343b0556346a5226f72e85b6416`  
		Last Modified: Tue, 24 Feb 2026 20:58:28 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d34f1980b9a1af1cb1f772e3fb84dd3e200f402936bbc8302e94a19d1749f94`  
		Last Modified: Thu, 26 Feb 2026 19:34:55 GMT  
		Size: 118.8 MB (118777024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25aef087c6fe2eb929d7673b8d9b227a45898db4f982841a40622845875fc0e`  
		Last Modified: Thu, 26 Feb 2026 19:34:52 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31480c7c03390760eadd2f3503dba782400d01bf8b77d449743ca74ec30415ca`  
		Last Modified: Thu, 26 Feb 2026 19:34:52 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f217c0e6289b55216e7997dd33626a81cc71990f68ff9a12c90f9dc7adef9b21`  
		Last Modified: Thu, 26 Feb 2026 19:34:52 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66644b1102ca38d5d5d25476c2ef4aeb6900a037575386fca16027e4ea2bec9a`  
		Last Modified: Thu, 26 Feb 2026 19:34:54 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb7efc27fb5bc452addcd95371d445bd680d602656af9436c6bd16632d8d301`  
		Last Modified: Thu, 26 Feb 2026 19:34:54 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:9684b20651e360e8059aee53d14feec6ed0351be9db58486eae7532d87d5781f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5703059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44b7eea52ecdcd5412d66b73f6b5f7b7f4ca4033562e47bbea17b9ced90aee92`

```dockerfile
```

-	Layers:
	-	`sha256:e6cce4189c3a1177b73d14391942c079c6f2a64025897b559e25d5057d7c7dca`  
		Last Modified: Thu, 26 Feb 2026 19:34:52 GMT  
		Size: 5.6 MB (5649129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d144b4e1c44083c30cfa235d88751a1ff4b7a3412f7018bbe7a46ed35fc20415`  
		Last Modified: Thu, 26 Feb 2026 19:34:52 GMT  
		Size: 53.9 KB (53930 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; riscv64

```console
$ docker pull postgres@sha256:542c676f0577618c22053107d932bd05e57cdc4c77361f9cea4f9e4c1393c406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (90001966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7361c0a0c60e6eaebeb4eda2a5e49de7a49784536a23d3733f4d037ab8c998`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 10:33:50 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Feb 2026 10:34:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 10:35:45 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Feb 2026 10:35:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Feb 2026 10:36:47 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Feb 2026 10:36:47 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 10:37:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 10:37:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 10:37:30 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Feb 2026 10:37:30 GMT
ENV PG_MAJOR=15
# Thu, 26 Feb 2026 10:37:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 26 Feb 2026 10:37:30 GMT
ENV PG_VERSION=15.17-1.pgdg13+1
# Tue, 03 Mar 2026 06:22:58 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 03 Mar 2026 06:22:58 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 03 Mar 2026 06:22:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 03 Mar 2026 06:22:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 03 Mar 2026 06:22:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 03 Mar 2026 06:22:59 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 03 Mar 2026 06:22:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 03 Mar 2026 06:23:00 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 03 Mar 2026 06:23:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Mar 2026 06:23:00 GMT
STOPSIGNAL SIGINT
# Tue, 03 Mar 2026 06:23:00 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 03 Mar 2026 06:23:00 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f4de74a642c2b3077707bd1d98d860fa32f2bfe2bc8bec6f008e70352924e8`  
		Last Modified: Thu, 26 Feb 2026 12:47:29 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a8407dad47f53b7bd1ea58319099c5eb75ab9c71c0eaca77278c4ffa19d752`  
		Last Modified: Thu, 26 Feb 2026 12:47:31 GMT  
		Size: 6.3 MB (6293365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66156bf55222d12e2c741e02df3bb126b84a2158817f228188816cf5fdc34b7`  
		Last Modified: Thu, 26 Feb 2026 12:47:30 GMT  
		Size: 1.2 MB (1202062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa18f458f01a6e3a060b40acab343ea7b503f8752ed19cc7d8238801887e74f`  
		Last Modified: Thu, 26 Feb 2026 12:47:32 GMT  
		Size: 8.2 MB (8203602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88856c3799c7a7a18d5a1caec1776767905d6d751c5ca34a43520e664345c9ea`  
		Last Modified: Thu, 26 Feb 2026 12:47:32 GMT  
		Size: 1.4 MB (1402389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9b9b4fafc817b06c3eff32d69f1a43108bca48d49089ec0a13884be0d56a4c`  
		Last Modified: Thu, 26 Feb 2026 12:47:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66199c3c0efda8b281834bafb7b9360c4a8cc288875a8db72f60084aa85bdde4`  
		Last Modified: Thu, 26 Feb 2026 12:47:33 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872ed19f3b3a19c3aad02e80cfdc47f608bd3bfd1be69c4e6f4b5248c80883e8`  
		Last Modified: Tue, 03 Mar 2026 06:25:29 GMT  
		Size: 44.6 MB (44603485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ea4c912a30ed466d26895054105284fb692854f26cbf85ba3cc527b6ba95fc`  
		Last Modified: Tue, 03 Mar 2026 06:25:22 GMT  
		Size: 9.9 KB (9893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8755ae69ea7f7a8364c3e66ed5ec99f45b7fa2a42c1c4a3fdb2bdccb5a06a6cc`  
		Last Modified: Tue, 03 Mar 2026 06:25:22 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388db3554c7d815a9dd425da2df7288f1cc098fd461a1a8a13445ea693fc2bd4`  
		Last Modified: Tue, 03 Mar 2026 06:25:22 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00d29daf8cdd10a02b295e855f5c8f5bfeddf6d5555c529f5313df779354570`  
		Last Modified: Tue, 03 Mar 2026 06:25:24 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff8d76e0d2c10339e2788a2d668358672390264d8bf5461a61daa59655e8770`  
		Last Modified: Tue, 03 Mar 2026 06:25:23 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:3311212e7925f0f2ce76bbd23a2e49468387d29b8e900beb3d88e91e950257c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5074486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5dcae7ff95db83b8bf5a9884666953beab35007455ed2136b61c8913f3d45e`

```dockerfile
```

-	Layers:
	-	`sha256:62015c80f557498f6c0163cf8b2de5f2cfb7424b77cc4757aa1deac71519db0f`  
		Last Modified: Tue, 03 Mar 2026 06:25:23 GMT  
		Size: 5.0 MB (5020562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b763b5d41603febf15c649018d9f77049cd64dea4538de0f8efb1169d3499f2`  
		Last Modified: Tue, 03 Mar 2026 06:25:22 GMT  
		Size: 53.9 KB (53924 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; s390x

```console
$ docker pull postgres@sha256:355d57f65f9153b63857b71ab48dac63dc0bd039c2197bce207b250ad883bb11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172576737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c59b5c2690276b21d2524ae1275d3b15085b5b7b8274423e4541ffe7a877d975`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:58:11 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 24 Feb 2026 19:58:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:58:53 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 19:58:53 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 19:59:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 24 Feb 2026 19:59:06 GMT
ENV LANG=en_US.utf8
# Tue, 24 Feb 2026 19:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:59:17 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 24 Feb 2026 19:59:19 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Feb 2026 19:59:19 GMT
ENV PG_MAJOR=15
# Tue, 24 Feb 2026 19:59:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 24 Feb 2026 19:59:19 GMT
ENV PG_VERSION=15.17-1.pgdg13+1
# Thu, 26 Feb 2026 20:04:54 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Feb 2026 20:04:55 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 20:04:56 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 20:04:56 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Feb 2026 20:04:56 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Feb 2026 20:04:56 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Feb 2026 20:04:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 20:04:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 20:04:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 20:04:57 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 20:04:57 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 20:04:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f89cb3e91c6f05a2aaaec1568bccf0111eb27a1ab74893e027443b68753fe02`  
		Last Modified: Tue, 24 Feb 2026 20:19:13 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a9edf2863b6ea34c01e1f1748cf97e7dd281137dc61ce0756f574075eb20a1`  
		Last Modified: Tue, 24 Feb 2026 20:19:14 GMT  
		Size: 6.4 MB (6408036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e46165db683fe547fefab107b048a75989012f8e59a7e07b3214f6859cda85`  
		Last Modified: Tue, 24 Feb 2026 20:19:13 GMT  
		Size: 1.2 MB (1230336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401960834c8d0f2124e6e9395cd51a41bd7b63a2824b2be6c2dc4ad40d62cec7`  
		Last Modified: Tue, 24 Feb 2026 20:19:14 GMT  
		Size: 8.3 MB (8259108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c1d91545d3cc0591e3d9a14913c132eb264fa903c87d6963052003e35af278`  
		Last Modified: Tue, 24 Feb 2026 20:19:15 GMT  
		Size: 1.4 MB (1398378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e346cb27898b2f1789b656b7135febb4bccaa5fd88dde8b888dad79f0e19e8`  
		Last Modified: Tue, 24 Feb 2026 20:19:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81644e2aa8f1737ea7e351dbd53555d39387732f1a73ed50e6be42548ef0fc01`  
		Last Modified: Tue, 24 Feb 2026 20:19:15 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d128c8b926bc30cd41dc0e92506b5a8ec0a8fba7f7418ae7deece619994b33e3`  
		Last Modified: Thu, 26 Feb 2026 20:05:45 GMT  
		Size: 125.4 MB (125422065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae67782339a381e4f9496f5923629e5f5e7b415bdc3b599403a49bbb6d3468cb`  
		Last Modified: Thu, 26 Feb 2026 20:05:41 GMT  
		Size: 9.9 KB (9886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc25964efc1dd9645b16c9ecd8043e39c952c7ea695004adba56f8316e14ace`  
		Last Modified: Thu, 26 Feb 2026 20:05:41 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6372cc33193c2d291cc214348fa7b5b785b8af363e0ccee0972b2dbc75b7d5ee`  
		Last Modified: Thu, 26 Feb 2026 20:05:41 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ea1d423a999083adf1f5888bdc8ca601ab8e0a555c559403925cc75270ab16`  
		Last Modified: Thu, 26 Feb 2026 20:05:43 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a57dd7c0e1117356aedfe2709f6c56721f1d038f69f391637f2cad82e3548c7`  
		Last Modified: Thu, 26 Feb 2026 20:05:43 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:20221e68fdcdecd3eb85266502bc94394dea723e3e440ee4f4a8aaca27a55759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5713049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8681e0eb134d2b4cf14d4e813ce80dab72ccec9f0b1dc99af8a87609db9abd53`

```dockerfile
```

-	Layers:
	-	`sha256:fe0a86753c8e55e728ec117e3b191ca9d5004d1cd930c16e87c56790233758d6`  
		Last Modified: Thu, 26 Feb 2026 20:05:42 GMT  
		Size: 5.7 MB (5659185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2482730ee35e5f6fad335b4fa991cd4af85c4c271425f813882e227fae925bc8`  
		Last Modified: Thu, 26 Feb 2026 20:05:41 GMT  
		Size: 53.9 KB (53864 bytes)  
		MIME: application/vnd.in-toto+json
