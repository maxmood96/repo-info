## `couchdb:latest`

```console
$ docker pull couchdb@sha256:570bcef2fc1a7ef94cd03b45fe680b8651940b34f1db870063ea98735223cd48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:b69002a3bb4454b0d9b20b13be2fd5358c4907812a8557317f0d3ce91912b925
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83244072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b86c5b0e945dd10121b221dc1fe4aaff7530a07e7dec5d397fbeab2b9c40b30`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 14:31:46 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Jul 2020 14:31:47 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 22 Jul 2020 14:31:55 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 14:31:55 GMT
ENV GOSU_VERSION=1.11
# Wed, 22 Jul 2020 14:31:56 GMT
ENV TINI_VERSION=0.18.0
# Wed, 22 Jul 2020 14:32:02 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Wed, 22 Jul 2020 14:32:02 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Wed, 22 Jul 2020 14:32:03 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Wed, 22 Jul 2020 14:32:03 GMT
ENV COUCHDB_VERSION=3.1.0
# Wed, 22 Jul 2020 14:32:04 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Wed, 22 Jul 2020 14:32:22 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 22 Jul 2020 14:32:22 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 22 Jul 2020 14:32:22 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 22 Jul 2020 14:32:22 GMT
COPY file:6952d2d38c707f223d813efd2d2969873cdd4b66d733559ef9be855aff5d8579 in /usr/local/bin 
# Wed, 22 Jul 2020 14:32:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 22 Jul 2020 14:32:23 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 22 Jul 2020 14:32:24 GMT
VOLUME [/opt/couchdb/data]
# Wed, 22 Jul 2020 14:32:24 GMT
EXPOSE 4369 5984 9100
# Wed, 22 Jul 2020 14:32:24 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3594488eae8f53832228d00f6775dbd8300b9c53596acd0fd987d7a82408b225`  
		Last Modified: Wed, 22 Jul 2020 14:35:38 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6322fcc7c62bc35bff33bc152a8ad699903584d92fa2e52f44b40e713f1dff8b`  
		Last Modified: Wed, 22 Jul 2020 14:35:38 GMT  
		Size: 6.7 MB (6669359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4d8b3b4f99c586d143d29e26fb0098c64c8a1cc005eaf1953afbdc42b4dc62`  
		Last Modified: Wed, 22 Jul 2020 14:35:38 GMT  
		Size: 1.2 MB (1192699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:becb9a751413200cab5959bf5ef95a2fa16aa805e80f10905bcd6b67f3c02a10`  
		Last Modified: Wed, 22 Jul 2020 14:35:37 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cadf7ec9d3188066b1f602065f523d1b26e9fd6b2d1eeb7db916b5afddcf6005`  
		Last Modified: Wed, 22 Jul 2020 14:35:37 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea5913108d53ed8844ee52fb440483a6c034db80278c7a7d76745cb586c009a`  
		Last Modified: Wed, 22 Jul 2020 14:35:46 GMT  
		Size: 48.3 MB (48274025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241b38b40d7f03ec45ce6060156ccfcf1e482f7306e73ad1d339c3e7c8482542`  
		Last Modified: Wed, 22 Jul 2020 14:35:36 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ba1e14c895d39b5da52e64843ee5084544cbb7ed875248400a54420268334f`  
		Last Modified: Wed, 22 Jul 2020 14:35:36 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e77712ecf61e8bf090ace125e8e225a9c3aac03324df95e96067ffeb01a312c`  
		Last Modified: Wed, 22 Jul 2020 14:35:36 GMT  
		Size: 2.1 KB (2051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6906ebcb6aa12f848d918cb05da6a162fbe559de08ec612c7e73084ebf6ce9`  
		Last Modified: Wed, 22 Jul 2020 14:35:36 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:3b4c09aa911b17bf4e0ed90df6c307b9fbc95e024556f3f3a7a4f512007ce267
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78302435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acddf6755793ca71781259382621ae28d1872ce76eda1d1f1cd6a0903b092227`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 22 Jul 2020 00:41:09 GMT
ADD file:1efd5b51a56f36bcf79a1bcea1df36ef28299a42bc11e758f9e49066f2a1f085 in / 
# Wed, 22 Jul 2020 00:41:10 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:57:39 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Jul 2020 03:57:42 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 22 Jul 2020 03:58:03 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:58:04 GMT
ENV GOSU_VERSION=1.11
# Wed, 22 Jul 2020 03:58:05 GMT
ENV TINI_VERSION=0.18.0
# Wed, 22 Jul 2020 04:00:34 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Wed, 22 Jul 2020 04:00:36 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Wed, 22 Jul 2020 04:03:05 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Wed, 22 Jul 2020 04:03:06 GMT
ENV COUCHDB_VERSION=3.1.0
# Wed, 22 Jul 2020 04:03:09 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Wed, 22 Jul 2020 04:03:37 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 22 Jul 2020 04:03:38 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 22 Jul 2020 04:03:39 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 22 Jul 2020 04:03:39 GMT
COPY file:6952d2d38c707f223d813efd2d2969873cdd4b66d733559ef9be855aff5d8579 in /usr/local/bin 
# Wed, 22 Jul 2020 04:03:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 22 Jul 2020 04:03:42 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 22 Jul 2020 04:03:43 GMT
VOLUME [/opt/couchdb/data]
# Wed, 22 Jul 2020 04:03:43 GMT
EXPOSE 4369 5984 9100
# Wed, 22 Jul 2020 04:03:44 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3999339def4d7591a8064bfc698302ae0e29bc5e0557ae392c122e1b3efa9305`  
		Last Modified: Wed, 22 Jul 2020 00:47:42 GMT  
		Size: 25.9 MB (25857826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad42e5dc34241914ff239bd29e8b8890a734811558e11f6f81fa483257fae1e`  
		Last Modified: Wed, 22 Jul 2020 04:07:52 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab6cf86ff9ea3931e4bc7e6ec3d587efef94fbfaa4af49d241828b75b77c27f`  
		Last Modified: Wed, 22 Jul 2020 04:07:53 GMT  
		Size: 6.5 MB (6533384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89b638798dbe08049dcc357bbfbdfad52694b22b6c469a0d24eae8cdeb9cd026`  
		Last Modified: Wed, 22 Jul 2020 04:07:51 GMT  
		Size: 1.1 MB (1127086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a9f4d939f0a4d2c35fa1e48ebb7f77bcbe68d440125140e2bf0e8637fbb80c`  
		Last Modified: Wed, 22 Jul 2020 04:07:50 GMT  
		Size: 2.5 KB (2495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:378f7bff9a6dfb15c58ecad97c5853f906b68731ad622c887ee47399037ca309`  
		Last Modified: Wed, 22 Jul 2020 04:07:50 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1deb6c03050f07fae4a4a59312cc05fbea2ab312bbf3265b5c5ddb8002b5156`  
		Last Modified: Wed, 22 Jul 2020 04:07:57 GMT  
		Size: 44.8 MB (44774658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88600700cb3d97a0acbeeb203d268e7998f971d29d7e0d579b11d19501df9ce5`  
		Last Modified: Wed, 22 Jul 2020 04:07:48 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7e5697500f859bf96940035f65580d57ebfbb3badf92b5354bc704bc82c1bc`  
		Last Modified: Wed, 22 Jul 2020 04:07:48 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f6bc20278b0e8936a7866b6a653fe8b3a7b888a6f22ed3d58aa6be013a56a5`  
		Last Modified: Wed, 22 Jul 2020 04:07:49 GMT  
		Size: 2.1 KB (2052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df60e90975744d02bf0f67bf53d23d02f31e54ccfe5b291d0c6198e73372ca64`  
		Last Modified: Wed, 22 Jul 2020 04:07:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:fda541d4e178dab8827efe23a140f29fe22eccd84bad956ff410201faf8e6eba
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 MB (88399026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a69ec9ae790f6570297bedf6c0cde71a68202ac910259ccda1a38a72c7f94dc`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 22 Jul 2020 02:16:05 GMT
ADD file:037dec996d9b742fc49f675272aa42ebd31f04226ba3d28836a6556cb61c29e7 in / 
# Wed, 22 Jul 2020 02:16:14 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 06:00:25 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Jul 2020 06:00:38 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 22 Jul 2020 06:01:45 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 06:01:49 GMT
ENV GOSU_VERSION=1.11
# Wed, 22 Jul 2020 06:01:53 GMT
ENV TINI_VERSION=0.18.0
# Wed, 22 Jul 2020 06:02:23 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Wed, 22 Jul 2020 06:02:28 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Wed, 22 Jul 2020 06:02:44 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Wed, 22 Jul 2020 06:02:49 GMT
ENV COUCHDB_VERSION=3.1.0
# Wed, 22 Jul 2020 06:03:00 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Wed, 22 Jul 2020 06:04:21 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 22 Jul 2020 06:04:25 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 22 Jul 2020 06:04:26 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 22 Jul 2020 06:04:29 GMT
COPY file:6952d2d38c707f223d813efd2d2969873cdd4b66d733559ef9be855aff5d8579 in /usr/local/bin 
# Wed, 22 Jul 2020 06:04:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 22 Jul 2020 06:04:37 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 22 Jul 2020 06:04:41 GMT
VOLUME [/opt/couchdb/data]
# Wed, 22 Jul 2020 06:04:44 GMT
EXPOSE 4369 5984 9100
# Wed, 22 Jul 2020 06:04:47 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:d022338f917106731b8902d4c3d7009435a41381c11c8d210bbd6af007569f69`  
		Last Modified: Wed, 22 Jul 2020 02:26:01 GMT  
		Size: 30.5 MB (30524562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:900094ebcd4754d54a025bda5c8d9a83aeb7e1ab6131465a96283e554dcbb118`  
		Last Modified: Wed, 22 Jul 2020 06:07:47 GMT  
		Size: 3.4 KB (3417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a853e10667aa5be7b33f98bb5c8d4856333a92e36f1641752124ff776d2ebc`  
		Last Modified: Wed, 22 Jul 2020 06:07:46 GMT  
		Size: 7.6 MB (7580133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41fdd15f8349005e4da3eb37d03c83f1ad44559c9b7091c6e58b855b3b81aaa5`  
		Last Modified: Wed, 22 Jul 2020 06:07:44 GMT  
		Size: 1.1 MB (1116125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:413949e92ad68b1fd27449ac01839a692be3cc54ee79c0c778533127f781b47d`  
		Last Modified: Wed, 22 Jul 2020 06:07:43 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2bcd43a9e58d3686b457a15937474bf43ab707a6f54f2adb26269eacfb0d33`  
		Last Modified: Wed, 22 Jul 2020 06:07:43 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b1fc0ec7fb9bf0c9ca268bcc48dd65b784eb5e3f0f8470040876aed0264e1aa`  
		Last Modified: Wed, 22 Jul 2020 06:07:48 GMT  
		Size: 49.2 MB (49168754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca12b0e33fc688094236ea934eb768384420f1067eea08d22935cd6817933b0c`  
		Last Modified: Wed, 22 Jul 2020 06:07:40 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d07ce75a9f7e73e0ab76d5c9c6754cc42f51edb52326d7ddf0d4d9b88bdce4e`  
		Last Modified: Wed, 22 Jul 2020 06:07:40 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97336b085538edfe04004b1a33bf29261d171c0bed31da93abca227b66340e6`  
		Last Modified: Wed, 22 Jul 2020 06:07:40 GMT  
		Size: 2.1 KB (2051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a97173d1a24125ce3d49ed64d643a7b7be40fcf13d58c19b386f27c42d79023`  
		Last Modified: Wed, 22 Jul 2020 06:07:40 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
