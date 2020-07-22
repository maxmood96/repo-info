<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchdb`

-	[`couchdb:2`](#couchdb2)
-	[`couchdb:2.3`](#couchdb23)
-	[`couchdb:2.3.1`](#couchdb231)
-	[`couchdb:3`](#couchdb3)
-	[`couchdb:3.0`](#couchdb30)
-	[`couchdb:3.0.1`](#couchdb301)
-	[`couchdb:3.1`](#couchdb31)
-	[`couchdb:3.1.0`](#couchdb310)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:2`

```console
$ docker pull couchdb@sha256:eaa0e298441a4a4188457ebaa609828744afe4592e356e09fa70a82a750dfc6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:2` - linux; amd64

```console
$ docker pull couchdb@sha256:f12de29122e73546a74458779301493785f9dd40158df8688560926c68d791c1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82403806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e18ed84526fdb1e347645125ec06d15a7d529e2120f65908b36aa1a57c70f7be`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 22 Jul 2020 02:07:07 GMT
ADD file:c11db0b135382f4c5b0f55b50740639bd8c1a22153b931b409cb9e41136734f2 in / 
# Wed, 22 Jul 2020 02:07:07 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 14:32:58 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Jul 2020 14:32:59 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 22 Jul 2020 14:33:09 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 14:33:09 GMT
ENV GOSU_VERSION=1.11
# Wed, 22 Jul 2020 14:33:09 GMT
ENV TINI_VERSION=0.18.0
# Wed, 22 Jul 2020 14:34:25 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Wed, 22 Jul 2020 14:34:26 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Wed, 22 Jul 2020 14:34:29 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Wed, 22 Jul 2020 14:34:30 GMT
ENV COUCHDB_VERSION=2.3.1
# Wed, 22 Jul 2020 14:34:31 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb stretch main" > /etc/apt/sources.list.d/couchdb.list
# Wed, 22 Jul 2020 14:35:06 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~stretch     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 22 Jul 2020 14:35:07 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 22 Jul 2020 14:35:07 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 22 Jul 2020 14:35:08 GMT
COPY file:5b465eec9f6f6fe5ff9abac1313cd161fcf9b5299d43cfb10ee0dd1935c99af4 in /usr/local/bin 
# Wed, 22 Jul 2020 14:35:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 22 Jul 2020 14:35:10 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 22 Jul 2020 14:35:10 GMT
VOLUME [/opt/couchdb/data]
# Wed, 22 Jul 2020 14:35:10 GMT
EXPOSE 4369 5984 9100
# Wed, 22 Jul 2020 14:35:11 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:cbd31ae332794bb723708526045b062b2fe6a08ccc0f143ea7dc18e0ebe46dea`  
		Last Modified: Wed, 22 Jul 2020 02:12:25 GMT  
		Size: 22.5 MB (22515635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519b7ae7672f7b79f3f1c7156cc1026b4bfee0fec70b7d9da1e82400acda9d00`  
		Last Modified: Wed, 22 Jul 2020 14:36:06 GMT  
		Size: 3.4 KB (3416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5030a78258fb852c965b15d540c2395275a1e0959aa48adc0c4edb08ab5bd9aa`  
		Last Modified: Wed, 22 Jul 2020 14:36:06 GMT  
		Size: 8.5 MB (8471869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca480f9c16e9b1ed3ca1fd7ecff7c21b01b24304880313e3cf374c72ed89ad0c`  
		Last Modified: Wed, 22 Jul 2020 14:36:05 GMT  
		Size: 1.2 MB (1190356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183ee44f62364876945d1f5e3708982f936f024e26f7af96501308c5a7d2bc73`  
		Last Modified: Wed, 22 Jul 2020 14:36:04 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7414b36739a9a98444ef6feebbe3a25f06f6298ee273e6f8900444a2c09b7a47`  
		Last Modified: Wed, 22 Jul 2020 14:36:04 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2a5e25ae5429d357c80504a96e8160e36c6776b1c0373d34a40b4da8f869fc`  
		Last Modified: Wed, 22 Jul 2020 14:36:12 GMT  
		Size: 50.2 MB (50216481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52abab3fec1463613eb74469c120060f3ea90522c2abf8bc6c7791cc40ab8fcd`  
		Last Modified: Wed, 22 Jul 2020 14:36:03 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ad9b8074f5e758280285869b667535d1302bd38c7ea0bbbb96684bb1cfa710`  
		Last Modified: Wed, 22 Jul 2020 14:36:03 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd70dc5f4b38438b97146beb69d020c36a5ff3d5bde8cef1d5f326920cd3a8f`  
		Last Modified: Wed, 22 Jul 2020 14:36:03 GMT  
		Size: 2.1 KB (2061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7570b6802bbe9c3a3ab38fcb97bf2e6bd9d73ad8fbe12c5c3aec6217e8a38c`  
		Last Modified: Wed, 22 Jul 2020 14:36:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:7cdd789a4d2e68bf62bf0ba09ac0474645e65893857efc4982c261dd3782de7b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76920738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4e7106a31a3a7c0400652760f118b28f4dd8d2a91ce6d23c68c756ca74da069`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 22 Jul 2020 00:44:08 GMT
ADD file:7a721f0a6a7d3eb45184986201740dc57ec00c3d3da61af70966d87f3675d2ef in / 
# Wed, 22 Jul 2020 00:44:10 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 04:04:53 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Jul 2020 04:05:00 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 22 Jul 2020 04:05:21 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 04:05:22 GMT
ENV GOSU_VERSION=1.11
# Wed, 22 Jul 2020 04:05:22 GMT
ENV TINI_VERSION=0.18.0
# Wed, 22 Jul 2020 04:05:38 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Wed, 22 Jul 2020 04:05:39 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Wed, 22 Jul 2020 04:06:40 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Wed, 22 Jul 2020 04:06:41 GMT
ENV COUCHDB_VERSION=2.3.1
# Wed, 22 Jul 2020 04:06:43 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb stretch main" > /etc/apt/sources.list.d/couchdb.list
# Wed, 22 Jul 2020 04:07:25 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~stretch     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 22 Jul 2020 04:07:28 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 22 Jul 2020 04:07:29 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 22 Jul 2020 04:07:29 GMT
COPY file:5b465eec9f6f6fe5ff9abac1313cd161fcf9b5299d43cfb10ee0dd1935c99af4 in /usr/local/bin 
# Wed, 22 Jul 2020 04:07:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 22 Jul 2020 04:07:34 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 22 Jul 2020 04:07:35 GMT
VOLUME [/opt/couchdb/data]
# Wed, 22 Jul 2020 04:07:36 GMT
EXPOSE 4369 5984 9100
# Wed, 22 Jul 2020 04:07:36 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3d187d5a7d59d9a1bf03dbd41bc2d56080ed75d089110b59508e3b246ae0e944`  
		Last Modified: Wed, 22 Jul 2020 00:50:16 GMT  
		Size: 20.4 MB (20371158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89bfb93e3dbd9c27248310743a476b5a1847c4ae72b99bc91b11c5ca7187c534`  
		Last Modified: Wed, 22 Jul 2020 04:08:25 GMT  
		Size: 3.4 KB (3437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ae3491efc960fe041e959370de422479b184d5f3a3f4faacae5888f397b198`  
		Last Modified: Wed, 22 Jul 2020 04:08:26 GMT  
		Size: 7.6 MB (7610052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f13244a46fc927e7d54643b497b3363957e26da14cc57eea3f54f502df2fdb`  
		Last Modified: Wed, 22 Jul 2020 04:08:24 GMT  
		Size: 1.1 MB (1124971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8270f63a1b2f48761b1f3567f9de1a12f55a8f0db1c74c5c6616c3b82100f394`  
		Last Modified: Wed, 22 Jul 2020 04:08:24 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c3c31cc1b1df3e86611d9cf482da163a7921119d3fa3cc4d20e5db2ece0104`  
		Last Modified: Wed, 22 Jul 2020 04:08:23 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e755640adf114bc5a07c1e0d629f1b24df6abf78e185c354d3c749f086d3ae`  
		Last Modified: Wed, 22 Jul 2020 04:08:37 GMT  
		Size: 47.8 MB (47805066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffadd776d6125f2a2241ac70bcc616a9cce9faccaccb320940ddff1af6a0232`  
		Last Modified: Wed, 22 Jul 2020 04:08:22 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e7b8171862368e3aad54805cc6991f61a1e573094304b87a2c4e647cb55a82`  
		Last Modified: Wed, 22 Jul 2020 04:08:22 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1d79f11550d428bd33186485c746c2d750f784e0f1f306467fcba4593a7505`  
		Last Modified: Wed, 22 Jul 2020 04:08:22 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7620b56298b1748c1db32608cf54c98bfa6c60cbf8cbc32e186e4e820a4097a9`  
		Last Modified: Wed, 22 Jul 2020 04:08:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2` - linux; ppc64le

```console
$ docker pull couchdb@sha256:66aec46721b63c0745b6eb3287d2ad10aadff04331db73d2c584ef8ed4775108
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.2 MB (81178999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c6ae7c0d01efa3ff79aa09abf597572cd6d637e7c0d9ae80bbadd25fc9058d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 09 Jun 2020 01:25:38 GMT
ADD file:41ec53d65aa183c2835f73989c9e4922f818e59774811eaa6e7395e5a36d5eab in / 
# Tue, 09 Jun 2020 01:25:42 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:02:24 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 09 Jun 2020 04:02:34 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 09 Jun 2020 04:03:24 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 04:03:27 GMT
ENV GOSU_VERSION=1.11
# Tue, 09 Jun 2020 04:03:29 GMT
ENV TINI_VERSION=0.18.0
# Tue, 09 Jun 2020 04:03:53 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 09 Jun 2020 04:03:58 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 09 Jun 2020 04:04:06 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 09 Jun 2020 04:04:10 GMT
ENV COUCHDB_VERSION=2.3.1
# Tue, 09 Jun 2020 04:04:15 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb stretch main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 09 Jun 2020 04:05:25 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~stretch     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 09 Jun 2020 04:05:29 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 09 Jun 2020 04:05:31 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 09 Jun 2020 04:05:34 GMT
COPY file:5b465eec9f6f6fe5ff9abac1313cd161fcf9b5299d43cfb10ee0dd1935c99af4 in /usr/local/bin 
# Tue, 09 Jun 2020 04:05:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 09 Jun 2020 04:05:41 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 09 Jun 2020 04:05:44 GMT
VOLUME [/opt/couchdb/data]
# Tue, 09 Jun 2020 04:05:46 GMT
EXPOSE 4369 5984 9100
# Tue, 09 Jun 2020 04:05:51 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a29e28607c9b96acae7ff89e56214e4339a87c59e40a6f030fa4cbcaab753f2c`  
		Last Modified: Tue, 09 Jun 2020 01:37:25 GMT  
		Size: 22.8 MB (22791269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317a40c9e16a2d1a4e5d86e4a4f2ff4c6548ee2e49f17ba077ff2d68f27a7378`  
		Last Modified: Tue, 09 Jun 2020 04:07:20 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51fb9cfd76107a1fcbec162ea73450793ff5c8922e3100db66e9005785189903`  
		Last Modified: Tue, 09 Jun 2020 04:07:21 GMT  
		Size: 8.0 MB (7953654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:924c2746d12be0500da82921201d15427a8fdf21a2af1b6572616d7f506d2a74`  
		Last Modified: Tue, 09 Jun 2020 04:07:14 GMT  
		Size: 1.1 MB (1113848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa97985db1aefc3640459e4a66fe4b0c9bcaf2a35059ab4ce60b1deede0293c4`  
		Last Modified: Tue, 09 Jun 2020 04:07:14 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e24b3a5982ab515f693252c92ea2ea6586b39269def7f28f9a73de2db7717f`  
		Last Modified: Tue, 09 Jun 2020 04:07:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a29b69109fd84b5816568b8e8bba9fbe10d0a20f2964e308d0eb90e4efc8108`  
		Last Modified: Tue, 09 Jun 2020 04:07:21 GMT  
		Size: 49.3 MB (49310761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a3f763330eafee3465f88f9c2ed617a0c2b242a48b2bdb4488f1c8a0803ad9`  
		Last Modified: Tue, 09 Jun 2020 04:07:09 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f97cffbb05623f0a1ee6fe8a5f29f5b8deb286b42f56e4ed62994fa8d1f6e1`  
		Last Modified: Tue, 09 Jun 2020 04:07:09 GMT  
		Size: 770.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007017ba2cd18d32306ca5c13ba81ffd3f882b9aa0686a631319c672318836dc`  
		Last Modified: Tue, 09 Jun 2020 04:07:09 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4515fda906d6370d16eaa1ad0e688c30faca4a2bdd04c5cd2d232e408c22637e`  
		Last Modified: Tue, 09 Jun 2020 04:07:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3`

```console
$ docker pull couchdb@sha256:eaa0e298441a4a4188457ebaa609828744afe4592e356e09fa70a82a750dfc6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:f12de29122e73546a74458779301493785f9dd40158df8688560926c68d791c1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82403806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e18ed84526fdb1e347645125ec06d15a7d529e2120f65908b36aa1a57c70f7be`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 22 Jul 2020 02:07:07 GMT
ADD file:c11db0b135382f4c5b0f55b50740639bd8c1a22153b931b409cb9e41136734f2 in / 
# Wed, 22 Jul 2020 02:07:07 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 14:32:58 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Jul 2020 14:32:59 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 22 Jul 2020 14:33:09 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 14:33:09 GMT
ENV GOSU_VERSION=1.11
# Wed, 22 Jul 2020 14:33:09 GMT
ENV TINI_VERSION=0.18.0
# Wed, 22 Jul 2020 14:34:25 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Wed, 22 Jul 2020 14:34:26 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Wed, 22 Jul 2020 14:34:29 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Wed, 22 Jul 2020 14:34:30 GMT
ENV COUCHDB_VERSION=2.3.1
# Wed, 22 Jul 2020 14:34:31 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb stretch main" > /etc/apt/sources.list.d/couchdb.list
# Wed, 22 Jul 2020 14:35:06 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~stretch     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 22 Jul 2020 14:35:07 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 22 Jul 2020 14:35:07 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 22 Jul 2020 14:35:08 GMT
COPY file:5b465eec9f6f6fe5ff9abac1313cd161fcf9b5299d43cfb10ee0dd1935c99af4 in /usr/local/bin 
# Wed, 22 Jul 2020 14:35:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 22 Jul 2020 14:35:10 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 22 Jul 2020 14:35:10 GMT
VOLUME [/opt/couchdb/data]
# Wed, 22 Jul 2020 14:35:10 GMT
EXPOSE 4369 5984 9100
# Wed, 22 Jul 2020 14:35:11 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:cbd31ae332794bb723708526045b062b2fe6a08ccc0f143ea7dc18e0ebe46dea`  
		Last Modified: Wed, 22 Jul 2020 02:12:25 GMT  
		Size: 22.5 MB (22515635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519b7ae7672f7b79f3f1c7156cc1026b4bfee0fec70b7d9da1e82400acda9d00`  
		Last Modified: Wed, 22 Jul 2020 14:36:06 GMT  
		Size: 3.4 KB (3416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5030a78258fb852c965b15d540c2395275a1e0959aa48adc0c4edb08ab5bd9aa`  
		Last Modified: Wed, 22 Jul 2020 14:36:06 GMT  
		Size: 8.5 MB (8471869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca480f9c16e9b1ed3ca1fd7ecff7c21b01b24304880313e3cf374c72ed89ad0c`  
		Last Modified: Wed, 22 Jul 2020 14:36:05 GMT  
		Size: 1.2 MB (1190356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183ee44f62364876945d1f5e3708982f936f024e26f7af96501308c5a7d2bc73`  
		Last Modified: Wed, 22 Jul 2020 14:36:04 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7414b36739a9a98444ef6feebbe3a25f06f6298ee273e6f8900444a2c09b7a47`  
		Last Modified: Wed, 22 Jul 2020 14:36:04 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2a5e25ae5429d357c80504a96e8160e36c6776b1c0373d34a40b4da8f869fc`  
		Last Modified: Wed, 22 Jul 2020 14:36:12 GMT  
		Size: 50.2 MB (50216481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52abab3fec1463613eb74469c120060f3ea90522c2abf8bc6c7791cc40ab8fcd`  
		Last Modified: Wed, 22 Jul 2020 14:36:03 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ad9b8074f5e758280285869b667535d1302bd38c7ea0bbbb96684bb1cfa710`  
		Last Modified: Wed, 22 Jul 2020 14:36:03 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd70dc5f4b38438b97146beb69d020c36a5ff3d5bde8cef1d5f326920cd3a8f`  
		Last Modified: Wed, 22 Jul 2020 14:36:03 GMT  
		Size: 2.1 KB (2061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7570b6802bbe9c3a3ab38fcb97bf2e6bd9d73ad8fbe12c5c3aec6217e8a38c`  
		Last Modified: Wed, 22 Jul 2020 14:36:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:7cdd789a4d2e68bf62bf0ba09ac0474645e65893857efc4982c261dd3782de7b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76920738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4e7106a31a3a7c0400652760f118b28f4dd8d2a91ce6d23c68c756ca74da069`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 22 Jul 2020 00:44:08 GMT
ADD file:7a721f0a6a7d3eb45184986201740dc57ec00c3d3da61af70966d87f3675d2ef in / 
# Wed, 22 Jul 2020 00:44:10 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 04:04:53 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Jul 2020 04:05:00 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 22 Jul 2020 04:05:21 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 04:05:22 GMT
ENV GOSU_VERSION=1.11
# Wed, 22 Jul 2020 04:05:22 GMT
ENV TINI_VERSION=0.18.0
# Wed, 22 Jul 2020 04:05:38 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Wed, 22 Jul 2020 04:05:39 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Wed, 22 Jul 2020 04:06:40 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Wed, 22 Jul 2020 04:06:41 GMT
ENV COUCHDB_VERSION=2.3.1
# Wed, 22 Jul 2020 04:06:43 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb stretch main" > /etc/apt/sources.list.d/couchdb.list
# Wed, 22 Jul 2020 04:07:25 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~stretch     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 22 Jul 2020 04:07:28 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 22 Jul 2020 04:07:29 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 22 Jul 2020 04:07:29 GMT
COPY file:5b465eec9f6f6fe5ff9abac1313cd161fcf9b5299d43cfb10ee0dd1935c99af4 in /usr/local/bin 
# Wed, 22 Jul 2020 04:07:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 22 Jul 2020 04:07:34 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 22 Jul 2020 04:07:35 GMT
VOLUME [/opt/couchdb/data]
# Wed, 22 Jul 2020 04:07:36 GMT
EXPOSE 4369 5984 9100
# Wed, 22 Jul 2020 04:07:36 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3d187d5a7d59d9a1bf03dbd41bc2d56080ed75d089110b59508e3b246ae0e944`  
		Last Modified: Wed, 22 Jul 2020 00:50:16 GMT  
		Size: 20.4 MB (20371158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89bfb93e3dbd9c27248310743a476b5a1847c4ae72b99bc91b11c5ca7187c534`  
		Last Modified: Wed, 22 Jul 2020 04:08:25 GMT  
		Size: 3.4 KB (3437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ae3491efc960fe041e959370de422479b184d5f3a3f4faacae5888f397b198`  
		Last Modified: Wed, 22 Jul 2020 04:08:26 GMT  
		Size: 7.6 MB (7610052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f13244a46fc927e7d54643b497b3363957e26da14cc57eea3f54f502df2fdb`  
		Last Modified: Wed, 22 Jul 2020 04:08:24 GMT  
		Size: 1.1 MB (1124971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8270f63a1b2f48761b1f3567f9de1a12f55a8f0db1c74c5c6616c3b82100f394`  
		Last Modified: Wed, 22 Jul 2020 04:08:24 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c3c31cc1b1df3e86611d9cf482da163a7921119d3fa3cc4d20e5db2ece0104`  
		Last Modified: Wed, 22 Jul 2020 04:08:23 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e755640adf114bc5a07c1e0d629f1b24df6abf78e185c354d3c749f086d3ae`  
		Last Modified: Wed, 22 Jul 2020 04:08:37 GMT  
		Size: 47.8 MB (47805066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffadd776d6125f2a2241ac70bcc616a9cce9faccaccb320940ddff1af6a0232`  
		Last Modified: Wed, 22 Jul 2020 04:08:22 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e7b8171862368e3aad54805cc6991f61a1e573094304b87a2c4e647cb55a82`  
		Last Modified: Wed, 22 Jul 2020 04:08:22 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1d79f11550d428bd33186485c746c2d750f784e0f1f306467fcba4593a7505`  
		Last Modified: Wed, 22 Jul 2020 04:08:22 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7620b56298b1748c1db32608cf54c98bfa6c60cbf8cbc32e186e4e820a4097a9`  
		Last Modified: Wed, 22 Jul 2020 04:08:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:66aec46721b63c0745b6eb3287d2ad10aadff04331db73d2c584ef8ed4775108
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.2 MB (81178999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c6ae7c0d01efa3ff79aa09abf597572cd6d637e7c0d9ae80bbadd25fc9058d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 09 Jun 2020 01:25:38 GMT
ADD file:41ec53d65aa183c2835f73989c9e4922f818e59774811eaa6e7395e5a36d5eab in / 
# Tue, 09 Jun 2020 01:25:42 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:02:24 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 09 Jun 2020 04:02:34 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 09 Jun 2020 04:03:24 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 04:03:27 GMT
ENV GOSU_VERSION=1.11
# Tue, 09 Jun 2020 04:03:29 GMT
ENV TINI_VERSION=0.18.0
# Tue, 09 Jun 2020 04:03:53 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 09 Jun 2020 04:03:58 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 09 Jun 2020 04:04:06 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 09 Jun 2020 04:04:10 GMT
ENV COUCHDB_VERSION=2.3.1
# Tue, 09 Jun 2020 04:04:15 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb stretch main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 09 Jun 2020 04:05:25 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~stretch     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 09 Jun 2020 04:05:29 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 09 Jun 2020 04:05:31 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 09 Jun 2020 04:05:34 GMT
COPY file:5b465eec9f6f6fe5ff9abac1313cd161fcf9b5299d43cfb10ee0dd1935c99af4 in /usr/local/bin 
# Tue, 09 Jun 2020 04:05:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 09 Jun 2020 04:05:41 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 09 Jun 2020 04:05:44 GMT
VOLUME [/opt/couchdb/data]
# Tue, 09 Jun 2020 04:05:46 GMT
EXPOSE 4369 5984 9100
# Tue, 09 Jun 2020 04:05:51 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a29e28607c9b96acae7ff89e56214e4339a87c59e40a6f030fa4cbcaab753f2c`  
		Last Modified: Tue, 09 Jun 2020 01:37:25 GMT  
		Size: 22.8 MB (22791269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317a40c9e16a2d1a4e5d86e4a4f2ff4c6548ee2e49f17ba077ff2d68f27a7378`  
		Last Modified: Tue, 09 Jun 2020 04:07:20 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51fb9cfd76107a1fcbec162ea73450793ff5c8922e3100db66e9005785189903`  
		Last Modified: Tue, 09 Jun 2020 04:07:21 GMT  
		Size: 8.0 MB (7953654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:924c2746d12be0500da82921201d15427a8fdf21a2af1b6572616d7f506d2a74`  
		Last Modified: Tue, 09 Jun 2020 04:07:14 GMT  
		Size: 1.1 MB (1113848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa97985db1aefc3640459e4a66fe4b0c9bcaf2a35059ab4ce60b1deede0293c4`  
		Last Modified: Tue, 09 Jun 2020 04:07:14 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e24b3a5982ab515f693252c92ea2ea6586b39269def7f28f9a73de2db7717f`  
		Last Modified: Tue, 09 Jun 2020 04:07:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a29b69109fd84b5816568b8e8bba9fbe10d0a20f2964e308d0eb90e4efc8108`  
		Last Modified: Tue, 09 Jun 2020 04:07:21 GMT  
		Size: 49.3 MB (49310761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a3f763330eafee3465f88f9c2ed617a0c2b242a48b2bdb4488f1c8a0803ad9`  
		Last Modified: Tue, 09 Jun 2020 04:07:09 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f97cffbb05623f0a1ee6fe8a5f29f5b8deb286b42f56e4ed62994fa8d1f6e1`  
		Last Modified: Tue, 09 Jun 2020 04:07:09 GMT  
		Size: 770.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007017ba2cd18d32306ca5c13ba81ffd3f882b9aa0686a631319c672318836dc`  
		Last Modified: Tue, 09 Jun 2020 04:07:09 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4515fda906d6370d16eaa1ad0e688c30faca4a2bdd04c5cd2d232e408c22637e`  
		Last Modified: Tue, 09 Jun 2020 04:07:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3.1`

```console
$ docker pull couchdb@sha256:eaa0e298441a4a4188457ebaa609828744afe4592e356e09fa70a82a750dfc6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:2.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:f12de29122e73546a74458779301493785f9dd40158df8688560926c68d791c1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82403806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e18ed84526fdb1e347645125ec06d15a7d529e2120f65908b36aa1a57c70f7be`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 22 Jul 2020 02:07:07 GMT
ADD file:c11db0b135382f4c5b0f55b50740639bd8c1a22153b931b409cb9e41136734f2 in / 
# Wed, 22 Jul 2020 02:07:07 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 14:32:58 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Jul 2020 14:32:59 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 22 Jul 2020 14:33:09 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 14:33:09 GMT
ENV GOSU_VERSION=1.11
# Wed, 22 Jul 2020 14:33:09 GMT
ENV TINI_VERSION=0.18.0
# Wed, 22 Jul 2020 14:34:25 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Wed, 22 Jul 2020 14:34:26 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Wed, 22 Jul 2020 14:34:29 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Wed, 22 Jul 2020 14:34:30 GMT
ENV COUCHDB_VERSION=2.3.1
# Wed, 22 Jul 2020 14:34:31 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb stretch main" > /etc/apt/sources.list.d/couchdb.list
# Wed, 22 Jul 2020 14:35:06 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~stretch     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 22 Jul 2020 14:35:07 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 22 Jul 2020 14:35:07 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 22 Jul 2020 14:35:08 GMT
COPY file:5b465eec9f6f6fe5ff9abac1313cd161fcf9b5299d43cfb10ee0dd1935c99af4 in /usr/local/bin 
# Wed, 22 Jul 2020 14:35:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 22 Jul 2020 14:35:10 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 22 Jul 2020 14:35:10 GMT
VOLUME [/opt/couchdb/data]
# Wed, 22 Jul 2020 14:35:10 GMT
EXPOSE 4369 5984 9100
# Wed, 22 Jul 2020 14:35:11 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:cbd31ae332794bb723708526045b062b2fe6a08ccc0f143ea7dc18e0ebe46dea`  
		Last Modified: Wed, 22 Jul 2020 02:12:25 GMT  
		Size: 22.5 MB (22515635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519b7ae7672f7b79f3f1c7156cc1026b4bfee0fec70b7d9da1e82400acda9d00`  
		Last Modified: Wed, 22 Jul 2020 14:36:06 GMT  
		Size: 3.4 KB (3416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5030a78258fb852c965b15d540c2395275a1e0959aa48adc0c4edb08ab5bd9aa`  
		Last Modified: Wed, 22 Jul 2020 14:36:06 GMT  
		Size: 8.5 MB (8471869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca480f9c16e9b1ed3ca1fd7ecff7c21b01b24304880313e3cf374c72ed89ad0c`  
		Last Modified: Wed, 22 Jul 2020 14:36:05 GMT  
		Size: 1.2 MB (1190356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183ee44f62364876945d1f5e3708982f936f024e26f7af96501308c5a7d2bc73`  
		Last Modified: Wed, 22 Jul 2020 14:36:04 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7414b36739a9a98444ef6feebbe3a25f06f6298ee273e6f8900444a2c09b7a47`  
		Last Modified: Wed, 22 Jul 2020 14:36:04 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2a5e25ae5429d357c80504a96e8160e36c6776b1c0373d34a40b4da8f869fc`  
		Last Modified: Wed, 22 Jul 2020 14:36:12 GMT  
		Size: 50.2 MB (50216481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52abab3fec1463613eb74469c120060f3ea90522c2abf8bc6c7791cc40ab8fcd`  
		Last Modified: Wed, 22 Jul 2020 14:36:03 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ad9b8074f5e758280285869b667535d1302bd38c7ea0bbbb96684bb1cfa710`  
		Last Modified: Wed, 22 Jul 2020 14:36:03 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd70dc5f4b38438b97146beb69d020c36a5ff3d5bde8cef1d5f326920cd3a8f`  
		Last Modified: Wed, 22 Jul 2020 14:36:03 GMT  
		Size: 2.1 KB (2061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7570b6802bbe9c3a3ab38fcb97bf2e6bd9d73ad8fbe12c5c3aec6217e8a38c`  
		Last Modified: Wed, 22 Jul 2020 14:36:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:7cdd789a4d2e68bf62bf0ba09ac0474645e65893857efc4982c261dd3782de7b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76920738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4e7106a31a3a7c0400652760f118b28f4dd8d2a91ce6d23c68c756ca74da069`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 22 Jul 2020 00:44:08 GMT
ADD file:7a721f0a6a7d3eb45184986201740dc57ec00c3d3da61af70966d87f3675d2ef in / 
# Wed, 22 Jul 2020 00:44:10 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 04:04:53 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 22 Jul 2020 04:05:00 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 22 Jul 2020 04:05:21 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 04:05:22 GMT
ENV GOSU_VERSION=1.11
# Wed, 22 Jul 2020 04:05:22 GMT
ENV TINI_VERSION=0.18.0
# Wed, 22 Jul 2020 04:05:38 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Wed, 22 Jul 2020 04:05:39 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Wed, 22 Jul 2020 04:06:40 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Wed, 22 Jul 2020 04:06:41 GMT
ENV COUCHDB_VERSION=2.3.1
# Wed, 22 Jul 2020 04:06:43 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb stretch main" > /etc/apt/sources.list.d/couchdb.list
# Wed, 22 Jul 2020 04:07:25 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~stretch     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 22 Jul 2020 04:07:28 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 22 Jul 2020 04:07:29 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 22 Jul 2020 04:07:29 GMT
COPY file:5b465eec9f6f6fe5ff9abac1313cd161fcf9b5299d43cfb10ee0dd1935c99af4 in /usr/local/bin 
# Wed, 22 Jul 2020 04:07:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 22 Jul 2020 04:07:34 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 22 Jul 2020 04:07:35 GMT
VOLUME [/opt/couchdb/data]
# Wed, 22 Jul 2020 04:07:36 GMT
EXPOSE 4369 5984 9100
# Wed, 22 Jul 2020 04:07:36 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3d187d5a7d59d9a1bf03dbd41bc2d56080ed75d089110b59508e3b246ae0e944`  
		Last Modified: Wed, 22 Jul 2020 00:50:16 GMT  
		Size: 20.4 MB (20371158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89bfb93e3dbd9c27248310743a476b5a1847c4ae72b99bc91b11c5ca7187c534`  
		Last Modified: Wed, 22 Jul 2020 04:08:25 GMT  
		Size: 3.4 KB (3437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ae3491efc960fe041e959370de422479b184d5f3a3f4faacae5888f397b198`  
		Last Modified: Wed, 22 Jul 2020 04:08:26 GMT  
		Size: 7.6 MB (7610052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f13244a46fc927e7d54643b497b3363957e26da14cc57eea3f54f502df2fdb`  
		Last Modified: Wed, 22 Jul 2020 04:08:24 GMT  
		Size: 1.1 MB (1124971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8270f63a1b2f48761b1f3567f9de1a12f55a8f0db1c74c5c6616c3b82100f394`  
		Last Modified: Wed, 22 Jul 2020 04:08:24 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c3c31cc1b1df3e86611d9cf482da163a7921119d3fa3cc4d20e5db2ece0104`  
		Last Modified: Wed, 22 Jul 2020 04:08:23 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e755640adf114bc5a07c1e0d629f1b24df6abf78e185c354d3c749f086d3ae`  
		Last Modified: Wed, 22 Jul 2020 04:08:37 GMT  
		Size: 47.8 MB (47805066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffadd776d6125f2a2241ac70bcc616a9cce9faccaccb320940ddff1af6a0232`  
		Last Modified: Wed, 22 Jul 2020 04:08:22 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e7b8171862368e3aad54805cc6991f61a1e573094304b87a2c4e647cb55a82`  
		Last Modified: Wed, 22 Jul 2020 04:08:22 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1d79f11550d428bd33186485c746c2d750f784e0f1f306467fcba4593a7505`  
		Last Modified: Wed, 22 Jul 2020 04:08:22 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7620b56298b1748c1db32608cf54c98bfa6c60cbf8cbc32e186e4e820a4097a9`  
		Last Modified: Wed, 22 Jul 2020 04:08:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3.1` - linux; ppc64le

```console
$ docker pull couchdb@sha256:66aec46721b63c0745b6eb3287d2ad10aadff04331db73d2c584ef8ed4775108
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.2 MB (81178999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c6ae7c0d01efa3ff79aa09abf597572cd6d637e7c0d9ae80bbadd25fc9058d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 09 Jun 2020 01:25:38 GMT
ADD file:41ec53d65aa183c2835f73989c9e4922f818e59774811eaa6e7395e5a36d5eab in / 
# Tue, 09 Jun 2020 01:25:42 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:02:24 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 09 Jun 2020 04:02:34 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 09 Jun 2020 04:03:24 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 04:03:27 GMT
ENV GOSU_VERSION=1.11
# Tue, 09 Jun 2020 04:03:29 GMT
ENV TINI_VERSION=0.18.0
# Tue, 09 Jun 2020 04:03:53 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Tue, 09 Jun 2020 04:03:58 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Tue, 09 Jun 2020 04:04:06 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Tue, 09 Jun 2020 04:04:10 GMT
ENV COUCHDB_VERSION=2.3.1
# Tue, 09 Jun 2020 04:04:15 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb stretch main" > /etc/apt/sources.list.d/couchdb.list
# Tue, 09 Jun 2020 04:05:25 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~stretch     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 09 Jun 2020 04:05:29 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 09 Jun 2020 04:05:31 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 09 Jun 2020 04:05:34 GMT
COPY file:5b465eec9f6f6fe5ff9abac1313cd161fcf9b5299d43cfb10ee0dd1935c99af4 in /usr/local/bin 
# Tue, 09 Jun 2020 04:05:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 09 Jun 2020 04:05:41 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 09 Jun 2020 04:05:44 GMT
VOLUME [/opt/couchdb/data]
# Tue, 09 Jun 2020 04:05:46 GMT
EXPOSE 4369 5984 9100
# Tue, 09 Jun 2020 04:05:51 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a29e28607c9b96acae7ff89e56214e4339a87c59e40a6f030fa4cbcaab753f2c`  
		Last Modified: Tue, 09 Jun 2020 01:37:25 GMT  
		Size: 22.8 MB (22791269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317a40c9e16a2d1a4e5d86e4a4f2ff4c6548ee2e49f17ba077ff2d68f27a7378`  
		Last Modified: Tue, 09 Jun 2020 04:07:20 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51fb9cfd76107a1fcbec162ea73450793ff5c8922e3100db66e9005785189903`  
		Last Modified: Tue, 09 Jun 2020 04:07:21 GMT  
		Size: 8.0 MB (7953654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:924c2746d12be0500da82921201d15427a8fdf21a2af1b6572616d7f506d2a74`  
		Last Modified: Tue, 09 Jun 2020 04:07:14 GMT  
		Size: 1.1 MB (1113848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa97985db1aefc3640459e4a66fe4b0c9bcaf2a35059ab4ce60b1deede0293c4`  
		Last Modified: Tue, 09 Jun 2020 04:07:14 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e24b3a5982ab515f693252c92ea2ea6586b39269def7f28f9a73de2db7717f`  
		Last Modified: Tue, 09 Jun 2020 04:07:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a29b69109fd84b5816568b8e8bba9fbe10d0a20f2964e308d0eb90e4efc8108`  
		Last Modified: Tue, 09 Jun 2020 04:07:21 GMT  
		Size: 49.3 MB (49310761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a3f763330eafee3465f88f9c2ed617a0c2b242a48b2bdb4488f1c8a0803ad9`  
		Last Modified: Tue, 09 Jun 2020 04:07:09 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f97cffbb05623f0a1ee6fe8a5f29f5b8deb286b42f56e4ed62994fa8d1f6e1`  
		Last Modified: Tue, 09 Jun 2020 04:07:09 GMT  
		Size: 770.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007017ba2cd18d32306ca5c13ba81ffd3f882b9aa0686a631319c672318836dc`  
		Last Modified: Tue, 09 Jun 2020 04:07:09 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4515fda906d6370d16eaa1ad0e688c30faca4a2bdd04c5cd2d232e408c22637e`  
		Last Modified: Tue, 09 Jun 2020 04:07:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3`

```console
$ docker pull couchdb@sha256:570bcef2fc1a7ef94cd03b45fe680b8651940b34f1db870063ea98735223cd48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3` - linux; amd64

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

### `couchdb:3` - linux; arm64 variant v8

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

### `couchdb:3` - linux; ppc64le

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

## `couchdb:3.0`

```console
$ docker pull couchdb@sha256:3611dda04bc98722a46f3a01a7f879e13c19b0c8920866aa2130a84d8b39f3c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.0` - linux; amd64

```console
$ docker pull couchdb@sha256:237795a431e430fcca78ed1d60df02e135c931d734fa0ee3d7e711f33c634c85
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83199559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6cedc1775cff8209e40529bb0fad4b252a211d961fe4d89fb5b83ccfceee62f`
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
# Wed, 22 Jul 2020 14:32:33 GMT
ENV COUCHDB_VERSION=3.0.1
# Wed, 22 Jul 2020 14:32:34 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Wed, 22 Jul 2020 14:32:49 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 22 Jul 2020 14:32:50 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 22 Jul 2020 14:32:50 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 22 Jul 2020 14:32:50 GMT
COPY file:6952d2d38c707f223d813efd2d2969873cdd4b66d733559ef9be855aff5d8579 in /usr/local/bin 
# Wed, 22 Jul 2020 14:32:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 22 Jul 2020 14:32:51 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 22 Jul 2020 14:32:51 GMT
VOLUME [/opt/couchdb/data]
# Wed, 22 Jul 2020 14:32:51 GMT
EXPOSE 4369 5984 9100
# Wed, 22 Jul 2020 14:32:52 GMT
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
	-	`sha256:01a2b99c219c22bc2b58b5b3bf08b656d7d1c08b86ea6936f5e0c23212d404ff`  
		Last Modified: Wed, 22 Jul 2020 14:35:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec31835a82559118e2c9270543522ba05f329c1fc41a8f5ab43c8129853082db`  
		Last Modified: Wed, 22 Jul 2020 14:35:58 GMT  
		Size: 48.2 MB (48229512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e5c8019170ae4bfe6fc75b74b6e2c8c66ddd2bdd165ccc0d29cba6f1ebf520`  
		Last Modified: Wed, 22 Jul 2020 14:35:51 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7587d2da0135be4b07ef835d59126239bd4a8c4c1478b553140870f633f9ebc`  
		Last Modified: Wed, 22 Jul 2020 14:35:51 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713e11b00abdab3a216685d61899cdc6d59c6e6e350ad774f5de8a8a188b336e`  
		Last Modified: Wed, 22 Jul 2020 14:35:51 GMT  
		Size: 2.0 KB (2049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d823bcb0484e3ded03cea094f13e2ad3c0c98291023a19680a4878a111676d0c`  
		Last Modified: Wed, 22 Jul 2020 14:35:51 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.0` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:198c1ea7be3b19305bbc75b08a8ef18dcb0d027608ed9a62cf3b9cbaa5ea16a1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.2 MB (78236205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:713a03561c3fc8afaf28beca921edb3c34905fa99723701b8346490c2e396b65`
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
# Wed, 22 Jul 2020 04:04:03 GMT
ENV COUCHDB_VERSION=3.0.1
# Wed, 22 Jul 2020 04:04:05 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Wed, 22 Jul 2020 04:04:33 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 22 Jul 2020 04:04:35 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 22 Jul 2020 04:04:35 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 22 Jul 2020 04:04:36 GMT
COPY file:6952d2d38c707f223d813efd2d2969873cdd4b66d733559ef9be855aff5d8579 in /usr/local/bin 
# Wed, 22 Jul 2020 04:04:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 22 Jul 2020 04:04:39 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 22 Jul 2020 04:04:40 GMT
VOLUME [/opt/couchdb/data]
# Wed, 22 Jul 2020 04:04:41 GMT
EXPOSE 4369 5984 9100
# Wed, 22 Jul 2020 04:04:41 GMT
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
	-	`sha256:4df523caf83c9a09a5d3dd5a763d86d5cca588f7f6d931507a1f8f77e03aa8df`  
		Last Modified: Wed, 22 Jul 2020 04:08:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d25e564d851a585677c52323a31150a060f291dc3e1504ad0681d3a7310fd318`  
		Last Modified: Wed, 22 Jul 2020 04:08:15 GMT  
		Size: 44.7 MB (44708433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd9042ae75ba222a0b0d5d01322fb00616284fbc0bbc18f40ac8ba56b3fb890`  
		Last Modified: Wed, 22 Jul 2020 04:08:06 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2f5e4b0e1a2d48e7206f86f49cd381a681a5f8c04c515301b3523e1ef6a173c`  
		Last Modified: Wed, 22 Jul 2020 04:08:06 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3248b8b84d724ec0d65d8f39433f8de2e198a7c15c23ed56f700030ba9ee69f`  
		Last Modified: Wed, 22 Jul 2020 04:08:07 GMT  
		Size: 2.1 KB (2052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243dccbc57714060bf4c2b5a74baae876f855938aff8d8922e5a128c63011032`  
		Last Modified: Wed, 22 Jul 2020 04:08:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.0` - linux; ppc64le

```console
$ docker pull couchdb@sha256:52bc75bd6458644770743541984730dc66bdfe93bcd584bf813ccfa9ea639bbf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 MB (88355316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f059cb4caddb7bf14aa6a34b5322c745224ee37a992ba914ba1a3a23a0972b8`
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
# Wed, 22 Jul 2020 06:04:55 GMT
ENV COUCHDB_VERSION=3.0.1
# Wed, 22 Jul 2020 06:05:04 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Wed, 22 Jul 2020 06:06:21 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 22 Jul 2020 06:06:31 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 22 Jul 2020 06:06:32 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 22 Jul 2020 06:06:33 GMT
COPY file:6952d2d38c707f223d813efd2d2969873cdd4b66d733559ef9be855aff5d8579 in /usr/local/bin 
# Wed, 22 Jul 2020 06:06:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 22 Jul 2020 06:06:52 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 22 Jul 2020 06:06:55 GMT
VOLUME [/opt/couchdb/data]
# Wed, 22 Jul 2020 06:06:59 GMT
EXPOSE 4369 5984 9100
# Wed, 22 Jul 2020 06:07:06 GMT
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
	-	`sha256:0b3998b500a4438c663c6ddff3243775e2001c0a3aa80b1ab282346ed00ec297`  
		Last Modified: Wed, 22 Jul 2020 06:08:09 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7c8710c5d25ec06f1f4cb08cd35302e87fc59839350cfd57d61def542b0a76`  
		Last Modified: Wed, 22 Jul 2020 06:08:13 GMT  
		Size: 49.1 MB (49125039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad6fba5e664a15057ca4170021c0379cfd241efe27fe7e5fa751754251cd7b1`  
		Last Modified: Wed, 22 Jul 2020 06:08:05 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781f269b4ac611f1f173ef363b179610efe70d76520931a1fa01670b2b75f273`  
		Last Modified: Wed, 22 Jul 2020 06:08:05 GMT  
		Size: 768.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605c65e312c1ec361af850aaf3459b649d4676c9064093b0533561d88abb665d`  
		Last Modified: Wed, 22 Jul 2020 06:08:05 GMT  
		Size: 2.1 KB (2051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b1041f357218543718e5acf1ecb1d1361f48e249e5b2ffc8862ee52617e582`  
		Last Modified: Wed, 22 Jul 2020 06:08:05 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.0.1`

```console
$ docker pull couchdb@sha256:3611dda04bc98722a46f3a01a7f879e13c19b0c8920866aa2130a84d8b39f3c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.0.1` - linux; amd64

```console
$ docker pull couchdb@sha256:237795a431e430fcca78ed1d60df02e135c931d734fa0ee3d7e711f33c634c85
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83199559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6cedc1775cff8209e40529bb0fad4b252a211d961fe4d89fb5b83ccfceee62f`
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
# Wed, 22 Jul 2020 14:32:33 GMT
ENV COUCHDB_VERSION=3.0.1
# Wed, 22 Jul 2020 14:32:34 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Wed, 22 Jul 2020 14:32:49 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 22 Jul 2020 14:32:50 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 22 Jul 2020 14:32:50 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 22 Jul 2020 14:32:50 GMT
COPY file:6952d2d38c707f223d813efd2d2969873cdd4b66d733559ef9be855aff5d8579 in /usr/local/bin 
# Wed, 22 Jul 2020 14:32:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 22 Jul 2020 14:32:51 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 22 Jul 2020 14:32:51 GMT
VOLUME [/opt/couchdb/data]
# Wed, 22 Jul 2020 14:32:51 GMT
EXPOSE 4369 5984 9100
# Wed, 22 Jul 2020 14:32:52 GMT
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
	-	`sha256:01a2b99c219c22bc2b58b5b3bf08b656d7d1c08b86ea6936f5e0c23212d404ff`  
		Last Modified: Wed, 22 Jul 2020 14:35:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec31835a82559118e2c9270543522ba05f329c1fc41a8f5ab43c8129853082db`  
		Last Modified: Wed, 22 Jul 2020 14:35:58 GMT  
		Size: 48.2 MB (48229512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e5c8019170ae4bfe6fc75b74b6e2c8c66ddd2bdd165ccc0d29cba6f1ebf520`  
		Last Modified: Wed, 22 Jul 2020 14:35:51 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7587d2da0135be4b07ef835d59126239bd4a8c4c1478b553140870f633f9ebc`  
		Last Modified: Wed, 22 Jul 2020 14:35:51 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713e11b00abdab3a216685d61899cdc6d59c6e6e350ad774f5de8a8a188b336e`  
		Last Modified: Wed, 22 Jul 2020 14:35:51 GMT  
		Size: 2.0 KB (2049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d823bcb0484e3ded03cea094f13e2ad3c0c98291023a19680a4878a111676d0c`  
		Last Modified: Wed, 22 Jul 2020 14:35:51 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.0.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:198c1ea7be3b19305bbc75b08a8ef18dcb0d027608ed9a62cf3b9cbaa5ea16a1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.2 MB (78236205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:713a03561c3fc8afaf28beca921edb3c34905fa99723701b8346490c2e396b65`
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
# Wed, 22 Jul 2020 04:04:03 GMT
ENV COUCHDB_VERSION=3.0.1
# Wed, 22 Jul 2020 04:04:05 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Wed, 22 Jul 2020 04:04:33 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 22 Jul 2020 04:04:35 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 22 Jul 2020 04:04:35 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 22 Jul 2020 04:04:36 GMT
COPY file:6952d2d38c707f223d813efd2d2969873cdd4b66d733559ef9be855aff5d8579 in /usr/local/bin 
# Wed, 22 Jul 2020 04:04:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 22 Jul 2020 04:04:39 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 22 Jul 2020 04:04:40 GMT
VOLUME [/opt/couchdb/data]
# Wed, 22 Jul 2020 04:04:41 GMT
EXPOSE 4369 5984 9100
# Wed, 22 Jul 2020 04:04:41 GMT
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
	-	`sha256:4df523caf83c9a09a5d3dd5a763d86d5cca588f7f6d931507a1f8f77e03aa8df`  
		Last Modified: Wed, 22 Jul 2020 04:08:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d25e564d851a585677c52323a31150a060f291dc3e1504ad0681d3a7310fd318`  
		Last Modified: Wed, 22 Jul 2020 04:08:15 GMT  
		Size: 44.7 MB (44708433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd9042ae75ba222a0b0d5d01322fb00616284fbc0bbc18f40ac8ba56b3fb890`  
		Last Modified: Wed, 22 Jul 2020 04:08:06 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2f5e4b0e1a2d48e7206f86f49cd381a681a5f8c04c515301b3523e1ef6a173c`  
		Last Modified: Wed, 22 Jul 2020 04:08:06 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3248b8b84d724ec0d65d8f39433f8de2e198a7c15c23ed56f700030ba9ee69f`  
		Last Modified: Wed, 22 Jul 2020 04:08:07 GMT  
		Size: 2.1 KB (2052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243dccbc57714060bf4c2b5a74baae876f855938aff8d8922e5a128c63011032`  
		Last Modified: Wed, 22 Jul 2020 04:08:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.0.1` - linux; ppc64le

```console
$ docker pull couchdb@sha256:52bc75bd6458644770743541984730dc66bdfe93bcd584bf813ccfa9ea639bbf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 MB (88355316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f059cb4caddb7bf14aa6a34b5322c745224ee37a992ba914ba1a3a23a0972b8`
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
# Wed, 22 Jul 2020 06:04:55 GMT
ENV COUCHDB_VERSION=3.0.1
# Wed, 22 Jul 2020 06:05:04 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Wed, 22 Jul 2020 06:06:21 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 22 Jul 2020 06:06:31 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 22 Jul 2020 06:06:32 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 22 Jul 2020 06:06:33 GMT
COPY file:6952d2d38c707f223d813efd2d2969873cdd4b66d733559ef9be855aff5d8579 in /usr/local/bin 
# Wed, 22 Jul 2020 06:06:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 22 Jul 2020 06:06:52 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 22 Jul 2020 06:06:55 GMT
VOLUME [/opt/couchdb/data]
# Wed, 22 Jul 2020 06:06:59 GMT
EXPOSE 4369 5984 9100
# Wed, 22 Jul 2020 06:07:06 GMT
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
	-	`sha256:0b3998b500a4438c663c6ddff3243775e2001c0a3aa80b1ab282346ed00ec297`  
		Last Modified: Wed, 22 Jul 2020 06:08:09 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7c8710c5d25ec06f1f4cb08cd35302e87fc59839350cfd57d61def542b0a76`  
		Last Modified: Wed, 22 Jul 2020 06:08:13 GMT  
		Size: 49.1 MB (49125039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad6fba5e664a15057ca4170021c0379cfd241efe27fe7e5fa751754251cd7b1`  
		Last Modified: Wed, 22 Jul 2020 06:08:05 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781f269b4ac611f1f173ef363b179610efe70d76520931a1fa01670b2b75f273`  
		Last Modified: Wed, 22 Jul 2020 06:08:05 GMT  
		Size: 768.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605c65e312c1ec361af850aaf3459b649d4676c9064093b0533561d88abb665d`  
		Last Modified: Wed, 22 Jul 2020 06:08:05 GMT  
		Size: 2.1 KB (2051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b1041f357218543718e5acf1ecb1d1361f48e249e5b2ffc8862ee52617e582`  
		Last Modified: Wed, 22 Jul 2020 06:08:05 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:570bcef2fc1a7ef94cd03b45fe680b8651940b34f1db870063ea98735223cd48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.1` - linux; amd64

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

### `couchdb:3.1` - linux; arm64 variant v8

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

### `couchdb:3.1` - linux; ppc64le

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

## `couchdb:3.1.0`

```console
$ docker pull couchdb@sha256:570bcef2fc1a7ef94cd03b45fe680b8651940b34f1db870063ea98735223cd48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.1.0` - linux; amd64

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

### `couchdb:3.1.0` - linux; arm64 variant v8

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

### `couchdb:3.1.0` - linux; ppc64le

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
