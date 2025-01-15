## `postgres:15-bullseye`

```console
$ docker pull postgres@sha256:860206224dcd5c3d7e56a5b619ba6176dc89700de9395c4ad4b5c2c8dd483fc4
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

### `postgres:15-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:ab7c235016465211f07cbe6cdc09b6792090746664e047947f7a2c3418f8bbc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.1 MB (147094469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:944938d38db6f82e7b42deadd25f4f82f5d313ac494a2e83bcd0a87407b1c5c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 21 Nov 2024 20:12:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Thu, 21 Nov 2024 20:12:11 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:12:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:12:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
ENV PG_MAJOR=15
# Thu, 21 Nov 2024 20:12:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 21 Nov 2024 20:12:11 GMT
ENV PG_VERSION=15.10-1.pgdg110+1
# Thu, 21 Nov 2024 20:12:11 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:12:11 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:12:11 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:12:11 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:12:11 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:12:11 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cee854f4ada3396a4ea0be23d007e5389b14ce66117fb198ee37edc5fe0d88b`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 1.7 KB (1681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79c00a781fa3a9b68e6c3d0b4231c39348f8251dc61bad880f861f71e058bb2`  
		Last Modified: Tue, 14 Jan 2025 02:17:27 GMT  
		Size: 4.3 MB (4308198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1171dbbb0b7867709ccddad0d22f804e068c5736f39f40e7ab3a2fd63bb2df`  
		Last Modified: Tue, 14 Jan 2025 02:17:27 GMT  
		Size: 1.5 MB (1472238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41bb709a9c92413e29898bcc3a5928a63778f453181c990039445d791a21a785`  
		Last Modified: Tue, 14 Jan 2025 02:17:27 GMT  
		Size: 8.0 MB (8044543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86c1f7d3d782cb625a0337d30f50e967a94c2132980683691555859674cb002`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 1.0 MB (1038326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d585241da30a2c77dd10ae1a031e3d2a94a14195342c8aabe34308adcd0dbf`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40330d5e00c6a32fa319d01e33efa4e67c07c510d7e49094dcf4a62824be462f`  
		Last Modified: Tue, 14 Jan 2025 02:17:28 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1221c6023dcdd4b79e03ef7547711c2770931f3d5f78363d9ce40979dd763ab0`  
		Last Modified: Tue, 14 Jan 2025 20:33:16 GMT  
		Size: 102.0 MB (101957889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41103f649742ee9dca17747a65f38215db1cf89bc06ebd7f957c364eac9ada3e`  
		Last Modified: Tue, 14 Jan 2025 20:33:03 GMT  
		Size: 9.8 KB (9778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e71fea9a05ac2230ee13b027709152e45cf95ff33680a2e32fbe49e3653962c`  
		Last Modified: Tue, 14 Jan 2025 02:17:29 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4072fa9175f886036eb4de713dc416f2df2f866d28fef1c75326e4a0d9049d75`  
		Last Modified: Tue, 14 Jan 2025 02:17:29 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c4adb5742a6518ea47d5e8108e59a276b89e9f87fce7f4688692c1db5b640c`  
		Last Modified: Tue, 14 Jan 2025 20:33:04 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7103692fe50ed9b3852d8cfc2d4ed28827704df987cbf827e7bd5cd868296e5a`  
		Last Modified: Tue, 14 Jan 2025 02:17:30 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:58d161bb939ca02d867aaca5127447422b64d9f02781e2fb89ceadb1a88631bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6006905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7506db85a3adee9d8b7cdfdb78e862108710483efc6e62d6c45dcef1adce66`

```dockerfile
```

-	Layers:
	-	`sha256:3dd81e46a9457d435bff29a46586166f6ff6d78a0e5dd50fac3542b11c40f277`  
		Last Modified: Tue, 14 Jan 2025 23:59:43 GMT  
		Size: 6.0 MB (5952912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87296cf660940d61c6ad24fed5f5e4f87f812fc2de084fc1a6acd41945144940`  
		Last Modified: Tue, 14 Jan 2025 02:17:27 GMT  
		Size: 54.0 KB (53993 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:f68d6e008274aa307daec4255242a957229a721b9e3990703e42f7a52212b6e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 MB (135287917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:779b9338f15c72e70731dd4d3e8c98db0d8f89e6f6b8a3e9205272d65fff7cac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 21 Nov 2024 20:12:11 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
# Thu, 21 Nov 2024 20:12:11 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:12:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:12:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
ENV PG_MAJOR=15
# Thu, 21 Nov 2024 20:12:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 21 Nov 2024 20:12:11 GMT
ENV PG_VERSION=15.10-1.pgdg110+1
# Thu, 21 Nov 2024 20:12:11 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:12:11 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:12:11 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:12:11 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:12:11 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:12:11 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:61fe776d618d9b70bea09742b3fce817da0393e8911c90f01094c0a407e1f7bf`  
		Last Modified: Tue, 14 Jan 2025 01:35:53 GMT  
		Size: 25.5 MB (25533960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2bafc0b709fff1b657a14551940af81807048c74c63e503c511c438265ec89a`  
		Last Modified: Tue, 14 Jan 2025 22:00:25 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f975e0807809fe76bf2c4859de932ee50e6f49e947f5a1a49aad510b7684de`  
		Last Modified: Tue, 14 Jan 2025 22:00:35 GMT  
		Size: 3.6 MB (3601695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb6df2b8e257a7eda1d3c59549e23c34af700b4f6ac7656286fad61dc52de9c`  
		Last Modified: Tue, 14 Jan 2025 22:00:28 GMT  
		Size: 1.4 MB (1439249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef35b898de2c2ed26801408e41cde59d5ae6ebe8f9354ae4c2eab3de5580b8f3`  
		Last Modified: Tue, 14 Jan 2025 22:00:40 GMT  
		Size: 8.0 MB (8044364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73ef971477037a6fe33388a4295f2f293a338bca50b62cf9510bc34c9977f3c`  
		Last Modified: Tue, 14 Jan 2025 22:00:42 GMT  
		Size: 908.7 KB (908668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a7e95dea3feea2efaa0acb94dd3daae8af06bed3c1673ce2399262422fc4e3`  
		Last Modified: Tue, 14 Jan 2025 22:00:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2983901e72058651f8b788f2a7f436da5ebb614efbd37a8d48ea69113c2cded7`  
		Last Modified: Wed, 15 Jan 2025 01:01:03 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2196c726344414778395bd25f8a45a74d53fada502503dc64f10db50482562ca`  
		Last Modified: Tue, 14 Jan 2025 07:13:14 GMT  
		Size: 95.7 MB (95739370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbb16803ab64feae23d3d7f167597466dba1fe1ddff500a2e9cc519d41e8656`  
		Last Modified: Tue, 14 Jan 2025 07:13:09 GMT  
		Size: 9.8 KB (9784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4998a810fd6abee479204561f65c8d104444dfed1757750fe62104d0ca7633f`  
		Last Modified: Tue, 14 Jan 2025 23:59:54 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac65f9e20a4467ddf442ebd81599e7e089959a2f1635866b56e97f748193fec5`  
		Last Modified: Tue, 14 Jan 2025 07:13:09 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd61f9db6acb11b248d492bdfb61cbc33fdc637fd3252c8c8a33cd0f1eeb49fc`  
		Last Modified: Wed, 15 Jan 2025 02:43:03 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a125570bf02d80cbc2d700088da8041c6b8a2b3113120980d0b54ede4f228bfe`  
		Last Modified: Tue, 14 Jan 2025 07:13:10 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:ffe05a6fd55cb487863336eda1c425756d03e592cf0868d51e1e058b08d10a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6018556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433c705e28094c058460f9480efbc665a369ef693d2f791e832a5ad3aafec0e8`

```dockerfile
```

-	Layers:
	-	`sha256:617fc1a0ab0c0143445eea365b52a1e777ca82faafa56c08ce6aaf3649967475`  
		Last Modified: Tue, 14 Jan 2025 07:13:10 GMT  
		Size: 6.0 MB (5964375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7507030bdea64f7cad7a1c1045c15f58e890e1c870ce575e6a049a7d7cb9f50d`  
		Last Modified: Wed, 15 Jan 2025 00:00:00 GMT  
		Size: 54.2 KB (54181 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:36b1c58d78367a6e7c424d1aa61f4c41b109ac08709bc5c495f21dbac39bde84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144105013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db1690a28732f5cbc9121fd51d97870153d13af2e22a2570b8f1afba6e6b662f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 21 Nov 2024 20:12:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Thu, 21 Nov 2024 20:12:11 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:12:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:12:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
ENV PG_MAJOR=15
# Thu, 21 Nov 2024 20:12:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 21 Nov 2024 20:12:11 GMT
ENV PG_VERSION=15.10-1.pgdg110+1
# Thu, 21 Nov 2024 20:12:11 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:12:11 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:12:11 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:12:11 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:12:11 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:12:11 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b36d302f8a9da22724b01ad3edb1d16101fab82359501ca8f1feed2fc2cd201`  
		Last Modified: Tue, 14 Jan 2025 06:08:07 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531d7f5be2b7506d5ad4b9aff5db2ac3041e805a533f4f226b0006057cbf1ed0`  
		Last Modified: Tue, 14 Jan 2025 20:35:18 GMT  
		Size: 4.3 MB (4312801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98618b8f6d5579fa5d5505874305171812cc5f23c215fd441412809fada53f9`  
		Last Modified: Tue, 14 Jan 2025 06:08:07 GMT  
		Size: 1.4 MB (1404115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8846735e7d020e5fed1640cd37bcc70daae404ce5c1d5d70cb00643286ff7cd`  
		Last Modified: Tue, 14 Jan 2025 06:08:07 GMT  
		Size: 8.0 MB (8044511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d373474bba828255b5311627514305148190e7243cf38df6346071a766d7adc`  
		Last Modified: Tue, 14 Jan 2025 06:08:08 GMT  
		Size: 1.0 MB (1026607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063c700837a47de565dffe0d6108dfac3680dd70b24434882224f9c82eb1d03b`  
		Last Modified: Tue, 14 Jan 2025 06:08:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7204c081de27f53fd775f5cd9393cefa72aa0d51587aabcfec8910197dd81c5c`  
		Last Modified: Tue, 14 Jan 2025 06:08:08 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6514e3ace7fac02c067a8875d00f4c06c48421a5aa79620286002ac6a087bf60`  
		Last Modified: Tue, 14 Jan 2025 21:56:58 GMT  
		Size: 100.6 MB (100551449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df42a6058172ea8a0973fec002af8acb5e1f372341f2ac617d9c9650f19cf16f`  
		Last Modified: Tue, 14 Jan 2025 21:56:49 GMT  
		Size: 9.8 KB (9777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067161936a086e02d8a6af14ead594e139a64036219bb45419b29211fd907d10`  
		Last Modified: Tue, 14 Jan 2025 06:15:55 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a56c578f53fbcdddc2f7f6936f5db2aa40548aed00851032706d5c8509df38`  
		Last Modified: Tue, 14 Jan 2025 20:50:27 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ea513c55a5485a024af7a89e277b4aae591e71596e14760c25d6711e125eea`  
		Last Modified: Tue, 14 Jan 2025 22:03:56 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217a9e34717457e7f64e5f8082e3c6b8b951d7102dfdb56df303a81a2c22fde4`  
		Last Modified: Tue, 14 Jan 2025 22:03:56 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:df78905e8860be4ad1730ef160844d3a4731285d6b71165582e916f57feb21e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6013438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4738c53e924d7f1607e578612d34f4b47c5c87a48214ab8f2e79ccd3ca5a0f8d`

```dockerfile
```

-	Layers:
	-	`sha256:115adde7eb463f652ce2c7d4698dd047956adc9fd624ec4b553cbe838ae594de`  
		Last Modified: Tue, 14 Jan 2025 06:15:56 GMT  
		Size: 6.0 MB (5959200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e23d8669f055de3155b87a05a704d06396b65adf9ae913a1994e2f89f45dc44d`  
		Last Modified: Wed, 15 Jan 2025 05:06:29 GMT  
		Size: 54.2 KB (54238 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:b36f284d388838c99d85e929c144d21d6e90babf340d81a0d0929799d37c4e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155195488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee9567c4d227e958ad1e113725d1be871c4ddcaa702ba083a035869b6e19d7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 21 Nov 2024 20:12:11 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
# Thu, 21 Nov 2024 20:12:11 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:12:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:12:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
ENV PG_MAJOR=15
# Thu, 21 Nov 2024 20:12:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 21 Nov 2024 20:12:11 GMT
ENV PG_VERSION=15.10-1.pgdg110+1
# Thu, 21 Nov 2024 20:12:11 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:12:11 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:12:11 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:12:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:12:11 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:12:11 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:12:11 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a492ed0bb6cc66719b4111965f26bfd6269b1fc3ecb8620118584501f25cabde`  
		Last Modified: Tue, 14 Jan 2025 20:37:11 GMT  
		Size: 31.2 MB (31179029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fef1aee21e16f879fdefded590ff2baea6baa2397446ce7bff4c573ab465c80`  
		Last Modified: Wed, 15 Jan 2025 02:19:12 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f134a19149a253c144f57c8ebb1808737ef011854e1248c9b2669274d69675`  
		Last Modified: Tue, 14 Jan 2025 02:44:19 GMT  
		Size: 4.7 MB (4719667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472257d9eb58e6d20e39011bd098159ea33703c208c0ec16412dedb115aec3d2`  
		Last Modified: Tue, 14 Jan 2025 02:44:18 GMT  
		Size: 1.4 MB (1447760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573deb6c8e60be586d58d2cf7f5d7b697979d9ee26d115342a4c4e105abcc124`  
		Last Modified: Wed, 15 Jan 2025 02:19:19 GMT  
		Size: 8.0 MB (8044450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6aea253af9ef4393896d6fe071d6c6ddf9572e26aa3decf7e74f159a1f16013`  
		Last Modified: Wed, 15 Jan 2025 02:19:21 GMT  
		Size: 1.0 MB (1028897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce7e25dc80f6b5aa7771a5d32a9fe3deac7c90b56083c14776551cab6b5f9a9`  
		Last Modified: Tue, 14 Jan 2025 02:44:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e410bc3dcf84ed08e3ea6e6d8e5bfd10e3e7d7617ae93bbbfd786025e0b31a`  
		Last Modified: Wed, 15 Jan 2025 00:00:25 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd13f658d80f0305ed99c3c90d2913b13e7a9d609c0c1e8fc1e8cc29662a220`  
		Last Modified: Tue, 14 Jan 2025 02:44:23 GMT  
		Size: 108.8 MB (108755069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42e8b203d311f933dd4ea498df18306078daf2432c01b446e5ba02abdd30317`  
		Last Modified: Wed, 15 Jan 2025 02:40:33 GMT  
		Size: 9.8 KB (9786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e84709d605038c574f8983cdee6f14aabad08df16a7068cb6e250ce69a403a`  
		Last Modified: Wed, 15 Jan 2025 02:19:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36497cbe9750d941f175952e316dd4fc78f37a4af6737a74e051d5b0b8c411f4`  
		Last Modified: Tue, 14 Jan 2025 02:44:20 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697ec49de86312167ef1351a3b11ce58ab1d199dfb9f750ae256516def19e84f`  
		Last Modified: Wed, 15 Jan 2025 02:19:31 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5349b0abc97cd011e6e9f7799d1c7c351d682eddf13eb6ca30498c4fec0c4c2`  
		Last Modified: Wed, 15 Jan 2025 02:19:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:f4f3443512e61932585538173d7fb47915a977fd4db460b3d864144ff5f20ef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6016099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c83d01efbcb6d707c2191c37318b1a70bdcaf15bf22b7451c2360e9cdcc42e`

```dockerfile
```

-	Layers:
	-	`sha256:bef8c6d0916ffaafcbd640ef61551b122f667ba3031f1845391ffa59e65a9971`  
		Last Modified: Wed, 15 Jan 2025 00:00:42 GMT  
		Size: 6.0 MB (5962150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f29e467d84a03ae478afbdf2569e57eeb9eaf82522ce8f66ef791ce0b20d4f1e`  
		Last Modified: Wed, 15 Jan 2025 02:39:52 GMT  
		Size: 53.9 KB (53949 bytes)  
		MIME: application/vnd.in-toto+json
