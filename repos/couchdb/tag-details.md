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
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:3`

```console
$ docker pull couchdb@sha256:3d084addff475d306e649594c0c160e15061288ea7cebf7aee7423201ccd1137
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:5f9dcb2e080ddab04c951d4437fe64a1a2e6a3be5ffbc77fb114a92da1d5158c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148846120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:675fb3d5555a6f5372c57f035f5a4a98260fd9e72d7866efb6ed0a47f0b5fd21`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:42:54 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jun 2026 00:42:54 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Thu, 11 Jun 2026 00:43:02 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:43:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Thu, 11 Jun 2026 00:43:06 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jun 2026 00:43:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:43:13 GMT
ENV COUCHDB_VERSION=3.5.2
# Thu, 11 Jun 2026 00:43:13 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Thu, 11 Jun 2026 00:43:28 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~trixie     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
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
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1d781db0e1cdbc0aebbf1d80d0f40b9ef74a2544e17720eea6edc50c6d2355`  
		Last Modified: Thu, 11 Jun 2026 00:43:42 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f8ddc7a400b99a132b35f260a127243ebfe9a2c5e80c79c4503557740ad514`  
		Last Modified: Thu, 11 Jun 2026 00:43:42 GMT  
		Size: 7.5 MB (7492010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d831eb5e99dd311231b6fb79196f1b682bcf82bab8b6eed8fd237102318bf6a0`  
		Last Modified: Thu, 11 Jun 2026 00:43:42 GMT  
		Size: 417.6 KB (417616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a9910738c763170c58834d0ce32b973fac4943b2470bdcb53d5a16daed6321`  
		Last Modified: Thu, 11 Jun 2026 00:43:42 GMT  
		Size: 338.6 KB (338624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37674aeaa1f920ad10223f237fd5411b99bb71f8fb9f8b19c36fdb13dcb84c9`  
		Last Modified: Thu, 11 Jun 2026 00:43:43 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9aff9d3aa9a205f46637e218bdeef355b200c33f4296ef48a1b7d806d53ffc`  
		Last Modified: Thu, 11 Jun 2026 00:43:46 GMT  
		Size: 110.8 MB (110807025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f9cd77abbeda6312101be60c5e5be4647ffa0760d0b3612ffddf59bb611da1`  
		Last Modified: Thu, 11 Jun 2026 00:43:44 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff672fb8de87613e25041cbebbc84f90c37b5e38b31b7d1269e371e496390808`  
		Last Modified: Thu, 11 Jun 2026 00:43:44 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5709330a98af03a764f21538ecd51b88b89b98fd0600dabf805a07b9226ab298`  
		Last Modified: Thu, 11 Jun 2026 00:43:45 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed666a0774bd5bd363c91d41a8e84e4460d801515ae9f222e97d1e71c511d801`  
		Last Modified: Thu, 11 Jun 2026 00:43:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:75dd47cf81914bcc3a82ed478b6e4a16adbc7ed35350e55c913f196bec0597cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4211734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb1d577108fde5a9594d815b710521243483ded40d967289eea941e570a8c45`

```dockerfile
```

-	Layers:
	-	`sha256:bb2cb492a16b1fcc92c3fc314339ca47e6c314bbfbe21e71ba995e42be2700e8`  
		Last Modified: Thu, 11 Jun 2026 00:43:42 GMT  
		Size: 4.2 MB (4180083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:946e2936ddd0603ef6079d0877092ee0c42bb527f3397dc992426e37afe421dc`  
		Last Modified: Thu, 11 Jun 2026 00:43:42 GMT  
		Size: 31.7 KB (31651 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:78c4036ec121ba774d6699dc2517b52a67153a6b3c06d6e7c549eb400fb74daf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148614280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca5752e437aedae64cc52ad592666e5a19a4b1235485f6a4891bc1c801ec0db2`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:44:32 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jun 2026 00:44:32 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Thu, 11 Jun 2026 00:44:41 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:44:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Thu, 11 Jun 2026 00:44:44 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jun 2026 00:44:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:44:51 GMT
ENV COUCHDB_VERSION=3.5.2
# Thu, 11 Jun 2026 00:44:52 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Thu, 11 Jun 2026 00:45:06 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~trixie     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 11 Jun 2026 00:45:06 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Thu, 11 Jun 2026 00:45:07 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Thu, 11 Jun 2026 00:45:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 11 Jun 2026 00:45:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:45:07 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:45:07 GMT
VOLUME [/opt/couchdb/data]
# Thu, 11 Jun 2026 00:45:07 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Thu, 11 Jun 2026 00:45:07 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b9104d73cec8347a19fb7db9056f21d499e57c12c82b034ab3266101d9207f`  
		Last Modified: Thu, 11 Jun 2026 00:45:20 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8819ed9e59187e835b62a37ad432562ce05bd573daf0261a1f4d8b505272bb`  
		Last Modified: Thu, 11 Jun 2026 00:45:21 GMT  
		Size: 7.3 MB (7261125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0564d3bbb152054f80a86c02872c5319a1b62727a6d30d4e1e741651378a279a`  
		Last Modified: Thu, 11 Jun 2026 00:45:21 GMT  
		Size: 382.6 KB (382571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce8f5227c8bb521bb3e8f44a872061703763873f4e595d2b7ef7fc47f8ad4e8`  
		Last Modified: Thu, 11 Jun 2026 00:45:21 GMT  
		Size: 338.7 KB (338713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e1548decefcbcbaa52e4514bceac186a27eb505f91670a76f24787f7e516c1`  
		Last Modified: Thu, 11 Jun 2026 00:45:22 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d8808404f8b51556697245351a51c8b0b99c19c95efad8f648f227294a4b4c`  
		Last Modified: Thu, 11 Jun 2026 00:45:25 GMT  
		Size: 110.5 MB (110477914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64b970cb404cbac590e7bad6ad2a2c96371431b62d437b48f67279644e9cdd3`  
		Last Modified: Thu, 11 Jun 2026 00:45:22 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e451ee86eb7c61a884631cb5a52dc316f451e170345a3ae3fffcbcf9a968792`  
		Last Modified: Thu, 11 Jun 2026 00:45:22 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0973272edd9ec7ce523b1d8e81521ab46ce47e95044005a736d815de1e1d8c27`  
		Last Modified: Thu, 11 Jun 2026 00:45:23 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712b1861067e4aebbd89e742b72ee5b3c32b80caff079ccf4998d8eefdc182db`  
		Last Modified: Thu, 11 Jun 2026 00:45:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:cefcc9c17e55f5c87dc150af08e84c8e35986ce88356055e3ff2cd2be24be513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a286a4a14c41fbb697d7c83a968c4fcaf02177018b761cd5e419380c6a3659`

```dockerfile
```

-	Layers:
	-	`sha256:0057c8c85de0ee5be5e18e1db0803e02c653f010e2b583e7b14890066e2a141c`  
		Last Modified: Thu, 11 Jun 2026 00:45:21 GMT  
		Size: 4.2 MB (4180379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9eb58339b034bed59979e553483f47ffed311d6cd0e0531fcf33c86819485aae`  
		Last Modified: Thu, 11 Jun 2026 00:45:20 GMT  
		Size: 31.8 KB (31845 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:6b85de03c9a8cb0508a64b64b95b0225083072f36758b87aefde32ea617600f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:cfefbfc0f227c757b98655b871bff11739fa77214aa039b3905e649728ed744d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150900751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b015e75deb3ae0a8375e2eb9acf563fb2212d81b8148e07b7629658c171cb6c1`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:42:58 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jun 2026 00:42:58 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Thu, 11 Jun 2026 00:43:06 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:43:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-21-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:43:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Thu, 11 Jun 2026 00:43:15 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jun 2026 00:43:20 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:43:20 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ trixie main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Thu, 11 Jun 2026 00:43:26 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.2~trixie;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Thu, 11 Jun 2026 00:43:26 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Thu, 11 Jun 2026 00:43:26 GMT
VOLUME [/opt/nouveau/data]
# Thu, 11 Jun 2026 00:43:26 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Thu, 11 Jun 2026 00:43:26 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b18b80571a2deb6db871472e35d6e1a830783fbd0b42e9ea9935d0828e97f0`  
		Last Modified: Thu, 11 Jun 2026 00:43:40 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f007b9e296d8715c6e0be565425770469299b3b1305efa642b242b736898b0`  
		Last Modified: Thu, 11 Jun 2026 00:43:41 GMT  
		Size: 7.5 MB (7492043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b4ff41b57edc67d42b6924ade565ef103521347e2a25241ecf7af892866d90`  
		Last Modified: Thu, 11 Jun 2026 00:43:42 GMT  
		Size: 70.0 MB (70032466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a883c6cfe25a6d7444b7bc546f10fefc7d52c5d1bdecdd48ee0113f5888d2d1`  
		Last Modified: Thu, 11 Jun 2026 00:43:41 GMT  
		Size: 426.0 KB (425960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8eb1c4c6b3ca01813e8eef8a28e16c4afb332223731429df8167e33b49345d8`  
		Last Modified: Thu, 11 Jun 2026 00:43:42 GMT  
		Size: 347.4 KB (347398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f86874e6d7168063282813e35bc2e58e904c2348228ddca029c0db26948e9ab`  
		Last Modified: Thu, 11 Jun 2026 00:43:42 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d77b7ddf811814f3fba786f81ff3935a00d15910234f5f33d3eb698d093a9d`  
		Last Modified: Thu, 11 Jun 2026 00:43:43 GMT  
		Size: 42.8 MB (42815594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86d5b78321f52d7fdb8ed2cefeb60cafe93044d681b9a639e9cf781bccf28dc`  
		Last Modified: Thu, 11 Jun 2026 00:43:43 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:a0c8fd1f8d35ee1d0a78536a9daf1a8f24ba2d5a3e46fb0188e994ba4730963e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3388759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b48b5aabc36b56625b9fc0027362ee623ab28fce8957511638b3f6a2df16fc`

```dockerfile
```

-	Layers:
	-	`sha256:13ab2990cdecc071a352846fa36aefe00eba620f35b7359de9427a52af54b07e`  
		Last Modified: Thu, 11 Jun 2026 00:43:41 GMT  
		Size: 3.4 MB (3364329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a29d1d2afa0492d771e4e1a8b1868eb3b91fa0391dd9e8e5032b8082665b388a`  
		Last Modified: Thu, 11 Jun 2026 00:43:40 GMT  
		Size: 24.4 KB (24430 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:fa61bcb1f79728aeadda41820c2c0f1c6ec5d67ead0775a43f72f72e7ca84892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150060784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81bb5653d40b7c64e7db4019214e1acef85b6950f1482f8c2021b9b97141e1d`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:44:39 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jun 2026 00:44:39 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Thu, 11 Jun 2026 00:44:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:44:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-21-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:44:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Thu, 11 Jun 2026 00:44:56 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jun 2026 00:45:02 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:02 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ trixie main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Thu, 11 Jun 2026 00:45:09 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.2~trixie;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Thu, 11 Jun 2026 00:45:09 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Thu, 11 Jun 2026 00:45:09 GMT
VOLUME [/opt/nouveau/data]
# Thu, 11 Jun 2026 00:45:09 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Thu, 11 Jun 2026 00:45:09 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62d4c2d254daeba1981b8a15040a842517ad6445132d22dbc03517304e8235b`  
		Last Modified: Thu, 11 Jun 2026 00:45:23 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e41f5c6d8a0fb14e5cc7da77d32bd0071aab46b635afaa63293799f65ebf8a`  
		Last Modified: Thu, 11 Jun 2026 00:45:24 GMT  
		Size: 7.3 MB (7261140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a88fb5573c9bc228db799e20598d3ee11dcc46607a493a5b058eafec4ef940`  
		Last Modified: Thu, 11 Jun 2026 00:45:26 GMT  
		Size: 69.2 MB (69179732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b04f0c0a56cf14174ee4029ec590b112a28402f5a038ae3534b26c6d337ce8`  
		Last Modified: Thu, 11 Jun 2026 00:45:23 GMT  
		Size: 390.2 KB (390242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8217e819d46f24950d242e27a92e980ca6d468d5e23c76bb9232f4980af196`  
		Last Modified: Thu, 11 Jun 2026 00:45:25 GMT  
		Size: 347.4 KB (347381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbfb0fb7555745ce7b7d12a8d06bf074d68e838269c0a7eff22b709d27710b9b`  
		Last Modified: Thu, 11 Jun 2026 00:45:25 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48b7285cee155f51cbc0e33672d6a50347dfbee2377ada3909e3ee2b5e36249`  
		Last Modified: Thu, 11 Jun 2026 00:45:27 GMT  
		Size: 42.7 MB (42731881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3433d4d1ee639f44994d46267971d935c6d841371a93040c90f368d2aadf47`  
		Last Modified: Thu, 11 Jun 2026 00:45:26 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:60da35351d7600c61aefc7d511fb6269fbb8f86085148a27705baea0aa6471fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3387582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb58c3c7978714eba602aa409909f02f4d196f89424300e95d59ecb0a15b1dba`

```dockerfile
```

-	Layers:
	-	`sha256:ef5c03dcadb3b46b87cb383c9c3a224a2ac9e8d13820f9d3d5c5fc992c212688`  
		Last Modified: Thu, 11 Jun 2026 00:45:24 GMT  
		Size: 3.4 MB (3362970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2062c03a7482ebf9d2739b431cf77442bce67dc163c9f9ac9d732a6e9913516`  
		Last Modified: Thu, 11 Jun 2026 00:45:23 GMT  
		Size: 24.6 KB (24612 bytes)  
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
$ docker pull couchdb@sha256:3d084addff475d306e649594c0c160e15061288ea7cebf7aee7423201ccd1137
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.5` - linux; amd64

```console
$ docker pull couchdb@sha256:5f9dcb2e080ddab04c951d4437fe64a1a2e6a3be5ffbc77fb114a92da1d5158c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148846120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:675fb3d5555a6f5372c57f035f5a4a98260fd9e72d7866efb6ed0a47f0b5fd21`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:42:54 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jun 2026 00:42:54 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Thu, 11 Jun 2026 00:43:02 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:43:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Thu, 11 Jun 2026 00:43:06 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jun 2026 00:43:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:43:13 GMT
ENV COUCHDB_VERSION=3.5.2
# Thu, 11 Jun 2026 00:43:13 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Thu, 11 Jun 2026 00:43:28 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~trixie     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
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
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1d781db0e1cdbc0aebbf1d80d0f40b9ef74a2544e17720eea6edc50c6d2355`  
		Last Modified: Thu, 11 Jun 2026 00:43:42 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f8ddc7a400b99a132b35f260a127243ebfe9a2c5e80c79c4503557740ad514`  
		Last Modified: Thu, 11 Jun 2026 00:43:42 GMT  
		Size: 7.5 MB (7492010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d831eb5e99dd311231b6fb79196f1b682bcf82bab8b6eed8fd237102318bf6a0`  
		Last Modified: Thu, 11 Jun 2026 00:43:42 GMT  
		Size: 417.6 KB (417616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a9910738c763170c58834d0ce32b973fac4943b2470bdcb53d5a16daed6321`  
		Last Modified: Thu, 11 Jun 2026 00:43:42 GMT  
		Size: 338.6 KB (338624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37674aeaa1f920ad10223f237fd5411b99bb71f8fb9f8b19c36fdb13dcb84c9`  
		Last Modified: Thu, 11 Jun 2026 00:43:43 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9aff9d3aa9a205f46637e218bdeef355b200c33f4296ef48a1b7d806d53ffc`  
		Last Modified: Thu, 11 Jun 2026 00:43:46 GMT  
		Size: 110.8 MB (110807025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f9cd77abbeda6312101be60c5e5be4647ffa0760d0b3612ffddf59bb611da1`  
		Last Modified: Thu, 11 Jun 2026 00:43:44 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff672fb8de87613e25041cbebbc84f90c37b5e38b31b7d1269e371e496390808`  
		Last Modified: Thu, 11 Jun 2026 00:43:44 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5709330a98af03a764f21538ecd51b88b89b98fd0600dabf805a07b9226ab298`  
		Last Modified: Thu, 11 Jun 2026 00:43:45 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed666a0774bd5bd363c91d41a8e84e4460d801515ae9f222e97d1e71c511d801`  
		Last Modified: Thu, 11 Jun 2026 00:43:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:75dd47cf81914bcc3a82ed478b6e4a16adbc7ed35350e55c913f196bec0597cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4211734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb1d577108fde5a9594d815b710521243483ded40d967289eea941e570a8c45`

```dockerfile
```

-	Layers:
	-	`sha256:bb2cb492a16b1fcc92c3fc314339ca47e6c314bbfbe21e71ba995e42be2700e8`  
		Last Modified: Thu, 11 Jun 2026 00:43:42 GMT  
		Size: 4.2 MB (4180083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:946e2936ddd0603ef6079d0877092ee0c42bb527f3397dc992426e37afe421dc`  
		Last Modified: Thu, 11 Jun 2026 00:43:42 GMT  
		Size: 31.7 KB (31651 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:78c4036ec121ba774d6699dc2517b52a67153a6b3c06d6e7c549eb400fb74daf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148614280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca5752e437aedae64cc52ad592666e5a19a4b1235485f6a4891bc1c801ec0db2`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:44:32 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jun 2026 00:44:32 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Thu, 11 Jun 2026 00:44:41 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:44:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Thu, 11 Jun 2026 00:44:44 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jun 2026 00:44:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:44:51 GMT
ENV COUCHDB_VERSION=3.5.2
# Thu, 11 Jun 2026 00:44:52 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Thu, 11 Jun 2026 00:45:06 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~trixie     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 11 Jun 2026 00:45:06 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Thu, 11 Jun 2026 00:45:07 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Thu, 11 Jun 2026 00:45:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 11 Jun 2026 00:45:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:45:07 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:45:07 GMT
VOLUME [/opt/couchdb/data]
# Thu, 11 Jun 2026 00:45:07 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Thu, 11 Jun 2026 00:45:07 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b9104d73cec8347a19fb7db9056f21d499e57c12c82b034ab3266101d9207f`  
		Last Modified: Thu, 11 Jun 2026 00:45:20 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8819ed9e59187e835b62a37ad432562ce05bd573daf0261a1f4d8b505272bb`  
		Last Modified: Thu, 11 Jun 2026 00:45:21 GMT  
		Size: 7.3 MB (7261125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0564d3bbb152054f80a86c02872c5319a1b62727a6d30d4e1e741651378a279a`  
		Last Modified: Thu, 11 Jun 2026 00:45:21 GMT  
		Size: 382.6 KB (382571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce8f5227c8bb521bb3e8f44a872061703763873f4e595d2b7ef7fc47f8ad4e8`  
		Last Modified: Thu, 11 Jun 2026 00:45:21 GMT  
		Size: 338.7 KB (338713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e1548decefcbcbaa52e4514bceac186a27eb505f91670a76f24787f7e516c1`  
		Last Modified: Thu, 11 Jun 2026 00:45:22 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d8808404f8b51556697245351a51c8b0b99c19c95efad8f648f227294a4b4c`  
		Last Modified: Thu, 11 Jun 2026 00:45:25 GMT  
		Size: 110.5 MB (110477914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64b970cb404cbac590e7bad6ad2a2c96371431b62d437b48f67279644e9cdd3`  
		Last Modified: Thu, 11 Jun 2026 00:45:22 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e451ee86eb7c61a884631cb5a52dc316f451e170345a3ae3fffcbcf9a968792`  
		Last Modified: Thu, 11 Jun 2026 00:45:22 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0973272edd9ec7ce523b1d8e81521ab46ce47e95044005a736d815de1e1d8c27`  
		Last Modified: Thu, 11 Jun 2026 00:45:23 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712b1861067e4aebbd89e742b72ee5b3c32b80caff079ccf4998d8eefdc182db`  
		Last Modified: Thu, 11 Jun 2026 00:45:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:cefcc9c17e55f5c87dc150af08e84c8e35986ce88356055e3ff2cd2be24be513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a286a4a14c41fbb697d7c83a968c4fcaf02177018b761cd5e419380c6a3659`

```dockerfile
```

-	Layers:
	-	`sha256:0057c8c85de0ee5be5e18e1db0803e02c653f010e2b583e7b14890066e2a141c`  
		Last Modified: Thu, 11 Jun 2026 00:45:21 GMT  
		Size: 4.2 MB (4180379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9eb58339b034bed59979e553483f47ffed311d6cd0e0531fcf33c86819485aae`  
		Last Modified: Thu, 11 Jun 2026 00:45:20 GMT  
		Size: 31.8 KB (31845 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5-nouveau`

```console
$ docker pull couchdb@sha256:6b85de03c9a8cb0508a64b64b95b0225083072f36758b87aefde32ea617600f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.5-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:cfefbfc0f227c757b98655b871bff11739fa77214aa039b3905e649728ed744d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150900751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b015e75deb3ae0a8375e2eb9acf563fb2212d81b8148e07b7629658c171cb6c1`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:42:58 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jun 2026 00:42:58 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Thu, 11 Jun 2026 00:43:06 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:43:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-21-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:43:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Thu, 11 Jun 2026 00:43:15 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jun 2026 00:43:20 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:43:20 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ trixie main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Thu, 11 Jun 2026 00:43:26 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.2~trixie;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Thu, 11 Jun 2026 00:43:26 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Thu, 11 Jun 2026 00:43:26 GMT
VOLUME [/opt/nouveau/data]
# Thu, 11 Jun 2026 00:43:26 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Thu, 11 Jun 2026 00:43:26 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b18b80571a2deb6db871472e35d6e1a830783fbd0b42e9ea9935d0828e97f0`  
		Last Modified: Thu, 11 Jun 2026 00:43:40 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f007b9e296d8715c6e0be565425770469299b3b1305efa642b242b736898b0`  
		Last Modified: Thu, 11 Jun 2026 00:43:41 GMT  
		Size: 7.5 MB (7492043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b4ff41b57edc67d42b6924ade565ef103521347e2a25241ecf7af892866d90`  
		Last Modified: Thu, 11 Jun 2026 00:43:42 GMT  
		Size: 70.0 MB (70032466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a883c6cfe25a6d7444b7bc546f10fefc7d52c5d1bdecdd48ee0113f5888d2d1`  
		Last Modified: Thu, 11 Jun 2026 00:43:41 GMT  
		Size: 426.0 KB (425960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8eb1c4c6b3ca01813e8eef8a28e16c4afb332223731429df8167e33b49345d8`  
		Last Modified: Thu, 11 Jun 2026 00:43:42 GMT  
		Size: 347.4 KB (347398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f86874e6d7168063282813e35bc2e58e904c2348228ddca029c0db26948e9ab`  
		Last Modified: Thu, 11 Jun 2026 00:43:42 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d77b7ddf811814f3fba786f81ff3935a00d15910234f5f33d3eb698d093a9d`  
		Last Modified: Thu, 11 Jun 2026 00:43:43 GMT  
		Size: 42.8 MB (42815594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86d5b78321f52d7fdb8ed2cefeb60cafe93044d681b9a639e9cf781bccf28dc`  
		Last Modified: Thu, 11 Jun 2026 00:43:43 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:a0c8fd1f8d35ee1d0a78536a9daf1a8f24ba2d5a3e46fb0188e994ba4730963e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3388759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b48b5aabc36b56625b9fc0027362ee623ab28fce8957511638b3f6a2df16fc`

```dockerfile
```

-	Layers:
	-	`sha256:13ab2990cdecc071a352846fa36aefe00eba620f35b7359de9427a52af54b07e`  
		Last Modified: Thu, 11 Jun 2026 00:43:41 GMT  
		Size: 3.4 MB (3364329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a29d1d2afa0492d771e4e1a8b1868eb3b91fa0391dd9e8e5032b8082665b388a`  
		Last Modified: Thu, 11 Jun 2026 00:43:40 GMT  
		Size: 24.4 KB (24430 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:fa61bcb1f79728aeadda41820c2c0f1c6ec5d67ead0775a43f72f72e7ca84892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150060784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81bb5653d40b7c64e7db4019214e1acef85b6950f1482f8c2021b9b97141e1d`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:44:39 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jun 2026 00:44:39 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Thu, 11 Jun 2026 00:44:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:44:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-21-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:44:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Thu, 11 Jun 2026 00:44:56 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jun 2026 00:45:02 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:02 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ trixie main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Thu, 11 Jun 2026 00:45:09 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.2~trixie;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Thu, 11 Jun 2026 00:45:09 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Thu, 11 Jun 2026 00:45:09 GMT
VOLUME [/opt/nouveau/data]
# Thu, 11 Jun 2026 00:45:09 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Thu, 11 Jun 2026 00:45:09 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62d4c2d254daeba1981b8a15040a842517ad6445132d22dbc03517304e8235b`  
		Last Modified: Thu, 11 Jun 2026 00:45:23 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e41f5c6d8a0fb14e5cc7da77d32bd0071aab46b635afaa63293799f65ebf8a`  
		Last Modified: Thu, 11 Jun 2026 00:45:24 GMT  
		Size: 7.3 MB (7261140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a88fb5573c9bc228db799e20598d3ee11dcc46607a493a5b058eafec4ef940`  
		Last Modified: Thu, 11 Jun 2026 00:45:26 GMT  
		Size: 69.2 MB (69179732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b04f0c0a56cf14174ee4029ec590b112a28402f5a038ae3534b26c6d337ce8`  
		Last Modified: Thu, 11 Jun 2026 00:45:23 GMT  
		Size: 390.2 KB (390242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8217e819d46f24950d242e27a92e980ca6d468d5e23c76bb9232f4980af196`  
		Last Modified: Thu, 11 Jun 2026 00:45:25 GMT  
		Size: 347.4 KB (347381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbfb0fb7555745ce7b7d12a8d06bf074d68e838269c0a7eff22b709d27710b9b`  
		Last Modified: Thu, 11 Jun 2026 00:45:25 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48b7285cee155f51cbc0e33672d6a50347dfbee2377ada3909e3ee2b5e36249`  
		Last Modified: Thu, 11 Jun 2026 00:45:27 GMT  
		Size: 42.7 MB (42731881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3433d4d1ee639f44994d46267971d935c6d841371a93040c90f368d2aadf47`  
		Last Modified: Thu, 11 Jun 2026 00:45:26 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:60da35351d7600c61aefc7d511fb6269fbb8f86085148a27705baea0aa6471fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3387582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb58c3c7978714eba602aa409909f02f4d196f89424300e95d59ecb0a15b1dba`

```dockerfile
```

-	Layers:
	-	`sha256:ef5c03dcadb3b46b87cb383c9c3a224a2ac9e8d13820f9d3d5c5fc992c212688`  
		Last Modified: Thu, 11 Jun 2026 00:45:24 GMT  
		Size: 3.4 MB (3362970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2062c03a7482ebf9d2739b431cf77442bce67dc163c9f9ac9d732a6e9913516`  
		Last Modified: Thu, 11 Jun 2026 00:45:23 GMT  
		Size: 24.6 KB (24612 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.2`

```console
$ docker pull couchdb@sha256:3d084addff475d306e649594c0c160e15061288ea7cebf7aee7423201ccd1137
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.5.2` - linux; amd64

```console
$ docker pull couchdb@sha256:5f9dcb2e080ddab04c951d4437fe64a1a2e6a3be5ffbc77fb114a92da1d5158c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148846120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:675fb3d5555a6f5372c57f035f5a4a98260fd9e72d7866efb6ed0a47f0b5fd21`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:42:54 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jun 2026 00:42:54 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Thu, 11 Jun 2026 00:43:02 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:43:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Thu, 11 Jun 2026 00:43:06 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jun 2026 00:43:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:43:13 GMT
ENV COUCHDB_VERSION=3.5.2
# Thu, 11 Jun 2026 00:43:13 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Thu, 11 Jun 2026 00:43:28 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~trixie     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
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
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1d781db0e1cdbc0aebbf1d80d0f40b9ef74a2544e17720eea6edc50c6d2355`  
		Last Modified: Thu, 11 Jun 2026 00:43:42 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f8ddc7a400b99a132b35f260a127243ebfe9a2c5e80c79c4503557740ad514`  
		Last Modified: Thu, 11 Jun 2026 00:43:42 GMT  
		Size: 7.5 MB (7492010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d831eb5e99dd311231b6fb79196f1b682bcf82bab8b6eed8fd237102318bf6a0`  
		Last Modified: Thu, 11 Jun 2026 00:43:42 GMT  
		Size: 417.6 KB (417616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a9910738c763170c58834d0ce32b973fac4943b2470bdcb53d5a16daed6321`  
		Last Modified: Thu, 11 Jun 2026 00:43:42 GMT  
		Size: 338.6 KB (338624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37674aeaa1f920ad10223f237fd5411b99bb71f8fb9f8b19c36fdb13dcb84c9`  
		Last Modified: Thu, 11 Jun 2026 00:43:43 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9aff9d3aa9a205f46637e218bdeef355b200c33f4296ef48a1b7d806d53ffc`  
		Last Modified: Thu, 11 Jun 2026 00:43:46 GMT  
		Size: 110.8 MB (110807025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f9cd77abbeda6312101be60c5e5be4647ffa0760d0b3612ffddf59bb611da1`  
		Last Modified: Thu, 11 Jun 2026 00:43:44 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff672fb8de87613e25041cbebbc84f90c37b5e38b31b7d1269e371e496390808`  
		Last Modified: Thu, 11 Jun 2026 00:43:44 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5709330a98af03a764f21538ecd51b88b89b98fd0600dabf805a07b9226ab298`  
		Last Modified: Thu, 11 Jun 2026 00:43:45 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed666a0774bd5bd363c91d41a8e84e4460d801515ae9f222e97d1e71c511d801`  
		Last Modified: Thu, 11 Jun 2026 00:43:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:75dd47cf81914bcc3a82ed478b6e4a16adbc7ed35350e55c913f196bec0597cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4211734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb1d577108fde5a9594d815b710521243483ded40d967289eea941e570a8c45`

```dockerfile
```

-	Layers:
	-	`sha256:bb2cb492a16b1fcc92c3fc314339ca47e6c314bbfbe21e71ba995e42be2700e8`  
		Last Modified: Thu, 11 Jun 2026 00:43:42 GMT  
		Size: 4.2 MB (4180083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:946e2936ddd0603ef6079d0877092ee0c42bb527f3397dc992426e37afe421dc`  
		Last Modified: Thu, 11 Jun 2026 00:43:42 GMT  
		Size: 31.7 KB (31651 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:78c4036ec121ba774d6699dc2517b52a67153a6b3c06d6e7c549eb400fb74daf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148614280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca5752e437aedae64cc52ad592666e5a19a4b1235485f6a4891bc1c801ec0db2`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:44:32 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jun 2026 00:44:32 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Thu, 11 Jun 2026 00:44:41 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:44:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Thu, 11 Jun 2026 00:44:44 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jun 2026 00:44:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:44:51 GMT
ENV COUCHDB_VERSION=3.5.2
# Thu, 11 Jun 2026 00:44:52 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Thu, 11 Jun 2026 00:45:06 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~trixie     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 11 Jun 2026 00:45:06 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Thu, 11 Jun 2026 00:45:07 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Thu, 11 Jun 2026 00:45:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 11 Jun 2026 00:45:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:45:07 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:45:07 GMT
VOLUME [/opt/couchdb/data]
# Thu, 11 Jun 2026 00:45:07 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Thu, 11 Jun 2026 00:45:07 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b9104d73cec8347a19fb7db9056f21d499e57c12c82b034ab3266101d9207f`  
		Last Modified: Thu, 11 Jun 2026 00:45:20 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8819ed9e59187e835b62a37ad432562ce05bd573daf0261a1f4d8b505272bb`  
		Last Modified: Thu, 11 Jun 2026 00:45:21 GMT  
		Size: 7.3 MB (7261125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0564d3bbb152054f80a86c02872c5319a1b62727a6d30d4e1e741651378a279a`  
		Last Modified: Thu, 11 Jun 2026 00:45:21 GMT  
		Size: 382.6 KB (382571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce8f5227c8bb521bb3e8f44a872061703763873f4e595d2b7ef7fc47f8ad4e8`  
		Last Modified: Thu, 11 Jun 2026 00:45:21 GMT  
		Size: 338.7 KB (338713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e1548decefcbcbaa52e4514bceac186a27eb505f91670a76f24787f7e516c1`  
		Last Modified: Thu, 11 Jun 2026 00:45:22 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d8808404f8b51556697245351a51c8b0b99c19c95efad8f648f227294a4b4c`  
		Last Modified: Thu, 11 Jun 2026 00:45:25 GMT  
		Size: 110.5 MB (110477914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64b970cb404cbac590e7bad6ad2a2c96371431b62d437b48f67279644e9cdd3`  
		Last Modified: Thu, 11 Jun 2026 00:45:22 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e451ee86eb7c61a884631cb5a52dc316f451e170345a3ae3fffcbcf9a968792`  
		Last Modified: Thu, 11 Jun 2026 00:45:22 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0973272edd9ec7ce523b1d8e81521ab46ce47e95044005a736d815de1e1d8c27`  
		Last Modified: Thu, 11 Jun 2026 00:45:23 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712b1861067e4aebbd89e742b72ee5b3c32b80caff079ccf4998d8eefdc182db`  
		Last Modified: Thu, 11 Jun 2026 00:45:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:cefcc9c17e55f5c87dc150af08e84c8e35986ce88356055e3ff2cd2be24be513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a286a4a14c41fbb697d7c83a968c4fcaf02177018b761cd5e419380c6a3659`

```dockerfile
```

-	Layers:
	-	`sha256:0057c8c85de0ee5be5e18e1db0803e02c653f010e2b583e7b14890066e2a141c`  
		Last Modified: Thu, 11 Jun 2026 00:45:21 GMT  
		Size: 4.2 MB (4180379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9eb58339b034bed59979e553483f47ffed311d6cd0e0531fcf33c86819485aae`  
		Last Modified: Thu, 11 Jun 2026 00:45:20 GMT  
		Size: 31.8 KB (31845 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.2-nouveau`

```console
$ docker pull couchdb@sha256:6b85de03c9a8cb0508a64b64b95b0225083072f36758b87aefde32ea617600f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.5.2-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:cfefbfc0f227c757b98655b871bff11739fa77214aa039b3905e649728ed744d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150900751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b015e75deb3ae0a8375e2eb9acf563fb2212d81b8148e07b7629658c171cb6c1`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:42:58 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jun 2026 00:42:58 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Thu, 11 Jun 2026 00:43:06 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:43:12 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-21-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:43:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Thu, 11 Jun 2026 00:43:15 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jun 2026 00:43:20 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:43:20 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ trixie main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Thu, 11 Jun 2026 00:43:26 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.2~trixie;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Thu, 11 Jun 2026 00:43:26 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Thu, 11 Jun 2026 00:43:26 GMT
VOLUME [/opt/nouveau/data]
# Thu, 11 Jun 2026 00:43:26 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Thu, 11 Jun 2026 00:43:26 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b18b80571a2deb6db871472e35d6e1a830783fbd0b42e9ea9935d0828e97f0`  
		Last Modified: Thu, 11 Jun 2026 00:43:40 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f007b9e296d8715c6e0be565425770469299b3b1305efa642b242b736898b0`  
		Last Modified: Thu, 11 Jun 2026 00:43:41 GMT  
		Size: 7.5 MB (7492043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b4ff41b57edc67d42b6924ade565ef103521347e2a25241ecf7af892866d90`  
		Last Modified: Thu, 11 Jun 2026 00:43:42 GMT  
		Size: 70.0 MB (70032466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a883c6cfe25a6d7444b7bc546f10fefc7d52c5d1bdecdd48ee0113f5888d2d1`  
		Last Modified: Thu, 11 Jun 2026 00:43:41 GMT  
		Size: 426.0 KB (425960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8eb1c4c6b3ca01813e8eef8a28e16c4afb332223731429df8167e33b49345d8`  
		Last Modified: Thu, 11 Jun 2026 00:43:42 GMT  
		Size: 347.4 KB (347398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f86874e6d7168063282813e35bc2e58e904c2348228ddca029c0db26948e9ab`  
		Last Modified: Thu, 11 Jun 2026 00:43:42 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d77b7ddf811814f3fba786f81ff3935a00d15910234f5f33d3eb698d093a9d`  
		Last Modified: Thu, 11 Jun 2026 00:43:43 GMT  
		Size: 42.8 MB (42815594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86d5b78321f52d7fdb8ed2cefeb60cafe93044d681b9a639e9cf781bccf28dc`  
		Last Modified: Thu, 11 Jun 2026 00:43:43 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.2-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:a0c8fd1f8d35ee1d0a78536a9daf1a8f24ba2d5a3e46fb0188e994ba4730963e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3388759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b48b5aabc36b56625b9fc0027362ee623ab28fce8957511638b3f6a2df16fc`

```dockerfile
```

-	Layers:
	-	`sha256:13ab2990cdecc071a352846fa36aefe00eba620f35b7359de9427a52af54b07e`  
		Last Modified: Thu, 11 Jun 2026 00:43:41 GMT  
		Size: 3.4 MB (3364329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a29d1d2afa0492d771e4e1a8b1868eb3b91fa0391dd9e8e5032b8082665b388a`  
		Last Modified: Thu, 11 Jun 2026 00:43:40 GMT  
		Size: 24.4 KB (24430 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.2-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:fa61bcb1f79728aeadda41820c2c0f1c6ec5d67ead0775a43f72f72e7ca84892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150060784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81bb5653d40b7c64e7db4019214e1acef85b6950f1482f8c2021b9b97141e1d`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:44:39 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jun 2026 00:44:39 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Thu, 11 Jun 2026 00:44:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:44:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-21-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:44:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Thu, 11 Jun 2026 00:44:56 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jun 2026 00:45:02 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:02 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ trixie main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Thu, 11 Jun 2026 00:45:09 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.2~trixie;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Thu, 11 Jun 2026 00:45:09 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Thu, 11 Jun 2026 00:45:09 GMT
VOLUME [/opt/nouveau/data]
# Thu, 11 Jun 2026 00:45:09 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Thu, 11 Jun 2026 00:45:09 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62d4c2d254daeba1981b8a15040a842517ad6445132d22dbc03517304e8235b`  
		Last Modified: Thu, 11 Jun 2026 00:45:23 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e41f5c6d8a0fb14e5cc7da77d32bd0071aab46b635afaa63293799f65ebf8a`  
		Last Modified: Thu, 11 Jun 2026 00:45:24 GMT  
		Size: 7.3 MB (7261140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a88fb5573c9bc228db799e20598d3ee11dcc46607a493a5b058eafec4ef940`  
		Last Modified: Thu, 11 Jun 2026 00:45:26 GMT  
		Size: 69.2 MB (69179732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b04f0c0a56cf14174ee4029ec590b112a28402f5a038ae3534b26c6d337ce8`  
		Last Modified: Thu, 11 Jun 2026 00:45:23 GMT  
		Size: 390.2 KB (390242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8217e819d46f24950d242e27a92e980ca6d468d5e23c76bb9232f4980af196`  
		Last Modified: Thu, 11 Jun 2026 00:45:25 GMT  
		Size: 347.4 KB (347381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbfb0fb7555745ce7b7d12a8d06bf074d68e838269c0a7eff22b709d27710b9b`  
		Last Modified: Thu, 11 Jun 2026 00:45:25 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48b7285cee155f51cbc0e33672d6a50347dfbee2377ada3909e3ee2b5e36249`  
		Last Modified: Thu, 11 Jun 2026 00:45:27 GMT  
		Size: 42.7 MB (42731881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3433d4d1ee639f44994d46267971d935c6d841371a93040c90f368d2aadf47`  
		Last Modified: Thu, 11 Jun 2026 00:45:26 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.2-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:60da35351d7600c61aefc7d511fb6269fbb8f86085148a27705baea0aa6471fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3387582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb58c3c7978714eba602aa409909f02f4d196f89424300e95d59ecb0a15b1dba`

```dockerfile
```

-	Layers:
	-	`sha256:ef5c03dcadb3b46b87cb383c9c3a224a2ac9e8d13820f9d3d5c5fc992c212688`  
		Last Modified: Thu, 11 Jun 2026 00:45:24 GMT  
		Size: 3.4 MB (3362970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2062c03a7482ebf9d2739b431cf77442bce67dc163c9f9ac9d732a6e9913516`  
		Last Modified: Thu, 11 Jun 2026 00:45:23 GMT  
		Size: 24.6 KB (24612 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:3d084addff475d306e649594c0c160e15061288ea7cebf7aee7423201ccd1137
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:5f9dcb2e080ddab04c951d4437fe64a1a2e6a3be5ffbc77fb114a92da1d5158c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148846120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:675fb3d5555a6f5372c57f035f5a4a98260fd9e72d7866efb6ed0a47f0b5fd21`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:42:54 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jun 2026 00:42:54 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Thu, 11 Jun 2026 00:43:02 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:43:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Thu, 11 Jun 2026 00:43:06 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jun 2026 00:43:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:43:13 GMT
ENV COUCHDB_VERSION=3.5.2
# Thu, 11 Jun 2026 00:43:13 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Thu, 11 Jun 2026 00:43:28 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~trixie     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
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
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1d781db0e1cdbc0aebbf1d80d0f40b9ef74a2544e17720eea6edc50c6d2355`  
		Last Modified: Thu, 11 Jun 2026 00:43:42 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f8ddc7a400b99a132b35f260a127243ebfe9a2c5e80c79c4503557740ad514`  
		Last Modified: Thu, 11 Jun 2026 00:43:42 GMT  
		Size: 7.5 MB (7492010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d831eb5e99dd311231b6fb79196f1b682bcf82bab8b6eed8fd237102318bf6a0`  
		Last Modified: Thu, 11 Jun 2026 00:43:42 GMT  
		Size: 417.6 KB (417616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a9910738c763170c58834d0ce32b973fac4943b2470bdcb53d5a16daed6321`  
		Last Modified: Thu, 11 Jun 2026 00:43:42 GMT  
		Size: 338.6 KB (338624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37674aeaa1f920ad10223f237fd5411b99bb71f8fb9f8b19c36fdb13dcb84c9`  
		Last Modified: Thu, 11 Jun 2026 00:43:43 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9aff9d3aa9a205f46637e218bdeef355b200c33f4296ef48a1b7d806d53ffc`  
		Last Modified: Thu, 11 Jun 2026 00:43:46 GMT  
		Size: 110.8 MB (110807025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f9cd77abbeda6312101be60c5e5be4647ffa0760d0b3612ffddf59bb611da1`  
		Last Modified: Thu, 11 Jun 2026 00:43:44 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff672fb8de87613e25041cbebbc84f90c37b5e38b31b7d1269e371e496390808`  
		Last Modified: Thu, 11 Jun 2026 00:43:44 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5709330a98af03a764f21538ecd51b88b89b98fd0600dabf805a07b9226ab298`  
		Last Modified: Thu, 11 Jun 2026 00:43:45 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed666a0774bd5bd363c91d41a8e84e4460d801515ae9f222e97d1e71c511d801`  
		Last Modified: Thu, 11 Jun 2026 00:43:44 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:75dd47cf81914bcc3a82ed478b6e4a16adbc7ed35350e55c913f196bec0597cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4211734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb1d577108fde5a9594d815b710521243483ded40d967289eea941e570a8c45`

```dockerfile
```

-	Layers:
	-	`sha256:bb2cb492a16b1fcc92c3fc314339ca47e6c314bbfbe21e71ba995e42be2700e8`  
		Last Modified: Thu, 11 Jun 2026 00:43:42 GMT  
		Size: 4.2 MB (4180083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:946e2936ddd0603ef6079d0877092ee0c42bb527f3397dc992426e37afe421dc`  
		Last Modified: Thu, 11 Jun 2026 00:43:42 GMT  
		Size: 31.7 KB (31651 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:78c4036ec121ba774d6699dc2517b52a67153a6b3c06d6e7c549eb400fb74daf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148614280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca5752e437aedae64cc52ad592666e5a19a4b1235485f6a4891bc1c801ec0db2`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:44:32 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jun 2026 00:44:32 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Thu, 11 Jun 2026 00:44:41 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:44:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Thu, 11 Jun 2026 00:44:44 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jun 2026 00:44:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:44:51 GMT
ENV COUCHDB_VERSION=3.5.2
# Thu, 11 Jun 2026 00:44:52 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Thu, 11 Jun 2026 00:45:06 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~trixie     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Thu, 11 Jun 2026 00:45:06 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Thu, 11 Jun 2026 00:45:07 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Thu, 11 Jun 2026 00:45:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 11 Jun 2026 00:45:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Thu, 11 Jun 2026 00:45:07 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:45:07 GMT
VOLUME [/opt/couchdb/data]
# Thu, 11 Jun 2026 00:45:07 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Thu, 11 Jun 2026 00:45:07 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b9104d73cec8347a19fb7db9056f21d499e57c12c82b034ab3266101d9207f`  
		Last Modified: Thu, 11 Jun 2026 00:45:20 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8819ed9e59187e835b62a37ad432562ce05bd573daf0261a1f4d8b505272bb`  
		Last Modified: Thu, 11 Jun 2026 00:45:21 GMT  
		Size: 7.3 MB (7261125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0564d3bbb152054f80a86c02872c5319a1b62727a6d30d4e1e741651378a279a`  
		Last Modified: Thu, 11 Jun 2026 00:45:21 GMT  
		Size: 382.6 KB (382571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce8f5227c8bb521bb3e8f44a872061703763873f4e595d2b7ef7fc47f8ad4e8`  
		Last Modified: Thu, 11 Jun 2026 00:45:21 GMT  
		Size: 338.7 KB (338713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e1548decefcbcbaa52e4514bceac186a27eb505f91670a76f24787f7e516c1`  
		Last Modified: Thu, 11 Jun 2026 00:45:22 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d8808404f8b51556697245351a51c8b0b99c19c95efad8f648f227294a4b4c`  
		Last Modified: Thu, 11 Jun 2026 00:45:25 GMT  
		Size: 110.5 MB (110477914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64b970cb404cbac590e7bad6ad2a2c96371431b62d437b48f67279644e9cdd3`  
		Last Modified: Thu, 11 Jun 2026 00:45:22 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e451ee86eb7c61a884631cb5a52dc316f451e170345a3ae3fffcbcf9a968792`  
		Last Modified: Thu, 11 Jun 2026 00:45:22 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0973272edd9ec7ce523b1d8e81521ab46ce47e95044005a736d815de1e1d8c27`  
		Last Modified: Thu, 11 Jun 2026 00:45:23 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712b1861067e4aebbd89e742b72ee5b3c32b80caff079ccf4998d8eefdc182db`  
		Last Modified: Thu, 11 Jun 2026 00:45:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:cefcc9c17e55f5c87dc150af08e84c8e35986ce88356055e3ff2cd2be24be513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a286a4a14c41fbb697d7c83a968c4fcaf02177018b761cd5e419380c6a3659`

```dockerfile
```

-	Layers:
	-	`sha256:0057c8c85de0ee5be5e18e1db0803e02c653f010e2b583e7b14890066e2a141c`  
		Last Modified: Thu, 11 Jun 2026 00:45:21 GMT  
		Size: 4.2 MB (4180379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9eb58339b034bed59979e553483f47ffed311d6cd0e0531fcf33c86819485aae`  
		Last Modified: Thu, 11 Jun 2026 00:45:20 GMT  
		Size: 31.8 KB (31845 bytes)  
		MIME: application/vnd.in-toto+json
