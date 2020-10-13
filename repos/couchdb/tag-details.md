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
$ docker pull couchdb@sha256:31f48869cf78f9d3ac2861340d4507cae251834db5525746af9bea146e04d798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2` - linux; amd64

```console
$ docker pull couchdb@sha256:4fc44c2f33a177fb988059730bb4aad754bbac6bbdc2361ea57bf57383a80d69
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82410425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b59b8463d45dbd15ed46c0fe8e245f628ca741ede9c29ea073eea21aabd9ec6`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 13 Oct 2020 01:44:45 GMT
ADD file:4453535d387fcb17ead2026c72c05444e7558aa4736e3c0cdfb87cf20eaa5a9f in / 
# Tue, 13 Oct 2020 01:44:45 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:34:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Oct 2020 02:34:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 13 Oct 2020 02:34:40 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:34:40 GMT
ENV GOSU_VERSION=1.11
# Tue, 13 Oct 2020 02:34:40 GMT
ENV TINI_VERSION=0.18.0
# Tue, 13 Oct 2020 02:34:50 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 13 Oct 2020 02:34:50 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 13 Oct 2020 02:34:53 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 13 Oct 2020 02:34:53 GMT
ENV COUCHDB_VERSION=2.3.1
# Tue, 13 Oct 2020 02:34:54 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb stretch main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 13 Oct 2020 02:35:19 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~stretch     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 13 Oct 2020 02:35:19 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 13 Oct 2020 02:35:19 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 13 Oct 2020 02:35:20 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 13 Oct 2020 02:35:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 13 Oct 2020 02:35:21 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Oct 2020 02:35:21 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Oct 2020 02:35:21 GMT
EXPOSE 4369 5984 9100
# Tue, 13 Oct 2020 02:35:21 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:babf97a3f00ae0a4d59c1a0f88918d8f7aa0f0758380258b2016f0cd17e97202`  
		Last Modified: Tue, 13 Oct 2020 01:51:03 GMT  
		Size: 22.5 MB (22522093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4da98eb800bbaf3551a5be094e07f693bba2c13499f1df31f19cb24519c62ba`  
		Last Modified: Tue, 13 Oct 2020 02:36:04 GMT  
		Size: 3.4 KB (3415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff2f7f97765254f62e75e335252360b74c10705f5e4be3c6d8678ae61c99a26`  
		Last Modified: Tue, 13 Oct 2020 02:36:05 GMT  
		Size: 8.5 MB (8471828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db2c9e34fb744697ea9814eed40e0e5a79ea3ed039750b3d78092688733137c`  
		Last Modified: Tue, 13 Oct 2020 02:36:04 GMT  
		Size: 1.2 MB (1190336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e839075c9f3685fad8aa3fe59ca84c5a4b72bd7262a2d94117d83a8eda05c242`  
		Last Modified: Tue, 13 Oct 2020 02:36:03 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838be41e99694924854449a6e9191c4f99cfe6159511effe418e61df0c7a0ad2`  
		Last Modified: Tue, 13 Oct 2020 02:36:03 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee020c4402ec6a7fc48bf26dc0c804681ce276fe0beab9bcf681625132131c3`  
		Last Modified: Tue, 13 Oct 2020 02:36:10 GMT  
		Size: 50.2 MB (50216693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5895bb1094d40dc1848bd1a7ad3b5f53c47cce46237355116898cb0cd7a9a8`  
		Last Modified: Tue, 13 Oct 2020 02:36:02 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a807854235c2ff4937b4e864b8e15f90038d2268c5d9731c6a887abfbb543052`  
		Last Modified: Tue, 13 Oct 2020 02:36:02 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91fa1461124cd294bfa69fce28a551f7a434c37b3ab7f4fb3a4089a8c8001841`  
		Last Modified: Tue, 13 Oct 2020 02:36:02 GMT  
		Size: 2.1 KB (2070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c06e5aa3981046589f685c746f025359bd5bd7f0875b0e3d8fd4d0735f137b09`  
		Last Modified: Tue, 13 Oct 2020 02:36:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:ce3c7ef01bc7a56b1ca188b48f88fcb33da07de795cf969e5124a490d41051af
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76927082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:112d81a8a80775eb806fe36c28410cb34259e5485a63c96766be1e8c40d17c7f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 13 Oct 2020 01:44:21 GMT
ADD file:1783101ec41dba711940487fb45a9287f74a0639658051ad8bc9b2618a15be61 in / 
# Tue, 13 Oct 2020 01:44:22 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:59:36 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Oct 2020 02:59:40 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 13 Oct 2020 03:00:02 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 03:00:03 GMT
ENV GOSU_VERSION=1.11
# Tue, 13 Oct 2020 03:00:04 GMT
ENV TINI_VERSION=0.18.0
# Tue, 13 Oct 2020 03:01:41 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 13 Oct 2020 03:01:42 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 13 Oct 2020 03:04:40 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 13 Oct 2020 03:04:41 GMT
ENV COUCHDB_VERSION=2.3.1
# Tue, 13 Oct 2020 03:04:43 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb stretch main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 13 Oct 2020 03:05:19 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~stretch     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 13 Oct 2020 03:05:22 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 13 Oct 2020 03:05:23 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 13 Oct 2020 03:05:24 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 13 Oct 2020 03:05:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 13 Oct 2020 03:05:29 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Oct 2020 03:05:30 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Oct 2020 03:05:31 GMT
EXPOSE 4369 5984 9100
# Tue, 13 Oct 2020 03:05:31 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f4bec48cdb322f1180477bdd362bcd92d70a1ab628fc36319017bf4e8058d9ee`  
		Last Modified: Tue, 13 Oct 2020 01:51:12 GMT  
		Size: 20.4 MB (20376997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0085bc8b8adcf89b5afbe5c6c1a8f259e11ae5981c9a0a4d91d0c4e54cacb7f`  
		Last Modified: Tue, 13 Oct 2020 03:06:35 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4443ecd7f82b0f49797b6745c499e44a4d53e1fcb0a4244229a1cef45194a7`  
		Last Modified: Tue, 13 Oct 2020 03:06:35 GMT  
		Size: 7.6 MB (7611099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31263b3512664d95c07ab93882f9df4576c521a5759b3bda37f628d06eca0204`  
		Last Modified: Tue, 13 Oct 2020 03:06:34 GMT  
		Size: 1.1 MB (1124990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec875578070923e5d0820e9e7e1d6366157cbe9465668dedb57f8bef8ed99b0`  
		Last Modified: Tue, 13 Oct 2020 03:06:33 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a706601ef10a87d2d2ce149e5809d1a8fab1c0d72006f5483e3fd620dd5e3f53`  
		Last Modified: Tue, 13 Oct 2020 03:06:33 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e66015a91a0f6d7adadc7f4632517c96689279afa907be528ec3e30672d3b119`  
		Last Modified: Tue, 13 Oct 2020 03:06:44 GMT  
		Size: 47.8 MB (47804496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90980f0c19a8050ee2d478c878bf091bb34c997d18d85d79f189869d31289f1`  
		Last Modified: Tue, 13 Oct 2020 03:06:31 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b0818db5973908f4f9512d235bda086f1b0d9b32f0b58c01c7d364ecd7371c`  
		Last Modified: Tue, 13 Oct 2020 03:06:31 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6487997194f7e45feb87a8566b9be6fdb16b665515ca1eef93e19b6bf8f2d3`  
		Last Modified: Tue, 13 Oct 2020 03:06:31 GMT  
		Size: 2.1 KB (2070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b0b8a403fcc6231809970dd45b1b1359388046935c69222febd6b49b67ff47`  
		Last Modified: Tue, 13 Oct 2020 03:06:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3`

```console
$ docker pull couchdb@sha256:31f48869cf78f9d3ac2861340d4507cae251834db5525746af9bea146e04d798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:4fc44c2f33a177fb988059730bb4aad754bbac6bbdc2361ea57bf57383a80d69
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82410425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b59b8463d45dbd15ed46c0fe8e245f628ca741ede9c29ea073eea21aabd9ec6`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 13 Oct 2020 01:44:45 GMT
ADD file:4453535d387fcb17ead2026c72c05444e7558aa4736e3c0cdfb87cf20eaa5a9f in / 
# Tue, 13 Oct 2020 01:44:45 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:34:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Oct 2020 02:34:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 13 Oct 2020 02:34:40 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:34:40 GMT
ENV GOSU_VERSION=1.11
# Tue, 13 Oct 2020 02:34:40 GMT
ENV TINI_VERSION=0.18.0
# Tue, 13 Oct 2020 02:34:50 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 13 Oct 2020 02:34:50 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 13 Oct 2020 02:34:53 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 13 Oct 2020 02:34:53 GMT
ENV COUCHDB_VERSION=2.3.1
# Tue, 13 Oct 2020 02:34:54 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb stretch main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 13 Oct 2020 02:35:19 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~stretch     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 13 Oct 2020 02:35:19 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 13 Oct 2020 02:35:19 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 13 Oct 2020 02:35:20 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 13 Oct 2020 02:35:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 13 Oct 2020 02:35:21 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Oct 2020 02:35:21 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Oct 2020 02:35:21 GMT
EXPOSE 4369 5984 9100
# Tue, 13 Oct 2020 02:35:21 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:babf97a3f00ae0a4d59c1a0f88918d8f7aa0f0758380258b2016f0cd17e97202`  
		Last Modified: Tue, 13 Oct 2020 01:51:03 GMT  
		Size: 22.5 MB (22522093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4da98eb800bbaf3551a5be094e07f693bba2c13499f1df31f19cb24519c62ba`  
		Last Modified: Tue, 13 Oct 2020 02:36:04 GMT  
		Size: 3.4 KB (3415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff2f7f97765254f62e75e335252360b74c10705f5e4be3c6d8678ae61c99a26`  
		Last Modified: Tue, 13 Oct 2020 02:36:05 GMT  
		Size: 8.5 MB (8471828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db2c9e34fb744697ea9814eed40e0e5a79ea3ed039750b3d78092688733137c`  
		Last Modified: Tue, 13 Oct 2020 02:36:04 GMT  
		Size: 1.2 MB (1190336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e839075c9f3685fad8aa3fe59ca84c5a4b72bd7262a2d94117d83a8eda05c242`  
		Last Modified: Tue, 13 Oct 2020 02:36:03 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838be41e99694924854449a6e9191c4f99cfe6159511effe418e61df0c7a0ad2`  
		Last Modified: Tue, 13 Oct 2020 02:36:03 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee020c4402ec6a7fc48bf26dc0c804681ce276fe0beab9bcf681625132131c3`  
		Last Modified: Tue, 13 Oct 2020 02:36:10 GMT  
		Size: 50.2 MB (50216693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5895bb1094d40dc1848bd1a7ad3b5f53c47cce46237355116898cb0cd7a9a8`  
		Last Modified: Tue, 13 Oct 2020 02:36:02 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a807854235c2ff4937b4e864b8e15f90038d2268c5d9731c6a887abfbb543052`  
		Last Modified: Tue, 13 Oct 2020 02:36:02 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91fa1461124cd294bfa69fce28a551f7a434c37b3ab7f4fb3a4089a8c8001841`  
		Last Modified: Tue, 13 Oct 2020 02:36:02 GMT  
		Size: 2.1 KB (2070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c06e5aa3981046589f685c746f025359bd5bd7f0875b0e3d8fd4d0735f137b09`  
		Last Modified: Tue, 13 Oct 2020 02:36:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:ce3c7ef01bc7a56b1ca188b48f88fcb33da07de795cf969e5124a490d41051af
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76927082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:112d81a8a80775eb806fe36c28410cb34259e5485a63c96766be1e8c40d17c7f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 13 Oct 2020 01:44:21 GMT
ADD file:1783101ec41dba711940487fb45a9287f74a0639658051ad8bc9b2618a15be61 in / 
# Tue, 13 Oct 2020 01:44:22 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:59:36 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Oct 2020 02:59:40 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 13 Oct 2020 03:00:02 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 03:00:03 GMT
ENV GOSU_VERSION=1.11
# Tue, 13 Oct 2020 03:00:04 GMT
ENV TINI_VERSION=0.18.0
# Tue, 13 Oct 2020 03:01:41 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 13 Oct 2020 03:01:42 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 13 Oct 2020 03:04:40 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 13 Oct 2020 03:04:41 GMT
ENV COUCHDB_VERSION=2.3.1
# Tue, 13 Oct 2020 03:04:43 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb stretch main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 13 Oct 2020 03:05:19 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~stretch     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 13 Oct 2020 03:05:22 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 13 Oct 2020 03:05:23 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 13 Oct 2020 03:05:24 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 13 Oct 2020 03:05:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 13 Oct 2020 03:05:29 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Oct 2020 03:05:30 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Oct 2020 03:05:31 GMT
EXPOSE 4369 5984 9100
# Tue, 13 Oct 2020 03:05:31 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f4bec48cdb322f1180477bdd362bcd92d70a1ab628fc36319017bf4e8058d9ee`  
		Last Modified: Tue, 13 Oct 2020 01:51:12 GMT  
		Size: 20.4 MB (20376997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0085bc8b8adcf89b5afbe5c6c1a8f259e11ae5981c9a0a4d91d0c4e54cacb7f`  
		Last Modified: Tue, 13 Oct 2020 03:06:35 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4443ecd7f82b0f49797b6745c499e44a4d53e1fcb0a4244229a1cef45194a7`  
		Last Modified: Tue, 13 Oct 2020 03:06:35 GMT  
		Size: 7.6 MB (7611099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31263b3512664d95c07ab93882f9df4576c521a5759b3bda37f628d06eca0204`  
		Last Modified: Tue, 13 Oct 2020 03:06:34 GMT  
		Size: 1.1 MB (1124990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec875578070923e5d0820e9e7e1d6366157cbe9465668dedb57f8bef8ed99b0`  
		Last Modified: Tue, 13 Oct 2020 03:06:33 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a706601ef10a87d2d2ce149e5809d1a8fab1c0d72006f5483e3fd620dd5e3f53`  
		Last Modified: Tue, 13 Oct 2020 03:06:33 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e66015a91a0f6d7adadc7f4632517c96689279afa907be528ec3e30672d3b119`  
		Last Modified: Tue, 13 Oct 2020 03:06:44 GMT  
		Size: 47.8 MB (47804496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90980f0c19a8050ee2d478c878bf091bb34c997d18d85d79f189869d31289f1`  
		Last Modified: Tue, 13 Oct 2020 03:06:31 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b0818db5973908f4f9512d235bda086f1b0d9b32f0b58c01c7d364ecd7371c`  
		Last Modified: Tue, 13 Oct 2020 03:06:31 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6487997194f7e45feb87a8566b9be6fdb16b665515ca1eef93e19b6bf8f2d3`  
		Last Modified: Tue, 13 Oct 2020 03:06:31 GMT  
		Size: 2.1 KB (2070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b0b8a403fcc6231809970dd45b1b1359388046935c69222febd6b49b67ff47`  
		Last Modified: Tue, 13 Oct 2020 03:06:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3.1`

```console
$ docker pull couchdb@sha256:31f48869cf78f9d3ac2861340d4507cae251834db5525746af9bea146e04d798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:4fc44c2f33a177fb988059730bb4aad754bbac6bbdc2361ea57bf57383a80d69
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82410425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b59b8463d45dbd15ed46c0fe8e245f628ca741ede9c29ea073eea21aabd9ec6`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 13 Oct 2020 01:44:45 GMT
ADD file:4453535d387fcb17ead2026c72c05444e7558aa4736e3c0cdfb87cf20eaa5a9f in / 
# Tue, 13 Oct 2020 01:44:45 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:34:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Oct 2020 02:34:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 13 Oct 2020 02:34:40 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:34:40 GMT
ENV GOSU_VERSION=1.11
# Tue, 13 Oct 2020 02:34:40 GMT
ENV TINI_VERSION=0.18.0
# Tue, 13 Oct 2020 02:34:50 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 13 Oct 2020 02:34:50 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 13 Oct 2020 02:34:53 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 13 Oct 2020 02:34:53 GMT
ENV COUCHDB_VERSION=2.3.1
# Tue, 13 Oct 2020 02:34:54 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb stretch main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 13 Oct 2020 02:35:19 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~stretch     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 13 Oct 2020 02:35:19 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 13 Oct 2020 02:35:19 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 13 Oct 2020 02:35:20 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 13 Oct 2020 02:35:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 13 Oct 2020 02:35:21 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Oct 2020 02:35:21 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Oct 2020 02:35:21 GMT
EXPOSE 4369 5984 9100
# Tue, 13 Oct 2020 02:35:21 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:babf97a3f00ae0a4d59c1a0f88918d8f7aa0f0758380258b2016f0cd17e97202`  
		Last Modified: Tue, 13 Oct 2020 01:51:03 GMT  
		Size: 22.5 MB (22522093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4da98eb800bbaf3551a5be094e07f693bba2c13499f1df31f19cb24519c62ba`  
		Last Modified: Tue, 13 Oct 2020 02:36:04 GMT  
		Size: 3.4 KB (3415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff2f7f97765254f62e75e335252360b74c10705f5e4be3c6d8678ae61c99a26`  
		Last Modified: Tue, 13 Oct 2020 02:36:05 GMT  
		Size: 8.5 MB (8471828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db2c9e34fb744697ea9814eed40e0e5a79ea3ed039750b3d78092688733137c`  
		Last Modified: Tue, 13 Oct 2020 02:36:04 GMT  
		Size: 1.2 MB (1190336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e839075c9f3685fad8aa3fe59ca84c5a4b72bd7262a2d94117d83a8eda05c242`  
		Last Modified: Tue, 13 Oct 2020 02:36:03 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838be41e99694924854449a6e9191c4f99cfe6159511effe418e61df0c7a0ad2`  
		Last Modified: Tue, 13 Oct 2020 02:36:03 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee020c4402ec6a7fc48bf26dc0c804681ce276fe0beab9bcf681625132131c3`  
		Last Modified: Tue, 13 Oct 2020 02:36:10 GMT  
		Size: 50.2 MB (50216693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5895bb1094d40dc1848bd1a7ad3b5f53c47cce46237355116898cb0cd7a9a8`  
		Last Modified: Tue, 13 Oct 2020 02:36:02 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a807854235c2ff4937b4e864b8e15f90038d2268c5d9731c6a887abfbb543052`  
		Last Modified: Tue, 13 Oct 2020 02:36:02 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91fa1461124cd294bfa69fce28a551f7a434c37b3ab7f4fb3a4089a8c8001841`  
		Last Modified: Tue, 13 Oct 2020 02:36:02 GMT  
		Size: 2.1 KB (2070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c06e5aa3981046589f685c746f025359bd5bd7f0875b0e3d8fd4d0735f137b09`  
		Last Modified: Tue, 13 Oct 2020 02:36:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:ce3c7ef01bc7a56b1ca188b48f88fcb33da07de795cf969e5124a490d41051af
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76927082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:112d81a8a80775eb806fe36c28410cb34259e5485a63c96766be1e8c40d17c7f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 13 Oct 2020 01:44:21 GMT
ADD file:1783101ec41dba711940487fb45a9287f74a0639658051ad8bc9b2618a15be61 in / 
# Tue, 13 Oct 2020 01:44:22 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:59:36 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Oct 2020 02:59:40 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 13 Oct 2020 03:00:02 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 03:00:03 GMT
ENV GOSU_VERSION=1.11
# Tue, 13 Oct 2020 03:00:04 GMT
ENV TINI_VERSION=0.18.0
# Tue, 13 Oct 2020 03:01:41 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 13 Oct 2020 03:01:42 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 13 Oct 2020 03:04:40 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 13 Oct 2020 03:04:41 GMT
ENV COUCHDB_VERSION=2.3.1
# Tue, 13 Oct 2020 03:04:43 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb stretch main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 13 Oct 2020 03:05:19 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~stretch     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 13 Oct 2020 03:05:22 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 13 Oct 2020 03:05:23 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 13 Oct 2020 03:05:24 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 13 Oct 2020 03:05:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 13 Oct 2020 03:05:29 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Oct 2020 03:05:30 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Oct 2020 03:05:31 GMT
EXPOSE 4369 5984 9100
# Tue, 13 Oct 2020 03:05:31 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f4bec48cdb322f1180477bdd362bcd92d70a1ab628fc36319017bf4e8058d9ee`  
		Last Modified: Tue, 13 Oct 2020 01:51:12 GMT  
		Size: 20.4 MB (20376997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0085bc8b8adcf89b5afbe5c6c1a8f259e11ae5981c9a0a4d91d0c4e54cacb7f`  
		Last Modified: Tue, 13 Oct 2020 03:06:35 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4443ecd7f82b0f49797b6745c499e44a4d53e1fcb0a4244229a1cef45194a7`  
		Last Modified: Tue, 13 Oct 2020 03:06:35 GMT  
		Size: 7.6 MB (7611099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31263b3512664d95c07ab93882f9df4576c521a5759b3bda37f628d06eca0204`  
		Last Modified: Tue, 13 Oct 2020 03:06:34 GMT  
		Size: 1.1 MB (1124990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec875578070923e5d0820e9e7e1d6366157cbe9465668dedb57f8bef8ed99b0`  
		Last Modified: Tue, 13 Oct 2020 03:06:33 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a706601ef10a87d2d2ce149e5809d1a8fab1c0d72006f5483e3fd620dd5e3f53`  
		Last Modified: Tue, 13 Oct 2020 03:06:33 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e66015a91a0f6d7adadc7f4632517c96689279afa907be528ec3e30672d3b119`  
		Last Modified: Tue, 13 Oct 2020 03:06:44 GMT  
		Size: 47.8 MB (47804496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90980f0c19a8050ee2d478c878bf091bb34c997d18d85d79f189869d31289f1`  
		Last Modified: Tue, 13 Oct 2020 03:06:31 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b0818db5973908f4f9512d235bda086f1b0d9b32f0b58c01c7d364ecd7371c`  
		Last Modified: Tue, 13 Oct 2020 03:06:31 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6487997194f7e45feb87a8566b9be6fdb16b665515ca1eef93e19b6bf8f2d3`  
		Last Modified: Tue, 13 Oct 2020 03:06:31 GMT  
		Size: 2.1 KB (2070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b0b8a403fcc6231809970dd45b1b1359388046935c69222febd6b49b67ff47`  
		Last Modified: Tue, 13 Oct 2020 03:06:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3`

```console
$ docker pull couchdb@sha256:b5e6939af792a0e40218e405e8656d68c14a03220899f470b58611a00dc65a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3` - linux; amd64

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

### `couchdb:3` - linux; arm64 variant v8

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

### `couchdb:3` - linux; ppc64le

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

## `couchdb:3.0`

```console
$ docker pull couchdb@sha256:8d494c58d2313cb4f0b7c0a7b6768dc2fee355fae950319d7d89be3e4d2228d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.0` - linux; amd64

```console
$ docker pull couchdb@sha256:390fb4b691fee489412fa5b0894fe26b0e1c35c8a4278c460bd620945a0267a2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83193491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be1777b37825d1b5b08b01f083d8388a5e5594084cfd5ec4487a794b94053b2`
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
# Tue, 13 Oct 2020 02:33:59 GMT
ENV COUCHDB_VERSION=3.0.1
# Tue, 13 Oct 2020 02:34:00 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 13 Oct 2020 02:34:18 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 13 Oct 2020 02:34:18 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 13 Oct 2020 02:34:19 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 13 Oct 2020 02:34:19 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 13 Oct 2020 02:34:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 13 Oct 2020 02:34:20 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Oct 2020 02:34:20 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Oct 2020 02:34:20 GMT
EXPOSE 4369 5984 9100
# Tue, 13 Oct 2020 02:34:21 GMT
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
	-	`sha256:55221f30611f3852808448b23731db7da4b7a8b151725fda023167072fa77677`  
		Last Modified: Tue, 13 Oct 2020 02:35:53 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3489f5874ed45c5db561c4d41479cf9ba91c49de39963901ef7f9e6d71607e`  
		Last Modified: Tue, 13 Oct 2020 02:35:58 GMT  
		Size: 48.2 MB (48229779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7179aa14542a5be377b6b5b7cbf08a76af68bd21336d2e997938b9e51f63fc`  
		Last Modified: Tue, 13 Oct 2020 02:35:51 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b163fdf128440409b26d9385fb512d3e964ae929b014a405a960c75ae90a47`  
		Last Modified: Tue, 13 Oct 2020 02:35:51 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4016283c33c2ba10acb5a24f1616fd8fb65778add53039d69f44ec6fb820c60d`  
		Last Modified: Tue, 13 Oct 2020 02:35:51 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe8447c4fe50bb7e9d58ee77755491693e99b675bd2da9bb6f6d98e753ccc75`  
		Last Modified: Tue, 13 Oct 2020 02:35:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.0` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:122c66ef6413444620e0c2c30ed8b61b36f9409e5256343753458f28d5c3f70e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.2 MB (78228253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0323cfcd021d6d090f1efd2d3f6c1fc71990ad154ffcd08b0ea42b72973e0fb9`
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
# Tue, 13 Oct 2020 02:58:54 GMT
ENV COUCHDB_VERSION=3.0.1
# Tue, 13 Oct 2020 02:58:57 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 13 Oct 2020 02:59:22 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 13 Oct 2020 02:59:23 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 13 Oct 2020 02:59:24 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 13 Oct 2020 02:59:25 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 13 Oct 2020 02:59:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 13 Oct 2020 02:59:28 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Oct 2020 02:59:28 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Oct 2020 02:59:29 GMT
EXPOSE 4369 5984 9100
# Tue, 13 Oct 2020 02:59:30 GMT
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
	-	`sha256:8cfc5b4a26342ad2590b20ea00ec411aa79c52553b2b9d840a3de706a010487e`  
		Last Modified: Tue, 13 Oct 2020 03:06:15 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9798abd048446687ef20524b58d9cebf5b4f61f4bd84a1163923f9f79bce5d92`  
		Last Modified: Tue, 13 Oct 2020 03:06:23 GMT  
		Size: 44.7 MB (44709038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e3cb7f49f5822ae75a2adab1207da35104b203911e5fbef070ecab1b5e299e`  
		Last Modified: Tue, 13 Oct 2020 03:06:13 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed83cc85c268cfbc7115512641f4e42ea2f74e84b060a935e7a51c45534b730c`  
		Last Modified: Tue, 13 Oct 2020 03:06:13 GMT  
		Size: 768.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f9630be8745cc07e134c989eb9478aa24fae18c37d80af169afadc6c45ce12`  
		Last Modified: Tue, 13 Oct 2020 03:06:13 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ec0f4d734a153e60e894630ac59e8e67bb4e9b954e3f02d710f089e62095d6`  
		Last Modified: Tue, 13 Oct 2020 03:06:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.0` - linux; ppc64le

```console
$ docker pull couchdb@sha256:9890c245ce30d9aec2a1df3c7c6911ca9f4fcf9566611e837985ac44fcddd3ba
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88348861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9408322da9c69518beecfb141b050ce19699117dd8fd80c2103be33e5430b62d`
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
# Tue, 13 Oct 2020 09:58:20 GMT
ENV COUCHDB_VERSION=3.0.1
# Tue, 13 Oct 2020 09:58:26 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 13 Oct 2020 09:59:33 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 13 Oct 2020 09:59:37 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 13 Oct 2020 09:59:38 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 13 Oct 2020 09:59:41 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 13 Oct 2020 09:59:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 13 Oct 2020 09:59:51 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Oct 2020 09:59:53 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Oct 2020 09:59:56 GMT
EXPOSE 4369 5984 9100
# Tue, 13 Oct 2020 09:59:58 GMT
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
	-	`sha256:8681f34598751ea4c4871e4229c80650bad2254239653ebbc821b43e6b56e0e8`  
		Last Modified: Tue, 13 Oct 2020 10:00:55 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57416623dc62b310158262d87445cabf2ff866df21248334b97a520af95e5c02`  
		Last Modified: Tue, 13 Oct 2020 10:01:01 GMT  
		Size: 49.1 MB (49125184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4366206d9b3fdc12c2285aec724f36b1f9df49db148625dfbf7278bede36d8a`  
		Last Modified: Tue, 13 Oct 2020 10:00:52 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2929c533eda8a765c36619ce7a0fa69b8bd934f2192728988423d2ce7f466bc1`  
		Last Modified: Tue, 13 Oct 2020 10:00:52 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955e6b65247da29aa39aa10aeb6098a0b035fde9d8e47ff9a680897fd1174382`  
		Last Modified: Tue, 13 Oct 2020 10:00:51 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98690a09e87b3bed8c324541a90154a033f91ca144fde816a2c3895a95dcf1b3`  
		Last Modified: Tue, 13 Oct 2020 10:00:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.0.1`

```console
$ docker pull couchdb@sha256:8d494c58d2313cb4f0b7c0a7b6768dc2fee355fae950319d7d89be3e4d2228d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.0.1` - linux; amd64

```console
$ docker pull couchdb@sha256:390fb4b691fee489412fa5b0894fe26b0e1c35c8a4278c460bd620945a0267a2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83193491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be1777b37825d1b5b08b01f083d8388a5e5594084cfd5ec4487a794b94053b2`
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
# Tue, 13 Oct 2020 02:33:59 GMT
ENV COUCHDB_VERSION=3.0.1
# Tue, 13 Oct 2020 02:34:00 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 13 Oct 2020 02:34:18 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 13 Oct 2020 02:34:18 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 13 Oct 2020 02:34:19 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 13 Oct 2020 02:34:19 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 13 Oct 2020 02:34:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 13 Oct 2020 02:34:20 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Oct 2020 02:34:20 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Oct 2020 02:34:20 GMT
EXPOSE 4369 5984 9100
# Tue, 13 Oct 2020 02:34:21 GMT
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
	-	`sha256:55221f30611f3852808448b23731db7da4b7a8b151725fda023167072fa77677`  
		Last Modified: Tue, 13 Oct 2020 02:35:53 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3489f5874ed45c5db561c4d41479cf9ba91c49de39963901ef7f9e6d71607e`  
		Last Modified: Tue, 13 Oct 2020 02:35:58 GMT  
		Size: 48.2 MB (48229779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7179aa14542a5be377b6b5b7cbf08a76af68bd21336d2e997938b9e51f63fc`  
		Last Modified: Tue, 13 Oct 2020 02:35:51 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b163fdf128440409b26d9385fb512d3e964ae929b014a405a960c75ae90a47`  
		Last Modified: Tue, 13 Oct 2020 02:35:51 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4016283c33c2ba10acb5a24f1616fd8fb65778add53039d69f44ec6fb820c60d`  
		Last Modified: Tue, 13 Oct 2020 02:35:51 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe8447c4fe50bb7e9d58ee77755491693e99b675bd2da9bb6f6d98e753ccc75`  
		Last Modified: Tue, 13 Oct 2020 02:35:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.0.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:122c66ef6413444620e0c2c30ed8b61b36f9409e5256343753458f28d5c3f70e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.2 MB (78228253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0323cfcd021d6d090f1efd2d3f6c1fc71990ad154ffcd08b0ea42b72973e0fb9`
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
# Tue, 13 Oct 2020 02:58:54 GMT
ENV COUCHDB_VERSION=3.0.1
# Tue, 13 Oct 2020 02:58:57 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 13 Oct 2020 02:59:22 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 13 Oct 2020 02:59:23 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 13 Oct 2020 02:59:24 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 13 Oct 2020 02:59:25 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 13 Oct 2020 02:59:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 13 Oct 2020 02:59:28 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Oct 2020 02:59:28 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Oct 2020 02:59:29 GMT
EXPOSE 4369 5984 9100
# Tue, 13 Oct 2020 02:59:30 GMT
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
	-	`sha256:8cfc5b4a26342ad2590b20ea00ec411aa79c52553b2b9d840a3de706a010487e`  
		Last Modified: Tue, 13 Oct 2020 03:06:15 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9798abd048446687ef20524b58d9cebf5b4f61f4bd84a1163923f9f79bce5d92`  
		Last Modified: Tue, 13 Oct 2020 03:06:23 GMT  
		Size: 44.7 MB (44709038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e3cb7f49f5822ae75a2adab1207da35104b203911e5fbef070ecab1b5e299e`  
		Last Modified: Tue, 13 Oct 2020 03:06:13 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed83cc85c268cfbc7115512641f4e42ea2f74e84b060a935e7a51c45534b730c`  
		Last Modified: Tue, 13 Oct 2020 03:06:13 GMT  
		Size: 768.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f9630be8745cc07e134c989eb9478aa24fae18c37d80af169afadc6c45ce12`  
		Last Modified: Tue, 13 Oct 2020 03:06:13 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ec0f4d734a153e60e894630ac59e8e67bb4e9b954e3f02d710f089e62095d6`  
		Last Modified: Tue, 13 Oct 2020 03:06:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.0.1` - linux; ppc64le

```console
$ docker pull couchdb@sha256:9890c245ce30d9aec2a1df3c7c6911ca9f4fcf9566611e837985ac44fcddd3ba
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88348861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9408322da9c69518beecfb141b050ce19699117dd8fd80c2103be33e5430b62d`
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
# Tue, 13 Oct 2020 09:58:20 GMT
ENV COUCHDB_VERSION=3.0.1
# Tue, 13 Oct 2020 09:58:26 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 13 Oct 2020 09:59:33 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 13 Oct 2020 09:59:37 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 13 Oct 2020 09:59:38 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 13 Oct 2020 09:59:41 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 13 Oct 2020 09:59:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 13 Oct 2020 09:59:51 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Oct 2020 09:59:53 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Oct 2020 09:59:56 GMT
EXPOSE 4369 5984 9100
# Tue, 13 Oct 2020 09:59:58 GMT
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
	-	`sha256:8681f34598751ea4c4871e4229c80650bad2254239653ebbc821b43e6b56e0e8`  
		Last Modified: Tue, 13 Oct 2020 10:00:55 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57416623dc62b310158262d87445cabf2ff866df21248334b97a520af95e5c02`  
		Last Modified: Tue, 13 Oct 2020 10:01:01 GMT  
		Size: 49.1 MB (49125184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4366206d9b3fdc12c2285aec724f36b1f9df49db148625dfbf7278bede36d8a`  
		Last Modified: Tue, 13 Oct 2020 10:00:52 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2929c533eda8a765c36619ce7a0fa69b8bd934f2192728988423d2ce7f466bc1`  
		Last Modified: Tue, 13 Oct 2020 10:00:52 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955e6b65247da29aa39aa10aeb6098a0b035fde9d8e47ff9a680897fd1174382`  
		Last Modified: Tue, 13 Oct 2020 10:00:51 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98690a09e87b3bed8c324541a90154a033f91ca144fde816a2c3895a95dcf1b3`  
		Last Modified: Tue, 13 Oct 2020 10:00:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:b5e6939af792a0e40218e405e8656d68c14a03220899f470b58611a00dc65a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.1` - linux; amd64

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

### `couchdb:3.1` - linux; arm64 variant v8

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

### `couchdb:3.1` - linux; ppc64le

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

## `couchdb:3.1.1`

```console
$ docker pull couchdb@sha256:b5e6939af792a0e40218e405e8656d68c14a03220899f470b58611a00dc65a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.1.1` - linux; amd64

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

### `couchdb:3.1.1` - linux; arm64 variant v8

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

### `couchdb:3.1.1` - linux; ppc64le

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
