## `postgres:14-bookworm`

```console
$ docker pull postgres@sha256:72e51f193817f23d4ad880a30d7bf018bcafb5e15d76aa4a4ef22afb71f1aa19
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
$ docker pull postgres@sha256:742d60f7a2242e32f2a9226e04baa32fe0bf8408760b0906041f3d9b64124eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.9 MB (151875541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0dd595b45b7e42edfed17ae34c4f2d71515f2d486127b057a3e2e628bcf648`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:34:46 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 16 Mar 2026 22:34:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:34:57 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 22:34:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 22:35:02 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 16 Mar 2026 22:35:02 GMT
ENV LANG=en_US.utf8
# Mon, 16 Mar 2026 22:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:35:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 16 Mar 2026 22:35:05 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:35:05 GMT
ENV PG_MAJOR=14
# Mon, 16 Mar 2026 22:35:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Mon, 16 Mar 2026 22:35:05 GMT
ENV PG_VERSION=14.22-1.pgdg12+1
# Mon, 16 Mar 2026 22:35:18 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 16 Mar 2026 22:35:18 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 16 Mar 2026 22:35:18 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 16 Mar 2026 22:35:18 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 16 Mar 2026 22:35:18 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 16 Mar 2026 22:35:18 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 16 Mar 2026 22:35:18 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:35:18 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 16 Mar 2026 22:35:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:35:18 GMT
STOPSIGNAL SIGINT
# Mon, 16 Mar 2026 22:35:18 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 16 Mar 2026 22:35:18 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250bfef6493e378fd51d49015a1e1c5732ffe2376ed3d92213515e5eb72b2c5e`  
		Last Modified: Mon, 16 Mar 2026 22:35:37 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ec4d2096796245c35b4768a3d7ea2c4f46467209eb76b433661aaa7275cb57`  
		Last Modified: Mon, 16 Mar 2026 22:35:38 GMT  
		Size: 4.5 MB (4534246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51dd94e5ef4a94f0924591c9519fcc676fba19680d808e89a0e4998a6253a92`  
		Last Modified: Mon, 16 Mar 2026 22:35:38 GMT  
		Size: 1.2 MB (1249529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c76cd72e76fbc349d3d8165dbde14b5e938c968c1aaeda12aaf9adb234af0bc`  
		Last Modified: Mon, 16 Mar 2026 22:35:38 GMT  
		Size: 8.1 MB (8066488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8cc46edc2462a1fcdc074b5bd372ea7ff7376124d43bbeee26b4f342b6d7d0`  
		Last Modified: Mon, 16 Mar 2026 22:35:39 GMT  
		Size: 1.2 MB (1196429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2882211af12951de9fa3a16af9f90a83a2f044c8081d4c1d321542cee0a7fe95`  
		Last Modified: Mon, 16 Mar 2026 22:35:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a562215c6a3eaed198eb8f4bfff7df6d940e0e8e8544ef9a29ffbab6b1ae8c4`  
		Last Modified: Mon, 16 Mar 2026 22:35:39 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930d3a23d1ee1ce076ab86a42fb0a68ced1e693a2bb0c3204505e4c326b5f05a`  
		Last Modified: Mon, 16 Mar 2026 22:35:42 GMT  
		Size: 108.6 MB (108572354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4245854325ec4a55b4aecab7c244199dbd95df12f7e66b3d6b3a6cbf099b13`  
		Last Modified: Mon, 16 Mar 2026 22:35:40 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0ad942a7680edd10545518e8b4739f7e34b2d3087ce36e1607c309c383f27e`  
		Last Modified: Mon, 16 Mar 2026 22:35:40 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311d1972ab9580a42eaaec937691816e750cc6c05157e8bb3bad566e388e8e9e`  
		Last Modified: Mon, 16 Mar 2026 22:35:40 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e0e81c855702823c768c3f0f03141c2d08db907cd1db91eb14c1c28cf18b24`  
		Last Modified: Mon, 16 Mar 2026 22:35:41 GMT  
		Size: 5.8 KB (5835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee68a124636c29ee28134e7e3e9cf7cc98f29f0955293318ba1f1fe6ff15a17`  
		Last Modified: Mon, 16 Mar 2026 22:35:41 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:5ea5f5ea37c04fa91ae19057776bb69db16a88e6296ac5218472dcb34ab4eb37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5847573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d34d7f093dc6d7aa1c8751038c04b84592cfabbc6deb6fa448abd5bee2d598`

```dockerfile
```

-	Layers:
	-	`sha256:8e774b859d641be5d14896152aff15ed8d422b3c7a384cfd0bcc91f4e058b6ce`  
		Last Modified: Mon, 16 Mar 2026 22:35:38 GMT  
		Size: 5.8 MB (5794277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40b46331290078605e7753076e35ab6b36a863b5b4632f3b96c82ef9eb820bfe`  
		Last Modified: Mon, 16 Mar 2026 22:35:37 GMT  
		Size: 53.3 KB (53296 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:1434defdd27596524bb12491e4891ff212c370537864d81872c86f4f13eeb6cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144820153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407e6cf0e29fea492fbf7337609d95f9890fbeab88da280b86629344958cd122`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:45:26 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 16 Mar 2026 22:45:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:45:43 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 22:45:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 22:45:51 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 16 Mar 2026 22:45:51 GMT
ENV LANG=en_US.utf8
# Mon, 16 Mar 2026 22:45:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:45:56 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 16 Mar 2026 22:45:57 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:45:57 GMT
ENV PG_MAJOR=14
# Mon, 16 Mar 2026 22:45:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Mon, 16 Mar 2026 22:45:57 GMT
ENV PG_VERSION=14.22-1.pgdg12+1
# Mon, 16 Mar 2026 23:16:41 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 16 Mar 2026 23:16:42 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 16 Mar 2026 23:16:42 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 16 Mar 2026 23:16:42 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 16 Mar 2026 23:16:42 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 16 Mar 2026 23:16:42 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 16 Mar 2026 23:16:42 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:16:42 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 16 Mar 2026 23:16:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:16:42 GMT
STOPSIGNAL SIGINT
# Mon, 16 Mar 2026 23:16:42 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 16 Mar 2026 23:16:42 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3f1e11847ee1bf3b5b4789698fd7943a2f92f317682fd98071438c59f096b12b`  
		Last Modified: Mon, 16 Mar 2026 21:51:51 GMT  
		Size: 25.8 MB (25765607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e9560b5d72a73e4a07f7b29cfc9eca5433cd4603500f59064fa2cadd8167ef`  
		Last Modified: Mon, 16 Mar 2026 23:02:03 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2185e0aed9202cc5bbf6d43eace71b445bb6f6d8ee2e2d1d85697b423d1b635e`  
		Last Modified: Mon, 16 Mar 2026 23:02:04 GMT  
		Size: 4.2 MB (4151249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f98318c3824493d367fd6f4fc99ea83deb2e348297bafa824da25041da0e4d`  
		Last Modified: Mon, 16 Mar 2026 23:02:04 GMT  
		Size: 1.2 MB (1220091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090ea24559fb42b20544786ae879b75b2d0508a4a60f1bf992ca52e252f8c0f8`  
		Last Modified: Mon, 16 Mar 2026 23:02:04 GMT  
		Size: 8.1 MB (8066550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a11af55df5d095f407d9dd58188460db1ab7e9d15503eb8f584c9e893a0014`  
		Last Modified: Mon, 16 Mar 2026 23:02:05 GMT  
		Size: 1.2 MB (1195061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40da321e6ec3c632d332283d17505b8ea5ed019e7181d038dba198526d173abf`  
		Last Modified: Mon, 16 Mar 2026 23:02:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1f6683aca027204c6df1501ccfdb08fe296060e3c88fa291e5e7d255fe68b5`  
		Last Modified: Mon, 16 Mar 2026 23:02:05 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b451f504ebd33f9b05acc3a4af7d52c7ad98491e24dbf74bf71987f1f4fef982`  
		Last Modified: Mon, 16 Mar 2026 23:17:02 GMT  
		Size: 104.4 MB (104401318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f348b5ba4c222abed739102c25fef503202e66e34dc0efd8d69636d1c48d084c`  
		Last Modified: Mon, 16 Mar 2026 23:16:59 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9c480cb9d0d0363856e962f72e2f23dd71d12b70427ea7f63ff9d20b1b966e`  
		Last Modified: Mon, 16 Mar 2026 23:16:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fe66d21dd8efc219c50609022c8bea086b1d014df5e3c3bf50083996e5d3ae`  
		Last Modified: Mon, 16 Mar 2026 23:16:59 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa0f9aa210f04cb8e229a0923b582971452956df36fb21803751641a101bf32`  
		Last Modified: Mon, 16 Mar 2026 23:17:00 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16de8693ff9aa48e47bba9bb3a03d56a37a6636167d73e86845dcec0942f927c`  
		Last Modified: Mon, 16 Mar 2026 23:17:00 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:250713c72e31d34e6ac6e4bc66c44607cb64e4b14fbe7b615cfb95be9e72de12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5863605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25718867c335e77d86133465f48208354e99f4182299b534b2557ccfe920e2bd`

```dockerfile
```

-	Layers:
	-	`sha256:297ad276800673196f9d1d3a7eef81070e23c3dfccb3b7f3586aca6f1e60bb34`  
		Last Modified: Mon, 16 Mar 2026 23:16:59 GMT  
		Size: 5.8 MB (5810102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3b0c56e41b15a44a25c81118b4e28374fc78373132a7044f6bb36985575e34b`  
		Last Modified: Mon, 16 Mar 2026 23:16:59 GMT  
		Size: 53.5 KB (53503 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:f365e7d8c451783014efc471cd25a34e29fe308bac881cf97f926b0e4527587a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139932516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c997ce1815bc8a861fde9799538232ec33cf3e4ba85c3e323b5aa580749f5b30`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:08:03 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 16 Mar 2026 23:08:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:08:16 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 23:08:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 23:08:22 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 16 Mar 2026 23:08:22 GMT
ENV LANG=en_US.utf8
# Mon, 16 Mar 2026 23:08:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:08:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 16 Mar 2026 23:08:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 23:08:26 GMT
ENV PG_MAJOR=14
# Mon, 16 Mar 2026 23:08:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Mon, 16 Mar 2026 23:08:26 GMT
ENV PG_VERSION=14.22-1.pgdg12+1
# Mon, 16 Mar 2026 23:22:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 16 Mar 2026 23:22:13 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 16 Mar 2026 23:22:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 16 Mar 2026 23:22:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 16 Mar 2026 23:22:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 16 Mar 2026 23:22:13 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 16 Mar 2026 23:22:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:22:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 16 Mar 2026 23:22:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:22:13 GMT
STOPSIGNAL SIGINT
# Mon, 16 Mar 2026 23:22:13 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 16 Mar 2026 23:22:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5713f371de38da178bc245d32c8f790731b17dcb234bd312ce549adb262d2531`  
		Last Modified: Mon, 16 Mar 2026 23:22:30 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58780b4a861cc8756133d665eaa961ca78f01b57c6c978104ed694f932dede99`  
		Last Modified: Mon, 16 Mar 2026 23:22:30 GMT  
		Size: 3.7 MB (3742688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920242fca18ff08109fab3ff2dd1291ad5acacb258c8e031493f2a7f740d50af`  
		Last Modified: Mon, 16 Mar 2026 23:22:30 GMT  
		Size: 1.2 MB (1215995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ad0f86e70db4035f9cc8e8273e1a14b59c0cc6f028cae5f82b4ad3f03a0212`  
		Last Modified: Mon, 16 Mar 2026 23:22:31 GMT  
		Size: 8.1 MB (8066427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49fbefe14a6cd2266599a8995db32d079d54fee506e39b99db5775b7b4b636a8`  
		Last Modified: Mon, 16 Mar 2026 23:22:31 GMT  
		Size: 1.1 MB (1067287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738f5994bbbf05648fc7d0b103a4f98553e313f819ce61da728ed8e111f52b27`  
		Last Modified: Mon, 16 Mar 2026 23:22:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf024a77203af4fa11b3b5277499e8d3b04af53c183e01c7403726a8bfc7ffd`  
		Last Modified: Mon, 16 Mar 2026 23:22:32 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f58f0dc3e512e3dbe6dfbb8c9f119efe4f5d5c889ec49ce7beb4683f2ecae73`  
		Last Modified: Mon, 16 Mar 2026 23:22:35 GMT  
		Size: 101.9 MB (101878501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4d7679aea463d9db31dce12de7473dd136adea89ed310a0412a4b86b28451e`  
		Last Modified: Mon, 16 Mar 2026 23:22:33 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af822c883d38039d285696457a6f331484f969337ee6181202686b7b1c3f3eb9`  
		Last Modified: Mon, 16 Mar 2026 23:22:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39fdfc51e2e14f044e8df49ceaa52ea58bf72010bb559b1190f3741e3afec62`  
		Last Modified: Mon, 16 Mar 2026 23:22:33 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea696c7396e6d66efa20b0904b924b41cd1dec4d6439af7cd5140c7fe3f0142`  
		Last Modified: Mon, 16 Mar 2026 23:22:34 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880b24b1f762fd1a359a4ade357bfe75abdb3063fca48b5c99c6f294f816b417`  
		Last Modified: Mon, 16 Mar 2026 23:22:34 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:2d1cf143ab5b986d8f5e010734eaf6e0ede417b0512ade90dc14baf809cffba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5862860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bed1a75a88e810fed44206520956c7a66d6175fd53d6cfa2e9a67828bb03f4f`

```dockerfile
```

-	Layers:
	-	`sha256:8a4abe723bc84a2cc175d0b5684515b1bf42c57234a2e8f4659578e162a93612`  
		Last Modified: Mon, 16 Mar 2026 23:22:30 GMT  
		Size: 5.8 MB (5809357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34a865a2bc52cbe5af53a406a7852f673c4770360f89e6c5f2cf1d885b80e0bf`  
		Last Modified: Mon, 16 Mar 2026 23:22:30 GMT  
		Size: 53.5 KB (53503 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:6ba8965629fcc349956dc3c0f5a877d7919d4fe3eaa7c90b35a45e816542d3fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.9 MB (149888250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed713dce0a6971afddbe607455625122f2b1be0e835976619921a4a5765c4435`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:35:32 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 16 Mar 2026 22:35:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:35:45 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 22:35:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 22:35:50 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 16 Mar 2026 22:35:50 GMT
ENV LANG=en_US.utf8
# Mon, 16 Mar 2026 22:35:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:35:53 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 16 Mar 2026 22:35:54 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:35:54 GMT
ENV PG_MAJOR=14
# Mon, 16 Mar 2026 22:35:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Mon, 16 Mar 2026 22:35:54 GMT
ENV PG_VERSION=14.22-1.pgdg12+1
# Mon, 16 Mar 2026 22:36:47 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 16 Mar 2026 22:36:47 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 16 Mar 2026 22:36:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 16 Mar 2026 22:36:47 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 16 Mar 2026 22:36:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 16 Mar 2026 22:36:47 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 16 Mar 2026 22:36:47 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:36:48 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 16 Mar 2026 22:36:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:36:48 GMT
STOPSIGNAL SIGINT
# Mon, 16 Mar 2026 22:36:48 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 16 Mar 2026 22:36:48 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d13c93a35a46936f4a9a091f67572517525b62f671d98d854a55264b984d9eb`  
		Last Modified: Mon, 16 Mar 2026 22:36:25 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a619633e242b0ebce0c43a5d8bad7ee6b79b4233e6e66a66da3b677424196b37`  
		Last Modified: Mon, 16 Mar 2026 22:36:25 GMT  
		Size: 4.5 MB (4519578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89ea63ba55328b3bb855f2548d7b577f235935ab11da04f50c6b730f497ec0c`  
		Last Modified: Mon, 16 Mar 2026 22:36:25 GMT  
		Size: 1.2 MB (1203345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829882cb4623961dfad662f23db3eddcf6947607e1d63bd2fa01f90aa0705b5d`  
		Last Modified: Mon, 16 Mar 2026 22:36:26 GMT  
		Size: 8.1 MB (8066489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b0822a7993e8983f470948dbc7fac93aa3934497f48136746c5e61eb14acc9`  
		Last Modified: Mon, 16 Mar 2026 22:36:26 GMT  
		Size: 1.1 MB (1109020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b320a5a0160749b7254db39c6f935cff2922e0995995f8520b038393e7693d44`  
		Last Modified: Mon, 16 Mar 2026 22:36:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbfca3af271c05b2f2353478e13094915312dc5809f95e05d63b954ed2750c1`  
		Last Modified: Mon, 16 Mar 2026 22:36:27 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33072536fda5ce4ff39d5a22f9aba242193244c5df15fa316a841c2389a41365`  
		Last Modified: Mon, 16 Mar 2026 22:37:08 GMT  
		Size: 106.9 MB (106853487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2116a6378862365a137188e8eedbc2550ec36694a4cd5f0d251771f5ac5a0b`  
		Last Modified: Mon, 16 Mar 2026 22:37:06 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d433537a0812a2a7c7afe92379d3e923ce268a377b776db7b5706eb580817a23`  
		Last Modified: Mon, 16 Mar 2026 22:37:06 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6826faeb57ecf89cec8f5899887c95d23ace9bd31bb3cda355d91f3ff5f60d4`  
		Last Modified: Mon, 16 Mar 2026 22:37:06 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899d50e0c800bb3b74d3ee8415cef7e97a5116b2593af666a1951f1d3e7a4b59`  
		Last Modified: Mon, 16 Mar 2026 22:37:07 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58c63c29eb2bd0d0d25b2214ecd71f8efaa1095227dfe428a47bbd4d8a6f93d`  
		Last Modified: Mon, 16 Mar 2026 22:37:07 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:e15fe608966a6a1b3dd9c832763d435b61506f8648604b68f7bbf4257525bea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5854129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1977caa8fc2809cbad5f9a9e2e3c72d52961c70babff8b94e883cc128e8c6b32`

```dockerfile
```

-	Layers:
	-	`sha256:5a6e0139e6b0dca62d4fa7961b4283b711285fff4326654a02b7f62eaa129c56`  
		Last Modified: Mon, 16 Mar 2026 22:37:06 GMT  
		Size: 5.8 MB (5800588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b46888969613a8ffd84775b6ff92abf8cc40813a5243620d81626904dd8ed17f`  
		Last Modified: Mon, 16 Mar 2026 22:37:05 GMT  
		Size: 53.5 KB (53541 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:b9b1e006e31f5b5c72793a419f05097ef9963944f4b181247a1327a84f875228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160566949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d49ebcc7d36d2c75810c1bb52e257b01d993ddda27ff7c01a01cd7995f0ee9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:33:07 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 16 Mar 2026 22:33:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:33:19 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 22:33:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 22:33:24 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 16 Mar 2026 22:33:24 GMT
ENV LANG=en_US.utf8
# Mon, 16 Mar 2026 22:33:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:33:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 16 Mar 2026 22:33:28 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:33:28 GMT
ENV PG_MAJOR=14
# Mon, 16 Mar 2026 22:33:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Mon, 16 Mar 2026 22:33:28 GMT
ENV PG_VERSION=14.22-1.pgdg12+1
# Mon, 16 Mar 2026 22:43:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 16 Mar 2026 22:43:59 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 16 Mar 2026 22:43:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 16 Mar 2026 22:43:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 16 Mar 2026 22:43:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 16 Mar 2026 22:43:59 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 16 Mar 2026 22:43:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:43:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 16 Mar 2026 22:43:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:43:59 GMT
STOPSIGNAL SIGINT
# Mon, 16 Mar 2026 22:43:59 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 16 Mar 2026 22:43:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f649af5ed0883ac0b5027f768cbd9576b7bc8c76adac1eddeb4035e88b9258fe`  
		Last Modified: Mon, 16 Mar 2026 21:53:10 GMT  
		Size: 29.2 MB (29221681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8225ec30eea6517fb559e4978aa23fd4bbef5304b16dcc18c6b35fb8baf640`  
		Last Modified: Mon, 16 Mar 2026 22:44:18 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8f80d3bdd4812c6dc8def43875cb4706dbfecfeeb47fdcf5d3429223eb5ed4`  
		Last Modified: Mon, 16 Mar 2026 22:44:18 GMT  
		Size: 5.0 MB (4966095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3874e4ddfcdb0dce8595fe69e7e6664c3490a29f5d782c19cf2a6b2ba650fe`  
		Last Modified: Mon, 16 Mar 2026 22:44:18 GMT  
		Size: 1.2 MB (1218631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d2bfed7954f756ad95d26bf588ea790215b455b844b9bf52d11e2606c4800b`  
		Last Modified: Mon, 16 Mar 2026 22:44:19 GMT  
		Size: 8.1 MB (8066434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821eb758fa66228796f17e50d7245ec71924c43f8baaf3af6840531a169bd801`  
		Last Modified: Mon, 16 Mar 2026 22:44:19 GMT  
		Size: 1.1 MB (1137475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07fce456b9bd14a1128553d4d2f6f0f43aaa219c5ef0fb6e36ee2ca0e9d2d0d`  
		Last Modified: Mon, 16 Mar 2026 22:44:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa378c0c50317875f698e543c1419aba0ce0e074683348025f007c78a0a1296`  
		Last Modified: Mon, 16 Mar 2026 22:44:20 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0555c8722d5eb1e780c9f3ab67be9a5460f5e8b6a599ff733a69d95b29c17d8`  
		Last Modified: Mon, 16 Mar 2026 22:44:25 GMT  
		Size: 115.9 MB (115936360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4f374303385aeb7699bb12b1b00da54719151cbf499ad035f6c9ffc30c26ef`  
		Last Modified: Mon, 16 Mar 2026 22:44:21 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66dcad8ece5160fb203e93ebc40a45d755e70e1c82cde0f3720a32c08c01d421`  
		Last Modified: Mon, 16 Mar 2026 22:44:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42587821cdd04876a1308a9de81c4dbc0ab055c52fc35975b40ce0bbccbb518b`  
		Last Modified: Mon, 16 Mar 2026 22:44:21 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b39332a17a36ddeeb5b61693694e388c17a10d8e6ee356fcacd16434e25c6a`  
		Last Modified: Mon, 16 Mar 2026 22:44:22 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377dce4317cee51813b664b7e5290b3d552e92188acfe2e3485e947395cbd434`  
		Last Modified: Mon, 16 Mar 2026 22:44:22 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:ea91c04c59c338b9af17357ff9e844744c9cc5d7ecb904b1ad8e9534bf94bee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5861497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:018509835fe88717e069f212fcf3ecfff83f31d8b291f443687c53941c0497c7`

```dockerfile
```

-	Layers:
	-	`sha256:144a18817817bc6a039cea555e0e4ca5571ecfeac83c3cd71d98a6474c0b950c`  
		Last Modified: Mon, 16 Mar 2026 22:44:18 GMT  
		Size: 5.8 MB (5808245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c18d5f428c9438d8e3c77a80cdc2f20e1b36e9d97113c4eb805215bf80ce5fa`  
		Last Modified: Mon, 16 Mar 2026 22:44:18 GMT  
		Size: 53.3 KB (53252 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:de86130a738f7afcaaee7e7b4f7d966af2ee08fdd697eb2d9fb2759c0b727eab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.7 MB (150683653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:044d9ea3b58448ca312befb9e0741dfd19cb727b7530be705a6db72188b085a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 23:43:05 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 24 Feb 2026 23:43:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 23:44:15 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 23:44:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 23:44:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 24 Feb 2026 23:44:43 GMT
ENV LANG=en_US.utf8
# Tue, 24 Feb 2026 23:45:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 23:45:04 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 24 Feb 2026 23:45:07 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Feb 2026 23:45:07 GMT
ENV PG_MAJOR=14
# Tue, 24 Feb 2026 23:45:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 24 Feb 2026 23:45:07 GMT
ENV PG_VERSION=14.22-1.pgdg12+1
# Fri, 27 Feb 2026 01:04:13 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 27 Feb 2026 01:04:15 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 27 Feb 2026 01:04:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 27 Feb 2026 01:04:16 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 27 Feb 2026 01:04:18 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 27 Feb 2026 01:04:18 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 27 Feb 2026 01:04:19 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 27 Feb 2026 01:04:21 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 27 Feb 2026 01:04:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Feb 2026 01:04:21 GMT
STOPSIGNAL SIGINT
# Fri, 27 Feb 2026 01:04:21 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 27 Feb 2026 01:04:21 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:00b501106805d55ebe605ff077d09c8c22aa2ccf0dd9ceffb2a21c5319633322`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 28.5 MB (28526197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a6f997a2bae9d6583f7a9d6141815e9b9041dff337d7ac153b3f46c5b805f5`  
		Last Modified: Wed, 25 Feb 2026 00:57:53 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd847e167f615e000df95c8ddbf4ec913956e8de429393c14d6579c8fa3b6eec`  
		Last Modified: Wed, 25 Feb 2026 00:57:53 GMT  
		Size: 4.5 MB (4475211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509b6c5cb25f9d256fb91972058d92c97ec72660257a5e4a0567b93d983683e4`  
		Last Modified: Wed, 25 Feb 2026 00:57:53 GMT  
		Size: 1.2 MB (1159230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d89b9e442925e9f99cc7d8126d286c933d9fa2af1dcd629bbe272d3991148e6`  
		Last Modified: Wed, 25 Feb 2026 00:57:54 GMT  
		Size: 8.1 MB (8066656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf9052eb778f8906ff20e40210c947a76e79676a164349c0d43640103061a45`  
		Last Modified: Wed, 25 Feb 2026 00:57:54 GMT  
		Size: 1.2 MB (1182880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6855c7d85646174eb68be28db5ef4c48412e69cc602e86bd03308406068383`  
		Last Modified: Wed, 25 Feb 2026 00:57:55 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b8fcdebfff3d96daa7d06b1c7d79991f36b897615adee4b706b0a3403cc991`  
		Last Modified: Wed, 25 Feb 2026 00:57:55 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10b3d8eaf78aed58fbfe744e263c23e2b7a111999bebe8f480ad23102163d9f`  
		Last Modified: Fri, 27 Feb 2026 01:06:22 GMT  
		Size: 107.3 MB (107253203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1689ff3580f0609b061696f01c939a75a85ec3d0213fb3e1a7133e85198d396c`  
		Last Modified: Fri, 27 Feb 2026 01:06:11 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1fcc7af781b66a62d8e2b98cc7f1658b55e11e51406a6387d4c56b75fca74e`  
		Last Modified: Fri, 27 Feb 2026 01:06:11 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78683ca29425439c8b35cb18bc4d5ab49dbeedd4dd166a70bbc22097b962bac2`  
		Last Modified: Fri, 27 Feb 2026 01:06:11 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f886dbd6940288f86c87cdf2f53c208180352121b7ac6796a31cc613c8fa8b`  
		Last Modified: Fri, 27 Feb 2026 01:06:13 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09a5f629bdc374bb83c4ef2accdeb302b5d950a57c7444f7cd60e972067ab7f`  
		Last Modified: Fri, 27 Feb 2026 01:06:13 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:1bc24690261fa3e09d7baefa132664dcf632f1969e7fcb94864f02a5fd6d0635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 KB (53162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:721a3abfc953875e2ebd5d828e5dc957c8df24876f4a2efbbf961b708c6e644a`

```dockerfile
```

-	Layers:
	-	`sha256:629fa80e786affa5d53a9e991ed49f007c016e2cfb76ed726f35a9c5ad7aaba7`  
		Last Modified: Fri, 27 Feb 2026 01:06:11 GMT  
		Size: 53.2 KB (53162 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:88b07681a0354b6d00e56de2b7b0521b287b8f092a918fdf82574313e7d9c62e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.6 MB (164565142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4d5033b2c121fd48f34347d2cbd71556feacb8006224145a5b3a529acd01c0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 01:29:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 17 Mar 2026 01:29:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:29:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 01:29:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 01:29:41 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 17 Mar 2026 01:29:41 GMT
ENV LANG=en_US.utf8
# Tue, 17 Mar 2026 01:29:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:29:47 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:29:48 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Mar 2026 01:29:48 GMT
ENV PG_MAJOR=14
# Tue, 17 Mar 2026 01:29:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 17 Mar 2026 01:29:48 GMT
ENV PG_VERSION=14.22-1.pgdg12+1
# Tue, 17 Mar 2026 01:36:58 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 17 Mar 2026 01:36:58 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 17 Mar 2026 01:36:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 17 Mar 2026 01:36:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 17 Mar 2026 01:36:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 17 Mar 2026 01:36:59 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 17 Mar 2026 01:37:00 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 01:37:00 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 17 Mar 2026 01:37:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:37:00 GMT
STOPSIGNAL SIGINT
# Tue, 17 Mar 2026 01:37:00 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 17 Mar 2026 01:37:00 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7a0392d98c02d4219c67a8e3d3837c1ac5d4af6836b9264bdd6c427cc7a24f76`  
		Last Modified: Mon, 16 Mar 2026 21:51:26 GMT  
		Size: 32.1 MB (32078368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73686b89d3fe322577b2012c352fd3afb7e45612b66dfd3bc70e179ecb73b562`  
		Last Modified: Tue, 17 Mar 2026 01:31:16 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68022e9c23ab840906f618d3703a0cf7eec7d323590d583eabc6f0b3ee25db68`  
		Last Modified: Tue, 17 Mar 2026 01:31:17 GMT  
		Size: 5.4 MB (5368503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fb104126a2925a34ec85667a7e49ee0dac150fc18997733eb755f92c50ccad`  
		Last Modified: Tue, 17 Mar 2026 01:31:16 GMT  
		Size: 1.2 MB (1208150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f44687134ee31bed8746b8e91a78d148a9e75db604477dcae1826f547bb7263`  
		Last Modified: Tue, 17 Mar 2026 01:31:17 GMT  
		Size: 8.1 MB (8066563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4612a910a915d54f8e453ce817958f137978382edd724f8b55a5f995eb2fa752`  
		Last Modified: Tue, 17 Mar 2026 01:31:17 GMT  
		Size: 1.3 MB (1283622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4f3db8b2463f570580b33f8ddfc3b2db10c9fe29c63cf3d0c777e2e2b45fdf`  
		Last Modified: Tue, 17 Mar 2026 01:31:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3da0f21b443527fd9b75e640657f608dc2d4e64fc66032a36372061e2825e0`  
		Last Modified: Tue, 17 Mar 2026 01:31:18 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da02a51c67be6fba08016df41215967d791ccc3a310d0029b6db6db0781203fd`  
		Last Modified: Tue, 17 Mar 2026 01:37:44 GMT  
		Size: 116.5 MB (116539664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d46357fcd15240745d67e40217c3e448e11fe6121721cb9aae2a53d3a1918b8`  
		Last Modified: Tue, 17 Mar 2026 01:37:41 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531d4e0323c3510deefd9819628ebf89571e2529b9af19f512fc2a244ab351ac`  
		Last Modified: Tue, 17 Mar 2026 01:37:41 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5e0d933bfe6926555365aa1e0eb9e27c560952d907c0b8afa7132bb956062b`  
		Last Modified: Tue, 17 Mar 2026 01:37:41 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fb034e8dc5ca290ff1449049e7ddae17723dcec091835a65514973756c7f2a`  
		Last Modified: Tue, 17 Mar 2026 01:37:42 GMT  
		Size: 5.8 KB (5835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87f2188efc1cbca75e48bf95b51411215934781895c06bf80105dc6c930eb9f`  
		Last Modified: Tue, 17 Mar 2026 01:37:42 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:8050f655675a55208c9893ed9a730a62c185e462b8618022b7aa8ac85d2e9ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5854988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2662b4fe0171a27cef259d4a13af51ebf700447c3444a226b02bb5b66342f19b`

```dockerfile
```

-	Layers:
	-	`sha256:aa5edf9903b0127274a47732307087e34d83673a1d4f68cc70f4087fdee90730`  
		Last Modified: Tue, 17 Mar 2026 01:37:41 GMT  
		Size: 5.8 MB (5801638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c74a03a6e103f5d43fe2cf5a90fb2183daf7a6e8e1cede9b15429c1c9056515`  
		Last Modified: Tue, 17 Mar 2026 01:37:40 GMT  
		Size: 53.4 KB (53350 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:be818b3c225052bf394c4080126fb80d2df4ac023307e965f56149528db966c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (161020604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d10744d493fcfbd8c6174c30f276e9aed728fb16b403a84bdc42e4da113c1137`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:03:47 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 16 Mar 2026 23:03:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:03:59 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 23:03:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 23:04:04 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 16 Mar 2026 23:04:04 GMT
ENV LANG=en_US.utf8
# Mon, 16 Mar 2026 23:04:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:04:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 16 Mar 2026 23:04:09 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 23:04:09 GMT
ENV PG_MAJOR=14
# Mon, 16 Mar 2026 23:04:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Mon, 16 Mar 2026 23:04:09 GMT
ENV PG_VERSION=14.22-1.pgdg12+1
# Mon, 16 Mar 2026 23:47:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 16 Mar 2026 23:47:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 16 Mar 2026 23:47:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 16 Mar 2026 23:47:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 16 Mar 2026 23:47:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 16 Mar 2026 23:47:07 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 16 Mar 2026 23:47:07 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:47:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 16 Mar 2026 23:47:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:47:07 GMT
STOPSIGNAL SIGINT
# Mon, 16 Mar 2026 23:47:07 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 16 Mar 2026 23:47:07 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37c397d4cf5d96014b5d7732cd538e0df4355c117dfb4919b2b0e1378ca3696`  
		Last Modified: Mon, 16 Mar 2026 23:18:54 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd735821172fbe4cf93079f7649cf26d2d82cf9774b02e60922c2a0413aca97c`  
		Last Modified: Mon, 16 Mar 2026 23:18:54 GMT  
		Size: 4.4 MB (4391203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9e2daece88cc5e28710972e14a1c56b2747e9a96335d8dbcdd197686fa12f8`  
		Last Modified: Mon, 16 Mar 2026 23:18:54 GMT  
		Size: 1.2 MB (1222800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30d84746c78b8bd690ce46a69ddd62108696fa7aa2309c0a5ce62038fa06aac`  
		Last Modified: Mon, 16 Mar 2026 23:18:54 GMT  
		Size: 8.1 MB (8120745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44539cfb76f7c2597f15d57769a0628faa73a794048554bfc8743dcd6f3d731`  
		Last Modified: Mon, 16 Mar 2026 23:18:55 GMT  
		Size: 1.1 MB (1097060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf246121e4f34eb7ab067d2936d11a5991af0bdd7570f0aa9da69970bdf4ba8b`  
		Last Modified: Mon, 16 Mar 2026 23:18:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd39ef00523133f2004b72289d610e6ad2fcc42f94dbc0ab53dc02fa1b6c463`  
		Last Modified: Mon, 16 Mar 2026 23:18:55 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c358832a1b377b5b7237a9043fff6dc20096e791dba3a95f805d34ff7d5f275e`  
		Last Modified: Mon, 16 Mar 2026 23:47:43 GMT  
		Size: 119.3 MB (119277004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e79a94bafb53cb8e5a54a0842fa2c56210d9218d1b1cd806c14681278da550`  
		Last Modified: Mon, 16 Mar 2026 23:47:40 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6de3b1b02969a4865fea75bafbf279018c9a56ecdf554fbff504ec8ce80482`  
		Last Modified: Mon, 16 Mar 2026 23:47:40 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d88b56908e331dc2e248f37eb04dc6d50d36ddd060851bf8b4d1c1c08a8afe`  
		Last Modified: Mon, 16 Mar 2026 23:47:40 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b16de211acaca8ace47c2d8a06bfbbfa7ea45484528d7ac993666693d7ddf8`  
		Last Modified: Mon, 16 Mar 2026 23:47:41 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4144ff1322f6a932d8fa6c9dbfdc91c60a3ab8161abd6514d4b420d74df9060`  
		Last Modified: Mon, 16 Mar 2026 23:47:41 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:c5c588dafa98db77abc81bff324aac569fa4d814d45aa672e317f4b0501275fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5858016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7e6481e956fbc27791414ed5812e11716539aa8eeb6b27de19d0e4ade61ec9`

```dockerfile
```

-	Layers:
	-	`sha256:af36134bfebc97b3b53c8b59f9792d716634609a259cca6ab0279484914e9866`  
		Last Modified: Mon, 16 Mar 2026 23:47:40 GMT  
		Size: 5.8 MB (5804721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:facdfe55c0c6fc283bd2182d83c1ba9aaff7198a7c26f334418034751eb003c9`  
		Last Modified: Mon, 16 Mar 2026 23:47:40 GMT  
		Size: 53.3 KB (53295 bytes)  
		MIME: application/vnd.in-toto+json
