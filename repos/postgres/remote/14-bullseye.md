## `postgres:14-bullseye`

```console
$ docker pull postgres@sha256:a12500903d5f3107c22f27a2743faf1b8fb93d16efff2f341a8469f627822d16
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
$ docker pull postgres@sha256:c927a75d81954e8899165aa74457b4f91645eff2819eca3a48e8f8dd48e1753d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141751683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000018281add65fd72aa3fcf08e5a278d19ff078020a92f17618346e4fc5d50b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 21 Feb 2024 00:46:13 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
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
ENV PG_MAJOR=14
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_VERSION=14.11-1.pgdg110+2
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
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225ad20506aeb01b212fbc9ce076260325c23587ddefd312a46af8ee49863b24`  
		Last Modified: Wed, 10 Apr 2024 02:55:56 GMT  
		Size: 1.7 KB (1683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5152f09be4a6bc65ace0d25147b4183fb3ec9fec9954f1aebc9bcd138dabf74d`  
		Last Modified: Wed, 10 Apr 2024 02:55:56 GMT  
		Size: 4.3 MB (4305822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1af77cc1c4cda4e5a82103e152cc45d8786e182b613fed92e33b8beb9362ff0`  
		Last Modified: Wed, 10 Apr 2024 02:55:56 GMT  
		Size: 1.5 MB (1472185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790e419330ca20a5fd9aa1070d03d4364562d8cc142bac6f2efbea5310207417`  
		Last Modified: Wed, 10 Apr 2024 02:55:56 GMT  
		Size: 8.0 MB (8044196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244abd1dd6c8cb8a43bade9271481c55fd259a9b9b47b24cb28b634fb8f69a20`  
		Last Modified: Wed, 10 Apr 2024 02:55:57 GMT  
		Size: 1.0 MB (1038385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05ed7468461037e35e04098f6411b4a2327d6c372d4138f388cc7a49b4bd774`  
		Last Modified: Wed, 10 Apr 2024 02:55:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29404eebbbb1edeca7976988676c891fb55e42c8e379a27b639f4b1ff8a0b415`  
		Last Modified: Wed, 10 Apr 2024 02:55:57 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8a0d7a4aaa67f2eb69c03b0f5ebbeb47f858127977077523c2ddcd99406b78`  
		Last Modified: Wed, 10 Apr 2024 02:55:58 GMT  
		Size: 95.4 MB (95442979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f894c80079cd5ae55c74d61cfea86bd9e5ad0f9ab9adfd8850f07c524eab4f6e`  
		Last Modified: Wed, 10 Apr 2024 02:55:58 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97a248b77d777280465571667a534ba49702342e0cc0ba5c67c5d28c267c9af`  
		Last Modified: Wed, 10 Apr 2024 02:55:58 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179e24ec1ecc978503e19acf12b12f3065cfcf2d0f1494895b97ed60036d85cf`  
		Last Modified: Wed, 10 Apr 2024 02:55:57 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964cea5278d452aa561000d7061a6c86e873627db29d3609244997d50a5db03b`  
		Last Modified: Wed, 10 Apr 2024 02:55:58 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdde9ab97e51a4c3e7a770bc49c0bba6a455566084fb2b9b870cf5393340e9fd`  
		Last Modified: Wed, 10 Apr 2024 02:55:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:d98a015786fc5a7b91658e3d3ef5fd0fc74a2bb72c31090818bc67207a17133d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5903666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a088be8a9f5364d4b66c268850e45d2bcf48ebf1376b8652b2d126563888bfa`

```dockerfile
```

-	Layers:
	-	`sha256:84bff2822f54829c057ddeb768b3cd0550da0245fd7a569155a8e3d483c2a14c`  
		Last Modified: Wed, 10 Apr 2024 02:55:56 GMT  
		Size: 5.8 MB (5849628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d755f4db71e49cb70e5bc59421a8df32ac35cd1e9e0d87eada51e56a39ba5af8`  
		Last Modified: Wed, 10 Apr 2024 02:55:56 GMT  
		Size: 54.0 KB (54038 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; arm variant v5

```console
$ docker pull postgres@sha256:4872a8a25076c71c0c43943b948b865c16a90131b94f039054710e214c3f926f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134592464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:674807626b086b67f52ae9825f1252e2744ad21671730578c2eaf00cc0fcaece`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 21 Feb 2024 00:46:13 GMT
ADD file:aeb4c3fa8d40bc17d70f21cc12bb887fee25ce28edd7cac250e250253b8d2819 in / 
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
ENV PG_MAJOR=14
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_VERSION=14.11-1.pgdg110+2
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
	-	`sha256:a106aa5ccf7f6fa63e0c6a2a69c3cda22393d46be963a8867a2894dab3644cc7`  
		Last Modified: Wed, 10 Apr 2024 00:55:28 GMT  
		Size: 28.9 MB (28930200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ce3d54ff4f6225b32945a7c96abb1492b9e155fa46f277bf38970b1adfa9d7`  
		Last Modified: Wed, 10 Apr 2024 20:14:09 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f63ad527ac2959d1b4242b380c92a884888c9c83b5a0e4b8dd27fccf7608e1a`  
		Last Modified: Wed, 10 Apr 2024 20:14:10 GMT  
		Size: 4.0 MB (3986263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7098a9b3d3577fdb72628e0f4f3be59d96b5d7493ad974c5dc9caf6858d357`  
		Last Modified: Wed, 10 Apr 2024 20:14:10 GMT  
		Size: 1.4 MB (1449279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd89c4bc2cd930e83b46c56d83d9c3fa9ef988ca626152817867c1690cda782`  
		Last Modified: Wed, 10 Apr 2024 20:14:10 GMT  
		Size: 8.0 MB (8044220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ddc40c28226c1c47c6c75af40ddfb06e3e1a6e51b7bd4374b9e770c66d9e80`  
		Last Modified: Wed, 10 Apr 2024 20:14:11 GMT  
		Size: 1.0 MB (1034887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e290977596feb34c3ac5233d90b897e4721483e5ed36f9a2714a396f5fb03d36`  
		Last Modified: Wed, 10 Apr 2024 20:14:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9ab073b68246b523aa1255967a8e4b637a89f69c43837f60154ec3f2418d91`  
		Last Modified: Wed, 10 Apr 2024 20:14:12 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7168b2974bc9672c43285719a48dd6b477189e1794d52cabd36ff86e59627c`  
		Last Modified: Wed, 10 Apr 2024 21:40:11 GMT  
		Size: 91.1 MB (91127245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b4f13f48b4514e1896a94d3403ad7fb7b4da81a45254b934151e0a39c2a5ae`  
		Last Modified: Wed, 10 Apr 2024 21:40:08 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88187c97cfa788cbb852fc00b38f7a27d169e7a0061046f557d4b1a6f4790b84`  
		Last Modified: Wed, 10 Apr 2024 21:40:08 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00407d41b0d401f66472ef74e927ea574a32469e6149b9f3cfd3f514e5a53486`  
		Last Modified: Wed, 10 Apr 2024 21:40:09 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e921b1a94389743824098876ec2cee2b453365cdd20cd29e3894d04b7198c5e0`  
		Last Modified: Wed, 10 Apr 2024 21:40:10 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfde8db075cc9136598c192e42ae8900dc601968b416ae47d4607175c70e62bd`  
		Last Modified: Wed, 10 Apr 2024 21:40:10 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:9b0629f4ee336854bbc4d2cb87055dd61095ff318aa38c764262a408dcfd16e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5913543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b12bb1b818169cc9cf9eb08b9188de0a18ae23b2ea28fe1e875a8bff816819c1`

```dockerfile
```

-	Layers:
	-	`sha256:286f1775f6b5b97cbf17bd4b88e2bcb38994ad2b5a2ee1390d5edee234dc2475`  
		Last Modified: Wed, 10 Apr 2024 21:40:09 GMT  
		Size: 5.9 MB (5859475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb035702f69ed47f24349eb245d276b3407fb5b8dfd77e1d7b7c27dab6c2c0a2`  
		Last Modified: Wed, 10 Apr 2024 21:40:08 GMT  
		Size: 54.1 KB (54068 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:f0eb8973a988e1859bbec7f4b333cd754c61cc86e5482c3a010bdc614275f1a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.7 MB (129720248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d49a62ba72bbf1b28fd3e3b88550547df06cda420df4267b746d8cb6c8ea505`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 21 Feb 2024 00:46:13 GMT
ADD file:f7685078edb9bb9e45a932713c0364f985baac4241d098518b48718ca3f587aa in / 
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
ENV PG_MAJOR=14
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_VERSION=14.11-1.pgdg110+2
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
	-	`sha256:e373dd4d84cbc3bf4d587e26357a41105c418866d41051d5ad5d54c706941e10`  
		Last Modified: Wed, 10 Apr 2024 01:05:12 GMT  
		Size: 26.6 MB (26588474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a2a214a05a73818c4a01dcd9a582b19c91f69b0375cbae58d32ed375332588`  
		Last Modified: Thu, 11 Apr 2024 06:58:26 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49252f6445d7fb96c92837deac4243293f80b292f7654ac3e2970af2993b9ea6`  
		Last Modified: Thu, 11 Apr 2024 06:58:26 GMT  
		Size: 3.6 MB (3598308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c774c90717ada2ea148026e0eb5468e6df86cdfbd828610774e26871a7ccb69b`  
		Last Modified: Thu, 11 Apr 2024 06:58:26 GMT  
		Size: 1.4 MB (1439318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7875a5749ccd93a1c8a8aae00337d52ba2c8f723fd5087cc39e46f39ec84ec`  
		Last Modified: Thu, 11 Apr 2024 06:58:27 GMT  
		Size: 8.0 MB (8044239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1afebc888792a44e7c3862d6a99fa368bf6fd6b92085213d3d5cbb5d64a0d2`  
		Last Modified: Thu, 11 Apr 2024 06:58:27 GMT  
		Size: 908.7 KB (908709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b180bea4a10ba25559672730460ccf763e0458acc5c662492bda599dcf812b8`  
		Last Modified: Thu, 11 Apr 2024 06:58:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1724913bc5f3b98bd959d5a29a198fdd455aa1365f864ab01926208dbf231bf3`  
		Last Modified: Thu, 11 Apr 2024 06:58:27 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fdc140a9b091d75e7c61df012803aeb7fa04f29b4f315e0962be11c5314c545`  
		Last Modified: Thu, 11 Apr 2024 08:29:33 GMT  
		Size: 89.1 MB (89120827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6fedfa319f067c6231bf22234c2dbb68ace02de5e9d2cbe5e4bbb414815f87`  
		Last Modified: Thu, 11 Apr 2024 08:29:29 GMT  
		Size: 9.5 KB (9536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c36e91dacf4703aeb211082647c325f3e6fd92ab5c763b494de9faf91bc0622`  
		Last Modified: Thu, 11 Apr 2024 08:29:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25211326313fd341d9e96528bf16415ab997834f091fcf2d979883c6965ecf0`  
		Last Modified: Thu, 11 Apr 2024 08:29:30 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17688eac2e081a74c6500df9c10f356d46aea435aeb28ce3ff286695f2364080`  
		Last Modified: Thu, 11 Apr 2024 08:29:30 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c06a683131588e68f972ad40281875e80f5494e64e4d463ee2c61191fcbcfe`  
		Last Modified: Thu, 11 Apr 2024 08:29:30 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:d1124e7381f0f9e8dd4761ca41482472681c8ac17b9c415494edff48c56cf2d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5913306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8263279bd88b66637d16c232aa330ebd692947c43cb317632f9148456f8e85f`

```dockerfile
```

-	Layers:
	-	`sha256:bf05ebf3b465106eded68a496ed76cfd6d1ac946001b8c917dddcc00b6fe4926`  
		Last Modified: Thu, 11 Apr 2024 08:29:29 GMT  
		Size: 5.9 MB (5859247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d102e58780cf0b29aedf14df331aa2758a4f5f60c6f830c92c1f489c792e4e0`  
		Last Modified: Thu, 11 Apr 2024 08:29:29 GMT  
		Size: 54.1 KB (54059 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:bb12454e45ce8889fc309f972c5d555a35edfadd571e0e430d5a3a91f0544fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.2 MB (138165335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:800ab67298fc5e2d3e6b51b5518a498221dd6e5d0d52313c7c6ef64487f4febd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 21 Feb 2024 00:46:13 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
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
ENV PG_MAJOR=14
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_VERSION=14.11-1.pgdg110+2
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
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23414e275c8ea999291eeb56d1fa598821a297e15b3578323281064ddcd1d6d1`  
		Last Modified: Wed, 10 Apr 2024 20:29:03 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca755ccfd7f2decbf9fccd926a0193d00945368f0cd9bb28ef49dd08a091cb2`  
		Last Modified: Wed, 10 Apr 2024 20:29:03 GMT  
		Size: 4.3 MB (4309294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbdc3bf360352dd9e29040ace90c93a8389f81b44b4450e9c1e90670f39d05be`  
		Last Modified: Wed, 10 Apr 2024 20:29:04 GMT  
		Size: 1.4 MB (1404141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab0edd30bcfa4284c1d8057d6c79887ac6958030284aa403102d28866cc25fa`  
		Last Modified: Wed, 10 Apr 2024 20:29:04 GMT  
		Size: 8.0 MB (8044212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010874b850a6c88b7c4dbce8dd6a35dd63c92684e64391f6ff66d61e8ad5c62a`  
		Last Modified: Wed, 10 Apr 2024 20:29:04 GMT  
		Size: 1.0 MB (1026631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c4076597ef85d154dca67cdd7f5cfbf81b500a96aa86e3ea6d6054a132fd11`  
		Last Modified: Wed, 10 Apr 2024 20:29:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f4baeba16740b16874d1212503e7e12004d914eea8a30a3a8ebfa546844ece`  
		Last Modified: Wed, 10 Apr 2024 20:29:05 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c77ea343b44dcc3c4935138de152c4efb28897f3380c639f5e39b296e92d8dc`  
		Last Modified: Wed, 10 Apr 2024 20:33:01 GMT  
		Size: 93.3 MB (93284386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc03eb27fa654e06b9abbcda2a891db656eb735ebbd172ad79b25ca09ebae81e`  
		Last Modified: Wed, 10 Apr 2024 20:32:58 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce16e65cb576043bf8042c5c4bb13b2c2cf78f6fc5ee516ff066ea07013d6aba`  
		Last Modified: Wed, 10 Apr 2024 20:32:58 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c9ace5e50b56609617b6d6cf7a65112b11b00a8682209b68c4af9308aa83e6`  
		Last Modified: Wed, 10 Apr 2024 20:32:59 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d0e2336143ce35b14768554315bcf9f168ad0084928307e829fe74a03263bc`  
		Last Modified: Wed, 10 Apr 2024 20:33:00 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84687d2154cb7443cefb3067e529bf6feb2196dbd72e6cd79a22ef3e48f96c56`  
		Last Modified: Wed, 10 Apr 2024 20:33:00 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:a49265610bc47838b781a88347c249e2e317c4701e7bd75abe5a17cf3de9f526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5909772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f68e2ceb9307b8ef806dd478e1717170f8fe94038b84dafdd385db528fb85f8`

```dockerfile
```

-	Layers:
	-	`sha256:79c8150fdc0136143f6803537e073b115450ad08ace514829e18c1b5ee6696a2`  
		Last Modified: Wed, 10 Apr 2024 20:32:59 GMT  
		Size: 5.9 MB (5855895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6def345405d31fa6aee367c8e0526fd726eda63a742509f9c606f2af13d6d1a0`  
		Last Modified: Wed, 10 Apr 2024 20:32:58 GMT  
		Size: 53.9 KB (53877 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:abaabe3911cb98efbd126649016c43dea18947526591900b0c9dca731619735d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144342959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c59adb4372dcb9565239e2dff5282607c8aa6bd7ee21da1e6c416be6713b4b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 21 Feb 2024 00:46:13 GMT
ADD file:107da403005e1b6808da193b1f269be14ac31b0bd6d87b7609e9080e75f08eab in / 
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
ENV PG_MAJOR=14
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_VERSION=14.11-1.pgdg110+2
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
	-	`sha256:ec8b01fa71b8466600831f50045cfc2951257ac6eee36ce2a0fbe3dbe0098d42`  
		Last Modified: Wed, 10 Apr 2024 01:02:53 GMT  
		Size: 32.4 MB (32413416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c25246ea040671b16835f8ededcc1f86ce970f0c1ccbba8c3ec5d483474cdf`  
		Last Modified: Wed, 10 Apr 2024 02:05:38 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4eb4ceff1651835707cf11a25e586214d9be4e3cffd36e7036e4bf3a0a6be3`  
		Last Modified: Wed, 10 Apr 2024 02:05:39 GMT  
		Size: 4.7 MB (4718001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc59d8d1549b93f636169c49c0bd32d1ce148415746bc4c0a94b83e7407efc6`  
		Last Modified: Wed, 10 Apr 2024 02:05:39 GMT  
		Size: 1.4 MB (1447767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bda38b19d15d259c15db19f7d686b39f01feaa7f2defed028b999b0424d9c06`  
		Last Modified: Wed, 10 Apr 2024 02:05:39 GMT  
		Size: 8.0 MB (8044151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3c414ef3586c4d91503925291f921d639af9baab55a312b49c440c33645399`  
		Last Modified: Wed, 10 Apr 2024 02:05:40 GMT  
		Size: 1.0 MB (1028932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5757bc7b67bb8634d0db6e30bcd6287487859692541d48eac58aa50b986fb7ba`  
		Last Modified: Wed, 10 Apr 2024 02:05:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07db0478b8f35335e91c3d0ff95fdd45af00c566fdf67c3c8e37185b178680e`  
		Last Modified: Wed, 10 Apr 2024 02:05:40 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76833c26c7fa605126d2ac171094ce43ba1edf9a216c5035c03d2e5bdfedf51`  
		Last Modified: Wed, 10 Apr 2024 02:05:43 GMT  
		Size: 96.7 MB (96670315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64716fe35931c2605a2bf5f44cb10770018a76090a27014cd47d8ee5ed57d7e`  
		Last Modified: Wed, 10 Apr 2024 02:05:41 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe01a7147ba302ab0caa96ba560f1097480f39ae2d09576427ad67511d65299`  
		Last Modified: Wed, 10 Apr 2024 02:05:41 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e90c58877db20405875fd80a4899437d35104215297b703b21c3d7264791534`  
		Last Modified: Wed, 10 Apr 2024 02:05:42 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2710fe6e0d533fbe3b2e1921ff4933d37660a9a7c028c3122038444bb6ace738`  
		Last Modified: Wed, 10 Apr 2024 02:05:42 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98886c0d8f50f09d0112882fd0494783b5271feced8a2eae394c5dd863b74876`  
		Last Modified: Wed, 10 Apr 2024 02:05:42 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:c5c3bde283675696a05da90f0f215396bef75067cbe16b441a315ffc2eaea6ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5910792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd03d3995bd9ff90fa322f004d50b1f1adf185d81186507ce0b3695152caa21f`

```dockerfile
```

-	Layers:
	-	`sha256:b9d3cefb281fe2295ec692450ebda61f8f5b5a7067f65c9b6606f4c3fe6d90c4`  
		Last Modified: Wed, 10 Apr 2024 02:05:39 GMT  
		Size: 5.9 MB (5856795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:617605240af81db7c13c341c599b74e8892a98b0056675c75faff5faca6c518b`  
		Last Modified: Wed, 10 Apr 2024 02:05:38 GMT  
		Size: 54.0 KB (53997 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; mips64le

```console
$ docker pull postgres@sha256:35e4d50d86cd65041bd99b602df50cee2bd5728adae4cd1c13c726d34a54e5de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (136010064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:202b56b25045ca37ac51064f9cdd6fcc30d8d19894b6a5bf5be6553e9d05537b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 21 Feb 2024 00:46:13 GMT
ADD file:5a3b2305df619d313e2592819c382781fd774d11c3f687bc9ca004eba259694b in / 
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
ENV PG_MAJOR=14
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_VERSION=14.11-1.pgdg110+2
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
	-	`sha256:94315f37c06e4616cd911d9cfbe5597a620ca0249447454791c232fa7b1e2724`  
		Last Modified: Wed, 10 Apr 2024 01:23:22 GMT  
		Size: 29.6 MB (29645932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5716b3c0fd8484ba0ba173e84268b3006276714d336d13ce5b6ed6dfc37feeb`  
		Last Modified: Thu, 11 Apr 2024 11:12:49 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd054391d6d6568fefd3b0c672f781ccaf49fc1c5b9dc616820cc6151b880e32`  
		Last Modified: Thu, 11 Apr 2024 11:12:49 GMT  
		Size: 4.3 MB (4306005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4cc695cadfcc39b3c66bf1c0cff3cddd97aa8148638b8a283d5b0cf5b1647af`  
		Last Modified: Thu, 11 Apr 2024 11:12:49 GMT  
		Size: 1.4 MB (1359338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896de91615ae35270c8b272817ec3b485ef2cf42ed57f00424a41e25c07d87b7`  
		Last Modified: Thu, 11 Apr 2024 11:12:50 GMT  
		Size: 8.0 MB (8044660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ce024baade3216d43c634b85b19c6dc897838fb94010cafbd9280674825d2c`  
		Last Modified: Thu, 11 Apr 2024 11:12:51 GMT  
		Size: 1.1 MB (1090280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bc9cb5951a327aa60ae91d0cf6bd280f497e8dd476e9563d258558b42f9a6b`  
		Last Modified: Thu, 11 Apr 2024 11:12:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcc34bdd50a4d303c59aa154b129f0cb951ec6635b4abc050dda82ce9600d53`  
		Last Modified: Thu, 11 Apr 2024 11:12:51 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5ba71fb7e467e27937fdf8bb46a5cfdbe38bb36a788224b0e1be9df089d8cb`  
		Last Modified: Thu, 11 Apr 2024 15:39:55 GMT  
		Size: 91.5 MB (91543466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f370288c30fe5299df4fa00b5b984dccb01e7edb52ed48d0e486b8b58fe96a80`  
		Last Modified: Thu, 11 Apr 2024 15:39:43 GMT  
		Size: 9.5 KB (9536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c124e6c6e970d557313203f165ebf8356bd9ed479eaff6e0fbf1f8a1e10a3a30`  
		Last Modified: Thu, 11 Apr 2024 15:39:43 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ae567e775fceb32f9369da9e94da0590db54c62b28052128fcd85501a534c2`  
		Last Modified: Thu, 11 Apr 2024 15:39:43 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b9cbf2e6f900725b191405f0795cd113d055d2128e07f77422f8623ee2b2b7`  
		Last Modified: Thu, 11 Apr 2024 15:39:44 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508ef76e45126eda4f88b7e0adab262b7f425e98c47a5a76423f445aea4e0411`  
		Last Modified: Thu, 11 Apr 2024 15:39:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:021b65255f983903ecbf728af03cfda682eaefce57794af6bab9faa334f17cb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 KB (53728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf5294aef709d397f8e84a93d5bfa96f6807064072b5858df248e39cfeee699b`

```dockerfile
```

-	Layers:
	-	`sha256:ce627bcda78fe2d712fd62c803172d0176c3e2ff2dc89eeed2c5abe488fe6efd`  
		Last Modified: Thu, 11 Apr 2024 15:39:43 GMT  
		Size: 53.7 KB (53728 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; ppc64le

```console
$ docker pull postgres@sha256:70c1a375869eb66c2996704634b780363d24a4be022fb8346ed65233aa60468a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152662399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f686f7c6a7428c068f713eb8d3e3b0301db5480025d31f761ecb54f783a07b87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 21 Feb 2024 00:46:13 GMT
ADD file:33f8251ee78dc536740a4ab4a9c9a75ab2c3f5d7be0a41f41dea318cc8e93dbd in / 
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
ENV PG_MAJOR=14
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_VERSION=14.11-1.pgdg110+2
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
	-	`sha256:2608681ad30ed92fce8f1b566ae32649b5bfa30cc4df8792977ed14a0bc7cbe6`  
		Last Modified: Wed, 10 Apr 2024 01:32:01 GMT  
		Size: 35.3 MB (35304089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53992000f1d69df062c6db21c48f5281957c18e1baada3914a6f3291ffb61523`  
		Last Modified: Wed, 10 Apr 2024 21:30:25 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d5b402ea5c7cffeea60aebe15a10e0c6fc7340f986ee7e54417972d41c6e51`  
		Last Modified: Wed, 10 Apr 2024 21:30:25 GMT  
		Size: 5.1 MB (5132015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b76b8ca3429461f953eb6811f1d66736ca48d11ea221bc1943aa2d79a4c1144`  
		Last Modified: Wed, 10 Apr 2024 21:30:25 GMT  
		Size: 1.4 MB (1393720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d185839e6d28ba7b50e785e6640ade5f7c89b66cdbbc30bb3762975a25275b`  
		Last Modified: Wed, 10 Apr 2024 21:30:25 GMT  
		Size: 8.0 MB (8044411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1eb33f54339890356b17486dbfdba01f621bc28f51e71f4baea81f737235143`  
		Last Modified: Wed, 10 Apr 2024 21:30:26 GMT  
		Size: 1.2 MB (1197664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6074e818e0367b66c3258a8c87019f1947e994b0a0083f3d6e592a40e41672`  
		Last Modified: Wed, 10 Apr 2024 21:30:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cc7b7ec071228617aa2e309bff460a4e773143742f78f1b2dee464b69bed46`  
		Last Modified: Wed, 10 Apr 2024 21:30:27 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a50ff54bad3630a226578de759c6515e1d9eee9886a759b4fe9a4196da3187`  
		Last Modified: Wed, 10 Apr 2024 21:38:06 GMT  
		Size: 101.6 MB (101570129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4eda85cd49fc9e9913f8f15ce6d186dbacf557d655aae770868dc1355d443aa`  
		Last Modified: Wed, 10 Apr 2024 21:38:02 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1743dcc2f0739e5b5dd575ea3dec03034214d7ce5ef6cbaeb5a82a142ebf683e`  
		Last Modified: Wed, 10 Apr 2024 21:38:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba796410161f176ad068b0ffc002b4f2582775a9b2f663851bcfd18ac627834`  
		Last Modified: Wed, 10 Apr 2024 21:38:02 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4542979d30c9366fe9747cac2cd68aee698407d1ae99099d8d2cb95512cc217a`  
		Last Modified: Wed, 10 Apr 2024 21:38:03 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401b8ab46a08d507d2ab905b3fa1ccb72315595f00fd12a4ee39921c1d9c5083`  
		Last Modified: Wed, 10 Apr 2024 21:38:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:4ef7acb9714a0b4ee4ad8a8b629ced8497ed129af2fae853cab59aa83c343638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5910687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5781152e0e9c23ca39874c39e978950482b548f611b8310838dca68b1afa7b`

```dockerfile
```

-	Layers:
	-	`sha256:25f664c01fd5bd8e04317f50cf56dcfd42f5003f4f26cf3a150b75bfaaa86d88`  
		Last Modified: Wed, 10 Apr 2024 21:38:02 GMT  
		Size: 5.9 MB (5856762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c39e08d55de8b5b163512eeb33cc5c0c22615219947133d6e8775a6513c12700`  
		Last Modified: Wed, 10 Apr 2024 21:38:02 GMT  
		Size: 53.9 KB (53925 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; s390x

```console
$ docker pull postgres@sha256:066362e68160ac794972f2749ceffc31549373e18ed431b373f691bb7e43cac2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146160255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6974d0b4274f2030e42ec9ba75bf3d23de9975328d78fef592c4dc7866bde758`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 21 Feb 2024 00:46:13 GMT
ADD file:173b309178d19f7fccea713c7c575233510e5f065fd2d92a5378f001a1d33846 in / 
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
ENV PG_MAJOR=14
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_VERSION=14.11-1.pgdg110+2
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
	-	`sha256:499f72f2d94381b6df4b58d8ad4918f9e03fc5d140cb0704842fd78e2e63e391`  
		Last Modified: Wed, 10 Apr 2024 01:49:00 GMT  
		Size: 29.7 MB (29666840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a88b797406d5a841af5a6df863af9a489380e97da38100567f38c054e5648a`  
		Last Modified: Sat, 13 Apr 2024 13:27:51 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8320bd3d6aef44b4ea58a952f2d9e912c6c1f24f733197422e6b68bdd82e7631`  
		Last Modified: Sat, 13 Apr 2024 13:27:51 GMT  
		Size: 4.2 MB (4195916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de5798a4424584c60a6cb888a1c1ca621902b32ef55370190d7bc37dd57d440`  
		Last Modified: Sat, 13 Apr 2024 13:27:51 GMT  
		Size: 1.4 MB (1438011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc15708e075bfd9fc316cab7b8e2133a1a86e6f25ed5279f19d6b5cd61eb7bcb`  
		Last Modified: Sat, 13 Apr 2024 13:27:52 GMT  
		Size: 8.1 MB (8098789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8a8e481b8a0366e03a82c42d5fbc4d1edb069408c3cd8b9f6bdb4924c5145e`  
		Last Modified: Sat, 13 Apr 2024 13:27:52 GMT  
		Size: 1.0 MB (1015280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22b5b683a176b9b0fb2b61d936e62311ac5d309b13b29843b3a517254bf664a`  
		Last Modified: Sat, 13 Apr 2024 13:27:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9712abeb90d827a4fbfb35230046dd493e073ab4d3a42cf44f301bd68f70d7`  
		Last Modified: Sat, 13 Apr 2024 13:27:53 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1270bcccda985f71971aa7be3a087590090fabe425a164db8c429f6f7a07e986`  
		Last Modified: Sat, 13 Apr 2024 14:06:34 GMT  
		Size: 101.7 MB (101725045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bd2080e7e73f5a7ae1f5995db8ca2e1bb9778e106631f2db65d54a349f7854`  
		Last Modified: Sat, 13 Apr 2024 14:06:32 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d23b2bf6e0c813c1b96b3548a241c1d95a4585d2af7f80633fa6fbe5ab3ffc`  
		Last Modified: Sat, 13 Apr 2024 14:06:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc3fbc3a227b3a36a205a4abe0c0aca0d2e693f4479154afe31ab2c0667bc59`  
		Last Modified: Sat, 13 Apr 2024 14:06:32 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddae64199f89d2ba5bf6ddcf1d8338baedbc24c4ef95a36f8264812a3b1da080`  
		Last Modified: Sat, 13 Apr 2024 14:06:33 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b13b218de8d088eb1b04c7c2c1b06183dd3feb559222bef7bb3af987167ea34`  
		Last Modified: Sat, 13 Apr 2024 14:06:33 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:29547bc61f843be456e6b51a6ef37315a543c25112ffbc9024b9b34198952129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5902484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4921347ff7a4e5493b234c604875b7d5a636c16c4521cb7996e951e7a1417399`

```dockerfile
```

-	Layers:
	-	`sha256:df4e2635977a81486dc371e0e7d696e9ba22682c21329e9f537d0638616c0355`  
		Last Modified: Sat, 13 Apr 2024 14:06:32 GMT  
		Size: 5.8 MB (5848607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a608682f1e58a8c3cd7c0b11ad32a1918c40786eded3483c6992d7cdbe5bf238`  
		Last Modified: Sat, 13 Apr 2024 14:06:32 GMT  
		Size: 53.9 KB (53877 bytes)  
		MIME: application/vnd.in-toto+json
