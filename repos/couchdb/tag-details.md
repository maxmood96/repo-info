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
$ docker pull couchdb@sha256:490e59db6149ce673734c1268a055e8ebd897b57a8d0b1f1b4bbc4264104cc9d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:2` - linux; amd64

```console
$ docker pull couchdb@sha256:80383de74598b295e382544e13a53574226d05e3b8f6293bf56f27f00940fd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84169041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e309f7c1828f7087e95cf0ba19507a4aeb02f7a884f620ab16c0dc9461776b61`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:232125261662ceeb0126b96defe05092c121fecd55c99db5f76a03ab0c87d07e in / 
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
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:789bca57d694bdff72d9fcb5bdc3f4684b63dee11402ed28245ae1c578d62ba3`  
		Last Modified: Tue, 13 Feb 2024 00:43:30 GMT  
		Size: 27.2 MB (27188190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b91f61f6301a3dec96508b2c97786e6f5f0221dc62a231d7316bcfe19957ad`  
		Last Modified: Tue, 13 Feb 2024 01:53:39 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e80f4954bc9432fc6237e3be6e8a331bfd1b13a6b61800448576c40ccd224e`  
		Last Modified: Tue, 13 Feb 2024 01:53:40 GMT  
		Size: 6.7 MB (6703566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122336ace0d79dce4d064680ffabce183a4c8c235e7e6346793cf0d3a6c4b400`  
		Last Modified: Tue, 13 Feb 2024 01:53:39 GMT  
		Size: 1.0 MB (1046479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beafd30c1a1026c0c414fc2590ac27d58dcc39e6e1275274e22eedf4c79824ca`  
		Last Modified: Tue, 13 Feb 2024 01:53:40 GMT  
		Size: 80.3 KB (80343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35cce46b847671d9b45e66ba1b59d3f2920f4edce1af98755f368912317ea04`  
		Last Modified: Tue, 13 Feb 2024 01:53:40 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feec791ad121e40adb3a59c351541070d7cf03a64a769c045a484dfa8a657946`  
		Last Modified: Tue, 13 Feb 2024 01:53:41 GMT  
		Size: 49.1 MB (49143540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957fb429ea1153c66d0457d7d04e089fe794aecfce225be2821b07e8d819e32f`  
		Last Modified: Tue, 13 Feb 2024 01:53:41 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92692d14e642732ac1689b0040df870af19b16dc235e76f0ec7d1d87fff51fc2`  
		Last Modified: Tue, 13 Feb 2024 01:53:41 GMT  
		Size: 762.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533f04efcf37f2520a6963fc68822980973daa2e88843825b34ef6421ddd64d1`  
		Last Modified: Tue, 13 Feb 2024 01:53:41 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6915c5098de94f2a090712fd944ad6b77e6540bf6adb78234fa51506bc43fc88`  
		Last Modified: Tue, 13 Feb 2024 01:53:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:2` - unknown; unknown

```console
$ docker pull couchdb@sha256:1bbf09eb5beff904b1ff1c4be6e52f171b638f012eff2fb479a23aefd9f1bbcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3549045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f473cac918935ae1aedf5b9eb875e41c192e2ecccd3a34d6a6f394e3928e993`

```dockerfile
```

-	Layers:
	-	`sha256:f34fd1af00b3d6cbc831ce1bc89dc79aa7dda3b23e8bad8a1bc83dfda62d3e97`  
		Last Modified: Tue, 13 Feb 2024 01:53:40 GMT  
		Size: 3.5 MB (3517463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e80ecd9d59ec42815b78c137040582373947384d2371eef2ceee6396a604897`  
		Last Modified: Tue, 13 Feb 2024 01:53:40 GMT  
		Size: 31.6 KB (31582 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:ccabf00dced68849dd5aed8fd479356aa4698e656f8f52aed38a7bcc0fc55494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72615460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb5836c03fcb70932bd31f00b9924302cee48d27f32806676201d396d2f5b41`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:de90e50e142aa92c29d5128e1cd025fd5c5b91f879a19a06a8b49451a4e6afb9 in / 
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
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:42641f7bf1512c205041cf7899e52e2185e49bcd6cfa0cb8ebfc73e3009221b7`  
		Last Modified: Wed, 31 Jan 2024 22:49:34 GMT  
		Size: 26.0 MB (25970227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195a5c7275e6e739113fc1bba1a86979ba02e51ce0e8d2809e4b0c91a949e951`  
		Last Modified: Thu, 01 Feb 2024 14:06:58 GMT  
		Size: 3.4 KB (3354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea98b1217ba4ee31a07f6858e2e3ab54a2ec3c90285fdf0e4a66d2c62420122`  
		Last Modified: Thu, 01 Feb 2024 14:06:59 GMT  
		Size: 6.6 MB (6576636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219447fdce8a83af3658eef95dae3b2b2d90ed96f8bead499713f344aefacde9`  
		Last Modified: Thu, 01 Feb 2024 14:06:58 GMT  
		Size: 951.3 KB (951318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe587eefa88b70481c6778e6e0081384c362b771571e970811dd6a5cf20a4f9`  
		Last Modified: Thu, 01 Feb 2024 14:06:59 GMT  
		Size: 80.2 KB (80182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f76842143d873297730e3c137e579618b8da303c12c9a4bf5ee85bfcddf1b17`  
		Last Modified: Thu, 01 Feb 2024 14:34:04 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93628300ad755a96bf9e7cb0af15cfafe6ab9b447c4fa663e4dc70a39084f50`  
		Last Modified: Thu, 01 Feb 2024 14:34:06 GMT  
		Size: 39.0 MB (39030149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef517268298c93c834923f5c12381f4fe0b5aaa5a6707ba9f149a0078e265153`  
		Last Modified: Thu, 01 Feb 2024 14:34:05 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fcddb3461b2b266c018d63ae3082c427dd63d5492f8ec149371d0da7a5ba5e5`  
		Last Modified: Thu, 01 Feb 2024 14:34:04 GMT  
		Size: 763.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4319d3dbd76421aff43c346568ab2edd1948b58981009feec9987db61bec1e0b`  
		Last Modified: Thu, 01 Feb 2024 14:34:05 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994152cee51d4da15621f1b85714b901d2065bb1862c0b734a62a462126ed018`  
		Last Modified: Thu, 01 Feb 2024 14:34:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:2` - unknown; unknown

```console
$ docker pull couchdb@sha256:ffe866e48a2620ba5909124aa30d335b6fee05cf68ee5ac6fa1e51b2d4c9ad11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2941978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07459d9c1dade9a0559d111ec0726431b3edfa06cfd76efcfd0b035ab123c733`

```dockerfile
```

-	Layers:
	-	`sha256:9debaf35ca6d7ce41755e63d171087079e91d35dea53f3b67a4a1359864a8fbe`  
		Last Modified: Thu, 01 Feb 2024 14:34:04 GMT  
		Size: 2.9 MB (2910563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abfb654d93d66c4e1dc690a542bf6d9ef45a92acd908f63be760504bc43dc119`  
		Last Modified: Thu, 01 Feb 2024 14:34:04 GMT  
		Size: 31.4 KB (31415 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:2.3`

```console
$ docker pull couchdb@sha256:490e59db6149ce673734c1268a055e8ebd897b57a8d0b1f1b4bbc4264104cc9d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:80383de74598b295e382544e13a53574226d05e3b8f6293bf56f27f00940fd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84169041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e309f7c1828f7087e95cf0ba19507a4aeb02f7a884f620ab16c0dc9461776b61`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:232125261662ceeb0126b96defe05092c121fecd55c99db5f76a03ab0c87d07e in / 
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
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:789bca57d694bdff72d9fcb5bdc3f4684b63dee11402ed28245ae1c578d62ba3`  
		Last Modified: Tue, 13 Feb 2024 00:43:30 GMT  
		Size: 27.2 MB (27188190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b91f61f6301a3dec96508b2c97786e6f5f0221dc62a231d7316bcfe19957ad`  
		Last Modified: Tue, 13 Feb 2024 01:53:39 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e80f4954bc9432fc6237e3be6e8a331bfd1b13a6b61800448576c40ccd224e`  
		Last Modified: Tue, 13 Feb 2024 01:53:40 GMT  
		Size: 6.7 MB (6703566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122336ace0d79dce4d064680ffabce183a4c8c235e7e6346793cf0d3a6c4b400`  
		Last Modified: Tue, 13 Feb 2024 01:53:39 GMT  
		Size: 1.0 MB (1046479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beafd30c1a1026c0c414fc2590ac27d58dcc39e6e1275274e22eedf4c79824ca`  
		Last Modified: Tue, 13 Feb 2024 01:53:40 GMT  
		Size: 80.3 KB (80343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35cce46b847671d9b45e66ba1b59d3f2920f4edce1af98755f368912317ea04`  
		Last Modified: Tue, 13 Feb 2024 01:53:40 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feec791ad121e40adb3a59c351541070d7cf03a64a769c045a484dfa8a657946`  
		Last Modified: Tue, 13 Feb 2024 01:53:41 GMT  
		Size: 49.1 MB (49143540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957fb429ea1153c66d0457d7d04e089fe794aecfce225be2821b07e8d819e32f`  
		Last Modified: Tue, 13 Feb 2024 01:53:41 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92692d14e642732ac1689b0040df870af19b16dc235e76f0ec7d1d87fff51fc2`  
		Last Modified: Tue, 13 Feb 2024 01:53:41 GMT  
		Size: 762.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533f04efcf37f2520a6963fc68822980973daa2e88843825b34ef6421ddd64d1`  
		Last Modified: Tue, 13 Feb 2024 01:53:41 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6915c5098de94f2a090712fd944ad6b77e6540bf6adb78234fa51506bc43fc88`  
		Last Modified: Tue, 13 Feb 2024 01:53:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:2.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:1bbf09eb5beff904b1ff1c4be6e52f171b638f012eff2fb479a23aefd9f1bbcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3549045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f473cac918935ae1aedf5b9eb875e41c192e2ecccd3a34d6a6f394e3928e993`

```dockerfile
```

-	Layers:
	-	`sha256:f34fd1af00b3d6cbc831ce1bc89dc79aa7dda3b23e8bad8a1bc83dfda62d3e97`  
		Last Modified: Tue, 13 Feb 2024 01:53:40 GMT  
		Size: 3.5 MB (3517463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e80ecd9d59ec42815b78c137040582373947384d2371eef2ceee6396a604897`  
		Last Modified: Tue, 13 Feb 2024 01:53:40 GMT  
		Size: 31.6 KB (31582 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:2.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:ccabf00dced68849dd5aed8fd479356aa4698e656f8f52aed38a7bcc0fc55494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72615460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb5836c03fcb70932bd31f00b9924302cee48d27f32806676201d396d2f5b41`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:de90e50e142aa92c29d5128e1cd025fd5c5b91f879a19a06a8b49451a4e6afb9 in / 
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
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:42641f7bf1512c205041cf7899e52e2185e49bcd6cfa0cb8ebfc73e3009221b7`  
		Last Modified: Wed, 31 Jan 2024 22:49:34 GMT  
		Size: 26.0 MB (25970227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195a5c7275e6e739113fc1bba1a86979ba02e51ce0e8d2809e4b0c91a949e951`  
		Last Modified: Thu, 01 Feb 2024 14:06:58 GMT  
		Size: 3.4 KB (3354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea98b1217ba4ee31a07f6858e2e3ab54a2ec3c90285fdf0e4a66d2c62420122`  
		Last Modified: Thu, 01 Feb 2024 14:06:59 GMT  
		Size: 6.6 MB (6576636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219447fdce8a83af3658eef95dae3b2b2d90ed96f8bead499713f344aefacde9`  
		Last Modified: Thu, 01 Feb 2024 14:06:58 GMT  
		Size: 951.3 KB (951318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe587eefa88b70481c6778e6e0081384c362b771571e970811dd6a5cf20a4f9`  
		Last Modified: Thu, 01 Feb 2024 14:06:59 GMT  
		Size: 80.2 KB (80182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f76842143d873297730e3c137e579618b8da303c12c9a4bf5ee85bfcddf1b17`  
		Last Modified: Thu, 01 Feb 2024 14:34:04 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93628300ad755a96bf9e7cb0af15cfafe6ab9b447c4fa663e4dc70a39084f50`  
		Last Modified: Thu, 01 Feb 2024 14:34:06 GMT  
		Size: 39.0 MB (39030149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef517268298c93c834923f5c12381f4fe0b5aaa5a6707ba9f149a0078e265153`  
		Last Modified: Thu, 01 Feb 2024 14:34:05 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fcddb3461b2b266c018d63ae3082c427dd63d5492f8ec149371d0da7a5ba5e5`  
		Last Modified: Thu, 01 Feb 2024 14:34:04 GMT  
		Size: 763.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4319d3dbd76421aff43c346568ab2edd1948b58981009feec9987db61bec1e0b`  
		Last Modified: Thu, 01 Feb 2024 14:34:05 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994152cee51d4da15621f1b85714b901d2065bb1862c0b734a62a462126ed018`  
		Last Modified: Thu, 01 Feb 2024 14:34:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:2.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:ffe866e48a2620ba5909124aa30d335b6fee05cf68ee5ac6fa1e51b2d4c9ad11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2941978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07459d9c1dade9a0559d111ec0726431b3edfa06cfd76efcfd0b035ab123c733`

```dockerfile
```

-	Layers:
	-	`sha256:9debaf35ca6d7ce41755e63d171087079e91d35dea53f3b67a4a1359864a8fbe`  
		Last Modified: Thu, 01 Feb 2024 14:34:04 GMT  
		Size: 2.9 MB (2910563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abfb654d93d66c4e1dc690a542bf6d9ef45a92acd908f63be760504bc43dc119`  
		Last Modified: Thu, 01 Feb 2024 14:34:04 GMT  
		Size: 31.4 KB (31415 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:2.3.1`

```console
$ docker pull couchdb@sha256:490e59db6149ce673734c1268a055e8ebd897b57a8d0b1f1b4bbc4264104cc9d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:2.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:80383de74598b295e382544e13a53574226d05e3b8f6293bf56f27f00940fd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84169041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e309f7c1828f7087e95cf0ba19507a4aeb02f7a884f620ab16c0dc9461776b61`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:232125261662ceeb0126b96defe05092c121fecd55c99db5f76a03ab0c87d07e in / 
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
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:789bca57d694bdff72d9fcb5bdc3f4684b63dee11402ed28245ae1c578d62ba3`  
		Last Modified: Tue, 13 Feb 2024 00:43:30 GMT  
		Size: 27.2 MB (27188190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b91f61f6301a3dec96508b2c97786e6f5f0221dc62a231d7316bcfe19957ad`  
		Last Modified: Tue, 13 Feb 2024 01:53:39 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e80f4954bc9432fc6237e3be6e8a331bfd1b13a6b61800448576c40ccd224e`  
		Last Modified: Tue, 13 Feb 2024 01:53:40 GMT  
		Size: 6.7 MB (6703566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122336ace0d79dce4d064680ffabce183a4c8c235e7e6346793cf0d3a6c4b400`  
		Last Modified: Tue, 13 Feb 2024 01:53:39 GMT  
		Size: 1.0 MB (1046479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beafd30c1a1026c0c414fc2590ac27d58dcc39e6e1275274e22eedf4c79824ca`  
		Last Modified: Tue, 13 Feb 2024 01:53:40 GMT  
		Size: 80.3 KB (80343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35cce46b847671d9b45e66ba1b59d3f2920f4edce1af98755f368912317ea04`  
		Last Modified: Tue, 13 Feb 2024 01:53:40 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feec791ad121e40adb3a59c351541070d7cf03a64a769c045a484dfa8a657946`  
		Last Modified: Tue, 13 Feb 2024 01:53:41 GMT  
		Size: 49.1 MB (49143540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957fb429ea1153c66d0457d7d04e089fe794aecfce225be2821b07e8d819e32f`  
		Last Modified: Tue, 13 Feb 2024 01:53:41 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92692d14e642732ac1689b0040df870af19b16dc235e76f0ec7d1d87fff51fc2`  
		Last Modified: Tue, 13 Feb 2024 01:53:41 GMT  
		Size: 762.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533f04efcf37f2520a6963fc68822980973daa2e88843825b34ef6421ddd64d1`  
		Last Modified: Tue, 13 Feb 2024 01:53:41 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6915c5098de94f2a090712fd944ad6b77e6540bf6adb78234fa51506bc43fc88`  
		Last Modified: Tue, 13 Feb 2024 01:53:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:2.3.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:1bbf09eb5beff904b1ff1c4be6e52f171b638f012eff2fb479a23aefd9f1bbcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3549045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f473cac918935ae1aedf5b9eb875e41c192e2ecccd3a34d6a6f394e3928e993`

```dockerfile
```

-	Layers:
	-	`sha256:f34fd1af00b3d6cbc831ce1bc89dc79aa7dda3b23e8bad8a1bc83dfda62d3e97`  
		Last Modified: Tue, 13 Feb 2024 01:53:40 GMT  
		Size: 3.5 MB (3517463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e80ecd9d59ec42815b78c137040582373947384d2371eef2ceee6396a604897`  
		Last Modified: Tue, 13 Feb 2024 01:53:40 GMT  
		Size: 31.6 KB (31582 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:2.3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:ccabf00dced68849dd5aed8fd479356aa4698e656f8f52aed38a7bcc0fc55494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72615460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb5836c03fcb70932bd31f00b9924302cee48d27f32806676201d396d2f5b41`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:de90e50e142aa92c29d5128e1cd025fd5c5b91f879a19a06a8b49451a4e6afb9 in / 
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
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:42641f7bf1512c205041cf7899e52e2185e49bcd6cfa0cb8ebfc73e3009221b7`  
		Last Modified: Wed, 31 Jan 2024 22:49:34 GMT  
		Size: 26.0 MB (25970227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195a5c7275e6e739113fc1bba1a86979ba02e51ce0e8d2809e4b0c91a949e951`  
		Last Modified: Thu, 01 Feb 2024 14:06:58 GMT  
		Size: 3.4 KB (3354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea98b1217ba4ee31a07f6858e2e3ab54a2ec3c90285fdf0e4a66d2c62420122`  
		Last Modified: Thu, 01 Feb 2024 14:06:59 GMT  
		Size: 6.6 MB (6576636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219447fdce8a83af3658eef95dae3b2b2d90ed96f8bead499713f344aefacde9`  
		Last Modified: Thu, 01 Feb 2024 14:06:58 GMT  
		Size: 951.3 KB (951318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe587eefa88b70481c6778e6e0081384c362b771571e970811dd6a5cf20a4f9`  
		Last Modified: Thu, 01 Feb 2024 14:06:59 GMT  
		Size: 80.2 KB (80182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f76842143d873297730e3c137e579618b8da303c12c9a4bf5ee85bfcddf1b17`  
		Last Modified: Thu, 01 Feb 2024 14:34:04 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93628300ad755a96bf9e7cb0af15cfafe6ab9b447c4fa663e4dc70a39084f50`  
		Last Modified: Thu, 01 Feb 2024 14:34:06 GMT  
		Size: 39.0 MB (39030149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef517268298c93c834923f5c12381f4fe0b5aaa5a6707ba9f149a0078e265153`  
		Last Modified: Thu, 01 Feb 2024 14:34:05 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fcddb3461b2b266c018d63ae3082c427dd63d5492f8ec149371d0da7a5ba5e5`  
		Last Modified: Thu, 01 Feb 2024 14:34:04 GMT  
		Size: 763.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4319d3dbd76421aff43c346568ab2edd1948b58981009feec9987db61bec1e0b`  
		Last Modified: Thu, 01 Feb 2024 14:34:05 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994152cee51d4da15621f1b85714b901d2065bb1862c0b734a62a462126ed018`  
		Last Modified: Thu, 01 Feb 2024 14:34:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:2.3.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:ffe866e48a2620ba5909124aa30d335b6fee05cf68ee5ac6fa1e51b2d4c9ad11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2941978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07459d9c1dade9a0559d111ec0726431b3edfa06cfd76efcfd0b035ab123c733`

```dockerfile
```

-	Layers:
	-	`sha256:9debaf35ca6d7ce41755e63d171087079e91d35dea53f3b67a4a1359864a8fbe`  
		Last Modified: Thu, 01 Feb 2024 14:34:04 GMT  
		Size: 2.9 MB (2910563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abfb654d93d66c4e1dc690a542bf6d9ef45a92acd908f63be760504bc43dc119`  
		Last Modified: Thu, 01 Feb 2024 14:34:04 GMT  
		Size: 31.4 KB (31415 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3`

```console
$ docker pull couchdb@sha256:2a51754c959060108556c0828e1e48ba72b8d6ac05d22d0efe2ffbc8a839e262
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
$ docker pull couchdb@sha256:405419c4ecce18030dbd1dd7fe692e349f83a0d68df71b6d40238c0c0dd45c73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89844973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3731fb1117f02a201e062576679a4d18a995cd23501c55013b528a2d549ee631`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
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
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249a1605c575ce96487ffac541cf15846a8ea40db5a3ea5145e408c89b649b1b`  
		Last Modified: Tue, 13 Feb 2024 01:53:26 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096352bc9320e7991dd9c0362807fb9a4d4597d01fce5fd6d3ba34c3bc92e6e1`  
		Last Modified: Tue, 13 Feb 2024 01:53:26 GMT  
		Size: 5.2 MB (5223271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201c40b734425007bbe328cb186eb7b070adef02d02e0f334b7abf1c9769368f`  
		Last Modified: Tue, 13 Feb 2024 01:53:26 GMT  
		Size: 394.3 KB (394334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e71ec88dde6821c3682b9f75ed25a997d664d50485223b87ab26b148fba8fdf`  
		Last Modified: Tue, 13 Feb 2024 01:53:27 GMT  
		Size: 77.9 KB (77896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1569272dcfe8e19f61c84f94b9d94e9fbbf0ac368aff718c06b7649e0e9dbe0`  
		Last Modified: Tue, 13 Feb 2024 01:53:27 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94053229a35c71f854d02cbb43092581e8b6cee7ef948f9b514acf1b9115c3b7`  
		Last Modified: Tue, 13 Feb 2024 01:53:28 GMT  
		Size: 52.7 MB (52719476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5574179220fd2064c4c86791f51e71502c5eed795327da1c0271e0a3bdc15025`  
		Last Modified: Tue, 13 Feb 2024 01:53:27 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb73ba5435db91092fe3694f3825701ad5cca6534fc4b12df96ef10ffe0ccf6`  
		Last Modified: Tue, 13 Feb 2024 01:53:28 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c99e0ab115184508946862ec52009d68ac8c02cf34c37517727a457f107cb0`  
		Last Modified: Tue, 13 Feb 2024 01:53:28 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635a5b575816fae0daa6b83453f0895a506e418b8b1ac15a657483365d4d3805`  
		Last Modified: Tue, 13 Feb 2024 01:53:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:d16ee81b162d4ab76c3d63eb24c759731f33182a74a0b8c127b6667ea743186a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3419330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e5d61dcb6a671d4bfabf370e7f61ed671efdcc236747afce88263a09acbbce`

```dockerfile
```

-	Layers:
	-	`sha256:c6b83df7389ff8ad90817f27160f302f285cd712a01ec06c1a98bf8d1eb0de4c`  
		Last Modified: Tue, 13 Feb 2024 01:53:26 GMT  
		Size: 3.4 MB (3387604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a6b40e9e902cc7e5708edcd2d223152519a7f697689ac57e6e6da3af916bcf3`  
		Last Modified: Tue, 13 Feb 2024 01:53:26 GMT  
		Size: 31.7 KB (31726 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:aba4ba41296b2d341929265e7fa5b87f641d58e358f7df3c4c05b9342dea1cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88075288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8a2bfcbb05ca1f3c14795e6c011a1805ad69d1a06c60f82f42e6a9bdcaf509`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
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
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ec1ba56fff57376a1e522907553fc77fc80bb5c48ed5b7746be835f2c791e8`  
		Last Modified: Thu, 01 Feb 2024 08:10:56 GMT  
		Size: 3.4 KB (3351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b20254b0592cead69bb43b1e572ee734ed6053b6445077e621c0af6234886fd`  
		Last Modified: Thu, 01 Feb 2024 08:10:57 GMT  
		Size: 5.0 MB (5004087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef6a435304886e6662c0e0f7d34448ae89903960a5b5747c29472d2ab308627`  
		Last Modified: Thu, 01 Feb 2024 08:10:57 GMT  
		Size: 350.5 KB (350527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b781cbda42a627dc3c93f9890aceb52d86295f2fd6459eae86f20f8928f9680d`  
		Last Modified: Thu, 01 Feb 2024 08:10:57 GMT  
		Size: 77.8 KB (77810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f135e41b52f16d917b667611579ce1a9b1c3c40fb5e1af14399790dd1363d0`  
		Last Modified: Thu, 01 Feb 2024 08:10:58 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60fd9abf17ec23f09f0362ac146a4a65b2e1377942ab70334879ed109e5ea176`  
		Last Modified: Thu, 01 Feb 2024 08:11:01 GMT  
		Size: 52.6 MB (52570938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919712266c6021b3387e6207117af5dcb125015985b3f174ddce70d7be6ba16c`  
		Last Modified: Thu, 01 Feb 2024 08:10:58 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e9f6a099c29cbf0e2a100d023db0b49a861c986bf8348c4422095d0ac09b2b`  
		Last Modified: Thu, 01 Feb 2024 08:10:59 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9007c269b338bc96ebc6dac4b6095fff1f04931e0e157c4863b1d1e6749d966`  
		Last Modified: Thu, 01 Feb 2024 08:10:59 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f229d8adc49602ddfc4cf87a6113566613959aa6f886e99244b294bd04c756`  
		Last Modified: Thu, 01 Feb 2024 08:11:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:b12586e7bf95de93b3536776f20986afff6aba57c6c150e82a0b13e5bf2d88df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3327922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eb1b85ebe108c883131c50f629b135ec4be556d9cb45a989876a93ca2f9366b`

```dockerfile
```

-	Layers:
	-	`sha256:133a0faddb7b4761e933cfc1db8ec5c9527f0f3025a2932950e637ca3446c44c`  
		Last Modified: Thu, 01 Feb 2024 08:10:57 GMT  
		Size: 3.3 MB (3296186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a92a98cf3352f51a7cfc54e983dd964e15db84ed67274e2550de9a59a3948a6`  
		Last Modified: Thu, 01 Feb 2024 08:10:56 GMT  
		Size: 31.7 KB (31736 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:583c58b2c631d310e8dd60c12a592ed075407fc5f68c3d14f8cb8c4105a7abc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95366126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e50cc7222008fd7804f91251acb7adcd498234fbb452c334de5ce685b8a49c1d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:35bb0428da48f0fbc9230db1ecddacb636bc61d82e6701574b518b720ae76d7f in / 
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
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:4df9a94c24ca5c52fd8a7f1aebc76690845edac56c36acaf79a984722b5e4e48`  
		Last Modified: Wed, 31 Jan 2024 22:35:16 GMT  
		Size: 35.3 MB (35293643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92f458db7320742599ab920741e07f9544cfd58f5b8686398d8966491b06f0f`  
		Last Modified: Thu, 01 Feb 2024 08:47:38 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cb9aa6b890ce8b704b2fc45c763a345ac7e2d83897d23f16186a05c4cbdbf9`  
		Last Modified: Thu, 01 Feb 2024 08:47:39 GMT  
		Size: 5.8 MB (5839188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1fbcb0d9961bb5bbde2b4b8215a1acd828df14abb5c76cdf98b4721c114bf1b`  
		Last Modified: Thu, 01 Feb 2024 08:47:39 GMT  
		Size: 446.7 KB (446667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023feedddc4860debc352c7ee2d9cd2885475659c7bc489eb74d89bd8ff14289`  
		Last Modified: Thu, 01 Feb 2024 08:47:40 GMT  
		Size: 77.9 KB (77900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33e850eba7cad89ca5087696f33c7ef6c29970a0d63be2e113e430b80f8c586`  
		Last Modified: Thu, 01 Feb 2024 08:47:40 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a44471fd006a5678cbd2ffaedd491dc3be8a8be56c8061db116fa085775ca1e6`  
		Last Modified: Thu, 01 Feb 2024 08:47:42 GMT  
		Size: 53.7 MB (53701137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48088e727ddc2db68bace99d3603026c3c92617ed9111f71c537b916aa0b5476`  
		Last Modified: Thu, 01 Feb 2024 08:47:41 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240dd27ec561dea5460665a316655f0aaaf2694a36db5adf88ff60c42019b1f5`  
		Last Modified: Thu, 01 Feb 2024 08:47:41 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a868dbb1cf5a7405695a29166dabe6be49a39eea3fb6ec2c90140ddede8265`  
		Last Modified: Thu, 01 Feb 2024 08:47:41 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d83e584f48b1ad066f05a03876f9ba26d6a68289e78c1ddbfc81bc21f211dd0`  
		Last Modified: Thu, 01 Feb 2024 08:47:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:ff19866200f9ca8aede65e78dbdfbe2695263926361922ebbff21151ac56aeba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3332254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a79d8c47ad4dd103ca59e9d983352e5ed55b3bfa3f927d618c6231ba1467dae`

```dockerfile
```

-	Layers:
	-	`sha256:1dabb5c0cafb5d7c64c681533260175d71ebcd148f7e9f41e6dc2b9630b536be`  
		Last Modified: Thu, 01 Feb 2024 08:47:39 GMT  
		Size: 3.3 MB (3300478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1266308b253a21d2adf89309c140514433b8e382a1aa16a118f0ee0def0228a9`  
		Last Modified: Thu, 01 Feb 2024 08:47:39 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; s390x

```console
$ docker pull couchdb@sha256:080c1de9aacbafef98684af7143fceca19926658bf69e495c9eaf5d82b0ee7ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86380517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55b098b432b943d787618e921aceb298b5577ee029ceab52415740d3b2dcce6e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:9a48c9d7fde8a2820cff9dc06434dc4dca8967438fa75bb93e6646cb44682b18 in / 
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
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:16651f5430ff52661c6729a9dc23c80d76205b6bd77d7730f38e39aca6731613`  
		Last Modified: Wed, 31 Jan 2024 23:29:40 GMT  
		Size: 29.7 MB (29657133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee3a0014482f190b29e7494f752808b6091b9a1dc21e95ca84554dc9b2e1cf7`  
		Last Modified: Thu, 01 Feb 2024 20:19:29 GMT  
		Size: 3.4 KB (3351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd8f5d8f498e66b04e07425c6d208f4dac87da21571314c3c29dad8ee96f014`  
		Last Modified: Thu, 01 Feb 2024 20:19:29 GMT  
		Size: 4.9 MB (4905554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c1c9f5ef6ccc47a6527e801ae5b534ede814bea1eb564abb63fba5367f8f20`  
		Last Modified: Thu, 01 Feb 2024 20:19:29 GMT  
		Size: 357.5 KB (357486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4044f8c1f294d8fc68c5a2c8daa30a8367d55128d9c795a74f9b5beb90e692ec`  
		Last Modified: Thu, 01 Feb 2024 20:19:30 GMT  
		Size: 77.8 KB (77849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97164cc599174153fa4fa6a7e3301eb60cf6caea1d81f74a1c1472cad406bf1`  
		Last Modified: Thu, 01 Feb 2024 20:19:30 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637a131379dee3f1cf9126a6973e37a6b30f10fdad830a30366295e5f97029aa`  
		Last Modified: Thu, 01 Feb 2024 20:19:31 GMT  
		Size: 51.4 MB (51374897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7a24b7d988302402886e32e4d08938faef1b31a27c533345d52bc184facbe4`  
		Last Modified: Thu, 01 Feb 2024 20:19:31 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0675d1c86abe9bbabcf7289c08791fbfc14005b01548de8678bb741971f0ca3`  
		Last Modified: Thu, 01 Feb 2024 20:19:31 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5078d90be17ce6b9ff3303773b194f78e6223fabc751d1299ca513d125964385`  
		Last Modified: Thu, 01 Feb 2024 20:19:31 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264b1f6b9b621e7e19168b4a2b4c74c8fd4569dee3971a3a5a19ba81d3d5cc7c`  
		Last Modified: Thu, 01 Feb 2024 20:19:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:9848e5715284986e828c3199ece6005a64cb9f7068af3bef360c71f24d19601a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3327136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d992047f39681d2d08f32e199d591cba16e5839804c320d98fb1fed6db0769`

```dockerfile
```

-	Layers:
	-	`sha256:3bb1797658c828db62b2c9f0f28e6b85ea80c6e241576ca7dae6da5b03a227da`  
		Last Modified: Thu, 01 Feb 2024 20:19:29 GMT  
		Size: 3.3 MB (3295410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23a896bfbf2407b03c6215476c940a4a0f1f63c4b707faa2770a0d91f1ff6e44`  
		Last Modified: Thu, 01 Feb 2024 20:19:29 GMT  
		Size: 31.7 KB (31726 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:0c874cc1842c27d46f89756cc505ddc3f42cfb52ef88a2e521ea9a2f02dbf7dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:9f69b5df73d2604f1d431f57208b3b67471789ee19a630b9972440cbc97bda28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79644338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51254b5c6c1b53c748f02200ba0e7163322103535f6a2d467f0f38abaa1e0e4e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:232125261662ceeb0126b96defe05092c121fecd55c99db5f76a03ab0c87d07e in / 
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
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:789bca57d694bdff72d9fcb5bdc3f4684b63dee11402ed28245ae1c578d62ba3`  
		Last Modified: Tue, 13 Feb 2024 00:43:30 GMT  
		Size: 27.2 MB (27188190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db97ec5d84acae0304a42acf996678d3c4a4fcb79b43970bc84ec18743cc10cf`  
		Last Modified: Tue, 13 Feb 2024 01:53:38 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c41aabfbc67c092464dc4193329dea62f71d05945fa0e4adc51ce65a07ae30e`  
		Last Modified: Tue, 13 Feb 2024 01:53:38 GMT  
		Size: 6.7 MB (6703460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf929ddecd5b7bfe0cffb700785ee7a5f8e38daf3d03e9acc4cf4ad15627850`  
		Last Modified: Tue, 13 Feb 2024 01:53:38 GMT  
		Size: 1.0 MB (1046480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9cef46cda574dc34449cdb5216a6d7e81f0062d6b7d2944de3d3b5e2f4fba9`  
		Last Modified: Tue, 13 Feb 2024 01:53:39 GMT  
		Size: 80.3 KB (80328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647da4cbf72e81dcf4dcf5eb93602ebdb7fd85b7a8ebf99281fe255ba988f889`  
		Last Modified: Tue, 13 Feb 2024 01:53:39 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c88c7a5e0d59787670de268289a6243924047cba8813a341c95a0326614d5c`  
		Last Modified: Tue, 13 Feb 2024 01:53:41 GMT  
		Size: 44.6 MB (44618957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a927d8356d38f01f1db9ba1cb63668f1904ef09784c3dc38af28556ca2786a`  
		Last Modified: Tue, 13 Feb 2024 01:53:40 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c29e8f6ac645e28519fd5b54619a2a925a59a739826863e4d248d4ab85fe3df`  
		Last Modified: Tue, 13 Feb 2024 01:53:40 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f82947b5bcae2f0c5167ec5118e71f1a392e11f29864424858ceb148948968`  
		Last Modified: Tue, 13 Feb 2024 01:53:41 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b22b9f6df8c6452b0e65728d1fb7b7492ab449e629444d0b078a5bd45ba605`  
		Last Modified: Tue, 13 Feb 2024 01:53:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:81c8adc09251e6729758cb7268857a2b0516f4a83a69f0d2a7e30031e727c3ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb60206eec6d85384d3698637c81943aba6e0b6768c18e0b54a592c6ec538d98`

```dockerfile
```

-	Layers:
	-	`sha256:d0d0c3de3547019209ab4124c409351bb5551f28cdb9a626e376132095bb0b71`  
		Last Modified: Tue, 13 Feb 2024 01:53:38 GMT  
		Size: 3.0 MB (2955438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ca969026a576f8a4781405b8fbe8b9cd8dd181e31a7305b6483a8afa53fd650`  
		Last Modified: Tue, 13 Feb 2024 01:53:38 GMT  
		Size: 31.3 KB (31282 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:aaa7ec37cf85da620a31b0164624b43766422ec5384c869d85d3697a921050fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74710151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9efe15462cdbcb36b54abf7046cdd9711cbde2bff05581f7cc499fc6064b9c46`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:de90e50e142aa92c29d5128e1cd025fd5c5b91f879a19a06a8b49451a4e6afb9 in / 
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
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:42641f7bf1512c205041cf7899e52e2185e49bcd6cfa0cb8ebfc73e3009221b7`  
		Last Modified: Wed, 31 Jan 2024 22:49:34 GMT  
		Size: 26.0 MB (25970227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195a5c7275e6e739113fc1bba1a86979ba02e51ce0e8d2809e4b0c91a949e951`  
		Last Modified: Thu, 01 Feb 2024 14:06:58 GMT  
		Size: 3.4 KB (3354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea98b1217ba4ee31a07f6858e2e3ab54a2ec3c90285fdf0e4a66d2c62420122`  
		Last Modified: Thu, 01 Feb 2024 14:06:59 GMT  
		Size: 6.6 MB (6576636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219447fdce8a83af3658eef95dae3b2b2d90ed96f8bead499713f344aefacde9`  
		Last Modified: Thu, 01 Feb 2024 14:06:58 GMT  
		Size: 951.3 KB (951318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe587eefa88b70481c6778e6e0081384c362b771571e970811dd6a5cf20a4f9`  
		Last Modified: Thu, 01 Feb 2024 14:06:59 GMT  
		Size: 80.2 KB (80182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c5cecb9f61b38b6dc342321c3921e337331796362cee7b481e0ed2c08f052d`  
		Last Modified: Thu, 01 Feb 2024 14:06:59 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a59cfcaf2c3331b83502e5a505a92726c42b728e04aa0631e2bafa339868f39`  
		Last Modified: Thu, 01 Feb 2024 14:07:01 GMT  
		Size: 41.1 MB (41124844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcf7a2ba16b14922a3b9b4f8f627a4e786a1ae1dc2fc0279c1ccf0502a2e343`  
		Last Modified: Thu, 01 Feb 2024 14:07:00 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5f5f0ee464ea2ea361998aff7796be2ae3f47c4098cfbfe1129687f184a340`  
		Last Modified: Thu, 01 Feb 2024 14:07:00 GMT  
		Size: 762.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a571c5fa7633b333f3d542919e899a52d981fcf589646f6a97e7d3cc611d6e86`  
		Last Modified: Thu, 01 Feb 2024 14:07:01 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb04df4feddea5be38f39a00877dd6f61e47032f942371c04ca8e407466979b2`  
		Last Modified: Thu, 01 Feb 2024 14:07:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:3992bfab24d449e55386032b9a7c22347f67b2d27d44e4861b10bab0db24acfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8740d4c214fa57f61bc5579259ff11630c5a19430f693ae77e2dedec6097fb8`

```dockerfile
```

-	Layers:
	-	`sha256:75ccc90350eb5e3f945de4fc22467457b4a58043cad265c28aceb390b743aaf8`  
		Last Modified: Thu, 01 Feb 2024 14:06:58 GMT  
		Size: 3.0 MB (2961717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87bff0ad911e596bb146c8ae07dd983e087800441107e91147cc161e1993c800`  
		Last Modified: Thu, 01 Feb 2024 14:06:58 GMT  
		Size: 31.3 KB (31280 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.1.2`

```console
$ docker pull couchdb@sha256:0c874cc1842c27d46f89756cc505ddc3f42cfb52ef88a2e521ea9a2f02dbf7dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.1.2` - linux; amd64

```console
$ docker pull couchdb@sha256:9f69b5df73d2604f1d431f57208b3b67471789ee19a630b9972440cbc97bda28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79644338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51254b5c6c1b53c748f02200ba0e7163322103535f6a2d467f0f38abaa1e0e4e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:232125261662ceeb0126b96defe05092c121fecd55c99db5f76a03ab0c87d07e in / 
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
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:789bca57d694bdff72d9fcb5bdc3f4684b63dee11402ed28245ae1c578d62ba3`  
		Last Modified: Tue, 13 Feb 2024 00:43:30 GMT  
		Size: 27.2 MB (27188190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db97ec5d84acae0304a42acf996678d3c4a4fcb79b43970bc84ec18743cc10cf`  
		Last Modified: Tue, 13 Feb 2024 01:53:38 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c41aabfbc67c092464dc4193329dea62f71d05945fa0e4adc51ce65a07ae30e`  
		Last Modified: Tue, 13 Feb 2024 01:53:38 GMT  
		Size: 6.7 MB (6703460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf929ddecd5b7bfe0cffb700785ee7a5f8e38daf3d03e9acc4cf4ad15627850`  
		Last Modified: Tue, 13 Feb 2024 01:53:38 GMT  
		Size: 1.0 MB (1046480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9cef46cda574dc34449cdb5216a6d7e81f0062d6b7d2944de3d3b5e2f4fba9`  
		Last Modified: Tue, 13 Feb 2024 01:53:39 GMT  
		Size: 80.3 KB (80328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647da4cbf72e81dcf4dcf5eb93602ebdb7fd85b7a8ebf99281fe255ba988f889`  
		Last Modified: Tue, 13 Feb 2024 01:53:39 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c88c7a5e0d59787670de268289a6243924047cba8813a341c95a0326614d5c`  
		Last Modified: Tue, 13 Feb 2024 01:53:41 GMT  
		Size: 44.6 MB (44618957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a927d8356d38f01f1db9ba1cb63668f1904ef09784c3dc38af28556ca2786a`  
		Last Modified: Tue, 13 Feb 2024 01:53:40 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c29e8f6ac645e28519fd5b54619a2a925a59a739826863e4d248d4ab85fe3df`  
		Last Modified: Tue, 13 Feb 2024 01:53:40 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f82947b5bcae2f0c5167ec5118e71f1a392e11f29864424858ceb148948968`  
		Last Modified: Tue, 13 Feb 2024 01:53:41 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b22b9f6df8c6452b0e65728d1fb7b7492ab449e629444d0b078a5bd45ba605`  
		Last Modified: Tue, 13 Feb 2024 01:53:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.1.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:81c8adc09251e6729758cb7268857a2b0516f4a83a69f0d2a7e30031e727c3ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb60206eec6d85384d3698637c81943aba6e0b6768c18e0b54a592c6ec538d98`

```dockerfile
```

-	Layers:
	-	`sha256:d0d0c3de3547019209ab4124c409351bb5551f28cdb9a626e376132095bb0b71`  
		Last Modified: Tue, 13 Feb 2024 01:53:38 GMT  
		Size: 3.0 MB (2955438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ca969026a576f8a4781405b8fbe8b9cd8dd181e31a7305b6483a8afa53fd650`  
		Last Modified: Tue, 13 Feb 2024 01:53:38 GMT  
		Size: 31.3 KB (31282 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.1.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:aaa7ec37cf85da620a31b0164624b43766422ec5384c869d85d3697a921050fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74710151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9efe15462cdbcb36b54abf7046cdd9711cbde2bff05581f7cc499fc6064b9c46`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:de90e50e142aa92c29d5128e1cd025fd5c5b91f879a19a06a8b49451a4e6afb9 in / 
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
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:42641f7bf1512c205041cf7899e52e2185e49bcd6cfa0cb8ebfc73e3009221b7`  
		Last Modified: Wed, 31 Jan 2024 22:49:34 GMT  
		Size: 26.0 MB (25970227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195a5c7275e6e739113fc1bba1a86979ba02e51ce0e8d2809e4b0c91a949e951`  
		Last Modified: Thu, 01 Feb 2024 14:06:58 GMT  
		Size: 3.4 KB (3354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea98b1217ba4ee31a07f6858e2e3ab54a2ec3c90285fdf0e4a66d2c62420122`  
		Last Modified: Thu, 01 Feb 2024 14:06:59 GMT  
		Size: 6.6 MB (6576636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219447fdce8a83af3658eef95dae3b2b2d90ed96f8bead499713f344aefacde9`  
		Last Modified: Thu, 01 Feb 2024 14:06:58 GMT  
		Size: 951.3 KB (951318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe587eefa88b70481c6778e6e0081384c362b771571e970811dd6a5cf20a4f9`  
		Last Modified: Thu, 01 Feb 2024 14:06:59 GMT  
		Size: 80.2 KB (80182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c5cecb9f61b38b6dc342321c3921e337331796362cee7b481e0ed2c08f052d`  
		Last Modified: Thu, 01 Feb 2024 14:06:59 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a59cfcaf2c3331b83502e5a505a92726c42b728e04aa0631e2bafa339868f39`  
		Last Modified: Thu, 01 Feb 2024 14:07:01 GMT  
		Size: 41.1 MB (41124844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcf7a2ba16b14922a3b9b4f8f627a4e786a1ae1dc2fc0279c1ccf0502a2e343`  
		Last Modified: Thu, 01 Feb 2024 14:07:00 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5f5f0ee464ea2ea361998aff7796be2ae3f47c4098cfbfe1129687f184a340`  
		Last Modified: Thu, 01 Feb 2024 14:07:00 GMT  
		Size: 762.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a571c5fa7633b333f3d542919e899a52d981fcf589646f6a97e7d3cc611d6e86`  
		Last Modified: Thu, 01 Feb 2024 14:07:01 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb04df4feddea5be38f39a00877dd6f61e47032f942371c04ca8e407466979b2`  
		Last Modified: Thu, 01 Feb 2024 14:07:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.1.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:3992bfab24d449e55386032b9a7c22347f67b2d27d44e4861b10bab0db24acfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8740d4c214fa57f61bc5579259ff11630c5a19430f693ae77e2dedec6097fb8`

```dockerfile
```

-	Layers:
	-	`sha256:75ccc90350eb5e3f945de4fc22467457b4a58043cad265c28aceb390b743aaf8`  
		Last Modified: Thu, 01 Feb 2024 14:06:58 GMT  
		Size: 3.0 MB (2961717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87bff0ad911e596bb146c8ae07dd983e087800441107e91147cc161e1993c800`  
		Last Modified: Thu, 01 Feb 2024 14:06:58 GMT  
		Size: 31.3 KB (31280 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.2`

```console
$ docker pull couchdb@sha256:fc1df1a39fae773fbc631b50d97c8e54d66104937249318873e771678809e1ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `couchdb:3.2` - linux; amd64

```console
$ docker pull couchdb@sha256:90eeaec3df9eb34c1ac3c3c5724f7aeb574ef92009570ff40bd39a736745f2da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.3 MB (89311917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134b7edbd2b5200e1bac946bff625afd2b2ea987812b975cba5e5b686cdd7fdd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
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
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f76c15a31a40060f8e4542a337f59f0ef4e8b3d7c3c40bda47abb59d710083`  
		Last Modified: Tue, 13 Feb 2024 01:53:30 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23baca0b107851d7b070618ef32ef9bda74227d6112c596fc62d58b236a383b8`  
		Last Modified: Tue, 13 Feb 2024 01:53:30 GMT  
		Size: 5.2 MB (5223296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1798ebb20ea24aa2573ddb7a74e727668e07dd7625172670d6366c2d05581b4b`  
		Last Modified: Tue, 13 Feb 2024 01:53:30 GMT  
		Size: 394.3 KB (394349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54685bc16356835ffc719166617150f43813594040700e7c96079a14630497fe`  
		Last Modified: Tue, 13 Feb 2024 01:53:29 GMT  
		Size: 77.9 KB (77906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f5343e4dcc05c0af6f62d36ad542542ed15e427fa88433acd985f8400a1f66`  
		Last Modified: Tue, 13 Feb 2024 01:53:30 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492ae7e95dcd1bed263d36e5c981ecccf90c9857799eeb7f8f03bd44d4136553`  
		Last Modified: Tue, 13 Feb 2024 01:53:31 GMT  
		Size: 52.2 MB (52186623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb78c43a96e4348395151d7315afe55398ece6c43d06c9b545d49ca5ee322893`  
		Last Modified: Tue, 13 Feb 2024 01:53:31 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e5a829cb377336afd6d6eedf70239cb09e574e1799b11e862f561e45794513`  
		Last Modified: Tue, 13 Feb 2024 01:53:31 GMT  
		Size: 997.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edbe3c5549e391824078ff4c7680f80fa3c4ccd101b4a733ac4c4ff893248e7`  
		Last Modified: Tue, 13 Feb 2024 01:53:31 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ff2b0ba295cfdcbe09f5008c94b0784c86ef7a8e674a99dc488ca6a0101b6f`  
		Last Modified: Tue, 13 Feb 2024 01:53:32 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:e8e6a443d790ec8d6690189a7c54eae4469d128d36249c2c8f0cd46fc63141b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3393754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:832739f144a7e6e954456534adb63d9a77ed1e4be24305be7b4a13c525d9b8e5`

```dockerfile
```

-	Layers:
	-	`sha256:38c194de38d6e456e143a9bf1a5b9cd32b44febf1f5854f04bd13a5b69b8aa17`  
		Last Modified: Tue, 13 Feb 2024 01:53:30 GMT  
		Size: 3.4 MB (3362621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daf8adb41724ea77b6a802a8d084d50753fd7f3f537753b2cf7713e7e99f9f11`  
		Last Modified: Tue, 13 Feb 2024 01:53:29 GMT  
		Size: 31.1 KB (31133 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.2.3`

```console
$ docker pull couchdb@sha256:fc1df1a39fae773fbc631b50d97c8e54d66104937249318873e771678809e1ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `couchdb:3.2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:90eeaec3df9eb34c1ac3c3c5724f7aeb574ef92009570ff40bd39a736745f2da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.3 MB (89311917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134b7edbd2b5200e1bac946bff625afd2b2ea987812b975cba5e5b686cdd7fdd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
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
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f76c15a31a40060f8e4542a337f59f0ef4e8b3d7c3c40bda47abb59d710083`  
		Last Modified: Tue, 13 Feb 2024 01:53:30 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23baca0b107851d7b070618ef32ef9bda74227d6112c596fc62d58b236a383b8`  
		Last Modified: Tue, 13 Feb 2024 01:53:30 GMT  
		Size: 5.2 MB (5223296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1798ebb20ea24aa2573ddb7a74e727668e07dd7625172670d6366c2d05581b4b`  
		Last Modified: Tue, 13 Feb 2024 01:53:30 GMT  
		Size: 394.3 KB (394349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54685bc16356835ffc719166617150f43813594040700e7c96079a14630497fe`  
		Last Modified: Tue, 13 Feb 2024 01:53:29 GMT  
		Size: 77.9 KB (77906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f5343e4dcc05c0af6f62d36ad542542ed15e427fa88433acd985f8400a1f66`  
		Last Modified: Tue, 13 Feb 2024 01:53:30 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492ae7e95dcd1bed263d36e5c981ecccf90c9857799eeb7f8f03bd44d4136553`  
		Last Modified: Tue, 13 Feb 2024 01:53:31 GMT  
		Size: 52.2 MB (52186623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb78c43a96e4348395151d7315afe55398ece6c43d06c9b545d49ca5ee322893`  
		Last Modified: Tue, 13 Feb 2024 01:53:31 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e5a829cb377336afd6d6eedf70239cb09e574e1799b11e862f561e45794513`  
		Last Modified: Tue, 13 Feb 2024 01:53:31 GMT  
		Size: 997.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edbe3c5549e391824078ff4c7680f80fa3c4ccd101b4a733ac4c4ff893248e7`  
		Last Modified: Tue, 13 Feb 2024 01:53:31 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ff2b0ba295cfdcbe09f5008c94b0784c86ef7a8e674a99dc488ca6a0101b6f`  
		Last Modified: Tue, 13 Feb 2024 01:53:32 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.2.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:e8e6a443d790ec8d6690189a7c54eae4469d128d36249c2c8f0cd46fc63141b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3393754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:832739f144a7e6e954456534adb63d9a77ed1e4be24305be7b4a13c525d9b8e5`

```dockerfile
```

-	Layers:
	-	`sha256:38c194de38d6e456e143a9bf1a5b9cd32b44febf1f5854f04bd13a5b69b8aa17`  
		Last Modified: Tue, 13 Feb 2024 01:53:30 GMT  
		Size: 3.4 MB (3362621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daf8adb41724ea77b6a802a8d084d50753fd7f3f537753b2cf7713e7e99f9f11`  
		Last Modified: Tue, 13 Feb 2024 01:53:29 GMT  
		Size: 31.1 KB (31133 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.3`

```console
$ docker pull couchdb@sha256:2a51754c959060108556c0828e1e48ba72b8d6ac05d22d0efe2ffbc8a839e262
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
$ docker pull couchdb@sha256:405419c4ecce18030dbd1dd7fe692e349f83a0d68df71b6d40238c0c0dd45c73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89844973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3731fb1117f02a201e062576679a4d18a995cd23501c55013b528a2d549ee631`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
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
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249a1605c575ce96487ffac541cf15846a8ea40db5a3ea5145e408c89b649b1b`  
		Last Modified: Tue, 13 Feb 2024 01:53:26 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096352bc9320e7991dd9c0362807fb9a4d4597d01fce5fd6d3ba34c3bc92e6e1`  
		Last Modified: Tue, 13 Feb 2024 01:53:26 GMT  
		Size: 5.2 MB (5223271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201c40b734425007bbe328cb186eb7b070adef02d02e0f334b7abf1c9769368f`  
		Last Modified: Tue, 13 Feb 2024 01:53:26 GMT  
		Size: 394.3 KB (394334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e71ec88dde6821c3682b9f75ed25a997d664d50485223b87ab26b148fba8fdf`  
		Last Modified: Tue, 13 Feb 2024 01:53:27 GMT  
		Size: 77.9 KB (77896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1569272dcfe8e19f61c84f94b9d94e9fbbf0ac368aff718c06b7649e0e9dbe0`  
		Last Modified: Tue, 13 Feb 2024 01:53:27 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94053229a35c71f854d02cbb43092581e8b6cee7ef948f9b514acf1b9115c3b7`  
		Last Modified: Tue, 13 Feb 2024 01:53:28 GMT  
		Size: 52.7 MB (52719476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5574179220fd2064c4c86791f51e71502c5eed795327da1c0271e0a3bdc15025`  
		Last Modified: Tue, 13 Feb 2024 01:53:27 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb73ba5435db91092fe3694f3825701ad5cca6534fc4b12df96ef10ffe0ccf6`  
		Last Modified: Tue, 13 Feb 2024 01:53:28 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c99e0ab115184508946862ec52009d68ac8c02cf34c37517727a457f107cb0`  
		Last Modified: Tue, 13 Feb 2024 01:53:28 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635a5b575816fae0daa6b83453f0895a506e418b8b1ac15a657483365d4d3805`  
		Last Modified: Tue, 13 Feb 2024 01:53:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:d16ee81b162d4ab76c3d63eb24c759731f33182a74a0b8c127b6667ea743186a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3419330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e5d61dcb6a671d4bfabf370e7f61ed671efdcc236747afce88263a09acbbce`

```dockerfile
```

-	Layers:
	-	`sha256:c6b83df7389ff8ad90817f27160f302f285cd712a01ec06c1a98bf8d1eb0de4c`  
		Last Modified: Tue, 13 Feb 2024 01:53:26 GMT  
		Size: 3.4 MB (3387604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a6b40e9e902cc7e5708edcd2d223152519a7f697689ac57e6e6da3af916bcf3`  
		Last Modified: Tue, 13 Feb 2024 01:53:26 GMT  
		Size: 31.7 KB (31726 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:aba4ba41296b2d341929265e7fa5b87f641d58e358f7df3c4c05b9342dea1cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88075288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8a2bfcbb05ca1f3c14795e6c011a1805ad69d1a06c60f82f42e6a9bdcaf509`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
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
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ec1ba56fff57376a1e522907553fc77fc80bb5c48ed5b7746be835f2c791e8`  
		Last Modified: Thu, 01 Feb 2024 08:10:56 GMT  
		Size: 3.4 KB (3351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b20254b0592cead69bb43b1e572ee734ed6053b6445077e621c0af6234886fd`  
		Last Modified: Thu, 01 Feb 2024 08:10:57 GMT  
		Size: 5.0 MB (5004087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef6a435304886e6662c0e0f7d34448ae89903960a5b5747c29472d2ab308627`  
		Last Modified: Thu, 01 Feb 2024 08:10:57 GMT  
		Size: 350.5 KB (350527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b781cbda42a627dc3c93f9890aceb52d86295f2fd6459eae86f20f8928f9680d`  
		Last Modified: Thu, 01 Feb 2024 08:10:57 GMT  
		Size: 77.8 KB (77810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f135e41b52f16d917b667611579ce1a9b1c3c40fb5e1af14399790dd1363d0`  
		Last Modified: Thu, 01 Feb 2024 08:10:58 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60fd9abf17ec23f09f0362ac146a4a65b2e1377942ab70334879ed109e5ea176`  
		Last Modified: Thu, 01 Feb 2024 08:11:01 GMT  
		Size: 52.6 MB (52570938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919712266c6021b3387e6207117af5dcb125015985b3f174ddce70d7be6ba16c`  
		Last Modified: Thu, 01 Feb 2024 08:10:58 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e9f6a099c29cbf0e2a100d023db0b49a861c986bf8348c4422095d0ac09b2b`  
		Last Modified: Thu, 01 Feb 2024 08:10:59 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9007c269b338bc96ebc6dac4b6095fff1f04931e0e157c4863b1d1e6749d966`  
		Last Modified: Thu, 01 Feb 2024 08:10:59 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f229d8adc49602ddfc4cf87a6113566613959aa6f886e99244b294bd04c756`  
		Last Modified: Thu, 01 Feb 2024 08:11:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:b12586e7bf95de93b3536776f20986afff6aba57c6c150e82a0b13e5bf2d88df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3327922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eb1b85ebe108c883131c50f629b135ec4be556d9cb45a989876a93ca2f9366b`

```dockerfile
```

-	Layers:
	-	`sha256:133a0faddb7b4761e933cfc1db8ec5c9527f0f3025a2932950e637ca3446c44c`  
		Last Modified: Thu, 01 Feb 2024 08:10:57 GMT  
		Size: 3.3 MB (3296186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a92a98cf3352f51a7cfc54e983dd964e15db84ed67274e2550de9a59a3948a6`  
		Last Modified: Thu, 01 Feb 2024 08:10:56 GMT  
		Size: 31.7 KB (31736 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:583c58b2c631d310e8dd60c12a592ed075407fc5f68c3d14f8cb8c4105a7abc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95366126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e50cc7222008fd7804f91251acb7adcd498234fbb452c334de5ce685b8a49c1d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:35bb0428da48f0fbc9230db1ecddacb636bc61d82e6701574b518b720ae76d7f in / 
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
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:4df9a94c24ca5c52fd8a7f1aebc76690845edac56c36acaf79a984722b5e4e48`  
		Last Modified: Wed, 31 Jan 2024 22:35:16 GMT  
		Size: 35.3 MB (35293643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92f458db7320742599ab920741e07f9544cfd58f5b8686398d8966491b06f0f`  
		Last Modified: Thu, 01 Feb 2024 08:47:38 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cb9aa6b890ce8b704b2fc45c763a345ac7e2d83897d23f16186a05c4cbdbf9`  
		Last Modified: Thu, 01 Feb 2024 08:47:39 GMT  
		Size: 5.8 MB (5839188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1fbcb0d9961bb5bbde2b4b8215a1acd828df14abb5c76cdf98b4721c114bf1b`  
		Last Modified: Thu, 01 Feb 2024 08:47:39 GMT  
		Size: 446.7 KB (446667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023feedddc4860debc352c7ee2d9cd2885475659c7bc489eb74d89bd8ff14289`  
		Last Modified: Thu, 01 Feb 2024 08:47:40 GMT  
		Size: 77.9 KB (77900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33e850eba7cad89ca5087696f33c7ef6c29970a0d63be2e113e430b80f8c586`  
		Last Modified: Thu, 01 Feb 2024 08:47:40 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a44471fd006a5678cbd2ffaedd491dc3be8a8be56c8061db116fa085775ca1e6`  
		Last Modified: Thu, 01 Feb 2024 08:47:42 GMT  
		Size: 53.7 MB (53701137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48088e727ddc2db68bace99d3603026c3c92617ed9111f71c537b916aa0b5476`  
		Last Modified: Thu, 01 Feb 2024 08:47:41 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240dd27ec561dea5460665a316655f0aaaf2694a36db5adf88ff60c42019b1f5`  
		Last Modified: Thu, 01 Feb 2024 08:47:41 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a868dbb1cf5a7405695a29166dabe6be49a39eea3fb6ec2c90140ddede8265`  
		Last Modified: Thu, 01 Feb 2024 08:47:41 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d83e584f48b1ad066f05a03876f9ba26d6a68289e78c1ddbfc81bc21f211dd0`  
		Last Modified: Thu, 01 Feb 2024 08:47:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:ff19866200f9ca8aede65e78dbdfbe2695263926361922ebbff21151ac56aeba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3332254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a79d8c47ad4dd103ca59e9d983352e5ed55b3bfa3f927d618c6231ba1467dae`

```dockerfile
```

-	Layers:
	-	`sha256:1dabb5c0cafb5d7c64c681533260175d71ebcd148f7e9f41e6dc2b9630b536be`  
		Last Modified: Thu, 01 Feb 2024 08:47:39 GMT  
		Size: 3.3 MB (3300478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1266308b253a21d2adf89309c140514433b8e382a1aa16a118f0ee0def0228a9`  
		Last Modified: Thu, 01 Feb 2024 08:47:39 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; s390x

```console
$ docker pull couchdb@sha256:080c1de9aacbafef98684af7143fceca19926658bf69e495c9eaf5d82b0ee7ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86380517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55b098b432b943d787618e921aceb298b5577ee029ceab52415740d3b2dcce6e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:9a48c9d7fde8a2820cff9dc06434dc4dca8967438fa75bb93e6646cb44682b18 in / 
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
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:16651f5430ff52661c6729a9dc23c80d76205b6bd77d7730f38e39aca6731613`  
		Last Modified: Wed, 31 Jan 2024 23:29:40 GMT  
		Size: 29.7 MB (29657133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee3a0014482f190b29e7494f752808b6091b9a1dc21e95ca84554dc9b2e1cf7`  
		Last Modified: Thu, 01 Feb 2024 20:19:29 GMT  
		Size: 3.4 KB (3351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd8f5d8f498e66b04e07425c6d208f4dac87da21571314c3c29dad8ee96f014`  
		Last Modified: Thu, 01 Feb 2024 20:19:29 GMT  
		Size: 4.9 MB (4905554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c1c9f5ef6ccc47a6527e801ae5b534ede814bea1eb564abb63fba5367f8f20`  
		Last Modified: Thu, 01 Feb 2024 20:19:29 GMT  
		Size: 357.5 KB (357486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4044f8c1f294d8fc68c5a2c8daa30a8367d55128d9c795a74f9b5beb90e692ec`  
		Last Modified: Thu, 01 Feb 2024 20:19:30 GMT  
		Size: 77.8 KB (77849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97164cc599174153fa4fa6a7e3301eb60cf6caea1d81f74a1c1472cad406bf1`  
		Last Modified: Thu, 01 Feb 2024 20:19:30 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637a131379dee3f1cf9126a6973e37a6b30f10fdad830a30366295e5f97029aa`  
		Last Modified: Thu, 01 Feb 2024 20:19:31 GMT  
		Size: 51.4 MB (51374897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7a24b7d988302402886e32e4d08938faef1b31a27c533345d52bc184facbe4`  
		Last Modified: Thu, 01 Feb 2024 20:19:31 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0675d1c86abe9bbabcf7289c08791fbfc14005b01548de8678bb741971f0ca3`  
		Last Modified: Thu, 01 Feb 2024 20:19:31 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5078d90be17ce6b9ff3303773b194f78e6223fabc751d1299ca513d125964385`  
		Last Modified: Thu, 01 Feb 2024 20:19:31 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264b1f6b9b621e7e19168b4a2b4c74c8fd4569dee3971a3a5a19ba81d3d5cc7c`  
		Last Modified: Thu, 01 Feb 2024 20:19:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:9848e5715284986e828c3199ece6005a64cb9f7068af3bef360c71f24d19601a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3327136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d992047f39681d2d08f32e199d591cba16e5839804c320d98fb1fed6db0769`

```dockerfile
```

-	Layers:
	-	`sha256:3bb1797658c828db62b2c9f0f28e6b85ea80c6e241576ca7dae6da5b03a227da`  
		Last Modified: Thu, 01 Feb 2024 20:19:29 GMT  
		Size: 3.3 MB (3295410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23a896bfbf2407b03c6215476c940a4a0f1f63c4b707faa2770a0d91f1ff6e44`  
		Last Modified: Thu, 01 Feb 2024 20:19:29 GMT  
		Size: 31.7 KB (31726 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.3.3`

```console
$ docker pull couchdb@sha256:2a51754c959060108556c0828e1e48ba72b8d6ac05d22d0efe2ffbc8a839e262
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
$ docker pull couchdb@sha256:405419c4ecce18030dbd1dd7fe692e349f83a0d68df71b6d40238c0c0dd45c73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89844973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3731fb1117f02a201e062576679a4d18a995cd23501c55013b528a2d549ee631`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
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
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249a1605c575ce96487ffac541cf15846a8ea40db5a3ea5145e408c89b649b1b`  
		Last Modified: Tue, 13 Feb 2024 01:53:26 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096352bc9320e7991dd9c0362807fb9a4d4597d01fce5fd6d3ba34c3bc92e6e1`  
		Last Modified: Tue, 13 Feb 2024 01:53:26 GMT  
		Size: 5.2 MB (5223271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201c40b734425007bbe328cb186eb7b070adef02d02e0f334b7abf1c9769368f`  
		Last Modified: Tue, 13 Feb 2024 01:53:26 GMT  
		Size: 394.3 KB (394334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e71ec88dde6821c3682b9f75ed25a997d664d50485223b87ab26b148fba8fdf`  
		Last Modified: Tue, 13 Feb 2024 01:53:27 GMT  
		Size: 77.9 KB (77896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1569272dcfe8e19f61c84f94b9d94e9fbbf0ac368aff718c06b7649e0e9dbe0`  
		Last Modified: Tue, 13 Feb 2024 01:53:27 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94053229a35c71f854d02cbb43092581e8b6cee7ef948f9b514acf1b9115c3b7`  
		Last Modified: Tue, 13 Feb 2024 01:53:28 GMT  
		Size: 52.7 MB (52719476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5574179220fd2064c4c86791f51e71502c5eed795327da1c0271e0a3bdc15025`  
		Last Modified: Tue, 13 Feb 2024 01:53:27 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb73ba5435db91092fe3694f3825701ad5cca6534fc4b12df96ef10ffe0ccf6`  
		Last Modified: Tue, 13 Feb 2024 01:53:28 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c99e0ab115184508946862ec52009d68ac8c02cf34c37517727a457f107cb0`  
		Last Modified: Tue, 13 Feb 2024 01:53:28 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635a5b575816fae0daa6b83453f0895a506e418b8b1ac15a657483365d4d3805`  
		Last Modified: Tue, 13 Feb 2024 01:53:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:d16ee81b162d4ab76c3d63eb24c759731f33182a74a0b8c127b6667ea743186a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3419330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e5d61dcb6a671d4bfabf370e7f61ed671efdcc236747afce88263a09acbbce`

```dockerfile
```

-	Layers:
	-	`sha256:c6b83df7389ff8ad90817f27160f302f285cd712a01ec06c1a98bf8d1eb0de4c`  
		Last Modified: Tue, 13 Feb 2024 01:53:26 GMT  
		Size: 3.4 MB (3387604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a6b40e9e902cc7e5708edcd2d223152519a7f697689ac57e6e6da3af916bcf3`  
		Last Modified: Tue, 13 Feb 2024 01:53:26 GMT  
		Size: 31.7 KB (31726 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:aba4ba41296b2d341929265e7fa5b87f641d58e358f7df3c4c05b9342dea1cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88075288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8a2bfcbb05ca1f3c14795e6c011a1805ad69d1a06c60f82f42e6a9bdcaf509`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
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
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ec1ba56fff57376a1e522907553fc77fc80bb5c48ed5b7746be835f2c791e8`  
		Last Modified: Thu, 01 Feb 2024 08:10:56 GMT  
		Size: 3.4 KB (3351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b20254b0592cead69bb43b1e572ee734ed6053b6445077e621c0af6234886fd`  
		Last Modified: Thu, 01 Feb 2024 08:10:57 GMT  
		Size: 5.0 MB (5004087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef6a435304886e6662c0e0f7d34448ae89903960a5b5747c29472d2ab308627`  
		Last Modified: Thu, 01 Feb 2024 08:10:57 GMT  
		Size: 350.5 KB (350527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b781cbda42a627dc3c93f9890aceb52d86295f2fd6459eae86f20f8928f9680d`  
		Last Modified: Thu, 01 Feb 2024 08:10:57 GMT  
		Size: 77.8 KB (77810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f135e41b52f16d917b667611579ce1a9b1c3c40fb5e1af14399790dd1363d0`  
		Last Modified: Thu, 01 Feb 2024 08:10:58 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60fd9abf17ec23f09f0362ac146a4a65b2e1377942ab70334879ed109e5ea176`  
		Last Modified: Thu, 01 Feb 2024 08:11:01 GMT  
		Size: 52.6 MB (52570938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919712266c6021b3387e6207117af5dcb125015985b3f174ddce70d7be6ba16c`  
		Last Modified: Thu, 01 Feb 2024 08:10:58 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e9f6a099c29cbf0e2a100d023db0b49a861c986bf8348c4422095d0ac09b2b`  
		Last Modified: Thu, 01 Feb 2024 08:10:59 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9007c269b338bc96ebc6dac4b6095fff1f04931e0e157c4863b1d1e6749d966`  
		Last Modified: Thu, 01 Feb 2024 08:10:59 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f229d8adc49602ddfc4cf87a6113566613959aa6f886e99244b294bd04c756`  
		Last Modified: Thu, 01 Feb 2024 08:11:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:b12586e7bf95de93b3536776f20986afff6aba57c6c150e82a0b13e5bf2d88df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3327922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eb1b85ebe108c883131c50f629b135ec4be556d9cb45a989876a93ca2f9366b`

```dockerfile
```

-	Layers:
	-	`sha256:133a0faddb7b4761e933cfc1db8ec5c9527f0f3025a2932950e637ca3446c44c`  
		Last Modified: Thu, 01 Feb 2024 08:10:57 GMT  
		Size: 3.3 MB (3296186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a92a98cf3352f51a7cfc54e983dd964e15db84ed67274e2550de9a59a3948a6`  
		Last Modified: Thu, 01 Feb 2024 08:10:56 GMT  
		Size: 31.7 KB (31736 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:583c58b2c631d310e8dd60c12a592ed075407fc5f68c3d14f8cb8c4105a7abc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95366126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e50cc7222008fd7804f91251acb7adcd498234fbb452c334de5ce685b8a49c1d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:35bb0428da48f0fbc9230db1ecddacb636bc61d82e6701574b518b720ae76d7f in / 
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
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:4df9a94c24ca5c52fd8a7f1aebc76690845edac56c36acaf79a984722b5e4e48`  
		Last Modified: Wed, 31 Jan 2024 22:35:16 GMT  
		Size: 35.3 MB (35293643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92f458db7320742599ab920741e07f9544cfd58f5b8686398d8966491b06f0f`  
		Last Modified: Thu, 01 Feb 2024 08:47:38 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cb9aa6b890ce8b704b2fc45c763a345ac7e2d83897d23f16186a05c4cbdbf9`  
		Last Modified: Thu, 01 Feb 2024 08:47:39 GMT  
		Size: 5.8 MB (5839188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1fbcb0d9961bb5bbde2b4b8215a1acd828df14abb5c76cdf98b4721c114bf1b`  
		Last Modified: Thu, 01 Feb 2024 08:47:39 GMT  
		Size: 446.7 KB (446667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023feedddc4860debc352c7ee2d9cd2885475659c7bc489eb74d89bd8ff14289`  
		Last Modified: Thu, 01 Feb 2024 08:47:40 GMT  
		Size: 77.9 KB (77900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33e850eba7cad89ca5087696f33c7ef6c29970a0d63be2e113e430b80f8c586`  
		Last Modified: Thu, 01 Feb 2024 08:47:40 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a44471fd006a5678cbd2ffaedd491dc3be8a8be56c8061db116fa085775ca1e6`  
		Last Modified: Thu, 01 Feb 2024 08:47:42 GMT  
		Size: 53.7 MB (53701137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48088e727ddc2db68bace99d3603026c3c92617ed9111f71c537b916aa0b5476`  
		Last Modified: Thu, 01 Feb 2024 08:47:41 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240dd27ec561dea5460665a316655f0aaaf2694a36db5adf88ff60c42019b1f5`  
		Last Modified: Thu, 01 Feb 2024 08:47:41 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a868dbb1cf5a7405695a29166dabe6be49a39eea3fb6ec2c90140ddede8265`  
		Last Modified: Thu, 01 Feb 2024 08:47:41 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d83e584f48b1ad066f05a03876f9ba26d6a68289e78c1ddbfc81bc21f211dd0`  
		Last Modified: Thu, 01 Feb 2024 08:47:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:ff19866200f9ca8aede65e78dbdfbe2695263926361922ebbff21151ac56aeba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3332254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a79d8c47ad4dd103ca59e9d983352e5ed55b3bfa3f927d618c6231ba1467dae`

```dockerfile
```

-	Layers:
	-	`sha256:1dabb5c0cafb5d7c64c681533260175d71ebcd148f7e9f41e6dc2b9630b536be`  
		Last Modified: Thu, 01 Feb 2024 08:47:39 GMT  
		Size: 3.3 MB (3300478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1266308b253a21d2adf89309c140514433b8e382a1aa16a118f0ee0def0228a9`  
		Last Modified: Thu, 01 Feb 2024 08:47:39 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; s390x

```console
$ docker pull couchdb@sha256:080c1de9aacbafef98684af7143fceca19926658bf69e495c9eaf5d82b0ee7ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86380517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55b098b432b943d787618e921aceb298b5577ee029ceab52415740d3b2dcce6e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:9a48c9d7fde8a2820cff9dc06434dc4dca8967438fa75bb93e6646cb44682b18 in / 
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
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:16651f5430ff52661c6729a9dc23c80d76205b6bd77d7730f38e39aca6731613`  
		Last Modified: Wed, 31 Jan 2024 23:29:40 GMT  
		Size: 29.7 MB (29657133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee3a0014482f190b29e7494f752808b6091b9a1dc21e95ca84554dc9b2e1cf7`  
		Last Modified: Thu, 01 Feb 2024 20:19:29 GMT  
		Size: 3.4 KB (3351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd8f5d8f498e66b04e07425c6d208f4dac87da21571314c3c29dad8ee96f014`  
		Last Modified: Thu, 01 Feb 2024 20:19:29 GMT  
		Size: 4.9 MB (4905554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c1c9f5ef6ccc47a6527e801ae5b534ede814bea1eb564abb63fba5367f8f20`  
		Last Modified: Thu, 01 Feb 2024 20:19:29 GMT  
		Size: 357.5 KB (357486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4044f8c1f294d8fc68c5a2c8daa30a8367d55128d9c795a74f9b5beb90e692ec`  
		Last Modified: Thu, 01 Feb 2024 20:19:30 GMT  
		Size: 77.8 KB (77849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97164cc599174153fa4fa6a7e3301eb60cf6caea1d81f74a1c1472cad406bf1`  
		Last Modified: Thu, 01 Feb 2024 20:19:30 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637a131379dee3f1cf9126a6973e37a6b30f10fdad830a30366295e5f97029aa`  
		Last Modified: Thu, 01 Feb 2024 20:19:31 GMT  
		Size: 51.4 MB (51374897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7a24b7d988302402886e32e4d08938faef1b31a27c533345d52bc184facbe4`  
		Last Modified: Thu, 01 Feb 2024 20:19:31 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0675d1c86abe9bbabcf7289c08791fbfc14005b01548de8678bb741971f0ca3`  
		Last Modified: Thu, 01 Feb 2024 20:19:31 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5078d90be17ce6b9ff3303773b194f78e6223fabc751d1299ca513d125964385`  
		Last Modified: Thu, 01 Feb 2024 20:19:31 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264b1f6b9b621e7e19168b4a2b4c74c8fd4569dee3971a3a5a19ba81d3d5cc7c`  
		Last Modified: Thu, 01 Feb 2024 20:19:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:9848e5715284986e828c3199ece6005a64cb9f7068af3bef360c71f24d19601a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3327136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d992047f39681d2d08f32e199d591cba16e5839804c320d98fb1fed6db0769`

```dockerfile
```

-	Layers:
	-	`sha256:3bb1797658c828db62b2c9f0f28e6b85ea80c6e241576ca7dae6da5b03a227da`  
		Last Modified: Thu, 01 Feb 2024 20:19:29 GMT  
		Size: 3.3 MB (3295410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23a896bfbf2407b03c6215476c940a4a0f1f63c4b707faa2770a0d91f1ff6e44`  
		Last Modified: Thu, 01 Feb 2024 20:19:29 GMT  
		Size: 31.7 KB (31726 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:2a51754c959060108556c0828e1e48ba72b8d6ac05d22d0efe2ffbc8a839e262
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
$ docker pull couchdb@sha256:405419c4ecce18030dbd1dd7fe692e349f83a0d68df71b6d40238c0c0dd45c73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89844973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3731fb1117f02a201e062576679a4d18a995cd23501c55013b528a2d549ee631`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
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
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249a1605c575ce96487ffac541cf15846a8ea40db5a3ea5145e408c89b649b1b`  
		Last Modified: Tue, 13 Feb 2024 01:53:26 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096352bc9320e7991dd9c0362807fb9a4d4597d01fce5fd6d3ba34c3bc92e6e1`  
		Last Modified: Tue, 13 Feb 2024 01:53:26 GMT  
		Size: 5.2 MB (5223271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201c40b734425007bbe328cb186eb7b070adef02d02e0f334b7abf1c9769368f`  
		Last Modified: Tue, 13 Feb 2024 01:53:26 GMT  
		Size: 394.3 KB (394334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e71ec88dde6821c3682b9f75ed25a997d664d50485223b87ab26b148fba8fdf`  
		Last Modified: Tue, 13 Feb 2024 01:53:27 GMT  
		Size: 77.9 KB (77896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1569272dcfe8e19f61c84f94b9d94e9fbbf0ac368aff718c06b7649e0e9dbe0`  
		Last Modified: Tue, 13 Feb 2024 01:53:27 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94053229a35c71f854d02cbb43092581e8b6cee7ef948f9b514acf1b9115c3b7`  
		Last Modified: Tue, 13 Feb 2024 01:53:28 GMT  
		Size: 52.7 MB (52719476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5574179220fd2064c4c86791f51e71502c5eed795327da1c0271e0a3bdc15025`  
		Last Modified: Tue, 13 Feb 2024 01:53:27 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb73ba5435db91092fe3694f3825701ad5cca6534fc4b12df96ef10ffe0ccf6`  
		Last Modified: Tue, 13 Feb 2024 01:53:28 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c99e0ab115184508946862ec52009d68ac8c02cf34c37517727a457f107cb0`  
		Last Modified: Tue, 13 Feb 2024 01:53:28 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635a5b575816fae0daa6b83453f0895a506e418b8b1ac15a657483365d4d3805`  
		Last Modified: Tue, 13 Feb 2024 01:53:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:d16ee81b162d4ab76c3d63eb24c759731f33182a74a0b8c127b6667ea743186a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3419330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e5d61dcb6a671d4bfabf370e7f61ed671efdcc236747afce88263a09acbbce`

```dockerfile
```

-	Layers:
	-	`sha256:c6b83df7389ff8ad90817f27160f302f285cd712a01ec06c1a98bf8d1eb0de4c`  
		Last Modified: Tue, 13 Feb 2024 01:53:26 GMT  
		Size: 3.4 MB (3387604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a6b40e9e902cc7e5708edcd2d223152519a7f697689ac57e6e6da3af916bcf3`  
		Last Modified: Tue, 13 Feb 2024 01:53:26 GMT  
		Size: 31.7 KB (31726 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:aba4ba41296b2d341929265e7fa5b87f641d58e358f7df3c4c05b9342dea1cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88075288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8a2bfcbb05ca1f3c14795e6c011a1805ad69d1a06c60f82f42e6a9bdcaf509`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
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
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ec1ba56fff57376a1e522907553fc77fc80bb5c48ed5b7746be835f2c791e8`  
		Last Modified: Thu, 01 Feb 2024 08:10:56 GMT  
		Size: 3.4 KB (3351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b20254b0592cead69bb43b1e572ee734ed6053b6445077e621c0af6234886fd`  
		Last Modified: Thu, 01 Feb 2024 08:10:57 GMT  
		Size: 5.0 MB (5004087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef6a435304886e6662c0e0f7d34448ae89903960a5b5747c29472d2ab308627`  
		Last Modified: Thu, 01 Feb 2024 08:10:57 GMT  
		Size: 350.5 KB (350527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b781cbda42a627dc3c93f9890aceb52d86295f2fd6459eae86f20f8928f9680d`  
		Last Modified: Thu, 01 Feb 2024 08:10:57 GMT  
		Size: 77.8 KB (77810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f135e41b52f16d917b667611579ce1a9b1c3c40fb5e1af14399790dd1363d0`  
		Last Modified: Thu, 01 Feb 2024 08:10:58 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60fd9abf17ec23f09f0362ac146a4a65b2e1377942ab70334879ed109e5ea176`  
		Last Modified: Thu, 01 Feb 2024 08:11:01 GMT  
		Size: 52.6 MB (52570938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919712266c6021b3387e6207117af5dcb125015985b3f174ddce70d7be6ba16c`  
		Last Modified: Thu, 01 Feb 2024 08:10:58 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e9f6a099c29cbf0e2a100d023db0b49a861c986bf8348c4422095d0ac09b2b`  
		Last Modified: Thu, 01 Feb 2024 08:10:59 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9007c269b338bc96ebc6dac4b6095fff1f04931e0e157c4863b1d1e6749d966`  
		Last Modified: Thu, 01 Feb 2024 08:10:59 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f229d8adc49602ddfc4cf87a6113566613959aa6f886e99244b294bd04c756`  
		Last Modified: Thu, 01 Feb 2024 08:11:00 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:b12586e7bf95de93b3536776f20986afff6aba57c6c150e82a0b13e5bf2d88df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3327922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eb1b85ebe108c883131c50f629b135ec4be556d9cb45a989876a93ca2f9366b`

```dockerfile
```

-	Layers:
	-	`sha256:133a0faddb7b4761e933cfc1db8ec5c9527f0f3025a2932950e637ca3446c44c`  
		Last Modified: Thu, 01 Feb 2024 08:10:57 GMT  
		Size: 3.3 MB (3296186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a92a98cf3352f51a7cfc54e983dd964e15db84ed67274e2550de9a59a3948a6`  
		Last Modified: Thu, 01 Feb 2024 08:10:56 GMT  
		Size: 31.7 KB (31736 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:583c58b2c631d310e8dd60c12a592ed075407fc5f68c3d14f8cb8c4105a7abc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95366126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e50cc7222008fd7804f91251acb7adcd498234fbb452c334de5ce685b8a49c1d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:35bb0428da48f0fbc9230db1ecddacb636bc61d82e6701574b518b720ae76d7f in / 
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
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:4df9a94c24ca5c52fd8a7f1aebc76690845edac56c36acaf79a984722b5e4e48`  
		Last Modified: Wed, 31 Jan 2024 22:35:16 GMT  
		Size: 35.3 MB (35293643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92f458db7320742599ab920741e07f9544cfd58f5b8686398d8966491b06f0f`  
		Last Modified: Thu, 01 Feb 2024 08:47:38 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cb9aa6b890ce8b704b2fc45c763a345ac7e2d83897d23f16186a05c4cbdbf9`  
		Last Modified: Thu, 01 Feb 2024 08:47:39 GMT  
		Size: 5.8 MB (5839188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1fbcb0d9961bb5bbde2b4b8215a1acd828df14abb5c76cdf98b4721c114bf1b`  
		Last Modified: Thu, 01 Feb 2024 08:47:39 GMT  
		Size: 446.7 KB (446667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023feedddc4860debc352c7ee2d9cd2885475659c7bc489eb74d89bd8ff14289`  
		Last Modified: Thu, 01 Feb 2024 08:47:40 GMT  
		Size: 77.9 KB (77900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33e850eba7cad89ca5087696f33c7ef6c29970a0d63be2e113e430b80f8c586`  
		Last Modified: Thu, 01 Feb 2024 08:47:40 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a44471fd006a5678cbd2ffaedd491dc3be8a8be56c8061db116fa085775ca1e6`  
		Last Modified: Thu, 01 Feb 2024 08:47:42 GMT  
		Size: 53.7 MB (53701137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48088e727ddc2db68bace99d3603026c3c92617ed9111f71c537b916aa0b5476`  
		Last Modified: Thu, 01 Feb 2024 08:47:41 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240dd27ec561dea5460665a316655f0aaaf2694a36db5adf88ff60c42019b1f5`  
		Last Modified: Thu, 01 Feb 2024 08:47:41 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a868dbb1cf5a7405695a29166dabe6be49a39eea3fb6ec2c90140ddede8265`  
		Last Modified: Thu, 01 Feb 2024 08:47:41 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d83e584f48b1ad066f05a03876f9ba26d6a68289e78c1ddbfc81bc21f211dd0`  
		Last Modified: Thu, 01 Feb 2024 08:47:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:ff19866200f9ca8aede65e78dbdfbe2695263926361922ebbff21151ac56aeba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3332254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a79d8c47ad4dd103ca59e9d983352e5ed55b3bfa3f927d618c6231ba1467dae`

```dockerfile
```

-	Layers:
	-	`sha256:1dabb5c0cafb5d7c64c681533260175d71ebcd148f7e9f41e6dc2b9630b536be`  
		Last Modified: Thu, 01 Feb 2024 08:47:39 GMT  
		Size: 3.3 MB (3300478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1266308b253a21d2adf89309c140514433b8e382a1aa16a118f0ee0def0228a9`  
		Last Modified: Thu, 01 Feb 2024 08:47:39 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:080c1de9aacbafef98684af7143fceca19926658bf69e495c9eaf5d82b0ee7ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86380517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55b098b432b943d787618e921aceb298b5577ee029ceab52415740d3b2dcce6e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:9a48c9d7fde8a2820cff9dc06434dc4dca8967438fa75bb93e6646cb44682b18 in / 
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
COPY 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 05 Dec 2023 19:33:12 GMT
COPY vm.args /opt/couchdb/etc/ # buildkit
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
	-	`sha256:16651f5430ff52661c6729a9dc23c80d76205b6bd77d7730f38e39aca6731613`  
		Last Modified: Wed, 31 Jan 2024 23:29:40 GMT  
		Size: 29.7 MB (29657133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee3a0014482f190b29e7494f752808b6091b9a1dc21e95ca84554dc9b2e1cf7`  
		Last Modified: Thu, 01 Feb 2024 20:19:29 GMT  
		Size: 3.4 KB (3351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd8f5d8f498e66b04e07425c6d208f4dac87da21571314c3c29dad8ee96f014`  
		Last Modified: Thu, 01 Feb 2024 20:19:29 GMT  
		Size: 4.9 MB (4905554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c1c9f5ef6ccc47a6527e801ae5b534ede814bea1eb564abb63fba5367f8f20`  
		Last Modified: Thu, 01 Feb 2024 20:19:29 GMT  
		Size: 357.5 KB (357486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4044f8c1f294d8fc68c5a2c8daa30a8367d55128d9c795a74f9b5beb90e692ec`  
		Last Modified: Thu, 01 Feb 2024 20:19:30 GMT  
		Size: 77.8 KB (77849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97164cc599174153fa4fa6a7e3301eb60cf6caea1d81f74a1c1472cad406bf1`  
		Last Modified: Thu, 01 Feb 2024 20:19:30 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637a131379dee3f1cf9126a6973e37a6b30f10fdad830a30366295e5f97029aa`  
		Last Modified: Thu, 01 Feb 2024 20:19:31 GMT  
		Size: 51.4 MB (51374897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7a24b7d988302402886e32e4d08938faef1b31a27c533345d52bc184facbe4`  
		Last Modified: Thu, 01 Feb 2024 20:19:31 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0675d1c86abe9bbabcf7289c08791fbfc14005b01548de8678bb741971f0ca3`  
		Last Modified: Thu, 01 Feb 2024 20:19:31 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5078d90be17ce6b9ff3303773b194f78e6223fabc751d1299ca513d125964385`  
		Last Modified: Thu, 01 Feb 2024 20:19:31 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264b1f6b9b621e7e19168b4a2b4c74c8fd4569dee3971a3a5a19ba81d3d5cc7c`  
		Last Modified: Thu, 01 Feb 2024 20:19:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:9848e5715284986e828c3199ece6005a64cb9f7068af3bef360c71f24d19601a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3327136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d992047f39681d2d08f32e199d591cba16e5839804c320d98fb1fed6db0769`

```dockerfile
```

-	Layers:
	-	`sha256:3bb1797658c828db62b2c9f0f28e6b85ea80c6e241576ca7dae6da5b03a227da`  
		Last Modified: Thu, 01 Feb 2024 20:19:29 GMT  
		Size: 3.3 MB (3295410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23a896bfbf2407b03c6215476c940a4a0f1f63c4b707faa2770a0d91f1ff6e44`  
		Last Modified: Thu, 01 Feb 2024 20:19:29 GMT  
		Size: 31.7 KB (31726 bytes)  
		MIME: application/vnd.in-toto+json
