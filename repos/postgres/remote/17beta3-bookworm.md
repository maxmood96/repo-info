## `postgres:17beta3-bookworm`

```console
$ docker pull postgres@sha256:7d07a4f00f87ad8ceb3e07c953360edcb4f0dbf200b69d227a241b99b3a90ac3
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

### `postgres:17beta3-bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:ca81c503801f85a6446b7d11899d7ce7720aa74027e1f500cd117d02ede2d377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154506094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b95c1c78fd342d6be16fbea8370cf40eb8240619c5aaad786d1044a1704f682d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:34:59 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Thu, 08 Aug 2024 17:34:59 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PG_MAJOR=17
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PG_VERSION=17~beta3-1.pgdg120+1
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:34:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:34:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:34:59 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:34:59 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:34:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1189021b00feb8826ca02c166d3de742f32ff2c4ced82666fc85ba474c5b27f8`  
		Last Modified: Wed, 04 Sep 2024 23:09:11 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e4810feb1414aa3d60fa145288550550547bdc190edbd0c15ff7ef2a95f084`  
		Last Modified: Wed, 04 Sep 2024 23:09:11 GMT  
		Size: 4.5 MB (4533697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7c372d53b0d03b68d18cbfdea069232878c7c1787f4ef4d3f0302d96cdf8a0`  
		Last Modified: Wed, 04 Sep 2024 23:09:11 GMT  
		Size: 1.4 MB (1446680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5b0e2238b181da8e409ec25a608e2fcefcc9765093aab7a5fdde2c6bbb2da7`  
		Last Modified: Wed, 04 Sep 2024 23:09:12 GMT  
		Size: 8.1 MB (8066308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350ae2ba815b366466bfc8f925d3c0ddee2352a574cdc6c460feba42cb8aae07`  
		Last Modified: Wed, 04 Sep 2024 23:09:12 GMT  
		Size: 1.2 MB (1196044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f550a1cfbe75e985b9e2fe089f63e5c1a2b0f63c1d515ae2e607232c4fd3b2`  
		Last Modified: Wed, 04 Sep 2024 23:09:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c88b6ba102b99f37ec5dcb18dcbba7d49e14178e0595e6b56c32ab417333b822`  
		Last Modified: Wed, 04 Sep 2024 23:09:10 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb96c7775af3959fc9c1ac85d57261ae955b877fa6db18e2df1322792080865`  
		Last Modified: Wed, 04 Sep 2024 23:09:15 GMT  
		Size: 110.1 MB (110116312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfa7d47159c55fccbea007c93addcadfec02f1a96775bb5e3707b479ea02ab3`  
		Last Modified: Wed, 04 Sep 2024 23:09:13 GMT  
		Size: 10.2 KB (10245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f8cb7e3e9244fc2e96fc869997e4d4676a5ed8390aa7d63b7b2ed13d350a96`  
		Last Modified: Wed, 04 Sep 2024 23:09:13 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7860aeb5d7a49315017b25af96af18f823305327b7ddee0f03c6aef3bf9707ab`  
		Last Modified: Wed, 04 Sep 2024 23:09:13 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc785132a0fca2df64050bb56ee7d9c669bcb9a29a7f2d63c11a12ac3351bf74`  
		Last Modified: Wed, 04 Sep 2024 23:09:14 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f84eaad120d67eb689726d0fd5d976f9825396a799e0a0b04f31b52d9e2a0b`  
		Last Modified: Wed, 04 Sep 2024 23:09:12 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta3-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:f056c16836d08afcec3e383c20dbe2d812768e9c56f202a2bd7c2457a00813f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5814591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15cb5b4624a59dc38a36097041ef8de1080e639acfb408ae48378a08b51a1a0c`

```dockerfile
```

-	Layers:
	-	`sha256:db380676986939cdce66a09ac77ba96af0c913089153460662b5bb07a1d2a352`  
		Last Modified: Wed, 04 Sep 2024 23:09:11 GMT  
		Size: 5.8 MB (5760724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40075eeee4c46045c9b36d50a1388049a32af29bba2b03db1cfd3144c48d6d5f`  
		Last Modified: Wed, 04 Sep 2024 23:09:11 GMT  
		Size: 53.9 KB (53867 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta3-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:561bb7b7aea4e47b3be3ef59593a67571a3644aa27af28228c5619f1386c4dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.2 MB (147235503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc008c95e34f6379ebf0a706bac43d2001c44d04e4ae139cb9ca8a81b173a71b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:34:59 GMT
ADD file:c162e60b24ef6aed489ba1986f407fd9ab4ace659e0e3e6759ffac7eb0b7f770 in / 
# Thu, 08 Aug 2024 17:34:59 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PG_MAJOR=17
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PG_VERSION=17~beta3-1.pgdg120+1
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:34:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:34:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:34:59 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:34:59 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:34:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:44990bd21e0c5db65674bd030d12ea2461a14f2bb4007469bc2667c8535a8357`  
		Last Modified: Wed, 04 Sep 2024 21:51:32 GMT  
		Size: 26.9 MB (26887411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9ae4c474ed95cd628af882b052c523086cc21ddc0f24ca9b6f8eca4312960b`  
		Last Modified: Thu, 05 Sep 2024 05:48:45 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3023e0032654f8aed6b728bbe7febaffd2807f896f9f134715dc315c905eb3`  
		Last Modified: Thu, 05 Sep 2024 05:48:45 GMT  
		Size: 4.2 MB (4150914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db5800f5b661f501fdde83e66e50910fd6072841f01392ff5fd0a36aff48cf8`  
		Last Modified: Thu, 05 Sep 2024 05:48:45 GMT  
		Size: 1.4 MB (1423884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815cd609b0d2444b8d98a1915bf7cad5e755ec79d47470f84c541d7a31a1fbc6`  
		Last Modified: Thu, 05 Sep 2024 05:48:46 GMT  
		Size: 8.1 MB (8066403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a7cb2e0c74c89d4f114cd0a22f9d61d3e0ab92973ef09055b2bddf249bf984`  
		Last Modified: Thu, 05 Sep 2024 05:48:46 GMT  
		Size: 1.2 MB (1194866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085b70053bc41f4c2a8d0d5a7da4aa763d1367f13f8a570840911645523f2a15`  
		Last Modified: Thu, 05 Sep 2024 05:48:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be49688ae1ba33a431c4a7bc035a0f29ffaff6c7c9bc16bd0dea362b144f6c74`  
		Last Modified: Thu, 05 Sep 2024 05:48:46 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591d30be5224ae48b9799c17f5337fdd32c381e50dabcd46ec056b5ea6d109d2`  
		Last Modified: Thu, 05 Sep 2024 05:48:50 GMT  
		Size: 105.5 MB (105491444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8785d2f2d91369795103c9cfaec2617f85255d203ba612b79ff278a931d2c096`  
		Last Modified: Thu, 05 Sep 2024 05:48:47 GMT  
		Size: 10.3 KB (10251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85089a71bf0bb1688f51c70418a6c32e7020d73b67dc495d6cecd23bde06f973`  
		Last Modified: Thu, 05 Sep 2024 05:48:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337a002973a4825d11b6d625b7b17fd9ae0d2c72f39c317b91e56d202f1ef4f3`  
		Last Modified: Thu, 05 Sep 2024 05:48:47 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6f9041ba9e7b1a95075d5d0a2d713fa913c6758e40e2c5bfa5b96395426729`  
		Last Modified: Thu, 05 Sep 2024 05:48:48 GMT  
		Size: 5.4 KB (5425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60438237197bf8d224cce32046d97df51368d2184bbb623dac7b1fdf5ac4ccc7`  
		Last Modified: Thu, 05 Sep 2024 05:48:48 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta3-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:0fbc95a83915e3529beb482d1d2e3553006f38d6d86452fcb13b33d8c0b0b63d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5832169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686ad71aa2fb2d4390c1ebabcaa6e6538ea40d3112c253c47ad8a8a2e9552d0e`

```dockerfile
```

-	Layers:
	-	`sha256:1312fb79a8648bfc738ae0756671866ebe44f3964c229f065dd2d909f308a6d5`  
		Last Modified: Thu, 05 Sep 2024 05:48:45 GMT  
		Size: 5.8 MB (5778105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3233e8170270c5e6844f9be1766c30fd6dd1c320df336ffda82b2994c30ec1d3`  
		Last Modified: Thu, 05 Sep 2024 05:48:45 GMT  
		Size: 54.1 KB (54064 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta3-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:e487127a1e58362477ccb27d26dc66116b772e5ebf263b7af0886e0d9f87e00e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141933599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d18a92ef6cd3f506e32a07637784883e8873d361ff29b9f31f28fb72bd6381d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:34:59 GMT
ADD file:90772cdf7913d0ef1bf41e513a6205fa3195a1583476a536ec770e8381f77ac1 in / 
# Thu, 08 Aug 2024 17:34:59 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PG_MAJOR=17
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PG_VERSION=17~beta3-1.pgdg120+1
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:34:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:34:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:34:59 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:34:59 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:34:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:670631d7a00e03a2701d6b6aff29204afdeff4cd2da308462d92f5743156ede1`  
		Last Modified: Wed, 04 Sep 2024 22:01:44 GMT  
		Size: 24.7 MB (24718265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50662b3d2205bfde48c7c7ee492df609b20867a450a872a8e34fae1467209e84`  
		Last Modified: Thu, 05 Sep 2024 06:53:30 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bccbd6b6c11095d20b4078ffe578897cefad73d15b33fc0a3eec8093f041eb2`  
		Last Modified: Thu, 05 Sep 2024 06:53:30 GMT  
		Size: 3.7 MB (3742532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f537b63140972adb053d00e6965e0d19ac96f9fcf53cc647875e3499d7e072`  
		Last Modified: Thu, 05 Sep 2024 06:53:30 GMT  
		Size: 1.4 MB (1413612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818684dea80d219b3b50b12b97fd00572b2325ae91d47de8905c8fb5a0ddd9d4`  
		Last Modified: Thu, 05 Sep 2024 06:53:30 GMT  
		Size: 8.1 MB (8066297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efebd8ca0e3760211b0743352214ceaf97423c6db72d91fe0c68e34edb58328`  
		Last Modified: Thu, 05 Sep 2024 06:53:31 GMT  
		Size: 1.1 MB (1066972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f3b1200790e6e3387c0d7caaadab6f6b8ec7d7b34ec10f50f3dea452ba6b39`  
		Last Modified: Thu, 05 Sep 2024 06:53:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01488d49e7609eeb21c76d857556114a92d131aa883ce884d9e9bb1b7f8b9955`  
		Last Modified: Thu, 05 Sep 2024 06:53:31 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03a21ab448c46a990922aed1f4007da5c84ca603ae8fb3cb11bd52f74d1a896`  
		Last Modified: Thu, 05 Sep 2024 06:53:34 GMT  
		Size: 102.9 MB (102905347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b20f56a4765ed38e76469d0890f3701be2c8143ba6cd168d32a40df5a4f111`  
		Last Modified: Thu, 05 Sep 2024 06:53:32 GMT  
		Size: 10.2 KB (10250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a88f207bc46f8f1b7953d6df0431fe2d8be124b04b046e13ed17b6ad63f239`  
		Last Modified: Thu, 05 Sep 2024 06:53:32 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1e632fd810a671a83c64059a4dfdde9959da06976aa538eb290b4d4b5f0f44`  
		Last Modified: Thu, 05 Sep 2024 06:53:32 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9710b4e4d8376831c696726a29535e3ef65ef1e3e3acee6bdeb5e321711502cf`  
		Last Modified: Thu, 05 Sep 2024 06:53:33 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63fa323f68cac8b3f4dca8c49e397119a54a267d3b3f149bb3a5f20cd975d936`  
		Last Modified: Thu, 05 Sep 2024 06:53:33 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta3-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:89fb952eb78f36e15d90efaa141a6099f9f462a8deb3036c0a47dc94fefb5768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5831838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e2c9a4c3b61b496c23e86c3e77a6fe853971107c86fc357ca10523dcc201bb0`

```dockerfile
```

-	Layers:
	-	`sha256:7c16c91d48236bd99313c22d78ce570d2b46515768e4c98ef9d4f05bfff18b73`  
		Last Modified: Thu, 05 Sep 2024 06:53:30 GMT  
		Size: 5.8 MB (5777774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee23e2ea0c11677609221b5e849e265017060c7720b2cb010a6f07db3e7242e5`  
		Last Modified: Thu, 05 Sep 2024 06:53:30 GMT  
		Size: 54.1 KB (54064 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta3-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:94d61abf98eb2d1165560cd22aaf11f96f2c4ba4ab868107940dd38c61959825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152669660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2d7c3b9ecd47e322e441e11bd5292ffaad8a62b5ccd0e5f8a81ec93d4586f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:34:59 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Thu, 08 Aug 2024 17:34:59 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PG_MAJOR=17
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PG_VERSION=17~beta3-1.pgdg120+1
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:34:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:34:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:34:59 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:34:59 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:34:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7495dd9a7534dc031e9ab69954fb433411b3a5e2d13b6b7aa3ef1d0ea900e3c6`  
		Last Modified: Tue, 13 Aug 2024 09:30:37 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315e4f3b46c2cf50f4850869012863150f85f947526b816238e127d72e7c2543`  
		Last Modified: Tue, 13 Aug 2024 09:30:37 GMT  
		Size: 4.5 MB (4499111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba82aab0ebf7e429fdfca16774a458f150afc39d97d8fdddbd5a2eef016d56fb`  
		Last Modified: Tue, 13 Aug 2024 09:30:37 GMT  
		Size: 1.4 MB (1378674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23c85d6eacd685eaa7458227091cfa23c0e25707befe09f2c6717f0dd862484`  
		Last Modified: Tue, 13 Aug 2024 09:30:38 GMT  
		Size: 8.1 MB (8066317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98eb4aa071fb95db04ba96eb0269f689ee05f25335128845cfcceaa3359494f`  
		Last Modified: Tue, 13 Aug 2024 09:30:38 GMT  
		Size: 1.1 MB (1108703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e138aa7cc779cd901cba0297fb6a61a13cd65bfd4edf9905e82bf694fbcfbb`  
		Last Modified: Tue, 13 Aug 2024 09:30:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d91cf4cf4f79f8fabf0a7711f3d23c3df3ee58b387038819671894ceb68dc95`  
		Last Modified: Tue, 13 Aug 2024 09:30:38 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211acebcea349d1fe467f8e410a75c1d9ee95c9fce2e7ebfb7ce03ba2eb884be`  
		Last Modified: Tue, 13 Aug 2024 09:30:42 GMT  
		Size: 108.4 MB (108439767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f38ae83649721e2af5cf94c1a72fb47139bea37ce57971ef3456e6b77ef68f4`  
		Last Modified: Tue, 13 Aug 2024 09:30:39 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8f8d9d9cf7b601a7b65400412fe230c969ad416ec684d041f56975242e1906`  
		Last Modified: Tue, 13 Aug 2024 09:30:39 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15fcd8f8c0c1c90df763b238bc4567bba68facf7a4b2bb2b2fab658211dec4c`  
		Last Modified: Tue, 13 Aug 2024 09:30:39 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cf6271e55977f904f9aca9c2930500c287a420544f160952a0dffb7b175113`  
		Last Modified: Tue, 13 Aug 2024 09:30:40 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f48bbc4325b428e75481f41570cfce8af0541b9673e6fc4535b513d9fd3e558`  
		Last Modified: Tue, 13 Aug 2024 09:30:40 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta3-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:b5401f0f7fec5c9e17bea74763984705037c39f54d78c887335b6ec96f435a50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5821193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a091a3c30a3d6a9873e76b5b48a875abc94cfe66d7f1f30e8cbcefa516bebc1`

```dockerfile
```

-	Layers:
	-	`sha256:65ce06d28bd2f2a2a4c7fbc4cc6e9e830efe87a0c65e0efeba319f08f5c6a908`  
		Last Modified: Tue, 13 Aug 2024 09:30:37 GMT  
		Size: 5.8 MB (5767041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:407c7082fc9a09b348c2a3e6a7dabba10168b468a55dc117dfd0a128061112f0`  
		Last Modified: Tue, 13 Aug 2024 09:30:37 GMT  
		Size: 54.2 KB (54152 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta3-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:28d614dbe71a96ab1df8a08c45c647a1b2ac9f3578b3e5bc92513e4bb64bde9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162677090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46a1280063efc082196d3e563f3867017171b07f0d84b588e3f971174a7ab411`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:34:59 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Thu, 08 Aug 2024 17:34:59 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PG_MAJOR=17
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PG_VERSION=17~beta3-1.pgdg120+1
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:34:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:34:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:34:59 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:34:59 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:34:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71e8f13f24224c571d63ac38bdc989b58362626b2360f80f9c2b43d884d10ac`  
		Last Modified: Thu, 05 Sep 2024 00:22:42 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2be089a3f6577756084257b19c66463a9ed3d7f80fd4c5293daf5c70976b14f`  
		Last Modified: Thu, 05 Sep 2024 00:22:43 GMT  
		Size: 5.0 MB (4965044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e529139c62d7f5e0405f37f6d3458c358c49a3fa0a7758d28a4222ef5fe63f18`  
		Last Modified: Thu, 05 Sep 2024 00:22:42 GMT  
		Size: 1.4 MB (1422113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83b48ba92d5ce9238e5dd4e8334eafeabfbbbf18c47fdbbf25de68a4d11423f`  
		Last Modified: Thu, 05 Sep 2024 00:22:43 GMT  
		Size: 8.1 MB (8066314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c931c49153367521397eca5fc99bdd2fb4fd56bdec853b74d28c1c402293e7`  
		Last Modified: Thu, 05 Sep 2024 00:22:43 GMT  
		Size: 1.1 MB (1137137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3684d24c9a9415c7630d991092fd434b994a908d0fab76f1f659f8752d4a5f`  
		Last Modified: Thu, 05 Sep 2024 00:22:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b028da6fc31a978d84cb0f824629016a8a9f5863fb140a4a61c83ada3c4751`  
		Last Modified: Thu, 05 Sep 2024 00:22:44 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7205bec7ea79990252d860712999a1dea47328d2cfa64c651dd10a2669a039e7`  
		Last Modified: Thu, 05 Sep 2024 00:22:47 GMT  
		Size: 116.9 MB (116921611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65337bc4bb986f841707886b814f1e8f26695064252217292c4c7542d3046f04`  
		Last Modified: Thu, 05 Sep 2024 00:22:44 GMT  
		Size: 10.3 KB (10251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95501f21a7f0c6c409accf97af4010366509302189b0c400868f047ace8e0ee1`  
		Last Modified: Thu, 05 Sep 2024 00:22:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61e941dcb2a3504e17e3fa947a4377c0b3cefb587f68fdbb87d05cd8e2eb977`  
		Last Modified: Thu, 05 Sep 2024 00:22:45 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d882174b44c263365bb06f27a3c7881415ff45d84b4fbfd69ca44275e49df55`  
		Last Modified: Thu, 05 Sep 2024 00:22:45 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408a6b27652bb3f814ba62aaf0dbe9d76dd985285215c3abfcf5891e49b46774`  
		Last Modified: Thu, 05 Sep 2024 00:22:45 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta3-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:69988b09a028dc25eb85714551319bfe12d4271ea4437954d2d6af10a468cafd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5830010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32f82cbbe7fc026e2e7c3c315f9fa2c83b63f6a6e81aaa9bc31e5e51808c1f2b`

```dockerfile
```

-	Layers:
	-	`sha256:d35d478f0d8c145934cf6998bb44ad5edb92c85bed423c8a9052d66a0d7258aa`  
		Last Modified: Thu, 05 Sep 2024 00:22:42 GMT  
		Size: 5.8 MB (5776184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d83c0a693444533856d9ab2ca2873b330faae270bf760808daf6df5598c87a9`  
		Last Modified: Thu, 05 Sep 2024 00:22:42 GMT  
		Size: 53.8 KB (53826 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta3-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:78e4802e6183ef8fac36d105cd34b257628030015bc0c9fc0111e60567a2ee6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.9 MB (149915365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3415bdbdfc9c62edc613dd38c007ed19ccdc4fdcac06ceae3605df0f726e91aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:34:59 GMT
ADD file:2fad80cfc89f7b624d81eb445f9c64e4cd3f190b85d89f40c33eb7e4bc562c6d in / 
# Thu, 08 Aug 2024 17:34:59 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PG_MAJOR=17
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PG_VERSION=17~beta3-1.pgdg120+1
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:34:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:34:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:34:59 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:34:59 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:34:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e8ebfef8c6b7f6250b54eec0d5d1ae5d66f60f418704f4094cb9291dc214be0f`  
		Last Modified: Tue, 13 Aug 2024 00:22:29 GMT  
		Size: 29.1 MB (29124941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93f7560d761ca88a87a34da8b7cbd12df3217df3fb0e1bbaa99c377af456e1a`  
		Last Modified: Wed, 14 Aug 2024 04:56:18 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d73f30a6cf5da5668a716fa72f716c9b45ef0623ca8e200744b07f433624c6`  
		Last Modified: Wed, 14 Aug 2024 04:56:18 GMT  
		Size: 4.5 MB (4475045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6bd9010f927a2d05d2a4ab1f6503af28972f57a34de059e6fed8b492b2ba0b`  
		Last Modified: Wed, 14 Aug 2024 04:56:18 GMT  
		Size: 1.3 MB (1333794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3e69d0bd50f0ecb7c9165e57462b6a8f7344b36df946e528a33b7d7d7404f5`  
		Last Modified: Wed, 14 Aug 2024 04:56:19 GMT  
		Size: 8.1 MB (8066404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42009232c6e75dbeab321cd15501b8d9416b4d13c778898b8fb1204e3b12a031`  
		Last Modified: Wed, 14 Aug 2024 04:56:19 GMT  
		Size: 1.2 MB (1182639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a192bc2a0130a14cbdbc53657704cf90a5db7903be57a5c7758e84a8e4478d48`  
		Last Modified: Wed, 14 Aug 2024 04:56:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9a20c1c6c88ec3a909047fea0619ba7a6e53c07b22272323856a12aaab4ef6`  
		Last Modified: Wed, 14 Aug 2024 04:56:19 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce7af84ae690336e3b8ae244aa0f93c27a26415ff77fce88bbfddd1e0bef653`  
		Last Modified: Wed, 14 Aug 2024 04:56:30 GMT  
		Size: 105.7 MB (105711968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c220192d652b5bd51db308b3942f2a28b722134387800caa87a3f266573221b`  
		Last Modified: Wed, 14 Aug 2024 04:56:20 GMT  
		Size: 10.2 KB (10247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4c72cc7797e9a5a7f7461716adff5077a6551f2707369cd8bcfb9456b31be5`  
		Last Modified: Wed, 14 Aug 2024 04:56:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606593d35efa063bb992efb9fc7ffeabeba0db868d9b0a1646cff0bc91ac9c87`  
		Last Modified: Wed, 14 Aug 2024 04:56:20 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd46024bfc055bb32fd676162a6479787e2c842203cc38e73a38511a5078301e`  
		Last Modified: Wed, 14 Aug 2024 04:56:21 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cd726183adc337038feb1e3fa64196799d406d23b521d3ec7d0c56799a6562`  
		Last Modified: Wed, 14 Aug 2024 04:56:21 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta3-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:07a2ad1f08da4f58f82a157913f3ce25d60e961e7c6578318c42c8f8aad5e769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 KB (53720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a33b939c067bbe36c087b3186015017809fa4a475f6e7ae1c011b49d9a1d607`

```dockerfile
```

-	Layers:
	-	`sha256:925399bcef35308bc1b146cdb30cd590472d3b4f97d4f67b36c3a6ff4f0ef9fb`  
		Last Modified: Wed, 14 Aug 2024 04:56:18 GMT  
		Size: 53.7 KB (53720 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta3-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:58b95142481d6ddd97ff8e82a17a98eca30cbe8a45bd92fd2260630ab280fa8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166754415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4fc6c29182db56658a2a7c88d6757120cd2f004091a0a55bd9bbb28bf23af2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:34:59 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Thu, 08 Aug 2024 17:34:59 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PG_MAJOR=17
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PG_VERSION=17~beta3-1.pgdg120+1
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:34:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:34:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:34:59 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:34:59 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:34:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7091a65b3af01393bb237a0dd5e1eb6eb6722714679ff5876b084574dc17706`  
		Last Modified: Thu, 05 Sep 2024 03:09:50 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800ed3f152dd7bf42d96276af7a9d1ce719fd2a3bcef42118e305c36e12221e1`  
		Last Modified: Thu, 05 Sep 2024 03:09:51 GMT  
		Size: 5.4 MB (5368161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075f522e2a21fb72d03df834c71e2fbf45a6ec691eeae0decaa36ad2bc0652b0`  
		Last Modified: Thu, 05 Sep 2024 03:09:51 GMT  
		Size: 1.4 MB (1368567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6dd0b39792e48b0b4936cc2735903bd6daaa6f632a856cfefabf8c621eb16ef`  
		Last Modified: Thu, 05 Sep 2024 03:09:51 GMT  
		Size: 8.1 MB (8066345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8784a13cd11f3237242eb57895bd508e0f5d410cc1017caeced52945e8b97322`  
		Last Modified: Thu, 05 Sep 2024 03:09:52 GMT  
		Size: 1.3 MB (1283474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35aba7bcf3d315f55153104351b2edee8c0103834595bc782d25cbec20f5001b`  
		Last Modified: Thu, 05 Sep 2024 03:09:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f872029cf50f514a97ad2dc9fb914632e626f454e72f4795b87ad68dabc7f3`  
		Last Modified: Thu, 05 Sep 2024 03:09:52 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae4c6d889abf9f1d52917b3f0fed3c49c2128864539fae548ac2e2765a04ea8`  
		Last Modified: Thu, 05 Sep 2024 03:09:55 GMT  
		Size: 117.5 MB (117524943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e945717825c22f54c97851023f02718b25560bfa15953f609d69aa76d991aaf`  
		Last Modified: Thu, 05 Sep 2024 03:09:53 GMT  
		Size: 10.2 KB (10242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a92b1832da4dc595d92dd637fcc38d3cf7f266a7501f5a862b69d079c32f085`  
		Last Modified: Thu, 05 Sep 2024 03:09:53 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0bf61fced1c7b5147fc8e700fae1d87ada933219c2f098999631e9486c0c0c`  
		Last Modified: Thu, 05 Sep 2024 03:09:53 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c5792d4437dda7f76c3dfa53e34b20d1251109c2cc43559623aa8f236b252c`  
		Last Modified: Thu, 05 Sep 2024 03:09:54 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba9a37746bd81724e7335cf586c5fdf4461f30a5dd82611b4043508a7121025`  
		Last Modified: Thu, 05 Sep 2024 03:09:54 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta3-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:1a70213bc190b09e9f5b6d8a3e9132cf23d13a7e4fa4cd937a92e106e6438cd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5821856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da25847998dcb29783643f5296fb3bdc5ac94d08d3b7146fd371c3cfd297809e`

```dockerfile
```

-	Layers:
	-	`sha256:7c9f1375d59f532f135a1bb45c4bf5b712b29b4bdf952ef243fd4bfa44048bf1`  
		Last Modified: Thu, 05 Sep 2024 03:09:51 GMT  
		Size: 5.8 MB (5767941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4134fee8d6e748186adfd50bd2e7794cafa848fd3a936baa4c1754bc07202135`  
		Last Modified: Thu, 05 Sep 2024 03:09:50 GMT  
		Size: 53.9 KB (53915 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta3-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:7aefc9c9abcbae9c72a811550afafeab001041c758b964ebd6944bde7a8cbc44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.0 MB (160017163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:820942c4daeb5dafa126aa03ca98987ebe798d428ca728e0270453dda2be2912`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:34:59 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Thu, 08 Aug 2024 17:34:59 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PG_MAJOR=17
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PG_VERSION=17~beta3-1.pgdg120+1
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:34:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:34:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:34:59 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:34:59 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:34:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a71df81faca4120f677817bbd051e773830b054e72626158c76b4df335fa5f5`  
		Last Modified: Thu, 05 Sep 2024 05:04:02 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697d886823662fa64c552d6ec433809a3b77ca9bb1355ec5cba3160fa530a060`  
		Last Modified: Thu, 05 Sep 2024 05:04:03 GMT  
		Size: 4.4 MB (4391038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8a2ee793ee906d11de05d1a1778d1a245ff0121f2521f0fcbd8c5dbc63acbd`  
		Last Modified: Thu, 05 Sep 2024 05:04:03 GMT  
		Size: 1.4 MB (1412694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a43f4933e2b533e4734d02a6cf60a19522e291bd446eabfa1ecb8031471b1beb`  
		Last Modified: Thu, 05 Sep 2024 05:04:04 GMT  
		Size: 8.1 MB (8120458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29a493f58318811251ef710e6785725733972cd6f778208e7a7663b01cf0128`  
		Last Modified: Thu, 05 Sep 2024 05:04:03 GMT  
		Size: 1.1 MB (1096735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd2aad8c7ec9a88dee775539c06b9f365c7fdbec866fd84fe4d372a6dcc4d14`  
		Last Modified: Thu, 05 Sep 2024 05:04:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e0224b48d801dc7fd91c13ef65aac3ab8b4b00134811da28553542be3631fc`  
		Last Modified: Thu, 05 Sep 2024 05:04:04 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8045357b8e30cf921d30769d13e08e7734913284c2759c2a5d4b1051c68dc803`  
		Last Modified: Thu, 05 Sep 2024 05:04:06 GMT  
		Size: 117.5 MB (117485354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d68801ca79a30dcb40bd52efd5e3c69083d321559d300ce8693dec7b0d618b`  
		Last Modified: Thu, 05 Sep 2024 05:04:04 GMT  
		Size: 10.2 KB (10243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f863ba4cf4afa20b7e6746a6286aa3a1846ccdb93c4111b4cfc9abc87d35e08`  
		Last Modified: Thu, 05 Sep 2024 05:04:04 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4636d547d015a17333dd9668e00ba9c1fd6df62b27657650c5ce22b8c108db68`  
		Last Modified: Thu, 05 Sep 2024 05:04:05 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8b4d235e08bbc97e74d42f81bb1ace70cb85098f11f9c404569b54945c231d`  
		Last Modified: Thu, 05 Sep 2024 05:04:05 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd276d8d88baca8d03387051c42046a9db1ee221d301ddf9f78b119a41de4d2`  
		Last Modified: Thu, 05 Sep 2024 05:04:05 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta3-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:247d111366afb16352ddc477e3b5caff52025ae8e4d0443dda46b5c71baf1be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5813985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c2ab87d66b171c7185982e50c8f67b846264854e73f1d387e919ba391cba15b`

```dockerfile
```

-	Layers:
	-	`sha256:450c436ed8c8d782489902542d79334d5e764a67b3c33e7849fb9b93f7b04183`  
		Last Modified: Thu, 05 Sep 2024 05:04:03 GMT  
		Size: 5.8 MB (5760118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9a29e81486d4b753bb3d04b3d88970146bf5f1af61fe3996390e6ff67cd597e`  
		Last Modified: Thu, 05 Sep 2024 05:04:03 GMT  
		Size: 53.9 KB (53867 bytes)  
		MIME: application/vnd.in-toto+json
