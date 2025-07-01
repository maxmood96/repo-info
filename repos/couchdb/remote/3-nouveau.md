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
