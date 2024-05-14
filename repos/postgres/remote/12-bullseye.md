## `postgres:12-bullseye`

```console
$ docker pull postgres@sha256:33b6732638323452127b954931d5a75bb2c51aa6742611c871a4a59c68e77eae
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

### `postgres:12-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:1894b75dabb1553b01268819f3eb7e3fa20a4605eb1089dcbe8c835247d5fa81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (140046175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e13513361950bf9b5e80145189aadcec850b41d06e3a91b6adcd26072c58214`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:02:23 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Thu, 09 May 2024 18:02:23 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV PG_MAJOR=12
# Thu, 09 May 2024 18:02:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Thu, 09 May 2024 18:02:23 GMT
ENV PG_VERSION=12.19-1.pgdg110+1
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:02:23 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:02:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:02:23 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:02:23 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:02:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e87889d376df97a42f93852776e008e337fb0c84777d7ac964da6b82e23287`  
		Last Modified: Tue, 14 May 2024 02:57:57 GMT  
		Size: 1.7 KB (1683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2da59996413e2a8a0fe9d583b5941c27cdd622c3736993b738e7176a37201d`  
		Last Modified: Tue, 14 May 2024 02:57:57 GMT  
		Size: 4.3 MB (4308176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a079d0c139fa6469dc716113ae0156ca33c8b8d884174018ae75b1a8da5d2b`  
		Last Modified: Tue, 14 May 2024 02:57:57 GMT  
		Size: 1.5 MB (1473530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958aac2ffaed9379359bef22d2d35707fbeaa4af4e0a30605fa5ee1f8d88a7f8`  
		Last Modified: Tue, 14 May 2024 02:57:57 GMT  
		Size: 8.0 MB (8045842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d982aaf2e8f1f7e18dc6598e4eb57bb69e827a1ce7f1a8888cd3e17ffebe640`  
		Last Modified: Tue, 14 May 2024 02:57:58 GMT  
		Size: 1.0 MB (1038350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1931bdb76a00e51abb44415018e02bec69473f1577a994a2753ac956772538e`  
		Last Modified: Tue, 14 May 2024 02:57:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab0fe21ea2706c772153c187ae862abacb15d1dc03ddee6f3e303a1195db5db`  
		Last Modified: Tue, 14 May 2024 02:57:58 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48667d83a28b7e277ed80efb227de3978074f0aac2e3792a3fbd468f1a090f4f`  
		Last Modified: Tue, 14 May 2024 02:58:00 GMT  
		Size: 93.7 MB (93726500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514db78b190e177b7989ba8a42463df0fb6295b3629ec7f4a5b319e9c74e63a5`  
		Last Modified: Tue, 14 May 2024 02:57:59 GMT  
		Size: 9.0 KB (9015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e26886c4a32665478dd2cd4857105d822d7cfa0dbbd05644944683721bee8fc`  
		Last Modified: Tue, 14 May 2024 02:57:59 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03692c705d1adf87abb77a6c918a5a8f904eef323d54b991825cc5514f54f04`  
		Last Modified: Tue, 14 May 2024 02:57:59 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff64b856830e2ae1ee4e0fe7cf47c2e1832cbd69ef7362f6cabb67791d0b27d`  
		Last Modified: Tue, 14 May 2024 02:57:59 GMT  
		Size: 5.4 KB (5414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1f4f45aca5f8d7ac3de8f2dad9e0a821f8b154487958c8d66536e30ae61184`  
		Last Modified: Tue, 14 May 2024 02:58:00 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:d65bd25efc7e84d4fcb96b2aa87d3f1b01d940521ec777e1d7a7e8097d86d49c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5870685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:792f3372765a44e200eb2dc143da5b285b564b44348da83a345a2400ac8d6f09`

```dockerfile
```

-	Layers:
	-	`sha256:916abdedc7eb63db8d061b27d909c5fac890854529810d57e80adbac299d428f`  
		Last Modified: Tue, 14 May 2024 02:57:57 GMT  
		Size: 5.8 MB (5816643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46bac29d0370cd18e24b064614f2db70dd8316822bfb58e485b9b2ac6592f284`  
		Last Modified: Tue, 14 May 2024 02:57:57 GMT  
		Size: 54.0 KB (54042 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bullseye` - linux; arm variant v5

```console
$ docker pull postgres@sha256:e2e794578f7de597450451b19fe4660d0ee5b7d090592920435e19925017758f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136943237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4827bb14b39433c92c0a46268779c75bde30873eef0a9fb0be108e085d80cf9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 24 Apr 2024 03:53:28 GMT
ADD file:4ccbd1f9bcc76d259ba2b235681f1b749e86690e8805ee49f9fb44abc9ff5dc2 in / 
# Wed, 24 Apr 2024 03:53:29 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV PG_MAJOR=12
# Thu, 09 May 2024 18:02:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Thu, 09 May 2024 18:02:23 GMT
ENV PG_VERSION=12.19-1.pgdg110+1
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:02:23 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:02:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:02:23 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:02:23 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:02:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2438f3883cb848a901cb08a6c99ec3ef261d41ca6f0d5321f274d995c58fa24e`  
		Last Modified: Wed, 24 Apr 2024 03:57:14 GMT  
		Size: 28.9 MB (28936577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd96f4ddeed3918920dda16f9ae697f5afc916e4e28204bc42d2ea5a6c03a80c`  
		Last Modified: Thu, 09 May 2024 22:31:53 GMT  
		Size: 1.7 KB (1679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a831087955c97e51222d4fffa1b289c65370286b8e61b6a6ba7e903322c0b0`  
		Last Modified: Thu, 09 May 2024 22:31:53 GMT  
		Size: 4.0 MB (3991748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60438ed248a1b2738126d39a409227de1e26e0c491891811c42aa87ed3e6dd3d`  
		Last Modified: Thu, 09 May 2024 22:31:53 GMT  
		Size: 1.5 MB (1450683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c91e703836f097f74f669c964cfc025d330a0bae6cb904edb6a717356d4f2d`  
		Last Modified: Thu, 09 May 2024 22:31:54 GMT  
		Size: 8.0 MB (8045747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680b5aa1fa768cebb527bc8b4fab06246611886807fff24af3b87e14c9de5693`  
		Last Modified: Thu, 09 May 2024 22:31:54 GMT  
		Size: 1.0 MB (1034899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e309ecf1a190edc1ef89b99d65cab41262c2ea861ec35682a2d5528f03c48485`  
		Last Modified: Thu, 09 May 2024 22:31:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681e12d84bf9bc40f3633e0dca8b7b03774d24f5189f3189804322a0b03a2fd2`  
		Last Modified: Thu, 09 May 2024 22:31:54 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238ba6583f1c375188a5cfb038613fd5039e50d64ad2b8118965baa7f272dd9b`  
		Last Modified: Fri, 10 May 2024 00:39:57 GMT  
		Size: 93.5 MB (93463717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fb691d6405617bfc924cb47b18dbfab5d46315075119b9aae8e9bef1910f0f`  
		Last Modified: Fri, 10 May 2024 00:39:54 GMT  
		Size: 9.0 KB (9025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcc4567c89afe38a5544630c7506b0d3959bfe877f0dcdd622488c6d4e14254`  
		Last Modified: Fri, 10 May 2024 00:39:54 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad045089afdc24ec0fcd2e1c3a48f180b1cf06a2c96663496be7aa0d2914342`  
		Last Modified: Fri, 10 May 2024 00:39:54 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70898a84ed5c007a43aa0828cacf2eec588b2cb5c6aa472604d784a4da2e672`  
		Last Modified: Fri, 10 May 2024 00:39:55 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42eec081f539d1fa6a1197686cdfc93e1966920a31de91b2e3e85908c7c1c44b`  
		Last Modified: Fri, 10 May 2024 00:39:55 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:e6b5fd03abcbe8899c30317046075936183e74b672601b6e66403ceefbb2cf89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5884055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120cee8ddba85e8d1153eca2ec09d34d2e4c392d2ee0b4e52c18de906e09a630`

```dockerfile
```

-	Layers:
	-	`sha256:f96380dfac60300b7b948d0b5c5d643671118ac1ad5a512bb7364d558566746c`  
		Last Modified: Fri, 10 May 2024 00:39:54 GMT  
		Size: 5.8 MB (5829983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1167e1fbd388b40508fefec828bf68fba9b58223633f9fee89375f09c2cbf5e7`  
		Last Modified: Fri, 10 May 2024 00:39:54 GMT  
		Size: 54.1 KB (54072 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:955e6a4e256c85152f0348defc983020e1df7e754960b935a44336e21994cf55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128096503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842f157bb810ba847b810782f4e38e7215643c307646bbe57fadb374152b2d87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:02:23 GMT
ADD file:b58f353e9d2a24c2c16ae0913b28705d3ecc439d60d82b5b4982780c59aae249 in / 
# Thu, 09 May 2024 18:02:23 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV PG_MAJOR=12
# Thu, 09 May 2024 18:02:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Thu, 09 May 2024 18:02:23 GMT
ENV PG_VERSION=12.19-1.pgdg110+1
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:02:23 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:02:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:02:23 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:02:23 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:02:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a5c0b9604ae49509a7875b258d98493d63bdb4c1c27a70f2befa5fa4fcea1888`  
		Last Modified: Tue, 14 May 2024 01:13:30 GMT  
		Size: 26.6 MB (26594493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494537f20540f58366b54264eefdb5692ddddbaee2a456edc2935f06c8b8a5f2`  
		Last Modified: Tue, 14 May 2024 17:26:29 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c291d4a01ceb73ea19c75f8b4ac99cabb6eb19544ba6676dbf055b2cfc64b7`  
		Last Modified: Tue, 14 May 2024 17:26:29 GMT  
		Size: 3.6 MB (3601586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8725ae31c4b0e23bd4a351739ad878aad4e31e9a0b0c7c1fa5e5f5e807443c`  
		Last Modified: Tue, 14 May 2024 17:26:29 GMT  
		Size: 1.4 MB (1440774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502fb5511561bab9f785ee1fc6496f94e4576d638a19238787194978941bcc9b`  
		Last Modified: Tue, 14 May 2024 17:26:30 GMT  
		Size: 8.0 MB (8045792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c2650bb8de51fb8b14edbb5243fef5cb0c7c73e0686f5410179710623a0a8b`  
		Last Modified: Tue, 14 May 2024 17:26:30 GMT  
		Size: 908.7 KB (908666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cdeeacebbd53fe190eca31f2415258a1fffe816587cf3f267b95c8e29e9ea2d`  
		Last Modified: Tue, 14 May 2024 17:26:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717b586b7108f72471cc5eded8bef265f1d62edd7744226d8aa3060404c6a926`  
		Last Modified: Tue, 14 May 2024 17:26:31 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5969b7b00a651d136cb3e06ca5e41ac7a073267163468e8edd23a02af18eb6a`  
		Last Modified: Tue, 14 May 2024 19:42:57 GMT  
		Size: 87.5 MB (87485339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e29efaf5d2e623c7fdf64f271322d4a8f413a661718b44b3e94286019ebc9eb`  
		Last Modified: Tue, 14 May 2024 19:42:54 GMT  
		Size: 9.0 KB (9022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c81dc7a09c2ecadf3de514ac5feb63d59e3cb99e0f2011b53cef0ec76888d99`  
		Last Modified: Tue, 14 May 2024 19:42:54 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68aadac42b0e3e2eb6ddc52b7af0851f2d79d8a3ed20a7aeef40096d6136414`  
		Last Modified: Tue, 14 May 2024 19:42:54 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2b7ee2257655e580f6952cd4a3ef529f55f2ef8061d9b7fd4fea96c15471e1`  
		Last Modified: Tue, 14 May 2024 19:42:55 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f601229065eda7c9c9cda5dda05f6ede9b7cccee64798c340a5449ef4e08e288`  
		Last Modified: Tue, 14 May 2024 19:42:55 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:32e3eb297c2cc9d945f96dee1de65b7edc56be23355e943110968dda98439007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5882830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3080fbecb66dbd0ee1bcdb9ca21a74bab4189662742ed6f07cfc7f39cde56d97`

```dockerfile
```

-	Layers:
	-	`sha256:0a90382580ee667e4a9e04dfe2a58bb7ddf280eb291a2051892f37b99ccf16e6`  
		Last Modified: Tue, 14 May 2024 19:42:54 GMT  
		Size: 5.8 MB (5828767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7b4a141409d5d8782ba8de890de3f47e715422f70f3a53150947cd6dc35caf9`  
		Last Modified: Tue, 14 May 2024 19:42:54 GMT  
		Size: 54.1 KB (54063 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:e427f7f3dfaf0d2caa310016fc8cefecb2042e2082b76366ed606cb7c38063c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136486116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7663ce4dbf61326dce4f3feaee17fe390bd7b8718c77d52f48eb87d4644f94b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV PG_MAJOR=12
# Thu, 09 May 2024 18:02:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Thu, 09 May 2024 18:02:23 GMT
ENV PG_VERSION=12.19-1.pgdg110+1
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:02:23 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:02:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:02:23 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:02:23 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:02:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4cf331cfa9ee1fa649059c460935e6a75297c0e548ed7312f67f968471fa23`  
		Last Modified: Thu, 09 May 2024 22:20:54 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a6b0883f3f14669d08ab8624d8a928a25fd19a061b08e9d3b4735d9db1c25a`  
		Last Modified: Thu, 09 May 2024 22:20:55 GMT  
		Size: 4.3 MB (4312687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76136eb3ac9cddd986058939565e8a5237c081ac7a022ebc93aaf629399cb068`  
		Last Modified: Thu, 09 May 2024 22:20:55 GMT  
		Size: 1.4 MB (1405860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa62ba99c82212b0d92903694703b31055ee84da6f304c3f104699cd5c20cf6`  
		Last Modified: Thu, 09 May 2024 22:20:55 GMT  
		Size: 8.0 MB (8045705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a00d9e4431f076c0cdf87f62e4974538250001df43bf785e35c9febe32bf6b`  
		Last Modified: Thu, 09 May 2024 22:20:56 GMT  
		Size: 1.0 MB (1026611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68bdef5210add3e65771bd7feb6ef9577508522f71adc32ae17e3263d9017e6`  
		Last Modified: Thu, 09 May 2024 22:20:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19eb433ae82866c7c6aa2c734680fc6a4e1aa84c507171a00898054d9ab7fec`  
		Last Modified: Thu, 09 May 2024 22:20:56 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f3afb6ddd8cfbdedc11bedd3c890f2ba332f20ec8cfe7381910d07af659dc3`  
		Last Modified: Thu, 09 May 2024 23:23:57 GMT  
		Size: 91.6 MB (91588045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b8adfb7d8448fb6c291d14038808a83a840a4c62760804d878be3586fe2dbe`  
		Last Modified: Thu, 09 May 2024 23:23:54 GMT  
		Size: 9.0 KB (9024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2cb190359824415c36cb3807d7cf22ec9a505e726fc3b7ca361060799da26a9`  
		Last Modified: Thu, 09 May 2024 23:23:54 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e90c0017c40786c190c041def7e4e21cbbe1f715e2d91beccaa149cb8d8726a`  
		Last Modified: Thu, 09 May 2024 23:23:54 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3668c2c2a60033c402138a492acaeeb04d5b3a771f65b5eeb34c2f18b74ad1d`  
		Last Modified: Thu, 09 May 2024 23:23:55 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e11141e9d5fbef68063450e86b9f28a732f84fbe510ea6a36a4e1bcd0c022e9`  
		Last Modified: Thu, 09 May 2024 23:23:55 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:81f851180d40adc56ba2bbe5a5fbc2d0b266cfd97ae9a00553290b45fa375998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5877775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:381313a0b91f35e3a7c9ae90c57f025dbb49835b8d1b411b7b775ef7cd0653ba`

```dockerfile
```

-	Layers:
	-	`sha256:5bc3b2045751a1427d9aa49d6876716dfe5eecf8d22c70ff7a89ac4c230e5ce2`  
		Last Modified: Thu, 09 May 2024 23:23:54 GMT  
		Size: 5.8 MB (5823894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3663d0ec629c00b3cee7bb04c82d18f25f62f05859752414eb9b5d51a18f596`  
		Last Modified: Thu, 09 May 2024 23:23:53 GMT  
		Size: 53.9 KB (53881 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:3f976847cd250406f43322d2974b4debd6ed05b509ed4c9a1cd2bc1c05695274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142607303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ab7b1701ccba59535d497650ef4244a77e74e7ae8256f55b4eecb5a2d4a42bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:02:23 GMT
ADD file:8cc17bd8431911317f7d91df00ff305ed2f31f83f3224da64f6d7b9c38819dae in / 
# Thu, 09 May 2024 18:02:23 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV PG_MAJOR=12
# Thu, 09 May 2024 18:02:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Thu, 09 May 2024 18:02:23 GMT
ENV PG_VERSION=12.19-1.pgdg110+1
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:02:23 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:02:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:02:23 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:02:23 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:02:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:de7432ff839295b583814dfc21a6afb18eb4e45d8144c26b1402229e5bc8105f`  
		Last Modified: Tue, 14 May 2024 00:52:45 GMT  
		Size: 32.4 MB (32424043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7678c20eb5dff1070d14949a42e162ee80adaebeb0f685f4edf0584d63ea8d`  
		Last Modified: Tue, 14 May 2024 02:04:57 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a758e9d6598a688c4b73cb014fe532024f80653996cefe2c9124ea8a4f84e5`  
		Last Modified: Tue, 14 May 2024 02:04:57 GMT  
		Size: 4.7 MB (4719620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4590b729c9b3e34df468cf6f5b95ce4af0dd9e0c9a9fd99aa5a4cd871d0ce2c1`  
		Last Modified: Tue, 14 May 2024 02:04:57 GMT  
		Size: 1.4 MB (1449308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538c2061a645d8ba852c5911d21af964e896554fd0f13a4c0e5c68a79be1b5c3`  
		Last Modified: Tue, 14 May 2024 02:04:58 GMT  
		Size: 8.0 MB (8045767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf52b1e5ac9068eaf137e4738836a961657f68938ed7ad5b5fe97240bd9abb0`  
		Last Modified: Tue, 14 May 2024 02:04:58 GMT  
		Size: 1.0 MB (1028895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ca5bbc216634ff815a41de7a6f387ed8c66e54300e26cd8e98f13f89ba33cf`  
		Last Modified: Tue, 14 May 2024 02:04:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b29eacf60ea2eb7abd3b0e50f440a7dcab9a742fe73e5cd6925290f37fd6c02`  
		Last Modified: Tue, 14 May 2024 02:04:58 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd5ff74858408df0d1ca275e3e6a3a5ba8416979a2dc340e5c50a8d9b2dd00c`  
		Last Modified: Tue, 14 May 2024 02:05:01 GMT  
		Size: 94.9 MB (94919812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a1e2a054f6213eb3946151f4f9cf3b76484357c4aaef59105b04f5e5c1c591`  
		Last Modified: Tue, 14 May 2024 02:04:59 GMT  
		Size: 9.0 KB (9018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58970b3f122959bd6faee8853e1911cb118c8d8373a1427cce745f58e990d9f4`  
		Last Modified: Tue, 14 May 2024 02:04:59 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e150158ed6de965cc026107edd83200b95dcae34233387c127987d6510f1466a`  
		Last Modified: Tue, 14 May 2024 02:04:59 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642ace7fa21135015f118fd9c2d7c8bbc0ad7599c1dd6576c7dcc00f23fb8dd3`  
		Last Modified: Tue, 14 May 2024 02:04:59 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12258a7901a806eb4281f523f407bcd87c08598a2c13eb2e5e9d91cb23ff00ed`  
		Last Modified: Tue, 14 May 2024 02:05:00 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:3733aac7548008ddf10c8c9758fe5fe04a4e5ebc537100197e0462225c007a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5880316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141cd7542c72d53a277a557f9a5fbea10b7e135f8ece2e6afde63aec86be7fd4`

```dockerfile
```

-	Layers:
	-	`sha256:4f83ac762ac21ddfe5a7eba01a465e55de823f82f3dab86638c5732222684bb1`  
		Last Modified: Tue, 14 May 2024 02:04:57 GMT  
		Size: 5.8 MB (5826315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cc9d14d21b94ba37bbd555d1c676b5654c3d93b531f9710534537a050ae4ce6`  
		Last Modified: Tue, 14 May 2024 02:04:57 GMT  
		Size: 54.0 KB (54001 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bullseye` - linux; mips64le

```console
$ docker pull postgres@sha256:c4d2e9da466b943d9966de902bd066fdcdf1fb23b6e9838718ff22e66703c45a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138658791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ef6bd3b9c408f893336af2f3b7e3fe2a5ecf71eb03db21548eaba98006b08ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 24 Apr 2024 03:15:35 GMT
ADD file:87680940dfe26d5f4583964a639405d4e00c6a3f72863f7b7e18eca764a73c67 in / 
# Wed, 24 Apr 2024 03:15:40 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV PG_MAJOR=12
# Thu, 09 May 2024 18:02:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Thu, 09 May 2024 18:02:23 GMT
ENV PG_VERSION=12.19-1.pgdg110+1
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:02:23 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:02:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:02:23 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:02:23 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:02:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2d257022fa7c7f0c7879f59891b7e4277d67c9114b820f229207724d5e65d6cf`  
		Last Modified: Wed, 24 Apr 2024 03:26:43 GMT  
		Size: 29.7 MB (29652163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86a280530a4c317a5198840d3370938c0168a63a83cff111f922767bc39e2ad`  
		Last Modified: Fri, 10 May 2024 00:21:43 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259b0e3493765c6bb3e879271d9d4a930c7c43177e8353303ef975dc35708d70`  
		Last Modified: Fri, 10 May 2024 00:21:43 GMT  
		Size: 4.3 MB (4308323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5305d15dab913cf26c8bf5d9fd89e07538a9af9f3367161d6c266a0cbaa71666`  
		Last Modified: Fri, 10 May 2024 00:21:43 GMT  
		Size: 1.4 MB (1360871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdebd054a6016165f935d7b707651efdb520ad1ec0d488cc1d39f14d40aaf03`  
		Last Modified: Fri, 10 May 2024 00:21:44 GMT  
		Size: 8.0 MB (8046083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef72e856f89f28556694e4803345d8b93f23e3ba8e59faf584f9ee7b8bc67f0`  
		Last Modified: Fri, 10 May 2024 00:21:44 GMT  
		Size: 1.1 MB (1090243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afda6a49625bba65b6e6a9ab9788ad582a178a8d8dfbbbd7ce2da9b5824515e2`  
		Last Modified: Fri, 10 May 2024 00:21:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e22d50fbc6da9abb9f4245803c24f6cc55de63f8625c1ec27975e0363e866ff1`  
		Last Modified: Fri, 10 May 2024 00:21:45 GMT  
		Size: 3.1 KB (3146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31274435faf31f4ad70df766b7b6eebd2c3e4cb1c412ada0e149e2e9148783de`  
		Last Modified: Fri, 10 May 2024 09:25:47 GMT  
		Size: 94.2 MB (94181221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6b966ed0167e5df6f762872ef9e8537acdeb275b024abbe247814d290a3839`  
		Last Modified: Fri, 10 May 2024 09:25:37 GMT  
		Size: 9.0 KB (9030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537d68f8ba97193b62020b0f7caf11cf793a002b04ecd09efc37e094c965c80d`  
		Last Modified: Fri, 10 May 2024 09:25:37 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db134c4b915201d5fa58d8f1d42d5c18a3f69bfdda6756fee3b682e3b3b2310`  
		Last Modified: Fri, 10 May 2024 09:25:38 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b9a8caf568839ec4d22102ef70acc2f06a8297eb9549e29a7b07cb37a0c3314`  
		Last Modified: Fri, 10 May 2024 09:25:38 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da429a27061cc883c2db62acd1e0cd7bfcb733a7325be24d62a0c24087a46a17`  
		Last Modified: Fri, 10 May 2024 09:25:38 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:37d734ddf9de8fd846f8f0b2f9df48a49c515d3706e6bf8f2033cf8fe1113d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 KB (53728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a94a7142488eb98832921909b9768ed8054accbfe4cc9721070681b5f78b4039`

```dockerfile
```

-	Layers:
	-	`sha256:69f607370a08a8057cc38a24f40d74ad1e86920bb2ed5e23409b0490d264a946`  
		Last Modified: Fri, 10 May 2024 09:25:37 GMT  
		Size: 53.7 KB (53728 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bullseye` - linux; ppc64le

```console
$ docker pull postgres@sha256:b6562225b24c60843141672b1202a3b4117618923bd913a9071306c152466d17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.8 MB (150812346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84512d4273d2559653bee17fb58c32ca520bf6593d47a22f0d48f8e4c0ef4ca5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:02:23 GMT
ADD file:7c74907a13931bf5f38ce8642536ee05738ba9d233424998c52fc548130034b5 in / 
# Thu, 09 May 2024 18:02:23 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV PG_MAJOR=12
# Thu, 09 May 2024 18:02:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Thu, 09 May 2024 18:02:23 GMT
ENV PG_VERSION=12.19-1.pgdg110+1
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:02:23 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:02:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:02:23 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:02:23 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:02:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8fd45f8fa7e828bdb5dd8878febd6f367c5092a047db5f6ca094056a1b0c627c`  
		Last Modified: Tue, 14 May 2024 01:24:52 GMT  
		Size: 35.3 MB (35311159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1235223a318cb62554e65c2d1f1a498b9792066e504a7b470bd5fbb4544df604`  
		Last Modified: Tue, 14 May 2024 15:40:49 GMT  
		Size: 1.7 KB (1681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e97dae3d796b39ab1573db218f4e5250543a4f6fd855a2f6d326ed88d7770d`  
		Last Modified: Tue, 14 May 2024 15:40:50 GMT  
		Size: 5.1 MB (5137874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e0c9e92539e0c2ba742726c009111c147f86960a9bf599bf04943ce1693870`  
		Last Modified: Tue, 14 May 2024 15:40:49 GMT  
		Size: 1.4 MB (1394903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06efbab62c9510c70a3fea123ee45c56fdbee1e768283666836cfe5710ef1f4e`  
		Last Modified: Tue, 14 May 2024 15:40:50 GMT  
		Size: 8.0 MB (8045878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974e84a835bb377946282ae200ef4e73b477298eb1d7a36016fa33ecdf176483`  
		Last Modified: Tue, 14 May 2024 15:40:51 GMT  
		Size: 1.2 MB (1197549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6669c23fcd244c2d8fe9a1adc5afd4f63cf65be06017f9b53c1b7ba040cab900`  
		Last Modified: Tue, 14 May 2024 15:40:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1647d546bb5750047f27efd7e3a9e79499c656a4f85656497605d0766bca97c1`  
		Last Modified: Tue, 14 May 2024 15:40:51 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a2131f961613ebad32ab5e450f9f6bece09d2a4bd0638e5fe66273a6d37cf8`  
		Last Modified: Tue, 14 May 2024 15:52:44 GMT  
		Size: 99.7 MB (99705126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c69bf09ea6cbc0ebf362e2a226fddad4f0badde390b19cdebfd7e3498833d21`  
		Last Modified: Tue, 14 May 2024 15:52:42 GMT  
		Size: 9.0 KB (9021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f649c679f656564d551cbbe21134fb3a33d57485a0e750e4dc15993528e433e3`  
		Last Modified: Tue, 14 May 2024 15:52:41 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47176b518432a3f7c3bdb1967b1b7a00b0a19b7a88ef4a1c1c9284a7bfea6d2`  
		Last Modified: Tue, 14 May 2024 15:52:42 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c3ecb2cc69bb89e251c62cfc062a4b8a9f8899b0aeb36742e740c99a4c29fa3`  
		Last Modified: Tue, 14 May 2024 15:52:43 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b729dd85d4b465aa8909612bed0b21c9c5f654fc626379547419b7eb42472f33`  
		Last Modified: Tue, 14 May 2024 15:52:43 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:697fec65289703b91ab4313b1655654b4260527e3152bc1e917d5c74c731ed8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5877698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dab96f47c39075420d4b8d103fd68f8ed3d826abe35e04e07400064687641fb`

```dockerfile
```

-	Layers:
	-	`sha256:95d1a0c5b9035f84a0864219d077ab1a02e0428d75467da4776b55bce01f3734`  
		Last Modified: Tue, 14 May 2024 15:52:42 GMT  
		Size: 5.8 MB (5823775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04bf69e85d2dc07e75e22b528d7e0c47768a49dedc892086891aa2dc0ce021d1`  
		Last Modified: Tue, 14 May 2024 15:52:41 GMT  
		Size: 53.9 KB (53923 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bullseye` - linux; s390x

```console
$ docker pull postgres@sha256:5776207d1e25cf77c0ca23359bc4394fa1e5a74afc5bd1e160b734f0d5c4cf90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144331000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83c6e3630b157db5eaa33ef8c0c3e40293d54fc8b5eaaa8d2a1fb39e512a8e27`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 24 Apr 2024 03:44:03 GMT
ADD file:acaea4e054f1ab7ae5cbc8f02c73b546c367aebfcc48c7fb4f0dd9f3628bc25e in / 
# Wed, 24 Apr 2024 03:44:09 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV PG_MAJOR=12
# Thu, 09 May 2024 18:02:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Thu, 09 May 2024 18:02:23 GMT
ENV PG_VERSION=12.19-1.pgdg110+1
# Thu, 09 May 2024 18:02:23 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:02:23 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:02:23 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:02:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:02:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:02:23 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:02:23 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:02:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6f588995519e0e04ef4c150b91ad96c3c85667869db0ad72e5a78d4fab796e70`  
		Last Modified: Wed, 24 Apr 2024 03:49:47 GMT  
		Size: 29.7 MB (29673934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7f9f87a3e9f2f6e90eeedf590bc47d168e0b91cd0664ed2940e19d9f8b7f4e`  
		Last Modified: Thu, 09 May 2024 22:09:02 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac51c47b584feec2373381408b6dc44d49048274ce17e024e7e9e4a23b47a80`  
		Last Modified: Thu, 09 May 2024 22:09:02 GMT  
		Size: 4.2 MB (4200335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70debdb95223b151048550657a7627fc1b8ff91aa5b455570fb79cebda457013`  
		Last Modified: Thu, 09 May 2024 22:09:02 GMT  
		Size: 1.4 MB (1439487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5ea228719ab884770597383ea3bf11f3deadf83a93c5b11675f5f7e501a69d`  
		Last Modified: Thu, 09 May 2024 22:09:02 GMT  
		Size: 8.1 MB (8099560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7353c69003022afdda61f27ad6bfac75f2ab850c7a6dce3b45d71fcf968e45da`  
		Last Modified: Thu, 09 May 2024 22:09:03 GMT  
		Size: 1.0 MB (1015299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32356c3b2e78bf0090cfb6c1abdf047e83dcd1b456b9157cf837f487023e2800`  
		Last Modified: Thu, 09 May 2024 22:09:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325769b7b2ba67dbb402d388eb6c4b55f6477f756ba46f650219d962edd1fba9`  
		Last Modified: Thu, 09 May 2024 22:09:04 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a339ea50eb1e74906492e209c3faf0c1028c9b8b10b2a22831e758b14c3346e2`  
		Last Modified: Thu, 09 May 2024 23:23:18 GMT  
		Size: 99.9 MB (99882512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90e22d84864a1290ce8442582d29f202055d2c629f3127f8b663ce038a1ff5c`  
		Last Modified: Thu, 09 May 2024 23:23:16 GMT  
		Size: 9.0 KB (9023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f9c4ab537d3fe4533cd8d9fd8ce8af7e5947589f99c1e2765a741fa132c623`  
		Last Modified: Thu, 09 May 2024 23:23:16 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252cfbbc4aba6bc748a278e084361bf64ce37b561a6c05400ab0cda9b80e91ec`  
		Last Modified: Thu, 09 May 2024 23:23:17 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c854c3a4a1da0f20c05f26ddfa3e28f1516b596a37495540717e4405d029b54`  
		Last Modified: Thu, 09 May 2024 23:23:17 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf16534d5ac7b8ac0f3db6c92d346ba2889d3227795539a66bfb8f605963cd1`  
		Last Modified: Thu, 09 May 2024 23:23:17 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:a563e7ef59ba31ddbb65fa7eb74ca8fea1bed94538e67cad20b7bbdcdb3dfeeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5870481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33ab0dc5389905e78c4bf3c2fb8ee5ae5282f652f273348a6236dea945c9b137`

```dockerfile
```

-	Layers:
	-	`sha256:9e39d34a5e205f0a93aee559f78b741b356fdee993e3ba99bba9a0733dcbe10c`  
		Last Modified: Thu, 09 May 2024 23:23:16 GMT  
		Size: 5.8 MB (5816606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0ca08d7b4ef131519a1590cd68f44e59727b4b5436a7f9ca20b3052791c3808`  
		Last Modified: Thu, 09 May 2024 23:23:16 GMT  
		Size: 53.9 KB (53875 bytes)  
		MIME: application/vnd.in-toto+json
