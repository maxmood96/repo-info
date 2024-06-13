<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchdb`

-	[`couchdb:2`](#couchdb2)
-	[`couchdb:2.3`](#couchdb23)
-	[`couchdb:2.3.1`](#couchdb231)
-	[`couchdb:3`](#couchdb3)
-	[`couchdb:3.1`](#couchdb31)
-	[`couchdb:3.1.2`](#couchdb312)
-	[`couchdb:3.2`](#couchdb32)
-	[`couchdb:3.2.3`](#couchdb323)
-	[`couchdb:3.3`](#couchdb33)
-	[`couchdb:3.3.3`](#couchdb333)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:2`

```console
$ docker pull couchdb@sha256:30dc067ce470fd437f4074d41f150fa81c1ff9c923a371d38f155d1a36159f4e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:2` - linux; amd64

```console
$ docker pull couchdb@sha256:89750921afa819641727ffd70ad38e3ad01d11ea9ac645db52a5f5495f051b4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84325686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e90b3327e152f23fdfb7ad3f5199c3fc966ca1ed580320ddd203544e97b62cd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:cce4de1623245f9f28e3365e6cf749d85dcfedddea2d6fbc963c309a40818f52 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b338562f40a7fb7360dfae935da6d7e40d2545db18bc461d9d70ec1b2b657f33`  
		Last Modified: Thu, 13 Jun 2024 01:26:49 GMT  
		Size: 27.3 MB (27337703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18996a36b8d72950a9ac86053f36c4a5fc9eacc914417902cdf1dbc30f45eb7`  
		Last Modified: Thu, 13 Jun 2024 18:14:04 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc5003a2699d9f9550d09185427c77384bd465e34a179611b922ee7adea94bf`  
		Last Modified: Thu, 13 Jun 2024 18:14:04 GMT  
		Size: 6.7 MB (6703175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301ed2df351bce6295999095e138d1a67e693d08f9d20c43f28f2b7a048b93da`  
		Last Modified: Thu, 13 Jun 2024 18:14:04 GMT  
		Size: 1.0 MB (1046499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83378b35f238a8acf19e241017ba2c6e68821d6ee65abef4d13d2916ab0dd19`  
		Last Modified: Thu, 13 Jun 2024 18:14:04 GMT  
		Size: 80.3 KB (80332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acc67f0ff5059e1e74d8a0ad02e7cbcf778748d60cb7613fd5f008bb3aec97d`  
		Last Modified: Thu, 13 Jun 2024 18:14:05 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b923935edfa1d2bf064fd5aad8030720e29cd6a7a246c3903b7a15fd2601468a`  
		Last Modified: Thu, 13 Jun 2024 18:14:05 GMT  
		Size: 49.2 MB (49151051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ec5a85f2d2842bb758563b5d272fbd0c5eaf2eee0a38fb445e20c3a4850f6a`  
		Last Modified: Thu, 13 Jun 2024 18:14:05 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9dfb3dcd32988086b27fcd2f72a05fb92b87b0cc7d9d2abccdf2daefe7930d`  
		Last Modified: Thu, 13 Jun 2024 18:14:05 GMT  
		Size: 761.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8346f410461807932d32317849c80d299a27002245b0fc4d24fbc4ea3e3e0a`  
		Last Modified: Thu, 13 Jun 2024 18:14:06 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65c80182a4eb1660cccbcb2582e85f36dcebd96cbae8ea16e4ea13e62f0fcfc`  
		Last Modified: Thu, 13 Jun 2024 18:14:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:2` - unknown; unknown

```console
$ docker pull couchdb@sha256:f8096fe431daab3a22c1d9397731e7c3d90a37eee17296adedbd24476a6a9d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4469947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479a94408bea25c19cbfa1eea5cb65bedd05e0ced966f6d9eb9b8cf6c17759da`

```dockerfile
```

-	Layers:
	-	`sha256:d0c8e8c3213c6bc57304a8eaa4ad95cd6c600024eecece85ac80119d6bf5f0f0`  
		Last Modified: Thu, 13 Jun 2024 18:14:04 GMT  
		Size: 4.4 MB (4438480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90f9aca84b6f1c51595c95acbd60b4525483ebf75225c6723d22f8aac2d36b66`  
		Last Modified: Thu, 13 Jun 2024 18:14:04 GMT  
		Size: 31.5 KB (31467 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:87a4a9e81c588c26aa24f1638af0d52b81c5645701390eb7e57a423c46fbeed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72754318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2875d4ebc5716e721022352fd0b117b599cce476ac426e71f9eff16a19ffa58`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:de9a2b323e6d7d969277e7e781875e3daf3f49f2c1dcc569a1eec4f5bd789c46 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7abf9f73c7747bb840a8edcd895830e53f09498136de3015568a9cd9f5ab10ed`  
		Last Modified: Thu, 13 Jun 2024 00:44:26 GMT  
		Size: 26.1 MB (26109272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eca7c66c8588ba658ce9600ea40b6f2b5d56c06f381a970e4d0f982449ef4cc`  
		Last Modified: Thu, 13 Jun 2024 12:07:26 GMT  
		Size: 3.4 KB (3354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93eefa6ad47ebab27d37425a2dbb0a7f35fd35f08b133559ce2b2dcb9f393b6`  
		Last Modified: Thu, 13 Jun 2024 12:07:27 GMT  
		Size: 6.6 MB (6576435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a366eb898e6bb117bb755e338a551dbf46e7138ae1668de0ff15ad96787044`  
		Last Modified: Thu, 13 Jun 2024 12:07:27 GMT  
		Size: 951.4 KB (951371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2779ec1172795a161516aee295018f37f87aa1b8aec259959f3bd2316ccb6674`  
		Last Modified: Thu, 13 Jun 2024 12:07:28 GMT  
		Size: 80.2 KB (80201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c41f8dee5aca59f6c2cf4b21c4ee45ac260d8fcce122eb6312b49e90066f38`  
		Last Modified: Thu, 13 Jun 2024 12:08:04 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f58d3d9e680f607741efb6143d7e07e2cb4cf6b8ff178e4f883df8c002ea8d`  
		Last Modified: Thu, 13 Jun 2024 12:08:05 GMT  
		Size: 39.0 MB (39030087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707fd66f6425f4ba6ecab5972e72712c6da5a8a550fc3778c8898289b1652fda`  
		Last Modified: Thu, 13 Jun 2024 12:08:04 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fc38277a1a9eac446226225d0f89c52c9c6532d32c7e75a2b4847ee8ddc64a`  
		Last Modified: Thu, 13 Jun 2024 12:08:04 GMT  
		Size: 762.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faca6a1834795adc30c3a7886d19159959424f4aa036f89a20497d60dabd2b69`  
		Last Modified: Thu, 13 Jun 2024 12:08:05 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21853c73d6968b4c91e6be1c5b3c28a6d794131df32978d88e207f8c6faa43c7`  
		Last Modified: Thu, 13 Jun 2024 12:08:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:2` - unknown; unknown

```console
$ docker pull couchdb@sha256:c180b8c4fee42e5a71a2cc30a5912b057a9ec58f43a0d78355041a49e6bb9cd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3781900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58104c2ed779690788017df679e2c3ea1ce8a55b5fbbfd1e2dd123ef433fef34`

```dockerfile
```

-	Layers:
	-	`sha256:ee1881752811808dc16e5df561d047168db83eb46a945dab5b094bbf3a4803ea`  
		Last Modified: Thu, 13 Jun 2024 12:08:04 GMT  
		Size: 3.8 MB (3750145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84622ed60653ed570da8c896133b19807cddb033faf4168277e29ff6cc6bc957`  
		Last Modified: Thu, 13 Jun 2024 12:08:03 GMT  
		Size: 31.8 KB (31755 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:2.3`

```console
$ docker pull couchdb@sha256:30dc067ce470fd437f4074d41f150fa81c1ff9c923a371d38f155d1a36159f4e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:89750921afa819641727ffd70ad38e3ad01d11ea9ac645db52a5f5495f051b4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84325686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e90b3327e152f23fdfb7ad3f5199c3fc966ca1ed580320ddd203544e97b62cd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:cce4de1623245f9f28e3365e6cf749d85dcfedddea2d6fbc963c309a40818f52 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b338562f40a7fb7360dfae935da6d7e40d2545db18bc461d9d70ec1b2b657f33`  
		Last Modified: Thu, 13 Jun 2024 01:26:49 GMT  
		Size: 27.3 MB (27337703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18996a36b8d72950a9ac86053f36c4a5fc9eacc914417902cdf1dbc30f45eb7`  
		Last Modified: Thu, 13 Jun 2024 18:14:04 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc5003a2699d9f9550d09185427c77384bd465e34a179611b922ee7adea94bf`  
		Last Modified: Thu, 13 Jun 2024 18:14:04 GMT  
		Size: 6.7 MB (6703175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301ed2df351bce6295999095e138d1a67e693d08f9d20c43f28f2b7a048b93da`  
		Last Modified: Thu, 13 Jun 2024 18:14:04 GMT  
		Size: 1.0 MB (1046499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83378b35f238a8acf19e241017ba2c6e68821d6ee65abef4d13d2916ab0dd19`  
		Last Modified: Thu, 13 Jun 2024 18:14:04 GMT  
		Size: 80.3 KB (80332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acc67f0ff5059e1e74d8a0ad02e7cbcf778748d60cb7613fd5f008bb3aec97d`  
		Last Modified: Thu, 13 Jun 2024 18:14:05 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b923935edfa1d2bf064fd5aad8030720e29cd6a7a246c3903b7a15fd2601468a`  
		Last Modified: Thu, 13 Jun 2024 18:14:05 GMT  
		Size: 49.2 MB (49151051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ec5a85f2d2842bb758563b5d272fbd0c5eaf2eee0a38fb445e20c3a4850f6a`  
		Last Modified: Thu, 13 Jun 2024 18:14:05 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9dfb3dcd32988086b27fcd2f72a05fb92b87b0cc7d9d2abccdf2daefe7930d`  
		Last Modified: Thu, 13 Jun 2024 18:14:05 GMT  
		Size: 761.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8346f410461807932d32317849c80d299a27002245b0fc4d24fbc4ea3e3e0a`  
		Last Modified: Thu, 13 Jun 2024 18:14:06 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65c80182a4eb1660cccbcb2582e85f36dcebd96cbae8ea16e4ea13e62f0fcfc`  
		Last Modified: Thu, 13 Jun 2024 18:14:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:2.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:f8096fe431daab3a22c1d9397731e7c3d90a37eee17296adedbd24476a6a9d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4469947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479a94408bea25c19cbfa1eea5cb65bedd05e0ced966f6d9eb9b8cf6c17759da`

```dockerfile
```

-	Layers:
	-	`sha256:d0c8e8c3213c6bc57304a8eaa4ad95cd6c600024eecece85ac80119d6bf5f0f0`  
		Last Modified: Thu, 13 Jun 2024 18:14:04 GMT  
		Size: 4.4 MB (4438480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90f9aca84b6f1c51595c95acbd60b4525483ebf75225c6723d22f8aac2d36b66`  
		Last Modified: Thu, 13 Jun 2024 18:14:04 GMT  
		Size: 31.5 KB (31467 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:2.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:87a4a9e81c588c26aa24f1638af0d52b81c5645701390eb7e57a423c46fbeed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72754318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2875d4ebc5716e721022352fd0b117b599cce476ac426e71f9eff16a19ffa58`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:de9a2b323e6d7d969277e7e781875e3daf3f49f2c1dcc569a1eec4f5bd789c46 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7abf9f73c7747bb840a8edcd895830e53f09498136de3015568a9cd9f5ab10ed`  
		Last Modified: Thu, 13 Jun 2024 00:44:26 GMT  
		Size: 26.1 MB (26109272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eca7c66c8588ba658ce9600ea40b6f2b5d56c06f381a970e4d0f982449ef4cc`  
		Last Modified: Thu, 13 Jun 2024 12:07:26 GMT  
		Size: 3.4 KB (3354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93eefa6ad47ebab27d37425a2dbb0a7f35fd35f08b133559ce2b2dcb9f393b6`  
		Last Modified: Thu, 13 Jun 2024 12:07:27 GMT  
		Size: 6.6 MB (6576435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a366eb898e6bb117bb755e338a551dbf46e7138ae1668de0ff15ad96787044`  
		Last Modified: Thu, 13 Jun 2024 12:07:27 GMT  
		Size: 951.4 KB (951371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2779ec1172795a161516aee295018f37f87aa1b8aec259959f3bd2316ccb6674`  
		Last Modified: Thu, 13 Jun 2024 12:07:28 GMT  
		Size: 80.2 KB (80201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c41f8dee5aca59f6c2cf4b21c4ee45ac260d8fcce122eb6312b49e90066f38`  
		Last Modified: Thu, 13 Jun 2024 12:08:04 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f58d3d9e680f607741efb6143d7e07e2cb4cf6b8ff178e4f883df8c002ea8d`  
		Last Modified: Thu, 13 Jun 2024 12:08:05 GMT  
		Size: 39.0 MB (39030087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707fd66f6425f4ba6ecab5972e72712c6da5a8a550fc3778c8898289b1652fda`  
		Last Modified: Thu, 13 Jun 2024 12:08:04 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fc38277a1a9eac446226225d0f89c52c9c6532d32c7e75a2b4847ee8ddc64a`  
		Last Modified: Thu, 13 Jun 2024 12:08:04 GMT  
		Size: 762.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faca6a1834795adc30c3a7886d19159959424f4aa036f89a20497d60dabd2b69`  
		Last Modified: Thu, 13 Jun 2024 12:08:05 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21853c73d6968b4c91e6be1c5b3c28a6d794131df32978d88e207f8c6faa43c7`  
		Last Modified: Thu, 13 Jun 2024 12:08:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:2.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:c180b8c4fee42e5a71a2cc30a5912b057a9ec58f43a0d78355041a49e6bb9cd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3781900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58104c2ed779690788017df679e2c3ea1ce8a55b5fbbfd1e2dd123ef433fef34`

```dockerfile
```

-	Layers:
	-	`sha256:ee1881752811808dc16e5df561d047168db83eb46a945dab5b094bbf3a4803ea`  
		Last Modified: Thu, 13 Jun 2024 12:08:04 GMT  
		Size: 3.8 MB (3750145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84622ed60653ed570da8c896133b19807cddb033faf4168277e29ff6cc6bc957`  
		Last Modified: Thu, 13 Jun 2024 12:08:03 GMT  
		Size: 31.8 KB (31755 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:2.3.1`

```console
$ docker pull couchdb@sha256:30dc067ce470fd437f4074d41f150fa81c1ff9c923a371d38f155d1a36159f4e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:2.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:89750921afa819641727ffd70ad38e3ad01d11ea9ac645db52a5f5495f051b4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84325686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e90b3327e152f23fdfb7ad3f5199c3fc966ca1ed580320ddd203544e97b62cd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:cce4de1623245f9f28e3365e6cf749d85dcfedddea2d6fbc963c309a40818f52 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b338562f40a7fb7360dfae935da6d7e40d2545db18bc461d9d70ec1b2b657f33`  
		Last Modified: Thu, 13 Jun 2024 01:26:49 GMT  
		Size: 27.3 MB (27337703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18996a36b8d72950a9ac86053f36c4a5fc9eacc914417902cdf1dbc30f45eb7`  
		Last Modified: Thu, 13 Jun 2024 18:14:04 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc5003a2699d9f9550d09185427c77384bd465e34a179611b922ee7adea94bf`  
		Last Modified: Thu, 13 Jun 2024 18:14:04 GMT  
		Size: 6.7 MB (6703175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301ed2df351bce6295999095e138d1a67e693d08f9d20c43f28f2b7a048b93da`  
		Last Modified: Thu, 13 Jun 2024 18:14:04 GMT  
		Size: 1.0 MB (1046499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83378b35f238a8acf19e241017ba2c6e68821d6ee65abef4d13d2916ab0dd19`  
		Last Modified: Thu, 13 Jun 2024 18:14:04 GMT  
		Size: 80.3 KB (80332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acc67f0ff5059e1e74d8a0ad02e7cbcf778748d60cb7613fd5f008bb3aec97d`  
		Last Modified: Thu, 13 Jun 2024 18:14:05 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b923935edfa1d2bf064fd5aad8030720e29cd6a7a246c3903b7a15fd2601468a`  
		Last Modified: Thu, 13 Jun 2024 18:14:05 GMT  
		Size: 49.2 MB (49151051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ec5a85f2d2842bb758563b5d272fbd0c5eaf2eee0a38fb445e20c3a4850f6a`  
		Last Modified: Thu, 13 Jun 2024 18:14:05 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9dfb3dcd32988086b27fcd2f72a05fb92b87b0cc7d9d2abccdf2daefe7930d`  
		Last Modified: Thu, 13 Jun 2024 18:14:05 GMT  
		Size: 761.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8346f410461807932d32317849c80d299a27002245b0fc4d24fbc4ea3e3e0a`  
		Last Modified: Thu, 13 Jun 2024 18:14:06 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65c80182a4eb1660cccbcb2582e85f36dcebd96cbae8ea16e4ea13e62f0fcfc`  
		Last Modified: Thu, 13 Jun 2024 18:14:06 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:2.3.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:f8096fe431daab3a22c1d9397731e7c3d90a37eee17296adedbd24476a6a9d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4469947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479a94408bea25c19cbfa1eea5cb65bedd05e0ced966f6d9eb9b8cf6c17759da`

```dockerfile
```

-	Layers:
	-	`sha256:d0c8e8c3213c6bc57304a8eaa4ad95cd6c600024eecece85ac80119d6bf5f0f0`  
		Last Modified: Thu, 13 Jun 2024 18:14:04 GMT  
		Size: 4.4 MB (4438480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90f9aca84b6f1c51595c95acbd60b4525483ebf75225c6723d22f8aac2d36b66`  
		Last Modified: Thu, 13 Jun 2024 18:14:04 GMT  
		Size: 31.5 KB (31467 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:2.3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:87a4a9e81c588c26aa24f1638af0d52b81c5645701390eb7e57a423c46fbeed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72754318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2875d4ebc5716e721022352fd0b117b599cce476ac426e71f9eff16a19ffa58`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:de9a2b323e6d7d969277e7e781875e3daf3f49f2c1dcc569a1eec4f5bd789c46 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7abf9f73c7747bb840a8edcd895830e53f09498136de3015568a9cd9f5ab10ed`  
		Last Modified: Thu, 13 Jun 2024 00:44:26 GMT  
		Size: 26.1 MB (26109272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eca7c66c8588ba658ce9600ea40b6f2b5d56c06f381a970e4d0f982449ef4cc`  
		Last Modified: Thu, 13 Jun 2024 12:07:26 GMT  
		Size: 3.4 KB (3354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93eefa6ad47ebab27d37425a2dbb0a7f35fd35f08b133559ce2b2dcb9f393b6`  
		Last Modified: Thu, 13 Jun 2024 12:07:27 GMT  
		Size: 6.6 MB (6576435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a366eb898e6bb117bb755e338a551dbf46e7138ae1668de0ff15ad96787044`  
		Last Modified: Thu, 13 Jun 2024 12:07:27 GMT  
		Size: 951.4 KB (951371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2779ec1172795a161516aee295018f37f87aa1b8aec259959f3bd2316ccb6674`  
		Last Modified: Thu, 13 Jun 2024 12:07:28 GMT  
		Size: 80.2 KB (80201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c41f8dee5aca59f6c2cf4b21c4ee45ac260d8fcce122eb6312b49e90066f38`  
		Last Modified: Thu, 13 Jun 2024 12:08:04 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f58d3d9e680f607741efb6143d7e07e2cb4cf6b8ff178e4f883df8c002ea8d`  
		Last Modified: Thu, 13 Jun 2024 12:08:05 GMT  
		Size: 39.0 MB (39030087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707fd66f6425f4ba6ecab5972e72712c6da5a8a550fc3778c8898289b1652fda`  
		Last Modified: Thu, 13 Jun 2024 12:08:04 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fc38277a1a9eac446226225d0f89c52c9c6532d32c7e75a2b4847ee8ddc64a`  
		Last Modified: Thu, 13 Jun 2024 12:08:04 GMT  
		Size: 762.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faca6a1834795adc30c3a7886d19159959424f4aa036f89a20497d60dabd2b69`  
		Last Modified: Thu, 13 Jun 2024 12:08:05 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21853c73d6968b4c91e6be1c5b3c28a6d794131df32978d88e207f8c6faa43c7`  
		Last Modified: Thu, 13 Jun 2024 12:08:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:2.3.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:c180b8c4fee42e5a71a2cc30a5912b057a9ec58f43a0d78355041a49e6bb9cd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3781900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58104c2ed779690788017df679e2c3ea1ce8a55b5fbbfd1e2dd123ef433fef34`

```dockerfile
```

-	Layers:
	-	`sha256:ee1881752811808dc16e5df561d047168db83eb46a945dab5b094bbf3a4803ea`  
		Last Modified: Thu, 13 Jun 2024 12:08:04 GMT  
		Size: 3.8 MB (3750145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84622ed60653ed570da8c896133b19807cddb033faf4168277e29ff6cc6bc957`  
		Last Modified: Thu, 13 Jun 2024 12:08:03 GMT  
		Size: 31.8 KB (31755 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3`

```console
$ docker pull couchdb@sha256:160a9080142b72a6f7a5da75b144205ee5dd7196e26bf9e2d3081629b6985812
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:c89cdc3f7f520837473b7754a8baeb1d08f3f03b5fa943915cd9f8559e14e044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89654324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a509ab16806a265c9d2b39575b783c1eae7659fed59735e1cc18aa22469a2ee0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43142df726fcf366d45c3c93f3a24895bab6445dc4c85c1090d6276da5227beb`  
		Last Modified: Thu, 13 Jun 2024 18:14:08 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6c961978fc9c2b56f0621b270d3e081603c5cfcc6c6ec238c21dad9964e724`  
		Last Modified: Thu, 13 Jun 2024 18:14:08 GMT  
		Size: 5.0 MB (5019749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4957de11597fc7cd0dec3ca88038dfcc1878a98f07613e9f0795fac467f921`  
		Last Modified: Thu, 13 Jun 2024 18:14:08 GMT  
		Size: 394.3 KB (394338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b85f5c11e3c02b69bea8a19eb3b59e79ac14162cfbbe967677e99fa33ad4643`  
		Last Modified: Thu, 13 Jun 2024 18:14:08 GMT  
		Size: 77.9 KB (77917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b14f3d85b653c195c068e01e589e8c19497ea832ba678e5c8010489ceabdaf3`  
		Last Modified: Thu, 13 Jun 2024 18:14:09 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a0fdca4130e4482c57fcc0afde01b9fbb61fa8bd1d5d4feec746c3bfae199d`  
		Last Modified: Thu, 13 Jun 2024 18:14:10 GMT  
		Size: 52.7 MB (52720703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac2369969bc2e901ccc9fc8e646b66f7661cbd500a010df29c00f8474306ca7`  
		Last Modified: Thu, 13 Jun 2024 18:14:09 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093df6b4a3aef5ff8c9c244d8805a77e28a1ce86a7a2f4f9c5411cd503f7efd3`  
		Last Modified: Thu, 13 Jun 2024 18:14:09 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26057758054349e7e345e8e4e93de87aec433203bb6215b50094ff7ac56c9b34`  
		Last Modified: Thu, 13 Jun 2024 18:14:10 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdab9184d1046a7e2512bed66ef56136d32fd239048f59fb576f310aa385bef`  
		Last Modified: Thu, 13 Jun 2024 18:14:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:d5b455ac44d205b8e1641520d4f77d7077f2c5be17625fb926ef01e3b78beec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083b21df3a41588c3bfc9d9ecace7ce8f441b0d5b164389db4b97dd31c0e0b65`

```dockerfile
```

-	Layers:
	-	`sha256:7496d83c92f48f5c5e745520e03c3618ee788f8b0211c79205896b5f4cd0149e`  
		Last Modified: Thu, 13 Jun 2024 18:14:08 GMT  
		Size: 4.0 MB (3965077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae3832983f05e916813dcee907f72537e895b3d0276cd4c213507c5f824043eb`  
		Last Modified: Thu, 13 Jun 2024 18:14:08 GMT  
		Size: 31.6 KB (31609 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:804af72aa57c3e8bbb305a4e02262334bb3f0faeb7d5dc5b43cc966c17942d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88098811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db8c02a1d75e56b5a577dad6b2195d8a0d3f73a2f460b44651394820cf062042`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159e03cc188503d00f7d8bdc64b7b0f20dcfa5c824b222b12f461596bddc211d`  
		Last Modified: Thu, 13 Jun 2024 12:06:24 GMT  
		Size: 3.4 KB (3353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8320ebe945db07b51a6e3d70c295d7235513336a604b2d761c1744bfa040a2a6`  
		Last Modified: Thu, 13 Jun 2024 12:06:24 GMT  
		Size: 5.0 MB (5004125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ace86e95f1826009a0f6d44e6dbbc38e40bd7077ae50bac6a6c9da05e6e4877`  
		Last Modified: Thu, 13 Jun 2024 12:06:24 GMT  
		Size: 350.6 KB (350556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc02dc62631fc1d2bc60c371ed48534cac30dc27130ba0630ef0f4daf5cb8bc`  
		Last Modified: Thu, 13 Jun 2024 12:06:24 GMT  
		Size: 77.8 KB (77833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b4a4bc11ee2e5fe692ab7e13b96ed67ef359e8d7709a901e438f44d64b6ab4`  
		Last Modified: Thu, 13 Jun 2024 12:06:25 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6805529927fd62e453786b7281dc3886c5bdd06ed66d3bb0df2c8bf52ca0a3`  
		Last Modified: Thu, 13 Jun 2024 12:06:27 GMT  
		Size: 52.6 MB (52571728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7f005f971d165a59678360458e7ca290628e45730317bd90251081721544a6`  
		Last Modified: Thu, 13 Jun 2024 12:06:25 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8176b116135534be6ec8372585d4705a428581f7e88aa6707e0887a4b0143ab2`  
		Last Modified: Thu, 13 Jun 2024 12:06:25 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812968abeb1a11962de024a4f7ed3f7bf9a494868420a12c7832b1cb28e78808`  
		Last Modified: Thu, 13 Jun 2024 12:06:25 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebe045b6921466a0f559a27ccc4109aa0a6b9fd6a23aaa96b39e4a9d3690f78`  
		Last Modified: Thu, 13 Jun 2024 12:06:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:e8d0e00285087fcc65f7429fece6dcfcea336d8c4ede18f239c08a158ed82979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c98598aeac3e0c5ea90cbf5a3512c6e8c1e522d2c1a1cb159d3e098478847e`

```dockerfile
```

-	Layers:
	-	`sha256:6a3377cc1a509bb80dba3fd66d9ea8a001dde4dd4889dafb8f901e21b0c2047a`  
		Last Modified: Thu, 13 Jun 2024 12:06:24 GMT  
		Size: 4.0 MB (3965362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32424633f2b2ab6abc7c5cb1ab05c5b4374a6c06f99d9546a5f716545053ab1b`  
		Last Modified: Thu, 13 Jun 2024 12:06:24 GMT  
		Size: 31.9 KB (31921 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:4fdfc8c484b8a689fee25f23c47ca02bdc3ab7f0cc714377918c54148dc06213
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95382915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9205e702b9ba1b8647c89c30c636904375988fd14f8163ef1cfe07a02088a6`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:a150537fc528657f8fa98f90c4629e38f111c3c3ef60bd40c28205959899c1a3 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:64741f366161eb41a5c86810e08ceabb9f4e4b69ac16c725aa2d48f19486e1be`  
		Last Modified: Thu, 13 Jun 2024 01:22:19 GMT  
		Size: 35.3 MB (35311302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3852c5abbc985d3037df23861f3c5ff9cda64e7ab0daf054ffd7fedb261ad92d`  
		Last Modified: Thu, 13 Jun 2024 18:14:14 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3122a60c35ac4d4fb9118461bccef76774e5a69752b40ad440f8e476368c2b3d`  
		Last Modified: Thu, 13 Jun 2024 18:14:15 GMT  
		Size: 5.8 MB (5839122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf2f330b8c80511e5590fa7f12f880371c56b8981e992d4c67f892fccce9bc8`  
		Last Modified: Thu, 13 Jun 2024 18:14:14 GMT  
		Size: 446.6 KB (446599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f3bbc58deb8c0699c4a7ad68fd5c71c63d7c86bf367d0fcf7bcca2e885115a`  
		Last Modified: Thu, 13 Jun 2024 18:14:15 GMT  
		Size: 77.8 KB (77794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c65f39caa49ed72d5f4a14258ba6149da0b2477911cf0304fa70a5d563661e`  
		Last Modified: Thu, 13 Jun 2024 18:14:15 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ab6a0d309e70e2bf3d342a3b3059d120cf68c5e15c754812906a7f36fa1a4e`  
		Last Modified: Thu, 13 Jun 2024 18:14:18 GMT  
		Size: 53.7 MB (53700519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a2dd36fcaefb8a84177f04058ecd8ac0ae1a11c35e731cb01578729b979e2f`  
		Last Modified: Thu, 13 Jun 2024 18:14:16 GMT  
		Size: 383.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe688117c8b6efc252f37a38161a14eadebac0c20fdcfcacc5a83141e7a32acf`  
		Last Modified: Thu, 13 Jun 2024 18:14:16 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf565e616d54f585d9f440b472f4d0482c2c0c8c707de7484f92bda06c48c27`  
		Last Modified: Thu, 13 Jun 2024 18:14:17 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9270f647e068e9000b871d92c52ee77721ed114f39942b33f61035c3462e72e8`  
		Last Modified: Thu, 13 Jun 2024 18:14:17 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:51e884eff706bb2a3f580afff80fe53d622b4b50180cd95e24db7f77e7adbf2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4001270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28477452f11f9fab30d286e8f3758f76df82232a92cda048a298f7882b4d39d4`

```dockerfile
```

-	Layers:
	-	`sha256:9704dcf0555f56be25d306e333474fe127b5b8739a1988299ca8a1adff3c4f0a`  
		Last Modified: Thu, 13 Jun 2024 18:14:14 GMT  
		Size: 4.0 MB (3969609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bbcef6054d78175b45e16d244dc008cc11fa5720ba24fb305003f8e73e29478`  
		Last Modified: Thu, 13 Jun 2024 18:14:14 GMT  
		Size: 31.7 KB (31661 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; s390x

```console
$ docker pull couchdb@sha256:09b4b2e2499b75abd472e542832a9ad39c3b3a74175f42611276689a14c540af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86398380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24917bbd18326fe14285376a9a30651cfa62eb3ff096159b5ecbb81d63efa2c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:dbc45f2c1dc4ae2fcf0e05b8c9401406afd0f7aa3623659e470bb7d0fb97f9ec in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b9966e11fe1c4138e9aa4f0356568463c21e36009b72062413bb596e0e57738f`  
		Last Modified: Thu, 13 Jun 2024 00:48:17 GMT  
		Size: 29.7 MB (29673762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd36feb4c5f57bfea6a5a257eaace52af47fc5984ceb78220e451a521549e80`  
		Last Modified: Thu, 13 Jun 2024 05:40:06 GMT  
		Size: 3.4 KB (3353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c5455ebb092eabd0a6e9af166cf42ead0109078cd8e9fddf62226c4d18ab0a`  
		Last Modified: Thu, 13 Jun 2024 05:40:06 GMT  
		Size: 4.9 MB (4905553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19e20b81689083bec0c0fba6e1081445bb6d38bd2121508accf14e86237259c`  
		Last Modified: Thu, 13 Jun 2024 05:40:06 GMT  
		Size: 357.5 KB (357476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03632898e77801853ed03d27b69101164538d5794e6c2b790e19f2092249e718`  
		Last Modified: Thu, 13 Jun 2024 05:40:07 GMT  
		Size: 77.8 KB (77844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96f922001e502fc5317b7f262c7640dee109f0288988dce86d27ee4626560f0`  
		Last Modified: Thu, 13 Jun 2024 05:40:07 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3c8738fbddab49cdb64c861b66f16af9697726b6bbef5e63327a4e30a5c904`  
		Last Modified: Thu, 13 Jun 2024 05:40:08 GMT  
		Size: 51.4 MB (51376141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff2bd2a020f20882db2ec938239f5c6ded2e604b7e994bea60c378539adfe6c`  
		Last Modified: Thu, 13 Jun 2024 05:40:07 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0229a5de529ffd3a2d629aeed992e842e37297669111b34e04b53d062e1c2075`  
		Last Modified: Thu, 13 Jun 2024 05:40:08 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc62edd78341ad2481627387967f1377adea7259afea2b42092c03258ed7f0aa`  
		Last Modified: Thu, 13 Jun 2024 05:40:08 GMT  
		Size: 2.2 KB (2231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ce661f13c44ae354d710b3c6d2ebb233cbf63e6ad2c8a8ab19eca24c46e30d`  
		Last Modified: Thu, 13 Jun 2024 05:40:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:70a48e66fd2f3ca5f9cc7894b05e78d85e2aa31113669d77fa86b1e9340b77ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f43b3e3c655d305399e35d5b5628de175de9a4fc62f354b65c480be472df4339`

```dockerfile
```

-	Layers:
	-	`sha256:5e0abb454a86678e3ae1bed9b7178395fb80f226b06106615935e63840cecaf3`  
		Last Modified: Thu, 13 Jun 2024 05:40:06 GMT  
		Size: 4.0 MB (3964647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2b70f2c7eeacb6070d0bfe8b5916d3b41689bc55fe36ccd12fba0206e09f97e`  
		Last Modified: Thu, 13 Jun 2024 05:40:06 GMT  
		Size: 31.6 KB (31609 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:27e15e61dbdf09524f3246e187affedb1074b47be78d4d589c2c74570f846466
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:41059a5dd8946d8f0f8ef19ce5ec7bbf958cd952bb835c900f4987771ae13dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79794247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:311845dc4a3f92cb76f6026d601476c1d4e3441478605efc3df75a55785239dd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:cce4de1623245f9f28e3365e6cf749d85dcfedddea2d6fbc963c309a40818f52 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b338562f40a7fb7360dfae935da6d7e40d2545db18bc461d9d70ec1b2b657f33`  
		Last Modified: Thu, 13 Jun 2024 01:26:49 GMT  
		Size: 27.3 MB (27337703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f71eb340d102ac139740ff648b77c7cb38fd9442aecdaed4be74dc4e9dd1d9`  
		Last Modified: Thu, 13 Jun 2024 18:14:00 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e00bbd7cddf6b459d31438ca8819a97c21bc281912b422900417af1ba50e5f1`  
		Last Modified: Thu, 13 Jun 2024 18:14:00 GMT  
		Size: 6.7 MB (6703093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd17ce531ca35a5604da44c29e8ec4542045c1026286b223ab422281ced9a2c`  
		Last Modified: Thu, 13 Jun 2024 18:14:00 GMT  
		Size: 1.0 MB (1046487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01dca656eab9f47d2b9d7eb356f55cea9843d17cd8250ac019fa0573d9e12d37`  
		Last Modified: Thu, 13 Jun 2024 18:14:01 GMT  
		Size: 80.3 KB (80311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6d8da3b179f647391910cfe8ec8c333f2a7b32b022e7e58946d89b594aa800`  
		Last Modified: Thu, 13 Jun 2024 18:14:01 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6726256ce4cb4428a09a154755ad11d2b49188c3dfb785ff690f3f0d693551`  
		Last Modified: Thu, 13 Jun 2024 18:14:03 GMT  
		Size: 44.6 MB (44619730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a298e52e4d5d211187b426881893cbe0914c1085f35270161b0f7dbc496a3a5`  
		Last Modified: Thu, 13 Jun 2024 18:14:01 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e46635e078ed8dd2c3ccbad492c22f257245a8501994d61e4445719b58c6ab`  
		Last Modified: Thu, 13 Jun 2024 18:14:02 GMT  
		Size: 762.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1957a21baf08559aabc4fc698236b5ea18db4e19f2172d4b1abcdc3b0496ace8`  
		Last Modified: Thu, 13 Jun 2024 18:14:02 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7193dc3cb422ad374cc8db19524a0d3a8e93508a4980f6105760ff8d609df3a7`  
		Last Modified: Thu, 13 Jun 2024 18:14:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:b8bcc6e0b9141acc1ff229e5d79d979be5b9811f7b204c394118d056e87c1060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:148b9cfb54806e1e04597d04d7a8d377a7c5dbc10d95326a328f6b592b773ad8`

```dockerfile
```

-	Layers:
	-	`sha256:897909373d1da9b3a0d93e7ea3eaf38ded78d0ea7b3676baf499d846d2b50341`  
		Last Modified: Thu, 13 Jun 2024 18:14:00 GMT  
		Size: 3.8 MB (3807389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55248b4e5e9c16e62266004e747bc20acdb731e439dc60e04f50a647542192af`  
		Last Modified: Thu, 13 Jun 2024 18:14:00 GMT  
		Size: 31.2 KB (31168 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:68db57a2e70a09d66c3546d771e2d3529b26cde5e1cddcaee8f6a280869e8179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74849426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ad3c5c21ecdca29c3c144df13b31e73fa6e362f48661d7af160e338598df4d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:de9a2b323e6d7d969277e7e781875e3daf3f49f2c1dcc569a1eec4f5bd789c46 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7abf9f73c7747bb840a8edcd895830e53f09498136de3015568a9cd9f5ab10ed`  
		Last Modified: Thu, 13 Jun 2024 00:44:26 GMT  
		Size: 26.1 MB (26109272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eca7c66c8588ba658ce9600ea40b6f2b5d56c06f381a970e4d0f982449ef4cc`  
		Last Modified: Thu, 13 Jun 2024 12:07:26 GMT  
		Size: 3.4 KB (3354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93eefa6ad47ebab27d37425a2dbb0a7f35fd35f08b133559ce2b2dcb9f393b6`  
		Last Modified: Thu, 13 Jun 2024 12:07:27 GMT  
		Size: 6.6 MB (6576435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a366eb898e6bb117bb755e338a551dbf46e7138ae1668de0ff15ad96787044`  
		Last Modified: Thu, 13 Jun 2024 12:07:27 GMT  
		Size: 951.4 KB (951371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2779ec1172795a161516aee295018f37f87aa1b8aec259959f3bd2316ccb6674`  
		Last Modified: Thu, 13 Jun 2024 12:07:28 GMT  
		Size: 80.2 KB (80201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963daa5ca753becf931984c6fbd766e4fa1f1368ccc08b427a44f7dfd0f3e12c`  
		Last Modified: Thu, 13 Jun 2024 12:07:28 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29944b0b0a23af78ca6c433e6bbf821eb927b3c9377a3e71cd168ddc3904345`  
		Last Modified: Thu, 13 Jun 2024 12:07:30 GMT  
		Size: 41.1 MB (41125196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20cdadb40f3bcf2c12dc0ec436654aa7a8a6320cffbb86e352fe4cf55b6da44b`  
		Last Modified: Thu, 13 Jun 2024 12:07:29 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ee16520edf23a05d8c57ff0050569d7c4ca1ca51e35bcd811c75caba3aceb2`  
		Last Modified: Thu, 13 Jun 2024 12:07:29 GMT  
		Size: 764.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936da29acc149c56f7679c9c2e84dad693cc5336824f74f138b0d9b367b18f2f`  
		Last Modified: Thu, 13 Jun 2024 12:07:30 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e83ce712ffa3bd3572724cd9078b6f3255bf0e0b81b2e74329ae2b011d12eb85`  
		Last Modified: Thu, 13 Jun 2024 12:07:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:2186528b11f4102c57761d1a6390dd3eeb452b25939c81dfeac51dcebdb489f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3845457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2841c6ff83af934fef792ccdae62d12e858e60adfd3618a0bedf72dc3263388e`

```dockerfile
```

-	Layers:
	-	`sha256:582692a41943c9dec10385244e5aa78f2532f447bca416bd3b00d70de8ecac98`  
		Last Modified: Thu, 13 Jun 2024 12:07:27 GMT  
		Size: 3.8 MB (3814015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c260bf6b0f059f95c32fae09065799ec399cc0d9b096864fbc25b61b5fd46c18`  
		Last Modified: Thu, 13 Jun 2024 12:07:27 GMT  
		Size: 31.4 KB (31442 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.1.2`

```console
$ docker pull couchdb@sha256:27e15e61dbdf09524f3246e187affedb1074b47be78d4d589c2c74570f846466
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.1.2` - linux; amd64

```console
$ docker pull couchdb@sha256:41059a5dd8946d8f0f8ef19ce5ec7bbf958cd952bb835c900f4987771ae13dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79794247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:311845dc4a3f92cb76f6026d601476c1d4e3441478605efc3df75a55785239dd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:cce4de1623245f9f28e3365e6cf749d85dcfedddea2d6fbc963c309a40818f52 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b338562f40a7fb7360dfae935da6d7e40d2545db18bc461d9d70ec1b2b657f33`  
		Last Modified: Thu, 13 Jun 2024 01:26:49 GMT  
		Size: 27.3 MB (27337703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f71eb340d102ac139740ff648b77c7cb38fd9442aecdaed4be74dc4e9dd1d9`  
		Last Modified: Thu, 13 Jun 2024 18:14:00 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e00bbd7cddf6b459d31438ca8819a97c21bc281912b422900417af1ba50e5f1`  
		Last Modified: Thu, 13 Jun 2024 18:14:00 GMT  
		Size: 6.7 MB (6703093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd17ce531ca35a5604da44c29e8ec4542045c1026286b223ab422281ced9a2c`  
		Last Modified: Thu, 13 Jun 2024 18:14:00 GMT  
		Size: 1.0 MB (1046487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01dca656eab9f47d2b9d7eb356f55cea9843d17cd8250ac019fa0573d9e12d37`  
		Last Modified: Thu, 13 Jun 2024 18:14:01 GMT  
		Size: 80.3 KB (80311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6d8da3b179f647391910cfe8ec8c333f2a7b32b022e7e58946d89b594aa800`  
		Last Modified: Thu, 13 Jun 2024 18:14:01 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6726256ce4cb4428a09a154755ad11d2b49188c3dfb785ff690f3f0d693551`  
		Last Modified: Thu, 13 Jun 2024 18:14:03 GMT  
		Size: 44.6 MB (44619730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a298e52e4d5d211187b426881893cbe0914c1085f35270161b0f7dbc496a3a5`  
		Last Modified: Thu, 13 Jun 2024 18:14:01 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e46635e078ed8dd2c3ccbad492c22f257245a8501994d61e4445719b58c6ab`  
		Last Modified: Thu, 13 Jun 2024 18:14:02 GMT  
		Size: 762.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1957a21baf08559aabc4fc698236b5ea18db4e19f2172d4b1abcdc3b0496ace8`  
		Last Modified: Thu, 13 Jun 2024 18:14:02 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7193dc3cb422ad374cc8db19524a0d3a8e93508a4980f6105760ff8d609df3a7`  
		Last Modified: Thu, 13 Jun 2024 18:14:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.1.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:b8bcc6e0b9141acc1ff229e5d79d979be5b9811f7b204c394118d056e87c1060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:148b9cfb54806e1e04597d04d7a8d377a7c5dbc10d95326a328f6b592b773ad8`

```dockerfile
```

-	Layers:
	-	`sha256:897909373d1da9b3a0d93e7ea3eaf38ded78d0ea7b3676baf499d846d2b50341`  
		Last Modified: Thu, 13 Jun 2024 18:14:00 GMT  
		Size: 3.8 MB (3807389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55248b4e5e9c16e62266004e747bc20acdb731e439dc60e04f50a647542192af`  
		Last Modified: Thu, 13 Jun 2024 18:14:00 GMT  
		Size: 31.2 KB (31168 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.1.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:68db57a2e70a09d66c3546d771e2d3529b26cde5e1cddcaee8f6a280869e8179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74849426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ad3c5c21ecdca29c3c144df13b31e73fa6e362f48661d7af160e338598df4d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:de9a2b323e6d7d969277e7e781875e3daf3f49f2c1dcc569a1eec4f5bd789c46 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7abf9f73c7747bb840a8edcd895830e53f09498136de3015568a9cd9f5ab10ed`  
		Last Modified: Thu, 13 Jun 2024 00:44:26 GMT  
		Size: 26.1 MB (26109272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eca7c66c8588ba658ce9600ea40b6f2b5d56c06f381a970e4d0f982449ef4cc`  
		Last Modified: Thu, 13 Jun 2024 12:07:26 GMT  
		Size: 3.4 KB (3354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93eefa6ad47ebab27d37425a2dbb0a7f35fd35f08b133559ce2b2dcb9f393b6`  
		Last Modified: Thu, 13 Jun 2024 12:07:27 GMT  
		Size: 6.6 MB (6576435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a366eb898e6bb117bb755e338a551dbf46e7138ae1668de0ff15ad96787044`  
		Last Modified: Thu, 13 Jun 2024 12:07:27 GMT  
		Size: 951.4 KB (951371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2779ec1172795a161516aee295018f37f87aa1b8aec259959f3bd2316ccb6674`  
		Last Modified: Thu, 13 Jun 2024 12:07:28 GMT  
		Size: 80.2 KB (80201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963daa5ca753becf931984c6fbd766e4fa1f1368ccc08b427a44f7dfd0f3e12c`  
		Last Modified: Thu, 13 Jun 2024 12:07:28 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29944b0b0a23af78ca6c433e6bbf821eb927b3c9377a3e71cd168ddc3904345`  
		Last Modified: Thu, 13 Jun 2024 12:07:30 GMT  
		Size: 41.1 MB (41125196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20cdadb40f3bcf2c12dc0ec436654aa7a8a6320cffbb86e352fe4cf55b6da44b`  
		Last Modified: Thu, 13 Jun 2024 12:07:29 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ee16520edf23a05d8c57ff0050569d7c4ca1ca51e35bcd811c75caba3aceb2`  
		Last Modified: Thu, 13 Jun 2024 12:07:29 GMT  
		Size: 764.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936da29acc149c56f7679c9c2e84dad693cc5336824f74f138b0d9b367b18f2f`  
		Last Modified: Thu, 13 Jun 2024 12:07:30 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e83ce712ffa3bd3572724cd9078b6f3255bf0e0b81b2e74329ae2b011d12eb85`  
		Last Modified: Thu, 13 Jun 2024 12:07:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.1.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:2186528b11f4102c57761d1a6390dd3eeb452b25939c81dfeac51dcebdb489f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3845457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2841c6ff83af934fef792ccdae62d12e858e60adfd3618a0bedf72dc3263388e`

```dockerfile
```

-	Layers:
	-	`sha256:582692a41943c9dec10385244e5aa78f2532f447bca416bd3b00d70de8ecac98`  
		Last Modified: Thu, 13 Jun 2024 12:07:27 GMT  
		Size: 3.8 MB (3814015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c260bf6b0f059f95c32fae09065799ec399cc0d9b096864fbc25b61b5fd46c18`  
		Last Modified: Thu, 13 Jun 2024 12:07:27 GMT  
		Size: 31.4 KB (31442 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.2`

```console
$ docker pull couchdb@sha256:7c2f2aa20473a2dd8650d7ca4d985dee704e2836403f92f7509915f4143b0816
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `couchdb:3.2` - linux; amd64

```console
$ docker pull couchdb@sha256:6e6728e69f3c64547f76b6d84f85c6f09f7f5ad9733fd379a2b93ca0fdbd503d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.1 MB (89121435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfcbe41b03e085f024e27382b67d0f2137aec5fdc6e57b0b50f858f8aa988bb1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.2.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10197cd43e0b14690db768864a63dbce33304ccf54aadde63c906051cee6d76`  
		Last Modified: Thu, 13 Jun 2024 18:14:00 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a36573fce19c7c084183d86f908867c7767051b588b21daf8d689e34555068`  
		Last Modified: Thu, 13 Jun 2024 18:14:00 GMT  
		Size: 5.0 MB (5019736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba49485a77c28d20b9135fa5025a16ab8c5402445ed511710dff31631956b8c`  
		Last Modified: Thu, 13 Jun 2024 18:14:00 GMT  
		Size: 394.3 KB (394338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25946edfea11b2d15e056c5072ab7ec1420302c90477419b19121e37950e59a9`  
		Last Modified: Thu, 13 Jun 2024 18:14:00 GMT  
		Size: 77.9 KB (77905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903bf1fc47eb4d29c659064156cdbc7dbda9a4168c222a684ac898450c20bf37`  
		Last Modified: Thu, 13 Jun 2024 18:14:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92478e48a449b28bf86729884d869958c7a3c419f9c7a5a0b36a6faaba1e1df8`  
		Last Modified: Thu, 13 Jun 2024 18:14:02 GMT  
		Size: 52.2 MB (52188088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a298e52e4d5d211187b426881893cbe0914c1085f35270161b0f7dbc496a3a5`  
		Last Modified: Thu, 13 Jun 2024 18:14:01 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c08034f72163323f67b13a3e6af0979cf0c9ee2ac6ad49f0cdd7ffdc524decb`  
		Last Modified: Thu, 13 Jun 2024 18:14:01 GMT  
		Size: 996.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a43891b4867c8c93392e116f223eb9242668f65f4b49debd8fe4fad41a71b9`  
		Last Modified: Thu, 13 Jun 2024 18:14:01 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236bf855d2bcf02e7f4941479b94720bafa5a36aec06dfec0eb611baa2392102`  
		Last Modified: Thu, 13 Jun 2024 18:14:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:030abeb004256852dcdf5e7aab9e9da6942c31a831bc19fec7c16e7bc204f34e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3966958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e064966d81c5c18d369a26833d20341ddb870aa7055c764281c08ddf126775d`

```dockerfile
```

-	Layers:
	-	`sha256:8c6cc5fcf5a173af925aec14d086b551522cfd424fdae140c9c071ca15a9f832`  
		Last Modified: Thu, 13 Jun 2024 18:14:00 GMT  
		Size: 3.9 MB (3935939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9066f861f55ff7fcbad14bf63839a6b565c1b10a61ba1434aed853ee4e51928`  
		Last Modified: Thu, 13 Jun 2024 18:14:00 GMT  
		Size: 31.0 KB (31019 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.2.3`

```console
$ docker pull couchdb@sha256:7c2f2aa20473a2dd8650d7ca4d985dee704e2836403f92f7509915f4143b0816
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `couchdb:3.2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:6e6728e69f3c64547f76b6d84f85c6f09f7f5ad9733fd379a2b93ca0fdbd503d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.1 MB (89121435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfcbe41b03e085f024e27382b67d0f2137aec5fdc6e57b0b50f858f8aa988bb1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.2.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10197cd43e0b14690db768864a63dbce33304ccf54aadde63c906051cee6d76`  
		Last Modified: Thu, 13 Jun 2024 18:14:00 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a36573fce19c7c084183d86f908867c7767051b588b21daf8d689e34555068`  
		Last Modified: Thu, 13 Jun 2024 18:14:00 GMT  
		Size: 5.0 MB (5019736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba49485a77c28d20b9135fa5025a16ab8c5402445ed511710dff31631956b8c`  
		Last Modified: Thu, 13 Jun 2024 18:14:00 GMT  
		Size: 394.3 KB (394338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25946edfea11b2d15e056c5072ab7ec1420302c90477419b19121e37950e59a9`  
		Last Modified: Thu, 13 Jun 2024 18:14:00 GMT  
		Size: 77.9 KB (77905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903bf1fc47eb4d29c659064156cdbc7dbda9a4168c222a684ac898450c20bf37`  
		Last Modified: Thu, 13 Jun 2024 18:14:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92478e48a449b28bf86729884d869958c7a3c419f9c7a5a0b36a6faaba1e1df8`  
		Last Modified: Thu, 13 Jun 2024 18:14:02 GMT  
		Size: 52.2 MB (52188088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a298e52e4d5d211187b426881893cbe0914c1085f35270161b0f7dbc496a3a5`  
		Last Modified: Thu, 13 Jun 2024 18:14:01 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c08034f72163323f67b13a3e6af0979cf0c9ee2ac6ad49f0cdd7ffdc524decb`  
		Last Modified: Thu, 13 Jun 2024 18:14:01 GMT  
		Size: 996.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a43891b4867c8c93392e116f223eb9242668f65f4b49debd8fe4fad41a71b9`  
		Last Modified: Thu, 13 Jun 2024 18:14:01 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236bf855d2bcf02e7f4941479b94720bafa5a36aec06dfec0eb611baa2392102`  
		Last Modified: Thu, 13 Jun 2024 18:14:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.2.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:030abeb004256852dcdf5e7aab9e9da6942c31a831bc19fec7c16e7bc204f34e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3966958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e064966d81c5c18d369a26833d20341ddb870aa7055c764281c08ddf126775d`

```dockerfile
```

-	Layers:
	-	`sha256:8c6cc5fcf5a173af925aec14d086b551522cfd424fdae140c9c071ca15a9f832`  
		Last Modified: Thu, 13 Jun 2024 18:14:00 GMT  
		Size: 3.9 MB (3935939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9066f861f55ff7fcbad14bf63839a6b565c1b10a61ba1434aed853ee4e51928`  
		Last Modified: Thu, 13 Jun 2024 18:14:00 GMT  
		Size: 31.0 KB (31019 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.3`

```console
$ docker pull couchdb@sha256:160a9080142b72a6f7a5da75b144205ee5dd7196e26bf9e2d3081629b6985812
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.3` - linux; amd64

```console
$ docker pull couchdb@sha256:c89cdc3f7f520837473b7754a8baeb1d08f3f03b5fa943915cd9f8559e14e044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89654324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a509ab16806a265c9d2b39575b783c1eae7659fed59735e1cc18aa22469a2ee0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43142df726fcf366d45c3c93f3a24895bab6445dc4c85c1090d6276da5227beb`  
		Last Modified: Thu, 13 Jun 2024 18:14:08 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6c961978fc9c2b56f0621b270d3e081603c5cfcc6c6ec238c21dad9964e724`  
		Last Modified: Thu, 13 Jun 2024 18:14:08 GMT  
		Size: 5.0 MB (5019749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4957de11597fc7cd0dec3ca88038dfcc1878a98f07613e9f0795fac467f921`  
		Last Modified: Thu, 13 Jun 2024 18:14:08 GMT  
		Size: 394.3 KB (394338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b85f5c11e3c02b69bea8a19eb3b59e79ac14162cfbbe967677e99fa33ad4643`  
		Last Modified: Thu, 13 Jun 2024 18:14:08 GMT  
		Size: 77.9 KB (77917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b14f3d85b653c195c068e01e589e8c19497ea832ba678e5c8010489ceabdaf3`  
		Last Modified: Thu, 13 Jun 2024 18:14:09 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a0fdca4130e4482c57fcc0afde01b9fbb61fa8bd1d5d4feec746c3bfae199d`  
		Last Modified: Thu, 13 Jun 2024 18:14:10 GMT  
		Size: 52.7 MB (52720703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac2369969bc2e901ccc9fc8e646b66f7661cbd500a010df29c00f8474306ca7`  
		Last Modified: Thu, 13 Jun 2024 18:14:09 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093df6b4a3aef5ff8c9c244d8805a77e28a1ce86a7a2f4f9c5411cd503f7efd3`  
		Last Modified: Thu, 13 Jun 2024 18:14:09 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26057758054349e7e345e8e4e93de87aec433203bb6215b50094ff7ac56c9b34`  
		Last Modified: Thu, 13 Jun 2024 18:14:10 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdab9184d1046a7e2512bed66ef56136d32fd239048f59fb576f310aa385bef`  
		Last Modified: Thu, 13 Jun 2024 18:14:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:d5b455ac44d205b8e1641520d4f77d7077f2c5be17625fb926ef01e3b78beec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083b21df3a41588c3bfc9d9ecace7ce8f441b0d5b164389db4b97dd31c0e0b65`

```dockerfile
```

-	Layers:
	-	`sha256:7496d83c92f48f5c5e745520e03c3618ee788f8b0211c79205896b5f4cd0149e`  
		Last Modified: Thu, 13 Jun 2024 18:14:08 GMT  
		Size: 4.0 MB (3965077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae3832983f05e916813dcee907f72537e895b3d0276cd4c213507c5f824043eb`  
		Last Modified: Thu, 13 Jun 2024 18:14:08 GMT  
		Size: 31.6 KB (31609 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:804af72aa57c3e8bbb305a4e02262334bb3f0faeb7d5dc5b43cc966c17942d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88098811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db8c02a1d75e56b5a577dad6b2195d8a0d3f73a2f460b44651394820cf062042`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159e03cc188503d00f7d8bdc64b7b0f20dcfa5c824b222b12f461596bddc211d`  
		Last Modified: Thu, 13 Jun 2024 12:06:24 GMT  
		Size: 3.4 KB (3353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8320ebe945db07b51a6e3d70c295d7235513336a604b2d761c1744bfa040a2a6`  
		Last Modified: Thu, 13 Jun 2024 12:06:24 GMT  
		Size: 5.0 MB (5004125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ace86e95f1826009a0f6d44e6dbbc38e40bd7077ae50bac6a6c9da05e6e4877`  
		Last Modified: Thu, 13 Jun 2024 12:06:24 GMT  
		Size: 350.6 KB (350556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc02dc62631fc1d2bc60c371ed48534cac30dc27130ba0630ef0f4daf5cb8bc`  
		Last Modified: Thu, 13 Jun 2024 12:06:24 GMT  
		Size: 77.8 KB (77833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b4a4bc11ee2e5fe692ab7e13b96ed67ef359e8d7709a901e438f44d64b6ab4`  
		Last Modified: Thu, 13 Jun 2024 12:06:25 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6805529927fd62e453786b7281dc3886c5bdd06ed66d3bb0df2c8bf52ca0a3`  
		Last Modified: Thu, 13 Jun 2024 12:06:27 GMT  
		Size: 52.6 MB (52571728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7f005f971d165a59678360458e7ca290628e45730317bd90251081721544a6`  
		Last Modified: Thu, 13 Jun 2024 12:06:25 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8176b116135534be6ec8372585d4705a428581f7e88aa6707e0887a4b0143ab2`  
		Last Modified: Thu, 13 Jun 2024 12:06:25 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812968abeb1a11962de024a4f7ed3f7bf9a494868420a12c7832b1cb28e78808`  
		Last Modified: Thu, 13 Jun 2024 12:06:25 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebe045b6921466a0f559a27ccc4109aa0a6b9fd6a23aaa96b39e4a9d3690f78`  
		Last Modified: Thu, 13 Jun 2024 12:06:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:e8d0e00285087fcc65f7429fece6dcfcea336d8c4ede18f239c08a158ed82979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c98598aeac3e0c5ea90cbf5a3512c6e8c1e522d2c1a1cb159d3e098478847e`

```dockerfile
```

-	Layers:
	-	`sha256:6a3377cc1a509bb80dba3fd66d9ea8a001dde4dd4889dafb8f901e21b0c2047a`  
		Last Modified: Thu, 13 Jun 2024 12:06:24 GMT  
		Size: 4.0 MB (3965362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32424633f2b2ab6abc7c5cb1ab05c5b4374a6c06f99d9546a5f716545053ab1b`  
		Last Modified: Thu, 13 Jun 2024 12:06:24 GMT  
		Size: 31.9 KB (31921 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:4fdfc8c484b8a689fee25f23c47ca02bdc3ab7f0cc714377918c54148dc06213
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95382915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9205e702b9ba1b8647c89c30c636904375988fd14f8163ef1cfe07a02088a6`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:a150537fc528657f8fa98f90c4629e38f111c3c3ef60bd40c28205959899c1a3 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:64741f366161eb41a5c86810e08ceabb9f4e4b69ac16c725aa2d48f19486e1be`  
		Last Modified: Thu, 13 Jun 2024 01:22:19 GMT  
		Size: 35.3 MB (35311302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3852c5abbc985d3037df23861f3c5ff9cda64e7ab0daf054ffd7fedb261ad92d`  
		Last Modified: Thu, 13 Jun 2024 18:14:14 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3122a60c35ac4d4fb9118461bccef76774e5a69752b40ad440f8e476368c2b3d`  
		Last Modified: Thu, 13 Jun 2024 18:14:15 GMT  
		Size: 5.8 MB (5839122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf2f330b8c80511e5590fa7f12f880371c56b8981e992d4c67f892fccce9bc8`  
		Last Modified: Thu, 13 Jun 2024 18:14:14 GMT  
		Size: 446.6 KB (446599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f3bbc58deb8c0699c4a7ad68fd5c71c63d7c86bf367d0fcf7bcca2e885115a`  
		Last Modified: Thu, 13 Jun 2024 18:14:15 GMT  
		Size: 77.8 KB (77794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c65f39caa49ed72d5f4a14258ba6149da0b2477911cf0304fa70a5d563661e`  
		Last Modified: Thu, 13 Jun 2024 18:14:15 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ab6a0d309e70e2bf3d342a3b3059d120cf68c5e15c754812906a7f36fa1a4e`  
		Last Modified: Thu, 13 Jun 2024 18:14:18 GMT  
		Size: 53.7 MB (53700519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a2dd36fcaefb8a84177f04058ecd8ac0ae1a11c35e731cb01578729b979e2f`  
		Last Modified: Thu, 13 Jun 2024 18:14:16 GMT  
		Size: 383.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe688117c8b6efc252f37a38161a14eadebac0c20fdcfcacc5a83141e7a32acf`  
		Last Modified: Thu, 13 Jun 2024 18:14:16 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf565e616d54f585d9f440b472f4d0482c2c0c8c707de7484f92bda06c48c27`  
		Last Modified: Thu, 13 Jun 2024 18:14:17 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9270f647e068e9000b871d92c52ee77721ed114f39942b33f61035c3462e72e8`  
		Last Modified: Thu, 13 Jun 2024 18:14:17 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:51e884eff706bb2a3f580afff80fe53d622b4b50180cd95e24db7f77e7adbf2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4001270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28477452f11f9fab30d286e8f3758f76df82232a92cda048a298f7882b4d39d4`

```dockerfile
```

-	Layers:
	-	`sha256:9704dcf0555f56be25d306e333474fe127b5b8739a1988299ca8a1adff3c4f0a`  
		Last Modified: Thu, 13 Jun 2024 18:14:14 GMT  
		Size: 4.0 MB (3969609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bbcef6054d78175b45e16d244dc008cc11fa5720ba24fb305003f8e73e29478`  
		Last Modified: Thu, 13 Jun 2024 18:14:14 GMT  
		Size: 31.7 KB (31661 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; s390x

```console
$ docker pull couchdb@sha256:09b4b2e2499b75abd472e542832a9ad39c3b3a74175f42611276689a14c540af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86398380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24917bbd18326fe14285376a9a30651cfa62eb3ff096159b5ecbb81d63efa2c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:dbc45f2c1dc4ae2fcf0e05b8c9401406afd0f7aa3623659e470bb7d0fb97f9ec in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b9966e11fe1c4138e9aa4f0356568463c21e36009b72062413bb596e0e57738f`  
		Last Modified: Thu, 13 Jun 2024 00:48:17 GMT  
		Size: 29.7 MB (29673762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd36feb4c5f57bfea6a5a257eaace52af47fc5984ceb78220e451a521549e80`  
		Last Modified: Thu, 13 Jun 2024 05:40:06 GMT  
		Size: 3.4 KB (3353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c5455ebb092eabd0a6e9af166cf42ead0109078cd8e9fddf62226c4d18ab0a`  
		Last Modified: Thu, 13 Jun 2024 05:40:06 GMT  
		Size: 4.9 MB (4905553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19e20b81689083bec0c0fba6e1081445bb6d38bd2121508accf14e86237259c`  
		Last Modified: Thu, 13 Jun 2024 05:40:06 GMT  
		Size: 357.5 KB (357476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03632898e77801853ed03d27b69101164538d5794e6c2b790e19f2092249e718`  
		Last Modified: Thu, 13 Jun 2024 05:40:07 GMT  
		Size: 77.8 KB (77844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96f922001e502fc5317b7f262c7640dee109f0288988dce86d27ee4626560f0`  
		Last Modified: Thu, 13 Jun 2024 05:40:07 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3c8738fbddab49cdb64c861b66f16af9697726b6bbef5e63327a4e30a5c904`  
		Last Modified: Thu, 13 Jun 2024 05:40:08 GMT  
		Size: 51.4 MB (51376141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff2bd2a020f20882db2ec938239f5c6ded2e604b7e994bea60c378539adfe6c`  
		Last Modified: Thu, 13 Jun 2024 05:40:07 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0229a5de529ffd3a2d629aeed992e842e37297669111b34e04b53d062e1c2075`  
		Last Modified: Thu, 13 Jun 2024 05:40:08 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc62edd78341ad2481627387967f1377adea7259afea2b42092c03258ed7f0aa`  
		Last Modified: Thu, 13 Jun 2024 05:40:08 GMT  
		Size: 2.2 KB (2231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ce661f13c44ae354d710b3c6d2ebb233cbf63e6ad2c8a8ab19eca24c46e30d`  
		Last Modified: Thu, 13 Jun 2024 05:40:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:70a48e66fd2f3ca5f9cc7894b05e78d85e2aa31113669d77fa86b1e9340b77ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f43b3e3c655d305399e35d5b5628de175de9a4fc62f354b65c480be472df4339`

```dockerfile
```

-	Layers:
	-	`sha256:5e0abb454a86678e3ae1bed9b7178395fb80f226b06106615935e63840cecaf3`  
		Last Modified: Thu, 13 Jun 2024 05:40:06 GMT  
		Size: 4.0 MB (3964647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2b70f2c7eeacb6070d0bfe8b5916d3b41689bc55fe36ccd12fba0206e09f97e`  
		Last Modified: Thu, 13 Jun 2024 05:40:06 GMT  
		Size: 31.6 KB (31609 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.3.3`

```console
$ docker pull couchdb@sha256:160a9080142b72a6f7a5da75b144205ee5dd7196e26bf9e2d3081629b6985812
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.3.3` - linux; amd64

```console
$ docker pull couchdb@sha256:c89cdc3f7f520837473b7754a8baeb1d08f3f03b5fa943915cd9f8559e14e044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89654324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a509ab16806a265c9d2b39575b783c1eae7659fed59735e1cc18aa22469a2ee0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43142df726fcf366d45c3c93f3a24895bab6445dc4c85c1090d6276da5227beb`  
		Last Modified: Thu, 13 Jun 2024 18:14:08 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6c961978fc9c2b56f0621b270d3e081603c5cfcc6c6ec238c21dad9964e724`  
		Last Modified: Thu, 13 Jun 2024 18:14:08 GMT  
		Size: 5.0 MB (5019749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4957de11597fc7cd0dec3ca88038dfcc1878a98f07613e9f0795fac467f921`  
		Last Modified: Thu, 13 Jun 2024 18:14:08 GMT  
		Size: 394.3 KB (394338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b85f5c11e3c02b69bea8a19eb3b59e79ac14162cfbbe967677e99fa33ad4643`  
		Last Modified: Thu, 13 Jun 2024 18:14:08 GMT  
		Size: 77.9 KB (77917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b14f3d85b653c195c068e01e589e8c19497ea832ba678e5c8010489ceabdaf3`  
		Last Modified: Thu, 13 Jun 2024 18:14:09 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a0fdca4130e4482c57fcc0afde01b9fbb61fa8bd1d5d4feec746c3bfae199d`  
		Last Modified: Thu, 13 Jun 2024 18:14:10 GMT  
		Size: 52.7 MB (52720703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac2369969bc2e901ccc9fc8e646b66f7661cbd500a010df29c00f8474306ca7`  
		Last Modified: Thu, 13 Jun 2024 18:14:09 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093df6b4a3aef5ff8c9c244d8805a77e28a1ce86a7a2f4f9c5411cd503f7efd3`  
		Last Modified: Thu, 13 Jun 2024 18:14:09 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26057758054349e7e345e8e4e93de87aec433203bb6215b50094ff7ac56c9b34`  
		Last Modified: Thu, 13 Jun 2024 18:14:10 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdab9184d1046a7e2512bed66ef56136d32fd239048f59fb576f310aa385bef`  
		Last Modified: Thu, 13 Jun 2024 18:14:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:d5b455ac44d205b8e1641520d4f77d7077f2c5be17625fb926ef01e3b78beec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083b21df3a41588c3bfc9d9ecace7ce8f441b0d5b164389db4b97dd31c0e0b65`

```dockerfile
```

-	Layers:
	-	`sha256:7496d83c92f48f5c5e745520e03c3618ee788f8b0211c79205896b5f4cd0149e`  
		Last Modified: Thu, 13 Jun 2024 18:14:08 GMT  
		Size: 4.0 MB (3965077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae3832983f05e916813dcee907f72537e895b3d0276cd4c213507c5f824043eb`  
		Last Modified: Thu, 13 Jun 2024 18:14:08 GMT  
		Size: 31.6 KB (31609 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:804af72aa57c3e8bbb305a4e02262334bb3f0faeb7d5dc5b43cc966c17942d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88098811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db8c02a1d75e56b5a577dad6b2195d8a0d3f73a2f460b44651394820cf062042`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159e03cc188503d00f7d8bdc64b7b0f20dcfa5c824b222b12f461596bddc211d`  
		Last Modified: Thu, 13 Jun 2024 12:06:24 GMT  
		Size: 3.4 KB (3353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8320ebe945db07b51a6e3d70c295d7235513336a604b2d761c1744bfa040a2a6`  
		Last Modified: Thu, 13 Jun 2024 12:06:24 GMT  
		Size: 5.0 MB (5004125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ace86e95f1826009a0f6d44e6dbbc38e40bd7077ae50bac6a6c9da05e6e4877`  
		Last Modified: Thu, 13 Jun 2024 12:06:24 GMT  
		Size: 350.6 KB (350556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc02dc62631fc1d2bc60c371ed48534cac30dc27130ba0630ef0f4daf5cb8bc`  
		Last Modified: Thu, 13 Jun 2024 12:06:24 GMT  
		Size: 77.8 KB (77833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b4a4bc11ee2e5fe692ab7e13b96ed67ef359e8d7709a901e438f44d64b6ab4`  
		Last Modified: Thu, 13 Jun 2024 12:06:25 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6805529927fd62e453786b7281dc3886c5bdd06ed66d3bb0df2c8bf52ca0a3`  
		Last Modified: Thu, 13 Jun 2024 12:06:27 GMT  
		Size: 52.6 MB (52571728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7f005f971d165a59678360458e7ca290628e45730317bd90251081721544a6`  
		Last Modified: Thu, 13 Jun 2024 12:06:25 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8176b116135534be6ec8372585d4705a428581f7e88aa6707e0887a4b0143ab2`  
		Last Modified: Thu, 13 Jun 2024 12:06:25 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812968abeb1a11962de024a4f7ed3f7bf9a494868420a12c7832b1cb28e78808`  
		Last Modified: Thu, 13 Jun 2024 12:06:25 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebe045b6921466a0f559a27ccc4109aa0a6b9fd6a23aaa96b39e4a9d3690f78`  
		Last Modified: Thu, 13 Jun 2024 12:06:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:e8d0e00285087fcc65f7429fece6dcfcea336d8c4ede18f239c08a158ed82979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c98598aeac3e0c5ea90cbf5a3512c6e8c1e522d2c1a1cb159d3e098478847e`

```dockerfile
```

-	Layers:
	-	`sha256:6a3377cc1a509bb80dba3fd66d9ea8a001dde4dd4889dafb8f901e21b0c2047a`  
		Last Modified: Thu, 13 Jun 2024 12:06:24 GMT  
		Size: 4.0 MB (3965362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32424633f2b2ab6abc7c5cb1ab05c5b4374a6c06f99d9546a5f716545053ab1b`  
		Last Modified: Thu, 13 Jun 2024 12:06:24 GMT  
		Size: 31.9 KB (31921 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:4fdfc8c484b8a689fee25f23c47ca02bdc3ab7f0cc714377918c54148dc06213
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95382915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9205e702b9ba1b8647c89c30c636904375988fd14f8163ef1cfe07a02088a6`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:a150537fc528657f8fa98f90c4629e38f111c3c3ef60bd40c28205959899c1a3 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:64741f366161eb41a5c86810e08ceabb9f4e4b69ac16c725aa2d48f19486e1be`  
		Last Modified: Thu, 13 Jun 2024 01:22:19 GMT  
		Size: 35.3 MB (35311302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3852c5abbc985d3037df23861f3c5ff9cda64e7ab0daf054ffd7fedb261ad92d`  
		Last Modified: Thu, 13 Jun 2024 18:14:14 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3122a60c35ac4d4fb9118461bccef76774e5a69752b40ad440f8e476368c2b3d`  
		Last Modified: Thu, 13 Jun 2024 18:14:15 GMT  
		Size: 5.8 MB (5839122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf2f330b8c80511e5590fa7f12f880371c56b8981e992d4c67f892fccce9bc8`  
		Last Modified: Thu, 13 Jun 2024 18:14:14 GMT  
		Size: 446.6 KB (446599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f3bbc58deb8c0699c4a7ad68fd5c71c63d7c86bf367d0fcf7bcca2e885115a`  
		Last Modified: Thu, 13 Jun 2024 18:14:15 GMT  
		Size: 77.8 KB (77794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c65f39caa49ed72d5f4a14258ba6149da0b2477911cf0304fa70a5d563661e`  
		Last Modified: Thu, 13 Jun 2024 18:14:15 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ab6a0d309e70e2bf3d342a3b3059d120cf68c5e15c754812906a7f36fa1a4e`  
		Last Modified: Thu, 13 Jun 2024 18:14:18 GMT  
		Size: 53.7 MB (53700519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a2dd36fcaefb8a84177f04058ecd8ac0ae1a11c35e731cb01578729b979e2f`  
		Last Modified: Thu, 13 Jun 2024 18:14:16 GMT  
		Size: 383.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe688117c8b6efc252f37a38161a14eadebac0c20fdcfcacc5a83141e7a32acf`  
		Last Modified: Thu, 13 Jun 2024 18:14:16 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf565e616d54f585d9f440b472f4d0482c2c0c8c707de7484f92bda06c48c27`  
		Last Modified: Thu, 13 Jun 2024 18:14:17 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9270f647e068e9000b871d92c52ee77721ed114f39942b33f61035c3462e72e8`  
		Last Modified: Thu, 13 Jun 2024 18:14:17 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:51e884eff706bb2a3f580afff80fe53d622b4b50180cd95e24db7f77e7adbf2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4001270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28477452f11f9fab30d286e8f3758f76df82232a92cda048a298f7882b4d39d4`

```dockerfile
```

-	Layers:
	-	`sha256:9704dcf0555f56be25d306e333474fe127b5b8739a1988299ca8a1adff3c4f0a`  
		Last Modified: Thu, 13 Jun 2024 18:14:14 GMT  
		Size: 4.0 MB (3969609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bbcef6054d78175b45e16d244dc008cc11fa5720ba24fb305003f8e73e29478`  
		Last Modified: Thu, 13 Jun 2024 18:14:14 GMT  
		Size: 31.7 KB (31661 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; s390x

```console
$ docker pull couchdb@sha256:09b4b2e2499b75abd472e542832a9ad39c3b3a74175f42611276689a14c540af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86398380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24917bbd18326fe14285376a9a30651cfa62eb3ff096159b5ecbb81d63efa2c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:dbc45f2c1dc4ae2fcf0e05b8c9401406afd0f7aa3623659e470bb7d0fb97f9ec in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b9966e11fe1c4138e9aa4f0356568463c21e36009b72062413bb596e0e57738f`  
		Last Modified: Thu, 13 Jun 2024 00:48:17 GMT  
		Size: 29.7 MB (29673762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd36feb4c5f57bfea6a5a257eaace52af47fc5984ceb78220e451a521549e80`  
		Last Modified: Thu, 13 Jun 2024 05:40:06 GMT  
		Size: 3.4 KB (3353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c5455ebb092eabd0a6e9af166cf42ead0109078cd8e9fddf62226c4d18ab0a`  
		Last Modified: Thu, 13 Jun 2024 05:40:06 GMT  
		Size: 4.9 MB (4905553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19e20b81689083bec0c0fba6e1081445bb6d38bd2121508accf14e86237259c`  
		Last Modified: Thu, 13 Jun 2024 05:40:06 GMT  
		Size: 357.5 KB (357476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03632898e77801853ed03d27b69101164538d5794e6c2b790e19f2092249e718`  
		Last Modified: Thu, 13 Jun 2024 05:40:07 GMT  
		Size: 77.8 KB (77844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96f922001e502fc5317b7f262c7640dee109f0288988dce86d27ee4626560f0`  
		Last Modified: Thu, 13 Jun 2024 05:40:07 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3c8738fbddab49cdb64c861b66f16af9697726b6bbef5e63327a4e30a5c904`  
		Last Modified: Thu, 13 Jun 2024 05:40:08 GMT  
		Size: 51.4 MB (51376141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff2bd2a020f20882db2ec938239f5c6ded2e604b7e994bea60c378539adfe6c`  
		Last Modified: Thu, 13 Jun 2024 05:40:07 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0229a5de529ffd3a2d629aeed992e842e37297669111b34e04b53d062e1c2075`  
		Last Modified: Thu, 13 Jun 2024 05:40:08 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc62edd78341ad2481627387967f1377adea7259afea2b42092c03258ed7f0aa`  
		Last Modified: Thu, 13 Jun 2024 05:40:08 GMT  
		Size: 2.2 KB (2231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ce661f13c44ae354d710b3c6d2ebb233cbf63e6ad2c8a8ab19eca24c46e30d`  
		Last Modified: Thu, 13 Jun 2024 05:40:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:70a48e66fd2f3ca5f9cc7894b05e78d85e2aa31113669d77fa86b1e9340b77ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f43b3e3c655d305399e35d5b5628de175de9a4fc62f354b65c480be472df4339`

```dockerfile
```

-	Layers:
	-	`sha256:5e0abb454a86678e3ae1bed9b7178395fb80f226b06106615935e63840cecaf3`  
		Last Modified: Thu, 13 Jun 2024 05:40:06 GMT  
		Size: 4.0 MB (3964647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2b70f2c7eeacb6070d0bfe8b5916d3b41689bc55fe36ccd12fba0206e09f97e`  
		Last Modified: Thu, 13 Jun 2024 05:40:06 GMT  
		Size: 31.6 KB (31609 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:160a9080142b72a6f7a5da75b144205ee5dd7196e26bf9e2d3081629b6985812
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:c89cdc3f7f520837473b7754a8baeb1d08f3f03b5fa943915cd9f8559e14e044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89654324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a509ab16806a265c9d2b39575b783c1eae7659fed59735e1cc18aa22469a2ee0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43142df726fcf366d45c3c93f3a24895bab6445dc4c85c1090d6276da5227beb`  
		Last Modified: Thu, 13 Jun 2024 18:14:08 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6c961978fc9c2b56f0621b270d3e081603c5cfcc6c6ec238c21dad9964e724`  
		Last Modified: Thu, 13 Jun 2024 18:14:08 GMT  
		Size: 5.0 MB (5019749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4957de11597fc7cd0dec3ca88038dfcc1878a98f07613e9f0795fac467f921`  
		Last Modified: Thu, 13 Jun 2024 18:14:08 GMT  
		Size: 394.3 KB (394338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b85f5c11e3c02b69bea8a19eb3b59e79ac14162cfbbe967677e99fa33ad4643`  
		Last Modified: Thu, 13 Jun 2024 18:14:08 GMT  
		Size: 77.9 KB (77917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b14f3d85b653c195c068e01e589e8c19497ea832ba678e5c8010489ceabdaf3`  
		Last Modified: Thu, 13 Jun 2024 18:14:09 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a0fdca4130e4482c57fcc0afde01b9fbb61fa8bd1d5d4feec746c3bfae199d`  
		Last Modified: Thu, 13 Jun 2024 18:14:10 GMT  
		Size: 52.7 MB (52720703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac2369969bc2e901ccc9fc8e646b66f7661cbd500a010df29c00f8474306ca7`  
		Last Modified: Thu, 13 Jun 2024 18:14:09 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093df6b4a3aef5ff8c9c244d8805a77e28a1ce86a7a2f4f9c5411cd503f7efd3`  
		Last Modified: Thu, 13 Jun 2024 18:14:09 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26057758054349e7e345e8e4e93de87aec433203bb6215b50094ff7ac56c9b34`  
		Last Modified: Thu, 13 Jun 2024 18:14:10 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdab9184d1046a7e2512bed66ef56136d32fd239048f59fb576f310aa385bef`  
		Last Modified: Thu, 13 Jun 2024 18:14:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:d5b455ac44d205b8e1641520d4f77d7077f2c5be17625fb926ef01e3b78beec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083b21df3a41588c3bfc9d9ecace7ce8f441b0d5b164389db4b97dd31c0e0b65`

```dockerfile
```

-	Layers:
	-	`sha256:7496d83c92f48f5c5e745520e03c3618ee788f8b0211c79205896b5f4cd0149e`  
		Last Modified: Thu, 13 Jun 2024 18:14:08 GMT  
		Size: 4.0 MB (3965077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae3832983f05e916813dcee907f72537e895b3d0276cd4c213507c5f824043eb`  
		Last Modified: Thu, 13 Jun 2024 18:14:08 GMT  
		Size: 31.6 KB (31609 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:804af72aa57c3e8bbb305a4e02262334bb3f0faeb7d5dc5b43cc966c17942d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88098811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db8c02a1d75e56b5a577dad6b2195d8a0d3f73a2f460b44651394820cf062042`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159e03cc188503d00f7d8bdc64b7b0f20dcfa5c824b222b12f461596bddc211d`  
		Last Modified: Thu, 13 Jun 2024 12:06:24 GMT  
		Size: 3.4 KB (3353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8320ebe945db07b51a6e3d70c295d7235513336a604b2d761c1744bfa040a2a6`  
		Last Modified: Thu, 13 Jun 2024 12:06:24 GMT  
		Size: 5.0 MB (5004125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ace86e95f1826009a0f6d44e6dbbc38e40bd7077ae50bac6a6c9da05e6e4877`  
		Last Modified: Thu, 13 Jun 2024 12:06:24 GMT  
		Size: 350.6 KB (350556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc02dc62631fc1d2bc60c371ed48534cac30dc27130ba0630ef0f4daf5cb8bc`  
		Last Modified: Thu, 13 Jun 2024 12:06:24 GMT  
		Size: 77.8 KB (77833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b4a4bc11ee2e5fe692ab7e13b96ed67ef359e8d7709a901e438f44d64b6ab4`  
		Last Modified: Thu, 13 Jun 2024 12:06:25 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6805529927fd62e453786b7281dc3886c5bdd06ed66d3bb0df2c8bf52ca0a3`  
		Last Modified: Thu, 13 Jun 2024 12:06:27 GMT  
		Size: 52.6 MB (52571728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7f005f971d165a59678360458e7ca290628e45730317bd90251081721544a6`  
		Last Modified: Thu, 13 Jun 2024 12:06:25 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8176b116135534be6ec8372585d4705a428581f7e88aa6707e0887a4b0143ab2`  
		Last Modified: Thu, 13 Jun 2024 12:06:25 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812968abeb1a11962de024a4f7ed3f7bf9a494868420a12c7832b1cb28e78808`  
		Last Modified: Thu, 13 Jun 2024 12:06:25 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebe045b6921466a0f559a27ccc4109aa0a6b9fd6a23aaa96b39e4a9d3690f78`  
		Last Modified: Thu, 13 Jun 2024 12:06:26 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:e8d0e00285087fcc65f7429fece6dcfcea336d8c4ede18f239c08a158ed82979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c98598aeac3e0c5ea90cbf5a3512c6e8c1e522d2c1a1cb159d3e098478847e`

```dockerfile
```

-	Layers:
	-	`sha256:6a3377cc1a509bb80dba3fd66d9ea8a001dde4dd4889dafb8f901e21b0c2047a`  
		Last Modified: Thu, 13 Jun 2024 12:06:24 GMT  
		Size: 4.0 MB (3965362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32424633f2b2ab6abc7c5cb1ab05c5b4374a6c06f99d9546a5f716545053ab1b`  
		Last Modified: Thu, 13 Jun 2024 12:06:24 GMT  
		Size: 31.9 KB (31921 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:4fdfc8c484b8a689fee25f23c47ca02bdc3ab7f0cc714377918c54148dc06213
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95382915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9205e702b9ba1b8647c89c30c636904375988fd14f8163ef1cfe07a02088a6`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:a150537fc528657f8fa98f90c4629e38f111c3c3ef60bd40c28205959899c1a3 in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:64741f366161eb41a5c86810e08ceabb9f4e4b69ac16c725aa2d48f19486e1be`  
		Last Modified: Thu, 13 Jun 2024 01:22:19 GMT  
		Size: 35.3 MB (35311302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3852c5abbc985d3037df23861f3c5ff9cda64e7ab0daf054ffd7fedb261ad92d`  
		Last Modified: Thu, 13 Jun 2024 18:14:14 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3122a60c35ac4d4fb9118461bccef76774e5a69752b40ad440f8e476368c2b3d`  
		Last Modified: Thu, 13 Jun 2024 18:14:15 GMT  
		Size: 5.8 MB (5839122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf2f330b8c80511e5590fa7f12f880371c56b8981e992d4c67f892fccce9bc8`  
		Last Modified: Thu, 13 Jun 2024 18:14:14 GMT  
		Size: 446.6 KB (446599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f3bbc58deb8c0699c4a7ad68fd5c71c63d7c86bf367d0fcf7bcca2e885115a`  
		Last Modified: Thu, 13 Jun 2024 18:14:15 GMT  
		Size: 77.8 KB (77794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c65f39caa49ed72d5f4a14258ba6149da0b2477911cf0304fa70a5d563661e`  
		Last Modified: Thu, 13 Jun 2024 18:14:15 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ab6a0d309e70e2bf3d342a3b3059d120cf68c5e15c754812906a7f36fa1a4e`  
		Last Modified: Thu, 13 Jun 2024 18:14:18 GMT  
		Size: 53.7 MB (53700519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a2dd36fcaefb8a84177f04058ecd8ac0ae1a11c35e731cb01578729b979e2f`  
		Last Modified: Thu, 13 Jun 2024 18:14:16 GMT  
		Size: 383.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe688117c8b6efc252f37a38161a14eadebac0c20fdcfcacc5a83141e7a32acf`  
		Last Modified: Thu, 13 Jun 2024 18:14:16 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf565e616d54f585d9f440b472f4d0482c2c0c8c707de7484f92bda06c48c27`  
		Last Modified: Thu, 13 Jun 2024 18:14:17 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9270f647e068e9000b871d92c52ee77721ed114f39942b33f61035c3462e72e8`  
		Last Modified: Thu, 13 Jun 2024 18:14:17 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:51e884eff706bb2a3f580afff80fe53d622b4b50180cd95e24db7f77e7adbf2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4001270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28477452f11f9fab30d286e8f3758f76df82232a92cda048a298f7882b4d39d4`

```dockerfile
```

-	Layers:
	-	`sha256:9704dcf0555f56be25d306e333474fe127b5b8739a1988299ca8a1adff3c4f0a`  
		Last Modified: Thu, 13 Jun 2024 18:14:14 GMT  
		Size: 4.0 MB (3969609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bbcef6054d78175b45e16d244dc008cc11fa5720ba24fb305003f8e73e29478`  
		Last Modified: Thu, 13 Jun 2024 18:14:14 GMT  
		Size: 31.7 KB (31661 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:09b4b2e2499b75abd472e542832a9ad39c3b3a74175f42611276689a14c540af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86398380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24917bbd18326fe14285376a9a30651cfa62eb3ff096159b5ecbb81d63efa2c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:dbc45f2c1dc4ae2fcf0e05b8c9401406afd0f7aa3623659e470bb7d0fb97f9ec in / 
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["bash"]
# Tue, 05 Dec 2023 19:33:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 05 Dec 2023 19:33:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 05 Dec 2023 19:33:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 05 Dec 2023 19:33:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 05 Dec 2023 19:33:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 05 Dec 2023 19:33:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b9966e11fe1c4138e9aa4f0356568463c21e36009b72062413bb596e0e57738f`  
		Last Modified: Thu, 13 Jun 2024 00:48:17 GMT  
		Size: 29.7 MB (29673762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd36feb4c5f57bfea6a5a257eaace52af47fc5984ceb78220e451a521549e80`  
		Last Modified: Thu, 13 Jun 2024 05:40:06 GMT  
		Size: 3.4 KB (3353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c5455ebb092eabd0a6e9af166cf42ead0109078cd8e9fddf62226c4d18ab0a`  
		Last Modified: Thu, 13 Jun 2024 05:40:06 GMT  
		Size: 4.9 MB (4905553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19e20b81689083bec0c0fba6e1081445bb6d38bd2121508accf14e86237259c`  
		Last Modified: Thu, 13 Jun 2024 05:40:06 GMT  
		Size: 357.5 KB (357476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03632898e77801853ed03d27b69101164538d5794e6c2b790e19f2092249e718`  
		Last Modified: Thu, 13 Jun 2024 05:40:07 GMT  
		Size: 77.8 KB (77844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96f922001e502fc5317b7f262c7640dee109f0288988dce86d27ee4626560f0`  
		Last Modified: Thu, 13 Jun 2024 05:40:07 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3c8738fbddab49cdb64c861b66f16af9697726b6bbef5e63327a4e30a5c904`  
		Last Modified: Thu, 13 Jun 2024 05:40:08 GMT  
		Size: 51.4 MB (51376141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff2bd2a020f20882db2ec938239f5c6ded2e604b7e994bea60c378539adfe6c`  
		Last Modified: Thu, 13 Jun 2024 05:40:07 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0229a5de529ffd3a2d629aeed992e842e37297669111b34e04b53d062e1c2075`  
		Last Modified: Thu, 13 Jun 2024 05:40:08 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc62edd78341ad2481627387967f1377adea7259afea2b42092c03258ed7f0aa`  
		Last Modified: Thu, 13 Jun 2024 05:40:08 GMT  
		Size: 2.2 KB (2231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ce661f13c44ae354d710b3c6d2ebb233cbf63e6ad2c8a8ab19eca24c46e30d`  
		Last Modified: Thu, 13 Jun 2024 05:40:08 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:70a48e66fd2f3ca5f9cc7894b05e78d85e2aa31113669d77fa86b1e9340b77ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f43b3e3c655d305399e35d5b5628de175de9a4fc62f354b65c480be472df4339`

```dockerfile
```

-	Layers:
	-	`sha256:5e0abb454a86678e3ae1bed9b7178395fb80f226b06106615935e63840cecaf3`  
		Last Modified: Thu, 13 Jun 2024 05:40:06 GMT  
		Size: 4.0 MB (3964647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2b70f2c7eeacb6070d0bfe8b5916d3b41689bc55fe36ccd12fba0206e09f97e`  
		Last Modified: Thu, 13 Jun 2024 05:40:06 GMT  
		Size: 31.6 KB (31609 bytes)  
		MIME: application/vnd.in-toto+json
