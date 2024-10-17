## `postgres:17-bookworm`

```console
$ docker pull postgres@sha256:7fe89c9e6879372f435dddacc4eb27785f48cdab345cb3052208705222f92376
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

### `postgres:17-bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:c92692786bdc336dd7abac4da89abc710abbe426821a1d053b178f77c1f697a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154576974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d57ed788c15419329a4d7d4f09f1f4a49bc0e0957c3d4709f31faf21b1e4c6c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 26 Sep 2024 18:19:57 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 26 Sep 2024 18:19:57 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV LANG=en_US.utf8
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_MAJOR=17
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_VERSION=17.0-1.pgdg120+1
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Sep 2024 18:19:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 18:19:57 GMT
STOPSIGNAL SIGINT
# Thu, 26 Sep 2024 18:19:57 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Sep 2024 18:19:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ece9c40e2bdc0cfa6346c1704f4fb1d07d3fdea7457e37a1b8ea7228fdd75d`  
		Last Modified: Thu, 17 Oct 2024 01:25:21 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241e5725184f79fcf7276790cec53ce57126de0b2178fd21e3e44a2f1146ef82`  
		Last Modified: Thu, 17 Oct 2024 01:25:21 GMT  
		Size: 4.5 MB (4533657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6832ae83547ede1f11b059963f1c5da8885290d2ba7f89c97ba6f474fdb2df6d`  
		Last Modified: Thu, 17 Oct 2024 01:25:21 GMT  
		Size: 1.4 MB (1446614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db87ef10d0d831866e55b7bd071f9e369095f533b6c3a0a26717e9db2f0cdb6`  
		Last Modified: Thu, 17 Oct 2024 01:25:21 GMT  
		Size: 8.1 MB (8066248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979fa3114f7b922b2396076d9ffcfea29bc31232dd52165b05a99c8b98fb944c`  
		Last Modified: Thu, 17 Oct 2024 01:25:21 GMT  
		Size: 1.2 MB (1196027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2bc6009bf64ed31a5785667ebdae9de4d8754c01e953aaacea72df71f377d70`  
		Last Modified: Thu, 17 Oct 2024 01:25:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9097748b1df9c81fddea6d64e454f4bd21a945bb978d6941cdb37837e983a7c`  
		Last Modified: Thu, 17 Oct 2024 01:25:22 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5c934890a853f78b094dbb09bfeef9b83af84a6fded799efd39023166662da`  
		Last Modified: Thu, 17 Oct 2024 01:25:24 GMT  
		Size: 110.2 MB (110187583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14a7815879ec78509e6b8522efe6cc5030cfc2e8a85a36f3860ffc0fcf8b81f`  
		Last Modified: Thu, 17 Oct 2024 01:25:22 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442a42d0b75affd793311cb3216843ae4161bf6faddf4aa266f740338dd122e8`  
		Last Modified: Thu, 17 Oct 2024 01:25:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82020414c082d91508001372610c92ec9d0c63b4d15d071120ef500c52b667f2`  
		Last Modified: Thu, 17 Oct 2024 01:25:23 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ce4c941ce70acf2b14f71ebe28eefa5a3614b35e7b5d1d7bebfaf8d8464ccf`  
		Last Modified: Thu, 17 Oct 2024 01:25:23 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e63a35cca788a2e2fef00b3663c1a5aa582b7ae265b71c4ec479bdabff5307`  
		Last Modified: Thu, 17 Oct 2024 01:25:23 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:0743f713bba9ddfe25fca5ce26e91ed95fcea450374ec979bf97e8cb6f821a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5819892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4236cb2c9a2687efc589d0f0b00934b17b4a6fe31b02a086f2ef2eb52d8ac516`

```dockerfile
```

-	Layers:
	-	`sha256:1b4e366c2f009e96ea9dc41c4e6a56b0fae226208d93e4e28c31a358edf10050`  
		Last Modified: Thu, 17 Oct 2024 01:25:21 GMT  
		Size: 5.8 MB (5764809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba3cbaf85219adba7ca65ea9725393bd126facb34468a33cf89cdf08e4dc7d81`  
		Last Modified: Thu, 17 Oct 2024 01:25:21 GMT  
		Size: 55.1 KB (55083 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:37bf3aebca71a9ab395fc0fc3e81ff3caabf670e71eb0f7147e1d26f5773e982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.3 MB (147286352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a835f896fef526b9dd2b272dbfbca6130424a5407183b9a420372f70647e8c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 26 Sep 2024 18:19:57 GMT
ADD file:c8ec8d65b2f61866a2c6085ed61e936733bc484abeeba1b91d12b9f6a97e456b in / 
# Thu, 26 Sep 2024 18:19:57 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV LANG=en_US.utf8
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_MAJOR=17
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_VERSION=17.0-1.pgdg120+1
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Sep 2024 18:19:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 18:19:57 GMT
STOPSIGNAL SIGINT
# Thu, 26 Sep 2024 18:19:57 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Sep 2024 18:19:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e51d4479d9f15eaafec663087c05baede0a0724dc30787f7912ade3b686f46b1`  
		Last Modified: Thu, 17 Oct 2024 00:57:27 GMT  
		Size: 26.9 MB (26887306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c4b9c03e068ba51c9db6968c5c7926dbe2e63d9b1be958b3a00fe12b69f122`  
		Last Modified: Thu, 17 Oct 2024 07:15:45 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac6db515ecbec72300ce1b73c9e17c39089c00bacda65344f1f7815e5e8f916`  
		Last Modified: Thu, 17 Oct 2024 07:15:46 GMT  
		Size: 4.2 MB (4150880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffced63b7b42201f05313de959b51a818e77f10e5df2c0f0cb7ef7d97f71feeb`  
		Last Modified: Thu, 17 Oct 2024 07:15:46 GMT  
		Size: 1.4 MB (1423860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b875211335a8d380f0a52c221c220c0c2b21012d06ae3f574c935b47c03d3c2`  
		Last Modified: Thu, 17 Oct 2024 07:15:46 GMT  
		Size: 8.1 MB (8066414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d7d3f01969c6f45756b4912cd7fff41f1120257fd0f64dc59fa672002bf9fe`  
		Last Modified: Thu, 17 Oct 2024 07:15:47 GMT  
		Size: 1.2 MB (1194856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff6d55049eee539ddcde0b30f52c8571485adc69270b60840d4b1f718d9b967`  
		Last Modified: Thu, 17 Oct 2024 07:15:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df17faf3e69702da338bfc129c8313d532121156f900de2011a63dc3ab0984d1`  
		Last Modified: Thu, 17 Oct 2024 07:15:47 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca8883f7e11d556d6503a292573821f2d049d4c15d1b8d89ea42045c6310053`  
		Last Modified: Thu, 17 Oct 2024 07:15:50 GMT  
		Size: 105.5 MB (105542473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedb8725632034c12498de61abf2ee80a95df3ad6a1efdf59fa954b35644c67b`  
		Last Modified: Thu, 17 Oct 2024 07:15:48 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1acd91fae951cd755366baa9631fed6bd235de2792e77b82777031cd22e5aa9`  
		Last Modified: Thu, 17 Oct 2024 07:15:48 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144d0f374285c786b0158d522dba00fe91eb4b2cfb4a8a554698b62b20b20bcc`  
		Last Modified: Thu, 17 Oct 2024 07:15:48 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2e075f60dc240024efaf251cfa4481efc677a6a6e64b04cba9109c2e63575b`  
		Last Modified: Thu, 17 Oct 2024 07:15:49 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16f323ed079fae475339f4ea1f46ae546a6577cf958db659d59227f3f075408`  
		Last Modified: Thu, 17 Oct 2024 07:15:49 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:991a3f3ce04ba43987c0423efc2e3fe8b2f3b5729d4a72521bdd329c6df0b9cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5837534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fade373440980b9d981067817b2a506c0328c193849c69ebbd9852e3b070b7b`

```dockerfile
```

-	Layers:
	-	`sha256:f1cd501822b2c212ce9d538eda6f742c3f9f96b67ddadfdd67d317e703dfaa0f`  
		Last Modified: Thu, 17 Oct 2024 07:15:46 GMT  
		Size: 5.8 MB (5782222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1568e0141090eed95b716a8f2491f0ad24745b76111ac6ebd512072b26fd515f`  
		Last Modified: Thu, 17 Oct 2024 07:15:45 GMT  
		Size: 55.3 KB (55312 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:f33b0e8b828311b8629cadcc9805aa977df1cf02232ac314d47d633fd18c32a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (141983253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fca5d15b0e6eaddb7ac59d8c8061bf2156a6a71f48f2f350bfe42f208fc6423`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 26 Sep 2024 18:19:57 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Thu, 26 Sep 2024 18:19:57 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV LANG=en_US.utf8
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_MAJOR=17
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_VERSION=17.0-1.pgdg120+1
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Sep 2024 18:19:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 18:19:57 GMT
STOPSIGNAL SIGINT
# Thu, 26 Sep 2024 18:19:57 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Sep 2024 18:19:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d39d2d96734dd6c7fab8068ba08f92c7cbc1c98f5894e1c25c2265db8f74a5`  
		Last Modified: Fri, 27 Sep 2024 13:19:22 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a22c508463eb866d2934abcd7fae9234d1932914b2986b18d2d3758cab849b`  
		Last Modified: Fri, 27 Sep 2024 13:19:22 GMT  
		Size: 3.7 MB (3742490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f5dd4f0fd99c6a3012452faaca1c7f98c7ab9c5fb902ab68355721421dfcbf`  
		Last Modified: Fri, 27 Sep 2024 13:19:22 GMT  
		Size: 1.4 MB (1413563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0666a7837552389500ae71853be89df7cc34d20e8d5504a056f763f2855fcf80`  
		Last Modified: Fri, 27 Sep 2024 13:19:23 GMT  
		Size: 8.1 MB (8066267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f162e5e3b3b23a992b39df4c6ca227d40dfd24548618a1b27edaae3f7b2c1cc`  
		Last Modified: Fri, 27 Sep 2024 13:19:23 GMT  
		Size: 1.1 MB (1066954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e04d94c3aff724f37298d31af669139c832234fb26aebfd50d54ebef6be80a`  
		Last Modified: Fri, 27 Sep 2024 13:19:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d780f92ccafa30779296e018d5d6148e75f89526330fc3bdf6e40d930801edd`  
		Last Modified: Fri, 27 Sep 2024 13:19:23 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c63c5835bc3715f594c5a44af659d5714f66ddfd28e592d439ae1c4ce83a86a`  
		Last Modified: Fri, 27 Sep 2024 13:19:27 GMT  
		Size: 103.0 MB (102955276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e847e6e2a567690dcaab072a7ae3b98b1d87b85ef7559b8c713a918fafc035`  
		Last Modified: Fri, 27 Sep 2024 13:19:24 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbd4b3298c9641a632651f99a06cf0796b38c7711ff12d19f5a1eb6c017e632`  
		Last Modified: Fri, 27 Sep 2024 13:19:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09700a288d14458a9977b998beefa55dd1e5200198fc69088d0ff0fa1bc444e9`  
		Last Modified: Fri, 27 Sep 2024 13:19:24 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed448c2421c47918bb3c2d573919dab61270b8cb1232ba2fd23e5c32100ae2e8`  
		Last Modified: Fri, 27 Sep 2024 13:19:25 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d2d40fd2e85b2335b60ba8c3f63bfa498cdac77050fb1863766ce5b81a0512`  
		Last Modified: Fri, 27 Sep 2024 13:19:25 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:ea6de40db8e87d9f8dcde0a3103a1d6051fcd9944995df96e0b08099b1f4cbb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5837165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a237ba619f9d38ce2bd279446f7ab3a80a6de6b7d99580f09c30c6726ffd62`

```dockerfile
```

-	Layers:
	-	`sha256:85b2214dede9a32b090a5a302b3144b91886e0c7d8e1d17b805aaebd894b0053`  
		Last Modified: Fri, 27 Sep 2024 13:19:22 GMT  
		Size: 5.8 MB (5781891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f69eb603d51b5806d6594f9c978de8a564c3cd214a8c8bf0967e93fb4782eba4`  
		Last Modified: Fri, 27 Sep 2024 13:19:22 GMT  
		Size: 55.3 KB (55274 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:c4d5e961b288b3770775bb8851a07223b37874549013ef2a9e204b025af99041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152747519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae3e9e1bbb01a19912de007b6f26b306c4b6e26716c407dc155febf580a3154`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 26 Sep 2024 18:19:57 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Thu, 26 Sep 2024 18:19:57 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV LANG=en_US.utf8
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_MAJOR=17
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_VERSION=17.0-1.pgdg120+1
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Sep 2024 18:19:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 18:19:57 GMT
STOPSIGNAL SIGINT
# Thu, 26 Sep 2024 18:19:57 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Sep 2024 18:19:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c88e7faf79a34dd0af94058994e066483fb95ac60c57004716687e64f9bed5`  
		Last Modified: Fri, 27 Sep 2024 19:04:17 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86552d6a2e14fbce88d8ffa08a7f7e06dd4c6d7f208b84997c96c0f91053cba5`  
		Last Modified: Fri, 27 Sep 2024 19:04:18 GMT  
		Size: 4.5 MB (4499154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a986120aadb711cc1e9e8fbd5f2f62c7b123e0c329d6c1812be7bc38d03479b2`  
		Last Modified: Fri, 27 Sep 2024 19:04:18 GMT  
		Size: 1.4 MB (1378717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f6f593e3897cc85ba643ed6309995123ad8701a994700d1a796bb9ab0a1200`  
		Last Modified: Fri, 27 Sep 2024 19:04:18 GMT  
		Size: 8.1 MB (8066349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76441873964fa4a8d07dd408edfe47b022e2506a9fdabd6467f71cce1bd6c96a`  
		Last Modified: Fri, 27 Sep 2024 19:04:19 GMT  
		Size: 1.1 MB (1108704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00daffc086af223cc3083937b64cb98e4f5dbaae60aca84f869b695d9be65b4`  
		Last Modified: Fri, 27 Sep 2024 19:04:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e872bee6899bad3fe1acbb7e580e8381aa1f6a99b1e8d7b427011fe3beb076a`  
		Last Modified: Fri, 27 Sep 2024 19:04:19 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92476ada8688f68b5e6acda135cc468258dcf23fce7e8ce5af8331f8c0502974`  
		Last Modified: Fri, 27 Sep 2024 19:04:23 GMT  
		Size: 108.5 MB (108517678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4a94075068264e1e978e869241ba248fdb46abb63679fc2b438890ceea05a1`  
		Last Modified: Fri, 27 Sep 2024 19:04:20 GMT  
		Size: 10.2 KB (10228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8c275e6b2982bdd7d790a575f8737b2b35cd15e1ba871a4b5ef765b533ab33`  
		Last Modified: Fri, 27 Sep 2024 19:04:20 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dc23fd2bd63e1c80b0af9017d0f44264274b9b64a426f0157f194686ff5219`  
		Last Modified: Fri, 27 Sep 2024 19:04:20 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c30b8058ffcf5d6da54f63d5c6fa67e798fa23d17cdb346029767080bf2a4d6`  
		Last Modified: Fri, 27 Sep 2024 19:04:21 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bfb4ee2a1ce9685683b9f05739aadbb812ff27c36126497eb3c6bc49dce48b`  
		Last Modified: Fri, 27 Sep 2024 19:04:21 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:bb2e01ac3c9c4f15d6c14b16a6e454c701e601f485764f6b9f650a17da34897d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5826552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485874c92fa3e2d620959aa33b3a03882da8a97137a9dc18eea8cf2bf2316bdc`

```dockerfile
```

-	Layers:
	-	`sha256:421bd38413e546b52ea7b63f8d6355e01a76b6a380e86635ae29c98772690dee`  
		Last Modified: Fri, 27 Sep 2024 19:04:18 GMT  
		Size: 5.8 MB (5771174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:459f0eeac4c7e64551a04cfcf2859a9b1e9efc5774fabdbf0ecf580d9aa7f4d1`  
		Last Modified: Fri, 27 Sep 2024 19:04:17 GMT  
		Size: 55.4 KB (55378 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:165d029dd9c2c1d831c3ba75bec270562e6f483224164e4eef6ca98cb6de9a5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162744433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d60af421284ef664e9253cce0a560885ba034ca7dcbb72ebfb9e3b446b0ad01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 26 Sep 2024 18:19:57 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Thu, 26 Sep 2024 18:19:57 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV LANG=en_US.utf8
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_MAJOR=17
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_VERSION=17.0-1.pgdg120+1
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Sep 2024 18:19:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 18:19:57 GMT
STOPSIGNAL SIGINT
# Thu, 26 Sep 2024 18:19:57 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Sep 2024 18:19:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0869cfc7c0ec79ce921af206c79b5fb1a92d1838593ee7218c426d22fc567a15`  
		Last Modified: Thu, 17 Oct 2024 01:38:29 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08af525bdfb5c505148dc6ad9a088dcef3df3f344b96a8cd7119681a3e4418a7`  
		Last Modified: Thu, 17 Oct 2024 01:38:29 GMT  
		Size: 5.0 MB (4965107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b4b55ab89ad92c313dc88b6305564a99ed2860cd10f179777ed3aeb6276707`  
		Last Modified: Thu, 17 Oct 2024 01:38:29 GMT  
		Size: 1.4 MB (1422125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87085c16b8ba2ff82ee4b7f2128d0ab8751e08e6cf3ff0e87303bd93e1660af3`  
		Last Modified: Thu, 17 Oct 2024 01:38:30 GMT  
		Size: 8.1 MB (8066274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522999d8efb817fe8bb46603f8e9f6fb39c05ecafdbc1900d08031cfd9d2672d`  
		Last Modified: Thu, 17 Oct 2024 01:38:30 GMT  
		Size: 1.1 MB (1137136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7c727d75965d6b3d6f1c755eb3ba366a3b53eed2776c42dfc174fca29de14c`  
		Last Modified: Thu, 17 Oct 2024 01:38:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09914ac7e7ee8cc38f60b1b8a1e4b44a3747f0f36725c69e7d40399e03f947a2`  
		Last Modified: Thu, 17 Oct 2024 01:38:30 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e45e86641dc1eac693fd27a3ebc493275d6b3026c9feaa24ce6c43e9483a71`  
		Last Modified: Thu, 17 Oct 2024 01:38:34 GMT  
		Size: 117.0 MB (116988966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8fcfaf273d54659cdaf2570e9c4cbf6e84eef7a7dafc90fde4a8260d5836f5`  
		Last Modified: Thu, 17 Oct 2024 01:38:31 GMT  
		Size: 10.2 KB (10239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e92ec86494a57081afaefe57582218f943a37228c18a3223dbf6b45e0e0602`  
		Last Modified: Thu, 17 Oct 2024 01:38:31 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccff688b72b7ae89abf76d3163ca648fa77c1a74e36e629f23f64c85d515084`  
		Last Modified: Thu, 17 Oct 2024 01:38:29 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db705b2b843895c34d71d9fad766415f691d06b4fff90a1ef3f23877f5b7f84`  
		Last Modified: Thu, 17 Oct 2024 01:38:31 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca2f0b90220139576486324ae6a83d1b3407cbd6f244b2b1cbfadb0d500aa98`  
		Last Modified: Thu, 17 Oct 2024 01:38:32 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:f65636c06ff39768cd67657bd8cbd219917415302c31c5ea6c158c86b6b002d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5835270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a0933830560d2066354e8669639cf36da47a4f540587a7354015767b9870df5`

```dockerfile
```

-	Layers:
	-	`sha256:4d112b06ee791cf5713c2fe49ea3efbbd426e2b0dd5fbfa612a9bf1cd2eefd76`  
		Last Modified: Thu, 17 Oct 2024 01:38:29 GMT  
		Size: 5.8 MB (5780249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ec10a9be4f19e8e0624a2c73d5f8bb2b60f56018b7cbb14f9f271781cef5387`  
		Last Modified: Thu, 17 Oct 2024 01:38:29 GMT  
		Size: 55.0 KB (55021 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:bb92c28d676b96ca1dbfa71caf4557de822c92928bc3cb9860607704d2baa6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (149983129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0add7eed6a88cc7875be1fb665c22f7e166897bb8111969da40a84fdbea5105`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 26 Sep 2024 18:19:57 GMT
ADD file:673970f358f62b6b095139e9647b41b9af839d4e01f7698755b040f471ff80b2 in / 
# Thu, 26 Sep 2024 18:19:57 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV LANG=en_US.utf8
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_MAJOR=17
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_VERSION=17.0-1.pgdg120+1
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Sep 2024 18:19:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 18:19:57 GMT
STOPSIGNAL SIGINT
# Thu, 26 Sep 2024 18:19:57 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Sep 2024 18:19:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:75358c79454e0fed44aa25dd323536443b4a1230fc432aa226620e470d72cf5f`  
		Last Modified: Fri, 27 Sep 2024 09:11:36 GMT  
		Size: 29.1 MB (29124858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af314cba9cb12e609d6f5e7e176fd1effba6f3378e51fcc24ee9659d84b3f295`  
		Last Modified: Sat, 28 Sep 2024 05:10:44 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21060f3e92dec884650f41e7e4e842b9df88d05e99485d146ea912652c492750`  
		Last Modified: Sat, 28 Sep 2024 05:10:46 GMT  
		Size: 4.5 MB (4475088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0eb518019f221edbdda47fb6b99a27dd048ba63a0c25b471237ee7f9d43a8c4`  
		Last Modified: Sat, 28 Sep 2024 05:10:45 GMT  
		Size: 1.3 MB (1333787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c02e504a5e7f5c5f1111ff9378296b1d069ce86909bf813ef0f94ab896cde83`  
		Last Modified: Sat, 28 Sep 2024 05:10:46 GMT  
		Size: 8.1 MB (8066541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867a2bbc7c3ae5d498f28416ae2860f1f4bf26780b58f517b7ef754a05d11348`  
		Last Modified: Sat, 28 Sep 2024 05:10:46 GMT  
		Size: 1.2 MB (1182634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06717b5d1895893f9dda00250577258ffc2015f94120a03d364ab453fd8e8eb8`  
		Last Modified: Sat, 28 Sep 2024 05:10:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ef5a261d5e09fdd65265fc5d8e3972550396a7bab51431bf87e09c42499e8b`  
		Last Modified: Sat, 28 Sep 2024 05:10:47 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47af68cccf2bde0d13ec51946142d96a67f21ded914c4e7708e1ced302feb98`  
		Last Modified: Sat, 28 Sep 2024 05:10:57 GMT  
		Size: 105.8 MB (105779654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56732aca44911cf1118b55ff8e51969383cc2adcbb2d03713c35342a05fa85a5`  
		Last Modified: Sat, 28 Sep 2024 05:10:47 GMT  
		Size: 10.2 KB (10241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1da0a527fef949c9fc5bffbcbee35e097301ee185ca11914c235ade84b6b13`  
		Last Modified: Sat, 28 Sep 2024 05:10:47 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a33352bed12da2682603769d9be75ac95f2b868b1b3f02d1e4c49dd99e289f1`  
		Last Modified: Sat, 28 Sep 2024 05:10:48 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c3bf20cca53df18a783c12a2882eb53ac2c06d22dc20e6622b2609c0149aea8`  
		Last Modified: Sat, 28 Sep 2024 05:10:48 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f274fd616bbd00de030838e4831979b17fda6c1f20536396f1dbef5d25ca96e0`  
		Last Modified: Sat, 28 Sep 2024 05:10:48 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:c8fe51179c1aab4ac50c2a4cc2bc4ec1c31e694620fbd876a591abf1f044248b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 KB (54934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd2f5b7930f9052ef77242584a7e03209c7f1c98ce230191d876d5025c6c048`

```dockerfile
```

-	Layers:
	-	`sha256:9be4e39aeccee46f712060a1bef48856ddd13891e990dea1119a062cf29b33f3`  
		Last Modified: Sat, 28 Sep 2024 05:10:45 GMT  
		Size: 54.9 KB (54934 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:995dea255b437c297ec2de89638dfd198576c3f7b5db60d25bd39b3813420a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166809174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc3cdee2c5d7d4138ef13780546f3cb4dfa629c8533e385bcc78d7e55a24bb5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 26 Sep 2024 18:19:57 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Thu, 26 Sep 2024 18:19:57 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV LANG=en_US.utf8
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_MAJOR=17
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_VERSION=17.0-1.pgdg120+1
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Sep 2024 18:19:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 18:19:57 GMT
STOPSIGNAL SIGINT
# Thu, 26 Sep 2024 18:19:57 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Sep 2024 18:19:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc57d97564b13bbf1a63a90ff8d0c39edf6bb4d7a18ec5af020246575c794170`  
		Last Modified: Thu, 17 Oct 2024 11:11:39 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c4ef2f7d34915d8f62fe809643174dd7ad490299d1197a408731669ca495f9`  
		Last Modified: Thu, 17 Oct 2024 11:11:40 GMT  
		Size: 5.4 MB (5368187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6473e3914c9bc16e0a4aef0617ab544835635d8c85cc3b26ee05efde2dbfea`  
		Last Modified: Thu, 17 Oct 2024 11:11:40 GMT  
		Size: 1.4 MB (1368565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3978046a25d39ab276194b63766ecc0de9306983c6fbd2dd6cd0b3f653004bba`  
		Last Modified: Thu, 17 Oct 2024 11:11:40 GMT  
		Size: 8.1 MB (8066318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa3b39a2d09d3b13f0746af494283525c9d9f5f264a77dd01d6c11208e27ab0`  
		Last Modified: Thu, 17 Oct 2024 11:11:41 GMT  
		Size: 1.3 MB (1283468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425aeaefc1ad865c7350c245ab8ab8e1f7394b1fbdaad36fd46886fc1d09e9fa`  
		Last Modified: Thu, 17 Oct 2024 11:11:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b537e6fed6497d1c5300b56f7e6860405902a27b242c87ea6e31e02378a2a3`  
		Last Modified: Thu, 17 Oct 2024 11:11:41 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0028897e69f9be14bbe64903b8c0bc4a40a2550e2a5961128a5e787ea02d543a`  
		Last Modified: Thu, 17 Oct 2024 11:11:44 GMT  
		Size: 117.6 MB (117579886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ede838e1fef16963195577bfe1c5c8797494695adcf57a789f48bdc846bda2e`  
		Last Modified: Thu, 17 Oct 2024 11:11:42 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b4b5a55df29e7c663fbbb6585eadb99fdee52f743cc315e5bf2f0a97000ebe`  
		Last Modified: Thu, 17 Oct 2024 11:11:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7d0893c6766d6b9397cac67a6c25ebc10bd05262d60bd487b2d8f00f558b98`  
		Last Modified: Thu, 17 Oct 2024 11:11:42 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f87fa66654a8bb26c9be33c60b29c945bb73dd8756058c8cd6386f362bff1ff`  
		Last Modified: Thu, 17 Oct 2024 11:11:43 GMT  
		Size: 5.4 KB (5413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7630ebf61eaf4fa70c9f976503399e02334054206f5e9565acdb94867332d4`  
		Last Modified: Thu, 17 Oct 2024 11:11:43 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:4259b52048a90cf0f6f66c7427e372d56a85a6726e574ba7bf71781f0f98df52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5827205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f42173c8ea47209053db570626cffbb5b1018ee369602f8e30c8e560e87ab765`

```dockerfile
```

-	Layers:
	-	`sha256:43fcf12aa026db59333f99b132c4c49661fa8038e75b161bf3b1782b44bf3303`  
		Last Modified: Thu, 17 Oct 2024 11:11:40 GMT  
		Size: 5.8 MB (5772050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d9d235d53e3857a335fab938a5ba69b38864e1a5b03028039cc7d0b1f1d1afe`  
		Last Modified: Thu, 17 Oct 2024 11:11:39 GMT  
		Size: 55.2 KB (55155 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:fb3b87f3789da2de237f2ad29a4f41d216ca80d74657f6b3a0cf43269ed7befb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.1 MB (160105728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3330e61c9e191f8a13aa57ed81985ee5674d930c7510004fac7cb10001a993c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 26 Sep 2024 18:19:57 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Thu, 26 Sep 2024 18:19:57 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV LANG=en_US.utf8
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_MAJOR=17
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PG_VERSION=17.0-1.pgdg120+1
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Sep 2024 18:19:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Sep 2024 18:19:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Sep 2024 18:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 18:19:57 GMT
STOPSIGNAL SIGINT
# Thu, 26 Sep 2024 18:19:57 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Sep 2024 18:19:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfaa36cfff6431c27e7935d616b6eaff6f513d497e83cebc6c0da04dc137c5a7`  
		Last Modified: Thu, 17 Oct 2024 16:02:27 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b577b666ea5a6dabbd2cde468e354956563b93ff50a86cc5a9ed1640fbd197e`  
		Last Modified: Thu, 17 Oct 2024 16:02:27 GMT  
		Size: 4.4 MB (4391094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a0d22fb1dfa0817b6e1fdfb7dab455c2bf35e9d891ba4b3590c70cbdb90cefc`  
		Last Modified: Thu, 17 Oct 2024 16:02:27 GMT  
		Size: 1.4 MB (1412722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7161abec880a4814c780af4b1ca00609d84db87d77284004a682002d03da9afc`  
		Last Modified: Thu, 17 Oct 2024 16:02:28 GMT  
		Size: 8.1 MB (8120484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a34a3d18d09ee17a76120a8f29bb6935c3430499ecc674a62f31e1d9160d4fd`  
		Last Modified: Thu, 17 Oct 2024 16:02:28 GMT  
		Size: 1.1 MB (1096778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e149db88224269c8cb5fec9f794b88f3e086a3742ce3dbe7f155d23625472b86`  
		Last Modified: Thu, 17 Oct 2024 16:02:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d3fe3a6b6f8e743519a04efddc5d478bca55f1ecc6c5f711f37d0f1ec235f5`  
		Last Modified: Thu, 17 Oct 2024 16:02:28 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13ea91c6702d70110c7085d80e794d6067b1195f9f726fb257442a9074ea6b6`  
		Last Modified: Thu, 17 Oct 2024 16:02:31 GMT  
		Size: 117.6 MB (117574008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfb53d124ff1efd64ce36e8d8550750d31b372a2cc14c807992fe7a78323726`  
		Last Modified: Thu, 17 Oct 2024 16:02:29 GMT  
		Size: 10.2 KB (10233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28694bf8c014662981a9b77d5eafd1f3f1724da636878ef5ba2ef50425b200cb`  
		Last Modified: Thu, 17 Oct 2024 16:02:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7bc341081e0ec8690b562cfb4a226e68594c5da1834f8fba72873b3b6736b0`  
		Last Modified: Thu, 17 Oct 2024 16:02:29 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41fb7d6b334204f1fdd61cdcadf3f013f4f03849c1a6f192f82b430eae9fa35a`  
		Last Modified: Thu, 17 Oct 2024 16:02:30 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55bcc216e2dd756dd2234d4bba43851f44e7e1c6a8e4c0ad2f001e396c3c8e5`  
		Last Modified: Thu, 17 Oct 2024 16:02:30 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:79cdea61dfcd567ac11367fe4c932c2ea68020e0eda4c54daf14e9219b5bf498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5819286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b6ad0a45d0b3690ed8e7993ee25af483f0e3f230ab1fd24900458fc5d1cf9aa`

```dockerfile
```

-	Layers:
	-	`sha256:d58ae866e2b86bc40953f17a6611f716f30c92afb06ed959a4d265b41cd50f33`  
		Last Modified: Thu, 17 Oct 2024 16:02:28 GMT  
		Size: 5.8 MB (5764203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0692a240425d5d2a04c4a8e9ea8b38661f73219bb59e6ed5e4c654310824adb`  
		Last Modified: Thu, 17 Oct 2024 16:02:28 GMT  
		Size: 55.1 KB (55083 bytes)  
		MIME: application/vnd.in-toto+json
