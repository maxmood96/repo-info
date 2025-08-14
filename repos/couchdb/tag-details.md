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
$ docker pull couchdb@sha256:432e99b1dbb8bd996b2af964b4731633956e9635548e82b037bda94bb1835193
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
$ docker pull couchdb@sha256:61b1f52d0853861f76353350a313289b31c2ee1b4804c1f6997074d8fcac7cd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139828882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6dbe6ebdaba35a59a45b23d5ce6a95b780604bbb7930465beef5725558681f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f51fa6c894ee9345fe0500a27ff388ecb72eabe2fe3b02d6edd3dc5b3350b93`  
		Last Modified: Tue, 12 Aug 2025 21:23:09 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764b70173c9e8ba1719c81377202f5f41a0420fae43271c3822ee720a613c396`  
		Last Modified: Tue, 12 Aug 2025 21:23:10 GMT  
		Size: 7.9 MB (7881552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6593eef0f94fd50f73d54db6bceb74c820fdaa4d0e2c9aee51d1afbd69b3f62e`  
		Last Modified: Tue, 12 Aug 2025 21:23:10 GMT  
		Size: 392.2 KB (392159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27598109e7c931cfd1cde74aa91bf06dc90e3ab15c837c242a01fb5c90d75f3e`  
		Last Modified: Tue, 12 Aug 2025 21:23:10 GMT  
		Size: 76.3 KB (76305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f674471e32b0c0267121748f62842811c187c1d308ce36cbf5697436e5727b72`  
		Last Modified: Tue, 12 Aug 2025 21:23:10 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3dc16bdec0642eb6c72e582680ee47bb502c5fbd7b2ddaeae7acf21dec07d51`  
		Last Modified: Tue, 12 Aug 2025 21:23:21 GMT  
		Size: 103.2 MB (103243184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75cbcfe770026e1e7036cf243a6b58d887661183d729bdffa652af37138f9f36`  
		Last Modified: Tue, 12 Aug 2025 21:23:10 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d750e10a43cb3769286b8f43be624ca1c41158ea9ea492a534148de3784a81`  
		Last Modified: Tue, 12 Aug 2025 21:23:10 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a114350064b8d1c007ae4c75d6ea1dfa2d9dcdf001b545a18c5083b27445c0`  
		Last Modified: Tue, 12 Aug 2025 21:23:11 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2090b99b69f9563438f44c6cfb8d0c9c55b293d66f6fb682dec49fa5cbb89af0`  
		Last Modified: Tue, 12 Aug 2025 21:23:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:6416bbb6b6baf528846e66900a2e9d6630b091c824bacebb800b8cb2a67336fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4170730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6af04829063d566a11789e76c7fcef29c85e001c106ec14c3efdd9865dd2a8`

```dockerfile
```

-	Layers:
	-	`sha256:f993f71f1e61426d80826a56f7b5044be5a4ca7aa7582f5d5cc145769198982d`  
		Last Modified: Wed, 13 Aug 2025 01:33:20 GMT  
		Size: 4.1 MB (4138949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:982abba7fef1ec1955de60a347341f458aeab3bf621264d1ce41dfdb38ee2913`  
		Last Modified: Wed, 13 Aug 2025 01:33:21 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:d4d661276bc55d6c7c97b92e1a692a06ff8db07bf9faef63722438cc11c93e15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139087709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:072f03e4437bff861b82d4ac70cfc6011b4f41d72ab741677a8d2efe213b54d3`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec13befd006fe986be6a8728105412886a583f41f71c6da9a69bcdafc5dca61a`  
		Last Modified: Wed, 13 Aug 2025 07:01:40 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d2aef50f2cd302839668b5ead9b50197b726f5dcab885cc3c48b47965bb73d`  
		Last Modified: Wed, 13 Aug 2025 07:01:41 GMT  
		Size: 7.7 MB (7671345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5301367e88b8bf291aa3e746da27aae27fca920b48b7ec9dce1e5a30e9ac85`  
		Last Modified: Wed, 13 Aug 2025 07:01:40 GMT  
		Size: 349.0 KB (349008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f67cda63d6c6f697113d856d3d51850bdca2557826056f6cc57d464cb605b4`  
		Last Modified: Wed, 13 Aug 2025 07:01:42 GMT  
		Size: 76.3 KB (76335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923cef98fe321ff8257c5ab2d2a257df741860e41a3a4874793e6cad524c5b4b`  
		Last Modified: Wed, 13 Aug 2025 07:01:42 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf41befbfe783db522e1c0f9273d8b3990e28c0ea994bccda5fa465b2377c93`  
		Last Modified: Wed, 13 Aug 2025 07:02:04 GMT  
		Size: 102.9 MB (102903580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb50d4b8156f07b71d73019935a3aee01a295f0c8d11efff59dacb5e0403dea`  
		Last Modified: Wed, 13 Aug 2025 07:01:36 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1d3615bc1b22a46b4b120f3cfa33d9921d4aca1e6575f8e57f41471a4b3c83`  
		Last Modified: Wed, 13 Aug 2025 07:01:36 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b50ca5361151149f77020482ac82c35cd96093e57456c10a50cd045674b2e2`  
		Last Modified: Wed, 13 Aug 2025 07:01:36 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b969e402096d53bed40bccd8c1b4492a774eb07ac9cfc390e7f16d99bc72a5b`  
		Last Modified: Wed, 13 Aug 2025 07:01:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:11252c508326fc8c25f42c580b0e2c55f29964f7261c2535cb86fd2bcf83d58a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4171217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d992e96908654319a7c0db09c8a678fea16da0a04d698bc9e1e7efd5acb93a`

```dockerfile
```

-	Layers:
	-	`sha256:0862edf1bc3bbd57fe812708c8c761759b6225d3c947158d0cdd755e6019ccfa`  
		Last Modified: Wed, 13 Aug 2025 07:33:23 GMT  
		Size: 4.1 MB (4139242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d3453eb326594daa4b8a25fcbcd3f70fa5c5dd2e143c24097ef3945c15a9ead`  
		Last Modified: Wed, 13 Aug 2025 07:33:23 GMT  
		Size: 32.0 KB (31975 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; s390x

```console
$ docker pull couchdb@sha256:e4a4fc9e58539d2868bd15e046780cd8d8b7a71a74c1eb9f555e22fdf9c0c86b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136521588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec4fca67cecb025b5c09cab9c9549cb681d94892aaf58073a27711545f702b5e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
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
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b7acab8e5e7b12089d79275ac325f69e00c57ef109efebab6c70c9cd73a40d`  
		Last Modified: Wed, 13 Aug 2025 15:09:36 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3abfab6aae8ef4c71d8ee0179a883e31407cdba29d7ec2aedcd6cf479dd3bf`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 7.4 MB (7397830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164187f5523648207c88c10beecff4fa873224418908ed2042111b9008220445`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 355.6 KB (355650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1ea234d9128aa5cf95bed7f6b642ed39541c3ce0421026891a6ae6c3a62cf6`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 76.3 KB (76347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d507f15e04c67e6c028ebaf9b70be03905c6b099f3280dc1ee5b6c61e54fb9`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b32a62c011f37d07095a847adb6849fc8b49b594312b80901dd3fa8730a8f14`  
		Last Modified: Wed, 13 Aug 2025 16:38:43 GMT  
		Size: 101.8 MB (101798492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021c7a0c08391ce264a34acc839e0c22ef3ae30cd5170382d429de2fd535dd89`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8e63f7118f360ea233b6a4b5bfe85601905a9f58ccd1f8e5bd49122797016e`  
		Last Modified: Wed, 13 Aug 2025 15:09:38 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c223e87672740895458e8f91f45b4a146badb15e846fc58f8860c7318a8ff3ab`  
		Last Modified: Wed, 13 Aug 2025 15:09:38 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317e7af7e41277224e9cbb8f9c30c37a3271c0df880f6cf92e4bb22db5ecefe2`  
		Last Modified: Wed, 13 Aug 2025 15:09:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:37f51edaf047cdf5f5111855683e13ea3c6672c8a15c2251ae5e354aae7a84a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4166926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36fa1cbb03efdd840bd2a162de1c1575a3bbbdb97b9d101b488ed2ce25e1f89`

```dockerfile
```

-	Layers:
	-	`sha256:66a48a697a343af104ea7f47a48904fb5b1d220938d9142743643f1b94344055`  
		Last Modified: Wed, 13 Aug 2025 16:33:26 GMT  
		Size: 4.1 MB (4135145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f50372cd52cb3fa8e4baf039bb58aa2c00bbb482d234fe623bfcf97bd2ac1f1`  
		Last Modified: Wed, 13 Aug 2025 16:33:27 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:308b04f6701f381607f7f47d7fb87aad8ed7ef45bb46801f2ebedebfae25008a
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
$ docker pull couchdb@sha256:8827e434487f67468be45e6638e7c262c202df39dab193f7a801d910337e1168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156388372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb51afec84a60b4ccca88637b6171dbf9c7bd64f5abbd8767fd148a8f7c83b86`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f790d8ace6bac688ec09887e051eca9bfb5dcec4060dbfa6e004dbd22c2335`  
		Last Modified: Tue, 12 Aug 2025 22:37:28 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa6399b477180c57907d82946e672511eca816592e7bde3ce7cbef0120d988c`  
		Last Modified: Wed, 13 Aug 2025 00:25:10 GMT  
		Size: 7.9 MB (7881623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a83b3d6009f4d95485272c64af79f09993fd79bf2642286b32d66b25f416bf`  
		Last Modified: Wed, 13 Aug 2025 00:25:20 GMT  
		Size: 77.3 MB (77324598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6505f4ba5ba4d521d87e5366d2ba43a91f994a54206091b2f9fe3bee5a92512f`  
		Last Modified: Tue, 12 Aug 2025 22:37:32 GMT  
		Size: 415.0 KB (415014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340137239ed9b3bc413c49b3966668ac8adb208cf72782ff5b6998c8c82b4275`  
		Last Modified: Tue, 12 Aug 2025 22:37:38 GMT  
		Size: 99.3 KB (99339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bfd6d48df450c319175586a5fc5f9d294e8b9451bc20ee8664c77abb7b7b74`  
		Last Modified: Tue, 12 Aug 2025 22:37:42 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b79bc1a224dbf16495d0825c96460fd749e928fa50b665ef3acbcada31284b2`  
		Last Modified: Wed, 13 Aug 2025 00:25:26 GMT  
		Size: 42.4 MB (42435666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2b0026af08d59058a3ac1b9cced2b8c5e42e21b78bffa8e164ec8f25f5ade8`  
		Last Modified: Tue, 12 Aug 2025 22:37:45 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:4bea6c1a7cfb86229cd87cdd581a659e80cd10d38b553dacb70f9d707510a143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3680310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466ac44f0db72062c95a977798b2237c29ace02c5cfac2dc2dad236a3b1bf388`

```dockerfile
```

-	Layers:
	-	`sha256:5017157d9a64a5a3e554661fa84aa621f6fa241a6fae928cc987a385f56c9a95`  
		Last Modified: Tue, 12 Aug 2025 22:33:25 GMT  
		Size: 3.7 MB (3655746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cf493157d9371e1e4b247e3eba8a5488e8eb19113b6ea7a3c83b9a60e3434e6`  
		Last Modified: Tue, 12 Aug 2025 22:33:26 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:994d10b57c5e3722231452c10346fb7c8c34339ca3822c23f76fdb864067b9d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155208987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b838d5ea4a740e9b50b8fafda01e1c0c8a8606d55c27f833fe32254fc197f5`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8f56cf1a4ba8c0ad0cfd1f9a290f664d03cebd21fb29d7a9e9979727ad1e16`  
		Last Modified: Wed, 13 Aug 2025 07:20:41 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ba4f4ec6243e7b597450fad0baf17bc5fd50afd711affb2ec4b046f852cee6`  
		Last Modified: Wed, 13 Aug 2025 07:33:35 GMT  
		Size: 7.7 MB (7671369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55aeeee205c8cacbc9c53a1532e4bb6a0211d3d431dfbeab036ba286c2b7baea`  
		Last Modified: Wed, 13 Aug 2025 07:33:39 GMT  
		Size: 76.6 MB (76644110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126318ea349d651273cfa24d6c4ff2541b9c14587b254c7bf0f127e3b43346d9`  
		Last Modified: Wed, 13 Aug 2025 07:20:45 GMT  
		Size: 371.8 KB (371845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a887a5f387999668994717fcfc7a927f5881a898f0cb4294990c361ceefa68d1`  
		Last Modified: Wed, 13 Aug 2025 07:21:05 GMT  
		Size: 99.3 KB (99348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a8a86b6bb6527f3e5bd7b06edbaa53bba62de03804f3c259fd1905f18670a4`  
		Last Modified: Wed, 13 Aug 2025 07:21:09 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f237626ff1625ab3dde05a7210e4027a57e23b7e51354eef2c88d54cd43c3b5`  
		Last Modified: Wed, 13 Aug 2025 08:26:49 GMT  
		Size: 42.3 MB (42338433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539f8c4b7d5a60cd1c8f430ef764660ffed11256b398f7a0634d6d3c7ad48c18`  
		Last Modified: Wed, 13 Aug 2025 07:21:25 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:31975122dcc76847341bc3ffbcab21203e56fd8fc9fd538595da887f88c86d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3679167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121f1940180000a473a7ebac7de6b76e04e001a69ec28f0bfe5498d8b9fecdb9`

```dockerfile
```

-	Layers:
	-	`sha256:bd468b9218245506154339f8e72b6f0a1db496c519e28667d2443c8c01f62cc2`  
		Last Modified: Wed, 13 Aug 2025 07:33:27 GMT  
		Size: 3.7 MB (3654422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ec1fe37a3d7dfcbd8c7fdbe627493b8961635f7a8e6f7ba1c0fc08181ceffec`  
		Last Modified: Wed, 13 Aug 2025 07:33:28 GMT  
		Size: 24.7 KB (24745 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:73824f0155e246b84dea55564307bb35e5f8c148c20955998c2141c0b530aaaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (150023195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05f9dc355961a03f42bc99f2f59d7ec43cc26298525416313408f7c14cf92e1`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
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
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3477dad2db3c13f403c9d3623e6dfb36742c6965d5f54e5dc14e6cdde7a66a`  
		Last Modified: Wed, 13 Aug 2025 15:10:45 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86997ea5cef151b0f22463c8db32b22377a36a2731a2463041c00e51c38e300a`  
		Last Modified: Wed, 13 Aug 2025 15:10:46 GMT  
		Size: 7.4 MB (7397796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b144c470493ab37c0bb7e68831cbd7adcb46418984ff5c2e15bc9294f2bbf8`  
		Last Modified: Wed, 13 Aug 2025 15:11:09 GMT  
		Size: 73.1 MB (73095781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00131fd1a5e3b4e5c4d46a08db3d5872c0188af95bf15854a2dbf3905f33f8bf`  
		Last Modified: Wed, 13 Aug 2025 15:10:45 GMT  
		Size: 378.1 KB (378144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f80705c9664868350b03281eb24469f3aceb54869ffc9f657263080c30ea5a`  
		Last Modified: Wed, 13 Aug 2025 15:10:46 GMT  
		Size: 99.5 KB (99457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1279ffc778b9acc33d5910aea83aa62f4b55cdb80c97d48981b56efa84efafa3`  
		Last Modified: Wed, 13 Aug 2025 15:10:46 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fee0e258dfab558556571f6bbf5be945aba0594c7d94ded0b2534a3e561ff0`  
		Last Modified: Wed, 13 Aug 2025 15:11:02 GMT  
		Size: 42.2 MB (42162304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3262828dcf86d709adeba6a2659dbcb199cb7c93304d7598634ace98064db058`  
		Last Modified: Wed, 13 Aug 2025 15:10:47 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:01e73baa3ddf3cc18244596980d9dbcd0715dd0f702b80e3442ad77f92b26036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3670839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c061cd234b8d24d411d7c378a6431d7b93c84e003406baf7937afd63b9eb74`

```dockerfile
```

-	Layers:
	-	`sha256:38077c4ca8e780d7f9c82c3324c4faef42cfd6c9bfa6bb634844fafe940de982`  
		Last Modified: Wed, 13 Aug 2025 16:33:34 GMT  
		Size: 3.6 MB (3646275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77f6c362c5aa68c17e5335c7507046ee6ac7c287bfa8c411dd4e163c833835dd`  
		Last Modified: Wed, 13 Aug 2025 16:33:35 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4`

```console
$ docker pull couchdb@sha256:fa7ac3986784ee65dd5af9e90c4760c1a9b3d04985541b6360af13cd9ceb99b1
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
$ docker pull couchdb@sha256:426b3ee8a8aa69ef937093e29d9e78c42c0a9d703bb2a8569300c7c9517cce00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139005426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806f64ee55872cfe2546c29f47ec5d672eb8a94843b47f579abce6eeac13c569`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c3c23aab0f931a56c97f8c36f4960616c102af8e0db2f8fd162c183227014a`  
		Last Modified: Tue, 12 Aug 2025 22:58:42 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04368d9eb32f07db45bef299a7261855334379086a8944bb831ab5af9ca941e`  
		Last Modified: Wed, 13 Aug 2025 01:34:36 GMT  
		Size: 7.9 MB (7881645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4bbb24b9d94ff63e33a3aaf7ec31b33ece3cbd1d5d3eedd626eea1bed81b99`  
		Last Modified: Tue, 12 Aug 2025 22:58:41 GMT  
		Size: 392.2 KB (392161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b34956d080b6d35c3b285c78cbf79d09748838af2b25f0445b7d67ff35c587d`  
		Last Modified: Tue, 12 Aug 2025 22:58:41 GMT  
		Size: 76.3 KB (76309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32abe28ea62df8726648141f63e83fabeab2dd93e8293e5a5987466b3ad98ea`  
		Last Modified: Tue, 12 Aug 2025 22:58:41 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7841bfa6d2faf8dec6f7ea77fea7859ac34d141621d85acd4ca6b0fb94c05b`  
		Last Modified: Wed, 13 Aug 2025 01:35:30 GMT  
		Size: 102.4 MB (102419626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76744d4f17cbf36c63303d7c46a13f0a4d422654696ad1264ff9f4539469d134`  
		Last Modified: Tue, 12 Aug 2025 22:58:41 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb3a0d09dd80500b169ef950846e8fdf57b5dd70e8197d95d50b47e6d631c72`  
		Last Modified: Tue, 12 Aug 2025 22:58:41 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36184f6ba9b5bcddfa59bcd1eafe59b834181bb08ae7bb284f5803f3b3bc74c`  
		Last Modified: Tue, 12 Aug 2025 22:58:41 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d4fba6be7755f3c26b553e011943f67cd9c8e82b3a9713a587cd650d0d1be5`  
		Last Modified: Tue, 12 Aug 2025 22:58:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:5ca5c829420057aff7d0db4f6b3d74e40fc7ed3eb592ab23d38ca7a2aff64246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4154273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92664eb59986b91c8cedf889fbf23f057bf4370cc1fd3295b0f3ed5eecf4af19`

```dockerfile
```

-	Layers:
	-	`sha256:c23ca06750e8d324953e45f5198a51ea742bb17aae4cde9d606c04ef486f3486`  
		Last Modified: Wed, 13 Aug 2025 01:33:26 GMT  
		Size: 4.1 MB (4123082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbcd8c7c40c81cd7ba5f6ef78d13fd445d84c07fc740473ee7eabcf8bfb0bfb0`  
		Last Modified: Wed, 13 Aug 2025 01:33:27 GMT  
		Size: 31.2 KB (31191 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:8ea72ab7bf121c79564ed5c04ea0b9d6547081efde28100de703e24581aae31f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.3 MB (138348030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8478201a877d58271ce65136854d29dc37940b7ab6b2b62057a5a8159df9aacf`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec13befd006fe986be6a8728105412886a583f41f71c6da9a69bcdafc5dca61a`  
		Last Modified: Wed, 13 Aug 2025 07:01:40 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d2aef50f2cd302839668b5ead9b50197b726f5dcab885cc3c48b47965bb73d`  
		Last Modified: Wed, 13 Aug 2025 07:01:41 GMT  
		Size: 7.7 MB (7671345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5301367e88b8bf291aa3e746da27aae27fca920b48b7ec9dce1e5a30e9ac85`  
		Last Modified: Wed, 13 Aug 2025 07:01:40 GMT  
		Size: 349.0 KB (349008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f67cda63d6c6f697113d856d3d51850bdca2557826056f6cc57d464cb605b4`  
		Last Modified: Wed, 13 Aug 2025 07:01:42 GMT  
		Size: 76.3 KB (76335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8732960ae16a12b47db734c1ea9ac4dbab7a16d0e3ac07da5cbf67929fb2df7f`  
		Last Modified: Wed, 13 Aug 2025 07:21:11 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f753db83745fd06b5fa03b86bd93ec72e0b128cf79f20a302182274032cffbf6`  
		Last Modified: Wed, 13 Aug 2025 07:33:41 GMT  
		Size: 102.2 MB (102163911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff9ea74c51696c9dda6ed6dc4c68d129b7673dd363965b4c9518770837fc3cb`  
		Last Modified: Wed, 13 Aug 2025 07:21:14 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a5afe394333cbe08c02546254ac9ebdb7151ff98f197fa95c65fe8b485f534`  
		Last Modified: Wed, 13 Aug 2025 07:21:17 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e2fb29f1587c3e50236f1e1b9b1a46b10b4620134b49ea8fbab01be81c6d92`  
		Last Modified: Wed, 13 Aug 2025 07:21:20 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99cacaf15a5ed1b930ca8db38aef17ad47f365026ebef856318cf69a448d5db5`  
		Last Modified: Wed, 13 Aug 2025 07:21:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:f03e42ae51d58eae8dc9be912f3596f8f4cf44ed2a0452cf52741d31c235595d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4154712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a83b29d0ff20ee1b899ab19effa3f862e4c30bac0fd49824e2fe6db4c7c4b8`

```dockerfile
```

-	Layers:
	-	`sha256:6f0a3975c77f10c7db8fce520ad034b2f5029ff47da21213c3b38cbf538704e2`  
		Last Modified: Wed, 13 Aug 2025 07:33:31 GMT  
		Size: 4.1 MB (4123351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ef55b204bc4e666d05fd8d52d885f9446f42a290230614a816f897fac455ff1`  
		Last Modified: Wed, 13 Aug 2025 07:33:33 GMT  
		Size: 31.4 KB (31361 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; s390x

```console
$ docker pull couchdb@sha256:475a31cbc44a2fb61db8f40f68d2a43a7df6203ab8541c60a04f00e75d23e9f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135779239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76feea0d35e5f28c68026e61d63cbeb55bb86c2d0648537d7ef91a50a675a6e5`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
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
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b7acab8e5e7b12089d79275ac325f69e00c57ef109efebab6c70c9cd73a40d`  
		Last Modified: Wed, 13 Aug 2025 15:09:36 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3abfab6aae8ef4c71d8ee0179a883e31407cdba29d7ec2aedcd6cf479dd3bf`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 7.4 MB (7397830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164187f5523648207c88c10beecff4fa873224418908ed2042111b9008220445`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 355.6 KB (355650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1ea234d9128aa5cf95bed7f6b642ed39541c3ce0421026891a6ae6c3a62cf6`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 76.3 KB (76347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31eafa29c931a560e6b3825d4cf7578551d10bac09d97f79640154888a5267d9`  
		Last Modified: Wed, 13 Aug 2025 15:11:41 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08bbebb2451e44f221410bb99fc16c68d6227619ea1d40e46f1c322fa6be8261`  
		Last Modified: Wed, 13 Aug 2025 17:22:56 GMT  
		Size: 101.1 MB (101056146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40a1e5db618c6db55c67aa7470d25b6ff665bf2eee0850c6b4a2434a6cc675f`  
		Last Modified: Wed, 13 Aug 2025 15:11:42 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d3a7c3c0f081c9aa325de28e5b1a88ce117e6e97089467714ef4323f8ff89d`  
		Last Modified: Wed, 13 Aug 2025 15:11:42 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13c04d1d7a1610a81b44627a0729e8ba8f83564f7bd9d8795d524445398c22b`  
		Last Modified: Wed, 13 Aug 2025 15:11:42 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31267d069eb208d9c0505bb4499401969fb3e2a1e110e98384699875ae34e7a4`  
		Last Modified: Wed, 13 Aug 2025 15:11:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:0702144fbd51bc0883bda128b39914edbe0b5411395774d5ddea3ed2ac41e3ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4150469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbf7d8ae3a1b05777fc68c846391b7efa5169afc93e352141483d064edeaa51f`

```dockerfile
```

-	Layers:
	-	`sha256:b8f331a35f1260a06b663f45696307c75875b555c396b2c05247c107c0307a32`  
		Last Modified: Wed, 13 Aug 2025 16:33:38 GMT  
		Size: 4.1 MB (4119278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fafd3d357f9aa58405db89a43e13ea3fcc657daf32211a0a9105be43ee526d31`  
		Last Modified: Wed, 13 Aug 2025 16:33:39 GMT  
		Size: 31.2 KB (31191 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4-nouveau`

```console
$ docker pull couchdb@sha256:3bc6388da272fa48f4e9bae18ad8a4edd7a86a45a3a0250f019a9bb95d339d38
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
$ docker pull couchdb@sha256:c9da683563761f3a381cf1ce17efe21e0b28e275dcd8396f054bedbe91977ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156388276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49339b75969153a00c9a2f45d4521c395f1bc2130f29aef9f5685449f3a7249c`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5b730a03713dda04994bd78a68b9d5636a568376ff85d32af32e9a4d0577cd`  
		Last Modified: Tue, 12 Aug 2025 21:23:31 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc75199dd7c33471a695e9bcd9550e04d99c34b4e473c39145539696de0d3720`  
		Last Modified: Tue, 12 Aug 2025 21:23:34 GMT  
		Size: 7.9 MB (7881570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e77ceda7e5874173c5e0a9152e270b3e5b573390359cd3369f627e84cecad7`  
		Last Modified: Tue, 12 Aug 2025 21:23:45 GMT  
		Size: 77.3 MB (77324703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6b072efaa0427eea053427d6c8a238430ce2d37f589f862739a267df73eb59`  
		Last Modified: Tue, 12 Aug 2025 21:23:33 GMT  
		Size: 415.0 KB (415027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35fde818110a931130fb085a21f8e00bf89d62ab6cc04ac74734e374131ee01a`  
		Last Modified: Tue, 12 Aug 2025 21:23:33 GMT  
		Size: 99.4 KB (99355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f90b230fd6da170edef3d20b1fbb00c457a36633c10c177db2cfd4605a5ab90`  
		Last Modified: Tue, 12 Aug 2025 21:23:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c69ced009bed2f10d2031ceac590d5a9b699c7f91cfec87959e4dffa6da0f9`  
		Last Modified: Tue, 12 Aug 2025 21:23:43 GMT  
		Size: 42.4 MB (42435491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa5eabcbb6ce8478ff5c5b1d34ee61eff60a9199a8b56a8a5684333d00ccd3e`  
		Last Modified: Tue, 12 Aug 2025 21:23:32 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:69b236b26da2714830fd4b9e540cd8f200f7bfa39164f3da910eae38ca3660cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3679698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:820be60a1d4d88617aea4cb2f5f23aebcaeb75d5d00e5edb429bb2d634298535`

```dockerfile
```

-	Layers:
	-	`sha256:42554c88e6861516dc5439942ceba0a54b0656ab1968158ce20691c338a3cb1a`  
		Last Modified: Wed, 13 Aug 2025 01:33:32 GMT  
		Size: 3.7 MB (3655440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c33e8a7631fbd19f34426410d0148b3f538022429be6fefbd7c244a644fab5f3`  
		Last Modified: Wed, 13 Aug 2025 01:33:33 GMT  
		Size: 24.3 KB (24258 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:e7dc0730470f9bce8a5f3ae07f78ca038c3f7054c696e5c105dc2f4f4bf7966b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155209038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:824d0b0f314e308cb3fc329f57953ba8ed7a4139d1cb1646dd4d72d37ece0e71`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8f56cf1a4ba8c0ad0cfd1f9a290f664d03cebd21fb29d7a9e9979727ad1e16`  
		Last Modified: Wed, 13 Aug 2025 07:20:41 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ba4f4ec6243e7b597450fad0baf17bc5fd50afd711affb2ec4b046f852cee6`  
		Last Modified: Wed, 13 Aug 2025 07:33:35 GMT  
		Size: 7.7 MB (7671369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55aeeee205c8cacbc9c53a1532e4bb6a0211d3d431dfbeab036ba286c2b7baea`  
		Last Modified: Wed, 13 Aug 2025 07:33:39 GMT  
		Size: 76.6 MB (76644110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126318ea349d651273cfa24d6c4ff2541b9c14587b254c7bf0f127e3b43346d9`  
		Last Modified: Wed, 13 Aug 2025 07:20:45 GMT  
		Size: 371.8 KB (371845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a887a5f387999668994717fcfc7a927f5881a898f0cb4294990c361ceefa68d1`  
		Last Modified: Wed, 13 Aug 2025 07:21:05 GMT  
		Size: 99.3 KB (99348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a8a86b6bb6527f3e5bd7b06edbaa53bba62de03804f3c259fd1905f18670a4`  
		Last Modified: Wed, 13 Aug 2025 07:21:09 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3e3f635b73ea305e8116f52caac2ece03dd1954587c6b67d7a98937e442c90`  
		Last Modified: Wed, 13 Aug 2025 07:33:38 GMT  
		Size: 42.3 MB (42338485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8151ed6eb75077a0d687575b02fd9bb856613c7f1587748a5af3d9f6152810d4`  
		Last Modified: Wed, 13 Aug 2025 07:21:12 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:a15508804a6cb7b690ed9d850cab400c1fad410e3dd400b8f24d3d5f4781145a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3678532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f5bd786c42c837f0e20f9169a0723423a675b9fba59ce8f1f09da4736b92ab1`

```dockerfile
```

-	Layers:
	-	`sha256:783af1e9f8121274f3830f5665c3d71fbc9eaa3c52b2b69945c6b1cb77daec81`  
		Last Modified: Wed, 13 Aug 2025 07:33:35 GMT  
		Size: 3.7 MB (3654104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b423f14e60a95876fdd4586deaadb66e7b9df6af1bf58ab91c4c8202e29c49e3`  
		Last Modified: Wed, 13 Aug 2025 07:33:36 GMT  
		Size: 24.4 KB (24428 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:eb802fc992e4559ff4a4d86931e8abacee7477e8bd7d9081a539d1b8e8cbe10f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (150022545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7eeefa47cf18467fbc3c8b1d80b71d0c9b760dfcd35e335d0ff8f8b59e4457`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
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
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3477dad2db3c13f403c9d3623e6dfb36742c6965d5f54e5dc14e6cdde7a66a`  
		Last Modified: Wed, 13 Aug 2025 15:10:45 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86997ea5cef151b0f22463c8db32b22377a36a2731a2463041c00e51c38e300a`  
		Last Modified: Wed, 13 Aug 2025 15:10:46 GMT  
		Size: 7.4 MB (7397796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b144c470493ab37c0bb7e68831cbd7adcb46418984ff5c2e15bc9294f2bbf8`  
		Last Modified: Wed, 13 Aug 2025 15:11:09 GMT  
		Size: 73.1 MB (73095781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00131fd1a5e3b4e5c4d46a08db3d5872c0188af95bf15854a2dbf3905f33f8bf`  
		Last Modified: Wed, 13 Aug 2025 15:10:45 GMT  
		Size: 378.1 KB (378144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f80705c9664868350b03281eb24469f3aceb54869ffc9f657263080c30ea5a`  
		Last Modified: Wed, 13 Aug 2025 15:10:46 GMT  
		Size: 99.5 KB (99457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1279ffc778b9acc33d5910aea83aa62f4b55cdb80c97d48981b56efa84efafa3`  
		Last Modified: Wed, 13 Aug 2025 15:10:46 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1e32bb5da08beecc59e3adfebac462d3735e0c1082b7aae9755aa546f19001`  
		Last Modified: Wed, 13 Aug 2025 15:11:47 GMT  
		Size: 42.2 MB (42161653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501d0bffdbbae076b8f7cf4c1e24462af05b6ee1ddd9d44f78b85acd0956579f`  
		Last Modified: Wed, 13 Aug 2025 16:11:52 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:c38b501e412cf53d89d7668f6ff5916acc23a521a495ec1e244d147125605c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3670226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85bf5b34db72d35433d90174d76b734fb1614dad3fdf0a5e17074ba96d3b858d`

```dockerfile
```

-	Layers:
	-	`sha256:6915d2adee7ad51bfb4d7c2bcc413e3c69a1e56f0befc34b51949dd445909dc1`  
		Last Modified: Wed, 13 Aug 2025 16:33:43 GMT  
		Size: 3.6 MB (3645969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b56d87596fc78b875c9be2053cd7dab18a060d82a70e52fc91dea42767b1636`  
		Last Modified: Wed, 13 Aug 2025 16:33:43 GMT  
		Size: 24.3 KB (24257 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3`

```console
$ docker pull couchdb@sha256:fa7ac3986784ee65dd5af9e90c4760c1a9b3d04985541b6360af13cd9ceb99b1
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
$ docker pull couchdb@sha256:426b3ee8a8aa69ef937093e29d9e78c42c0a9d703bb2a8569300c7c9517cce00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139005426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806f64ee55872cfe2546c29f47ec5d672eb8a94843b47f579abce6eeac13c569`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c3c23aab0f931a56c97f8c36f4960616c102af8e0db2f8fd162c183227014a`  
		Last Modified: Tue, 12 Aug 2025 22:58:42 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04368d9eb32f07db45bef299a7261855334379086a8944bb831ab5af9ca941e`  
		Last Modified: Wed, 13 Aug 2025 01:34:36 GMT  
		Size: 7.9 MB (7881645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4bbb24b9d94ff63e33a3aaf7ec31b33ece3cbd1d5d3eedd626eea1bed81b99`  
		Last Modified: Tue, 12 Aug 2025 22:58:41 GMT  
		Size: 392.2 KB (392161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b34956d080b6d35c3b285c78cbf79d09748838af2b25f0445b7d67ff35c587d`  
		Last Modified: Tue, 12 Aug 2025 22:58:41 GMT  
		Size: 76.3 KB (76309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32abe28ea62df8726648141f63e83fabeab2dd93e8293e5a5987466b3ad98ea`  
		Last Modified: Tue, 12 Aug 2025 22:58:41 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7841bfa6d2faf8dec6f7ea77fea7859ac34d141621d85acd4ca6b0fb94c05b`  
		Last Modified: Wed, 13 Aug 2025 01:35:30 GMT  
		Size: 102.4 MB (102419626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76744d4f17cbf36c63303d7c46a13f0a4d422654696ad1264ff9f4539469d134`  
		Last Modified: Tue, 12 Aug 2025 22:58:41 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb3a0d09dd80500b169ef950846e8fdf57b5dd70e8197d95d50b47e6d631c72`  
		Last Modified: Tue, 12 Aug 2025 22:58:41 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36184f6ba9b5bcddfa59bcd1eafe59b834181bb08ae7bb284f5803f3b3bc74c`  
		Last Modified: Tue, 12 Aug 2025 22:58:41 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d4fba6be7755f3c26b553e011943f67cd9c8e82b3a9713a587cd650d0d1be5`  
		Last Modified: Tue, 12 Aug 2025 22:58:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:5ca5c829420057aff7d0db4f6b3d74e40fc7ed3eb592ab23d38ca7a2aff64246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4154273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92664eb59986b91c8cedf889fbf23f057bf4370cc1fd3295b0f3ed5eecf4af19`

```dockerfile
```

-	Layers:
	-	`sha256:c23ca06750e8d324953e45f5198a51ea742bb17aae4cde9d606c04ef486f3486`  
		Last Modified: Wed, 13 Aug 2025 01:33:26 GMT  
		Size: 4.1 MB (4123082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbcd8c7c40c81cd7ba5f6ef78d13fd445d84c07fc740473ee7eabcf8bfb0bfb0`  
		Last Modified: Wed, 13 Aug 2025 01:33:27 GMT  
		Size: 31.2 KB (31191 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:8ea72ab7bf121c79564ed5c04ea0b9d6547081efde28100de703e24581aae31f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.3 MB (138348030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8478201a877d58271ce65136854d29dc37940b7ab6b2b62057a5a8159df9aacf`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec13befd006fe986be6a8728105412886a583f41f71c6da9a69bcdafc5dca61a`  
		Last Modified: Wed, 13 Aug 2025 07:01:40 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d2aef50f2cd302839668b5ead9b50197b726f5dcab885cc3c48b47965bb73d`  
		Last Modified: Wed, 13 Aug 2025 07:01:41 GMT  
		Size: 7.7 MB (7671345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5301367e88b8bf291aa3e746da27aae27fca920b48b7ec9dce1e5a30e9ac85`  
		Last Modified: Wed, 13 Aug 2025 07:01:40 GMT  
		Size: 349.0 KB (349008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f67cda63d6c6f697113d856d3d51850bdca2557826056f6cc57d464cb605b4`  
		Last Modified: Wed, 13 Aug 2025 07:01:42 GMT  
		Size: 76.3 KB (76335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8732960ae16a12b47db734c1ea9ac4dbab7a16d0e3ac07da5cbf67929fb2df7f`  
		Last Modified: Wed, 13 Aug 2025 07:21:11 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f753db83745fd06b5fa03b86bd93ec72e0b128cf79f20a302182274032cffbf6`  
		Last Modified: Wed, 13 Aug 2025 07:33:41 GMT  
		Size: 102.2 MB (102163911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff9ea74c51696c9dda6ed6dc4c68d129b7673dd363965b4c9518770837fc3cb`  
		Last Modified: Wed, 13 Aug 2025 07:21:14 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a5afe394333cbe08c02546254ac9ebdb7151ff98f197fa95c65fe8b485f534`  
		Last Modified: Wed, 13 Aug 2025 07:21:17 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e2fb29f1587c3e50236f1e1b9b1a46b10b4620134b49ea8fbab01be81c6d92`  
		Last Modified: Wed, 13 Aug 2025 07:21:20 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99cacaf15a5ed1b930ca8db38aef17ad47f365026ebef856318cf69a448d5db5`  
		Last Modified: Wed, 13 Aug 2025 07:21:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:f03e42ae51d58eae8dc9be912f3596f8f4cf44ed2a0452cf52741d31c235595d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4154712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a83b29d0ff20ee1b899ab19effa3f862e4c30bac0fd49824e2fe6db4c7c4b8`

```dockerfile
```

-	Layers:
	-	`sha256:6f0a3975c77f10c7db8fce520ad034b2f5029ff47da21213c3b38cbf538704e2`  
		Last Modified: Wed, 13 Aug 2025 07:33:31 GMT  
		Size: 4.1 MB (4123351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ef55b204bc4e666d05fd8d52d885f9446f42a290230614a816f897fac455ff1`  
		Last Modified: Wed, 13 Aug 2025 07:33:33 GMT  
		Size: 31.4 KB (31361 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3` - linux; s390x

```console
$ docker pull couchdb@sha256:475a31cbc44a2fb61db8f40f68d2a43a7df6203ab8541c60a04f00e75d23e9f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135779239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76feea0d35e5f28c68026e61d63cbeb55bb86c2d0648537d7ef91a50a675a6e5`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
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
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b7acab8e5e7b12089d79275ac325f69e00c57ef109efebab6c70c9cd73a40d`  
		Last Modified: Wed, 13 Aug 2025 15:09:36 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3abfab6aae8ef4c71d8ee0179a883e31407cdba29d7ec2aedcd6cf479dd3bf`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 7.4 MB (7397830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164187f5523648207c88c10beecff4fa873224418908ed2042111b9008220445`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 355.6 KB (355650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1ea234d9128aa5cf95bed7f6b642ed39541c3ce0421026891a6ae6c3a62cf6`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 76.3 KB (76347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31eafa29c931a560e6b3825d4cf7578551d10bac09d97f79640154888a5267d9`  
		Last Modified: Wed, 13 Aug 2025 15:11:41 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08bbebb2451e44f221410bb99fc16c68d6227619ea1d40e46f1c322fa6be8261`  
		Last Modified: Wed, 13 Aug 2025 17:22:56 GMT  
		Size: 101.1 MB (101056146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40a1e5db618c6db55c67aa7470d25b6ff665bf2eee0850c6b4a2434a6cc675f`  
		Last Modified: Wed, 13 Aug 2025 15:11:42 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d3a7c3c0f081c9aa325de28e5b1a88ce117e6e97089467714ef4323f8ff89d`  
		Last Modified: Wed, 13 Aug 2025 15:11:42 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13c04d1d7a1610a81b44627a0729e8ba8f83564f7bd9d8795d524445398c22b`  
		Last Modified: Wed, 13 Aug 2025 15:11:42 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31267d069eb208d9c0505bb4499401969fb3e2a1e110e98384699875ae34e7a4`  
		Last Modified: Wed, 13 Aug 2025 15:11:42 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:0702144fbd51bc0883bda128b39914edbe0b5411395774d5ddea3ed2ac41e3ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4150469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbf7d8ae3a1b05777fc68c846391b7efa5169afc93e352141483d064edeaa51f`

```dockerfile
```

-	Layers:
	-	`sha256:b8f331a35f1260a06b663f45696307c75875b555c396b2c05247c107c0307a32`  
		Last Modified: Wed, 13 Aug 2025 16:33:38 GMT  
		Size: 4.1 MB (4119278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fafd3d357f9aa58405db89a43e13ea3fcc657daf32211a0a9105be43ee526d31`  
		Last Modified: Wed, 13 Aug 2025 16:33:39 GMT  
		Size: 31.2 KB (31191 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3-nouveau`

```console
$ docker pull couchdb@sha256:3bc6388da272fa48f4e9bae18ad8a4edd7a86a45a3a0250f019a9bb95d339d38
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
$ docker pull couchdb@sha256:c9da683563761f3a381cf1ce17efe21e0b28e275dcd8396f054bedbe91977ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156388276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49339b75969153a00c9a2f45d4521c395f1bc2130f29aef9f5685449f3a7249c`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5b730a03713dda04994bd78a68b9d5636a568376ff85d32af32e9a4d0577cd`  
		Last Modified: Tue, 12 Aug 2025 21:23:31 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc75199dd7c33471a695e9bcd9550e04d99c34b4e473c39145539696de0d3720`  
		Last Modified: Tue, 12 Aug 2025 21:23:34 GMT  
		Size: 7.9 MB (7881570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e77ceda7e5874173c5e0a9152e270b3e5b573390359cd3369f627e84cecad7`  
		Last Modified: Tue, 12 Aug 2025 21:23:45 GMT  
		Size: 77.3 MB (77324703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6b072efaa0427eea053427d6c8a238430ce2d37f589f862739a267df73eb59`  
		Last Modified: Tue, 12 Aug 2025 21:23:33 GMT  
		Size: 415.0 KB (415027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35fde818110a931130fb085a21f8e00bf89d62ab6cc04ac74734e374131ee01a`  
		Last Modified: Tue, 12 Aug 2025 21:23:33 GMT  
		Size: 99.4 KB (99355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f90b230fd6da170edef3d20b1fbb00c457a36633c10c177db2cfd4605a5ab90`  
		Last Modified: Tue, 12 Aug 2025 21:23:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c69ced009bed2f10d2031ceac590d5a9b699c7f91cfec87959e4dffa6da0f9`  
		Last Modified: Tue, 12 Aug 2025 21:23:43 GMT  
		Size: 42.4 MB (42435491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa5eabcbb6ce8478ff5c5b1d34ee61eff60a9199a8b56a8a5684333d00ccd3e`  
		Last Modified: Tue, 12 Aug 2025 21:23:32 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:69b236b26da2714830fd4b9e540cd8f200f7bfa39164f3da910eae38ca3660cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3679698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:820be60a1d4d88617aea4cb2f5f23aebcaeb75d5d00e5edb429bb2d634298535`

```dockerfile
```

-	Layers:
	-	`sha256:42554c88e6861516dc5439942ceba0a54b0656ab1968158ce20691c338a3cb1a`  
		Last Modified: Wed, 13 Aug 2025 01:33:32 GMT  
		Size: 3.7 MB (3655440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c33e8a7631fbd19f34426410d0148b3f538022429be6fefbd7c244a644fab5f3`  
		Last Modified: Wed, 13 Aug 2025 01:33:33 GMT  
		Size: 24.3 KB (24258 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:e7dc0730470f9bce8a5f3ae07f78ca038c3f7054c696e5c105dc2f4f4bf7966b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155209038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:824d0b0f314e308cb3fc329f57953ba8ed7a4139d1cb1646dd4d72d37ece0e71`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8f56cf1a4ba8c0ad0cfd1f9a290f664d03cebd21fb29d7a9e9979727ad1e16`  
		Last Modified: Wed, 13 Aug 2025 07:20:41 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ba4f4ec6243e7b597450fad0baf17bc5fd50afd711affb2ec4b046f852cee6`  
		Last Modified: Wed, 13 Aug 2025 07:33:35 GMT  
		Size: 7.7 MB (7671369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55aeeee205c8cacbc9c53a1532e4bb6a0211d3d431dfbeab036ba286c2b7baea`  
		Last Modified: Wed, 13 Aug 2025 07:33:39 GMT  
		Size: 76.6 MB (76644110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126318ea349d651273cfa24d6c4ff2541b9c14587b254c7bf0f127e3b43346d9`  
		Last Modified: Wed, 13 Aug 2025 07:20:45 GMT  
		Size: 371.8 KB (371845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a887a5f387999668994717fcfc7a927f5881a898f0cb4294990c361ceefa68d1`  
		Last Modified: Wed, 13 Aug 2025 07:21:05 GMT  
		Size: 99.3 KB (99348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a8a86b6bb6527f3e5bd7b06edbaa53bba62de03804f3c259fd1905f18670a4`  
		Last Modified: Wed, 13 Aug 2025 07:21:09 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3e3f635b73ea305e8116f52caac2ece03dd1954587c6b67d7a98937e442c90`  
		Last Modified: Wed, 13 Aug 2025 07:33:38 GMT  
		Size: 42.3 MB (42338485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8151ed6eb75077a0d687575b02fd9bb856613c7f1587748a5af3d9f6152810d4`  
		Last Modified: Wed, 13 Aug 2025 07:21:12 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:a15508804a6cb7b690ed9d850cab400c1fad410e3dd400b8f24d3d5f4781145a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3678532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f5bd786c42c837f0e20f9169a0723423a675b9fba59ce8f1f09da4736b92ab1`

```dockerfile
```

-	Layers:
	-	`sha256:783af1e9f8121274f3830f5665c3d71fbc9eaa3c52b2b69945c6b1cb77daec81`  
		Last Modified: Wed, 13 Aug 2025 07:33:35 GMT  
		Size: 3.7 MB (3654104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b423f14e60a95876fdd4586deaadb66e7b9df6af1bf58ab91c4c8202e29c49e3`  
		Last Modified: Wed, 13 Aug 2025 07:33:36 GMT  
		Size: 24.4 KB (24428 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:eb802fc992e4559ff4a4d86931e8abacee7477e8bd7d9081a539d1b8e8cbe10f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (150022545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7eeefa47cf18467fbc3c8b1d80b71d0c9b760dfcd35e335d0ff8f8b59e4457`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
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
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3477dad2db3c13f403c9d3623e6dfb36742c6965d5f54e5dc14e6cdde7a66a`  
		Last Modified: Wed, 13 Aug 2025 15:10:45 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86997ea5cef151b0f22463c8db32b22377a36a2731a2463041c00e51c38e300a`  
		Last Modified: Wed, 13 Aug 2025 15:10:46 GMT  
		Size: 7.4 MB (7397796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b144c470493ab37c0bb7e68831cbd7adcb46418984ff5c2e15bc9294f2bbf8`  
		Last Modified: Wed, 13 Aug 2025 15:11:09 GMT  
		Size: 73.1 MB (73095781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00131fd1a5e3b4e5c4d46a08db3d5872c0188af95bf15854a2dbf3905f33f8bf`  
		Last Modified: Wed, 13 Aug 2025 15:10:45 GMT  
		Size: 378.1 KB (378144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f80705c9664868350b03281eb24469f3aceb54869ffc9f657263080c30ea5a`  
		Last Modified: Wed, 13 Aug 2025 15:10:46 GMT  
		Size: 99.5 KB (99457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1279ffc778b9acc33d5910aea83aa62f4b55cdb80c97d48981b56efa84efafa3`  
		Last Modified: Wed, 13 Aug 2025 15:10:46 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1e32bb5da08beecc59e3adfebac462d3735e0c1082b7aae9755aa546f19001`  
		Last Modified: Wed, 13 Aug 2025 15:11:47 GMT  
		Size: 42.2 MB (42161653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501d0bffdbbae076b8f7cf4c1e24462af05b6ee1ddd9d44f78b85acd0956579f`  
		Last Modified: Wed, 13 Aug 2025 16:11:52 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:c38b501e412cf53d89d7668f6ff5916acc23a521a495ec1e244d147125605c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3670226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85bf5b34db72d35433d90174d76b734fb1614dad3fdf0a5e17074ba96d3b858d`

```dockerfile
```

-	Layers:
	-	`sha256:6915d2adee7ad51bfb4d7c2bcc413e3c69a1e56f0befc34b51949dd445909dc1`  
		Last Modified: Wed, 13 Aug 2025 16:33:43 GMT  
		Size: 3.6 MB (3645969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b56d87596fc78b875c9be2053cd7dab18a060d82a70e52fc91dea42767b1636`  
		Last Modified: Wed, 13 Aug 2025 16:33:43 GMT  
		Size: 24.3 KB (24257 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5`

```console
$ docker pull couchdb@sha256:432e99b1dbb8bd996b2af964b4731633956e9635548e82b037bda94bb1835193
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
$ docker pull couchdb@sha256:61b1f52d0853861f76353350a313289b31c2ee1b4804c1f6997074d8fcac7cd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139828882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6dbe6ebdaba35a59a45b23d5ce6a95b780604bbb7930465beef5725558681f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f51fa6c894ee9345fe0500a27ff388ecb72eabe2fe3b02d6edd3dc5b3350b93`  
		Last Modified: Tue, 12 Aug 2025 21:23:09 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764b70173c9e8ba1719c81377202f5f41a0420fae43271c3822ee720a613c396`  
		Last Modified: Tue, 12 Aug 2025 21:23:10 GMT  
		Size: 7.9 MB (7881552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6593eef0f94fd50f73d54db6bceb74c820fdaa4d0e2c9aee51d1afbd69b3f62e`  
		Last Modified: Tue, 12 Aug 2025 21:23:10 GMT  
		Size: 392.2 KB (392159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27598109e7c931cfd1cde74aa91bf06dc90e3ab15c837c242a01fb5c90d75f3e`  
		Last Modified: Tue, 12 Aug 2025 21:23:10 GMT  
		Size: 76.3 KB (76305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f674471e32b0c0267121748f62842811c187c1d308ce36cbf5697436e5727b72`  
		Last Modified: Tue, 12 Aug 2025 21:23:10 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3dc16bdec0642eb6c72e582680ee47bb502c5fbd7b2ddaeae7acf21dec07d51`  
		Last Modified: Tue, 12 Aug 2025 21:23:21 GMT  
		Size: 103.2 MB (103243184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75cbcfe770026e1e7036cf243a6b58d887661183d729bdffa652af37138f9f36`  
		Last Modified: Tue, 12 Aug 2025 21:23:10 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d750e10a43cb3769286b8f43be624ca1c41158ea9ea492a534148de3784a81`  
		Last Modified: Tue, 12 Aug 2025 21:23:10 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a114350064b8d1c007ae4c75d6ea1dfa2d9dcdf001b545a18c5083b27445c0`  
		Last Modified: Tue, 12 Aug 2025 21:23:11 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2090b99b69f9563438f44c6cfb8d0c9c55b293d66f6fb682dec49fa5cbb89af0`  
		Last Modified: Tue, 12 Aug 2025 21:23:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:6416bbb6b6baf528846e66900a2e9d6630b091c824bacebb800b8cb2a67336fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4170730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6af04829063d566a11789e76c7fcef29c85e001c106ec14c3efdd9865dd2a8`

```dockerfile
```

-	Layers:
	-	`sha256:f993f71f1e61426d80826a56f7b5044be5a4ca7aa7582f5d5cc145769198982d`  
		Last Modified: Wed, 13 Aug 2025 01:33:20 GMT  
		Size: 4.1 MB (4138949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:982abba7fef1ec1955de60a347341f458aeab3bf621264d1ce41dfdb38ee2913`  
		Last Modified: Wed, 13 Aug 2025 01:33:21 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:d4d661276bc55d6c7c97b92e1a692a06ff8db07bf9faef63722438cc11c93e15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139087709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:072f03e4437bff861b82d4ac70cfc6011b4f41d72ab741677a8d2efe213b54d3`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec13befd006fe986be6a8728105412886a583f41f71c6da9a69bcdafc5dca61a`  
		Last Modified: Wed, 13 Aug 2025 07:01:40 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d2aef50f2cd302839668b5ead9b50197b726f5dcab885cc3c48b47965bb73d`  
		Last Modified: Wed, 13 Aug 2025 07:01:41 GMT  
		Size: 7.7 MB (7671345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5301367e88b8bf291aa3e746da27aae27fca920b48b7ec9dce1e5a30e9ac85`  
		Last Modified: Wed, 13 Aug 2025 07:01:40 GMT  
		Size: 349.0 KB (349008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f67cda63d6c6f697113d856d3d51850bdca2557826056f6cc57d464cb605b4`  
		Last Modified: Wed, 13 Aug 2025 07:01:42 GMT  
		Size: 76.3 KB (76335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923cef98fe321ff8257c5ab2d2a257df741860e41a3a4874793e6cad524c5b4b`  
		Last Modified: Wed, 13 Aug 2025 07:01:42 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf41befbfe783db522e1c0f9273d8b3990e28c0ea994bccda5fa465b2377c93`  
		Last Modified: Wed, 13 Aug 2025 07:02:04 GMT  
		Size: 102.9 MB (102903580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb50d4b8156f07b71d73019935a3aee01a295f0c8d11efff59dacb5e0403dea`  
		Last Modified: Wed, 13 Aug 2025 07:01:36 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1d3615bc1b22a46b4b120f3cfa33d9921d4aca1e6575f8e57f41471a4b3c83`  
		Last Modified: Wed, 13 Aug 2025 07:01:36 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b50ca5361151149f77020482ac82c35cd96093e57456c10a50cd045674b2e2`  
		Last Modified: Wed, 13 Aug 2025 07:01:36 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b969e402096d53bed40bccd8c1b4492a774eb07ac9cfc390e7f16d99bc72a5b`  
		Last Modified: Wed, 13 Aug 2025 07:01:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:11252c508326fc8c25f42c580b0e2c55f29964f7261c2535cb86fd2bcf83d58a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4171217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d992e96908654319a7c0db09c8a678fea16da0a04d698bc9e1e7efd5acb93a`

```dockerfile
```

-	Layers:
	-	`sha256:0862edf1bc3bbd57fe812708c8c761759b6225d3c947158d0cdd755e6019ccfa`  
		Last Modified: Wed, 13 Aug 2025 07:33:23 GMT  
		Size: 4.1 MB (4139242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d3453eb326594daa4b8a25fcbcd3f70fa5c5dd2e143c24097ef3945c15a9ead`  
		Last Modified: Wed, 13 Aug 2025 07:33:23 GMT  
		Size: 32.0 KB (31975 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5` - linux; s390x

```console
$ docker pull couchdb@sha256:e4a4fc9e58539d2868bd15e046780cd8d8b7a71a74c1eb9f555e22fdf9c0c86b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136521588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec4fca67cecb025b5c09cab9c9549cb681d94892aaf58073a27711545f702b5e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
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
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b7acab8e5e7b12089d79275ac325f69e00c57ef109efebab6c70c9cd73a40d`  
		Last Modified: Wed, 13 Aug 2025 15:09:36 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3abfab6aae8ef4c71d8ee0179a883e31407cdba29d7ec2aedcd6cf479dd3bf`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 7.4 MB (7397830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164187f5523648207c88c10beecff4fa873224418908ed2042111b9008220445`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 355.6 KB (355650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1ea234d9128aa5cf95bed7f6b642ed39541c3ce0421026891a6ae6c3a62cf6`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 76.3 KB (76347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d507f15e04c67e6c028ebaf9b70be03905c6b099f3280dc1ee5b6c61e54fb9`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b32a62c011f37d07095a847adb6849fc8b49b594312b80901dd3fa8730a8f14`  
		Last Modified: Wed, 13 Aug 2025 16:38:43 GMT  
		Size: 101.8 MB (101798492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021c7a0c08391ce264a34acc839e0c22ef3ae30cd5170382d429de2fd535dd89`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8e63f7118f360ea233b6a4b5bfe85601905a9f58ccd1f8e5bd49122797016e`  
		Last Modified: Wed, 13 Aug 2025 15:09:38 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c223e87672740895458e8f91f45b4a146badb15e846fc58f8860c7318a8ff3ab`  
		Last Modified: Wed, 13 Aug 2025 15:09:38 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317e7af7e41277224e9cbb8f9c30c37a3271c0df880f6cf92e4bb22db5ecefe2`  
		Last Modified: Wed, 13 Aug 2025 15:09:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:37f51edaf047cdf5f5111855683e13ea3c6672c8a15c2251ae5e354aae7a84a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4166926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36fa1cbb03efdd840bd2a162de1c1575a3bbbdb97b9d101b488ed2ce25e1f89`

```dockerfile
```

-	Layers:
	-	`sha256:66a48a697a343af104ea7f47a48904fb5b1d220938d9142743643f1b94344055`  
		Last Modified: Wed, 13 Aug 2025 16:33:26 GMT  
		Size: 4.1 MB (4135145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f50372cd52cb3fa8e4baf039bb58aa2c00bbb482d234fe623bfcf97bd2ac1f1`  
		Last Modified: Wed, 13 Aug 2025 16:33:27 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5-nouveau`

```console
$ docker pull couchdb@sha256:308b04f6701f381607f7f47d7fb87aad8ed7ef45bb46801f2ebedebfae25008a
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
$ docker pull couchdb@sha256:8827e434487f67468be45e6638e7c262c202df39dab193f7a801d910337e1168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156388372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb51afec84a60b4ccca88637b6171dbf9c7bd64f5abbd8767fd148a8f7c83b86`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f790d8ace6bac688ec09887e051eca9bfb5dcec4060dbfa6e004dbd22c2335`  
		Last Modified: Tue, 12 Aug 2025 22:37:28 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa6399b477180c57907d82946e672511eca816592e7bde3ce7cbef0120d988c`  
		Last Modified: Wed, 13 Aug 2025 00:25:10 GMT  
		Size: 7.9 MB (7881623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a83b3d6009f4d95485272c64af79f09993fd79bf2642286b32d66b25f416bf`  
		Last Modified: Wed, 13 Aug 2025 00:25:20 GMT  
		Size: 77.3 MB (77324598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6505f4ba5ba4d521d87e5366d2ba43a91f994a54206091b2f9fe3bee5a92512f`  
		Last Modified: Tue, 12 Aug 2025 22:37:32 GMT  
		Size: 415.0 KB (415014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340137239ed9b3bc413c49b3966668ac8adb208cf72782ff5b6998c8c82b4275`  
		Last Modified: Tue, 12 Aug 2025 22:37:38 GMT  
		Size: 99.3 KB (99339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bfd6d48df450c319175586a5fc5f9d294e8b9451bc20ee8664c77abb7b7b74`  
		Last Modified: Tue, 12 Aug 2025 22:37:42 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b79bc1a224dbf16495d0825c96460fd749e928fa50b665ef3acbcada31284b2`  
		Last Modified: Wed, 13 Aug 2025 00:25:26 GMT  
		Size: 42.4 MB (42435666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2b0026af08d59058a3ac1b9cced2b8c5e42e21b78bffa8e164ec8f25f5ade8`  
		Last Modified: Tue, 12 Aug 2025 22:37:45 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:4bea6c1a7cfb86229cd87cdd581a659e80cd10d38b553dacb70f9d707510a143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3680310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466ac44f0db72062c95a977798b2237c29ace02c5cfac2dc2dad236a3b1bf388`

```dockerfile
```

-	Layers:
	-	`sha256:5017157d9a64a5a3e554661fa84aa621f6fa241a6fae928cc987a385f56c9a95`  
		Last Modified: Tue, 12 Aug 2025 22:33:25 GMT  
		Size: 3.7 MB (3655746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cf493157d9371e1e4b247e3eba8a5488e8eb19113b6ea7a3c83b9a60e3434e6`  
		Last Modified: Tue, 12 Aug 2025 22:33:26 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:994d10b57c5e3722231452c10346fb7c8c34339ca3822c23f76fdb864067b9d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155208987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b838d5ea4a740e9b50b8fafda01e1c0c8a8606d55c27f833fe32254fc197f5`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8f56cf1a4ba8c0ad0cfd1f9a290f664d03cebd21fb29d7a9e9979727ad1e16`  
		Last Modified: Wed, 13 Aug 2025 07:20:41 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ba4f4ec6243e7b597450fad0baf17bc5fd50afd711affb2ec4b046f852cee6`  
		Last Modified: Wed, 13 Aug 2025 07:33:35 GMT  
		Size: 7.7 MB (7671369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55aeeee205c8cacbc9c53a1532e4bb6a0211d3d431dfbeab036ba286c2b7baea`  
		Last Modified: Wed, 13 Aug 2025 07:33:39 GMT  
		Size: 76.6 MB (76644110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126318ea349d651273cfa24d6c4ff2541b9c14587b254c7bf0f127e3b43346d9`  
		Last Modified: Wed, 13 Aug 2025 07:20:45 GMT  
		Size: 371.8 KB (371845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a887a5f387999668994717fcfc7a927f5881a898f0cb4294990c361ceefa68d1`  
		Last Modified: Wed, 13 Aug 2025 07:21:05 GMT  
		Size: 99.3 KB (99348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a8a86b6bb6527f3e5bd7b06edbaa53bba62de03804f3c259fd1905f18670a4`  
		Last Modified: Wed, 13 Aug 2025 07:21:09 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f237626ff1625ab3dde05a7210e4027a57e23b7e51354eef2c88d54cd43c3b5`  
		Last Modified: Wed, 13 Aug 2025 08:26:49 GMT  
		Size: 42.3 MB (42338433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539f8c4b7d5a60cd1c8f430ef764660ffed11256b398f7a0634d6d3c7ad48c18`  
		Last Modified: Wed, 13 Aug 2025 07:21:25 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:31975122dcc76847341bc3ffbcab21203e56fd8fc9fd538595da887f88c86d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3679167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121f1940180000a473a7ebac7de6b76e04e001a69ec28f0bfe5498d8b9fecdb9`

```dockerfile
```

-	Layers:
	-	`sha256:bd468b9218245506154339f8e72b6f0a1db496c519e28667d2443c8c01f62cc2`  
		Last Modified: Wed, 13 Aug 2025 07:33:27 GMT  
		Size: 3.7 MB (3654422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ec1fe37a3d7dfcbd8c7fdbe627493b8961635f7a8e6f7ba1c0fc08181ceffec`  
		Last Modified: Wed, 13 Aug 2025 07:33:28 GMT  
		Size: 24.7 KB (24745 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:73824f0155e246b84dea55564307bb35e5f8c148c20955998c2141c0b530aaaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (150023195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05f9dc355961a03f42bc99f2f59d7ec43cc26298525416313408f7c14cf92e1`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
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
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3477dad2db3c13f403c9d3623e6dfb36742c6965d5f54e5dc14e6cdde7a66a`  
		Last Modified: Wed, 13 Aug 2025 15:10:45 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86997ea5cef151b0f22463c8db32b22377a36a2731a2463041c00e51c38e300a`  
		Last Modified: Wed, 13 Aug 2025 15:10:46 GMT  
		Size: 7.4 MB (7397796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b144c470493ab37c0bb7e68831cbd7adcb46418984ff5c2e15bc9294f2bbf8`  
		Last Modified: Wed, 13 Aug 2025 15:11:09 GMT  
		Size: 73.1 MB (73095781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00131fd1a5e3b4e5c4d46a08db3d5872c0188af95bf15854a2dbf3905f33f8bf`  
		Last Modified: Wed, 13 Aug 2025 15:10:45 GMT  
		Size: 378.1 KB (378144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f80705c9664868350b03281eb24469f3aceb54869ffc9f657263080c30ea5a`  
		Last Modified: Wed, 13 Aug 2025 15:10:46 GMT  
		Size: 99.5 KB (99457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1279ffc778b9acc33d5910aea83aa62f4b55cdb80c97d48981b56efa84efafa3`  
		Last Modified: Wed, 13 Aug 2025 15:10:46 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fee0e258dfab558556571f6bbf5be945aba0594c7d94ded0b2534a3e561ff0`  
		Last Modified: Wed, 13 Aug 2025 15:11:02 GMT  
		Size: 42.2 MB (42162304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3262828dcf86d709adeba6a2659dbcb199cb7c93304d7598634ace98064db058`  
		Last Modified: Wed, 13 Aug 2025 15:10:47 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:01e73baa3ddf3cc18244596980d9dbcd0715dd0f702b80e3442ad77f92b26036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3670839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c061cd234b8d24d411d7c378a6431d7b93c84e003406baf7937afd63b9eb74`

```dockerfile
```

-	Layers:
	-	`sha256:38077c4ca8e780d7f9c82c3324c4faef42cfd6c9bfa6bb634844fafe940de982`  
		Last Modified: Wed, 13 Aug 2025 16:33:34 GMT  
		Size: 3.6 MB (3646275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77f6c362c5aa68c17e5335c7507046ee6ac7c287bfa8c411dd4e163c833835dd`  
		Last Modified: Wed, 13 Aug 2025 16:33:35 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.0`

```console
$ docker pull couchdb@sha256:432e99b1dbb8bd996b2af964b4731633956e9635548e82b037bda94bb1835193
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
$ docker pull couchdb@sha256:61b1f52d0853861f76353350a313289b31c2ee1b4804c1f6997074d8fcac7cd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139828882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6dbe6ebdaba35a59a45b23d5ce6a95b780604bbb7930465beef5725558681f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f51fa6c894ee9345fe0500a27ff388ecb72eabe2fe3b02d6edd3dc5b3350b93`  
		Last Modified: Tue, 12 Aug 2025 21:23:09 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764b70173c9e8ba1719c81377202f5f41a0420fae43271c3822ee720a613c396`  
		Last Modified: Tue, 12 Aug 2025 21:23:10 GMT  
		Size: 7.9 MB (7881552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6593eef0f94fd50f73d54db6bceb74c820fdaa4d0e2c9aee51d1afbd69b3f62e`  
		Last Modified: Tue, 12 Aug 2025 21:23:10 GMT  
		Size: 392.2 KB (392159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27598109e7c931cfd1cde74aa91bf06dc90e3ab15c837c242a01fb5c90d75f3e`  
		Last Modified: Tue, 12 Aug 2025 21:23:10 GMT  
		Size: 76.3 KB (76305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f674471e32b0c0267121748f62842811c187c1d308ce36cbf5697436e5727b72`  
		Last Modified: Tue, 12 Aug 2025 21:23:10 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3dc16bdec0642eb6c72e582680ee47bb502c5fbd7b2ddaeae7acf21dec07d51`  
		Last Modified: Tue, 12 Aug 2025 21:23:21 GMT  
		Size: 103.2 MB (103243184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75cbcfe770026e1e7036cf243a6b58d887661183d729bdffa652af37138f9f36`  
		Last Modified: Tue, 12 Aug 2025 21:23:10 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d750e10a43cb3769286b8f43be624ca1c41158ea9ea492a534148de3784a81`  
		Last Modified: Tue, 12 Aug 2025 21:23:10 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a114350064b8d1c007ae4c75d6ea1dfa2d9dcdf001b545a18c5083b27445c0`  
		Last Modified: Tue, 12 Aug 2025 21:23:11 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2090b99b69f9563438f44c6cfb8d0c9c55b293d66f6fb682dec49fa5cbb89af0`  
		Last Modified: Tue, 12 Aug 2025 21:23:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0` - unknown; unknown

```console
$ docker pull couchdb@sha256:6416bbb6b6baf528846e66900a2e9d6630b091c824bacebb800b8cb2a67336fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4170730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6af04829063d566a11789e76c7fcef29c85e001c106ec14c3efdd9865dd2a8`

```dockerfile
```

-	Layers:
	-	`sha256:f993f71f1e61426d80826a56f7b5044be5a4ca7aa7582f5d5cc145769198982d`  
		Last Modified: Wed, 13 Aug 2025 01:33:20 GMT  
		Size: 4.1 MB (4138949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:982abba7fef1ec1955de60a347341f458aeab3bf621264d1ce41dfdb38ee2913`  
		Last Modified: Wed, 13 Aug 2025 01:33:21 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.0` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:d4d661276bc55d6c7c97b92e1a692a06ff8db07bf9faef63722438cc11c93e15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139087709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:072f03e4437bff861b82d4ac70cfc6011b4f41d72ab741677a8d2efe213b54d3`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec13befd006fe986be6a8728105412886a583f41f71c6da9a69bcdafc5dca61a`  
		Last Modified: Wed, 13 Aug 2025 07:01:40 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d2aef50f2cd302839668b5ead9b50197b726f5dcab885cc3c48b47965bb73d`  
		Last Modified: Wed, 13 Aug 2025 07:01:41 GMT  
		Size: 7.7 MB (7671345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5301367e88b8bf291aa3e746da27aae27fca920b48b7ec9dce1e5a30e9ac85`  
		Last Modified: Wed, 13 Aug 2025 07:01:40 GMT  
		Size: 349.0 KB (349008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f67cda63d6c6f697113d856d3d51850bdca2557826056f6cc57d464cb605b4`  
		Last Modified: Wed, 13 Aug 2025 07:01:42 GMT  
		Size: 76.3 KB (76335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923cef98fe321ff8257c5ab2d2a257df741860e41a3a4874793e6cad524c5b4b`  
		Last Modified: Wed, 13 Aug 2025 07:01:42 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf41befbfe783db522e1c0f9273d8b3990e28c0ea994bccda5fa465b2377c93`  
		Last Modified: Wed, 13 Aug 2025 07:02:04 GMT  
		Size: 102.9 MB (102903580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb50d4b8156f07b71d73019935a3aee01a295f0c8d11efff59dacb5e0403dea`  
		Last Modified: Wed, 13 Aug 2025 07:01:36 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1d3615bc1b22a46b4b120f3cfa33d9921d4aca1e6575f8e57f41471a4b3c83`  
		Last Modified: Wed, 13 Aug 2025 07:01:36 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b50ca5361151149f77020482ac82c35cd96093e57456c10a50cd045674b2e2`  
		Last Modified: Wed, 13 Aug 2025 07:01:36 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b969e402096d53bed40bccd8c1b4492a774eb07ac9cfc390e7f16d99bc72a5b`  
		Last Modified: Wed, 13 Aug 2025 07:01:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0` - unknown; unknown

```console
$ docker pull couchdb@sha256:11252c508326fc8c25f42c580b0e2c55f29964f7261c2535cb86fd2bcf83d58a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4171217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d992e96908654319a7c0db09c8a678fea16da0a04d698bc9e1e7efd5acb93a`

```dockerfile
```

-	Layers:
	-	`sha256:0862edf1bc3bbd57fe812708c8c761759b6225d3c947158d0cdd755e6019ccfa`  
		Last Modified: Wed, 13 Aug 2025 07:33:23 GMT  
		Size: 4.1 MB (4139242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d3453eb326594daa4b8a25fcbcd3f70fa5c5dd2e143c24097ef3945c15a9ead`  
		Last Modified: Wed, 13 Aug 2025 07:33:23 GMT  
		Size: 32.0 KB (31975 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.0` - linux; s390x

```console
$ docker pull couchdb@sha256:e4a4fc9e58539d2868bd15e046780cd8d8b7a71a74c1eb9f555e22fdf9c0c86b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136521588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec4fca67cecb025b5c09cab9c9549cb681d94892aaf58073a27711545f702b5e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
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
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b7acab8e5e7b12089d79275ac325f69e00c57ef109efebab6c70c9cd73a40d`  
		Last Modified: Wed, 13 Aug 2025 15:09:36 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3abfab6aae8ef4c71d8ee0179a883e31407cdba29d7ec2aedcd6cf479dd3bf`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 7.4 MB (7397830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164187f5523648207c88c10beecff4fa873224418908ed2042111b9008220445`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 355.6 KB (355650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1ea234d9128aa5cf95bed7f6b642ed39541c3ce0421026891a6ae6c3a62cf6`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 76.3 KB (76347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d507f15e04c67e6c028ebaf9b70be03905c6b099f3280dc1ee5b6c61e54fb9`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b32a62c011f37d07095a847adb6849fc8b49b594312b80901dd3fa8730a8f14`  
		Last Modified: Wed, 13 Aug 2025 16:38:43 GMT  
		Size: 101.8 MB (101798492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021c7a0c08391ce264a34acc839e0c22ef3ae30cd5170382d429de2fd535dd89`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8e63f7118f360ea233b6a4b5bfe85601905a9f58ccd1f8e5bd49122797016e`  
		Last Modified: Wed, 13 Aug 2025 15:09:38 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c223e87672740895458e8f91f45b4a146badb15e846fc58f8860c7318a8ff3ab`  
		Last Modified: Wed, 13 Aug 2025 15:09:38 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317e7af7e41277224e9cbb8f9c30c37a3271c0df880f6cf92e4bb22db5ecefe2`  
		Last Modified: Wed, 13 Aug 2025 15:09:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0` - unknown; unknown

```console
$ docker pull couchdb@sha256:37f51edaf047cdf5f5111855683e13ea3c6672c8a15c2251ae5e354aae7a84a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4166926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36fa1cbb03efdd840bd2a162de1c1575a3bbbdb97b9d101b488ed2ce25e1f89`

```dockerfile
```

-	Layers:
	-	`sha256:66a48a697a343af104ea7f47a48904fb5b1d220938d9142743643f1b94344055`  
		Last Modified: Wed, 13 Aug 2025 16:33:26 GMT  
		Size: 4.1 MB (4135145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f50372cd52cb3fa8e4baf039bb58aa2c00bbb482d234fe623bfcf97bd2ac1f1`  
		Last Modified: Wed, 13 Aug 2025 16:33:27 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.0-nouveau`

```console
$ docker pull couchdb@sha256:308b04f6701f381607f7f47d7fb87aad8ed7ef45bb46801f2ebedebfae25008a
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
$ docker pull couchdb@sha256:8827e434487f67468be45e6638e7c262c202df39dab193f7a801d910337e1168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156388372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb51afec84a60b4ccca88637b6171dbf9c7bd64f5abbd8767fd148a8f7c83b86`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f790d8ace6bac688ec09887e051eca9bfb5dcec4060dbfa6e004dbd22c2335`  
		Last Modified: Tue, 12 Aug 2025 22:37:28 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa6399b477180c57907d82946e672511eca816592e7bde3ce7cbef0120d988c`  
		Last Modified: Wed, 13 Aug 2025 00:25:10 GMT  
		Size: 7.9 MB (7881623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a83b3d6009f4d95485272c64af79f09993fd79bf2642286b32d66b25f416bf`  
		Last Modified: Wed, 13 Aug 2025 00:25:20 GMT  
		Size: 77.3 MB (77324598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6505f4ba5ba4d521d87e5366d2ba43a91f994a54206091b2f9fe3bee5a92512f`  
		Last Modified: Tue, 12 Aug 2025 22:37:32 GMT  
		Size: 415.0 KB (415014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340137239ed9b3bc413c49b3966668ac8adb208cf72782ff5b6998c8c82b4275`  
		Last Modified: Tue, 12 Aug 2025 22:37:38 GMT  
		Size: 99.3 KB (99339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bfd6d48df450c319175586a5fc5f9d294e8b9451bc20ee8664c77abb7b7b74`  
		Last Modified: Tue, 12 Aug 2025 22:37:42 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b79bc1a224dbf16495d0825c96460fd749e928fa50b665ef3acbcada31284b2`  
		Last Modified: Wed, 13 Aug 2025 00:25:26 GMT  
		Size: 42.4 MB (42435666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2b0026af08d59058a3ac1b9cced2b8c5e42e21b78bffa8e164ec8f25f5ade8`  
		Last Modified: Tue, 12 Aug 2025 22:37:45 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:4bea6c1a7cfb86229cd87cdd581a659e80cd10d38b553dacb70f9d707510a143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3680310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466ac44f0db72062c95a977798b2237c29ace02c5cfac2dc2dad236a3b1bf388`

```dockerfile
```

-	Layers:
	-	`sha256:5017157d9a64a5a3e554661fa84aa621f6fa241a6fae928cc987a385f56c9a95`  
		Last Modified: Tue, 12 Aug 2025 22:33:25 GMT  
		Size: 3.7 MB (3655746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cf493157d9371e1e4b247e3eba8a5488e8eb19113b6ea7a3c83b9a60e3434e6`  
		Last Modified: Tue, 12 Aug 2025 22:33:26 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.0-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:994d10b57c5e3722231452c10346fb7c8c34339ca3822c23f76fdb864067b9d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155208987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b838d5ea4a740e9b50b8fafda01e1c0c8a8606d55c27f833fe32254fc197f5`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8f56cf1a4ba8c0ad0cfd1f9a290f664d03cebd21fb29d7a9e9979727ad1e16`  
		Last Modified: Wed, 13 Aug 2025 07:20:41 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ba4f4ec6243e7b597450fad0baf17bc5fd50afd711affb2ec4b046f852cee6`  
		Last Modified: Wed, 13 Aug 2025 07:33:35 GMT  
		Size: 7.7 MB (7671369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55aeeee205c8cacbc9c53a1532e4bb6a0211d3d431dfbeab036ba286c2b7baea`  
		Last Modified: Wed, 13 Aug 2025 07:33:39 GMT  
		Size: 76.6 MB (76644110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126318ea349d651273cfa24d6c4ff2541b9c14587b254c7bf0f127e3b43346d9`  
		Last Modified: Wed, 13 Aug 2025 07:20:45 GMT  
		Size: 371.8 KB (371845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a887a5f387999668994717fcfc7a927f5881a898f0cb4294990c361ceefa68d1`  
		Last Modified: Wed, 13 Aug 2025 07:21:05 GMT  
		Size: 99.3 KB (99348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a8a86b6bb6527f3e5bd7b06edbaa53bba62de03804f3c259fd1905f18670a4`  
		Last Modified: Wed, 13 Aug 2025 07:21:09 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f237626ff1625ab3dde05a7210e4027a57e23b7e51354eef2c88d54cd43c3b5`  
		Last Modified: Wed, 13 Aug 2025 08:26:49 GMT  
		Size: 42.3 MB (42338433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539f8c4b7d5a60cd1c8f430ef764660ffed11256b398f7a0634d6d3c7ad48c18`  
		Last Modified: Wed, 13 Aug 2025 07:21:25 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:31975122dcc76847341bc3ffbcab21203e56fd8fc9fd538595da887f88c86d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3679167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121f1940180000a473a7ebac7de6b76e04e001a69ec28f0bfe5498d8b9fecdb9`

```dockerfile
```

-	Layers:
	-	`sha256:bd468b9218245506154339f8e72b6f0a1db496c519e28667d2443c8c01f62cc2`  
		Last Modified: Wed, 13 Aug 2025 07:33:27 GMT  
		Size: 3.7 MB (3654422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ec1fe37a3d7dfcbd8c7fdbe627493b8961635f7a8e6f7ba1c0fc08181ceffec`  
		Last Modified: Wed, 13 Aug 2025 07:33:28 GMT  
		Size: 24.7 KB (24745 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.0-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:73824f0155e246b84dea55564307bb35e5f8c148c20955998c2141c0b530aaaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (150023195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05f9dc355961a03f42bc99f2f59d7ec43cc26298525416313408f7c14cf92e1`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
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
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3477dad2db3c13f403c9d3623e6dfb36742c6965d5f54e5dc14e6cdde7a66a`  
		Last Modified: Wed, 13 Aug 2025 15:10:45 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86997ea5cef151b0f22463c8db32b22377a36a2731a2463041c00e51c38e300a`  
		Last Modified: Wed, 13 Aug 2025 15:10:46 GMT  
		Size: 7.4 MB (7397796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b144c470493ab37c0bb7e68831cbd7adcb46418984ff5c2e15bc9294f2bbf8`  
		Last Modified: Wed, 13 Aug 2025 15:11:09 GMT  
		Size: 73.1 MB (73095781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00131fd1a5e3b4e5c4d46a08db3d5872c0188af95bf15854a2dbf3905f33f8bf`  
		Last Modified: Wed, 13 Aug 2025 15:10:45 GMT  
		Size: 378.1 KB (378144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f80705c9664868350b03281eb24469f3aceb54869ffc9f657263080c30ea5a`  
		Last Modified: Wed, 13 Aug 2025 15:10:46 GMT  
		Size: 99.5 KB (99457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1279ffc778b9acc33d5910aea83aa62f4b55cdb80c97d48981b56efa84efafa3`  
		Last Modified: Wed, 13 Aug 2025 15:10:46 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fee0e258dfab558556571f6bbf5be945aba0594c7d94ded0b2534a3e561ff0`  
		Last Modified: Wed, 13 Aug 2025 15:11:02 GMT  
		Size: 42.2 MB (42162304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3262828dcf86d709adeba6a2659dbcb199cb7c93304d7598634ace98064db058`  
		Last Modified: Wed, 13 Aug 2025 15:10:47 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.0-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:01e73baa3ddf3cc18244596980d9dbcd0715dd0f702b80e3442ad77f92b26036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3670839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c061cd234b8d24d411d7c378a6431d7b93c84e003406baf7937afd63b9eb74`

```dockerfile
```

-	Layers:
	-	`sha256:38077c4ca8e780d7f9c82c3324c4faef42cfd6c9bfa6bb634844fafe940de982`  
		Last Modified: Wed, 13 Aug 2025 16:33:34 GMT  
		Size: 3.6 MB (3646275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77f6c362c5aa68c17e5335c7507046ee6ac7c287bfa8c411dd4e163c833835dd`  
		Last Modified: Wed, 13 Aug 2025 16:33:35 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:432e99b1dbb8bd996b2af964b4731633956e9635548e82b037bda94bb1835193
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
$ docker pull couchdb@sha256:61b1f52d0853861f76353350a313289b31c2ee1b4804c1f6997074d8fcac7cd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139828882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6dbe6ebdaba35a59a45b23d5ce6a95b780604bbb7930465beef5725558681f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f51fa6c894ee9345fe0500a27ff388ecb72eabe2fe3b02d6edd3dc5b3350b93`  
		Last Modified: Tue, 12 Aug 2025 21:23:09 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764b70173c9e8ba1719c81377202f5f41a0420fae43271c3822ee720a613c396`  
		Last Modified: Tue, 12 Aug 2025 21:23:10 GMT  
		Size: 7.9 MB (7881552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6593eef0f94fd50f73d54db6bceb74c820fdaa4d0e2c9aee51d1afbd69b3f62e`  
		Last Modified: Tue, 12 Aug 2025 21:23:10 GMT  
		Size: 392.2 KB (392159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27598109e7c931cfd1cde74aa91bf06dc90e3ab15c837c242a01fb5c90d75f3e`  
		Last Modified: Tue, 12 Aug 2025 21:23:10 GMT  
		Size: 76.3 KB (76305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f674471e32b0c0267121748f62842811c187c1d308ce36cbf5697436e5727b72`  
		Last Modified: Tue, 12 Aug 2025 21:23:10 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3dc16bdec0642eb6c72e582680ee47bb502c5fbd7b2ddaeae7acf21dec07d51`  
		Last Modified: Tue, 12 Aug 2025 21:23:21 GMT  
		Size: 103.2 MB (103243184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75cbcfe770026e1e7036cf243a6b58d887661183d729bdffa652af37138f9f36`  
		Last Modified: Tue, 12 Aug 2025 21:23:10 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d750e10a43cb3769286b8f43be624ca1c41158ea9ea492a534148de3784a81`  
		Last Modified: Tue, 12 Aug 2025 21:23:10 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a114350064b8d1c007ae4c75d6ea1dfa2d9dcdf001b545a18c5083b27445c0`  
		Last Modified: Tue, 12 Aug 2025 21:23:11 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2090b99b69f9563438f44c6cfb8d0c9c55b293d66f6fb682dec49fa5cbb89af0`  
		Last Modified: Tue, 12 Aug 2025 21:23:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:6416bbb6b6baf528846e66900a2e9d6630b091c824bacebb800b8cb2a67336fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4170730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6af04829063d566a11789e76c7fcef29c85e001c106ec14c3efdd9865dd2a8`

```dockerfile
```

-	Layers:
	-	`sha256:f993f71f1e61426d80826a56f7b5044be5a4ca7aa7582f5d5cc145769198982d`  
		Last Modified: Wed, 13 Aug 2025 01:33:20 GMT  
		Size: 4.1 MB (4138949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:982abba7fef1ec1955de60a347341f458aeab3bf621264d1ce41dfdb38ee2913`  
		Last Modified: Wed, 13 Aug 2025 01:33:21 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:d4d661276bc55d6c7c97b92e1a692a06ff8db07bf9faef63722438cc11c93e15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139087709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:072f03e4437bff861b82d4ac70cfc6011b4f41d72ab741677a8d2efe213b54d3`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec13befd006fe986be6a8728105412886a583f41f71c6da9a69bcdafc5dca61a`  
		Last Modified: Wed, 13 Aug 2025 07:01:40 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d2aef50f2cd302839668b5ead9b50197b726f5dcab885cc3c48b47965bb73d`  
		Last Modified: Wed, 13 Aug 2025 07:01:41 GMT  
		Size: 7.7 MB (7671345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5301367e88b8bf291aa3e746da27aae27fca920b48b7ec9dce1e5a30e9ac85`  
		Last Modified: Wed, 13 Aug 2025 07:01:40 GMT  
		Size: 349.0 KB (349008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f67cda63d6c6f697113d856d3d51850bdca2557826056f6cc57d464cb605b4`  
		Last Modified: Wed, 13 Aug 2025 07:01:42 GMT  
		Size: 76.3 KB (76335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923cef98fe321ff8257c5ab2d2a257df741860e41a3a4874793e6cad524c5b4b`  
		Last Modified: Wed, 13 Aug 2025 07:01:42 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf41befbfe783db522e1c0f9273d8b3990e28c0ea994bccda5fa465b2377c93`  
		Last Modified: Wed, 13 Aug 2025 07:02:04 GMT  
		Size: 102.9 MB (102903580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb50d4b8156f07b71d73019935a3aee01a295f0c8d11efff59dacb5e0403dea`  
		Last Modified: Wed, 13 Aug 2025 07:01:36 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1d3615bc1b22a46b4b120f3cfa33d9921d4aca1e6575f8e57f41471a4b3c83`  
		Last Modified: Wed, 13 Aug 2025 07:01:36 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b50ca5361151149f77020482ac82c35cd96093e57456c10a50cd045674b2e2`  
		Last Modified: Wed, 13 Aug 2025 07:01:36 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b969e402096d53bed40bccd8c1b4492a774eb07ac9cfc390e7f16d99bc72a5b`  
		Last Modified: Wed, 13 Aug 2025 07:01:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:11252c508326fc8c25f42c580b0e2c55f29964f7261c2535cb86fd2bcf83d58a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4171217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d992e96908654319a7c0db09c8a678fea16da0a04d698bc9e1e7efd5acb93a`

```dockerfile
```

-	Layers:
	-	`sha256:0862edf1bc3bbd57fe812708c8c761759b6225d3c947158d0cdd755e6019ccfa`  
		Last Modified: Wed, 13 Aug 2025 07:33:23 GMT  
		Size: 4.1 MB (4139242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d3453eb326594daa4b8a25fcbcd3f70fa5c5dd2e143c24097ef3945c15a9ead`  
		Last Modified: Wed, 13 Aug 2025 07:33:23 GMT  
		Size: 32.0 KB (31975 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:e4a4fc9e58539d2868bd15e046780cd8d8b7a71a74c1eb9f555e22fdf9c0c86b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136521588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec4fca67cecb025b5c09cab9c9549cb681d94892aaf58073a27711545f702b5e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
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
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b7acab8e5e7b12089d79275ac325f69e00c57ef109efebab6c70c9cd73a40d`  
		Last Modified: Wed, 13 Aug 2025 15:09:36 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3abfab6aae8ef4c71d8ee0179a883e31407cdba29d7ec2aedcd6cf479dd3bf`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 7.4 MB (7397830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164187f5523648207c88c10beecff4fa873224418908ed2042111b9008220445`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 355.6 KB (355650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1ea234d9128aa5cf95bed7f6b642ed39541c3ce0421026891a6ae6c3a62cf6`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 76.3 KB (76347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d507f15e04c67e6c028ebaf9b70be03905c6b099f3280dc1ee5b6c61e54fb9`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b32a62c011f37d07095a847adb6849fc8b49b594312b80901dd3fa8730a8f14`  
		Last Modified: Wed, 13 Aug 2025 16:38:43 GMT  
		Size: 101.8 MB (101798492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021c7a0c08391ce264a34acc839e0c22ef3ae30cd5170382d429de2fd535dd89`  
		Last Modified: Wed, 13 Aug 2025 15:09:37 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8e63f7118f360ea233b6a4b5bfe85601905a9f58ccd1f8e5bd49122797016e`  
		Last Modified: Wed, 13 Aug 2025 15:09:38 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c223e87672740895458e8f91f45b4a146badb15e846fc58f8860c7318a8ff3ab`  
		Last Modified: Wed, 13 Aug 2025 15:09:38 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317e7af7e41277224e9cbb8f9c30c37a3271c0df880f6cf92e4bb22db5ecefe2`  
		Last Modified: Wed, 13 Aug 2025 15:09:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:37f51edaf047cdf5f5111855683e13ea3c6672c8a15c2251ae5e354aae7a84a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4166926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36fa1cbb03efdd840bd2a162de1c1575a3bbbdb97b9d101b488ed2ce25e1f89`

```dockerfile
```

-	Layers:
	-	`sha256:66a48a697a343af104ea7f47a48904fb5b1d220938d9142743643f1b94344055`  
		Last Modified: Wed, 13 Aug 2025 16:33:26 GMT  
		Size: 4.1 MB (4135145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f50372cd52cb3fa8e4baf039bb58aa2c00bbb482d234fe623bfcf97bd2ac1f1`  
		Last Modified: Wed, 13 Aug 2025 16:33:27 GMT  
		Size: 31.8 KB (31781 bytes)  
		MIME: application/vnd.in-toto+json
