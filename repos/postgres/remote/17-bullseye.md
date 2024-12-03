## `postgres:17-bullseye`

```console
$ docker pull postgres@sha256:c2a477d239bf166c77c01713bc07befca760a9c77e81566d8f6f8356604648d0
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
$ docker pull postgres@sha256:39d86bccdc55650f27806b3bdca3b8eaa02b2e731258172ee72bbd12738ac2d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.4 MB (150370572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2630bbcd572294cafaefd16f3c9843f28a7cc1b32a69b3c5d49d434085ffb73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 21 Nov 2024 20:16:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
ENV PG_MAJOR=17
# Thu, 21 Nov 2024 20:16:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 21 Nov 2024 20:16:44 GMT
ENV PG_VERSION=17.2-1.pgdg110+1
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:16:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:16:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:16:44 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:16:44 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:16:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ff61fca8ac889fe77d65c6ed2bec9bcea8505bf6d547154bfbe61bfddf4a66`  
		Last Modified: Tue, 03 Dec 2024 02:27:28 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38f3c7dfafcad9f46947141bf2e45be47a98720098d0f1b80d6645b41517201`  
		Last Modified: Tue, 03 Dec 2024 02:27:29 GMT  
		Size: 4.3 MB (4308184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895fbad562081ad56ff98d4c2c930331b68f05f379a8051f2b55c0ed3a15faea`  
		Last Modified: Tue, 03 Dec 2024 02:27:29 GMT  
		Size: 1.5 MB (1472219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20349e765a80b8b3dc683f37327fe9e2f47063e661171e5095afcda3b9dfe9e0`  
		Last Modified: Tue, 03 Dec 2024 02:27:30 GMT  
		Size: 8.0 MB (8044524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d10937fb39211afe16acd6f5db6a5c14ac8818bd6e0e985a7f759114b86801`  
		Last Modified: Tue, 03 Dec 2024 02:27:30 GMT  
		Size: 1.0 MB (1038337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3d138399040b2fd8f12b6bc4fef0984501f8c25ba41a4016615e25b50fe78d`  
		Last Modified: Tue, 03 Dec 2024 02:27:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150ea94b3a834453835223ce9d4125be7c2746f1f03f9f8db0ff818027e206d7`  
		Last Modified: Tue, 03 Dec 2024 02:27:30 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90f29aea35949fce848e1a5be8d1b2fa3e32470de9b7e28b66280b56ea44acb`  
		Last Modified: Tue, 03 Dec 2024 02:27:34 GMT  
		Size: 105.2 MB (105233586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09aa25aff9b75b87360946ccb03f071597ef77e6045d5ab21121232fba8e7c9`  
		Last Modified: Tue, 03 Dec 2024 02:27:31 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a4c03fb06453ce4972c9ddcb3ca00d2e05358cef4edb0890055c9ef38429580`  
		Last Modified: Tue, 03 Dec 2024 02:27:31 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922ff8346899610e4a60796020f46201d07603f02e78d7a2682eee16ce35ecda`  
		Last Modified: Tue, 03 Dec 2024 02:27:31 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54dee37b05f45603c1a7a0db2886df5cd93033e667b323aa97d924233d14ec5c`  
		Last Modified: Tue, 03 Dec 2024 02:27:32 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c001797204e2283df3d59bc8031b6784746e0a1690d4129e47b258b9e6bda3d9`  
		Last Modified: Tue, 03 Dec 2024 02:27:32 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:902fa6deac8b5e3ae2da25ba1e2c8d856fde75edeb4bb062747b4ec665a1b613
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6095771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3626db84a1c526a6a400eb93e18a1cbf028c3f9680ade7293dfa882226c1985c`

```dockerfile
```

-	Layers:
	-	`sha256:08b6569ce298ec4345cec1f9cb99779e0094ba4fc52168906adbd623c2337736`  
		Last Modified: Tue, 03 Dec 2024 02:27:29 GMT  
		Size: 6.0 MB (6041474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34b1376e513c5ef4ee52f3bfebc35fcd80e3dd74c2d277da13bf9429be75c578`  
		Last Modified: Tue, 03 Dec 2024 02:27:28 GMT  
		Size: 54.3 KB (54297 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:468599b0b2180f358e7a986a0a930cb2df7d5ff87e60e4773ca34e236c9e96bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138581145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a0327ab2a088e80b4f4d5cf0fc3ed91c97deb7e46b6b83bb4d71b7de2cb260`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 21 Nov 2024 20:16:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1733097600'
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
ENV PG_MAJOR=17
# Thu, 21 Nov 2024 20:16:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 21 Nov 2024 20:16:44 GMT
ENV PG_VERSION=17.2-1.pgdg110+1
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:16:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:16:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:16:44 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:16:44 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:16:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:79ae44024aa8e358b5fbaad284a41a7c359d47ad28af854839c0e44435b875ba`  
		Last Modified: Tue, 03 Dec 2024 01:28:54 GMT  
		Size: 25.5 MB (25533944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56650716f75efcee4d51ef4e5ad69dd2a7915bad0bb4a2483477bead6b07149`  
		Last Modified: Tue, 03 Dec 2024 04:59:04 GMT  
		Size: 1.7 KB (1680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2236e2358d1ce4ce902ddbf6f1d63cca19745e08b1dffe3fe19941d13ecf6219`  
		Last Modified: Tue, 03 Dec 2024 04:59:04 GMT  
		Size: 3.6 MB (3601748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af3987bbb0adc6674d4b46bd515b4b2b69e678c1a92a4e77a5b0e34a2c961c4`  
		Last Modified: Tue, 03 Dec 2024 04:59:04 GMT  
		Size: 1.4 MB (1439267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ccbc0c07776fca1a6b8cf3a8f8e02c5a811cd449cea29a7fa8167deefd8be5`  
		Last Modified: Tue, 03 Dec 2024 04:59:04 GMT  
		Size: 8.0 MB (8044499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eff024c17bac452525764c081f20b6bd0b46b454a933f93f52d8ac790e40d8f`  
		Last Modified: Tue, 03 Dec 2024 04:59:05 GMT  
		Size: 908.6 KB (908649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60707cfdc39f445ad524c709e000d7ca380050cda2951a446e4998939e8ccf1`  
		Last Modified: Tue, 03 Dec 2024 04:59:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49d413f92f0c6e1525386da639209dfbeabf7a36f06c6fa9bb9ab28eb8c6b8d`  
		Last Modified: Tue, 03 Dec 2024 04:59:05 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0711f09110f846de16c48e65ba7388e7498464fa39774704499241ef1023efd`  
		Last Modified: Tue, 03 Dec 2024 04:59:08 GMT  
		Size: 99.0 MB (99031964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6ec8b5bc5a8886709019fb77d2dce9151c4aba9713015f561b0aebf0a58525`  
		Last Modified: Tue, 03 Dec 2024 04:59:06 GMT  
		Size: 10.2 KB (10237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763b36336cc3284633e222ff3773cc4af4821da71a5a535bccd5b1a8265e9826`  
		Last Modified: Tue, 03 Dec 2024 04:59:06 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3de50a59da853e49a33f4816d4e40d522c2d1b0bffd04e8399b7fb814128de`  
		Last Modified: Tue, 03 Dec 2024 04:59:06 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76428c413f184bee48c82a58b21029d6d94020e4c4fbddfa550e5275fc84223`  
		Last Modified: Tue, 03 Dec 2024 04:59:07 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f58206804051455feb0062694b4b05075e564941f7e2330891a914063ae7cb4`  
		Last Modified: Tue, 03 Dec 2024 04:59:07 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:a7af9465bd1f061870aef4026e245f2299abfd5a353f828d98495f2f5eec9a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6113108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cdb5e75880cadd8240155fe009ef2042a33383046e09aef79bd640be95bdd54`

```dockerfile
```

-	Layers:
	-	`sha256:69bbe5e928cc6ccb3f1d53702490d845e297d51ddc25447209ac4ef2b2e36687`  
		Last Modified: Tue, 03 Dec 2024 04:59:04 GMT  
		Size: 6.1 MB (6058615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7178b576665f0b3ebcf16e7b260de2c3ca2212e07fa410981bc8412d25ba9f1`  
		Last Modified: Tue, 03 Dec 2024 04:59:04 GMT  
		Size: 54.5 KB (54493 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:1a3de3d638ff28e0876232a9db31e5747cd5b6c53a65e3890aa713ceb763e31c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147365747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da6404f4ecef981285a8acc1590f20b638965665fc5c2a80f143d2cdd7d2adad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 21 Nov 2024 20:16:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
ENV PG_MAJOR=17
# Thu, 21 Nov 2024 20:16:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 21 Nov 2024 20:16:44 GMT
ENV PG_VERSION=17.2-1.pgdg110+1
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:16:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:16:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:16:44 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:16:44 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:16:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8b80562b98380f4d25ff0e1ec437b36e11db387f2dea5dce6a19a4837bf1ab`  
		Last Modified: Tue, 03 Dec 2024 04:53:32 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41eb784e6609ceacd3cf1cde63437ff62c716a86087589a3b7c299e8ea7f77fc`  
		Last Modified: Tue, 03 Dec 2024 04:53:33 GMT  
		Size: 4.3 MB (4312809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2153d0d5e5df27b45cb7b5ccb871564967fa58f7de67908e6fc2e3a060d2cedc`  
		Last Modified: Tue, 03 Dec 2024 04:53:33 GMT  
		Size: 1.4 MB (1404093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83d68bdff67a2c31fef8a93a01a8607cd4826cdd4f7c18b6586b8b8b2e6f9a0`  
		Last Modified: Tue, 03 Dec 2024 04:53:33 GMT  
		Size: 8.0 MB (8044485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d616d99ca3e54d6bf8a2544191d8797a5c2126f8cd2c15c4cef7c456590d36`  
		Last Modified: Tue, 03 Dec 2024 04:53:34 GMT  
		Size: 1.0 MB (1026573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9e28c761f3931f06ea9a80edce984b81e122f8049d96b9907ed38eaf14fa13`  
		Last Modified: Tue, 03 Dec 2024 04:53:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4e526653713b8164164922c64bc2ac8ac74040c69985865622e19158539e67`  
		Last Modified: Tue, 03 Dec 2024 04:53:34 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e6ca585147654b5774b8c75aa7e48b253b7aacf0eb4acc86df34f226527ca0`  
		Last Modified: Tue, 03 Dec 2024 04:53:37 GMT  
		Size: 103.8 MB (103811783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82cf447a1d220ad9212df8e6e9dde2e06956ece86e9d8c5fa566b0b839aa361`  
		Last Modified: Tue, 03 Dec 2024 04:53:35 GMT  
		Size: 10.2 KB (10241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a000c6dd79418d781221c3336041531ddc7793631514ce97604394869e71b617`  
		Last Modified: Tue, 03 Dec 2024 04:53:35 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be01134b936b48c3529d87b659452b38f60f4c1d4b58499cbb60d10a5750fe85`  
		Last Modified: Tue, 03 Dec 2024 04:53:35 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ce7ec8d7d2194e3865ca73094a873caf89f4cdbe9a66f7444d073d50723647`  
		Last Modified: Tue, 03 Dec 2024 04:53:35 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:399133913ca4577568bd8ce4fcf725c48b572754042a0e5e7acd7878e2d95ce3`  
		Last Modified: Tue, 03 Dec 2024 04:53:35 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:82e6403ca5a4593a3ffe7ea5422f084d20ba2e5a4baeed4bedb7b10f27d97f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6102334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ca047c69f5b403a9b0145180d0a22e515a722bf1e6dccb64ef74cab6a6b60f`

```dockerfile
```

-	Layers:
	-	`sha256:12df35733e2dfe377bb2200037addae9e932b713e2b2d99763e021b5877f1c03`  
		Last Modified: Tue, 03 Dec 2024 04:53:33 GMT  
		Size: 6.0 MB (6047780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3e230557471bffbd6fb759ca1b042ae593a965391ef1483cccb6057eb7c0809`  
		Last Modified: Tue, 03 Dec 2024 04:53:32 GMT  
		Size: 54.6 KB (54554 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:739f293b9ef883204096a6a46ad6c83c5079f37277fe8a4a7475766c4d821add
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.6 MB (158615990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0583587f6d881ade27548700ddd3d6e4d6f4326ebd8932d7522d51b06412a42c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 21 Nov 2024 20:16:44 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1733097600'
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
ENV PG_MAJOR=17
# Thu, 21 Nov 2024 20:16:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 21 Nov 2024 20:16:44 GMT
ENV PG_VERSION=17.2-1.pgdg110+1
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:16:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:16:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:16:44 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:16:44 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:16:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c321449a7780a0f6febb0c1425384629e366cd30dd2d0d9cab29fc6e33f6955c`  
		Last Modified: Tue, 03 Dec 2024 01:27:12 GMT  
		Size: 31.2 MB (31179058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60eb7448e0d8b0a22171eb828509118a75204ad279c63113bdb85184c9c8374f`  
		Last Modified: Tue, 03 Dec 2024 02:38:45 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78f2ba66d5bb36798175a127b31d1f82025c8efa91354a15cadd570f85417ce`  
		Last Modified: Tue, 03 Dec 2024 02:38:45 GMT  
		Size: 4.7 MB (4719690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4f63badcef844b310a7f484a5c658110bd3b1e02084e6e8bb81b3786512378`  
		Last Modified: Tue, 03 Dec 2024 02:38:45 GMT  
		Size: 1.4 MB (1447776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82dd13ecd8ca87da9069df41f9d8dd246ccc2f8b86e9819c7c18f252e735b0a7`  
		Last Modified: Tue, 03 Dec 2024 02:38:46 GMT  
		Size: 8.0 MB (8044246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91367dd3cde196df4b2c4f3a2d3cb67e605933d574c4e5d310c64b2e1f715d32`  
		Last Modified: Tue, 03 Dec 2024 02:38:46 GMT  
		Size: 1.0 MB (1028937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d4d665c0bf978ce7ad6d5e324e3a179bee6c57e0846d65a9e973c077cdd92b`  
		Last Modified: Tue, 03 Dec 2024 02:38:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9feef4655f345e3585b639dc7e73a3a273c32405bb7b15bd92b1ac5b82edf4e`  
		Last Modified: Tue, 03 Dec 2024 02:38:46 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02491880f2c779909f9bad685a2a741865351611d4bd2854e74bc365a0ac9fea`  
		Last Modified: Tue, 03 Dec 2024 02:38:49 GMT  
		Size: 112.2 MB (112175209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09295bf8b2c91c651d4229dfb064c06d90dce9077ce2fb024d1d66172b1f5070`  
		Last Modified: Tue, 03 Dec 2024 02:38:47 GMT  
		Size: 10.2 KB (10239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55451ccca91da3ecf50bff0e56972419a1bfbd7599337c9d8025d39363d0684e`  
		Last Modified: Tue, 03 Dec 2024 02:37:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33c1b1587952adcce5f182433b019bd88cf64da41c33fb6787f45f9dd4835a2`  
		Last Modified: Tue, 03 Dec 2024 02:38:47 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeec6c8bd7fc5bb90265e29764d073629d183c42072432a351b3223f68bed7a8`  
		Last Modified: Tue, 03 Dec 2024 02:38:47 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e816f0a6f347e7e3758884b3060c908894543a80ef6850763360cea6a1194f8a`  
		Last Modified: Tue, 03 Dec 2024 02:38:48 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:a01ca0a8443a0206e89136989bf1bb98fbb41fbb10ee70ca9345922cb8c47cab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6110627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:521040253d90a2c2e960a632f5caa47f1fd62a73ae7eda18a13bcccf8f4e289f`

```dockerfile
```

-	Layers:
	-	`sha256:640dfb0b52413b325dc99db5d3984f5b3be27e355a9166a17b348a553c92dcbb`  
		Last Modified: Tue, 03 Dec 2024 02:38:45 GMT  
		Size: 6.1 MB (6056379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:049e0229da68ee6671f3fa6676d807fa8ceeb82c3545c971d40db71a010e9583`  
		Last Modified: Tue, 03 Dec 2024 02:38:45 GMT  
		Size: 54.2 KB (54248 bytes)  
		MIME: application/vnd.in-toto+json
