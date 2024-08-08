## `postgres:17beta3-bullseye`

```console
$ docker pull postgres@sha256:b71602fb58c611bb586f6b00bb36e518ab68925a9922dceb6ce3e36217fae936
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm variant v5
	-	unknown; unknown

### `postgres:17beta3-bullseye` - linux; arm variant v5

```console
$ docker pull postgres@sha256:353e7d6218dc803e74cf754fd0fec5ded23eb6ab50c90517fe7bb894652a3298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139034509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b0584c84004af375fcab072abde782a12f101c9d7fec817fc02b81773e906f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jul 2024 23:57:24 GMT
ADD file:56b9d2d0e0360f64ade3cbe073b446e10c8e6bd253b761c16b5f319a8103d181 in / 
# Mon, 22 Jul 2024 23:57:26 GMT
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
ENV PG_VERSION=17~beta3-1.pgdg110+1
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:5b04226d50f1c00a6c8950192ad70a2038016868ab6ffb162ad447e35e67a3cb`  
		Last Modified: Tue, 23 Jul 2024 00:02:06 GMT  
		Size: 28.9 MB (28930588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc751e343fdac6420d03ca6aba7b7203c64f459884877bbda5a9f08cb4562a2`  
		Last Modified: Thu, 08 Aug 2024 19:36:05 GMT  
		Size: 1.7 KB (1681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9ad34ad9ea0805efb5831c8fd7352fffebdc7730a8f33e88979aac5cffda36`  
		Last Modified: Thu, 08 Aug 2024 19:36:06 GMT  
		Size: 4.0 MB (3991607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0e2b6fe97724233a2c948d81554a249e031ccbbebf471555d14f939764af64`  
		Last Modified: Thu, 08 Aug 2024 19:36:06 GMT  
		Size: 1.4 MB (1449196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e748d04946305900cc338534ed8baedc7c066d55d6542db003d6f48136d78e`  
		Last Modified: Thu, 08 Aug 2024 19:36:06 GMT  
		Size: 8.0 MB (8044379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ec16bf3b5687c7f7c9ca5456176ef460917e9e423c154cf7647060be441b86`  
		Last Modified: Thu, 08 Aug 2024 19:36:07 GMT  
		Size: 1.0 MB (1034825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a648f7c543f33bf6cee210828f43d0d593b9cd466a8ce9372462f93d4453cab`  
		Last Modified: Thu, 08 Aug 2024 19:36:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dbe19ec3123a5b23efa019792214d8583302c72298c0db655c694a26c7cd05`  
		Last Modified: Thu, 08 Aug 2024 19:36:07 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13749008bd3b12070a2e5c1e923dfdf0d810d8b67c5dd1f7eecf99efe10f0aee`  
		Last Modified: Thu, 08 Aug 2024 19:36:10 GMT  
		Size: 95.6 MB (95562825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e719b74253d1fd6ef6f257edff82da511a06306023152fc153c427e8841073`  
		Last Modified: Thu, 08 Aug 2024 19:36:08 GMT  
		Size: 10.2 KB (10246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:246de7bb1dbb9db7ef72e45862b8953076f487989cad6d1e1a7da1a9e0940ee8`  
		Last Modified: Thu, 08 Aug 2024 19:36:08 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99bd78291bace39923c8796260a4d78286170c3f5eb335cad03b882d03a88ad3`  
		Last Modified: Thu, 08 Aug 2024 19:36:08 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec488c6e4e9a4df20a89730ff9ced82c155d9d1d0e2b0b92ba3cc49d3a620c0d`  
		Last Modified: Thu, 08 Aug 2024 19:36:09 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d069bafcb9ca2f2da74f786e2c439ba039b85b5c78e832aa83cdca06025c60`  
		Last Modified: Thu, 08 Aug 2024 19:36:09 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta3-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:29b68a4f3e239bd616057b63fbf6173c372155aea5a8b2bca8e5bdd7d1c8ad3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6079583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a985ccff8ec488f65b861dc4fa348266f0ffd7eb0cb076747e7561072baf0038`

```dockerfile
```

-	Layers:
	-	`sha256:dcd6d2d2d49ea5e4eafe3d3c2387820f5a3c43c11de39a31803be339fd799ba8`  
		Last Modified: Thu, 08 Aug 2024 19:36:06 GMT  
		Size: 6.0 MB (6025837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd64fb4d922a5645e1f75845ea8998c05885f6226abec62907df7f1a1066cb76`  
		Last Modified: Thu, 08 Aug 2024 19:36:06 GMT  
		Size: 53.7 KB (53746 bytes)  
		MIME: application/vnd.in-toto+json
