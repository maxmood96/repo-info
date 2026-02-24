<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchdb`

-	[`couchdb:3`](#couchdb3)
-	[`couchdb:3-nouveau`](#couchdb3-nouveau)
-	[`couchdb:3.4`](#couchdb34)
-	[`couchdb:3.4-nouveau`](#couchdb34-nouveau)
-	[`couchdb:3.4.3`](#couchdb343)
-	[`couchdb:3.4.3-nouveau`](#couchdb343-nouveau)
-	[`couchdb:3.5`](#couchdb35)
-	[`couchdb:3.5-nouveau`](#couchdb35-nouveau)
-	[`couchdb:3.5.1`](#couchdb351)
-	[`couchdb:3.5.1-nouveau`](#couchdb351-nouveau)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:3`

```console
$ docker pull couchdb@sha256:d55f35ffc020ca4c615fccfddd4f893d11f957593b12b33fce5e7b0840366ccd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:41766fcef3c3ab64a2b6d36560f237b23df3d29cea7c5c9d945f29d83896ac06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142059668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71979498d495be6e72756259eff755a726b88dd825408be29fb3aba1b5240175`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:20:54 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 24 Feb 2026 19:20:54 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 24 Feb 2026 19:21:00 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 24 Feb 2026 19:21:02 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 24 Feb 2026 19:21:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:07 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 24 Feb 2026 19:21:07 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 24 Feb 2026 19:21:21 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 24 Feb 2026 19:21:21 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 24 Feb 2026 19:21:21 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 24 Feb 2026 19:21:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Feb 2026 19:21:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:21:21 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:21:21 GMT
VOLUME [/opt/couchdb/data]
# Tue, 24 Feb 2026 19:21:21 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 24 Feb 2026 19:21:21 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7d73966d9314fcd3d72b1b0595152eb892287a887426b08e9811b94ae2b379`  
		Last Modified: Tue, 24 Feb 2026 19:21:34 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b3b202dd2e4a1bbf752929191ebe478db7474b2b54bf6748156e639d1336c6`  
		Last Modified: Tue, 24 Feb 2026 19:21:34 GMT  
		Size: 7.9 MB (7883121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7271a9298cc81eb015423fe434ed96701a704ee22755593dc7ab377c3d833050`  
		Last Modified: Tue, 24 Feb 2026 19:21:34 GMT  
		Size: 401.8 KB (401802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788dcc4a23034e7f3d98e0c1208b1d84d892332d87774695962802b0bc3c0ba4`  
		Last Modified: Tue, 24 Feb 2026 19:21:34 GMT  
		Size: 76.5 KB (76508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a61888d031364c28d8b161262599c1af189256403e0753623d967a543e66fc2`  
		Last Modified: Tue, 24 Feb 2026 19:21:35 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f591ba27f1c6cb2b55ff86d593c814940f7cfec9027f144771ca1abb4f1484d`  
		Last Modified: Tue, 24 Feb 2026 19:21:37 GMT  
		Size: 105.5 MB (105456525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296ca6c03411e008479fc5f485ead2445d1c10e83542a0f803f26e693f8c990f`  
		Last Modified: Tue, 24 Feb 2026 19:21:35 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269188377ea3f7d37af3b7885f565f7d389edb04de18151f2a6912e78d9636de`  
		Last Modified: Tue, 24 Feb 2026 19:21:35 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1361f09b26e9d82d4283c4bebe3697cce16e5c358fb2e5b0d7d307bc6b62ec15`  
		Last Modified: Tue, 24 Feb 2026 19:21:36 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a75cb6d22638fcb69fb3d276b158b220964f410718633d00c472bbf795fc0e1`  
		Last Modified: Tue, 24 Feb 2026 19:21:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:6538ab89712240a307f4f3cc91b72512adcc89143967f8bbe4ad622d85ed6e0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99925e22ce7d2cb43c93f63b1e6827c2f235c3e9808a820d7d95820deb5fe769`

```dockerfile
```

-	Layers:
	-	`sha256:2d6482430b6b5635652a50047b4489bb7944b7974c056abc260ef4fdeff9687a`  
		Last Modified: Tue, 24 Feb 2026 19:21:34 GMT  
		Size: 4.2 MB (4184421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fa746e2a5678a43070ce809bd32b3918490c0cfa6c206f7f768bd208f1da7de`  
		Last Modified: Tue, 24 Feb 2026 19:21:34 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:770dce57c3d96e16be18d9c33673657a065bc5cf0b72ddd4a469de4ce0e28339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141419192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f29a3517318bc3af48f6be7a479b9ba60373ac6af58d062f5b3a967d7f63d2a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:25:24 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 24 Feb 2026 19:25:24 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 24 Feb 2026 19:25:30 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:25:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 24 Feb 2026 19:25:33 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 24 Feb 2026 19:25:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:25:37 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 24 Feb 2026 19:25:37 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 24 Feb 2026 19:25:51 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 24 Feb 2026 19:25:51 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 24 Feb 2026 19:25:52 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 24 Feb 2026 19:25:52 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Feb 2026 19:25:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:25:52 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:25:52 GMT
VOLUME [/opt/couchdb/data]
# Tue, 24 Feb 2026 19:25:52 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 24 Feb 2026 19:25:52 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5195943c8bc81ff3ccacc7d15e0222f0ddc0a363f1da17509b63e4dd41b2299f`  
		Last Modified: Tue, 24 Feb 2026 19:26:05 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbba4689c9413d25ec04c6c788241c6a8ab4ca2ee82346c96241d886dd4588b`  
		Last Modified: Tue, 24 Feb 2026 19:26:05 GMT  
		Size: 7.7 MB (7692638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3981bae95c2cf4b56a60963485420ec03af0c4467a5c204fc9de44bbfaa076c5`  
		Last Modified: Tue, 24 Feb 2026 19:26:05 GMT  
		Size: 370.5 KB (370543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0780dc8172b862928867ea7afe0354b30bfee9ddd9500fcd0ee128ec7db63069`  
		Last Modified: Tue, 24 Feb 2026 19:26:05 GMT  
		Size: 76.5 KB (76468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada3951d847dd448afd38f10999ea754f9d96abd69c5e876ea8eb8e0708cda8c`  
		Last Modified: Tue, 24 Feb 2026 19:26:06 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081dd262f305fc888779fda5162e7ef14b3dd157bda32f9adfe0c71e3c53b9f3`  
		Last Modified: Tue, 24 Feb 2026 19:26:08 GMT  
		Size: 105.2 MB (105158034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae02b6144e60ba0617faf2dabd56adf4ae0b8ca4696cec8383550db4ccfeb03a`  
		Last Modified: Tue, 24 Feb 2026 19:26:06 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349350c52f60a43ac4b9153a28573e1ed7c6230729482261de86e4eec142f621`  
		Last Modified: Tue, 24 Feb 2026 19:26:06 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d040afc70746c77854a2e80fbac73e1f602fbf8ac82fecebc968cef9598cf9`  
		Last Modified: Tue, 24 Feb 2026 19:26:07 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aaa06830632dd23874fc9a34e260c5027305c63c186b36c7cf19232e3c3e9c9`  
		Last Modified: Tue, 24 Feb 2026 19:26:07 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:8e105bac4709d132c2132b3c176eec75158d671f9088324761cffbc47aff3602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa658a9c5ab56fe8f6fd623762676a48f4c87358be034ae7fecbbf3b1500921`

```dockerfile
```

-	Layers:
	-	`sha256:3a05677e5b72845cdfc530571ac1a2ef5046321baf165d46020942e6fd7d4ca9`  
		Last Modified: Tue, 24 Feb 2026 19:26:05 GMT  
		Size: 4.2 MB (4184714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57719038c77b024cd456dcee02cf0aa52f7a7b967dc3a6056213dbffc43702c5`  
		Last Modified: Tue, 24 Feb 2026 19:26:05 GMT  
		Size: 31.9 KB (31932 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; s390x

```console
$ docker pull couchdb@sha256:b37585c645221c6f47e1720d73d41e2913dd4c5d9da1325227b92148e3f00c53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138773629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9ccda5442365d739afa4c52c7891f387b7a41f8159f6d886b58c68ab7da04b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:58:41 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 24 Feb 2026 20:58:41 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 24 Feb 2026 20:59:11 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:59:16 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 24 Feb 2026 20:59:16 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 24 Feb 2026 20:59:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:59:33 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 24 Feb 2026 20:59:34 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 24 Feb 2026 21:00:16 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 24 Feb 2026 21:00:17 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 24 Feb 2026 21:00:17 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 24 Feb 2026 21:00:18 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Feb 2026 21:00:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 21:00:18 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 21:00:18 GMT
VOLUME [/opt/couchdb/data]
# Tue, 24 Feb 2026 21:00:18 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 24 Feb 2026 21:00:18 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1eeb0a30f79824913befe6cff540b6bbef64ce01bcd01d02353436b346f1c52`  
		Last Modified: Tue, 24 Feb 2026 21:01:18 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed832851f69da334438fcc233f300fb11f53288452d86a31700195783d07b7b`  
		Last Modified: Tue, 24 Feb 2026 21:01:23 GMT  
		Size: 7.4 MB (7399099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283498defbfbbe68c63defadeb6bd597efc21eeae2245bd6ef3a48b45792b2eb`  
		Last Modified: Tue, 24 Feb 2026 21:01:17 GMT  
		Size: 372.2 KB (372246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e76b77d775634501854d45ab3d68cf569581ce20c532eb424e4b24916cc697`  
		Last Modified: Tue, 24 Feb 2026 21:01:18 GMT  
		Size: 76.7 KB (76745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7caefca7f93130ff023ae08185691df23526132092c2d1c0f6abbe4953830c`  
		Last Modified: Tue, 24 Feb 2026 21:01:21 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9967421ea9282f965997b6135e3475d745fa5dbf3779675c500ca2da629a6879`  
		Last Modified: Tue, 24 Feb 2026 21:01:24 GMT  
		Size: 104.0 MB (104028576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185c2f75ff7c0754709bd9b4d1960fa9befe3e99a1740f14b2a362a4e8f893e4`  
		Last Modified: Tue, 24 Feb 2026 21:01:19 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75895523cafbc3bf7cc90bcd1beb3eb6446ff705134466fc56c3d3dd5f46b12`  
		Last Modified: Tue, 24 Feb 2026 21:01:21 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c9910bd6a90ab78f2a16acf8792a2f83e235d516f41e2e74a5b64df59d78f0`  
		Last Modified: Tue, 24 Feb 2026 21:01:22 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46ae2bc44dafb76079ab9db1dd230550789fad97c3b93aef7bbbd770298056c`  
		Last Modified: Tue, 24 Feb 2026 21:01:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:b6a18a48d50c63a224991d5e294fc51a4096f16c8d0cc7533d18e8af2c00b9d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35047fcb81ed162b1e68c86ff7087b1eab1a17c69fa0b371b511f7912315824`

```dockerfile
```

-	Layers:
	-	`sha256:ebf92ddcfc83a696b60fc5a62ee38340c62d83b965fcfc2fa6abad4a5217e495`  
		Last Modified: Tue, 24 Feb 2026 21:01:18 GMT  
		Size: 4.2 MB (4180617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f74ac14845fdc83f326ed34daccc3fda4c7d18d05582eaccd9dfc0e2891e4325`  
		Last Modified: Tue, 24 Feb 2026 21:01:17 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:ad299a7562b39c51224020dc60f1f909fb0ff1042493b77f12b54d202831b5ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:63028f38a14c746b6610482b292f2b70386fb8420371d81e899dc171bf9e1cac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156462375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8f868f8ae52c99fd9de628425892e417ef6c3e09a08bbb4f7ace5d1e8da629`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:21:02 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 24 Feb 2026 19:21:02 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 24 Feb 2026 19:21:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:15 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 24 Feb 2026 19:21:18 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 24 Feb 2026 19:21:21 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:22 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 24 Feb 2026 19:21:28 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 24 Feb 2026 19:21:28 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 24 Feb 2026 19:21:28 GMT
VOLUME [/opt/nouveau/data]
# Tue, 24 Feb 2026 19:21:28 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 24 Feb 2026 19:21:28 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ddecf20ba5b4b57590d3302037e328fd1e5b649ada9afe1077b1527b57ea1d`  
		Last Modified: Tue, 24 Feb 2026 19:21:43 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f050c4933d55a438411503b72e2599a05933423782db3fdbe74c1169b1eb9f79`  
		Last Modified: Tue, 24 Feb 2026 19:21:44 GMT  
		Size: 7.9 MB (7883160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8766f1911d4db3708ea04e17aec8ef20c715fe46f8fa163ca3ce5fb7da96c0`  
		Last Modified: Tue, 24 Feb 2026 19:21:45 GMT  
		Size: 77.4 MB (77380921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27505ffdad9b3b9ee1faf0425665128cde5fa3d92e437985492bfcfd48c3daaf`  
		Last Modified: Tue, 24 Feb 2026 19:21:43 GMT  
		Size: 424.2 KB (424151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775b0f7b272fa1afd4e729b58d254862b055044b412ad10d149e941a5160a8bd`  
		Last Modified: Tue, 24 Feb 2026 19:21:45 GMT  
		Size: 99.6 KB (99567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103c9a7e496556a022a3693afb975edd7f5d2c030589b6507aeb0e875bc63784`  
		Last Modified: Tue, 24 Feb 2026 19:21:45 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43708c9e9bf3275d81d21f997991dd95b3fcb1d8b3d913c4998f716ede5eaa63`  
		Last Modified: Tue, 24 Feb 2026 19:21:46 GMT  
		Size: 42.4 MB (42436414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9309990c5553a8aba351cd8e6cef3b1e0bf7d4b6cd2018e8ee26b2ee680f18`  
		Last Modified: Tue, 24 Feb 2026 19:21:46 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:88a4a1b5d2bf9af1822defa276f9543e062d8f7cd349c08cecbcde70094878cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631682cf89179999d5b185f059802920a43a7d4e464fbcc862160c18e843f455`

```dockerfile
```

-	Layers:
	-	`sha256:499345d0a7a481daaffbb8965f4762e8dfe41f4174953070f2f2a757872028a2`  
		Last Modified: Tue, 24 Feb 2026 19:21:43 GMT  
		Size: 3.7 MB (3658095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00348bba47c2e9b12086a11819274c277f12e27cc217565f02b5ee77e41e7dff`  
		Last Modified: Tue, 24 Feb 2026 19:21:43 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:90300ee575847a78a0ac8469e4ca439296ff76a18037c079b043ef1240a2fc4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155342048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095919028295ae8e9811d72082cd88abe6ce7a7b9fdd493ea45257a426a9fa90`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:25:45 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 24 Feb 2026 19:25:45 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 24 Feb 2026 19:25:51 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:25:58 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 24 Feb 2026 19:26:01 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 24 Feb 2026 19:26:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 24 Feb 2026 19:26:11 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 24 Feb 2026 19:26:12 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 24 Feb 2026 19:26:12 GMT
VOLUME [/opt/nouveau/data]
# Tue, 24 Feb 2026 19:26:12 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 24 Feb 2026 19:26:12 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e26c0f056669b165a8ae59eaff14387edf0f261e8b450067813093d83930c73`  
		Last Modified: Tue, 24 Feb 2026 19:26:26 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9820074d8ac8dcf46e3efdf9679ade22002a185cc39b3f7578826f640e83587`  
		Last Modified: Tue, 24 Feb 2026 19:26:27 GMT  
		Size: 7.7 MB (7692622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e888a3c3c9fa56a143880febc9d826e8bec60a6a09ce8f2f1bfa5ac7c2dc29f1`  
		Last Modified: Tue, 24 Feb 2026 19:26:28 GMT  
		Size: 76.7 MB (76700050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56721790700ad6a8decec8f7e7c2da18ad1c9b0708cc502a05a49e174ce46d06`  
		Last Modified: Tue, 24 Feb 2026 19:26:26 GMT  
		Size: 392.8 KB (392770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e29871ea620339c69ce3817fc2d93fa827c472742ac3f984d6798318379448`  
		Last Modified: Tue, 24 Feb 2026 19:26:27 GMT  
		Size: 99.5 KB (99520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6e3773a84b9dae8befc65af5e5a3e970f192593d2e36b0b1836abc3a018724`  
		Last Modified: Tue, 24 Feb 2026 19:26:28 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb2b450c1ba8c12a3548ef9746da587ae85038952093ec2c15072768da58330`  
		Last Modified: Tue, 24 Feb 2026 19:26:29 GMT  
		Size: 42.3 MB (42339126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbeb35bc414ae41b2b4da730a59d4ee5a8181e35a4e3b83842f742121b99993`  
		Last Modified: Tue, 24 Feb 2026 19:26:29 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:6a6fb2fe398fca430e75696ef76cdf08024df46c6feeed01e317aa99233671e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa2f6ebf52b151e48808601cae4de7825d0f252285de645a9cb4dd9b86a46b2`

```dockerfile
```

-	Layers:
	-	`sha256:dcfc735a1fabe515dca1c188ca05762d93b1db9e33112021574819b5d4742ef7`  
		Last Modified: Tue, 24 Feb 2026 19:26:26 GMT  
		Size: 3.7 MB (3656771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ca8f03f33a2591f16bea1316bd8899b382a7710144eb8162622e7584d3a39a3`  
		Last Modified: Tue, 24 Feb 2026 19:26:26 GMT  
		Size: 24.7 KB (24703 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:2e4472b408c0333e2977f33a8bfb7d510f88cb1aab0a7988af6739167e6e1eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150105815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7852f3425b90f93b2dc01b1e9f55e19fdd6b31db61e5e4b360ac68079cb5f896`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:58:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 24 Feb 2026 20:58:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 24 Feb 2026 20:59:11 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:59:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:59:41 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 24 Feb 2026 20:59:41 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 24 Feb 2026 21:00:02 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:00:03 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 24 Feb 2026 21:00:22 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 24 Feb 2026 21:00:24 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 24 Feb 2026 21:00:24 GMT
VOLUME [/opt/nouveau/data]
# Tue, 24 Feb 2026 21:00:24 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 24 Feb 2026 21:00:24 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a950e14c7d88cf86c9d9f9f5d81eb0a6b66998ba15461f24cf32c54767ad382`  
		Last Modified: Tue, 24 Feb 2026 21:01:23 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ad91eaeb8b4d910bab5880a0168f86b9d9ccd494cc0e2c363abef9ed6361d5`  
		Last Modified: Tue, 24 Feb 2026 21:01:23 GMT  
		Size: 7.4 MB (7399125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ecc468cc57fa7504bc399c879bbdeeababdcf31c418cdd66c4c5078deded16`  
		Last Modified: Tue, 24 Feb 2026 21:01:25 GMT  
		Size: 73.2 MB (73153712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28c50c2f86346560509995780e524a097a56cc46e1be1ff10e6d9b7215617df`  
		Last Modified: Tue, 24 Feb 2026 21:01:23 GMT  
		Size: 394.6 KB (394634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f944fabb2ccbde3fd8f7bae3e9dfcc47f3404a64b0155a38b80bf162ccced73`  
		Last Modified: Tue, 24 Feb 2026 21:01:24 GMT  
		Size: 99.9 KB (99898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcc8fc571c26bb731d288c5f2e27c40b126abe67e58f979bd6ae46e51befb76`  
		Last Modified: Tue, 24 Feb 2026 21:01:24 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385829014d2303d4b21b8b070f89c2ef8a306df85e8c3e8d0e85a8883c4c2217`  
		Last Modified: Tue, 24 Feb 2026 21:01:25 GMT  
		Size: 42.2 MB (42165035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08a99fb7b0c3348916dd13728c92af578510c3769cb53f3b5f6d7d9daa58ee73`  
		Last Modified: Tue, 24 Feb 2026 21:01:25 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:6668e725b2c526b9c98685853b218fabcfe534c0bbe372c9c52d62958868c2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0f3fa400a6f7d0917b3d1feb53fa0f8a6f92f09779bae79f9861bed5f1a30b`

```dockerfile
```

-	Layers:
	-	`sha256:33647360be3076acd9276e12e6453e64a05fe294f1152df02bd81def6ae34b86`  
		Last Modified: Tue, 24 Feb 2026 21:01:23 GMT  
		Size: 3.6 MB (3648624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2786da3d1f564b542091d726336018be02ead528326f1772e60c8a37807fd671`  
		Last Modified: Tue, 24 Feb 2026 21:01:22 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4`

```console
$ docker pull couchdb@sha256:01204091e6741331df41129e8ef40759d8823c2984138f655e6338cbc4f58b49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.4` - linux; amd64

```console
$ docker pull couchdb@sha256:0e4991a742d5565970442c58d716aa28504ca1ada5e37e53b1acbdf79b2e980f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139023018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db5f1922073e9c3c697f66e22b5ff4ea481d930943e24e7fb4dbd1753b528ab`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:20:55 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 24 Feb 2026 19:20:55 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 24 Feb 2026 19:21:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 24 Feb 2026 19:21:03 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 24 Feb 2026 19:21:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:08 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 24 Feb 2026 19:21:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 24 Feb 2026 19:21:22 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 24 Feb 2026 19:21:22 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 24 Feb 2026 19:21:22 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 24 Feb 2026 19:21:22 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Feb 2026 19:21:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:21:22 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:21:22 GMT
VOLUME [/opt/couchdb/data]
# Tue, 24 Feb 2026 19:21:22 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 24 Feb 2026 19:21:22 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a683baf7f8a6c265f389828fd08373642cdef3abede137a2e747c07a2ddd3646`  
		Last Modified: Tue, 24 Feb 2026 19:21:34 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf81c5cd0abaa9b95efb1238d0115073ea7af9a0c052eb1230cb022c10291b00`  
		Last Modified: Tue, 24 Feb 2026 19:21:34 GMT  
		Size: 7.9 MB (7883119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2ddde98185ea8e526dbe7e9dee56e09e278380bbcea64403e3860a75df3385`  
		Last Modified: Tue, 24 Feb 2026 19:21:34 GMT  
		Size: 401.8 KB (401804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f936bc2fd65af0470fb51e4b3e8d58d8e576bd8548c4acc2bdae3406838f082`  
		Last Modified: Tue, 24 Feb 2026 19:21:34 GMT  
		Size: 76.5 KB (76503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04743336f0803fdac5b43449e135fb61edc978bcc467a3f51a4211595ad4191a`  
		Last Modified: Tue, 24 Feb 2026 19:21:35 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68e61b5d4b34c9ed519f9fbfac9e667c9bc73fd1d63ac9e48378a5b6dd9338c`  
		Last Modified: Tue, 24 Feb 2026 19:21:37 GMT  
		Size: 102.4 MB (102419880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd840b9221289c7922c86ea7a89adabf87cea68ae1d0a500169f55722145358`  
		Last Modified: Tue, 24 Feb 2026 19:21:35 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11e050400c21ba703f5698401cc59fdd9c78f7c96454db2b6c8a0dcfb472108`  
		Last Modified: Tue, 24 Feb 2026 19:21:36 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5916a7f5eb1b7c77f78c93c6f02d12282969c65b9e4ee1cc198cf098e12709`  
		Last Modified: Tue, 24 Feb 2026 19:21:36 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2662f0586b3d359b31a0d164df20cce5c8831951852b8d53efe36abf6339b6`  
		Last Modified: Tue, 24 Feb 2026 19:21:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:162731868319f530a4b1b00c5089f7f0395a24a24368a0aa5ce66440cd9fec5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c1a9b5d4365d534be3ce56a49f6f16d3d2cdcc70dc9916b88185e25d6dacd33`

```dockerfile
```

-	Layers:
	-	`sha256:7402abfa944f8ae92f9b87bc0bac2b6a1d76687641b9eff6a40e2fa68ebcc920`  
		Last Modified: Tue, 24 Feb 2026 19:21:34 GMT  
		Size: 4.1 MB (4125395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e6f57df0139d3b85fb554e0021577efa66b3383cbbbe1cbff34e17da5456cc1`  
		Last Modified: Tue, 24 Feb 2026 19:21:34 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:a778be373bfa48e25079f01a884489cd703f5a2f60041900425b76ef4d09756d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138430308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd69c64beee820811587f39871b3d66d946314295f724774ff900d949ae124a6`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:25:49 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 24 Feb 2026 19:25:49 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 24 Feb 2026 19:25:55 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:25:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 24 Feb 2026 19:25:58 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 24 Feb 2026 19:26:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:03 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 24 Feb 2026 19:26:04 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 24 Feb 2026 19:26:17 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 24 Feb 2026 19:26:17 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 24 Feb 2026 19:26:18 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 24 Feb 2026 19:26:18 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Feb 2026 19:26:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:26:18 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:26:18 GMT
VOLUME [/opt/couchdb/data]
# Tue, 24 Feb 2026 19:26:18 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 24 Feb 2026 19:26:18 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b28d2d12bad652a55c58ab7bf4d17670fd6aab9979954aa3884e485d3149af8`  
		Last Modified: Tue, 24 Feb 2026 19:26:31 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3fcc6cddb2755eaa032a78d87b6e1feeda7b1e2a2bb8caf2d8371a1fe9377e`  
		Last Modified: Tue, 24 Feb 2026 19:26:31 GMT  
		Size: 7.7 MB (7692635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72fcb8d72aa88c8fea61ed14aa330c04a2ffb4179404f99dfeee3faa77193e4e`  
		Last Modified: Tue, 24 Feb 2026 19:26:30 GMT  
		Size: 370.5 KB (370523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40efd2a2232b7aa9ef4b46e15e1f66681c8bd92d67a16b0001e517f86d23b22`  
		Last Modified: Tue, 24 Feb 2026 19:26:31 GMT  
		Size: 76.5 KB (76516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078dd7c0bddb561417644e2ba1d49a6350bf80fff84afd4faff1e01b66149671`  
		Last Modified: Tue, 24 Feb 2026 19:26:32 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55631184889826b81cd2e8b606fd4bc04de2be6679e1db088ee80659668969b`  
		Last Modified: Tue, 24 Feb 2026 19:26:39 GMT  
		Size: 102.2 MB (102169108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db4eb7d337ab5afd4d84fbed6f257b45991592ed1369d424f3de86f7085a9f17`  
		Last Modified: Tue, 24 Feb 2026 19:26:33 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8726f9d73eba2cd63901c6d3fb2cf2a60d59554f8f35518655bd46d1f5e312`  
		Last Modified: Tue, 24 Feb 2026 19:26:33 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b807cf16d9797b98d1d8f9c2f2f31999eaf46bbd16c7f782b08fa776f17b60`  
		Last Modified: Tue, 24 Feb 2026 19:26:34 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6f08b4ae8b26be7ea998b896ab6599abc74b582d17cf55027a82dfc0f984b4`  
		Last Modified: Tue, 24 Feb 2026 19:26:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:0845d0af4e2091278dd04147b8f0e95a1543b3bad69759e3a16ff575c4ad3b00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41f855b205c643d0ae89a0b82c5aa869c01c3fc702384bc4def5b6ed3a290b3d`

```dockerfile
```

-	Layers:
	-	`sha256:b5cb499d4bbf287b6640cdebb2b1b76298240ad7d4ba44fc62e55c5c493bb767`  
		Last Modified: Tue, 24 Feb 2026 19:26:31 GMT  
		Size: 4.1 MB (4125664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f04750f39f834bb9ca489ecc291ae657ef44869528bc6dacdc8df8e5f6278fde`  
		Last Modified: Tue, 24 Feb 2026 19:26:30 GMT  
		Size: 31.3 KB (31318 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; s390x

```console
$ docker pull couchdb@sha256:a47d16e7e14ba98e63ac796cab261c72f68c96b3f6c3094430ede9e2f63a42f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135801600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd1011a14856c3429db9fb744a49a2566d70094e9db7d1d67f4eff6042ad4179`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 21:00:09 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 24 Feb 2026 21:00:09 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 24 Feb 2026 21:00:24 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:00:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 24 Feb 2026 21:00:29 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 24 Feb 2026 21:00:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:00:51 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 24 Feb 2026 21:00:51 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 24 Feb 2026 21:01:25 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 24 Feb 2026 21:01:25 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 24 Feb 2026 21:01:26 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 24 Feb 2026 21:01:26 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Feb 2026 21:01:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 21:01:27 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 21:01:27 GMT
VOLUME [/opt/couchdb/data]
# Tue, 24 Feb 2026 21:01:27 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 24 Feb 2026 21:01:27 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a340bdf9c7c5ba07c112275cebe27ccde1fa61c7659de0debe073728d819059c`  
		Last Modified: Tue, 24 Feb 2026 21:02:08 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d02088da685a9d9b76e98c5228b8b904660c77c03c2cbdf1ce83922b81eadf6`  
		Last Modified: Tue, 24 Feb 2026 21:02:09 GMT  
		Size: 7.4 MB (7398990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf8644328d48b42c38c7dd84d0d2beb60fc1fb8b84efb6aee0fefba5db05646`  
		Last Modified: Tue, 24 Feb 2026 21:02:08 GMT  
		Size: 372.2 KB (372185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd72e9d17fc8e6e638b6a642c356ea55e2705d491756fb71c166ca597bc7792`  
		Last Modified: Tue, 24 Feb 2026 21:02:08 GMT  
		Size: 76.7 KB (76678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51943d754b5cb7725df1367d50ce6e9e57c2f06152d84be449e646a3cfb1d1f0`  
		Last Modified: Tue, 24 Feb 2026 21:02:09 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412b690160da2671bc7c123437535fb6e6048babbaec4a9825fe3a5b875b0f17`  
		Last Modified: Tue, 24 Feb 2026 21:02:12 GMT  
		Size: 101.1 MB (101056780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e9c499db2dada13189d46f57e60700ff5f64a1c4e23c3547207585f86b3a51`  
		Last Modified: Tue, 24 Feb 2026 21:02:10 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50772484603279fe83f59102b79ede21c1fcb6e492ba192cf996ccc4f73bc263`  
		Last Modified: Tue, 24 Feb 2026 21:02:10 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfda85c39641c6570f2de3a92678394e3c3c67c94798f4537819b7c6bf25f22`  
		Last Modified: Tue, 24 Feb 2026 21:02:11 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f42fc6ec048ef3563ed295ed8d1d21cff8f6712d3812e82263fb524515a4a11`  
		Last Modified: Tue, 24 Feb 2026 21:02:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:cb194641b2ea2865a51b18429ec630227618b275df006d480cf1a325d64e0173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49de05c81b3a96406ec3411d6b2c0dee49a32e3a90982081724d676ca746058c`

```dockerfile
```

-	Layers:
	-	`sha256:4d7da816c5f606e004b7c4a6b4a201461d005262698c9aea95e821c9d7414297`  
		Last Modified: Tue, 24 Feb 2026 21:02:09 GMT  
		Size: 4.1 MB (4121591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35d514871f4d725c93b9abcff7e8460eb701171f0183773da70bffebff05008e`  
		Last Modified: Tue, 24 Feb 2026 21:02:08 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4-nouveau`

```console
$ docker pull couchdb@sha256:831fde8ccc1a7f3453d1aede5977b9217de16b6f37553cd97d6cfdfc3d3c4c90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.4-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:8c0318b75e79ceac04a9ce37e77841e936e94c5b8428dfc0bd8abfeb813b46b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156462150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3948e2913127a9f2cb3c117872a85060d8f6b2ddb873b339a9c060b531da5cd`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:21:16 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 24 Feb 2026 19:21:16 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 24 Feb 2026 19:21:22 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:30 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 24 Feb 2026 19:21:32 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 24 Feb 2026 19:21:36 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:36 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 24 Feb 2026 19:21:41 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 24 Feb 2026 19:21:42 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 24 Feb 2026 19:21:42 GMT
VOLUME [/opt/nouveau/data]
# Tue, 24 Feb 2026 19:21:42 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 24 Feb 2026 19:21:42 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d786beeca1062353bf08793c9c6bf98a0f87418152080a90eb130e1c5965f8f6`  
		Last Modified: Tue, 24 Feb 2026 19:21:56 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1232e4788dea0cdb9581cdbe33ae964be23854c6ba3262d0ddbd70271ab4e2`  
		Last Modified: Tue, 24 Feb 2026 19:21:57 GMT  
		Size: 7.9 MB (7883139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eea41a6714c45b751163a46e19ba3c01f7bf0184a0c6c32392d70120d93c6c1`  
		Last Modified: Tue, 24 Feb 2026 19:21:59 GMT  
		Size: 77.4 MB (77380971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753887b2408fbeb9f6e042ae2842c33652b5abb9e3013b5363364437ce55c044`  
		Last Modified: Tue, 24 Feb 2026 19:21:57 GMT  
		Size: 424.2 KB (424172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cd36223fc5a9085843fc83719ee93222c5b7f3015b8ee042cee0703195d7f0`  
		Last Modified: Tue, 24 Feb 2026 19:21:58 GMT  
		Size: 99.6 KB (99593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5348cedb545b737771245e0a3142aa524f3fe83c031fa5eadd381397bad709`  
		Last Modified: Tue, 24 Feb 2026 19:21:58 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b4f78934567782c3933e2b1a7d1ce3edcbca0ca48ab4370e68d40093c69153`  
		Last Modified: Tue, 24 Feb 2026 19:22:00 GMT  
		Size: 42.4 MB (42436113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c427adfba75e7b9583fa82531baddd53a52b748e5f60413d0ee35c918d40aeb`  
		Last Modified: Tue, 24 Feb 2026 19:21:59 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:17d3bec69aaa0db494c3d4ad21edff4ebbe1ddab435ba4c4526899e8e594be19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3c2a142840d43535e346bf332a82a4059b8527c2125b78da8ed5ce0fd5d35e`

```dockerfile
```

-	Layers:
	-	`sha256:621df8e47d1bbb28b609baa47b5cc9b17e874d76b2a9d92984e5f6d664bfa6f5`  
		Last Modified: Tue, 24 Feb 2026 19:21:57 GMT  
		Size: 3.7 MB (3657789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ed5c79902c3cd66725094e87a5d7f5a79ba31fea78cf2d8d0bc858fce945252`  
		Last Modified: Tue, 24 Feb 2026 19:21:56 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:c8760aedf9f3ca7fab4054a45bb0f06306c809fee4ba265e665577cf4d954bd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155341123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6baa571ae1462fde33e464b5cce727354362bccf2aa3027736ec8453b73aaf9`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:25:50 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 24 Feb 2026 19:25:50 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 24 Feb 2026 19:25:56 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:03 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 24 Feb 2026 19:26:06 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 24 Feb 2026 19:26:10 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:10 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 24 Feb 2026 19:26:15 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 24 Feb 2026 19:26:15 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 24 Feb 2026 19:26:15 GMT
VOLUME [/opt/nouveau/data]
# Tue, 24 Feb 2026 19:26:15 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 24 Feb 2026 19:26:15 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227e384de6cd851ba010ab55fd097b78f1455d789ec6571ff85551fe42c66592`  
		Last Modified: Tue, 24 Feb 2026 19:26:30 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e143170d7088ef52275cb83ede528717dded1fc89ef30e180341730440de118c`  
		Last Modified: Tue, 24 Feb 2026 19:26:31 GMT  
		Size: 7.7 MB (7692654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1921aece143404191b4e7b6ef3569c019b94f4a537ffe73c19906522cdd30c7b`  
		Last Modified: Tue, 24 Feb 2026 19:26:32 GMT  
		Size: 76.7 MB (76700067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea535af4a8896de3981cb593bec663699183279d1c0f2790b4455fc640fcdb2a`  
		Last Modified: Tue, 24 Feb 2026 19:26:30 GMT  
		Size: 392.8 KB (392760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99983fa952bf9c5cfad5ba086d94005dcfad9533e710c9d47a7e88a76c22457e`  
		Last Modified: Tue, 24 Feb 2026 19:26:31 GMT  
		Size: 99.5 KB (99523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46cff693433aa6f3215ca4304ce1ade00c5d146c69122cf17511458ec2559125`  
		Last Modified: Tue, 24 Feb 2026 19:26:32 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216191418b7524c42e28d13c007476075fbceaaa80b42071b4f6aded28efdd8c`  
		Last Modified: Tue, 24 Feb 2026 19:26:33 GMT  
		Size: 42.3 MB (42338155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab33c06eabaf323ab625c8d9b524e0b98da7c63ecb4a9425b7e446d908cf4cf`  
		Last Modified: Tue, 24 Feb 2026 19:26:33 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:56d92e6171fbd62abcc2d5086396e0628196d68e7c46047584569a7332c13ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3680838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c511b3dfcb4f84381c6ab3ac001fef2818aa7e0a7508cf107fe2bb32e6b2494`

```dockerfile
```

-	Layers:
	-	`sha256:4727687559b55ce121ddb0d368b0a858849fa69077bae7ed7a3f5ef841e051ee`  
		Last Modified: Tue, 24 Feb 2026 19:26:30 GMT  
		Size: 3.7 MB (3656453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da11af15d871d64e39437bbe4310cc9d0872021fcd10afcd219d0de6a0450c20`  
		Last Modified: Tue, 24 Feb 2026 19:26:30 GMT  
		Size: 24.4 KB (24385 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:9c05b18dff0cf00441a9d9e3d8b681f5e3e9507c98bed2235a0370520a772f7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150103941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8773f2908b035ba7b5e0196a3b08c9eb7ef58464769a75a5b9deaaab730021`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 21:00:37 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 24 Feb 2026 21:00:37 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 24 Feb 2026 21:01:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:01:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:01:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 24 Feb 2026 21:01:33 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 24 Feb 2026 21:01:49 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:01:51 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 24 Feb 2026 21:02:14 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 24 Feb 2026 21:02:15 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 24 Feb 2026 21:02:15 GMT
VOLUME [/opt/nouveau/data]
# Tue, 24 Feb 2026 21:02:15 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 24 Feb 2026 21:02:15 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1f3fec8b48066b20be403a988ba842f0d420ac3eefffa49d99bb38555aa745`  
		Last Modified: Tue, 24 Feb 2026 21:02:47 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d3c2e86b6018b10bac3442abddc96c7d49b6d15c2321f47a75cb25356a6ff4`  
		Last Modified: Tue, 24 Feb 2026 21:02:48 GMT  
		Size: 7.4 MB (7399151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9dbc3ec363bde23293f059da65cff7972bd5f84a3a6e016f8be1c7f3895e0d5`  
		Last Modified: Tue, 24 Feb 2026 21:02:50 GMT  
		Size: 73.2 MB (73153462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75c677841d683f6911c3e01b7cc4c0144a01135bd9ef330d8ccf949cb561c49`  
		Last Modified: Tue, 24 Feb 2026 21:02:47 GMT  
		Size: 394.6 KB (394627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9905a105efb9f40c8b4b01994eb3f53b91c7d5e53c337bdf2f5ce0b01408afc1`  
		Last Modified: Tue, 24 Feb 2026 21:02:49 GMT  
		Size: 99.8 KB (99850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a14c1303bf766d3c1b07ca076074648c21be156b33e58890bd477c71d205d0`  
		Last Modified: Tue, 24 Feb 2026 21:02:49 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3671e6a5c6dc3e5c0c2c4647d27b605e77b7598d12c4e440076f9b55c5b5348`  
		Last Modified: Tue, 24 Feb 2026 21:02:50 GMT  
		Size: 42.2 MB (42163440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13611bc3d7c364e9358bdfa09574d1d17228c97d6c328f062c83b4a9b5d516f7`  
		Last Modified: Tue, 24 Feb 2026 21:02:50 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:d9d82bb35155ed46a6b002c86ce7e2e3519931065eb21d9dd845335a0fc13b99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3672533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d19a97fa8445d03eba812dfea1542179c91a0938f88979ea19a9b7e699b26f2`

```dockerfile
```

-	Layers:
	-	`sha256:bff50073476f6c4da9e4175358cc89840d9f093a6f6a7f9dbfdfc64ad352f0b5`  
		Last Modified: Tue, 24 Feb 2026 21:02:48 GMT  
		Size: 3.6 MB (3648318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03a69c40b8d693f6b65ecc2e05aa1668ff7765125928f56102a3771b097e33cd`  
		Last Modified: Tue, 24 Feb 2026 21:02:47 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3`

```console
$ docker pull couchdb@sha256:01204091e6741331df41129e8ef40759d8823c2984138f655e6338cbc4f58b49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.4.3` - linux; amd64

```console
$ docker pull couchdb@sha256:0e4991a742d5565970442c58d716aa28504ca1ada5e37e53b1acbdf79b2e980f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139023018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db5f1922073e9c3c697f66e22b5ff4ea481d930943e24e7fb4dbd1753b528ab`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:20:55 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 24 Feb 2026 19:20:55 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 24 Feb 2026 19:21:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 24 Feb 2026 19:21:03 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 24 Feb 2026 19:21:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:08 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 24 Feb 2026 19:21:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 24 Feb 2026 19:21:22 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 24 Feb 2026 19:21:22 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 24 Feb 2026 19:21:22 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 24 Feb 2026 19:21:22 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Feb 2026 19:21:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:21:22 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:21:22 GMT
VOLUME [/opt/couchdb/data]
# Tue, 24 Feb 2026 19:21:22 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 24 Feb 2026 19:21:22 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a683baf7f8a6c265f389828fd08373642cdef3abede137a2e747c07a2ddd3646`  
		Last Modified: Tue, 24 Feb 2026 19:21:34 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf81c5cd0abaa9b95efb1238d0115073ea7af9a0c052eb1230cb022c10291b00`  
		Last Modified: Tue, 24 Feb 2026 19:21:34 GMT  
		Size: 7.9 MB (7883119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2ddde98185ea8e526dbe7e9dee56e09e278380bbcea64403e3860a75df3385`  
		Last Modified: Tue, 24 Feb 2026 19:21:34 GMT  
		Size: 401.8 KB (401804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f936bc2fd65af0470fb51e4b3e8d58d8e576bd8548c4acc2bdae3406838f082`  
		Last Modified: Tue, 24 Feb 2026 19:21:34 GMT  
		Size: 76.5 KB (76503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04743336f0803fdac5b43449e135fb61edc978bcc467a3f51a4211595ad4191a`  
		Last Modified: Tue, 24 Feb 2026 19:21:35 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68e61b5d4b34c9ed519f9fbfac9e667c9bc73fd1d63ac9e48378a5b6dd9338c`  
		Last Modified: Tue, 24 Feb 2026 19:21:37 GMT  
		Size: 102.4 MB (102419880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd840b9221289c7922c86ea7a89adabf87cea68ae1d0a500169f55722145358`  
		Last Modified: Tue, 24 Feb 2026 19:21:35 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11e050400c21ba703f5698401cc59fdd9c78f7c96454db2b6c8a0dcfb472108`  
		Last Modified: Tue, 24 Feb 2026 19:21:36 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5916a7f5eb1b7c77f78c93c6f02d12282969c65b9e4ee1cc198cf098e12709`  
		Last Modified: Tue, 24 Feb 2026 19:21:36 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2662f0586b3d359b31a0d164df20cce5c8831951852b8d53efe36abf6339b6`  
		Last Modified: Tue, 24 Feb 2026 19:21:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:162731868319f530a4b1b00c5089f7f0395a24a24368a0aa5ce66440cd9fec5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c1a9b5d4365d534be3ce56a49f6f16d3d2cdcc70dc9916b88185e25d6dacd33`

```dockerfile
```

-	Layers:
	-	`sha256:7402abfa944f8ae92f9b87bc0bac2b6a1d76687641b9eff6a40e2fa68ebcc920`  
		Last Modified: Tue, 24 Feb 2026 19:21:34 GMT  
		Size: 4.1 MB (4125395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e6f57df0139d3b85fb554e0021577efa66b3383cbbbe1cbff34e17da5456cc1`  
		Last Modified: Tue, 24 Feb 2026 19:21:34 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:a778be373bfa48e25079f01a884489cd703f5a2f60041900425b76ef4d09756d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138430308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd69c64beee820811587f39871b3d66d946314295f724774ff900d949ae124a6`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:25:49 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 24 Feb 2026 19:25:49 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 24 Feb 2026 19:25:55 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:25:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 24 Feb 2026 19:25:58 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 24 Feb 2026 19:26:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:03 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 24 Feb 2026 19:26:04 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 24 Feb 2026 19:26:17 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 24 Feb 2026 19:26:17 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 24 Feb 2026 19:26:18 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 24 Feb 2026 19:26:18 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Feb 2026 19:26:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:26:18 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:26:18 GMT
VOLUME [/opt/couchdb/data]
# Tue, 24 Feb 2026 19:26:18 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 24 Feb 2026 19:26:18 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b28d2d12bad652a55c58ab7bf4d17670fd6aab9979954aa3884e485d3149af8`  
		Last Modified: Tue, 24 Feb 2026 19:26:31 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3fcc6cddb2755eaa032a78d87b6e1feeda7b1e2a2bb8caf2d8371a1fe9377e`  
		Last Modified: Tue, 24 Feb 2026 19:26:31 GMT  
		Size: 7.7 MB (7692635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72fcb8d72aa88c8fea61ed14aa330c04a2ffb4179404f99dfeee3faa77193e4e`  
		Last Modified: Tue, 24 Feb 2026 19:26:30 GMT  
		Size: 370.5 KB (370523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40efd2a2232b7aa9ef4b46e15e1f66681c8bd92d67a16b0001e517f86d23b22`  
		Last Modified: Tue, 24 Feb 2026 19:26:31 GMT  
		Size: 76.5 KB (76516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078dd7c0bddb561417644e2ba1d49a6350bf80fff84afd4faff1e01b66149671`  
		Last Modified: Tue, 24 Feb 2026 19:26:32 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55631184889826b81cd2e8b606fd4bc04de2be6679e1db088ee80659668969b`  
		Last Modified: Tue, 24 Feb 2026 19:26:39 GMT  
		Size: 102.2 MB (102169108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db4eb7d337ab5afd4d84fbed6f257b45991592ed1369d424f3de86f7085a9f17`  
		Last Modified: Tue, 24 Feb 2026 19:26:33 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8726f9d73eba2cd63901c6d3fb2cf2a60d59554f8f35518655bd46d1f5e312`  
		Last Modified: Tue, 24 Feb 2026 19:26:33 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b807cf16d9797b98d1d8f9c2f2f31999eaf46bbd16c7f782b08fa776f17b60`  
		Last Modified: Tue, 24 Feb 2026 19:26:34 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6f08b4ae8b26be7ea998b896ab6599abc74b582d17cf55027a82dfc0f984b4`  
		Last Modified: Tue, 24 Feb 2026 19:26:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:0845d0af4e2091278dd04147b8f0e95a1543b3bad69759e3a16ff575c4ad3b00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41f855b205c643d0ae89a0b82c5aa869c01c3fc702384bc4def5b6ed3a290b3d`

```dockerfile
```

-	Layers:
	-	`sha256:b5cb499d4bbf287b6640cdebb2b1b76298240ad7d4ba44fc62e55c5c493bb767`  
		Last Modified: Tue, 24 Feb 2026 19:26:31 GMT  
		Size: 4.1 MB (4125664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f04750f39f834bb9ca489ecc291ae657ef44869528bc6dacdc8df8e5f6278fde`  
		Last Modified: Tue, 24 Feb 2026 19:26:30 GMT  
		Size: 31.3 KB (31318 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3` - linux; s390x

```console
$ docker pull couchdb@sha256:a47d16e7e14ba98e63ac796cab261c72f68c96b3f6c3094430ede9e2f63a42f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135801600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd1011a14856c3429db9fb744a49a2566d70094e9db7d1d67f4eff6042ad4179`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 21:00:09 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 24 Feb 2026 21:00:09 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 24 Feb 2026 21:00:24 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:00:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 24 Feb 2026 21:00:29 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 24 Feb 2026 21:00:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:00:51 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 24 Feb 2026 21:00:51 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 24 Feb 2026 21:01:25 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 24 Feb 2026 21:01:25 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 24 Feb 2026 21:01:26 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 24 Feb 2026 21:01:26 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Feb 2026 21:01:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 21:01:27 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 21:01:27 GMT
VOLUME [/opt/couchdb/data]
# Tue, 24 Feb 2026 21:01:27 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 24 Feb 2026 21:01:27 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a340bdf9c7c5ba07c112275cebe27ccde1fa61c7659de0debe073728d819059c`  
		Last Modified: Tue, 24 Feb 2026 21:02:08 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d02088da685a9d9b76e98c5228b8b904660c77c03c2cbdf1ce83922b81eadf6`  
		Last Modified: Tue, 24 Feb 2026 21:02:09 GMT  
		Size: 7.4 MB (7398990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf8644328d48b42c38c7dd84d0d2beb60fc1fb8b84efb6aee0fefba5db05646`  
		Last Modified: Tue, 24 Feb 2026 21:02:08 GMT  
		Size: 372.2 KB (372185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd72e9d17fc8e6e638b6a642c356ea55e2705d491756fb71c166ca597bc7792`  
		Last Modified: Tue, 24 Feb 2026 21:02:08 GMT  
		Size: 76.7 KB (76678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51943d754b5cb7725df1367d50ce6e9e57c2f06152d84be449e646a3cfb1d1f0`  
		Last Modified: Tue, 24 Feb 2026 21:02:09 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412b690160da2671bc7c123437535fb6e6048babbaec4a9825fe3a5b875b0f17`  
		Last Modified: Tue, 24 Feb 2026 21:02:12 GMT  
		Size: 101.1 MB (101056780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e9c499db2dada13189d46f57e60700ff5f64a1c4e23c3547207585f86b3a51`  
		Last Modified: Tue, 24 Feb 2026 21:02:10 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50772484603279fe83f59102b79ede21c1fcb6e492ba192cf996ccc4f73bc263`  
		Last Modified: Tue, 24 Feb 2026 21:02:10 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfda85c39641c6570f2de3a92678394e3c3c67c94798f4537819b7c6bf25f22`  
		Last Modified: Tue, 24 Feb 2026 21:02:11 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f42fc6ec048ef3563ed295ed8d1d21cff8f6712d3812e82263fb524515a4a11`  
		Last Modified: Tue, 24 Feb 2026 21:02:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:cb194641b2ea2865a51b18429ec630227618b275df006d480cf1a325d64e0173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49de05c81b3a96406ec3411d6b2c0dee49a32e3a90982081724d676ca746058c`

```dockerfile
```

-	Layers:
	-	`sha256:4d7da816c5f606e004b7c4a6b4a201461d005262698c9aea95e821c9d7414297`  
		Last Modified: Tue, 24 Feb 2026 21:02:09 GMT  
		Size: 4.1 MB (4121591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35d514871f4d725c93b9abcff7e8460eb701171f0183773da70bffebff05008e`  
		Last Modified: Tue, 24 Feb 2026 21:02:08 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3-nouveau`

```console
$ docker pull couchdb@sha256:831fde8ccc1a7f3453d1aede5977b9217de16b6f37553cd97d6cfdfc3d3c4c90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.4.3-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:8c0318b75e79ceac04a9ce37e77841e936e94c5b8428dfc0bd8abfeb813b46b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156462150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3948e2913127a9f2cb3c117872a85060d8f6b2ddb873b339a9c060b531da5cd`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:21:16 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 24 Feb 2026 19:21:16 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 24 Feb 2026 19:21:22 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:30 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 24 Feb 2026 19:21:32 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 24 Feb 2026 19:21:36 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:36 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 24 Feb 2026 19:21:41 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 24 Feb 2026 19:21:42 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 24 Feb 2026 19:21:42 GMT
VOLUME [/opt/nouveau/data]
# Tue, 24 Feb 2026 19:21:42 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 24 Feb 2026 19:21:42 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d786beeca1062353bf08793c9c6bf98a0f87418152080a90eb130e1c5965f8f6`  
		Last Modified: Tue, 24 Feb 2026 19:21:56 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1232e4788dea0cdb9581cdbe33ae964be23854c6ba3262d0ddbd70271ab4e2`  
		Last Modified: Tue, 24 Feb 2026 19:21:57 GMT  
		Size: 7.9 MB (7883139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eea41a6714c45b751163a46e19ba3c01f7bf0184a0c6c32392d70120d93c6c1`  
		Last Modified: Tue, 24 Feb 2026 19:21:59 GMT  
		Size: 77.4 MB (77380971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753887b2408fbeb9f6e042ae2842c33652b5abb9e3013b5363364437ce55c044`  
		Last Modified: Tue, 24 Feb 2026 19:21:57 GMT  
		Size: 424.2 KB (424172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cd36223fc5a9085843fc83719ee93222c5b7f3015b8ee042cee0703195d7f0`  
		Last Modified: Tue, 24 Feb 2026 19:21:58 GMT  
		Size: 99.6 KB (99593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5348cedb545b737771245e0a3142aa524f3fe83c031fa5eadd381397bad709`  
		Last Modified: Tue, 24 Feb 2026 19:21:58 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b4f78934567782c3933e2b1a7d1ce3edcbca0ca48ab4370e68d40093c69153`  
		Last Modified: Tue, 24 Feb 2026 19:22:00 GMT  
		Size: 42.4 MB (42436113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c427adfba75e7b9583fa82531baddd53a52b748e5f60413d0ee35c918d40aeb`  
		Last Modified: Tue, 24 Feb 2026 19:21:59 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:17d3bec69aaa0db494c3d4ad21edff4ebbe1ddab435ba4c4526899e8e594be19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3c2a142840d43535e346bf332a82a4059b8527c2125b78da8ed5ce0fd5d35e`

```dockerfile
```

-	Layers:
	-	`sha256:621df8e47d1bbb28b609baa47b5cc9b17e874d76b2a9d92984e5f6d664bfa6f5`  
		Last Modified: Tue, 24 Feb 2026 19:21:57 GMT  
		Size: 3.7 MB (3657789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ed5c79902c3cd66725094e87a5d7f5a79ba31fea78cf2d8d0bc858fce945252`  
		Last Modified: Tue, 24 Feb 2026 19:21:56 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:c8760aedf9f3ca7fab4054a45bb0f06306c809fee4ba265e665577cf4d954bd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155341123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6baa571ae1462fde33e464b5cce727354362bccf2aa3027736ec8453b73aaf9`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:25:50 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 24 Feb 2026 19:25:50 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 24 Feb 2026 19:25:56 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:03 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 24 Feb 2026 19:26:06 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 24 Feb 2026 19:26:10 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:10 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 24 Feb 2026 19:26:15 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 24 Feb 2026 19:26:15 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 24 Feb 2026 19:26:15 GMT
VOLUME [/opt/nouveau/data]
# Tue, 24 Feb 2026 19:26:15 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 24 Feb 2026 19:26:15 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227e384de6cd851ba010ab55fd097b78f1455d789ec6571ff85551fe42c66592`  
		Last Modified: Tue, 24 Feb 2026 19:26:30 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e143170d7088ef52275cb83ede528717dded1fc89ef30e180341730440de118c`  
		Last Modified: Tue, 24 Feb 2026 19:26:31 GMT  
		Size: 7.7 MB (7692654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1921aece143404191b4e7b6ef3569c019b94f4a537ffe73c19906522cdd30c7b`  
		Last Modified: Tue, 24 Feb 2026 19:26:32 GMT  
		Size: 76.7 MB (76700067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea535af4a8896de3981cb593bec663699183279d1c0f2790b4455fc640fcdb2a`  
		Last Modified: Tue, 24 Feb 2026 19:26:30 GMT  
		Size: 392.8 KB (392760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99983fa952bf9c5cfad5ba086d94005dcfad9533e710c9d47a7e88a76c22457e`  
		Last Modified: Tue, 24 Feb 2026 19:26:31 GMT  
		Size: 99.5 KB (99523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46cff693433aa6f3215ca4304ce1ade00c5d146c69122cf17511458ec2559125`  
		Last Modified: Tue, 24 Feb 2026 19:26:32 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216191418b7524c42e28d13c007476075fbceaaa80b42071b4f6aded28efdd8c`  
		Last Modified: Tue, 24 Feb 2026 19:26:33 GMT  
		Size: 42.3 MB (42338155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab33c06eabaf323ab625c8d9b524e0b98da7c63ecb4a9425b7e446d908cf4cf`  
		Last Modified: Tue, 24 Feb 2026 19:26:33 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:56d92e6171fbd62abcc2d5086396e0628196d68e7c46047584569a7332c13ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3680838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c511b3dfcb4f84381c6ab3ac001fef2818aa7e0a7508cf107fe2bb32e6b2494`

```dockerfile
```

-	Layers:
	-	`sha256:4727687559b55ce121ddb0d368b0a858849fa69077bae7ed7a3f5ef841e051ee`  
		Last Modified: Tue, 24 Feb 2026 19:26:30 GMT  
		Size: 3.7 MB (3656453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da11af15d871d64e39437bbe4310cc9d0872021fcd10afcd219d0de6a0450c20`  
		Last Modified: Tue, 24 Feb 2026 19:26:30 GMT  
		Size: 24.4 KB (24385 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:9c05b18dff0cf00441a9d9e3d8b681f5e3e9507c98bed2235a0370520a772f7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150103941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8773f2908b035ba7b5e0196a3b08c9eb7ef58464769a75a5b9deaaab730021`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 21:00:37 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 24 Feb 2026 21:00:37 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 24 Feb 2026 21:01:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:01:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:01:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 24 Feb 2026 21:01:33 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 24 Feb 2026 21:01:49 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:01:51 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 24 Feb 2026 21:02:14 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 24 Feb 2026 21:02:15 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 24 Feb 2026 21:02:15 GMT
VOLUME [/opt/nouveau/data]
# Tue, 24 Feb 2026 21:02:15 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 24 Feb 2026 21:02:15 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1f3fec8b48066b20be403a988ba842f0d420ac3eefffa49d99bb38555aa745`  
		Last Modified: Tue, 24 Feb 2026 21:02:47 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d3c2e86b6018b10bac3442abddc96c7d49b6d15c2321f47a75cb25356a6ff4`  
		Last Modified: Tue, 24 Feb 2026 21:02:48 GMT  
		Size: 7.4 MB (7399151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9dbc3ec363bde23293f059da65cff7972bd5f84a3a6e016f8be1c7f3895e0d5`  
		Last Modified: Tue, 24 Feb 2026 21:02:50 GMT  
		Size: 73.2 MB (73153462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75c677841d683f6911c3e01b7cc4c0144a01135bd9ef330d8ccf949cb561c49`  
		Last Modified: Tue, 24 Feb 2026 21:02:47 GMT  
		Size: 394.6 KB (394627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9905a105efb9f40c8b4b01994eb3f53b91c7d5e53c337bdf2f5ce0b01408afc1`  
		Last Modified: Tue, 24 Feb 2026 21:02:49 GMT  
		Size: 99.8 KB (99850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a14c1303bf766d3c1b07ca076074648c21be156b33e58890bd477c71d205d0`  
		Last Modified: Tue, 24 Feb 2026 21:02:49 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3671e6a5c6dc3e5c0c2c4647d27b605e77b7598d12c4e440076f9b55c5b5348`  
		Last Modified: Tue, 24 Feb 2026 21:02:50 GMT  
		Size: 42.2 MB (42163440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13611bc3d7c364e9358bdfa09574d1d17228c97d6c328f062c83b4a9b5d516f7`  
		Last Modified: Tue, 24 Feb 2026 21:02:50 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:d9d82bb35155ed46a6b002c86ce7e2e3519931065eb21d9dd845335a0fc13b99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3672533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d19a97fa8445d03eba812dfea1542179c91a0938f88979ea19a9b7e699b26f2`

```dockerfile
```

-	Layers:
	-	`sha256:bff50073476f6c4da9e4175358cc89840d9f093a6f6a7f9dbfdfc64ad352f0b5`  
		Last Modified: Tue, 24 Feb 2026 21:02:48 GMT  
		Size: 3.6 MB (3648318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03a69c40b8d693f6b65ecc2e05aa1668ff7765125928f56102a3771b097e33cd`  
		Last Modified: Tue, 24 Feb 2026 21:02:47 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5`

```console
$ docker pull couchdb@sha256:d55f35ffc020ca4c615fccfddd4f893d11f957593b12b33fce5e7b0840366ccd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.5` - linux; amd64

```console
$ docker pull couchdb@sha256:41766fcef3c3ab64a2b6d36560f237b23df3d29cea7c5c9d945f29d83896ac06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142059668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71979498d495be6e72756259eff755a726b88dd825408be29fb3aba1b5240175`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:20:54 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 24 Feb 2026 19:20:54 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 24 Feb 2026 19:21:00 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 24 Feb 2026 19:21:02 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 24 Feb 2026 19:21:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:07 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 24 Feb 2026 19:21:07 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 24 Feb 2026 19:21:21 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 24 Feb 2026 19:21:21 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 24 Feb 2026 19:21:21 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 24 Feb 2026 19:21:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Feb 2026 19:21:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:21:21 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:21:21 GMT
VOLUME [/opt/couchdb/data]
# Tue, 24 Feb 2026 19:21:21 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 24 Feb 2026 19:21:21 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7d73966d9314fcd3d72b1b0595152eb892287a887426b08e9811b94ae2b379`  
		Last Modified: Tue, 24 Feb 2026 19:21:34 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b3b202dd2e4a1bbf752929191ebe478db7474b2b54bf6748156e639d1336c6`  
		Last Modified: Tue, 24 Feb 2026 19:21:34 GMT  
		Size: 7.9 MB (7883121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7271a9298cc81eb015423fe434ed96701a704ee22755593dc7ab377c3d833050`  
		Last Modified: Tue, 24 Feb 2026 19:21:34 GMT  
		Size: 401.8 KB (401802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788dcc4a23034e7f3d98e0c1208b1d84d892332d87774695962802b0bc3c0ba4`  
		Last Modified: Tue, 24 Feb 2026 19:21:34 GMT  
		Size: 76.5 KB (76508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a61888d031364c28d8b161262599c1af189256403e0753623d967a543e66fc2`  
		Last Modified: Tue, 24 Feb 2026 19:21:35 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f591ba27f1c6cb2b55ff86d593c814940f7cfec9027f144771ca1abb4f1484d`  
		Last Modified: Tue, 24 Feb 2026 19:21:37 GMT  
		Size: 105.5 MB (105456525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296ca6c03411e008479fc5f485ead2445d1c10e83542a0f803f26e693f8c990f`  
		Last Modified: Tue, 24 Feb 2026 19:21:35 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269188377ea3f7d37af3b7885f565f7d389edb04de18151f2a6912e78d9636de`  
		Last Modified: Tue, 24 Feb 2026 19:21:35 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1361f09b26e9d82d4283c4bebe3697cce16e5c358fb2e5b0d7d307bc6b62ec15`  
		Last Modified: Tue, 24 Feb 2026 19:21:36 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a75cb6d22638fcb69fb3d276b158b220964f410718633d00c472bbf795fc0e1`  
		Last Modified: Tue, 24 Feb 2026 19:21:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:6538ab89712240a307f4f3cc91b72512adcc89143967f8bbe4ad622d85ed6e0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99925e22ce7d2cb43c93f63b1e6827c2f235c3e9808a820d7d95820deb5fe769`

```dockerfile
```

-	Layers:
	-	`sha256:2d6482430b6b5635652a50047b4489bb7944b7974c056abc260ef4fdeff9687a`  
		Last Modified: Tue, 24 Feb 2026 19:21:34 GMT  
		Size: 4.2 MB (4184421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fa746e2a5678a43070ce809bd32b3918490c0cfa6c206f7f768bd208f1da7de`  
		Last Modified: Tue, 24 Feb 2026 19:21:34 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:770dce57c3d96e16be18d9c33673657a065bc5cf0b72ddd4a469de4ce0e28339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141419192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f29a3517318bc3af48f6be7a479b9ba60373ac6af58d062f5b3a967d7f63d2a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:25:24 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 24 Feb 2026 19:25:24 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 24 Feb 2026 19:25:30 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:25:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 24 Feb 2026 19:25:33 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 24 Feb 2026 19:25:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:25:37 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 24 Feb 2026 19:25:37 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 24 Feb 2026 19:25:51 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 24 Feb 2026 19:25:51 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 24 Feb 2026 19:25:52 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 24 Feb 2026 19:25:52 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Feb 2026 19:25:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:25:52 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:25:52 GMT
VOLUME [/opt/couchdb/data]
# Tue, 24 Feb 2026 19:25:52 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 24 Feb 2026 19:25:52 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5195943c8bc81ff3ccacc7d15e0222f0ddc0a363f1da17509b63e4dd41b2299f`  
		Last Modified: Tue, 24 Feb 2026 19:26:05 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbba4689c9413d25ec04c6c788241c6a8ab4ca2ee82346c96241d886dd4588b`  
		Last Modified: Tue, 24 Feb 2026 19:26:05 GMT  
		Size: 7.7 MB (7692638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3981bae95c2cf4b56a60963485420ec03af0c4467a5c204fc9de44bbfaa076c5`  
		Last Modified: Tue, 24 Feb 2026 19:26:05 GMT  
		Size: 370.5 KB (370543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0780dc8172b862928867ea7afe0354b30bfee9ddd9500fcd0ee128ec7db63069`  
		Last Modified: Tue, 24 Feb 2026 19:26:05 GMT  
		Size: 76.5 KB (76468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada3951d847dd448afd38f10999ea754f9d96abd69c5e876ea8eb8e0708cda8c`  
		Last Modified: Tue, 24 Feb 2026 19:26:06 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081dd262f305fc888779fda5162e7ef14b3dd157bda32f9adfe0c71e3c53b9f3`  
		Last Modified: Tue, 24 Feb 2026 19:26:08 GMT  
		Size: 105.2 MB (105158034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae02b6144e60ba0617faf2dabd56adf4ae0b8ca4696cec8383550db4ccfeb03a`  
		Last Modified: Tue, 24 Feb 2026 19:26:06 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349350c52f60a43ac4b9153a28573e1ed7c6230729482261de86e4eec142f621`  
		Last Modified: Tue, 24 Feb 2026 19:26:06 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d040afc70746c77854a2e80fbac73e1f602fbf8ac82fecebc968cef9598cf9`  
		Last Modified: Tue, 24 Feb 2026 19:26:07 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aaa06830632dd23874fc9a34e260c5027305c63c186b36c7cf19232e3c3e9c9`  
		Last Modified: Tue, 24 Feb 2026 19:26:07 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:8e105bac4709d132c2132b3c176eec75158d671f9088324761cffbc47aff3602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa658a9c5ab56fe8f6fd623762676a48f4c87358be034ae7fecbbf3b1500921`

```dockerfile
```

-	Layers:
	-	`sha256:3a05677e5b72845cdfc530571ac1a2ef5046321baf165d46020942e6fd7d4ca9`  
		Last Modified: Tue, 24 Feb 2026 19:26:05 GMT  
		Size: 4.2 MB (4184714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57719038c77b024cd456dcee02cf0aa52f7a7b967dc3a6056213dbffc43702c5`  
		Last Modified: Tue, 24 Feb 2026 19:26:05 GMT  
		Size: 31.9 KB (31932 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5` - linux; s390x

```console
$ docker pull couchdb@sha256:b37585c645221c6f47e1720d73d41e2913dd4c5d9da1325227b92148e3f00c53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138773629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9ccda5442365d739afa4c52c7891f387b7a41f8159f6d886b58c68ab7da04b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:58:41 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 24 Feb 2026 20:58:41 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 24 Feb 2026 20:59:11 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:59:16 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 24 Feb 2026 20:59:16 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 24 Feb 2026 20:59:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:59:33 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 24 Feb 2026 20:59:34 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 24 Feb 2026 21:00:16 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 24 Feb 2026 21:00:17 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 24 Feb 2026 21:00:17 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 24 Feb 2026 21:00:18 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Feb 2026 21:00:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 21:00:18 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 21:00:18 GMT
VOLUME [/opt/couchdb/data]
# Tue, 24 Feb 2026 21:00:18 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 24 Feb 2026 21:00:18 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1eeb0a30f79824913befe6cff540b6bbef64ce01bcd01d02353436b346f1c52`  
		Last Modified: Tue, 24 Feb 2026 21:01:18 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed832851f69da334438fcc233f300fb11f53288452d86a31700195783d07b7b`  
		Last Modified: Tue, 24 Feb 2026 21:01:23 GMT  
		Size: 7.4 MB (7399099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283498defbfbbe68c63defadeb6bd597efc21eeae2245bd6ef3a48b45792b2eb`  
		Last Modified: Tue, 24 Feb 2026 21:01:17 GMT  
		Size: 372.2 KB (372246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e76b77d775634501854d45ab3d68cf569581ce20c532eb424e4b24916cc697`  
		Last Modified: Tue, 24 Feb 2026 21:01:18 GMT  
		Size: 76.7 KB (76745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7caefca7f93130ff023ae08185691df23526132092c2d1c0f6abbe4953830c`  
		Last Modified: Tue, 24 Feb 2026 21:01:21 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9967421ea9282f965997b6135e3475d745fa5dbf3779675c500ca2da629a6879`  
		Last Modified: Tue, 24 Feb 2026 21:01:24 GMT  
		Size: 104.0 MB (104028576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185c2f75ff7c0754709bd9b4d1960fa9befe3e99a1740f14b2a362a4e8f893e4`  
		Last Modified: Tue, 24 Feb 2026 21:01:19 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75895523cafbc3bf7cc90bcd1beb3eb6446ff705134466fc56c3d3dd5f46b12`  
		Last Modified: Tue, 24 Feb 2026 21:01:21 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c9910bd6a90ab78f2a16acf8792a2f83e235d516f41e2e74a5b64df59d78f0`  
		Last Modified: Tue, 24 Feb 2026 21:01:22 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46ae2bc44dafb76079ab9db1dd230550789fad97c3b93aef7bbbd770298056c`  
		Last Modified: Tue, 24 Feb 2026 21:01:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:b6a18a48d50c63a224991d5e294fc51a4096f16c8d0cc7533d18e8af2c00b9d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35047fcb81ed162b1e68c86ff7087b1eab1a17c69fa0b371b511f7912315824`

```dockerfile
```

-	Layers:
	-	`sha256:ebf92ddcfc83a696b60fc5a62ee38340c62d83b965fcfc2fa6abad4a5217e495`  
		Last Modified: Tue, 24 Feb 2026 21:01:18 GMT  
		Size: 4.2 MB (4180617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f74ac14845fdc83f326ed34daccc3fda4c7d18d05582eaccd9dfc0e2891e4325`  
		Last Modified: Tue, 24 Feb 2026 21:01:17 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5-nouveau`

```console
$ docker pull couchdb@sha256:ad299a7562b39c51224020dc60f1f909fb0ff1042493b77f12b54d202831b5ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.5-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:63028f38a14c746b6610482b292f2b70386fb8420371d81e899dc171bf9e1cac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156462375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8f868f8ae52c99fd9de628425892e417ef6c3e09a08bbb4f7ace5d1e8da629`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:21:02 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 24 Feb 2026 19:21:02 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 24 Feb 2026 19:21:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:15 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 24 Feb 2026 19:21:18 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 24 Feb 2026 19:21:21 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:22 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 24 Feb 2026 19:21:28 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 24 Feb 2026 19:21:28 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 24 Feb 2026 19:21:28 GMT
VOLUME [/opt/nouveau/data]
# Tue, 24 Feb 2026 19:21:28 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 24 Feb 2026 19:21:28 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ddecf20ba5b4b57590d3302037e328fd1e5b649ada9afe1077b1527b57ea1d`  
		Last Modified: Tue, 24 Feb 2026 19:21:43 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f050c4933d55a438411503b72e2599a05933423782db3fdbe74c1169b1eb9f79`  
		Last Modified: Tue, 24 Feb 2026 19:21:44 GMT  
		Size: 7.9 MB (7883160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8766f1911d4db3708ea04e17aec8ef20c715fe46f8fa163ca3ce5fb7da96c0`  
		Last Modified: Tue, 24 Feb 2026 19:21:45 GMT  
		Size: 77.4 MB (77380921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27505ffdad9b3b9ee1faf0425665128cde5fa3d92e437985492bfcfd48c3daaf`  
		Last Modified: Tue, 24 Feb 2026 19:21:43 GMT  
		Size: 424.2 KB (424151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775b0f7b272fa1afd4e729b58d254862b055044b412ad10d149e941a5160a8bd`  
		Last Modified: Tue, 24 Feb 2026 19:21:45 GMT  
		Size: 99.6 KB (99567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103c9a7e496556a022a3693afb975edd7f5d2c030589b6507aeb0e875bc63784`  
		Last Modified: Tue, 24 Feb 2026 19:21:45 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43708c9e9bf3275d81d21f997991dd95b3fcb1d8b3d913c4998f716ede5eaa63`  
		Last Modified: Tue, 24 Feb 2026 19:21:46 GMT  
		Size: 42.4 MB (42436414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9309990c5553a8aba351cd8e6cef3b1e0bf7d4b6cd2018e8ee26b2ee680f18`  
		Last Modified: Tue, 24 Feb 2026 19:21:46 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:88a4a1b5d2bf9af1822defa276f9543e062d8f7cd349c08cecbcde70094878cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631682cf89179999d5b185f059802920a43a7d4e464fbcc862160c18e843f455`

```dockerfile
```

-	Layers:
	-	`sha256:499345d0a7a481daaffbb8965f4762e8dfe41f4174953070f2f2a757872028a2`  
		Last Modified: Tue, 24 Feb 2026 19:21:43 GMT  
		Size: 3.7 MB (3658095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00348bba47c2e9b12086a11819274c277f12e27cc217565f02b5ee77e41e7dff`  
		Last Modified: Tue, 24 Feb 2026 19:21:43 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:90300ee575847a78a0ac8469e4ca439296ff76a18037c079b043ef1240a2fc4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155342048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095919028295ae8e9811d72082cd88abe6ce7a7b9fdd493ea45257a426a9fa90`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:25:45 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 24 Feb 2026 19:25:45 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 24 Feb 2026 19:25:51 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:25:58 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 24 Feb 2026 19:26:01 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 24 Feb 2026 19:26:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 24 Feb 2026 19:26:11 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 24 Feb 2026 19:26:12 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 24 Feb 2026 19:26:12 GMT
VOLUME [/opt/nouveau/data]
# Tue, 24 Feb 2026 19:26:12 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 24 Feb 2026 19:26:12 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e26c0f056669b165a8ae59eaff14387edf0f261e8b450067813093d83930c73`  
		Last Modified: Tue, 24 Feb 2026 19:26:26 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9820074d8ac8dcf46e3efdf9679ade22002a185cc39b3f7578826f640e83587`  
		Last Modified: Tue, 24 Feb 2026 19:26:27 GMT  
		Size: 7.7 MB (7692622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e888a3c3c9fa56a143880febc9d826e8bec60a6a09ce8f2f1bfa5ac7c2dc29f1`  
		Last Modified: Tue, 24 Feb 2026 19:26:28 GMT  
		Size: 76.7 MB (76700050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56721790700ad6a8decec8f7e7c2da18ad1c9b0708cc502a05a49e174ce46d06`  
		Last Modified: Tue, 24 Feb 2026 19:26:26 GMT  
		Size: 392.8 KB (392770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e29871ea620339c69ce3817fc2d93fa827c472742ac3f984d6798318379448`  
		Last Modified: Tue, 24 Feb 2026 19:26:27 GMT  
		Size: 99.5 KB (99520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6e3773a84b9dae8befc65af5e5a3e970f192593d2e36b0b1836abc3a018724`  
		Last Modified: Tue, 24 Feb 2026 19:26:28 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb2b450c1ba8c12a3548ef9746da587ae85038952093ec2c15072768da58330`  
		Last Modified: Tue, 24 Feb 2026 19:26:29 GMT  
		Size: 42.3 MB (42339126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbeb35bc414ae41b2b4da730a59d4ee5a8181e35a4e3b83842f742121b99993`  
		Last Modified: Tue, 24 Feb 2026 19:26:29 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:6a6fb2fe398fca430e75696ef76cdf08024df46c6feeed01e317aa99233671e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa2f6ebf52b151e48808601cae4de7825d0f252285de645a9cb4dd9b86a46b2`

```dockerfile
```

-	Layers:
	-	`sha256:dcfc735a1fabe515dca1c188ca05762d93b1db9e33112021574819b5d4742ef7`  
		Last Modified: Tue, 24 Feb 2026 19:26:26 GMT  
		Size: 3.7 MB (3656771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ca8f03f33a2591f16bea1316bd8899b382a7710144eb8162622e7584d3a39a3`  
		Last Modified: Tue, 24 Feb 2026 19:26:26 GMT  
		Size: 24.7 KB (24703 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:2e4472b408c0333e2977f33a8bfb7d510f88cb1aab0a7988af6739167e6e1eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150105815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7852f3425b90f93b2dc01b1e9f55e19fdd6b31db61e5e4b360ac68079cb5f896`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:58:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 24 Feb 2026 20:58:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 24 Feb 2026 20:59:11 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:59:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:59:41 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 24 Feb 2026 20:59:41 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 24 Feb 2026 21:00:02 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:00:03 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 24 Feb 2026 21:00:22 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 24 Feb 2026 21:00:24 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 24 Feb 2026 21:00:24 GMT
VOLUME [/opt/nouveau/data]
# Tue, 24 Feb 2026 21:00:24 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 24 Feb 2026 21:00:24 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a950e14c7d88cf86c9d9f9f5d81eb0a6b66998ba15461f24cf32c54767ad382`  
		Last Modified: Tue, 24 Feb 2026 21:01:23 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ad91eaeb8b4d910bab5880a0168f86b9d9ccd494cc0e2c363abef9ed6361d5`  
		Last Modified: Tue, 24 Feb 2026 21:01:23 GMT  
		Size: 7.4 MB (7399125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ecc468cc57fa7504bc399c879bbdeeababdcf31c418cdd66c4c5078deded16`  
		Last Modified: Tue, 24 Feb 2026 21:01:25 GMT  
		Size: 73.2 MB (73153712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28c50c2f86346560509995780e524a097a56cc46e1be1ff10e6d9b7215617df`  
		Last Modified: Tue, 24 Feb 2026 21:01:23 GMT  
		Size: 394.6 KB (394634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f944fabb2ccbde3fd8f7bae3e9dfcc47f3404a64b0155a38b80bf162ccced73`  
		Last Modified: Tue, 24 Feb 2026 21:01:24 GMT  
		Size: 99.9 KB (99898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcc8fc571c26bb731d288c5f2e27c40b126abe67e58f979bd6ae46e51befb76`  
		Last Modified: Tue, 24 Feb 2026 21:01:24 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385829014d2303d4b21b8b070f89c2ef8a306df85e8c3e8d0e85a8883c4c2217`  
		Last Modified: Tue, 24 Feb 2026 21:01:25 GMT  
		Size: 42.2 MB (42165035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08a99fb7b0c3348916dd13728c92af578510c3769cb53f3b5f6d7d9daa58ee73`  
		Last Modified: Tue, 24 Feb 2026 21:01:25 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:6668e725b2c526b9c98685853b218fabcfe534c0bbe372c9c52d62958868c2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0f3fa400a6f7d0917b3d1feb53fa0f8a6f92f09779bae79f9861bed5f1a30b`

```dockerfile
```

-	Layers:
	-	`sha256:33647360be3076acd9276e12e6453e64a05fe294f1152df02bd81def6ae34b86`  
		Last Modified: Tue, 24 Feb 2026 21:01:23 GMT  
		Size: 3.6 MB (3648624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2786da3d1f564b542091d726336018be02ead528326f1772e60c8a37807fd671`  
		Last Modified: Tue, 24 Feb 2026 21:01:22 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.1`

```console
$ docker pull couchdb@sha256:d55f35ffc020ca4c615fccfddd4f893d11f957593b12b33fce5e7b0840366ccd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.5.1` - linux; amd64

```console
$ docker pull couchdb@sha256:41766fcef3c3ab64a2b6d36560f237b23df3d29cea7c5c9d945f29d83896ac06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142059668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71979498d495be6e72756259eff755a726b88dd825408be29fb3aba1b5240175`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:20:54 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 24 Feb 2026 19:20:54 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 24 Feb 2026 19:21:00 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 24 Feb 2026 19:21:02 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 24 Feb 2026 19:21:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:07 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 24 Feb 2026 19:21:07 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 24 Feb 2026 19:21:21 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 24 Feb 2026 19:21:21 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 24 Feb 2026 19:21:21 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 24 Feb 2026 19:21:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Feb 2026 19:21:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:21:21 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:21:21 GMT
VOLUME [/opt/couchdb/data]
# Tue, 24 Feb 2026 19:21:21 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 24 Feb 2026 19:21:21 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7d73966d9314fcd3d72b1b0595152eb892287a887426b08e9811b94ae2b379`  
		Last Modified: Tue, 24 Feb 2026 19:21:34 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b3b202dd2e4a1bbf752929191ebe478db7474b2b54bf6748156e639d1336c6`  
		Last Modified: Tue, 24 Feb 2026 19:21:34 GMT  
		Size: 7.9 MB (7883121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7271a9298cc81eb015423fe434ed96701a704ee22755593dc7ab377c3d833050`  
		Last Modified: Tue, 24 Feb 2026 19:21:34 GMT  
		Size: 401.8 KB (401802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788dcc4a23034e7f3d98e0c1208b1d84d892332d87774695962802b0bc3c0ba4`  
		Last Modified: Tue, 24 Feb 2026 19:21:34 GMT  
		Size: 76.5 KB (76508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a61888d031364c28d8b161262599c1af189256403e0753623d967a543e66fc2`  
		Last Modified: Tue, 24 Feb 2026 19:21:35 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f591ba27f1c6cb2b55ff86d593c814940f7cfec9027f144771ca1abb4f1484d`  
		Last Modified: Tue, 24 Feb 2026 19:21:37 GMT  
		Size: 105.5 MB (105456525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296ca6c03411e008479fc5f485ead2445d1c10e83542a0f803f26e693f8c990f`  
		Last Modified: Tue, 24 Feb 2026 19:21:35 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269188377ea3f7d37af3b7885f565f7d389edb04de18151f2a6912e78d9636de`  
		Last Modified: Tue, 24 Feb 2026 19:21:35 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1361f09b26e9d82d4283c4bebe3697cce16e5c358fb2e5b0d7d307bc6b62ec15`  
		Last Modified: Tue, 24 Feb 2026 19:21:36 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a75cb6d22638fcb69fb3d276b158b220964f410718633d00c472bbf795fc0e1`  
		Last Modified: Tue, 24 Feb 2026 19:21:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:6538ab89712240a307f4f3cc91b72512adcc89143967f8bbe4ad622d85ed6e0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99925e22ce7d2cb43c93f63b1e6827c2f235c3e9808a820d7d95820deb5fe769`

```dockerfile
```

-	Layers:
	-	`sha256:2d6482430b6b5635652a50047b4489bb7944b7974c056abc260ef4fdeff9687a`  
		Last Modified: Tue, 24 Feb 2026 19:21:34 GMT  
		Size: 4.2 MB (4184421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fa746e2a5678a43070ce809bd32b3918490c0cfa6c206f7f768bd208f1da7de`  
		Last Modified: Tue, 24 Feb 2026 19:21:34 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:770dce57c3d96e16be18d9c33673657a065bc5cf0b72ddd4a469de4ce0e28339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141419192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f29a3517318bc3af48f6be7a479b9ba60373ac6af58d062f5b3a967d7f63d2a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:25:24 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 24 Feb 2026 19:25:24 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 24 Feb 2026 19:25:30 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:25:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 24 Feb 2026 19:25:33 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 24 Feb 2026 19:25:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:25:37 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 24 Feb 2026 19:25:37 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 24 Feb 2026 19:25:51 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 24 Feb 2026 19:25:51 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 24 Feb 2026 19:25:52 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 24 Feb 2026 19:25:52 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Feb 2026 19:25:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:25:52 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:25:52 GMT
VOLUME [/opt/couchdb/data]
# Tue, 24 Feb 2026 19:25:52 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 24 Feb 2026 19:25:52 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5195943c8bc81ff3ccacc7d15e0222f0ddc0a363f1da17509b63e4dd41b2299f`  
		Last Modified: Tue, 24 Feb 2026 19:26:05 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbba4689c9413d25ec04c6c788241c6a8ab4ca2ee82346c96241d886dd4588b`  
		Last Modified: Tue, 24 Feb 2026 19:26:05 GMT  
		Size: 7.7 MB (7692638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3981bae95c2cf4b56a60963485420ec03af0c4467a5c204fc9de44bbfaa076c5`  
		Last Modified: Tue, 24 Feb 2026 19:26:05 GMT  
		Size: 370.5 KB (370543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0780dc8172b862928867ea7afe0354b30bfee9ddd9500fcd0ee128ec7db63069`  
		Last Modified: Tue, 24 Feb 2026 19:26:05 GMT  
		Size: 76.5 KB (76468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada3951d847dd448afd38f10999ea754f9d96abd69c5e876ea8eb8e0708cda8c`  
		Last Modified: Tue, 24 Feb 2026 19:26:06 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081dd262f305fc888779fda5162e7ef14b3dd157bda32f9adfe0c71e3c53b9f3`  
		Last Modified: Tue, 24 Feb 2026 19:26:08 GMT  
		Size: 105.2 MB (105158034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae02b6144e60ba0617faf2dabd56adf4ae0b8ca4696cec8383550db4ccfeb03a`  
		Last Modified: Tue, 24 Feb 2026 19:26:06 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349350c52f60a43ac4b9153a28573e1ed7c6230729482261de86e4eec142f621`  
		Last Modified: Tue, 24 Feb 2026 19:26:06 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d040afc70746c77854a2e80fbac73e1f602fbf8ac82fecebc968cef9598cf9`  
		Last Modified: Tue, 24 Feb 2026 19:26:07 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aaa06830632dd23874fc9a34e260c5027305c63c186b36c7cf19232e3c3e9c9`  
		Last Modified: Tue, 24 Feb 2026 19:26:07 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:8e105bac4709d132c2132b3c176eec75158d671f9088324761cffbc47aff3602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa658a9c5ab56fe8f6fd623762676a48f4c87358be034ae7fecbbf3b1500921`

```dockerfile
```

-	Layers:
	-	`sha256:3a05677e5b72845cdfc530571ac1a2ef5046321baf165d46020942e6fd7d4ca9`  
		Last Modified: Tue, 24 Feb 2026 19:26:05 GMT  
		Size: 4.2 MB (4184714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57719038c77b024cd456dcee02cf0aa52f7a7b967dc3a6056213dbffc43702c5`  
		Last Modified: Tue, 24 Feb 2026 19:26:05 GMT  
		Size: 31.9 KB (31932 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.1` - linux; s390x

```console
$ docker pull couchdb@sha256:b37585c645221c6f47e1720d73d41e2913dd4c5d9da1325227b92148e3f00c53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138773629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9ccda5442365d739afa4c52c7891f387b7a41f8159f6d886b58c68ab7da04b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:58:41 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 24 Feb 2026 20:58:41 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 24 Feb 2026 20:59:11 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:59:16 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 24 Feb 2026 20:59:16 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 24 Feb 2026 20:59:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:59:33 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 24 Feb 2026 20:59:34 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 24 Feb 2026 21:00:16 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 24 Feb 2026 21:00:17 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 24 Feb 2026 21:00:17 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 24 Feb 2026 21:00:18 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Feb 2026 21:00:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 21:00:18 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 21:00:18 GMT
VOLUME [/opt/couchdb/data]
# Tue, 24 Feb 2026 21:00:18 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 24 Feb 2026 21:00:18 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1eeb0a30f79824913befe6cff540b6bbef64ce01bcd01d02353436b346f1c52`  
		Last Modified: Tue, 24 Feb 2026 21:01:18 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed832851f69da334438fcc233f300fb11f53288452d86a31700195783d07b7b`  
		Last Modified: Tue, 24 Feb 2026 21:01:23 GMT  
		Size: 7.4 MB (7399099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283498defbfbbe68c63defadeb6bd597efc21eeae2245bd6ef3a48b45792b2eb`  
		Last Modified: Tue, 24 Feb 2026 21:01:17 GMT  
		Size: 372.2 KB (372246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e76b77d775634501854d45ab3d68cf569581ce20c532eb424e4b24916cc697`  
		Last Modified: Tue, 24 Feb 2026 21:01:18 GMT  
		Size: 76.7 KB (76745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7caefca7f93130ff023ae08185691df23526132092c2d1c0f6abbe4953830c`  
		Last Modified: Tue, 24 Feb 2026 21:01:21 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9967421ea9282f965997b6135e3475d745fa5dbf3779675c500ca2da629a6879`  
		Last Modified: Tue, 24 Feb 2026 21:01:24 GMT  
		Size: 104.0 MB (104028576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185c2f75ff7c0754709bd9b4d1960fa9befe3e99a1740f14b2a362a4e8f893e4`  
		Last Modified: Tue, 24 Feb 2026 21:01:19 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75895523cafbc3bf7cc90bcd1beb3eb6446ff705134466fc56c3d3dd5f46b12`  
		Last Modified: Tue, 24 Feb 2026 21:01:21 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c9910bd6a90ab78f2a16acf8792a2f83e235d516f41e2e74a5b64df59d78f0`  
		Last Modified: Tue, 24 Feb 2026 21:01:22 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46ae2bc44dafb76079ab9db1dd230550789fad97c3b93aef7bbbd770298056c`  
		Last Modified: Tue, 24 Feb 2026 21:01:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:b6a18a48d50c63a224991d5e294fc51a4096f16c8d0cc7533d18e8af2c00b9d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35047fcb81ed162b1e68c86ff7087b1eab1a17c69fa0b371b511f7912315824`

```dockerfile
```

-	Layers:
	-	`sha256:ebf92ddcfc83a696b60fc5a62ee38340c62d83b965fcfc2fa6abad4a5217e495`  
		Last Modified: Tue, 24 Feb 2026 21:01:18 GMT  
		Size: 4.2 MB (4180617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f74ac14845fdc83f326ed34daccc3fda4c7d18d05582eaccd9dfc0e2891e4325`  
		Last Modified: Tue, 24 Feb 2026 21:01:17 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.1-nouveau`

```console
$ docker pull couchdb@sha256:ad299a7562b39c51224020dc60f1f909fb0ff1042493b77f12b54d202831b5ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.5.1-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:63028f38a14c746b6610482b292f2b70386fb8420371d81e899dc171bf9e1cac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156462375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8f868f8ae52c99fd9de628425892e417ef6c3e09a08bbb4f7ace5d1e8da629`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:21:02 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 24 Feb 2026 19:21:02 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 24 Feb 2026 19:21:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:15 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 24 Feb 2026 19:21:18 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 24 Feb 2026 19:21:21 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:22 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 24 Feb 2026 19:21:28 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 24 Feb 2026 19:21:28 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 24 Feb 2026 19:21:28 GMT
VOLUME [/opt/nouveau/data]
# Tue, 24 Feb 2026 19:21:28 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 24 Feb 2026 19:21:28 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ddecf20ba5b4b57590d3302037e328fd1e5b649ada9afe1077b1527b57ea1d`  
		Last Modified: Tue, 24 Feb 2026 19:21:43 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f050c4933d55a438411503b72e2599a05933423782db3fdbe74c1169b1eb9f79`  
		Last Modified: Tue, 24 Feb 2026 19:21:44 GMT  
		Size: 7.9 MB (7883160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8766f1911d4db3708ea04e17aec8ef20c715fe46f8fa163ca3ce5fb7da96c0`  
		Last Modified: Tue, 24 Feb 2026 19:21:45 GMT  
		Size: 77.4 MB (77380921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27505ffdad9b3b9ee1faf0425665128cde5fa3d92e437985492bfcfd48c3daaf`  
		Last Modified: Tue, 24 Feb 2026 19:21:43 GMT  
		Size: 424.2 KB (424151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775b0f7b272fa1afd4e729b58d254862b055044b412ad10d149e941a5160a8bd`  
		Last Modified: Tue, 24 Feb 2026 19:21:45 GMT  
		Size: 99.6 KB (99567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103c9a7e496556a022a3693afb975edd7f5d2c030589b6507aeb0e875bc63784`  
		Last Modified: Tue, 24 Feb 2026 19:21:45 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43708c9e9bf3275d81d21f997991dd95b3fcb1d8b3d913c4998f716ede5eaa63`  
		Last Modified: Tue, 24 Feb 2026 19:21:46 GMT  
		Size: 42.4 MB (42436414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9309990c5553a8aba351cd8e6cef3b1e0bf7d4b6cd2018e8ee26b2ee680f18`  
		Last Modified: Tue, 24 Feb 2026 19:21:46 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:88a4a1b5d2bf9af1822defa276f9543e062d8f7cd349c08cecbcde70094878cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631682cf89179999d5b185f059802920a43a7d4e464fbcc862160c18e843f455`

```dockerfile
```

-	Layers:
	-	`sha256:499345d0a7a481daaffbb8965f4762e8dfe41f4174953070f2f2a757872028a2`  
		Last Modified: Tue, 24 Feb 2026 19:21:43 GMT  
		Size: 3.7 MB (3658095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00348bba47c2e9b12086a11819274c277f12e27cc217565f02b5ee77e41e7dff`  
		Last Modified: Tue, 24 Feb 2026 19:21:43 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.1-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:90300ee575847a78a0ac8469e4ca439296ff76a18037c079b043ef1240a2fc4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155342048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095919028295ae8e9811d72082cd88abe6ce7a7b9fdd493ea45257a426a9fa90`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:25:45 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 24 Feb 2026 19:25:45 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 24 Feb 2026 19:25:51 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:25:58 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 24 Feb 2026 19:26:01 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 24 Feb 2026 19:26:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 24 Feb 2026 19:26:11 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 24 Feb 2026 19:26:12 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 24 Feb 2026 19:26:12 GMT
VOLUME [/opt/nouveau/data]
# Tue, 24 Feb 2026 19:26:12 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 24 Feb 2026 19:26:12 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e26c0f056669b165a8ae59eaff14387edf0f261e8b450067813093d83930c73`  
		Last Modified: Tue, 24 Feb 2026 19:26:26 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9820074d8ac8dcf46e3efdf9679ade22002a185cc39b3f7578826f640e83587`  
		Last Modified: Tue, 24 Feb 2026 19:26:27 GMT  
		Size: 7.7 MB (7692622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e888a3c3c9fa56a143880febc9d826e8bec60a6a09ce8f2f1bfa5ac7c2dc29f1`  
		Last Modified: Tue, 24 Feb 2026 19:26:28 GMT  
		Size: 76.7 MB (76700050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56721790700ad6a8decec8f7e7c2da18ad1c9b0708cc502a05a49e174ce46d06`  
		Last Modified: Tue, 24 Feb 2026 19:26:26 GMT  
		Size: 392.8 KB (392770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e29871ea620339c69ce3817fc2d93fa827c472742ac3f984d6798318379448`  
		Last Modified: Tue, 24 Feb 2026 19:26:27 GMT  
		Size: 99.5 KB (99520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6e3773a84b9dae8befc65af5e5a3e970f192593d2e36b0b1836abc3a018724`  
		Last Modified: Tue, 24 Feb 2026 19:26:28 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb2b450c1ba8c12a3548ef9746da587ae85038952093ec2c15072768da58330`  
		Last Modified: Tue, 24 Feb 2026 19:26:29 GMT  
		Size: 42.3 MB (42339126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbeb35bc414ae41b2b4da730a59d4ee5a8181e35a4e3b83842f742121b99993`  
		Last Modified: Tue, 24 Feb 2026 19:26:29 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:6a6fb2fe398fca430e75696ef76cdf08024df46c6feeed01e317aa99233671e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa2f6ebf52b151e48808601cae4de7825d0f252285de645a9cb4dd9b86a46b2`

```dockerfile
```

-	Layers:
	-	`sha256:dcfc735a1fabe515dca1c188ca05762d93b1db9e33112021574819b5d4742ef7`  
		Last Modified: Tue, 24 Feb 2026 19:26:26 GMT  
		Size: 3.7 MB (3656771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ca8f03f33a2591f16bea1316bd8899b382a7710144eb8162622e7584d3a39a3`  
		Last Modified: Tue, 24 Feb 2026 19:26:26 GMT  
		Size: 24.7 KB (24703 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.1-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:2e4472b408c0333e2977f33a8bfb7d510f88cb1aab0a7988af6739167e6e1eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150105815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7852f3425b90f93b2dc01b1e9f55e19fdd6b31db61e5e4b360ac68079cb5f896`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:58:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 24 Feb 2026 20:58:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 24 Feb 2026 20:59:11 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:59:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:59:41 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 24 Feb 2026 20:59:41 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 24 Feb 2026 21:00:02 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:00:03 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 24 Feb 2026 21:00:22 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 24 Feb 2026 21:00:24 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 24 Feb 2026 21:00:24 GMT
VOLUME [/opt/nouveau/data]
# Tue, 24 Feb 2026 21:00:24 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 24 Feb 2026 21:00:24 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a950e14c7d88cf86c9d9f9f5d81eb0a6b66998ba15461f24cf32c54767ad382`  
		Last Modified: Tue, 24 Feb 2026 21:01:23 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ad91eaeb8b4d910bab5880a0168f86b9d9ccd494cc0e2c363abef9ed6361d5`  
		Last Modified: Tue, 24 Feb 2026 21:01:23 GMT  
		Size: 7.4 MB (7399125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ecc468cc57fa7504bc399c879bbdeeababdcf31c418cdd66c4c5078deded16`  
		Last Modified: Tue, 24 Feb 2026 21:01:25 GMT  
		Size: 73.2 MB (73153712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28c50c2f86346560509995780e524a097a56cc46e1be1ff10e6d9b7215617df`  
		Last Modified: Tue, 24 Feb 2026 21:01:23 GMT  
		Size: 394.6 KB (394634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f944fabb2ccbde3fd8f7bae3e9dfcc47f3404a64b0155a38b80bf162ccced73`  
		Last Modified: Tue, 24 Feb 2026 21:01:24 GMT  
		Size: 99.9 KB (99898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcc8fc571c26bb731d288c5f2e27c40b126abe67e58f979bd6ae46e51befb76`  
		Last Modified: Tue, 24 Feb 2026 21:01:24 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385829014d2303d4b21b8b070f89c2ef8a306df85e8c3e8d0e85a8883c4c2217`  
		Last Modified: Tue, 24 Feb 2026 21:01:25 GMT  
		Size: 42.2 MB (42165035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08a99fb7b0c3348916dd13728c92af578510c3769cb53f3b5f6d7d9daa58ee73`  
		Last Modified: Tue, 24 Feb 2026 21:01:25 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:6668e725b2c526b9c98685853b218fabcfe534c0bbe372c9c52d62958868c2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0f3fa400a6f7d0917b3d1feb53fa0f8a6f92f09779bae79f9861bed5f1a30b`

```dockerfile
```

-	Layers:
	-	`sha256:33647360be3076acd9276e12e6453e64a05fe294f1152df02bd81def6ae34b86`  
		Last Modified: Tue, 24 Feb 2026 21:01:23 GMT  
		Size: 3.6 MB (3648624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2786da3d1f564b542091d726336018be02ead528326f1772e60c8a37807fd671`  
		Last Modified: Tue, 24 Feb 2026 21:01:22 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:d55f35ffc020ca4c615fccfddd4f893d11f957593b12b33fce5e7b0840366ccd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:41766fcef3c3ab64a2b6d36560f237b23df3d29cea7c5c9d945f29d83896ac06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142059668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71979498d495be6e72756259eff755a726b88dd825408be29fb3aba1b5240175`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:20:54 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 24 Feb 2026 19:20:54 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 24 Feb 2026 19:21:00 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 24 Feb 2026 19:21:02 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 24 Feb 2026 19:21:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:07 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 24 Feb 2026 19:21:07 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 24 Feb 2026 19:21:21 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 24 Feb 2026 19:21:21 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 24 Feb 2026 19:21:21 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 24 Feb 2026 19:21:21 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Feb 2026 19:21:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:21:21 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:21:21 GMT
VOLUME [/opt/couchdb/data]
# Tue, 24 Feb 2026 19:21:21 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 24 Feb 2026 19:21:21 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7d73966d9314fcd3d72b1b0595152eb892287a887426b08e9811b94ae2b379`  
		Last Modified: Tue, 24 Feb 2026 19:21:34 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b3b202dd2e4a1bbf752929191ebe478db7474b2b54bf6748156e639d1336c6`  
		Last Modified: Tue, 24 Feb 2026 19:21:34 GMT  
		Size: 7.9 MB (7883121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7271a9298cc81eb015423fe434ed96701a704ee22755593dc7ab377c3d833050`  
		Last Modified: Tue, 24 Feb 2026 19:21:34 GMT  
		Size: 401.8 KB (401802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788dcc4a23034e7f3d98e0c1208b1d84d892332d87774695962802b0bc3c0ba4`  
		Last Modified: Tue, 24 Feb 2026 19:21:34 GMT  
		Size: 76.5 KB (76508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a61888d031364c28d8b161262599c1af189256403e0753623d967a543e66fc2`  
		Last Modified: Tue, 24 Feb 2026 19:21:35 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f591ba27f1c6cb2b55ff86d593c814940f7cfec9027f144771ca1abb4f1484d`  
		Last Modified: Tue, 24 Feb 2026 19:21:37 GMT  
		Size: 105.5 MB (105456525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296ca6c03411e008479fc5f485ead2445d1c10e83542a0f803f26e693f8c990f`  
		Last Modified: Tue, 24 Feb 2026 19:21:35 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269188377ea3f7d37af3b7885f565f7d389edb04de18151f2a6912e78d9636de`  
		Last Modified: Tue, 24 Feb 2026 19:21:35 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1361f09b26e9d82d4283c4bebe3697cce16e5c358fb2e5b0d7d307bc6b62ec15`  
		Last Modified: Tue, 24 Feb 2026 19:21:36 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a75cb6d22638fcb69fb3d276b158b220964f410718633d00c472bbf795fc0e1`  
		Last Modified: Tue, 24 Feb 2026 19:21:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:6538ab89712240a307f4f3cc91b72512adcc89143967f8bbe4ad622d85ed6e0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99925e22ce7d2cb43c93f63b1e6827c2f235c3e9808a820d7d95820deb5fe769`

```dockerfile
```

-	Layers:
	-	`sha256:2d6482430b6b5635652a50047b4489bb7944b7974c056abc260ef4fdeff9687a`  
		Last Modified: Tue, 24 Feb 2026 19:21:34 GMT  
		Size: 4.2 MB (4184421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fa746e2a5678a43070ce809bd32b3918490c0cfa6c206f7f768bd208f1da7de`  
		Last Modified: Tue, 24 Feb 2026 19:21:34 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:770dce57c3d96e16be18d9c33673657a065bc5cf0b72ddd4a469de4ce0e28339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141419192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f29a3517318bc3af48f6be7a479b9ba60373ac6af58d062f5b3a967d7f63d2a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:25:24 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 24 Feb 2026 19:25:24 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 24 Feb 2026 19:25:30 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:25:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 24 Feb 2026 19:25:33 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 24 Feb 2026 19:25:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:25:37 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 24 Feb 2026 19:25:37 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 24 Feb 2026 19:25:51 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 24 Feb 2026 19:25:51 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 24 Feb 2026 19:25:52 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 24 Feb 2026 19:25:52 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Feb 2026 19:25:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 19:25:52 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:25:52 GMT
VOLUME [/opt/couchdb/data]
# Tue, 24 Feb 2026 19:25:52 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 24 Feb 2026 19:25:52 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5195943c8bc81ff3ccacc7d15e0222f0ddc0a363f1da17509b63e4dd41b2299f`  
		Last Modified: Tue, 24 Feb 2026 19:26:05 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbba4689c9413d25ec04c6c788241c6a8ab4ca2ee82346c96241d886dd4588b`  
		Last Modified: Tue, 24 Feb 2026 19:26:05 GMT  
		Size: 7.7 MB (7692638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3981bae95c2cf4b56a60963485420ec03af0c4467a5c204fc9de44bbfaa076c5`  
		Last Modified: Tue, 24 Feb 2026 19:26:05 GMT  
		Size: 370.5 KB (370543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0780dc8172b862928867ea7afe0354b30bfee9ddd9500fcd0ee128ec7db63069`  
		Last Modified: Tue, 24 Feb 2026 19:26:05 GMT  
		Size: 76.5 KB (76468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada3951d847dd448afd38f10999ea754f9d96abd69c5e876ea8eb8e0708cda8c`  
		Last Modified: Tue, 24 Feb 2026 19:26:06 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081dd262f305fc888779fda5162e7ef14b3dd157bda32f9adfe0c71e3c53b9f3`  
		Last Modified: Tue, 24 Feb 2026 19:26:08 GMT  
		Size: 105.2 MB (105158034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae02b6144e60ba0617faf2dabd56adf4ae0b8ca4696cec8383550db4ccfeb03a`  
		Last Modified: Tue, 24 Feb 2026 19:26:06 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349350c52f60a43ac4b9153a28573e1ed7c6230729482261de86e4eec142f621`  
		Last Modified: Tue, 24 Feb 2026 19:26:06 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d040afc70746c77854a2e80fbac73e1f602fbf8ac82fecebc968cef9598cf9`  
		Last Modified: Tue, 24 Feb 2026 19:26:07 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aaa06830632dd23874fc9a34e260c5027305c63c186b36c7cf19232e3c3e9c9`  
		Last Modified: Tue, 24 Feb 2026 19:26:07 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:8e105bac4709d132c2132b3c176eec75158d671f9088324761cffbc47aff3602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa658a9c5ab56fe8f6fd623762676a48f4c87358be034ae7fecbbf3b1500921`

```dockerfile
```

-	Layers:
	-	`sha256:3a05677e5b72845cdfc530571ac1a2ef5046321baf165d46020942e6fd7d4ca9`  
		Last Modified: Tue, 24 Feb 2026 19:26:05 GMT  
		Size: 4.2 MB (4184714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57719038c77b024cd456dcee02cf0aa52f7a7b967dc3a6056213dbffc43702c5`  
		Last Modified: Tue, 24 Feb 2026 19:26:05 GMT  
		Size: 31.9 KB (31932 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:b37585c645221c6f47e1720d73d41e2913dd4c5d9da1325227b92148e3f00c53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138773629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9ccda5442365d739afa4c52c7891f387b7a41f8159f6d886b58c68ab7da04b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:58:41 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 24 Feb 2026 20:58:41 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 24 Feb 2026 20:59:11 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:59:16 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 24 Feb 2026 20:59:16 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 24 Feb 2026 20:59:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:59:33 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 24 Feb 2026 20:59:34 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 24 Feb 2026 21:00:16 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 24 Feb 2026 21:00:17 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 24 Feb 2026 21:00:17 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 24 Feb 2026 21:00:18 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Feb 2026 21:00:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 24 Feb 2026 21:00:18 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 21:00:18 GMT
VOLUME [/opt/couchdb/data]
# Tue, 24 Feb 2026 21:00:18 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 24 Feb 2026 21:00:18 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1eeb0a30f79824913befe6cff540b6bbef64ce01bcd01d02353436b346f1c52`  
		Last Modified: Tue, 24 Feb 2026 21:01:18 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed832851f69da334438fcc233f300fb11f53288452d86a31700195783d07b7b`  
		Last Modified: Tue, 24 Feb 2026 21:01:23 GMT  
		Size: 7.4 MB (7399099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283498defbfbbe68c63defadeb6bd597efc21eeae2245bd6ef3a48b45792b2eb`  
		Last Modified: Tue, 24 Feb 2026 21:01:17 GMT  
		Size: 372.2 KB (372246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e76b77d775634501854d45ab3d68cf569581ce20c532eb424e4b24916cc697`  
		Last Modified: Tue, 24 Feb 2026 21:01:18 GMT  
		Size: 76.7 KB (76745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7caefca7f93130ff023ae08185691df23526132092c2d1c0f6abbe4953830c`  
		Last Modified: Tue, 24 Feb 2026 21:01:21 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9967421ea9282f965997b6135e3475d745fa5dbf3779675c500ca2da629a6879`  
		Last Modified: Tue, 24 Feb 2026 21:01:24 GMT  
		Size: 104.0 MB (104028576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185c2f75ff7c0754709bd9b4d1960fa9befe3e99a1740f14b2a362a4e8f893e4`  
		Last Modified: Tue, 24 Feb 2026 21:01:19 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75895523cafbc3bf7cc90bcd1beb3eb6446ff705134466fc56c3d3dd5f46b12`  
		Last Modified: Tue, 24 Feb 2026 21:01:21 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c9910bd6a90ab78f2a16acf8792a2f83e235d516f41e2e74a5b64df59d78f0`  
		Last Modified: Tue, 24 Feb 2026 21:01:22 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46ae2bc44dafb76079ab9db1dd230550789fad97c3b93aef7bbbd770298056c`  
		Last Modified: Tue, 24 Feb 2026 21:01:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:b6a18a48d50c63a224991d5e294fc51a4096f16c8d0cc7533d18e8af2c00b9d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35047fcb81ed162b1e68c86ff7087b1eab1a17c69fa0b371b511f7912315824`

```dockerfile
```

-	Layers:
	-	`sha256:ebf92ddcfc83a696b60fc5a62ee38340c62d83b965fcfc2fa6abad4a5217e495`  
		Last Modified: Tue, 24 Feb 2026 21:01:18 GMT  
		Size: 4.2 MB (4180617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f74ac14845fdc83f326ed34daccc3fda4c7d18d05582eaccd9dfc0e2891e4325`  
		Last Modified: Tue, 24 Feb 2026 21:01:17 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json
