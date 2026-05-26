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
$ docker pull couchdb@sha256:ccea1e8035bf7afd68336e24056a1ca9c1c46d7abe42da686322c0ac7218e5c2
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
$ docker pull couchdb@sha256:09b52d7ef639c76be25a7e09cfa96f0b5c43716341432af6b9b69296c25d947c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142058343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a90b450fc37c41f09cfe760f9e5c41b41a106f5c17861a66a85623393c84a1e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:30 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 May 2026 23:23:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 19 May 2026 23:23:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:23:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 19 May 2026 23:23:38 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 May 2026 23:23:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:23:43 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 19 May 2026 23:23:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 19 May 2026 23:23:57 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 19 May 2026 23:23:57 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 19 May 2026 23:23:57 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 19 May 2026 23:23:57 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 19 May 2026 23:23:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 19 May 2026 23:23:57 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 May 2026 23:23:57 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 May 2026 23:23:57 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 19 May 2026 23:23:57 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d87ffdf697e28d18b4eeb0a8d1d768b895464e0ae7d26f400499188dab4dcf`  
		Last Modified: Tue, 19 May 2026 23:24:10 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d4d2c2632d51f0fee8fb039f27beaecf7928c5c3019b6e371705051245f4e0`  
		Last Modified: Tue, 19 May 2026 23:24:10 GMT  
		Size: 7.9 MB (7884263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b425c7b9d89cf53bd5e690f47d266e2fa1f976ed03c33b5d21208783dfb79e`  
		Last Modified: Tue, 19 May 2026 23:24:10 GMT  
		Size: 401.8 KB (401768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f19c3418d8748695c75c59323373440311c3b75d373a279b5d6f993e0564e03`  
		Last Modified: Tue, 19 May 2026 23:24:10 GMT  
		Size: 76.5 KB (76511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73154ca85a92b6433c5a44e7ffe0f337949da39b5a572708d9d13ba91d546d4`  
		Last Modified: Tue, 19 May 2026 23:24:11 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abc75c4e20b40d156aa48cbcf77a4d397957680a7f96f32d8c1b437fbb7bbd3`  
		Last Modified: Tue, 19 May 2026 23:24:14 GMT  
		Size: 105.5 MB (105456830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899a91b0daaba92f5c2bae2f5fcd951b47148f9eb4e2d9f765f52db961bada33`  
		Last Modified: Tue, 19 May 2026 23:24:12 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc121e2a64ebd3bba759a5b6c1dbf4ee3ec6264cda384ae1174863bceb551d6`  
		Last Modified: Tue, 19 May 2026 23:24:12 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a9e26ff2802324e688ac2dd228284530dd8d636f6d5bcc7e3f654266fd89ee`  
		Last Modified: Tue, 19 May 2026 23:24:12 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f024794f059b1f69b3457a0c98454a9713c9f7757c5e8dc68a2c7b092a02ae`  
		Last Modified: Tue, 19 May 2026 23:24:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:1f38cfbf48b42d81459d804c11a774eb18eea24cda47a2f6b72548261ac1480f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadc2c0087a0b40fe55ea12021314db6ecaf24467fd2fbb0ac38bc5c3c82c9fc`

```dockerfile
```

-	Layers:
	-	`sha256:5970fc12dcc23fbf1c7e1fd5beb8b38148391163230f8df116acfbfa92e81ce9`  
		Last Modified: Tue, 19 May 2026 23:24:10 GMT  
		Size: 4.2 MB (4184439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c3a0078900b2a20ee9590364c77bdacf67a45a1b6459ec64edf2843739594ab`  
		Last Modified: Tue, 19 May 2026 23:24:10 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:b7176956426645f7ab91cfb0673d6fa791c548e69ecb0bdcd31c2322b82459b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141420899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a29d99a11349876560d65720cb2500f758d6c268b4ce83dd003467318e9af9ff`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:27:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 May 2026 23:27:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 19 May 2026 23:27:11 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:14 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 19 May 2026 23:27:14 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 May 2026 23:27:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:19 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 19 May 2026 23:27:19 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 19 May 2026 23:27:33 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 19 May 2026 23:27:33 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 19 May 2026 23:27:33 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 19 May 2026 23:27:33 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 19 May 2026 23:27:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 19 May 2026 23:27:33 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 May 2026 23:27:33 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 May 2026 23:27:33 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 19 May 2026 23:27:33 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207d5e816f1b653cf6cf1dfaf88b2e833edabd255ed64a2ceb4dfb0bb06d3d1d`  
		Last Modified: Tue, 19 May 2026 23:27:46 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee01d5686c343d9d942d5763de8fec23ce28536abbe0edeb563a46123a3e23f3`  
		Last Modified: Tue, 19 May 2026 23:27:47 GMT  
		Size: 7.7 MB (7695155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aead94788b9f92728da249312943ffa094e410bb26f31cb625f5649f6386c87`  
		Last Modified: Tue, 19 May 2026 23:27:46 GMT  
		Size: 370.5 KB (370533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36032904add5ab79f200e99bdce3a29bf50cff2877755d309598f42f64c6c3e`  
		Last Modified: Tue, 19 May 2026 23:27:47 GMT  
		Size: 76.5 KB (76511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5226977736149250abf09625c32d88dd8cc60a048b76a2d0be25f499504c475c`  
		Last Modified: Tue, 19 May 2026 23:27:48 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb6489dfc879dc5a78a4c35fc051c4c879cd2f8be64af5f98a914c859a713f7`  
		Last Modified: Tue, 19 May 2026 23:27:50 GMT  
		Size: 105.2 MB (105158221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9b98d1676bb46f0e83d27fd5c1af5243d83bb39bb53dd97428b3a647dbd673`  
		Last Modified: Tue, 19 May 2026 23:27:48 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4737a0ed9c20e76eb585e449073111217256029e1e87802fb22386fd6192f8`  
		Last Modified: Tue, 19 May 2026 23:27:48 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59688f55bbd7f0cdb249f36b1677326ae7d20d01cc257083b45ad929057b4d6`  
		Last Modified: Tue, 19 May 2026 23:27:49 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c04a6c46e262d21d685073fb9837cc0ee3a8de9d98f978189ea05bf62bac681`  
		Last Modified: Tue, 19 May 2026 23:27:49 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:c4947fd32d28629c9cadc11c3b0b72cff06449499e87ebf82495f38517695a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e70de05fdeea721dfdb1a15f309c4d6b1771ddf910239dc35ef59e7596b4db`

```dockerfile
```

-	Layers:
	-	`sha256:8e08a7d31bd63f26291598eedf87ae610357cbaf462e08316ce235a612e3656f`  
		Last Modified: Tue, 19 May 2026 23:27:47 GMT  
		Size: 4.2 MB (4184732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1878dfd62c3c800a27e5ab10bfc19849cbbd5816c82a3ad6735ea1e12233099`  
		Last Modified: Tue, 19 May 2026 23:27:47 GMT  
		Size: 31.9 KB (31932 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; s390x

```console
$ docker pull couchdb@sha256:76de6eff1c868ce94a63d2ddd5b5fd721b0055d8f6733ed5f09d7ff6232bf2f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138771252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f44a4c43a005d699aa1531f111caf142341bcefd98b1978c25a8746f544cad77`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:19:13 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 20 May 2026 00:19:13 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 20 May 2026 00:19:19 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:19:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 20 May 2026 00:19:22 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 20 May 2026 00:19:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:19:27 GMT
ENV COUCHDB_VERSION=3.5.1
# Wed, 20 May 2026 00:19:27 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 20 May 2026 00:19:44 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 20 May 2026 00:19:44 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 20 May 2026 00:19:44 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 20 May 2026 00:19:44 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 00:19:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 20 May 2026 00:19:44 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 20 May 2026 00:19:44 GMT
VOLUME [/opt/couchdb/data]
# Wed, 20 May 2026 00:19:44 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 20 May 2026 00:19:44 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2119d20228b0ee7dc34f2d8ae50ddc482133d4a46b75ef39cee53837e06a0b`  
		Last Modified: Wed, 20 May 2026 00:20:05 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a006620367a25e0aa2b2d85669f3382121b884eac2d944403ea899a9f28bc3a`  
		Last Modified: Wed, 20 May 2026 00:20:05 GMT  
		Size: 7.4 MB (7400088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a087ffd583427a623a7fbb6d5cd92146fa7fe562b3691275df4895f13a96e4`  
		Last Modified: Wed, 20 May 2026 00:20:05 GMT  
		Size: 372.2 KB (372152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d614b0a4ac50680b2c89e16a8817e441882e4f8a74c0efa6a724b927bfe5d32c`  
		Last Modified: Wed, 20 May 2026 00:20:05 GMT  
		Size: 76.5 KB (76539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a870d76e1f3afb6201a63608520cb8174f7d1672346eb3332cea2e37f4f1cd9e`  
		Last Modified: Wed, 20 May 2026 00:20:06 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5adb01efb8694d80e39bf12de91b861383f6a88f7add83424b5800e99b96d67`  
		Last Modified: Wed, 20 May 2026 00:20:08 GMT  
		Size: 104.0 MB (104028456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02b4b27d6d6743e59c472d833f03c8e80f4f507c5e1af57920390734a0cc4da`  
		Last Modified: Wed, 20 May 2026 00:20:06 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd01387718dcd18b409353134fe1a48b7fe039050318bae2d83f749251e5b5a`  
		Last Modified: Wed, 20 May 2026 00:20:06 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8be35f18dfda1fa008590a40a550ebca59f6feed5a0751df486655b973a0ad`  
		Last Modified: Wed, 20 May 2026 00:20:07 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad1c999649df933c865b874c165aa1b98893f1713eca21e8950faf01c71c761`  
		Last Modified: Wed, 20 May 2026 00:20:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:c7b89f39f6c9ed1b5219d4c80c4784e6b9e01549aa3d7281d999206e67c3271f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4072facf62633c168c635a226652d1e5441034a1ccd5b7c7e651f24e590b338`

```dockerfile
```

-	Layers:
	-	`sha256:ca3e264ce2fe47ba09799d31e60d681d285326875424c22ac69285baca76978b`  
		Last Modified: Wed, 20 May 2026 00:20:05 GMT  
		Size: 4.2 MB (4180635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7ceacf997acb8d668e341d6b8b2c3661a2bed3e4152acf1c0cb8c3fdbc63069`  
		Last Modified: Wed, 20 May 2026 00:20:05 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:1ac782d8867be6b364c566f43ed5302d4b91c7e189cc26385ff6936fa352c557
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
$ docker pull couchdb@sha256:a53952e2264a34693a7fcbd17adf5ffaa3d6f27763251ad21644b2aefcfd2b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.6 MB (156557623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071f487d402e6cb43464653c9e1a195e772104291531869a5fe8f948995d6c08`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:37 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 May 2026 23:23:37 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 19 May 2026 23:23:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:23:52 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:23:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 19 May 2026 23:23:54 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 May 2026 23:23:59 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:23:59 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 19 May 2026 23:24:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 19 May 2026 23:24:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 19 May 2026 23:24:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 19 May 2026 23:24:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 19 May 2026 23:24:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f55187b4934e056c680d6e91549329607ce47ec51776501ac73d8bc1bba9176`  
		Last Modified: Tue, 19 May 2026 23:24:20 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd0bc89c040283119b651af145e97ef098cc1b2b054e3e7bf7af6dc8adf211a6`  
		Last Modified: Tue, 19 May 2026 23:24:20 GMT  
		Size: 7.9 MB (7884206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44649a9110a9a5ccd1737df67a46e606d02b61085ae41dfe63409416c4ee8ec`  
		Last Modified: Tue, 19 May 2026 23:24:22 GMT  
		Size: 77.5 MB (77477908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae71b0eed42b7d26bdb16759f9bfd007eabd413cac68409c5613c165a64dd6f`  
		Last Modified: Tue, 19 May 2026 23:24:20 GMT  
		Size: 424.2 KB (424171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303155b8a67b8b99800b9a2204efb2d5f2aefb9cc20a9486117646b1b72d644b`  
		Last Modified: Tue, 19 May 2026 23:24:21 GMT  
		Size: 99.6 KB (99627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76daa6193200c830022f9be24af04803cf3c8dad18832c8acf36765fa10c224`  
		Last Modified: Tue, 19 May 2026 23:24:21 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febec42ec387c3429c25295b90efc0b4fce77a7f36bbee9e5f1d1b5af995b186`  
		Last Modified: Tue, 19 May 2026 23:24:22 GMT  
		Size: 42.4 MB (42436288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d598b8820fe2b2b91338ba428d09274914f7d04d3d357ee0942258ebe38c65`  
		Last Modified: Tue, 19 May 2026 23:24:22 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:94c7834a10dd38e96a47d2b062a70093c61257a2223b3c5c558f84c360e0bcee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3683480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a58f59868ef764a8218f59ec8e51f8148a561b74654e80458a6cc74b6584a318`

```dockerfile
```

-	Layers:
	-	`sha256:bb1647008b09a4338f745df17b41aa347576085b74c7f10332f96afc36d34444`  
		Last Modified: Tue, 19 May 2026 23:24:20 GMT  
		Size: 3.7 MB (3658959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:174075f2d213288f23092903ba95fd10d4b8356b833edd7c83c0987b0e32c5ef`  
		Last Modified: Tue, 19 May 2026 23:24:19 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:9a59349312a5702bb7bff3346726c6d7e1c37df0e5723f8dbd041bec8e5cd9f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155436748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aca94e84d6e887330b70a1a271457b445394a33d7ca0c9ae07a22eb400c8a76`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:27:09 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 May 2026 23:27:09 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 19 May 2026 23:27:15 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:23 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 19 May 2026 23:27:25 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 May 2026 23:27:30 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:30 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 19 May 2026 23:27:36 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 19 May 2026 23:27:36 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 19 May 2026 23:27:36 GMT
VOLUME [/opt/nouveau/data]
# Tue, 19 May 2026 23:27:36 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 19 May 2026 23:27:36 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0660a5ba91ed2ceb43e5ba98840c9a45b676fc87e8d521ff727eb0d7a1389f13`  
		Last Modified: Tue, 19 May 2026 23:27:51 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40157edc7727629f8fe52bb2d849f861475f0bc518d76d6a004a67da5a605fb3`  
		Last Modified: Tue, 19 May 2026 23:27:51 GMT  
		Size: 7.7 MB (7695099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6efcd070ffca23467b828b1bfd13af99d03f56a3abedf45b27059da3c9fae7`  
		Last Modified: Tue, 19 May 2026 23:27:55 GMT  
		Size: 76.8 MB (76793447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8467613a6e749c52d0ec773927373f9cb960f95fd10fc2dbee3b762f4bee39a2`  
		Last Modified: Tue, 19 May 2026 23:27:51 GMT  
		Size: 392.8 KB (392776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9d3c250fd125a835a2adff1a24d315e2da082db0eec62940fa83779419335b`  
		Last Modified: Tue, 19 May 2026 23:27:52 GMT  
		Size: 99.5 KB (99523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54db9e883bb069403d111165a75ab234a2524c59667021def0c2016daf2647e`  
		Last Modified: Tue, 19 May 2026 23:27:52 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f298e4411d38607887f8a92d3f51fb1fc315bf47f696318f2e4311f3db44fa8`  
		Last Modified: Tue, 19 May 2026 23:27:55 GMT  
		Size: 42.3 MB (42338980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d05cdc4e9cb7f6ac6d18eb69732dbf99e6eec99e64a83b5751d5db66599eeb`  
		Last Modified: Tue, 19 May 2026 23:27:54 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:94aca52e7d9afe99912951c1431c803d81a49e915b30d263fb198d6b5399850a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:899adac63c9796e2bf48ba07185e219ff1546bc77e1ec817d07c5011ae76041a`

```dockerfile
```

-	Layers:
	-	`sha256:d887223f03033388ec110a35f1585bb3fb6c4c574684c0fe5e9ff91fc3a19ecc`  
		Last Modified: Tue, 19 May 2026 23:27:51 GMT  
		Size: 3.7 MB (3657639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49422572d47602cc606a6c5d156205a36ed7e4ea6e0f0f0b29c33a67752677c9`  
		Last Modified: Tue, 19 May 2026 23:27:51 GMT  
		Size: 24.7 KB (24703 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:d1330882e3531b96283ce80dbed9f713adb21b7ba633e089ef83921669d8f23f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.2 MB (150174644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e732564359f80d5ae39b646d3271a461f174828f6e2e4f926f8c5ff3d8daf86e`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:19:26 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 20 May 2026 00:19:26 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 20 May 2026 00:19:33 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:19:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:19:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 20 May 2026 00:19:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 20 May 2026 00:19:50 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:19:50 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 20 May 2026 00:19:57 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 20 May 2026 00:19:57 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 20 May 2026 00:19:57 GMT
VOLUME [/opt/nouveau/data]
# Wed, 20 May 2026 00:19:57 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 20 May 2026 00:19:57 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735715cce2082c3ee3f9a3e1340e641fd3c8a4c27a986dfa1e0711d23ab1bfd3`  
		Last Modified: Wed, 20 May 2026 00:20:19 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d408f2f91f087b84b8fc0b5eaab3a385e9c71c6d1aea5cdd41add6b52a42875`  
		Last Modified: Wed, 20 May 2026 00:20:20 GMT  
		Size: 7.4 MB (7400058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9862fef3db5700ef619b2c3c7787c171007e7038deabe8151310df8531e354c4`  
		Last Modified: Wed, 20 May 2026 00:20:20 GMT  
		Size: 73.2 MB (73225383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa09fc31e5567156b4208ae4d6e44d3f8c7fcc9372b1f65223c892703e7b785`  
		Last Modified: Wed, 20 May 2026 00:20:19 GMT  
		Size: 394.5 KB (394501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93eb29090836c1a783acc896684e8094b507792c57f4e34f997b56fbbe53038e`  
		Last Modified: Wed, 20 May 2026 00:20:20 GMT  
		Size: 99.7 KB (99671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6bf9c655d2ba99361dd631c89376c408f4241337194d618f695647f46b1893`  
		Last Modified: Wed, 20 May 2026 00:20:20 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1626c6f29ea03bd3f02121e49788d0a1598081af520493c082775a80212c2a0e`  
		Last Modified: Wed, 20 May 2026 00:20:22 GMT  
		Size: 42.2 MB (42164559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb3708c7856914821db2d45a870a7b4f276ee63a1504d8a0351be2a7ad0f0df`  
		Last Modified: Wed, 20 May 2026 00:20:21 GMT  
		Size: 415.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:74bf10806c26372b203e56e1b669533da4bcf86947e45c64c0495cdf0891b8fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3674013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a63f7ef1e02ba24716d614c580430054a0f24e9fce3a171f078aed465c00f31c`

```dockerfile
```

-	Layers:
	-	`sha256:c88ba0d2fa26953de302b0ce999917e535786ca1ff751c6d58afc4a1e8a50c15`  
		Last Modified: Wed, 20 May 2026 00:20:19 GMT  
		Size: 3.6 MB (3649492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9efadf28d263fc1c7ab013f81ed2a347b116742fb90a18583835275affb68c35`  
		Last Modified: Wed, 20 May 2026 00:20:19 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4`

```console
$ docker pull couchdb@sha256:9cce5bc04939873f599c1ea6dc1cd4c7f167c211d66f3b75c4194bea1ed414c4
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
$ docker pull couchdb@sha256:da9dfd0b56b3f19f977bdf49b88bcbaac99cab1b137c0a1e6f0eacdc16dac825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139021530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5389ab5904456ba37bc7dcc4b60ce55420ccb79bf6f58486ccc5ed64c9e314`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:39 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 May 2026 23:23:39 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 19 May 2026 23:23:45 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:23:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 19 May 2026 23:23:48 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 May 2026 23:23:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:23:53 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 19 May 2026 23:23:53 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 19 May 2026 23:24:07 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 19 May 2026 23:24:07 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 19 May 2026 23:24:07 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 19 May 2026 23:24:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 19 May 2026 23:24:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 19 May 2026 23:24:07 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 May 2026 23:24:07 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 May 2026 23:24:07 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 19 May 2026 23:24:07 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1262100da0332167345f1c3f8a8958fa9a26874c27a4b57b6a3a30856037301f`  
		Last Modified: Tue, 19 May 2026 23:24:20 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ada3b1dc40cc15c77f2669616d8c01ea1138da9b81fc178bee72aa0538bfb6`  
		Last Modified: Tue, 19 May 2026 23:24:21 GMT  
		Size: 7.9 MB (7884230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2414144aa61f08516e81e5fdfd052c4e4f0e1502d90dcdd8abf0e2b6b68995`  
		Last Modified: Tue, 19 May 2026 23:24:21 GMT  
		Size: 401.8 KB (401770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135f72b7003198b2a94e736b698889c65472538ee43218073f30592400c94c72`  
		Last Modified: Tue, 19 May 2026 23:24:21 GMT  
		Size: 76.5 KB (76515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76c826d6272c2e2b12dfddef78fc3d67096b627464b457e4957432ef8f88869`  
		Last Modified: Tue, 19 May 2026 23:24:22 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beba1e49e0306ddfebc9e1b048d9b1c11b6bab6e93342992c8537ac36719ae10`  
		Last Modified: Tue, 19 May 2026 23:24:25 GMT  
		Size: 102.4 MB (102420035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c21ae961cc871d4dbdec90d331edc5a0fd7dd76672dc41e03624ccff1ada048`  
		Last Modified: Tue, 19 May 2026 23:24:22 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4dd5d9fafaf05c89374d93f2212ce0cdecefe313d8ea9ef5d3d7bbd9fd504c`  
		Last Modified: Tue, 19 May 2026 23:24:23 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7984aba3dbbb4eb6e29d581bca0bdb234a8edf69a094debd1eb55ca739e7d1`  
		Last Modified: Tue, 19 May 2026 23:24:23 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d41909fdbd5f49d26bcf56adceadb68df102431f4fa1faec539e888ac0b114f`  
		Last Modified: Tue, 19 May 2026 23:24:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:f0fc03dfaf8bda1f4f036a5310dfd064549350dde25f5b90ad11683ff086b5e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d698b479d5e1e28523c60764e45db15661ce65609fd3e136c5f1118337f8aa0`

```dockerfile
```

-	Layers:
	-	`sha256:fb84baa222cf5738f1fc4eda1aa42743c3d324f36d9378cf4dc5c642c599bc26`  
		Last Modified: Tue, 19 May 2026 23:24:21 GMT  
		Size: 4.1 MB (4125413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6c589b3463b8e04d89e1627ed9442cca79f5d301117a77e8e425cff7eb8d826`  
		Last Modified: Tue, 19 May 2026 23:24:20 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:4ba0bdf097abd17ae046318d9c76996bf3e4ab2cfe23035b1145ee20844bc3d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138432129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7640d7a1a9851a160111f910f34fcdb4731c03d9288ba1f7bd3da327e8a01a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:27:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 May 2026 23:27:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 19 May 2026 23:27:18 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 19 May 2026 23:27:21 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 May 2026 23:27:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:27 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 19 May 2026 23:27:27 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 19 May 2026 23:27:39 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 19 May 2026 23:27:39 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 19 May 2026 23:27:39 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 19 May 2026 23:27:39 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 19 May 2026 23:27:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 19 May 2026 23:27:39 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 May 2026 23:27:39 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 May 2026 23:27:39 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 19 May 2026 23:27:39 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e24e8c7fa768cc75e150b10e330b1a3a0dae912a24792f5390bb8e784d276e`  
		Last Modified: Tue, 19 May 2026 23:27:52 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9be4175f9e60c07473387372d8b1cc1d73a9ca8371b0f9e862c969768332df`  
		Last Modified: Tue, 19 May 2026 23:27:53 GMT  
		Size: 7.7 MB (7695136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60895f958d75b236cbd3de1a7743caa9e7e5541440dc66e3570b8aee43b8460d`  
		Last Modified: Tue, 19 May 2026 23:27:52 GMT  
		Size: 370.5 KB (370518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b727c0acdbaf659ee8d9719167b91704919f9b7261443de1634fb4134c896691`  
		Last Modified: Tue, 19 May 2026 23:27:52 GMT  
		Size: 76.5 KB (76494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7b37b356bbcf3e6ec862220aafb20c2d2cdf6f4271416dda5aa35b50063742`  
		Last Modified: Tue, 19 May 2026 23:27:53 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84790b386021daac75f5318352d72adb33c403620ccb6ef75a4145752d31ded`  
		Last Modified: Tue, 19 May 2026 23:28:00 GMT  
		Size: 102.2 MB (102169501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561a494cfc5b960fa1f0d22909ab94a0eb86faaccb0ffb511df42dbd2e6acbd6`  
		Last Modified: Tue, 19 May 2026 23:27:54 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc2e727f7d8d0ac6b84d7f32fd4a674ec3ec855702794c727fa4c5a31f7d277`  
		Last Modified: Tue, 19 May 2026 23:27:54 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffef35d93e31e4c7a411a7f382d68fdc09c0dce5e39d3e1b51baf52032914350`  
		Last Modified: Tue, 19 May 2026 23:27:55 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03290f47b7e4fdfd4a628ec8ce171c4c15aa514f56a489351cd2d819b019209a`  
		Last Modified: Tue, 19 May 2026 23:27:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:349654ff9e5346cee26e33294616538047ecda436e09a34b45efd236fee9060d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4157000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a7f538c545a1031ff02a6c87b5dd80dcf3110b8b99893f4a26fdb170d14bbe2`

```dockerfile
```

-	Layers:
	-	`sha256:e755df63d492cacf092f8cf8bca007aff36d9d3f56e410d75beb5e35c8a3d408`  
		Last Modified: Tue, 19 May 2026 23:27:52 GMT  
		Size: 4.1 MB (4125682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:babc27fcaf933d28f19d1aa7a1d216f997fb332cc79b527263d664b4f945e1e9`  
		Last Modified: Tue, 19 May 2026 23:27:52 GMT  
		Size: 31.3 KB (31318 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; s390x

```console
$ docker pull couchdb@sha256:e781ab57f107167881e4db431f78e4f064e945de629ea29bf316660ba74c2960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135799283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062e4f15317b3254d5e2464e22455b60685314becd06ed6aec4158195e33b9ef`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:19:13 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 20 May 2026 00:19:13 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 20 May 2026 00:19:19 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:19:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 20 May 2026 00:19:22 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 20 May 2026 00:19:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:19:27 GMT
ENV COUCHDB_VERSION=3.4.3
# Wed, 20 May 2026 00:20:26 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 20 May 2026 00:20:42 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 20 May 2026 00:20:42 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 20 May 2026 00:20:42 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 20 May 2026 00:20:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 00:20:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 20 May 2026 00:20:42 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 20 May 2026 00:20:42 GMT
VOLUME [/opt/couchdb/data]
# Wed, 20 May 2026 00:20:42 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 20 May 2026 00:20:42 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2119d20228b0ee7dc34f2d8ae50ddc482133d4a46b75ef39cee53837e06a0b`  
		Last Modified: Wed, 20 May 2026 00:20:05 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a006620367a25e0aa2b2d85669f3382121b884eac2d944403ea899a9f28bc3a`  
		Last Modified: Wed, 20 May 2026 00:20:05 GMT  
		Size: 7.4 MB (7400088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a087ffd583427a623a7fbb6d5cd92146fa7fe562b3691275df4895f13a96e4`  
		Last Modified: Wed, 20 May 2026 00:20:05 GMT  
		Size: 372.2 KB (372152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d614b0a4ac50680b2c89e16a8817e441882e4f8a74c0efa6a724b927bfe5d32c`  
		Last Modified: Wed, 20 May 2026 00:20:05 GMT  
		Size: 76.5 KB (76539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89faf5f17de2b2b482ddd66c4d475c7b419239d8742d05dbd95eaaa6d8b6ebe`  
		Last Modified: Wed, 20 May 2026 00:21:02 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf982cfac72c8ce5675c24908face2e97a41c66c513fa73a7f98f32887929e0`  
		Last Modified: Wed, 20 May 2026 00:21:04 GMT  
		Size: 101.1 MB (101056473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737006e8dd12dc6a7920d4dbba81a2adcf894b9cfd9f08ab2d3d145a8cd45709`  
		Last Modified: Wed, 20 May 2026 00:21:02 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e2d485598b4cebfc1a39eebe635307861eaa609fb69ff124c4f154eda4967c`  
		Last Modified: Wed, 20 May 2026 00:21:02 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa737a67a9719364a9f105ceed1a7ec93c62cab245ba118dd0e4a833951aaee`  
		Last Modified: Wed, 20 May 2026 00:21:03 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bfdb266525bb6bb7c2ae862c3481a27a3daffcf35d31fdc308a35b0ca885e3`  
		Last Modified: Wed, 20 May 2026 00:21:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:d021b449200ed580cbbbe31a87fbc1819de9e7184a28bce4de7c1a2320239f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aca100fbcff26d70e9c7b924c2c1e92801717ad8da1b502e4ef4426921c585a`

```dockerfile
```

-	Layers:
	-	`sha256:4ba18fc91a85113f0265a18ad5ef30da02285ac1407b69d4061a53071b7a8dc0`  
		Last Modified: Wed, 20 May 2026 00:21:02 GMT  
		Size: 4.1 MB (4121609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70d0601c2dade617704cfd0f266a23794d0e8fb0d1aa9449d1b9417f1c595b8f`  
		Last Modified: Wed, 20 May 2026 00:21:02 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4-nouveau`

```console
$ docker pull couchdb@sha256:b65a46e8e77e3ceb3cc7422e50ba4a8cf13b1edb45865d9b9bd4f9afeead8498
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
$ docker pull couchdb@sha256:1b28577b7e1406b3097460f849c00ea0ad9e3d222e6f2468773509f43cb8a2dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.6 MB (156557052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f559137e9771bc303aa4ca977cbb1c8aab911b77e4d2b6e86c44e18fdcbd79`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 May 2026 23:23:40 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 19 May 2026 23:23:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:23:52 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:23:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 19 May 2026 23:23:54 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 May 2026 23:23:57 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:23:58 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 19 May 2026 23:24:02 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 19 May 2026 23:24:02 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 19 May 2026 23:24:02 GMT
VOLUME [/opt/nouveau/data]
# Tue, 19 May 2026 23:24:02 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 19 May 2026 23:24:02 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034254b8e01952c9c67ffb0d8201fea6ebaf4775ea8cd7ac91b509de3f1ed3cc`  
		Last Modified: Tue, 19 May 2026 23:24:18 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ab98cf14d02a29c4aa86f540fe6c9889bd595c7a5db98d9d74981914478c16`  
		Last Modified: Tue, 19 May 2026 23:24:19 GMT  
		Size: 7.9 MB (7884170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df177a882181db0ec0c60e4aaf9fd94a18c1e34280e5e15946ed2cd69c4904b0`  
		Last Modified: Tue, 19 May 2026 23:24:21 GMT  
		Size: 77.5 MB (77477910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2fcee25a09246222319e9d38fef98b79c45d8595a47e3e3d9e462078276f09`  
		Last Modified: Tue, 19 May 2026 23:24:18 GMT  
		Size: 424.1 KB (424149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3576391464b6e7080306d56d23930c9ea9ba29bd0f95e3be148fe155b12a1de7`  
		Last Modified: Tue, 19 May 2026 23:24:20 GMT  
		Size: 99.6 KB (99563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babd490be78878864bc284dcf28a23e501af9f9260196bb80f61429b8d461e1e`  
		Last Modified: Tue, 19 May 2026 23:24:20 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59817ab8b38f3c70e51a30216d2038aa6eba6ff190c71bdce4d7fcfb976ebd08`  
		Last Modified: Tue, 19 May 2026 23:24:21 GMT  
		Size: 42.4 MB (42435835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99aee7e3b66f991598df233f16dd0b28b833e965fbdb7e02a4370c18806a70b7`  
		Last Modified: Tue, 19 May 2026 23:24:21 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:626d48c311ffef0cf077ed4d2e06c70f4bb5dda0863d6623f6b580dae5330064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc25db8e2d359542585ef547dd522d304d4bddf3581e9bd5e43eec9c2255092`

```dockerfile
```

-	Layers:
	-	`sha256:bdac17e5c586326819a4977371c126aca1b183b1a4e823a9bfafd8ee4559a90b`  
		Last Modified: Tue, 19 May 2026 23:24:19 GMT  
		Size: 3.7 MB (3658653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3454d1187cebbe56eb5cef5de8e167ba87117fa0d0547c1d40e8e9152059bf96`  
		Last Modified: Tue, 19 May 2026 23:24:18 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:cefdb1385ab4a451d2aea210ccc3ea8760acaa52067780e3a4836be3e39da549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155435730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b36ceedfbd6190ca9b093c68d82626c05d620f7a694f0efc30c37d909654e6cd`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:27:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 May 2026 23:27:19 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 19 May 2026 23:27:25 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 19 May 2026 23:27:34 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 May 2026 23:27:38 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:38 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 19 May 2026 23:27:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 19 May 2026 23:27:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 19 May 2026 23:27:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 19 May 2026 23:27:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 19 May 2026 23:27:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b431e0800be10532b8cdccd281d397a606f541a408e919fe06261c077301a006`  
		Last Modified: Tue, 19 May 2026 23:27:57 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42477eae5cec1dedc000ef75f969c8a87f8769385122615b007e689d818716dc`  
		Last Modified: Tue, 19 May 2026 23:27:58 GMT  
		Size: 7.7 MB (7695083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a0fe90886376d1d4d332acfec00cd36ca36b57e90eaf4785f5aafbc63ae938`  
		Last Modified: Tue, 19 May 2026 23:28:00 GMT  
		Size: 76.8 MB (76793468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c465194c14ac1c736796410733d7a5dd83b39c68678383ed896651efea8df5d5`  
		Last Modified: Tue, 19 May 2026 23:27:58 GMT  
		Size: 392.8 KB (392782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27d9b7f356e47858f4d282ed5f6d14748a682626af2ec2c978da028b1f07d89f`  
		Last Modified: Tue, 19 May 2026 23:27:59 GMT  
		Size: 99.5 KB (99507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7288fcfdfcbdabf602e1d2b92be07ebd2731eb28a2c85ef2449a25f9ff79b92`  
		Last Modified: Tue, 19 May 2026 23:27:59 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47eb77540f225caf0dfd731cd23c6d99c4eacab7fcc32501206406f3f058a84e`  
		Last Modified: Tue, 19 May 2026 23:28:00 GMT  
		Size: 42.3 MB (42337966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c05e22b278e6181c2299b996a4312ce0d6f6f193cc6d490ad06bacf56bddb4e`  
		Last Modified: Tue, 19 May 2026 23:28:00 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:b291a7b3423e66d516c470f2bd971e08d78f6da85685811ec75a2e44afeb9b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aacc0519a174443d14e7e47f321ddc3d964ee5c2a44354f8776f70174215d93`

```dockerfile
```

-	Layers:
	-	`sha256:1f9e0d0e366e8d52579f2d7bbea0d58216660c96b6ed8aef682d7e2dd8dd6635`  
		Last Modified: Tue, 19 May 2026 23:27:58 GMT  
		Size: 3.7 MB (3657321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2e306c7e7342dc8957898406f6555b25411a7f849b9aa21a7fd768e2f9b3c5c`  
		Last Modified: Tue, 19 May 2026 23:27:57 GMT  
		Size: 24.4 KB (24384 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:4dc2a0634528573ef1a7cf7f418b30902b021c6f36a8f97ab045b809a25cdbcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.2 MB (150172945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9bbd6c813f57e84313da6c907f21e34ca378e73a80a6881e14f03e124f96546`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:19:26 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 20 May 2026 00:19:26 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 20 May 2026 00:19:33 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:19:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:19:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 20 May 2026 00:19:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 20 May 2026 00:19:50 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:19:50 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 20 May 2026 00:20:48 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 20 May 2026 00:20:48 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 20 May 2026 00:20:48 GMT
VOLUME [/opt/nouveau/data]
# Wed, 20 May 2026 00:20:48 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 20 May 2026 00:20:48 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735715cce2082c3ee3f9a3e1340e641fd3c8a4c27a986dfa1e0711d23ab1bfd3`  
		Last Modified: Wed, 20 May 2026 00:20:19 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d408f2f91f087b84b8fc0b5eaab3a385e9c71c6d1aea5cdd41add6b52a42875`  
		Last Modified: Wed, 20 May 2026 00:20:20 GMT  
		Size: 7.4 MB (7400058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9862fef3db5700ef619b2c3c7787c171007e7038deabe8151310df8531e354c4`  
		Last Modified: Wed, 20 May 2026 00:20:20 GMT  
		Size: 73.2 MB (73225383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa09fc31e5567156b4208ae4d6e44d3f8c7fcc9372b1f65223c892703e7b785`  
		Last Modified: Wed, 20 May 2026 00:20:19 GMT  
		Size: 394.5 KB (394501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93eb29090836c1a783acc896684e8094b507792c57f4e34f997b56fbbe53038e`  
		Last Modified: Wed, 20 May 2026 00:20:20 GMT  
		Size: 99.7 KB (99671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6bf9c655d2ba99361dd631c89376c408f4241337194d618f695647f46b1893`  
		Last Modified: Wed, 20 May 2026 00:20:20 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70b8ea5924d1d6ddeed842229d696c5d7339bd591d0a4e18332a1f853a14128`  
		Last Modified: Wed, 20 May 2026 00:21:04 GMT  
		Size: 42.2 MB (42162858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa511f6c6cad159de580bb827928f4c832dd41ea35ceadcdaa771c67a8626b38`  
		Last Modified: Wed, 20 May 2026 00:21:03 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:ab6d822426e364949911ae45953e5655df9dd41fd3fe427a2c6ffcadb3c58b1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e185b56f0a0f457d0e0345bf17a86dd144c6c0429136757651eaf6c322a5b998`

```dockerfile
```

-	Layers:
	-	`sha256:f350fdb2b2edbfa085859a68071502e2d0eda2f585d913dea3203739704f57fe`  
		Last Modified: Wed, 20 May 2026 00:21:03 GMT  
		Size: 3.6 MB (3649186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16c57fb6fb6ffd2ff26271b6130b1d5df9c6e6c7cdf5779f88c271f91018c041`  
		Last Modified: Wed, 20 May 2026 00:21:03 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3`

```console
$ docker pull couchdb@sha256:9cce5bc04939873f599c1ea6dc1cd4c7f167c211d66f3b75c4194bea1ed414c4
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
$ docker pull couchdb@sha256:da9dfd0b56b3f19f977bdf49b88bcbaac99cab1b137c0a1e6f0eacdc16dac825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139021530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5389ab5904456ba37bc7dcc4b60ce55420ccb79bf6f58486ccc5ed64c9e314`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:39 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 May 2026 23:23:39 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 19 May 2026 23:23:45 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:23:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 19 May 2026 23:23:48 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 May 2026 23:23:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:23:53 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 19 May 2026 23:23:53 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 19 May 2026 23:24:07 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 19 May 2026 23:24:07 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 19 May 2026 23:24:07 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 19 May 2026 23:24:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 19 May 2026 23:24:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 19 May 2026 23:24:07 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 May 2026 23:24:07 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 May 2026 23:24:07 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 19 May 2026 23:24:07 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1262100da0332167345f1c3f8a8958fa9a26874c27a4b57b6a3a30856037301f`  
		Last Modified: Tue, 19 May 2026 23:24:20 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ada3b1dc40cc15c77f2669616d8c01ea1138da9b81fc178bee72aa0538bfb6`  
		Last Modified: Tue, 19 May 2026 23:24:21 GMT  
		Size: 7.9 MB (7884230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2414144aa61f08516e81e5fdfd052c4e4f0e1502d90dcdd8abf0e2b6b68995`  
		Last Modified: Tue, 19 May 2026 23:24:21 GMT  
		Size: 401.8 KB (401770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135f72b7003198b2a94e736b698889c65472538ee43218073f30592400c94c72`  
		Last Modified: Tue, 19 May 2026 23:24:21 GMT  
		Size: 76.5 KB (76515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76c826d6272c2e2b12dfddef78fc3d67096b627464b457e4957432ef8f88869`  
		Last Modified: Tue, 19 May 2026 23:24:22 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beba1e49e0306ddfebc9e1b048d9b1c11b6bab6e93342992c8537ac36719ae10`  
		Last Modified: Tue, 19 May 2026 23:24:25 GMT  
		Size: 102.4 MB (102420035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c21ae961cc871d4dbdec90d331edc5a0fd7dd76672dc41e03624ccff1ada048`  
		Last Modified: Tue, 19 May 2026 23:24:22 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4dd5d9fafaf05c89374d93f2212ce0cdecefe313d8ea9ef5d3d7bbd9fd504c`  
		Last Modified: Tue, 19 May 2026 23:24:23 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7984aba3dbbb4eb6e29d581bca0bdb234a8edf69a094debd1eb55ca739e7d1`  
		Last Modified: Tue, 19 May 2026 23:24:23 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d41909fdbd5f49d26bcf56adceadb68df102431f4fa1faec539e888ac0b114f`  
		Last Modified: Tue, 19 May 2026 23:24:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:f0fc03dfaf8bda1f4f036a5310dfd064549350dde25f5b90ad11683ff086b5e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d698b479d5e1e28523c60764e45db15661ce65609fd3e136c5f1118337f8aa0`

```dockerfile
```

-	Layers:
	-	`sha256:fb84baa222cf5738f1fc4eda1aa42743c3d324f36d9378cf4dc5c642c599bc26`  
		Last Modified: Tue, 19 May 2026 23:24:21 GMT  
		Size: 4.1 MB (4125413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6c589b3463b8e04d89e1627ed9442cca79f5d301117a77e8e425cff7eb8d826`  
		Last Modified: Tue, 19 May 2026 23:24:20 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:4ba0bdf097abd17ae046318d9c76996bf3e4ab2cfe23035b1145ee20844bc3d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138432129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7640d7a1a9851a160111f910f34fcdb4731c03d9288ba1f7bd3da327e8a01a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:27:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 May 2026 23:27:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 19 May 2026 23:27:18 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 19 May 2026 23:27:21 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 May 2026 23:27:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:27 GMT
ENV COUCHDB_VERSION=3.4.3
# Tue, 19 May 2026 23:27:27 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 19 May 2026 23:27:39 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 19 May 2026 23:27:39 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 19 May 2026 23:27:39 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 19 May 2026 23:27:39 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 19 May 2026 23:27:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 19 May 2026 23:27:39 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 May 2026 23:27:39 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 May 2026 23:27:39 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 19 May 2026 23:27:39 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e24e8c7fa768cc75e150b10e330b1a3a0dae912a24792f5390bb8e784d276e`  
		Last Modified: Tue, 19 May 2026 23:27:52 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9be4175f9e60c07473387372d8b1cc1d73a9ca8371b0f9e862c969768332df`  
		Last Modified: Tue, 19 May 2026 23:27:53 GMT  
		Size: 7.7 MB (7695136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60895f958d75b236cbd3de1a7743caa9e7e5541440dc66e3570b8aee43b8460d`  
		Last Modified: Tue, 19 May 2026 23:27:52 GMT  
		Size: 370.5 KB (370518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b727c0acdbaf659ee8d9719167b91704919f9b7261443de1634fb4134c896691`  
		Last Modified: Tue, 19 May 2026 23:27:52 GMT  
		Size: 76.5 KB (76494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7b37b356bbcf3e6ec862220aafb20c2d2cdf6f4271416dda5aa35b50063742`  
		Last Modified: Tue, 19 May 2026 23:27:53 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84790b386021daac75f5318352d72adb33c403620ccb6ef75a4145752d31ded`  
		Last Modified: Tue, 19 May 2026 23:28:00 GMT  
		Size: 102.2 MB (102169501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561a494cfc5b960fa1f0d22909ab94a0eb86faaccb0ffb511df42dbd2e6acbd6`  
		Last Modified: Tue, 19 May 2026 23:27:54 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc2e727f7d8d0ac6b84d7f32fd4a674ec3ec855702794c727fa4c5a31f7d277`  
		Last Modified: Tue, 19 May 2026 23:27:54 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffef35d93e31e4c7a411a7f382d68fdc09c0dce5e39d3e1b51baf52032914350`  
		Last Modified: Tue, 19 May 2026 23:27:55 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03290f47b7e4fdfd4a628ec8ce171c4c15aa514f56a489351cd2d819b019209a`  
		Last Modified: Tue, 19 May 2026 23:27:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:349654ff9e5346cee26e33294616538047ecda436e09a34b45efd236fee9060d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4157000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a7f538c545a1031ff02a6c87b5dd80dcf3110b8b99893f4a26fdb170d14bbe2`

```dockerfile
```

-	Layers:
	-	`sha256:e755df63d492cacf092f8cf8bca007aff36d9d3f56e410d75beb5e35c8a3d408`  
		Last Modified: Tue, 19 May 2026 23:27:52 GMT  
		Size: 4.1 MB (4125682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:babc27fcaf933d28f19d1aa7a1d216f997fb332cc79b527263d664b4f945e1e9`  
		Last Modified: Tue, 19 May 2026 23:27:52 GMT  
		Size: 31.3 KB (31318 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3` - linux; s390x

```console
$ docker pull couchdb@sha256:e781ab57f107167881e4db431f78e4f064e945de629ea29bf316660ba74c2960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135799283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062e4f15317b3254d5e2464e22455b60685314becd06ed6aec4158195e33b9ef`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:19:13 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 20 May 2026 00:19:13 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 20 May 2026 00:19:19 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:19:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 20 May 2026 00:19:22 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 20 May 2026 00:19:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:19:27 GMT
ENV COUCHDB_VERSION=3.4.3
# Wed, 20 May 2026 00:20:26 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 20 May 2026 00:20:42 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 20 May 2026 00:20:42 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 20 May 2026 00:20:42 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 20 May 2026 00:20:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 00:20:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 20 May 2026 00:20:42 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 20 May 2026 00:20:42 GMT
VOLUME [/opt/couchdb/data]
# Wed, 20 May 2026 00:20:42 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 20 May 2026 00:20:42 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2119d20228b0ee7dc34f2d8ae50ddc482133d4a46b75ef39cee53837e06a0b`  
		Last Modified: Wed, 20 May 2026 00:20:05 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a006620367a25e0aa2b2d85669f3382121b884eac2d944403ea899a9f28bc3a`  
		Last Modified: Wed, 20 May 2026 00:20:05 GMT  
		Size: 7.4 MB (7400088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a087ffd583427a623a7fbb6d5cd92146fa7fe562b3691275df4895f13a96e4`  
		Last Modified: Wed, 20 May 2026 00:20:05 GMT  
		Size: 372.2 KB (372152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d614b0a4ac50680b2c89e16a8817e441882e4f8a74c0efa6a724b927bfe5d32c`  
		Last Modified: Wed, 20 May 2026 00:20:05 GMT  
		Size: 76.5 KB (76539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89faf5f17de2b2b482ddd66c4d475c7b419239d8742d05dbd95eaaa6d8b6ebe`  
		Last Modified: Wed, 20 May 2026 00:21:02 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf982cfac72c8ce5675c24908face2e97a41c66c513fa73a7f98f32887929e0`  
		Last Modified: Wed, 20 May 2026 00:21:04 GMT  
		Size: 101.1 MB (101056473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737006e8dd12dc6a7920d4dbba81a2adcf894b9cfd9f08ab2d3d145a8cd45709`  
		Last Modified: Wed, 20 May 2026 00:21:02 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e2d485598b4cebfc1a39eebe635307861eaa609fb69ff124c4f154eda4967c`  
		Last Modified: Wed, 20 May 2026 00:21:02 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa737a67a9719364a9f105ceed1a7ec93c62cab245ba118dd0e4a833951aaee`  
		Last Modified: Wed, 20 May 2026 00:21:03 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bfdb266525bb6bb7c2ae862c3481a27a3daffcf35d31fdc308a35b0ca885e3`  
		Last Modified: Wed, 20 May 2026 00:21:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:d021b449200ed580cbbbe31a87fbc1819de9e7184a28bce4de7c1a2320239f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aca100fbcff26d70e9c7b924c2c1e92801717ad8da1b502e4ef4426921c585a`

```dockerfile
```

-	Layers:
	-	`sha256:4ba18fc91a85113f0265a18ad5ef30da02285ac1407b69d4061a53071b7a8dc0`  
		Last Modified: Wed, 20 May 2026 00:21:02 GMT  
		Size: 4.1 MB (4121609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70d0601c2dade617704cfd0f266a23794d0e8fb0d1aa9449d1b9417f1c595b8f`  
		Last Modified: Wed, 20 May 2026 00:21:02 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3-nouveau`

```console
$ docker pull couchdb@sha256:b65a46e8e77e3ceb3cc7422e50ba4a8cf13b1edb45865d9b9bd4f9afeead8498
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
$ docker pull couchdb@sha256:1b28577b7e1406b3097460f849c00ea0ad9e3d222e6f2468773509f43cb8a2dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.6 MB (156557052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f559137e9771bc303aa4ca977cbb1c8aab911b77e4d2b6e86c44e18fdcbd79`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 May 2026 23:23:40 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 19 May 2026 23:23:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:23:52 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:23:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 19 May 2026 23:23:54 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 May 2026 23:23:57 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:23:58 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 19 May 2026 23:24:02 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 19 May 2026 23:24:02 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 19 May 2026 23:24:02 GMT
VOLUME [/opt/nouveau/data]
# Tue, 19 May 2026 23:24:02 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 19 May 2026 23:24:02 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034254b8e01952c9c67ffb0d8201fea6ebaf4775ea8cd7ac91b509de3f1ed3cc`  
		Last Modified: Tue, 19 May 2026 23:24:18 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ab98cf14d02a29c4aa86f540fe6c9889bd595c7a5db98d9d74981914478c16`  
		Last Modified: Tue, 19 May 2026 23:24:19 GMT  
		Size: 7.9 MB (7884170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df177a882181db0ec0c60e4aaf9fd94a18c1e34280e5e15946ed2cd69c4904b0`  
		Last Modified: Tue, 19 May 2026 23:24:21 GMT  
		Size: 77.5 MB (77477910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2fcee25a09246222319e9d38fef98b79c45d8595a47e3e3d9e462078276f09`  
		Last Modified: Tue, 19 May 2026 23:24:18 GMT  
		Size: 424.1 KB (424149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3576391464b6e7080306d56d23930c9ea9ba29bd0f95e3be148fe155b12a1de7`  
		Last Modified: Tue, 19 May 2026 23:24:20 GMT  
		Size: 99.6 KB (99563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babd490be78878864bc284dcf28a23e501af9f9260196bb80f61429b8d461e1e`  
		Last Modified: Tue, 19 May 2026 23:24:20 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59817ab8b38f3c70e51a30216d2038aa6eba6ff190c71bdce4d7fcfb976ebd08`  
		Last Modified: Tue, 19 May 2026 23:24:21 GMT  
		Size: 42.4 MB (42435835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99aee7e3b66f991598df233f16dd0b28b833e965fbdb7e02a4370c18806a70b7`  
		Last Modified: Tue, 19 May 2026 23:24:21 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:626d48c311ffef0cf077ed4d2e06c70f4bb5dda0863d6623f6b580dae5330064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc25db8e2d359542585ef547dd522d304d4bddf3581e9bd5e43eec9c2255092`

```dockerfile
```

-	Layers:
	-	`sha256:bdac17e5c586326819a4977371c126aca1b183b1a4e823a9bfafd8ee4559a90b`  
		Last Modified: Tue, 19 May 2026 23:24:19 GMT  
		Size: 3.7 MB (3658653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3454d1187cebbe56eb5cef5de8e167ba87117fa0d0547c1d40e8e9152059bf96`  
		Last Modified: Tue, 19 May 2026 23:24:18 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:cefdb1385ab4a451d2aea210ccc3ea8760acaa52067780e3a4836be3e39da549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155435730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b36ceedfbd6190ca9b093c68d82626c05d620f7a694f0efc30c37d909654e6cd`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:27:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 May 2026 23:27:19 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 19 May 2026 23:27:25 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 19 May 2026 23:27:34 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 May 2026 23:27:38 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:38 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 19 May 2026 23:27:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 19 May 2026 23:27:43 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 19 May 2026 23:27:43 GMT
VOLUME [/opt/nouveau/data]
# Tue, 19 May 2026 23:27:43 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 19 May 2026 23:27:43 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b431e0800be10532b8cdccd281d397a606f541a408e919fe06261c077301a006`  
		Last Modified: Tue, 19 May 2026 23:27:57 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42477eae5cec1dedc000ef75f969c8a87f8769385122615b007e689d818716dc`  
		Last Modified: Tue, 19 May 2026 23:27:58 GMT  
		Size: 7.7 MB (7695083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a0fe90886376d1d4d332acfec00cd36ca36b57e90eaf4785f5aafbc63ae938`  
		Last Modified: Tue, 19 May 2026 23:28:00 GMT  
		Size: 76.8 MB (76793468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c465194c14ac1c736796410733d7a5dd83b39c68678383ed896651efea8df5d5`  
		Last Modified: Tue, 19 May 2026 23:27:58 GMT  
		Size: 392.8 KB (392782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27d9b7f356e47858f4d282ed5f6d14748a682626af2ec2c978da028b1f07d89f`  
		Last Modified: Tue, 19 May 2026 23:27:59 GMT  
		Size: 99.5 KB (99507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7288fcfdfcbdabf602e1d2b92be07ebd2731eb28a2c85ef2449a25f9ff79b92`  
		Last Modified: Tue, 19 May 2026 23:27:59 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47eb77540f225caf0dfd731cd23c6d99c4eacab7fcc32501206406f3f058a84e`  
		Last Modified: Tue, 19 May 2026 23:28:00 GMT  
		Size: 42.3 MB (42337966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c05e22b278e6181c2299b996a4312ce0d6f6f193cc6d490ad06bacf56bddb4e`  
		Last Modified: Tue, 19 May 2026 23:28:00 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:b291a7b3423e66d516c470f2bd971e08d78f6da85685811ec75a2e44afeb9b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aacc0519a174443d14e7e47f321ddc3d964ee5c2a44354f8776f70174215d93`

```dockerfile
```

-	Layers:
	-	`sha256:1f9e0d0e366e8d52579f2d7bbea0d58216660c96b6ed8aef682d7e2dd8dd6635`  
		Last Modified: Tue, 19 May 2026 23:27:58 GMT  
		Size: 3.7 MB (3657321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2e306c7e7342dc8957898406f6555b25411a7f849b9aa21a7fd768e2f9b3c5c`  
		Last Modified: Tue, 19 May 2026 23:27:57 GMT  
		Size: 24.4 KB (24384 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:4dc2a0634528573ef1a7cf7f418b30902b021c6f36a8f97ab045b809a25cdbcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.2 MB (150172945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9bbd6c813f57e84313da6c907f21e34ca378e73a80a6881e14f03e124f96546`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:19:26 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 20 May 2026 00:19:26 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 20 May 2026 00:19:33 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:19:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:19:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 20 May 2026 00:19:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 20 May 2026 00:19:50 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:19:50 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 20 May 2026 00:20:48 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 20 May 2026 00:20:48 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 20 May 2026 00:20:48 GMT
VOLUME [/opt/nouveau/data]
# Wed, 20 May 2026 00:20:48 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 20 May 2026 00:20:48 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735715cce2082c3ee3f9a3e1340e641fd3c8a4c27a986dfa1e0711d23ab1bfd3`  
		Last Modified: Wed, 20 May 2026 00:20:19 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d408f2f91f087b84b8fc0b5eaab3a385e9c71c6d1aea5cdd41add6b52a42875`  
		Last Modified: Wed, 20 May 2026 00:20:20 GMT  
		Size: 7.4 MB (7400058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9862fef3db5700ef619b2c3c7787c171007e7038deabe8151310df8531e354c4`  
		Last Modified: Wed, 20 May 2026 00:20:20 GMT  
		Size: 73.2 MB (73225383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa09fc31e5567156b4208ae4d6e44d3f8c7fcc9372b1f65223c892703e7b785`  
		Last Modified: Wed, 20 May 2026 00:20:19 GMT  
		Size: 394.5 KB (394501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93eb29090836c1a783acc896684e8094b507792c57f4e34f997b56fbbe53038e`  
		Last Modified: Wed, 20 May 2026 00:20:20 GMT  
		Size: 99.7 KB (99671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6bf9c655d2ba99361dd631c89376c408f4241337194d618f695647f46b1893`  
		Last Modified: Wed, 20 May 2026 00:20:20 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70b8ea5924d1d6ddeed842229d696c5d7339bd591d0a4e18332a1f853a14128`  
		Last Modified: Wed, 20 May 2026 00:21:04 GMT  
		Size: 42.2 MB (42162858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa511f6c6cad159de580bb827928f4c832dd41ea35ceadcdaa771c67a8626b38`  
		Last Modified: Wed, 20 May 2026 00:21:03 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:ab6d822426e364949911ae45953e5655df9dd41fd3fe427a2c6ffcadb3c58b1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e185b56f0a0f457d0e0345bf17a86dd144c6c0429136757651eaf6c322a5b998`

```dockerfile
```

-	Layers:
	-	`sha256:f350fdb2b2edbfa085859a68071502e2d0eda2f585d913dea3203739704f57fe`  
		Last Modified: Wed, 20 May 2026 00:21:03 GMT  
		Size: 3.6 MB (3649186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16c57fb6fb6ffd2ff26271b6130b1d5df9c6e6c7cdf5779f88c271f91018c041`  
		Last Modified: Wed, 20 May 2026 00:21:03 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5`

```console
$ docker pull couchdb@sha256:ccea1e8035bf7afd68336e24056a1ca9c1c46d7abe42da686322c0ac7218e5c2
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
$ docker pull couchdb@sha256:09b52d7ef639c76be25a7e09cfa96f0b5c43716341432af6b9b69296c25d947c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142058343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a90b450fc37c41f09cfe760f9e5c41b41a106f5c17861a66a85623393c84a1e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:30 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 May 2026 23:23:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 19 May 2026 23:23:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:23:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 19 May 2026 23:23:38 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 May 2026 23:23:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:23:43 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 19 May 2026 23:23:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 19 May 2026 23:23:57 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 19 May 2026 23:23:57 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 19 May 2026 23:23:57 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 19 May 2026 23:23:57 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 19 May 2026 23:23:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 19 May 2026 23:23:57 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 May 2026 23:23:57 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 May 2026 23:23:57 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 19 May 2026 23:23:57 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d87ffdf697e28d18b4eeb0a8d1d768b895464e0ae7d26f400499188dab4dcf`  
		Last Modified: Tue, 19 May 2026 23:24:10 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d4d2c2632d51f0fee8fb039f27beaecf7928c5c3019b6e371705051245f4e0`  
		Last Modified: Tue, 19 May 2026 23:24:10 GMT  
		Size: 7.9 MB (7884263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b425c7b9d89cf53bd5e690f47d266e2fa1f976ed03c33b5d21208783dfb79e`  
		Last Modified: Tue, 19 May 2026 23:24:10 GMT  
		Size: 401.8 KB (401768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f19c3418d8748695c75c59323373440311c3b75d373a279b5d6f993e0564e03`  
		Last Modified: Tue, 19 May 2026 23:24:10 GMT  
		Size: 76.5 KB (76511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73154ca85a92b6433c5a44e7ffe0f337949da39b5a572708d9d13ba91d546d4`  
		Last Modified: Tue, 19 May 2026 23:24:11 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abc75c4e20b40d156aa48cbcf77a4d397957680a7f96f32d8c1b437fbb7bbd3`  
		Last Modified: Tue, 19 May 2026 23:24:14 GMT  
		Size: 105.5 MB (105456830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899a91b0daaba92f5c2bae2f5fcd951b47148f9eb4e2d9f765f52db961bada33`  
		Last Modified: Tue, 19 May 2026 23:24:12 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc121e2a64ebd3bba759a5b6c1dbf4ee3ec6264cda384ae1174863bceb551d6`  
		Last Modified: Tue, 19 May 2026 23:24:12 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a9e26ff2802324e688ac2dd228284530dd8d636f6d5bcc7e3f654266fd89ee`  
		Last Modified: Tue, 19 May 2026 23:24:12 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f024794f059b1f69b3457a0c98454a9713c9f7757c5e8dc68a2c7b092a02ae`  
		Last Modified: Tue, 19 May 2026 23:24:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:1f38cfbf48b42d81459d804c11a774eb18eea24cda47a2f6b72548261ac1480f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadc2c0087a0b40fe55ea12021314db6ecaf24467fd2fbb0ac38bc5c3c82c9fc`

```dockerfile
```

-	Layers:
	-	`sha256:5970fc12dcc23fbf1c7e1fd5beb8b38148391163230f8df116acfbfa92e81ce9`  
		Last Modified: Tue, 19 May 2026 23:24:10 GMT  
		Size: 4.2 MB (4184439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c3a0078900b2a20ee9590364c77bdacf67a45a1b6459ec64edf2843739594ab`  
		Last Modified: Tue, 19 May 2026 23:24:10 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:b7176956426645f7ab91cfb0673d6fa791c548e69ecb0bdcd31c2322b82459b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141420899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a29d99a11349876560d65720cb2500f758d6c268b4ce83dd003467318e9af9ff`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:27:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 May 2026 23:27:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 19 May 2026 23:27:11 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:14 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 19 May 2026 23:27:14 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 May 2026 23:27:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:19 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 19 May 2026 23:27:19 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 19 May 2026 23:27:33 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 19 May 2026 23:27:33 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 19 May 2026 23:27:33 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 19 May 2026 23:27:33 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 19 May 2026 23:27:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 19 May 2026 23:27:33 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 May 2026 23:27:33 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 May 2026 23:27:33 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 19 May 2026 23:27:33 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207d5e816f1b653cf6cf1dfaf88b2e833edabd255ed64a2ceb4dfb0bb06d3d1d`  
		Last Modified: Tue, 19 May 2026 23:27:46 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee01d5686c343d9d942d5763de8fec23ce28536abbe0edeb563a46123a3e23f3`  
		Last Modified: Tue, 19 May 2026 23:27:47 GMT  
		Size: 7.7 MB (7695155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aead94788b9f92728da249312943ffa094e410bb26f31cb625f5649f6386c87`  
		Last Modified: Tue, 19 May 2026 23:27:46 GMT  
		Size: 370.5 KB (370533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36032904add5ab79f200e99bdce3a29bf50cff2877755d309598f42f64c6c3e`  
		Last Modified: Tue, 19 May 2026 23:27:47 GMT  
		Size: 76.5 KB (76511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5226977736149250abf09625c32d88dd8cc60a048b76a2d0be25f499504c475c`  
		Last Modified: Tue, 19 May 2026 23:27:48 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb6489dfc879dc5a78a4c35fc051c4c879cd2f8be64af5f98a914c859a713f7`  
		Last Modified: Tue, 19 May 2026 23:27:50 GMT  
		Size: 105.2 MB (105158221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9b98d1676bb46f0e83d27fd5c1af5243d83bb39bb53dd97428b3a647dbd673`  
		Last Modified: Tue, 19 May 2026 23:27:48 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4737a0ed9c20e76eb585e449073111217256029e1e87802fb22386fd6192f8`  
		Last Modified: Tue, 19 May 2026 23:27:48 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59688f55bbd7f0cdb249f36b1677326ae7d20d01cc257083b45ad929057b4d6`  
		Last Modified: Tue, 19 May 2026 23:27:49 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c04a6c46e262d21d685073fb9837cc0ee3a8de9d98f978189ea05bf62bac681`  
		Last Modified: Tue, 19 May 2026 23:27:49 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:c4947fd32d28629c9cadc11c3b0b72cff06449499e87ebf82495f38517695a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e70de05fdeea721dfdb1a15f309c4d6b1771ddf910239dc35ef59e7596b4db`

```dockerfile
```

-	Layers:
	-	`sha256:8e08a7d31bd63f26291598eedf87ae610357cbaf462e08316ce235a612e3656f`  
		Last Modified: Tue, 19 May 2026 23:27:47 GMT  
		Size: 4.2 MB (4184732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1878dfd62c3c800a27e5ab10bfc19849cbbd5816c82a3ad6735ea1e12233099`  
		Last Modified: Tue, 19 May 2026 23:27:47 GMT  
		Size: 31.9 KB (31932 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5` - linux; s390x

```console
$ docker pull couchdb@sha256:76de6eff1c868ce94a63d2ddd5b5fd721b0055d8f6733ed5f09d7ff6232bf2f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138771252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f44a4c43a005d699aa1531f111caf142341bcefd98b1978c25a8746f544cad77`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:19:13 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 20 May 2026 00:19:13 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 20 May 2026 00:19:19 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:19:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 20 May 2026 00:19:22 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 20 May 2026 00:19:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:19:27 GMT
ENV COUCHDB_VERSION=3.5.1
# Wed, 20 May 2026 00:19:27 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 20 May 2026 00:19:44 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 20 May 2026 00:19:44 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 20 May 2026 00:19:44 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 20 May 2026 00:19:44 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 00:19:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 20 May 2026 00:19:44 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 20 May 2026 00:19:44 GMT
VOLUME [/opt/couchdb/data]
# Wed, 20 May 2026 00:19:44 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 20 May 2026 00:19:44 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2119d20228b0ee7dc34f2d8ae50ddc482133d4a46b75ef39cee53837e06a0b`  
		Last Modified: Wed, 20 May 2026 00:20:05 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a006620367a25e0aa2b2d85669f3382121b884eac2d944403ea899a9f28bc3a`  
		Last Modified: Wed, 20 May 2026 00:20:05 GMT  
		Size: 7.4 MB (7400088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a087ffd583427a623a7fbb6d5cd92146fa7fe562b3691275df4895f13a96e4`  
		Last Modified: Wed, 20 May 2026 00:20:05 GMT  
		Size: 372.2 KB (372152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d614b0a4ac50680b2c89e16a8817e441882e4f8a74c0efa6a724b927bfe5d32c`  
		Last Modified: Wed, 20 May 2026 00:20:05 GMT  
		Size: 76.5 KB (76539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a870d76e1f3afb6201a63608520cb8174f7d1672346eb3332cea2e37f4f1cd9e`  
		Last Modified: Wed, 20 May 2026 00:20:06 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5adb01efb8694d80e39bf12de91b861383f6a88f7add83424b5800e99b96d67`  
		Last Modified: Wed, 20 May 2026 00:20:08 GMT  
		Size: 104.0 MB (104028456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02b4b27d6d6743e59c472d833f03c8e80f4f507c5e1af57920390734a0cc4da`  
		Last Modified: Wed, 20 May 2026 00:20:06 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd01387718dcd18b409353134fe1a48b7fe039050318bae2d83f749251e5b5a`  
		Last Modified: Wed, 20 May 2026 00:20:06 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8be35f18dfda1fa008590a40a550ebca59f6feed5a0751df486655b973a0ad`  
		Last Modified: Wed, 20 May 2026 00:20:07 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad1c999649df933c865b874c165aa1b98893f1713eca21e8950faf01c71c761`  
		Last Modified: Wed, 20 May 2026 00:20:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:c7b89f39f6c9ed1b5219d4c80c4784e6b9e01549aa3d7281d999206e67c3271f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4072facf62633c168c635a226652d1e5441034a1ccd5b7c7e651f24e590b338`

```dockerfile
```

-	Layers:
	-	`sha256:ca3e264ce2fe47ba09799d31e60d681d285326875424c22ac69285baca76978b`  
		Last Modified: Wed, 20 May 2026 00:20:05 GMT  
		Size: 4.2 MB (4180635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7ceacf997acb8d668e341d6b8b2c3661a2bed3e4152acf1c0cb8c3fdbc63069`  
		Last Modified: Wed, 20 May 2026 00:20:05 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5-nouveau`

```console
$ docker pull couchdb@sha256:1ac782d8867be6b364c566f43ed5302d4b91c7e189cc26385ff6936fa352c557
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
$ docker pull couchdb@sha256:a53952e2264a34693a7fcbd17adf5ffaa3d6f27763251ad21644b2aefcfd2b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.6 MB (156557623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071f487d402e6cb43464653c9e1a195e772104291531869a5fe8f948995d6c08`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:37 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 May 2026 23:23:37 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 19 May 2026 23:23:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:23:52 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:23:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 19 May 2026 23:23:54 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 May 2026 23:23:59 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:23:59 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 19 May 2026 23:24:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 19 May 2026 23:24:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 19 May 2026 23:24:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 19 May 2026 23:24:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 19 May 2026 23:24:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f55187b4934e056c680d6e91549329607ce47ec51776501ac73d8bc1bba9176`  
		Last Modified: Tue, 19 May 2026 23:24:20 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd0bc89c040283119b651af145e97ef098cc1b2b054e3e7bf7af6dc8adf211a6`  
		Last Modified: Tue, 19 May 2026 23:24:20 GMT  
		Size: 7.9 MB (7884206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44649a9110a9a5ccd1737df67a46e606d02b61085ae41dfe63409416c4ee8ec`  
		Last Modified: Tue, 19 May 2026 23:24:22 GMT  
		Size: 77.5 MB (77477908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae71b0eed42b7d26bdb16759f9bfd007eabd413cac68409c5613c165a64dd6f`  
		Last Modified: Tue, 19 May 2026 23:24:20 GMT  
		Size: 424.2 KB (424171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303155b8a67b8b99800b9a2204efb2d5f2aefb9cc20a9486117646b1b72d644b`  
		Last Modified: Tue, 19 May 2026 23:24:21 GMT  
		Size: 99.6 KB (99627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76daa6193200c830022f9be24af04803cf3c8dad18832c8acf36765fa10c224`  
		Last Modified: Tue, 19 May 2026 23:24:21 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febec42ec387c3429c25295b90efc0b4fce77a7f36bbee9e5f1d1b5af995b186`  
		Last Modified: Tue, 19 May 2026 23:24:22 GMT  
		Size: 42.4 MB (42436288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d598b8820fe2b2b91338ba428d09274914f7d04d3d357ee0942258ebe38c65`  
		Last Modified: Tue, 19 May 2026 23:24:22 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:94c7834a10dd38e96a47d2b062a70093c61257a2223b3c5c558f84c360e0bcee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3683480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a58f59868ef764a8218f59ec8e51f8148a561b74654e80458a6cc74b6584a318`

```dockerfile
```

-	Layers:
	-	`sha256:bb1647008b09a4338f745df17b41aa347576085b74c7f10332f96afc36d34444`  
		Last Modified: Tue, 19 May 2026 23:24:20 GMT  
		Size: 3.7 MB (3658959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:174075f2d213288f23092903ba95fd10d4b8356b833edd7c83c0987b0e32c5ef`  
		Last Modified: Tue, 19 May 2026 23:24:19 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:9a59349312a5702bb7bff3346726c6d7e1c37df0e5723f8dbd041bec8e5cd9f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155436748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aca94e84d6e887330b70a1a271457b445394a33d7ca0c9ae07a22eb400c8a76`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:27:09 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 May 2026 23:27:09 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 19 May 2026 23:27:15 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:23 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 19 May 2026 23:27:25 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 May 2026 23:27:30 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:30 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 19 May 2026 23:27:36 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 19 May 2026 23:27:36 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 19 May 2026 23:27:36 GMT
VOLUME [/opt/nouveau/data]
# Tue, 19 May 2026 23:27:36 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 19 May 2026 23:27:36 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0660a5ba91ed2ceb43e5ba98840c9a45b676fc87e8d521ff727eb0d7a1389f13`  
		Last Modified: Tue, 19 May 2026 23:27:51 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40157edc7727629f8fe52bb2d849f861475f0bc518d76d6a004a67da5a605fb3`  
		Last Modified: Tue, 19 May 2026 23:27:51 GMT  
		Size: 7.7 MB (7695099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6efcd070ffca23467b828b1bfd13af99d03f56a3abedf45b27059da3c9fae7`  
		Last Modified: Tue, 19 May 2026 23:27:55 GMT  
		Size: 76.8 MB (76793447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8467613a6e749c52d0ec773927373f9cb960f95fd10fc2dbee3b762f4bee39a2`  
		Last Modified: Tue, 19 May 2026 23:27:51 GMT  
		Size: 392.8 KB (392776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9d3c250fd125a835a2adff1a24d315e2da082db0eec62940fa83779419335b`  
		Last Modified: Tue, 19 May 2026 23:27:52 GMT  
		Size: 99.5 KB (99523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54db9e883bb069403d111165a75ab234a2524c59667021def0c2016daf2647e`  
		Last Modified: Tue, 19 May 2026 23:27:52 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f298e4411d38607887f8a92d3f51fb1fc315bf47f696318f2e4311f3db44fa8`  
		Last Modified: Tue, 19 May 2026 23:27:55 GMT  
		Size: 42.3 MB (42338980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d05cdc4e9cb7f6ac6d18eb69732dbf99e6eec99e64a83b5751d5db66599eeb`  
		Last Modified: Tue, 19 May 2026 23:27:54 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:94aca52e7d9afe99912951c1431c803d81a49e915b30d263fb198d6b5399850a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:899adac63c9796e2bf48ba07185e219ff1546bc77e1ec817d07c5011ae76041a`

```dockerfile
```

-	Layers:
	-	`sha256:d887223f03033388ec110a35f1585bb3fb6c4c574684c0fe5e9ff91fc3a19ecc`  
		Last Modified: Tue, 19 May 2026 23:27:51 GMT  
		Size: 3.7 MB (3657639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49422572d47602cc606a6c5d156205a36ed7e4ea6e0f0f0b29c33a67752677c9`  
		Last Modified: Tue, 19 May 2026 23:27:51 GMT  
		Size: 24.7 KB (24703 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:d1330882e3531b96283ce80dbed9f713adb21b7ba633e089ef83921669d8f23f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.2 MB (150174644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e732564359f80d5ae39b646d3271a461f174828f6e2e4f926f8c5ff3d8daf86e`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:19:26 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 20 May 2026 00:19:26 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 20 May 2026 00:19:33 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:19:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:19:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 20 May 2026 00:19:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 20 May 2026 00:19:50 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:19:50 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 20 May 2026 00:19:57 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 20 May 2026 00:19:57 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 20 May 2026 00:19:57 GMT
VOLUME [/opt/nouveau/data]
# Wed, 20 May 2026 00:19:57 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 20 May 2026 00:19:57 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735715cce2082c3ee3f9a3e1340e641fd3c8a4c27a986dfa1e0711d23ab1bfd3`  
		Last Modified: Wed, 20 May 2026 00:20:19 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d408f2f91f087b84b8fc0b5eaab3a385e9c71c6d1aea5cdd41add6b52a42875`  
		Last Modified: Wed, 20 May 2026 00:20:20 GMT  
		Size: 7.4 MB (7400058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9862fef3db5700ef619b2c3c7787c171007e7038deabe8151310df8531e354c4`  
		Last Modified: Wed, 20 May 2026 00:20:20 GMT  
		Size: 73.2 MB (73225383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa09fc31e5567156b4208ae4d6e44d3f8c7fcc9372b1f65223c892703e7b785`  
		Last Modified: Wed, 20 May 2026 00:20:19 GMT  
		Size: 394.5 KB (394501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93eb29090836c1a783acc896684e8094b507792c57f4e34f997b56fbbe53038e`  
		Last Modified: Wed, 20 May 2026 00:20:20 GMT  
		Size: 99.7 KB (99671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6bf9c655d2ba99361dd631c89376c408f4241337194d618f695647f46b1893`  
		Last Modified: Wed, 20 May 2026 00:20:20 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1626c6f29ea03bd3f02121e49788d0a1598081af520493c082775a80212c2a0e`  
		Last Modified: Wed, 20 May 2026 00:20:22 GMT  
		Size: 42.2 MB (42164559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb3708c7856914821db2d45a870a7b4f276ee63a1504d8a0351be2a7ad0f0df`  
		Last Modified: Wed, 20 May 2026 00:20:21 GMT  
		Size: 415.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:74bf10806c26372b203e56e1b669533da4bcf86947e45c64c0495cdf0891b8fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3674013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a63f7ef1e02ba24716d614c580430054a0f24e9fce3a171f078aed465c00f31c`

```dockerfile
```

-	Layers:
	-	`sha256:c88ba0d2fa26953de302b0ce999917e535786ca1ff751c6d58afc4a1e8a50c15`  
		Last Modified: Wed, 20 May 2026 00:20:19 GMT  
		Size: 3.6 MB (3649492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9efadf28d263fc1c7ab013f81ed2a347b116742fb90a18583835275affb68c35`  
		Last Modified: Wed, 20 May 2026 00:20:19 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.2`

**does not exist** (yet?)

## `couchdb:3.5.2-nouveau`

**does not exist** (yet?)

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:ccea1e8035bf7afd68336e24056a1ca9c1c46d7abe42da686322c0ac7218e5c2
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
$ docker pull couchdb@sha256:09b52d7ef639c76be25a7e09cfa96f0b5c43716341432af6b9b69296c25d947c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142058343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a90b450fc37c41f09cfe760f9e5c41b41a106f5c17861a66a85623393c84a1e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:30 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 May 2026 23:23:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 19 May 2026 23:23:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:23:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 19 May 2026 23:23:38 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 May 2026 23:23:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:23:43 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 19 May 2026 23:23:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 19 May 2026 23:23:57 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 19 May 2026 23:23:57 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 19 May 2026 23:23:57 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 19 May 2026 23:23:57 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 19 May 2026 23:23:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 19 May 2026 23:23:57 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 May 2026 23:23:57 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 May 2026 23:23:57 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 19 May 2026 23:23:57 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d87ffdf697e28d18b4eeb0a8d1d768b895464e0ae7d26f400499188dab4dcf`  
		Last Modified: Tue, 19 May 2026 23:24:10 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d4d2c2632d51f0fee8fb039f27beaecf7928c5c3019b6e371705051245f4e0`  
		Last Modified: Tue, 19 May 2026 23:24:10 GMT  
		Size: 7.9 MB (7884263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b425c7b9d89cf53bd5e690f47d266e2fa1f976ed03c33b5d21208783dfb79e`  
		Last Modified: Tue, 19 May 2026 23:24:10 GMT  
		Size: 401.8 KB (401768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f19c3418d8748695c75c59323373440311c3b75d373a279b5d6f993e0564e03`  
		Last Modified: Tue, 19 May 2026 23:24:10 GMT  
		Size: 76.5 KB (76511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73154ca85a92b6433c5a44e7ffe0f337949da39b5a572708d9d13ba91d546d4`  
		Last Modified: Tue, 19 May 2026 23:24:11 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abc75c4e20b40d156aa48cbcf77a4d397957680a7f96f32d8c1b437fbb7bbd3`  
		Last Modified: Tue, 19 May 2026 23:24:14 GMT  
		Size: 105.5 MB (105456830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899a91b0daaba92f5c2bae2f5fcd951b47148f9eb4e2d9f765f52db961bada33`  
		Last Modified: Tue, 19 May 2026 23:24:12 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc121e2a64ebd3bba759a5b6c1dbf4ee3ec6264cda384ae1174863bceb551d6`  
		Last Modified: Tue, 19 May 2026 23:24:12 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a9e26ff2802324e688ac2dd228284530dd8d636f6d5bcc7e3f654266fd89ee`  
		Last Modified: Tue, 19 May 2026 23:24:12 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f024794f059b1f69b3457a0c98454a9713c9f7757c5e8dc68a2c7b092a02ae`  
		Last Modified: Tue, 19 May 2026 23:24:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:1f38cfbf48b42d81459d804c11a774eb18eea24cda47a2f6b72548261ac1480f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadc2c0087a0b40fe55ea12021314db6ecaf24467fd2fbb0ac38bc5c3c82c9fc`

```dockerfile
```

-	Layers:
	-	`sha256:5970fc12dcc23fbf1c7e1fd5beb8b38148391163230f8df116acfbfa92e81ce9`  
		Last Modified: Tue, 19 May 2026 23:24:10 GMT  
		Size: 4.2 MB (4184439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c3a0078900b2a20ee9590364c77bdacf67a45a1b6459ec64edf2843739594ab`  
		Last Modified: Tue, 19 May 2026 23:24:10 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:b7176956426645f7ab91cfb0673d6fa791c548e69ecb0bdcd31c2322b82459b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141420899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a29d99a11349876560d65720cb2500f758d6c268b4ce83dd003467318e9af9ff`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:27:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 May 2026 23:27:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 19 May 2026 23:27:11 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:14 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 19 May 2026 23:27:14 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 May 2026 23:27:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:19 GMT
ENV COUCHDB_VERSION=3.5.1
# Tue, 19 May 2026 23:27:19 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 19 May 2026 23:27:33 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 19 May 2026 23:27:33 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 19 May 2026 23:27:33 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 19 May 2026 23:27:33 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 19 May 2026 23:27:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 19 May 2026 23:27:33 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 May 2026 23:27:33 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 May 2026 23:27:33 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 19 May 2026 23:27:33 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207d5e816f1b653cf6cf1dfaf88b2e833edabd255ed64a2ceb4dfb0bb06d3d1d`  
		Last Modified: Tue, 19 May 2026 23:27:46 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee01d5686c343d9d942d5763de8fec23ce28536abbe0edeb563a46123a3e23f3`  
		Last Modified: Tue, 19 May 2026 23:27:47 GMT  
		Size: 7.7 MB (7695155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aead94788b9f92728da249312943ffa094e410bb26f31cb625f5649f6386c87`  
		Last Modified: Tue, 19 May 2026 23:27:46 GMT  
		Size: 370.5 KB (370533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36032904add5ab79f200e99bdce3a29bf50cff2877755d309598f42f64c6c3e`  
		Last Modified: Tue, 19 May 2026 23:27:47 GMT  
		Size: 76.5 KB (76511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5226977736149250abf09625c32d88dd8cc60a048b76a2d0be25f499504c475c`  
		Last Modified: Tue, 19 May 2026 23:27:48 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb6489dfc879dc5a78a4c35fc051c4c879cd2f8be64af5f98a914c859a713f7`  
		Last Modified: Tue, 19 May 2026 23:27:50 GMT  
		Size: 105.2 MB (105158221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9b98d1676bb46f0e83d27fd5c1af5243d83bb39bb53dd97428b3a647dbd673`  
		Last Modified: Tue, 19 May 2026 23:27:48 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4737a0ed9c20e76eb585e449073111217256029e1e87802fb22386fd6192f8`  
		Last Modified: Tue, 19 May 2026 23:27:48 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59688f55bbd7f0cdb249f36b1677326ae7d20d01cc257083b45ad929057b4d6`  
		Last Modified: Tue, 19 May 2026 23:27:49 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c04a6c46e262d21d685073fb9837cc0ee3a8de9d98f978189ea05bf62bac681`  
		Last Modified: Tue, 19 May 2026 23:27:49 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:c4947fd32d28629c9cadc11c3b0b72cff06449499e87ebf82495f38517695a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e70de05fdeea721dfdb1a15f309c4d6b1771ddf910239dc35ef59e7596b4db`

```dockerfile
```

-	Layers:
	-	`sha256:8e08a7d31bd63f26291598eedf87ae610357cbaf462e08316ce235a612e3656f`  
		Last Modified: Tue, 19 May 2026 23:27:47 GMT  
		Size: 4.2 MB (4184732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1878dfd62c3c800a27e5ab10bfc19849cbbd5816c82a3ad6735ea1e12233099`  
		Last Modified: Tue, 19 May 2026 23:27:47 GMT  
		Size: 31.9 KB (31932 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:76de6eff1c868ce94a63d2ddd5b5fd721b0055d8f6733ed5f09d7ff6232bf2f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138771252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f44a4c43a005d699aa1531f111caf142341bcefd98b1978c25a8746f544cad77`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:19:13 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 20 May 2026 00:19:13 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 20 May 2026 00:19:19 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:19:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 20 May 2026 00:19:22 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 20 May 2026 00:19:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:19:27 GMT
ENV COUCHDB_VERSION=3.5.1
# Wed, 20 May 2026 00:19:27 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 20 May 2026 00:19:44 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 20 May 2026 00:19:44 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 20 May 2026 00:19:44 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 20 May 2026 00:19:44 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 20 May 2026 00:19:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 20 May 2026 00:19:44 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 20 May 2026 00:19:44 GMT
VOLUME [/opt/couchdb/data]
# Wed, 20 May 2026 00:19:44 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 20 May 2026 00:19:44 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2119d20228b0ee7dc34f2d8ae50ddc482133d4a46b75ef39cee53837e06a0b`  
		Last Modified: Wed, 20 May 2026 00:20:05 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a006620367a25e0aa2b2d85669f3382121b884eac2d944403ea899a9f28bc3a`  
		Last Modified: Wed, 20 May 2026 00:20:05 GMT  
		Size: 7.4 MB (7400088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a087ffd583427a623a7fbb6d5cd92146fa7fe562b3691275df4895f13a96e4`  
		Last Modified: Wed, 20 May 2026 00:20:05 GMT  
		Size: 372.2 KB (372152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d614b0a4ac50680b2c89e16a8817e441882e4f8a74c0efa6a724b927bfe5d32c`  
		Last Modified: Wed, 20 May 2026 00:20:05 GMT  
		Size: 76.5 KB (76539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a870d76e1f3afb6201a63608520cb8174f7d1672346eb3332cea2e37f4f1cd9e`  
		Last Modified: Wed, 20 May 2026 00:20:06 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5adb01efb8694d80e39bf12de91b861383f6a88f7add83424b5800e99b96d67`  
		Last Modified: Wed, 20 May 2026 00:20:08 GMT  
		Size: 104.0 MB (104028456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02b4b27d6d6743e59c472d833f03c8e80f4f507c5e1af57920390734a0cc4da`  
		Last Modified: Wed, 20 May 2026 00:20:06 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd01387718dcd18b409353134fe1a48b7fe039050318bae2d83f749251e5b5a`  
		Last Modified: Wed, 20 May 2026 00:20:06 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8be35f18dfda1fa008590a40a550ebca59f6feed5a0751df486655b973a0ad`  
		Last Modified: Wed, 20 May 2026 00:20:07 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad1c999649df933c865b874c165aa1b98893f1713eca21e8950faf01c71c761`  
		Last Modified: Wed, 20 May 2026 00:20:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:c7b89f39f6c9ed1b5219d4c80c4784e6b9e01549aa3d7281d999206e67c3271f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4072facf62633c168c635a226652d1e5441034a1ccd5b7c7e651f24e590b338`

```dockerfile
```

-	Layers:
	-	`sha256:ca3e264ce2fe47ba09799d31e60d681d285326875424c22ac69285baca76978b`  
		Last Modified: Wed, 20 May 2026 00:20:05 GMT  
		Size: 4.2 MB (4180635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7ceacf997acb8d668e341d6b8b2c3661a2bed3e4152acf1c0cb8c3fdbc63069`  
		Last Modified: Wed, 20 May 2026 00:20:05 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json
