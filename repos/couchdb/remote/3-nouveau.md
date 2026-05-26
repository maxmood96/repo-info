## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:5fea57e73aecc512b829b25e09deb2f8ae79b8e0d203bf8d3912ed57962ca2df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:b023387918d50d3845f8473ff48db48b4f1f2482924ad3ab2d63bb03ea9be41c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150895583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4081591f6f0c7ba97c750131f877958e0833f16e21178d6d040c01069ffc46b1`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 19:12:21 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 26 May 2026 19:12:21 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 26 May 2026 19:12:29 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:12:35 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-21-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:12:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 26 May 2026 19:12:38 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 26 May 2026 19:12:45 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:12:45 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ trixie main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 26 May 2026 19:12:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.2~trixie;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 26 May 2026 19:12:52 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 26 May 2026 19:12:52 GMT
VOLUME [/opt/nouveau/data]
# Tue, 26 May 2026 19:12:52 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 26 May 2026 19:12:52 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adfe4274313c392eaae20352b57638571532c448f9d84f803895a7be9d34d99`  
		Last Modified: Tue, 26 May 2026 19:13:07 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b93c55a8a17efa21140a145fd562147dec16822626ea1fdbce157c87130b7d`  
		Last Modified: Tue, 26 May 2026 19:13:07 GMT  
		Size: 7.5 MB (7492164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb7c98c9da64692549be1b8d19d50b69c53473f24cb80d00d00bcc49d405703`  
		Last Modified: Tue, 26 May 2026 19:13:09 GMT  
		Size: 70.0 MB (70032507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9d90032b71529deec699e234f8c1e5f230e15afb2af9ed78f7d0e0ec2ede3d`  
		Last Modified: Tue, 26 May 2026 19:13:07 GMT  
		Size: 425.9 KB (425935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab98cb1d74db07915b7b1827c6a4bcf710244c844f86dfee323d670dac30646`  
		Last Modified: Tue, 26 May 2026 19:13:09 GMT  
		Size: 347.4 KB (347400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eded855bf9a27128e7cb32a1b5de87627789da0af98fe332221078cd232ee5c9`  
		Last Modified: Tue, 26 May 2026 19:13:08 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02921ca98efc95457685f61ec045d65e8ef5b0eb0583da320bf69b66d014a5fc`  
		Last Modified: Tue, 26 May 2026 19:13:10 GMT  
		Size: 42.8 MB (42815773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b11220b94c0da697b7694ad7215de07096e324d44080c7e14fe60d4cf4585eb`  
		Last Modified: Tue, 26 May 2026 19:13:09 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:8c778f5178140ba5d74207021493415318525e05d16193d1470c9706b9bde32b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3388759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bbd0f745d242a85ff69cd85d8e7cce3a421ff50bc4b7250f239a016b52b848c`

```dockerfile
```

-	Layers:
	-	`sha256:2b0e20389789aa223ce1281ba70d7e10d48fd4ab0bd37ae05eed938b3c59b532`  
		Last Modified: Tue, 26 May 2026 19:13:07 GMT  
		Size: 3.4 MB (3364329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c68180b30148fc0ed0bd328a02bc8f8f40105dbe4f49492c10cc96cc819dd1f`  
		Last Modified: Tue, 26 May 2026 19:13:07 GMT  
		Size: 24.4 KB (24430 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:0f9f531bfa4789601ee3332831064ce0c36a3d310050b09642101b9d8dfd74d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150054078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:866b12f85c6e83d60ad30361eac4681bbd18835ed93592503375780e9dc98a32`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 19:15:28 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 26 May 2026 19:15:28 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 26 May 2026 19:15:35 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:15:41 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-21-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:15:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 26 May 2026 19:15:44 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 26 May 2026 19:15:50 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:15:50 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ trixie main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 26 May 2026 19:15:56 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.2~trixie;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 26 May 2026 19:15:56 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 26 May 2026 19:15:56 GMT
VOLUME [/opt/nouveau/data]
# Tue, 26 May 2026 19:15:56 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 26 May 2026 19:15:56 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94b8c22a9aee84828061db0dd7d76c57cb2a7fd8e9323aaee931c95a0f6dc6c`  
		Last Modified: Tue, 26 May 2026 19:16:10 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899235a1ecdb426e0b3da18b61f42992f10ee1fd1a10b2c541fd669297f2d5b2`  
		Last Modified: Tue, 26 May 2026 19:16:11 GMT  
		Size: 7.3 MB (7261186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bc6b67f11a43dcedc8cf7dc50c2154ff2c60d4d0c774fb49fbf2f46566bc9e`  
		Last Modified: Tue, 26 May 2026 19:16:13 GMT  
		Size: 69.2 MB (69179669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7429788cc833857a325c900b7a0c2016a5b5de0f2f72fe9aba140e4ba160aafe`  
		Last Modified: Tue, 26 May 2026 19:16:10 GMT  
		Size: 390.2 KB (390234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d873aa82ca7ed235720ae188282afa5273741e99dbdf33261c1a6fc59f6779db`  
		Last Modified: Tue, 26 May 2026 19:16:12 GMT  
		Size: 347.4 KB (347355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca6365ca4a609038d3e36cdce14dd01e8185aea71b1a223c88451270a4bc9f5`  
		Last Modified: Tue, 26 May 2026 19:16:12 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f241c015171f7d7834492271e36620bb63c15966b4ff3d9a3d8a8a1ec6a848ed`  
		Last Modified: Tue, 26 May 2026 19:16:14 GMT  
		Size: 42.7 MB (42731840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c4929e8c4527ada0d772f38f8d68322cf21814750e8122e1806ae9b04928dc`  
		Last Modified: Tue, 26 May 2026 19:16:13 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:dcd22f542736aefd4d2a30a7548d8ffb85effc726edb9436fb5c4411e52b3a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3387582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380190f460d059d992367b535aa7953a4933d47e782c86303c532a8b7b15431b`

```dockerfile
```

-	Layers:
	-	`sha256:2d5490b97830a7a6171783bf1e51b72cc215ba1c2ff0827e6d39f519ac60f47b`  
		Last Modified: Tue, 26 May 2026 19:16:10 GMT  
		Size: 3.4 MB (3362970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d46173a258ed8d68f45424b620960e6ad3380b9d4e7632b7c2489b8fe44c102`  
		Last Modified: Tue, 26 May 2026 19:16:10 GMT  
		Size: 24.6 KB (24612 bytes)  
		MIME: application/vnd.in-toto+json
