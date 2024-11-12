## `postgres:14-bullseye`

```console
$ docker pull postgres@sha256:0a8768e5b33a733a1ed3c016e62d271156965e5c7dd23eaf041499950b94c715
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

### `postgres:14-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:e429ea9f82245ae8bbd00f5eb290b4fd40cd05c46058bf68b593b059c31cc1c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141809241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e442916f82a1a29375ff2289906a9292208b8c5433783076fe13dd12d8b09ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:52:20 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_MAJOR=14
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_VERSION=14.13-1.pgdg110+1
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:52:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:52:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:52:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827e8f2ad49e0c7c8b6cbac979416075d7604c77a10df16010e6b3852526ab51`  
		Last Modified: Tue, 12 Nov 2024 02:33:56 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391b3210ec6486f1c37eba1b02f7adfb2737d4d2923851ee8778f52afa6d0c19`  
		Last Modified: Tue, 12 Nov 2024 02:33:56 GMT  
		Size: 4.3 MB (4308141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c37fabdfb21327fd6f35aaab70841c3623738fb86e92e17561cc21ad8f26eb`  
		Last Modified: Tue, 12 Nov 2024 02:33:56 GMT  
		Size: 1.5 MB (1472202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055183969d8127b01af28aca266748edae9d0b655f5dc7fb40d8fc16912125c1`  
		Last Modified: Tue, 12 Nov 2024 02:33:56 GMT  
		Size: 8.0 MB (8044563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5419759e45b7635f962cc4df67fa9cb2d60a2d8bd39a26974ede0003215f47`  
		Last Modified: Tue, 12 Nov 2024 02:33:57 GMT  
		Size: 1.0 MB (1038357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ec2afa0c35304dd837de98dd24554f987a2328c27936adb78ade61b5ffb9fa`  
		Last Modified: Tue, 12 Nov 2024 02:33:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7111c41b2a6e81238e43620343e38de7598127a82dcc0e89dd082a30dd42100`  
		Last Modified: Tue, 12 Nov 2024 02:33:57 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbeb2a644b763257400b974f891fb1fdfd8997c1d0b4be0eda2472496a3f3b1`  
		Last Modified: Tue, 12 Nov 2024 02:33:59 GMT  
		Size: 95.5 MB (95474044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3aa88edd82a7b64a145ba50c7ee84cd1c54a82cb426e467beb55f163c5766f`  
		Last Modified: Tue, 12 Nov 2024 02:33:58 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565857c1c2ad09f2d6017a94d3e2ed5559ec3eba558268a23cf96f2d7b22eb43`  
		Last Modified: Tue, 12 Nov 2024 02:33:58 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a98381de060b4df1aca14b30423739247188e69f4eb0142ac2e73829c2f6b1a`  
		Last Modified: Tue, 12 Nov 2024 02:33:58 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0d95ad4f69975efc4e9758a64b17cc24a236da607c74ef35e08112fe587705`  
		Last Modified: Tue, 12 Nov 2024 02:33:59 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b914f28eb542c6492314810104a53b9ce79927655008565e60d85b94a8085d9`  
		Last Modified: Tue, 12 Nov 2024 02:33:59 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:2d2b1c9e4fbfb6bd73dfe77fe1c26721531de4cffc2f3a376ab98edc6d661123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5955154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ffa357c3facfe586249afd5f7fcec81388bfb400a7fdfb48b30a7ed0a5a4c5`

```dockerfile
```

-	Layers:
	-	`sha256:88696f3b57ce97bf5a9692a564d3e98db7d9e9044c70983e11eb9093476e215b`  
		Last Modified: Tue, 12 Nov 2024 02:33:56 GMT  
		Size: 5.9 MB (5901167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:002f9cb4ff3c900e16360766844228de786d423443ec2399a34db8f1aea56fc3`  
		Last Modified: Tue, 12 Nov 2024 02:33:56 GMT  
		Size: 54.0 KB (53987 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:7ed19929877b9150bea9190a26089f84fdfba2c8d579282019d03d804970fdf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.8 MB (129750213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeca43210aa825c63eeb76de55b5593c49c6433179cbdf772057747fa9e8e19a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:52:20 GMT
ADD file:1a0a5d58e9eaa765a367c84b6a41097f2f807ca887b02e8a1a36fa504592a5e4 in / 
# Thu, 08 Aug 2024 16:52:20 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_MAJOR=14
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_VERSION=14.13-1.pgdg110+1
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:52:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:52:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:52:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:25eb86cb375819dcc30b18c185d2922f7f09900a247460cef95d47222230e7dc`  
		Last Modified: Thu, 17 Oct 2024 03:08:12 GMT  
		Size: 26.6 MB (26589555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de32be9c720a52367b74940afdb2d3e32862ccfc2147df092aa04adf6a42f26`  
		Last Modified: Thu, 17 Oct 2024 18:32:55 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ff15a87f66f6a908a6a576490ac34bf482409d26897b5135ebd6948998dd0f`  
		Last Modified: Thu, 17 Oct 2024 18:32:56 GMT  
		Size: 3.6 MB (3601804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ffc3f08141a457f9b4c53e40f5589900074e98aac2c94bd540d05315b969199`  
		Last Modified: Thu, 17 Oct 2024 18:32:56 GMT  
		Size: 1.4 MB (1439278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3822cf805c301d7318b7c57c3f006094cff7c26d51121b8fa2b0af8f43468a5`  
		Last Modified: Thu, 17 Oct 2024 18:32:56 GMT  
		Size: 8.0 MB (8044509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c36a59a85b06e2bd52d2ec2cb341155d250d3f2be1f9ac26b04df0c11e87acd2`  
		Last Modified: Thu, 17 Oct 2024 18:32:57 GMT  
		Size: 908.7 KB (908668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fbcffbce846085f1aeb1ca37200c908e3fec136a9e13d47da767b24f4c52ef`  
		Last Modified: Thu, 17 Oct 2024 18:32:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d07a02586715b0161df3cbe44f34958fd39fb7cc20fd8d25dd384432c3e9a3b`  
		Last Modified: Thu, 17 Oct 2024 18:32:57 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a134d7fbf6dff8466a84cb69b737da4ab11672b2b8ba4b0e1aed3ac1f074e3bf`  
		Last Modified: Thu, 17 Oct 2024 20:01:27 GMT  
		Size: 89.1 MB (89146041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a07d90b5b80253b95eb412f079695ad6c41a094010c58dfa6c070acca734706e`  
		Last Modified: Thu, 17 Oct 2024 20:01:24 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7858d10525193d00641a2f163dcba4912f0ce6c5ef8f1ff655ea1b93d15581fd`  
		Last Modified: Thu, 17 Oct 2024 20:01:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba773542357c44dd52d041b57dc931943f0c28289cb9240aad81b0789e4eb3b2`  
		Last Modified: Thu, 17 Oct 2024 20:01:24 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205ec8ed1f001b535387004fd96eac4409910c828768371bbb8e5aeae236abad`  
		Last Modified: Thu, 17 Oct 2024 20:01:25 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12f033a819b5a2335d10228291301df728d64201b24c280aada7695b586cefd`  
		Last Modified: Thu, 17 Oct 2024 20:01:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:6be0bd22175a63256e2d4111d392df06d91e1c8ec72252e4da68e2ccaaf70874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5946066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1709d3b2ce58ac6ae723aa2d3aa5194e065c44443e9e19855149ee2b67c6415b`

```dockerfile
```

-	Layers:
	-	`sha256:d42600747d7e2195457c5ab0df3ec0e58077ea7d94cad91c12acd9f341e2569b`  
		Last Modified: Thu, 17 Oct 2024 20:01:24 GMT  
		Size: 5.9 MB (5891999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:252d9c60e97f60617c17bbc00a04087550fb49f99ee94a9cec82419e824beda3`  
		Last Modified: Thu, 17 Oct 2024 20:01:23 GMT  
		Size: 54.1 KB (54067 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:893978a550cc9935b4f7aa52f36143ebdf1096092e717756aa50f8da01e601b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.2 MB (138218562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc78307ff1cab2b27caa63429a7ab5c8c4535d452243d23bfe976d9331c1e0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:52:20 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_MAJOR=14
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_VERSION=14.13-1.pgdg110+1
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:52:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:52:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:52:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625705541eb2c232ec6868052605994a58fd1783ec6af4d33d62324beabdd4ce`  
		Last Modified: Tue, 12 Nov 2024 09:10:50 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86ef8349dcde0e9538a12f2b24d39955b32259d90fd9226e4b09e83a23c6eea`  
		Last Modified: Tue, 12 Nov 2024 09:10:51 GMT  
		Size: 4.3 MB (4312806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408ba174abce076b100b1775066ae161d8f3c617fc9f8c9c5f24d6d9452e4822`  
		Last Modified: Tue, 12 Nov 2024 09:10:51 GMT  
		Size: 1.4 MB (1404090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1823cb8ddc148ec3c8dec960e1f98604509d055e771c71cd86a89084c02d09`  
		Last Modified: Tue, 12 Nov 2024 09:10:51 GMT  
		Size: 8.0 MB (8044346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4ea35053fdfd2a5d6a7dbf5900c78c319262391884c26e2fcc89dddee4be76`  
		Last Modified: Tue, 12 Nov 2024 09:10:52 GMT  
		Size: 1.0 MB (1026586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37385ec28429364a4917c18b2047c5afbbf75d0d2d92d13edaa098af60ce190d`  
		Last Modified: Tue, 12 Nov 2024 09:10:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c022894a4b9e1da9147eceeaa4898b06811b419e7f3efb2aefdf946bb2f7d4`  
		Last Modified: Tue, 12 Nov 2024 09:10:52 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50982bbe871c38ec79690d0decd9a722cff03b9098de8c3a0e9d6fa7dfecf8f`  
		Last Modified: Tue, 12 Nov 2024 09:35:36 GMT  
		Size: 93.3 MB (93318770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effa2e803799e385ab900ab29dc45cb246d15e23a66582ad671590151d0c22ba`  
		Last Modified: Tue, 12 Nov 2024 09:35:34 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4eeeeed0c07637cee2add6a0c662eafe070dfaffdf655214371e0ee08dc99dc`  
		Last Modified: Tue, 12 Nov 2024 09:35:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3e63c7fa0475fbe80f1a20e4875fc4a7ead86a7f5973f1251882c7a58d4088`  
		Last Modified: Tue, 12 Nov 2024 09:35:34 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa616b5267486a3cfcf2c240979e4c02f96d449bb67707566d1b9f2361581ac1`  
		Last Modified: Tue, 12 Nov 2024 09:35:34 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b44cb7648e7253895768797aa97926ea16ea86deeca5ca3e878310a5616cc05`  
		Last Modified: Tue, 12 Nov 2024 09:35:35 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:c9ae7dbc8c7da3eb07014cf5bb24ee3c649d99c7938cf8df065340f0ae491646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5961689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:796bdc346ef53ef32b345544be89796b15384375a2a0f1b8a149b43b8a156f38`

```dockerfile
```

-	Layers:
	-	`sha256:dba73cecbaf07b9dc242fe99e5d14b18db3d300fd6134f05a3e1561cffb34186`  
		Last Modified: Tue, 12 Nov 2024 09:35:34 GMT  
		Size: 5.9 MB (5907457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7fcca564ef41516e275015180647338f74c5f8a78874eb22e10a86d78756c56`  
		Last Modified: Tue, 12 Nov 2024 09:35:34 GMT  
		Size: 54.2 KB (54232 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:4b4106b8a71dd8e522987e8b13315c2b65fadc33f71de571318dcbdc884b5f07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.4 MB (144389843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2fe1d3995adbc2743f4ec952160bcbbb7308d9b7923152788a591a86696c297`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:52:20 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_MAJOR=14
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_VERSION=14.13-1.pgdg110+1
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:52:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:52:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:52:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2aea24d0416284c8bc498d91bac1c90e2bf12b01e7867f799161bbb874a8323b`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 32.4 MB (32423351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f1a74fe7267234a07d5a4f1b3172d165f35b4e5029b072b2836cc65c3cdd6c`  
		Last Modified: Tue, 12 Nov 2024 02:45:37 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfcf90824ea36173daa4cf105352199bae01d45aab90d60ded92c1bda603e5c`  
		Last Modified: Tue, 12 Nov 2024 02:45:37 GMT  
		Size: 4.7 MB (4719652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b76a0b8ad1d3ceba3fd4be7b7861d5c7d623d804c12b958a0cba897a3eebb5`  
		Last Modified: Tue, 12 Nov 2024 02:45:37 GMT  
		Size: 1.4 MB (1447783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a9c3fa45ec5cac55b0d1d067da00695e20f6a1f094aa017b5fecb8b3704cf3`  
		Last Modified: Tue, 12 Nov 2024 02:45:37 GMT  
		Size: 8.0 MB (8044461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1578111d3c5f43df926284fd305b5e2f08c829dbf52673b413c3013ecdae26`  
		Last Modified: Tue, 12 Nov 2024 02:45:38 GMT  
		Size: 1.0 MB (1028888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6bf0b74a292a06d34d4bcdc3e848c9d2247334d2dc07e1940b2a7953c94d8a`  
		Last Modified: Tue, 12 Nov 2024 02:38:25 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677293d54d52db83786ae21900834ee5783fbb69f518251b5892245c05be1deb`  
		Last Modified: Tue, 12 Nov 2024 02:45:38 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b0cec9208f2b4fafb4125c7a0b12f82ed13b1a248bcd9baf38d509ca4a5fb8`  
		Last Modified: Tue, 12 Nov 2024 02:45:41 GMT  
		Size: 96.7 MB (96705343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb33ddb60f618c4cf4962fd4a23d4f2ea1fee82e12f6f75e1e8b6986b85c5be2`  
		Last Modified: Tue, 12 Nov 2024 02:45:38 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46cdd67b4fb0749215e1e24600541dfbcdc508769dfe63a5d9eb21bc744b0b01`  
		Last Modified: Tue, 12 Nov 2024 02:45:39 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e5bf2fd7979b93f584ff5d7818b580e521ed0a83cbb517e1ab05039fbca0787`  
		Last Modified: Tue, 12 Nov 2024 02:45:39 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42023c9d0636930357ae7869ae29c34b85cbbf4c8bd930aa3be144235345764`  
		Last Modified: Tue, 12 Nov 2024 02:45:39 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717bb3c32b97b6de1de7fdcd8aeb81b3603c349d9d8736880ee7e55a8dfa9599`  
		Last Modified: Tue, 12 Nov 2024 02:45:40 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:940dbb6634e4cb0eb70bb0dabbf9f59af1b93fe5ae814c494f6f7376c088dc72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5962630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84d92c2a9f27d1ad03a985d25c32a5ce7888a3955faf5c206b7c86edb6b846af`

```dockerfile
```

-	Layers:
	-	`sha256:5213d271ec46f5ffd1dc35f8116997af3d60fef784d7171dcfeac3b86a1a64e0`  
		Last Modified: Tue, 12 Nov 2024 02:45:37 GMT  
		Size: 5.9 MB (5908687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e508c1f3ee27cb4ddcf1318206f2720df2c8e99a76f3132b9ea26d3c1a8c13eb`  
		Last Modified: Tue, 12 Nov 2024 02:45:37 GMT  
		Size: 53.9 KB (53943 bytes)  
		MIME: application/vnd.in-toto+json
