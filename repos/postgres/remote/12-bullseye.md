## `postgres:12-bullseye`

```console
$ docker pull postgres@sha256:8199bc100f92cea45ee6b172274aad96622af1ab3188ee956b469ef9c0327895
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
$ docker pull postgres@sha256:32090c3e89062a98a699db4a6ab2f9003ea46e102f986e18e69a3a9ec6a14093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (140046550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b1c2950a5cdfd76b70c17bd0bd881fb54219846a289cb6441894e014fbedf4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
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
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f5a37ff3c978bb21053358f91a40827c0513e84cd33d1f3d9a73b98e15932f`  
		Last Modified: Thu, 09 May 2024 21:53:26 GMT  
		Size: 1.7 KB (1683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2f1f0d0eebb5c8e82b18b599fdbd41db531ca0f46fe1f0475642a149ffff26`  
		Last Modified: Thu, 09 May 2024 21:53:27 GMT  
		Size: 4.3 MB (4308196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ee6d59c2f1d4fb67fe5a48bbd8e8223c34fa83210f803a2f57cb46a37b145c`  
		Last Modified: Thu, 09 May 2024 21:53:27 GMT  
		Size: 1.5 MB (1473544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea690ef17ec3f5da0f1694470d4f214e45b5be7d323fffa875cf2244d0510f75`  
		Last Modified: Thu, 09 May 2024 21:53:27 GMT  
		Size: 8.0 MB (8045776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275fcee04c14ad0229c834b1adb18bc2fd68359a76a6e3818ecad7cf644805c8`  
		Last Modified: Thu, 09 May 2024 21:53:28 GMT  
		Size: 1.0 MB (1038392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca2c392b5073b946f1c1daafc2301b009702ab27345fc31eae9ac3afc7aed26`  
		Last Modified: Thu, 09 May 2024 21:53:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89fda314f1aa0db9f7da9b8ef076be53db76b269a8dde250249d7e5efa936ee`  
		Last Modified: Thu, 09 May 2024 21:53:29 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f353c6ea146b7431d60d114d52fe5eecc19c09e711de4db7ca1cc3d8a6fa1f`  
		Last Modified: Thu, 09 May 2024 21:53:31 GMT  
		Size: 93.7 MB (93726502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6320d585eeed2e5ebee1cc965de64921cc717305636a094802ce94f51dd33d`  
		Last Modified: Thu, 09 May 2024 21:53:29 GMT  
		Size: 9.0 KB (9027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6001ecb5e4c32b13a5fa926f068a8b7ea0495c958adac096535264a3933cb3c4`  
		Last Modified: Thu, 09 May 2024 21:53:29 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4201ed3b743e8a450802f46ef6eebfd7f84cead30f869d16110c1c8a490c0ae6`  
		Last Modified: Thu, 09 May 2024 21:53:30 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e976b90f736f78e2ef18a7710cbfc727703aaa4db1bc83cc55ec74853f7ecb9`  
		Last Modified: Thu, 09 May 2024 21:53:30 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137e9238247180e94d5a1fa99e436ca2109e0e1b3dcfd76d051c5d4957b4c668`  
		Last Modified: Thu, 09 May 2024 21:53:30 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:36a3659a507b40547829340b44c6a994bba99bf52a4141fee3cd33a2b00e6b12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5871671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec94f7999a07e8e5d5997ba92b3703702498e2b36b8f39543d0648ba82655b9`

```dockerfile
```

-	Layers:
	-	`sha256:ab104afc696dff808bea1031c113f5f5b4cfb6f547e72e742ccb7e82bb8057b1`  
		Last Modified: Thu, 09 May 2024 21:53:27 GMT  
		Size: 5.8 MB (5817629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de3fafbeb635b12cd231d28c6b66b590c7badc2e4a532aa230407dbf6ade250b`  
		Last Modified: Thu, 09 May 2024 21:53:26 GMT  
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
$ docker pull postgres@sha256:73f45b549f6cef3a98c8b3bac2ce87050672f0f38cbe994fd3a2504a93aa7d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128089578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee5b5a417016bb9d57d42b03cb9e39db32ad8fc6fce40a953b82c7e4dba7920b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 21 Feb 2024 00:46:13 GMT
ADD file:83a77ac4b262a896dbca1f6974e4401639b3e4d4ca432d88a933c7983e8ccf10 in / 
# Wed, 21 Feb 2024 00:46:13 GMT
CMD ["bash"]
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV GOSU_VERSION=1.17
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV LANG=en_US.utf8
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_MAJOR=12
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_VERSION=12.18-1.pgdg110+2
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 21 Feb 2024 00:46:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Feb 2024 00:46:13 GMT
STOPSIGNAL SIGINT
# Wed, 21 Feb 2024 00:46:13 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 21 Feb 2024 00:46:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:913a7319952754f0a4a369ee846fb9ecf15cbbead6a1be0f4bdf4a7cbeb1d33c`  
		Last Modified: Wed, 24 Apr 2024 04:11:56 GMT  
		Size: 26.6 MB (26594742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05567ed7205d81046d035c24d1a1f20a19ad18d7b6756ece9732197a2eb328a`  
		Last Modified: Wed, 24 Apr 2024 21:01:16 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f3619264270cd97bec7a249b2baeacb6dba3c4db5d067785285552f437b271`  
		Last Modified: Wed, 24 Apr 2024 21:01:16 GMT  
		Size: 3.6 MB (3598271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e737e054941d44443936b0bc82a33fbaa047d3a14c57efe400e56ae07b638b4c`  
		Last Modified: Wed, 24 Apr 2024 21:01:16 GMT  
		Size: 1.4 MB (1440840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e396755532d3b796470d0668873e5aab9b673093a5632fbb8eb366a05b9be7`  
		Last Modified: Wed, 24 Apr 2024 21:01:16 GMT  
		Size: 8.0 MB (8045826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b986c07c625ef3fa9b184c72cada5a26599f4b816cb728ecd86d6d01786c66`  
		Last Modified: Wed, 24 Apr 2024 21:01:17 GMT  
		Size: 908.7 KB (908670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913ccb34575fe713245e767d1f8c70557ef45d3c837d43361df5c480302531c4`  
		Last Modified: Wed, 24 Apr 2024 21:01:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704e094050fad8f912c15d03b38591a0a99fbe7bd55a33c8531473948f80219f`  
		Last Modified: Wed, 24 Apr 2024 21:01:18 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a039464b7d66f6c23ca3544005de44bdf13213e8477830d25f2e2473fcd98783`  
		Last Modified: Wed, 24 Apr 2024 23:17:16 GMT  
		Size: 87.5 MB (87481354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3029c0efe44bb33c4723f7f0b7317ef374b815bd15acf1753d73546f88b174e`  
		Last Modified: Wed, 24 Apr 2024 23:17:13 GMT  
		Size: 9.0 KB (9035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ba31cfd3bd86d78755453e390366ebec6272618c82050b0c2a7a4feb3879ed`  
		Last Modified: Wed, 24 Apr 2024 23:17:13 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de359b0e0bd5cf893617c93aaa5e6f2ab1387b023f3b094aca2639abe7af2124`  
		Last Modified: Wed, 24 Apr 2024 23:17:13 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9bb85db917ae3e956628ac68de64cbdab59fa2f301824c85ab6887d49ca8b56`  
		Last Modified: Wed, 24 Apr 2024 23:17:14 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d9b540b65046e0dace4815fe4092234957bfc2f26d16cf6f87fa7cb7319e4c`  
		Last Modified: Wed, 24 Apr 2024 23:17:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:75f96f10b4699fddb35b7d0030e81d6235bd614733363a11640eed15e00c9f44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5882176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d715fa3782b6c9eb30affe4ba991f2d849b45a0959c7f4163e8e8c3e2d3cf6d2`

```dockerfile
```

-	Layers:
	-	`sha256:51977dce5c96500da89b79d758cf5cde909151b9b39ee4673fe2456c81b3a876`  
		Last Modified: Wed, 24 Apr 2024 23:17:13 GMT  
		Size: 5.8 MB (5828113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d505f890009c6917cb4eeb7416a8d776e478f7385e6724f27bc7e577499ec5ff`  
		Last Modified: Wed, 24 Apr 2024 23:17:13 GMT  
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
$ docker pull postgres@sha256:0df1e98bb50a0fa09cdcba87af1512d093d58af7eb265d9745f74ecd653886d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.1 MB (147121959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c826b91a98895a03625cfedd3a29c6de2e929fe2aaba27b5c63c87bf7627608`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 24 Apr 2024 03:39:20 GMT
ADD file:51089e94fd65259117206f5ee6b1fd709e8c1754176d4f625ae49abbee751047 in / 
# Wed, 24 Apr 2024 03:39:20 GMT
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
	-	`sha256:112c04b2ac24eb2c6dfef961130b9b3d298e6d4b8e125bbebaa1137d773f7d7d`  
		Last Modified: Wed, 24 Apr 2024 03:44:22 GMT  
		Size: 32.4 MB (32424773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cbde9ff33fb973f4f464cf3a2100b1d8a650eda51426837a60657ebb523a00`  
		Last Modified: Thu, 09 May 2024 22:04:13 GMT  
		Size: 1.7 KB (1679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efde9a8a667dc785d3f81de5f93f6f66ca42039e94f4a4102ad708d0e5d20fc6`  
		Last Modified: Thu, 09 May 2024 22:04:13 GMT  
		Size: 4.7 MB (4719579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198d3f071218414ed413ca8362b3b6eb6fef7c682ce65abe479c145be219f325`  
		Last Modified: Thu, 09 May 2024 22:04:13 GMT  
		Size: 1.4 MB (1449286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7160e2eef5800ea5844c77160fc06b79cd0042fb731d88ecc562a7c396af28f1`  
		Last Modified: Thu, 09 May 2024 22:04:14 GMT  
		Size: 8.0 MB (8045678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b61fa23f0484fc866adf96f0860173f39f3daf1536698ffdeca5dc452bc60a2`  
		Last Modified: Thu, 09 May 2024 22:04:14 GMT  
		Size: 1.0 MB (1028917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea0e94307aebe54d000057f1677ee1a5d088a16d4d81adb4edf0543376feffa`  
		Last Modified: Thu, 09 May 2024 22:04:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41c5e6bbed4bff8975a747597ab443a474218296244e90d3aa2761de6378147`  
		Last Modified: Thu, 09 May 2024 22:04:14 GMT  
		Size: 3.1 KB (3146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c89e053f07fb30b66decb7bab751c9080e5a808d0b1cfedaf74fda0a69ecfc`  
		Last Modified: Thu, 09 May 2024 22:04:18 GMT  
		Size: 99.4 MB (99433849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c740cac479996c4caa860ac619ca7605deb035200629d5b93d09caf8482380`  
		Last Modified: Thu, 09 May 2024 22:04:15 GMT  
		Size: 9.0 KB (9023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ebb689f7fc341a1d5c451aa9b44b6f81acbd2f64ba0538b46e4a7dff49171d`  
		Last Modified: Thu, 09 May 2024 22:04:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735260281b1502b27a0054013e5ce8a4c06fe50532aad9f4b3cb6f440d9cceb1`  
		Last Modified: Thu, 09 May 2024 22:04:16 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d537750cb1e5e9ac337d3671a4c94399b276e209889f4a4b824cdbf451246b`  
		Last Modified: Thu, 09 May 2024 22:04:17 GMT  
		Size: 5.4 KB (5426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1e2aa9b3c43a58396d8cb9ad2df97a0a68007ef4c7406eaffeefebff22dd15`  
		Last Modified: Thu, 09 May 2024 22:04:17 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:fb22476d1af352f872e6660a1786abaf4f31858aa2499ca4d79b43df6b48c855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5881303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9521bf3e995d5530ceb88906dc95f1b1a8634778c5dab901daa4220057e909c`

```dockerfile
```

-	Layers:
	-	`sha256:1d706905fed9f10aeb06d352813ee95f1e5abc50ab5df041d9a09c47145f4dab`  
		Last Modified: Thu, 09 May 2024 22:04:13 GMT  
		Size: 5.8 MB (5827303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbe51a0031a0d0865514d6dc415d4ac66bfd337cc56ba270de8dc3f83c553c5f`  
		Last Modified: Thu, 09 May 2024 22:04:13 GMT  
		Size: 54.0 KB (54000 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bullseye` - linux; mips64le

```console
$ docker pull postgres@sha256:777a8131d9dda5c5004d6853553ff650b45d4183f2edff2cb46030a2c07119c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 MB (134378605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b17bbc3a69bd7e0c5489edf919190d189859dfc80fb284dcb4ce96da52fe2bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 21 Feb 2024 00:46:13 GMT
ADD file:87680940dfe26d5f4583964a639405d4e00c6a3f72863f7b7e18eca764a73c67 in / 
# Wed, 21 Feb 2024 00:46:13 GMT
CMD ["bash"]
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV GOSU_VERSION=1.17
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV LANG=en_US.utf8
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_MAJOR=12
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_VERSION=12.18-1.pgdg110+2
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 21 Feb 2024 00:46:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Feb 2024 00:46:13 GMT
STOPSIGNAL SIGINT
# Wed, 21 Feb 2024 00:46:13 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 21 Feb 2024 00:46:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2d257022fa7c7f0c7879f59891b7e4277d67c9114b820f229207724d5e65d6cf`  
		Last Modified: Wed, 24 Apr 2024 03:26:43 GMT  
		Size: 29.7 MB (29652163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0f690b15cb742be61ecdd9d9219b2232214beaaa9711968a525df49a59a5fd`  
		Last Modified: Thu, 25 Apr 2024 18:31:52 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f84ca1aab3523057834d224fad6ba16505e3330b66b320c6d558d95b54a6db3`  
		Last Modified: Thu, 25 Apr 2024 18:31:52 GMT  
		Size: 4.3 MB (4305976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065376357491bbd2ede5fb94f2c0f2663a1cd5770fc3ecee785f31b4cfa3677d`  
		Last Modified: Thu, 25 Apr 2024 18:31:52 GMT  
		Size: 1.4 MB (1360866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9911938090c605e0bd876986529a710d553a6132c88b3a799d8fee5e1d66ec36`  
		Last Modified: Thu, 25 Apr 2024 18:31:55 GMT  
		Size: 8.0 MB (8045976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2db3237fae77154f5f2bea545e5ebf16e575c4689dffaa884e7d3c0e1d86fed`  
		Last Modified: Thu, 25 Apr 2024 18:31:53 GMT  
		Size: 1.1 MB (1090261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c51eb76d2b52b0bd466928417775a65b90a0c76ca8d8d0eb0852dd6259ba894`  
		Last Modified: Thu, 25 Apr 2024 18:31:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149a451296a2ec69e3f7b33e81ba803f01b042eadac836b645de3efd45053d42`  
		Last Modified: Thu, 25 Apr 2024 18:31:54 GMT  
		Size: 3.1 KB (3146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df999b78d4b33cf8ef59b3a4c0f45862376f16fc47e9f198d0e16ec91eb05c9f`  
		Last Modified: Fri, 26 Apr 2024 01:03:26 GMT  
		Size: 89.9 MB (89903466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb289047129e584e53e2aa165e4d974b0f9eb481cd3c09be01eb8cae3ab8c721`  
		Last Modified: Fri, 26 Apr 2024 01:03:17 GMT  
		Size: 9.0 KB (9036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856faa35f4ff2674fb5abe2d70cbe27814f7da340a3e1849c14a476932a4dff4`  
		Last Modified: Fri, 26 Apr 2024 01:03:17 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ed36c181b915c05bbfaeeade5b98c253e985d0a09f9a75c4983024d50ffbfa`  
		Last Modified: Fri, 26 Apr 2024 01:03:17 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0ec02f66e0b01a7c62853c5c521f4433843d32462ce7e5d8b449ee39cc13bd`  
		Last Modified: Fri, 26 Apr 2024 01:03:18 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a4af84d915784d6433f0bbcb8d4d758ded1d00692b65f8155f0eab92e1a38d`  
		Last Modified: Fri, 26 Apr 2024 01:03:19 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:c83545567d9cad56c5926bf4702fe7dc88fa6ff39ddc22e9dd3c314b42c19021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 KB (53728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f5a2e490f1aec70baab54a0dc868403696030b0c31d635072434db15e93bb71`

```dockerfile
```

-	Layers:
	-	`sha256:c46d9352721c41fdb7dfaf43d25605b9045ed9e50ec26114495432a816b0bd17`  
		Last Modified: Fri, 26 Apr 2024 01:03:16 GMT  
		Size: 53.7 KB (53728 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bullseye` - linux; ppc64le

```console
$ docker pull postgres@sha256:7e729ac9f58251a229df4261c9ac78e8c2458713f4ef831c2035855a48849799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.8 MB (150814163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618eeed2937c8612eb8b2d3fb8caa8ce4217278555cf84ef72adcbd391b14d0b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:44 GMT
ADD file:19695f701b790b512ac412bc124ed3ccf6357f5d22743aa24dcfb6767ccbb2c7 in / 
# Wed, 24 Apr 2024 03:21:47 GMT
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
	-	`sha256:fa4abeac727fcd70f1806e99adfdd8ed879ac1ffc30990e111f5169e9a451eaf`  
		Last Modified: Wed, 24 Apr 2024 03:27:40 GMT  
		Size: 35.3 MB (35311725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029427aa463732d3362fbd40e396b07f3ecfb3340c996fdc67d856cb7d0115fd`  
		Last Modified: Thu, 09 May 2024 22:17:12 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ecde9077e3e03b5811c77e50cbad40c3e902a228b1cbd06a04899a36cb84b9`  
		Last Modified: Thu, 09 May 2024 22:17:13 GMT  
		Size: 5.1 MB (5138138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79239441bcfb41ecc185a79263273fdc1ba3b01b995cc5f7f8164b746db5f19b`  
		Last Modified: Thu, 09 May 2024 22:17:13 GMT  
		Size: 1.4 MB (1395169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f650dedd744b1aaf95f1cc5e84ce9dfcc3f237197844c850261a31c625cd9a`  
		Last Modified: Thu, 09 May 2024 22:17:13 GMT  
		Size: 8.0 MB (8046006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd83429485b43895d52cf83d0b26a554cc333f8fff9208466a69e25c84e1d9d4`  
		Last Modified: Thu, 09 May 2024 22:17:14 GMT  
		Size: 1.2 MB (1197798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba07924ecf76b32ac691ff0c571d9094820d94ac9f2572b21867a83e5e8c3a4`  
		Last Modified: Thu, 09 May 2024 22:17:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e918a87840dda72e46066ea1f76b7d6ea77f8b1bdb0216337ebc867b0c7720`  
		Last Modified: Thu, 09 May 2024 22:17:15 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625f5a62f3580cb935c91b76055a98cffc344b589c8aa9f11a9b6d0c5841512e`  
		Last Modified: Thu, 09 May 2024 23:32:58 GMT  
		Size: 99.7 MB (99705451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd9c08b8cccf148f03e0cb7829b83c984726b6ce81040d8c5afa5583acaceb0`  
		Last Modified: Thu, 09 May 2024 23:32:55 GMT  
		Size: 9.0 KB (9028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb7641b68d404d7be9dff55841caa04860b18889f1297a0d9c2717b857bd4b8`  
		Last Modified: Thu, 09 May 2024 23:32:55 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc5321f193c881a53b62d58369329f70e1d865d8b99dff390a2a24fa80cdc10`  
		Last Modified: Thu, 09 May 2024 23:32:55 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e471694c838c0ddce9d92346cfb581890ecd6b4ac458469d97ca944cd8d34af2`  
		Last Modified: Thu, 09 May 2024 23:32:56 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b893f83198a1a6ba0db921447deb37cfd9d75fd148497bb2c346f4fb92560a3b`  
		Last Modified: Thu, 09 May 2024 23:32:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:5689ff2714b197a061d6e79ea0826d13030931df1c641100511d2c13b0ff74bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5878684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcafcf65cc4f5531d039ce16a2e9b3c1505d26eee4793852f8dd8cbab06da47f`

```dockerfile
```

-	Layers:
	-	`sha256:702c2259c7b83947ca2234349b23b3cb4836bf5d271ea38b7cd791385ba07008`  
		Last Modified: Thu, 09 May 2024 23:32:55 GMT  
		Size: 5.8 MB (5824761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:070e20006cfd925f6834742fdce082b0be5d447f39761d89f62880d1da62e4f3`  
		Last Modified: Thu, 09 May 2024 23:32:55 GMT  
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
