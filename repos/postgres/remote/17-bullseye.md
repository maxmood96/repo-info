## `postgres:17-bullseye`

```console
$ docker pull postgres@sha256:b55c8ea317ef3491a7eb1ff79447b14f17ee0a6890a3cfe94746b21b2ba9f635
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

### `postgres:17-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:83ee9e9700768865cffc188842c87257bc4f86ca8ba7770cd5e71a2a2b6075fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151570834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcabd3716b6b05561deb541889507de8e87dc1bc499f774fb3c63916a36b7492`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PG_MAJOR=17
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PG_VERSION=17.1-1.pgdg110+1
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 19:48:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 19:48:01 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 19:48:01 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 19:48:01 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 19:48:01 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa1285f79e328901401ba4d32d3aabd2b56680e3b1adff22bef49439a724b2d`  
		Last Modified: Thu, 14 Nov 2024 21:06:59 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c583857a1438149df6255baeae87d84370c37175f9df768a4c8d4a8e38a715e`  
		Last Modified: Thu, 14 Nov 2024 21:07:00 GMT  
		Size: 4.3 MB (4308216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391d22e68cf0b42d7dce25bbe2c3328be9f3251199b65ffc0cb997679b12d946`  
		Last Modified: Thu, 14 Nov 2024 21:07:00 GMT  
		Size: 1.5 MB (1472230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bcf2142687c7095bfc2b238a2abae2a0cc56341e296e7cd91ea9703e301c98`  
		Last Modified: Thu, 14 Nov 2024 21:07:00 GMT  
		Size: 8.0 MB (8044571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b0befdfaa04dc25fd53ed5116c9ac89ef7b193daf18bc06fe1edc03556c5065`  
		Last Modified: Thu, 14 Nov 2024 21:07:01 GMT  
		Size: 1.0 MB (1038366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4540e3e0ca693f9fb9750c8dc603cc0869ea6aefddc37d5973889a3b4e4b1074`  
		Last Modified: Thu, 14 Nov 2024 21:07:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ce6783251fa965360a85902eff8b4d26768b98d658d1491e39834eb638d12b`  
		Last Modified: Thu, 14 Nov 2024 21:07:01 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90823a5fa9b5fd80f4943ac398a72d8b8570e335281af65a07bbe2c33ee26ee0`  
		Last Modified: Thu, 14 Nov 2024 21:07:03 GMT  
		Size: 105.2 MB (105234813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f150cd2496e1a815a1902372c9b7ca428291c0ccb737c28aacdf2433651687`  
		Last Modified: Thu, 14 Nov 2024 21:07:01 GMT  
		Size: 10.2 KB (10234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbd95d53b8deb148b6b4685fa2a8677d9723ce8f0ce2e5d95881f66d7e669fd`  
		Last Modified: Thu, 14 Nov 2024 21:07:01 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bef37d383e8fb24106c0379b7fb2458534e8af8cf3d8503811844f61c568a62`  
		Last Modified: Thu, 14 Nov 2024 21:07:02 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae4b0db1dad7a4fec43f8ac81c4c3799e8f7152487e3e483b5801d376f9e0d5`  
		Last Modified: Thu, 14 Nov 2024 21:07:02 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15132f4da407f144736e7991d84575f4d86882c09f26c6c5903e4d078a7eaab5`  
		Last Modified: Thu, 14 Nov 2024 21:07:02 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:684d4ff08f6bf23dc7708079686ee64bb80ec414e374c36dd6a2cfbe4462525f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6097646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01259c81d2a1563353b5a0186dbbae4f2542fed66a2c5c0b6f2720303fec69b6`

```dockerfile
```

-	Layers:
	-	`sha256:edb7383844e7c1de47e6f0be4d607f0e58e3da93b2c3cae9c406f1b2ebbb6004`  
		Last Modified: Thu, 14 Nov 2024 21:07:00 GMT  
		Size: 6.0 MB (6043349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bdf1f7e8307cb1d99eb6888a74f273f361614d3a43dd45e3010371c97396037`  
		Last Modified: Thu, 14 Nov 2024 21:07:00 GMT  
		Size: 54.3 KB (54297 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:d0e2073f439f0f5f4479fc7258a3aaf7d56fc4702ac247c98bb90582dcc7aa8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139649556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05d5199b354d0e61bd5b063e3b6d567a594b0cba38e1984b33a5c2bff8d7b96e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PG_MAJOR=17
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PG_VERSION=17.1-1.pgdg110+1
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 19:48:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 19:48:01 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 19:48:01 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 19:48:01 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 19:48:01 GMT
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
	-	`sha256:1ebfd5904bbab9e15e406aa940993ce97e0bfa3ba6b6931b711237506159d729`  
		Last Modified: Thu, 14 Nov 2024 21:39:36 GMT  
		Size: 99.0 MB (99024891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea243e2658b93838e1c04b7ca785e57a9af931d05d1e30b9901b3bfcbf24c6f`  
		Last Modified: Thu, 14 Nov 2024 21:39:33 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00baf9cec6d094579d8b3ee64d78c246e639991c97a62f653326e204ccfeb23`  
		Last Modified: Thu, 14 Nov 2024 21:39:33 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e0b11ed42b77f4611761b05dd8d871f9fd5ee9a76f4ee865a31325b82ac452`  
		Last Modified: Thu, 14 Nov 2024 21:39:33 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79ec0f3fae5d3ea6c5ff1f1105c59385af168d0fa76905c9e5a1bdddd7ec7dc`  
		Last Modified: Thu, 14 Nov 2024 21:39:34 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f361e170d94e77cf19f98d9921786dd510d7835f24cd8568d6c20441944bcf6`  
		Last Modified: Thu, 14 Nov 2024 21:39:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:e5ebb14cb4d78c7b568b0052508d994647873b96c36b27da8e275bd0fa2e634f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6114983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faabc4bb3fb6574133f913d3f48d8339d62ad62a47821cb01d720397a724767a`

```dockerfile
```

-	Layers:
	-	`sha256:24b5f93c0af5bed5c4028ff73a4ae46b01a266ea29cd4428317c1bb99345146c`  
		Last Modified: Thu, 14 Nov 2024 21:39:33 GMT  
		Size: 6.1 MB (6060490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96fbcd36e5a791c53336b1e0c85eaacb06b882fc371fa695f347535551a7569c`  
		Last Modified: Thu, 14 Nov 2024 21:39:33 GMT  
		Size: 54.5 KB (54493 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:51de65771a58aa6b5462191f8f51e379ce2e12eda16248ce2648edfb617768dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148718708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d54bebfaf133ac6f90789498060277a6d0878ff61520a829eeaa55c4fa6dd3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PG_MAJOR=17
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PG_VERSION=17.1-1.pgdg110+1
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 19:48:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 19:48:01 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 19:48:01 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 19:48:01 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 19:48:01 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625705541eb2c232ec6868052605994a58fd1783ec6af4d33d62324beabdd4ce`  
		Last Modified: Tue, 12 Nov 2024 09:10:50 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86ef8349dcde0e9538a12f2b24d39955b32259d90fd9226e4b09e83a23c6eea`  
		Last Modified: Tue, 12 Nov 2024 09:10:51 GMT  
		Size: 4.3 MB (4312806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408ba174abce076b100b1775066ae161d8f3c617fc9f8c9c5f24d6d9452e4822`  
		Last Modified: Tue, 12 Nov 2024 09:10:51 GMT  
		Size: 1.4 MB (1404090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1823cb8ddc148ec3c8dec960e1f98604509d055e771c71cd86a89084c02d09`  
		Last Modified: Tue, 12 Nov 2024 09:10:51 GMT  
		Size: 8.0 MB (8044346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4ea35053fdfd2a5d6a7dbf5900c78c319262391884c26e2fcc89dddee4be76`  
		Last Modified: Tue, 12 Nov 2024 09:10:52 GMT  
		Size: 1.0 MB (1026586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37385ec28429364a4917c18b2047c5afbbf75d0d2d92d13edaa098af60ce190d`  
		Last Modified: Tue, 12 Nov 2024 09:10:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c022894a4b9e1da9147eceeaa4898b06811b419e7f3efb2aefdf946bb2f7d4`  
		Last Modified: Tue, 12 Nov 2024 09:10:52 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d75f72ede900ca55060d0dfaf1dbf0b59bfb09830acb42b16509034fe9865e`  
		Last Modified: Thu, 14 Nov 2024 21:07:41 GMT  
		Size: 103.8 MB (103818210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da2177210794c0d62bce7b9121db75b8be042e80bad05ad804f708bd61e64f5`  
		Last Modified: Thu, 14 Nov 2024 21:07:38 GMT  
		Size: 10.2 KB (10234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7edeec942767e90baa3e6fe821b499794fd37004756c1c17bd6e51348107d4`  
		Last Modified: Thu, 14 Nov 2024 21:07:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c582f7f9dc91f69474e3b59b61de460a378eaaf491203b2a06e9a70218cd22bf`  
		Last Modified: Thu, 14 Nov 2024 21:07:38 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a056f38827e9eddf78a3f3170b5e9f7369ee2db875fca95d85e1c9579ba5f69`  
		Last Modified: Thu, 14 Nov 2024 21:07:39 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc459b587dfd73903836666603163337ad784645279d7f3507b38909892c404`  
		Last Modified: Thu, 14 Nov 2024 21:07:39 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:d8781b35ca6eef8383bf2df9e01ee287447c2a0efb8129ab2f1ff90fd00e02c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6104209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af551df9b737ae4e3bda31cae9fd24e4acdd29d6edc205ae2f139e4f6021e3e0`

```dockerfile
```

-	Layers:
	-	`sha256:8753613f38013ecb288a66e8e65534047806e4c6cd3bee691008c88f00e75a5d`  
		Last Modified: Thu, 14 Nov 2024 21:07:38 GMT  
		Size: 6.0 MB (6049655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3625a2b773031742ee79156b96b775fe6cc7b9617bda526c4ab3b8206b9431d4`  
		Last Modified: Thu, 14 Nov 2024 21:07:38 GMT  
		Size: 54.6 KB (54554 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:4047e8014f13a7c7c21092271d4460309e834be28b976607a95d184a7eb62946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159855321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98980f8041cca99525f9569133143b6d80719623ff7a54e880d0db66cb6113f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV LANG=en_US.utf8
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PG_MAJOR=17
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PG_VERSION=17.1-1.pgdg110+1
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Nov 2024 19:48:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Nov 2024 19:48:01 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Nov 2024 19:48:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Nov 2024 19:48:01 GMT
STOPSIGNAL SIGINT
# Thu, 14 Nov 2024 19:48:01 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Nov 2024 19:48:01 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2aea24d0416284c8bc498d91bac1c90e2bf12b01e7867f799161bbb874a8323b`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 32.4 MB (32423351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9527a45eac1e8aac30ad51ee4805c88d8d7e123e01d937354a24ef7ce1bfb1`  
		Last Modified: Thu, 14 Nov 2024 21:19:58 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d35ec081489f678f932be8f2aea50d36888f67d1968c83baa984c55899fb9d`  
		Last Modified: Thu, 14 Nov 2024 21:19:58 GMT  
		Size: 4.7 MB (4719633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98690596b9e085fcc5c56921c74d9ac266add2b860ebb418fac93202acd021c1`  
		Last Modified: Thu, 14 Nov 2024 21:19:58 GMT  
		Size: 1.4 MB (1447773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e155a110bfaaa72bba45e6c64cd5794f04a02c2c38f044ac318f7bd15e980609`  
		Last Modified: Thu, 14 Nov 2024 21:19:58 GMT  
		Size: 8.0 MB (8044433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43431552942b9a05c56c8c70d613282aef64cfa7c3354db74fa0c30bffcf81d3`  
		Last Modified: Thu, 14 Nov 2024 21:19:59 GMT  
		Size: 1.0 MB (1028913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5288e76755f1e54cdfa8c263698a118637b095b1813a31c77c0dc66b7f3385d`  
		Last Modified: Thu, 14 Nov 2024 21:07:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d15e44eae04ae50202ef550dccfb7948446d8ae8fb2878eca9843b2365edb7c`  
		Last Modified: Thu, 14 Nov 2024 21:07:09 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8bcdb632530e9ece4ce9ba871f94c83eaafd59c4ff803455595ad44f22b3d76`  
		Last Modified: Thu, 14 Nov 2024 21:20:03 GMT  
		Size: 112.2 MB (112170141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b679621b71465f72f325dee5a38c51d622d1d7880a0fa90de134b0b08a90fc`  
		Last Modified: Thu, 14 Nov 2024 21:20:00 GMT  
		Size: 10.2 KB (10237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5b880160b62e4b3104adabbca8ecee3dbbac4dc054286c3f8097d8335f2f89`  
		Last Modified: Thu, 14 Nov 2024 21:20:00 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e2b65f1f43b56785089bb41b32ebea2b44f3bddf3e1248876f43fe4b95adcf`  
		Last Modified: Thu, 14 Nov 2024 21:20:00 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04470e78d68d703b23af8b249c4a31669456f1dd980cdbf439a90e1c8b08f5c`  
		Last Modified: Thu, 14 Nov 2024 21:20:01 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5214929a854afaa4eeed00812f87da980d477ddb583cde1a4e69cad7b2ba9497`  
		Last Modified: Thu, 14 Nov 2024 21:20:01 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:472d9dbfeab627852cae4a6fee027100810e05be95a1d748dd03ebb2a6c33130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6112501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a373ba693e8d9c3c1611f45e7bddf6a7d2a6677d69e674cb9fcdbbdcf6f6355`

```dockerfile
```

-	Layers:
	-	`sha256:9990f148b09bc027098d8d8f1bccac6932be66a9e3974a7f4a5deede8036a27a`  
		Last Modified: Thu, 14 Nov 2024 21:19:58 GMT  
		Size: 6.1 MB (6058254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3b918952f497366019fd1d9c9839b5aa6e4aa76f7bc5377eae585178a853f5b`  
		Last Modified: Thu, 14 Nov 2024 21:19:58 GMT  
		Size: 54.2 KB (54247 bytes)  
		MIME: application/vnd.in-toto+json
