## `postgres:15-bullseye`

```console
$ docker pull postgres@sha256:f91f2248e87bff8bc5b1040088148b53a3727cbe60e134589bf993e1aede847f
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
$ docker pull postgres@sha256:b6fea5c32fe7e53c5c744bf759669b4d67893ef3cfef10f4a10ac656876f04b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.3 MB (147257005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56fda0fd82ece111c75527a3d4a93451ad5b7c433c8ef9dab07f24ee2c205908`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV GOSU_VERSION=1.17
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV LANG=en_US.utf8
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV PG_MAJOR=15
# Thu, 22 May 2025 00:48:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 22 May 2025 00:48:07 GMT
ENV PG_VERSION=15.13-1.pgdg110+1
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 22 May 2025 00:48:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 22 May 2025 00:48:07 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 May 2025 00:48:07 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 00:48:07 GMT
STOPSIGNAL SIGINT
# Thu, 22 May 2025 00:48:07 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 22 May 2025 00:48:07 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Wed, 21 May 2025 22:28:05 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bfc2303f15259d3bbeb117f51c2bc18183cd019405e4e4b279f0e74334a5b19`  
		Last Modified: Thu, 22 May 2025 16:52:42 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08452701929850bce020fd65141f7f156365a4c736682e0237ee3cf1d7e72c29`  
		Last Modified: Thu, 22 May 2025 16:52:42 GMT  
		Size: 4.3 MB (4308118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:162e2cc58e7ee22a4c02cbde47e56f5ca092845abb7f3bb0e62165290fb0f941`  
		Last Modified: Thu, 22 May 2025 16:52:42 GMT  
		Size: 1.5 MB (1473573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c360302f7cb0537ecfafeadea0dc3beb7fcc4d8bb3f6c1e2a9e3971d42cb47`  
		Last Modified: Thu, 22 May 2025 16:52:42 GMT  
		Size: 8.0 MB (8045753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0411d4cd1a3ff08d8061317d78f2aa5a1492fadd5791b6e2f5b489e4f3b917`  
		Last Modified: Thu, 22 May 2025 16:52:43 GMT  
		Size: 1.0 MB (1038346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61887648e4b498884ff139167d09540bca8af948bce6e16abc49400e2b0193d9`  
		Last Modified: Thu, 22 May 2025 16:52:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba01a4fbfc68b69b22b87b9f7a7d7c050f581392c4e91fd2cac796d88680e4e`  
		Last Modified: Thu, 22 May 2025 16:52:43 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ead7a20e095b31f47ac74cfc629fbfa214269ea6fb442456701a8cc17804c19`  
		Last Modified: Thu, 22 May 2025 16:52:45 GMT  
		Size: 102.1 MB (102114600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5892f508a406ce1b6a441d1d6f67563fef30721e27159bc99e2fc8d7d3fcce`  
		Last Modified: Thu, 22 May 2025 16:52:43 GMT  
		Size: 9.8 KB (9775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6da7cc7f048853c7de43fc8ffacf8674736b76cca788d64e8e3891c79218322`  
		Last Modified: Thu, 22 May 2025 16:52:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef25c2a167eb41ecb84f3324cb9b3280c73895386caf6fb81e6c8baf128291f8`  
		Last Modified: Thu, 22 May 2025 16:52:44 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a013a6e8210bf84c31a28b80e2e8f4044fd95b12332105bae7e4157176e2e1`  
		Last Modified: Thu, 22 May 2025 16:52:44 GMT  
		Size: 5.5 KB (5473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58bb03a5cdf50dc864f2e0be715e8721966d41ce4c544faaba7a116665ab01f`  
		Last Modified: Thu, 22 May 2025 16:52:45 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:94735dbef7c14f0c423c878f023460edd45113b980267bd89cbd6de328ad0126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6065320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d371b1546a42c98740ba9899a92fadfb2dec1552cd69177e06664d74c18d22d0`

```dockerfile
```

-	Layers:
	-	`sha256:36f20ea2c730143427d272d36bc5d6b1d0acf7cbae3b1d3210b5376c15439c1a`  
		Last Modified: Thu, 22 May 2025 16:52:42 GMT  
		Size: 6.0 MB (6011975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:011515030ba3e61a79b785ec61a13d1efabfc8cea583754c6306d4702a95accb`  
		Last Modified: Thu, 22 May 2025 16:52:42 GMT  
		Size: 53.3 KB (53345 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:9b00c6d098f24f76da71d964e179e137710158472aadae8eb46099f6f483b818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 MB (135439066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0bab8f9f1cc131f1f9d5fb7880193b15e7189c92923a159d2912f751fdae07b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1747699200'
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV GOSU_VERSION=1.17
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV LANG=en_US.utf8
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV PG_MAJOR=15
# Thu, 22 May 2025 00:48:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 22 May 2025 00:48:07 GMT
ENV PG_VERSION=15.13-1.pgdg110+1
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 22 May 2025 00:48:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 22 May 2025 00:48:07 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 May 2025 00:48:07 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 00:48:07 GMT
STOPSIGNAL SIGINT
# Thu, 22 May 2025 00:48:07 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 22 May 2025 00:48:07 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2091b63a268a34467e23520ae27c312421298f420abd278e760061e42a678899`  
		Last Modified: Wed, 21 May 2025 22:28:43 GMT  
		Size: 25.5 MB (25543902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2819feb174cd62d9afe4efa58f14c05d6404e45e9fd646186b5caf9e4ffb95`  
		Last Modified: Fri, 23 May 2025 06:01:46 GMT  
		Size: 1.7 KB (1679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b854a91797948fa74505443fa76802d4719c60aea4cc87fd15783f71c9acfd55`  
		Last Modified: Fri, 23 May 2025 06:01:47 GMT  
		Size: 3.6 MB (3601790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6970d22b731c3a99427af1912f1730e34e40009bc7af854735159a9603ffa3f`  
		Last Modified: Fri, 23 May 2025 06:01:46 GMT  
		Size: 1.4 MB (1440887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a3cd249b6bf25ca9bbea16ab2a0959459eff6af0e43e16d8c956d2888065c1`  
		Last Modified: Fri, 23 May 2025 06:01:47 GMT  
		Size: 8.0 MB (8045791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d46adcc9f43b0fd86209d8380e586d2c3465d713fe7c68169a9b3899cfd39f0`  
		Last Modified: Fri, 23 May 2025 06:01:48 GMT  
		Size: 908.7 KB (908651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6aa3404576c56b7e91cee8f6cec2f6cd80e371cbe93a5a27e90528f7ed08518`  
		Last Modified: Fri, 23 May 2025 06:01:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd2b53fdac06669f7ad19fd8504e96e7e1429ba317a634f81a63c8d05cc0b2c`  
		Last Modified: Fri, 23 May 2025 06:01:48 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0da845d8b8d30e9672bb41fc4ce21ec0005aa10107fd52e7959d23a437214d3`  
		Last Modified: Fri, 23 May 2025 06:59:10 GMT  
		Size: 95.9 MB (95877377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16cd18c89f6661d36176db3d0b3a3c4ca3c069c6a4f70df155e9d7894436c0f`  
		Last Modified: Fri, 23 May 2025 06:59:07 GMT  
		Size: 9.8 KB (9779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34740b9f1a02cf05968241c41fa23b59d5559f5d3841cb4b27045adcaafa3b8`  
		Last Modified: Fri, 23 May 2025 06:59:07 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfbeb18e8711a8b1e25e2985d1f1fface4d39627e663b0abe383de761414250`  
		Last Modified: Fri, 23 May 2025 06:59:07 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfbbc68eec6c2bc9d73212983a99969d19c978626134008953e0a9d533c655f`  
		Last Modified: Fri, 23 May 2025 06:59:08 GMT  
		Size: 5.5 KB (5472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450c803d21262a56a7e679662741c25608faaf98b38e6ce532bb805a8fb4c576`  
		Last Modified: Fri, 23 May 2025 06:59:08 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:fcf367972a38d23486d9d646a292d5c46aca82d59c6f4ac74bded8d3df0d3ea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6076928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb478e4705e0335b2abee9a3b77d6fa6c5f3e36a2dcf5b83be4d8f2dca7e9aca`

```dockerfile
```

-	Layers:
	-	`sha256:2d696746d924692931ce8449e6ff4f035486a502c88b3190f7bf4cc59b4e6ee5`  
		Last Modified: Fri, 23 May 2025 06:59:07 GMT  
		Size: 6.0 MB (6023395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b264e8c68130984f48d47e4e93ffb0e56fb083114e52565b8430bf0b2b7cacd3`  
		Last Modified: Fri, 23 May 2025 06:59:07 GMT  
		Size: 53.5 KB (53533 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:9c0e7bfda0c6522a53b2a52f445e4429c99079ffeaeca621d9c2507b5a021e83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144279683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c940c9d64e0fcf423b91da374a0b261de11ba4feee7c237ad9b548025553eda`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV GOSU_VERSION=1.17
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV LANG=en_US.utf8
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV PG_MAJOR=15
# Thu, 22 May 2025 00:48:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 22 May 2025 00:48:07 GMT
ENV PG_VERSION=15.13-1.pgdg110+1
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 22 May 2025 00:48:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 22 May 2025 00:48:07 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 May 2025 00:48:07 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 00:48:07 GMT
STOPSIGNAL SIGINT
# Thu, 22 May 2025 00:48:07 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 22 May 2025 00:48:07 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Wed, 21 May 2025 22:28:28 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32236ba1b821f7c23d25fdf75521f88c96d3223ff4d2910edd70bd6adab8c233`  
		Last Modified: Thu, 22 May 2025 02:08:46 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0d3b9230c80850de668fac2e5bd9a62e220978ee0fc44a5884f3bd6f86f489`  
		Last Modified: Thu, 22 May 2025 02:08:47 GMT  
		Size: 4.3 MB (4312803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:defd546e9378a792a8305e5024aab05e8b5bf2e0d6d7bd768f72c42fe731a75d`  
		Last Modified: Thu, 22 May 2025 02:08:46 GMT  
		Size: 1.4 MB (1405889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb1b788a19b9e3bca37df18caa5a08422119f78322397fb5bbced6505d845a2`  
		Last Modified: Thu, 22 May 2025 02:08:47 GMT  
		Size: 8.0 MB (8045785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef0ec8ddfab83b5e0deb2e20fd330b90628b37ee9ace4ef9d685519eb8d637f`  
		Last Modified: Thu, 22 May 2025 02:08:48 GMT  
		Size: 1.0 MB (1026595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1137dc2ab794992162498823a64a9165a7a2c92fe8f04754a932bae9919e8be`  
		Last Modified: Thu, 22 May 2025 02:08:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a6988ceff54ce62d68edc1d1a0a5056cd10320ba65103b42820fb1f0388ad6`  
		Last Modified: Thu, 22 May 2025 02:08:48 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b441d85912fa293da9f4a83bf9aa3aa30e17de4ce84f0b80026d27e75a7fe9`  
		Last Modified: Thu, 22 May 2025 20:09:01 GMT  
		Size: 100.7 MB (100721678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c16a7bee040cab51b75adc29d556f173d45630f793ebcefd94e5dd57674c873`  
		Last Modified: Thu, 22 May 2025 20:08:58 GMT  
		Size: 9.8 KB (9776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e288b4739b7b052815dd9cc49c6c501ab22c581dc37e1fcd01dc64b497276d76`  
		Last Modified: Thu, 22 May 2025 20:08:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344ad189550c1489ff05a9f6a30a14bcf2325420141cd28fb1b341f52b0143b0`  
		Last Modified: Thu, 22 May 2025 20:08:57 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d2a587aea3ad149a490c09bfcef1c80b8f61e1cdef18f6ade69bc99d742848`  
		Last Modified: Thu, 22 May 2025 20:08:59 GMT  
		Size: 5.5 KB (5473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988767c2439372592266e14a352cea3bfead2bc2af565fb8cb0a7294c5daf0e9`  
		Last Modified: Thu, 22 May 2025 20:08:59 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:5b6811b5cc74c47902d37e7e2be61355baabd1c5f64ec4e07a100a23b1197482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6071853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d740aec394823789deffa3915bde3bbf15e5e5655d440fba3b4efc790dde0cd`

```dockerfile
```

-	Layers:
	-	`sha256:3f6103cb4ab15ff8959a2572bcb2a9f94344a4c01223db94d9fa0fe05024b863`  
		Last Modified: Thu, 22 May 2025 20:08:58 GMT  
		Size: 6.0 MB (6018263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da7ce8f497e92064a8977eb9495efc18b4a1ed016f47369f0ce10c2dedb7e57a`  
		Last Modified: Thu, 22 May 2025 20:08:57 GMT  
		Size: 53.6 KB (53590 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:2e828bad8ff3157b20c858bcc9f040a3407b202e8e3433064eb4cdd8149b76dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155361893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e1c46407938b593e5828dc3bfeb2bdffc1d7678642d6f639b83fbc04d046b99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1747699200'
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV GOSU_VERSION=1.17
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV LANG=en_US.utf8
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV PG_MAJOR=15
# Thu, 22 May 2025 00:48:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 22 May 2025 00:48:07 GMT
ENV PG_VERSION=15.13-1.pgdg110+1
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 22 May 2025 00:48:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 22 May 2025 00:48:07 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 May 2025 00:48:07 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 00:48:07 GMT
STOPSIGNAL SIGINT
# Thu, 22 May 2025 00:48:07 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 22 May 2025 00:48:07 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:12052fdf3ab2e6e9fdb28b8a21b88f649fc9d652cf2290c0d091eadc22d4fb91`  
		Last Modified: Wed, 21 May 2025 22:28:00 GMT  
		Size: 31.2 MB (31189200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d569cb295f4c867549dc6a2945e2edf500550ff8166a6fd77747ba496acba8fa`  
		Last Modified: Thu, 22 May 2025 17:04:37 GMT  
		Size: 1.7 KB (1680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:824c8e0522556e45617a4fb3167bd327fab07e83b762ea230955fc9c98d7a02e`  
		Last Modified: Thu, 22 May 2025 17:04:37 GMT  
		Size: 4.7 MB (4719675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9e9a0517498a02c06a7d554af6be87117e52a03ebc7ca873d1c3bd9c16beaf`  
		Last Modified: Thu, 22 May 2025 17:04:37 GMT  
		Size: 1.4 MB (1449291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a163363cbe738a42c1bd61b6ce245f04af07725b6677df338ed8feba3739cb55`  
		Last Modified: Thu, 22 May 2025 17:04:37 GMT  
		Size: 8.0 MB (8045644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af232f0df08ab5b8b46b2d2d7cfdb8f234adcab25ecac3fc5ce3c16038469ea6`  
		Last Modified: Thu, 22 May 2025 17:04:38 GMT  
		Size: 1.0 MB (1028914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34799c93bdbcf00dd84fa14a56b2396b4a47514bec80f8a71e4109a2d1f448fc`  
		Last Modified: Thu, 22 May 2025 17:04:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16a2d77e32127fbaf2b1c4a977da9661523e50f6f402e585bb15a9395291a01`  
		Last Modified: Thu, 22 May 2025 17:04:38 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae2034a857ec52e311778ed4eab0bdd62fa659f7c05fde6522d78a31ede2bc3`  
		Last Modified: Thu, 22 May 2025 17:04:41 GMT  
		Size: 108.9 MB (108908497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f796116d4cb5bb0c7c172da031317a9769703080757214e205316d347d09e71f`  
		Last Modified: Thu, 22 May 2025 17:04:39 GMT  
		Size: 9.8 KB (9779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed75a96c0c5aef77b43d909377cc16c6285bb7719890ac5d7021b52af7b73ca2`  
		Last Modified: Thu, 22 May 2025 17:04:39 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1a9217a441162986d9e1eab611557759d9807a04619ac4d6a93ca5ef33ec42`  
		Last Modified: Thu, 22 May 2025 17:04:39 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8a31220218959b6de21b2627496488c5084dd571f95002ec5d556692e388b8`  
		Last Modified: Thu, 22 May 2025 17:04:40 GMT  
		Size: 5.5 KB (5473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f59260a76b4f4f75e7ff884241f3f990443c24458eded7518a92fd3b101fba37`  
		Last Modified: Thu, 22 May 2025 17:04:40 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:c9c65ce90d70c6efb947ee4766e20a0ab02e9c57db41497d8d5b82c2091f0eb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6074831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ef380cad264deb7db69f0ee90c9d80fa97d296c99b0627eb20843458a241d03`

```dockerfile
```

-	Layers:
	-	`sha256:13f65fa99d7a79cb20704bfcaabec7650d5738c5969cd935949d1d495501af43`  
		Last Modified: Thu, 22 May 2025 17:04:37 GMT  
		Size: 6.0 MB (6021530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0993120d5fd7364eebb56b235f96482408254a0b5e6e86901fdd903c88666f93`  
		Last Modified: Thu, 22 May 2025 17:04:37 GMT  
		Size: 53.3 KB (53301 bytes)  
		MIME: application/vnd.in-toto+json
