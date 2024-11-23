## `postgres:13-bullseye`

```console
$ docker pull postgres@sha256:c0a82fdc7463b4ce928a67a86ba8f1362bd842da146f6dbb60c4075a6807e954
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `postgres:13-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:a4cdb8acc15e3dce485541ddb2731da317e3a7421aca3cd38ebd59261fb725ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.9 MB (145901874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8fac1715ffcd6a50cca0c60f6fa8bdea26a16cceeb190cd3166fe4d2f88c30`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENV PG_MAJOR=13
# Thu, 21 Nov 2024 20:07:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 21 Nov 2024 20:07:48 GMT
ENV PG_VERSION=13.18-1.pgdg110+1
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:07:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:07:48 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:07:48 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:07:48 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:07:48 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4157cd33f1d51348449394adbb40a83940130c0b422096f344f50e727aee63`  
		Last Modified: Fri, 22 Nov 2024 20:24:49 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f381bb332ab5497c5f2c0de680d52f4da11c5804ca1896bf2d19851e61b0b26`  
		Last Modified: Fri, 22 Nov 2024 20:24:49 GMT  
		Size: 4.3 MB (4308187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53a9c9692bf09dec730ad1745eb193a4b1c95a88ba7029e5c93fd7e063d7b7c`  
		Last Modified: Fri, 22 Nov 2024 20:24:49 GMT  
		Size: 1.5 MB (1472232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149309003298d6cd015c663010057032f7e66a9a41359f1a69f350c547431ca8`  
		Last Modified: Fri, 22 Nov 2024 20:24:49 GMT  
		Size: 8.0 MB (8044520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c157b7b995c1f066234af35ceefdbfec8113f8909573e5f98b216e254370d477`  
		Last Modified: Fri, 22 Nov 2024 20:24:50 GMT  
		Size: 1.0 MB (1038343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606890a071d0ccf5eedf776c4c3ead89cbaf3be57cbec5afdd384f15a65e70c1`  
		Last Modified: Fri, 22 Nov 2024 20:24:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b0587af87ed27ded966c83af86dab35348aa29addb880f2fb9e1975082546d`  
		Last Modified: Fri, 22 Nov 2024 20:24:49 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e09516a59784f0bae9dc7748efd22ba70771a18bc9ec4577fd1898e76ab80f`  
		Last Modified: Fri, 22 Nov 2024 20:24:51 GMT  
		Size: 99.6 MB (99566831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569f50d2c6bc42e3a8c6e150304437795f7c49be0395bf14b7506b4c1a232762`  
		Last Modified: Fri, 22 Nov 2024 20:24:50 GMT  
		Size: 9.4 KB (9354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f257103c4d8d55d57e14899d6c233334d6afadb8b764b4a292e95b5a07cebbb`  
		Last Modified: Fri, 22 Nov 2024 20:24:50 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b6d77f618ca9f61b3d8d6ea3cc066f08d3d6c302a43dbe9393c6c552212f48`  
		Last Modified: Fri, 22 Nov 2024 20:24:50 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b5da32f01f90840e0bbd4835de9bd5f42388304d8869b8d8d3d581d2c76fd6`  
		Last Modified: Fri, 22 Nov 2024 20:24:51 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68f3c359358ed75e080c9dd692ec35a1e88bca188f9830a064244682bab11f1`  
		Last Modified: Fri, 22 Nov 2024 20:24:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:b200fa80a853b846a9c75f1f4e7a9fe81d3acabcdfcfe09abda1e099f89a9ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5926577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dde48b84e5f48008e7168e1019c146a08d4ad686569770f28dc56d80c21d8c6`

```dockerfile
```

-	Layers:
	-	`sha256:296a45d4ba196c5e210706c7048902dd8370634b3f8424630260effed025fb05`  
		Last Modified: Fri, 22 Nov 2024 20:24:49 GMT  
		Size: 5.9 MB (5872201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37a63c1fc2694ed49b4254bdcc09ad9e2ce1cd797c52c3b3fa98b497fe7b14f2`  
		Last Modified: Fri, 22 Nov 2024 20:24:49 GMT  
		Size: 54.4 KB (54376 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:605d620eed2990ed203801b1e3633b548185397713a67772ebf7eb2eb31e6f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (133981317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42c01efa1014b736d9138a9534e876489c7aba76d88da791c09513131d11295b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_MAJOR=13
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PG_VERSION=13.17-1.pgdg110+1
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 18:53:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 18:53:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 18:53:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 18:53:24 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 18:53:24 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 18:53:24 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bbaa022ef9e0b119beb47d4a40af03cbd55afe3bf050a7353d06e43694cf5c25`  
		Last Modified: Tue, 12 Nov 2024 00:57:51 GMT  
		Size: 26.6 MB (26609257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996a8e55d17d62205dceee91515111eae9b32877a15584574b4fbb1ffd893d14`  
		Last Modified: Tue, 12 Nov 2024 11:37:58 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79085ce56ecea899420a90c1faa994c6e2a6be5b0d2c699b8dc9cad2163a194e`  
		Last Modified: Tue, 12 Nov 2024 11:37:59 GMT  
		Size: 3.6 MB (3601838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a612d84717c6022a49b864ab6154e8e40ecf168a31cca66c1c431f214d4ff440`  
		Last Modified: Tue, 12 Nov 2024 11:37:58 GMT  
		Size: 1.4 MB (1439292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb31a8313e6740a7df864869a720ce58a2a1afd0be22b1c5a4faca6f2c36aa17`  
		Last Modified: Tue, 12 Nov 2024 11:37:59 GMT  
		Size: 8.0 MB (8044516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce631e44ea85e5d5b5aeb686756fc11367dab2cf1a7d7b3b02920538c8241fc8`  
		Last Modified: Tue, 12 Nov 2024 11:37:59 GMT  
		Size: 908.7 KB (908690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7fd50a77adf6fc2423ae28b58b90372af285845471bd629289f1c450fedd682`  
		Last Modified: Tue, 12 Nov 2024 11:37:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21772a558953dbe1c63d70a7e8ae5302ece83606f990cbdd2fa63c395d8eee95`  
		Last Modified: Tue, 12 Nov 2024 11:38:00 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45cc3073b0934591b2883dd842f7e4a4d335840aad8b82be23bd86edc362e5ff`  
		Last Modified: Fri, 15 Nov 2024 00:07:24 GMT  
		Size: 93.4 MB (93357532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93c529f6a4cfe719560310afa1e8f6ddc094b6d9d0bc049f153f1070ae73d82`  
		Last Modified: Fri, 15 Nov 2024 00:07:21 GMT  
		Size: 9.4 KB (9356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176fe509ec4109834c1d805e9e23d29bbf84587705a0799b51097950606c0dee`  
		Last Modified: Fri, 15 Nov 2024 00:07:21 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a352b7625df2503c7556eed24e4016f2a5fdb8931737f32768562f43a5d0998`  
		Last Modified: Fri, 15 Nov 2024 00:07:21 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d21d83c6c71efe1b69cc321a2e1c105821fa19626900af7a2cf33fc6773ccbb4`  
		Last Modified: Fri, 15 Nov 2024 00:07:22 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5768935034ef0864791bd0a33f9accefdd28108c627b437709933e9c9440b249`  
		Last Modified: Fri, 15 Nov 2024 00:07:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:1f87e27500d614cba0e534ee5aaea3b7f8daff96a1ab960270979bf3b194af9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5937305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0ec404e273ddfd7acf8123a61132baf4fa037cd859eb5478cb46e7aa7c70a8`

```dockerfile
```

-	Layers:
	-	`sha256:2ae120e2b1a1456d4e788efff68792cc2f672625075a4c556a866925093ab631`  
		Last Modified: Fri, 15 Nov 2024 00:07:22 GMT  
		Size: 5.9 MB (5882735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e638dcb702d676cb6a6ec0752cce799b99b13db5d562fa0e6222d453287474d6`  
		Last Modified: Fri, 15 Nov 2024 00:07:21 GMT  
		Size: 54.6 KB (54570 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:7834f303b445a726ac81c58adfcdaddce8e1e8905715af5a1ecb05a2360d2ff1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143069034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8936dc5cf7d7bccb4cb71001f8ee908fec5393a16db482f27caba31badef6eac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENV PG_MAJOR=13
# Thu, 21 Nov 2024 20:07:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 21 Nov 2024 20:07:48 GMT
ENV PG_VERSION=13.18-1.pgdg110+1
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:07:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:07:48 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:07:48 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:07:48 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:07:48 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb13e3bddc816329c03504b2dd1f555426f4ca4b1f63a40b38676bb7aeadf67`  
		Last Modified: Fri, 22 Nov 2024 20:27:21 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b465497241a0b6b4a6f567faeeeeb5ff1e360255fc54bfd83ec8c7d187721f`  
		Last Modified: Fri, 22 Nov 2024 20:27:21 GMT  
		Size: 4.3 MB (4312826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68769824f0ef2ecb12c6e484230d484378396c14da12a0d23211b176f3ea49dd`  
		Last Modified: Fri, 22 Nov 2024 20:27:21 GMT  
		Size: 1.4 MB (1404096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481e887f7af7e65be9c27170e4d28740bf0f474fb9b6173430dd1376a4b96fcb`  
		Last Modified: Fri, 22 Nov 2024 20:27:22 GMT  
		Size: 8.0 MB (8044515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77f96bac628794a9a9be97366e19050be17d1de1c414d301430e8b2e4b3187e`  
		Last Modified: Fri, 22 Nov 2024 20:27:22 GMT  
		Size: 1.0 MB (1026588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f7a052381eeba5ddb6d15112e15dc47b4c0e6e31a7227b82181c4f2b7c83b7`  
		Last Modified: Fri, 22 Nov 2024 20:27:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd81b9930bacae289040d7d2b89eca8f875204c0ab28ba6ac7b351983e81e25`  
		Last Modified: Fri, 22 Nov 2024 20:27:22 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2197080d3d82bb3d5c7ed1f7ad3d059eaa989f5fcf1ae8a49f5aadca32eea35f`  
		Last Modified: Fri, 22 Nov 2024 20:59:49 GMT  
		Size: 98.2 MB (98169207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f41029ac41b3fe58d98e99ca6d61a143039b7da8bdc9be9fa1ba8c17c6e82f`  
		Last Modified: Fri, 22 Nov 2024 20:59:47 GMT  
		Size: 9.4 KB (9353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6829eaab6ebc33b89f9dafd7e418c5c5b700489e70b0d08e70dcca17c2d00b2`  
		Last Modified: Fri, 22 Nov 2024 20:59:47 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67319e621fa82139a235f6644efa914ba1e5f46f31c7cc172b21cf1266d6321e`  
		Last Modified: Fri, 22 Nov 2024 20:59:47 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7124c7cb47779f1d330440294af5a8b21722ed6ff8c8de02f8902573e8c3813a`  
		Last Modified: Fri, 22 Nov 2024 20:59:48 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efab939b9cf76e8b9060cbd2c3e2fd86f55e53d72a7d814766c9d2d0615932ec`  
		Last Modified: Fri, 22 Nov 2024 20:59:48 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:6f6d7131827d3870491646cd579df1c016ec9dc81b5c3303cbdc51922e59beb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5933114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c81ebfb553b60dee1d35ce32a5fbfcac0c54dd8a11b3a377e76b95ed11f87a50`

```dockerfile
```

-	Layers:
	-	`sha256:4cb0d7cd7425b2af15f7a8fca71824acbbe5c5e4755bd21a9a1859601f220ef9`  
		Last Modified: Fri, 22 Nov 2024 20:59:47 GMT  
		Size: 5.9 MB (5878495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca3f0a5fac7c26a958b24a3ad4abc6f149c34976c1a2f2abe5f9382f2a533a0e`  
		Last Modified: Fri, 22 Nov 2024 20:59:47 GMT  
		Size: 54.6 KB (54619 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:e19c3ae50170aada0bd852de38890eaec3cada076e53e4d0439abe99d8f4dc65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153988866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64619e9093b6c3623fa7e26037b99edf366d4bffe534627e7aec22d1ddc7b9e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENV PG_MAJOR=13
# Thu, 21 Nov 2024 20:07:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 21 Nov 2024 20:07:48 GMT
ENV PG_VERSION=13.18-1.pgdg110+1
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:07:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:07:48 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:07:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:07:48 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:07:48 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:07:48 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2aea24d0416284c8bc498d91bac1c90e2bf12b01e7867f799161bbb874a8323b`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 32.4 MB (32423351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7fcf810de951fb1fde82f85909aee1665d08159db80b0e6c21bac8088fbf54`  
		Last Modified: Fri, 22 Nov 2024 20:34:35 GMT  
		Size: 1.7 KB (1679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3817f2b8c71b0312c1b7fd052cff2668fbf15ecaf76fbbae5489b02c6b05da5e`  
		Last Modified: Fri, 22 Nov 2024 20:35:05 GMT  
		Size: 4.7 MB (4719704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc37a3ca11ee02ef2f258273d8659c438f30089161f4bad6876ac56b125fcea`  
		Last Modified: Fri, 22 Nov 2024 20:35:05 GMT  
		Size: 1.4 MB (1447812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e6bd79853515f73a9884ca4c62d8ca6df181247067008858ce283507d71c8f`  
		Last Modified: Fri, 22 Nov 2024 20:35:05 GMT  
		Size: 8.0 MB (8044391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7d8cd0b40b95ef74b0b5ac4b77d75dcbffb5b424dd6bb9f769d6b62be238b7`  
		Last Modified: Fri, 22 Nov 2024 20:35:05 GMT  
		Size: 1.0 MB (1028901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2675d9f2f2a7dd595b0e650f293c1940b6f4363e8f38896e44d50fb0baa27052`  
		Last Modified: Fri, 22 Nov 2024 20:24:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29dab49c472ac8b457da46feeac51fb5752de99cdec632834e720ef8b9320e2d`  
		Last Modified: Fri, 22 Nov 2024 20:35:06 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc13d84c9303cefa6ddacd92a68164a6bbd2af12a0421fbcec1a68a455eeb763`  
		Last Modified: Fri, 22 Nov 2024 20:35:09 GMT  
		Size: 106.3 MB (106304505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0036801c4191e3c0d407b17e26dcb962ee9754b9c7dfdb4b42528792f5de8aa8`  
		Last Modified: Fri, 22 Nov 2024 20:35:06 GMT  
		Size: 9.4 KB (9358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ccfcd7f057bd8be59610c4f4d9e53ea55e58786880d4ed21c5d257a1cc907a`  
		Last Modified: Fri, 22 Nov 2024 20:35:07 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400fb83d1d1a8168decaaf46d8074bbc8df4ef8e10daa897a3a5e3b89ee1d8e7`  
		Last Modified: Fri, 22 Nov 2024 20:35:07 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddced18fb8abcec3b8f024873c63ad25965772921442cc95f426a59f3377abac`  
		Last Modified: Fri, 22 Nov 2024 20:35:07 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7339d3276c66cabb825f7f1826224694485807a2664e51010205288a0eaa0cef`  
		Last Modified: Fri, 22 Nov 2024 20:35:08 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:d274a8bede1f12736c0bc4e41dc0f2847943bed00dcae5020e7f72704ca3088f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5934850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e0a8118fc26c27280e6cbf89afb12629cc2b169d5bf2c264cba2bd8644fed9b`

```dockerfile
```

-	Layers:
	-	`sha256:78734874d96649253ac47cc73dd3ac009becfabf509ad218f581b32196f49d28`  
		Last Modified: Fri, 22 Nov 2024 20:35:05 GMT  
		Size: 5.9 MB (5880512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1514b005d992f94e40dd55041cffae3575e80cadb117839e6ab2975a61e5334d`  
		Last Modified: Fri, 22 Nov 2024 20:35:05 GMT  
		Size: 54.3 KB (54338 bytes)  
		MIME: application/vnd.in-toto+json
