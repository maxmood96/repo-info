## `postgres:19beta1-bookworm`

```console
$ docker pull postgres@sha256:d08badde5401957e1b22247fcef35073383e5bad2938fd7e1fdd1e9cd766123e
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

### `postgres:19beta1-bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:7f8b1b846126adfad835ed90ad5921cd883c2581ca62de1617954f456b469c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.5 MB (158466115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:623e3ba2126aba28b4410461418b5b594be84035c934ff211d09620e3c1b1d66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Sat, 06 Jun 2026 00:20:23 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sat, 06 Jun 2026 00:20:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jun 2026 00:20:34 GMT
ENV GOSU_VERSION=1.19
# Sat, 06 Jun 2026 00:20:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 06 Jun 2026 00:20:38 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Sat, 06 Jun 2026 00:20:38 GMT
ENV LANG=en_US.utf8
# Sat, 06 Jun 2026 00:20:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jun 2026 00:20:41 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 06 Jun 2026 00:20:41 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 06 Jun 2026 00:20:41 GMT
ENV PG_MAJOR=19
# Sat, 06 Jun 2026 00:20:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/19/bin
# Sat, 06 Jun 2026 00:20:41 GMT
ENV PG_VERSION=19~beta1-1.pgdg12+1
# Sat, 06 Jun 2026 00:21:00 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Sat, 06 Jun 2026 00:21:00 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 06 Jun 2026 00:21:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 06 Jun 2026 00:21:00 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Sat, 06 Jun 2026 00:21:00 GMT
VOLUME [/var/lib/postgresql]
# Sat, 06 Jun 2026 00:21:00 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 00:21:00 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 06 Jun 2026 00:21:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Jun 2026 00:21:00 GMT
STOPSIGNAL SIGINT
# Sat, 06 Jun 2026 00:21:00 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 06 Jun 2026 00:21:00 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33dbf7c10f5b7ced9bf801cb601415ec0e96db02fb646deea42610612dfb0651`  
		Last Modified: Sat, 06 Jun 2026 00:21:19 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf81d0222f01f01e55809e1ed902a4e591aa92c99778d9ad989ba89d006debae`  
		Last Modified: Sat, 06 Jun 2026 00:21:19 GMT  
		Size: 4.5 MB (4534241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c2495e132c41f937b540487580b232acf019416dd945ccacbad8ec2e3b4ebc`  
		Last Modified: Sat, 06 Jun 2026 00:21:19 GMT  
		Size: 1.2 MB (1249559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9efd496415e68bfdb6af85b1ce9bcc3f6121485f85bda4e4e0611776340464`  
		Last Modified: Sat, 06 Jun 2026 00:21:20 GMT  
		Size: 8.1 MB (8066421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac606790b225498f5032b3804aadf71a845c82a7d855035f7b5c158df41007bb`  
		Last Modified: Sat, 06 Jun 2026 00:21:20 GMT  
		Size: 1.2 MB (1196402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390f0950cc14064cbe8d4566437337943154695f9a85ef38cbf19adbef620dcb`  
		Last Modified: Sat, 06 Jun 2026 00:21:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb30bc5ff0ce0706509689590455e16734252603e46235a0cb9759d573c8ec1`  
		Last Modified: Sat, 06 Jun 2026 00:21:21 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92deeedb6359ea36940c69517b5d7586e80ae9f53079a9ad780c50cc08bb1238`  
		Last Modified: Sat, 06 Jun 2026 00:21:27 GMT  
		Size: 115.2 MB (115153788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52edda05cdb235e7c412e0ac42895785a864456c33a318134d0881f4c4489e20`  
		Last Modified: Sat, 06 Jun 2026 00:21:22 GMT  
		Size: 21.3 KB (21324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0975304d5aa4fe1b21c1343c6180cdf709cf583f8320d2d0eb28bfd2321437ef`  
		Last Modified: Sat, 06 Jun 2026 00:21:22 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db62a00cd9f22b078156b157e07677f2a6c5aacdaf2274076125066e25048724`  
		Last Modified: Sat, 06 Jun 2026 00:21:22 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02c9cd622353f3213ea70d4c1228fc5f64a8dd8be13f6324992b51bbd293d36`  
		Last Modified: Sat, 06 Jun 2026 00:21:23 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:ca2ab797d08c075f5350d30055ffacae0a8ec3c38690f6fef54994f41f812fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6249045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9960949485bc6bcc69776ec7f4aab6d8212a7fa6b418c87392b840b595bd819c`

```dockerfile
```

-	Layers:
	-	`sha256:327b28f432304ef12f3c7b40755fc598090a84563c102bebecc8fd6cfa327f9d`  
		Last Modified: Sat, 06 Jun 2026 00:21:19 GMT  
		Size: 6.2 MB (6198043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd173c410cd2dbf70d7a81db355209b2009e71f036ede78fd11423eb5bc1f5aa`  
		Last Modified: Sat, 06 Jun 2026 00:21:19 GMT  
		Size: 51.0 KB (51002 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:fd99dda4f72ea2bc760b26db6dfd9473efc936b992636974d7d1314f028ca204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87762007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c30a13233f52f0ba268bde6f1e3c67531468509c6dcc790dd895e83cf02b476d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1779062400'
# Sat, 06 Jun 2026 00:23:09 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sat, 06 Jun 2026 00:23:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jun 2026 00:23:25 GMT
ENV GOSU_VERSION=1.19
# Sat, 06 Jun 2026 00:23:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 06 Jun 2026 00:23:32 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Sat, 06 Jun 2026 00:23:32 GMT
ENV LANG=en_US.utf8
# Sat, 06 Jun 2026 00:23:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jun 2026 00:23:38 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 06 Jun 2026 00:23:38 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 06 Jun 2026 00:23:38 GMT
ENV PG_MAJOR=19
# Sat, 06 Jun 2026 00:23:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/19/bin
# Sat, 06 Jun 2026 00:23:38 GMT
ENV PG_VERSION=19~beta1-1.pgdg12+1
# Sat, 06 Jun 2026 00:36:05 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Sat, 06 Jun 2026 00:36:05 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 06 Jun 2026 00:36:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 06 Jun 2026 00:36:06 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Sat, 06 Jun 2026 00:36:06 GMT
VOLUME [/var/lib/postgresql]
# Sat, 06 Jun 2026 00:36:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 00:36:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 06 Jun 2026 00:36:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Jun 2026 00:36:06 GMT
STOPSIGNAL SIGINT
# Sat, 06 Jun 2026 00:36:06 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 06 Jun 2026 00:36:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3e5afa2eeb01167c187727ebcf5bb90554d4e6dd21fe61f1f694b128ceb15ac1`  
		Last Modified: Tue, 19 May 2026 22:36:20 GMT  
		Size: 25.8 MB (25768291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae7fcf9811c4333992ded468ffc2ef883d6e7fb4fa4e88b7469f12254aa8464`  
		Last Modified: Sat, 06 Jun 2026 00:36:19 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f437b44fa5f64fd9b1474c224f1680db200a70485b520f6d2ed9c08d5c598c79`  
		Last Modified: Sat, 06 Jun 2026 00:36:19 GMT  
		Size: 4.2 MB (4151276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66070084f55f60d608eb150a82459691b5377494bcdb7b8d833d309acd1f8ae6`  
		Last Modified: Sat, 06 Jun 2026 00:36:19 GMT  
		Size: 1.2 MB (1220069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba823ec77ab5d79d3f6e70b0fece3c537c85ef6400b18835f485157d38a1dc0`  
		Last Modified: Sat, 06 Jun 2026 00:36:19 GMT  
		Size: 8.1 MB (8066563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff2604269930375764e4f81436f12b3b80e8c737ac95747ff4f9e9cc5b85fd0`  
		Last Modified: Sat, 06 Jun 2026 00:36:20 GMT  
		Size: 1.2 MB (1195062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c256119faefe9aa61f65776640c6c6cca9aff19550d8d9db6ad5107ae9b46575`  
		Last Modified: Sat, 06 Jun 2026 00:36:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ddf9bfc4a5d5ec41e78816c46760e273074085555d61760278a19eeaf5b933`  
		Last Modified: Sat, 06 Jun 2026 00:36:20 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45121b81841a30e3d6637cb686b63c18c51bb5b3907f0e00a5b279fc0b8eb0b8`  
		Last Modified: Sat, 06 Jun 2026 00:36:22 GMT  
		Size: 47.3 MB (47328585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f930f1a3d11f0f1783499608cdc0c5c0ef0685c0f2472118c726f7b475f43a6`  
		Last Modified: Sat, 06 Jun 2026 00:36:22 GMT  
		Size: 21.3 KB (21322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec130964ceca9b18b01011dec5f5bcd1193ae1ed8db50075107f0571b5f1cf98`  
		Last Modified: Sat, 06 Jun 2026 00:36:22 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f97327e7e15ab9b7a7f465ed4b492e7f7a7c5505647a5158f45e20629e006a5`  
		Last Modified: Sat, 06 Jun 2026 00:36:22 GMT  
		Size: 6.1 KB (6100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd6180c0eb29cfb4a68d1df42418a35918465c961734e481de5623c4603c09f`  
		Last Modified: Sat, 06 Jun 2026 00:36:23 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:c6d537009c6c3ae41e2837a1f020dca8b50d6b7dc05d393589fceebc8d5f80aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5376862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d57d407fe5c5e62635636ad528e4f0d808200a664083a479b5ae9911ebd53aed`

```dockerfile
```

-	Layers:
	-	`sha256:2ad5ac112f9f9e8a124edde991ba992c412d58a416d9422fad338015918cf079`  
		Last Modified: Sat, 06 Jun 2026 00:36:19 GMT  
		Size: 5.3 MB (5325679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:716147e51500a1f57dd21660edc03e89cc1a2e748c933691e0d3e6dd8ba904fc`  
		Last Modified: Sat, 06 Jun 2026 00:36:18 GMT  
		Size: 51.2 KB (51183 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:fd11865e6a603b5e014e32641e6a1013f8b474522f135a2443675993b7fa704c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.8 MB (83842770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e10686a47756b94f675a851721e829ab24111e350a3b55e03cb71e7619eae57`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1779062400'
# Sat, 06 Jun 2026 00:26:55 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sat, 06 Jun 2026 00:27:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jun 2026 00:27:08 GMT
ENV GOSU_VERSION=1.19
# Sat, 06 Jun 2026 00:27:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 06 Jun 2026 00:27:13 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Sat, 06 Jun 2026 00:27:13 GMT
ENV LANG=en_US.utf8
# Sat, 06 Jun 2026 00:27:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jun 2026 00:27:18 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 06 Jun 2026 00:27:19 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 06 Jun 2026 00:27:19 GMT
ENV PG_MAJOR=19
# Sat, 06 Jun 2026 00:27:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/19/bin
# Sat, 06 Jun 2026 00:27:19 GMT
ENV PG_VERSION=19~beta1-1.pgdg12+1
# Sat, 06 Jun 2026 00:39:23 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Sat, 06 Jun 2026 00:39:24 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 06 Jun 2026 00:39:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 06 Jun 2026 00:39:24 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Sat, 06 Jun 2026 00:39:24 GMT
VOLUME [/var/lib/postgresql]
# Sat, 06 Jun 2026 00:39:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 00:39:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 06 Jun 2026 00:39:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Jun 2026 00:39:24 GMT
STOPSIGNAL SIGINT
# Sat, 06 Jun 2026 00:39:24 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 06 Jun 2026 00:39:24 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:af86988b12731b7fa2ac73fa1c3f6ab4510a6641d04afb18df09600383bc399d`  
		Last Modified: Tue, 19 May 2026 22:36:05 GMT  
		Size: 23.9 MB (23941643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042c46401dc94854d4c25bf8cb86c18ec0381371025694df817fad68c4577c58`  
		Last Modified: Sat, 06 Jun 2026 00:39:36 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c829d3697074d18a01297fa9750768ad82a76905fd227cc0dbcbb35f043aff1`  
		Last Modified: Sat, 06 Jun 2026 00:39:36 GMT  
		Size: 3.7 MB (3742722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01139c14f6c63385c077a08840dc9924c88a15732230746d3018c84de630637`  
		Last Modified: Sat, 06 Jun 2026 00:39:36 GMT  
		Size: 1.2 MB (1216050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7821fe81dac4c88bf16a188da843776faec084f765005ec34543eaaacdef7a66`  
		Last Modified: Sat, 06 Jun 2026 00:39:37 GMT  
		Size: 8.1 MB (8066409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0856f8e0ed36e184925e1dc3d008f2261749a9f0ca1810d5baba3b09bb6ba193`  
		Last Modified: Sat, 06 Jun 2026 00:39:37 GMT  
		Size: 1.1 MB (1067273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9309de0c9790f5ef4c7e1e0e386e7724f20354536c4565d6b039bc726fcdbd6b`  
		Last Modified: Sat, 06 Jun 2026 00:39:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb693297dc0308384932c3ae4471ae074dc2ada93fd9e0e020d6d00a9d4b819`  
		Last Modified: Sat, 06 Jun 2026 00:39:38 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c8d129c6c7f3b313b1f7bc883f79382c689d40ddd460c85a4bada00c48868b`  
		Last Modified: Sat, 06 Jun 2026 00:39:39 GMT  
		Size: 45.8 MB (45776505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e680378455bddb33f3e4b10784f6ddb3abaf5d44092a432d3f845efc151e5209`  
		Last Modified: Sat, 06 Jun 2026 00:39:39 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d047aa9b118145c7ce6b9b60a61288f69502b48f205592f4472dbd63b378155b`  
		Last Modified: Sat, 06 Jun 2026 00:39:39 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65112f88767c1c3232c120d5be7a8f300f053a311265988ca74645a12399d989`  
		Last Modified: Sat, 06 Jun 2026 00:39:39 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd1b1e32cd8de7cf21a3d85867b35676ea7e0f2b62cfc6c69766b3ca1245bb0`  
		Last Modified: Sat, 06 Jun 2026 00:39:40 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:30ab862f2b2d253a5a97e799fff4da8a8764c8fd8f4b43500c57f4ed42e7c577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5376113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b5105c5ca6b9d8f916c7ae6d8f169083280e32c6ce1b2f0d5e6dfa6faf0ae3`

```dockerfile
```

-	Layers:
	-	`sha256:89bbc495268b813c66b12204caa6d5fb4aaf8dbea573304284a2a535bc3ed964`  
		Last Modified: Sat, 06 Jun 2026 00:39:36 GMT  
		Size: 5.3 MB (5324930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f237a40b6ce2afe67a8b5be4023574bf985259ee0cef8628f8fc77d4090f8fdf`  
		Last Modified: Sat, 06 Jun 2026 00:39:36 GMT  
		Size: 51.2 KB (51183 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:3eeb4002af485fe3ccf89fab8901e3f51455a2b88c2ac2f9a4bb25f80c11b5a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156412288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b4406c00dd18760d1729c418c21a6c5f2ff13502818cf25be17c0cc8eaddaa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Sat, 06 Jun 2026 00:21:46 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sat, 06 Jun 2026 00:21:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jun 2026 00:21:56 GMT
ENV GOSU_VERSION=1.19
# Sat, 06 Jun 2026 00:21:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 06 Jun 2026 00:22:01 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Sat, 06 Jun 2026 00:22:01 GMT
ENV LANG=en_US.utf8
# Sat, 06 Jun 2026 00:22:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jun 2026 00:22:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 06 Jun 2026 00:22:04 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 06 Jun 2026 00:22:04 GMT
ENV PG_MAJOR=19
# Sat, 06 Jun 2026 00:22:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/19/bin
# Sat, 06 Jun 2026 00:22:04 GMT
ENV PG_VERSION=19~beta1-1.pgdg12+1
# Sat, 06 Jun 2026 00:22:23 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Sat, 06 Jun 2026 00:22:23 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 06 Jun 2026 00:22:23 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 06 Jun 2026 00:22:23 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Sat, 06 Jun 2026 00:22:23 GMT
VOLUME [/var/lib/postgresql]
# Sat, 06 Jun 2026 00:22:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 00:22:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 06 Jun 2026 00:22:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Jun 2026 00:22:23 GMT
STOPSIGNAL SIGINT
# Sat, 06 Jun 2026 00:22:23 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 06 Jun 2026 00:22:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5772d33135f8ba5e8c8caf680bbc67c8e3d189a21134244e6220d94f45a16359`  
		Last Modified: Sat, 06 Jun 2026 00:22:42 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828bbc45fbcf46c41c6be159e568b359777cb14c679a1ebb4a5800cfda9aec66`  
		Last Modified: Sat, 06 Jun 2026 00:22:43 GMT  
		Size: 4.5 MB (4519473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578bf7ae4f7a84aa27f1c6e15e0efca36a12fd5590585773e97716181fba5559`  
		Last Modified: Sat, 06 Jun 2026 00:22:43 GMT  
		Size: 1.2 MB (1203252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5698164f4c9870dcb5733affd31fa700c6eeec7ec2c6f372b01d810c32b8a6d9`  
		Last Modified: Sat, 06 Jun 2026 00:22:43 GMT  
		Size: 8.1 MB (8066455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ab3ce8a152d4939836577c52accd630095febc278791a69b4075ad3abd5f9f`  
		Last Modified: Sat, 06 Jun 2026 00:22:44 GMT  
		Size: 1.1 MB (1109023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90825a73afc8b2ffbb8b72d9c93b7bee5004620323efa6e40395ef60d01b44b7`  
		Last Modified: Sat, 06 Jun 2026 00:22:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6488f38238eb612a911889dbc5483944a36ed20b05d73272499f078ddbf508`  
		Last Modified: Sat, 06 Jun 2026 00:22:44 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5529e7260f49f5d4878b070151005e6f6799e61f406ece72f38ef75f73fed102`  
		Last Modified: Sat, 06 Jun 2026 00:22:47 GMT  
		Size: 113.4 MB (113366874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb1639cd54a948018966b0b4ad5092df23d5e5dabcbba3b16e4113e75d864d5b`  
		Last Modified: Sat, 06 Jun 2026 00:22:45 GMT  
		Size: 21.3 KB (21324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09dc9dc74d1564499d49f9478391eb2384c01bc65edd95406949a4ad6b8b0b3`  
		Last Modified: Sat, 06 Jun 2026 00:22:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992f23b4743dcbb5e06ee4a67fd11b5cc12f44dec9525e3369b658558c653b4c`  
		Last Modified: Sat, 06 Jun 2026 00:22:46 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7dbd2daea7246d92de0a2a4d35dc0745cb0d1bdef2833db6c8e91cdd0dcb9a`  
		Last Modified: Sat, 06 Jun 2026 00:22:47 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:89d6fef88d2d6744d484d7649f9f379f233c11ca9b89c893ce121bb2f9bd0c26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6255564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e655e8eda0987370e61853c58c1aae364060f491469ada83f4a218622d368538`

```dockerfile
```

-	Layers:
	-	`sha256:4db6cfb825ff657dbef6669841b3b642bcd498a33661f01020985928460fb24c`  
		Last Modified: Sat, 06 Jun 2026 00:22:43 GMT  
		Size: 6.2 MB (6204344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:559cf46cf71b29f35c240b9f1aae4e63e3b428fe920a5d196efd8b220b62a849`  
		Last Modified: Sat, 06 Jun 2026 00:22:42 GMT  
		Size: 51.2 KB (51220 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:4152d2684cd7d5d75644326f4dcbf9a0c6a68468a46fe02dd47751111ffe71fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94615599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8163b8f6584f33ae7f164f9d021b3a3dfe7deab15d9a62fe40f89061d2976c6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1779062400'
# Sat, 06 Jun 2026 00:21:20 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sat, 06 Jun 2026 00:21:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jun 2026 00:21:32 GMT
ENV GOSU_VERSION=1.19
# Sat, 06 Jun 2026 00:21:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 06 Jun 2026 00:21:36 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Sat, 06 Jun 2026 00:21:36 GMT
ENV LANG=en_US.utf8
# Sat, 06 Jun 2026 00:21:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jun 2026 00:21:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 06 Jun 2026 00:21:40 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 06 Jun 2026 00:21:40 GMT
ENV PG_MAJOR=19
# Sat, 06 Jun 2026 00:21:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/19/bin
# Sat, 06 Jun 2026 00:21:40 GMT
ENV PG_VERSION=19~beta1-1.pgdg12+1
# Sat, 06 Jun 2026 00:30:55 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Sat, 06 Jun 2026 00:30:55 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 06 Jun 2026 00:30:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 06 Jun 2026 00:30:55 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Sat, 06 Jun 2026 00:30:55 GMT
VOLUME [/var/lib/postgresql]
# Sat, 06 Jun 2026 00:30:55 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 00:30:55 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 06 Jun 2026 00:30:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Jun 2026 00:30:55 GMT
STOPSIGNAL SIGINT
# Sat, 06 Jun 2026 00:30:55 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 06 Jun 2026 00:30:55 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:408fe432485bb366e9a4871b553de2e6347ca580fe8a5d45c84c87fa58d5e5c7`  
		Last Modified: Tue, 19 May 2026 22:37:12 GMT  
		Size: 29.2 MB (29218601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e899700ce852ff98fc4f1edac5aeaf73624fc39bc1e213c6ee75568aa3e7b2`  
		Last Modified: Sat, 06 Jun 2026 00:31:07 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ae7e45cfb9577ad1e9651fb2d55d2db3291e9d31390d3d21cc5a4e66ab6f15`  
		Last Modified: Sat, 06 Jun 2026 00:31:08 GMT  
		Size: 5.0 MB (4966087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67eddecb79a70344c5e80f1d108219b7f8cc813a78a5544a8523f0c7d6163f93`  
		Last Modified: Sat, 06 Jun 2026 00:31:08 GMT  
		Size: 1.2 MB (1218644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1834b51da2213a5975fa032a77838e90f70e40b88bb785c78b5fe445da7bca3`  
		Last Modified: Sat, 06 Jun 2026 00:31:08 GMT  
		Size: 8.1 MB (8066450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a720ddabcf5385e4ac22fb82c11ed802a92ae462f06a3ada73975fdbdb8dfe7`  
		Last Modified: Sat, 06 Jun 2026 00:31:09 GMT  
		Size: 1.1 MB (1137455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c964a204261b7089ba1b9e971fe65162eee25cbe35393c56a8912b9972b75af`  
		Last Modified: Sat, 06 Jun 2026 00:31:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967add5fd1aa1bc875bc8c5f2b37f1c9a0b310b703638c8a5d47487299be60ee`  
		Last Modified: Sat, 06 Jun 2026 00:31:09 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f5845d729d6f245e453613d915900adea4961cfd6f83aec783c7708d81642d`  
		Last Modified: Sat, 06 Jun 2026 00:31:11 GMT  
		Size: 50.0 MB (49976198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a68e28ab7bca789e5852d9e48a808b666ba87d8dd64104e8a4a39977a2e8d56`  
		Last Modified: Sat, 06 Jun 2026 00:31:10 GMT  
		Size: 21.3 KB (21328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5aad79843ec808e4655c741fb27df0a3ca8636a9f9f55985b3342b655ec851`  
		Last Modified: Sat, 06 Jun 2026 00:31:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e859de1f9418e6f80c53d3393aa87c954d3ad50cde2022838dae98063841ed98`  
		Last Modified: Sat, 06 Jun 2026 00:31:11 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67e2466538c395cd8266de93f0324eee17c5a042237a1ce43976a9d0067d44b`  
		Last Modified: Sat, 06 Jun 2026 00:31:12 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:d5a1be42f686d56e8dd8a904296d16a5d05615ad4aaa33338a614587e89a82e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5371231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5355e34e59c7a3684945dd9ca7dc72e3449bca8e3c72151d3f53f3c703ae8072`

```dockerfile
```

-	Layers:
	-	`sha256:11ef260696741fe89a2d61842426383d7964a69b7092fad606fec5ef82f95354`  
		Last Modified: Sat, 06 Jun 2026 00:31:08 GMT  
		Size: 5.3 MB (5320271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:706acd87a681dd31a77565317bb564305613c62cb37de3bd557391b5680f1000`  
		Last Modified: Sat, 06 Jun 2026 00:31:08 GMT  
		Size: 51.0 KB (50960 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:3dc9e7f57668ea5e0cf663e02468d2c5930320efda8e146447c19bdfe266b46b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.3 MB (157285106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4540512e0c0e9706997bd1a5b05333f680e2c49c9e4e099173ef41b4f050f0d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 03:47:32 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 20 May 2026 03:48:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 03:48:39 GMT
ENV GOSU_VERSION=1.19
# Wed, 20 May 2026 03:48:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 20 May 2026 03:49:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 20 May 2026 03:49:06 GMT
ENV LANG=en_US.utf8
# Wed, 20 May 2026 03:49:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jun 2026 00:51:49 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 06 Jun 2026 00:51:52 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 06 Jun 2026 00:51:52 GMT
ENV PG_MAJOR=19
# Sat, 06 Jun 2026 00:51:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/19/bin
# Sat, 06 Jun 2026 00:51:52 GMT
ENV PG_VERSION=19~beta1-1.pgdg12+1
# Sat, 06 Jun 2026 02:13:14 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Sat, 06 Jun 2026 02:13:16 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 06 Jun 2026 02:13:18 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 06 Jun 2026 02:13:18 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Sat, 06 Jun 2026 02:13:18 GMT
VOLUME [/var/lib/postgresql]
# Sat, 06 Jun 2026 02:13:19 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 02:13:21 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 06 Jun 2026 02:13:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Jun 2026 02:13:21 GMT
STOPSIGNAL SIGINT
# Sat, 06 Jun 2026 02:13:21 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 06 Jun 2026 02:13:21 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:83efaacc11aede9fdd3dcef1c025f5df70c81553b815dfb44caceaf1fa9eba75`  
		Last Modified: Tue, 19 May 2026 22:35:42 GMT  
		Size: 28.5 MB (28522504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eab0ac5538ed0c0ccb817c384f2da276651cb900c4ee7f52230d296d7319ecf`  
		Last Modified: Wed, 20 May 2026 05:02:21 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3f24330c464e9c9a34b9c04f2af74377fb284ba681aecf1eaca7b0c8d5b376`  
		Last Modified: Wed, 20 May 2026 05:02:22 GMT  
		Size: 4.5 MB (4475198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98381d3276d839839fdcebfcf33bf865cf90eaf43ccf575978aa617c4059ff4`  
		Last Modified: Wed, 20 May 2026 05:02:21 GMT  
		Size: 1.2 MB (1159226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbabcffa59b806ff40b6d0aca34bf8d4642e4fe8a0529111a0a19fcc23d24a8f`  
		Last Modified: Wed, 20 May 2026 05:02:22 GMT  
		Size: 8.1 MB (8066669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec23172ba38a0ef878da18a9628307ee3ba06cb2002c4d210fac8bf8332c862`  
		Last Modified: Wed, 20 May 2026 05:02:23 GMT  
		Size: 1.2 MB (1182959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b882910da423554623661e4da3ec8c0aca3506dc9c5185d885a45b7dfb780a`  
		Last Modified: Sat, 06 Jun 2026 02:15:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024c7337409d4b9f3e2f3c7d7af86076a1ec1e439643a602614a110fd5f593a3`  
		Last Modified: Sat, 06 Jun 2026 02:15:34 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be16cbb65f2f97e32a8e523ff3d074dabc96bec6d9ba97ab39d065a0e45cdce`  
		Last Modified: Sat, 06 Jun 2026 02:15:49 GMT  
		Size: 113.8 MB (113846377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690a1ca3a38c863c530dffff3e28cf32f88895c09e4b04899eeca6928369355b`  
		Last Modified: Sat, 06 Jun 2026 02:15:34 GMT  
		Size: 21.3 KB (21330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe341309fee51add2f59ad471ead394eceb3c125586dfef652aaf2553c93f7a`  
		Last Modified: Sat, 06 Jun 2026 02:15:35 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e5283de03c1a47a3c3c93041d2d8fb2f66093a2622aa1bf3c0dfdb4d6255c7`  
		Last Modified: Sat, 06 Jun 2026 02:15:35 GMT  
		Size: 6.1 KB (6100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b8fcabf0a04cfcf4c7b8df865acf4ec17b243190e334e3c02598f191fdfd4c`  
		Last Modified: Sat, 06 Jun 2026 02:15:35 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:97ec5fcb7684e37686d72e5f5a2f1c1a372e9704ba3a02cee685f9b1e6db3846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 KB (50856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0fceab474ab0684a76b39681e5fa11d35866d9ba8bba9f268595cb4c8df0788`

```dockerfile
```

-	Layers:
	-	`sha256:8ebe2caaf5adb54d723869a2092e542340994c1558c737276c1acb590a15e0e6`  
		Last Modified: Sat, 06 Jun 2026 02:15:34 GMT  
		Size: 50.9 KB (50856 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:bf8de9a8f15eabbb321d647f4e3f836fa13875b36ab5baf9f94b1f6764a72b1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.4 MB (171448662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6575ccc6355cdebc8f527ec98fa3dbe03e40ab4b470f58d99fdabefa4e7aa21b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Sat, 06 Jun 2026 01:04:43 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sat, 06 Jun 2026 01:04:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jun 2026 01:05:09 GMT
ENV GOSU_VERSION=1.19
# Sat, 06 Jun 2026 01:05:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 06 Jun 2026 01:05:17 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Sat, 06 Jun 2026 01:05:17 GMT
ENV LANG=en_US.utf8
# Sat, 06 Jun 2026 01:05:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jun 2026 01:05:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 06 Jun 2026 01:05:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 06 Jun 2026 01:05:26 GMT
ENV PG_MAJOR=19
# Sat, 06 Jun 2026 01:05:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/19/bin
# Sat, 06 Jun 2026 01:05:26 GMT
ENV PG_VERSION=19~beta1-1.pgdg12+1
# Sat, 06 Jun 2026 01:06:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Sat, 06 Jun 2026 01:06:07 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 06 Jun 2026 01:06:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 06 Jun 2026 01:06:08 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Sat, 06 Jun 2026 01:06:08 GMT
VOLUME [/var/lib/postgresql]
# Sat, 06 Jun 2026 01:06:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 01:06:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 06 Jun 2026 01:06:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Jun 2026 01:06:08 GMT
STOPSIGNAL SIGINT
# Sat, 06 Jun 2026 01:06:08 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 06 Jun 2026 01:06:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:562cecbb5aa529d280e58ef1f95f14cdcd37a90c5ea9181798a78377e934e6e7`  
		Last Modified: Tue, 19 May 2026 22:35:14 GMT  
		Size: 32.1 MB (32075742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65fb76d3442e74499cb63951a7a179a4bac0a5f1f704daca58d4fafd2399c1c`  
		Last Modified: Sat, 06 Jun 2026 01:07:00 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085619a8c9a97c6d8f38e5f158ae5936650a8e550512066f5525a4f4f0466095`  
		Last Modified: Sat, 06 Jun 2026 01:07:00 GMT  
		Size: 5.4 MB (5368607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d35864fb0213c2010f6d21563e95e71a82f1e13512cc6584a77e34993898597`  
		Last Modified: Sat, 06 Jun 2026 01:07:00 GMT  
		Size: 1.2 MB (1208177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb857abe3c9d2a8488a60518e1e1d4a5a5ff004cb5b32afdebc6eda67eba429`  
		Last Modified: Sat, 06 Jun 2026 01:07:00 GMT  
		Size: 8.1 MB (8066570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd6e9bc8d13e26f4de8bcc4213ca3d7a0670fc6d8f4cdd007f41f78bf7034ba`  
		Last Modified: Sat, 06 Jun 2026 01:07:01 GMT  
		Size: 1.3 MB (1283650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ed9f86db4b1a541cd241cb1c72011e990f7c9b424729636e7d14ba5af59c9f`  
		Last Modified: Sat, 06 Jun 2026 01:07:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6736a7958c56664b61c9df127734297c99ffe02f5703ee64d5e4f1885a2fc37`  
		Last Modified: Sat, 06 Jun 2026 01:07:02 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a1a303f88248665d8b0196b2ddd585958c7dd27d1eb13e9fa80ee459ea108f`  
		Last Modified: Sat, 06 Jun 2026 01:07:05 GMT  
		Size: 123.4 MB (123413754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3991885069efb6f6640ea53332a9cab0427e4c17d5fa6ff9d59e84ce3476fa6`  
		Last Modified: Sat, 06 Jun 2026 01:07:03 GMT  
		Size: 21.3 KB (21322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008b35196faa97a26f562458596a4d43682ed991d59d101f82237a86077dfe13`  
		Last Modified: Sat, 06 Jun 2026 01:07:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6fbe50c0e195371d01ff5dffaa22498cb72c7b3f7f22cd035140dd6d90c2f6e`  
		Last Modified: Sat, 06 Jun 2026 01:07:03 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4a3fe797e7fbb71fdf0459d11dae0dd59c9b51b95e6d12155b21f23e1ee1a7`  
		Last Modified: Sat, 06 Jun 2026 01:07:04 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:0d07394cf7731d09ad9939e26ee60d2f33f4cf7f1aa0c4eb80f30768a1397129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6256463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4bebf488d1e70639c835bf19a9d984c3ef14fb182af75ad67a7390903b4ec1`

```dockerfile
```

-	Layers:
	-	`sha256:a76f995b07574af899154f780490867bf3e3e1943039f7a4cbdf7283c0277917`  
		Last Modified: Sat, 06 Jun 2026 01:07:00 GMT  
		Size: 6.2 MB (6205416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e299c35ad77e0e3893e4b1007af933c6d68d69df9be9e111f89e1806e9277769`  
		Last Modified: Sat, 06 Jun 2026 01:07:00 GMT  
		Size: 51.0 KB (51047 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:2342a8097721d20781e832e6782078c4a4979c006ac23416b3b1fbf0ddc21789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167797769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdf3ab0ecabad761b497bfc4b55c927e8f2fe8d2fe514f069faf1ac5725ffd80`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Sat, 06 Jun 2026 00:30:47 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sat, 06 Jun 2026 00:30:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jun 2026 00:31:00 GMT
ENV GOSU_VERSION=1.19
# Sat, 06 Jun 2026 00:31:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 06 Jun 2026 00:31:05 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Sat, 06 Jun 2026 00:31:05 GMT
ENV LANG=en_US.utf8
# Sat, 06 Jun 2026 00:31:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jun 2026 00:31:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 06 Jun 2026 00:31:09 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 06 Jun 2026 00:31:09 GMT
ENV PG_MAJOR=19
# Sat, 06 Jun 2026 00:31:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/19/bin
# Sat, 06 Jun 2026 00:31:09 GMT
ENV PG_VERSION=19~beta1-1.pgdg12+1
# Sat, 06 Jun 2026 00:45:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Sat, 06 Jun 2026 00:45:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 06 Jun 2026 00:45:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 06 Jun 2026 00:45:12 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Sat, 06 Jun 2026 00:45:12 GMT
VOLUME [/var/lib/postgresql]
# Sat, 06 Jun 2026 00:45:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 00:45:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 06 Jun 2026 00:45:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Jun 2026 00:45:12 GMT
STOPSIGNAL SIGINT
# Sat, 06 Jun 2026 00:45:12 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 06 Jun 2026 00:45:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f68f0b97bbcc8e9b228a5585b8232e9a03b85ceb75522df7330c0e21071254`  
		Last Modified: Sat, 06 Jun 2026 00:45:43 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4717d5e7758c20b8fc350a88d450d4135c8f56319dff2cf30eebc7bc33e559d`  
		Last Modified: Sat, 06 Jun 2026 00:45:43 GMT  
		Size: 4.4 MB (4391190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806baf047d5ee2d1d92b764c12ccc2c1ae561cabae3afeda57df72d4b4de34a1`  
		Last Modified: Sat, 06 Jun 2026 00:45:43 GMT  
		Size: 1.2 MB (1222826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985fdc550fedbe827c1b577fe3e13f524d7b98d07b036fad169e1d773da09664`  
		Last Modified: Sat, 06 Jun 2026 00:45:43 GMT  
		Size: 8.1 MB (8120769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af725c1517aead93cd7fe06f1fcf6d0b26905207eb4ea9aed8d27f253d7f418f`  
		Last Modified: Sat, 06 Jun 2026 00:45:44 GMT  
		Size: 1.1 MB (1097083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed73bd90967f3836a15201963c68376b186b01df266aec01da68e3cd8071d84b`  
		Last Modified: Sat, 06 Jun 2026 00:45:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e734f69afbde7413b6cdbb686e3e129ac8395ceb3951adc93b571ed69c54340`  
		Last Modified: Sat, 06 Jun 2026 00:45:44 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d63a0aec0b3486143a8ae16b0d7b88497a5e1b283faa84cbaee06061a7aaaf`  
		Last Modified: Sat, 06 Jun 2026 00:45:46 GMT  
		Size: 126.0 MB (126045138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afa9069c9a798221b353b00a5a4242e0d7f4ca1c227275fbf1d105f4a409898`  
		Last Modified: Sat, 06 Jun 2026 00:45:45 GMT  
		Size: 21.3 KB (21324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258f6b604240331ad909354f942da8035abe53404f779e6f68987258bcef5981`  
		Last Modified: Sat, 06 Jun 2026 00:45:45 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d591b14f73a2bbc85c44a08af9fdb8caa1885bb48a83af4aeec30a2c5225bb`  
		Last Modified: Sat, 06 Jun 2026 00:45:45 GMT  
		Size: 6.1 KB (6100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df128650fe486606949bb8829af5e6dfa22885ca6ec834a2e97cc2b14ed69c63`  
		Last Modified: Sat, 06 Jun 2026 00:45:46 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:09f39801ae2567877f3aae8d1ebb544b3820dd9b5159797eae74b16425202a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6263703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f90ed581d4e751166d8310a8763327a039963c51c369c240c7c942d7486a682`

```dockerfile
```

-	Layers:
	-	`sha256:33df15eb30b4d12c8843f5ea05de71b61b06abcec743754a712b896542dea649`  
		Last Modified: Sat, 06 Jun 2026 00:45:43 GMT  
		Size: 6.2 MB (6212701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50c3bc75ad814bd1debe380925869216f016fcff5ed907adc738dc194acbde7c`  
		Last Modified: Sat, 06 Jun 2026 00:45:43 GMT  
		Size: 51.0 KB (51002 bytes)  
		MIME: application/vnd.in-toto+json
