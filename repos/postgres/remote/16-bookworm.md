## `postgres:16-bookworm`

```console
$ docker pull postgres@sha256:dba2cc7c4928e44d1157e8b2ab99eaae0ee743837700f17ffbd7a3c544d8da1b
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

### `postgres:16-bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:10a028bdde46f9ac6786a8609b16672a7d0d141d6cbe776f7fbad5e82f4fca3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.4 MB (153421810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07a4ee949b9e7851d9ef860fd36f486aa821f23e1c17939244155fe825eaf79a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:58:11 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Thu, 09 May 2024 18:58:11 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV PG_MAJOR=16
# Thu, 09 May 2024 18:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 09 May 2024 18:58:11 GMT
ENV PG_VERSION=16.3-1.pgdg120+1
# Thu, 09 May 2024 18:58:11 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:58:11 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:58:11 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:58:11 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:58:11 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:58:11 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33c47d38f2237fc96b17fb3d70fc979da86113bffe2de8af9274424d5f93a7e`  
		Last Modified: Tue, 23 Jul 2024 07:23:30 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87cb89a22d1ecccd02ced4c9d0abf955705c08d169df50a234c7ee4b7d77a7f2`  
		Last Modified: Tue, 23 Jul 2024 07:23:30 GMT  
		Size: 4.5 MB (4533714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd66d978bf1a02590a99bcb28c0a7dcf8014adb75f85bbc6ee8fd57fcf4a146b`  
		Last Modified: Tue, 23 Jul 2024 07:23:30 GMT  
		Size: 1.4 MB (1446654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1723030f70fd750a1dbf46990544e05376cee1e047247d3e2051ab41780ab5a`  
		Last Modified: Tue, 23 Jul 2024 07:23:30 GMT  
		Size: 8.1 MB (8066193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed8886da429dd46244ee7685c003965e5d22f3b10a2f74b0f0f5c8f17923ec6`  
		Last Modified: Tue, 23 Jul 2024 07:23:31 GMT  
		Size: 1.2 MB (1196032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0a96a00eeb3b2046b0c70fb4ce3b34562998870a75502a7669af2a6932797f`  
		Last Modified: Tue, 23 Jul 2024 07:23:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224e967d76854bd0ee904bd7578b9a36eccb7e69d6dac529ca136f0d366b2dd7`  
		Last Modified: Tue, 23 Jul 2024 07:23:31 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4774bf58af6aacd28f667545b94b17aeda7e165db2c165f1950c2481834ceed7`  
		Last Modified: Tue, 23 Jul 2024 07:23:33 GMT  
		Size: 109.0 MB (109032694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f45270309c1d4281125c3bbc6da6bfdabceacd250126ccb9d09f7e85da96e1f`  
		Last Modified: Tue, 23 Jul 2024 07:23:32 GMT  
		Size: 9.9 KB (9917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60cb0fc6dcac311da69995cc895c838d731a9d34c3079629eadfe0bfa4b311b8`  
		Last Modified: Tue, 23 Jul 2024 07:23:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcf585d57b061b36c17e3007fe31aa3095858782566d7158e01f2741c2027a0`  
		Last Modified: Tue, 23 Jul 2024 07:23:32 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87cb29313a81dec1457eaade68b9e0504827c83789c7063acdc9920edf4bceeb`  
		Last Modified: Tue, 23 Jul 2024 07:23:33 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7f0c5387bd324c6b87a3743d4553a4c02c32b6fc04ce2fdc25d65a05945cc3`  
		Last Modified: Tue, 23 Jul 2024 07:23:33 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:fdd5eb2984a32ec160be6c0eecb466ec140269a54de301b8b45222c4055cfaa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5804868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d035676898c0543bb3d27f5eebf023d68dbb6ffc07e05f32439d51f19a752d4`

```dockerfile
```

-	Layers:
	-	`sha256:f92d7476b110194622de3e8c9dcab627afc49596562daea7977dc462aecc93b5`  
		Last Modified: Tue, 23 Jul 2024 07:23:30 GMT  
		Size: 5.7 MB (5749749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:763d22e3c858bf637138f8c196ebbc331ed991dcae8e182fa8c898799eb23168`  
		Last Modified: Tue, 23 Jul 2024 07:23:30 GMT  
		Size: 55.1 KB (55119 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:6c6fe4d70707f27e369d0ff1af2b9b0febc0d3b92a553b361fcc8a033fe1187b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146153757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a32305408573f8c799e01159e5389206cddb462f5f5d97db9b9c7677381573fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:58:11 GMT
ADD file:752589c0ca446e2e74ef0b8c412eabb01e2a8035cfec47b1d9630b9f704fbda7 in / 
# Thu, 09 May 2024 18:58:11 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV PG_MAJOR=16
# Thu, 09 May 2024 18:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 09 May 2024 18:58:11 GMT
ENV PG_VERSION=16.3-1.pgdg120+1
# Thu, 09 May 2024 18:58:11 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:58:11 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:58:11 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:58:11 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:58:11 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:58:11 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b695a3453560aacd42060f43ccf1cbd7d20412f50126ca6a469af38d3fe1e5b1`  
		Last Modified: Tue, 23 Jul 2024 00:01:19 GMT  
		Size: 26.9 MB (26887299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb41e481b09a752e739801af291cd24c907097d22bae86d11610455288bb0aa9`  
		Last Modified: Tue, 23 Jul 2024 10:34:18 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6157b9d09e77586784e9a43637e8af8a77d145aa1de55c54bea926c3008ceea2`  
		Last Modified: Tue, 23 Jul 2024 10:34:19 GMT  
		Size: 4.2 MB (4150884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545a2b3080adc0577292593d5eae7f41abc93fff2a7e126504861b534f51348a`  
		Last Modified: Tue, 23 Jul 2024 10:34:19 GMT  
		Size: 1.4 MB (1423876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5dd846411e83023dfed386a37427c0d8ad3ead0f3e3c2520c4a6c09134f49a`  
		Last Modified: Tue, 23 Jul 2024 10:34:19 GMT  
		Size: 8.1 MB (8066345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d5b3fd0f0817d1f48e28158c7a91cf1caf3466db89e7da7987cf2a8ef92268`  
		Last Modified: Tue, 23 Jul 2024 10:34:20 GMT  
		Size: 1.2 MB (1194838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925d94f0b922ecf6efe178c24aa54f4f330c757af4b6f33a2c05d03d9dded246`  
		Last Modified: Tue, 23 Jul 2024 10:34:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cff86d79df434b58238ae6a007384549d0605cdaa1195c205aa3f112e2ae82`  
		Last Modified: Tue, 23 Jul 2024 10:34:20 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6337e8d1331b06152fa81e22c639800514be8f1d2d1a9d3e62fc59ee2e216f16`  
		Last Modified: Tue, 23 Jul 2024 11:09:50 GMT  
		Size: 104.4 MB (104410266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff23ac4507fec81c9136c3d11ce52e1ce55bfd5a4739de6bbe244bab909524a2`  
		Last Modified: Tue, 23 Jul 2024 11:09:47 GMT  
		Size: 9.9 KB (9925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e704488d9060317ae776051dbf221c1f9090e412e004a71052df111671ec2bef`  
		Last Modified: Tue, 23 Jul 2024 11:09:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2532b929b6893b86a4d8972577c8df16a8f4aa335f31af3e2531fc7522e76b`  
		Last Modified: Tue, 23 Jul 2024 11:09:47 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63ea6d3c45e9a8de855c58328d78a70afbac3023226adeb642be690b8438ab7`  
		Last Modified: Tue, 23 Jul 2024 11:09:48 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e6d7dc1238dc4ab0848b5ea3d65ec5eb479147eb5640637c860eafc5c459fc`  
		Last Modified: Tue, 23 Jul 2024 11:09:48 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:4697e10b69fc655c3777c899b81d154b54eee7060d2bb2e68f585b03d8b69db2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5822510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:486540861505ac45bd57ed99dec8be8b840ff38262f63e5b9d879addabbc8cfd`

```dockerfile
```

-	Layers:
	-	`sha256:3c6d496d91f63afeecf48662a232d5da9be515e2f4795b639ca2c723490e6443`  
		Last Modified: Tue, 23 Jul 2024 11:09:47 GMT  
		Size: 5.8 MB (5767162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ea1da299b80cb46abbe8dd0a5083f842d453f510d84015d710627f1c7373777`  
		Last Modified: Tue, 23 Jul 2024 11:09:46 GMT  
		Size: 55.3 KB (55348 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:f0874fea5be320326c67e8226eafd782a7f0c82f30979bd81b0df75eb48879fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140870855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71eafa1ec92d8b42ac5a37a94555f1da9a47557189563b99906110ea279ac4eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:58:11 GMT
ADD file:b3438b93a141bfac397342418c34c4fe554bd257eeee378da353577c3d2206ca in / 
# Thu, 09 May 2024 18:58:11 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV PG_MAJOR=16
# Thu, 09 May 2024 18:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 09 May 2024 18:58:11 GMT
ENV PG_VERSION=16.3-1.pgdg120+1
# Thu, 09 May 2024 18:58:11 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:58:11 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:58:11 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:58:11 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:58:11 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:58:11 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ec16b40bfa260bcfd3b351a12bda1032683bb7db1fc4a9630b03194691569e14`  
		Last Modified: Tue, 23 Jul 2024 03:06:55 GMT  
		Size: 24.7 MB (24718200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5d0569dc5d23e5d5bc3955f1de3be701ad5c0d0cce906489688bfe5d4e7282`  
		Last Modified: Wed, 24 Jul 2024 03:23:50 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0360215b9da0a230c55c4449508d0573bf39723d1c01794535b56b43ad27724c`  
		Last Modified: Wed, 24 Jul 2024 03:23:51 GMT  
		Size: 3.7 MB (3742512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9425f16b994d419301607485de861222a995a10fb8dcec2cf2cf54fc6a2b6232`  
		Last Modified: Wed, 24 Jul 2024 03:23:50 GMT  
		Size: 1.4 MB (1413637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df114fa7b8d343ed4edc4f5db2345e420a2bcf0c3c53b689632cb2f952636463`  
		Last Modified: Wed, 24 Jul 2024 03:23:51 GMT  
		Size: 8.1 MB (8066253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf09eead83b5372a6a514b62d198a1f1b2d3925ffdc628d9e65ccaf19ff6088`  
		Last Modified: Wed, 24 Jul 2024 03:23:51 GMT  
		Size: 1.1 MB (1066956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e157355c5bc566664b47a05ff987f3525e8dc23473a22984bd89ad2f449093`  
		Last Modified: Wed, 24 Jul 2024 03:23:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be91f83fde51bf60ff5f4111b4329d74b19f3b2697e18bd0f39c80cfc46e26f6`  
		Last Modified: Wed, 24 Jul 2024 03:23:52 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706c182afea2595ee36f185b3716e55c49f2a3c2d95aa19b4b461c0fc0028c94`  
		Last Modified: Wed, 24 Jul 2024 04:03:11 GMT  
		Size: 101.8 MB (101843041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba723c5be4a8d688be27e965856f82a0ec9da1b4345307e9b4e76260605552ff`  
		Last Modified: Wed, 24 Jul 2024 04:03:08 GMT  
		Size: 9.9 KB (9926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ac84cf0f5f65105e46f99e4df9b9b2df57814dd8341a341e10918685d5aed2`  
		Last Modified: Wed, 24 Jul 2024 04:03:08 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6f59fbb0dbcaaed3e9666a37cc65a09a72ec275c78c9a01f542a9dd9cc415e`  
		Last Modified: Wed, 24 Jul 2024 04:03:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f160457020a82f764a10ab8097e8edee6fdce5c3f8b1860928c727a2ae5d0ef6`  
		Last Modified: Wed, 24 Jul 2024 04:03:09 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e56bcf2d46303275fadbf61992e9b349c6feaa6cf785e651e971c9bb9df2b5c`  
		Last Modified: Wed, 24 Jul 2024 04:03:09 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:e475b3fce9ec432cd62ecb823815399f9204e2f1c2e0df99e206b79d1f04fdcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5822179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0c9602f3de93fb733efd1468c240c12bc866b99c31455bc01c381881562130`

```dockerfile
```

-	Layers:
	-	`sha256:4a251fc7956b432d67c6ec9317decf21a8c9f43c8518a0335e7ca8782a7a385f`  
		Last Modified: Wed, 24 Jul 2024 04:03:08 GMT  
		Size: 5.8 MB (5766831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e27b12728c4048c0b7146f7d9242dab1211f8264a3c4db9b018ea6effcaa1d45`  
		Last Modified: Wed, 24 Jul 2024 04:03:07 GMT  
		Size: 55.3 KB (55348 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:7c5f032614297f561716f82d069837db5e7648d38059cc7e07585a6e9bbd6ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151594604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aaea6e555c2f526761a3e61c21fbb305ba214c674b14aaed760f030aeaffe9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:58:11 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Thu, 09 May 2024 18:58:11 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV PG_MAJOR=16
# Thu, 09 May 2024 18:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 09 May 2024 18:58:11 GMT
ENV PG_VERSION=16.3-1.pgdg120+1
# Thu, 09 May 2024 18:58:11 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:58:11 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:58:11 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:58:11 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:58:11 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:58:11 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01dca17b7ddcc79164d0a94372d7017a13e831f924f338bb57d21b603f2b590d`  
		Last Modified: Wed, 24 Jul 2024 01:16:31 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52de7f5e396e2b3293aebdd0311c46b000e07294a748f2c90f34fffff614233b`  
		Last Modified: Wed, 24 Jul 2024 01:16:32 GMT  
		Size: 4.5 MB (4499121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f20f97ca3f1eac8235b46c5af0bb18bf9fc44fe463eb892cf9c2dbd1da33a8d`  
		Last Modified: Wed, 24 Jul 2024 01:16:32 GMT  
		Size: 1.4 MB (1378679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10710bf0fe8019c198539d5ffa92ee930b096dd2eec37754a2ab89a6036fdf35`  
		Last Modified: Wed, 24 Jul 2024 01:16:32 GMT  
		Size: 8.1 MB (8066274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbbd7ab8dab09a619911034e4e9227f6bd91a42bffbc5a392717144a09ac19c`  
		Last Modified: Wed, 24 Jul 2024 01:16:33 GMT  
		Size: 1.1 MB (1108682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda565a705121f0128bc867aa1ea4fca361184a5172d42e3d8f9009bac5d8dc6`  
		Last Modified: Wed, 24 Jul 2024 01:16:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946c50ce7e116a8a5ca826c35b3c1f1806c48237a20cf327d658d2e4aba74515`  
		Last Modified: Wed, 24 Jul 2024 01:16:33 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac058a753ea2d9c765c143249ee1797b7bc972e73b55f3e1006efe100003657`  
		Last Modified: Wed, 24 Jul 2024 01:26:02 GMT  
		Size: 107.4 MB (107365032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e7cf2ccf452b8b8b98570428af908de10c6e1368ac0febbc438bf74a3da867`  
		Last Modified: Wed, 24 Jul 2024 01:25:59 GMT  
		Size: 9.9 KB (9920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6795e98abb84bbf44a345a92fdfc5435c4dc3b48745e8742f9ca55bfb1c4a163`  
		Last Modified: Wed, 24 Jul 2024 01:25:59 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c3d38ee8b8baa440c7f5721910a44e9fefe323f0426d26969aea2b25f96e61`  
		Last Modified: Wed, 24 Jul 2024 01:25:59 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327a852adcb59ab7aea20a5acc2997610083c275dff4c145c9670b5fd5694145`  
		Last Modified: Wed, 24 Jul 2024 01:26:00 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16ed6d9fa6144d61c3faa4a5fa214aac7ac597050f979a8ab767ffb5fa9af5f`  
		Last Modified: Wed, 24 Jul 2024 01:26:00 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:7fef127df1b7e9a75c2c92e4d81a9673f351f4003f3a4fb66739b918aa54876e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5811565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4155053fbafbd99501f974ca7a07055f7c7c721c4cbe0f12509c728d00851ca4`

```dockerfile
```

-	Layers:
	-	`sha256:992c5609bf93713669536c9e6f8004d58807126cb017569fa7317cd92a336679`  
		Last Modified: Wed, 24 Jul 2024 01:25:59 GMT  
		Size: 5.8 MB (5756114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1645b43c768260c9191970d4545ef8a3010f9bc3d5411622d673404245e359f1`  
		Last Modified: Wed, 24 Jul 2024 01:25:58 GMT  
		Size: 55.5 KB (55451 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:1b277d0af2273577d8547b295e3834baaf0c04f5b3b823882f686bac23502cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.5 MB (161533636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab0b8138592b6070f075d1b896fbc9029c3fa495b8ecdb8b9e10574e0379272`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:58:11 GMT
ADD file:9b63a9d86a51a3d56d700d09e1152578d700ba4453d852325d8eb9896534f3ba in / 
# Thu, 09 May 2024 18:58:11 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV PG_MAJOR=16
# Thu, 09 May 2024 18:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 09 May 2024 18:58:11 GMT
ENV PG_VERSION=16.3-1.pgdg120+1
# Thu, 09 May 2024 18:58:11 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:58:11 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:58:11 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:58:11 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:58:11 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:58:11 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7fa64a47f35cb425a1275bff76c45df3b76d3ff6b07911737090b82e4f221e93`  
		Last Modified: Tue, 23 Jul 2024 03:57:51 GMT  
		Size: 30.1 MB (30144309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa74a5cec2994b252b86aefbaf69bc97a6fa3f2ff4410ebd3b25eb313c9bc80`  
		Last Modified: Tue, 23 Jul 2024 06:24:01 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68d222e447d0a8b096a3522038927c841caf156e74a8fe99881402645fc34ff`  
		Last Modified: Tue, 23 Jul 2024 06:24:02 GMT  
		Size: 5.0 MB (4965093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7de8ae52e3490623568d5bd7d489fd290b7f037f9bd6c50cabeb0d4eeb49881`  
		Last Modified: Tue, 23 Jul 2024 06:24:02 GMT  
		Size: 1.4 MB (1422131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8350603794a3def60baab1a9dbf99f26025ab4c67bfa2fd0f304f0a8940dacb5`  
		Last Modified: Tue, 23 Jul 2024 06:24:02 GMT  
		Size: 8.1 MB (8066288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb22c46e483082b3d2256cf0de95f9fc64c426fd32d902490921c2fb1f4bf100`  
		Last Modified: Tue, 23 Jul 2024 06:24:02 GMT  
		Size: 1.1 MB (1137161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a3b5330e4b285a78938ca964d498a883b9be9bbb8db21972cf1fad9c60cadb`  
		Last Modified: Tue, 23 Jul 2024 06:24:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1588413ff088bb8c4b6c6a34f44aa24ae9d74ed87f163adee1c96f65e2b28dcf`  
		Last Modified: Tue, 23 Jul 2024 06:24:03 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a217d54dac0e8e89dd668321db588e8705d12cd40102b2769c824e779cd7a30`  
		Last Modified: Tue, 23 Jul 2024 06:24:06 GMT  
		Size: 115.8 MB (115778411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2786ba36d6bf5e51652004f0dd2de609d532c5d3c27beb1b1861e69d6b9830ab`  
		Last Modified: Tue, 23 Jul 2024 06:24:03 GMT  
		Size: 9.9 KB (9926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dde670e4254077198ef5a6860fccd5f9e5c9dd11c14caedf63dabc1aa84f689`  
		Last Modified: Tue, 23 Jul 2024 06:24:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acac74f6961228a6ab943342456817c859cd1ba8c579b6ada7a6a933081f12d`  
		Last Modified: Tue, 23 Jul 2024 06:24:03 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeabd10ed987fd223ab48f0943b80cd44712c1c4d12bb48aff55e71627fe81dd`  
		Last Modified: Tue, 23 Jul 2024 06:24:04 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082c313ce1799307995c2ef67879d5174d26dd3ef07d07cdbf274174c013d532`  
		Last Modified: Tue, 23 Jul 2024 06:24:04 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:a69cbd94b774d07b3e4202594788f919e58574a6511f3f5ad296f6403c759bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5820247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5850c406cfb525e8f2f26a72d14228ea72a44a7cd318355b556a92b1b1365f9`

```dockerfile
```

-	Layers:
	-	`sha256:98c300343a38d924e8948e5a8fc53179b03cc44e67495819cef8216d852dd320`  
		Last Modified: Tue, 23 Jul 2024 06:24:02 GMT  
		Size: 5.8 MB (5765189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7c5a82375e64b4b8827bcb5fc1afe8837972f030c5819f7a4c5bcff7a583a00`  
		Last Modified: Tue, 23 Jul 2024 06:24:02 GMT  
		Size: 55.1 KB (55058 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:0439d18179bc4e22f5ddc9465fabc3287341bd1663c486e9767fb67298e9ed75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148844215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0968dc048632434795d6d215f5d10900b8ecd38deb6a31d2ff7c886f3ac78bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:58:11 GMT
ADD file:9a0f0c8ed27f6f2bb89272036da4d44a63dcaf43fb03528dd2d970fbe64ccc92 in / 
# Thu, 09 May 2024 18:58:11 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV PG_MAJOR=16
# Thu, 09 May 2024 18:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 09 May 2024 18:58:11 GMT
ENV PG_VERSION=16.3-1.pgdg120+1
# Thu, 09 May 2024 18:58:11 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:58:11 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:58:11 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:58:11 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:58:11 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:58:11 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:cbefe199012545da86e0f461f1964dea0c9bab400e37766ee5f32b967423cf0b`  
		Last Modified: Tue, 02 Jul 2024 01:29:29 GMT  
		Size: 29.1 MB (29124929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb032b040f73cba01ab49188322bf0a798f9ab64835b69c36d32e4588d00bc1a`  
		Last Modified: Wed, 03 Jul 2024 07:48:15 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ad57ee31ac76036e218d38ee1c7413168534c91b00841edd94394a2997bede`  
		Last Modified: Wed, 03 Jul 2024 07:48:16 GMT  
		Size: 4.5 MB (4475070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae5b6b1dcb3be35340288d72332dc5a195c73c7aa9e0a8b61ccc1e69102d74b`  
		Last Modified: Wed, 03 Jul 2024 07:48:15 GMT  
		Size: 1.3 MB (1333829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7738e40a5338cb3e98989d68cb3f12b2193323152be14c8b2ee0ac12854b6797`  
		Last Modified: Wed, 03 Jul 2024 07:48:16 GMT  
		Size: 8.1 MB (8066444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666f040fd55101b468457f71d839f5a238c0330f7d71c7bb51b92e1df4dfa57c`  
		Last Modified: Wed, 03 Jul 2024 07:48:16 GMT  
		Size: 1.2 MB (1182662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530f1bbf91aaa54cfbcb4936a8dab88f2e1f0329666ef979145739b2c9f0cd82`  
		Last Modified: Wed, 03 Jul 2024 07:48:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a4026483394afafb672a9a076de74c38ac6cf9ad529a4dabca860604ea4986`  
		Last Modified: Wed, 03 Jul 2024 07:48:17 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e12f21cc916030c6947ab628dfcc0844d5ceded4f1ad6e61f020c252ccefb4b`  
		Last Modified: Wed, 03 Jul 2024 07:48:27 GMT  
		Size: 104.6 MB (104641020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64c87f9d92320b7fcd827ae2d76ff25bb1208b1a3c073d04eb170062eb1752b`  
		Last Modified: Wed, 03 Jul 2024 07:48:17 GMT  
		Size: 9.9 KB (9925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923ae9471d39adbc16e2e8686c985398c9db7a14969daed14387ae1cb0debf2c`  
		Last Modified: Wed, 03 Jul 2024 07:48:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c1e1dd374daeb5e99344859aa12841b68fbe1160d930f23fb7ae281c126f00`  
		Last Modified: Wed, 03 Jul 2024 07:48:18 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89864d6b5615f1617bb8c6eba965dbd813f30ce219a9655657158091b054e6de`  
		Last Modified: Wed, 03 Jul 2024 07:48:18 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6209975529cf958272ee934398d69cebb8055c62c5c1ba22fc79b8162e8462d1`  
		Last Modified: Wed, 03 Jul 2024 07:48:19 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:ab4376214a78c448d4ce8a7b754a3dc6833ffb95b1a82626d8cf585c60eeb4c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 KB (55008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa0bb982daa2d2138865a58317e1ecabdbcec0b4ca5cb6986c75022a6c6e9dbf`

```dockerfile
```

-	Layers:
	-	`sha256:9d991d847ffdb8d06e1e6cb9a32674f05e83895a24aa83abb2aae43cce6c1a9e`  
		Last Modified: Wed, 03 Jul 2024 07:48:15 GMT  
		Size: 55.0 KB (55008 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:1bf80f7f11c834474a00cd1bf81694ba5db21d46e0d1ade0f59dd0d04890bfad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.6 MB (165599782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51f2e4e29799f60d90e9d28e101ebe13926a92dea0999d786aec8f404b70bfeb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:58:11 GMT
ADD file:5cc77fc68bd67c95f4f51e07f554f0227244f40137fb23780dfc932a424e1b0b in / 
# Thu, 09 May 2024 18:58:11 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV PG_MAJOR=16
# Thu, 09 May 2024 18:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 09 May 2024 18:58:11 GMT
ENV PG_VERSION=16.3-1.pgdg120+1
# Thu, 09 May 2024 18:58:11 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:58:11 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:58:11 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:58:11 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:58:11 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:58:11 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4d94a6ac7a4136997b66aca74cb19ab0acecd94c24cada5ab7ab322f2467eb86`  
		Last Modified: Tue, 23 Jul 2024 01:31:12 GMT  
		Size: 33.1 MB (33122275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3308034efda7e17d2e8bb36f64da7fb538890623537308d9c64245cd3ddc501`  
		Last Modified: Tue, 23 Jul 2024 23:14:11 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1271d606e4f0ab4aad9cb312ae7a27785fe0174a398c9ab38308cb3809ce8635`  
		Last Modified: Tue, 23 Jul 2024 23:14:11 GMT  
		Size: 5.4 MB (5368152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3808909756c41ca4f48469e1cc63bf63720d030092cd79160259aa3a3424c884`  
		Last Modified: Tue, 23 Jul 2024 23:14:11 GMT  
		Size: 1.4 MB (1368590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42d725582d51854451a1c67ffa5591a4ccfd91549a027305c4f9a69574c00c9`  
		Last Modified: Tue, 23 Jul 2024 23:14:12 GMT  
		Size: 8.1 MB (8066299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4247c6d0aba64814cc272dc4ed2fd546c985992b8301373f6a3ff92988664fa4`  
		Last Modified: Tue, 23 Jul 2024 23:14:12 GMT  
		Size: 1.3 MB (1283458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ef9ccbaa89b1712234d1d4f4aa9ba2187f06a58f91207ef89172b8ef10e6cb`  
		Last Modified: Tue, 23 Jul 2024 23:14:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17dc82ec9556e1494b2f5fc653a04ae746ebfef1bb9ccdb0a6d5b39dad85e91`  
		Last Modified: Tue, 23 Jul 2024 23:14:13 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da759a411816100003db69c578a3ac8d297033733973f876c6a959ee77947c1`  
		Last Modified: Tue, 23 Jul 2024 23:25:21 GMT  
		Size: 116.4 MB (116370759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ca07edb2b14ccd83b2f295ea2daf3280ada48517773816a882a3e87c940c9f`  
		Last Modified: Tue, 23 Jul 2024 23:25:17 GMT  
		Size: 9.9 KB (9920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f142b3ee9adccf6be6794c84d307b5aaec895e5ad0ef6596c8b9c10a3e27f7`  
		Last Modified: Tue, 23 Jul 2024 23:25:17 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58df32b9c6c1a23d714b65ed792b0eea66fb12abbe125432c72dacc16687b238`  
		Last Modified: Tue, 23 Jul 2024 23:25:17 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5448b9ca0ef9977e0c70a415d71ae78693313ec33a68e3468377274650dac863`  
		Last Modified: Tue, 23 Jul 2024 23:25:18 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57437b931684d77ea6bb0c84fc7e4e9c56160e1585a18e8c741210595e05c0cd`  
		Last Modified: Tue, 23 Jul 2024 23:25:18 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:c3010208ba3337af7d03b4098e2549b66c323b4c498c9423d5af39a1514a3538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5812181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d2e300897b37b92b78e6b9ab55822322ef574dc6abce5c95667aad6c0d9b251`

```dockerfile
```

-	Layers:
	-	`sha256:f3b37905b50826e31aabdd065202393662ad9e5744f0d150d298f859e2e5d022`  
		Last Modified: Tue, 23 Jul 2024 23:25:17 GMT  
		Size: 5.8 MB (5756990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7813d58ababb7e7d8ba54bbbd48101520fa0576bdb0acf1ca74aae0e72e7a0d`  
		Last Modified: Tue, 23 Jul 2024 23:25:17 GMT  
		Size: 55.2 KB (55191 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:19fc282037f1609f65748ab8231a66833bd2691c0b05ff8e19bfd2a1df5e85e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.9 MB (158928027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da60467a4e4b6d42d017fd1bccdedd9e6feaa00204fb2dceb7c4c6527fb6988`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:58:11 GMT
ADD file:d8b037f30c0a2aeded43f72fe61531da3a0e449e034255bb0a7b2182e4e3ca8a in / 
# Thu, 09 May 2024 18:58:11 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV PG_MAJOR=16
# Thu, 09 May 2024 18:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 09 May 2024 18:58:11 GMT
ENV PG_VERSION=16.3-1.pgdg120+1
# Thu, 09 May 2024 18:58:11 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:58:11 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:58:11 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:58:11 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:58:11 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:58:11 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:48319744c6dacda7d13413becf85a83639982e97ecf615295a1257ccc3082721`  
		Last Modified: Tue, 23 Jul 2024 02:32:44 GMT  
		Size: 27.5 MB (27490099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147dd64dad16303f59cc3e1be657c732823eafc35b2fecb791beef9f87f13278`  
		Last Modified: Wed, 24 Jul 2024 02:19:21 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80197d984afce5448f82b413d0a8a4b1c927f69c4d55217b750a604403aa37d6`  
		Last Modified: Wed, 24 Jul 2024 02:19:21 GMT  
		Size: 4.4 MB (4391032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc3f2f201cb331a9ce6621cdd54fced414cfc7effa258b2d0da1fa55c1e3039`  
		Last Modified: Wed, 24 Jul 2024 02:19:22 GMT  
		Size: 1.4 MB (1412679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:584e80a0e3a1b55f93a2887e20eca5dbf0233ba83b19a2a2bf76cff1266da997`  
		Last Modified: Wed, 24 Jul 2024 02:19:22 GMT  
		Size: 8.1 MB (8120424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc20ebbefccc80a085f5a9f2faa9104a1cc455f9acc9a2168fa8b5e126001af8`  
		Last Modified: Wed, 24 Jul 2024 02:19:22 GMT  
		Size: 1.1 MB (1096714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a0c92b152583bb2e655eb8a54bc4d41ee91b67a6c1243783e12efbea940ca0`  
		Last Modified: Wed, 24 Jul 2024 02:19:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba46c1d5e6a922ff87a67637b633a0169fa6838c0fe4069f4b1967e687414b49`  
		Last Modified: Wed, 24 Jul 2024 02:19:22 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e441a588d4216cfeaf991c646e3735c6ed348dd1119a8c4dffa7211a1425d08`  
		Last Modified: Wed, 24 Jul 2024 02:32:42 GMT  
		Size: 116.4 MB (116396828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802b237106cdf9f3a37e823291e26f4ad7949a1d77262beb714b94e888294d23`  
		Last Modified: Wed, 24 Jul 2024 02:32:40 GMT  
		Size: 9.9 KB (9923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dabe9b24425342393cce5cdd84d431cf4fa4edde33b5d6118d15696beb799be`  
		Last Modified: Wed, 24 Jul 2024 02:32:40 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b9f31a1ebecd250163e08a33bf0cac9c0b538ba367cade4d421eba9ba6ea86b`  
		Last Modified: Wed, 24 Jul 2024 02:32:40 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b408819b723acdea1c5cdd9083efcb8d9d32677d0a00b330df4ff24197d4cd7f`  
		Last Modified: Wed, 24 Jul 2024 02:32:41 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d700d7e7b4b3729391439857480d414bdecaaa4f9636411b78a08b0aad60e1`  
		Last Modified: Wed, 24 Jul 2024 02:32:41 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:f7cb6b6fb0a070b5fc88657bd52049a22d48011b268cb774deea8a10a9383477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5804262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7972336b8744b3083305bf9b387641a7ab28a9812a2174ef19473f62812a3068`

```dockerfile
```

-	Layers:
	-	`sha256:3feac28c3f76620fd889b526259be864a904cdbfe52a1b1e2085484ff570b84a`  
		Last Modified: Wed, 24 Jul 2024 02:32:40 GMT  
		Size: 5.7 MB (5749143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05ece64460be6daa47b740b8623e4593c9d9ed0c6b20d14dbbc662de0aa281d0`  
		Last Modified: Wed, 24 Jul 2024 02:32:39 GMT  
		Size: 55.1 KB (55119 bytes)  
		MIME: application/vnd.in-toto+json
