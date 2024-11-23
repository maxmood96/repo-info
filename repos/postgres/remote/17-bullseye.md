## `postgres:17-bullseye`

```console
$ docker pull postgres@sha256:8263253867f04ee580dd936221704b0637a213eb203e9de6880ed00aa4af0406
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
$ docker pull postgres@sha256:603796d3b8244fd15cf7f6d4a10fe2ffcc57f23ccb0f5885a50e64c274404c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151569434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12904aba17e0121f02f0a87248506774407708b1f8cfd9278492f01eaf4e5e30`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
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
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782c1a27186e75032fc83ac1a79bea88048be12317b9a93295fd258f8743b455`  
		Last Modified: Fri, 22 Nov 2024 20:23:51 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80984faabca5f28912bc9986e8386e6bb5150fe86a8efd8514a0958664fb832e`  
		Last Modified: Fri, 22 Nov 2024 20:23:51 GMT  
		Size: 4.3 MB (4308259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f719fb0f8d0b4cfb592cf0c8821155b4f5f1f06672f509122bd55554ed3480d`  
		Last Modified: Fri, 22 Nov 2024 20:23:51 GMT  
		Size: 1.5 MB (1472222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c555dc3ccc91272258223a8a57be56f5fa3d34ed5a84b3e39c8626f158c17f9c`  
		Last Modified: Fri, 22 Nov 2024 20:23:51 GMT  
		Size: 8.0 MB (8044441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393133dc5c86c967b491adaf7c89a1244152943a94fb70d7e64de945d2aeb59a`  
		Last Modified: Fri, 22 Nov 2024 20:23:52 GMT  
		Size: 1.0 MB (1038371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04122fdccbe4a626bc7d72b62ec34b8db231e187906eb3910aa752e3bfa8e392`  
		Last Modified: Fri, 22 Nov 2024 20:23:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f35141eef11c0dbf3676916b21381c2ce82b8bb355ddb4186afd111402553c9`  
		Last Modified: Fri, 22 Nov 2024 20:23:52 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508499293152dc4d0cac5e86f8f3eaf3abcb10a0b351d8bf6e06a34d0e8b6d98`  
		Last Modified: Fri, 22 Nov 2024 20:23:54 GMT  
		Size: 105.2 MB (105233498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5edb98ec2b0b3f4e4fe632058a6c4f03aaca172b81cafa9932d05da8566f931b`  
		Last Modified: Fri, 22 Nov 2024 20:23:52 GMT  
		Size: 10.2 KB (10238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2588d08a7dbf751bf4ae75b3c01d0ea1d34c5f2800a94867443ffa323e5eaa`  
		Last Modified: Fri, 22 Nov 2024 20:23:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a475be761b3b8a6e66f5d9094aac0608f01427e318bc3a93be7110c5683f8080`  
		Last Modified: Fri, 22 Nov 2024 20:23:53 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52fcf1817e97533d18fc6e5bee06c12b27f0221c075f209012c1757793cc172`  
		Last Modified: Fri, 22 Nov 2024 20:23:53 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77b94bcee2c499d25467b13dc1ca3888eb9b7b142432b4eeac592d34790203d`  
		Last Modified: Fri, 22 Nov 2024 20:23:53 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:08ee994badf5972768af94152c2b5318deb6463a7e39952ed40fb50dd7e90464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6097646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf69d1e3d8ab5c2b04791c61d0a4250ca7f9dd43ef868b6ef562cbe3a8515ce`

```dockerfile
```

-	Layers:
	-	`sha256:ec87d41087a2af2f81fb474ec4a7b7a1dfd08beead4862864ae3987d5ef37a75`  
		Last Modified: Fri, 22 Nov 2024 20:23:51 GMT  
		Size: 6.0 MB (6043349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81d4589e9c60e579e266bd627bf3d888680ffd6ce8eed235d7d0b0a52b6aeacc`  
		Last Modified: Fri, 22 Nov 2024 20:23:51 GMT  
		Size: 54.3 KB (54297 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:13eafea0d012b48e5c7bbf6fce56ed2501eee3014267a9a71901d3a2f4dd8ab9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139657618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:122a4777299f483e55de8a87b8672c28d64f5bebb904f13d723da368ae083f33`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
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
	-	`sha256:ffb425cb228d1443e7bb481e7662ebd8bbae82890777624387d60062e7ab28d0`  
		Last Modified: Fri, 22 Nov 2024 20:58:24 GMT  
		Size: 99.0 MB (99032945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e95f9f99ed59d5608115b2a3b971245276dbb9bccac7ee7e27d07aa5f8ce7a`  
		Last Modified: Fri, 22 Nov 2024 20:58:21 GMT  
		Size: 10.2 KB (10243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad48a2ef0688933db20ded25eca65d9e80c4922b629fd2d7a0296c61a8161f7`  
		Last Modified: Fri, 22 Nov 2024 20:58:21 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10db0bf98040264ad67174856d93ba6525252fb54d640d17ebbb7d0af9587775`  
		Last Modified: Fri, 22 Nov 2024 20:58:21 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59eb667b86f0967f32997168f6c3bafd03c506055821b3c2a2d956e6dfb5be6`  
		Last Modified: Fri, 22 Nov 2024 20:58:22 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddc384b2b15af26f6c1c7c0ffa7476939283244c943355346aa072795b2e3f3`  
		Last Modified: Fri, 22 Nov 2024 20:58:22 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:2401b8a7223bab6935405180fc2e696fd63be902a66a92eaec6957591a8694d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6114983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:779bc1070dbe968862686cf521b0f2d8d3e49dddba8494c7f23d7bf6777d1890`

```dockerfile
```

-	Layers:
	-	`sha256:59ef1786cbe00d75baa0caf48eaaf10dc186af4e4b19b54c3856922db4e4f44d`  
		Last Modified: Fri, 22 Nov 2024 20:58:22 GMT  
		Size: 6.1 MB (6060490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ceaf35d417a0591d670c5fb21e3d282dcfafecb7dcabfbce4b778b7f61a66fb3`  
		Last Modified: Fri, 22 Nov 2024 20:58:21 GMT  
		Size: 54.5 KB (54493 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:e18bb9f8af11dee34d58f9078351fe0d7948ed595721ff118f535819fd8fc4e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148712718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37ace0dfda3e4df3cf6d4fabff79f7d2e10327e078765b60a35c33f24db747c2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
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
	-	`sha256:4d5ec29b5cfbb8a97c634983a1e31d2350d9e768aeae0e8587b9085b68b83b13`  
		Last Modified: Fri, 22 Nov 2024 20:27:25 GMT  
		Size: 103.8 MB (103812000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0502070640a9cd8c3def63e7fa736eaddab4c81d0b1aedbd07f43deecc63174f`  
		Last Modified: Fri, 22 Nov 2024 20:27:23 GMT  
		Size: 10.2 KB (10239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2594a1ac388fde6fe2e8d6491026d0d47600c602f400db86d9ffcd07157160`  
		Last Modified: Fri, 22 Nov 2024 20:27:23 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5ca9a652f95e6b2c17b2464adc1e713a8331303c639501413b4f983976b868`  
		Last Modified: Fri, 22 Nov 2024 20:27:23 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01102a7c44710da7182980756680b5ee2e1baf77ce12abd964612b9d7f9496e`  
		Last Modified: Fri, 22 Nov 2024 20:27:24 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e93dc3de1359266d57f5485e383c9a7fad7a76b1695f92ca69c5fff2b5324c7`  
		Last Modified: Fri, 22 Nov 2024 20:27:24 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:6d0241e4a27250fa782c0ddcb1dbf366eaee8d1d6f615311d0c5c3d558e6e752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6104209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f581cd4c974c68952b7d028db6e03586865dbbac80dfe24f4cdb9020c734532f`

```dockerfile
```

-	Layers:
	-	`sha256:406c8d693613d61f48f8aae4885bb89b278cec8a732fa06b26b2ddbcb751390e`  
		Last Modified: Fri, 22 Nov 2024 20:27:21 GMT  
		Size: 6.0 MB (6049655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c56d096d08d5a7c3d647104239deebd765f269bb41b56cc4711cbe13b1aead3`  
		Last Modified: Fri, 22 Nov 2024 20:27:21 GMT  
		Size: 54.6 KB (54554 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:84e082e1305ff4c97292531c285e28ef74a3fd65ba19c561532c13324f0a4bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159860579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61fd906657f30dbed295a3431bc6cdbd3f7d008434f296df7994d29afee5c84a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
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
	-	`sha256:2aea24d0416284c8bc498d91bac1c90e2bf12b01e7867f799161bbb874a8323b`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 32.4 MB (32423351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ff4e8c0b3f7cac99474f71cb7d832074ec11b2d746a96b2f49b29987d755c2`  
		Last Modified: Fri, 22 Nov 2024 20:37:22 GMT  
		Size: 1.7 KB (1680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44799bc53b4af86ccf8975e22c9f986eb09da0f7fc9c2637cf9480ef0a075e1`  
		Last Modified: Fri, 22 Nov 2024 20:37:22 GMT  
		Size: 4.7 MB (4719704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0617dfcebb4e4eb6e28321e850f89604bd1d3c25ff23f46524a1ea127f679ff3`  
		Last Modified: Fri, 22 Nov 2024 20:37:22 GMT  
		Size: 1.4 MB (1447774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b73cc9c5d3f2c790e47ef5c4b80717b07d52925c9454f298520a11fe800d8d2`  
		Last Modified: Fri, 22 Nov 2024 20:37:22 GMT  
		Size: 8.0 MB (8044386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3de993c01ae396044e6ae246f8e35428244a839d0ee35ef46911a629dee4183`  
		Last Modified: Fri, 22 Nov 2024 20:37:23 GMT  
		Size: 1.0 MB (1028908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4aea017e8c644f62550a5e357ebab0a70673a3a2cd76f5fde4338000db5ed6d`  
		Last Modified: Fri, 22 Nov 2024 20:24:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd18f2ae96ec49c475957c506e64ad11420cda4b29f0a3b461480c915ff309d3`  
		Last Modified: Fri, 22 Nov 2024 20:37:23 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6fee1299c1b2a3e62455d7b5ea028f4c5bacbec4358ccc3620825a55a27df9d`  
		Last Modified: Fri, 22 Nov 2024 20:37:26 GMT  
		Size: 112.2 MB (112175377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f474872660efb5c06e808626b04736610c3fe135eb04422fb6cd7cef9b8a0d3d`  
		Last Modified: Fri, 22 Nov 2024 20:37:23 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf86aad43ab727d50264b17448876630c88ed2801408ba204c69aa8be39ff9d`  
		Last Modified: Fri, 22 Nov 2024 20:37:23 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e214f1b883efe7deb1a27e7cdd14079342e9ae3109dafe2a306073849ab9a27`  
		Last Modified: Fri, 22 Nov 2024 20:37:23 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5e58b358b9715cd6ee31591f3b0e1de17687f37e9b5631ec2ea76a05b5f690`  
		Last Modified: Fri, 22 Nov 2024 20:37:24 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e593122bea4258506f92cbfc4111b6443684bda642a1aaca14949f6dfd7aff8c`  
		Last Modified: Fri, 22 Nov 2024 20:37:24 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:d429a8a841c8c8bbbec0b996035637253c4968de6e5b1c66ac16469ed6984aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6112502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:729916568cf0eb6c4598602bb9392a5e6a41dba4b07dc3bb8c7538c76e6fe3b6`

```dockerfile
```

-	Layers:
	-	`sha256:83bd341784c6c80341efc61011f1c85db1a52904696b2e6bab7bb20ed8a2a3bc`  
		Last Modified: Fri, 22 Nov 2024 20:37:22 GMT  
		Size: 6.1 MB (6058254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf222d005fb69fd64f2d83924102ea7880e3e24bcff15707042d040215b3dfda`  
		Last Modified: Fri, 22 Nov 2024 20:37:22 GMT  
		Size: 54.2 KB (54248 bytes)  
		MIME: application/vnd.in-toto+json
