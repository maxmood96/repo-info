## `postgres:14-bookworm`

```console
$ docker pull postgres@sha256:8c0fa7c0a2f15b2b4598ab21fe49b3a57ae9990485ca96fefacf3b576699054d
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

### `postgres:14-bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:19d59590a60e7ba394dddf24838642a3871fb78646620272a0e9d2ce403baaf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.9 MB (151875397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc77fbd8d5acba006c8edc840bc8f8e3d6b0b06d2633e62c2be6f95cd383222`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:40:30 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 07 Apr 2026 01:40:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:40:41 GMT
ENV GOSU_VERSION=1.19
# Tue, 07 Apr 2026 01:40:41 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 07 Apr 2026 01:40:46 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 07 Apr 2026 01:40:46 GMT
ENV LANG=en_US.utf8
# Tue, 07 Apr 2026 01:40:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:40:49 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 07 Apr 2026 01:40:50 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:40:50 GMT
ENV PG_MAJOR=14
# Tue, 07 Apr 2026 01:40:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 07 Apr 2026 01:40:50 GMT
ENV PG_VERSION=14.22-1.pgdg12+1
# Tue, 07 Apr 2026 01:41:03 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 07 Apr 2026 01:41:03 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 07 Apr 2026 01:41:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 07 Apr 2026 01:41:03 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 07 Apr 2026 01:41:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 07 Apr 2026 01:41:03 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 07 Apr 2026 01:41:03 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:41:03 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 07 Apr 2026 01:41:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:41:03 GMT
STOPSIGNAL SIGINT
# Tue, 07 Apr 2026 01:41:03 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 07 Apr 2026 01:41:03 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21609f833d9caefaf8fab483f79262ecf4692d4e089c51f9e2eb63a9275db721`  
		Last Modified: Tue, 07 Apr 2026 01:41:23 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59316a2b5ad7cec315e56c4807bee21de32102d07dfa9da16892a4c6dc6a0a35`  
		Last Modified: Tue, 07 Apr 2026 01:41:23 GMT  
		Size: 4.5 MB (4534256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa5f5b55f3f0de4223327b3d3288e4f80a3a92f9d95d38ad9c3dc96c94b63e0`  
		Last Modified: Tue, 07 Apr 2026 01:41:23 GMT  
		Size: 1.2 MB (1249542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8f70a3e07217205398426195694bdd5a3c5eaee85ccc25c1c935e8a4a0d0b0`  
		Last Modified: Tue, 07 Apr 2026 01:41:23 GMT  
		Size: 8.1 MB (8066449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0785c7774676223f4fb79cc0b8c8dcc266e939cb8915abc9f1e2d71fb97bc438`  
		Last Modified: Tue, 07 Apr 2026 01:41:24 GMT  
		Size: 1.2 MB (1196392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d9111717c805610e67ba66a3cb46f88e49fa4db33afb9a0b47b7ca24b3d554`  
		Last Modified: Tue, 07 Apr 2026 01:41:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8310543721211e06090301f17397ae54a334eed339a71bebea0edea94961260`  
		Last Modified: Tue, 07 Apr 2026 01:41:25 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16831f55389c6f1230e4875a212d7adb4ca9779b40c1d46683d9e7e434bb91ef`  
		Last Modified: Tue, 07 Apr 2026 01:41:28 GMT  
		Size: 108.6 MB (108572149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b29be80b51e002958043a839315325fa710ae7cd4df0b53eb0a30a8fc54716`  
		Last Modified: Tue, 07 Apr 2026 01:41:25 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc419917a44dc18e6bd7d915fa894c91930ea1835e1e7a909737a0d22545517`  
		Last Modified: Tue, 07 Apr 2026 01:41:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105174c8ec48c10a223c403b63423a357768e0222c28712bc386a91157940af5`  
		Last Modified: Tue, 07 Apr 2026 01:41:26 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab197a6eaca7b89be3baa1bf844502d034c7c6ad8c46b4c4e69bc9422137aa6`  
		Last Modified: Tue, 07 Apr 2026 01:41:26 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a04f4d3655844891caecc52f358b7cc91d9b66010170260c00ee0b839c5eb86`  
		Last Modified: Tue, 07 Apr 2026 01:41:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:98267980587ae5ddf6df1276104de84aeb4e733c20fb8fc294d2da65c9dc1a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5847573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1189a9fd2c6949c72850b30b915661e54f9ea17181d01cd4e585baeec6fb753c`

```dockerfile
```

-	Layers:
	-	`sha256:a039c6746235b53109933d8eb26fb26698523563b468b0928e7ad0f7f95bc7bb`  
		Last Modified: Tue, 07 Apr 2026 01:41:23 GMT  
		Size: 5.8 MB (5794277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebc64b412a32bf5c1a1e3e7d2e8f9436734b9753f996a8d80c7b8a51f3362267`  
		Last Modified: Tue, 07 Apr 2026 01:41:23 GMT  
		Size: 53.3 KB (53296 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:2db91728415b0cdf1b8c3990a8117c0138e2cfd34515ff81cf14f35b8192c88c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144819650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466a84ebe45690e770994924eabc253d0cfd29a63aac179fea01c9a0c037a65a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:19:16 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 07 Apr 2026 02:19:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:19:33 GMT
ENV GOSU_VERSION=1.19
# Tue, 07 Apr 2026 02:19:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 07 Apr 2026 02:19:40 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 07 Apr 2026 02:19:40 GMT
ENV LANG=en_US.utf8
# Tue, 07 Apr 2026 02:19:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:19:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 07 Apr 2026 02:19:47 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:19:47 GMT
ENV PG_MAJOR=14
# Tue, 07 Apr 2026 02:19:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 07 Apr 2026 02:19:47 GMT
ENV PG_VERSION=14.22-1.pgdg12+1
# Tue, 07 Apr 2026 02:46:52 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 07 Apr 2026 02:46:53 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 07 Apr 2026 02:46:53 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 07 Apr 2026 02:46:53 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 07 Apr 2026 02:46:53 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 07 Apr 2026 02:46:53 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 07 Apr 2026 02:46:53 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 02:46:53 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 07 Apr 2026 02:46:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 02:46:53 GMT
STOPSIGNAL SIGINT
# Tue, 07 Apr 2026 02:46:53 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 07 Apr 2026 02:46:53 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4748d6bbb5a5b9e671dcabe2f909bdd7514f760a5cfdcd37d5b04627424120f2`  
		Last Modified: Tue, 07 Apr 2026 00:10:57 GMT  
		Size: 25.8 MB (25765667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250b541138bf361848237aaefdb9b20f836308acbe3c833782e6bc7d75bad358`  
		Last Modified: Tue, 07 Apr 2026 02:32:17 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f95597210f8a7d2c4d3345f7a3f16ac93660569d18b06f2ccaeadab82033d67`  
		Last Modified: Tue, 07 Apr 2026 02:32:17 GMT  
		Size: 4.2 MB (4151297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d534945b1192cf0e32b3064dfa737de633dad38e3408542542a0a58c59e408`  
		Last Modified: Tue, 07 Apr 2026 02:32:17 GMT  
		Size: 1.2 MB (1220124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279eeba8279a04ef67fe5c6d90503cc78939dfded81a88af5211cb27294c2139`  
		Last Modified: Tue, 07 Apr 2026 02:32:17 GMT  
		Size: 8.1 MB (8066580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac64f3a39408578a5db85aa07177a86b45b89fc4c807c67815e439bb8c099ba8`  
		Last Modified: Tue, 07 Apr 2026 02:32:18 GMT  
		Size: 1.2 MB (1195087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41ac3e5f5cfb1a12863ba7b6f47886657b0d2085eb1321805fdce6933feb2ac`  
		Last Modified: Tue, 07 Apr 2026 02:32:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a111d5accd3fdf77aed93073edf13a4dced1c34d91b2a3ae7fd4ae4c6b769f`  
		Last Modified: Tue, 07 Apr 2026 02:32:18 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d913d35a1e3bbd93d523af1cd750bfd02b5aff180a17b529be5ed5dc9b2ec14`  
		Last Modified: Tue, 07 Apr 2026 02:47:13 GMT  
		Size: 104.4 MB (104400616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5aa0b42a172cf103865e9d4a14763c5e147074cfcbebba18f97058a2209d15e`  
		Last Modified: Tue, 07 Apr 2026 02:47:11 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc122844d61a0a413d2d6fdf2f36f83201a849c858ba5ce83d9a9ff290039de5`  
		Last Modified: Tue, 07 Apr 2026 02:47:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ae5d7de6a562faba6cdcecae19ce3f51c9955bd4e6a3e28c68f25f034cc319`  
		Last Modified: Tue, 07 Apr 2026 02:47:11 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2676368ee4ae7acef8a486ef237ba816c501679df50a1696bdb02a01607e1af`  
		Last Modified: Tue, 07 Apr 2026 02:47:12 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf82b53191764b2613054f53d16a2d5379088dce703b41b7f6fff05f9dbefb8`  
		Last Modified: Tue, 07 Apr 2026 02:47:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:1b17135150d1c6808d99481f0b6ee240e75a808340c4abaf7add90a48baaaac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5863604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4b5bbf618e179d0257112b42ea49fff985563a3a4216989ab6440bf19ebce7`

```dockerfile
```

-	Layers:
	-	`sha256:a8d50087a57c00a84d4ad6bef0d0ceff960b43ab375a8ae679e96282ebcd93ea`  
		Last Modified: Tue, 07 Apr 2026 02:47:11 GMT  
		Size: 5.8 MB (5810102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4554ac7c91d2a270fa8d23616fb1b72fb17ecea44f621c1af7aac5d264b9791b`  
		Last Modified: Tue, 07 Apr 2026 02:47:11 GMT  
		Size: 53.5 KB (53502 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:41a9aff4fef5d23fdbcde2e00de65e381894127bed2a43bd1111467999e0f818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139931400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631b038c130610614b90272434799fa6d961cc95fbfdd3007b6d53359548ee30`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:36:11 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 07 Apr 2026 01:36:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:36:25 GMT
ENV GOSU_VERSION=1.19
# Tue, 07 Apr 2026 01:36:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 07 Apr 2026 01:36:31 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 07 Apr 2026 01:36:31 GMT
ENV LANG=en_US.utf8
# Tue, 07 Apr 2026 01:36:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:36:35 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 07 Apr 2026 01:36:36 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:36:36 GMT
ENV PG_MAJOR=14
# Tue, 07 Apr 2026 01:36:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 07 Apr 2026 01:36:36 GMT
ENV PG_VERSION=14.22-1.pgdg12+1
# Tue, 07 Apr 2026 02:02:16 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 07 Apr 2026 02:02:16 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 07 Apr 2026 02:02:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 07 Apr 2026 02:02:16 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 07 Apr 2026 02:02:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 07 Apr 2026 02:02:16 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 07 Apr 2026 02:02:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 02:02:16 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 07 Apr 2026 02:02:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 02:02:16 GMT
STOPSIGNAL SIGINT
# Tue, 07 Apr 2026 02:02:16 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 07 Apr 2026 02:02:16 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:dabf2c04988ff47a9777c2e6aee85c1e347525704928c5c1a366fae1fb63fea2`  
		Last Modified: Tue, 07 Apr 2026 00:58:55 GMT  
		Size: 23.9 MB (23941461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d443fbe4a0e6423a64b646ad6edea8925cce40e0bf48de3c31726b7d94c67aa2`  
		Last Modified: Tue, 07 Apr 2026 01:48:24 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e199b3b376af2fb673c06a12150c495f903db93a482c4871a4cbbbbd430ba91`  
		Last Modified: Tue, 07 Apr 2026 01:48:25 GMT  
		Size: 3.7 MB (3742705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86cdd415439032cfa38b1468aff82b8d323e2eee32e5ff9c66fe4de03055f47b`  
		Last Modified: Tue, 07 Apr 2026 01:48:25 GMT  
		Size: 1.2 MB (1216038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541d6a3d2c253cbf5cb61497b9a4167f201a6aad37617a1d4fca64dedeea9f6e`  
		Last Modified: Tue, 07 Apr 2026 01:48:25 GMT  
		Size: 8.1 MB (8066428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed970f24b64957fbd70dac7e383f3c81a9e2a6ce6100f6ec78f5f7f17a74b34`  
		Last Modified: Tue, 07 Apr 2026 01:48:26 GMT  
		Size: 1.1 MB (1067267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37de465ca5639080b00af2e88dd0d91b9afe95ad27ab9e819ceb45de74bab9ef`  
		Last Modified: Tue, 07 Apr 2026 01:48:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efa476c687fa958f8786685d75a9f198764e2ce070808fcb42986c19a62956c`  
		Last Modified: Tue, 07 Apr 2026 01:48:26 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb96ea05dd30df9c94356a4aa80808961aeca9305757881c9f341c433d33e887`  
		Last Modified: Tue, 07 Apr 2026 02:02:36 GMT  
		Size: 101.9 MB (101877218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819db3f275aad04aaeec0588896bf6d4f68a6f03832e0cbfeb30adb26b0cdb8c`  
		Last Modified: Tue, 07 Apr 2026 02:02:33 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422f48928cb575d62695627479c436ec8ac188991511560a60042315e7b05fe7`  
		Last Modified: Tue, 07 Apr 2026 02:02:33 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32cbe953ad1d227cb1b8df5d56486434fde19772151a0aeec4ee158325c474dd`  
		Last Modified: Tue, 07 Apr 2026 02:02:33 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f2b65d8807a359a23b00e6b8efd3f7301b8eb88ca2ce9855aef0bde61f20638`  
		Last Modified: Tue, 07 Apr 2026 02:02:34 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8703364da219ddce82aec2edda9b50488b86a197587105433ec5c8dc90e1799a`  
		Last Modified: Tue, 07 Apr 2026 02:02:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:08820932fc4754f65e61326118f7f464d011c814c79a3e68c5fed7a85f83dc5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5862860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350dab93dd49051e70e0aef1ab0e54d08a69337c87aae9f52258a91d1340158b`

```dockerfile
```

-	Layers:
	-	`sha256:4445f05785cf22e06457a87da114a1c2d9ecbf56748f54932959bb614bb12467`  
		Last Modified: Tue, 07 Apr 2026 02:02:33 GMT  
		Size: 5.8 MB (5809357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9aad2ae6094ce5583388789ecdfe2d7e9ec3886341380a1495ebede471f393b4`  
		Last Modified: Tue, 07 Apr 2026 02:02:33 GMT  
		Size: 53.5 KB (53503 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:e3aa5f02a1a78c7c4f2022f9cfaafb3f4174ce4d17d5bbb4e028bbd92da31730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.9 MB (149888244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ed42c003c37145759bf620f22ea2d27f8d869891d9a16b493b7a1f7bb2b2c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:43:08 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 07 Apr 2026 01:43:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:43:19 GMT
ENV GOSU_VERSION=1.19
# Tue, 07 Apr 2026 01:43:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 07 Apr 2026 01:43:24 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 07 Apr 2026 01:43:24 GMT
ENV LANG=en_US.utf8
# Tue, 07 Apr 2026 01:43:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:43:27 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 07 Apr 2026 01:43:28 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:43:28 GMT
ENV PG_MAJOR=14
# Tue, 07 Apr 2026 01:43:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 07 Apr 2026 01:43:28 GMT
ENV PG_VERSION=14.22-1.pgdg12+1
# Tue, 07 Apr 2026 01:43:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 07 Apr 2026 01:43:40 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 07 Apr 2026 01:43:40 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 07 Apr 2026 01:43:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 07 Apr 2026 01:43:40 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 07 Apr 2026 01:43:40 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 07 Apr 2026 01:43:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:43:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 07 Apr 2026 01:43:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:43:40 GMT
STOPSIGNAL SIGINT
# Tue, 07 Apr 2026 01:43:40 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 07 Apr 2026 01:43:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9836bbb193452ddd3d4d1c0ba83c5e634e28d5a66972fe6a106bbaa4fbda65be`  
		Last Modified: Tue, 07 Apr 2026 01:43:59 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9a9639a6eb4448222f6eb5fcd84b5907432c91ea2d7c9802398a7e54c7e735`  
		Last Modified: Tue, 07 Apr 2026 01:43:59 GMT  
		Size: 4.5 MB (4519555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89eee8bbea31050519756d5e64e6618422d400bc4a72241c5779a124bc8150dc`  
		Last Modified: Tue, 07 Apr 2026 01:43:59 GMT  
		Size: 1.2 MB (1203300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cbdef9cc1670dbb4b29021587cdedc3b312e70486656097a948f13cde3b85d6`  
		Last Modified: Tue, 07 Apr 2026 01:43:59 GMT  
		Size: 8.1 MB (8066467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29144514ffc8842d2edc662c91a6cfced9ec5710d4e04ec77679880108b284f`  
		Last Modified: Tue, 07 Apr 2026 01:44:00 GMT  
		Size: 1.1 MB (1109016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ac0d690c1d6d9e9a6f855b9c12e343cc915f0e48deddfdaa44e3dec02b0af4`  
		Last Modified: Tue, 07 Apr 2026 01:44:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d79399f73ac175bffaae4b4f64ab91413579e2dfba0b2fce046369b09c54a56`  
		Last Modified: Tue, 07 Apr 2026 01:44:00 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1fe7d7b2b0117e96f363488724e65e19467062f74caca9de1168a173cd7e16`  
		Last Modified: Tue, 07 Apr 2026 01:44:03 GMT  
		Size: 106.9 MB (106853463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7e4b59700aac374787b244e14978669494a36fcb5067c8cb0e80fbb33ff889`  
		Last Modified: Tue, 07 Apr 2026 01:44:01 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd555e029f0a41def7fadf8c67494b756ef1751c2d177bd3612d6e8279f1892f`  
		Last Modified: Tue, 07 Apr 2026 01:44:02 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7babb545564cc4de62778aed300e8aa03723e989564015a38d86d3a888789316`  
		Last Modified: Tue, 07 Apr 2026 01:44:02 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336eeb184c7f34e7c9bfd59a84d47bfbc6225d3656229246373f1f0f9d1eb428`  
		Last Modified: Tue, 07 Apr 2026 01:44:02 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c290f3f71ff8157eae964da0a66f65f019294c57249504557bee195f65ab1187`  
		Last Modified: Tue, 07 Apr 2026 01:44:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:44f9137b600c915a5cbb3459e9d6454eb9a47c79ed5b493bfc0acc0417ba9420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5854129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:800b55c1cea78d331fd73d6080d0b95b9b68c4da480c06ea33cb96006588cb63`

```dockerfile
```

-	Layers:
	-	`sha256:57a6c0e391c9176fce231699ad9725c627d195514c5de32d55cf8d6324d811c2`  
		Last Modified: Tue, 07 Apr 2026 01:43:59 GMT  
		Size: 5.8 MB (5800588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:194a3335fa805a476a712704c568328d3dcd96bb4d5ab42759a9f47427c6a002`  
		Last Modified: Tue, 07 Apr 2026 01:43:58 GMT  
		Size: 53.5 KB (53541 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:0439c9a6ec6037e08c59d33bba7d6df0a34ac1ef538728e77d776d1842a247ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160577956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e74bbb86738eb886bd99373af2a3c4dee86c0f563d906d1ee0e24df31648455`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:37:32 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 07 Apr 2026 01:37:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:37:44 GMT
ENV GOSU_VERSION=1.19
# Tue, 07 Apr 2026 01:37:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 07 Apr 2026 01:37:49 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 07 Apr 2026 01:37:49 GMT
ENV LANG=en_US.utf8
# Tue, 07 Apr 2026 01:37:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:37:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 07 Apr 2026 01:37:53 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:37:53 GMT
ENV PG_MAJOR=14
# Tue, 07 Apr 2026 01:37:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 07 Apr 2026 01:37:53 GMT
ENV PG_VERSION=14.22-1.pgdg12+1
# Tue, 07 Apr 2026 01:48:07 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 07 Apr 2026 01:48:07 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 07 Apr 2026 01:48:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 07 Apr 2026 01:48:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 07 Apr 2026 01:48:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 07 Apr 2026 01:48:07 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 07 Apr 2026 01:48:07 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:48:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 07 Apr 2026 01:48:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:48:07 GMT
STOPSIGNAL SIGINT
# Tue, 07 Apr 2026 01:48:07 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 07 Apr 2026 01:48:07 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2686573d3309fb5ec86398e0f20a729a351a259d4d793edf6cb41a0ef910fccb`  
		Last Modified: Tue, 07 Apr 2026 00:10:58 GMT  
		Size: 29.2 MB (29221768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed58db5311a3993e3a929d60f7205cbcfd71102191627d3820578787fdf46b7`  
		Last Modified: Tue, 07 Apr 2026 01:48:26 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab77e5400156d3a72ed3fa46f99464ed518db592533ef4d788c69cf7b2499bc5`  
		Last Modified: Tue, 07 Apr 2026 01:48:26 GMT  
		Size: 5.0 MB (4966108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132807fc6d174fd2b2f81a79fa87d98b96890deb2498f27559c2995a6520edf3`  
		Last Modified: Tue, 07 Apr 2026 01:48:26 GMT  
		Size: 1.2 MB (1218681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e171382f65bd8d360b9cb98d34aad6ed784899527ff1f1c82b7d17d70720658a`  
		Last Modified: Tue, 07 Apr 2026 01:48:26 GMT  
		Size: 8.1 MB (8066445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47189283544121d10f6325d7d11c604f5d0094220f987759ca1d8dd4d381e77`  
		Last Modified: Tue, 07 Apr 2026 01:48:27 GMT  
		Size: 1.1 MB (1137466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cda44e801e40d3a6f137313b962c323be4484b72cb20612eca67064aada51bd`  
		Last Modified: Tue, 07 Apr 2026 01:48:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d6fad1152e8375a683ed719a64a424ee88b43c0e610d6e28724b3c6fe56f83`  
		Last Modified: Tue, 07 Apr 2026 01:48:27 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1588be75e808c9b03a42d09f956cc4ca826764a0f0eccfa875078a40516bf6d9`  
		Last Modified: Tue, 07 Apr 2026 01:48:30 GMT  
		Size: 115.9 MB (115947205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195592700da281e894bf47d15bd81d3e85b4f00df2622c510eff833bf2cb521f`  
		Last Modified: Tue, 07 Apr 2026 01:48:28 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2086bbbbfc3d9528eea93d6f363c909db8a4dbccc559bfb467c4b79aa036512`  
		Last Modified: Tue, 07 Apr 2026 01:48:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e5b4d8f2ed312636632453482c04b51f95eef0aabdb821c79afb6b5871ee36`  
		Last Modified: Tue, 07 Apr 2026 01:48:28 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0dc472da5a498597a222c9c01f9ab1f0a336962888f1fbdcc732bf43678808`  
		Last Modified: Tue, 07 Apr 2026 01:48:29 GMT  
		Size: 5.8 KB (5843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199f4f9cc8802efbcc89c102becaf67504e4341be354c5daf7c2211ab04d53fb`  
		Last Modified: Tue, 07 Apr 2026 01:48:29 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:47fa0366ab045b71878a308a7d6b3f036fec9e39bc9ae76a57e11a1c58a950fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5861497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f07f5548790fec815b4ec8df5263d812b290ff333329674fb91846bbacc2bf6`

```dockerfile
```

-	Layers:
	-	`sha256:76ea22c3afb68db824221e5757cd8e27fba3bde9f93242d840c506c30edc6ab9`  
		Last Modified: Tue, 07 Apr 2026 01:48:26 GMT  
		Size: 5.8 MB (5808245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03922a58e0484a83acfbb573d3d78139d3526e0770c1fcbb52a513603a85522a`  
		Last Modified: Tue, 07 Apr 2026 01:48:25 GMT  
		Size: 53.3 KB (53252 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:b7ea34920be93246807efc3f515af7699a02b34a059c3b3974132d69af67e25b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.7 MB (150687684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4621cacb283906800a9d058a53953aa86e26ad71e908237b4aa69c92f79e6a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 03:07:51 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 17 Mar 2026 03:08:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:09:00 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 03:09:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 03:09:29 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 17 Mar 2026 03:09:29 GMT
ENV LANG=en_US.utf8
# Tue, 17 Mar 2026 03:09:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:09:50 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 03:09:52 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Mar 2026 03:09:52 GMT
ENV PG_MAJOR=14
# Tue, 17 Mar 2026 03:09:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 17 Mar 2026 03:09:52 GMT
ENV PG_VERSION=14.22-1.pgdg12+1
# Tue, 17 Mar 2026 08:55:24 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 17 Mar 2026 08:55:27 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 17 Mar 2026 08:55:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 17 Mar 2026 08:55:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 17 Mar 2026 08:55:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 17 Mar 2026 08:55:30 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 17 Mar 2026 08:55:32 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 08:55:34 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 17 Mar 2026 08:55:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 08:55:34 GMT
STOPSIGNAL SIGINT
# Tue, 17 Mar 2026 08:55:34 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 17 Mar 2026 08:55:34 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:036b690c37cf2dc49974818e200658ce29b93c4d917171332d28ada375e6f68b`  
		Last Modified: Mon, 16 Mar 2026 21:51:40 GMT  
		Size: 28.5 MB (28526147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a44e02bd38b2cc6c45fb11d2014eb5481ef4b720cecae6fbfc8611666d8dec`  
		Last Modified: Tue, 17 Mar 2026 04:22:53 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99aa438604d0ad0a20b10162a536346646d6b9a27218eb304d3f2267c991d8e8`  
		Last Modified: Tue, 17 Mar 2026 04:22:59 GMT  
		Size: 4.5 MB (4475221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a2e3cf1220f5308b864548a8a37453fe15abaee48fa3088f1542815d764ee0`  
		Last Modified: Tue, 17 Mar 2026 04:22:53 GMT  
		Size: 1.2 MB (1159254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca784a5c447b79e03e42be65fcb7373ddedfe282015193ccf549a049e2b67fd`  
		Last Modified: Tue, 17 Mar 2026 04:22:54 GMT  
		Size: 8.1 MB (8066597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b287156e480b380b14c9af643becc91c0377d38ad1e3038d1d7abac16700b5eb`  
		Last Modified: Tue, 17 Mar 2026 04:22:54 GMT  
		Size: 1.2 MB (1182913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db23322e1e34a87af7dba3e8e7b32da589330c45c99d0da07866bad91af37c71`  
		Last Modified: Tue, 17 Mar 2026 04:22:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0042c702082bbdf506e4e14c7cc66ac0f2e15879f880896d9e567a91d44959d8`  
		Last Modified: Tue, 17 Mar 2026 04:22:56 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101d3a5765c89e7a0785b98435e23e84e648bdd8bd79759ffa35d16a5f0e9ea4`  
		Last Modified: Tue, 17 Mar 2026 08:57:38 GMT  
		Size: 107.3 MB (107257264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0e323adeb1ff369d0deebf0d61e83412334b2350ae2909cca34cf164a06934`  
		Last Modified: Tue, 17 Mar 2026 08:57:28 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03330ed3cf349a618ac8861fdff7b62caf828ea3d8149311aec6d6f6962d077a`  
		Last Modified: Tue, 17 Mar 2026 08:57:27 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8058f3c68e6378a0587129ec61a40cdd43f03b95d20c1fb61480482423d699`  
		Last Modified: Tue, 17 Mar 2026 08:57:27 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddfc2f2d18b29002cb2b28d0fab8ee0013c5c3e44e259cf3287b0d49cda6331`  
		Last Modified: Tue, 17 Mar 2026 08:57:28 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c6ab2994d98aa59049b29707f778f995dce9b0c2371ac3cc338cf53812b834`  
		Last Modified: Tue, 17 Mar 2026 08:57:29 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:b9ea68b40c60bf67c8696c8c02ec3edaf2788d6d7768f4d39f2529e282794124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 KB (53162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:671aa71d8537298e255a856873f46a16639585deeda3c78084eee0863c578a46`

```dockerfile
```

-	Layers:
	-	`sha256:112d3d43358a880a833ecf082fc3c105e9dde3a252b94cf5b7ccba9465152d17`  
		Last Modified: Tue, 17 Mar 2026 08:57:27 GMT  
		Size: 53.2 KB (53162 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:e2ac91a82d4da10382b0c7a781fc2a3da7119615e89892093ce19fb93d76d30b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.6 MB (164565688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e1c8ea05ef848d31021920a21f7435da4a09bbd40793a4b1983bef90d866e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 04:01:02 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 07 Apr 2026 04:01:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:01:34 GMT
ENV GOSU_VERSION=1.19
# Tue, 07 Apr 2026 04:01:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 07 Apr 2026 04:01:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 07 Apr 2026 04:01:43 GMT
ENV LANG=en_US.utf8
# Tue, 07 Apr 2026 04:01:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:01:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 07 Apr 2026 04:01:53 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 04:01:53 GMT
ENV PG_MAJOR=14
# Tue, 07 Apr 2026 04:01:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 07 Apr 2026 04:01:53 GMT
ENV PG_VERSION=14.22-1.pgdg12+1
# Tue, 07 Apr 2026 04:08:34 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 07 Apr 2026 04:08:35 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 07 Apr 2026 04:08:35 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 07 Apr 2026 04:08:35 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 07 Apr 2026 04:08:36 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 07 Apr 2026 04:08:36 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 07 Apr 2026 04:08:36 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 04:08:36 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 07 Apr 2026 04:08:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 04:08:36 GMT
STOPSIGNAL SIGINT
# Tue, 07 Apr 2026 04:08:36 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 07 Apr 2026 04:08:36 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b1c56220ca211bc9d02f1ed5c589465809676b6ab2cef705f1e2fb8e9726de76`  
		Last Modified: Tue, 07 Apr 2026 00:09:42 GMT  
		Size: 32.1 MB (32078464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c73a4e80f8eee9e890cb47bedd35d02c67ef5bcca2b473c6d3e00a80965b06a`  
		Last Modified: Tue, 07 Apr 2026 04:04:12 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7947f119f83a299b47ca573148739e01949d18cbaa9318e7ab4a40e85e5823df`  
		Last Modified: Tue, 07 Apr 2026 04:04:13 GMT  
		Size: 5.4 MB (5368665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f2363b8d0c3c8477a5c830c8f04da66b6b2dbe1de9983fe4475a83363c62b90`  
		Last Modified: Tue, 07 Apr 2026 04:04:13 GMT  
		Size: 1.2 MB (1208247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73441d3fd6b801869bfe2128fece0f8cfd3dae11351c3d17ba334f6a60758933`  
		Last Modified: Tue, 07 Apr 2026 04:04:13 GMT  
		Size: 8.1 MB (8066577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b825f5e783521a55f9a2725ca3ae6863c9ebc88d6eeb23db6ad9f4a50720cb7f`  
		Last Modified: Tue, 07 Apr 2026 04:04:14 GMT  
		Size: 1.3 MB (1283671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255852130442a8dd66f03e76d6c53fb783681b9f0b0f0deb8976c69d771ebc43`  
		Last Modified: Tue, 07 Apr 2026 04:04:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b958c25dd0ceaa8626e0e80c7b5ef496a8edd59a35e667fc15c63e5053d77b`  
		Last Modified: Tue, 07 Apr 2026 04:04:14 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed717f399795e529d58b5669266d760bc2bbf5c4c361956fed52b9e94e82ae44`  
		Last Modified: Tue, 07 Apr 2026 04:09:24 GMT  
		Size: 116.5 MB (116539784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab741327aa739024b9398c6cdcb23fb5a5ac392d6f9179ca4d0416af1de78e46`  
		Last Modified: Tue, 07 Apr 2026 04:09:20 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1650a0ea26ac8f44c756f6d6c390fc51ac9c63f33803768375e455c503eb3b0`  
		Last Modified: Tue, 07 Apr 2026 04:09:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47159453c1a2dcc1bab02a3f8b37d755a2d1c7396dbc551a88ee433631173da2`  
		Last Modified: Tue, 07 Apr 2026 04:09:21 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da82e4fbe238c5975456452e8fc43d86dd956c36b1b895de80679cc819e4395e`  
		Last Modified: Tue, 07 Apr 2026 04:09:22 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d54afd60d602c4a6286d16fd9c564599fbcbf9deafafa6fc5386416e9812a9`  
		Last Modified: Tue, 07 Apr 2026 04:09:22 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:fff7f661d0c22ab8f87c8d73fb39f7668756344c30cd5e0a2e5830bb0a033582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5854987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:928d01a3f8f180ceadac285c9ae4b1a4b56a14317b4947152a16198b9fbc310e`

```dockerfile
```

-	Layers:
	-	`sha256:f50bc670da73640e1e99fa89e3e5d25cc0e04a9ab3e517f591298d6ceeaa4ec0`  
		Last Modified: Tue, 07 Apr 2026 04:09:21 GMT  
		Size: 5.8 MB (5801638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76150d653c9fe54b8db23ca600bb24ba84ceddbb3acc7c76ddbdd10fcdcbc5eb`  
		Last Modified: Tue, 07 Apr 2026 04:09:20 GMT  
		Size: 53.3 KB (53349 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:7bc700cad2cb5ff68dd2031e9129ee4c78ebf3b542f3ca89558714125aa12f4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (161024547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbaad2c3cef94ea6d07a41255bf0e424dd540c54705c40d92057ca7cf5bb72e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:29:03 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 07 Apr 2026 02:29:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:29:15 GMT
ENV GOSU_VERSION=1.19
# Tue, 07 Apr 2026 02:29:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 07 Apr 2026 02:29:20 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 07 Apr 2026 02:29:20 GMT
ENV LANG=en_US.utf8
# Tue, 07 Apr 2026 02:29:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:29:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 07 Apr 2026 02:29:23 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:29:23 GMT
ENV PG_MAJOR=14
# Tue, 07 Apr 2026 02:29:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 07 Apr 2026 02:29:23 GMT
ENV PG_VERSION=14.22-1.pgdg12+1
# Tue, 07 Apr 2026 03:08:47 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 07 Apr 2026 03:08:47 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 07 Apr 2026 03:08:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 07 Apr 2026 03:08:47 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 07 Apr 2026 03:08:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 07 Apr 2026 03:08:47 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 07 Apr 2026 03:08:47 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 03:08:47 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 07 Apr 2026 03:08:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 03:08:47 GMT
STOPSIGNAL SIGINT
# Tue, 07 Apr 2026 03:08:47 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 07 Apr 2026 03:08:47 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236fd51a3479082dfc3f0b4b4e81de73cb849cdbea17a0216df6e8cfc6329d24`  
		Last Modified: Tue, 07 Apr 2026 02:43:04 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c29f625556d8187921bf9418aa7c48feb65a32b433fa3c0583273c38e7f722`  
		Last Modified: Tue, 07 Apr 2026 02:43:05 GMT  
		Size: 4.4 MB (4391221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a23794f8883744351d0d51b7366c179b04e11a587428e5503b9f2e2f4e8e218`  
		Last Modified: Tue, 07 Apr 2026 02:43:04 GMT  
		Size: 1.2 MB (1222826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca5b59ba0c5dcc94492315b685d06b1b8df0dd4abd7a257f792574a446671c3`  
		Last Modified: Tue, 07 Apr 2026 02:43:05 GMT  
		Size: 8.1 MB (8120743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f81d84e1dc5d16f4f84c482df7b68f549a7bc8f30b75873efe7d872211bac9`  
		Last Modified: Tue, 07 Apr 2026 02:43:05 GMT  
		Size: 1.1 MB (1097062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4d60dbaf0bf5edc6c3ab87b9e7bc6aa438bee7d4ae20264862047f8a222199`  
		Last Modified: Tue, 07 Apr 2026 02:43:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fd67408ad4a5c1eb55e5ced9c4c5252a10fd8af6165925ae7dbf744085a51f`  
		Last Modified: Tue, 07 Apr 2026 02:43:06 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e615684298758ef13931078de86ffc7f52ff3c77c4a4953d68e71b8113968132`  
		Last Modified: Tue, 07 Apr 2026 03:09:20 GMT  
		Size: 119.3 MB (119280778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0e05604744f1681c74ed02274781bcdedbec71ecea987ac1570eee6937eb33`  
		Last Modified: Tue, 07 Apr 2026 03:09:17 GMT  
		Size: 9.5 KB (9536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81abd895f3d6e798d9634f60fa211354f10ecfd4bd8aed511ed3508a11b6eb13`  
		Last Modified: Tue, 07 Apr 2026 03:09:17 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616c7a49cae5da270ba441457494e19520308f250a76cd378ab4be281baec973`  
		Last Modified: Tue, 07 Apr 2026 03:09:17 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64de3d92a02e2fab8db554c20797952677a2210eee0507bd9d1e5d2e5dcc75f7`  
		Last Modified: Tue, 07 Apr 2026 03:09:18 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cae5502ebbe1be8a68945943de70084f5a8f5950353eff06957af22a8fdd53c`  
		Last Modified: Tue, 07 Apr 2026 03:09:18 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:84cf3791befc8bc040c0d13d075cd60a91e52bffe861ed29209ec7d690e7605d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5858017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6487e761bb063d0033059c06b027aa3e42f0e865c8704594a3f5f728b971b7a9`

```dockerfile
```

-	Layers:
	-	`sha256:330de7e0bc18c57aadcec5a4d309a2101afbf83de2fe823b6cc827999708ac89`  
		Last Modified: Tue, 07 Apr 2026 03:09:17 GMT  
		Size: 5.8 MB (5804721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:012ac5e90a8a744e2a06f8dfc9db39695b3b533191ab11d69ece6bdb4fe5acb5`  
		Last Modified: Tue, 07 Apr 2026 03:09:17 GMT  
		Size: 53.3 KB (53296 bytes)  
		MIME: application/vnd.in-toto+json
