## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:7aa225cc2752c9f713a6da74c1f0fb5dd26d59909cf6e65bdfa1042643f93e33
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
$ docker pull couchdb@sha256:89743ee7151b366d6b28891c88f05210539626294c3321c7345d2efd0e90baae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156452823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb0753316d72cc07f4f3abbacfdc4ac02d3c7f4ecd6c71fd7c837e33285365f`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:08:07 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 08 Dec 2025 23:08:07 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Mon, 08 Dec 2025 23:08:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:22 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 08 Dec 2025 23:08:24 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 08 Dec 2025 23:08:28 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:28 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 08 Dec 2025 23:08:34 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Mon, 08 Dec 2025 23:08:34 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Mon, 08 Dec 2025 23:08:34 GMT
VOLUME [/opt/nouveau/data]
# Mon, 08 Dec 2025 23:08:34 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Mon, 08 Dec 2025 23:08:34 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10769f6e3ca05b0d30f4148aa16e7c13217c6a625a803ea087ee5804768ab4a9`  
		Last Modified: Mon, 08 Dec 2025 23:08:59 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0703e44e2d7cafd694d8589161e1f5636f76a9b3d970195a5db2aa4b2406a2`  
		Last Modified: Mon, 08 Dec 2025 23:09:01 GMT  
		Size: 7.9 MB (7881795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d787b4bdf36bea424e37ecda03ad1f3ea9805c39521e250c7d97b554b8cd29a3`  
		Last Modified: Mon, 08 Dec 2025 23:09:07 GMT  
		Size: 77.4 MB (77380734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1380eab6cfd83025c297d8099e1247247d56bf95db84862a76d1a5becb1d35f`  
		Last Modified: Mon, 08 Dec 2025 23:08:59 GMT  
		Size: 424.1 KB (424123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daf5d2841e907f58723ac0ae3c6fc6078ec51ae8600573953ff5e97445202ad`  
		Last Modified: Mon, 08 Dec 2025 23:08:59 GMT  
		Size: 99.5 KB (99518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6cb9bf85b66a1cc208c72599a77b2136ea9d83b7646638973352fec03986fb`  
		Last Modified: Mon, 08 Dec 2025 23:08:59 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c573270414f2f71a211e02c3a9aacdcc054f37201a785bd7b76d105e0f142c1`  
		Last Modified: Mon, 08 Dec 2025 23:09:03 GMT  
		Size: 42.4 MB (42436360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbfe2f3d09ee37fa7d61d8b5bc8348ab29b5fbcd32c65e3a0814f1387c4cf010`  
		Last Modified: Mon, 08 Dec 2025 23:08:59 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:2e4168227791331cacb1f46381af60e5517e8a49edc38ed67a04d517236fed73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3f852f63f06fb6a6280ac9e16c490f7f1d4c953810bcd05e1e15444a2153c2e`

```dockerfile
```

-	Layers:
	-	`sha256:1e1592694180e85e28f9f9b10cca96e33f11889b75314b91185faceba2b0a0f1`  
		Last Modified: Mon, 08 Dec 2025 23:34:26 GMT  
		Size: 3.7 MB (3658053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:178217fabee2aa3c6d311ebede57eca5ce36fbe5975f4a8d599ad046659d337b`  
		Last Modified: Mon, 08 Dec 2025 23:34:26 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:a66ded546ea638eea1b1e6606f7807c953a83f6f4b8f4f3e0a7060a80ef4db83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155319057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1449e314b7659f7e9f5cac4040dfc02ac1ea6fb07fc1b139d072c343d7f8a3e8`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:11:34 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 08 Dec 2025 23:11:34 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Mon, 08 Dec 2025 23:11:40 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:11:48 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:11:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 08 Dec 2025 23:11:50 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 08 Dec 2025 23:11:55 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:11:55 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 08 Dec 2025 23:12:01 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Mon, 08 Dec 2025 23:12:01 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Mon, 08 Dec 2025 23:12:01 GMT
VOLUME [/opt/nouveau/data]
# Mon, 08 Dec 2025 23:12:01 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Mon, 08 Dec 2025 23:12:01 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6eba3ed937a66dd32e288cb57c956c3f9c02d9bff7ded9ec7a41d1293212c3`  
		Last Modified: Mon, 08 Dec 2025 23:12:24 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b10e0f0698717d20e4ae819b97f586be1e19407bde2f4244d0666878875a42`  
		Last Modified: Mon, 08 Dec 2025 23:12:25 GMT  
		Size: 7.7 MB (7692063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960d27dd6da6030143a0782364b9056774ecedbf3e60a097948599b18c4f050f`  
		Last Modified: Mon, 08 Dec 2025 23:12:33 GMT  
		Size: 76.7 MB (76691609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9abc4bacdbe333df02199646e76d5fc7fdb56e41deb84a2139151bb1d65a94`  
		Last Modified: Mon, 08 Dec 2025 23:12:25 GMT  
		Size: 392.7 KB (392695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2991ace0a10c0d0a9151f3e3e33264613df0c6bacc2e3e39a1f9dfad4af009`  
		Last Modified: Mon, 08 Dec 2025 23:12:25 GMT  
		Size: 99.5 KB (99499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c2b7279d74d54bfd0a52ae53268c0315157fbd7b2decbd7465f82ea2c081aa`  
		Last Modified: Mon, 08 Dec 2025 23:12:25 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cbedf57041f3c896dba518b8e3c6db301b748a20745a9e2f137ba26785e517`  
		Last Modified: Mon, 08 Dec 2025 23:12:28 GMT  
		Size: 42.3 MB (42339091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2796c1185dac7371a566307b03c6fef1fc84f5447fc111de92a8557be9a3711`  
		Last Modified: Mon, 08 Dec 2025 23:12:25 GMT  
		Size: 415.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:cb77664c7e9e649b597ef162dd1f40e36e82941bf25dfb176b1dbec888a1d0fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ba42ef3c6bbe478ac2933ab0f2dea9fbc30d8d30c154d0169eb239020d59b35`

```dockerfile
```

-	Layers:
	-	`sha256:f09c6ebb48a92ec8608c6c931e58da2eb88a5c2b361b6a5ce342a5d24ce0f61e`  
		Last Modified: Tue, 09 Dec 2025 05:33:38 GMT  
		Size: 3.7 MB (3656729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8317b7ee60ef9edcf00bd9ea9dad98b15997a2a376b8c3fd3df0d4a99fc56fda`  
		Last Modified: Tue, 09 Dec 2025 05:33:39 GMT  
		Size: 24.7 KB (24703 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:7c12e5c2d11a4e335bc8a826debcde85a8431afeb2d5ded342bc42c376eb1274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150085870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76459a52a9683cd87c99ca9180c3ada00aaf5d7d8038c9914d42a391453dea26`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:12:23 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 09 Dec 2025 00:12:23 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 09 Dec 2025 00:12:29 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:12:37 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:12:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 09 Dec 2025 00:12:39 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 09 Dec 2025 00:12:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:12:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 09 Dec 2025 00:12:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 09 Dec 2025 00:12:52 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 09 Dec 2025 00:12:52 GMT
VOLUME [/opt/nouveau/data]
# Tue, 09 Dec 2025 00:12:52 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 09 Dec 2025 00:12:52 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:00a29f44cb5b31bbcf043ec5426ee1c018bb26435350712cb5e48d56c6d95792`  
		Last Modified: Mon, 08 Dec 2025 22:15:04 GMT  
		Size: 26.9 MB (26884429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c612ddb2613792ba5de7275ede737232c8919bcc9a90ad4dc4a90f42280a0c1`  
		Last Modified: Tue, 09 Dec 2025 00:13:19 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe05b0e865a4ea871efebb32075b19d70f33e93973dbf638d5e901eacd7440b`  
		Last Modified: Tue, 09 Dec 2025 00:13:20 GMT  
		Size: 7.4 MB (7398109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a18a834e5966996b03bde3dcc826f2b0f461c9717c2a61a157c164bc0035d65`  
		Last Modified: Tue, 09 Dec 2025 00:13:26 GMT  
		Size: 73.1 MB (73142808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508bcd23c82e79bad82091e27743c8746f4b842f6e06556e20c6f6f34a1cf953`  
		Last Modified: Tue, 09 Dec 2025 00:13:19 GMT  
		Size: 394.4 KB (394392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bbf41a4ae36e10031fc97050f94fbb0ca20081067177751280bee84b46f9584`  
		Last Modified: Tue, 09 Dec 2025 00:13:19 GMT  
		Size: 99.6 KB (99616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6092dee6efcbddddabba5653f407f3336d213fc568ad9c6706694ef1f9d439`  
		Last Modified: Tue, 09 Dec 2025 00:13:19 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a684fa098de563675f00459f674e4c14b2b3edb8dbf71202bc5d7f45c816cd`  
		Last Modified: Tue, 09 Dec 2025 00:13:22 GMT  
		Size: 42.2 MB (42164639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d62053a9e778fc9ff6f26567bed49bc2cc11e771c13d99a53c5014a70c3a393`  
		Last Modified: Tue, 09 Dec 2025 00:13:19 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:fafb2fb277c2d762056e9587dee834882ec7139cc3b0784d183c8b78e67d1ab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e08fae2b3c9cf16c44563ea23595fa688447bc2544e2f2df04f047d64771c55`

```dockerfile
```

-	Layers:
	-	`sha256:c5809d637293d25977e1b07b589b7d0fd3dce59684371058f33db1b61ec2b506`  
		Last Modified: Tue, 09 Dec 2025 02:33:53 GMT  
		Size: 3.6 MB (3648582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d2c29a59962a0f97410221034dec64942903f474ca029dc5e698be9544e54a0`  
		Last Modified: Tue, 09 Dec 2025 02:33:53 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json
