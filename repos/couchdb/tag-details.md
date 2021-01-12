<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchdb`

-	[`couchdb:2`](#couchdb2)
-	[`couchdb:2.3`](#couchdb23)
-	[`couchdb:2.3.1`](#couchdb231)
-	[`couchdb:3`](#couchdb3)
-	[`couchdb:3.0`](#couchdb30)
-	[`couchdb:3.0.1`](#couchdb301)
-	[`couchdb:3.1`](#couchdb31)
-	[`couchdb:3.1.1`](#couchdb311)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:2`

```console
$ docker pull couchdb@sha256:ef82b77dd5ffec80f154c203d7a96df6934baa423b2a8b9450df6fd692472075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2` - linux; amd64

```console
$ docker pull couchdb@sha256:4eeba0428570ea0dc90d1cbf148454956052f314935d4c48208d32fc69cc9be5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82401068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:493c01c773ded205388203a5eb88aad25eb14e3009066d49089f04d5d011007a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Jan 2021 00:35:21 GMT
ADD file:f47757e25d3861a5c0180542919c21264323d4dace1f5a6761fc2f38b53a9003 in / 
# Tue, 12 Jan 2021 00:35:21 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:51:50 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Jan 2021 03:51:51 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Jan 2021 03:52:02 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 03:52:02 GMT
ENV GOSU_VERSION=1.11
# Tue, 12 Jan 2021 03:52:02 GMT
ENV TINI_VERSION=0.18.0
# Tue, 12 Jan 2021 03:52:12 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 12 Jan 2021 03:52:12 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 12 Jan 2021 03:53:18 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 12 Jan 2021 03:53:19 GMT
ENV COUCHDB_VERSION=2.3.1
# Tue, 12 Jan 2021 03:53:20 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb stretch main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 12 Jan 2021 03:53:43 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~stretch     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Jan 2021 03:53:43 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Jan 2021 03:53:44 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Jan 2021 03:53:44 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 12 Jan 2021 03:53:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Jan 2021 03:53:45 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Jan 2021 03:53:45 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Jan 2021 03:53:45 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Jan 2021 03:53:46 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8aff230071c97ddc86b6d29fbbb7a4caae7a0183a83f08aa5a06e69e26ce2c81`  
		Last Modified: Tue, 12 Jan 2021 00:43:25 GMT  
		Size: 22.5 MB (22528609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276e247f0cd63a1fe827f9b85dd8d969ae4d1dd8a33c60d314c097e1bb4653f0`  
		Last Modified: Tue, 12 Jan 2021 03:54:49 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b2066d261b6ece5cf40fbc6ccfb3c25564dd961837135be8e5b028fa8d4e50`  
		Last Modified: Tue, 12 Jan 2021 03:54:50 GMT  
		Size: 8.5 MB (8471914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd4d1b0a4337f95727e774ed6509fdc16bdcc24fd85e81bb453517ae3d89f415`  
		Last Modified: Tue, 12 Jan 2021 03:54:48 GMT  
		Size: 1.2 MB (1190389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83230eedf25eafa49423179d1d5fd973cf6027ef8eb030b39ee0c23fc96a3184`  
		Last Modified: Tue, 12 Jan 2021 03:54:48 GMT  
		Size: 3.1 KB (3061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50eec4085f700aaed8cb7583d1315eb10cef41023049268e061054320a38bd4`  
		Last Modified: Tue, 12 Jan 2021 03:54:47 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3896d223e87c808c03543b6ec19d4eeb0bbe14a937800ab1248468bb7a3042cb`  
		Last Modified: Tue, 12 Jan 2021 03:54:53 GMT  
		Size: 50.2 MB (50200111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9189261b9f49b6febe68dd585900c38a763d81895ddd4f82bd503f3c13d8d427`  
		Last Modified: Tue, 12 Jan 2021 03:54:47 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dd0e70fe85e2d846c9c55376f500be720da3f8468b20cb3507fabd4b47de552`  
		Last Modified: Tue, 12 Jan 2021 03:54:46 GMT  
		Size: 768.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf6aed357877fc58ba1cdfe094e75f8e8329175d6fea2c003abd24a973748f7`  
		Last Modified: Tue, 12 Jan 2021 03:54:46 GMT  
		Size: 2.1 KB (2070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b404ef974526a12ada33f0e265a832b6b77d5c0f326af7d07d8be7b2bc625fa`  
		Last Modified: Tue, 12 Jan 2021 03:54:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:c8d18ffe5dfc1aca5139faa5d80ff87d347520ec2af41e40bacdab6f27b8444a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76941278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f70d504662e64ba26c3c362cf2a9b94e5ada14a9b0493298129d90613db3a6ab`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Jan 2021 00:45:57 GMT
ADD file:1dbf496d4adcfe7f12aea3440df891e77dfc1ebe060293de4f1ce37805fa65dc in / 
# Tue, 12 Jan 2021 00:46:05 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 02:08:10 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Jan 2021 02:08:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Jan 2021 02:08:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 02:08:32 GMT
ENV GOSU_VERSION=1.11
# Tue, 12 Jan 2021 02:08:33 GMT
ENV TINI_VERSION=0.18.0
# Tue, 12 Jan 2021 02:09:32 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 12 Jan 2021 02:09:33 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 12 Jan 2021 02:09:40 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 12 Jan 2021 02:09:42 GMT
ENV COUCHDB_VERSION=2.3.1
# Tue, 12 Jan 2021 02:09:44 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb stretch main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 12 Jan 2021 02:10:21 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~stretch     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Jan 2021 02:10:23 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Jan 2021 02:10:24 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Jan 2021 02:10:25 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 12 Jan 2021 02:10:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Jan 2021 02:10:27 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Jan 2021 02:10:28 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Jan 2021 02:10:29 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Jan 2021 02:10:30 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f5ae4cb78f788ad985447f014f2a5d2a878b9aa7496e12d4f62aaab1069093da`  
		Last Modified: Tue, 12 Jan 2021 00:55:18 GMT  
		Size: 20.4 MB (20389454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c9b14c2de98327146c9473154f5741a2414233aac0375d0dd938ef0bf38034`  
		Last Modified: Tue, 12 Jan 2021 02:11:46 GMT  
		Size: 3.4 KB (3435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ca0ddece3c518dbb1e74b028101d7b5a45d86c4935e4bc67dac5d209a67f47`  
		Last Modified: Tue, 12 Jan 2021 02:11:46 GMT  
		Size: 7.6 MB (7611430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08eb19d48147b89f95d8896d76fd62f0697eb18d9fadb83cf4fe8b1fef9e4681`  
		Last Modified: Tue, 12 Jan 2021 02:11:44 GMT  
		Size: 1.1 MB (1125001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1892d5a5e1ff3c84006db8c0a0fd255087bab35e3d1d1f80da8b1e78ad50708`  
		Last Modified: Tue, 12 Jan 2021 02:11:45 GMT  
		Size: 3.1 KB (3058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ecf57c0d377e5760592842e4f021b29d7dd721e0969872f82394f023b29807`  
		Last Modified: Tue, 12 Jan 2021 02:11:45 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e35c7cd0713a880257fc4c28c42446e7ee37fe6235f2f32f7b16c3181dde4f7`  
		Last Modified: Tue, 12 Jan 2021 02:11:54 GMT  
		Size: 47.8 MB (47805337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50b3d346d14e77f5072e50ed4d55be61b607dbff24affc098cdaf89ae3e26d0`  
		Last Modified: Tue, 12 Jan 2021 02:11:41 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3d921e5f13021f67aba2ba902576f08b202fe39b38d660e3319f14e3fd5edd`  
		Last Modified: Tue, 12 Jan 2021 02:11:42 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6433843863b566073633e24fb26b5c0926cecb5ddf43fea475332326145bfe95`  
		Last Modified: Tue, 12 Jan 2021 02:11:41 GMT  
		Size: 2.1 KB (2068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5ee1e1e092238af8e93b4ecdcdf20a9e9fe802bfeb7680b4b19a9eee9fdaa4`  
		Last Modified: Tue, 12 Jan 2021 02:11:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3`

```console
$ docker pull couchdb@sha256:ef82b77dd5ffec80f154c203d7a96df6934baa423b2a8b9450df6fd692472075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:4eeba0428570ea0dc90d1cbf148454956052f314935d4c48208d32fc69cc9be5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82401068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:493c01c773ded205388203a5eb88aad25eb14e3009066d49089f04d5d011007a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Jan 2021 00:35:21 GMT
ADD file:f47757e25d3861a5c0180542919c21264323d4dace1f5a6761fc2f38b53a9003 in / 
# Tue, 12 Jan 2021 00:35:21 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:51:50 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Jan 2021 03:51:51 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Jan 2021 03:52:02 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 03:52:02 GMT
ENV GOSU_VERSION=1.11
# Tue, 12 Jan 2021 03:52:02 GMT
ENV TINI_VERSION=0.18.0
# Tue, 12 Jan 2021 03:52:12 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 12 Jan 2021 03:52:12 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 12 Jan 2021 03:53:18 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 12 Jan 2021 03:53:19 GMT
ENV COUCHDB_VERSION=2.3.1
# Tue, 12 Jan 2021 03:53:20 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb stretch main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 12 Jan 2021 03:53:43 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~stretch     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Jan 2021 03:53:43 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Jan 2021 03:53:44 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Jan 2021 03:53:44 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 12 Jan 2021 03:53:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Jan 2021 03:53:45 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Jan 2021 03:53:45 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Jan 2021 03:53:45 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Jan 2021 03:53:46 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8aff230071c97ddc86b6d29fbbb7a4caae7a0183a83f08aa5a06e69e26ce2c81`  
		Last Modified: Tue, 12 Jan 2021 00:43:25 GMT  
		Size: 22.5 MB (22528609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276e247f0cd63a1fe827f9b85dd8d969ae4d1dd8a33c60d314c097e1bb4653f0`  
		Last Modified: Tue, 12 Jan 2021 03:54:49 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b2066d261b6ece5cf40fbc6ccfb3c25564dd961837135be8e5b028fa8d4e50`  
		Last Modified: Tue, 12 Jan 2021 03:54:50 GMT  
		Size: 8.5 MB (8471914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd4d1b0a4337f95727e774ed6509fdc16bdcc24fd85e81bb453517ae3d89f415`  
		Last Modified: Tue, 12 Jan 2021 03:54:48 GMT  
		Size: 1.2 MB (1190389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83230eedf25eafa49423179d1d5fd973cf6027ef8eb030b39ee0c23fc96a3184`  
		Last Modified: Tue, 12 Jan 2021 03:54:48 GMT  
		Size: 3.1 KB (3061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50eec4085f700aaed8cb7583d1315eb10cef41023049268e061054320a38bd4`  
		Last Modified: Tue, 12 Jan 2021 03:54:47 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3896d223e87c808c03543b6ec19d4eeb0bbe14a937800ab1248468bb7a3042cb`  
		Last Modified: Tue, 12 Jan 2021 03:54:53 GMT  
		Size: 50.2 MB (50200111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9189261b9f49b6febe68dd585900c38a763d81895ddd4f82bd503f3c13d8d427`  
		Last Modified: Tue, 12 Jan 2021 03:54:47 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dd0e70fe85e2d846c9c55376f500be720da3f8468b20cb3507fabd4b47de552`  
		Last Modified: Tue, 12 Jan 2021 03:54:46 GMT  
		Size: 768.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf6aed357877fc58ba1cdfe094e75f8e8329175d6fea2c003abd24a973748f7`  
		Last Modified: Tue, 12 Jan 2021 03:54:46 GMT  
		Size: 2.1 KB (2070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b404ef974526a12ada33f0e265a832b6b77d5c0f326af7d07d8be7b2bc625fa`  
		Last Modified: Tue, 12 Jan 2021 03:54:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:c8d18ffe5dfc1aca5139faa5d80ff87d347520ec2af41e40bacdab6f27b8444a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76941278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f70d504662e64ba26c3c362cf2a9b94e5ada14a9b0493298129d90613db3a6ab`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Jan 2021 00:45:57 GMT
ADD file:1dbf496d4adcfe7f12aea3440df891e77dfc1ebe060293de4f1ce37805fa65dc in / 
# Tue, 12 Jan 2021 00:46:05 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 02:08:10 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Jan 2021 02:08:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Jan 2021 02:08:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 02:08:32 GMT
ENV GOSU_VERSION=1.11
# Tue, 12 Jan 2021 02:08:33 GMT
ENV TINI_VERSION=0.18.0
# Tue, 12 Jan 2021 02:09:32 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 12 Jan 2021 02:09:33 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 12 Jan 2021 02:09:40 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 12 Jan 2021 02:09:42 GMT
ENV COUCHDB_VERSION=2.3.1
# Tue, 12 Jan 2021 02:09:44 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb stretch main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 12 Jan 2021 02:10:21 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~stretch     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Jan 2021 02:10:23 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Jan 2021 02:10:24 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Jan 2021 02:10:25 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 12 Jan 2021 02:10:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Jan 2021 02:10:27 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Jan 2021 02:10:28 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Jan 2021 02:10:29 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Jan 2021 02:10:30 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f5ae4cb78f788ad985447f014f2a5d2a878b9aa7496e12d4f62aaab1069093da`  
		Last Modified: Tue, 12 Jan 2021 00:55:18 GMT  
		Size: 20.4 MB (20389454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c9b14c2de98327146c9473154f5741a2414233aac0375d0dd938ef0bf38034`  
		Last Modified: Tue, 12 Jan 2021 02:11:46 GMT  
		Size: 3.4 KB (3435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ca0ddece3c518dbb1e74b028101d7b5a45d86c4935e4bc67dac5d209a67f47`  
		Last Modified: Tue, 12 Jan 2021 02:11:46 GMT  
		Size: 7.6 MB (7611430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08eb19d48147b89f95d8896d76fd62f0697eb18d9fadb83cf4fe8b1fef9e4681`  
		Last Modified: Tue, 12 Jan 2021 02:11:44 GMT  
		Size: 1.1 MB (1125001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1892d5a5e1ff3c84006db8c0a0fd255087bab35e3d1d1f80da8b1e78ad50708`  
		Last Modified: Tue, 12 Jan 2021 02:11:45 GMT  
		Size: 3.1 KB (3058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ecf57c0d377e5760592842e4f021b29d7dd721e0969872f82394f023b29807`  
		Last Modified: Tue, 12 Jan 2021 02:11:45 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e35c7cd0713a880257fc4c28c42446e7ee37fe6235f2f32f7b16c3181dde4f7`  
		Last Modified: Tue, 12 Jan 2021 02:11:54 GMT  
		Size: 47.8 MB (47805337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50b3d346d14e77f5072e50ed4d55be61b607dbff24affc098cdaf89ae3e26d0`  
		Last Modified: Tue, 12 Jan 2021 02:11:41 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3d921e5f13021f67aba2ba902576f08b202fe39b38d660e3319f14e3fd5edd`  
		Last Modified: Tue, 12 Jan 2021 02:11:42 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6433843863b566073633e24fb26b5c0926cecb5ddf43fea475332326145bfe95`  
		Last Modified: Tue, 12 Jan 2021 02:11:41 GMT  
		Size: 2.1 KB (2068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5ee1e1e092238af8e93b4ecdcdf20a9e9fe802bfeb7680b4b19a9eee9fdaa4`  
		Last Modified: Tue, 12 Jan 2021 02:11:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3.1`

```console
$ docker pull couchdb@sha256:ef82b77dd5ffec80f154c203d7a96df6934baa423b2a8b9450df6fd692472075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:4eeba0428570ea0dc90d1cbf148454956052f314935d4c48208d32fc69cc9be5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82401068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:493c01c773ded205388203a5eb88aad25eb14e3009066d49089f04d5d011007a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Jan 2021 00:35:21 GMT
ADD file:f47757e25d3861a5c0180542919c21264323d4dace1f5a6761fc2f38b53a9003 in / 
# Tue, 12 Jan 2021 00:35:21 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:51:50 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Jan 2021 03:51:51 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Jan 2021 03:52:02 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 03:52:02 GMT
ENV GOSU_VERSION=1.11
# Tue, 12 Jan 2021 03:52:02 GMT
ENV TINI_VERSION=0.18.0
# Tue, 12 Jan 2021 03:52:12 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 12 Jan 2021 03:52:12 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 12 Jan 2021 03:53:18 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 12 Jan 2021 03:53:19 GMT
ENV COUCHDB_VERSION=2.3.1
# Tue, 12 Jan 2021 03:53:20 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb stretch main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 12 Jan 2021 03:53:43 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~stretch     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Jan 2021 03:53:43 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Jan 2021 03:53:44 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Jan 2021 03:53:44 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 12 Jan 2021 03:53:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Jan 2021 03:53:45 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Jan 2021 03:53:45 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Jan 2021 03:53:45 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Jan 2021 03:53:46 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8aff230071c97ddc86b6d29fbbb7a4caae7a0183a83f08aa5a06e69e26ce2c81`  
		Last Modified: Tue, 12 Jan 2021 00:43:25 GMT  
		Size: 22.5 MB (22528609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276e247f0cd63a1fe827f9b85dd8d969ae4d1dd8a33c60d314c097e1bb4653f0`  
		Last Modified: Tue, 12 Jan 2021 03:54:49 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b2066d261b6ece5cf40fbc6ccfb3c25564dd961837135be8e5b028fa8d4e50`  
		Last Modified: Tue, 12 Jan 2021 03:54:50 GMT  
		Size: 8.5 MB (8471914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd4d1b0a4337f95727e774ed6509fdc16bdcc24fd85e81bb453517ae3d89f415`  
		Last Modified: Tue, 12 Jan 2021 03:54:48 GMT  
		Size: 1.2 MB (1190389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83230eedf25eafa49423179d1d5fd973cf6027ef8eb030b39ee0c23fc96a3184`  
		Last Modified: Tue, 12 Jan 2021 03:54:48 GMT  
		Size: 3.1 KB (3061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50eec4085f700aaed8cb7583d1315eb10cef41023049268e061054320a38bd4`  
		Last Modified: Tue, 12 Jan 2021 03:54:47 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3896d223e87c808c03543b6ec19d4eeb0bbe14a937800ab1248468bb7a3042cb`  
		Last Modified: Tue, 12 Jan 2021 03:54:53 GMT  
		Size: 50.2 MB (50200111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9189261b9f49b6febe68dd585900c38a763d81895ddd4f82bd503f3c13d8d427`  
		Last Modified: Tue, 12 Jan 2021 03:54:47 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dd0e70fe85e2d846c9c55376f500be720da3f8468b20cb3507fabd4b47de552`  
		Last Modified: Tue, 12 Jan 2021 03:54:46 GMT  
		Size: 768.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf6aed357877fc58ba1cdfe094e75f8e8329175d6fea2c003abd24a973748f7`  
		Last Modified: Tue, 12 Jan 2021 03:54:46 GMT  
		Size: 2.1 KB (2070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b404ef974526a12ada33f0e265a832b6b77d5c0f326af7d07d8be7b2bc625fa`  
		Last Modified: Tue, 12 Jan 2021 03:54:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:c8d18ffe5dfc1aca5139faa5d80ff87d347520ec2af41e40bacdab6f27b8444a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76941278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f70d504662e64ba26c3c362cf2a9b94e5ada14a9b0493298129d90613db3a6ab`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Jan 2021 00:45:57 GMT
ADD file:1dbf496d4adcfe7f12aea3440df891e77dfc1ebe060293de4f1ce37805fa65dc in / 
# Tue, 12 Jan 2021 00:46:05 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 02:08:10 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Jan 2021 02:08:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Jan 2021 02:08:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 02:08:32 GMT
ENV GOSU_VERSION=1.11
# Tue, 12 Jan 2021 02:08:33 GMT
ENV TINI_VERSION=0.18.0
# Tue, 12 Jan 2021 02:09:32 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 12 Jan 2021 02:09:33 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 12 Jan 2021 02:09:40 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 12 Jan 2021 02:09:42 GMT
ENV COUCHDB_VERSION=2.3.1
# Tue, 12 Jan 2021 02:09:44 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb stretch main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 12 Jan 2021 02:10:21 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~stretch     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Jan 2021 02:10:23 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Jan 2021 02:10:24 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Jan 2021 02:10:25 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 12 Jan 2021 02:10:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Jan 2021 02:10:27 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Jan 2021 02:10:28 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Jan 2021 02:10:29 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Jan 2021 02:10:30 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f5ae4cb78f788ad985447f014f2a5d2a878b9aa7496e12d4f62aaab1069093da`  
		Last Modified: Tue, 12 Jan 2021 00:55:18 GMT  
		Size: 20.4 MB (20389454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c9b14c2de98327146c9473154f5741a2414233aac0375d0dd938ef0bf38034`  
		Last Modified: Tue, 12 Jan 2021 02:11:46 GMT  
		Size: 3.4 KB (3435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ca0ddece3c518dbb1e74b028101d7b5a45d86c4935e4bc67dac5d209a67f47`  
		Last Modified: Tue, 12 Jan 2021 02:11:46 GMT  
		Size: 7.6 MB (7611430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08eb19d48147b89f95d8896d76fd62f0697eb18d9fadb83cf4fe8b1fef9e4681`  
		Last Modified: Tue, 12 Jan 2021 02:11:44 GMT  
		Size: 1.1 MB (1125001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1892d5a5e1ff3c84006db8c0a0fd255087bab35e3d1d1f80da8b1e78ad50708`  
		Last Modified: Tue, 12 Jan 2021 02:11:45 GMT  
		Size: 3.1 KB (3058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ecf57c0d377e5760592842e4f021b29d7dd721e0969872f82394f023b29807`  
		Last Modified: Tue, 12 Jan 2021 02:11:45 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e35c7cd0713a880257fc4c28c42446e7ee37fe6235f2f32f7b16c3181dde4f7`  
		Last Modified: Tue, 12 Jan 2021 02:11:54 GMT  
		Size: 47.8 MB (47805337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50b3d346d14e77f5072e50ed4d55be61b607dbff24affc098cdaf89ae3e26d0`  
		Last Modified: Tue, 12 Jan 2021 02:11:41 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3d921e5f13021f67aba2ba902576f08b202fe39b38d660e3319f14e3fd5edd`  
		Last Modified: Tue, 12 Jan 2021 02:11:42 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6433843863b566073633e24fb26b5c0926cecb5ddf43fea475332326145bfe95`  
		Last Modified: Tue, 12 Jan 2021 02:11:41 GMT  
		Size: 2.1 KB (2068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5ee1e1e092238af8e93b4ecdcdf20a9e9fe802bfeb7680b4b19a9eee9fdaa4`  
		Last Modified: Tue, 12 Jan 2021 02:11:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3`

```console
$ docker pull couchdb@sha256:9c8aa0cf9e8029f1162fb467054d23f7b6ea7d1918b181eebedb4ca584287950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:7e374287cfa1f7d4ce9bd70286f143f99aa2b67c4c762c28a1c09d2dbfc993ea
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83352073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65ce6e3f7fc66f50cb6acfc26a74ec2cf23d4ae741318fea21fe49214b0fde4d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:49:23 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Jan 2021 03:49:24 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Jan 2021 03:49:33 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 03:49:33 GMT
ENV GOSU_VERSION=1.11
# Tue, 12 Jan 2021 03:49:33 GMT
ENV TINI_VERSION=0.18.0
# Tue, 12 Jan 2021 03:49:39 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 12 Jan 2021 03:49:39 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 12 Jan 2021 03:50:51 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 12 Jan 2021 03:50:51 GMT
ENV COUCHDB_VERSION=3.1.1
# Tue, 12 Jan 2021 03:50:52 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 12 Jan 2021 03:51:09 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Jan 2021 03:51:09 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Jan 2021 03:51:09 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Jan 2021 03:51:09 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 12 Jan 2021 03:51:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Jan 2021 03:51:11 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Jan 2021 03:51:11 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Jan 2021 03:51:11 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Jan 2021 03:51:11 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d64397181ee91050f1762374def7688fa28fb694ebca9607b9a3aa6572354f`  
		Last Modified: Tue, 12 Jan 2021 03:54:15 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bde8705eb543fe6c86547d8d82bdad7e03cd0320b4bcc5c5467fcd20ccc7f7`  
		Last Modified: Tue, 12 Jan 2021 03:54:15 GMT  
		Size: 6.7 MB (6669496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb9a606c61dbd6d0681e686307acfb5b6e6bcb485fc6b356eaa343345bf8bf5`  
		Last Modified: Tue, 12 Jan 2021 03:54:12 GMT  
		Size: 1.2 MB (1192711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb1a1ddacf3c4338daf4eed21374c917616c024869366a44a751e6f928d9a4e`  
		Last Modified: Tue, 12 Jan 2021 03:54:12 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeda1d5eae36c1bd6568e3b906ef6ca5ed27985a7af8c1057c35bfd3126ed74a`  
		Last Modified: Tue, 12 Jan 2021 03:54:12 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2cd25ac1f11f65d4adf8b07aa5c68003d5d0aad332d9f4de1c5794bc8d01d9c`  
		Last Modified: Tue, 12 Jan 2021 03:54:17 GMT  
		Size: 48.4 MB (48372335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce00a4cabfe9a6b357d6cdddb273bc5278fa186e57e03c993c24a7761db7c6a`  
		Last Modified: Tue, 12 Jan 2021 03:54:10 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64ca45e2f7eea6fffc4e0a895ecc6e577d174f80605db75d40a7dd3ec790393`  
		Last Modified: Tue, 12 Jan 2021 03:54:10 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6081e575864d56d24bb01a6060a7cdd1c7d76326419942b0c3629ec908c38bb`  
		Last Modified: Tue, 12 Jan 2021 03:54:12 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6904a13f618518b1a0236409c8ae4e7181903606432c2a4624418ac7b53b3809`  
		Last Modified: Tue, 12 Jan 2021 03:54:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:8f317d56350abe43761d86a708e7c6dff258d83d8677f6f26540f787f8958ad9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78391368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c03c462205826a0f78c8ff2db191d5e2bbce4bf8ba1dcb0a40e7ef6b90c027a9`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Jan 2021 00:41:13 GMT
ADD file:0252dccbbfb76766e0e189783d38f6a6afd13f44daa7c5370ffd094adea0f583 in / 
# Tue, 12 Jan 2021 00:41:21 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 02:04:54 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Jan 2021 02:04:57 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Jan 2021 02:05:15 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 02:05:17 GMT
ENV GOSU_VERSION=1.11
# Tue, 12 Jan 2021 02:05:18 GMT
ENV TINI_VERSION=0.18.0
# Tue, 12 Jan 2021 02:06:05 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 12 Jan 2021 02:06:06 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 12 Jan 2021 02:06:23 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 12 Jan 2021 02:06:24 GMT
ENV COUCHDB_VERSION=3.1.1
# Tue, 12 Jan 2021 02:06:26 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 12 Jan 2021 02:06:53 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Jan 2021 02:06:54 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Jan 2021 02:06:56 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Jan 2021 02:06:57 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 12 Jan 2021 02:06:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Jan 2021 02:07:00 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Jan 2021 02:07:01 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Jan 2021 02:07:03 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Jan 2021 02:07:04 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f8be76fcf2062bd14a3a78f858da701db8bcd907a2d0f33716d89d9329df2b1f`  
		Last Modified: Tue, 12 Jan 2021 00:51:54 GMT  
		Size: 25.9 MB (25864492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e438aed85b876dc1d5e3abe716b60e487649116ec5bdb2252faf4c457d4b29e`  
		Last Modified: Tue, 12 Jan 2021 02:11:08 GMT  
		Size: 3.4 KB (3437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba35939d871bf49516c4b8e9c49b082e7907547359c17edaf3ba93807d241099`  
		Last Modified: Tue, 12 Jan 2021 02:11:09 GMT  
		Size: 6.5 MB (6533527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7243f4e2d904bd229ea1848d840b6c156e276766e4ccb1b0158c12e5c85b3c70`  
		Last Modified: Tue, 12 Jan 2021 02:11:06 GMT  
		Size: 1.1 MB (1127120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a88a5b01dd81fc1acffe468a565449d2321064998727ea8be45934c77a1ea21`  
		Last Modified: Tue, 12 Jan 2021 02:11:05 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d51563f7b4ffd3ce59f748a3fefc37869c72d3eae53ce2c5835e5e229c9656`  
		Last Modified: Tue, 12 Jan 2021 02:11:04 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb419b9afdd147ed666a830bc8a7ef013f7093247dc848d131a12b61135e7ae7`  
		Last Modified: Tue, 12 Jan 2021 02:11:11 GMT  
		Size: 44.9 MB (44856747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4e4a029e01f6e635c0fe2ec44d3d25b23649453b5c79514042e6173655011f`  
		Last Modified: Tue, 12 Jan 2021 02:11:03 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb241969a20df2845dcd6b5189d901e33a20f2d81715bbbf6528d2150f6c6eab`  
		Last Modified: Tue, 12 Jan 2021 02:11:03 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe04d8ff39715883e5b0b7e16bafe58360da16bdf9f4e12e48ff2f64b0eb6578`  
		Last Modified: Tue, 12 Jan 2021 02:11:02 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4d12e6a014fe5b72b1021183d5a5a6b1053b592187dd107b2f57a1bd90ad8a`  
		Last Modified: Tue, 12 Jan 2021 02:11:03 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:0a24c8eef72922d639e04ea3b80ea53edba7909a1f52ffde36bcb0e0775d93e5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88514519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31145748472efdd0f90280a0b0d81a17c02a40e74fd9d2ff7ada83aefc7b28bf`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Jan 2021 00:25:06 GMT
ADD file:9d7252c169da9a089a0caa2f26cea24678267c15c0e129e7320d4defe0d4637b in / 
# Tue, 12 Jan 2021 00:25:16 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:23:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Jan 2021 01:23:59 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Jan 2021 01:26:26 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:26:32 GMT
ENV GOSU_VERSION=1.11
# Tue, 12 Jan 2021 01:26:36 GMT
ENV TINI_VERSION=0.18.0
# Tue, 12 Jan 2021 01:27:12 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 12 Jan 2021 01:27:18 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 12 Jan 2021 01:27:32 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 12 Jan 2021 01:27:37 GMT
ENV COUCHDB_VERSION=3.1.1
# Tue, 12 Jan 2021 01:27:45 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 12 Jan 2021 01:29:34 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Jan 2021 01:29:41 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Jan 2021 01:29:45 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Jan 2021 01:29:49 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 12 Jan 2021 01:30:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Jan 2021 01:30:06 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Jan 2021 01:30:11 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Jan 2021 01:30:16 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Jan 2021 01:30:19 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:cb701c1e59a3b25dcb09b089f31d61af3065659cd29a7c748f66f3e3c8a96d58`  
		Last Modified: Tue, 12 Jan 2021 00:34:11 GMT  
		Size: 30.5 MB (30532837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e70c701092def27535a2729a97ff54374694fb51d7b7a9178aa38719bcffcd1`  
		Last Modified: Tue, 12 Jan 2021 01:34:04 GMT  
		Size: 3.4 KB (3416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23a2d04a2cb1bf3e22af2f16579b13d8106e0343619a3250c0b79862ed60d92`  
		Last Modified: Tue, 12 Jan 2021 01:34:03 GMT  
		Size: 7.6 MB (7580646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1458c44d75dcadeb6308623a87b08d356bc5a584a1159ba562a34e6e9d4daa7f`  
		Last Modified: Tue, 12 Jan 2021 01:34:02 GMT  
		Size: 1.1 MB (1116280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03caed2b60160fa146791aa072bafcb43ab6f05d6bee03ccf248c727dcf7683`  
		Last Modified: Tue, 12 Jan 2021 01:33:59 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6ea873bcdc65542ad245b368c03dbcce37bc534759891dd050ba01cff75eb3`  
		Last Modified: Tue, 12 Jan 2021 01:33:59 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ee6ab5a64da42e0610a35550e605c9531358aa3173d2466cde8ec630e1e30b`  
		Last Modified: Tue, 12 Jan 2021 01:34:02 GMT  
		Size: 49.3 MB (49275292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14abc94d5ac1d6e515e44e2b70263a044da083a95536993d625511a144667da8`  
		Last Modified: Tue, 12 Jan 2021 01:33:53 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0102e2f339dd82e84045a1dfc50b7a13da8b93dd76a981d9d3147b02b86b4f83`  
		Last Modified: Tue, 12 Jan 2021 01:33:53 GMT  
		Size: 768.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3029afbd5b0172ae32e2189caee20d9b4ffbf6503e0971ffdbfb91390bbeac46`  
		Last Modified: Tue, 12 Jan 2021 01:33:53 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2524650ab85d0adda44b218c1f4117452025f17eb1c9cb6690ae49c9a6949f78`  
		Last Modified: Tue, 12 Jan 2021 01:33:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.0`

```console
$ docker pull couchdb@sha256:b55253cd9e7ee4074a3a4118257bf9978821b531f77bbb3e858e166455c785fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.0` - linux; amd64

```console
$ docker pull couchdb@sha256:14299273fffef70621d4cf2c2300cb8df29a4e92d929c9f1d731124d87a228ec
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83209548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208bc68637a5b3e7feb35a7742dc9a5ea3d5a2981a3fa832844db3ed8c5ec230`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:49:23 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Jan 2021 03:49:24 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Jan 2021 03:49:33 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 03:49:33 GMT
ENV GOSU_VERSION=1.11
# Tue, 12 Jan 2021 03:49:33 GMT
ENV TINI_VERSION=0.18.0
# Tue, 12 Jan 2021 03:49:39 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 12 Jan 2021 03:49:39 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 12 Jan 2021 03:50:51 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 12 Jan 2021 03:51:25 GMT
ENV COUCHDB_VERSION=3.0.1
# Tue, 12 Jan 2021 03:51:26 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 12 Jan 2021 03:51:43 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Jan 2021 03:51:44 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Jan 2021 03:51:44 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Jan 2021 03:51:44 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 12 Jan 2021 03:51:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Jan 2021 03:51:46 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Jan 2021 03:51:46 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Jan 2021 03:51:46 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Jan 2021 03:51:46 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d64397181ee91050f1762374def7688fa28fb694ebca9607b9a3aa6572354f`  
		Last Modified: Tue, 12 Jan 2021 03:54:15 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bde8705eb543fe6c86547d8d82bdad7e03cd0320b4bcc5c5467fcd20ccc7f7`  
		Last Modified: Tue, 12 Jan 2021 03:54:15 GMT  
		Size: 6.7 MB (6669496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb9a606c61dbd6d0681e686307acfb5b6e6bcb485fc6b356eaa343345bf8bf5`  
		Last Modified: Tue, 12 Jan 2021 03:54:12 GMT  
		Size: 1.2 MB (1192711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb1a1ddacf3c4338daf4eed21374c917616c024869366a44a751e6f928d9a4e`  
		Last Modified: Tue, 12 Jan 2021 03:54:12 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f6d8a1e69cb734127ef8e2f1e583eb1897afdd9417ff386052be6638c50f17`  
		Last Modified: Tue, 12 Jan 2021 03:54:33 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9b966e7658128aa8967b1a7e46e8b4168f87665da1997827e7085661bdb424c`  
		Last Modified: Tue, 12 Jan 2021 03:54:37 GMT  
		Size: 48.2 MB (48229815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30dbf89c4c399d8ab508357d9d769cca701354b62afdace374f340b7fa9321ae`  
		Last Modified: Tue, 12 Jan 2021 03:54:30 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab0a745a988bd2d9abf9852a5088a52a485d0b7cdf98170ecfc7173de0c94f7`  
		Last Modified: Tue, 12 Jan 2021 03:54:30 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d87fa0cc8a5f8e7898806c93a106b40ec41eb1c0fe15a9d280982c08f4d1f07`  
		Last Modified: Tue, 12 Jan 2021 03:54:31 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a5c1d8eb23b4ef8d4ff616463016e77a52f2cc56110cd136dfd10cb22fa49d`  
		Last Modified: Tue, 12 Jan 2021 03:54:34 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.0` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:32c8ce33ff84814fb524cbd071ed6ae47a4d5b83814446dd46e247a3740e7e3c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.2 MB (78242927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d716db17ae99f0c652abdd82cb6cd976d5ecb8dbe32cf7a45c53bb5ae7a1cf3`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Jan 2021 00:41:13 GMT
ADD file:0252dccbbfb76766e0e189783d38f6a6afd13f44daa7c5370ffd094adea0f583 in / 
# Tue, 12 Jan 2021 00:41:21 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 02:04:54 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Jan 2021 02:04:57 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Jan 2021 02:05:15 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 02:05:17 GMT
ENV GOSU_VERSION=1.11
# Tue, 12 Jan 2021 02:05:18 GMT
ENV TINI_VERSION=0.18.0
# Tue, 12 Jan 2021 02:06:05 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 12 Jan 2021 02:06:06 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 12 Jan 2021 02:06:23 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 12 Jan 2021 02:07:15 GMT
ENV COUCHDB_VERSION=3.0.1
# Tue, 12 Jan 2021 02:07:19 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 12 Jan 2021 02:07:49 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Jan 2021 02:07:50 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Jan 2021 02:07:51 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Jan 2021 02:07:52 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 12 Jan 2021 02:07:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Jan 2021 02:07:55 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Jan 2021 02:07:56 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Jan 2021 02:07:57 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Jan 2021 02:07:57 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f8be76fcf2062bd14a3a78f858da701db8bcd907a2d0f33716d89d9329df2b1f`  
		Last Modified: Tue, 12 Jan 2021 00:51:54 GMT  
		Size: 25.9 MB (25864492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e438aed85b876dc1d5e3abe716b60e487649116ec5bdb2252faf4c457d4b29e`  
		Last Modified: Tue, 12 Jan 2021 02:11:08 GMT  
		Size: 3.4 KB (3437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba35939d871bf49516c4b8e9c49b082e7907547359c17edaf3ba93807d241099`  
		Last Modified: Tue, 12 Jan 2021 02:11:09 GMT  
		Size: 6.5 MB (6533527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7243f4e2d904bd229ea1848d840b6c156e276766e4ccb1b0158c12e5c85b3c70`  
		Last Modified: Tue, 12 Jan 2021 02:11:06 GMT  
		Size: 1.1 MB (1127120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a88a5b01dd81fc1acffe468a565449d2321064998727ea8be45934c77a1ea21`  
		Last Modified: Tue, 12 Jan 2021 02:11:05 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4973305c26a99e6d2f068e61626f8d413a565fc5076b665035b0e3d7652b937e`  
		Last Modified: Tue, 12 Jan 2021 02:11:27 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b229614543a2561107721d9d2b30146fe2b26a2c25dc3ed2efa2d3c14a03702`  
		Last Modified: Tue, 12 Jan 2021 02:11:33 GMT  
		Size: 44.7 MB (44708313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba8e1a25d2f592f0b61638155bf69d4ac8e58ea4f6161f2b6a94f9b3181f41d`  
		Last Modified: Tue, 12 Jan 2021 02:11:25 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a568eb78097d2433f03e6c734a521fd2b25789be0180e3084264e1486edf21`  
		Last Modified: Tue, 12 Jan 2021 02:11:25 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be12ee4c9628dc520d343a952a8e8a31ac5f118c3e2840de04851b1aa7d6bec6`  
		Last Modified: Tue, 12 Jan 2021 02:11:24 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bbbd123ab25d1a3363de16fb7f110b1ec82517452b6f9087320454118897613`  
		Last Modified: Tue, 12 Jan 2021 02:11:25 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.0` - linux; ppc64le

```console
$ docker pull couchdb@sha256:f960dfb2b28854796014463ce92ba3248680b273aaddecdfa33c63d7950f5256
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 MB (88364595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff282912c0a5dc81f475e89052976fddab2b004f7872d50710da68ae37a95b1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Jan 2021 00:25:06 GMT
ADD file:9d7252c169da9a089a0caa2f26cea24678267c15c0e129e7320d4defe0d4637b in / 
# Tue, 12 Jan 2021 00:25:16 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:23:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Jan 2021 01:23:59 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Jan 2021 01:26:26 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:26:32 GMT
ENV GOSU_VERSION=1.11
# Tue, 12 Jan 2021 01:26:36 GMT
ENV TINI_VERSION=0.18.0
# Tue, 12 Jan 2021 01:27:12 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 12 Jan 2021 01:27:18 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 12 Jan 2021 01:27:32 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 12 Jan 2021 01:30:33 GMT
ENV COUCHDB_VERSION=3.0.1
# Tue, 12 Jan 2021 01:30:47 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 12 Jan 2021 01:33:05 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Jan 2021 01:33:09 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Jan 2021 01:33:11 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Jan 2021 01:33:14 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 12 Jan 2021 01:33:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Jan 2021 01:33:23 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Jan 2021 01:33:27 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Jan 2021 01:33:29 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Jan 2021 01:33:34 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:cb701c1e59a3b25dcb09b089f31d61af3065659cd29a7c748f66f3e3c8a96d58`  
		Last Modified: Tue, 12 Jan 2021 00:34:11 GMT  
		Size: 30.5 MB (30532837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e70c701092def27535a2729a97ff54374694fb51d7b7a9178aa38719bcffcd1`  
		Last Modified: Tue, 12 Jan 2021 01:34:04 GMT  
		Size: 3.4 KB (3416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23a2d04a2cb1bf3e22af2f16579b13d8106e0343619a3250c0b79862ed60d92`  
		Last Modified: Tue, 12 Jan 2021 01:34:03 GMT  
		Size: 7.6 MB (7580646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1458c44d75dcadeb6308623a87b08d356bc5a584a1159ba562a34e6e9d4daa7f`  
		Last Modified: Tue, 12 Jan 2021 01:34:02 GMT  
		Size: 1.1 MB (1116280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03caed2b60160fa146791aa072bafcb43ab6f05d6bee03ccf248c727dcf7683`  
		Last Modified: Tue, 12 Jan 2021 01:33:59 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb493f9930bbd069e6d927f6fc3a8691c82a158bdff9eb4b2194a56d54d9158`  
		Last Modified: Tue, 12 Jan 2021 01:34:31 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb79ebaf4a8fadcb2ca8c13f71ff845593603f8a62451a2cdb3ac7d2f8949122`  
		Last Modified: Tue, 12 Jan 2021 01:34:36 GMT  
		Size: 49.1 MB (49125367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4932bf0986656019a3c361cf4996f7cea0fd105b8ebd30570e1fd9f8d11a6bcf`  
		Last Modified: Tue, 12 Jan 2021 01:34:28 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef80172af7c130e8399acb4c6b5cb7530f4e755eb382dca1355cf44200f9da5`  
		Last Modified: Tue, 12 Jan 2021 01:34:27 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b7a95beb81d3cb4a819bd12ab8227d0ac57a43fa9a58cd57f2ea9fde601404`  
		Last Modified: Tue, 12 Jan 2021 01:34:27 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e03c08d7fb51c6dca4802dc38d7ca0cc36b487327cba9462733c0892ee7bed50`  
		Last Modified: Tue, 12 Jan 2021 01:34:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.0.1`

```console
$ docker pull couchdb@sha256:b55253cd9e7ee4074a3a4118257bf9978821b531f77bbb3e858e166455c785fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.0.1` - linux; amd64

```console
$ docker pull couchdb@sha256:14299273fffef70621d4cf2c2300cb8df29a4e92d929c9f1d731124d87a228ec
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83209548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208bc68637a5b3e7feb35a7742dc9a5ea3d5a2981a3fa832844db3ed8c5ec230`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:49:23 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Jan 2021 03:49:24 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Jan 2021 03:49:33 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 03:49:33 GMT
ENV GOSU_VERSION=1.11
# Tue, 12 Jan 2021 03:49:33 GMT
ENV TINI_VERSION=0.18.0
# Tue, 12 Jan 2021 03:49:39 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 12 Jan 2021 03:49:39 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 12 Jan 2021 03:50:51 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 12 Jan 2021 03:51:25 GMT
ENV COUCHDB_VERSION=3.0.1
# Tue, 12 Jan 2021 03:51:26 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 12 Jan 2021 03:51:43 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Jan 2021 03:51:44 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Jan 2021 03:51:44 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Jan 2021 03:51:44 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 12 Jan 2021 03:51:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Jan 2021 03:51:46 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Jan 2021 03:51:46 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Jan 2021 03:51:46 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Jan 2021 03:51:46 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d64397181ee91050f1762374def7688fa28fb694ebca9607b9a3aa6572354f`  
		Last Modified: Tue, 12 Jan 2021 03:54:15 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bde8705eb543fe6c86547d8d82bdad7e03cd0320b4bcc5c5467fcd20ccc7f7`  
		Last Modified: Tue, 12 Jan 2021 03:54:15 GMT  
		Size: 6.7 MB (6669496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb9a606c61dbd6d0681e686307acfb5b6e6bcb485fc6b356eaa343345bf8bf5`  
		Last Modified: Tue, 12 Jan 2021 03:54:12 GMT  
		Size: 1.2 MB (1192711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb1a1ddacf3c4338daf4eed21374c917616c024869366a44a751e6f928d9a4e`  
		Last Modified: Tue, 12 Jan 2021 03:54:12 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f6d8a1e69cb734127ef8e2f1e583eb1897afdd9417ff386052be6638c50f17`  
		Last Modified: Tue, 12 Jan 2021 03:54:33 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9b966e7658128aa8967b1a7e46e8b4168f87665da1997827e7085661bdb424c`  
		Last Modified: Tue, 12 Jan 2021 03:54:37 GMT  
		Size: 48.2 MB (48229815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30dbf89c4c399d8ab508357d9d769cca701354b62afdace374f340b7fa9321ae`  
		Last Modified: Tue, 12 Jan 2021 03:54:30 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab0a745a988bd2d9abf9852a5088a52a485d0b7cdf98170ecfc7173de0c94f7`  
		Last Modified: Tue, 12 Jan 2021 03:54:30 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d87fa0cc8a5f8e7898806c93a106b40ec41eb1c0fe15a9d280982c08f4d1f07`  
		Last Modified: Tue, 12 Jan 2021 03:54:31 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a5c1d8eb23b4ef8d4ff616463016e77a52f2cc56110cd136dfd10cb22fa49d`  
		Last Modified: Tue, 12 Jan 2021 03:54:34 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.0.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:32c8ce33ff84814fb524cbd071ed6ae47a4d5b83814446dd46e247a3740e7e3c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.2 MB (78242927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d716db17ae99f0c652abdd82cb6cd976d5ecb8dbe32cf7a45c53bb5ae7a1cf3`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Jan 2021 00:41:13 GMT
ADD file:0252dccbbfb76766e0e189783d38f6a6afd13f44daa7c5370ffd094adea0f583 in / 
# Tue, 12 Jan 2021 00:41:21 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 02:04:54 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Jan 2021 02:04:57 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Jan 2021 02:05:15 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 02:05:17 GMT
ENV GOSU_VERSION=1.11
# Tue, 12 Jan 2021 02:05:18 GMT
ENV TINI_VERSION=0.18.0
# Tue, 12 Jan 2021 02:06:05 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 12 Jan 2021 02:06:06 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 12 Jan 2021 02:06:23 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 12 Jan 2021 02:07:15 GMT
ENV COUCHDB_VERSION=3.0.1
# Tue, 12 Jan 2021 02:07:19 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 12 Jan 2021 02:07:49 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Jan 2021 02:07:50 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Jan 2021 02:07:51 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Jan 2021 02:07:52 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 12 Jan 2021 02:07:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Jan 2021 02:07:55 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Jan 2021 02:07:56 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Jan 2021 02:07:57 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Jan 2021 02:07:57 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f8be76fcf2062bd14a3a78f858da701db8bcd907a2d0f33716d89d9329df2b1f`  
		Last Modified: Tue, 12 Jan 2021 00:51:54 GMT  
		Size: 25.9 MB (25864492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e438aed85b876dc1d5e3abe716b60e487649116ec5bdb2252faf4c457d4b29e`  
		Last Modified: Tue, 12 Jan 2021 02:11:08 GMT  
		Size: 3.4 KB (3437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba35939d871bf49516c4b8e9c49b082e7907547359c17edaf3ba93807d241099`  
		Last Modified: Tue, 12 Jan 2021 02:11:09 GMT  
		Size: 6.5 MB (6533527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7243f4e2d904bd229ea1848d840b6c156e276766e4ccb1b0158c12e5c85b3c70`  
		Last Modified: Tue, 12 Jan 2021 02:11:06 GMT  
		Size: 1.1 MB (1127120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a88a5b01dd81fc1acffe468a565449d2321064998727ea8be45934c77a1ea21`  
		Last Modified: Tue, 12 Jan 2021 02:11:05 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4973305c26a99e6d2f068e61626f8d413a565fc5076b665035b0e3d7652b937e`  
		Last Modified: Tue, 12 Jan 2021 02:11:27 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b229614543a2561107721d9d2b30146fe2b26a2c25dc3ed2efa2d3c14a03702`  
		Last Modified: Tue, 12 Jan 2021 02:11:33 GMT  
		Size: 44.7 MB (44708313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba8e1a25d2f592f0b61638155bf69d4ac8e58ea4f6161f2b6a94f9b3181f41d`  
		Last Modified: Tue, 12 Jan 2021 02:11:25 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a568eb78097d2433f03e6c734a521fd2b25789be0180e3084264e1486edf21`  
		Last Modified: Tue, 12 Jan 2021 02:11:25 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be12ee4c9628dc520d343a952a8e8a31ac5f118c3e2840de04851b1aa7d6bec6`  
		Last Modified: Tue, 12 Jan 2021 02:11:24 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bbbd123ab25d1a3363de16fb7f110b1ec82517452b6f9087320454118897613`  
		Last Modified: Tue, 12 Jan 2021 02:11:25 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.0.1` - linux; ppc64le

```console
$ docker pull couchdb@sha256:f960dfb2b28854796014463ce92ba3248680b273aaddecdfa33c63d7950f5256
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 MB (88364595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff282912c0a5dc81f475e89052976fddab2b004f7872d50710da68ae37a95b1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Jan 2021 00:25:06 GMT
ADD file:9d7252c169da9a089a0caa2f26cea24678267c15c0e129e7320d4defe0d4637b in / 
# Tue, 12 Jan 2021 00:25:16 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:23:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Jan 2021 01:23:59 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Jan 2021 01:26:26 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:26:32 GMT
ENV GOSU_VERSION=1.11
# Tue, 12 Jan 2021 01:26:36 GMT
ENV TINI_VERSION=0.18.0
# Tue, 12 Jan 2021 01:27:12 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 12 Jan 2021 01:27:18 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 12 Jan 2021 01:27:32 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 12 Jan 2021 01:30:33 GMT
ENV COUCHDB_VERSION=3.0.1
# Tue, 12 Jan 2021 01:30:47 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 12 Jan 2021 01:33:05 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Jan 2021 01:33:09 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Jan 2021 01:33:11 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Jan 2021 01:33:14 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 12 Jan 2021 01:33:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Jan 2021 01:33:23 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Jan 2021 01:33:27 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Jan 2021 01:33:29 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Jan 2021 01:33:34 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:cb701c1e59a3b25dcb09b089f31d61af3065659cd29a7c748f66f3e3c8a96d58`  
		Last Modified: Tue, 12 Jan 2021 00:34:11 GMT  
		Size: 30.5 MB (30532837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e70c701092def27535a2729a97ff54374694fb51d7b7a9178aa38719bcffcd1`  
		Last Modified: Tue, 12 Jan 2021 01:34:04 GMT  
		Size: 3.4 KB (3416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23a2d04a2cb1bf3e22af2f16579b13d8106e0343619a3250c0b79862ed60d92`  
		Last Modified: Tue, 12 Jan 2021 01:34:03 GMT  
		Size: 7.6 MB (7580646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1458c44d75dcadeb6308623a87b08d356bc5a584a1159ba562a34e6e9d4daa7f`  
		Last Modified: Tue, 12 Jan 2021 01:34:02 GMT  
		Size: 1.1 MB (1116280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03caed2b60160fa146791aa072bafcb43ab6f05d6bee03ccf248c727dcf7683`  
		Last Modified: Tue, 12 Jan 2021 01:33:59 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb493f9930bbd069e6d927f6fc3a8691c82a158bdff9eb4b2194a56d54d9158`  
		Last Modified: Tue, 12 Jan 2021 01:34:31 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb79ebaf4a8fadcb2ca8c13f71ff845593603f8a62451a2cdb3ac7d2f8949122`  
		Last Modified: Tue, 12 Jan 2021 01:34:36 GMT  
		Size: 49.1 MB (49125367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4932bf0986656019a3c361cf4996f7cea0fd105b8ebd30570e1fd9f8d11a6bcf`  
		Last Modified: Tue, 12 Jan 2021 01:34:28 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef80172af7c130e8399acb4c6b5cb7530f4e755eb382dca1355cf44200f9da5`  
		Last Modified: Tue, 12 Jan 2021 01:34:27 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b7a95beb81d3cb4a819bd12ab8227d0ac57a43fa9a58cd57f2ea9fde601404`  
		Last Modified: Tue, 12 Jan 2021 01:34:27 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e03c08d7fb51c6dca4802dc38d7ca0cc36b487327cba9462733c0892ee7bed50`  
		Last Modified: Tue, 12 Jan 2021 01:34:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:9c8aa0cf9e8029f1162fb467054d23f7b6ea7d1918b181eebedb4ca584287950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:7e374287cfa1f7d4ce9bd70286f143f99aa2b67c4c762c28a1c09d2dbfc993ea
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83352073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65ce6e3f7fc66f50cb6acfc26a74ec2cf23d4ae741318fea21fe49214b0fde4d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:49:23 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Jan 2021 03:49:24 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Jan 2021 03:49:33 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 03:49:33 GMT
ENV GOSU_VERSION=1.11
# Tue, 12 Jan 2021 03:49:33 GMT
ENV TINI_VERSION=0.18.0
# Tue, 12 Jan 2021 03:49:39 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 12 Jan 2021 03:49:39 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 12 Jan 2021 03:50:51 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 12 Jan 2021 03:50:51 GMT
ENV COUCHDB_VERSION=3.1.1
# Tue, 12 Jan 2021 03:50:52 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 12 Jan 2021 03:51:09 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Jan 2021 03:51:09 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Jan 2021 03:51:09 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Jan 2021 03:51:09 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 12 Jan 2021 03:51:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Jan 2021 03:51:11 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Jan 2021 03:51:11 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Jan 2021 03:51:11 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Jan 2021 03:51:11 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d64397181ee91050f1762374def7688fa28fb694ebca9607b9a3aa6572354f`  
		Last Modified: Tue, 12 Jan 2021 03:54:15 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bde8705eb543fe6c86547d8d82bdad7e03cd0320b4bcc5c5467fcd20ccc7f7`  
		Last Modified: Tue, 12 Jan 2021 03:54:15 GMT  
		Size: 6.7 MB (6669496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb9a606c61dbd6d0681e686307acfb5b6e6bcb485fc6b356eaa343345bf8bf5`  
		Last Modified: Tue, 12 Jan 2021 03:54:12 GMT  
		Size: 1.2 MB (1192711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb1a1ddacf3c4338daf4eed21374c917616c024869366a44a751e6f928d9a4e`  
		Last Modified: Tue, 12 Jan 2021 03:54:12 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeda1d5eae36c1bd6568e3b906ef6ca5ed27985a7af8c1057c35bfd3126ed74a`  
		Last Modified: Tue, 12 Jan 2021 03:54:12 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2cd25ac1f11f65d4adf8b07aa5c68003d5d0aad332d9f4de1c5794bc8d01d9c`  
		Last Modified: Tue, 12 Jan 2021 03:54:17 GMT  
		Size: 48.4 MB (48372335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce00a4cabfe9a6b357d6cdddb273bc5278fa186e57e03c993c24a7761db7c6a`  
		Last Modified: Tue, 12 Jan 2021 03:54:10 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64ca45e2f7eea6fffc4e0a895ecc6e577d174f80605db75d40a7dd3ec790393`  
		Last Modified: Tue, 12 Jan 2021 03:54:10 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6081e575864d56d24bb01a6060a7cdd1c7d76326419942b0c3629ec908c38bb`  
		Last Modified: Tue, 12 Jan 2021 03:54:12 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6904a13f618518b1a0236409c8ae4e7181903606432c2a4624418ac7b53b3809`  
		Last Modified: Tue, 12 Jan 2021 03:54:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:8f317d56350abe43761d86a708e7c6dff258d83d8677f6f26540f787f8958ad9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78391368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c03c462205826a0f78c8ff2db191d5e2bbce4bf8ba1dcb0a40e7ef6b90c027a9`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Jan 2021 00:41:13 GMT
ADD file:0252dccbbfb76766e0e189783d38f6a6afd13f44daa7c5370ffd094adea0f583 in / 
# Tue, 12 Jan 2021 00:41:21 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 02:04:54 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Jan 2021 02:04:57 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Jan 2021 02:05:15 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 02:05:17 GMT
ENV GOSU_VERSION=1.11
# Tue, 12 Jan 2021 02:05:18 GMT
ENV TINI_VERSION=0.18.0
# Tue, 12 Jan 2021 02:06:05 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 12 Jan 2021 02:06:06 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 12 Jan 2021 02:06:23 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 12 Jan 2021 02:06:24 GMT
ENV COUCHDB_VERSION=3.1.1
# Tue, 12 Jan 2021 02:06:26 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 12 Jan 2021 02:06:53 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Jan 2021 02:06:54 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Jan 2021 02:06:56 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Jan 2021 02:06:57 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 12 Jan 2021 02:06:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Jan 2021 02:07:00 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Jan 2021 02:07:01 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Jan 2021 02:07:03 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Jan 2021 02:07:04 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f8be76fcf2062bd14a3a78f858da701db8bcd907a2d0f33716d89d9329df2b1f`  
		Last Modified: Tue, 12 Jan 2021 00:51:54 GMT  
		Size: 25.9 MB (25864492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e438aed85b876dc1d5e3abe716b60e487649116ec5bdb2252faf4c457d4b29e`  
		Last Modified: Tue, 12 Jan 2021 02:11:08 GMT  
		Size: 3.4 KB (3437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba35939d871bf49516c4b8e9c49b082e7907547359c17edaf3ba93807d241099`  
		Last Modified: Tue, 12 Jan 2021 02:11:09 GMT  
		Size: 6.5 MB (6533527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7243f4e2d904bd229ea1848d840b6c156e276766e4ccb1b0158c12e5c85b3c70`  
		Last Modified: Tue, 12 Jan 2021 02:11:06 GMT  
		Size: 1.1 MB (1127120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a88a5b01dd81fc1acffe468a565449d2321064998727ea8be45934c77a1ea21`  
		Last Modified: Tue, 12 Jan 2021 02:11:05 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d51563f7b4ffd3ce59f748a3fefc37869c72d3eae53ce2c5835e5e229c9656`  
		Last Modified: Tue, 12 Jan 2021 02:11:04 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb419b9afdd147ed666a830bc8a7ef013f7093247dc848d131a12b61135e7ae7`  
		Last Modified: Tue, 12 Jan 2021 02:11:11 GMT  
		Size: 44.9 MB (44856747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4e4a029e01f6e635c0fe2ec44d3d25b23649453b5c79514042e6173655011f`  
		Last Modified: Tue, 12 Jan 2021 02:11:03 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb241969a20df2845dcd6b5189d901e33a20f2d81715bbbf6528d2150f6c6eab`  
		Last Modified: Tue, 12 Jan 2021 02:11:03 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe04d8ff39715883e5b0b7e16bafe58360da16bdf9f4e12e48ff2f64b0eb6578`  
		Last Modified: Tue, 12 Jan 2021 02:11:02 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4d12e6a014fe5b72b1021183d5a5a6b1053b592187dd107b2f57a1bd90ad8a`  
		Last Modified: Tue, 12 Jan 2021 02:11:03 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1` - linux; ppc64le

```console
$ docker pull couchdb@sha256:0a24c8eef72922d639e04ea3b80ea53edba7909a1f52ffde36bcb0e0775d93e5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88514519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31145748472efdd0f90280a0b0d81a17c02a40e74fd9d2ff7ada83aefc7b28bf`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Jan 2021 00:25:06 GMT
ADD file:9d7252c169da9a089a0caa2f26cea24678267c15c0e129e7320d4defe0d4637b in / 
# Tue, 12 Jan 2021 00:25:16 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:23:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Jan 2021 01:23:59 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Jan 2021 01:26:26 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:26:32 GMT
ENV GOSU_VERSION=1.11
# Tue, 12 Jan 2021 01:26:36 GMT
ENV TINI_VERSION=0.18.0
# Tue, 12 Jan 2021 01:27:12 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 12 Jan 2021 01:27:18 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 12 Jan 2021 01:27:32 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 12 Jan 2021 01:27:37 GMT
ENV COUCHDB_VERSION=3.1.1
# Tue, 12 Jan 2021 01:27:45 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 12 Jan 2021 01:29:34 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Jan 2021 01:29:41 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Jan 2021 01:29:45 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Jan 2021 01:29:49 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 12 Jan 2021 01:30:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Jan 2021 01:30:06 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Jan 2021 01:30:11 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Jan 2021 01:30:16 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Jan 2021 01:30:19 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:cb701c1e59a3b25dcb09b089f31d61af3065659cd29a7c748f66f3e3c8a96d58`  
		Last Modified: Tue, 12 Jan 2021 00:34:11 GMT  
		Size: 30.5 MB (30532837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e70c701092def27535a2729a97ff54374694fb51d7b7a9178aa38719bcffcd1`  
		Last Modified: Tue, 12 Jan 2021 01:34:04 GMT  
		Size: 3.4 KB (3416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23a2d04a2cb1bf3e22af2f16579b13d8106e0343619a3250c0b79862ed60d92`  
		Last Modified: Tue, 12 Jan 2021 01:34:03 GMT  
		Size: 7.6 MB (7580646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1458c44d75dcadeb6308623a87b08d356bc5a584a1159ba562a34e6e9d4daa7f`  
		Last Modified: Tue, 12 Jan 2021 01:34:02 GMT  
		Size: 1.1 MB (1116280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03caed2b60160fa146791aa072bafcb43ab6f05d6bee03ccf248c727dcf7683`  
		Last Modified: Tue, 12 Jan 2021 01:33:59 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6ea873bcdc65542ad245b368c03dbcce37bc534759891dd050ba01cff75eb3`  
		Last Modified: Tue, 12 Jan 2021 01:33:59 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ee6ab5a64da42e0610a35550e605c9531358aa3173d2466cde8ec630e1e30b`  
		Last Modified: Tue, 12 Jan 2021 01:34:02 GMT  
		Size: 49.3 MB (49275292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14abc94d5ac1d6e515e44e2b70263a044da083a95536993d625511a144667da8`  
		Last Modified: Tue, 12 Jan 2021 01:33:53 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0102e2f339dd82e84045a1dfc50b7a13da8b93dd76a981d9d3147b02b86b4f83`  
		Last Modified: Tue, 12 Jan 2021 01:33:53 GMT  
		Size: 768.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3029afbd5b0172ae32e2189caee20d9b4ffbf6503e0971ffdbfb91390bbeac46`  
		Last Modified: Tue, 12 Jan 2021 01:33:53 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2524650ab85d0adda44b218c1f4117452025f17eb1c9cb6690ae49c9a6949f78`  
		Last Modified: Tue, 12 Jan 2021 01:33:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1.1`

```console
$ docker pull couchdb@sha256:9c8aa0cf9e8029f1162fb467054d23f7b6ea7d1918b181eebedb4ca584287950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.1.1` - linux; amd64

```console
$ docker pull couchdb@sha256:7e374287cfa1f7d4ce9bd70286f143f99aa2b67c4c762c28a1c09d2dbfc993ea
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83352073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65ce6e3f7fc66f50cb6acfc26a74ec2cf23d4ae741318fea21fe49214b0fde4d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:49:23 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Jan 2021 03:49:24 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Jan 2021 03:49:33 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 03:49:33 GMT
ENV GOSU_VERSION=1.11
# Tue, 12 Jan 2021 03:49:33 GMT
ENV TINI_VERSION=0.18.0
# Tue, 12 Jan 2021 03:49:39 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 12 Jan 2021 03:49:39 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 12 Jan 2021 03:50:51 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 12 Jan 2021 03:50:51 GMT
ENV COUCHDB_VERSION=3.1.1
# Tue, 12 Jan 2021 03:50:52 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 12 Jan 2021 03:51:09 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Jan 2021 03:51:09 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Jan 2021 03:51:09 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Jan 2021 03:51:09 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 12 Jan 2021 03:51:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Jan 2021 03:51:11 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Jan 2021 03:51:11 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Jan 2021 03:51:11 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Jan 2021 03:51:11 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d64397181ee91050f1762374def7688fa28fb694ebca9607b9a3aa6572354f`  
		Last Modified: Tue, 12 Jan 2021 03:54:15 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bde8705eb543fe6c86547d8d82bdad7e03cd0320b4bcc5c5467fcd20ccc7f7`  
		Last Modified: Tue, 12 Jan 2021 03:54:15 GMT  
		Size: 6.7 MB (6669496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb9a606c61dbd6d0681e686307acfb5b6e6bcb485fc6b356eaa343345bf8bf5`  
		Last Modified: Tue, 12 Jan 2021 03:54:12 GMT  
		Size: 1.2 MB (1192711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb1a1ddacf3c4338daf4eed21374c917616c024869366a44a751e6f928d9a4e`  
		Last Modified: Tue, 12 Jan 2021 03:54:12 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeda1d5eae36c1bd6568e3b906ef6ca5ed27985a7af8c1057c35bfd3126ed74a`  
		Last Modified: Tue, 12 Jan 2021 03:54:12 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2cd25ac1f11f65d4adf8b07aa5c68003d5d0aad332d9f4de1c5794bc8d01d9c`  
		Last Modified: Tue, 12 Jan 2021 03:54:17 GMT  
		Size: 48.4 MB (48372335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce00a4cabfe9a6b357d6cdddb273bc5278fa186e57e03c993c24a7761db7c6a`  
		Last Modified: Tue, 12 Jan 2021 03:54:10 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64ca45e2f7eea6fffc4e0a895ecc6e577d174f80605db75d40a7dd3ec790393`  
		Last Modified: Tue, 12 Jan 2021 03:54:10 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6081e575864d56d24bb01a6060a7cdd1c7d76326419942b0c3629ec908c38bb`  
		Last Modified: Tue, 12 Jan 2021 03:54:12 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6904a13f618518b1a0236409c8ae4e7181903606432c2a4624418ac7b53b3809`  
		Last Modified: Tue, 12 Jan 2021 03:54:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:8f317d56350abe43761d86a708e7c6dff258d83d8677f6f26540f787f8958ad9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78391368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c03c462205826a0f78c8ff2db191d5e2bbce4bf8ba1dcb0a40e7ef6b90c027a9`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Jan 2021 00:41:13 GMT
ADD file:0252dccbbfb76766e0e189783d38f6a6afd13f44daa7c5370ffd094adea0f583 in / 
# Tue, 12 Jan 2021 00:41:21 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 02:04:54 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Jan 2021 02:04:57 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Jan 2021 02:05:15 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 02:05:17 GMT
ENV GOSU_VERSION=1.11
# Tue, 12 Jan 2021 02:05:18 GMT
ENV TINI_VERSION=0.18.0
# Tue, 12 Jan 2021 02:06:05 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 12 Jan 2021 02:06:06 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 12 Jan 2021 02:06:23 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 12 Jan 2021 02:06:24 GMT
ENV COUCHDB_VERSION=3.1.1
# Tue, 12 Jan 2021 02:06:26 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 12 Jan 2021 02:06:53 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Jan 2021 02:06:54 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Jan 2021 02:06:56 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Jan 2021 02:06:57 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 12 Jan 2021 02:06:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Jan 2021 02:07:00 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Jan 2021 02:07:01 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Jan 2021 02:07:03 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Jan 2021 02:07:04 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f8be76fcf2062bd14a3a78f858da701db8bcd907a2d0f33716d89d9329df2b1f`  
		Last Modified: Tue, 12 Jan 2021 00:51:54 GMT  
		Size: 25.9 MB (25864492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e438aed85b876dc1d5e3abe716b60e487649116ec5bdb2252faf4c457d4b29e`  
		Last Modified: Tue, 12 Jan 2021 02:11:08 GMT  
		Size: 3.4 KB (3437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba35939d871bf49516c4b8e9c49b082e7907547359c17edaf3ba93807d241099`  
		Last Modified: Tue, 12 Jan 2021 02:11:09 GMT  
		Size: 6.5 MB (6533527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7243f4e2d904bd229ea1848d840b6c156e276766e4ccb1b0158c12e5c85b3c70`  
		Last Modified: Tue, 12 Jan 2021 02:11:06 GMT  
		Size: 1.1 MB (1127120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a88a5b01dd81fc1acffe468a565449d2321064998727ea8be45934c77a1ea21`  
		Last Modified: Tue, 12 Jan 2021 02:11:05 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d51563f7b4ffd3ce59f748a3fefc37869c72d3eae53ce2c5835e5e229c9656`  
		Last Modified: Tue, 12 Jan 2021 02:11:04 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb419b9afdd147ed666a830bc8a7ef013f7093247dc848d131a12b61135e7ae7`  
		Last Modified: Tue, 12 Jan 2021 02:11:11 GMT  
		Size: 44.9 MB (44856747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4e4a029e01f6e635c0fe2ec44d3d25b23649453b5c79514042e6173655011f`  
		Last Modified: Tue, 12 Jan 2021 02:11:03 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb241969a20df2845dcd6b5189d901e33a20f2d81715bbbf6528d2150f6c6eab`  
		Last Modified: Tue, 12 Jan 2021 02:11:03 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe04d8ff39715883e5b0b7e16bafe58360da16bdf9f4e12e48ff2f64b0eb6578`  
		Last Modified: Tue, 12 Jan 2021 02:11:02 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4d12e6a014fe5b72b1021183d5a5a6b1053b592187dd107b2f57a1bd90ad8a`  
		Last Modified: Tue, 12 Jan 2021 02:11:03 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1.1` - linux; ppc64le

```console
$ docker pull couchdb@sha256:0a24c8eef72922d639e04ea3b80ea53edba7909a1f52ffde36bcb0e0775d93e5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88514519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31145748472efdd0f90280a0b0d81a17c02a40e74fd9d2ff7ada83aefc7b28bf`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Jan 2021 00:25:06 GMT
ADD file:9d7252c169da9a089a0caa2f26cea24678267c15c0e129e7320d4defe0d4637b in / 
# Tue, 12 Jan 2021 00:25:16 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:23:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Jan 2021 01:23:59 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Jan 2021 01:26:26 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:26:32 GMT
ENV GOSU_VERSION=1.11
# Tue, 12 Jan 2021 01:26:36 GMT
ENV TINI_VERSION=0.18.0
# Tue, 12 Jan 2021 01:27:12 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 12 Jan 2021 01:27:18 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 12 Jan 2021 01:27:32 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 12 Jan 2021 01:27:37 GMT
ENV COUCHDB_VERSION=3.1.1
# Tue, 12 Jan 2021 01:27:45 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 12 Jan 2021 01:29:34 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Jan 2021 01:29:41 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Jan 2021 01:29:45 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Jan 2021 01:29:49 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 12 Jan 2021 01:30:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Jan 2021 01:30:06 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Jan 2021 01:30:11 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Jan 2021 01:30:16 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Jan 2021 01:30:19 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:cb701c1e59a3b25dcb09b089f31d61af3065659cd29a7c748f66f3e3c8a96d58`  
		Last Modified: Tue, 12 Jan 2021 00:34:11 GMT  
		Size: 30.5 MB (30532837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e70c701092def27535a2729a97ff54374694fb51d7b7a9178aa38719bcffcd1`  
		Last Modified: Tue, 12 Jan 2021 01:34:04 GMT  
		Size: 3.4 KB (3416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23a2d04a2cb1bf3e22af2f16579b13d8106e0343619a3250c0b79862ed60d92`  
		Last Modified: Tue, 12 Jan 2021 01:34:03 GMT  
		Size: 7.6 MB (7580646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1458c44d75dcadeb6308623a87b08d356bc5a584a1159ba562a34e6e9d4daa7f`  
		Last Modified: Tue, 12 Jan 2021 01:34:02 GMT  
		Size: 1.1 MB (1116280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03caed2b60160fa146791aa072bafcb43ab6f05d6bee03ccf248c727dcf7683`  
		Last Modified: Tue, 12 Jan 2021 01:33:59 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6ea873bcdc65542ad245b368c03dbcce37bc534759891dd050ba01cff75eb3`  
		Last Modified: Tue, 12 Jan 2021 01:33:59 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ee6ab5a64da42e0610a35550e605c9531358aa3173d2466cde8ec630e1e30b`  
		Last Modified: Tue, 12 Jan 2021 01:34:02 GMT  
		Size: 49.3 MB (49275292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14abc94d5ac1d6e515e44e2b70263a044da083a95536993d625511a144667da8`  
		Last Modified: Tue, 12 Jan 2021 01:33:53 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0102e2f339dd82e84045a1dfc50b7a13da8b93dd76a981d9d3147b02b86b4f83`  
		Last Modified: Tue, 12 Jan 2021 01:33:53 GMT  
		Size: 768.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3029afbd5b0172ae32e2189caee20d9b4ffbf6503e0971ffdbfb91390bbeac46`  
		Last Modified: Tue, 12 Jan 2021 01:33:53 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2524650ab85d0adda44b218c1f4117452025f17eb1c9cb6690ae49c9a6949f78`  
		Last Modified: Tue, 12 Jan 2021 01:33:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:9c8aa0cf9e8029f1162fb467054d23f7b6ea7d1918b181eebedb4ca584287950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:7e374287cfa1f7d4ce9bd70286f143f99aa2b67c4c762c28a1c09d2dbfc993ea
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83352073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65ce6e3f7fc66f50cb6acfc26a74ec2cf23d4ae741318fea21fe49214b0fde4d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:49:23 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Jan 2021 03:49:24 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Jan 2021 03:49:33 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 03:49:33 GMT
ENV GOSU_VERSION=1.11
# Tue, 12 Jan 2021 03:49:33 GMT
ENV TINI_VERSION=0.18.0
# Tue, 12 Jan 2021 03:49:39 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 12 Jan 2021 03:49:39 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 12 Jan 2021 03:50:51 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 12 Jan 2021 03:50:51 GMT
ENV COUCHDB_VERSION=3.1.1
# Tue, 12 Jan 2021 03:50:52 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 12 Jan 2021 03:51:09 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Jan 2021 03:51:09 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Jan 2021 03:51:09 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Jan 2021 03:51:09 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 12 Jan 2021 03:51:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Jan 2021 03:51:11 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Jan 2021 03:51:11 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Jan 2021 03:51:11 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Jan 2021 03:51:11 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d64397181ee91050f1762374def7688fa28fb694ebca9607b9a3aa6572354f`  
		Last Modified: Tue, 12 Jan 2021 03:54:15 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bde8705eb543fe6c86547d8d82bdad7e03cd0320b4bcc5c5467fcd20ccc7f7`  
		Last Modified: Tue, 12 Jan 2021 03:54:15 GMT  
		Size: 6.7 MB (6669496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb9a606c61dbd6d0681e686307acfb5b6e6bcb485fc6b356eaa343345bf8bf5`  
		Last Modified: Tue, 12 Jan 2021 03:54:12 GMT  
		Size: 1.2 MB (1192711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb1a1ddacf3c4338daf4eed21374c917616c024869366a44a751e6f928d9a4e`  
		Last Modified: Tue, 12 Jan 2021 03:54:12 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeda1d5eae36c1bd6568e3b906ef6ca5ed27985a7af8c1057c35bfd3126ed74a`  
		Last Modified: Tue, 12 Jan 2021 03:54:12 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2cd25ac1f11f65d4adf8b07aa5c68003d5d0aad332d9f4de1c5794bc8d01d9c`  
		Last Modified: Tue, 12 Jan 2021 03:54:17 GMT  
		Size: 48.4 MB (48372335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce00a4cabfe9a6b357d6cdddb273bc5278fa186e57e03c993c24a7761db7c6a`  
		Last Modified: Tue, 12 Jan 2021 03:54:10 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64ca45e2f7eea6fffc4e0a895ecc6e577d174f80605db75d40a7dd3ec790393`  
		Last Modified: Tue, 12 Jan 2021 03:54:10 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6081e575864d56d24bb01a6060a7cdd1c7d76326419942b0c3629ec908c38bb`  
		Last Modified: Tue, 12 Jan 2021 03:54:12 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6904a13f618518b1a0236409c8ae4e7181903606432c2a4624418ac7b53b3809`  
		Last Modified: Tue, 12 Jan 2021 03:54:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:8f317d56350abe43761d86a708e7c6dff258d83d8677f6f26540f787f8958ad9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78391368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c03c462205826a0f78c8ff2db191d5e2bbce4bf8ba1dcb0a40e7ef6b90c027a9`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Jan 2021 00:41:13 GMT
ADD file:0252dccbbfb76766e0e189783d38f6a6afd13f44daa7c5370ffd094adea0f583 in / 
# Tue, 12 Jan 2021 00:41:21 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 02:04:54 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Jan 2021 02:04:57 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Jan 2021 02:05:15 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 02:05:17 GMT
ENV GOSU_VERSION=1.11
# Tue, 12 Jan 2021 02:05:18 GMT
ENV TINI_VERSION=0.18.0
# Tue, 12 Jan 2021 02:06:05 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 12 Jan 2021 02:06:06 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 12 Jan 2021 02:06:23 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 12 Jan 2021 02:06:24 GMT
ENV COUCHDB_VERSION=3.1.1
# Tue, 12 Jan 2021 02:06:26 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 12 Jan 2021 02:06:53 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Jan 2021 02:06:54 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Jan 2021 02:06:56 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Jan 2021 02:06:57 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 12 Jan 2021 02:06:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Jan 2021 02:07:00 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Jan 2021 02:07:01 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Jan 2021 02:07:03 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Jan 2021 02:07:04 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f8be76fcf2062bd14a3a78f858da701db8bcd907a2d0f33716d89d9329df2b1f`  
		Last Modified: Tue, 12 Jan 2021 00:51:54 GMT  
		Size: 25.9 MB (25864492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e438aed85b876dc1d5e3abe716b60e487649116ec5bdb2252faf4c457d4b29e`  
		Last Modified: Tue, 12 Jan 2021 02:11:08 GMT  
		Size: 3.4 KB (3437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba35939d871bf49516c4b8e9c49b082e7907547359c17edaf3ba93807d241099`  
		Last Modified: Tue, 12 Jan 2021 02:11:09 GMT  
		Size: 6.5 MB (6533527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7243f4e2d904bd229ea1848d840b6c156e276766e4ccb1b0158c12e5c85b3c70`  
		Last Modified: Tue, 12 Jan 2021 02:11:06 GMT  
		Size: 1.1 MB (1127120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a88a5b01dd81fc1acffe468a565449d2321064998727ea8be45934c77a1ea21`  
		Last Modified: Tue, 12 Jan 2021 02:11:05 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d51563f7b4ffd3ce59f748a3fefc37869c72d3eae53ce2c5835e5e229c9656`  
		Last Modified: Tue, 12 Jan 2021 02:11:04 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb419b9afdd147ed666a830bc8a7ef013f7093247dc848d131a12b61135e7ae7`  
		Last Modified: Tue, 12 Jan 2021 02:11:11 GMT  
		Size: 44.9 MB (44856747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4e4a029e01f6e635c0fe2ec44d3d25b23649453b5c79514042e6173655011f`  
		Last Modified: Tue, 12 Jan 2021 02:11:03 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb241969a20df2845dcd6b5189d901e33a20f2d81715bbbf6528d2150f6c6eab`  
		Last Modified: Tue, 12 Jan 2021 02:11:03 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe04d8ff39715883e5b0b7e16bafe58360da16bdf9f4e12e48ff2f64b0eb6578`  
		Last Modified: Tue, 12 Jan 2021 02:11:02 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4d12e6a014fe5b72b1021183d5a5a6b1053b592187dd107b2f57a1bd90ad8a`  
		Last Modified: Tue, 12 Jan 2021 02:11:03 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:0a24c8eef72922d639e04ea3b80ea53edba7909a1f52ffde36bcb0e0775d93e5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88514519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31145748472efdd0f90280a0b0d81a17c02a40e74fd9d2ff7ada83aefc7b28bf`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 12 Jan 2021 00:25:06 GMT
ADD file:9d7252c169da9a089a0caa2f26cea24678267c15c0e129e7320d4defe0d4637b in / 
# Tue, 12 Jan 2021 00:25:16 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:23:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 12 Jan 2021 01:23:59 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 12 Jan 2021 01:26:26 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:26:32 GMT
ENV GOSU_VERSION=1.11
# Tue, 12 Jan 2021 01:26:36 GMT
ENV TINI_VERSION=0.18.0
# Tue, 12 Jan 2021 01:27:12 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 12 Jan 2021 01:27:18 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 12 Jan 2021 01:27:32 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 12 Jan 2021 01:27:37 GMT
ENV COUCHDB_VERSION=3.1.1
# Tue, 12 Jan 2021 01:27:45 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 12 Jan 2021 01:29:34 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 12 Jan 2021 01:29:41 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 12 Jan 2021 01:29:45 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 12 Jan 2021 01:29:49 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 12 Jan 2021 01:30:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 12 Jan 2021 01:30:06 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 12 Jan 2021 01:30:11 GMT
VOLUME [/opt/couchdb/data]
# Tue, 12 Jan 2021 01:30:16 GMT
EXPOSE 4369 5984 9100
# Tue, 12 Jan 2021 01:30:19 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:cb701c1e59a3b25dcb09b089f31d61af3065659cd29a7c748f66f3e3c8a96d58`  
		Last Modified: Tue, 12 Jan 2021 00:34:11 GMT  
		Size: 30.5 MB (30532837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e70c701092def27535a2729a97ff54374694fb51d7b7a9178aa38719bcffcd1`  
		Last Modified: Tue, 12 Jan 2021 01:34:04 GMT  
		Size: 3.4 KB (3416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23a2d04a2cb1bf3e22af2f16579b13d8106e0343619a3250c0b79862ed60d92`  
		Last Modified: Tue, 12 Jan 2021 01:34:03 GMT  
		Size: 7.6 MB (7580646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1458c44d75dcadeb6308623a87b08d356bc5a584a1159ba562a34e6e9d4daa7f`  
		Last Modified: Tue, 12 Jan 2021 01:34:02 GMT  
		Size: 1.1 MB (1116280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03caed2b60160fa146791aa072bafcb43ab6f05d6bee03ccf248c727dcf7683`  
		Last Modified: Tue, 12 Jan 2021 01:33:59 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6ea873bcdc65542ad245b368c03dbcce37bc534759891dd050ba01cff75eb3`  
		Last Modified: Tue, 12 Jan 2021 01:33:59 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ee6ab5a64da42e0610a35550e605c9531358aa3173d2466cde8ec630e1e30b`  
		Last Modified: Tue, 12 Jan 2021 01:34:02 GMT  
		Size: 49.3 MB (49275292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14abc94d5ac1d6e515e44e2b70263a044da083a95536993d625511a144667da8`  
		Last Modified: Tue, 12 Jan 2021 01:33:53 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0102e2f339dd82e84045a1dfc50b7a13da8b93dd76a981d9d3147b02b86b4f83`  
		Last Modified: Tue, 12 Jan 2021 01:33:53 GMT  
		Size: 768.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3029afbd5b0172ae32e2189caee20d9b4ffbf6503e0971ffdbfb91390bbeac46`  
		Last Modified: Tue, 12 Jan 2021 01:33:53 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2524650ab85d0adda44b218c1f4117452025f17eb1c9cb6690ae49c9a6949f78`  
		Last Modified: Tue, 12 Jan 2021 01:33:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
