## `postgres:14-bullseye`

```console
$ docker pull postgres@sha256:4183e0dfe6457a779c2b0a37708568c690978d9d19557b12e7a76c020a99a962
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

### `postgres:14-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:2770274cc38de013028e88060167d4e8e03eeee2a60ce851675490a16d32582c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137677169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7ef9e2f2bbf583b504d9816b36f5107f44e92731bcd34d716c2a9948f3f8de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 10 Aug 2023 18:35:14 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Thu, 10 Aug 2023 18:35:14 GMT
CMD ["bash"]
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
ENV GOSU_VERSION=1.16
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8 # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
ENV LANG=en_US.utf8
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
ENV PG_MAJOR=14
# Thu, 10 Aug 2023 18:35:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 10 Aug 2023 18:35:14 GMT
ENV PG_VERSION=14.9-1.pgdg110+1
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 10 Aug 2023 18:35:14 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA" # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 10 Aug 2023 18:35:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Aug 2023 18:35:14 GMT
STOPSIGNAL SIGINT
# Thu, 10 Aug 2023 18:35:14 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 10 Aug 2023 18:35:14 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b084488d29d065787917d33a5fcb6e37315a75ef0589298b8f782dd5c97d74`  
		Last Modified: Wed, 11 Oct 2023 20:03:34 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991ad90d690fc938764cdfc6a85e28fcf30eeed1cc2ae8e3e16f5feb742e7af0`  
		Last Modified: Wed, 11 Oct 2023 20:03:34 GMT  
		Size: 4.2 MB (4207541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef5c98dcbde248f48a7ad8a57623db27212cc3a66b45845f285b7a171d35171`  
		Last Modified: Wed, 11 Oct 2023 20:03:34 GMT  
		Size: 1.5 MB (1472467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91bd8ef63484c7038174dcac5f6662d1e72a211ecbdf51bb8e21ea50f6eb884a`  
		Last Modified: Wed, 11 Oct 2023 20:03:34 GMT  
		Size: 8.0 MB (8045205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b5ea30461cad62b3778313551c2a86b3aea15e55036fa30289250d703de9ab`  
		Last Modified: Wed, 11 Oct 2023 20:03:35 GMT  
		Size: 1.0 MB (1037471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7738c3d445bfe1dee15915cfc13ccd59a8b2f3a9785c91fc9d2d01c1ba8bcbe1`  
		Last Modified: Wed, 11 Oct 2023 20:03:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8b6e1ab70649be4937071434342e2138a71d5171e792c5d97654b237a27528`  
		Last Modified: Wed, 11 Oct 2023 20:03:35 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ab10bee7bac027e8cf21f73f55960279e1d285ad77114b0e51f4b994aee4a3`  
		Last Modified: Wed, 11 Oct 2023 20:03:41 GMT  
		Size: 91.5 MB (91477064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c948c1cafb7494278930addabac8c7baba4988958f88c238d4cfb1219245913b`  
		Last Modified: Wed, 11 Oct 2023 20:03:36 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24199580f385abb6f4208088118b952fd3dc874971aff695f06ff65541ffc22a`  
		Last Modified: Wed, 11 Oct 2023 20:03:36 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6f1718f269b50d3bc4cb3e250627ac78efccc34db93229fab2011c532f9718`  
		Last Modified: Wed, 11 Oct 2023 20:03:39 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d0b86602e693b6f878c000f3ebc9b235b645462833a002e412ff616498b660`  
		Last Modified: Wed, 11 Oct 2023 20:03:37 GMT  
		Size: 4.8 KB (4783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:924ccb42ae665e1162a66b0b71c62a1c3e234844c9fc85fea192c262b0f2bd24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4998631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:811224dbdbdc51b94d180897fc6218c0f90a27a700d1d430ce44d9f23a1c4c25`

```dockerfile
```

-	Layers:
	-	`sha256:aac231303ddee94d3f0bbf14c9b04e526219c1299c92518a0455a2385b1666d7`  
		Last Modified: Wed, 11 Oct 2023 20:03:34 GMT  
		Size: 4.9 MB (4948607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72e5f434950a8facdb1c1e10d9d4bfe8452f3ceddb5c254786930c8f9d90e515`  
		Last Modified: Wed, 11 Oct 2023 20:03:34 GMT  
		Size: 50.0 KB (50024 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; arm variant v5

```console
$ docker pull postgres@sha256:a898af1634c984bd6e34bd7f5a0eddf5db288cbd74a57e2e349812352ca1f33e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130881868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b6a06637313e40f2800e198c73f07697c0593a2f939b834519faf9a80a8527`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 10 Aug 2023 18:35:14 GMT
ADD file:01d6efe5a08019fcf00cfd0af4d6d61c6d4e43fd98cbb0054e82e8a78275573f in / 
# Thu, 10 Aug 2023 18:35:14 GMT
CMD ["bash"]
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
ENV GOSU_VERSION=1.16
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8 # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
ENV LANG=en_US.utf8
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
ENV PG_MAJOR=14
# Thu, 10 Aug 2023 18:35:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 10 Aug 2023 18:35:14 GMT
ENV PG_VERSION=14.9-1.pgdg110+1
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 10 Aug 2023 18:35:14 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA" # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 10 Aug 2023 18:35:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Aug 2023 18:35:14 GMT
STOPSIGNAL SIGINT
# Thu, 10 Aug 2023 18:35:14 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 10 Aug 2023 18:35:14 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5419c984dacdb9784c03bde904accd013b4e056c627102949c262726f4cae135`  
		Last Modified: Wed, 11 Oct 2023 17:41:31 GMT  
		Size: 28.9 MB (28921245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa39e72e06193c4a93892a4a95c1c4ff64206ae694f4efd507d333d403fe730`  
		Last Modified: Thu, 12 Oct 2023 11:39:13 GMT  
		Size: 1.7 KB (1679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712888ca43f3cb8fe52d49b87a8b2a64c8403746a86525b805b110fe16ab256e`  
		Last Modified: Thu, 12 Oct 2023 11:39:14 GMT  
		Size: 3.9 MB (3889283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4979b28d9ef24dbd33ca483de78e5829e3ba4bee87ade11ae61dfa372102724`  
		Last Modified: Thu, 12 Oct 2023 11:39:14 GMT  
		Size: 1.4 MB (1449967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e2edc561cbefe35b8ab9dd2e786c28d22d2e39889c23cf3e0a482b0d88cc1f`  
		Last Modified: Thu, 12 Oct 2023 11:39:15 GMT  
		Size: 8.0 MB (8045211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2099ee510f652639b5ea11ce8a3604c79a37fbe11be4b9b312cb5286c54db58d`  
		Last Modified: Thu, 12 Oct 2023 11:39:15 GMT  
		Size: 1.0 MB (1033898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50e406d8a62e26577c8ae1b023ca618d0e44a211232228ca0c4645a12b98872`  
		Last Modified: Thu, 12 Oct 2023 11:39:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53cb1acdcb1303605c510e64ade8c16692fda2c3ba070d84363f0c8cfc154a2`  
		Last Modified: Thu, 12 Oct 2023 11:39:16 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038cb75a9baa904ba0bcd354fc3a5d22a418218df4c3d82c7307bf5a152affd1`  
		Last Modified: Thu, 12 Oct 2023 12:44:10 GMT  
		Size: 87.5 MB (87522712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6482fe6b2be061a26eeac1d9098767d4efe9162af3455d7529980b34ba1deaf9`  
		Last Modified: Thu, 12 Oct 2023 12:44:04 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab76aeda7c441a77e99f9cd3667b113419cfa80c42b0f687b0e3379a0c5f5893`  
		Last Modified: Thu, 12 Oct 2023 12:44:04 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99030ffea66524dc811c5c58ac5db1fc8a4f0268c1fedf95cc55621d74990d48`  
		Last Modified: Thu, 12 Oct 2023 12:44:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6217147cc02ee20d8e8bceae5afb8940e7bbbf7bdc8baa719b27bd654e164fa3`  
		Last Modified: Thu, 12 Oct 2023 12:44:05 GMT  
		Size: 4.8 KB (4785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:4be90386566ccf528991198f55bc31cbacaf93eba09cb99f85a292ccab35a072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 KB (49826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b1f2f399e9222ec0a5f3310aab8801b1b3c16a69e307ff2a2bf67cce859c93`

```dockerfile
```

-	Layers:
	-	`sha256:e47c16ddcca262141a7ac434312bf939c3105ff06ac96648a70223487cfe0fe9`  
		Last Modified: Thu, 12 Oct 2023 12:44:04 GMT  
		Size: 49.8 KB (49826 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:dd78384a24547c1664f644da52f3adb100e33815989c5d2b76e6433e6450a3fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125530724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98b03f3d66b8bb51ec7fc59ba2681961c4d4d02b32eb0702aeb0692cc5bb8acc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 10 Aug 2023 18:35:14 GMT
ADD file:0d1753bfedd7193184780166819d0407867a22d82804c0045274f1f13afecac0 in / 
# Thu, 10 Aug 2023 18:35:14 GMT
CMD ["bash"]
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
ENV GOSU_VERSION=1.16
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8 # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
ENV LANG=en_US.utf8
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
ENV PG_MAJOR=14
# Thu, 10 Aug 2023 18:35:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 10 Aug 2023 18:35:14 GMT
ENV PG_VERSION=14.9-1.pgdg110+1
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 10 Aug 2023 18:35:14 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA" # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 10 Aug 2023 18:35:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Aug 2023 18:35:14 GMT
STOPSIGNAL SIGINT
# Thu, 10 Aug 2023 18:35:14 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 10 Aug 2023 18:35:14 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bb9c59b28e9fb9c31ffdb002ca9a6656677eee093c8093fcbea8818e927df70a`  
		Last Modified: Wed, 11 Oct 2023 17:47:06 GMT  
		Size: 26.6 MB (26579008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9068411873aad6400bd295ce3c9c7615bb6257f3b060c0f1fc34bcb50f8bf21d`  
		Last Modified: Thu, 12 Oct 2023 19:10:06 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4750f4a9686081f92d8054512c1471329d5326ef79ed1c5efe80edca386cd44`  
		Last Modified: Thu, 12 Oct 2023 19:10:07 GMT  
		Size: 3.5 MB (3509896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fe86832a3034209b008abcdb414302ec2070eda610180c13f76f530190fdec`  
		Last Modified: Thu, 12 Oct 2023 19:10:07 GMT  
		Size: 1.4 MB (1440047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13825c0974702ea42928129106f722061873a4abc5a7fcf312f3a89ad56fce38`  
		Last Modified: Thu, 12 Oct 2023 19:10:09 GMT  
		Size: 8.0 MB (8045175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15702f5c7849e612b622235b1a9a828d2774452e6970b395b7a04f51998945dd`  
		Last Modified: Thu, 12 Oct 2023 19:10:08 GMT  
		Size: 907.8 KB (907773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d313a66e66cb3c84dd849228ca8ce662d61f4d66e252f1beb4119fe71b9211`  
		Last Modified: Thu, 12 Oct 2023 19:10:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e37a96c90f46ce7575d15e600aa2987758b2c5db2b8a9e4fd30b9c070c5673`  
		Last Modified: Thu, 12 Oct 2023 19:10:10 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e48a3e5dad7a968f715601cf85c25153b28fc44e355a81e1f44177b1767851`  
		Last Modified: Thu, 12 Oct 2023 20:18:31 GMT  
		Size: 85.0 MB (85029269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75488cc38532bebb715e7f65ae85cdd02211d1c861744b4e0c0e8cb7583d8b44`  
		Last Modified: Thu, 12 Oct 2023 20:18:24 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db0147eb9ec579a1f0d9e77cba730968e454133efed4e775fb873f63030f363`  
		Last Modified: Thu, 12 Oct 2023 20:18:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25150f353433130023f84ccaffede6518ff84b9e3668fe672f47147a0a3b5d1`  
		Last Modified: Thu, 12 Oct 2023 20:18:25 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06dfc449b71e746e5c2e5d189b7b9d723313a83afabcf7de2e096a9cb1c1bb88`  
		Last Modified: Thu, 12 Oct 2023 20:18:25 GMT  
		Size: 4.8 KB (4788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:72c67eee3feefcd54dc6ec415d01c5f6a9cbf10e60eb3880cbb2d928abfa765f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5014925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db5447f9f22e0c03b0de52a4b9dc10961a712ef12724cffdee05c552a2f4ab97`

```dockerfile
```

-	Layers:
	-	`sha256:d88e41fe9f162a161e951de76bb4bee427373efcc24053269e16affe8ef47ece`  
		Last Modified: Thu, 12 Oct 2023 20:18:24 GMT  
		Size: 5.0 MB (4964893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e423b697b12177def7b856c4a10ee93d190d4a9c6031d439df6bf27df0038904`  
		Last Modified: Thu, 12 Oct 2023 20:18:23 GMT  
		Size: 50.0 KB (50032 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:fc15e932880851b91c290a968cca0b7654f05beebe32f147a28cdc3071712cf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132786347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ada7fb74d7398ae04393df2e6750d76aa41039ebe01420f52b1520545eae5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 10 Aug 2023 18:35:14 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Thu, 10 Aug 2023 18:35:14 GMT
CMD ["bash"]
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
ENV GOSU_VERSION=1.16
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8 # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
ENV LANG=en_US.utf8
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
ENV PG_MAJOR=14
# Thu, 10 Aug 2023 18:35:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 10 Aug 2023 18:35:14 GMT
ENV PG_VERSION=14.9-1.pgdg110+1
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 10 Aug 2023 18:35:14 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA" # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 10 Aug 2023 18:35:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Aug 2023 18:35:14 GMT
STOPSIGNAL SIGINT
# Thu, 10 Aug 2023 18:35:14 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 10 Aug 2023 18:35:14 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3ff771def927f093d5cc616091c5539f37a8b0de84b60aaa56c91249fcf525`  
		Last Modified: Thu, 12 Oct 2023 16:58:45 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7317a2026c07cdafdc60688a261cdcfc8df77cb91c3e3c20842df1cbeee7ba5b`  
		Last Modified: Thu, 12 Oct 2023 16:58:46 GMT  
		Size: 4.2 MB (4209380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe90c16a41a91765b7306289bce9c685bd727bd0f070a33c93b9c89cb91fbc62`  
		Last Modified: Thu, 12 Oct 2023 16:58:45 GMT  
		Size: 1.4 MB (1404387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2891aa9a8d9ed3643130aabdab4999c4b8d141e76951f1c3bfeec15982db5d`  
		Last Modified: Thu, 12 Oct 2023 16:58:47 GMT  
		Size: 8.0 MB (8045182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03cdd3e15684a5ee8e3d3603b87a72c606be98a36e41e3032dc3bb09b343a831`  
		Last Modified: Thu, 12 Oct 2023 16:58:47 GMT  
		Size: 1.0 MB (1025926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621ae45f35e5a9a2017b0cbdffe8a2f82a266900c8e0008be54d9c19d9ee369b`  
		Last Modified: Thu, 12 Oct 2023 16:58:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf98eff2f6bbd9d2c42178020852f6be97591005572dd2eb2f4917b91e0e388`  
		Last Modified: Thu, 12 Oct 2023 16:58:48 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8b72d537ee0a72a65a22b9e09e083cc9cc8767cc5f1bc860d650b2ab1c9794`  
		Last Modified: Thu, 12 Oct 2023 21:05:18 GMT  
		Size: 88.0 MB (88017823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8487311b7a67c375b48a721b062d32b83812be2018546b30baf03a203417f9fd`  
		Last Modified: Thu, 12 Oct 2023 21:05:12 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1739fe5c113c0fe4e06c0a4de3d17445621b08fcfc6b422f0a3a5c69931df5`  
		Last Modified: Thu, 12 Oct 2023 21:05:12 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558f368bb012bee50c4250d6e2d38a70076a849f1647ea312d3fc03a0779b563`  
		Last Modified: Thu, 12 Oct 2023 21:05:12 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01070433b5b65cb99c36719708ce66549ebce6d11fe1aa3901208ca97027c5f9`  
		Last Modified: Thu, 12 Oct 2023 21:05:13 GMT  
		Size: 4.8 KB (4788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:4d965d70a466da18727f4d36f0a922c88f2be0d77b3485945bd64c0ff1238e0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5006223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1323ae5d7dac8faff5f05f684d58bc629fd838ce13620f30e3cd8c4195a6ee`

```dockerfile
```

-	Layers:
	-	`sha256:77d256c1f9b4d95628a44a68a5d293c33770898e8278d764f1fa76de63d4cdf6`  
		Last Modified: Thu, 12 Oct 2023 21:05:12 GMT  
		Size: 5.0 MB (4956360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:153758ecf32ceedfe2d7ead51527670d60696d3830dc5d974f817e542d693ce0`  
		Last Modified: Thu, 12 Oct 2023 21:05:12 GMT  
		Size: 49.9 KB (49863 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:ad2a39507a7435dd8c34664751978e8f482b83c16bf20b9e24627b5c10ac9a65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139670719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:994abe9a771470ae9ea3ba569776cb04d4950670f6dc8f21aef0a264541048c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 10 Aug 2023 18:35:14 GMT
ADD file:ec6d51df021532be6c52d882f60a33d5cce8c3bff039efe8b98e923f2658ba45 in / 
# Thu, 10 Aug 2023 18:35:14 GMT
CMD ["bash"]
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
ENV GOSU_VERSION=1.16
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8 # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
ENV LANG=en_US.utf8
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
ENV PG_MAJOR=14
# Thu, 10 Aug 2023 18:35:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 10 Aug 2023 18:35:14 GMT
ENV PG_VERSION=14.9-1.pgdg110+1
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 10 Aug 2023 18:35:14 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA" # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 10 Aug 2023 18:35:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Aug 2023 18:35:14 GMT
STOPSIGNAL SIGINT
# Thu, 10 Aug 2023 18:35:14 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 10 Aug 2023 18:35:14 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f088164df28359c53d5766709e069e084073984ecf4688687b4c7c529a8926a5`  
		Last Modified: Wed, 11 Oct 2023 17:46:21 GMT  
		Size: 32.4 MB (32402649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9a9b11eca6d6431e9530877801dc13dd50ffcf5204f1d1c356dab97b84b5413`  
		Last Modified: Wed, 11 Oct 2023 19:17:17 GMT  
		Size: 1.7 KB (1679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9421485f6aba1c431899cd296f7798a3ee99a85d33a70e7f7b84d751db1a930b`  
		Last Modified: Wed, 11 Oct 2023 19:17:17 GMT  
		Size: 4.6 MB (4607418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dfa0accb6b06c43edb1860a81ba22c21d25e2e00ccac4010490c6c349df0ee`  
		Last Modified: Wed, 11 Oct 2023 19:17:17 GMT  
		Size: 1.4 MB (1448266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156eaa97bc127dc9d887d9e43a92f8cb4d3e116826e4d49500874c044a7d0f9c`  
		Last Modified: Wed, 11 Oct 2023 19:17:17 GMT  
		Size: 8.0 MB (8045180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037ec4bbb05f2f3349a8b35acbd6629112fef8659558c1958a172feeff91cc41`  
		Last Modified: Wed, 11 Oct 2023 19:17:18 GMT  
		Size: 1.0 MB (1027976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861a5f0ae63fd9367b8f051ee96f082518bf0e0ea70da65175145221d54ceee5`  
		Last Modified: Wed, 11 Oct 2023 19:14:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3507e192e89d86686e9a1be11ecac0971f138866f9e0b8619c71d272ab8ca1`  
		Last Modified: Wed, 11 Oct 2023 19:17:18 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ca664e69564a93948b981f7cda28672442ba352029dcbaaa3debcaecbf41b5`  
		Last Modified: Wed, 11 Oct 2023 19:17:23 GMT  
		Size: 92.1 MB (92119676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3713b69f8c157716254a676ec216603ff15c4d1f9fbb9947888ba8947544b200`  
		Last Modified: Wed, 11 Oct 2023 19:17:18 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7daefaa8a0475c714d4701e57882192b30a76aa01228bd67aae22ef2a76b0d3b`  
		Last Modified: Wed, 11 Oct 2023 19:17:19 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1f1e0a8f19b9977ec7ef153f3a71fe05747226bb9194683074ab038e73ae2d`  
		Last Modified: Wed, 11 Oct 2023 19:17:19 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4c21345951a2a31cbacac9ca109c9bea7a5d11ccc451b4c7f63904ece80ef4`  
		Last Modified: Wed, 11 Oct 2023 19:17:19 GMT  
		Size: 4.8 KB (4791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:d3f704488250a814bd30ced084b92d2133219cd0ae6db3a3e29b0ee20e31bdbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 KB (49770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc02f25bf9c5d4806be8f3877ae6c8b9aab9f8e134159618fb83322edeb64262`

```dockerfile
```

-	Layers:
	-	`sha256:cc16afa82f45cbdd901adad3b87bec5d117b792d612e71c0971c1eff2487a2ba`  
		Last Modified: Wed, 11 Oct 2023 19:17:16 GMT  
		Size: 49.8 KB (49770 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; mips64le

```console
$ docker pull postgres@sha256:764a1fd60ffd73e1d4b80d8e9c795cac8cd17d114693c8914bdb04f347e4748e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132425758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da14fa4f59285edb29be3191a806512fdfff89901cd6a2ad3292f456a3207639`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 10 Aug 2023 18:35:14 GMT
ADD file:86abe5722ef15fa073bf5b38a44ec0524e99a0cf1a6dbf0c6510fb1926c7abf8 in / 
# Thu, 10 Aug 2023 18:35:14 GMT
CMD ["bash"]
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
ENV GOSU_VERSION=1.16
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8 # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
ENV LANG=en_US.utf8
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
ENV PG_MAJOR=14
# Thu, 10 Aug 2023 18:35:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 10 Aug 2023 18:35:14 GMT
ENV PG_VERSION=14.9-1.pgdg110+1
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 10 Aug 2023 18:35:14 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA" # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 10 Aug 2023 18:35:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Aug 2023 18:35:14 GMT
STOPSIGNAL SIGINT
# Thu, 10 Aug 2023 18:35:14 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 10 Aug 2023 18:35:14 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7ed8396e400b964776cd6b7c617ad90d450d2ece3dbd9e26e9c264e98e7145ea`  
		Last Modified: Wed, 11 Oct 2023 18:02:07 GMT  
		Size: 29.6 MB (29636021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b008e488c7d4ee897ad11bd699878f86490e0474f62c64ac40471668858e050b`  
		Last Modified: Fri, 13 Oct 2023 11:54:19 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f03a676413bb8d48d9d914e8d87292411e808f14348b534310007cb2b5fad9`  
		Last Modified: Fri, 13 Oct 2023 11:54:20 GMT  
		Size: 4.2 MB (4196256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f41f2a2594d3c210d1d53011b1edc77aaac0404df9a1799a76d4d65178a099d`  
		Last Modified: Fri, 13 Oct 2023 11:54:20 GMT  
		Size: 1.4 MB (1359938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585a591333b0a0f53fc80eb815fdd55339e9075bb02c03c630bcd56da6283f3a`  
		Last Modified: Fri, 13 Oct 2023 11:54:22 GMT  
		Size: 8.0 MB (8045432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47563d4a845a70efccd2fa326ec2f84ae675602956b4fa6841c7cd1808eac7e4`  
		Last Modified: Fri, 13 Oct 2023 11:54:21 GMT  
		Size: 1.1 MB (1089514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d93f4c0c4d8842fc172b1b64e352a70e544455d64575be0f4c240c4b2dfe361`  
		Last Modified: Fri, 13 Oct 2023 11:54:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0795e78108b2b9b204f919bbd8c91454c083917772fc2b8e4286e06299246c12`  
		Last Modified: Fri, 13 Oct 2023 11:54:23 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb07ec4b6685c15c23122069a74245338a9bfa4c347ffa1869e8876d5de9da5`  
		Last Modified: Fri, 13 Oct 2023 21:08:21 GMT  
		Size: 88.1 MB (88079025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758a6f9395520570993692f078a0fdc28c3ed53684cdf65ac94424714a4e8415`  
		Last Modified: Fri, 13 Oct 2023 21:08:13 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58757ac1b5eb44439a9c33df9bf348a55c2fd69f8fd88828822397fbe1408a5`  
		Last Modified: Fri, 13 Oct 2023 21:08:13 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbd16036a8691330b72ab6ea06b17ba97a8c98159469dd04aa3d59d1ebde4b3`  
		Last Modified: Fri, 13 Oct 2023 21:08:13 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2633ee4cc2b7c2aac112cd09f62bda2c77636e08318d8b4f3dc4130462f0c140`  
		Last Modified: Fri, 13 Oct 2023 21:08:14 GMT  
		Size: 4.8 KB (4787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:bb065e19fc7380db79ce8fbc23b46d960027801549cac007bd5e7f579949e4a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 KB (49711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d355ce7ab21681a6f5dfbdc6bae3e2e288420122dc849ad287941e2ffd4730d5`

```dockerfile
```

-	Layers:
	-	`sha256:9570ced02d45fd07f15c21bc9252be5968f42ce0e85acbc50420655a2d173970`  
		Last Modified: Fri, 13 Oct 2023 21:08:12 GMT  
		Size: 49.7 KB (49711 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; ppc64le

```console
$ docker pull postgres@sha256:2cfd172cdf5f6fc3f237f7cd9c4fe5b3f0767c2afdf16459b7f5d82599a5be31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146751585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2b78da2213ef9f2783b8a7e295beb0b4a514f9b3b49f9a36a1eaa52cfc4604`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 10 Aug 2023 18:35:14 GMT
ADD file:96450fb62af4cd68105cbbf612cb5d2f79139cc9416835b6c2fdf40727635939 in / 
# Thu, 10 Aug 2023 18:35:14 GMT
CMD ["bash"]
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
ENV GOSU_VERSION=1.16
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8 # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
ENV LANG=en_US.utf8
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
ENV PG_MAJOR=14
# Thu, 10 Aug 2023 18:35:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 10 Aug 2023 18:35:14 GMT
ENV PG_VERSION=14.9-1.pgdg110+1
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 10 Aug 2023 18:35:14 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA" # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 10 Aug 2023 18:35:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Aug 2023 18:35:14 GMT
STOPSIGNAL SIGINT
# Thu, 10 Aug 2023 18:35:14 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 10 Aug 2023 18:35:14 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:cde4df93466f96fbb1bbc513d09d354ea1e58d3e619c19fcf9120dbba87405ea`  
		Last Modified: Wed, 11 Oct 2023 17:50:55 GMT  
		Size: 35.3 MB (35293715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b9accccc56d67302b8282298cf43134bf1b6b22e19aa37eac676d9a26722bfc`  
		Last Modified: Fri, 13 Oct 2023 01:17:28 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1089fd3e26d899e532efbef9567a350913ebb264c3ba51e0373d090b5afdc19`  
		Last Modified: Fri, 13 Oct 2023 01:17:29 GMT  
		Size: 5.0 MB (5016026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f057edb42f8a0e92b99ef76189c94833e644d8fa34a000bc93747f36bf04972d`  
		Last Modified: Fri, 13 Oct 2023 01:17:29 GMT  
		Size: 1.4 MB (1394092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5da68b7d5d20015c8ca7a56e22763f89fb058d4103aa6fcec648b387de37d44`  
		Last Modified: Fri, 13 Oct 2023 01:17:30 GMT  
		Size: 8.0 MB (8045327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6f4b040ea332c453b7edbdd6aaec76217214034d2c9246c7405facacbd9e5f`  
		Last Modified: Fri, 13 Oct 2023 01:17:31 GMT  
		Size: 1.2 MB (1196970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9904b269eb0444c7988db66c03e1de71b34aabfcabff07fc5d1b41ee5ba931`  
		Last Modified: Fri, 13 Oct 2023 01:17:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e9270c34e21ccc313eaa1cca93c472787b31139910b55ca4a415772ef8e43f`  
		Last Modified: Fri, 13 Oct 2023 01:17:31 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa21a5e1f2d9816521ffdadeed145f1fe896ddc9487e49c02bd2eb85c28d740b`  
		Last Modified: Fri, 13 Oct 2023 01:24:22 GMT  
		Size: 95.8 MB (95785891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327ca8809708887091a45b946023d376659db3a69bf838b86c91d1840a38ec4c`  
		Last Modified: Fri, 13 Oct 2023 01:24:16 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcedd0d8f3c7f12904feec0c866b3c63239ac54545938cf34c9f2b14c06b301`  
		Last Modified: Fri, 13 Oct 2023 01:24:16 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b1af6d80a172edc05aba0b52e6e8e4ae2e816ba74f91b970c20c0464111260`  
		Last Modified: Fri, 13 Oct 2023 01:24:16 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3a8cb52178c97da4003f173a65d2762ad4d4e005d66b2107cec35736580469`  
		Last Modified: Fri, 13 Oct 2023 01:24:17 GMT  
		Size: 4.8 KB (4788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:df660a8bf632a47e9b1bffc8315c73e12538086c8dc596162326a2f0ca8401f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5019721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a6f02d82f7b94230f61ed6531b87e43192d9a7497e324de779d6c5da2fcaaed`

```dockerfile
```

-	Layers:
	-	`sha256:325c0e859c054acf1e46bce3926a133ba3da928cad1c76decaa5685bb5819aba`  
		Last Modified: Fri, 13 Oct 2023 01:24:16 GMT  
		Size: 5.0 MB (4969819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4c23fdf1269dc1157759e7fdfba3aafade04833955b2ad0e68b2f8c365aa33e`  
		Last Modified: Fri, 13 Oct 2023 01:24:16 GMT  
		Size: 49.9 KB (49902 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; s390x

```console
$ docker pull postgres@sha256:85b5f889375de394aafb7059925700d55d6b77d322f3cc7c8da3fb6cb18772c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.3 MB (141323078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37cf407c10446bc5b0bf7a4f616e07c3bef786879a4e98bffdbe03771ad4390e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 10 Aug 2023 18:35:14 GMT
ADD file:0cfc89fea6da8404b2bccfb0c408dde9e7497e8a93304c4ced9e51bd2b3a319a in / 
# Thu, 10 Aug 2023 18:35:14 GMT
CMD ["bash"]
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
ENV GOSU_VERSION=1.16
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8 # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
ENV LANG=en_US.utf8
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
ENV PG_MAJOR=14
# Thu, 10 Aug 2023 18:35:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 10 Aug 2023 18:35:14 GMT
ENV PG_VERSION=14.9-1.pgdg110+1
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 10 Aug 2023 18:35:14 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA" # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 10 Aug 2023 18:35:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Aug 2023 18:35:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Aug 2023 18:35:14 GMT
STOPSIGNAL SIGINT
# Thu, 10 Aug 2023 18:35:14 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 10 Aug 2023 18:35:14 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a12df18f4c86c0f825c6b30eb023dc9f30ba0de34f6b97dca708a7247f4f6c49`  
		Last Modified: Wed, 11 Oct 2023 17:57:36 GMT  
		Size: 29.7 MB (29656917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029f80cb736850ba17c8026acafbb79cd0ddd66e3d7ecdd91eefc30b3e359e83`  
		Last Modified: Fri, 13 Oct 2023 05:43:27 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0a7fbd651b88fdf1017a8c6220522452d9ed292c58aac9d726bda66d557517`  
		Last Modified: Fri, 13 Oct 2023 05:43:28 GMT  
		Size: 4.1 MB (4096084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be05afd754a3c2077dd01a515f3b1d7d8eea22ed5b706533acbe8ff12dfd3446`  
		Last Modified: Fri, 13 Oct 2023 05:43:28 GMT  
		Size: 1.4 MB (1438315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71150d0671d9f12bb6d2f72185f0ec0589c215aee42448de141aa48444e77522`  
		Last Modified: Fri, 13 Oct 2023 05:43:29 GMT  
		Size: 8.1 MB (8099085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d403e04c732c69e65a56717b3c095d9cacca3f12c6bfbce08470a4f1828334`  
		Last Modified: Fri, 13 Oct 2023 05:43:29 GMT  
		Size: 1.0 MB (1014304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5dc7504ba64f3f021e874f79dd38345c182aafc7918a92fe011c9a23b0c4afb`  
		Last Modified: Fri, 13 Oct 2023 05:43:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24420643e53f95befbb6422c897e9f105fa2b8cfea3279e8de078153e7d22a85`  
		Last Modified: Fri, 13 Oct 2023 05:43:30 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693537d2ce1841d99e3cf5ef619428375eeae734ec049e4f09a343f3780f27c1`  
		Last Modified: Fri, 13 Oct 2023 06:00:58 GMT  
		Size: 97.0 MB (96998808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c21d2ea04d2028d1a23d1b95eab3c3a82f561a24551ec4e02b273b6c0262e8f`  
		Last Modified: Fri, 13 Oct 2023 06:00:51 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864784accdeb7689d94f4dbd70af0e4ce1ab63a9e516b6200a8332bbcf789893`  
		Last Modified: Fri, 13 Oct 2023 06:00:51 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0078a05fd1e2b8a880c637c8320d637856baf73f1fe19cae5d04c11607a304da`  
		Last Modified: Fri, 13 Oct 2023 06:00:51 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518dc534969605d23de5723dba0219d1222b67c92a5e62ce480043e2b0221e3c`  
		Last Modified: Fri, 13 Oct 2023 06:00:52 GMT  
		Size: 4.8 KB (4790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:254cc95a460e042168d1a1612258d152a3c8a153b5ecfae9fb688ee8c596ada9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4994052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e826cc2a2a67363e3a22397b8bf037218c1ad52ab5c90f5d6804815ca0cc9919`

```dockerfile
```

-	Layers:
	-	`sha256:9a7093575a580ca29e43578038b3a030ab00f162c67d05a6fba91cf9b804ad86`  
		Last Modified: Fri, 13 Oct 2023 06:00:51 GMT  
		Size: 4.9 MB (4944196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a1ce1aa0e35dd38153c4d707d3fb371b4f2b279e0e4ecd900e9c3ad3c3d6c3b`  
		Last Modified: Fri, 13 Oct 2023 06:00:51 GMT  
		Size: 49.9 KB (49856 bytes)  
		MIME: application/vnd.in-toto+json
