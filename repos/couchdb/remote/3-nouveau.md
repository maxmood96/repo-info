## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:35d66c57efa2d6793f4dbecca8669fa1b73848b30e122e0271fd55f94996defc
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
$ docker pull couchdb@sha256:3367d5bccdc6396d4dfceaefb7be51f7b620060687976d4cb9710ca25e74edf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155532459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d8f9304ca9fc9cd9e8cfc0eebe108b76ec0de354123c8ccb5c037d31fd7c8c`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d037aa722688de92adccb49fc02c65a62c4c2cd27dcad1aeb2669f2bc91c80`  
		Last Modified: Tue, 04 Feb 2025 04:38:57 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e1d3bf05d75710981db4a96e2b04ef0c4afbbf6e85fd66a75f47fa297c4418`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 7.9 MB (7874966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6ca1ef4e87822fa39ec77697ee19ee6e4c576d95cd6abbc110cb78e304e7fd`  
		Last Modified: Tue, 04 Feb 2025 04:39:00 GMT  
		Size: 77.3 MB (77297441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b372823eab782fcf3ece2ce60437b076a83b6c18a91556dffbe12dcda6b77afb`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 414.9 KB (414935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c576d613f05214b663520384e2869fbfc8f022d828d799aba2eec3f39b0938`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 99.3 KB (99256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c158c51f6fa6055b49d8c93af63541e2a089873c92e50b60fcfd0042c460906d`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8b077ccd40cbf7eb1c494f65740d7a239a1c73a17c6fde0c9ce8ce66110c20`  
		Last Modified: Tue, 04 Feb 2025 04:39:00 GMT  
		Size: 41.6 MB (41631683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6b94af6e4c08acd7923e4e5a16820d970152112c37a2fad99d74c7699868cc`  
		Last Modified: Tue, 04 Feb 2025 04:38:59 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:0de0127374b8540c659ab771f5b9745858025812986f54653259e636e896bd8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3486616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dae0896f708bd13ef93048d280814ecc91d146a5ad7bd37adb354883947042d`

```dockerfile
```

-	Layers:
	-	`sha256:a889570ca4ab953857162a24ba10a8455803b9bef0e936f01a53f75796efce8c`  
		Last Modified: Tue, 04 Feb 2025 04:38:58 GMT  
		Size: 3.5 MB (3462052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3d12304afa1e2544372cf3ebd188cbc02fb0d22a90f98f6add8b5b32f904428`  
		Last Modified: Tue, 04 Feb 2025 04:38:57 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:ef7c562863a9fb584cc36263dc82db193a4a5c3956927ae78e18f702c0c5518e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.3 MB (154278229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b719cad0c7b5fdbfdbbac6dcb7a1e2ebde3550a3fe03266cf60522f6be67bab3`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79173b3fddb7da2629dd339e0d53b403ea8827bcbd9b247d684b58d32dff7cbf`  
		Last Modified: Tue, 14 Jan 2025 07:05:12 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31829078e1f4de67fcedf6a2d2d8ca1872f489122c7b4bcfa3cd33532c8cb239`  
		Last Modified: Tue, 14 Jan 2025 07:05:12 GMT  
		Size: 7.7 MB (7654485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3369295dc500f95559ea4509a427d2c0a4ee1c8ad2b7a79ee1dc560350241f77`  
		Last Modified: Tue, 14 Jan 2025 07:05:14 GMT  
		Size: 76.6 MB (76582294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e5bbcf4591afaea2d2cdc136dc489080dd97d81c24bd3ccbe400297114b51b`  
		Last Modified: Tue, 14 Jan 2025 07:05:12 GMT  
		Size: 371.7 KB (371693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acdad20d9a721bac2eb158329512906baee9555218f01a8e6ff0f9275510c66`  
		Last Modified: Tue, 14 Jan 2025 07:05:13 GMT  
		Size: 99.2 KB (99208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e627f9bf3e789b44c13cb9953004b89c6d68b322ee687562fe9fb76268a2d868`  
		Last Modified: Tue, 14 Jan 2025 07:05:13 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebeb5aa1e3f7f6837e61861bc4d688a7cb0e40daf66afe7b53355998b6c50ed`  
		Last Modified: Tue, 14 Jan 2025 07:05:14 GMT  
		Size: 41.5 MB (41527641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10a636108d2adc58e1f2c66283165d3226827a0d533ede0055e897d2464c6ed`  
		Last Modified: Tue, 14 Jan 2025 07:05:14 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:80be29eb1df008c822ee482e3954caa2ef94c11a5a1950dd74dbbaa0c6ace91a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3485478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071743ecadfba0fe3591807a89eb13c2932c9c451dc0d4b7924bb78aef478550`

```dockerfile
```

-	Layers:
	-	`sha256:c09558bcbcbf4d95c177b3cde1b9c16427e89ea9acbaf37de09ff936af7f2e77`  
		Last Modified: Tue, 14 Jan 2025 07:05:12 GMT  
		Size: 3.5 MB (3460732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1295fd7d68dfa423f317cb0bff79f1b1008e1459b1398163e931f34e6ccd895d`  
		Last Modified: Tue, 14 Jan 2025 07:05:12 GMT  
		Size: 24.7 KB (24746 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:c7ef31bf2d0cf9cadfe093f47d3336284a052b7c09043f3baa84a0e3fa393386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149142669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4aeeab96a922d7a1ab78f8460fac69a2a816ca3b6e125fed1cb4a6eed7411b5`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
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
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41a23a693d0435d9096a59c377a713b723450b592d3b5f06316fef9eeb38f17`  
		Last Modified: Tue, 04 Feb 2025 07:37:06 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc051593c4a07ef7ad5fd762b44283836710587d01abf2ebeb0a56303ab6172`  
		Last Modified: Tue, 04 Feb 2025 07:37:06 GMT  
		Size: 7.4 MB (7387901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f817f6fdb7f13d39c4df0f552ef9ca2bfa6e668a454e1da6ca2517a8efc439d9`  
		Last Modified: Tue, 04 Feb 2025 07:37:09 GMT  
		Size: 73.1 MB (73065167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0494d93c365c028f5059417ba8bf7f9b24d431a31b87fa6377d4e1d180e457af`  
		Last Modified: Tue, 04 Feb 2025 07:37:06 GMT  
		Size: 378.0 KB (378017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7ebdc392d75cc71bd7cc7de5e4d9eea830b1b497cc592e1fec293906ad84a9`  
		Last Modified: Tue, 04 Feb 2025 07:37:07 GMT  
		Size: 99.4 KB (99372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4bcabe0e2faf2b52aaaa7bd8b12785b477e128f41870e5861a2fb57f266265`  
		Last Modified: Tue, 04 Feb 2025 07:37:07 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5594b52dc2ed41f07ca8731f1d3a1508f5f12286f3634272fb8051567df6b2`  
		Last Modified: Tue, 04 Feb 2025 07:37:08 GMT  
		Size: 41.4 MB (41351710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850c8d679dc3d3d2968163532ab43de3cb43616f56858284de5bf2568d257228`  
		Last Modified: Tue, 04 Feb 2025 07:37:08 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:147ab9a2677c357e1185b231e231327efff5ee9bd4cb79ccd3cd7fee80e76849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3480036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e49dab81e90811dc3c065f49d460570083ed955142335d69205c40bcdf8370`

```dockerfile
```

-	Layers:
	-	`sha256:37f16ce50caae56e4424d9c7450676605d4306866eae78748dc06d4a5f21d5ac`  
		Last Modified: Tue, 04 Feb 2025 07:37:06 GMT  
		Size: 3.5 MB (3455473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11ef3b0df1d1e6be3ac92374cbf00a63eb24792839bf9e5fbd9a50931ab50a58`  
		Last Modified: Tue, 04 Feb 2025 07:37:06 GMT  
		Size: 24.6 KB (24563 bytes)  
		MIME: application/vnd.in-toto+json
