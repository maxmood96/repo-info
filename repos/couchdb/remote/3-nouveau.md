## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:1926f3b80d1d7b2447ecbe26aed9c6688897332f0e04d7767d82c8850fd72524
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
$ docker pull couchdb@sha256:7d73dd1c6b22690398fd72ff27a25874164de7d806fd9772c4c137cdb2d7980c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156433595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b23780d2087cf211c268ccd827028c5c107a9278082704c4cd701de05ad3248`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3e36b499d69fac410ec13e0e90b60065a5b483078f5d3e2536254423e5222f`  
		Last Modified: Tue, 12 Nov 2024 02:38:58 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a763829d6bfcab12c49dcd6b99fedaee601a9530fdef21eb74787cd2d7bb51`  
		Last Modified: Tue, 12 Nov 2024 02:38:59 GMT  
		Size: 7.9 MB (7874861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f566daf2fdaf3790e6e330ee6247a9905d27094c64f025b74bf822ecc1fd00`  
		Last Modified: Tue, 12 Nov 2024 02:39:02 GMT  
		Size: 77.3 MB (77283799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce07e481c7742184cdcb01de441e4178ae91c88aa40f42a7f18b94c4c1783c60`  
		Last Modified: Tue, 12 Nov 2024 02:38:59 GMT  
		Size: 415.0 KB (414956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0aff5ca936036838c76a8d98fc6b07c79f42bf78110b37f28a3ba34bf970b5`  
		Last Modified: Tue, 12 Nov 2024 02:38:59 GMT  
		Size: 99.3 KB (99285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04889d990fb1ce0f1ca9e4b6e4f74f4b76af37331fe91a4e11300b33a6dca558`  
		Last Modified: Tue, 12 Nov 2024 02:39:00 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ee84f15d3c696930742e848143b57371c46d7abfef5b603f149daa53cdac08`  
		Last Modified: Tue, 12 Nov 2024 02:39:02 GMT  
		Size: 41.6 MB (41630822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba664c1772d53c31b6a9bd5cb04686013b55788ee8e6c84c8b3662d9afa76033`  
		Last Modified: Tue, 12 Nov 2024 02:39:01 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:5fa80ed1bb4a2513c114fedad9b26e6ded2360a2792c6a566f0574aee8c3068e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3499647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a25a7ac49f8a425785a8beda80ee4155187481585517753a83409d9924ed016`

```dockerfile
```

-	Layers:
	-	`sha256:ffa03f762479765e205bfad5e8dd0fbbb0e09ab401ecc2b1ddcd19c70335fdf0`  
		Last Modified: Tue, 12 Nov 2024 02:38:59 GMT  
		Size: 3.5 MB (3475085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff075489e5b49cb272d18000416cbb85dad3443e7f28df20fb6e7c5a6a6b4ac4`  
		Last Modified: Tue, 12 Nov 2024 02:38:58 GMT  
		Size: 24.6 KB (24562 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:b87d41d8a4dc850c9df23b5e490b0eaf7534cfe9a81c549507cda07de713114a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155393649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1603b44f6c46c1b5e9aec253ff61d9d9f108720c3a74cd92ba52f643eb92595`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c23dade21ddc63b42d2647ee5bd298a2ef267e5acab231c2d6da080d9d71e6e`  
		Last Modified: Thu, 17 Oct 2024 08:37:08 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a2f199b083cc236d74acc480bc9abac691d493b1b8e8369c9b0d711304a0d0`  
		Last Modified: Tue, 22 Oct 2024 22:57:00 GMT  
		Size: 7.7 MB (7653607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8459eb8b4c9964bd391e5d65122d9a6b51597679a46b26371df1aa25c7981230`  
		Last Modified: Tue, 22 Oct 2024 22:57:02 GMT  
		Size: 76.6 MB (76584069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d986d3cb2299ff5e9dcb002b84ed876ae4e141113c44029975f6e0285da4e5`  
		Last Modified: Tue, 22 Oct 2024 22:57:00 GMT  
		Size: 371.7 KB (371687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3658ba1a93b3f07ccb268aeee3cb247fd401728815cc696750fe4aa47e142d86`  
		Last Modified: Tue, 22 Oct 2024 22:57:00 GMT  
		Size: 99.2 KB (99196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa093cddfcef74b5ea9feb12e196ed0de5282e3862fdfbe9388a13a8c3eba4f`  
		Last Modified: Tue, 22 Oct 2024 22:57:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c7071f8700c62ae031ca50097a10bcd1c1e8a1b663bb00a6de3432fd5f37d4`  
		Last Modified: Tue, 22 Oct 2024 22:57:02 GMT  
		Size: 41.5 MB (41526874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d704fde3024b8d5493329ea84940158034a267430e68c3b5fc6aa9b0ac28709b`  
		Last Modified: Tue, 22 Oct 2024 22:57:01 GMT  
		Size: 416.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:8c740bc74395f333b71bbaba633ce42a1d82c5d44247db9146df72b187582fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3498284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b511829792aaf6014b3919f785f3fd3597e0bbd618669e654196b9ef11d97bf8`

```dockerfile
```

-	Layers:
	-	`sha256:4bca8295be7075aaf79068a58523545f2b3f747f8d1182985c8834b17445ba74`  
		Last Modified: Tue, 22 Oct 2024 22:57:00 GMT  
		Size: 3.5 MB (3473686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca52556d4416346ade61f88b44b846655e00138f989397d40478b0dc89035e1f`  
		Last Modified: Tue, 22 Oct 2024 22:56:59 GMT  
		Size: 24.6 KB (24598 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:9c1ef8d882ad2a39aabede9dd9618fc509ea688a2656516d9e7bc5cbad8815b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.7 MB (149694297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f357876e799ae616d266610e1d06caa8caf32864db5e7aeec036af831dcc6f`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Thu, 17 Oct 2024 01:46:19 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Thu, 17 Oct 2024 01:46:20 GMT
CMD ["bash"]
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1da9e475f448a5faef36ac7b6cb60c0ad8ce9821f2cbaa18d4ee80f33bb576e`  
		Last Modified: Thu, 17 Oct 2024 05:24:05 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca823418cdd443363165feda244a9e4293b99d5a5ac44d9df8a9ca407b4e094a`  
		Last Modified: Thu, 17 Oct 2024 05:24:06 GMT  
		Size: 7.4 MB (7387056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74513d24c6f38678360078dd599c83f6bc450d3c4cc8a46592c568a62d65b05c`  
		Last Modified: Thu, 17 Oct 2024 05:24:07 GMT  
		Size: 73.0 MB (72987699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85ee38c5a5951cf9fc20bccabb755a2a8d30f1b5fac51d652db2480d4a66777`  
		Last Modified: Thu, 17 Oct 2024 05:24:05 GMT  
		Size: 378.1 KB (378063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cb6d89a6b9087d4daf3331a8be333d5960b84a86130082d8bfd1aaf2f36edb`  
		Last Modified: Tue, 22 Oct 2024 23:56:24 GMT  
		Size: 99.4 KB (99401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e31eff99c6fb1216cf68e2d0f529445ba1aae32b5b67413f295c6d7fd4a16fa`  
		Last Modified: Tue, 22 Oct 2024 23:56:24 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84b21674d70f2a1777465fab7d6bf597d8964a204d7e78a8875fddfeb417d5c`  
		Last Modified: Tue, 22 Oct 2024 23:56:26 GMT  
		Size: 41.4 MB (41350117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ea2dbcdf1c3031ae0f80e99fc0ffe1db1d1e28e9b9ca3efa88387f1d859a27`  
		Last Modified: Tue, 22 Oct 2024 23:56:25 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:1417ea97a276ee8a8fb10abe083039bf3ae9b3742e42efda44a3a2cc8ef06352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3492025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4d79b4570f0c96ab938e0077a4c59472d12f9848cabca62474036bcbb1134a`

```dockerfile
```

-	Layers:
	-	`sha256:6360006e3ebd940c18522319a3bcacf1080b903d41fe0f7cd245ea0c02328b76`  
		Last Modified: Tue, 22 Oct 2024 23:56:24 GMT  
		Size: 3.5 MB (3467603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42af42392434bcfb940dc5dc3ffdd68e9721234cbcb8fed39457a9b116126596`  
		Last Modified: Tue, 22 Oct 2024 23:56:24 GMT  
		Size: 24.4 KB (24422 bytes)  
		MIME: application/vnd.in-toto+json
