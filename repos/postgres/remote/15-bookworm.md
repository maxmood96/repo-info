## `postgres:15-bookworm`

```console
$ docker pull postgres@sha256:491aea6e557dea673887a9008f872225b667d0f54223a10e085059a239459ccb
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

### `postgres:15-bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:46fb9e4c3ac90f6cd09c0ed5dc12c6a2eff608ca302bf1bf82dc9569ffb38e33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151307421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2258b53bc9c69c8f74f08efb76e559d2b11a5ed9410ef67ed81557efacc4541`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:06:32 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 08 Aug 2024 17:06:32 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_MAJOR=15
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_VERSION=15.8-1.pgdg120+1
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:06:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:06:32 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:06:32 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:06:32 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:06:32 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61eece249d74f45358f69dcbeb2bcf89a805e9059186cba7947c1119db8adbcd`  
		Last Modified: Thu, 17 Oct 2024 01:25:56 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b5694108bb093dd25fa9ac5400d344e3813b747c335ddd8c8480c264867971`  
		Last Modified: Thu, 17 Oct 2024 01:25:56 GMT  
		Size: 4.5 MB (4533670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058fb4f2d0d2991c9d426ba5d66cfa95572f6c266b02517f7c29898774018226`  
		Last Modified: Thu, 17 Oct 2024 01:25:56 GMT  
		Size: 1.4 MB (1446646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7371aaafb43b0f221eb5e0c4efc9cbb8e1ea30657ee70f0ab7e878daff51dbfa`  
		Last Modified: Thu, 17 Oct 2024 01:25:56 GMT  
		Size: 8.1 MB (8066297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09993ebd1f9b925499a548133b6bee0e38633bb6dbc609064ab47dea090181ff`  
		Last Modified: Thu, 17 Oct 2024 01:25:57 GMT  
		Size: 1.2 MB (1196027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e0872ca03da62ed9d89a3f86d2e603ad72bc699a578efcda655b8c07576756`  
		Last Modified: Thu, 17 Oct 2024 01:25:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a653ce7e67130b4aa7fbbcb4c0e31843babb938bd99a0c02994c94dd5e9cdb26`  
		Last Modified: Thu, 17 Oct 2024 01:25:57 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1c729ec064bf2dbae8774973b76a57eeda0a6f23ec44c91c709de19a1f6389`  
		Last Modified: Thu, 17 Oct 2024 01:25:59 GMT  
		Size: 106.9 MB (106918395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ad473ab07d5e8ce27b1aba6ab9d3458c68cc0867ff6c1f187fb1a0ab360c1a`  
		Last Modified: Thu, 17 Oct 2024 01:25:57 GMT  
		Size: 9.8 KB (9777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc6080182b99db1f28f7f8b9d6134f7137e471235aa8227556e997333ebb52b`  
		Last Modified: Thu, 17 Oct 2024 01:25:58 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3be4d9979519102722c1a3ff9aa428bee108e766ede4a142d556a7d35cec4b5`  
		Last Modified: Thu, 17 Oct 2024 01:25:58 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbb2ce63b4518f7bfe1a5aa4d6e7f06b90e0ad0ded29d8c90c8f98f5f18ac2a`  
		Last Modified: Thu, 17 Oct 2024 01:25:58 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d64aa43b4a0e96ca15e242555f3226683e4401e2bb80e9a7eca605368f48906`  
		Last Modified: Thu, 17 Oct 2024 01:25:58 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:a7ac5cd9acf8062332d6cdc2fe897f49aaef2b7f736e419a349c6f60fcb5090d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5739796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:235cac5c17241074dc3c608e2f3fec3f5d5aafdd066827912c5a76266d30ee5c`

```dockerfile
```

-	Layers:
	-	`sha256:240cd1827c843751028ccd102f0b51158cc88636db02b1abe18b74f1eaf4bb52`  
		Last Modified: Thu, 17 Oct 2024 01:25:56 GMT  
		Size: 5.7 MB (5685326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c08a47d5830a26c4a38ed938b481c4110d687a0512e881f8b1b7b015390a82aa`  
		Last Modified: Thu, 17 Oct 2024 01:25:56 GMT  
		Size: 54.5 KB (54470 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:6dddbae8cd93e7b3a8eb7fe9e4f197bbff46471acb7f9c5ae0e92bba1ad5bc63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143973307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0cee80c6a2de5f344f2d871e89b614ec5cb982e7af39b80e629d25c3ce55847`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:06:32 GMT
ADD file:c8ec8d65b2f61866a2c6085ed61e936733bc484abeeba1b91d12b9f6a97e456b in / 
# Thu, 08 Aug 2024 17:06:32 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_MAJOR=15
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_VERSION=15.8-1.pgdg120+1
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:06:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:06:32 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:06:32 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:06:32 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:06:32 GMT
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
	-	`sha256:b38d65a4f8f9d390729ded7490c5c07ea49f633a7153d072508308f48dd62cd5`  
		Last Modified: Thu, 17 Oct 2024 07:47:35 GMT  
		Size: 102.2 MB (102229885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a2b1e8f4f90afdc77af5b3ccb91a8da16d7f315adba425a74e4e6463e6ccb0`  
		Last Modified: Thu, 17 Oct 2024 07:47:32 GMT  
		Size: 9.8 KB (9783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9aae47f8f82b3004aa12e261906faafee70ad2120437223bc03535b4953f30`  
		Last Modified: Thu, 17 Oct 2024 07:47:32 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f14e13d73ff1ac8fda55526c82858700f8cd3393e79581f6608e187b131cbd`  
		Last Modified: Thu, 17 Oct 2024 07:47:32 GMT  
		Size: 165.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d254bc5ae00d09d65e02d54586d5502aedfc7fdbafe682d2fae8f64504720d`  
		Last Modified: Thu, 17 Oct 2024 07:47:33 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aad2b7a3491a4b864cb618ef51aa743c2aba6ea8b3f2be57dcf94ed8cbbd60a`  
		Last Modified: Thu, 17 Oct 2024 07:47:33 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:dadeb04250e4ca233cb42b30ba7ce020534ae89e10cd4901f2180cdc23f1fe60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5751574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6862e8d2fd6621ec42efd4f2286a2cca7a8c0fb02350047e3ae781636aa6c16`

```dockerfile
```

-	Layers:
	-	`sha256:9bca7d6d40f69e7d24eee98ec55a070bedcfad3d0ffebdf4b59b501844e169c6`  
		Last Modified: Thu, 17 Oct 2024 07:47:32 GMT  
		Size: 5.7 MB (5696893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0016e2802625fca20d28e3452492e3cfd61cf736bb40524b87ab218adc0cf19`  
		Last Modified: Thu, 17 Oct 2024 07:47:31 GMT  
		Size: 54.7 KB (54681 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:51ccc2765bebeac1b0bba81b8f8aad52cf4b2d714377320d050a227ac1539652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138718232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4892cd63dfe128f20f9dff93d1f06be12677d49d0fb57356e520a9c464ca2631`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:06:32 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 08 Aug 2024 17:06:32 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_MAJOR=15
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_VERSION=15.8-1.pgdg120+1
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:06:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:06:32 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:06:32 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:06:32 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:06:32 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ce2863b6239d64258cb5259fe7c6662af1a6608de30cfbd083cbd8f2c4444a`  
		Last Modified: Thu, 17 Oct 2024 18:17:29 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca05ab1f003fb8509ac57a2e4c7d6878be5f1bea874573563d5b8f1c08ae5ad5`  
		Last Modified: Thu, 17 Oct 2024 18:17:30 GMT  
		Size: 3.7 MB (3742584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83f5906664d16faa0b6d62929bea3e5c74cad9286294ee54eb7117da1297007`  
		Last Modified: Thu, 17 Oct 2024 18:17:30 GMT  
		Size: 1.4 MB (1413641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c58f3f3af02b25f25b523ed0ea1fb442270ebf32158b3855452ba22389eaab`  
		Last Modified: Thu, 17 Oct 2024 18:17:30 GMT  
		Size: 8.1 MB (8066302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0aa0d5d266482ff233121591ef9a5eb2b155bb6cbca321c85bd71a5155470c`  
		Last Modified: Thu, 17 Oct 2024 18:17:31 GMT  
		Size: 1.1 MB (1066987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40edc6be753b3463eed28795acbc46b6f93f7f81ec0a582168c3755bb900e4e`  
		Last Modified: Thu, 17 Oct 2024 18:17:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42646e9542367c42cf1121b90465e4c66d80e11169ced1e36404b204b75a037c`  
		Last Modified: Thu, 17 Oct 2024 18:17:31 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18135ab7f024906e68fc28a6b5e1e0e9639ae148a1a876b478fcdb046882d469`  
		Last Modified: Thu, 17 Oct 2024 19:19:00 GMT  
		Size: 99.7 MB (99690418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc53bb35954f21ccf34437374033301fcbc4ad4e38c37bfd1325e6a27b1be3f`  
		Last Modified: Thu, 17 Oct 2024 19:18:57 GMT  
		Size: 9.8 KB (9783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db01c5ebc6d3ecfe9076391bba467191bfbc5bdf8ee738a26c9463a0334d6599`  
		Last Modified: Thu, 17 Oct 2024 19:18:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6c1dfe89e8af2d8afe4c2c9eb9a08011a961556246a2052027c39cacdc3825`  
		Last Modified: Thu, 17 Oct 2024 19:18:57 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851fcc5ee4d9f23555aba8a2093be297c5a11dc04685d55617748cadda021c5b`  
		Last Modified: Thu, 17 Oct 2024 19:18:58 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f22398a02c383c61946221f636e2efdeb7a7651f88792d7060ee4c75cc3078`  
		Last Modified: Thu, 17 Oct 2024 19:18:58 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:03d48fc68023d92d2c6c65ce0cc37b481d31c5f3ca37726b27ead50cd917b7a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5751239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89cbaa480ea4d71253b3292a26c5ac3cd47a934924ed5b7b2163be53ede92cdc`

```dockerfile
```

-	Layers:
	-	`sha256:4d2bb59243fa0df2acac73ccb5c680aff4f037b9cd82c52cf4d784bb0fa5b172`  
		Last Modified: Thu, 17 Oct 2024 19:18:57 GMT  
		Size: 5.7 MB (5696562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36821275abcb463f75253228a280e16e83c8a4fa52ee7348834d41d08e821172`  
		Last Modified: Thu, 17 Oct 2024 19:18:56 GMT  
		Size: 54.7 KB (54677 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:3f65904f99ea2efb1ea3900626bb88291fb540a4ae71bc410e5bd841e9b0da92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.5 MB (149517105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac86eeb81fe8a18039c5d9cd35ae47354105a21df6c146d4c7daf98ba32af8e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:06:32 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 08 Aug 2024 17:06:32 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_MAJOR=15
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_VERSION=15.8-1.pgdg120+1
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:06:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:06:32 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:06:32 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:06:32 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:06:32 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0dd2bf7a18016080f59a7ca20afcfd90b91b83dbe2f041cf829b175f8ed6417`  
		Last Modified: Thu, 17 Oct 2024 16:52:20 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecbc93de950e66abc2e48dcd67567fe8383702b3328af21a2dc72ad541ee30b`  
		Last Modified: Thu, 17 Oct 2024 16:52:21 GMT  
		Size: 4.5 MB (4499091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90646cadd7e608655d76f77b10a651de51ff7e45e8622c6be9155e37520bbc36`  
		Last Modified: Thu, 17 Oct 2024 16:52:21 GMT  
		Size: 1.4 MB (1378704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1dbef7dcaa1cabc44cc6659c4062b8fc5551dc57b9f3cb74f848092759b3516`  
		Last Modified: Thu, 17 Oct 2024 16:52:21 GMT  
		Size: 8.1 MB (8066287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7fdac227b96bb069a8114e3b8b41fe86c9e151bdabc4e73bd68643c5c49dffb`  
		Last Modified: Thu, 17 Oct 2024 16:52:22 GMT  
		Size: 1.1 MB (1108682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425a818d8223761585857cfa34430bf776e000e24eee1c9d6dd2631cded5b9a6`  
		Last Modified: Thu, 17 Oct 2024 16:52:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a40d31bfac2ea14b8ca0c6eaceef69b4fbe8241145ca06710903bc02fee8c5`  
		Last Modified: Thu, 17 Oct 2024 16:52:22 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2454e873980037b97635f87b5323d8f97b673c826959e8dbd71c011f947034d6`  
		Last Modified: Thu, 17 Oct 2024 16:56:26 GMT  
		Size: 105.3 MB (105287900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5aebdca29247210f0c2bc3865956a0e67e8658b7ae8168eb7774726c57c627`  
		Last Modified: Thu, 17 Oct 2024 16:56:22 GMT  
		Size: 9.8 KB (9774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b072345dc800ee52e8326261d657e4d715492055e7fa1f720f535a59a39bcebc`  
		Last Modified: Thu, 17 Oct 2024 16:56:22 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203c255034b7e4144d70c610dd4b528cbfb1f385e3630d0ee6d8192d8fe3423a`  
		Last Modified: Thu, 17 Oct 2024 16:56:22 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2263067458bf35e192cb765b8a631a2727e72e02dfd0151bc44eeda1612a173f`  
		Last Modified: Thu, 17 Oct 2024 16:56:23 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ec239a88b4e55e1fb8c362bd47930f15ac6c4d0578610ca7cb2820a03da052`  
		Last Modified: Thu, 17 Oct 2024 16:56:23 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:1b6e7c95fbb60b1113749f1c2afa8a63290ea0f297fccb441e338ba95c7cab7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5746400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2706bd82c7cc2a6a84c2a5d4fee295cc5b32be4c3f22a5ca3da82062f69ae68c`

```dockerfile
```

-	Layers:
	-	`sha256:25bea552643c4a62b7d7005a9f8b88b9a40f6ceba5c5fbcd9c606629e30736a6`  
		Last Modified: Thu, 17 Oct 2024 16:56:23 GMT  
		Size: 5.7 MB (5691667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3de443542e86269c3cdeb85d18850e11acd7d84e0012a14e1dcd9212a4787fe7`  
		Last Modified: Thu, 17 Oct 2024 16:56:22 GMT  
		Size: 54.7 KB (54733 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:dd76a44da2ca031ad82bdcfdbecab3b18b63330b9dcef918ba64e2f39dc22ab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.4 MB (159370831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9cfd8121fe3e64b6068a4f9188bfab7eb0a2006e8d767640ac89e3350097c99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:06:32 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Thu, 08 Aug 2024 17:06:32 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_MAJOR=15
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_VERSION=15.8-1.pgdg120+1
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:06:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:06:32 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:06:32 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:06:32 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:06:32 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef262d054afe03cde779bc46be9bd36fe827c03660455740d4ceff58cbf672c`  
		Last Modified: Thu, 17 Oct 2024 01:38:13 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6946a2c96dd86ccc0613a4cd0bdbe715ceff50d094879920297f8a0f9daed7ab`  
		Last Modified: Thu, 17 Oct 2024 01:38:13 GMT  
		Size: 5.0 MB (4965057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5916fb055a6b6629a522ae09621f8a23d6b498a392764ab5f64ca2392097df97`  
		Last Modified: Thu, 17 Oct 2024 01:38:13 GMT  
		Size: 1.4 MB (1422116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c639a462e7fc0449a47f0a8d2f7ee0ce10679fed35885a4ca325eb06c2d74daf`  
		Last Modified: Thu, 17 Oct 2024 01:38:13 GMT  
		Size: 8.1 MB (8066280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4314c921b3d282acde4759ca0505dfec031a307d630f3a816c95fd690837f8`  
		Last Modified: Thu, 17 Oct 2024 01:38:13 GMT  
		Size: 1.1 MB (1137120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca6d34cf2e76895a18c8ab90eb6de748272b98d9a4f1f39707f911c696080e1`  
		Last Modified: Thu, 17 Oct 2024 01:38:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f8fb7964a382e1231cc0f26b7ba3fd5d372113fe56d1b8e6d5db8b0e15828f`  
		Last Modified: Thu, 17 Oct 2024 01:38:14 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc86adc02b033bd0f72df9a4357fb0204e6b698312482048b1e51699c9d4c599`  
		Last Modified: Thu, 17 Oct 2024 01:38:17 GMT  
		Size: 113.6 MB (113615888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239e89c854a710072630679123c542992925da192e7d0ef81a54dd5657fc3181`  
		Last Modified: Thu, 17 Oct 2024 01:38:14 GMT  
		Size: 9.8 KB (9782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97c27f1f5a8814909d0a07ee967bada86859dc5b5002cfff4538a0e6a1145a4`  
		Last Modified: Thu, 17 Oct 2024 01:38:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1577b72173540a637d70878f876be662500486adb609e3c331afecbb69630286`  
		Last Modified: Thu, 17 Oct 2024 01:38:14 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e998d63d4231e77e4717d90e33b38d50ca5702f728b4db767334996944e1865`  
		Last Modified: Thu, 17 Oct 2024 01:38:15 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b88d3acc3f1024a5ad98e44995ec0d6a46e61c496e570d6a96f0507b3a4e115`  
		Last Modified: Thu, 17 Oct 2024 01:38:15 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:4f2a665be75fe5b2b1c6f1d59aec4eadb1395a3d577261fb284e4037547ab3ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c4cac17e1c983218517de515cf57a93964280eba2bc10a4e7faffddb4c9986`

```dockerfile
```

-	Layers:
	-	`sha256:e750bc26721714ac14e6eb9d805adffcdc3f15d610ce1099ecef0d735fbf7fa9`  
		Last Modified: Thu, 17 Oct 2024 01:38:13 GMT  
		Size: 5.7 MB (5694946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcb098a90596b1938492aea25f7296597863e565c0deea861364efd9f379752b`  
		Last Modified: Thu, 17 Oct 2024 01:38:13 GMT  
		Size: 54.4 KB (54419 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:3c8996c35d352aa803a4fcefe7f5403accffc923767645dbc0a385f01922e307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.7 MB (146680914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8a6c2e95976dce6dbab76a3ae0c91dc13e94a2281c0583cc07947973e54b1c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:06:32 GMT
ADD file:6c11edc513b28b5a4034ee9c0d4cdcf019a82635ebb8a9e02732800fa457f683 in / 
# Thu, 08 Aug 2024 17:06:32 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_MAJOR=15
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_VERSION=15.8-1.pgdg120+1
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:06:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:06:32 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:06:32 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:06:32 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:06:32 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8f9d02f0305fc460f51690aebcb328c22e13a197228c0910e24b813db943a15b`  
		Last Modified: Thu, 17 Oct 2024 01:18:03 GMT  
		Size: 29.1 MB (29124779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8229a2b987c573ce24ec7945077cf94f45b4a93df0198919b64922db9c3d8e`  
		Last Modified: Fri, 18 Oct 2024 03:04:08 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a489944320ceb947ee507a596c278713aa6c35f4d279d0113f6974c16f35bcd`  
		Last Modified: Fri, 18 Oct 2024 03:04:09 GMT  
		Size: 4.5 MB (4475088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de62f1c89cab68b642617b5cafd8e41baac61f9645a7354c67920d5f17ad27b`  
		Last Modified: Fri, 18 Oct 2024 03:04:09 GMT  
		Size: 1.3 MB (1333805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057ffadde1b963c62db1ed441776e0a13abb6f376f7b12989b3f8dcf720fe931`  
		Last Modified: Fri, 18 Oct 2024 03:04:10 GMT  
		Size: 8.1 MB (8066484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df456abfb9c28297ff9a11730d0e8bed88a2748b1208c1083cc2a8bb4446f42`  
		Last Modified: Fri, 18 Oct 2024 03:04:10 GMT  
		Size: 1.2 MB (1182670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec8f00e859c32d94c35f3cfc73660226851eafc696f6b834bec9c4ee51bb6b5`  
		Last Modified: Fri, 18 Oct 2024 03:04:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234a24e0f4148cf6ec18bd7c5e0b0c4485e91eb339b11945f4639e671624e1bc`  
		Last Modified: Fri, 18 Oct 2024 03:04:10 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37350cfe78ea0ace115493162ca1b02c60f6d45a28a1e770f112c7966343909`  
		Last Modified: Fri, 18 Oct 2024 05:23:24 GMT  
		Size: 102.5 MB (102477975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a917b2ec9a2a3763dd5984239bdb5a5a6c17b5d538f8db7f0b1d819056946d`  
		Last Modified: Fri, 18 Oct 2024 05:23:14 GMT  
		Size: 9.8 KB (9784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325f4b43816e21e49a8302b2ed9b3bb5664ea60a7a9d0ae7b91da062374e5720`  
		Last Modified: Fri, 18 Oct 2024 05:23:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af8caf29eb14a183507226ebfffe04224c455e3de8c60c88125db3adf268c8a`  
		Last Modified: Fri, 18 Oct 2024 05:23:14 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df22b42f21873b1bce10aabf77b15ce6a1e73256fc49356d6dd4b9cd12b3f60e`  
		Last Modified: Fri, 18 Oct 2024 05:23:15 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3209dfe7659df70f97bac85c628541cdcff61a2eccc31af029e58b8e7636dbc`  
		Last Modified: Fri, 18 Oct 2024 05:23:15 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:1d20fddb7f71f5d79bccb68b8c7334c750f681ba3f3cd06806c2861512237a0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 KB (54341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41f1b128f417758f3ef244314994eea1be7ed829812d29007fa28b102d9f0d0d`

```dockerfile
```

-	Layers:
	-	`sha256:10bcc05ec0f2dec7947acad6938ac1f1f30a8ef950d0116e1c578edc5c81a2a4`  
		Last Modified: Fri, 18 Oct 2024 05:23:14 GMT  
		Size: 54.3 KB (54341 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:5a17ff17f419e1673c78822193da7be999698dd487803653b6bc2ce8e0f1edc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.5 MB (163484243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae4e0de4349f2f88a6a06102b3cd6ec6af4fca0c2ae5cb7e0e386ff10a413be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:06:32 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Thu, 08 Aug 2024 17:06:32 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_MAJOR=15
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_VERSION=15.8-1.pgdg120+1
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:06:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:06:32 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:06:32 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:06:32 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:06:32 GMT
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
	-	`sha256:44600cf6e943e414055a7845fa4463137385c5558f5ec57948a6eb0090ea421c`  
		Last Modified: Thu, 17 Oct 2024 11:15:10 GMT  
		Size: 114.3 MB (114255406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a03bda33c94d43860b736042bf585b7f960c3b413965993b0168610068142d8`  
		Last Modified: Thu, 17 Oct 2024 11:15:06 GMT  
		Size: 9.8 KB (9783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49524771101d2f95b624a31ae1c042f7c9a345b1c3847f69339c48281781d8c9`  
		Last Modified: Thu, 17 Oct 2024 11:15:06 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b76f32ac73e122c9f060576640e09c6e29f5aeeb47c4f62e95e7e07fcf6fcff`  
		Last Modified: Thu, 17 Oct 2024 11:15:06 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689a8c4b24fa9710df490e34a5a8bb412672041e20b63ec0b800342f6a365ddb`  
		Last Modified: Thu, 17 Oct 2024 11:15:07 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8aaaadb7b39fd2b0b1d9b8018cafa7aa3ae6893a489d1f1c38b8af9aef2960c`  
		Last Modified: Thu, 17 Oct 2024 11:15:07 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:e0cd7992916ca38601c49c4528d3c758b1ffbbefec4687e0a148a103e1c760df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5747085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87f1de178ae711c62e165f9f99d4a9b300c8220c69f863c63d114dd468059084`

```dockerfile
```

-	Layers:
	-	`sha256:f6e4e6d0125f63d661e3171c036da730e4a44771b797a19adcee3a5661bac6d1`  
		Last Modified: Thu, 17 Oct 2024 11:15:07 GMT  
		Size: 5.7 MB (5692555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab6b06ef9075b3e406683f6b2b3c62ad81d0eb607158a997801c3e613e95d7f7`  
		Last Modified: Thu, 17 Oct 2024 11:15:06 GMT  
		Size: 54.5 KB (54530 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:5fda1403d4dd4f592e36c653682fd1d52b6537c8749cb4b575d1351ddbe3b966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.9 MB (156872043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59e5044f346720dfbca3ba097af3c83d83cf457d24d6e38f886224d9805dc1e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:06:32 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Thu, 08 Aug 2024 17:06:32 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_MAJOR=15
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PG_VERSION=15.8-1.pgdg120+1
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:06:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:06:32 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:06:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:06:32 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:06:32 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:06:32 GMT
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
	-	`sha256:46aa6d2c91913b84558cbe0120449f700e46f863f6e3286403ec8aed350204f7`  
		Last Modified: Thu, 17 Oct 2024 16:05:18 GMT  
		Size: 114.3 MB (114340784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9fe3665ab074ce4486b810cbdc8277c5083248140d55dfe0400caf443e1863f`  
		Last Modified: Thu, 17 Oct 2024 16:05:16 GMT  
		Size: 9.8 KB (9775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8118c9038d490b7e0be57225f00034d73fb2da7282717582b37ec0dd7809a696`  
		Last Modified: Thu, 17 Oct 2024 16:05:16 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4086fd05e6adb48534e325f5a8da88d965d64c24b4104588075121744a9b0a67`  
		Last Modified: Thu, 17 Oct 2024 16:05:16 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36def569aeac30fa22eec1475add522bdd315153c3af52eb033ee30de83f3ae0`  
		Last Modified: Thu, 17 Oct 2024 16:05:17 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b79772ab4e621cbfd15663a36e7639bf1509a69f62bf6d514ccdfb77352704f`  
		Last Modified: Thu, 17 Oct 2024 16:05:17 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:f036108e28d55dd64eb91941a9ad4d9be333511b5c1884baeed7b9ca32d1138d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5739190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:886a0fccc8ee327fd49b5d696f973537b62b4e57eb7237ca48bd1ffedb2816a8`

```dockerfile
```

-	Layers:
	-	`sha256:ac8c6475680842facbb8f491860f745e1138fd6fc4b1c91bb950ad089b18a002`  
		Last Modified: Thu, 17 Oct 2024 16:05:16 GMT  
		Size: 5.7 MB (5684720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a012fd66863907b2a2a9912022bdf8ddad4a9ae671360049834146a7db33c05`  
		Last Modified: Thu, 17 Oct 2024 16:05:15 GMT  
		Size: 54.5 KB (54470 bytes)  
		MIME: application/vnd.in-toto+json
