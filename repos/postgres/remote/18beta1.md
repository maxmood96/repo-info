## `postgres:18beta1`

```console
$ docker pull postgres@sha256:8e24e2dcc0ead42a5fa672b41d6079f690effa5f252f6a2e81b7162cebcbb690
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

### `postgres:18beta1` - linux; amd64

```console
$ docker pull postgres@sha256:4b3c8c15fcfa779a61918a265962d7e73ea7ce0613427f80764efa0222538637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157208641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ac9a56d090cafd97077ed00f5fbc3f872bff7d0f1fe5918fb7492f663e0fff9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 09 Jun 2025 21:23:06 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV GOSU_VERSION=1.17
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV LANG=en_US.utf8
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PG_MAJOR=18
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PG_VERSION=18~beta1-1.pgdg120+1
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 09 Jun 2025 21:23:06 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
VOLUME [/var/lib/postgresql]
# Mon, 09 Jun 2025 21:23:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jun 2025 21:23:06 GMT
STOPSIGNAL SIGINT
# Mon, 09 Jun 2025 21:23:06 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 09 Jun 2025 21:23:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d04498d548f4438af15a48631de5efddccfc476f3113dcac550ccb9e942e974`  
		Last Modified: Tue, 01 Jul 2025 02:21:53 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa2a49d7984d1a06faa8999ed4011628760730904ce715b91fc1379f7b3fb1a`  
		Last Modified: Tue, 01 Jul 2025 02:21:55 GMT  
		Size: 4.5 MB (4533805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec71a98f01b86a33d23194dbd912cd8de06f721d49b884071fd26e0572e7701f`  
		Last Modified: Tue, 01 Jul 2025 02:21:53 GMT  
		Size: 1.4 MB (1446822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a6b98d3637319827c3becffa5d6af6faff1819ea5a01c17c9bd1dae56630be`  
		Last Modified: Tue, 01 Jul 2025 02:21:55 GMT  
		Size: 8.1 MB (8066292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fb1f7ffef4a46eb8b1914c07c7c82dbfc7f793d979cfa706f652276322c59f`  
		Last Modified: Tue, 01 Jul 2025 02:21:53 GMT  
		Size: 1.2 MB (1196146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9b83fbb1dffdfd632f1f9d583df67db9dcbfc076bafcbe31810bfbee09b895`  
		Last Modified: Tue, 01 Jul 2025 02:21:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b1dfbe51a107ea4dc6081a1f2c0d4716711c5555d9659c4ff3387732fe76e67`  
		Last Modified: Tue, 01 Jul 2025 02:21:53 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c9ae732a3be647a2d2303a7441bc42ba9b09e8d7246ae8856a7d766c2b5a33`  
		Last Modified: Tue, 01 Jul 2025 02:22:09 GMT  
		Size: 113.7 MB (113705480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844e8a3b931b34691485dfde7c17be1d2d236483f148f04d24ed5971778f19c6`  
		Last Modified: Tue, 01 Jul 2025 02:21:54 GMT  
		Size: 19.1 KB (19107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03febadd1e534ad4f82432c7439f36ec4a9ba1e8ad0538c90fe939100b2602b`  
		Last Modified: Tue, 01 Jul 2025 02:21:54 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e7c0948872ba8ba58e0a5e93d98b943f18a0cff3fc54d14eeade95775c0d19`  
		Last Modified: Tue, 01 Jul 2025 02:22:14 GMT  
		Size: 180.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5456c8f8dde9be103574df3e325622b6ea0f14ba469c40bfe291ac072ad0f6c9`  
		Last Modified: Tue, 01 Jul 2025 02:22:14 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de41fd89fa661dddafb9d20b7d87cf49c7cbb7c6771ee456a6a797cf3cea59c`  
		Last Modified: Tue, 01 Jul 2025 02:22:14 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta1` - unknown; unknown

```console
$ docker pull postgres@sha256:ae89c01f05826cc1da61a200109c6414c2b5bbb09eb30c66d7f28fe32cde33c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6285831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d1d675ac30a0b65e0cf0be486138a8837886ab6bafe5707a7e515c97ad00d2c`

```dockerfile
```

-	Layers:
	-	`sha256:cd40a66732c3dab5f4bbd50a2de1694a48472a7e67715c14fdbab0e131c58620`  
		Last Modified: Tue, 01 Jul 2025 05:11:24 GMT  
		Size: 6.2 MB (6231360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7e1cb6e3df453ffbebddd6bff99c7dfd9678d809717fae8d4d51a1c2e944b82`  
		Last Modified: Tue, 01 Jul 2025 05:11:24 GMT  
		Size: 54.5 KB (54471 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18beta1` - linux; arm variant v5

```console
$ docker pull postgres@sha256:b3c5986d6af20b0245fde9f020c1920ce641147e4620a63d7225fa1256844101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.3 MB (87346234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55916ebbadd15e0501c739ac9a163969b152daacdfae0cb0a267d3c3659e666d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 09 Jun 2025 21:23:06 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1751241600'
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV GOSU_VERSION=1.17
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV LANG=en_US.utf8
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PG_MAJOR=18
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PG_VERSION=18~beta1-1.pgdg120+1
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 09 Jun 2025 21:23:06 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
VOLUME [/var/lib/postgresql]
# Mon, 09 Jun 2025 21:23:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jun 2025 21:23:06 GMT
STOPSIGNAL SIGINT
# Mon, 09 Jun 2025 21:23:06 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 09 Jun 2025 21:23:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:57a7872a7ce75b95d171f720f215d4e72b887ae709c5c0b319f93f704bd71e07`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 25.8 MB (25762460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a99af74ac41b5e2e14fa4513d76698005608e5ddc2d8aa5942109a572907ce`  
		Last Modified: Tue, 01 Jul 2025 04:40:08 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2929fa29f2d446225733e6eed57e6ad637cec5e7f3de512cce34d7eea0476ce`  
		Last Modified: Tue, 01 Jul 2025 04:40:08 GMT  
		Size: 4.2 MB (4151002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad1c89473e8b87c0193fd110743e6877d967558433e3d715712cd78f2dc64ed`  
		Last Modified: Tue, 01 Jul 2025 04:40:10 GMT  
		Size: 1.4 MB (1424011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf3674f0c0373c3a8436d8f0426c4c07dd6780e03768df3905aed72f39ea0f1`  
		Last Modified: Tue, 01 Jul 2025 04:40:09 GMT  
		Size: 8.1 MB (8066384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87efba02fa0f71548385b89589e0980ba97ec9773e0202a0ebb98d6722b78547`  
		Last Modified: Tue, 01 Jul 2025 04:40:08 GMT  
		Size: 1.2 MB (1194862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46620737aabb5ffa6a72a3107afab8eb77c70e1ca1af6bcd0d12e50e679307d2`  
		Last Modified: Tue, 01 Jul 2025 04:40:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0de0fb5f3add8a6e7c84a0687c3f3264f9be367fc10f0a67cfac0e33bd79284`  
		Last Modified: Tue, 01 Jul 2025 04:40:08 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4cf4a4ad944bef3bc2790c04f7e6fc2d9a3ece40519eb758b475a05f90c9af`  
		Last Modified: Tue, 01 Jul 2025 04:40:11 GMT  
		Size: 46.7 MB (46717560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93441c477d075c908471f90af6c08d52b89902413948918eb7716264ccf27a30`  
		Last Modified: Tue, 01 Jul 2025 04:40:08 GMT  
		Size: 19.1 KB (19112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b99a571935bfc8f2328541b1ea404f53eb42e549ce40a311f64cd2acb5208fc`  
		Last Modified: Tue, 01 Jul 2025 04:40:08 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d54bbffcdea823f468669a7ebbefb8f18aa3111d03b355ba91b3c3f3b1622b`  
		Last Modified: Tue, 01 Jul 2025 04:40:08 GMT  
		Size: 180.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5e9687b6d2a89a278e29c559b76b25336ec1756ffc39f8e8168b3f726e4f66`  
		Last Modified: Tue, 01 Jul 2025 04:40:09 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876f0451d4be44f4a53f0b0fecea66dfb716695ad489747463bd142783140c67`  
		Last Modified: Tue, 01 Jul 2025 04:40:09 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta1` - unknown; unknown

```console
$ docker pull postgres@sha256:322da21e6476d674d4eb118c637deb1a3b764a1ffb3f0db7cc6c75f635d52cbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5446532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958ced390e3520df3826c5e5e12f1c8701fb7c2961d3798b74f0e7d484824080`

```dockerfile
```

-	Layers:
	-	`sha256:341d286c98bc6f1fee677d249054a4aa75aebefb172dd9183095628998dd4166`  
		Last Modified: Tue, 01 Jul 2025 05:11:30 GMT  
		Size: 5.4 MB (5391864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96fd240a4d710f4b32715e5179f14844fab1d2aa33ef886129cee1c0e2d7bc92`  
		Last Modified: Tue, 01 Jul 2025 05:11:31 GMT  
		Size: 54.7 KB (54668 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18beta1` - linux; arm variant v7

```console
$ docker pull postgres@sha256:980a58af312e987d4e756e644d67a1578c874982d0dff1bd7f9544cfdb43fb94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83451869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da7bfc9ebd9fa200422b4a5086ab76a96911d2bc11fbdf2a3d056e0ee7c08a52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 09 Jun 2025 21:23:06 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV GOSU_VERSION=1.17
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV LANG=en_US.utf8
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PG_MAJOR=18
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PG_VERSION=18~beta1-1.pgdg120+1
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 09 Jun 2025 21:23:06 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
VOLUME [/var/lib/postgresql]
# Mon, 09 Jun 2025 21:23:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jun 2025 21:23:06 GMT
STOPSIGNAL SIGINT
# Mon, 09 Jun 2025 21:23:06 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 09 Jun 2025 21:23:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f678460491e6e3e58b29b0794ecb56fc8a96a30f10f03022d693958941109d7`  
		Last Modified: Wed, 11 Jun 2025 02:16:53 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1541c2cc21989ce4e95e9bbac293eceebf4241d35720c1072b615757a2dc15`  
		Last Modified: Wed, 11 Jun 2025 02:17:00 GMT  
		Size: 3.7 MB (3742536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1dd2cd14ae8d9868080c92a323b88ba19a70f5a6e1c981f8be6e7af33e6558`  
		Last Modified: Wed, 11 Jun 2025 02:17:13 GMT  
		Size: 1.4 MB (1413713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6197ced2d4fd27c59bb966da1995d8f62ceee2380cc9da7b746aef85a24ff7`  
		Last Modified: Wed, 11 Jun 2025 05:11:59 GMT  
		Size: 8.1 MB (8066263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e751019b3b3890e6992143f7fec0be633bc51abd84dc751e188bbdb929e2179`  
		Last Modified: Wed, 11 Jun 2025 02:17:22 GMT  
		Size: 1.1 MB (1067003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533b1db079026151bc8338c2ea9d6d34229a62d61ee93ea1ae1d181c9b780081`  
		Last Modified: Wed, 11 Jun 2025 02:17:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436d3b49bcef8a85b111c526bb62af81819de9dc67083d03d23cbd0884b7014f`  
		Last Modified: Wed, 11 Jun 2025 02:17:31 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77805f11bc38fd36314b0b47ff8c35b5fee5ae985dd553b89a32dbae1679371b`  
		Last Modified: Wed, 11 Jun 2025 11:05:24 GMT  
		Size: 45.2 MB (45193638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05060e7df7ca8480ee02445f62b8094b7c98166425dcb268cabd7dee277f3c06`  
		Last Modified: Wed, 11 Jun 2025 02:17:38 GMT  
		Size: 19.1 KB (19115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1018e1f601c54632736edb4dcc2ea713f3121c183fb467d2f74540aa72d345`  
		Last Modified: Wed, 11 Jun 2025 02:17:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7c0855247046556007fe4421b1d24b4555c40e8448bd7fcc2e1328129acc8d`  
		Last Modified: Wed, 11 Jun 2025 02:17:46 GMT  
		Size: 180.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd8563f1dc83e9e1db9e88cc9274d393e52a2800cdcf51a2c41727d326557f7`  
		Last Modified: Wed, 11 Jun 2025 02:17:49 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d6f524caeea2a80492502f215ffef2ba999cb5c20472fb8469bdeede07dded`  
		Last Modified: Wed, 11 Jun 2025 02:17:53 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta1` - unknown; unknown

```console
$ docker pull postgres@sha256:d788a857f7ab9efddf835eb3d0afe35e7e57c981756fa4b3cc689476579115e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5445753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3412e3629b333c64484996c06c613657cb32143a0e569be5c3aa6a120ab45721`

```dockerfile
```

-	Layers:
	-	`sha256:93fb86b85959832c1d292f6d64af9190219a1194f702e60c6d06a15dae7ba369`  
		Last Modified: Wed, 11 Jun 2025 05:11:09 GMT  
		Size: 5.4 MB (5391085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5f26576bfb9dd885f1dc3aa5834649d8d14918dc4313fa8b2afa6de52fa239a`  
		Last Modified: Wed, 11 Jun 2025 05:11:10 GMT  
		Size: 54.7 KB (54668 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18beta1` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:4655eca50c7592df49c86487fd43eb6cf8aecc355f990f98240750d3205c1890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155052244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:040f7d3bd0507c73198ddeeab453e77463d3add6e35855859091578aa768e50f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 09 Jun 2025 21:23:06 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV GOSU_VERSION=1.17
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV LANG=en_US.utf8
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PG_MAJOR=18
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PG_VERSION=18~beta1-1.pgdg120+1
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 09 Jun 2025 21:23:06 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
VOLUME [/var/lib/postgresql]
# Mon, 09 Jun 2025 21:23:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jun 2025 21:23:06 GMT
STOPSIGNAL SIGINT
# Mon, 09 Jun 2025 21:23:06 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 09 Jun 2025 21:23:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a490481288f236c28b2a0846973de7abdb045d17d9725da79516bf5a86457944`  
		Last Modified: Wed, 11 Jun 2025 02:22:12 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72cda6e94dd3728e1acfea2d662960b10c52c751667b2894153c36d5147e779e`  
		Last Modified: Wed, 11 Jun 2025 02:22:18 GMT  
		Size: 4.5 MB (4499204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc122681691c60b576e4074626fc06ccc51fc48b245bac716f43edc65e71be9`  
		Last Modified: Wed, 11 Jun 2025 02:22:27 GMT  
		Size: 1.4 MB (1378810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe317346973e0991f4cb39fac76732c09f2ff5b9b0e2b388fa9cd44a24324dc`  
		Last Modified: Wed, 11 Jun 2025 03:17:39 GMT  
		Size: 8.1 MB (8066329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320a6740ddc14fd55dacd11f2c397c03fef424a8028f2aee73893cbe4024338e`  
		Last Modified: Wed, 11 Jun 2025 02:22:32 GMT  
		Size: 1.1 MB (1108757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c514d4e4ea347617f4fa1c44cc646d08783397f5dac368644d5b2ed9f8b656ff`  
		Last Modified: Wed, 11 Jun 2025 02:22:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5457eb3f232d1874d90675ed8aa11bbe345bb05aed7b2b6a2000091fc6d45c`  
		Last Modified: Wed, 11 Jun 2025 02:22:41 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a0a369c0ab255398a8d403c21924faedfbf0ec420b6a786d540685f7a9386a`  
		Last Modified: Wed, 11 Jun 2025 06:06:28 GMT  
		Size: 111.9 MB (111891512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d13cbeeb50b4431aa189232ded239ccd5b10fa5188e3a592a69287ab87977f`  
		Last Modified: Wed, 11 Jun 2025 02:22:57 GMT  
		Size: 19.1 KB (19102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0804781c008cafa2af1b261e8e7c19ec5c558aa83f218efa5596b44015688375`  
		Last Modified: Wed, 11 Jun 2025 02:23:01 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abd9f42376275a69944b1557e97f231a9612ebb7b90b8c600925b95497b7a38`  
		Last Modified: Wed, 11 Jun 2025 02:23:03 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f78c9994f903fc50f111c7f55891c17856dbb5597ba4621f948e69445c40d8`  
		Last Modified: Wed, 11 Jun 2025 02:23:06 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f996c433364bd1c2b0fecb0d50ead00f85b329a22fd34ea0651707f20a62ec63`  
		Last Modified: Wed, 11 Jun 2025 02:23:08 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta1` - unknown; unknown

```console
$ docker pull postgres@sha256:266114f70834882a68a3df2f59e41046806c9629be9a876a6d3e0ff3853dc728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6292356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26e9f19ff4c19c8a45688cc0e88d1e8cea44ecc3ba28d7da859828e4a3377d5`

```dockerfile
```

-	Layers:
	-	`sha256:01c84c4de59296246c9ba2796c5ca2805caa8679f42174006a9410ef27fd2b7e`  
		Last Modified: Wed, 11 Jun 2025 05:11:15 GMT  
		Size: 6.2 MB (6237640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38e20490cd81df274ba54cbe613dabf684fa01eaf48c7bdf410bba6f4a206a19`  
		Last Modified: Wed, 11 Jun 2025 05:11:16 GMT  
		Size: 54.7 KB (54716 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18beta1` - linux; 386

```console
$ docker pull postgres@sha256:5c1609ce200e3efac28aad3aaed9337b1ef122ae0d206706b6c639784e28e0ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 MB (94105863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492e87f359468a4deee806c70d4a3c932b8c9a62e4ab8dd0d58de5856f9fe5c2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 09 Jun 2025 21:23:06 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV GOSU_VERSION=1.17
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV LANG=en_US.utf8
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PG_MAJOR=18
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PG_VERSION=18~beta1-1.pgdg120+1
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 09 Jun 2025 21:23:06 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
VOLUME [/var/lib/postgresql]
# Mon, 09 Jun 2025 21:23:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jun 2025 21:23:06 GMT
STOPSIGNAL SIGINT
# Mon, 09 Jun 2025 21:23:06 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 09 Jun 2025 21:23:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83fca07b195d150a373a7bbc560f1e2bcbcc142a201d68c99ab55d4c87d08ca0`  
		Last Modified: Tue, 01 Jul 2025 02:30:35 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def20d553115b0c93bfc5bc257276077e6ad5b4398ab9277d4b22a02aa410491`  
		Last Modified: Tue, 01 Jul 2025 02:30:38 GMT  
		Size: 5.0 MB (4965059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdb6f3f8e6df062daa828bb3da08a06fdcefae8cd7d287db4067aaff5bc2fa2`  
		Last Modified: Tue, 01 Jul 2025 02:30:36 GMT  
		Size: 1.4 MB (1422248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122718c031a16cdb3032d8d4be2ae8a03064dc7631e796098ddd08e606894548`  
		Last Modified: Tue, 01 Jul 2025 02:30:36 GMT  
		Size: 8.1 MB (8066298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2100266e02faa4d3369f5dc8e25f76451fdc6fb5afb6290ec8815e0f8796bc8e`  
		Last Modified: Tue, 01 Jul 2025 02:30:36 GMT  
		Size: 1.1 MB (1137185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903cdc9d6e18c4862f6831a0e56e72ca689efa1609c3f240a2e4355e6426e9a3`  
		Last Modified: Tue, 01 Jul 2025 02:30:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7bf5edbb2acef5eaac3f70da136ce36b2905eb5104076ac0a845575f947358`  
		Last Modified: Tue, 01 Jul 2025 02:30:36 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3eb177cc4f6e54b50f84db0c7a77254c2fccfce03d65fb0538db08be62d83e1`  
		Last Modified: Tue, 01 Jul 2025 02:30:38 GMT  
		Size: 49.3 MB (49272686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7335f9d07877d9ed056707bda425bee856f629ca0ba225af36368d9f85d2dce`  
		Last Modified: Tue, 01 Jul 2025 02:30:35 GMT  
		Size: 19.1 KB (19111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a350555fcf7bd71620010f74648ebe6c833c9a836cfc2021ae8ce7c3d14962bf`  
		Last Modified: Tue, 01 Jul 2025 02:30:35 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c9a492ae7076101d6d53c738700457791efb04a83432b5e192ce359bf556b5`  
		Last Modified: Tue, 01 Jul 2025 02:30:38 GMT  
		Size: 180.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236e7ed9dab92064ef18c1860377555a64cc7d935e67b36b130d30005eb39eef`  
		Last Modified: Tue, 01 Jul 2025 02:30:38 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2cbe32070b5b1c3d85f1596545c41fde5116e58431817ff872e9c17448877c7`  
		Last Modified: Tue, 01 Jul 2025 02:30:39 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta1` - unknown; unknown

```console
$ docker pull postgres@sha256:a2463983a8fc13f69c7f2e9d987e7a37660f7820e1e4494d8c1f0efa4794adeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5440855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286580608693da0e253b4b5c56c9768df27036c00dc36716bc85b60b582e451b`

```dockerfile
```

-	Layers:
	-	`sha256:7602c6318d286c90a40ed00415d805a87ce2c1c6ddb3a4f9828cc92abd765a8a`  
		Last Modified: Tue, 01 Jul 2025 05:11:51 GMT  
		Size: 5.4 MB (5386434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d282932ae6f97fd0762425e8213d3687b4796a56d700f6bc498d4d48788fae5`  
		Last Modified: Tue, 01 Jul 2025 05:11:52 GMT  
		Size: 54.4 KB (54421 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18beta1` - linux; mips64le

```console
$ docker pull postgres@sha256:684817f43a6d63f74f9cf0abf9860cbe48e81a39a6c0ecbfbb6005033f4cca19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156057401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e479e94ea742d1e83bbbef992511bc421aa0d85d00a3b6ff87d75386ecf9b6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 09 Jun 2025 21:23:06 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV GOSU_VERSION=1.17
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV LANG=en_US.utf8
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PG_MAJOR=18
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PG_VERSION=18~beta1-1.pgdg120+1
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 09 Jun 2025 21:23:06 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
VOLUME [/var/lib/postgresql]
# Mon, 09 Jun 2025 21:23:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jun 2025 21:23:06 GMT
STOPSIGNAL SIGINT
# Mon, 09 Jun 2025 21:23:06 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 09 Jun 2025 21:23:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ac3f61581c7f5755d8598b3a0857c417db0251b17c0e4e4f43a5fc0e24023524`  
		Last Modified: Tue, 10 Jun 2025 22:48:26 GMT  
		Size: 28.5 MB (28516717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223758daa5d17a67cc490bac729023fa551cef41870ec1cab91a1950c530a532`  
		Last Modified: Wed, 11 Jun 2025 06:56:47 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8de5d0c0a8ea490074635a86cb6458ef442b2ad6d711d4bb01f504ad47c6f6`  
		Last Modified: Wed, 11 Jun 2025 06:56:52 GMT  
		Size: 4.5 MB (4475133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982cb2cf82d00cd9007464556f0b7fa746eda305059c9801fdcaff50803667a7`  
		Last Modified: Wed, 11 Jun 2025 06:57:07 GMT  
		Size: 1.3 MB (1333874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd63fc4ec338c1ba4211b37ad630d35eeae03fd7e36c2cf391c8419a5d93781`  
		Last Modified: Wed, 11 Jun 2025 08:10:18 GMT  
		Size: 8.1 MB (8066484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74696133f03722f21cd7c4c3fc0e50e98b8fff8c6c523a5f87327bb32ab4d03`  
		Last Modified: Wed, 11 Jun 2025 06:57:12 GMT  
		Size: 1.2 MB (1182615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df5cfba69da36c505a05e3b030c85b63ea2e8e6ff32677ac4ece26f265502ab`  
		Last Modified: Wed, 11 Jun 2025 06:57:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f50998f3198c22411b36434112a5f950a7552f528b036784d67bd29a9c7b422a`  
		Last Modified: Wed, 11 Jun 2025 06:57:22 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2fe0f4408699444e17f4e4b885bcf2b95acb72b510e4bc68c51a99c447e1f5`  
		Last Modified: Wed, 11 Jun 2025 08:10:22 GMT  
		Size: 112.5 MB (112452612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78798e1fa7e8b16b8059641ddafaa8d91b4278a3ad309437bbbdddf7cd51e66`  
		Last Modified: Wed, 11 Jun 2025 06:57:26 GMT  
		Size: 19.1 KB (19114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861d5163a6b2c30ac8fee06b2d5c4fee39b68eb97f0594ad2246948de22ddb70`  
		Last Modified: Wed, 11 Jun 2025 06:57:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5548847ca6db6fcf08935f228869af3d2c4eb514444951367b80234005455f3c`  
		Last Modified: Wed, 11 Jun 2025 06:57:32 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc7835f5864470230d1fca51dab73962cdd4446697fe71398a677d0de5456cc`  
		Last Modified: Wed, 11 Jun 2025 06:57:36 GMT  
		Size: 5.9 KB (5930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608a42bb1eaa72ca338842871a8bd525a6f8ab25ad29aecdc83acdc6ea6b9586`  
		Last Modified: Wed, 11 Jun 2025 06:57:38 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta1` - unknown; unknown

```console
$ docker pull postgres@sha256:76896d3d03142f3975bd94a912126c5295bac41943d743c8b15e54ef9d8100d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 KB (54337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a329e8aac7437e06057168954b0ce909e39a132debb2f04f08e191a1a02b7df`

```dockerfile
```

-	Layers:
	-	`sha256:b3faaad48caf6baebdc965b68c258387dabb0e67a3c4d70096a53c0e377ba327`  
		Last Modified: Wed, 11 Jun 2025 08:09:42 GMT  
		Size: 54.3 KB (54337 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18beta1` - linux; ppc64le

```console
$ docker pull postgres@sha256:c2f510f581c816cd6f883d5bb5a1b61f74f1b149c039db6ae0aabf5585b96d49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.1 MB (170060369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:387f51cc2279ae1eb6d064e1f3ba35631451f4449033e12d8e6026598345b8fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 09 Jun 2025 21:23:06 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV GOSU_VERSION=1.17
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV LANG=en_US.utf8
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PG_MAJOR=18
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PG_VERSION=18~beta1-1.pgdg120+1
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 09 Jun 2025 21:23:06 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
VOLUME [/var/lib/postgresql]
# Mon, 09 Jun 2025 21:23:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jun 2025 21:23:06 GMT
STOPSIGNAL SIGINT
# Mon, 09 Jun 2025 21:23:06 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 09 Jun 2025 21:23:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ea11528749ed33c47316b22db3ad2aeb6a120a081a31b6be07dbfc58c80694`  
		Last Modified: Wed, 11 Jun 2025 04:09:18 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28912c9fb8228de6de61cadc5bb5c80a21c253acb4ddcb3c132fa1a952fa547f`  
		Last Modified: Wed, 11 Jun 2025 04:09:19 GMT  
		Size: 5.4 MB (5368168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067f4f82ee10da21a56dddece2091747cb5c4b58285443f6c325ef95f7cb7f6b`  
		Last Modified: Wed, 11 Jun 2025 04:09:19 GMT  
		Size: 1.4 MB (1368695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55081cc90c50f8f22c24ce03b21dd98ea13843dd6952697dde0a28a77621dc34`  
		Last Modified: Wed, 11 Jun 2025 04:09:20 GMT  
		Size: 8.1 MB (8066368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb9fe949190da61cccdb95b10e91005b651a6ab4a107fab6e48179145ecb35b`  
		Last Modified: Wed, 11 Jun 2025 04:09:19 GMT  
		Size: 1.3 MB (1283538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b30ed51df6659aed6a3bc950756a969eec237cdb7e612ef0ad25848d02f712`  
		Last Modified: Wed, 11 Jun 2025 04:09:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa3e4c2e8b5b9845bc9ef6101ccf62466b317167717ec75fe20a9e498fc30e1`  
		Last Modified: Wed, 11 Jun 2025 04:09:20 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2db14d34d749b61d99aa79a3de1b580105ca1c4f90eb2189a241dbc5d0a593`  
		Last Modified: Wed, 11 Jun 2025 04:09:28 GMT  
		Size: 121.9 MB (121870843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7768ee920f74fe5e87cc079e19d9c63288914689c82efc5715372f81f0defa5b`  
		Last Modified: Wed, 11 Jun 2025 04:09:22 GMT  
		Size: 19.1 KB (19113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c7269a155202d4aedaf618087397310d1d4033860684967c3b150ea5e68f11`  
		Last Modified: Wed, 11 Jun 2025 04:09:22 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b02fb82b4815fe33dbb1a334703542aebfc2e64b3e15add9cdf9e3383234b5`  
		Last Modified: Wed, 11 Jun 2025 04:09:22 GMT  
		Size: 181.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2575246c1c9c6274aee96ee3a9a3272cf9f317613b6e7f4b6464546510448eca`  
		Last Modified: Wed, 11 Jun 2025 04:09:23 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d4e1e415ab0616c6d94577648f58e6bcf75166bc41d7a09e66a85709c8cae9`  
		Last Modified: Wed, 11 Jun 2025 04:09:23 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta1` - unknown; unknown

```console
$ docker pull postgres@sha256:49e72994f06cb6bf5b12a9a661e87c5977ac6f69ac11e0cee790dfcaccbb45ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6293239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54faa48df5346f1f6a711a23fff1bfeeff442f4b74df829cafa80875031b3dfc`

```dockerfile
```

-	Layers:
	-	`sha256:2134769526be79a02c2d3c3e3d976e08b470971f978fa5cc8edd404f8cbe51f2`  
		Last Modified: Wed, 11 Jun 2025 05:11:26 GMT  
		Size: 6.2 MB (6238714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:077d5cdcbdb017ea3a0d2abccfef01d59368aa1452b808cfb3d8ee03cdaf772b`  
		Last Modified: Wed, 11 Jun 2025 05:11:27 GMT  
		Size: 54.5 KB (54525 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18beta1` - linux; s390x

```console
$ docker pull postgres@sha256:25c0ed0d5452b4792962bcc6452aad4e5cf7aec8ef596c5f92f38d96f39903ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166533105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4106639669b77f429741e311cd20764e2df6ca76d0118902bb2c856630821591`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 09 Jun 2025 21:23:06 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV GOSU_VERSION=1.17
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV LANG=en_US.utf8
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PG_MAJOR=18
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PG_VERSION=18~beta1-1.pgdg120+1
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 09 Jun 2025 21:23:06 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
VOLUME [/var/lib/postgresql]
# Mon, 09 Jun 2025 21:23:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jun 2025 21:23:06 GMT
STOPSIGNAL SIGINT
# Mon, 09 Jun 2025 21:23:06 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 09 Jun 2025 21:23:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc70566b1e81464517f00a2131125b995f48aa9b73001a88b4e4b59b7dd02fd`  
		Last Modified: Tue, 01 Jul 2025 04:12:56 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3468e3f8feb65f8c6ea67fd15d40648d79970bd1b046b79030649d9a5d44a9`  
		Last Modified: Tue, 01 Jul 2025 04:12:57 GMT  
		Size: 4.4 MB (4390967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62a421f1170ff7e87352e2a4366d73b3e7b8dcb71f77f946e94738217bbbdd1`  
		Last Modified: Tue, 01 Jul 2025 04:12:57 GMT  
		Size: 1.4 MB (1412704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d271641961acf3d3d3fc06590f49e87cee35199469ecccfa3dc420b92ab9b0d`  
		Last Modified: Tue, 01 Jul 2025 04:12:57 GMT  
		Size: 8.1 MB (8120465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54656ed4e2a3b688785b931cd0d31640db4355f1edb13cac3e0d45fb68567b1f`  
		Last Modified: Tue, 01 Jul 2025 04:12:56 GMT  
		Size: 1.1 MB (1096782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01065eca2aaf636fd14ff8acbdbd64bab14e5b68327c4bafb24b2032e288d10d`  
		Last Modified: Tue, 01 Jul 2025 04:12:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b8c86b28805d339a2e28d6dce4172a4f812063755fd40bb4632d50912f948e`  
		Last Modified: Tue, 01 Jul 2025 04:12:56 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22827f9cb99b610764f64f6918816e7ea2bbe9711a9704e8ee8fa75bb263659c`  
		Last Modified: Tue, 01 Jul 2025 04:13:05 GMT  
		Size: 124.6 MB (124594418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4469e5f1a4e5ee1035c4066bdebaf6a94cb502cf476f4bb0e043c5801c21a1`  
		Last Modified: Tue, 01 Jul 2025 04:12:56 GMT  
		Size: 19.1 KB (19110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325365d077204fdd3431bc9a10970a825015f397ac80ac625b416ff98340b4bb`  
		Last Modified: Tue, 01 Jul 2025 04:12:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450a4412d1fd64a92e9100ec900b1dda4bb5e17ec8cf9cb0f2fadda65230ff85`  
		Last Modified: Tue, 01 Jul 2025 04:12:57 GMT  
		Size: 180.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244715e9ab0f35364dc46bfaeab084914c46f6c11a4b1246b4188886cc3d6248`  
		Last Modified: Tue, 01 Jul 2025 04:12:57 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee8f7c53142d0beee51b33e1922ffa568db3f50a56f3c879f0d8947a8d69c90`  
		Last Modified: Tue, 01 Jul 2025 04:12:57 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta1` - unknown; unknown

```console
$ docker pull postgres@sha256:cbc52b5cabc4490858b4458c1be71039dabfb131d3f42d22167c63b04e472deb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6300486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c44fa72933bde186ade0cc1d379ec941f85d2e39f844098750a5d8982c3aa08`

```dockerfile
```

-	Layers:
	-	`sha256:da8af35d6edc14f88cb057745f50bbcda55396924ee5a566902840f9e707eca2`  
		Last Modified: Tue, 01 Jul 2025 05:12:08 GMT  
		Size: 6.2 MB (6246015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e692ded868d185db6d9fa01b63773104809452cefd14f2374405ec99a495c36d`  
		Last Modified: Tue, 01 Jul 2025 05:12:09 GMT  
		Size: 54.5 KB (54471 bytes)  
		MIME: application/vnd.in-toto+json
