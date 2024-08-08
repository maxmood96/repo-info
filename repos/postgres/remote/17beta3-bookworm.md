## `postgres:17beta3-bookworm`

```console
$ docker pull postgres@sha256:daa24ab2dec25e7cddd0a95a01a75675d3bc786f5aeadc312ad8c63dba741d8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm variant v5
	-	unknown; unknown

### `postgres:17beta3-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:816e87b3e08954a30ea60878500829577c351a4c9e2e762c6a60d4fa7b96ddcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.2 MB (147227265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a1320283b027da20b958234688e74f739363344b6e6ef8dc6cf2104ab668936`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jul 2024 23:57:01 GMT
ADD file:752589c0ca446e2e74ef0b8c412eabb01e2a8035cfec47b1d9630b9f704fbda7 in / 
# Mon, 22 Jul 2024 23:57:01 GMT
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
	-	`sha256:b695a3453560aacd42060f43ccf1cbd7d20412f50126ca6a469af38d3fe1e5b1`  
		Last Modified: Tue, 23 Jul 2024 00:01:19 GMT  
		Size: 26.9 MB (26887299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e5f426a0038285fe41e79a1f182ce2b0fc81ae1511ed7b086d11c72960b81d`  
		Last Modified: Thu, 08 Aug 2024 19:17:33 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514b72509b73a0239738641cab477b8ec41b14d4d4408cb36bc46508a83e70c6`  
		Last Modified: Thu, 08 Aug 2024 19:17:33 GMT  
		Size: 4.2 MB (4150875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ba1e65c1d6c89e4cecafa0fd0431610f25fb0391042bbff174575671107215`  
		Last Modified: Thu, 08 Aug 2024 19:17:33 GMT  
		Size: 1.4 MB (1423818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf55ec4029974d792237a9ae53f2426fcc983f4f8cdf4aaca942975daf2404f`  
		Last Modified: Thu, 08 Aug 2024 19:17:34 GMT  
		Size: 8.1 MB (8066322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e922c489574b9892bcf87bde34bfd5fca6f658fb9dc0db029c2e5db2017e07ca`  
		Last Modified: Thu, 08 Aug 2024 19:17:34 GMT  
		Size: 1.2 MB (1194823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340c34ca24c124b5241ac6f06a02304f858bc457ba9855110c323fdc9b047bb9`  
		Last Modified: Thu, 08 Aug 2024 19:17:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb7b24a6ecc9edaa06a0578a468c3040001301f073ee7532f089cb647c7ff4a`  
		Last Modified: Thu, 08 Aug 2024 19:17:34 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6ba8b819c236d0c82462fedbba0537c33315b585bc73b1d0768e2f7dfd2109`  
		Last Modified: Thu, 08 Aug 2024 19:17:38 GMT  
		Size: 105.5 MB (105483546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2773732f185fc660c07a6b40864bd0caf048bcea117438d7182a27435af72e6`  
		Last Modified: Thu, 08 Aug 2024 19:17:35 GMT  
		Size: 10.3 KB (10251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782141c288247ef01cc307c4f00387e00e738c6c7ef129971d625e55ed0cf2df`  
		Last Modified: Thu, 08 Aug 2024 19:17:35 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91b2490bd7f3325151da51fe2f1c7691b2840ef8cf1be3ad27786c54b97e7ef`  
		Last Modified: Thu, 08 Aug 2024 19:17:35 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3442f1b5305d8c9093559876a86fcf9caffc4bcbbbd924ccb267ff1a06530fd1`  
		Last Modified: Thu, 08 Aug 2024 19:17:36 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6ec7baea31bb7424004329fd39789a8f20dbf7ac70f9f71515fff5e04cbe16`  
		Last Modified: Thu, 08 Aug 2024 19:17:36 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta3-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:e276a62ffd77c344461979b0d349bbdf22011769267a3591252da497543150ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5832169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09a5f8a8d7b5816fb05f368eb6b187e33a1e5bdda1950faba11bb1741e2f87f`

```dockerfile
```

-	Layers:
	-	`sha256:3d812f569644cebe527a0526a68dd11f7ee6c471f933f26a04d3e940cdda5bfe`  
		Last Modified: Thu, 08 Aug 2024 19:17:33 GMT  
		Size: 5.8 MB (5778105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a4786b3c69c3bfc3136793480f1fc207b61fa7ed9f40ee40beb2d31f669bc6d`  
		Last Modified: Thu, 08 Aug 2024 19:17:33 GMT  
		Size: 54.1 KB (54064 bytes)  
		MIME: application/vnd.in-toto+json
