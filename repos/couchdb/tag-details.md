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
$ docker pull couchdb@sha256:30c14bf9d5d1a04c0b1b9ef0442131df69624f91221b0631ab6e75dd7f99fac5
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
$ docker pull couchdb@sha256:650816f7a1006f5a1b3e11a45c1cde40f3f5e8d2968e921268bc6ee7a14487ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139823939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4be8cafa64bcfa821cd43fd6b36081b3e21abc405d1e6ac268849176e379a85`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa98feb63093c87a2fbef9a528fcb0100e4b549abd70c810bb1d83a89d3a40c`  
		Last Modified: Tue, 10 Jun 2025 23:37:44 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6af541d5ad9b46b3581c08015d9efa0bb34ab7201c486654432b547404ad8d9`  
		Last Modified: Tue, 10 Jun 2025 23:37:45 GMT  
		Size: 7.9 MB (7876608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23529365cfa8356ef20af79faafbfcf4a227f69a5d0867f4b58541964362f97a`  
		Last Modified: Tue, 10 Jun 2025 23:37:45 GMT  
		Size: 392.1 KB (392136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff48d6b0776af8bf12a15456f0ef5366a1a0f61b8176573937877c841860d5f`  
		Last Modified: Tue, 10 Jun 2025 23:37:45 GMT  
		Size: 76.3 KB (76318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2e5aa79a5d0311974e5ab3be5f12cc7fc056c785fdcff6d72d4d510b6e2bfb`  
		Last Modified: Tue, 10 Jun 2025 23:37:45 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5079dacc7d9108ffae28bb29ab88aa2bd5c028ce94a7c922376e2c4b3c017e9f`  
		Last Modified: Tue, 10 Jun 2025 23:37:51 GMT  
		Size: 103.2 MB (103243324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5417499cb993cec049da7c7cd8770d9e713bf3c7ca693b370b296d8a872af00d`  
		Last Modified: Tue, 10 Jun 2025 23:37:45 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c12f91365777bfd974aebd2fe56e2f2673cf2f8116a672ef08c601bd36d432b`  
		Last Modified: Tue, 10 Jun 2025 23:37:46 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37db75e31662ccb5742ad5cdee2506b30a223880b937bea9ff4098adea32a207`  
		Last Modified: Tue, 10 Jun 2025 23:37:46 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d8afe72a86ea1a4a1d3bda4a98de4bdb9f6d2c3e9e1b3aed6c395b519cb813`  
		Last Modified: Tue, 10 Jun 2025 23:37:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:c70516dc7ac5d5ac16466ab4d2112b0ef68f64dd581f148913bc67245d34dc3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4169338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c41048a33369a9543660c0210cba330bf0973b092aaf7cb9d324d9c8c07c40d2`

```dockerfile
```

-	Layers:
	-	`sha256:59294ef9fa53e56a45c2badee7867b173babeb75717a858003040762f7d8ae11`  
		Last Modified: Wed, 11 Jun 2025 01:33:19 GMT  
		Size: 4.1 MB (4137557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2274988eb7c5e4108cbe94c99ed0b79b56ab4d321660f32aa86a44c5ba710a23`  
		Last Modified: Wed, 11 Jun 2025 01:33:20 GMT  
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
$ docker pull couchdb@sha256:b0346ec3bc28165f80378b038fd1a6d5ee446f0fcb44ca17b8d54fdc7b373c14
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
$ docker pull couchdb@sha256:af94c41e1a577f9f0368d93139035bc2fef98a8064a5fcfbe4467ce722b105aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156383379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:943ceeaa4bc9f025c27b5c65db56e2dd4a97990a9a1a30093a7fa558f5ca0784`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d44569cb297eb28d4ff419ad9edafca9a631b6918f51afc2645b27cf032824`  
		Last Modified: Tue, 10 Jun 2025 23:37:56 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90c842f875a09baf9748bdc12473aebbcd40a254d6f0337c8fff1133b62a20b`  
		Last Modified: Wed, 11 Jun 2025 05:34:18 GMT  
		Size: 7.9 MB (7876636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f90426813dc42a51ecf2f149ddbd49144780d12bda23a14121c3c32ecc78eb2`  
		Last Modified: Tue, 10 Jun 2025 23:38:03 GMT  
		Size: 77.3 MB (77324908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78240b230d48a51695db890d2d358d0746e87c52257befd5d2891d91134e9f16`  
		Last Modified: Tue, 10 Jun 2025 23:37:57 GMT  
		Size: 415.0 KB (414977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed75d6869dbcb6059987515c19bfe7f709e0e20006a5565253e863057ed99736`  
		Last Modified: Tue, 10 Jun 2025 23:37:57 GMT  
		Size: 99.3 KB (99295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d14d1d6a8d14b19e2ed9059a99e3dcb9519d61a0106c0b7f7d632c60a7120b4`  
		Last Modified: Tue, 10 Jun 2025 23:37:58 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c1e50a62cc24b3d3a3e976e91f990ee7797d4cbec71efc65eca0adbefcb8d2`  
		Last Modified: Tue, 10 Jun 2025 23:38:01 GMT  
		Size: 42.4 MB (42435562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6003201ca33590ce10fd133b9fbb92ae4a424f9666fb540020ebfa7fa345878`  
		Last Modified: Tue, 10 Jun 2025 23:37:58 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:bba6d09243f9a3b886ffe86c9132a4482c0ea0e36a446859c7e3539a9904031e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3678954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e560747821ef2c676675a73deae02f80298d8a978832a53e0bf42bde5fe46f9b`

```dockerfile
```

-	Layers:
	-	`sha256:ae305fdfb94dfc74f50d6b45b7dceac45970e747442b0a6ef57233136c19a66e`  
		Last Modified: Wed, 11 Jun 2025 01:33:25 GMT  
		Size: 3.7 MB (3654390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:068cf40840553703ce1ed297cd1f04c201c51dddd38ac095984a9d25cc1f0f5b`  
		Last Modified: Wed, 11 Jun 2025 01:33:26 GMT  
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
$ docker pull couchdb@sha256:7ea0a6117e82610d99b5b4cc116244a2f913417fe6c030fb22846838c62585db
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
$ docker pull couchdb@sha256:c6cff58ca517f888e29f0a89ec7c44ca64883880d9a45be1b5a4fa6bf65caf16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139000135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c36f6bd731c5aa08ff2718a48cf46f98d7b07032df4a53255a3b878298feaa6d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b874e74aea5349bf33cec9464d521d97de96ac1a6cc8a7b888e937fc0d252101`  
		Last Modified: Tue, 10 Jun 2025 23:38:02 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aceb2db0eb0efc5e0b5b37a76127cbb4c39238b007abe5de7aaa2d7519a645d6`  
		Last Modified: Tue, 10 Jun 2025 23:38:02 GMT  
		Size: 7.9 MB (7876480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee7d0988888171512bdf50c71ca83a230874b975b07eacd9dc61a4da9d32af1`  
		Last Modified: Tue, 10 Jun 2025 23:38:02 GMT  
		Size: 392.1 KB (392128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e19cb238831ecb0f2c63bedc129455407fe09c6e59d4f9a1ad5c9005059210`  
		Last Modified: Tue, 10 Jun 2025 23:38:02 GMT  
		Size: 76.3 KB (76273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e421ad90dfa6bf7b9838aa55a85fbc1deea093fcadd1af4d5248564251720a7f`  
		Last Modified: Tue, 10 Jun 2025 23:38:02 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874b8375b921f5f203013da03ab33fd7a1bd20cbeba5a669c7bc7ae68345c7c6`  
		Last Modified: Tue, 10 Jun 2025 23:38:06 GMT  
		Size: 102.4 MB (102419691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617b44ea937401f727a594df242fc2dc711f8bbd2aea98654fa9468ac1037b66`  
		Last Modified: Tue, 10 Jun 2025 23:38:02 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7a5938be48c851f6ac890df6509c9a37e4930f2a2ed3507d76020bb527f45a`  
		Last Modified: Tue, 10 Jun 2025 23:38:03 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b0b7628f5d4b89585bd60a4bfa94d788ae2f83d78c5e062d3250903d8f1b81`  
		Last Modified: Tue, 10 Jun 2025 23:38:03 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b88d92a9288c7ed30f1492e2a67c6092d17e0ca93579914d7f190846e5dbb67`  
		Last Modified: Tue, 10 Jun 2025 23:38:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:25ead22d0cb332634193f63e5f810929723c2aee8975b5c4ba419901d3827b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05ffa3823dc71804a64ed4e13ea5b89a2c722aa01aaa647c757ec881fe693202`

```dockerfile
```

-	Layers:
	-	`sha256:ce9f6d3478e5b190fa033cd0d1604d0c040ca25f8202558ba163d4b26d025421`  
		Last Modified: Wed, 11 Jun 2025 01:33:30 GMT  
		Size: 4.1 MB (4121690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33ac19a9ba19b41f0422e615667a51d3ea038717aacd5feb24ac2d47f3559d5d`  
		Last Modified: Wed, 11 Jun 2025 01:33:31 GMT  
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
$ docker pull couchdb@sha256:c14c2aead933c549ffc452ded49bd9e7cc29d07ae00d0cf046d16bbea59dddf0
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
$ docker pull couchdb@sha256:1c4d76145f8ddddf586ea3fbf78c07d53b42bff0aaa67d4aadbb1044e26b6221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156383507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:573788f886d8032bcc1753a2954b32acf2786d63c0632412d543898fc5af0c98`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639480b89fb18642d269d9d4fc274b15548abfc7eee9a06fe4eeaf3fd2164465`  
		Last Modified: Tue, 10 Jun 2025 23:38:17 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a121bd23becd4a29f1a356783bb0007d2b4ba1eabe8d0ea87346b014b7f994`  
		Last Modified: Tue, 10 Jun 2025 23:38:19 GMT  
		Size: 7.9 MB (7876573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ae5361c11d3061b02369233807cb8240f757eddf3688f01b110ca874510c6d`  
		Last Modified: Tue, 10 Jun 2025 23:38:21 GMT  
		Size: 77.3 MB (77325212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bf00b6796fb1955083c084b1102607c7e2eae3160e5a456eac6eddfe036a73`  
		Last Modified: Tue, 10 Jun 2025 23:38:18 GMT  
		Size: 415.0 KB (414982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0f6ae655cda15f132ef399601ba2d6bf95b8d8f3707943fadf458a890557fc`  
		Last Modified: Tue, 10 Jun 2025 23:38:19 GMT  
		Size: 99.3 KB (99316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3741f9d9affd8694174670ea33f112f163cca4a9fe4d468d0251d5a3d868f03`  
		Last Modified: Tue, 10 Jun 2025 23:38:19 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26059bac976a83102ff3785eddb09c1f6c9c69416dca55f06e8c07ce798ae214`  
		Last Modified: Tue, 10 Jun 2025 23:38:22 GMT  
		Size: 42.4 MB (42435416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd6f3fd19e0f707e5891951b53263e50d95d6bfbb45ce4e3175796dcb535593`  
		Last Modified: Tue, 10 Jun 2025 23:38:20 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:df76f98303c972fc5d98b41b67cdc49b735bc61a08e4dda5d7daf061cd0cafca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3678342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e040dd5a17aa1bb853b2fb39a4e1fb3ae45ce09287033f2a273c7ab43a44a64c`

```dockerfile
```

-	Layers:
	-	`sha256:05d7032c44b8d4044992155d23bdd572d748d7cb89def2a7617609c25155760f`  
		Last Modified: Wed, 11 Jun 2025 01:33:35 GMT  
		Size: 3.7 MB (3654084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:227e4377399cc48d8c8e65ae8c5399b09c80e088d21e0c71433749ac70b47926`  
		Last Modified: Wed, 11 Jun 2025 01:33:36 GMT  
		Size: 24.3 KB (24258 bytes)  
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
$ docker pull couchdb@sha256:7ea0a6117e82610d99b5b4cc116244a2f913417fe6c030fb22846838c62585db
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
$ docker pull couchdb@sha256:c6cff58ca517f888e29f0a89ec7c44ca64883880d9a45be1b5a4fa6bf65caf16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139000135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c36f6bd731c5aa08ff2718a48cf46f98d7b07032df4a53255a3b878298feaa6d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b874e74aea5349bf33cec9464d521d97de96ac1a6cc8a7b888e937fc0d252101`  
		Last Modified: Tue, 10 Jun 2025 23:38:02 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aceb2db0eb0efc5e0b5b37a76127cbb4c39238b007abe5de7aaa2d7519a645d6`  
		Last Modified: Tue, 10 Jun 2025 23:38:02 GMT  
		Size: 7.9 MB (7876480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee7d0988888171512bdf50c71ca83a230874b975b07eacd9dc61a4da9d32af1`  
		Last Modified: Tue, 10 Jun 2025 23:38:02 GMT  
		Size: 392.1 KB (392128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e19cb238831ecb0f2c63bedc129455407fe09c6e59d4f9a1ad5c9005059210`  
		Last Modified: Tue, 10 Jun 2025 23:38:02 GMT  
		Size: 76.3 KB (76273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e421ad90dfa6bf7b9838aa55a85fbc1deea093fcadd1af4d5248564251720a7f`  
		Last Modified: Tue, 10 Jun 2025 23:38:02 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874b8375b921f5f203013da03ab33fd7a1bd20cbeba5a669c7bc7ae68345c7c6`  
		Last Modified: Tue, 10 Jun 2025 23:38:06 GMT  
		Size: 102.4 MB (102419691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617b44ea937401f727a594df242fc2dc711f8bbd2aea98654fa9468ac1037b66`  
		Last Modified: Tue, 10 Jun 2025 23:38:02 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7a5938be48c851f6ac890df6509c9a37e4930f2a2ed3507d76020bb527f45a`  
		Last Modified: Tue, 10 Jun 2025 23:38:03 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b0b7628f5d4b89585bd60a4bfa94d788ae2f83d78c5e062d3250903d8f1b81`  
		Last Modified: Tue, 10 Jun 2025 23:38:03 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b88d92a9288c7ed30f1492e2a67c6092d17e0ca93579914d7f190846e5dbb67`  
		Last Modified: Tue, 10 Jun 2025 23:38:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:25ead22d0cb332634193f63e5f810929723c2aee8975b5c4ba419901d3827b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05ffa3823dc71804a64ed4e13ea5b89a2c722aa01aaa647c757ec881fe693202`

```dockerfile
```

-	Layers:
	-	`sha256:ce9f6d3478e5b190fa033cd0d1604d0c040ca25f8202558ba163d4b26d025421`  
		Last Modified: Wed, 11 Jun 2025 01:33:30 GMT  
		Size: 4.1 MB (4121690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33ac19a9ba19b41f0422e615667a51d3ea038717aacd5feb24ac2d47f3559d5d`  
		Last Modified: Wed, 11 Jun 2025 01:33:31 GMT  
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
$ docker pull couchdb@sha256:c14c2aead933c549ffc452ded49bd9e7cc29d07ae00d0cf046d16bbea59dddf0
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
$ docker pull couchdb@sha256:1c4d76145f8ddddf586ea3fbf78c07d53b42bff0aaa67d4aadbb1044e26b6221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156383507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:573788f886d8032bcc1753a2954b32acf2786d63c0632412d543898fc5af0c98`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639480b89fb18642d269d9d4fc274b15548abfc7eee9a06fe4eeaf3fd2164465`  
		Last Modified: Tue, 10 Jun 2025 23:38:17 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a121bd23becd4a29f1a356783bb0007d2b4ba1eabe8d0ea87346b014b7f994`  
		Last Modified: Tue, 10 Jun 2025 23:38:19 GMT  
		Size: 7.9 MB (7876573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ae5361c11d3061b02369233807cb8240f757eddf3688f01b110ca874510c6d`  
		Last Modified: Tue, 10 Jun 2025 23:38:21 GMT  
		Size: 77.3 MB (77325212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bf00b6796fb1955083c084b1102607c7e2eae3160e5a456eac6eddfe036a73`  
		Last Modified: Tue, 10 Jun 2025 23:38:18 GMT  
		Size: 415.0 KB (414982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0f6ae655cda15f132ef399601ba2d6bf95b8d8f3707943fadf458a890557fc`  
		Last Modified: Tue, 10 Jun 2025 23:38:19 GMT  
		Size: 99.3 KB (99316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3741f9d9affd8694174670ea33f112f163cca4a9fe4d468d0251d5a3d868f03`  
		Last Modified: Tue, 10 Jun 2025 23:38:19 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26059bac976a83102ff3785eddb09c1f6c9c69416dca55f06e8c07ce798ae214`  
		Last Modified: Tue, 10 Jun 2025 23:38:22 GMT  
		Size: 42.4 MB (42435416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd6f3fd19e0f707e5891951b53263e50d95d6bfbb45ce4e3175796dcb535593`  
		Last Modified: Tue, 10 Jun 2025 23:38:20 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:df76f98303c972fc5d98b41b67cdc49b735bc61a08e4dda5d7daf061cd0cafca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3678342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e040dd5a17aa1bb853b2fb39a4e1fb3ae45ce09287033f2a273c7ab43a44a64c`

```dockerfile
```

-	Layers:
	-	`sha256:05d7032c44b8d4044992155d23bdd572d748d7cb89def2a7617609c25155760f`  
		Last Modified: Wed, 11 Jun 2025 01:33:35 GMT  
		Size: 3.7 MB (3654084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:227e4377399cc48d8c8e65ae8c5399b09c80e088d21e0c71433749ac70b47926`  
		Last Modified: Wed, 11 Jun 2025 01:33:36 GMT  
		Size: 24.3 KB (24258 bytes)  
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
$ docker pull couchdb@sha256:30c14bf9d5d1a04c0b1b9ef0442131df69624f91221b0631ab6e75dd7f99fac5
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
$ docker pull couchdb@sha256:650816f7a1006f5a1b3e11a45c1cde40f3f5e8d2968e921268bc6ee7a14487ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139823939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4be8cafa64bcfa821cd43fd6b36081b3e21abc405d1e6ac268849176e379a85`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa98feb63093c87a2fbef9a528fcb0100e4b549abd70c810bb1d83a89d3a40c`  
		Last Modified: Tue, 10 Jun 2025 23:37:44 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6af541d5ad9b46b3581c08015d9efa0bb34ab7201c486654432b547404ad8d9`  
		Last Modified: Tue, 10 Jun 2025 23:37:45 GMT  
		Size: 7.9 MB (7876608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23529365cfa8356ef20af79faafbfcf4a227f69a5d0867f4b58541964362f97a`  
		Last Modified: Tue, 10 Jun 2025 23:37:45 GMT  
		Size: 392.1 KB (392136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff48d6b0776af8bf12a15456f0ef5366a1a0f61b8176573937877c841860d5f`  
		Last Modified: Tue, 10 Jun 2025 23:37:45 GMT  
		Size: 76.3 KB (76318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2e5aa79a5d0311974e5ab3be5f12cc7fc056c785fdcff6d72d4d510b6e2bfb`  
		Last Modified: Tue, 10 Jun 2025 23:37:45 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5079dacc7d9108ffae28bb29ab88aa2bd5c028ce94a7c922376e2c4b3c017e9f`  
		Last Modified: Tue, 10 Jun 2025 23:37:51 GMT  
		Size: 103.2 MB (103243324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5417499cb993cec049da7c7cd8770d9e713bf3c7ca693b370b296d8a872af00d`  
		Last Modified: Tue, 10 Jun 2025 23:37:45 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c12f91365777bfd974aebd2fe56e2f2673cf2f8116a672ef08c601bd36d432b`  
		Last Modified: Tue, 10 Jun 2025 23:37:46 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37db75e31662ccb5742ad5cdee2506b30a223880b937bea9ff4098adea32a207`  
		Last Modified: Tue, 10 Jun 2025 23:37:46 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d8afe72a86ea1a4a1d3bda4a98de4bdb9f6d2c3e9e1b3aed6c395b519cb813`  
		Last Modified: Tue, 10 Jun 2025 23:37:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:c70516dc7ac5d5ac16466ab4d2112b0ef68f64dd581f148913bc67245d34dc3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4169338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c41048a33369a9543660c0210cba330bf0973b092aaf7cb9d324d9c8c07c40d2`

```dockerfile
```

-	Layers:
	-	`sha256:59294ef9fa53e56a45c2badee7867b173babeb75717a858003040762f7d8ae11`  
		Last Modified: Wed, 11 Jun 2025 01:33:19 GMT  
		Size: 4.1 MB (4137557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2274988eb7c5e4108cbe94c99ed0b79b56ab4d321660f32aa86a44c5ba710a23`  
		Last Modified: Wed, 11 Jun 2025 01:33:20 GMT  
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
$ docker pull couchdb@sha256:b0346ec3bc28165f80378b038fd1a6d5ee446f0fcb44ca17b8d54fdc7b373c14
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
$ docker pull couchdb@sha256:af94c41e1a577f9f0368d93139035bc2fef98a8064a5fcfbe4467ce722b105aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156383379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:943ceeaa4bc9f025c27b5c65db56e2dd4a97990a9a1a30093a7fa558f5ca0784`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d44569cb297eb28d4ff419ad9edafca9a631b6918f51afc2645b27cf032824`  
		Last Modified: Tue, 10 Jun 2025 23:37:56 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90c842f875a09baf9748bdc12473aebbcd40a254d6f0337c8fff1133b62a20b`  
		Last Modified: Wed, 11 Jun 2025 05:34:18 GMT  
		Size: 7.9 MB (7876636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f90426813dc42a51ecf2f149ddbd49144780d12bda23a14121c3c32ecc78eb2`  
		Last Modified: Tue, 10 Jun 2025 23:38:03 GMT  
		Size: 77.3 MB (77324908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78240b230d48a51695db890d2d358d0746e87c52257befd5d2891d91134e9f16`  
		Last Modified: Tue, 10 Jun 2025 23:37:57 GMT  
		Size: 415.0 KB (414977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed75d6869dbcb6059987515c19bfe7f709e0e20006a5565253e863057ed99736`  
		Last Modified: Tue, 10 Jun 2025 23:37:57 GMT  
		Size: 99.3 KB (99295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d14d1d6a8d14b19e2ed9059a99e3dcb9519d61a0106c0b7f7d632c60a7120b4`  
		Last Modified: Tue, 10 Jun 2025 23:37:58 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c1e50a62cc24b3d3a3e976e91f990ee7797d4cbec71efc65eca0adbefcb8d2`  
		Last Modified: Tue, 10 Jun 2025 23:38:01 GMT  
		Size: 42.4 MB (42435562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6003201ca33590ce10fd133b9fbb92ae4a424f9666fb540020ebfa7fa345878`  
		Last Modified: Tue, 10 Jun 2025 23:37:58 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:bba6d09243f9a3b886ffe86c9132a4482c0ea0e36a446859c7e3539a9904031e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3678954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e560747821ef2c676675a73deae02f80298d8a978832a53e0bf42bde5fe46f9b`

```dockerfile
```

-	Layers:
	-	`sha256:ae305fdfb94dfc74f50d6b45b7dceac45970e747442b0a6ef57233136c19a66e`  
		Last Modified: Wed, 11 Jun 2025 01:33:25 GMT  
		Size: 3.7 MB (3654390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:068cf40840553703ce1ed297cd1f04c201c51dddd38ac095984a9d25cc1f0f5b`  
		Last Modified: Wed, 11 Jun 2025 01:33:26 GMT  
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
$ docker pull couchdb@sha256:30c14bf9d5d1a04c0b1b9ef0442131df69624f91221b0631ab6e75dd7f99fac5
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
$ docker pull couchdb@sha256:650816f7a1006f5a1b3e11a45c1cde40f3f5e8d2968e921268bc6ee7a14487ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139823939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4be8cafa64bcfa821cd43fd6b36081b3e21abc405d1e6ac268849176e379a85`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa98feb63093c87a2fbef9a528fcb0100e4b549abd70c810bb1d83a89d3a40c`  
		Last Modified: Tue, 10 Jun 2025 23:37:44 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6af541d5ad9b46b3581c08015d9efa0bb34ab7201c486654432b547404ad8d9`  
		Last Modified: Tue, 10 Jun 2025 23:37:45 GMT  
		Size: 7.9 MB (7876608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23529365cfa8356ef20af79faafbfcf4a227f69a5d0867f4b58541964362f97a`  
		Last Modified: Tue, 10 Jun 2025 23:37:45 GMT  
		Size: 392.1 KB (392136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff48d6b0776af8bf12a15456f0ef5366a1a0f61b8176573937877c841860d5f`  
		Last Modified: Tue, 10 Jun 2025 23:37:45 GMT  
		Size: 76.3 KB (76318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2e5aa79a5d0311974e5ab3be5f12cc7fc056c785fdcff6d72d4d510b6e2bfb`  
		Last Modified: Tue, 10 Jun 2025 23:37:45 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5079dacc7d9108ffae28bb29ab88aa2bd5c028ce94a7c922376e2c4b3c017e9f`  
		Last Modified: Tue, 10 Jun 2025 23:37:51 GMT  
		Size: 103.2 MB (103243324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5417499cb993cec049da7c7cd8770d9e713bf3c7ca693b370b296d8a872af00d`  
		Last Modified: Tue, 10 Jun 2025 23:37:45 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c12f91365777bfd974aebd2fe56e2f2673cf2f8116a672ef08c601bd36d432b`  
		Last Modified: Tue, 10 Jun 2025 23:37:46 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37db75e31662ccb5742ad5cdee2506b30a223880b937bea9ff4098adea32a207`  
		Last Modified: Tue, 10 Jun 2025 23:37:46 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d8afe72a86ea1a4a1d3bda4a98de4bdb9f6d2c3e9e1b3aed6c395b519cb813`  
		Last Modified: Tue, 10 Jun 2025 23:37:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0` - unknown; unknown

```console
$ docker pull couchdb@sha256:c70516dc7ac5d5ac16466ab4d2112b0ef68f64dd581f148913bc67245d34dc3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4169338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c41048a33369a9543660c0210cba330bf0973b092aaf7cb9d324d9c8c07c40d2`

```dockerfile
```

-	Layers:
	-	`sha256:59294ef9fa53e56a45c2badee7867b173babeb75717a858003040762f7d8ae11`  
		Last Modified: Wed, 11 Jun 2025 01:33:19 GMT  
		Size: 4.1 MB (4137557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2274988eb7c5e4108cbe94c99ed0b79b56ab4d321660f32aa86a44c5ba710a23`  
		Last Modified: Wed, 11 Jun 2025 01:33:20 GMT  
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
$ docker pull couchdb@sha256:b0346ec3bc28165f80378b038fd1a6d5ee446f0fcb44ca17b8d54fdc7b373c14
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
$ docker pull couchdb@sha256:af94c41e1a577f9f0368d93139035bc2fef98a8064a5fcfbe4467ce722b105aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156383379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:943ceeaa4bc9f025c27b5c65db56e2dd4a97990a9a1a30093a7fa558f5ca0784`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d44569cb297eb28d4ff419ad9edafca9a631b6918f51afc2645b27cf032824`  
		Last Modified: Tue, 10 Jun 2025 23:37:56 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90c842f875a09baf9748bdc12473aebbcd40a254d6f0337c8fff1133b62a20b`  
		Last Modified: Wed, 11 Jun 2025 05:34:18 GMT  
		Size: 7.9 MB (7876636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f90426813dc42a51ecf2f149ddbd49144780d12bda23a14121c3c32ecc78eb2`  
		Last Modified: Tue, 10 Jun 2025 23:38:03 GMT  
		Size: 77.3 MB (77324908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78240b230d48a51695db890d2d358d0746e87c52257befd5d2891d91134e9f16`  
		Last Modified: Tue, 10 Jun 2025 23:37:57 GMT  
		Size: 415.0 KB (414977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed75d6869dbcb6059987515c19bfe7f709e0e20006a5565253e863057ed99736`  
		Last Modified: Tue, 10 Jun 2025 23:37:57 GMT  
		Size: 99.3 KB (99295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d14d1d6a8d14b19e2ed9059a99e3dcb9519d61a0106c0b7f7d632c60a7120b4`  
		Last Modified: Tue, 10 Jun 2025 23:37:58 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c1e50a62cc24b3d3a3e976e91f990ee7797d4cbec71efc65eca0adbefcb8d2`  
		Last Modified: Tue, 10 Jun 2025 23:38:01 GMT  
		Size: 42.4 MB (42435562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6003201ca33590ce10fd133b9fbb92ae4a424f9666fb540020ebfa7fa345878`  
		Last Modified: Tue, 10 Jun 2025 23:37:58 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:bba6d09243f9a3b886ffe86c9132a4482c0ea0e36a446859c7e3539a9904031e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3678954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e560747821ef2c676675a73deae02f80298d8a978832a53e0bf42bde5fe46f9b`

```dockerfile
```

-	Layers:
	-	`sha256:ae305fdfb94dfc74f50d6b45b7dceac45970e747442b0a6ef57233136c19a66e`  
		Last Modified: Wed, 11 Jun 2025 01:33:25 GMT  
		Size: 3.7 MB (3654390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:068cf40840553703ce1ed297cd1f04c201c51dddd38ac095984a9d25cc1f0f5b`  
		Last Modified: Wed, 11 Jun 2025 01:33:26 GMT  
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
$ docker pull couchdb@sha256:30c14bf9d5d1a04c0b1b9ef0442131df69624f91221b0631ab6e75dd7f99fac5
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
$ docker pull couchdb@sha256:650816f7a1006f5a1b3e11a45c1cde40f3f5e8d2968e921268bc6ee7a14487ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139823939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4be8cafa64bcfa821cd43fd6b36081b3e21abc405d1e6ac268849176e379a85`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa98feb63093c87a2fbef9a528fcb0100e4b549abd70c810bb1d83a89d3a40c`  
		Last Modified: Tue, 10 Jun 2025 23:37:44 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6af541d5ad9b46b3581c08015d9efa0bb34ab7201c486654432b547404ad8d9`  
		Last Modified: Tue, 10 Jun 2025 23:37:45 GMT  
		Size: 7.9 MB (7876608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23529365cfa8356ef20af79faafbfcf4a227f69a5d0867f4b58541964362f97a`  
		Last Modified: Tue, 10 Jun 2025 23:37:45 GMT  
		Size: 392.1 KB (392136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff48d6b0776af8bf12a15456f0ef5366a1a0f61b8176573937877c841860d5f`  
		Last Modified: Tue, 10 Jun 2025 23:37:45 GMT  
		Size: 76.3 KB (76318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2e5aa79a5d0311974e5ab3be5f12cc7fc056c785fdcff6d72d4d510b6e2bfb`  
		Last Modified: Tue, 10 Jun 2025 23:37:45 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5079dacc7d9108ffae28bb29ab88aa2bd5c028ce94a7c922376e2c4b3c017e9f`  
		Last Modified: Tue, 10 Jun 2025 23:37:51 GMT  
		Size: 103.2 MB (103243324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5417499cb993cec049da7c7cd8770d9e713bf3c7ca693b370b296d8a872af00d`  
		Last Modified: Tue, 10 Jun 2025 23:37:45 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c12f91365777bfd974aebd2fe56e2f2673cf2f8116a672ef08c601bd36d432b`  
		Last Modified: Tue, 10 Jun 2025 23:37:46 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37db75e31662ccb5742ad5cdee2506b30a223880b937bea9ff4098adea32a207`  
		Last Modified: Tue, 10 Jun 2025 23:37:46 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d8afe72a86ea1a4a1d3bda4a98de4bdb9f6d2c3e9e1b3aed6c395b519cb813`  
		Last Modified: Tue, 10 Jun 2025 23:37:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:c70516dc7ac5d5ac16466ab4d2112b0ef68f64dd581f148913bc67245d34dc3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4169338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c41048a33369a9543660c0210cba330bf0973b092aaf7cb9d324d9c8c07c40d2`

```dockerfile
```

-	Layers:
	-	`sha256:59294ef9fa53e56a45c2badee7867b173babeb75717a858003040762f7d8ae11`  
		Last Modified: Wed, 11 Jun 2025 01:33:19 GMT  
		Size: 4.1 MB (4137557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2274988eb7c5e4108cbe94c99ed0b79b56ab4d321660f32aa86a44c5ba710a23`  
		Last Modified: Wed, 11 Jun 2025 01:33:20 GMT  
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
