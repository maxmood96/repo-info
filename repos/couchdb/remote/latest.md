## `couchdb:latest`

```console
$ docker pull couchdb@sha256:b5e6939af792a0e40218e405e8656d68c14a03220899f470b58611a00dc65a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:a78f1b85d7530e49155715ed10733e06271878e6c82ee9696de771b175c4fcb6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83335968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:015b6fbd87be45fb0dc925f0cecb45844192a93b647f4c10e72b4c863b7f8bc8`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 13 Oct 2020 01:39:05 GMT
ADD file:0dc53e7886c35bc21ae6c4f6cedda54d56ae9c9e9cd367678f1a72e68b3c43d4 in / 
# Tue, 13 Oct 2020 01:39:05 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:32:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Oct 2020 02:32:44 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 13 Oct 2020 02:32:54 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:32:55 GMT
ENV GOSU_VERSION=1.11
# Tue, 13 Oct 2020 02:32:55 GMT
ENV TINI_VERSION=0.18.0
# Tue, 13 Oct 2020 02:33:02 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 13 Oct 2020 02:33:02 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 13 Oct 2020 02:33:33 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 13 Oct 2020 02:33:33 GMT
ENV COUCHDB_VERSION=3.1.1
# Tue, 13 Oct 2020 02:33:34 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 13 Oct 2020 02:33:53 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 13 Oct 2020 02:33:53 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 13 Oct 2020 02:33:54 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 13 Oct 2020 02:33:54 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 13 Oct 2020 02:33:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 13 Oct 2020 02:33:55 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Oct 2020 02:33:55 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Oct 2020 02:33:55 GMT
EXPOSE 4369 5984 9100
# Tue, 13 Oct 2020 02:33:55 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:bb79b6b2107fea8e8a47133a660b78e3a546998fcf0427be39ac9a0af4a97e90`  
		Last Modified: Tue, 13 Oct 2020 01:48:17 GMT  
		Size: 27.1 MB (27092228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64047dc3beaeda4c7dd4d074c33fdaf24223f4451d5dd0b05a12795f5f5562bb`  
		Last Modified: Tue, 13 Oct 2020 02:35:41 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf5219be029f9aabfcf12ca2168bc602620bb8a1d970d6461ad7aad71945fd6`  
		Last Modified: Tue, 13 Oct 2020 02:35:42 GMT  
		Size: 6.7 MB (6669379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe133310c07e761f41d37d687d4a8d8a3ccaca129a3205d3045d68384aa93d87`  
		Last Modified: Tue, 13 Oct 2020 02:35:40 GMT  
		Size: 1.2 MB (1192649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605d5fefdc3de395cbe8ed7b110a5fd38d7ae1db5a2b8e1ac15174d7fdfa09ce`  
		Last Modified: Tue, 13 Oct 2020 02:35:40 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38f02fa873023d43bce775319b8a54cbbfded60017286eb8b127d14c5027a93a`  
		Last Modified: Tue, 13 Oct 2020 02:35:40 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d6364744601b308998ba7d0a99c60c439915e2f5e0e58d96915595394433a2`  
		Last Modified: Tue, 13 Oct 2020 02:35:46 GMT  
		Size: 48.4 MB (48372250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf601c5e86bc4d66d9513a92806733cd8b4ad840ad612418d71828df94a4bab`  
		Last Modified: Tue, 13 Oct 2020 02:35:39 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7540b73bba440cc89e12ed517dd50488647d1afeb63e4c2fa46962d5026cc7fd`  
		Last Modified: Tue, 13 Oct 2020 02:35:38 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1d0befd4e18e3e4614bb3bf8ba768f52e81c60d2375d8ab7b5aeb0e69bf0b2`  
		Last Modified: Tue, 13 Oct 2020 02:35:39 GMT  
		Size: 2.1 KB (2061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d632d0fb7a8ec083b5a100f3181d0e81f783cdef4981ef5e0f7db189dbc89bc`  
		Last Modified: Tue, 13 Oct 2020 02:35:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:5dcc4ae9ff8ec1460b3e0dfcd6b02c730232f9327e775ec2c47e7f760e61bc26
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78375705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:319f24e72748f4a4ab49f4dad4aa5bfb8206feb8ded9953ecf9f3af230663a5a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 13 Oct 2020 01:41:09 GMT
ADD file:3488b1423094a75be5bb5956e9187827b8dd35d7a1f2b14081f8e74a1629e7d0 in / 
# Tue, 13 Oct 2020 01:41:11 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:56:36 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Oct 2020 02:56:38 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 13 Oct 2020 02:56:55 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:56:56 GMT
ENV GOSU_VERSION=1.11
# Tue, 13 Oct 2020 02:56:57 GMT
ENV TINI_VERSION=0.18.0
# Tue, 13 Oct 2020 02:57:08 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 13 Oct 2020 02:57:09 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 13 Oct 2020 02:58:05 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 13 Oct 2020 02:58:05 GMT
ENV COUCHDB_VERSION=3.1.1
# Tue, 13 Oct 2020 02:58:07 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 13 Oct 2020 02:58:32 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 13 Oct 2020 02:58:34 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 13 Oct 2020 02:58:35 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 13 Oct 2020 02:58:35 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 13 Oct 2020 02:58:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 13 Oct 2020 02:58:38 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Oct 2020 02:58:39 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Oct 2020 02:58:39 GMT
EXPOSE 4369 5984 9100
# Tue, 13 Oct 2020 02:58:40 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4e6164a63b7b4cf981546947e191644c122214975d40b51ede0536791ebec3d4`  
		Last Modified: Tue, 13 Oct 2020 01:48:17 GMT  
		Size: 25.8 MB (25849329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb0f7abeff6e4318676ef798b7df16301ee45ef2bca4699be064b8c517eacbb`  
		Last Modified: Tue, 13 Oct 2020 03:05:59 GMT  
		Size: 3.4 KB (3442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:babab4ba99a739ea24d3deb43d7ce1381ed1b9e4f07d6035f4203e203ac0c417`  
		Last Modified: Tue, 13 Oct 2020 03:05:59 GMT  
		Size: 6.5 MB (6533336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ba66c368ff3951b3258f53e13358d5e263e61c2d3ae33f85d57813a16dff29`  
		Last Modified: Tue, 13 Oct 2020 03:05:57 GMT  
		Size: 1.1 MB (1127062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e70c59632e7b2428bba82fb03145708a80902edd82e8f8292de181f0fcfae3a`  
		Last Modified: Tue, 13 Oct 2020 03:05:57 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37fee75b0a0f58b78a14b69e62d641b1c3f8c6e10ba7934096cf7b1a7d4a57fe`  
		Last Modified: Tue, 13 Oct 2020 03:05:56 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3560cecc1bbf82e1f2d0c2770498c17c6e94c6554112a2aa5aaeacd6d2580fe1`  
		Last Modified: Tue, 13 Oct 2020 03:06:03 GMT  
		Size: 44.9 MB (44856490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b2bdd3ba35d21476e704bdeb548ae3fbefae85939088464493ac50e8946df7`  
		Last Modified: Tue, 13 Oct 2020 03:05:55 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c9febba01b0841894f9864b32f4c15ce6b222e242076f9c0e93ebff11cb0447`  
		Last Modified: Tue, 13 Oct 2020 03:05:55 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b460652074238ff0e937460976ef88f9aea5d43188ae80131fb480a2572b95`  
		Last Modified: Tue, 13 Oct 2020 03:05:55 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f0645881fc0442aeb6d999ea646554560b301a3f19f0872cc76aa2adb75172`  
		Last Modified: Tue, 13 Oct 2020 03:05:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:e890ebeb3e2d9d7304dd4e5732673c929424c57c12eda99a03f47ce7424a6cdc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88498771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eb20bb9a153de6458a0d1089a7cfe6903c66e9d7619391c591f280ba24d6008`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 13 Oct 2020 01:38:54 GMT
ADD file:9992867f855c9bed54df6d26f3d8076689aff8a51e808fefba7d3b66dab250e5 in / 
# Tue, 13 Oct 2020 01:38:59 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 09:51:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Oct 2020 09:51:58 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 13 Oct 2020 09:53:15 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 09:53:22 GMT
ENV GOSU_VERSION=1.11
# Tue, 13 Oct 2020 09:53:28 GMT
ENV TINI_VERSION=0.18.0
# Tue, 13 Oct 2020 09:56:29 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 13 Oct 2020 09:56:33 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 13 Oct 2020 09:56:41 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 13 Oct 2020 09:56:44 GMT
ENV COUCHDB_VERSION=3.1.1
# Tue, 13 Oct 2020 09:56:49 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 13 Oct 2020 09:57:41 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 13 Oct 2020 09:57:45 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 13 Oct 2020 09:57:49 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 13 Oct 2020 09:57:51 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 13 Oct 2020 09:57:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 13 Oct 2020 09:57:59 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Oct 2020 09:58:02 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Oct 2020 09:58:08 GMT
EXPOSE 4369 5984 9100
# Tue, 13 Oct 2020 09:58:13 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:523555c6877c72cfcdec912b4d0053c298b1c97835efc7c6b0211585a06bd563`  
		Last Modified: Tue, 13 Oct 2020 01:50:10 GMT  
		Size: 30.5 MB (30517878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec18e010b303f397d5d2d4ce7db81813755566365786df639a79695e49e73922`  
		Last Modified: Tue, 13 Oct 2020 10:00:34 GMT  
		Size: 3.4 KB (3415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0328f181b2c3ff2579283288bb4c3e0a535924e07366fd73664574ca5a990e4`  
		Last Modified: Tue, 13 Oct 2020 10:00:34 GMT  
		Size: 7.6 MB (7580203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814ef320a304e1bac6e5633c4cb1a62758ddf286951768e41f5fc72bc39e527f`  
		Last Modified: Tue, 13 Oct 2020 10:00:33 GMT  
		Size: 1.1 MB (1116132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edfac921cc8366496c85c4428116b640232473f5ddabe2a0eb4e0cb1a156fd24`  
		Last Modified: Tue, 13 Oct 2020 10:00:31 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95c25f01fa7cd08af4240f80b88d6be956745a1f040f229f6f9fa30878ba095`  
		Last Modified: Tue, 13 Oct 2020 10:00:30 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668e2c04105f8160107ebf4161c674668bbf5f164b0b4f73cb86cddaab4646c2`  
		Last Modified: Tue, 13 Oct 2020 10:00:34 GMT  
		Size: 49.3 MB (49275088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a3cdd328dc5e450659e58070b625ae98c14f26961968e8ba555babab7ced3c`  
		Last Modified: Tue, 13 Oct 2020 10:00:26 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc55a37735528c67f64b31b74be46b58c7a88d70f39d443925ea076f048cba00`  
		Last Modified: Tue, 13 Oct 2020 10:00:26 GMT  
		Size: 769.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d250e8cab43b7a29a20e796a12e9eeca3b93903af329c8158d705495d3f2ac`  
		Last Modified: Tue, 13 Oct 2020 10:00:26 GMT  
		Size: 2.1 KB (2062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcbdba5f41d3972422a01360ebec1089b9b41fac2fdd4df961882682fe252689`  
		Last Modified: Tue, 13 Oct 2020 10:00:26 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
