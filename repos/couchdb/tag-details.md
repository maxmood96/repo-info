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
-	[`couchdb:3.5.0`](#couchdb350)
-	[`couchdb:3.5.0-nouveau`](#couchdb350-nouveau)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:3`

```console
$ docker pull couchdb@sha256:6c8a172f9aa64020d9a28c5bcbbdd3852b12125c5a2ab7345d7525abc8c7dfad
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
$ docker pull couchdb@sha256:559adbf2abdcf39ec99438c9ec22f9fd99128c80e6b8cc8dadb6d9375b046ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139826730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c85f9965112d24415932aa1fcfcde7badc9d2af1e311157270e41d4bd3bc88`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c3653e969dba91bf2d72c46e9130dec51413c23470ff9c7600b1b9a2a22c15`  
		Last Modified: Tue, 01 Jul 2025 02:26:21 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669656cd19f0d2cb942f87fdf029d76d45f8659f8de4fa6fc763498cdf182c43`  
		Last Modified: Tue, 01 Jul 2025 02:26:22 GMT  
		Size: 7.9 MB (7880077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073b8f1405c2e7f5538a819f3cb16871c9d23ca63bc1908604e0c1af55a6c5f0`  
		Last Modified: Tue, 01 Jul 2025 02:26:22 GMT  
		Size: 392.2 KB (392155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a088a900fab20f7d7abdac9ed1b6a2424012c6090811bc148da1f638df2aeff`  
		Last Modified: Tue, 01 Jul 2025 02:26:21 GMT  
		Size: 76.3 KB (76292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acb5c0c5c3da23be9cbf3c8f9e667dd82bc717526d3f3a8d898a66f1c1ae2f5`  
		Last Modified: Tue, 01 Jul 2025 02:26:21 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36349e7d193a6d840744dcbb64fa007f223dd6514434ae595a55d7061141f6f`  
		Last Modified: Tue, 01 Jul 2025 02:26:29 GMT  
		Size: 103.2 MB (103242642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c265eaefef330605b11794439399d081e9fc30f04386bf368f80a7d45db9fdd`  
		Last Modified: Tue, 01 Jul 2025 02:26:21 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5093f072c38d770ebd9bab0fe8fe8d88ab2fc2843666cb4f31610ccd0485f0`  
		Last Modified: Tue, 01 Jul 2025 02:26:21 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f71f0a586f2926bd9b4ffb04a1e2ae60b01a47bcafb0fb71a544a1fcd094d0`  
		Last Modified: Tue, 01 Jul 2025 02:26:22 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa3e8c78ebfbc39808737a5c8af960782293837715eaa8054b94523d9f6efa9`  
		Last Modified: Tue, 01 Jul 2025 02:26:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:db1bc8f53da793df6ec4ba90325f1fc6fa8c0096396ed58d2f359e87af02eaad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4170730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0035fc1e70dac383413afc75dc284be2f43b92e1097dbdaf992e45ad3a6d40`

```dockerfile
```

-	Layers:
	-	`sha256:b546dc6207c4fcb6f3ec3b18acf42bb82c203ab6118fd2d19002611cc3983aef`  
		Last Modified: Tue, 01 Jul 2025 04:33:20 GMT  
		Size: 4.1 MB (4138949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:604740e2a9a064960e852a52f212bce3bdfa1bb4f28a692115744e097dca49be`  
		Last Modified: Tue, 01 Jul 2025 04:33:20 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:b4afa7cd0272b0d4093f886b715f7df199ce2beda69aaf8736ba2730cc974d9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139071247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7521534de45ccf5227aba43a1b0681c1fcd41ff93302471185eee8cecd984bed`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057de2c1ce1dcd497a72f651e85c5c264a9cddcc9c4e3a9212efcd2ffde822f9`  
		Last Modified: Tue, 01 Jul 2025 06:55:58 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d789849c49c3d61dca13a6d384124e89af9aba2681d81849d2bfeada0c45e0`  
		Last Modified: Tue, 01 Jul 2025 06:55:59 GMT  
		Size: 7.7 MB (7659249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b17c162e267f76b3133ea3b14f100b475df8ea392a73b744e56298491d4a8b`  
		Last Modified: Tue, 01 Jul 2025 06:55:59 GMT  
		Size: 349.0 KB (348987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbfba2339642f8fdfdebf0bfe490c31c7d25f1558bf4e67bfdfd3b74d605b2d`  
		Last Modified: Tue, 01 Jul 2025 06:55:58 GMT  
		Size: 76.3 KB (76332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f096dbc2fc52e8e0ac8d6f43dcb6f377663760330864e2c53bf1453e5e81888`  
		Last Modified: Tue, 01 Jul 2025 06:55:58 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f193351f15f4f3106ca77ca9b3f09a278b33be341eaa6a75b187185d44c4e2`  
		Last Modified: Tue, 01 Jul 2025 06:56:04 GMT  
		Size: 102.9 MB (102903570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20cf586e8e201643afca22216e624b19e180bf42ff21599c6519ae146fb33993`  
		Last Modified: Tue, 01 Jul 2025 06:55:58 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221274c508510f838ecfef7e14486ae6aa5d8660bb39963e9c06c2c31940d3e5`  
		Last Modified: Tue, 01 Jul 2025 06:55:58 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09397da69982d94f542b2bf8fdde3b4860486ccdd47539cc9b9afc0b9bd1a3b5`  
		Last Modified: Tue, 01 Jul 2025 06:55:58 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ae5a71de8a50502b40c9ff6ccbdd6d0804cf5171bf03695ee630ac525cafed`  
		Last Modified: Tue, 01 Jul 2025 06:55:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:9a97e8b52454838dc7b70ff7a33b60b7947aea730389cbaba963a6765dd4e341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4171217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b276c1b3b9170df5e035c2a2c7f6de25afb8620bfb50bdf27a83ca54ea4eebc9`

```dockerfile
```

-	Layers:
	-	`sha256:bf1b2ccaa466fdfdd3b5019257f958be163d0aad3e5050c4ba7e765803b5a55e`  
		Last Modified: Tue, 01 Jul 2025 07:33:26 GMT  
		Size: 4.1 MB (4139242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c720b19990429e8a1f92a410aee8043df9db2dd289beafcb3c7b83c0966b824`  
		Last Modified: Tue, 01 Jul 2025 07:33:27 GMT  
		Size: 32.0 KB (31975 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; s390x

```console
$ docker pull couchdb@sha256:ac73fdf4fd54cee56fc8b6a426f51fc1b8e22ec5e16bdbaefaa6ce2f3f0b2664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136519415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c56607e8d73bd9020c348266288695dd30b582708275bea02973a416de330b8`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2126b1cb24a815801c16b429e02991eaeb9b8f45dc5690d80b3f27caaa0d598`  
		Last Modified: Tue, 01 Jul 2025 05:32:55 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd567b9748513d6b63ef8171d49c4a79eacd4da3746d8ef2c54060e165cc7480`  
		Last Modified: Tue, 01 Jul 2025 05:32:56 GMT  
		Size: 7.4 MB (7396227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21e60876b291985d5300fdfefe23016d85e5c8079b171e0a5ba04a5f434b6f7`  
		Last Modified: Tue, 01 Jul 2025 05:32:55 GMT  
		Size: 355.6 KB (355631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fbe52ee3623356d1ca5da444a3b3828a1eba1935602aecabf431b111c871bc`  
		Last Modified: Tue, 01 Jul 2025 05:32:55 GMT  
		Size: 76.3 KB (76313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076c16c9bf9ab9cd7554a7c638316128a1b7a4111c3b64cf92ce541596bf6d09`  
		Last Modified: Tue, 01 Jul 2025 05:32:55 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce1c620b837005ab7259ef43fac1435a47c9d6d1d6c88df96b61bdda21ea8e4`  
		Last Modified: Tue, 01 Jul 2025 05:33:15 GMT  
		Size: 101.8 MB (101797998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259fccf09046b7349d27cff59cec939bdb16f27ed4e2ec515ab9b12c17287e89`  
		Last Modified: Tue, 01 Jul 2025 05:32:55 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da974b84f7c7b36159ee03225e6ac8a002eaf95f2870fd1920139956c94ee6a`  
		Last Modified: Tue, 01 Jul 2025 05:32:56 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fb09fc14b8d03d8f6dd86565c54d412d45fce2c3d7578036f32e4ad55e7dfb`  
		Last Modified: Tue, 01 Jul 2025 05:32:56 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84756ec6179c3645b09f561aa70305b85412d9e158d0d08e9a6afe8cc647f576`  
		Last Modified: Tue, 01 Jul 2025 05:32:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:fb4d5a7a2d4b1bdf9a531ea16983eaf5950ad70e502fb102ec9390c733f440c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4166926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dba334bcd3dd1485ab1044da6e1967868a6e8a57f3eb1c07a726d03cea0bc2ee`

```dockerfile
```

-	Layers:
	-	`sha256:33fa93d481a94be3718287da6d86cb3be87b783860915c39355c523fa5b5fe38`  
		Last Modified: Tue, 01 Jul 2025 07:33:31 GMT  
		Size: 4.1 MB (4135145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41ae36a9f81ff5111c4db988dda3ff8e22a9bd6daf6a80703a34344b323544b3`  
		Last Modified: Tue, 01 Jul 2025 07:33:32 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:46474eb6bc641038d4556d527b8a3f6679856e10a7c97a71bec1dece081fb9e5
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
$ docker pull couchdb@sha256:ab1f747f0a24bb842442e8868938ba4036c6314c1d06d9adf1d26528119ef65c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156381636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b87f99fface8da68ab53d61a4cd841195621faafa5278eb08c1089c630a53e`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.0~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f77e651dc504aa144144706bce3af6f1882459bc41a109e3d69b0b6148070e3`  
		Last Modified: Tue, 01 Jul 2025 02:26:21 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f39da046be640b8c175172a536a24ab99edfc4a7ce2a035f675deb46ed04178`  
		Last Modified: Tue, 01 Jul 2025 02:26:22 GMT  
		Size: 7.9 MB (7880098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9461e93b2f846fb523ee7cb05a8d55a0eb7db765550e6f6769ace08d53e02f13`  
		Last Modified: Tue, 01 Jul 2025 02:26:28 GMT  
		Size: 77.3 MB (77319523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd7858aad009aff0578a5276f585237cf2dac140381e3b7cbf242e7fb38600d`  
		Last Modified: Tue, 01 Jul 2025 02:26:21 GMT  
		Size: 415.0 KB (415002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab69dffab1ca6f54f9de20c24880e51f6c8a7310cdb9210ae0b96ae78c1fbc1a`  
		Last Modified: Tue, 01 Jul 2025 02:26:21 GMT  
		Size: 99.3 KB (99342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15003ce6f991c0a48d366074ea39ee6af5da6a49e9745271879a5a73000e016`  
		Last Modified: Tue, 01 Jul 2025 02:26:21 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cf7f1297e1777935088974b048aa508b99924c321c5b95c8e65bc176fb8baa`  
		Last Modified: Tue, 01 Jul 2025 02:26:25 GMT  
		Size: 42.4 MB (42435648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c10db5dc067ecbd68b167b83808012942585d4038ba5f47e4957ae5f55dae1c`  
		Last Modified: Tue, 01 Jul 2025 02:26:21 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:451cd0ac40fced0df08bb2d19e91330773f6539524eb25d23d055156f3ff1eec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3680310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be72ad36932d58568a7f698148e529d37442bb86e0b1159b20c6b27193e9812`

```dockerfile
```

-	Layers:
	-	`sha256:8f01c7e99dc10b6ef0028737f6305049e8244fd870c3b23188101c88965309e4`  
		Last Modified: Tue, 01 Jul 2025 04:33:25 GMT  
		Size: 3.7 MB (3655746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd275016fb5b0143feea30922e7bdfddfee4e2be6b9c0e1e3cd8b0635786bc39`  
		Last Modified: Tue, 01 Jul 2025 04:33:26 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:db116fcf30dc07174fc38f70bf3a5ed76acb76b384b07e17609a7a0d4fc55f46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155201194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e47749be40012be2041a5e4a6413494c0488e94101277aa4b1c4f8401321362`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.0~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a693cf798537b8f1a0fdb8283841b92e518a7e3197417f3eed4dac1f9bae0758`  
		Last Modified: Tue, 01 Jul 2025 06:57:05 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d69f839f98418c99edccd088b9dc936ff6c5c6d5b86f5d30382d93c8839a13`  
		Last Modified: Tue, 01 Jul 2025 06:57:06 GMT  
		Size: 7.7 MB (7659267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893cbb9e4bbc0e3c46cbd7073378e2b9d3b7721ee9d2729ec716d1aac8f31cb4`  
		Last Modified: Tue, 01 Jul 2025 06:57:16 GMT  
		Size: 76.7 MB (76652832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e58f8e109d892b64448dc4c0cb910510c7058ba6af57573e92b30eb8bf4bba5`  
		Last Modified: Tue, 01 Jul 2025 06:57:05 GMT  
		Size: 371.8 KB (371802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6091d2f9f55226b99ddd02744efed6dd46834e1131c44504c94e93c9edabf2`  
		Last Modified: Tue, 01 Jul 2025 06:57:05 GMT  
		Size: 99.3 KB (99316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e024635eecf21ef2e7fc52aeba13bb7c50099099c5f787f2ef206a7bafddebaf`  
		Last Modified: Tue, 01 Jul 2025 06:57:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff2eb34a38bf8e6324b0b05a365aa266e2ce19a21192834a2d214405b5e6070`  
		Last Modified: Tue, 01 Jul 2025 06:57:12 GMT  
		Size: 42.3 MB (42338418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c2a290261296ae3b0ab6c38c3822b9cefff7157669181e9560346de7918dc3`  
		Last Modified: Tue, 01 Jul 2025 06:57:05 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:2cad67354524c81e1e6d392712f9bac8d070950ebeae5cfd2a484ce58d64fa68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3679168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85dd2ebc36f137ab0571fc6d33fa8de49e0795d02fd68f55233675757bc7fd7a`

```dockerfile
```

-	Layers:
	-	`sha256:7881b6766c55e9334fd6ca448ba3c6db249961c146494732c05e1117dfacf2e4`  
		Last Modified: Tue, 01 Jul 2025 07:33:36 GMT  
		Size: 3.7 MB (3654422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf649ca3e42aeb205c12902d05cfc9891032a7f6690241e8b327d5376c7705ff`  
		Last Modified: Tue, 01 Jul 2025 07:33:36 GMT  
		Size: 24.7 KB (24746 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:2e9d03343ad4bd4cc7bb44b910458c53408d1724d6449c081d98f6798b01f0e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (150005135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae7f63d7c73b16e52b8061076c6de3a1cdc31f37d33b0eeff77201ba2f14cad`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.0~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1cfd19a3932c2cefb87deb176dedfae9fc04b2c159d13af1e7639a7d297b0cd`  
		Last Modified: Tue, 01 Jul 2025 05:34:03 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba12806f817aa737143cd871d66cf31e264802e3fbdeb94528ae0fa19a20c0e9`  
		Last Modified: Tue, 01 Jul 2025 05:34:04 GMT  
		Size: 7.4 MB (7396271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4225734fe1d0f4799937a239f3a4d7327e995e5306e116644452a997890a0c`  
		Last Modified: Tue, 01 Jul 2025 05:34:07 GMT  
		Size: 73.1 MB (73079488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c27b651fab7650b0ed9ace9430ced920feef406ca24cbabea45762025fe0a84`  
		Last Modified: Tue, 01 Jul 2025 05:34:04 GMT  
		Size: 378.1 KB (378098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4ff360bc1afd86e2255f945cd5031ed759fecda6fbefa405a888015f571364`  
		Last Modified: Tue, 01 Jul 2025 05:34:03 GMT  
		Size: 99.4 KB (99447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c5086a911f2ad88703f95c02030c4e899521b38ac62e7b5360b015c1fbb6da`  
		Last Modified: Tue, 01 Jul 2025 05:34:03 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4701041b714fbef33c400888a08cebe1aaf3490d9ba9ff876fe569e66148c95`  
		Last Modified: Tue, 01 Jul 2025 05:34:07 GMT  
		Size: 42.2 MB (42162137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32968435ed0d8750d29229da48a7882876a71a95456168578e0abd55dc63fa26`  
		Last Modified: Tue, 01 Jul 2025 05:34:03 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:dc986a0227184267e2b1388c7df99f41bfc6d295ff97256c587a14068483bf26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3670839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:200ada59a746cc8d2c7815ed660ac6f65c3f8d740a50f662aa10fa9c8990a8e8`

```dockerfile
```

-	Layers:
	-	`sha256:d2a7aab3935eb1632112f673e48887ac872c8b7015dbdd26b706dbfb5da24953`  
		Last Modified: Tue, 01 Jul 2025 07:33:41 GMT  
		Size: 3.6 MB (3646275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3202daddc04f223f4ddef033ace3d2788fda2690cf9797dd6b0f7edeeb96e70`  
		Last Modified: Tue, 01 Jul 2025 07:33:42 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4`

```console
$ docker pull couchdb@sha256:791493a47b15464e0d572b603a5f378511edadf9e151b83b4b91a2e6dacd723d
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
$ docker pull couchdb@sha256:e90cb7013372f2a0a1d5dc454262845e62ace4a0e3f781bf0fcf3ebcf2405b74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139003829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6da55f828fe9c771d4b168da9a2c88859a2bc45fe0419a8f270a219cb6c0774`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbfc7240ae8bd25eaed5adec0ac49eb98c0ff78146dc243c1af5e9ba721aea0`  
		Last Modified: Tue, 01 Jul 2025 02:26:22 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d2d1593cd49d882f448908f3b4cccfe833dc9aa695f841f29f3d33532fe966`  
		Last Modified: Tue, 01 Jul 2025 02:26:23 GMT  
		Size: 7.9 MB (7880091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1698682ebb4652b7bf8b0204a9f60ce399b6393c06cae281bd0690da7e4b870c`  
		Last Modified: Tue, 01 Jul 2025 02:26:23 GMT  
		Size: 392.2 KB (392154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8fb2318f1bf988b75dcce19c80796003bb7f0e9ad87d630250d91321bcbd12`  
		Last Modified: Tue, 01 Jul 2025 02:26:23 GMT  
		Size: 76.3 KB (76294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a394e78b6943d39d8eb6d701c1d9e3fc9ff6776ab88c4469ab142cea84a3155`  
		Last Modified: Tue, 01 Jul 2025 02:26:23 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacb9d0afdc7637e9f9580aec73a78fa83fd9908f80d5a11d3cd0e81aa126323`  
		Last Modified: Tue, 01 Jul 2025 02:26:31 GMT  
		Size: 102.4 MB (102419713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f46989a96d771dd88b0af76c07c1aa6d12fd64934819919cc7cdd7dabae97b`  
		Last Modified: Tue, 01 Jul 2025 02:26:23 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a889abbdac2002c86610057c00cfcdad162822833eb0f575c46edc7a90f6cace`  
		Last Modified: Tue, 01 Jul 2025 02:26:23 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a26648a2a431522d3316cbe77ceebfaf941a4b272650b4db02a285ea757be2`  
		Last Modified: Tue, 01 Jul 2025 02:26:23 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2006614ddef25232c8f64522498336b810dfd2e17c5cf9afdecc7fe4809185ba`  
		Last Modified: Tue, 01 Jul 2025 02:26:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:6dbe8cf2cce545123d8c2bdb7b9392640bc55604238211665fc57f4bf6d3624c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4154272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd4ed6028947984ab010645bd9f69d5645f39289df8847cbc8bd67e61394ac6b`

```dockerfile
```

-	Layers:
	-	`sha256:f2cf3379acf68282e711eeea53d25a22b4074662eecfb495686b9cd7fdb72c00`  
		Last Modified: Tue, 01 Jul 2025 04:33:30 GMT  
		Size: 4.1 MB (4123082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fc84f95867c22212754d5529cfde91653618b35db29d5ae0564c831722e6807`  
		Last Modified: Tue, 01 Jul 2025 04:33:31 GMT  
		Size: 31.2 KB (31190 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:02aee182495702666c9494328844f605d6e29a351e95c98d5e76f43fd3facad4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.3 MB (138331168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:759f07612a24d567b16ed7d68204abf2a8a93eba0c2b85263d6d39fe62b59cf2`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057de2c1ce1dcd497a72f651e85c5c264a9cddcc9c4e3a9212efcd2ffde822f9`  
		Last Modified: Tue, 01 Jul 2025 06:55:58 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d789849c49c3d61dca13a6d384124e89af9aba2681d81849d2bfeada0c45e0`  
		Last Modified: Tue, 01 Jul 2025 06:55:59 GMT  
		Size: 7.7 MB (7659249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b17c162e267f76b3133ea3b14f100b475df8ea392a73b744e56298491d4a8b`  
		Last Modified: Tue, 01 Jul 2025 06:55:59 GMT  
		Size: 349.0 KB (348987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbfba2339642f8fdfdebf0bfe490c31c7d25f1558bf4e67bfdfd3b74d605b2d`  
		Last Modified: Tue, 01 Jul 2025 06:55:58 GMT  
		Size: 76.3 KB (76332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b250e07422379b841dfb652b751816d5c33fac6656d9c829cd1072d9b6285d5a`  
		Last Modified: Tue, 01 Jul 2025 06:57:50 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65abe9f2ac8b8e834b1c0e7e905a9948f43d45b9d3db4f91957a02388d19464e`  
		Last Modified: Tue, 01 Jul 2025 07:55:35 GMT  
		Size: 102.2 MB (102163498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc075ced62bfb75dcca2da6ecc8302684916994141395a2a26a0fe5e549571f6`  
		Last Modified: Tue, 01 Jul 2025 06:57:55 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff1ea884708a54eb54b3dd7f771b39216dfc0185bf9bb5c487a051e224ae8a1`  
		Last Modified: Tue, 01 Jul 2025 06:57:57 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f5ce9bc31ba58d97d41f029abac6b54caa73e066f21f1936319a8f4d06e30e`  
		Last Modified: Tue, 01 Jul 2025 06:57:58 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebce77b42b013b2a363da72921dfac7a17f025a9a0d80839e28ed5be5d5d422c`  
		Last Modified: Tue, 01 Jul 2025 06:57:57 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:d1e95b2e0ed8142a11bdf8194a4f38a9da0a94863f008398661d9405e11b1777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4154712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9bb5881f82d8257d27c7688a2cc7148d67ee5e6b5a873a8254d65a80c65f610`

```dockerfile
```

-	Layers:
	-	`sha256:752d90e1bb6a23ab2ac52a8039545f37fb6f6c25ac33b82bf69b413f8249b9fb`  
		Last Modified: Tue, 01 Jul 2025 07:33:45 GMT  
		Size: 4.1 MB (4123351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7f2d5a1d89dc28bcf11f7d9c036899913561c69080d7eb8d5c0858c89d6a7de`  
		Last Modified: Tue, 01 Jul 2025 07:33:46 GMT  
		Size: 31.4 KB (31361 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; s390x

```console
$ docker pull couchdb@sha256:5b51d24f9515363f0414248891f43dd3dafa9feeaa944900a3701c1dc3d87551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135777392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192b6f53d02ba9c8bd99d0fa1bfd73df2dfcdb0ef4b8045109028d0c36e97b15`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2126b1cb24a815801c16b429e02991eaeb9b8f45dc5690d80b3f27caaa0d598`  
		Last Modified: Tue, 01 Jul 2025 05:32:55 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd567b9748513d6b63ef8171d49c4a79eacd4da3746d8ef2c54060e165cc7480`  
		Last Modified: Tue, 01 Jul 2025 05:32:56 GMT  
		Size: 7.4 MB (7396227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21e60876b291985d5300fdfefe23016d85e5c8079b171e0a5ba04a5f434b6f7`  
		Last Modified: Tue, 01 Jul 2025 05:32:55 GMT  
		Size: 355.6 KB (355631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fbe52ee3623356d1ca5da444a3b3828a1eba1935602aecabf431b111c871bc`  
		Last Modified: Tue, 01 Jul 2025 05:32:55 GMT  
		Size: 76.3 KB (76313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84442adfb3fccd74c8d9a6dbfeac075831a82bcc81fbb343d2fdb2a6f2ddc522`  
		Last Modified: Tue, 01 Jul 2025 05:35:00 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49592611da8e30a9f0828f2846a5adf3abc594ba46363ca5cea066f2ee51bb9`  
		Last Modified: Tue, 01 Jul 2025 05:35:12 GMT  
		Size: 101.1 MB (101055975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a1b8583d2fac0622737476496f8bd8ef4f6cca7615adf726f8a694ae5d6aac`  
		Last Modified: Tue, 01 Jul 2025 05:35:01 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf271496377b29a716a92772e045770a3cd96a0ee4cb14d8bb0e85b66444172`  
		Last Modified: Tue, 01 Jul 2025 05:35:01 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3f250d7726ea434100851e974bd281395a6ccfda5560f78956e7a20639c989`  
		Last Modified: Tue, 01 Jul 2025 05:35:01 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f2b1d2c7fc3ec047026ff70f0c49401413d04c5c23c7a033bbc572acba8e10`  
		Last Modified: Tue, 01 Jul 2025 05:35:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:29513a8635fc2b97d342c1bf0539b28eeb93feffddf0a76f69ae34bec6b02671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4150469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4415e069633e081718394dc950d8e374d25d2035c494b0db3e4eb85225a35fc6`

```dockerfile
```

-	Layers:
	-	`sha256:2590470e0d87b11cd4d33f9774faa41be6a43ba4c229d061deb8203cc3b8c044`  
		Last Modified: Tue, 01 Jul 2025 07:33:50 GMT  
		Size: 4.1 MB (4119278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd63ef51fcf32fa04024833483e1f36259d88a8953f69ba728f6739756c69997`  
		Last Modified: Tue, 01 Jul 2025 07:33:50 GMT  
		Size: 31.2 KB (31191 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4-nouveau`

```console
$ docker pull couchdb@sha256:f7f657adea04937d1a36aa7c79de49f878a1f6135a19b191191470e917989d94
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
$ docker pull couchdb@sha256:7ed43570b35536e7f91953364affcd72b34377402550ade3640eeb73298955af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156381430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7a5d1a4046fcbfee5e18f0d006c33f31b2171fd74429d6e4c778e1bda6f0d3`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966256215e0e32982c6bdb166e6c0d555f08a1475640ed73f3bccc837bd2d5f2`  
		Last Modified: Tue, 01 Jul 2025 02:29:17 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b5d96376b64a9782611a87f4b707a87412140294cc61f12b1923ad8e56ccce`  
		Last Modified: Tue, 01 Jul 2025 04:33:51 GMT  
		Size: 7.9 MB (7880099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a204a8f49b5ef4c27a91cec9d6be9b2ea1642d1d9087ec9bda1cafdb6e6eba2`  
		Last Modified: Tue, 01 Jul 2025 04:33:54 GMT  
		Size: 77.3 MB (77319510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67ecaeeedc854493503fd1cc605b9a08930bf23db6b78b4abebc9f4e170f77a`  
		Last Modified: Tue, 01 Jul 2025 02:29:20 GMT  
		Size: 415.0 KB (414996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8579ed1ad624b166cc9710c4884006eb2a8ddf5c265565d8c803e366d1b4e492`  
		Last Modified: Tue, 01 Jul 2025 02:29:24 GMT  
		Size: 99.3 KB (99341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbcb5fa26591c9b46f92dadc0ec589b0fceeedd6e7e200e6039e680091073fc`  
		Last Modified: Tue, 01 Jul 2025 02:29:30 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769241397a7bba288659aad48de7e64c98c4256e9ca59a7ed933999bf791f316`  
		Last Modified: Tue, 01 Jul 2025 04:33:54 GMT  
		Size: 42.4 MB (42435462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c85cd0e2a01ca7180ae723a928251bc9fddba79ae69c1f703130c9c443e268`  
		Last Modified: Tue, 01 Jul 2025 02:29:35 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:8193a64e890ea6c303fb12728d70ed69f2eed19df9ab205e4451d834efad3d81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3679697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20b1876f86db081e930d8f234fbf88f7772dcaba4534cea387a8ec5d599e832d`

```dockerfile
```

-	Layers:
	-	`sha256:12924991a24111943d45b38336815371c56cd352c68d3cf05d2d03d8e1f4103c`  
		Last Modified: Tue, 01 Jul 2025 04:33:36 GMT  
		Size: 3.7 MB (3655440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:398c17c5878a1274a353e5ba14ca030d4bd1d7784685d2165c8115ed7e73141b`  
		Last Modified: Tue, 01 Jul 2025 04:33:36 GMT  
		Size: 24.3 KB (24257 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:8f2fdbc1d80877b5ad6685351cfbaa7b8f6699684ba10bad370cf6f2e88fbf31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155201131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05a5381f5e6a0417f281c0d5f4022c0bee04933cb241ce2a6f5f1de3bc4d390`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a693cf798537b8f1a0fdb8283841b92e518a7e3197417f3eed4dac1f9bae0758`  
		Last Modified: Tue, 01 Jul 2025 06:57:05 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d69f839f98418c99edccd088b9dc936ff6c5c6d5b86f5d30382d93c8839a13`  
		Last Modified: Tue, 01 Jul 2025 06:57:06 GMT  
		Size: 7.7 MB (7659267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893cbb9e4bbc0e3c46cbd7073378e2b9d3b7721ee9d2729ec716d1aac8f31cb4`  
		Last Modified: Tue, 01 Jul 2025 06:57:16 GMT  
		Size: 76.7 MB (76652832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e58f8e109d892b64448dc4c0cb910510c7058ba6af57573e92b30eb8bf4bba5`  
		Last Modified: Tue, 01 Jul 2025 06:57:05 GMT  
		Size: 371.8 KB (371802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6091d2f9f55226b99ddd02744efed6dd46834e1131c44504c94e93c9edabf2`  
		Last Modified: Tue, 01 Jul 2025 06:57:05 GMT  
		Size: 99.3 KB (99316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e024635eecf21ef2e7fc52aeba13bb7c50099099c5f787f2ef206a7bafddebaf`  
		Last Modified: Tue, 01 Jul 2025 06:57:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48fbd185289ac7c8358d7e2bed8aaed955c709ce9d987bc57056ff0ff375e80a`  
		Last Modified: Tue, 01 Jul 2025 06:59:03 GMT  
		Size: 42.3 MB (42338356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90af7c19e3a60f7af5621c7554c3945d2c05d7d100fc94faa2241bc0617863f6`  
		Last Modified: Tue, 01 Jul 2025 06:58:55 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:b7036d2db39f6e5d34f47782594b17eb69548e45e5ae0056e657c04b624cf30f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3678529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b7154cb981ed647d2a758d547eb61cb2ea112ed97e5683dbac3df57eed56096`

```dockerfile
```

-	Layers:
	-	`sha256:a06e03f93cb088abe347b53c29a93b3e4932a65bc0804c7f2ce1e78d58e2a1b3`  
		Last Modified: Tue, 01 Jul 2025 07:33:54 GMT  
		Size: 3.7 MB (3654104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae52776a14b6d6fee5eafa1a17d4eec080fc654a74f43b9cacfb382cddd5e6fa`  
		Last Modified: Tue, 01 Jul 2025 07:33:54 GMT  
		Size: 24.4 KB (24425 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:2d1e689142273880955878cf00d254457b870b64b15fc048581cb08a90ec3b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (150004673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b26f4ed94d27f4a34c25239475d4284a65885a652fda18381323fe4b11c618dc`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1cfd19a3932c2cefb87deb176dedfae9fc04b2c159d13af1e7639a7d297b0cd`  
		Last Modified: Tue, 01 Jul 2025 05:34:03 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba12806f817aa737143cd871d66cf31e264802e3fbdeb94528ae0fa19a20c0e9`  
		Last Modified: Tue, 01 Jul 2025 05:34:04 GMT  
		Size: 7.4 MB (7396271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4225734fe1d0f4799937a239f3a4d7327e995e5306e116644452a997890a0c`  
		Last Modified: Tue, 01 Jul 2025 05:34:07 GMT  
		Size: 73.1 MB (73079488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c27b651fab7650b0ed9ace9430ced920feef406ca24cbabea45762025fe0a84`  
		Last Modified: Tue, 01 Jul 2025 05:34:04 GMT  
		Size: 378.1 KB (378098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4ff360bc1afd86e2255f945cd5031ed759fecda6fbefa405a888015f571364`  
		Last Modified: Tue, 01 Jul 2025 05:34:03 GMT  
		Size: 99.4 KB (99447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c5086a911f2ad88703f95c02030c4e899521b38ac62e7b5360b015c1fbb6da`  
		Last Modified: Tue, 01 Jul 2025 05:34:03 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d9984ac2fca5fd474a7e7d4c6ec7d23cea3257ff8739518e18eb3f92b6b19a`  
		Last Modified: Tue, 01 Jul 2025 05:35:44 GMT  
		Size: 42.2 MB (42161676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bcd98faf8498e3a4dcdf1bc8c9dce0202498891509715bc939b42491f7d1ae`  
		Last Modified: Tue, 01 Jul 2025 05:35:41 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:259c4e53f6c7daf14fe0f58d22cfca5cf0686d2ea628e86cc2949be0e027578c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3670226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22544bcbdd2c144c3b6597d8ba5ce97b8503e5e6673993d9c3e9ea6d7b61b805`

```dockerfile
```

-	Layers:
	-	`sha256:beca12f02d52dc9f16325f3d24e5065ca1fed1c6bbc436360622379d99b6f80d`  
		Last Modified: Tue, 01 Jul 2025 07:33:59 GMT  
		Size: 3.6 MB (3645969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5e6e2bb3e3eacd29a89445fd1431cf1ca1c627427540b75ae7721141e09bdd7`  
		Last Modified: Tue, 01 Jul 2025 07:33:59 GMT  
		Size: 24.3 KB (24257 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3`

```console
$ docker pull couchdb@sha256:791493a47b15464e0d572b603a5f378511edadf9e151b83b4b91a2e6dacd723d
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
$ docker pull couchdb@sha256:e90cb7013372f2a0a1d5dc454262845e62ace4a0e3f781bf0fcf3ebcf2405b74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139003829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6da55f828fe9c771d4b168da9a2c88859a2bc45fe0419a8f270a219cb6c0774`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbfc7240ae8bd25eaed5adec0ac49eb98c0ff78146dc243c1af5e9ba721aea0`  
		Last Modified: Tue, 01 Jul 2025 02:26:22 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d2d1593cd49d882f448908f3b4cccfe833dc9aa695f841f29f3d33532fe966`  
		Last Modified: Tue, 01 Jul 2025 02:26:23 GMT  
		Size: 7.9 MB (7880091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1698682ebb4652b7bf8b0204a9f60ce399b6393c06cae281bd0690da7e4b870c`  
		Last Modified: Tue, 01 Jul 2025 02:26:23 GMT  
		Size: 392.2 KB (392154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8fb2318f1bf988b75dcce19c80796003bb7f0e9ad87d630250d91321bcbd12`  
		Last Modified: Tue, 01 Jul 2025 02:26:23 GMT  
		Size: 76.3 KB (76294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a394e78b6943d39d8eb6d701c1d9e3fc9ff6776ab88c4469ab142cea84a3155`  
		Last Modified: Tue, 01 Jul 2025 02:26:23 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacb9d0afdc7637e9f9580aec73a78fa83fd9908f80d5a11d3cd0e81aa126323`  
		Last Modified: Tue, 01 Jul 2025 02:26:31 GMT  
		Size: 102.4 MB (102419713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f46989a96d771dd88b0af76c07c1aa6d12fd64934819919cc7cdd7dabae97b`  
		Last Modified: Tue, 01 Jul 2025 02:26:23 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a889abbdac2002c86610057c00cfcdad162822833eb0f575c46edc7a90f6cace`  
		Last Modified: Tue, 01 Jul 2025 02:26:23 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a26648a2a431522d3316cbe77ceebfaf941a4b272650b4db02a285ea757be2`  
		Last Modified: Tue, 01 Jul 2025 02:26:23 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2006614ddef25232c8f64522498336b810dfd2e17c5cf9afdecc7fe4809185ba`  
		Last Modified: Tue, 01 Jul 2025 02:26:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:6dbe8cf2cce545123d8c2bdb7b9392640bc55604238211665fc57f4bf6d3624c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4154272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd4ed6028947984ab010645bd9f69d5645f39289df8847cbc8bd67e61394ac6b`

```dockerfile
```

-	Layers:
	-	`sha256:f2cf3379acf68282e711eeea53d25a22b4074662eecfb495686b9cd7fdb72c00`  
		Last Modified: Tue, 01 Jul 2025 04:33:30 GMT  
		Size: 4.1 MB (4123082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fc84f95867c22212754d5529cfde91653618b35db29d5ae0564c831722e6807`  
		Last Modified: Tue, 01 Jul 2025 04:33:31 GMT  
		Size: 31.2 KB (31190 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:02aee182495702666c9494328844f605d6e29a351e95c98d5e76f43fd3facad4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.3 MB (138331168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:759f07612a24d567b16ed7d68204abf2a8a93eba0c2b85263d6d39fe62b59cf2`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057de2c1ce1dcd497a72f651e85c5c264a9cddcc9c4e3a9212efcd2ffde822f9`  
		Last Modified: Tue, 01 Jul 2025 06:55:58 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d789849c49c3d61dca13a6d384124e89af9aba2681d81849d2bfeada0c45e0`  
		Last Modified: Tue, 01 Jul 2025 06:55:59 GMT  
		Size: 7.7 MB (7659249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b17c162e267f76b3133ea3b14f100b475df8ea392a73b744e56298491d4a8b`  
		Last Modified: Tue, 01 Jul 2025 06:55:59 GMT  
		Size: 349.0 KB (348987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbfba2339642f8fdfdebf0bfe490c31c7d25f1558bf4e67bfdfd3b74d605b2d`  
		Last Modified: Tue, 01 Jul 2025 06:55:58 GMT  
		Size: 76.3 KB (76332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b250e07422379b841dfb652b751816d5c33fac6656d9c829cd1072d9b6285d5a`  
		Last Modified: Tue, 01 Jul 2025 06:57:50 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65abe9f2ac8b8e834b1c0e7e905a9948f43d45b9d3db4f91957a02388d19464e`  
		Last Modified: Tue, 01 Jul 2025 07:55:35 GMT  
		Size: 102.2 MB (102163498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc075ced62bfb75dcca2da6ecc8302684916994141395a2a26a0fe5e549571f6`  
		Last Modified: Tue, 01 Jul 2025 06:57:55 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff1ea884708a54eb54b3dd7f771b39216dfc0185bf9bb5c487a051e224ae8a1`  
		Last Modified: Tue, 01 Jul 2025 06:57:57 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f5ce9bc31ba58d97d41f029abac6b54caa73e066f21f1936319a8f4d06e30e`  
		Last Modified: Tue, 01 Jul 2025 06:57:58 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebce77b42b013b2a363da72921dfac7a17f025a9a0d80839e28ed5be5d5d422c`  
		Last Modified: Tue, 01 Jul 2025 06:57:57 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:d1e95b2e0ed8142a11bdf8194a4f38a9da0a94863f008398661d9405e11b1777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4154712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9bb5881f82d8257d27c7688a2cc7148d67ee5e6b5a873a8254d65a80c65f610`

```dockerfile
```

-	Layers:
	-	`sha256:752d90e1bb6a23ab2ac52a8039545f37fb6f6c25ac33b82bf69b413f8249b9fb`  
		Last Modified: Tue, 01 Jul 2025 07:33:45 GMT  
		Size: 4.1 MB (4123351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7f2d5a1d89dc28bcf11f7d9c036899913561c69080d7eb8d5c0858c89d6a7de`  
		Last Modified: Tue, 01 Jul 2025 07:33:46 GMT  
		Size: 31.4 KB (31361 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3` - linux; s390x

```console
$ docker pull couchdb@sha256:5b51d24f9515363f0414248891f43dd3dafa9feeaa944900a3701c1dc3d87551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135777392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192b6f53d02ba9c8bd99d0fa1bfd73df2dfcdb0ef4b8045109028d0c36e97b15`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2126b1cb24a815801c16b429e02991eaeb9b8f45dc5690d80b3f27caaa0d598`  
		Last Modified: Tue, 01 Jul 2025 05:32:55 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd567b9748513d6b63ef8171d49c4a79eacd4da3746d8ef2c54060e165cc7480`  
		Last Modified: Tue, 01 Jul 2025 05:32:56 GMT  
		Size: 7.4 MB (7396227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21e60876b291985d5300fdfefe23016d85e5c8079b171e0a5ba04a5f434b6f7`  
		Last Modified: Tue, 01 Jul 2025 05:32:55 GMT  
		Size: 355.6 KB (355631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fbe52ee3623356d1ca5da444a3b3828a1eba1935602aecabf431b111c871bc`  
		Last Modified: Tue, 01 Jul 2025 05:32:55 GMT  
		Size: 76.3 KB (76313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84442adfb3fccd74c8d9a6dbfeac075831a82bcc81fbb343d2fdb2a6f2ddc522`  
		Last Modified: Tue, 01 Jul 2025 05:35:00 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49592611da8e30a9f0828f2846a5adf3abc594ba46363ca5cea066f2ee51bb9`  
		Last Modified: Tue, 01 Jul 2025 05:35:12 GMT  
		Size: 101.1 MB (101055975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a1b8583d2fac0622737476496f8bd8ef4f6cca7615adf726f8a694ae5d6aac`  
		Last Modified: Tue, 01 Jul 2025 05:35:01 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf271496377b29a716a92772e045770a3cd96a0ee4cb14d8bb0e85b66444172`  
		Last Modified: Tue, 01 Jul 2025 05:35:01 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3f250d7726ea434100851e974bd281395a6ccfda5560f78956e7a20639c989`  
		Last Modified: Tue, 01 Jul 2025 05:35:01 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f2b1d2c7fc3ec047026ff70f0c49401413d04c5c23c7a033bbc572acba8e10`  
		Last Modified: Tue, 01 Jul 2025 05:35:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:29513a8635fc2b97d342c1bf0539b28eeb93feffddf0a76f69ae34bec6b02671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4150469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4415e069633e081718394dc950d8e374d25d2035c494b0db3e4eb85225a35fc6`

```dockerfile
```

-	Layers:
	-	`sha256:2590470e0d87b11cd4d33f9774faa41be6a43ba4c229d061deb8203cc3b8c044`  
		Last Modified: Tue, 01 Jul 2025 07:33:50 GMT  
		Size: 4.1 MB (4119278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd63ef51fcf32fa04024833483e1f36259d88a8953f69ba728f6739756c69997`  
		Last Modified: Tue, 01 Jul 2025 07:33:50 GMT  
		Size: 31.2 KB (31191 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3-nouveau`

```console
$ docker pull couchdb@sha256:f7f657adea04937d1a36aa7c79de49f878a1f6135a19b191191470e917989d94
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
$ docker pull couchdb@sha256:7ed43570b35536e7f91953364affcd72b34377402550ade3640eeb73298955af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156381430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7a5d1a4046fcbfee5e18f0d006c33f31b2171fd74429d6e4c778e1bda6f0d3`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966256215e0e32982c6bdb166e6c0d555f08a1475640ed73f3bccc837bd2d5f2`  
		Last Modified: Tue, 01 Jul 2025 02:29:17 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b5d96376b64a9782611a87f4b707a87412140294cc61f12b1923ad8e56ccce`  
		Last Modified: Tue, 01 Jul 2025 04:33:51 GMT  
		Size: 7.9 MB (7880099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a204a8f49b5ef4c27a91cec9d6be9b2ea1642d1d9087ec9bda1cafdb6e6eba2`  
		Last Modified: Tue, 01 Jul 2025 04:33:54 GMT  
		Size: 77.3 MB (77319510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67ecaeeedc854493503fd1cc605b9a08930bf23db6b78b4abebc9f4e170f77a`  
		Last Modified: Tue, 01 Jul 2025 02:29:20 GMT  
		Size: 415.0 KB (414996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8579ed1ad624b166cc9710c4884006eb2a8ddf5c265565d8c803e366d1b4e492`  
		Last Modified: Tue, 01 Jul 2025 02:29:24 GMT  
		Size: 99.3 KB (99341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbcb5fa26591c9b46f92dadc0ec589b0fceeedd6e7e200e6039e680091073fc`  
		Last Modified: Tue, 01 Jul 2025 02:29:30 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769241397a7bba288659aad48de7e64c98c4256e9ca59a7ed933999bf791f316`  
		Last Modified: Tue, 01 Jul 2025 04:33:54 GMT  
		Size: 42.4 MB (42435462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c85cd0e2a01ca7180ae723a928251bc9fddba79ae69c1f703130c9c443e268`  
		Last Modified: Tue, 01 Jul 2025 02:29:35 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:8193a64e890ea6c303fb12728d70ed69f2eed19df9ab205e4451d834efad3d81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3679697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20b1876f86db081e930d8f234fbf88f7772dcaba4534cea387a8ec5d599e832d`

```dockerfile
```

-	Layers:
	-	`sha256:12924991a24111943d45b38336815371c56cd352c68d3cf05d2d03d8e1f4103c`  
		Last Modified: Tue, 01 Jul 2025 04:33:36 GMT  
		Size: 3.7 MB (3655440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:398c17c5878a1274a353e5ba14ca030d4bd1d7784685d2165c8115ed7e73141b`  
		Last Modified: Tue, 01 Jul 2025 04:33:36 GMT  
		Size: 24.3 KB (24257 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:8f2fdbc1d80877b5ad6685351cfbaa7b8f6699684ba10bad370cf6f2e88fbf31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155201131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05a5381f5e6a0417f281c0d5f4022c0bee04933cb241ce2a6f5f1de3bc4d390`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a693cf798537b8f1a0fdb8283841b92e518a7e3197417f3eed4dac1f9bae0758`  
		Last Modified: Tue, 01 Jul 2025 06:57:05 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d69f839f98418c99edccd088b9dc936ff6c5c6d5b86f5d30382d93c8839a13`  
		Last Modified: Tue, 01 Jul 2025 06:57:06 GMT  
		Size: 7.7 MB (7659267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893cbb9e4bbc0e3c46cbd7073378e2b9d3b7721ee9d2729ec716d1aac8f31cb4`  
		Last Modified: Tue, 01 Jul 2025 06:57:16 GMT  
		Size: 76.7 MB (76652832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e58f8e109d892b64448dc4c0cb910510c7058ba6af57573e92b30eb8bf4bba5`  
		Last Modified: Tue, 01 Jul 2025 06:57:05 GMT  
		Size: 371.8 KB (371802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6091d2f9f55226b99ddd02744efed6dd46834e1131c44504c94e93c9edabf2`  
		Last Modified: Tue, 01 Jul 2025 06:57:05 GMT  
		Size: 99.3 KB (99316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e024635eecf21ef2e7fc52aeba13bb7c50099099c5f787f2ef206a7bafddebaf`  
		Last Modified: Tue, 01 Jul 2025 06:57:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48fbd185289ac7c8358d7e2bed8aaed955c709ce9d987bc57056ff0ff375e80a`  
		Last Modified: Tue, 01 Jul 2025 06:59:03 GMT  
		Size: 42.3 MB (42338356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90af7c19e3a60f7af5621c7554c3945d2c05d7d100fc94faa2241bc0617863f6`  
		Last Modified: Tue, 01 Jul 2025 06:58:55 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:b7036d2db39f6e5d34f47782594b17eb69548e45e5ae0056e657c04b624cf30f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3678529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b7154cb981ed647d2a758d547eb61cb2ea112ed97e5683dbac3df57eed56096`

```dockerfile
```

-	Layers:
	-	`sha256:a06e03f93cb088abe347b53c29a93b3e4932a65bc0804c7f2ce1e78d58e2a1b3`  
		Last Modified: Tue, 01 Jul 2025 07:33:54 GMT  
		Size: 3.7 MB (3654104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae52776a14b6d6fee5eafa1a17d4eec080fc654a74f43b9cacfb382cddd5e6fa`  
		Last Modified: Tue, 01 Jul 2025 07:33:54 GMT  
		Size: 24.4 KB (24425 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:2d1e689142273880955878cf00d254457b870b64b15fc048581cb08a90ec3b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (150004673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b26f4ed94d27f4a34c25239475d4284a65885a652fda18381323fe4b11c618dc`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1cfd19a3932c2cefb87deb176dedfae9fc04b2c159d13af1e7639a7d297b0cd`  
		Last Modified: Tue, 01 Jul 2025 05:34:03 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba12806f817aa737143cd871d66cf31e264802e3fbdeb94528ae0fa19a20c0e9`  
		Last Modified: Tue, 01 Jul 2025 05:34:04 GMT  
		Size: 7.4 MB (7396271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4225734fe1d0f4799937a239f3a4d7327e995e5306e116644452a997890a0c`  
		Last Modified: Tue, 01 Jul 2025 05:34:07 GMT  
		Size: 73.1 MB (73079488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c27b651fab7650b0ed9ace9430ced920feef406ca24cbabea45762025fe0a84`  
		Last Modified: Tue, 01 Jul 2025 05:34:04 GMT  
		Size: 378.1 KB (378098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4ff360bc1afd86e2255f945cd5031ed759fecda6fbefa405a888015f571364`  
		Last Modified: Tue, 01 Jul 2025 05:34:03 GMT  
		Size: 99.4 KB (99447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c5086a911f2ad88703f95c02030c4e899521b38ac62e7b5360b015c1fbb6da`  
		Last Modified: Tue, 01 Jul 2025 05:34:03 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d9984ac2fca5fd474a7e7d4c6ec7d23cea3257ff8739518e18eb3f92b6b19a`  
		Last Modified: Tue, 01 Jul 2025 05:35:44 GMT  
		Size: 42.2 MB (42161676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bcd98faf8498e3a4dcdf1bc8c9dce0202498891509715bc939b42491f7d1ae`  
		Last Modified: Tue, 01 Jul 2025 05:35:41 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:259c4e53f6c7daf14fe0f58d22cfca5cf0686d2ea628e86cc2949be0e027578c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3670226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22544bcbdd2c144c3b6597d8ba5ce97b8503e5e6673993d9c3e9ea6d7b61b805`

```dockerfile
```

-	Layers:
	-	`sha256:beca12f02d52dc9f16325f3d24e5065ca1fed1c6bbc436360622379d99b6f80d`  
		Last Modified: Tue, 01 Jul 2025 07:33:59 GMT  
		Size: 3.6 MB (3645969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5e6e2bb3e3eacd29a89445fd1431cf1ca1c627427540b75ae7721141e09bdd7`  
		Last Modified: Tue, 01 Jul 2025 07:33:59 GMT  
		Size: 24.3 KB (24257 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5`

```console
$ docker pull couchdb@sha256:6c8a172f9aa64020d9a28c5bcbbdd3852b12125c5a2ab7345d7525abc8c7dfad
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
$ docker pull couchdb@sha256:559adbf2abdcf39ec99438c9ec22f9fd99128c80e6b8cc8dadb6d9375b046ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139826730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c85f9965112d24415932aa1fcfcde7badc9d2af1e311157270e41d4bd3bc88`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c3653e969dba91bf2d72c46e9130dec51413c23470ff9c7600b1b9a2a22c15`  
		Last Modified: Tue, 01 Jul 2025 02:26:21 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669656cd19f0d2cb942f87fdf029d76d45f8659f8de4fa6fc763498cdf182c43`  
		Last Modified: Tue, 01 Jul 2025 02:26:22 GMT  
		Size: 7.9 MB (7880077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073b8f1405c2e7f5538a819f3cb16871c9d23ca63bc1908604e0c1af55a6c5f0`  
		Last Modified: Tue, 01 Jul 2025 02:26:22 GMT  
		Size: 392.2 KB (392155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a088a900fab20f7d7abdac9ed1b6a2424012c6090811bc148da1f638df2aeff`  
		Last Modified: Tue, 01 Jul 2025 02:26:21 GMT  
		Size: 76.3 KB (76292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acb5c0c5c3da23be9cbf3c8f9e667dd82bc717526d3f3a8d898a66f1c1ae2f5`  
		Last Modified: Tue, 01 Jul 2025 02:26:21 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36349e7d193a6d840744dcbb64fa007f223dd6514434ae595a55d7061141f6f`  
		Last Modified: Tue, 01 Jul 2025 02:26:29 GMT  
		Size: 103.2 MB (103242642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c265eaefef330605b11794439399d081e9fc30f04386bf368f80a7d45db9fdd`  
		Last Modified: Tue, 01 Jul 2025 02:26:21 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5093f072c38d770ebd9bab0fe8fe8d88ab2fc2843666cb4f31610ccd0485f0`  
		Last Modified: Tue, 01 Jul 2025 02:26:21 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f71f0a586f2926bd9b4ffb04a1e2ae60b01a47bcafb0fb71a544a1fcd094d0`  
		Last Modified: Tue, 01 Jul 2025 02:26:22 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa3e8c78ebfbc39808737a5c8af960782293837715eaa8054b94523d9f6efa9`  
		Last Modified: Tue, 01 Jul 2025 02:26:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:db1bc8f53da793df6ec4ba90325f1fc6fa8c0096396ed58d2f359e87af02eaad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4170730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0035fc1e70dac383413afc75dc284be2f43b92e1097dbdaf992e45ad3a6d40`

```dockerfile
```

-	Layers:
	-	`sha256:b546dc6207c4fcb6f3ec3b18acf42bb82c203ab6118fd2d19002611cc3983aef`  
		Last Modified: Tue, 01 Jul 2025 04:33:20 GMT  
		Size: 4.1 MB (4138949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:604740e2a9a064960e852a52f212bce3bdfa1bb4f28a692115744e097dca49be`  
		Last Modified: Tue, 01 Jul 2025 04:33:20 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:b4afa7cd0272b0d4093f886b715f7df199ce2beda69aaf8736ba2730cc974d9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139071247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7521534de45ccf5227aba43a1b0681c1fcd41ff93302471185eee8cecd984bed`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057de2c1ce1dcd497a72f651e85c5c264a9cddcc9c4e3a9212efcd2ffde822f9`  
		Last Modified: Tue, 01 Jul 2025 06:55:58 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d789849c49c3d61dca13a6d384124e89af9aba2681d81849d2bfeada0c45e0`  
		Last Modified: Tue, 01 Jul 2025 06:55:59 GMT  
		Size: 7.7 MB (7659249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b17c162e267f76b3133ea3b14f100b475df8ea392a73b744e56298491d4a8b`  
		Last Modified: Tue, 01 Jul 2025 06:55:59 GMT  
		Size: 349.0 KB (348987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbfba2339642f8fdfdebf0bfe490c31c7d25f1558bf4e67bfdfd3b74d605b2d`  
		Last Modified: Tue, 01 Jul 2025 06:55:58 GMT  
		Size: 76.3 KB (76332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f096dbc2fc52e8e0ac8d6f43dcb6f377663760330864e2c53bf1453e5e81888`  
		Last Modified: Tue, 01 Jul 2025 06:55:58 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f193351f15f4f3106ca77ca9b3f09a278b33be341eaa6a75b187185d44c4e2`  
		Last Modified: Tue, 01 Jul 2025 06:56:04 GMT  
		Size: 102.9 MB (102903570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20cf586e8e201643afca22216e624b19e180bf42ff21599c6519ae146fb33993`  
		Last Modified: Tue, 01 Jul 2025 06:55:58 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221274c508510f838ecfef7e14486ae6aa5d8660bb39963e9c06c2c31940d3e5`  
		Last Modified: Tue, 01 Jul 2025 06:55:58 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09397da69982d94f542b2bf8fdde3b4860486ccdd47539cc9b9afc0b9bd1a3b5`  
		Last Modified: Tue, 01 Jul 2025 06:55:58 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ae5a71de8a50502b40c9ff6ccbdd6d0804cf5171bf03695ee630ac525cafed`  
		Last Modified: Tue, 01 Jul 2025 06:55:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:9a97e8b52454838dc7b70ff7a33b60b7947aea730389cbaba963a6765dd4e341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4171217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b276c1b3b9170df5e035c2a2c7f6de25afb8620bfb50bdf27a83ca54ea4eebc9`

```dockerfile
```

-	Layers:
	-	`sha256:bf1b2ccaa466fdfdd3b5019257f958be163d0aad3e5050c4ba7e765803b5a55e`  
		Last Modified: Tue, 01 Jul 2025 07:33:26 GMT  
		Size: 4.1 MB (4139242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c720b19990429e8a1f92a410aee8043df9db2dd289beafcb3c7b83c0966b824`  
		Last Modified: Tue, 01 Jul 2025 07:33:27 GMT  
		Size: 32.0 KB (31975 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5` - linux; s390x

```console
$ docker pull couchdb@sha256:ac73fdf4fd54cee56fc8b6a426f51fc1b8e22ec5e16bdbaefaa6ce2f3f0b2664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136519415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c56607e8d73bd9020c348266288695dd30b582708275bea02973a416de330b8`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2126b1cb24a815801c16b429e02991eaeb9b8f45dc5690d80b3f27caaa0d598`  
		Last Modified: Tue, 01 Jul 2025 05:32:55 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd567b9748513d6b63ef8171d49c4a79eacd4da3746d8ef2c54060e165cc7480`  
		Last Modified: Tue, 01 Jul 2025 05:32:56 GMT  
		Size: 7.4 MB (7396227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21e60876b291985d5300fdfefe23016d85e5c8079b171e0a5ba04a5f434b6f7`  
		Last Modified: Tue, 01 Jul 2025 05:32:55 GMT  
		Size: 355.6 KB (355631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fbe52ee3623356d1ca5da444a3b3828a1eba1935602aecabf431b111c871bc`  
		Last Modified: Tue, 01 Jul 2025 05:32:55 GMT  
		Size: 76.3 KB (76313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076c16c9bf9ab9cd7554a7c638316128a1b7a4111c3b64cf92ce541596bf6d09`  
		Last Modified: Tue, 01 Jul 2025 05:32:55 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce1c620b837005ab7259ef43fac1435a47c9d6d1d6c88df96b61bdda21ea8e4`  
		Last Modified: Tue, 01 Jul 2025 05:33:15 GMT  
		Size: 101.8 MB (101797998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259fccf09046b7349d27cff59cec939bdb16f27ed4e2ec515ab9b12c17287e89`  
		Last Modified: Tue, 01 Jul 2025 05:32:55 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da974b84f7c7b36159ee03225e6ac8a002eaf95f2870fd1920139956c94ee6a`  
		Last Modified: Tue, 01 Jul 2025 05:32:56 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fb09fc14b8d03d8f6dd86565c54d412d45fce2c3d7578036f32e4ad55e7dfb`  
		Last Modified: Tue, 01 Jul 2025 05:32:56 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84756ec6179c3645b09f561aa70305b85412d9e158d0d08e9a6afe8cc647f576`  
		Last Modified: Tue, 01 Jul 2025 05:32:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:fb4d5a7a2d4b1bdf9a531ea16983eaf5950ad70e502fb102ec9390c733f440c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4166926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dba334bcd3dd1485ab1044da6e1967868a6e8a57f3eb1c07a726d03cea0bc2ee`

```dockerfile
```

-	Layers:
	-	`sha256:33fa93d481a94be3718287da6d86cb3be87b783860915c39355c523fa5b5fe38`  
		Last Modified: Tue, 01 Jul 2025 07:33:31 GMT  
		Size: 4.1 MB (4135145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41ae36a9f81ff5111c4db988dda3ff8e22a9bd6daf6a80703a34344b323544b3`  
		Last Modified: Tue, 01 Jul 2025 07:33:32 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5-nouveau`

```console
$ docker pull couchdb@sha256:46474eb6bc641038d4556d527b8a3f6679856e10a7c97a71bec1dece081fb9e5
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
$ docker pull couchdb@sha256:ab1f747f0a24bb842442e8868938ba4036c6314c1d06d9adf1d26528119ef65c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156381636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b87f99fface8da68ab53d61a4cd841195621faafa5278eb08c1089c630a53e`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.0~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f77e651dc504aa144144706bce3af6f1882459bc41a109e3d69b0b6148070e3`  
		Last Modified: Tue, 01 Jul 2025 02:26:21 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f39da046be640b8c175172a536a24ab99edfc4a7ce2a035f675deb46ed04178`  
		Last Modified: Tue, 01 Jul 2025 02:26:22 GMT  
		Size: 7.9 MB (7880098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9461e93b2f846fb523ee7cb05a8d55a0eb7db765550e6f6769ace08d53e02f13`  
		Last Modified: Tue, 01 Jul 2025 02:26:28 GMT  
		Size: 77.3 MB (77319523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd7858aad009aff0578a5276f585237cf2dac140381e3b7cbf242e7fb38600d`  
		Last Modified: Tue, 01 Jul 2025 02:26:21 GMT  
		Size: 415.0 KB (415002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab69dffab1ca6f54f9de20c24880e51f6c8a7310cdb9210ae0b96ae78c1fbc1a`  
		Last Modified: Tue, 01 Jul 2025 02:26:21 GMT  
		Size: 99.3 KB (99342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15003ce6f991c0a48d366074ea39ee6af5da6a49e9745271879a5a73000e016`  
		Last Modified: Tue, 01 Jul 2025 02:26:21 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cf7f1297e1777935088974b048aa508b99924c321c5b95c8e65bc176fb8baa`  
		Last Modified: Tue, 01 Jul 2025 02:26:25 GMT  
		Size: 42.4 MB (42435648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c10db5dc067ecbd68b167b83808012942585d4038ba5f47e4957ae5f55dae1c`  
		Last Modified: Tue, 01 Jul 2025 02:26:21 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:451cd0ac40fced0df08bb2d19e91330773f6539524eb25d23d055156f3ff1eec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3680310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be72ad36932d58568a7f698148e529d37442bb86e0b1159b20c6b27193e9812`

```dockerfile
```

-	Layers:
	-	`sha256:8f01c7e99dc10b6ef0028737f6305049e8244fd870c3b23188101c88965309e4`  
		Last Modified: Tue, 01 Jul 2025 04:33:25 GMT  
		Size: 3.7 MB (3655746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd275016fb5b0143feea30922e7bdfddfee4e2be6b9c0e1e3cd8b0635786bc39`  
		Last Modified: Tue, 01 Jul 2025 04:33:26 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:db116fcf30dc07174fc38f70bf3a5ed76acb76b384b07e17609a7a0d4fc55f46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155201194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e47749be40012be2041a5e4a6413494c0488e94101277aa4b1c4f8401321362`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.0~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a693cf798537b8f1a0fdb8283841b92e518a7e3197417f3eed4dac1f9bae0758`  
		Last Modified: Tue, 01 Jul 2025 06:57:05 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d69f839f98418c99edccd088b9dc936ff6c5c6d5b86f5d30382d93c8839a13`  
		Last Modified: Tue, 01 Jul 2025 06:57:06 GMT  
		Size: 7.7 MB (7659267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893cbb9e4bbc0e3c46cbd7073378e2b9d3b7721ee9d2729ec716d1aac8f31cb4`  
		Last Modified: Tue, 01 Jul 2025 06:57:16 GMT  
		Size: 76.7 MB (76652832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e58f8e109d892b64448dc4c0cb910510c7058ba6af57573e92b30eb8bf4bba5`  
		Last Modified: Tue, 01 Jul 2025 06:57:05 GMT  
		Size: 371.8 KB (371802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6091d2f9f55226b99ddd02744efed6dd46834e1131c44504c94e93c9edabf2`  
		Last Modified: Tue, 01 Jul 2025 06:57:05 GMT  
		Size: 99.3 KB (99316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e024635eecf21ef2e7fc52aeba13bb7c50099099c5f787f2ef206a7bafddebaf`  
		Last Modified: Tue, 01 Jul 2025 06:57:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff2eb34a38bf8e6324b0b05a365aa266e2ce19a21192834a2d214405b5e6070`  
		Last Modified: Tue, 01 Jul 2025 06:57:12 GMT  
		Size: 42.3 MB (42338418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c2a290261296ae3b0ab6c38c3822b9cefff7157669181e9560346de7918dc3`  
		Last Modified: Tue, 01 Jul 2025 06:57:05 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:2cad67354524c81e1e6d392712f9bac8d070950ebeae5cfd2a484ce58d64fa68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3679168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85dd2ebc36f137ab0571fc6d33fa8de49e0795d02fd68f55233675757bc7fd7a`

```dockerfile
```

-	Layers:
	-	`sha256:7881b6766c55e9334fd6ca448ba3c6db249961c146494732c05e1117dfacf2e4`  
		Last Modified: Tue, 01 Jul 2025 07:33:36 GMT  
		Size: 3.7 MB (3654422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf649ca3e42aeb205c12902d05cfc9891032a7f6690241e8b327d5376c7705ff`  
		Last Modified: Tue, 01 Jul 2025 07:33:36 GMT  
		Size: 24.7 KB (24746 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:2e9d03343ad4bd4cc7bb44b910458c53408d1724d6449c081d98f6798b01f0e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (150005135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae7f63d7c73b16e52b8061076c6de3a1cdc31f37d33b0eeff77201ba2f14cad`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.0~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1cfd19a3932c2cefb87deb176dedfae9fc04b2c159d13af1e7639a7d297b0cd`  
		Last Modified: Tue, 01 Jul 2025 05:34:03 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba12806f817aa737143cd871d66cf31e264802e3fbdeb94528ae0fa19a20c0e9`  
		Last Modified: Tue, 01 Jul 2025 05:34:04 GMT  
		Size: 7.4 MB (7396271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4225734fe1d0f4799937a239f3a4d7327e995e5306e116644452a997890a0c`  
		Last Modified: Tue, 01 Jul 2025 05:34:07 GMT  
		Size: 73.1 MB (73079488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c27b651fab7650b0ed9ace9430ced920feef406ca24cbabea45762025fe0a84`  
		Last Modified: Tue, 01 Jul 2025 05:34:04 GMT  
		Size: 378.1 KB (378098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4ff360bc1afd86e2255f945cd5031ed759fecda6fbefa405a888015f571364`  
		Last Modified: Tue, 01 Jul 2025 05:34:03 GMT  
		Size: 99.4 KB (99447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c5086a911f2ad88703f95c02030c4e899521b38ac62e7b5360b015c1fbb6da`  
		Last Modified: Tue, 01 Jul 2025 05:34:03 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4701041b714fbef33c400888a08cebe1aaf3490d9ba9ff876fe569e66148c95`  
		Last Modified: Tue, 01 Jul 2025 05:34:07 GMT  
		Size: 42.2 MB (42162137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32968435ed0d8750d29229da48a7882876a71a95456168578e0abd55dc63fa26`  
		Last Modified: Tue, 01 Jul 2025 05:34:03 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:dc986a0227184267e2b1388c7df99f41bfc6d295ff97256c587a14068483bf26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3670839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:200ada59a746cc8d2c7815ed660ac6f65c3f8d740a50f662aa10fa9c8990a8e8`

```dockerfile
```

-	Layers:
	-	`sha256:d2a7aab3935eb1632112f673e48887ac872c8b7015dbdd26b706dbfb5da24953`  
		Last Modified: Tue, 01 Jul 2025 07:33:41 GMT  
		Size: 3.6 MB (3646275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3202daddc04f223f4ddef033ace3d2788fda2690cf9797dd6b0f7edeeb96e70`  
		Last Modified: Tue, 01 Jul 2025 07:33:42 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.0`

```console
$ docker pull couchdb@sha256:6c8a172f9aa64020d9a28c5bcbbdd3852b12125c5a2ab7345d7525abc8c7dfad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.5.0` - linux; amd64

```console
$ docker pull couchdb@sha256:559adbf2abdcf39ec99438c9ec22f9fd99128c80e6b8cc8dadb6d9375b046ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139826730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c85f9965112d24415932aa1fcfcde7badc9d2af1e311157270e41d4bd3bc88`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c3653e969dba91bf2d72c46e9130dec51413c23470ff9c7600b1b9a2a22c15`  
		Last Modified: Tue, 01 Jul 2025 02:26:21 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669656cd19f0d2cb942f87fdf029d76d45f8659f8de4fa6fc763498cdf182c43`  
		Last Modified: Tue, 01 Jul 2025 02:26:22 GMT  
		Size: 7.9 MB (7880077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073b8f1405c2e7f5538a819f3cb16871c9d23ca63bc1908604e0c1af55a6c5f0`  
		Last Modified: Tue, 01 Jul 2025 02:26:22 GMT  
		Size: 392.2 KB (392155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a088a900fab20f7d7abdac9ed1b6a2424012c6090811bc148da1f638df2aeff`  
		Last Modified: Tue, 01 Jul 2025 02:26:21 GMT  
		Size: 76.3 KB (76292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acb5c0c5c3da23be9cbf3c8f9e667dd82bc717526d3f3a8d898a66f1c1ae2f5`  
		Last Modified: Tue, 01 Jul 2025 02:26:21 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36349e7d193a6d840744dcbb64fa007f223dd6514434ae595a55d7061141f6f`  
		Last Modified: Tue, 01 Jul 2025 02:26:29 GMT  
		Size: 103.2 MB (103242642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c265eaefef330605b11794439399d081e9fc30f04386bf368f80a7d45db9fdd`  
		Last Modified: Tue, 01 Jul 2025 02:26:21 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5093f072c38d770ebd9bab0fe8fe8d88ab2fc2843666cb4f31610ccd0485f0`  
		Last Modified: Tue, 01 Jul 2025 02:26:21 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f71f0a586f2926bd9b4ffb04a1e2ae60b01a47bcafb0fb71a544a1fcd094d0`  
		Last Modified: Tue, 01 Jul 2025 02:26:22 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa3e8c78ebfbc39808737a5c8af960782293837715eaa8054b94523d9f6efa9`  
		Last Modified: Tue, 01 Jul 2025 02:26:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0` - unknown; unknown

```console
$ docker pull couchdb@sha256:db1bc8f53da793df6ec4ba90325f1fc6fa8c0096396ed58d2f359e87af02eaad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4170730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0035fc1e70dac383413afc75dc284be2f43b92e1097dbdaf992e45ad3a6d40`

```dockerfile
```

-	Layers:
	-	`sha256:b546dc6207c4fcb6f3ec3b18acf42bb82c203ab6118fd2d19002611cc3983aef`  
		Last Modified: Tue, 01 Jul 2025 04:33:20 GMT  
		Size: 4.1 MB (4138949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:604740e2a9a064960e852a52f212bce3bdfa1bb4f28a692115744e097dca49be`  
		Last Modified: Tue, 01 Jul 2025 04:33:20 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.0` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:b4afa7cd0272b0d4093f886b715f7df199ce2beda69aaf8736ba2730cc974d9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139071247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7521534de45ccf5227aba43a1b0681c1fcd41ff93302471185eee8cecd984bed`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057de2c1ce1dcd497a72f651e85c5c264a9cddcc9c4e3a9212efcd2ffde822f9`  
		Last Modified: Tue, 01 Jul 2025 06:55:58 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d789849c49c3d61dca13a6d384124e89af9aba2681d81849d2bfeada0c45e0`  
		Last Modified: Tue, 01 Jul 2025 06:55:59 GMT  
		Size: 7.7 MB (7659249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b17c162e267f76b3133ea3b14f100b475df8ea392a73b744e56298491d4a8b`  
		Last Modified: Tue, 01 Jul 2025 06:55:59 GMT  
		Size: 349.0 KB (348987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbfba2339642f8fdfdebf0bfe490c31c7d25f1558bf4e67bfdfd3b74d605b2d`  
		Last Modified: Tue, 01 Jul 2025 06:55:58 GMT  
		Size: 76.3 KB (76332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f096dbc2fc52e8e0ac8d6f43dcb6f377663760330864e2c53bf1453e5e81888`  
		Last Modified: Tue, 01 Jul 2025 06:55:58 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f193351f15f4f3106ca77ca9b3f09a278b33be341eaa6a75b187185d44c4e2`  
		Last Modified: Tue, 01 Jul 2025 06:56:04 GMT  
		Size: 102.9 MB (102903570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20cf586e8e201643afca22216e624b19e180bf42ff21599c6519ae146fb33993`  
		Last Modified: Tue, 01 Jul 2025 06:55:58 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221274c508510f838ecfef7e14486ae6aa5d8660bb39963e9c06c2c31940d3e5`  
		Last Modified: Tue, 01 Jul 2025 06:55:58 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09397da69982d94f542b2bf8fdde3b4860486ccdd47539cc9b9afc0b9bd1a3b5`  
		Last Modified: Tue, 01 Jul 2025 06:55:58 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ae5a71de8a50502b40c9ff6ccbdd6d0804cf5171bf03695ee630ac525cafed`  
		Last Modified: Tue, 01 Jul 2025 06:55:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0` - unknown; unknown

```console
$ docker pull couchdb@sha256:9a97e8b52454838dc7b70ff7a33b60b7947aea730389cbaba963a6765dd4e341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4171217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b276c1b3b9170df5e035c2a2c7f6de25afb8620bfb50bdf27a83ca54ea4eebc9`

```dockerfile
```

-	Layers:
	-	`sha256:bf1b2ccaa466fdfdd3b5019257f958be163d0aad3e5050c4ba7e765803b5a55e`  
		Last Modified: Tue, 01 Jul 2025 07:33:26 GMT  
		Size: 4.1 MB (4139242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c720b19990429e8a1f92a410aee8043df9db2dd289beafcb3c7b83c0966b824`  
		Last Modified: Tue, 01 Jul 2025 07:33:27 GMT  
		Size: 32.0 KB (31975 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.0` - linux; s390x

```console
$ docker pull couchdb@sha256:ac73fdf4fd54cee56fc8b6a426f51fc1b8e22ec5e16bdbaefaa6ce2f3f0b2664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136519415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c56607e8d73bd9020c348266288695dd30b582708275bea02973a416de330b8`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2126b1cb24a815801c16b429e02991eaeb9b8f45dc5690d80b3f27caaa0d598`  
		Last Modified: Tue, 01 Jul 2025 05:32:55 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd567b9748513d6b63ef8171d49c4a79eacd4da3746d8ef2c54060e165cc7480`  
		Last Modified: Tue, 01 Jul 2025 05:32:56 GMT  
		Size: 7.4 MB (7396227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21e60876b291985d5300fdfefe23016d85e5c8079b171e0a5ba04a5f434b6f7`  
		Last Modified: Tue, 01 Jul 2025 05:32:55 GMT  
		Size: 355.6 KB (355631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fbe52ee3623356d1ca5da444a3b3828a1eba1935602aecabf431b111c871bc`  
		Last Modified: Tue, 01 Jul 2025 05:32:55 GMT  
		Size: 76.3 KB (76313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076c16c9bf9ab9cd7554a7c638316128a1b7a4111c3b64cf92ce541596bf6d09`  
		Last Modified: Tue, 01 Jul 2025 05:32:55 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce1c620b837005ab7259ef43fac1435a47c9d6d1d6c88df96b61bdda21ea8e4`  
		Last Modified: Tue, 01 Jul 2025 05:33:15 GMT  
		Size: 101.8 MB (101797998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259fccf09046b7349d27cff59cec939bdb16f27ed4e2ec515ab9b12c17287e89`  
		Last Modified: Tue, 01 Jul 2025 05:32:55 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da974b84f7c7b36159ee03225e6ac8a002eaf95f2870fd1920139956c94ee6a`  
		Last Modified: Tue, 01 Jul 2025 05:32:56 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fb09fc14b8d03d8f6dd86565c54d412d45fce2c3d7578036f32e4ad55e7dfb`  
		Last Modified: Tue, 01 Jul 2025 05:32:56 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84756ec6179c3645b09f561aa70305b85412d9e158d0d08e9a6afe8cc647f576`  
		Last Modified: Tue, 01 Jul 2025 05:32:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0` - unknown; unknown

```console
$ docker pull couchdb@sha256:fb4d5a7a2d4b1bdf9a531ea16983eaf5950ad70e502fb102ec9390c733f440c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4166926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dba334bcd3dd1485ab1044da6e1967868a6e8a57f3eb1c07a726d03cea0bc2ee`

```dockerfile
```

-	Layers:
	-	`sha256:33fa93d481a94be3718287da6d86cb3be87b783860915c39355c523fa5b5fe38`  
		Last Modified: Tue, 01 Jul 2025 07:33:31 GMT  
		Size: 4.1 MB (4135145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41ae36a9f81ff5111c4db988dda3ff8e22a9bd6daf6a80703a34344b323544b3`  
		Last Modified: Tue, 01 Jul 2025 07:33:32 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.0-nouveau`

```console
$ docker pull couchdb@sha256:46474eb6bc641038d4556d527b8a3f6679856e10a7c97a71bec1dece081fb9e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.5.0-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:ab1f747f0a24bb842442e8868938ba4036c6314c1d06d9adf1d26528119ef65c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156381636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b87f99fface8da68ab53d61a4cd841195621faafa5278eb08c1089c630a53e`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.0~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f77e651dc504aa144144706bce3af6f1882459bc41a109e3d69b0b6148070e3`  
		Last Modified: Tue, 01 Jul 2025 02:26:21 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f39da046be640b8c175172a536a24ab99edfc4a7ce2a035f675deb46ed04178`  
		Last Modified: Tue, 01 Jul 2025 02:26:22 GMT  
		Size: 7.9 MB (7880098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9461e93b2f846fb523ee7cb05a8d55a0eb7db765550e6f6769ace08d53e02f13`  
		Last Modified: Tue, 01 Jul 2025 02:26:28 GMT  
		Size: 77.3 MB (77319523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd7858aad009aff0578a5276f585237cf2dac140381e3b7cbf242e7fb38600d`  
		Last Modified: Tue, 01 Jul 2025 02:26:21 GMT  
		Size: 415.0 KB (415002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab69dffab1ca6f54f9de20c24880e51f6c8a7310cdb9210ae0b96ae78c1fbc1a`  
		Last Modified: Tue, 01 Jul 2025 02:26:21 GMT  
		Size: 99.3 KB (99342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15003ce6f991c0a48d366074ea39ee6af5da6a49e9745271879a5a73000e016`  
		Last Modified: Tue, 01 Jul 2025 02:26:21 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cf7f1297e1777935088974b048aa508b99924c321c5b95c8e65bc176fb8baa`  
		Last Modified: Tue, 01 Jul 2025 02:26:25 GMT  
		Size: 42.4 MB (42435648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c10db5dc067ecbd68b167b83808012942585d4038ba5f47e4957ae5f55dae1c`  
		Last Modified: Tue, 01 Jul 2025 02:26:21 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:451cd0ac40fced0df08bb2d19e91330773f6539524eb25d23d055156f3ff1eec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3680310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be72ad36932d58568a7f698148e529d37442bb86e0b1159b20c6b27193e9812`

```dockerfile
```

-	Layers:
	-	`sha256:8f01c7e99dc10b6ef0028737f6305049e8244fd870c3b23188101c88965309e4`  
		Last Modified: Tue, 01 Jul 2025 04:33:25 GMT  
		Size: 3.7 MB (3655746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd275016fb5b0143feea30922e7bdfddfee4e2be6b9c0e1e3cd8b0635786bc39`  
		Last Modified: Tue, 01 Jul 2025 04:33:26 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.0-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:db116fcf30dc07174fc38f70bf3a5ed76acb76b384b07e17609a7a0d4fc55f46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155201194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e47749be40012be2041a5e4a6413494c0488e94101277aa4b1c4f8401321362`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.0~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a693cf798537b8f1a0fdb8283841b92e518a7e3197417f3eed4dac1f9bae0758`  
		Last Modified: Tue, 01 Jul 2025 06:57:05 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d69f839f98418c99edccd088b9dc936ff6c5c6d5b86f5d30382d93c8839a13`  
		Last Modified: Tue, 01 Jul 2025 06:57:06 GMT  
		Size: 7.7 MB (7659267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893cbb9e4bbc0e3c46cbd7073378e2b9d3b7721ee9d2729ec716d1aac8f31cb4`  
		Last Modified: Tue, 01 Jul 2025 06:57:16 GMT  
		Size: 76.7 MB (76652832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e58f8e109d892b64448dc4c0cb910510c7058ba6af57573e92b30eb8bf4bba5`  
		Last Modified: Tue, 01 Jul 2025 06:57:05 GMT  
		Size: 371.8 KB (371802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6091d2f9f55226b99ddd02744efed6dd46834e1131c44504c94e93c9edabf2`  
		Last Modified: Tue, 01 Jul 2025 06:57:05 GMT  
		Size: 99.3 KB (99316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e024635eecf21ef2e7fc52aeba13bb7c50099099c5f787f2ef206a7bafddebaf`  
		Last Modified: Tue, 01 Jul 2025 06:57:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff2eb34a38bf8e6324b0b05a365aa266e2ce19a21192834a2d214405b5e6070`  
		Last Modified: Tue, 01 Jul 2025 06:57:12 GMT  
		Size: 42.3 MB (42338418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c2a290261296ae3b0ab6c38c3822b9cefff7157669181e9560346de7918dc3`  
		Last Modified: Tue, 01 Jul 2025 06:57:05 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:2cad67354524c81e1e6d392712f9bac8d070950ebeae5cfd2a484ce58d64fa68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3679168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85dd2ebc36f137ab0571fc6d33fa8de49e0795d02fd68f55233675757bc7fd7a`

```dockerfile
```

-	Layers:
	-	`sha256:7881b6766c55e9334fd6ca448ba3c6db249961c146494732c05e1117dfacf2e4`  
		Last Modified: Tue, 01 Jul 2025 07:33:36 GMT  
		Size: 3.7 MB (3654422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf649ca3e42aeb205c12902d05cfc9891032a7f6690241e8b327d5376c7705ff`  
		Last Modified: Tue, 01 Jul 2025 07:33:36 GMT  
		Size: 24.7 KB (24746 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.0-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:2e9d03343ad4bd4cc7bb44b910458c53408d1724d6449c081d98f6798b01f0e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (150005135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae7f63d7c73b16e52b8061076c6de3a1cdc31f37d33b0eeff77201ba2f14cad`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.0~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1cfd19a3932c2cefb87deb176dedfae9fc04b2c159d13af1e7639a7d297b0cd`  
		Last Modified: Tue, 01 Jul 2025 05:34:03 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba12806f817aa737143cd871d66cf31e264802e3fbdeb94528ae0fa19a20c0e9`  
		Last Modified: Tue, 01 Jul 2025 05:34:04 GMT  
		Size: 7.4 MB (7396271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4225734fe1d0f4799937a239f3a4d7327e995e5306e116644452a997890a0c`  
		Last Modified: Tue, 01 Jul 2025 05:34:07 GMT  
		Size: 73.1 MB (73079488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c27b651fab7650b0ed9ace9430ced920feef406ca24cbabea45762025fe0a84`  
		Last Modified: Tue, 01 Jul 2025 05:34:04 GMT  
		Size: 378.1 KB (378098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4ff360bc1afd86e2255f945cd5031ed759fecda6fbefa405a888015f571364`  
		Last Modified: Tue, 01 Jul 2025 05:34:03 GMT  
		Size: 99.4 KB (99447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c5086a911f2ad88703f95c02030c4e899521b38ac62e7b5360b015c1fbb6da`  
		Last Modified: Tue, 01 Jul 2025 05:34:03 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4701041b714fbef33c400888a08cebe1aaf3490d9ba9ff876fe569e66148c95`  
		Last Modified: Tue, 01 Jul 2025 05:34:07 GMT  
		Size: 42.2 MB (42162137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32968435ed0d8750d29229da48a7882876a71a95456168578e0abd55dc63fa26`  
		Last Modified: Tue, 01 Jul 2025 05:34:03 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:dc986a0227184267e2b1388c7df99f41bfc6d295ff97256c587a14068483bf26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3670839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:200ada59a746cc8d2c7815ed660ac6f65c3f8d740a50f662aa10fa9c8990a8e8`

```dockerfile
```

-	Layers:
	-	`sha256:d2a7aab3935eb1632112f673e48887ac872c8b7015dbdd26b706dbfb5da24953`  
		Last Modified: Tue, 01 Jul 2025 07:33:41 GMT  
		Size: 3.6 MB (3646275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3202daddc04f223f4ddef033ace3d2788fda2690cf9797dd6b0f7edeeb96e70`  
		Last Modified: Tue, 01 Jul 2025 07:33:42 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:6c8a172f9aa64020d9a28c5bcbbdd3852b12125c5a2ab7345d7525abc8c7dfad
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
$ docker pull couchdb@sha256:559adbf2abdcf39ec99438c9ec22f9fd99128c80e6b8cc8dadb6d9375b046ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139826730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c85f9965112d24415932aa1fcfcde7badc9d2af1e311157270e41d4bd3bc88`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c3653e969dba91bf2d72c46e9130dec51413c23470ff9c7600b1b9a2a22c15`  
		Last Modified: Tue, 01 Jul 2025 02:26:21 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669656cd19f0d2cb942f87fdf029d76d45f8659f8de4fa6fc763498cdf182c43`  
		Last Modified: Tue, 01 Jul 2025 02:26:22 GMT  
		Size: 7.9 MB (7880077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073b8f1405c2e7f5538a819f3cb16871c9d23ca63bc1908604e0c1af55a6c5f0`  
		Last Modified: Tue, 01 Jul 2025 02:26:22 GMT  
		Size: 392.2 KB (392155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a088a900fab20f7d7abdac9ed1b6a2424012c6090811bc148da1f638df2aeff`  
		Last Modified: Tue, 01 Jul 2025 02:26:21 GMT  
		Size: 76.3 KB (76292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acb5c0c5c3da23be9cbf3c8f9e667dd82bc717526d3f3a8d898a66f1c1ae2f5`  
		Last Modified: Tue, 01 Jul 2025 02:26:21 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36349e7d193a6d840744dcbb64fa007f223dd6514434ae595a55d7061141f6f`  
		Last Modified: Tue, 01 Jul 2025 02:26:29 GMT  
		Size: 103.2 MB (103242642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c265eaefef330605b11794439399d081e9fc30f04386bf368f80a7d45db9fdd`  
		Last Modified: Tue, 01 Jul 2025 02:26:21 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5093f072c38d770ebd9bab0fe8fe8d88ab2fc2843666cb4f31610ccd0485f0`  
		Last Modified: Tue, 01 Jul 2025 02:26:21 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f71f0a586f2926bd9b4ffb04a1e2ae60b01a47bcafb0fb71a544a1fcd094d0`  
		Last Modified: Tue, 01 Jul 2025 02:26:22 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa3e8c78ebfbc39808737a5c8af960782293837715eaa8054b94523d9f6efa9`  
		Last Modified: Tue, 01 Jul 2025 02:26:22 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:db1bc8f53da793df6ec4ba90325f1fc6fa8c0096396ed58d2f359e87af02eaad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4170730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0035fc1e70dac383413afc75dc284be2f43b92e1097dbdaf992e45ad3a6d40`

```dockerfile
```

-	Layers:
	-	`sha256:b546dc6207c4fcb6f3ec3b18acf42bb82c203ab6118fd2d19002611cc3983aef`  
		Last Modified: Tue, 01 Jul 2025 04:33:20 GMT  
		Size: 4.1 MB (4138949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:604740e2a9a064960e852a52f212bce3bdfa1bb4f28a692115744e097dca49be`  
		Last Modified: Tue, 01 Jul 2025 04:33:20 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:b4afa7cd0272b0d4093f886b715f7df199ce2beda69aaf8736ba2730cc974d9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139071247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7521534de45ccf5227aba43a1b0681c1fcd41ff93302471185eee8cecd984bed`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057de2c1ce1dcd497a72f651e85c5c264a9cddcc9c4e3a9212efcd2ffde822f9`  
		Last Modified: Tue, 01 Jul 2025 06:55:58 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d789849c49c3d61dca13a6d384124e89af9aba2681d81849d2bfeada0c45e0`  
		Last Modified: Tue, 01 Jul 2025 06:55:59 GMT  
		Size: 7.7 MB (7659249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b17c162e267f76b3133ea3b14f100b475df8ea392a73b744e56298491d4a8b`  
		Last Modified: Tue, 01 Jul 2025 06:55:59 GMT  
		Size: 349.0 KB (348987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbfba2339642f8fdfdebf0bfe490c31c7d25f1558bf4e67bfdfd3b74d605b2d`  
		Last Modified: Tue, 01 Jul 2025 06:55:58 GMT  
		Size: 76.3 KB (76332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f096dbc2fc52e8e0ac8d6f43dcb6f377663760330864e2c53bf1453e5e81888`  
		Last Modified: Tue, 01 Jul 2025 06:55:58 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f193351f15f4f3106ca77ca9b3f09a278b33be341eaa6a75b187185d44c4e2`  
		Last Modified: Tue, 01 Jul 2025 06:56:04 GMT  
		Size: 102.9 MB (102903570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20cf586e8e201643afca22216e624b19e180bf42ff21599c6519ae146fb33993`  
		Last Modified: Tue, 01 Jul 2025 06:55:58 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221274c508510f838ecfef7e14486ae6aa5d8660bb39963e9c06c2c31940d3e5`  
		Last Modified: Tue, 01 Jul 2025 06:55:58 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09397da69982d94f542b2bf8fdde3b4860486ccdd47539cc9b9afc0b9bd1a3b5`  
		Last Modified: Tue, 01 Jul 2025 06:55:58 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ae5a71de8a50502b40c9ff6ccbdd6d0804cf5171bf03695ee630ac525cafed`  
		Last Modified: Tue, 01 Jul 2025 06:55:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:9a97e8b52454838dc7b70ff7a33b60b7947aea730389cbaba963a6765dd4e341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4171217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b276c1b3b9170df5e035c2a2c7f6de25afb8620bfb50bdf27a83ca54ea4eebc9`

```dockerfile
```

-	Layers:
	-	`sha256:bf1b2ccaa466fdfdd3b5019257f958be163d0aad3e5050c4ba7e765803b5a55e`  
		Last Modified: Tue, 01 Jul 2025 07:33:26 GMT  
		Size: 4.1 MB (4139242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c720b19990429e8a1f92a410aee8043df9db2dd289beafcb3c7b83c0966b824`  
		Last Modified: Tue, 01 Jul 2025 07:33:27 GMT  
		Size: 32.0 KB (31975 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:ac73fdf4fd54cee56fc8b6a426f51fc1b8e22ec5e16bdbaefaa6ce2f3f0b2664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136519415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c56607e8d73bd9020c348266288695dd30b582708275bea02973a416de330b8`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Tue, 06 May 2025 02:16:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 06 May 2025 02:16:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENV COUCHDB_VERSION=3.5.0
# Tue, 06 May 2025 02:16:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 06 May 2025 02:16:43 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 06 May 2025 02:16:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 06 May 2025 02:16:43 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 06 May 2025 02:16:43 GMT
VOLUME [/opt/couchdb/data]
# Tue, 06 May 2025 02:16:43 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 06 May 2025 02:16:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2126b1cb24a815801c16b429e02991eaeb9b8f45dc5690d80b3f27caaa0d598`  
		Last Modified: Tue, 01 Jul 2025 05:32:55 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd567b9748513d6b63ef8171d49c4a79eacd4da3746d8ef2c54060e165cc7480`  
		Last Modified: Tue, 01 Jul 2025 05:32:56 GMT  
		Size: 7.4 MB (7396227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21e60876b291985d5300fdfefe23016d85e5c8079b171e0a5ba04a5f434b6f7`  
		Last Modified: Tue, 01 Jul 2025 05:32:55 GMT  
		Size: 355.6 KB (355631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fbe52ee3623356d1ca5da444a3b3828a1eba1935602aecabf431b111c871bc`  
		Last Modified: Tue, 01 Jul 2025 05:32:55 GMT  
		Size: 76.3 KB (76313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076c16c9bf9ab9cd7554a7c638316128a1b7a4111c3b64cf92ce541596bf6d09`  
		Last Modified: Tue, 01 Jul 2025 05:32:55 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce1c620b837005ab7259ef43fac1435a47c9d6d1d6c88df96b61bdda21ea8e4`  
		Last Modified: Tue, 01 Jul 2025 05:33:15 GMT  
		Size: 101.8 MB (101797998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259fccf09046b7349d27cff59cec939bdb16f27ed4e2ec515ab9b12c17287e89`  
		Last Modified: Tue, 01 Jul 2025 05:32:55 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da974b84f7c7b36159ee03225e6ac8a002eaf95f2870fd1920139956c94ee6a`  
		Last Modified: Tue, 01 Jul 2025 05:32:56 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fb09fc14b8d03d8f6dd86565c54d412d45fce2c3d7578036f32e4ad55e7dfb`  
		Last Modified: Tue, 01 Jul 2025 05:32:56 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84756ec6179c3645b09f561aa70305b85412d9e158d0d08e9a6afe8cc647f576`  
		Last Modified: Tue, 01 Jul 2025 05:32:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:fb4d5a7a2d4b1bdf9a531ea16983eaf5950ad70e502fb102ec9390c733f440c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4166926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dba334bcd3dd1485ab1044da6e1967868a6e8a57f3eb1c07a726d03cea0bc2ee`

```dockerfile
```

-	Layers:
	-	`sha256:33fa93d481a94be3718287da6d86cb3be87b783860915c39355c523fa5b5fe38`  
		Last Modified: Tue, 01 Jul 2025 07:33:31 GMT  
		Size: 4.1 MB (4135145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41ae36a9f81ff5111c4db988dda3ff8e22a9bd6daf6a80703a34344b323544b3`  
		Last Modified: Tue, 01 Jul 2025 07:33:32 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json
