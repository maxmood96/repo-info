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
-	[`couchdb:3.5.2`](#couchdb352)
-	[`couchdb:3.5.2-nouveau`](#couchdb352-nouveau)
-	[`couchdb:3.5.2.1`](#couchdb3521)
-	[`couchdb:3.5.2.1-nouveau`](#couchdb3521-nouveau)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:3`

```console
$ docker pull couchdb@sha256:db82596f7f5f5400071e66ece18d20d23329808df144fb399b7fb81e353e09db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:be60886dbb322f19a0971e6a9486470f5c084b01fdf949f5c0fe5fa001c73d85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148844645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df47e6b11fec6a9f139e0a4cd799195b9335a6ee66d0499f8832b259c565e1d7`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Tue, 23 Jun 2026 23:32:13 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 23 Jun 2026 23:32:13 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 23 Jun 2026 23:32:20 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 23 Jun 2026 23:32:23 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 23 Jun 2026 23:32:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:29 GMT
ENV COUCHDB_VERSION=3.5.2.1
# Tue, 23 Jun 2026 23:32:29 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 23 Jun 2026 23:32:42 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y couchdb="$COUCHDB_VERSION"~trixie ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 23 Jun 2026 23:32:42 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 23 Jun 2026 23:32:42 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 23 Jun 2026 23:32:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Jun 2026 23:32:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 23 Jun 2026 23:32:42 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 23 Jun 2026 23:32:42 GMT
VOLUME [/opt/couchdb/data]
# Tue, 23 Jun 2026 23:32:42 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 23 Jun 2026 23:32:42 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125d88fbb416bd132b2b8f3d3eabf258f48efefa96038c36085071bdd2af609c`  
		Last Modified: Tue, 23 Jun 2026 23:32:55 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d074679e62d672aee25403ccced7b29caa1896e83304bd63213e3a375113f046`  
		Last Modified: Tue, 23 Jun 2026 23:32:56 GMT  
		Size: 7.5 MB (7492092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6663734fecee46bd6dcb01731369c2ebf481c3a5936a080e1d8df3d4007f4d39`  
		Last Modified: Tue, 23 Jun 2026 23:32:56 GMT  
		Size: 417.6 KB (417587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67431044312ca3082fe7a2b3dc7bb930e80426deeebb680cf86e48e35fadcb2`  
		Last Modified: Tue, 23 Jun 2026 23:32:56 GMT  
		Size: 338.6 KB (338565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0d4985a9a56e5b22d40b28b97cdb659b734d2047b31e58acc76437eda7d3b2`  
		Last Modified: Tue, 23 Jun 2026 23:32:57 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700ec22e118fc20f9e3a895d0356c6328b522b0879d2e02346eac766ad384519`  
		Last Modified: Tue, 23 Jun 2026 23:33:00 GMT  
		Size: 110.8 MB (110805544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8bbde769c44cc9f31bce4fe5db619e92ee33d588bcdbd52e231e393a483a32`  
		Last Modified: Tue, 23 Jun 2026 23:32:57 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45cc4197154079e3f6baf01c4b8e9b1806fef3723f5e6c01b96c4457e045eb3`  
		Last Modified: Tue, 23 Jun 2026 23:32:58 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d2b70b4d764bf7f01f504f54aaf0184ddfaf16eb856b8ff054b3e19ca4616d`  
		Last Modified: Tue, 23 Jun 2026 23:32:58 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4342d5ebfbefc83074c8c48dcc48b04bb7b2beae212bab75ad0452728751d656`  
		Last Modified: Tue, 23 Jun 2026 23:32:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:cbadb92886e6ef4f494469f00d360b388f391a6869b1f65ec93fc4f7e1f3731e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffe06c4953ad56cbbde51d72829d9997a33ff4fa58467688ad34edfecc0e13c0`

```dockerfile
```

-	Layers:
	-	`sha256:2f0750e97f8e849e59fc02b42b2092399c35c47e3e9796b0726bc08271ea615f`  
		Last Modified: Tue, 23 Jun 2026 23:32:56 GMT  
		Size: 4.2 MB (4180389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c235be1ef4669946d2150eaf5111f1c1fde4bf3a55f8b20fabcf81011479953`  
		Last Modified: Tue, 23 Jun 2026 23:32:55 GMT  
		Size: 31.7 KB (31675 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:944dfe008f706100d9b057834e3b40c5458a8c6067128f0ad663d273150c3eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148610940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad95c003b35e7fe7956ebdfa924318bce0a6e1b5963594b06515e77c62742870`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Tue, 23 Jun 2026 23:32:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 23 Jun 2026 23:32:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 23 Jun 2026 23:32:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 23 Jun 2026 23:32:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 23 Jun 2026 23:32:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:51 GMT
ENV COUCHDB_VERSION=3.5.2.1
# Tue, 23 Jun 2026 23:32:51 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y couchdb="$COUCHDB_VERSION"~trixie ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 23 Jun 2026 23:33:23 GMT
VOLUME [/opt/couchdb/data]
# Tue, 23 Jun 2026 23:33:23 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 23 Jun 2026 23:33:23 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97325a7b140fe651aff8154d858a5a021c7b18c0b6aa682a107ba073a5ab4879`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f167452d2cba1aff408cd8774a342c06c7f6a04cc37baa0babef0c91a3f5625c`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 7.3 MB (7261105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ce20fd804da016a251954138074418b094a0dc4bcfc6ee19b8cd22088e4129`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 382.6 KB (382557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ad336cd92502642e2f46731304ff5129e7e079b418a0d2f9f8076af161f1a1`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 338.7 KB (338710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c13331aba23eb23da2064499c081c6c3a520fd7f7ffb5ddb550936bff241a9`  
		Last Modified: Tue, 23 Jun 2026 23:33:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa8af252651ec950c2e762b7b6be36b2607e24b082a1ea8eda27e848e4bf461`  
		Last Modified: Tue, 23 Jun 2026 23:33:41 GMT  
		Size: 110.5 MB (110474604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3ca67ecc05254da1956d0294bae75089e9baeaae4b55a4040cf2104523569e`  
		Last Modified: Tue, 23 Jun 2026 23:33:39 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc2ad2ae49d30c206b47a550edbfdb8f272d4655f1df57ff2a325879200801c`  
		Last Modified: Tue, 23 Jun 2026 23:33:39 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ba0691351b5030d43fcf1ba78d55b5379ab91823c2196eabf6e913e9730452`  
		Last Modified: Tue, 23 Jun 2026 23:33:40 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6ceb85a9d500a56bae2f07da226dcfe1b0205fa0376ee99bab8cc3d7dfa6da`  
		Last Modified: Tue, 23 Jun 2026 23:33:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:415c6f64ce0b44c20e9a1df07f92ca185b56638dacb503c74820fadf51f1fab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:420cd8298ed3cfb7b0358d7b5d372573c7432bb6ddc7e9e996a25dfd75e3df71`

```dockerfile
```

-	Layers:
	-	`sha256:772fe5e4c62244afd01871715e0219380812c7045c0eebdf7c9f304cd4cacc10`  
		Last Modified: Tue, 23 Jun 2026 23:33:38 GMT  
		Size: 4.2 MB (4180697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870cc7123fb12633ccff3283c814b3d934e261eb18435e57a2948acf80e2829c`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 31.9 KB (31882 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:3d5fa356d316c88e8faaa639748ad1a9cbeb9c120d2f09ff6b3957e489d465dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:cf845280d11988b085245878e553d805404e325e1e9eb3f506873611533c40db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150900728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35180336f9ee14b1127e7a59aa52e1682e5cf44a3ea32cbbc423fedc601c54da`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Tue, 23 Jun 2026 23:32:15 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 23 Jun 2026 23:32:15 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 23 Jun 2026 23:32:21 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:26 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-21-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 23 Jun 2026 23:32:29 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 23 Jun 2026 23:32:34 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:34 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ trixie main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 23 Jun 2026 23:32:39 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --no-install-recommends couchdb-nouveau=3.5.2.1~trixie;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 23 Jun 2026 23:32:39 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 23 Jun 2026 23:32:39 GMT
VOLUME [/opt/nouveau/data]
# Tue, 23 Jun 2026 23:32:39 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 23 Jun 2026 23:32:39 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc1f003886a886b79e960038e80e6cb7fadff93ce1dfb08bc9528a6eca1be2e`  
		Last Modified: Tue, 23 Jun 2026 23:32:54 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a65cb72c4048e85e128ff5506d06591b6600c65429c4e3e2ed6cd1f16d31e90`  
		Last Modified: Tue, 23 Jun 2026 23:32:54 GMT  
		Size: 7.5 MB (7492030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2edbbc7d3d01fa0668be25cbc1bdae07f69ec42a68589679149cbfef4114d7`  
		Last Modified: Tue, 23 Jun 2026 23:32:56 GMT  
		Size: 70.0 MB (70032437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a376a3d0804c72aa79e235daa49be253a66a6d2be1dd7a6c17f00b1843582df5`  
		Last Modified: Tue, 23 Jun 2026 23:32:54 GMT  
		Size: 425.9 KB (425936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc013a92d1d24936f3851f3d5f42547202dad3cf95123c80ffe9276fa2fa88bc`  
		Last Modified: Tue, 23 Jun 2026 23:32:55 GMT  
		Size: 347.4 KB (347354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28709f3155cca3bf22e74af624cb00bd6eb7856690cdc32ba7b84b9649cadf82`  
		Last Modified: Tue, 23 Jun 2026 23:32:55 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ec7befc43ef270f329bc2a51d1e21683d75fd4210b560dc13d7d7883317ab4`  
		Last Modified: Tue, 23 Jun 2026 23:32:57 GMT  
		Size: 42.8 MB (42815675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd7a66cac537898204ca6f30745053c2edb2fbd1c788cffba36b61aadea9c82`  
		Last Modified: Tue, 23 Jun 2026 23:32:56 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:eecd9a40c14c87ecf57b4fa84a535f0b459c5092e9d984e26f2a2c33129ef74c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3389170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3794e3be70f8b586c99be65ba27c3da261be1ef2e951c1de4dfdedcd426d6d`

```dockerfile
```

-	Layers:
	-	`sha256:8b2b6bebeec38a0f7608c5c5c0cbda80eb6a973d1814cf1472a5f771b1b941d1`  
		Last Modified: Tue, 23 Jun 2026 23:32:54 GMT  
		Size: 3.4 MB (3364655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e995bd20f5e9575f68aa587c9946db0a390fd93bf1e6e3aa382e17168ea1bd7f`  
		Last Modified: Tue, 23 Jun 2026 23:32:54 GMT  
		Size: 24.5 KB (24515 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:b58614245c5f6861f59c37c7370a9be54fc61087a96a9ffb9f2b712a273da2f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150060763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:410645668157d46958b1415602b102a7ab2a5128ec41b8b426df94922d5dcb93`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Tue, 23 Jun 2026 23:32:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 23 Jun 2026 23:32:40 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 23 Jun 2026 23:32:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-21-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 23 Jun 2026 23:32:56 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 23 Jun 2026 23:33:02 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:33:02 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ trixie main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 23 Jun 2026 23:33:15 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --no-install-recommends couchdb-nouveau=3.5.2.1~trixie;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 23 Jun 2026 23:33:15 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 23 Jun 2026 23:33:15 GMT
VOLUME [/opt/nouveau/data]
# Tue, 23 Jun 2026 23:33:15 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 23 Jun 2026 23:33:15 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5313ce6db74f98627afe0c7e4d43f8b57a0ad77d4d3184ea9e0d01253abd33c8`  
		Last Modified: Tue, 23 Jun 2026 23:33:30 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40836ca234bd40b8c4295cd5a94a7f4a82f682c8f33844bae255d7a478d7dc4a`  
		Last Modified: Tue, 23 Jun 2026 23:33:31 GMT  
		Size: 7.3 MB (7261179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a9848ec6c2ee307d8714baeec49e7bf5425762816245c9b0fb5f279c422a3f`  
		Last Modified: Tue, 23 Jun 2026 23:33:32 GMT  
		Size: 69.2 MB (69179730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7010cf1c1c6d1a1900757033c5552425409fc6a2ca148b95da9821808d0c7b`  
		Last Modified: Tue, 23 Jun 2026 23:33:30 GMT  
		Size: 390.2 KB (390249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce482bfa8391c85475e9b9f5c31fc168fc5ed90ad518340b7f4d25f8d6fec8b2`  
		Last Modified: Tue, 23 Jun 2026 23:33:31 GMT  
		Size: 347.4 KB (347418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8dc170d66d6619a3baeb573638bde792eb024ff90158a35042dfe10130708ef`  
		Last Modified: Tue, 23 Jun 2026 23:33:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fcb5ef627136ba3bcfdfeb04eaf3befa8df1179de18c09851623e49eb1ee6ca`  
		Last Modified: Tue, 23 Jun 2026 23:33:33 GMT  
		Size: 42.7 MB (42731780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e19d0ccfba4ad18823eb374f84b7eda28d7d3febcf012f3d0a055e344190e2e`  
		Last Modified: Tue, 23 Jun 2026 23:33:33 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:1a3070bb6674fbd4130b503a1ea4f1b33ef83e3c1f047f52e375976113bd771b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3388017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a85de82f4abfe2b8fb1830a1dff75fcf62b7badf54c28672ddef151f1f9922ea`

```dockerfile
```

-	Layers:
	-	`sha256:7b7e3cf0d0456eb003b663814fc3d531897a1574d956b425fa5151d48d39b3aa`  
		Last Modified: Tue, 23 Jun 2026 23:33:30 GMT  
		Size: 3.4 MB (3363308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b577a1dc55bd252562e26292b066fa2b53cfbb445788988c8f0fdba069317ce`  
		Last Modified: Tue, 23 Jun 2026 23:33:30 GMT  
		Size: 24.7 KB (24709 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4`

```console
$ docker pull couchdb@sha256:af9d39a66d53cbf1cfe53ff20fb093e426f7c09a90d15585e13b028d490a7f08
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
$ docker pull couchdb@sha256:7ad0813282bfff43d752399d579eaa2f177cbd5a56eb1f6e065616068c6ee8a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139025638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fce1b26668bcfb01a4fbe888bb8cfb87c997c389ac6a7d23077c9de1a169522`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:43:02 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jun 2026 00:43:02 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Thu, 11 Jun 2026 00:43:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:43:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Thu, 11 Jun 2026 00:43:10 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jun 2026 00:43:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:43:15 GMT
ENV COUCHDB_VERSION=3.4.3
# Thu, 11 Jun 2026 00:43:15 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Thu, 11 Jun 2026 00:43:28 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 11 Jun 2026 00:43:28 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Thu, 11 Jun 2026 00:43:28 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Thu, 11 Jun 2026 00:43:28 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 11 Jun 2026 00:43:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:43:28 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:43:28 GMT
VOLUME [/opt/couchdb/data]
# Thu, 11 Jun 2026 00:43:28 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Thu, 11 Jun 2026 00:43:28 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34a0275fad5b2e7f49d1894fb5f1026b3b31b97929de2d013b119dca6cb462a`  
		Last Modified: Thu, 11 Jun 2026 00:43:41 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3733f903902830325b46abc774ae0d9bcb1908d30ac1575c7480026c780f50`  
		Last Modified: Thu, 11 Jun 2026 00:43:42 GMT  
		Size: 7.9 MB (7884340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe6800d9a14d0974a5fd6c1aae0ae2c6b8467591def6a698bf309fd74c8a500`  
		Last Modified: Thu, 11 Jun 2026 00:43:42 GMT  
		Size: 401.8 KB (401782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab1a15f499321e3f2e0dd95343938831b8da745a8edc1421f56c1f287578157`  
		Last Modified: Thu, 11 Jun 2026 00:43:42 GMT  
		Size: 76.5 KB (76514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a420a9be7bf7491b147f477830d50ee6469d2715d2b4cf395389ed37b91f584`  
		Last Modified: Thu, 11 Jun 2026 00:43:43 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7825bc62808ff0bf76ca60dd86e60b5c30b74cb6e2a3479740dc11aefc5de2ea`  
		Last Modified: Thu, 11 Jun 2026 00:43:46 GMT  
		Size: 102.4 MB (102419947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad63740a525d364b0fd6ccb41e364b3a59ed9e6a3d815937d0c879cbc78e7830`  
		Last Modified: Thu, 11 Jun 2026 00:43:43 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d130a03529fcfbabf52984c04b64c0c422018d468037db30813f951e5c1e6d4`  
		Last Modified: Thu, 11 Jun 2026 00:43:43 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d6205c0c97278579454c7a428016fe25519757283975ea4ffc0b920b9fc953`  
		Last Modified: Thu, 11 Jun 2026 00:43:44 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed666a0774bd5bd363c91d41a8e84e4460d801515ae9f222e97d1e71c511d801`  
		Last Modified: Thu, 11 Jun 2026 00:43:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:cc68fc0d6d4d5d6db9b977548951b44685c36809a53b803289a1699cd3782a59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e27689688f220cb2f83268b0c7697768e1b8ef85441b39f341a6e1b1df3c6a`

```dockerfile
```

-	Layers:
	-	`sha256:e5eacdde0ed46cee0e1aaa84fd239df276e07d6e0acb55d784a2d5aae67500e1`  
		Last Modified: Thu, 11 Jun 2026 00:43:42 GMT  
		Size: 4.1 MB (4125431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5a1a13b96bf9a8c7a96928541615fd615d87626b82b4441840be2972ee4b27c`  
		Last Modified: Thu, 11 Jun 2026 00:43:41 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:049514162c51d11865cdc310c1769749a2275331bd02a0a0138c40bf3464af1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138439846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69255e01667ccabe19378b986197d6dc9d240fb231608608f1b38cd0cdcc9a73`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:44:46 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jun 2026 00:44:46 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Thu, 11 Jun 2026 00:44:52 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:44:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Thu, 11 Jun 2026 00:44:55 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jun 2026 00:44:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:44:59 GMT
ENV COUCHDB_VERSION=3.4.3
# Thu, 11 Jun 2026 00:45:00 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Thu, 11 Jun 2026 00:45:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 11 Jun 2026 00:45:12 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Thu, 11 Jun 2026 00:45:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Thu, 11 Jun 2026 00:45:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 11 Jun 2026 00:45:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:45:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:45:12 GMT
VOLUME [/opt/couchdb/data]
# Thu, 11 Jun 2026 00:45:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Thu, 11 Jun 2026 00:45:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08aee71e24adb5275604b9f50abc13d3f67677bc222d3395a0c0076e081d0e5a`  
		Last Modified: Thu, 11 Jun 2026 00:45:24 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9832854a56a6d76b1da37f382b69d09edad10c4539bdb32ba1f61e5259190d3`  
		Last Modified: Thu, 11 Jun 2026 00:45:25 GMT  
		Size: 7.7 MB (7695522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a66c66cfafaa1a452b9c6a9c9b4e8eb3a4dfcef9fb0ecbb19fb9a4206098c23`  
		Last Modified: Thu, 11 Jun 2026 00:45:24 GMT  
		Size: 370.5 KB (370546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd35905aad39aac2dcbf4da522f1846f833ee3af602e3b2bb585cbab1403494b`  
		Last Modified: Thu, 11 Jun 2026 00:45:24 GMT  
		Size: 76.5 KB (76507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5782207841376aee6faa094eb6d431b354b3a3b44150c609ccc2a85e606745be`  
		Last Modified: Thu, 11 Jun 2026 00:45:26 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc146342ab1f431d43e62af84fbb85b14c31929d61e0e4b50f7fcc425fe53c32`  
		Last Modified: Thu, 11 Jun 2026 00:45:29 GMT  
		Size: 102.2 MB (102169527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4b23147c3ec7f86e6ba9007751db3411c36cfdf3154c36e653e01e79f98d5a`  
		Last Modified: Thu, 11 Jun 2026 00:45:26 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ccb8a8e416945485ebb66919e88f61d697b750c824d9c860accadffb860e32`  
		Last Modified: Thu, 11 Jun 2026 00:45:26 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efead0bbb4af60da230f69031439e25fe81305c4e370cfad8e2052964d2dd3f`  
		Last Modified: Thu, 11 Jun 2026 00:45:27 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e44c90c7482adff76124a2a002a12cda9e73d17e0ab2c074e140e2b8a9c783`  
		Last Modified: Thu, 11 Jun 2026 00:45:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:2f801e4f0f7ff763e2259f5faed3ef8c965467194047b3be1317646b09472510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4157017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0bb7b0366e3c8eb790d70be9320cdfd0ec30f6e3bb1ce8742fd0baff8e66201`

```dockerfile
```

-	Layers:
	-	`sha256:efc6e4277213e5a7af3497f65f3f5c1ee886776e2e0b6a0bc45a6edcaf3ff605`  
		Last Modified: Thu, 11 Jun 2026 00:45:25 GMT  
		Size: 4.1 MB (4125700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7040609ff024b230a9cbe93499304aca43746c882934eb0094c4517dc58b1c9`  
		Last Modified: Thu, 11 Jun 2026 00:45:24 GMT  
		Size: 31.3 KB (31317 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; s390x

```console
$ docker pull couchdb@sha256:1371ccf96d064deb202eb7007f60767a936d3f9261b57d5d3b7957dbe0170076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135804454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae9ba37196ac8d1f4ca59dd6b453ccad444dcdef0df7550fc007615d85692e39`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:44:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jun 2026 01:44:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Thu, 11 Jun 2026 01:44:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:44:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Thu, 11 Jun 2026 01:44:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jun 2026 01:44:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:44:50 GMT
ENV COUCHDB_VERSION=3.4.3
# Thu, 11 Jun 2026 01:44:50 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Thu, 11 Jun 2026 01:45:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 11 Jun 2026 01:45:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Thu, 11 Jun 2026 01:45:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Thu, 11 Jun 2026 01:45:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 11 Jun 2026 01:45:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 01:45:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 01:45:05 GMT
VOLUME [/opt/couchdb/data]
# Thu, 11 Jun 2026 01:45:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Thu, 11 Jun 2026 01:45:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5f5cf8ed0a968e830e44f74f3f92eafe3be66d07ac4fee39b40ffcbe40e9ba`  
		Last Modified: Thu, 11 Jun 2026 01:45:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06b734ad2ca75e58b97b0905894fad5a05612bac9d58df146f4cfc7a34e3c69`  
		Last Modified: Thu, 11 Jun 2026 01:45:26 GMT  
		Size: 7.4 MB (7400233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f33679d10a6a3da802174cf113fe9a18201c399d2df1acedb48d3e15cc87eea`  
		Last Modified: Thu, 11 Jun 2026 01:45:25 GMT  
		Size: 372.2 KB (372190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f0a85e866c372a63d32cc9b04a3f1391d130a1a14ab63b23d19626d103f9bc`  
		Last Modified: Thu, 11 Jun 2026 01:45:25 GMT  
		Size: 76.5 KB (76543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1624ba1089fe474ab711259a9c638d5f2a35509c8fcaa0f3d6c1c7024a982d78`  
		Last Modified: Thu, 11 Jun 2026 01:45:27 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb6aed714ef171dfdc763c826d68e4961771927cf962f9c2958c51ac318121d`  
		Last Modified: Thu, 11 Jun 2026 01:45:29 GMT  
		Size: 101.1 MB (101056549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613051bab9b42ff0c6bdd0f982da5ad98b42863e425280a705a0af33a324b97c`  
		Last Modified: Thu, 11 Jun 2026 01:45:26 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5c03f4258a77892f6e2c31383e5ef571e56badceb291b4f151605cb4ae19c2`  
		Last Modified: Thu, 11 Jun 2026 01:45:27 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71d7d3e376d998fe98fc505bafc56a8f7211cd2be27593d158e4dd6fb240f47`  
		Last Modified: Thu, 11 Jun 2026 01:45:27 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89ecd3b42a4079bb33a718d8e8788a7ee37704dcec36448fc8b01dced722ff6`  
		Last Modified: Thu, 11 Jun 2026 01:45:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:ecdfaa5f3fe49f293f7a222a62d39959074cf6c83a7b1ddc3fd69357705f07d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ddd0b327eef7425ce79cfe4a657585a1c29161d647422ca0f78e5bdb12a698e`

```dockerfile
```

-	Layers:
	-	`sha256:72512a5c4b0363c040b9c43c543b783a15f9eae58d749d4d03f3606ef2f71a3b`  
		Last Modified: Thu, 11 Jun 2026 01:45:25 GMT  
		Size: 4.1 MB (4121627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c3bdff540d67a7087f41bacf4cc6191acc855eba2b974f92cb60a4129d3518d`  
		Last Modified: Thu, 11 Jun 2026 01:45:25 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4-nouveau`

```console
$ docker pull couchdb@sha256:25d1e0ccaabf1526890afa5082f1e24536579bd20feb5085266e38d8d2aedc7e
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
$ docker pull couchdb@sha256:46efa75e43e50cf8e3b32ab45997022e3f2a4862aff284b2135756b31bd103a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.6 MB (156561571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf3976ecfff0e9d68edd0b2dbbf6d3163f681c8ca3ad65c7945b65242babf1e2`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:43:06 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jun 2026 00:43:06 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Thu, 11 Jun 2026 00:43:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:43:22 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:43:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Thu, 11 Jun 2026 00:43:25 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jun 2026 00:43:30 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:43:30 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Thu, 11 Jun 2026 00:43:36 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Thu, 11 Jun 2026 00:43:36 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Thu, 11 Jun 2026 00:43:36 GMT
VOLUME [/opt/nouveau/data]
# Thu, 11 Jun 2026 00:43:36 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Thu, 11 Jun 2026 00:43:36 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8c6ebb2e85d5d0dca4b7eee74b4bb13d0a47f94488cabcb97682347f64f8a0`  
		Last Modified: Thu, 11 Jun 2026 00:43:51 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea5a2cae3a8725077de4aacc3c054747ce8d030d202c9017db9c1ccefe48e7f`  
		Last Modified: Thu, 11 Jun 2026 00:43:51 GMT  
		Size: 7.9 MB (7884346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eee0af3073fb579cd0ea4d27bc47f95fa4b20a8e0be665cf4eec74bf1a001cf`  
		Last Modified: Thu, 11 Jun 2026 00:43:53 GMT  
		Size: 77.5 MB (77478120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df80a1ba0ce0ac2a64573925cd2acae4b4ceebbc0fded8ba492d895d842ff49e`  
		Last Modified: Thu, 11 Jun 2026 00:43:51 GMT  
		Size: 424.2 KB (424159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8540a7a0af2ae69eb99a41b3214f87bc963eae9379559145eb6274f3518856da`  
		Last Modified: Thu, 11 Jun 2026 00:43:52 GMT  
		Size: 99.6 KB (99627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4fd65d8fc0ba13c33a9570ae4831fe8936912f02697195f7ba583b4b28d8dc`  
		Last Modified: Thu, 11 Jun 2026 00:43:52 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f1af6ab22429caa7ee66a32034aea07527423cd20f60e554c9d18529dba2e9`  
		Last Modified: Thu, 11 Jun 2026 00:43:54 GMT  
		Size: 42.4 MB (42435815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38ba33c68199233a1ff1058b3be662e9acf138988b7121e0b03ef6266a06069`  
		Last Modified: Thu, 11 Jun 2026 00:43:53 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:c10ce3a0b0bc97812564f6d8fe0dc37ba7392fd91f5ce538864c59df0686890c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e96ecb2455c4404855bfdddc341f755ee37ab3ac12ff05c8f425775aad2dd6c`

```dockerfile
```

-	Layers:
	-	`sha256:7d91b213225d770abc4651cae2cb12fc8a991ec1ea4ac5531320e34c74a76b59`  
		Last Modified: Thu, 11 Jun 2026 00:43:51 GMT  
		Size: 3.7 MB (3658671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0978a1da9ffddd8fa55c876ab7898321807e1d62cb09a0d725748b10881aef98`  
		Last Modified: Thu, 11 Jun 2026 00:43:51 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:0a5996ce00cdec6425d2b154a0b3363a9aa54d9967c62aed814ec263ea4548d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155443294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ff954b6eb81e7184f39bf7b459ec6109e450b138ef955c997c0508f0f11656`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:44:53 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jun 2026 00:44:53 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Thu, 11 Jun 2026 00:44:58 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:06 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Thu, 11 Jun 2026 00:45:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jun 2026 00:45:12 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:12 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Thu, 11 Jun 2026 00:45:17 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Thu, 11 Jun 2026 00:45:17 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Thu, 11 Jun 2026 00:45:17 GMT
VOLUME [/opt/nouveau/data]
# Thu, 11 Jun 2026 00:45:17 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Thu, 11 Jun 2026 00:45:17 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad224af02a5321b3eb29482ae705ae0f1e6544a563c86c09116caa3e8de361b5`  
		Last Modified: Thu, 11 Jun 2026 00:45:32 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6841905915492705f7458eb369dfce8ab834bf46a1423f78939762c62141d594`  
		Last Modified: Thu, 11 Jun 2026 00:45:33 GMT  
		Size: 7.7 MB (7695462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d263ded6b9aebd1331abaf55b3c7fe3f4f129ebcdc161ffd0566ce20b41c3b26`  
		Last Modified: Thu, 11 Jun 2026 00:45:35 GMT  
		Size: 76.8 MB (76793345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13bd7bb1465de6505ba9a4f4352aebec9172629dd2281cc3a8ee824808364665`  
		Last Modified: Thu, 11 Jun 2026 00:45:32 GMT  
		Size: 392.8 KB (392802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635bdeee11d0d90063c9252f316bc0d4b33c5b9c2c3693d696ff99341751d501`  
		Last Modified: Thu, 11 Jun 2026 00:45:34 GMT  
		Size: 99.5 KB (99545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86cafb0efd9657ed3a9a81947f88bbeb6f1d21c62a247b3407f08c1a40b4e66`  
		Last Modified: Thu, 11 Jun 2026 00:45:34 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0407a0241520f6ad2cc044f1f1c3336e3afcb74cd1d18eae6e93e6bc21e5ac19`  
		Last Modified: Thu, 11 Jun 2026 00:45:35 GMT  
		Size: 42.3 MB (42337953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cbf3cb3452afa3a7f5e686c07bc4eca25aeeec96425337ff7e80bffbb976e3`  
		Last Modified: Thu, 11 Jun 2026 00:45:35 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:ce501070e9e01b977a9af7464dbc4cfc820556d36a7ea1b745a5a504748fd4f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c263201881589b1be3f9766ab240d76bf68f4f466caacb01ec9b6f31624420b`

```dockerfile
```

-	Layers:
	-	`sha256:9f0ff81bd1d2e8b87d77163b3cb04e4df47839789155190b480f8c03dffceb8a`  
		Last Modified: Thu, 11 Jun 2026 00:45:33 GMT  
		Size: 3.7 MB (3657339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95da38822ce4f7bd93a39d0a00d7e28af1c721db9a7bdcf0c3f06c46709d32e9`  
		Last Modified: Thu, 11 Jun 2026 00:45:32 GMT  
		Size: 24.4 KB (24385 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:5f01d1a396975fcb18e6d7b8e26b000a53da4b967282c49d9986560c903e3ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.2 MB (150178271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06bdc4f5885ab1f5195cf05bb7699c173ff309b5505670b31b87edd2435ca706`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:44:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jun 2026 01:44:35 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Thu, 11 Jun 2026 01:44:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:44:52 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:44:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Thu, 11 Jun 2026 01:44:55 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jun 2026 01:44:59 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:44:59 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Thu, 11 Jun 2026 01:45:06 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Thu, 11 Jun 2026 01:45:06 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Thu, 11 Jun 2026 01:45:06 GMT
VOLUME [/opt/nouveau/data]
# Thu, 11 Jun 2026 01:45:06 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Thu, 11 Jun 2026 01:45:06 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84bc8db000f588b08571788f3f12d69b76501e751a18c6c2755f82a5fe68f588`  
		Last Modified: Thu, 11 Jun 2026 01:45:29 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37bdc5e8b6e872f0c6c1651d480846683e3daa9959e65e4c1a81cd1d713488e1`  
		Last Modified: Thu, 11 Jun 2026 01:45:30 GMT  
		Size: 7.4 MB (7400235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c60ab7447cd65e5c548b8f4f4cd81886409007edba6aac5bc31cd0f91b6e43`  
		Last Modified: Thu, 11 Jun 2026 01:45:32 GMT  
		Size: 73.2 MB (73225561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c4f8e7df6d45d1588bc1849c9dbe149afbea03758a816b47f44ce96b9f037d`  
		Last Modified: Thu, 11 Jun 2026 01:45:29 GMT  
		Size: 394.5 KB (394514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637ab811bb523af983dfa04da05bf838b461a604ad8c862f2dca46b72eaf61e2`  
		Last Modified: Thu, 11 Jun 2026 01:45:30 GMT  
		Size: 99.7 KB (99695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0333935d5ea23bb8735d411badac6860e225714d8fbce0b14c8909c0b821dde7`  
		Last Modified: Thu, 11 Jun 2026 01:45:31 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c87a6d8d98620e6b24c320b1b31ab7ccc4d890630b9c7eb4d94258eeaf9c9ba`  
		Last Modified: Thu, 11 Jun 2026 01:45:32 GMT  
		Size: 42.2 MB (42162881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8e4f15690348463aade48dfb64010bcca002efa6eaa56f4014a5337ef4da3c`  
		Last Modified: Thu, 11 Jun 2026 01:45:32 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:456173ecd6df5e2b420778241a563d4bd356d41119956c6ba28d3702bd2c9967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ae6a15d0ede23071584a7d66158f5c8422baeab63263f9a8f9debeab0a7a5b`

```dockerfile
```

-	Layers:
	-	`sha256:a759e5be1a235919d1bbd15627f56243ab5ead1c3311b3d2de8d177b1771652b`  
		Last Modified: Thu, 11 Jun 2026 01:45:30 GMT  
		Size: 3.6 MB (3649204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b8d9c2eea136d57e500d41d66d7816254c7b80990aea81ed21474f79193b24c`  
		Last Modified: Thu, 11 Jun 2026 01:45:29 GMT  
		Size: 24.2 KB (24214 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3`

```console
$ docker pull couchdb@sha256:af9d39a66d53cbf1cfe53ff20fb093e426f7c09a90d15585e13b028d490a7f08
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
$ docker pull couchdb@sha256:7ad0813282bfff43d752399d579eaa2f177cbd5a56eb1f6e065616068c6ee8a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139025638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fce1b26668bcfb01a4fbe888bb8cfb87c997c389ac6a7d23077c9de1a169522`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:43:02 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jun 2026 00:43:02 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Thu, 11 Jun 2026 00:43:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:43:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Thu, 11 Jun 2026 00:43:10 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jun 2026 00:43:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:43:15 GMT
ENV COUCHDB_VERSION=3.4.3
# Thu, 11 Jun 2026 00:43:15 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Thu, 11 Jun 2026 00:43:28 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 11 Jun 2026 00:43:28 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Thu, 11 Jun 2026 00:43:28 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Thu, 11 Jun 2026 00:43:28 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 11 Jun 2026 00:43:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:43:28 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:43:28 GMT
VOLUME [/opt/couchdb/data]
# Thu, 11 Jun 2026 00:43:28 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Thu, 11 Jun 2026 00:43:28 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34a0275fad5b2e7f49d1894fb5f1026b3b31b97929de2d013b119dca6cb462a`  
		Last Modified: Thu, 11 Jun 2026 00:43:41 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3733f903902830325b46abc774ae0d9bcb1908d30ac1575c7480026c780f50`  
		Last Modified: Thu, 11 Jun 2026 00:43:42 GMT  
		Size: 7.9 MB (7884340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe6800d9a14d0974a5fd6c1aae0ae2c6b8467591def6a698bf309fd74c8a500`  
		Last Modified: Thu, 11 Jun 2026 00:43:42 GMT  
		Size: 401.8 KB (401782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab1a15f499321e3f2e0dd95343938831b8da745a8edc1421f56c1f287578157`  
		Last Modified: Thu, 11 Jun 2026 00:43:42 GMT  
		Size: 76.5 KB (76514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a420a9be7bf7491b147f477830d50ee6469d2715d2b4cf395389ed37b91f584`  
		Last Modified: Thu, 11 Jun 2026 00:43:43 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7825bc62808ff0bf76ca60dd86e60b5c30b74cb6e2a3479740dc11aefc5de2ea`  
		Last Modified: Thu, 11 Jun 2026 00:43:46 GMT  
		Size: 102.4 MB (102419947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad63740a525d364b0fd6ccb41e364b3a59ed9e6a3d815937d0c879cbc78e7830`  
		Last Modified: Thu, 11 Jun 2026 00:43:43 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d130a03529fcfbabf52984c04b64c0c422018d468037db30813f951e5c1e6d4`  
		Last Modified: Thu, 11 Jun 2026 00:43:43 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d6205c0c97278579454c7a428016fe25519757283975ea4ffc0b920b9fc953`  
		Last Modified: Thu, 11 Jun 2026 00:43:44 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed666a0774bd5bd363c91d41a8e84e4460d801515ae9f222e97d1e71c511d801`  
		Last Modified: Thu, 11 Jun 2026 00:43:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:cc68fc0d6d4d5d6db9b977548951b44685c36809a53b803289a1699cd3782a59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e27689688f220cb2f83268b0c7697768e1b8ef85441b39f341a6e1b1df3c6a`

```dockerfile
```

-	Layers:
	-	`sha256:e5eacdde0ed46cee0e1aaa84fd239df276e07d6e0acb55d784a2d5aae67500e1`  
		Last Modified: Thu, 11 Jun 2026 00:43:42 GMT  
		Size: 4.1 MB (4125431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5a1a13b96bf9a8c7a96928541615fd615d87626b82b4441840be2972ee4b27c`  
		Last Modified: Thu, 11 Jun 2026 00:43:41 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:049514162c51d11865cdc310c1769749a2275331bd02a0a0138c40bf3464af1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138439846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69255e01667ccabe19378b986197d6dc9d240fb231608608f1b38cd0cdcc9a73`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:44:46 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jun 2026 00:44:46 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Thu, 11 Jun 2026 00:44:52 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:44:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Thu, 11 Jun 2026 00:44:55 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jun 2026 00:44:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:44:59 GMT
ENV COUCHDB_VERSION=3.4.3
# Thu, 11 Jun 2026 00:45:00 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Thu, 11 Jun 2026 00:45:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 11 Jun 2026 00:45:12 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Thu, 11 Jun 2026 00:45:12 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Thu, 11 Jun 2026 00:45:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 11 Jun 2026 00:45:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:45:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:45:12 GMT
VOLUME [/opt/couchdb/data]
# Thu, 11 Jun 2026 00:45:12 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Thu, 11 Jun 2026 00:45:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08aee71e24adb5275604b9f50abc13d3f67677bc222d3395a0c0076e081d0e5a`  
		Last Modified: Thu, 11 Jun 2026 00:45:24 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9832854a56a6d76b1da37f382b69d09edad10c4539bdb32ba1f61e5259190d3`  
		Last Modified: Thu, 11 Jun 2026 00:45:25 GMT  
		Size: 7.7 MB (7695522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a66c66cfafaa1a452b9c6a9c9b4e8eb3a4dfcef9fb0ecbb19fb9a4206098c23`  
		Last Modified: Thu, 11 Jun 2026 00:45:24 GMT  
		Size: 370.5 KB (370546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd35905aad39aac2dcbf4da522f1846f833ee3af602e3b2bb585cbab1403494b`  
		Last Modified: Thu, 11 Jun 2026 00:45:24 GMT  
		Size: 76.5 KB (76507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5782207841376aee6faa094eb6d431b354b3a3b44150c609ccc2a85e606745be`  
		Last Modified: Thu, 11 Jun 2026 00:45:26 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc146342ab1f431d43e62af84fbb85b14c31929d61e0e4b50f7fcc425fe53c32`  
		Last Modified: Thu, 11 Jun 2026 00:45:29 GMT  
		Size: 102.2 MB (102169527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4b23147c3ec7f86e6ba9007751db3411c36cfdf3154c36e653e01e79f98d5a`  
		Last Modified: Thu, 11 Jun 2026 00:45:26 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ccb8a8e416945485ebb66919e88f61d697b750c824d9c860accadffb860e32`  
		Last Modified: Thu, 11 Jun 2026 00:45:26 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efead0bbb4af60da230f69031439e25fe81305c4e370cfad8e2052964d2dd3f`  
		Last Modified: Thu, 11 Jun 2026 00:45:27 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e44c90c7482adff76124a2a002a12cda9e73d17e0ab2c074e140e2b8a9c783`  
		Last Modified: Thu, 11 Jun 2026 00:45:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:2f801e4f0f7ff763e2259f5faed3ef8c965467194047b3be1317646b09472510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4157017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0bb7b0366e3c8eb790d70be9320cdfd0ec30f6e3bb1ce8742fd0baff8e66201`

```dockerfile
```

-	Layers:
	-	`sha256:efc6e4277213e5a7af3497f65f3f5c1ee886776e2e0b6a0bc45a6edcaf3ff605`  
		Last Modified: Thu, 11 Jun 2026 00:45:25 GMT  
		Size: 4.1 MB (4125700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7040609ff024b230a9cbe93499304aca43746c882934eb0094c4517dc58b1c9`  
		Last Modified: Thu, 11 Jun 2026 00:45:24 GMT  
		Size: 31.3 KB (31317 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3` - linux; s390x

```console
$ docker pull couchdb@sha256:1371ccf96d064deb202eb7007f60767a936d3f9261b57d5d3b7957dbe0170076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135804454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae9ba37196ac8d1f4ca59dd6b453ccad444dcdef0df7550fc007615d85692e39`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:44:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jun 2026 01:44:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Thu, 11 Jun 2026 01:44:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:44:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Thu, 11 Jun 2026 01:44:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jun 2026 01:44:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:44:50 GMT
ENV COUCHDB_VERSION=3.4.3
# Thu, 11 Jun 2026 01:44:50 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Thu, 11 Jun 2026 01:45:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 11 Jun 2026 01:45:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Thu, 11 Jun 2026 01:45:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Thu, 11 Jun 2026 01:45:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 11 Jun 2026 01:45:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 01:45:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 01:45:05 GMT
VOLUME [/opt/couchdb/data]
# Thu, 11 Jun 2026 01:45:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Thu, 11 Jun 2026 01:45:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5f5cf8ed0a968e830e44f74f3f92eafe3be66d07ac4fee39b40ffcbe40e9ba`  
		Last Modified: Thu, 11 Jun 2026 01:45:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06b734ad2ca75e58b97b0905894fad5a05612bac9d58df146f4cfc7a34e3c69`  
		Last Modified: Thu, 11 Jun 2026 01:45:26 GMT  
		Size: 7.4 MB (7400233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f33679d10a6a3da802174cf113fe9a18201c399d2df1acedb48d3e15cc87eea`  
		Last Modified: Thu, 11 Jun 2026 01:45:25 GMT  
		Size: 372.2 KB (372190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f0a85e866c372a63d32cc9b04a3f1391d130a1a14ab63b23d19626d103f9bc`  
		Last Modified: Thu, 11 Jun 2026 01:45:25 GMT  
		Size: 76.5 KB (76543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1624ba1089fe474ab711259a9c638d5f2a35509c8fcaa0f3d6c1c7024a982d78`  
		Last Modified: Thu, 11 Jun 2026 01:45:27 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb6aed714ef171dfdc763c826d68e4961771927cf962f9c2958c51ac318121d`  
		Last Modified: Thu, 11 Jun 2026 01:45:29 GMT  
		Size: 101.1 MB (101056549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613051bab9b42ff0c6bdd0f982da5ad98b42863e425280a705a0af33a324b97c`  
		Last Modified: Thu, 11 Jun 2026 01:45:26 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5c03f4258a77892f6e2c31383e5ef571e56badceb291b4f151605cb4ae19c2`  
		Last Modified: Thu, 11 Jun 2026 01:45:27 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71d7d3e376d998fe98fc505bafc56a8f7211cd2be27593d158e4dd6fb240f47`  
		Last Modified: Thu, 11 Jun 2026 01:45:27 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89ecd3b42a4079bb33a718d8e8788a7ee37704dcec36448fc8b01dced722ff6`  
		Last Modified: Thu, 11 Jun 2026 01:45:28 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:ecdfaa5f3fe49f293f7a222a62d39959074cf6c83a7b1ddc3fd69357705f07d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ddd0b327eef7425ce79cfe4a657585a1c29161d647422ca0f78e5bdb12a698e`

```dockerfile
```

-	Layers:
	-	`sha256:72512a5c4b0363c040b9c43c543b783a15f9eae58d749d4d03f3606ef2f71a3b`  
		Last Modified: Thu, 11 Jun 2026 01:45:25 GMT  
		Size: 4.1 MB (4121627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c3bdff540d67a7087f41bacf4cc6191acc855eba2b974f92cb60a4129d3518d`  
		Last Modified: Thu, 11 Jun 2026 01:45:25 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3-nouveau`

```console
$ docker pull couchdb@sha256:25d1e0ccaabf1526890afa5082f1e24536579bd20feb5085266e38d8d2aedc7e
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
$ docker pull couchdb@sha256:46efa75e43e50cf8e3b32ab45997022e3f2a4862aff284b2135756b31bd103a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.6 MB (156561571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf3976ecfff0e9d68edd0b2dbbf6d3163f681c8ca3ad65c7945b65242babf1e2`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:43:06 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jun 2026 00:43:06 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Thu, 11 Jun 2026 00:43:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:43:22 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:43:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Thu, 11 Jun 2026 00:43:25 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jun 2026 00:43:30 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:43:30 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Thu, 11 Jun 2026 00:43:36 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Thu, 11 Jun 2026 00:43:36 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Thu, 11 Jun 2026 00:43:36 GMT
VOLUME [/opt/nouveau/data]
# Thu, 11 Jun 2026 00:43:36 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Thu, 11 Jun 2026 00:43:36 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8c6ebb2e85d5d0dca4b7eee74b4bb13d0a47f94488cabcb97682347f64f8a0`  
		Last Modified: Thu, 11 Jun 2026 00:43:51 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea5a2cae3a8725077de4aacc3c054747ce8d030d202c9017db9c1ccefe48e7f`  
		Last Modified: Thu, 11 Jun 2026 00:43:51 GMT  
		Size: 7.9 MB (7884346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eee0af3073fb579cd0ea4d27bc47f95fa4b20a8e0be665cf4eec74bf1a001cf`  
		Last Modified: Thu, 11 Jun 2026 00:43:53 GMT  
		Size: 77.5 MB (77478120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df80a1ba0ce0ac2a64573925cd2acae4b4ceebbc0fded8ba492d895d842ff49e`  
		Last Modified: Thu, 11 Jun 2026 00:43:51 GMT  
		Size: 424.2 KB (424159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8540a7a0af2ae69eb99a41b3214f87bc963eae9379559145eb6274f3518856da`  
		Last Modified: Thu, 11 Jun 2026 00:43:52 GMT  
		Size: 99.6 KB (99627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4fd65d8fc0ba13c33a9570ae4831fe8936912f02697195f7ba583b4b28d8dc`  
		Last Modified: Thu, 11 Jun 2026 00:43:52 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f1af6ab22429caa7ee66a32034aea07527423cd20f60e554c9d18529dba2e9`  
		Last Modified: Thu, 11 Jun 2026 00:43:54 GMT  
		Size: 42.4 MB (42435815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38ba33c68199233a1ff1058b3be662e9acf138988b7121e0b03ef6266a06069`  
		Last Modified: Thu, 11 Jun 2026 00:43:53 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:c10ce3a0b0bc97812564f6d8fe0dc37ba7392fd91f5ce538864c59df0686890c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e96ecb2455c4404855bfdddc341f755ee37ab3ac12ff05c8f425775aad2dd6c`

```dockerfile
```

-	Layers:
	-	`sha256:7d91b213225d770abc4651cae2cb12fc8a991ec1ea4ac5531320e34c74a76b59`  
		Last Modified: Thu, 11 Jun 2026 00:43:51 GMT  
		Size: 3.7 MB (3658671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0978a1da9ffddd8fa55c876ab7898321807e1d62cb09a0d725748b10881aef98`  
		Last Modified: Thu, 11 Jun 2026 00:43:51 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:0a5996ce00cdec6425d2b154a0b3363a9aa54d9967c62aed814ec263ea4548d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155443294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ff954b6eb81e7184f39bf7b459ec6109e450b138ef955c997c0508f0f11656`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:44:53 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jun 2026 00:44:53 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Thu, 11 Jun 2026 00:44:58 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:06 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Thu, 11 Jun 2026 00:45:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jun 2026 00:45:12 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:12 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Thu, 11 Jun 2026 00:45:17 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Thu, 11 Jun 2026 00:45:17 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Thu, 11 Jun 2026 00:45:17 GMT
VOLUME [/opt/nouveau/data]
# Thu, 11 Jun 2026 00:45:17 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Thu, 11 Jun 2026 00:45:17 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad224af02a5321b3eb29482ae705ae0f1e6544a563c86c09116caa3e8de361b5`  
		Last Modified: Thu, 11 Jun 2026 00:45:32 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6841905915492705f7458eb369dfce8ab834bf46a1423f78939762c62141d594`  
		Last Modified: Thu, 11 Jun 2026 00:45:33 GMT  
		Size: 7.7 MB (7695462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d263ded6b9aebd1331abaf55b3c7fe3f4f129ebcdc161ffd0566ce20b41c3b26`  
		Last Modified: Thu, 11 Jun 2026 00:45:35 GMT  
		Size: 76.8 MB (76793345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13bd7bb1465de6505ba9a4f4352aebec9172629dd2281cc3a8ee824808364665`  
		Last Modified: Thu, 11 Jun 2026 00:45:32 GMT  
		Size: 392.8 KB (392802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635bdeee11d0d90063c9252f316bc0d4b33c5b9c2c3693d696ff99341751d501`  
		Last Modified: Thu, 11 Jun 2026 00:45:34 GMT  
		Size: 99.5 KB (99545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86cafb0efd9657ed3a9a81947f88bbeb6f1d21c62a247b3407f08c1a40b4e66`  
		Last Modified: Thu, 11 Jun 2026 00:45:34 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0407a0241520f6ad2cc044f1f1c3336e3afcb74cd1d18eae6e93e6bc21e5ac19`  
		Last Modified: Thu, 11 Jun 2026 00:45:35 GMT  
		Size: 42.3 MB (42337953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cbf3cb3452afa3a7f5e686c07bc4eca25aeeec96425337ff7e80bffbb976e3`  
		Last Modified: Thu, 11 Jun 2026 00:45:35 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:ce501070e9e01b977a9af7464dbc4cfc820556d36a7ea1b745a5a504748fd4f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c263201881589b1be3f9766ab240d76bf68f4f466caacb01ec9b6f31624420b`

```dockerfile
```

-	Layers:
	-	`sha256:9f0ff81bd1d2e8b87d77163b3cb04e4df47839789155190b480f8c03dffceb8a`  
		Last Modified: Thu, 11 Jun 2026 00:45:33 GMT  
		Size: 3.7 MB (3657339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95da38822ce4f7bd93a39d0a00d7e28af1c721db9a7bdcf0c3f06c46709d32e9`  
		Last Modified: Thu, 11 Jun 2026 00:45:32 GMT  
		Size: 24.4 KB (24385 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:5f01d1a396975fcb18e6d7b8e26b000a53da4b967282c49d9986560c903e3ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.2 MB (150178271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06bdc4f5885ab1f5195cf05bb7699c173ff309b5505670b31b87edd2435ca706`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:44:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jun 2026 01:44:35 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Thu, 11 Jun 2026 01:44:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:44:52 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:44:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Thu, 11 Jun 2026 01:44:55 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jun 2026 01:44:59 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:44:59 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Thu, 11 Jun 2026 01:45:06 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Thu, 11 Jun 2026 01:45:06 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Thu, 11 Jun 2026 01:45:06 GMT
VOLUME [/opt/nouveau/data]
# Thu, 11 Jun 2026 01:45:06 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Thu, 11 Jun 2026 01:45:06 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84bc8db000f588b08571788f3f12d69b76501e751a18c6c2755f82a5fe68f588`  
		Last Modified: Thu, 11 Jun 2026 01:45:29 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37bdc5e8b6e872f0c6c1651d480846683e3daa9959e65e4c1a81cd1d713488e1`  
		Last Modified: Thu, 11 Jun 2026 01:45:30 GMT  
		Size: 7.4 MB (7400235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c60ab7447cd65e5c548b8f4f4cd81886409007edba6aac5bc31cd0f91b6e43`  
		Last Modified: Thu, 11 Jun 2026 01:45:32 GMT  
		Size: 73.2 MB (73225561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c4f8e7df6d45d1588bc1849c9dbe149afbea03758a816b47f44ce96b9f037d`  
		Last Modified: Thu, 11 Jun 2026 01:45:29 GMT  
		Size: 394.5 KB (394514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637ab811bb523af983dfa04da05bf838b461a604ad8c862f2dca46b72eaf61e2`  
		Last Modified: Thu, 11 Jun 2026 01:45:30 GMT  
		Size: 99.7 KB (99695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0333935d5ea23bb8735d411badac6860e225714d8fbce0b14c8909c0b821dde7`  
		Last Modified: Thu, 11 Jun 2026 01:45:31 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c87a6d8d98620e6b24c320b1b31ab7ccc4d890630b9c7eb4d94258eeaf9c9ba`  
		Last Modified: Thu, 11 Jun 2026 01:45:32 GMT  
		Size: 42.2 MB (42162881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8e4f15690348463aade48dfb64010bcca002efa6eaa56f4014a5337ef4da3c`  
		Last Modified: Thu, 11 Jun 2026 01:45:32 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:456173ecd6df5e2b420778241a563d4bd356d41119956c6ba28d3702bd2c9967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ae6a15d0ede23071584a7d66158f5c8422baeab63263f9a8f9debeab0a7a5b`

```dockerfile
```

-	Layers:
	-	`sha256:a759e5be1a235919d1bbd15627f56243ab5ead1c3311b3d2de8d177b1771652b`  
		Last Modified: Thu, 11 Jun 2026 01:45:30 GMT  
		Size: 3.6 MB (3649204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b8d9c2eea136d57e500d41d66d7816254c7b80990aea81ed21474f79193b24c`  
		Last Modified: Thu, 11 Jun 2026 01:45:29 GMT  
		Size: 24.2 KB (24214 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5`

```console
$ docker pull couchdb@sha256:db82596f7f5f5400071e66ece18d20d23329808df144fb399b7fb81e353e09db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.5` - linux; amd64

```console
$ docker pull couchdb@sha256:be60886dbb322f19a0971e6a9486470f5c084b01fdf949f5c0fe5fa001c73d85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148844645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df47e6b11fec6a9f139e0a4cd799195b9335a6ee66d0499f8832b259c565e1d7`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Tue, 23 Jun 2026 23:32:13 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 23 Jun 2026 23:32:13 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 23 Jun 2026 23:32:20 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 23 Jun 2026 23:32:23 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 23 Jun 2026 23:32:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:29 GMT
ENV COUCHDB_VERSION=3.5.2.1
# Tue, 23 Jun 2026 23:32:29 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 23 Jun 2026 23:32:42 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y couchdb="$COUCHDB_VERSION"~trixie ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 23 Jun 2026 23:32:42 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 23 Jun 2026 23:32:42 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 23 Jun 2026 23:32:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Jun 2026 23:32:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 23 Jun 2026 23:32:42 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 23 Jun 2026 23:32:42 GMT
VOLUME [/opt/couchdb/data]
# Tue, 23 Jun 2026 23:32:42 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 23 Jun 2026 23:32:42 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125d88fbb416bd132b2b8f3d3eabf258f48efefa96038c36085071bdd2af609c`  
		Last Modified: Tue, 23 Jun 2026 23:32:55 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d074679e62d672aee25403ccced7b29caa1896e83304bd63213e3a375113f046`  
		Last Modified: Tue, 23 Jun 2026 23:32:56 GMT  
		Size: 7.5 MB (7492092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6663734fecee46bd6dcb01731369c2ebf481c3a5936a080e1d8df3d4007f4d39`  
		Last Modified: Tue, 23 Jun 2026 23:32:56 GMT  
		Size: 417.6 KB (417587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67431044312ca3082fe7a2b3dc7bb930e80426deeebb680cf86e48e35fadcb2`  
		Last Modified: Tue, 23 Jun 2026 23:32:56 GMT  
		Size: 338.6 KB (338565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0d4985a9a56e5b22d40b28b97cdb659b734d2047b31e58acc76437eda7d3b2`  
		Last Modified: Tue, 23 Jun 2026 23:32:57 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700ec22e118fc20f9e3a895d0356c6328b522b0879d2e02346eac766ad384519`  
		Last Modified: Tue, 23 Jun 2026 23:33:00 GMT  
		Size: 110.8 MB (110805544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8bbde769c44cc9f31bce4fe5db619e92ee33d588bcdbd52e231e393a483a32`  
		Last Modified: Tue, 23 Jun 2026 23:32:57 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45cc4197154079e3f6baf01c4b8e9b1806fef3723f5e6c01b96c4457e045eb3`  
		Last Modified: Tue, 23 Jun 2026 23:32:58 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d2b70b4d764bf7f01f504f54aaf0184ddfaf16eb856b8ff054b3e19ca4616d`  
		Last Modified: Tue, 23 Jun 2026 23:32:58 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4342d5ebfbefc83074c8c48dcc48b04bb7b2beae212bab75ad0452728751d656`  
		Last Modified: Tue, 23 Jun 2026 23:32:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:cbadb92886e6ef4f494469f00d360b388f391a6869b1f65ec93fc4f7e1f3731e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffe06c4953ad56cbbde51d72829d9997a33ff4fa58467688ad34edfecc0e13c0`

```dockerfile
```

-	Layers:
	-	`sha256:2f0750e97f8e849e59fc02b42b2092399c35c47e3e9796b0726bc08271ea615f`  
		Last Modified: Tue, 23 Jun 2026 23:32:56 GMT  
		Size: 4.2 MB (4180389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c235be1ef4669946d2150eaf5111f1c1fde4bf3a55f8b20fabcf81011479953`  
		Last Modified: Tue, 23 Jun 2026 23:32:55 GMT  
		Size: 31.7 KB (31675 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:944dfe008f706100d9b057834e3b40c5458a8c6067128f0ad663d273150c3eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148610940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad95c003b35e7fe7956ebdfa924318bce0a6e1b5963594b06515e77c62742870`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Tue, 23 Jun 2026 23:32:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 23 Jun 2026 23:32:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 23 Jun 2026 23:32:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 23 Jun 2026 23:32:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 23 Jun 2026 23:32:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:51 GMT
ENV COUCHDB_VERSION=3.5.2.1
# Tue, 23 Jun 2026 23:32:51 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y couchdb="$COUCHDB_VERSION"~trixie ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 23 Jun 2026 23:33:23 GMT
VOLUME [/opt/couchdb/data]
# Tue, 23 Jun 2026 23:33:23 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 23 Jun 2026 23:33:23 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97325a7b140fe651aff8154d858a5a021c7b18c0b6aa682a107ba073a5ab4879`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f167452d2cba1aff408cd8774a342c06c7f6a04cc37baa0babef0c91a3f5625c`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 7.3 MB (7261105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ce20fd804da016a251954138074418b094a0dc4bcfc6ee19b8cd22088e4129`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 382.6 KB (382557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ad336cd92502642e2f46731304ff5129e7e079b418a0d2f9f8076af161f1a1`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 338.7 KB (338710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c13331aba23eb23da2064499c081c6c3a520fd7f7ffb5ddb550936bff241a9`  
		Last Modified: Tue, 23 Jun 2026 23:33:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa8af252651ec950c2e762b7b6be36b2607e24b082a1ea8eda27e848e4bf461`  
		Last Modified: Tue, 23 Jun 2026 23:33:41 GMT  
		Size: 110.5 MB (110474604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3ca67ecc05254da1956d0294bae75089e9baeaae4b55a4040cf2104523569e`  
		Last Modified: Tue, 23 Jun 2026 23:33:39 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc2ad2ae49d30c206b47a550edbfdb8f272d4655f1df57ff2a325879200801c`  
		Last Modified: Tue, 23 Jun 2026 23:33:39 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ba0691351b5030d43fcf1ba78d55b5379ab91823c2196eabf6e913e9730452`  
		Last Modified: Tue, 23 Jun 2026 23:33:40 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6ceb85a9d500a56bae2f07da226dcfe1b0205fa0376ee99bab8cc3d7dfa6da`  
		Last Modified: Tue, 23 Jun 2026 23:33:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:415c6f64ce0b44c20e9a1df07f92ca185b56638dacb503c74820fadf51f1fab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:420cd8298ed3cfb7b0358d7b5d372573c7432bb6ddc7e9e996a25dfd75e3df71`

```dockerfile
```

-	Layers:
	-	`sha256:772fe5e4c62244afd01871715e0219380812c7045c0eebdf7c9f304cd4cacc10`  
		Last Modified: Tue, 23 Jun 2026 23:33:38 GMT  
		Size: 4.2 MB (4180697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870cc7123fb12633ccff3283c814b3d934e261eb18435e57a2948acf80e2829c`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 31.9 KB (31882 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5-nouveau`

```console
$ docker pull couchdb@sha256:3d5fa356d316c88e8faaa639748ad1a9cbeb9c120d2f09ff6b3957e489d465dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.5-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:cf845280d11988b085245878e553d805404e325e1e9eb3f506873611533c40db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150900728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35180336f9ee14b1127e7a59aa52e1682e5cf44a3ea32cbbc423fedc601c54da`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Tue, 23 Jun 2026 23:32:15 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 23 Jun 2026 23:32:15 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 23 Jun 2026 23:32:21 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:26 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-21-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 23 Jun 2026 23:32:29 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 23 Jun 2026 23:32:34 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:34 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ trixie main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 23 Jun 2026 23:32:39 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --no-install-recommends couchdb-nouveau=3.5.2.1~trixie;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 23 Jun 2026 23:32:39 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 23 Jun 2026 23:32:39 GMT
VOLUME [/opt/nouveau/data]
# Tue, 23 Jun 2026 23:32:39 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 23 Jun 2026 23:32:39 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc1f003886a886b79e960038e80e6cb7fadff93ce1dfb08bc9528a6eca1be2e`  
		Last Modified: Tue, 23 Jun 2026 23:32:54 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a65cb72c4048e85e128ff5506d06591b6600c65429c4e3e2ed6cd1f16d31e90`  
		Last Modified: Tue, 23 Jun 2026 23:32:54 GMT  
		Size: 7.5 MB (7492030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2edbbc7d3d01fa0668be25cbc1bdae07f69ec42a68589679149cbfef4114d7`  
		Last Modified: Tue, 23 Jun 2026 23:32:56 GMT  
		Size: 70.0 MB (70032437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a376a3d0804c72aa79e235daa49be253a66a6d2be1dd7a6c17f00b1843582df5`  
		Last Modified: Tue, 23 Jun 2026 23:32:54 GMT  
		Size: 425.9 KB (425936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc013a92d1d24936f3851f3d5f42547202dad3cf95123c80ffe9276fa2fa88bc`  
		Last Modified: Tue, 23 Jun 2026 23:32:55 GMT  
		Size: 347.4 KB (347354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28709f3155cca3bf22e74af624cb00bd6eb7856690cdc32ba7b84b9649cadf82`  
		Last Modified: Tue, 23 Jun 2026 23:32:55 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ec7befc43ef270f329bc2a51d1e21683d75fd4210b560dc13d7d7883317ab4`  
		Last Modified: Tue, 23 Jun 2026 23:32:57 GMT  
		Size: 42.8 MB (42815675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd7a66cac537898204ca6f30745053c2edb2fbd1c788cffba36b61aadea9c82`  
		Last Modified: Tue, 23 Jun 2026 23:32:56 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:eecd9a40c14c87ecf57b4fa84a535f0b459c5092e9d984e26f2a2c33129ef74c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3389170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3794e3be70f8b586c99be65ba27c3da261be1ef2e951c1de4dfdedcd426d6d`

```dockerfile
```

-	Layers:
	-	`sha256:8b2b6bebeec38a0f7608c5c5c0cbda80eb6a973d1814cf1472a5f771b1b941d1`  
		Last Modified: Tue, 23 Jun 2026 23:32:54 GMT  
		Size: 3.4 MB (3364655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e995bd20f5e9575f68aa587c9946db0a390fd93bf1e6e3aa382e17168ea1bd7f`  
		Last Modified: Tue, 23 Jun 2026 23:32:54 GMT  
		Size: 24.5 KB (24515 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:b58614245c5f6861f59c37c7370a9be54fc61087a96a9ffb9f2b712a273da2f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150060763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:410645668157d46958b1415602b102a7ab2a5128ec41b8b426df94922d5dcb93`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Tue, 23 Jun 2026 23:32:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 23 Jun 2026 23:32:40 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 23 Jun 2026 23:32:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-21-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 23 Jun 2026 23:32:56 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 23 Jun 2026 23:33:02 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:33:02 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ trixie main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 23 Jun 2026 23:33:15 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --no-install-recommends couchdb-nouveau=3.5.2.1~trixie;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 23 Jun 2026 23:33:15 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 23 Jun 2026 23:33:15 GMT
VOLUME [/opt/nouveau/data]
# Tue, 23 Jun 2026 23:33:15 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 23 Jun 2026 23:33:15 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5313ce6db74f98627afe0c7e4d43f8b57a0ad77d4d3184ea9e0d01253abd33c8`  
		Last Modified: Tue, 23 Jun 2026 23:33:30 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40836ca234bd40b8c4295cd5a94a7f4a82f682c8f33844bae255d7a478d7dc4a`  
		Last Modified: Tue, 23 Jun 2026 23:33:31 GMT  
		Size: 7.3 MB (7261179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a9848ec6c2ee307d8714baeec49e7bf5425762816245c9b0fb5f279c422a3f`  
		Last Modified: Tue, 23 Jun 2026 23:33:32 GMT  
		Size: 69.2 MB (69179730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7010cf1c1c6d1a1900757033c5552425409fc6a2ca148b95da9821808d0c7b`  
		Last Modified: Tue, 23 Jun 2026 23:33:30 GMT  
		Size: 390.2 KB (390249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce482bfa8391c85475e9b9f5c31fc168fc5ed90ad518340b7f4d25f8d6fec8b2`  
		Last Modified: Tue, 23 Jun 2026 23:33:31 GMT  
		Size: 347.4 KB (347418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8dc170d66d6619a3baeb573638bde792eb024ff90158a35042dfe10130708ef`  
		Last Modified: Tue, 23 Jun 2026 23:33:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fcb5ef627136ba3bcfdfeb04eaf3befa8df1179de18c09851623e49eb1ee6ca`  
		Last Modified: Tue, 23 Jun 2026 23:33:33 GMT  
		Size: 42.7 MB (42731780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e19d0ccfba4ad18823eb374f84b7eda28d7d3febcf012f3d0a055e344190e2e`  
		Last Modified: Tue, 23 Jun 2026 23:33:33 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:1a3070bb6674fbd4130b503a1ea4f1b33ef83e3c1f047f52e375976113bd771b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3388017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a85de82f4abfe2b8fb1830a1dff75fcf62b7badf54c28672ddef151f1f9922ea`

```dockerfile
```

-	Layers:
	-	`sha256:7b7e3cf0d0456eb003b663814fc3d531897a1574d956b425fa5151d48d39b3aa`  
		Last Modified: Tue, 23 Jun 2026 23:33:30 GMT  
		Size: 3.4 MB (3363308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b577a1dc55bd252562e26292b066fa2b53cfbb445788988c8f0fdba069317ce`  
		Last Modified: Tue, 23 Jun 2026 23:33:30 GMT  
		Size: 24.7 KB (24709 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.2`

```console
$ docker pull couchdb@sha256:db82596f7f5f5400071e66ece18d20d23329808df144fb399b7fb81e353e09db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.5.2` - linux; amd64

```console
$ docker pull couchdb@sha256:be60886dbb322f19a0971e6a9486470f5c084b01fdf949f5c0fe5fa001c73d85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148844645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df47e6b11fec6a9f139e0a4cd799195b9335a6ee66d0499f8832b259c565e1d7`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Tue, 23 Jun 2026 23:32:13 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 23 Jun 2026 23:32:13 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 23 Jun 2026 23:32:20 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 23 Jun 2026 23:32:23 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 23 Jun 2026 23:32:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:29 GMT
ENV COUCHDB_VERSION=3.5.2.1
# Tue, 23 Jun 2026 23:32:29 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 23 Jun 2026 23:32:42 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y couchdb="$COUCHDB_VERSION"~trixie ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 23 Jun 2026 23:32:42 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 23 Jun 2026 23:32:42 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 23 Jun 2026 23:32:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Jun 2026 23:32:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 23 Jun 2026 23:32:42 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 23 Jun 2026 23:32:42 GMT
VOLUME [/opt/couchdb/data]
# Tue, 23 Jun 2026 23:32:42 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 23 Jun 2026 23:32:42 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125d88fbb416bd132b2b8f3d3eabf258f48efefa96038c36085071bdd2af609c`  
		Last Modified: Tue, 23 Jun 2026 23:32:55 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d074679e62d672aee25403ccced7b29caa1896e83304bd63213e3a375113f046`  
		Last Modified: Tue, 23 Jun 2026 23:32:56 GMT  
		Size: 7.5 MB (7492092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6663734fecee46bd6dcb01731369c2ebf481c3a5936a080e1d8df3d4007f4d39`  
		Last Modified: Tue, 23 Jun 2026 23:32:56 GMT  
		Size: 417.6 KB (417587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67431044312ca3082fe7a2b3dc7bb930e80426deeebb680cf86e48e35fadcb2`  
		Last Modified: Tue, 23 Jun 2026 23:32:56 GMT  
		Size: 338.6 KB (338565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0d4985a9a56e5b22d40b28b97cdb659b734d2047b31e58acc76437eda7d3b2`  
		Last Modified: Tue, 23 Jun 2026 23:32:57 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700ec22e118fc20f9e3a895d0356c6328b522b0879d2e02346eac766ad384519`  
		Last Modified: Tue, 23 Jun 2026 23:33:00 GMT  
		Size: 110.8 MB (110805544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8bbde769c44cc9f31bce4fe5db619e92ee33d588bcdbd52e231e393a483a32`  
		Last Modified: Tue, 23 Jun 2026 23:32:57 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45cc4197154079e3f6baf01c4b8e9b1806fef3723f5e6c01b96c4457e045eb3`  
		Last Modified: Tue, 23 Jun 2026 23:32:58 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d2b70b4d764bf7f01f504f54aaf0184ddfaf16eb856b8ff054b3e19ca4616d`  
		Last Modified: Tue, 23 Jun 2026 23:32:58 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4342d5ebfbefc83074c8c48dcc48b04bb7b2beae212bab75ad0452728751d656`  
		Last Modified: Tue, 23 Jun 2026 23:32:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:cbadb92886e6ef4f494469f00d360b388f391a6869b1f65ec93fc4f7e1f3731e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffe06c4953ad56cbbde51d72829d9997a33ff4fa58467688ad34edfecc0e13c0`

```dockerfile
```

-	Layers:
	-	`sha256:2f0750e97f8e849e59fc02b42b2092399c35c47e3e9796b0726bc08271ea615f`  
		Last Modified: Tue, 23 Jun 2026 23:32:56 GMT  
		Size: 4.2 MB (4180389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c235be1ef4669946d2150eaf5111f1c1fde4bf3a55f8b20fabcf81011479953`  
		Last Modified: Tue, 23 Jun 2026 23:32:55 GMT  
		Size: 31.7 KB (31675 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:944dfe008f706100d9b057834e3b40c5458a8c6067128f0ad663d273150c3eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148610940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad95c003b35e7fe7956ebdfa924318bce0a6e1b5963594b06515e77c62742870`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Tue, 23 Jun 2026 23:32:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 23 Jun 2026 23:32:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 23 Jun 2026 23:32:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 23 Jun 2026 23:32:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 23 Jun 2026 23:32:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:51 GMT
ENV COUCHDB_VERSION=3.5.2.1
# Tue, 23 Jun 2026 23:32:51 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y couchdb="$COUCHDB_VERSION"~trixie ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 23 Jun 2026 23:33:23 GMT
VOLUME [/opt/couchdb/data]
# Tue, 23 Jun 2026 23:33:23 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 23 Jun 2026 23:33:23 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97325a7b140fe651aff8154d858a5a021c7b18c0b6aa682a107ba073a5ab4879`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f167452d2cba1aff408cd8774a342c06c7f6a04cc37baa0babef0c91a3f5625c`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 7.3 MB (7261105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ce20fd804da016a251954138074418b094a0dc4bcfc6ee19b8cd22088e4129`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 382.6 KB (382557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ad336cd92502642e2f46731304ff5129e7e079b418a0d2f9f8076af161f1a1`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 338.7 KB (338710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c13331aba23eb23da2064499c081c6c3a520fd7f7ffb5ddb550936bff241a9`  
		Last Modified: Tue, 23 Jun 2026 23:33:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa8af252651ec950c2e762b7b6be36b2607e24b082a1ea8eda27e848e4bf461`  
		Last Modified: Tue, 23 Jun 2026 23:33:41 GMT  
		Size: 110.5 MB (110474604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3ca67ecc05254da1956d0294bae75089e9baeaae4b55a4040cf2104523569e`  
		Last Modified: Tue, 23 Jun 2026 23:33:39 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc2ad2ae49d30c206b47a550edbfdb8f272d4655f1df57ff2a325879200801c`  
		Last Modified: Tue, 23 Jun 2026 23:33:39 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ba0691351b5030d43fcf1ba78d55b5379ab91823c2196eabf6e913e9730452`  
		Last Modified: Tue, 23 Jun 2026 23:33:40 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6ceb85a9d500a56bae2f07da226dcfe1b0205fa0376ee99bab8cc3d7dfa6da`  
		Last Modified: Tue, 23 Jun 2026 23:33:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:415c6f64ce0b44c20e9a1df07f92ca185b56638dacb503c74820fadf51f1fab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:420cd8298ed3cfb7b0358d7b5d372573c7432bb6ddc7e9e996a25dfd75e3df71`

```dockerfile
```

-	Layers:
	-	`sha256:772fe5e4c62244afd01871715e0219380812c7045c0eebdf7c9f304cd4cacc10`  
		Last Modified: Tue, 23 Jun 2026 23:33:38 GMT  
		Size: 4.2 MB (4180697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870cc7123fb12633ccff3283c814b3d934e261eb18435e57a2948acf80e2829c`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 31.9 KB (31882 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.2-nouveau`

```console
$ docker pull couchdb@sha256:3d5fa356d316c88e8faaa639748ad1a9cbeb9c120d2f09ff6b3957e489d465dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.5.2-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:cf845280d11988b085245878e553d805404e325e1e9eb3f506873611533c40db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150900728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35180336f9ee14b1127e7a59aa52e1682e5cf44a3ea32cbbc423fedc601c54da`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Tue, 23 Jun 2026 23:32:15 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 23 Jun 2026 23:32:15 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 23 Jun 2026 23:32:21 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:26 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-21-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 23 Jun 2026 23:32:29 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 23 Jun 2026 23:32:34 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:34 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ trixie main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 23 Jun 2026 23:32:39 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --no-install-recommends couchdb-nouveau=3.5.2.1~trixie;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 23 Jun 2026 23:32:39 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 23 Jun 2026 23:32:39 GMT
VOLUME [/opt/nouveau/data]
# Tue, 23 Jun 2026 23:32:39 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 23 Jun 2026 23:32:39 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc1f003886a886b79e960038e80e6cb7fadff93ce1dfb08bc9528a6eca1be2e`  
		Last Modified: Tue, 23 Jun 2026 23:32:54 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a65cb72c4048e85e128ff5506d06591b6600c65429c4e3e2ed6cd1f16d31e90`  
		Last Modified: Tue, 23 Jun 2026 23:32:54 GMT  
		Size: 7.5 MB (7492030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2edbbc7d3d01fa0668be25cbc1bdae07f69ec42a68589679149cbfef4114d7`  
		Last Modified: Tue, 23 Jun 2026 23:32:56 GMT  
		Size: 70.0 MB (70032437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a376a3d0804c72aa79e235daa49be253a66a6d2be1dd7a6c17f00b1843582df5`  
		Last Modified: Tue, 23 Jun 2026 23:32:54 GMT  
		Size: 425.9 KB (425936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc013a92d1d24936f3851f3d5f42547202dad3cf95123c80ffe9276fa2fa88bc`  
		Last Modified: Tue, 23 Jun 2026 23:32:55 GMT  
		Size: 347.4 KB (347354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28709f3155cca3bf22e74af624cb00bd6eb7856690cdc32ba7b84b9649cadf82`  
		Last Modified: Tue, 23 Jun 2026 23:32:55 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ec7befc43ef270f329bc2a51d1e21683d75fd4210b560dc13d7d7883317ab4`  
		Last Modified: Tue, 23 Jun 2026 23:32:57 GMT  
		Size: 42.8 MB (42815675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd7a66cac537898204ca6f30745053c2edb2fbd1c788cffba36b61aadea9c82`  
		Last Modified: Tue, 23 Jun 2026 23:32:56 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.2-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:eecd9a40c14c87ecf57b4fa84a535f0b459c5092e9d984e26f2a2c33129ef74c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3389170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3794e3be70f8b586c99be65ba27c3da261be1ef2e951c1de4dfdedcd426d6d`

```dockerfile
```

-	Layers:
	-	`sha256:8b2b6bebeec38a0f7608c5c5c0cbda80eb6a973d1814cf1472a5f771b1b941d1`  
		Last Modified: Tue, 23 Jun 2026 23:32:54 GMT  
		Size: 3.4 MB (3364655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e995bd20f5e9575f68aa587c9946db0a390fd93bf1e6e3aa382e17168ea1bd7f`  
		Last Modified: Tue, 23 Jun 2026 23:32:54 GMT  
		Size: 24.5 KB (24515 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.2-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:b58614245c5f6861f59c37c7370a9be54fc61087a96a9ffb9f2b712a273da2f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150060763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:410645668157d46958b1415602b102a7ab2a5128ec41b8b426df94922d5dcb93`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Tue, 23 Jun 2026 23:32:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 23 Jun 2026 23:32:40 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 23 Jun 2026 23:32:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-21-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 23 Jun 2026 23:32:56 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 23 Jun 2026 23:33:02 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:33:02 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ trixie main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 23 Jun 2026 23:33:15 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --no-install-recommends couchdb-nouveau=3.5.2.1~trixie;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 23 Jun 2026 23:33:15 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 23 Jun 2026 23:33:15 GMT
VOLUME [/opt/nouveau/data]
# Tue, 23 Jun 2026 23:33:15 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 23 Jun 2026 23:33:15 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5313ce6db74f98627afe0c7e4d43f8b57a0ad77d4d3184ea9e0d01253abd33c8`  
		Last Modified: Tue, 23 Jun 2026 23:33:30 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40836ca234bd40b8c4295cd5a94a7f4a82f682c8f33844bae255d7a478d7dc4a`  
		Last Modified: Tue, 23 Jun 2026 23:33:31 GMT  
		Size: 7.3 MB (7261179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a9848ec6c2ee307d8714baeec49e7bf5425762816245c9b0fb5f279c422a3f`  
		Last Modified: Tue, 23 Jun 2026 23:33:32 GMT  
		Size: 69.2 MB (69179730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7010cf1c1c6d1a1900757033c5552425409fc6a2ca148b95da9821808d0c7b`  
		Last Modified: Tue, 23 Jun 2026 23:33:30 GMT  
		Size: 390.2 KB (390249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce482bfa8391c85475e9b9f5c31fc168fc5ed90ad518340b7f4d25f8d6fec8b2`  
		Last Modified: Tue, 23 Jun 2026 23:33:31 GMT  
		Size: 347.4 KB (347418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8dc170d66d6619a3baeb573638bde792eb024ff90158a35042dfe10130708ef`  
		Last Modified: Tue, 23 Jun 2026 23:33:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fcb5ef627136ba3bcfdfeb04eaf3befa8df1179de18c09851623e49eb1ee6ca`  
		Last Modified: Tue, 23 Jun 2026 23:33:33 GMT  
		Size: 42.7 MB (42731780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e19d0ccfba4ad18823eb374f84b7eda28d7d3febcf012f3d0a055e344190e2e`  
		Last Modified: Tue, 23 Jun 2026 23:33:33 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.2-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:1a3070bb6674fbd4130b503a1ea4f1b33ef83e3c1f047f52e375976113bd771b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3388017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a85de82f4abfe2b8fb1830a1dff75fcf62b7badf54c28672ddef151f1f9922ea`

```dockerfile
```

-	Layers:
	-	`sha256:7b7e3cf0d0456eb003b663814fc3d531897a1574d956b425fa5151d48d39b3aa`  
		Last Modified: Tue, 23 Jun 2026 23:33:30 GMT  
		Size: 3.4 MB (3363308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b577a1dc55bd252562e26292b066fa2b53cfbb445788988c8f0fdba069317ce`  
		Last Modified: Tue, 23 Jun 2026 23:33:30 GMT  
		Size: 24.7 KB (24709 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.2.1`

```console
$ docker pull couchdb@sha256:db82596f7f5f5400071e66ece18d20d23329808df144fb399b7fb81e353e09db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.5.2.1` - linux; amd64

```console
$ docker pull couchdb@sha256:be60886dbb322f19a0971e6a9486470f5c084b01fdf949f5c0fe5fa001c73d85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148844645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df47e6b11fec6a9f139e0a4cd799195b9335a6ee66d0499f8832b259c565e1d7`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Tue, 23 Jun 2026 23:32:13 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 23 Jun 2026 23:32:13 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 23 Jun 2026 23:32:20 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 23 Jun 2026 23:32:23 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 23 Jun 2026 23:32:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:29 GMT
ENV COUCHDB_VERSION=3.5.2.1
# Tue, 23 Jun 2026 23:32:29 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 23 Jun 2026 23:32:42 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y couchdb="$COUCHDB_VERSION"~trixie ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 23 Jun 2026 23:32:42 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 23 Jun 2026 23:32:42 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 23 Jun 2026 23:32:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Jun 2026 23:32:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 23 Jun 2026 23:32:42 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 23 Jun 2026 23:32:42 GMT
VOLUME [/opt/couchdb/data]
# Tue, 23 Jun 2026 23:32:42 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 23 Jun 2026 23:32:42 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125d88fbb416bd132b2b8f3d3eabf258f48efefa96038c36085071bdd2af609c`  
		Last Modified: Tue, 23 Jun 2026 23:32:55 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d074679e62d672aee25403ccced7b29caa1896e83304bd63213e3a375113f046`  
		Last Modified: Tue, 23 Jun 2026 23:32:56 GMT  
		Size: 7.5 MB (7492092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6663734fecee46bd6dcb01731369c2ebf481c3a5936a080e1d8df3d4007f4d39`  
		Last Modified: Tue, 23 Jun 2026 23:32:56 GMT  
		Size: 417.6 KB (417587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67431044312ca3082fe7a2b3dc7bb930e80426deeebb680cf86e48e35fadcb2`  
		Last Modified: Tue, 23 Jun 2026 23:32:56 GMT  
		Size: 338.6 KB (338565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0d4985a9a56e5b22d40b28b97cdb659b734d2047b31e58acc76437eda7d3b2`  
		Last Modified: Tue, 23 Jun 2026 23:32:57 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700ec22e118fc20f9e3a895d0356c6328b522b0879d2e02346eac766ad384519`  
		Last Modified: Tue, 23 Jun 2026 23:33:00 GMT  
		Size: 110.8 MB (110805544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8bbde769c44cc9f31bce4fe5db619e92ee33d588bcdbd52e231e393a483a32`  
		Last Modified: Tue, 23 Jun 2026 23:32:57 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45cc4197154079e3f6baf01c4b8e9b1806fef3723f5e6c01b96c4457e045eb3`  
		Last Modified: Tue, 23 Jun 2026 23:32:58 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d2b70b4d764bf7f01f504f54aaf0184ddfaf16eb856b8ff054b3e19ca4616d`  
		Last Modified: Tue, 23 Jun 2026 23:32:58 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4342d5ebfbefc83074c8c48dcc48b04bb7b2beae212bab75ad0452728751d656`  
		Last Modified: Tue, 23 Jun 2026 23:32:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.2.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:cbadb92886e6ef4f494469f00d360b388f391a6869b1f65ec93fc4f7e1f3731e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffe06c4953ad56cbbde51d72829d9997a33ff4fa58467688ad34edfecc0e13c0`

```dockerfile
```

-	Layers:
	-	`sha256:2f0750e97f8e849e59fc02b42b2092399c35c47e3e9796b0726bc08271ea615f`  
		Last Modified: Tue, 23 Jun 2026 23:32:56 GMT  
		Size: 4.2 MB (4180389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c235be1ef4669946d2150eaf5111f1c1fde4bf3a55f8b20fabcf81011479953`  
		Last Modified: Tue, 23 Jun 2026 23:32:55 GMT  
		Size: 31.7 KB (31675 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.2.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:944dfe008f706100d9b057834e3b40c5458a8c6067128f0ad663d273150c3eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148610940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad95c003b35e7fe7956ebdfa924318bce0a6e1b5963594b06515e77c62742870`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Tue, 23 Jun 2026 23:32:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 23 Jun 2026 23:32:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 23 Jun 2026 23:32:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 23 Jun 2026 23:32:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 23 Jun 2026 23:32:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:51 GMT
ENV COUCHDB_VERSION=3.5.2.1
# Tue, 23 Jun 2026 23:32:51 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y couchdb="$COUCHDB_VERSION"~trixie ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 23 Jun 2026 23:33:23 GMT
VOLUME [/opt/couchdb/data]
# Tue, 23 Jun 2026 23:33:23 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 23 Jun 2026 23:33:23 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97325a7b140fe651aff8154d858a5a021c7b18c0b6aa682a107ba073a5ab4879`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f167452d2cba1aff408cd8774a342c06c7f6a04cc37baa0babef0c91a3f5625c`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 7.3 MB (7261105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ce20fd804da016a251954138074418b094a0dc4bcfc6ee19b8cd22088e4129`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 382.6 KB (382557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ad336cd92502642e2f46731304ff5129e7e079b418a0d2f9f8076af161f1a1`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 338.7 KB (338710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c13331aba23eb23da2064499c081c6c3a520fd7f7ffb5ddb550936bff241a9`  
		Last Modified: Tue, 23 Jun 2026 23:33:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa8af252651ec950c2e762b7b6be36b2607e24b082a1ea8eda27e848e4bf461`  
		Last Modified: Tue, 23 Jun 2026 23:33:41 GMT  
		Size: 110.5 MB (110474604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3ca67ecc05254da1956d0294bae75089e9baeaae4b55a4040cf2104523569e`  
		Last Modified: Tue, 23 Jun 2026 23:33:39 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc2ad2ae49d30c206b47a550edbfdb8f272d4655f1df57ff2a325879200801c`  
		Last Modified: Tue, 23 Jun 2026 23:33:39 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ba0691351b5030d43fcf1ba78d55b5379ab91823c2196eabf6e913e9730452`  
		Last Modified: Tue, 23 Jun 2026 23:33:40 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6ceb85a9d500a56bae2f07da226dcfe1b0205fa0376ee99bab8cc3d7dfa6da`  
		Last Modified: Tue, 23 Jun 2026 23:33:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.2.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:415c6f64ce0b44c20e9a1df07f92ca185b56638dacb503c74820fadf51f1fab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:420cd8298ed3cfb7b0358d7b5d372573c7432bb6ddc7e9e996a25dfd75e3df71`

```dockerfile
```

-	Layers:
	-	`sha256:772fe5e4c62244afd01871715e0219380812c7045c0eebdf7c9f304cd4cacc10`  
		Last Modified: Tue, 23 Jun 2026 23:33:38 GMT  
		Size: 4.2 MB (4180697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870cc7123fb12633ccff3283c814b3d934e261eb18435e57a2948acf80e2829c`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 31.9 KB (31882 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.2.1-nouveau`

```console
$ docker pull couchdb@sha256:3d5fa356d316c88e8faaa639748ad1a9cbeb9c120d2f09ff6b3957e489d465dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.5.2.1-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:cf845280d11988b085245878e553d805404e325e1e9eb3f506873611533c40db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150900728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35180336f9ee14b1127e7a59aa52e1682e5cf44a3ea32cbbc423fedc601c54da`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Tue, 23 Jun 2026 23:32:15 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 23 Jun 2026 23:32:15 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 23 Jun 2026 23:32:21 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:26 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-21-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 23 Jun 2026 23:32:29 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 23 Jun 2026 23:32:34 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:34 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ trixie main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 23 Jun 2026 23:32:39 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --no-install-recommends couchdb-nouveau=3.5.2.1~trixie;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 23 Jun 2026 23:32:39 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 23 Jun 2026 23:32:39 GMT
VOLUME [/opt/nouveau/data]
# Tue, 23 Jun 2026 23:32:39 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 23 Jun 2026 23:32:39 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc1f003886a886b79e960038e80e6cb7fadff93ce1dfb08bc9528a6eca1be2e`  
		Last Modified: Tue, 23 Jun 2026 23:32:54 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a65cb72c4048e85e128ff5506d06591b6600c65429c4e3e2ed6cd1f16d31e90`  
		Last Modified: Tue, 23 Jun 2026 23:32:54 GMT  
		Size: 7.5 MB (7492030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2edbbc7d3d01fa0668be25cbc1bdae07f69ec42a68589679149cbfef4114d7`  
		Last Modified: Tue, 23 Jun 2026 23:32:56 GMT  
		Size: 70.0 MB (70032437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a376a3d0804c72aa79e235daa49be253a66a6d2be1dd7a6c17f00b1843582df5`  
		Last Modified: Tue, 23 Jun 2026 23:32:54 GMT  
		Size: 425.9 KB (425936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc013a92d1d24936f3851f3d5f42547202dad3cf95123c80ffe9276fa2fa88bc`  
		Last Modified: Tue, 23 Jun 2026 23:32:55 GMT  
		Size: 347.4 KB (347354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28709f3155cca3bf22e74af624cb00bd6eb7856690cdc32ba7b84b9649cadf82`  
		Last Modified: Tue, 23 Jun 2026 23:32:55 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ec7befc43ef270f329bc2a51d1e21683d75fd4210b560dc13d7d7883317ab4`  
		Last Modified: Tue, 23 Jun 2026 23:32:57 GMT  
		Size: 42.8 MB (42815675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd7a66cac537898204ca6f30745053c2edb2fbd1c788cffba36b61aadea9c82`  
		Last Modified: Tue, 23 Jun 2026 23:32:56 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.2.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:eecd9a40c14c87ecf57b4fa84a535f0b459c5092e9d984e26f2a2c33129ef74c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3389170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3794e3be70f8b586c99be65ba27c3da261be1ef2e951c1de4dfdedcd426d6d`

```dockerfile
```

-	Layers:
	-	`sha256:8b2b6bebeec38a0f7608c5c5c0cbda80eb6a973d1814cf1472a5f771b1b941d1`  
		Last Modified: Tue, 23 Jun 2026 23:32:54 GMT  
		Size: 3.4 MB (3364655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e995bd20f5e9575f68aa587c9946db0a390fd93bf1e6e3aa382e17168ea1bd7f`  
		Last Modified: Tue, 23 Jun 2026 23:32:54 GMT  
		Size: 24.5 KB (24515 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.2.1-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:b58614245c5f6861f59c37c7370a9be54fc61087a96a9ffb9f2b712a273da2f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150060763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:410645668157d46958b1415602b102a7ab2a5128ec41b8b426df94922d5dcb93`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Tue, 23 Jun 2026 23:32:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 23 Jun 2026 23:32:40 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 23 Jun 2026 23:32:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-21-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 23 Jun 2026 23:32:56 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 23 Jun 2026 23:33:02 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:33:02 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ trixie main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 23 Jun 2026 23:33:15 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --no-install-recommends couchdb-nouveau=3.5.2.1~trixie;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 23 Jun 2026 23:33:15 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 23 Jun 2026 23:33:15 GMT
VOLUME [/opt/nouveau/data]
# Tue, 23 Jun 2026 23:33:15 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 23 Jun 2026 23:33:15 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5313ce6db74f98627afe0c7e4d43f8b57a0ad77d4d3184ea9e0d01253abd33c8`  
		Last Modified: Tue, 23 Jun 2026 23:33:30 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40836ca234bd40b8c4295cd5a94a7f4a82f682c8f33844bae255d7a478d7dc4a`  
		Last Modified: Tue, 23 Jun 2026 23:33:31 GMT  
		Size: 7.3 MB (7261179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a9848ec6c2ee307d8714baeec49e7bf5425762816245c9b0fb5f279c422a3f`  
		Last Modified: Tue, 23 Jun 2026 23:33:32 GMT  
		Size: 69.2 MB (69179730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7010cf1c1c6d1a1900757033c5552425409fc6a2ca148b95da9821808d0c7b`  
		Last Modified: Tue, 23 Jun 2026 23:33:30 GMT  
		Size: 390.2 KB (390249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce482bfa8391c85475e9b9f5c31fc168fc5ed90ad518340b7f4d25f8d6fec8b2`  
		Last Modified: Tue, 23 Jun 2026 23:33:31 GMT  
		Size: 347.4 KB (347418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8dc170d66d6619a3baeb573638bde792eb024ff90158a35042dfe10130708ef`  
		Last Modified: Tue, 23 Jun 2026 23:33:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fcb5ef627136ba3bcfdfeb04eaf3befa8df1179de18c09851623e49eb1ee6ca`  
		Last Modified: Tue, 23 Jun 2026 23:33:33 GMT  
		Size: 42.7 MB (42731780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e19d0ccfba4ad18823eb374f84b7eda28d7d3febcf012f3d0a055e344190e2e`  
		Last Modified: Tue, 23 Jun 2026 23:33:33 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.2.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:1a3070bb6674fbd4130b503a1ea4f1b33ef83e3c1f047f52e375976113bd771b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3388017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a85de82f4abfe2b8fb1830a1dff75fcf62b7badf54c28672ddef151f1f9922ea`

```dockerfile
```

-	Layers:
	-	`sha256:7b7e3cf0d0456eb003b663814fc3d531897a1574d956b425fa5151d48d39b3aa`  
		Last Modified: Tue, 23 Jun 2026 23:33:30 GMT  
		Size: 3.4 MB (3363308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b577a1dc55bd252562e26292b066fa2b53cfbb445788988c8f0fdba069317ce`  
		Last Modified: Tue, 23 Jun 2026 23:33:30 GMT  
		Size: 24.7 KB (24709 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:db82596f7f5f5400071e66ece18d20d23329808df144fb399b7fb81e353e09db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:be60886dbb322f19a0971e6a9486470f5c084b01fdf949f5c0fe5fa001c73d85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148844645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df47e6b11fec6a9f139e0a4cd799195b9335a6ee66d0499f8832b259c565e1d7`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Tue, 23 Jun 2026 23:32:13 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 23 Jun 2026 23:32:13 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 23 Jun 2026 23:32:20 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 23 Jun 2026 23:32:23 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 23 Jun 2026 23:32:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:29 GMT
ENV COUCHDB_VERSION=3.5.2.1
# Tue, 23 Jun 2026 23:32:29 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 23 Jun 2026 23:32:42 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y couchdb="$COUCHDB_VERSION"~trixie ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 23 Jun 2026 23:32:42 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 23 Jun 2026 23:32:42 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 23 Jun 2026 23:32:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Jun 2026 23:32:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 23 Jun 2026 23:32:42 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 23 Jun 2026 23:32:42 GMT
VOLUME [/opt/couchdb/data]
# Tue, 23 Jun 2026 23:32:42 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 23 Jun 2026 23:32:42 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125d88fbb416bd132b2b8f3d3eabf258f48efefa96038c36085071bdd2af609c`  
		Last Modified: Tue, 23 Jun 2026 23:32:55 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d074679e62d672aee25403ccced7b29caa1896e83304bd63213e3a375113f046`  
		Last Modified: Tue, 23 Jun 2026 23:32:56 GMT  
		Size: 7.5 MB (7492092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6663734fecee46bd6dcb01731369c2ebf481c3a5936a080e1d8df3d4007f4d39`  
		Last Modified: Tue, 23 Jun 2026 23:32:56 GMT  
		Size: 417.6 KB (417587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67431044312ca3082fe7a2b3dc7bb930e80426deeebb680cf86e48e35fadcb2`  
		Last Modified: Tue, 23 Jun 2026 23:32:56 GMT  
		Size: 338.6 KB (338565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0d4985a9a56e5b22d40b28b97cdb659b734d2047b31e58acc76437eda7d3b2`  
		Last Modified: Tue, 23 Jun 2026 23:32:57 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700ec22e118fc20f9e3a895d0356c6328b522b0879d2e02346eac766ad384519`  
		Last Modified: Tue, 23 Jun 2026 23:33:00 GMT  
		Size: 110.8 MB (110805544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8bbde769c44cc9f31bce4fe5db619e92ee33d588bcdbd52e231e393a483a32`  
		Last Modified: Tue, 23 Jun 2026 23:32:57 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45cc4197154079e3f6baf01c4b8e9b1806fef3723f5e6c01b96c4457e045eb3`  
		Last Modified: Tue, 23 Jun 2026 23:32:58 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d2b70b4d764bf7f01f504f54aaf0184ddfaf16eb856b8ff054b3e19ca4616d`  
		Last Modified: Tue, 23 Jun 2026 23:32:58 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4342d5ebfbefc83074c8c48dcc48b04bb7b2beae212bab75ad0452728751d656`  
		Last Modified: Tue, 23 Jun 2026 23:32:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:cbadb92886e6ef4f494469f00d360b388f391a6869b1f65ec93fc4f7e1f3731e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffe06c4953ad56cbbde51d72829d9997a33ff4fa58467688ad34edfecc0e13c0`

```dockerfile
```

-	Layers:
	-	`sha256:2f0750e97f8e849e59fc02b42b2092399c35c47e3e9796b0726bc08271ea615f`  
		Last Modified: Tue, 23 Jun 2026 23:32:56 GMT  
		Size: 4.2 MB (4180389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c235be1ef4669946d2150eaf5111f1c1fde4bf3a55f8b20fabcf81011479953`  
		Last Modified: Tue, 23 Jun 2026 23:32:55 GMT  
		Size: 31.7 KB (31675 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:944dfe008f706100d9b057834e3b40c5458a8c6067128f0ad663d273150c3eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148610940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad95c003b35e7fe7956ebdfa924318bce0a6e1b5963594b06515e77c62742870`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Tue, 23 Jun 2026 23:32:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 23 Jun 2026 23:32:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 23 Jun 2026 23:32:42 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 23 Jun 2026 23:32:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 23 Jun 2026 23:32:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:51 GMT
ENV COUCHDB_VERSION=3.5.2.1
# Tue, 23 Jun 2026 23:32:51 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y couchdb="$COUCHDB_VERSION"~trixie ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 23 Jun 2026 23:33:23 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 23 Jun 2026 23:33:23 GMT
VOLUME [/opt/couchdb/data]
# Tue, 23 Jun 2026 23:33:23 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 23 Jun 2026 23:33:23 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97325a7b140fe651aff8154d858a5a021c7b18c0b6aa682a107ba073a5ab4879`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f167452d2cba1aff408cd8774a342c06c7f6a04cc37baa0babef0c91a3f5625c`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 7.3 MB (7261105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ce20fd804da016a251954138074418b094a0dc4bcfc6ee19b8cd22088e4129`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 382.6 KB (382557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ad336cd92502642e2f46731304ff5129e7e079b418a0d2f9f8076af161f1a1`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 338.7 KB (338710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c13331aba23eb23da2064499c081c6c3a520fd7f7ffb5ddb550936bff241a9`  
		Last Modified: Tue, 23 Jun 2026 23:33:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa8af252651ec950c2e762b7b6be36b2607e24b082a1ea8eda27e848e4bf461`  
		Last Modified: Tue, 23 Jun 2026 23:33:41 GMT  
		Size: 110.5 MB (110474604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3ca67ecc05254da1956d0294bae75089e9baeaae4b55a4040cf2104523569e`  
		Last Modified: Tue, 23 Jun 2026 23:33:39 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc2ad2ae49d30c206b47a550edbfdb8f272d4655f1df57ff2a325879200801c`  
		Last Modified: Tue, 23 Jun 2026 23:33:39 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ba0691351b5030d43fcf1ba78d55b5379ab91823c2196eabf6e913e9730452`  
		Last Modified: Tue, 23 Jun 2026 23:33:40 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6ceb85a9d500a56bae2f07da226dcfe1b0205fa0376ee99bab8cc3d7dfa6da`  
		Last Modified: Tue, 23 Jun 2026 23:33:40 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:415c6f64ce0b44c20e9a1df07f92ca185b56638dacb503c74820fadf51f1fab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:420cd8298ed3cfb7b0358d7b5d372573c7432bb6ddc7e9e996a25dfd75e3df71`

```dockerfile
```

-	Layers:
	-	`sha256:772fe5e4c62244afd01871715e0219380812c7045c0eebdf7c9f304cd4cacc10`  
		Last Modified: Tue, 23 Jun 2026 23:33:38 GMT  
		Size: 4.2 MB (4180697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870cc7123fb12633ccff3283c814b3d934e261eb18435e57a2948acf80e2829c`  
		Last Modified: Tue, 23 Jun 2026 23:33:37 GMT  
		Size: 31.9 KB (31882 bytes)  
		MIME: application/vnd.in-toto+json
