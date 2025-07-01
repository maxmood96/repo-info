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
$ docker pull couchdb@sha256:bfcf56d766f6e85aa3834197dee2849ed013907130fbe7b137269bc6dab84b29
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
$ docker pull couchdb@sha256:10159340a455126b0039a6c616258f61fb48990722b7f3d78e38efedf4f49dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139053286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efb0ac883c2114cb29fc3bb00964d3d6212c74a83f58fb0a49105f2c1300c3dd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699d385a56341dc4eca603cb63ab006476be4cb08a753f1a480b78c61886d5bd`  
		Last Modified: Wed, 11 Jun 2025 03:00:14 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39112042a5e68058792d92bcf41abba59268974d788b6d03ca6ae25b9eaae866`  
		Last Modified: Wed, 11 Jun 2025 03:00:16 GMT  
		Size: 7.7 MB (7655745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7ecf0714dbbded096bf25904f9f199b23c48ecd57eb8f188802cfdc07dfd50`  
		Last Modified: Wed, 11 Jun 2025 03:00:14 GMT  
		Size: 349.0 KB (348957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce88728e5f50fb5c57ce17692eb0a190d5220159249d0713e0b6c86807b7ba4`  
		Last Modified: Wed, 11 Jun 2025 03:00:14 GMT  
		Size: 76.3 KB (76295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b6ae98000b8ca8683d91c5052250a43963399ae199d45cdcf1f168eb63033c`  
		Last Modified: Wed, 11 Jun 2025 03:00:14 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0499fd43a835922cb9b40e1e5f35bc3dfd60938e9057a41c88fdc7eb107914de`  
		Last Modified: Wed, 11 Jun 2025 03:00:21 GMT  
		Size: 102.9 MB (102889172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf55c9860891b15c1049fc9627990536eda0ab9ba5604790714bd8173acf807`  
		Last Modified: Wed, 11 Jun 2025 03:00:14 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c298ad74cc2a3e12580740ef96b9b4c176d4001c79964f77fc4c77ba8400cf1f`  
		Last Modified: Wed, 11 Jun 2025 03:00:14 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f88b881ddf57c9aee182c813e18cf4a540c5084a04bd4084b825fb8357beda`  
		Last Modified: Wed, 11 Jun 2025 03:00:16 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767cdb597d3b7571d40221e4118697dc65eef4d9a0f5b161c6ec8b1bf5c39b71`  
		Last Modified: Wed, 11 Jun 2025 03:00:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:bb69d4d557e2b15cc52396a81a672cfbcf78540a39f35df9fa29133b2c30a6b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4169825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637953dc20bcf8062965e6626dd6f658761d49d2648cc1d23a0a70acdb363c14`

```dockerfile
```

-	Layers:
	-	`sha256:d51eeae0aaee7e2c7db21353b7cdc84592b41dca690513cb7fe9a495c42de539`  
		Last Modified: Wed, 11 Jun 2025 04:33:22 GMT  
		Size: 4.1 MB (4137850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bba0af450f31f51cea7b7faec600738dcd8e966e98b58d646d3b3adbc9b6aed`  
		Last Modified: Wed, 11 Jun 2025 04:33:23 GMT  
		Size: 32.0 KB (31975 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; s390x

```console
$ docker pull couchdb@sha256:70a40edbe2931e6c61ca9b87d702703e0e34cc81ef669b553645bd4a2f0810a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136514785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37111e3b2c0d7ce3fc7329887734346d84810a8a3a03f7c061cfa9822b0ed0ef`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7638cec2b1dd418d3648a58f2ff51f4e8c71d4a0e97a69f6b885c49b8abb52`  
		Last Modified: Wed, 11 Jun 2025 02:54:18 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6d3b6a7190c29cd3d87e0534ba65c82ca07adaf7c481f25a3ab2b8ec8dfacd`  
		Last Modified: Wed, 11 Jun 2025 02:54:20 GMT  
		Size: 7.4 MB (7391008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e13446e7ec304491354fbbde8273cbbff88817c38fee62076eabfbed576426`  
		Last Modified: Wed, 11 Jun 2025 02:54:19 GMT  
		Size: 355.6 KB (355626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b86396b56c86902e6883c0432db94761c7d4a10454af7b19d3beb817ab4064`  
		Last Modified: Wed, 11 Jun 2025 02:54:19 GMT  
		Size: 76.3 KB (76350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af21af686138b5422cc1b475a30fc9bcc248385f6792df2c32029293e0c00ef`  
		Last Modified: Wed, 11 Jun 2025 06:07:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ac84f9fe4e7e9dbc101fb7147afb2731f413cd2d26424bd8ef24fffd8499aa`  
		Last Modified: Wed, 11 Jun 2025 08:04:07 GMT  
		Size: 101.8 MB (101798517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073097c83b8062b974ad403672e4d054f9554b15f3bc5932428ab43311672a7f`  
		Last Modified: Wed, 11 Jun 2025 06:07:22 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9bc7737db2d11df145c6878bfbc548696b7a5e4a1700b644f1d6fee3967979a`  
		Last Modified: Wed, 11 Jun 2025 06:07:26 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73536106cb7ce4d875ef6b84693f465795d59646d8fc66d0c6a38aa500154eb1`  
		Last Modified: Wed, 11 Jun 2025 06:07:29 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7488eb0b92a2c7ff3502aa1d998b1efd701362b8399b8bd850d8701b3b4e3e59`  
		Last Modified: Wed, 11 Jun 2025 06:07:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:b796d6a9719c7f09f486358d454507e4b9e2dc2153249b862496eebc2a1867e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4165534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e2bb58e11b7e33906937c1b885fa8b5f509093685cc95c846f05c4fcfa523f`

```dockerfile
```

-	Layers:
	-	`sha256:7073765a63c504b9f6b446f6076e638256e453ec9c708ac1d161b97891ec87f2`  
		Last Modified: Wed, 11 Jun 2025 07:33:24 GMT  
		Size: 4.1 MB (4133753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ff3140839540892dee98635e327daa6ebcfcca43f01a39377bf85635e357921`  
		Last Modified: Wed, 11 Jun 2025 07:33:25 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:93c623b7f212a7a50bf0ac210f8cf65aa29b44e51d8be3e51e51b2e7a39195a5
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
$ docker pull couchdb@sha256:61be76d912255e93b30cf1945f014b4fdf76e855777c534beaa082474c92ea7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155198481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da0e1bcaaa8669646b95ada35469270b7e5acd29ffdea5c36aedda0a0132286`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f727c2cbc5714897417b3bf92251c1ca577c681e1cd4980da1e0a2b431cfb1`  
		Last Modified: Wed, 11 Jun 2025 03:01:03 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4fcda2a3359e316d27ca77539e490e9675e0c09813866f3057f68bfa46ba52`  
		Last Modified: Wed, 11 Jun 2025 03:01:04 GMT  
		Size: 7.7 MB (7655686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98e53920dc0c838f505bb8f5c58498d1729ede7142b247585fbb6f2eeb9e6f8`  
		Last Modified: Wed, 11 Jun 2025 03:01:09 GMT  
		Size: 76.7 MB (76653830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e57bacc8b343b9d3e9cfd79301d2848e9f456723c4ff035f5466a9af631a3e9`  
		Last Modified: Wed, 11 Jun 2025 03:01:03 GMT  
		Size: 371.8 KB (371775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14885eef1f40435843adc0a9862dcb7e864f00e793527847a43cb667f768318`  
		Last Modified: Wed, 11 Jun 2025 03:01:04 GMT  
		Size: 99.3 KB (99289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a5ab6732cf30b1956d2427f8bb4c0b235684efbba3eef54b998ed3e670b32a`  
		Last Modified: Wed, 11 Jun 2025 03:01:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf39d19cde025967aed40a9b4330c966ec21090d4ddbad6f805ec6361f9b4b25`  
		Last Modified: Wed, 11 Jun 2025 03:01:07 GMT  
		Size: 42.3 MB (42338343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608b4fdb60bc3e355862f2bc7e1cb9d10c1010116ac9b3ffb19574d033f3bdc0`  
		Last Modified: Wed, 11 Jun 2025 03:01:05 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:28b3f34e3cae365f40577b9d4cc00022c011cf439378a8f7f391049df355ba7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3677812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb60e8de67c02bbc6d9d397dfaa4b367c76d915a7b52700c4cb64dd1cd02060c`

```dockerfile
```

-	Layers:
	-	`sha256:50114b44d6ab1e22d0f8189abebe1eaf92f096aa041486cae8923f1191f5000a`  
		Last Modified: Wed, 11 Jun 2025 04:33:31 GMT  
		Size: 3.7 MB (3653066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1f7b285a519755f67215c2d46c1b594fd3c7cec213165681b8ecf947d092ebc`  
		Last Modified: Wed, 11 Jun 2025 04:33:32 GMT  
		Size: 24.7 KB (24746 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:9428288909b8b8780ff7256cfaa475dfa7cae9787a8c199fa25a5484feeb957c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (149996183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a7a848960ad42d247b6c8cff11f2fb2bb2db639481885f9fef05176da69d826`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27c5344ebf30f80f4535f49a310b31534afd0e30faa287c2f76794168336c12`  
		Last Modified: Wed, 11 Jun 2025 02:53:08 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7613b58989fe943ef5c79460458da358ff15e59da26c00710d2b35058e86fc`  
		Last Modified: Wed, 11 Jun 2025 02:53:09 GMT  
		Size: 7.4 MB (7391037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae980140a28827f67b7331e73db1665544940532e164e45c80b6c78379bc623`  
		Last Modified: Wed, 11 Jun 2025 02:53:13 GMT  
		Size: 73.1 MB (73075802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09451d171b5334d09ddef99e66f401719ea42fefd74cc946f70f4e144d2b9773`  
		Last Modified: Wed, 11 Jun 2025 02:53:09 GMT  
		Size: 378.1 KB (378095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebcb908b216a8512e6db9e0369099fabf5cc207e27ff06cb96a606556ebe5db`  
		Last Modified: Wed, 11 Jun 2025 02:53:09 GMT  
		Size: 99.4 KB (99419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae4c49bd5f4e303ad8871abcc0328792f4c36d63a3bac236266189eaa875aee`  
		Last Modified: Wed, 11 Jun 2025 02:53:09 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e22ced4f81a0aa6f3cec1052bab74c62d3fd61860da74efd2ea47f1dbcb5287`  
		Last Modified: Wed, 11 Jun 2025 02:53:12 GMT  
		Size: 42.2 MB (42162095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e6a140c73952436c63b826d49f3ca1dc4502867f54809f6ffa15309f5196cf`  
		Last Modified: Wed, 11 Jun 2025 02:53:10 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:d644aae5f48deb39ab35807efd7339906fe75ae9f71da8dc3dfb7a7ececc3927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3669483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c786bdcb66a2a06c4e498f97125c5286af66de6ece5d3728db0649369c2861`

```dockerfile
```

-	Layers:
	-	`sha256:e7bac52cfee4e7614f1df282f0e9225e48cc895ff50dcbf86b6267184d437230`  
		Last Modified: Wed, 11 Jun 2025 04:33:36 GMT  
		Size: 3.6 MB (3644919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c788e021d6e8698fd1889130f527f5fea495bae07c9640626152301c9bec455`  
		Last Modified: Wed, 11 Jun 2025 04:33:37 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4`

```console
$ docker pull couchdb@sha256:afb5e049d3ea4e2d25b1940ef31a979c21badc84e8c496fc1a8840befc9eb4c4
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
$ docker pull couchdb@sha256:1a43047353f128144897134cb71c61f20c502b7fd2a133280ed3f2d0fa273ab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.3 MB (138313610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64bdcc6fc57768aa8aef4972a25581b940037acbdf3589e67f50c7e504d61326`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699d385a56341dc4eca603cb63ab006476be4cb08a753f1a480b78c61886d5bd`  
		Last Modified: Wed, 11 Jun 2025 03:00:14 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39112042a5e68058792d92bcf41abba59268974d788b6d03ca6ae25b9eaae866`  
		Last Modified: Wed, 11 Jun 2025 03:00:16 GMT  
		Size: 7.7 MB (7655745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7ecf0714dbbded096bf25904f9f199b23c48ecd57eb8f188802cfdc07dfd50`  
		Last Modified: Wed, 11 Jun 2025 03:00:14 GMT  
		Size: 349.0 KB (348957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce88728e5f50fb5c57ce17692eb0a190d5220159249d0713e0b6c86807b7ba4`  
		Last Modified: Wed, 11 Jun 2025 03:00:14 GMT  
		Size: 76.3 KB (76295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71086ef3a328ee22fd9f6b5afd0dc578eef75738bae0979d7c211804c367273b`  
		Last Modified: Wed, 11 Jun 2025 03:01:44 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a23cfe052a89028f587864dd16ecb25da8a842d22a8d16105db83a7dff88523`  
		Last Modified: Wed, 11 Jun 2025 03:01:56 GMT  
		Size: 102.1 MB (102149499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37401a866d0c523f979599aad305dcc1b28f2d92604c464030ace3c1d1a5749b`  
		Last Modified: Wed, 11 Jun 2025 03:01:45 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9c92bb43c702359ec3c51865dafc17ab7f7642621cd02a25c190e3bdf3611b`  
		Last Modified: Wed, 11 Jun 2025 03:01:44 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b67dd2eb5bff47853414325953ed87d5a67eefb604e3b1bc813405f39c1f41b`  
		Last Modified: Wed, 11 Jun 2025 03:01:44 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc996756b1b2d8e077b5e086adc79f871dcbadca13bbe27688455ade339bd901`  
		Last Modified: Wed, 11 Jun 2025 03:01:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:9cbca4c5c5b2cb6a9023f65bb6c0908f3d9a07d261716bd1a8c62e39030e833e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4153320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1966bd306a3a908e3d76bb9181208e7eef069abf039c6fcbd47e2d0b303e2cab`

```dockerfile
```

-	Layers:
	-	`sha256:8a7f2f37c43f0189f42f8645a13a58390a59cd3ca054c874281f366ea9db4ec9`  
		Last Modified: Wed, 11 Jun 2025 04:33:39 GMT  
		Size: 4.1 MB (4121959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74c5b228f90d1c54a515756123083262d5e0ed447fb5aa78cc0c9398b866bb1f`  
		Last Modified: Wed, 11 Jun 2025 04:33:40 GMT  
		Size: 31.4 KB (31361 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; s390x

```console
$ docker pull couchdb@sha256:de2eb9f1f4fac8d86d4959ddeabce773df9d70bed6378c4b16da741d7c67d445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135772427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c3ec87793c79cc11c1d08f3141b9333c1d595e807f181581dbf470baaa7bea7`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7638cec2b1dd418d3648a58f2ff51f4e8c71d4a0e97a69f6b885c49b8abb52`  
		Last Modified: Wed, 11 Jun 2025 02:54:18 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6d3b6a7190c29cd3d87e0534ba65c82ca07adaf7c481f25a3ab2b8ec8dfacd`  
		Last Modified: Wed, 11 Jun 2025 02:54:20 GMT  
		Size: 7.4 MB (7391008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e13446e7ec304491354fbbde8273cbbff88817c38fee62076eabfbed576426`  
		Last Modified: Wed, 11 Jun 2025 02:54:19 GMT  
		Size: 355.6 KB (355626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b86396b56c86902e6883c0432db94761c7d4a10454af7b19d3beb817ab4064`  
		Last Modified: Wed, 11 Jun 2025 02:54:19 GMT  
		Size: 76.3 KB (76350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671f8e3c2d0412bc7e6b5d3e3d104ef21e81f9505061dca702f3acb22f819438`  
		Last Modified: Wed, 11 Jun 2025 02:54:19 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6932103c24c63846d536f898a100bcc12cd99e5e032cf146e09a602ff8cccd9c`  
		Last Modified: Wed, 11 Jun 2025 02:54:26 GMT  
		Size: 101.1 MB (101056161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f994523919ffdd34455c64e70e0a4cc2781b725eb741bb7c7f09aa32902346`  
		Last Modified: Wed, 11 Jun 2025 02:54:20 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b06699f67dca2cdca1d34d7eb82daaa3cfff979e2bfafdd916d2f0cde2cf55`  
		Last Modified: Wed, 11 Jun 2025 02:54:20 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62883712456a7baae762ae5713afaef3ba78931af390f207742967a30069bbe6`  
		Last Modified: Wed, 11 Jun 2025 02:54:20 GMT  
		Size: 2.2 KB (2223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e65fc67b6c9c5da5a6dd0a6e366b1c4e2dc0be902904da075c33291d6eee0f`  
		Last Modified: Wed, 11 Jun 2025 02:54:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:c1e48c4e6ba8dce29cf50910354a1e136893c8d5a75982c5e270e4495d988475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4149076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ffbb70c0049b1c544bf4bc1ec39830aaa137e10f5f90f6875dd817558f83fb2`

```dockerfile
```

-	Layers:
	-	`sha256:e755d8d7f9c61009d72c4795ca7918db818906171411a961778c08d55de7ad14`  
		Last Modified: Wed, 11 Jun 2025 04:33:44 GMT  
		Size: 4.1 MB (4117886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:722c60b8401d59cf84efe9f1839da9536282e5fef021d176d7e32819d2fe18e2`  
		Last Modified: Wed, 11 Jun 2025 04:33:45 GMT  
		Size: 31.2 KB (31190 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4-nouveau`

```console
$ docker pull couchdb@sha256:8b574553c6c5222bd724b9bf4b50e4b9085952b6c02d2d8830b2efdbacd8aefe
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
$ docker pull couchdb@sha256:410e6caeab2c1c636d0cff23197485ab37eb7367f307c0c8dc0db540671d2a5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155198594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b86a8079cfde2618ee8f206a7f598ee11209c68951446ab3d24386c46c6f9d86`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f727c2cbc5714897417b3bf92251c1ca577c681e1cd4980da1e0a2b431cfb1`  
		Last Modified: Wed, 11 Jun 2025 03:01:03 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4fcda2a3359e316d27ca77539e490e9675e0c09813866f3057f68bfa46ba52`  
		Last Modified: Wed, 11 Jun 2025 03:01:04 GMT  
		Size: 7.7 MB (7655686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98e53920dc0c838f505bb8f5c58498d1729ede7142b247585fbb6f2eeb9e6f8`  
		Last Modified: Wed, 11 Jun 2025 03:01:09 GMT  
		Size: 76.7 MB (76653830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e57bacc8b343b9d3e9cfd79301d2848e9f456723c4ff035f5466a9af631a3e9`  
		Last Modified: Wed, 11 Jun 2025 03:01:03 GMT  
		Size: 371.8 KB (371775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14885eef1f40435843adc0a9862dcb7e864f00e793527847a43cb667f768318`  
		Last Modified: Wed, 11 Jun 2025 03:01:04 GMT  
		Size: 99.3 KB (99289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a5ab6732cf30b1956d2427f8bb4c0b235684efbba3eef54b998ed3e670b32a`  
		Last Modified: Wed, 11 Jun 2025 03:01:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6f256aa85ccccc0d3bbef9e209f59aa1579d55174d99eaac3a4b42777789bd`  
		Last Modified: Wed, 11 Jun 2025 03:02:05 GMT  
		Size: 42.3 MB (42338456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89c22bda585ef4b61e91411069feb04fbc1c4d093f833af6c20dd90e76e087e`  
		Last Modified: Wed, 11 Jun 2025 03:02:03 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:ac124ea33cafe773806cda7614f047bb4466439041bdf0e4cf91a7e942959080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3677176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ec303e0389c480782839bd95a10adecc7d574ec4f0c4e864d4cee2ae4f07b0`

```dockerfile
```

-	Layers:
	-	`sha256:a8886c6ea8456ab8b6a4f204a105b8318814d8ea1272f6d452e49808bfae9afe`  
		Last Modified: Wed, 11 Jun 2025 04:33:48 GMT  
		Size: 3.7 MB (3652748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8873cb330c58c7ee369d7e9d4f6268ff8bb2fc5dfcbceaf10151cea4a7d62bf5`  
		Last Modified: Wed, 11 Jun 2025 04:33:49 GMT  
		Size: 24.4 KB (24428 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:f9ee41f46eaa17e55edff1472c24d22cda47250e8b2e197bc75f9db4c672ccdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (149995746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d608cde8564f16961bc9b39844f93e6a019f503e28be9a2c31adb9c7623c44ce`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27c5344ebf30f80f4535f49a310b31534afd0e30faa287c2f76794168336c12`  
		Last Modified: Wed, 11 Jun 2025 02:53:08 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7613b58989fe943ef5c79460458da358ff15e59da26c00710d2b35058e86fc`  
		Last Modified: Wed, 11 Jun 2025 02:53:09 GMT  
		Size: 7.4 MB (7391037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae980140a28827f67b7331e73db1665544940532e164e45c80b6c78379bc623`  
		Last Modified: Wed, 11 Jun 2025 02:53:13 GMT  
		Size: 73.1 MB (73075802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09451d171b5334d09ddef99e66f401719ea42fefd74cc946f70f4e144d2b9773`  
		Last Modified: Wed, 11 Jun 2025 02:53:09 GMT  
		Size: 378.1 KB (378095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebcb908b216a8512e6db9e0369099fabf5cc207e27ff06cb96a606556ebe5db`  
		Last Modified: Wed, 11 Jun 2025 02:53:09 GMT  
		Size: 99.4 KB (99419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae4c49bd5f4e303ad8871abcc0328792f4c36d63a3bac236266189eaa875aee`  
		Last Modified: Wed, 11 Jun 2025 02:53:09 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e150935a477bd994159253027a6747e5e05949816b4c22a858c59eb09cfa9e1`  
		Last Modified: Wed, 11 Jun 2025 02:55:04 GMT  
		Size: 42.2 MB (42161659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dfdacdc57d0aaeb4f7cedef81d33381076a2aeebd232a7eb230ff0be723abe`  
		Last Modified: Wed, 11 Jun 2025 02:55:01 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:99230260be226e4c58682fdc453fc795b36d10ecbbf5afbc552f42c12ebb2946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3668870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2864cbe1d945201bb9052920374894a27ec78898751cf69133fa67834a288b3b`

```dockerfile
```

-	Layers:
	-	`sha256:56cdfa85b233a1d60442e2c24bb701c10d8c51bb576bff920b4a3ebe1993be09`  
		Last Modified: Wed, 11 Jun 2025 04:33:53 GMT  
		Size: 3.6 MB (3644613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f596efe772c5e037f017516612d75b8f88f8eb7b8674748577be4e8271bd8e04`  
		Last Modified: Wed, 11 Jun 2025 04:33:54 GMT  
		Size: 24.3 KB (24257 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3`

```console
$ docker pull couchdb@sha256:afb5e049d3ea4e2d25b1940ef31a979c21badc84e8c496fc1a8840befc9eb4c4
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
$ docker pull couchdb@sha256:1a43047353f128144897134cb71c61f20c502b7fd2a133280ed3f2d0fa273ab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.3 MB (138313610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64bdcc6fc57768aa8aef4972a25581b940037acbdf3589e67f50c7e504d61326`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699d385a56341dc4eca603cb63ab006476be4cb08a753f1a480b78c61886d5bd`  
		Last Modified: Wed, 11 Jun 2025 03:00:14 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39112042a5e68058792d92bcf41abba59268974d788b6d03ca6ae25b9eaae866`  
		Last Modified: Wed, 11 Jun 2025 03:00:16 GMT  
		Size: 7.7 MB (7655745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7ecf0714dbbded096bf25904f9f199b23c48ecd57eb8f188802cfdc07dfd50`  
		Last Modified: Wed, 11 Jun 2025 03:00:14 GMT  
		Size: 349.0 KB (348957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce88728e5f50fb5c57ce17692eb0a190d5220159249d0713e0b6c86807b7ba4`  
		Last Modified: Wed, 11 Jun 2025 03:00:14 GMT  
		Size: 76.3 KB (76295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71086ef3a328ee22fd9f6b5afd0dc578eef75738bae0979d7c211804c367273b`  
		Last Modified: Wed, 11 Jun 2025 03:01:44 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a23cfe052a89028f587864dd16ecb25da8a842d22a8d16105db83a7dff88523`  
		Last Modified: Wed, 11 Jun 2025 03:01:56 GMT  
		Size: 102.1 MB (102149499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37401a866d0c523f979599aad305dcc1b28f2d92604c464030ace3c1d1a5749b`  
		Last Modified: Wed, 11 Jun 2025 03:01:45 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9c92bb43c702359ec3c51865dafc17ab7f7642621cd02a25c190e3bdf3611b`  
		Last Modified: Wed, 11 Jun 2025 03:01:44 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b67dd2eb5bff47853414325953ed87d5a67eefb604e3b1bc813405f39c1f41b`  
		Last Modified: Wed, 11 Jun 2025 03:01:44 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc996756b1b2d8e077b5e086adc79f871dcbadca13bbe27688455ade339bd901`  
		Last Modified: Wed, 11 Jun 2025 03:01:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:9cbca4c5c5b2cb6a9023f65bb6c0908f3d9a07d261716bd1a8c62e39030e833e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4153320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1966bd306a3a908e3d76bb9181208e7eef069abf039c6fcbd47e2d0b303e2cab`

```dockerfile
```

-	Layers:
	-	`sha256:8a7f2f37c43f0189f42f8645a13a58390a59cd3ca054c874281f366ea9db4ec9`  
		Last Modified: Wed, 11 Jun 2025 04:33:39 GMT  
		Size: 4.1 MB (4121959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74c5b228f90d1c54a515756123083262d5e0ed447fb5aa78cc0c9398b866bb1f`  
		Last Modified: Wed, 11 Jun 2025 04:33:40 GMT  
		Size: 31.4 KB (31361 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3` - linux; s390x

```console
$ docker pull couchdb@sha256:de2eb9f1f4fac8d86d4959ddeabce773df9d70bed6378c4b16da741d7c67d445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135772427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c3ec87793c79cc11c1d08f3141b9333c1d595e807f181581dbf470baaa7bea7`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7638cec2b1dd418d3648a58f2ff51f4e8c71d4a0e97a69f6b885c49b8abb52`  
		Last Modified: Wed, 11 Jun 2025 02:54:18 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6d3b6a7190c29cd3d87e0534ba65c82ca07adaf7c481f25a3ab2b8ec8dfacd`  
		Last Modified: Wed, 11 Jun 2025 02:54:20 GMT  
		Size: 7.4 MB (7391008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e13446e7ec304491354fbbde8273cbbff88817c38fee62076eabfbed576426`  
		Last Modified: Wed, 11 Jun 2025 02:54:19 GMT  
		Size: 355.6 KB (355626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b86396b56c86902e6883c0432db94761c7d4a10454af7b19d3beb817ab4064`  
		Last Modified: Wed, 11 Jun 2025 02:54:19 GMT  
		Size: 76.3 KB (76350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671f8e3c2d0412bc7e6b5d3e3d104ef21e81f9505061dca702f3acb22f819438`  
		Last Modified: Wed, 11 Jun 2025 02:54:19 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6932103c24c63846d536f898a100bcc12cd99e5e032cf146e09a602ff8cccd9c`  
		Last Modified: Wed, 11 Jun 2025 02:54:26 GMT  
		Size: 101.1 MB (101056161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f994523919ffdd34455c64e70e0a4cc2781b725eb741bb7c7f09aa32902346`  
		Last Modified: Wed, 11 Jun 2025 02:54:20 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b06699f67dca2cdca1d34d7eb82daaa3cfff979e2bfafdd916d2f0cde2cf55`  
		Last Modified: Wed, 11 Jun 2025 02:54:20 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62883712456a7baae762ae5713afaef3ba78931af390f207742967a30069bbe6`  
		Last Modified: Wed, 11 Jun 2025 02:54:20 GMT  
		Size: 2.2 KB (2223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e65fc67b6c9c5da5a6dd0a6e366b1c4e2dc0be902904da075c33291d6eee0f`  
		Last Modified: Wed, 11 Jun 2025 02:54:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:c1e48c4e6ba8dce29cf50910354a1e136893c8d5a75982c5e270e4495d988475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4149076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ffbb70c0049b1c544bf4bc1ec39830aaa137e10f5f90f6875dd817558f83fb2`

```dockerfile
```

-	Layers:
	-	`sha256:e755d8d7f9c61009d72c4795ca7918db818906171411a961778c08d55de7ad14`  
		Last Modified: Wed, 11 Jun 2025 04:33:44 GMT  
		Size: 4.1 MB (4117886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:722c60b8401d59cf84efe9f1839da9536282e5fef021d176d7e32819d2fe18e2`  
		Last Modified: Wed, 11 Jun 2025 04:33:45 GMT  
		Size: 31.2 KB (31190 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3-nouveau`

```console
$ docker pull couchdb@sha256:8b574553c6c5222bd724b9bf4b50e4b9085952b6c02d2d8830b2efdbacd8aefe
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
$ docker pull couchdb@sha256:410e6caeab2c1c636d0cff23197485ab37eb7367f307c0c8dc0db540671d2a5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155198594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b86a8079cfde2618ee8f206a7f598ee11209c68951446ab3d24386c46c6f9d86`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f727c2cbc5714897417b3bf92251c1ca577c681e1cd4980da1e0a2b431cfb1`  
		Last Modified: Wed, 11 Jun 2025 03:01:03 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4fcda2a3359e316d27ca77539e490e9675e0c09813866f3057f68bfa46ba52`  
		Last Modified: Wed, 11 Jun 2025 03:01:04 GMT  
		Size: 7.7 MB (7655686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98e53920dc0c838f505bb8f5c58498d1729ede7142b247585fbb6f2eeb9e6f8`  
		Last Modified: Wed, 11 Jun 2025 03:01:09 GMT  
		Size: 76.7 MB (76653830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e57bacc8b343b9d3e9cfd79301d2848e9f456723c4ff035f5466a9af631a3e9`  
		Last Modified: Wed, 11 Jun 2025 03:01:03 GMT  
		Size: 371.8 KB (371775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14885eef1f40435843adc0a9862dcb7e864f00e793527847a43cb667f768318`  
		Last Modified: Wed, 11 Jun 2025 03:01:04 GMT  
		Size: 99.3 KB (99289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a5ab6732cf30b1956d2427f8bb4c0b235684efbba3eef54b998ed3e670b32a`  
		Last Modified: Wed, 11 Jun 2025 03:01:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6f256aa85ccccc0d3bbef9e209f59aa1579d55174d99eaac3a4b42777789bd`  
		Last Modified: Wed, 11 Jun 2025 03:02:05 GMT  
		Size: 42.3 MB (42338456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89c22bda585ef4b61e91411069feb04fbc1c4d093f833af6c20dd90e76e087e`  
		Last Modified: Wed, 11 Jun 2025 03:02:03 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:ac124ea33cafe773806cda7614f047bb4466439041bdf0e4cf91a7e942959080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3677176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ec303e0389c480782839bd95a10adecc7d574ec4f0c4e864d4cee2ae4f07b0`

```dockerfile
```

-	Layers:
	-	`sha256:a8886c6ea8456ab8b6a4f204a105b8318814d8ea1272f6d452e49808bfae9afe`  
		Last Modified: Wed, 11 Jun 2025 04:33:48 GMT  
		Size: 3.7 MB (3652748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8873cb330c58c7ee369d7e9d4f6268ff8bb2fc5dfcbceaf10151cea4a7d62bf5`  
		Last Modified: Wed, 11 Jun 2025 04:33:49 GMT  
		Size: 24.4 KB (24428 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:f9ee41f46eaa17e55edff1472c24d22cda47250e8b2e197bc75f9db4c672ccdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (149995746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d608cde8564f16961bc9b39844f93e6a019f503e28be9a2c31adb9c7623c44ce`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27c5344ebf30f80f4535f49a310b31534afd0e30faa287c2f76794168336c12`  
		Last Modified: Wed, 11 Jun 2025 02:53:08 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7613b58989fe943ef5c79460458da358ff15e59da26c00710d2b35058e86fc`  
		Last Modified: Wed, 11 Jun 2025 02:53:09 GMT  
		Size: 7.4 MB (7391037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae980140a28827f67b7331e73db1665544940532e164e45c80b6c78379bc623`  
		Last Modified: Wed, 11 Jun 2025 02:53:13 GMT  
		Size: 73.1 MB (73075802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09451d171b5334d09ddef99e66f401719ea42fefd74cc946f70f4e144d2b9773`  
		Last Modified: Wed, 11 Jun 2025 02:53:09 GMT  
		Size: 378.1 KB (378095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebcb908b216a8512e6db9e0369099fabf5cc207e27ff06cb96a606556ebe5db`  
		Last Modified: Wed, 11 Jun 2025 02:53:09 GMT  
		Size: 99.4 KB (99419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae4c49bd5f4e303ad8871abcc0328792f4c36d63a3bac236266189eaa875aee`  
		Last Modified: Wed, 11 Jun 2025 02:53:09 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e150935a477bd994159253027a6747e5e05949816b4c22a858c59eb09cfa9e1`  
		Last Modified: Wed, 11 Jun 2025 02:55:04 GMT  
		Size: 42.2 MB (42161659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dfdacdc57d0aaeb4f7cedef81d33381076a2aeebd232a7eb230ff0be723abe`  
		Last Modified: Wed, 11 Jun 2025 02:55:01 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:99230260be226e4c58682fdc453fc795b36d10ecbbf5afbc552f42c12ebb2946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3668870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2864cbe1d945201bb9052920374894a27ec78898751cf69133fa67834a288b3b`

```dockerfile
```

-	Layers:
	-	`sha256:56cdfa85b233a1d60442e2c24bb701c10d8c51bb576bff920b4a3ebe1993be09`  
		Last Modified: Wed, 11 Jun 2025 04:33:53 GMT  
		Size: 3.6 MB (3644613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f596efe772c5e037f017516612d75b8f88f8eb7b8674748577be4e8271bd8e04`  
		Last Modified: Wed, 11 Jun 2025 04:33:54 GMT  
		Size: 24.3 KB (24257 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5`

```console
$ docker pull couchdb@sha256:bfcf56d766f6e85aa3834197dee2849ed013907130fbe7b137269bc6dab84b29
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
$ docker pull couchdb@sha256:10159340a455126b0039a6c616258f61fb48990722b7f3d78e38efedf4f49dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139053286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efb0ac883c2114cb29fc3bb00964d3d6212c74a83f58fb0a49105f2c1300c3dd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699d385a56341dc4eca603cb63ab006476be4cb08a753f1a480b78c61886d5bd`  
		Last Modified: Wed, 11 Jun 2025 03:00:14 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39112042a5e68058792d92bcf41abba59268974d788b6d03ca6ae25b9eaae866`  
		Last Modified: Wed, 11 Jun 2025 03:00:16 GMT  
		Size: 7.7 MB (7655745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7ecf0714dbbded096bf25904f9f199b23c48ecd57eb8f188802cfdc07dfd50`  
		Last Modified: Wed, 11 Jun 2025 03:00:14 GMT  
		Size: 349.0 KB (348957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce88728e5f50fb5c57ce17692eb0a190d5220159249d0713e0b6c86807b7ba4`  
		Last Modified: Wed, 11 Jun 2025 03:00:14 GMT  
		Size: 76.3 KB (76295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b6ae98000b8ca8683d91c5052250a43963399ae199d45cdcf1f168eb63033c`  
		Last Modified: Wed, 11 Jun 2025 03:00:14 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0499fd43a835922cb9b40e1e5f35bc3dfd60938e9057a41c88fdc7eb107914de`  
		Last Modified: Wed, 11 Jun 2025 03:00:21 GMT  
		Size: 102.9 MB (102889172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf55c9860891b15c1049fc9627990536eda0ab9ba5604790714bd8173acf807`  
		Last Modified: Wed, 11 Jun 2025 03:00:14 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c298ad74cc2a3e12580740ef96b9b4c176d4001c79964f77fc4c77ba8400cf1f`  
		Last Modified: Wed, 11 Jun 2025 03:00:14 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f88b881ddf57c9aee182c813e18cf4a540c5084a04bd4084b825fb8357beda`  
		Last Modified: Wed, 11 Jun 2025 03:00:16 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767cdb597d3b7571d40221e4118697dc65eef4d9a0f5b161c6ec8b1bf5c39b71`  
		Last Modified: Wed, 11 Jun 2025 03:00:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:bb69d4d557e2b15cc52396a81a672cfbcf78540a39f35df9fa29133b2c30a6b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4169825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637953dc20bcf8062965e6626dd6f658761d49d2648cc1d23a0a70acdb363c14`

```dockerfile
```

-	Layers:
	-	`sha256:d51eeae0aaee7e2c7db21353b7cdc84592b41dca690513cb7fe9a495c42de539`  
		Last Modified: Wed, 11 Jun 2025 04:33:22 GMT  
		Size: 4.1 MB (4137850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bba0af450f31f51cea7b7faec600738dcd8e966e98b58d646d3b3adbc9b6aed`  
		Last Modified: Wed, 11 Jun 2025 04:33:23 GMT  
		Size: 32.0 KB (31975 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5` - linux; s390x

```console
$ docker pull couchdb@sha256:70a40edbe2931e6c61ca9b87d702703e0e34cc81ef669b553645bd4a2f0810a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136514785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37111e3b2c0d7ce3fc7329887734346d84810a8a3a03f7c061cfa9822b0ed0ef`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7638cec2b1dd418d3648a58f2ff51f4e8c71d4a0e97a69f6b885c49b8abb52`  
		Last Modified: Wed, 11 Jun 2025 02:54:18 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6d3b6a7190c29cd3d87e0534ba65c82ca07adaf7c481f25a3ab2b8ec8dfacd`  
		Last Modified: Wed, 11 Jun 2025 02:54:20 GMT  
		Size: 7.4 MB (7391008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e13446e7ec304491354fbbde8273cbbff88817c38fee62076eabfbed576426`  
		Last Modified: Wed, 11 Jun 2025 02:54:19 GMT  
		Size: 355.6 KB (355626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b86396b56c86902e6883c0432db94761c7d4a10454af7b19d3beb817ab4064`  
		Last Modified: Wed, 11 Jun 2025 02:54:19 GMT  
		Size: 76.3 KB (76350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af21af686138b5422cc1b475a30fc9bcc248385f6792df2c32029293e0c00ef`  
		Last Modified: Wed, 11 Jun 2025 06:07:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ac84f9fe4e7e9dbc101fb7147afb2731f413cd2d26424bd8ef24fffd8499aa`  
		Last Modified: Wed, 11 Jun 2025 08:04:07 GMT  
		Size: 101.8 MB (101798517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073097c83b8062b974ad403672e4d054f9554b15f3bc5932428ab43311672a7f`  
		Last Modified: Wed, 11 Jun 2025 06:07:22 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9bc7737db2d11df145c6878bfbc548696b7a5e4a1700b644f1d6fee3967979a`  
		Last Modified: Wed, 11 Jun 2025 06:07:26 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73536106cb7ce4d875ef6b84693f465795d59646d8fc66d0c6a38aa500154eb1`  
		Last Modified: Wed, 11 Jun 2025 06:07:29 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7488eb0b92a2c7ff3502aa1d998b1efd701362b8399b8bd850d8701b3b4e3e59`  
		Last Modified: Wed, 11 Jun 2025 06:07:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:b796d6a9719c7f09f486358d454507e4b9e2dc2153249b862496eebc2a1867e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4165534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e2bb58e11b7e33906937c1b885fa8b5f509093685cc95c846f05c4fcfa523f`

```dockerfile
```

-	Layers:
	-	`sha256:7073765a63c504b9f6b446f6076e638256e453ec9c708ac1d161b97891ec87f2`  
		Last Modified: Wed, 11 Jun 2025 07:33:24 GMT  
		Size: 4.1 MB (4133753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ff3140839540892dee98635e327daa6ebcfcca43f01a39377bf85635e357921`  
		Last Modified: Wed, 11 Jun 2025 07:33:25 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5-nouveau`

```console
$ docker pull couchdb@sha256:93c623b7f212a7a50bf0ac210f8cf65aa29b44e51d8be3e51e51b2e7a39195a5
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
$ docker pull couchdb@sha256:61be76d912255e93b30cf1945f014b4fdf76e855777c534beaa082474c92ea7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155198481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da0e1bcaaa8669646b95ada35469270b7e5acd29ffdea5c36aedda0a0132286`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f727c2cbc5714897417b3bf92251c1ca577c681e1cd4980da1e0a2b431cfb1`  
		Last Modified: Wed, 11 Jun 2025 03:01:03 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4fcda2a3359e316d27ca77539e490e9675e0c09813866f3057f68bfa46ba52`  
		Last Modified: Wed, 11 Jun 2025 03:01:04 GMT  
		Size: 7.7 MB (7655686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98e53920dc0c838f505bb8f5c58498d1729ede7142b247585fbb6f2eeb9e6f8`  
		Last Modified: Wed, 11 Jun 2025 03:01:09 GMT  
		Size: 76.7 MB (76653830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e57bacc8b343b9d3e9cfd79301d2848e9f456723c4ff035f5466a9af631a3e9`  
		Last Modified: Wed, 11 Jun 2025 03:01:03 GMT  
		Size: 371.8 KB (371775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14885eef1f40435843adc0a9862dcb7e864f00e793527847a43cb667f768318`  
		Last Modified: Wed, 11 Jun 2025 03:01:04 GMT  
		Size: 99.3 KB (99289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a5ab6732cf30b1956d2427f8bb4c0b235684efbba3eef54b998ed3e670b32a`  
		Last Modified: Wed, 11 Jun 2025 03:01:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf39d19cde025967aed40a9b4330c966ec21090d4ddbad6f805ec6361f9b4b25`  
		Last Modified: Wed, 11 Jun 2025 03:01:07 GMT  
		Size: 42.3 MB (42338343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608b4fdb60bc3e355862f2bc7e1cb9d10c1010116ac9b3ffb19574d033f3bdc0`  
		Last Modified: Wed, 11 Jun 2025 03:01:05 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:28b3f34e3cae365f40577b9d4cc00022c011cf439378a8f7f391049df355ba7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3677812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb60e8de67c02bbc6d9d397dfaa4b367c76d915a7b52700c4cb64dd1cd02060c`

```dockerfile
```

-	Layers:
	-	`sha256:50114b44d6ab1e22d0f8189abebe1eaf92f096aa041486cae8923f1191f5000a`  
		Last Modified: Wed, 11 Jun 2025 04:33:31 GMT  
		Size: 3.7 MB (3653066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1f7b285a519755f67215c2d46c1b594fd3c7cec213165681b8ecf947d092ebc`  
		Last Modified: Wed, 11 Jun 2025 04:33:32 GMT  
		Size: 24.7 KB (24746 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:9428288909b8b8780ff7256cfaa475dfa7cae9787a8c199fa25a5484feeb957c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (149996183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a7a848960ad42d247b6c8cff11f2fb2bb2db639481885f9fef05176da69d826`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27c5344ebf30f80f4535f49a310b31534afd0e30faa287c2f76794168336c12`  
		Last Modified: Wed, 11 Jun 2025 02:53:08 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7613b58989fe943ef5c79460458da358ff15e59da26c00710d2b35058e86fc`  
		Last Modified: Wed, 11 Jun 2025 02:53:09 GMT  
		Size: 7.4 MB (7391037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae980140a28827f67b7331e73db1665544940532e164e45c80b6c78379bc623`  
		Last Modified: Wed, 11 Jun 2025 02:53:13 GMT  
		Size: 73.1 MB (73075802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09451d171b5334d09ddef99e66f401719ea42fefd74cc946f70f4e144d2b9773`  
		Last Modified: Wed, 11 Jun 2025 02:53:09 GMT  
		Size: 378.1 KB (378095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebcb908b216a8512e6db9e0369099fabf5cc207e27ff06cb96a606556ebe5db`  
		Last Modified: Wed, 11 Jun 2025 02:53:09 GMT  
		Size: 99.4 KB (99419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae4c49bd5f4e303ad8871abcc0328792f4c36d63a3bac236266189eaa875aee`  
		Last Modified: Wed, 11 Jun 2025 02:53:09 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e22ced4f81a0aa6f3cec1052bab74c62d3fd61860da74efd2ea47f1dbcb5287`  
		Last Modified: Wed, 11 Jun 2025 02:53:12 GMT  
		Size: 42.2 MB (42162095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e6a140c73952436c63b826d49f3ca1dc4502867f54809f6ffa15309f5196cf`  
		Last Modified: Wed, 11 Jun 2025 02:53:10 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:d644aae5f48deb39ab35807efd7339906fe75ae9f71da8dc3dfb7a7ececc3927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3669483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c786bdcb66a2a06c4e498f97125c5286af66de6ece5d3728db0649369c2861`

```dockerfile
```

-	Layers:
	-	`sha256:e7bac52cfee4e7614f1df282f0e9225e48cc895ff50dcbf86b6267184d437230`  
		Last Modified: Wed, 11 Jun 2025 04:33:36 GMT  
		Size: 3.6 MB (3644919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c788e021d6e8698fd1889130f527f5fea495bae07c9640626152301c9bec455`  
		Last Modified: Wed, 11 Jun 2025 04:33:37 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.0`

```console
$ docker pull couchdb@sha256:bfcf56d766f6e85aa3834197dee2849ed013907130fbe7b137269bc6dab84b29
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
$ docker pull couchdb@sha256:10159340a455126b0039a6c616258f61fb48990722b7f3d78e38efedf4f49dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139053286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efb0ac883c2114cb29fc3bb00964d3d6212c74a83f58fb0a49105f2c1300c3dd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699d385a56341dc4eca603cb63ab006476be4cb08a753f1a480b78c61886d5bd`  
		Last Modified: Wed, 11 Jun 2025 03:00:14 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39112042a5e68058792d92bcf41abba59268974d788b6d03ca6ae25b9eaae866`  
		Last Modified: Wed, 11 Jun 2025 03:00:16 GMT  
		Size: 7.7 MB (7655745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7ecf0714dbbded096bf25904f9f199b23c48ecd57eb8f188802cfdc07dfd50`  
		Last Modified: Wed, 11 Jun 2025 03:00:14 GMT  
		Size: 349.0 KB (348957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce88728e5f50fb5c57ce17692eb0a190d5220159249d0713e0b6c86807b7ba4`  
		Last Modified: Wed, 11 Jun 2025 03:00:14 GMT  
		Size: 76.3 KB (76295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b6ae98000b8ca8683d91c5052250a43963399ae199d45cdcf1f168eb63033c`  
		Last Modified: Wed, 11 Jun 2025 03:00:14 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0499fd43a835922cb9b40e1e5f35bc3dfd60938e9057a41c88fdc7eb107914de`  
		Last Modified: Wed, 11 Jun 2025 03:00:21 GMT  
		Size: 102.9 MB (102889172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf55c9860891b15c1049fc9627990536eda0ab9ba5604790714bd8173acf807`  
		Last Modified: Wed, 11 Jun 2025 03:00:14 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c298ad74cc2a3e12580740ef96b9b4c176d4001c79964f77fc4c77ba8400cf1f`  
		Last Modified: Wed, 11 Jun 2025 03:00:14 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f88b881ddf57c9aee182c813e18cf4a540c5084a04bd4084b825fb8357beda`  
		Last Modified: Wed, 11 Jun 2025 03:00:16 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767cdb597d3b7571d40221e4118697dc65eef4d9a0f5b161c6ec8b1bf5c39b71`  
		Last Modified: Wed, 11 Jun 2025 03:00:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0` - unknown; unknown

```console
$ docker pull couchdb@sha256:bb69d4d557e2b15cc52396a81a672cfbcf78540a39f35df9fa29133b2c30a6b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4169825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637953dc20bcf8062965e6626dd6f658761d49d2648cc1d23a0a70acdb363c14`

```dockerfile
```

-	Layers:
	-	`sha256:d51eeae0aaee7e2c7db21353b7cdc84592b41dca690513cb7fe9a495c42de539`  
		Last Modified: Wed, 11 Jun 2025 04:33:22 GMT  
		Size: 4.1 MB (4137850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bba0af450f31f51cea7b7faec600738dcd8e966e98b58d646d3b3adbc9b6aed`  
		Last Modified: Wed, 11 Jun 2025 04:33:23 GMT  
		Size: 32.0 KB (31975 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.0` - linux; s390x

```console
$ docker pull couchdb@sha256:70a40edbe2931e6c61ca9b87d702703e0e34cc81ef669b553645bd4a2f0810a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136514785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37111e3b2c0d7ce3fc7329887734346d84810a8a3a03f7c061cfa9822b0ed0ef`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7638cec2b1dd418d3648a58f2ff51f4e8c71d4a0e97a69f6b885c49b8abb52`  
		Last Modified: Wed, 11 Jun 2025 02:54:18 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6d3b6a7190c29cd3d87e0534ba65c82ca07adaf7c481f25a3ab2b8ec8dfacd`  
		Last Modified: Wed, 11 Jun 2025 02:54:20 GMT  
		Size: 7.4 MB (7391008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e13446e7ec304491354fbbde8273cbbff88817c38fee62076eabfbed576426`  
		Last Modified: Wed, 11 Jun 2025 02:54:19 GMT  
		Size: 355.6 KB (355626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b86396b56c86902e6883c0432db94761c7d4a10454af7b19d3beb817ab4064`  
		Last Modified: Wed, 11 Jun 2025 02:54:19 GMT  
		Size: 76.3 KB (76350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af21af686138b5422cc1b475a30fc9bcc248385f6792df2c32029293e0c00ef`  
		Last Modified: Wed, 11 Jun 2025 06:07:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ac84f9fe4e7e9dbc101fb7147afb2731f413cd2d26424bd8ef24fffd8499aa`  
		Last Modified: Wed, 11 Jun 2025 08:04:07 GMT  
		Size: 101.8 MB (101798517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073097c83b8062b974ad403672e4d054f9554b15f3bc5932428ab43311672a7f`  
		Last Modified: Wed, 11 Jun 2025 06:07:22 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9bc7737db2d11df145c6878bfbc548696b7a5e4a1700b644f1d6fee3967979a`  
		Last Modified: Wed, 11 Jun 2025 06:07:26 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73536106cb7ce4d875ef6b84693f465795d59646d8fc66d0c6a38aa500154eb1`  
		Last Modified: Wed, 11 Jun 2025 06:07:29 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7488eb0b92a2c7ff3502aa1d998b1efd701362b8399b8bd850d8701b3b4e3e59`  
		Last Modified: Wed, 11 Jun 2025 06:07:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0` - unknown; unknown

```console
$ docker pull couchdb@sha256:b796d6a9719c7f09f486358d454507e4b9e2dc2153249b862496eebc2a1867e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4165534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e2bb58e11b7e33906937c1b885fa8b5f509093685cc95c846f05c4fcfa523f`

```dockerfile
```

-	Layers:
	-	`sha256:7073765a63c504b9f6b446f6076e638256e453ec9c708ac1d161b97891ec87f2`  
		Last Modified: Wed, 11 Jun 2025 07:33:24 GMT  
		Size: 4.1 MB (4133753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ff3140839540892dee98635e327daa6ebcfcca43f01a39377bf85635e357921`  
		Last Modified: Wed, 11 Jun 2025 07:33:25 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.0-nouveau`

```console
$ docker pull couchdb@sha256:93c623b7f212a7a50bf0ac210f8cf65aa29b44e51d8be3e51e51b2e7a39195a5
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
$ docker pull couchdb@sha256:61be76d912255e93b30cf1945f014b4fdf76e855777c534beaa082474c92ea7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155198481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da0e1bcaaa8669646b95ada35469270b7e5acd29ffdea5c36aedda0a0132286`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f727c2cbc5714897417b3bf92251c1ca577c681e1cd4980da1e0a2b431cfb1`  
		Last Modified: Wed, 11 Jun 2025 03:01:03 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4fcda2a3359e316d27ca77539e490e9675e0c09813866f3057f68bfa46ba52`  
		Last Modified: Wed, 11 Jun 2025 03:01:04 GMT  
		Size: 7.7 MB (7655686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98e53920dc0c838f505bb8f5c58498d1729ede7142b247585fbb6f2eeb9e6f8`  
		Last Modified: Wed, 11 Jun 2025 03:01:09 GMT  
		Size: 76.7 MB (76653830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e57bacc8b343b9d3e9cfd79301d2848e9f456723c4ff035f5466a9af631a3e9`  
		Last Modified: Wed, 11 Jun 2025 03:01:03 GMT  
		Size: 371.8 KB (371775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14885eef1f40435843adc0a9862dcb7e864f00e793527847a43cb667f768318`  
		Last Modified: Wed, 11 Jun 2025 03:01:04 GMT  
		Size: 99.3 KB (99289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a5ab6732cf30b1956d2427f8bb4c0b235684efbba3eef54b998ed3e670b32a`  
		Last Modified: Wed, 11 Jun 2025 03:01:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf39d19cde025967aed40a9b4330c966ec21090d4ddbad6f805ec6361f9b4b25`  
		Last Modified: Wed, 11 Jun 2025 03:01:07 GMT  
		Size: 42.3 MB (42338343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608b4fdb60bc3e355862f2bc7e1cb9d10c1010116ac9b3ffb19574d033f3bdc0`  
		Last Modified: Wed, 11 Jun 2025 03:01:05 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:28b3f34e3cae365f40577b9d4cc00022c011cf439378a8f7f391049df355ba7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3677812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb60e8de67c02bbc6d9d397dfaa4b367c76d915a7b52700c4cb64dd1cd02060c`

```dockerfile
```

-	Layers:
	-	`sha256:50114b44d6ab1e22d0f8189abebe1eaf92f096aa041486cae8923f1191f5000a`  
		Last Modified: Wed, 11 Jun 2025 04:33:31 GMT  
		Size: 3.7 MB (3653066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1f7b285a519755f67215c2d46c1b594fd3c7cec213165681b8ecf947d092ebc`  
		Last Modified: Wed, 11 Jun 2025 04:33:32 GMT  
		Size: 24.7 KB (24746 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.0-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:9428288909b8b8780ff7256cfaa475dfa7cae9787a8c199fa25a5484feeb957c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (149996183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a7a848960ad42d247b6c8cff11f2fb2bb2db639481885f9fef05176da69d826`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27c5344ebf30f80f4535f49a310b31534afd0e30faa287c2f76794168336c12`  
		Last Modified: Wed, 11 Jun 2025 02:53:08 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7613b58989fe943ef5c79460458da358ff15e59da26c00710d2b35058e86fc`  
		Last Modified: Wed, 11 Jun 2025 02:53:09 GMT  
		Size: 7.4 MB (7391037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae980140a28827f67b7331e73db1665544940532e164e45c80b6c78379bc623`  
		Last Modified: Wed, 11 Jun 2025 02:53:13 GMT  
		Size: 73.1 MB (73075802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09451d171b5334d09ddef99e66f401719ea42fefd74cc946f70f4e144d2b9773`  
		Last Modified: Wed, 11 Jun 2025 02:53:09 GMT  
		Size: 378.1 KB (378095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebcb908b216a8512e6db9e0369099fabf5cc207e27ff06cb96a606556ebe5db`  
		Last Modified: Wed, 11 Jun 2025 02:53:09 GMT  
		Size: 99.4 KB (99419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae4c49bd5f4e303ad8871abcc0328792f4c36d63a3bac236266189eaa875aee`  
		Last Modified: Wed, 11 Jun 2025 02:53:09 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e22ced4f81a0aa6f3cec1052bab74c62d3fd61860da74efd2ea47f1dbcb5287`  
		Last Modified: Wed, 11 Jun 2025 02:53:12 GMT  
		Size: 42.2 MB (42162095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e6a140c73952436c63b826d49f3ca1dc4502867f54809f6ffa15309f5196cf`  
		Last Modified: Wed, 11 Jun 2025 02:53:10 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:d644aae5f48deb39ab35807efd7339906fe75ae9f71da8dc3dfb7a7ececc3927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3669483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c786bdcb66a2a06c4e498f97125c5286af66de6ece5d3728db0649369c2861`

```dockerfile
```

-	Layers:
	-	`sha256:e7bac52cfee4e7614f1df282f0e9225e48cc895ff50dcbf86b6267184d437230`  
		Last Modified: Wed, 11 Jun 2025 04:33:36 GMT  
		Size: 3.6 MB (3644919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c788e021d6e8698fd1889130f527f5fea495bae07c9640626152301c9bec455`  
		Last Modified: Wed, 11 Jun 2025 04:33:37 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:bfcf56d766f6e85aa3834197dee2849ed013907130fbe7b137269bc6dab84b29
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
$ docker pull couchdb@sha256:10159340a455126b0039a6c616258f61fb48990722b7f3d78e38efedf4f49dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139053286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efb0ac883c2114cb29fc3bb00964d3d6212c74a83f58fb0a49105f2c1300c3dd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699d385a56341dc4eca603cb63ab006476be4cb08a753f1a480b78c61886d5bd`  
		Last Modified: Wed, 11 Jun 2025 03:00:14 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39112042a5e68058792d92bcf41abba59268974d788b6d03ca6ae25b9eaae866`  
		Last Modified: Wed, 11 Jun 2025 03:00:16 GMT  
		Size: 7.7 MB (7655745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7ecf0714dbbded096bf25904f9f199b23c48ecd57eb8f188802cfdc07dfd50`  
		Last Modified: Wed, 11 Jun 2025 03:00:14 GMT  
		Size: 349.0 KB (348957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce88728e5f50fb5c57ce17692eb0a190d5220159249d0713e0b6c86807b7ba4`  
		Last Modified: Wed, 11 Jun 2025 03:00:14 GMT  
		Size: 76.3 KB (76295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b6ae98000b8ca8683d91c5052250a43963399ae199d45cdcf1f168eb63033c`  
		Last Modified: Wed, 11 Jun 2025 03:00:14 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0499fd43a835922cb9b40e1e5f35bc3dfd60938e9057a41c88fdc7eb107914de`  
		Last Modified: Wed, 11 Jun 2025 03:00:21 GMT  
		Size: 102.9 MB (102889172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf55c9860891b15c1049fc9627990536eda0ab9ba5604790714bd8173acf807`  
		Last Modified: Wed, 11 Jun 2025 03:00:14 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c298ad74cc2a3e12580740ef96b9b4c176d4001c79964f77fc4c77ba8400cf1f`  
		Last Modified: Wed, 11 Jun 2025 03:00:14 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f88b881ddf57c9aee182c813e18cf4a540c5084a04bd4084b825fb8357beda`  
		Last Modified: Wed, 11 Jun 2025 03:00:16 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767cdb597d3b7571d40221e4118697dc65eef4d9a0f5b161c6ec8b1bf5c39b71`  
		Last Modified: Wed, 11 Jun 2025 03:00:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:bb69d4d557e2b15cc52396a81a672cfbcf78540a39f35df9fa29133b2c30a6b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4169825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637953dc20bcf8062965e6626dd6f658761d49d2648cc1d23a0a70acdb363c14`

```dockerfile
```

-	Layers:
	-	`sha256:d51eeae0aaee7e2c7db21353b7cdc84592b41dca690513cb7fe9a495c42de539`  
		Last Modified: Wed, 11 Jun 2025 04:33:22 GMT  
		Size: 4.1 MB (4137850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bba0af450f31f51cea7b7faec600738dcd8e966e98b58d646d3b3adbc9b6aed`  
		Last Modified: Wed, 11 Jun 2025 04:33:23 GMT  
		Size: 32.0 KB (31975 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:70a40edbe2931e6c61ca9b87d702703e0e34cc81ef669b553645bd4a2f0810a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136514785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37111e3b2c0d7ce3fc7329887734346d84810a8a3a03f7c061cfa9822b0ed0ef`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7638cec2b1dd418d3648a58f2ff51f4e8c71d4a0e97a69f6b885c49b8abb52`  
		Last Modified: Wed, 11 Jun 2025 02:54:18 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6d3b6a7190c29cd3d87e0534ba65c82ca07adaf7c481f25a3ab2b8ec8dfacd`  
		Last Modified: Wed, 11 Jun 2025 02:54:20 GMT  
		Size: 7.4 MB (7391008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e13446e7ec304491354fbbde8273cbbff88817c38fee62076eabfbed576426`  
		Last Modified: Wed, 11 Jun 2025 02:54:19 GMT  
		Size: 355.6 KB (355626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b86396b56c86902e6883c0432db94761c7d4a10454af7b19d3beb817ab4064`  
		Last Modified: Wed, 11 Jun 2025 02:54:19 GMT  
		Size: 76.3 KB (76350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af21af686138b5422cc1b475a30fc9bcc248385f6792df2c32029293e0c00ef`  
		Last Modified: Wed, 11 Jun 2025 06:07:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ac84f9fe4e7e9dbc101fb7147afb2731f413cd2d26424bd8ef24fffd8499aa`  
		Last Modified: Wed, 11 Jun 2025 08:04:07 GMT  
		Size: 101.8 MB (101798517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073097c83b8062b974ad403672e4d054f9554b15f3bc5932428ab43311672a7f`  
		Last Modified: Wed, 11 Jun 2025 06:07:22 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9bc7737db2d11df145c6878bfbc548696b7a5e4a1700b644f1d6fee3967979a`  
		Last Modified: Wed, 11 Jun 2025 06:07:26 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73536106cb7ce4d875ef6b84693f465795d59646d8fc66d0c6a38aa500154eb1`  
		Last Modified: Wed, 11 Jun 2025 06:07:29 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7488eb0b92a2c7ff3502aa1d998b1efd701362b8399b8bd850d8701b3b4e3e59`  
		Last Modified: Wed, 11 Jun 2025 06:07:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:b796d6a9719c7f09f486358d454507e4b9e2dc2153249b862496eebc2a1867e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4165534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e2bb58e11b7e33906937c1b885fa8b5f509093685cc95c846f05c4fcfa523f`

```dockerfile
```

-	Layers:
	-	`sha256:7073765a63c504b9f6b446f6076e638256e453ec9c708ac1d161b97891ec87f2`  
		Last Modified: Wed, 11 Jun 2025 07:33:24 GMT  
		Size: 4.1 MB (4133753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ff3140839540892dee98635e327daa6ebcfcca43f01a39377bf85635e357921`  
		Last Modified: Wed, 11 Jun 2025 07:33:25 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json
