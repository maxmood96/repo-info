## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:326237f0552c116d1340a4abd47f0f7108fb3dbd1dc34d22cbcdbfc493e95a4c
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
$ docker pull couchdb@sha256:7bd253076622dcfcb6390cca1f7e0ef8fe83d3504e6b64619ba3090670eacbc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156398496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81b0eb4603d1137e4adfdfc2f8785f91a0311569bf4cc7cd673f4079ac8a842`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1639cafcca63de311712b892899c6cc4aed9b5371718452f73380bcd6d15774`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fe5ecf3044eb58f2d7bb999fa2981b736f0433e5d8aafb88a1cf01b3c274ae`  
		Last Modified: Tue, 21 Oct 2025 01:44:15 GMT  
		Size: 7.9 MB (7881771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff1706f57bdad1e318fdf510014d94c77ab287f8247cd180e39062e3109065b`  
		Last Modified: Tue, 21 Oct 2025 01:44:25 GMT  
		Size: 77.3 MB (77326889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32856d57f2141400969d53beba7c40d25dad6311f6709c266be89652f44f7cf2`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 424.1 KB (424064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce9b35b25040ddc65ea8f8e44b67cc3700ff2c7d6a1d7a1e9af3292d6d296cc`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 99.5 KB (99487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472adf561563b0ecd0f159f3fa8916f2b8d9757a4d6f1e5c473d706367c41280`  
		Last Modified: Tue, 21 Oct 2025 01:44:14 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7880d7850c9a69d617f6f008c3ef14c95ad8e3d094439388b97c6551ca9e7051`  
		Last Modified: Tue, 21 Oct 2025 01:44:17 GMT  
		Size: 42.4 MB (42436086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b827c26d71cef106323dddc4f16c6d5bea3d454c6c63f5d10dd630b965ce66`  
		Last Modified: Tue, 21 Oct 2025 01:44:15 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:353d203253063a16bb3ebefcb3e68999a8d5829ea8764433c3284b52347c42f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9e95b2bd113e2f279f39a4dcd398e62ea0a6106ee21cc82003119a5fa95e12`

```dockerfile
```

-	Layers:
	-	`sha256:a9941eaff4817d44a1e322cffe23af5051161dbc6dea017aea5806c3e3937b5c`  
		Last Modified: Tue, 21 Oct 2025 10:33:32 GMT  
		Size: 3.7 MB (3658049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a221761a19ff308c3e9acc58f511ffb2d53322d69e772e24f853ec43e9ae0605`  
		Last Modified: Tue, 21 Oct 2025 10:33:33 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:e33829de3bae4d35bb957449de2e0a183c4f0aef75f46dfba71c4da45a6364f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155279417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25262966e44ddd3f261905517a41e46d230b9c0996f3d41602081d90ad5e5a88`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 06 May 2025 02:16:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b23ec744cbf628e7915ee0abd034e7b1082b4d9f9f922d47a701c7b39c8fa0`  
		Last Modified: Tue, 21 Oct 2025 01:48:39 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf943ff90737b14c37e7d4d2a8682196e70ebdf1ca2ca6fe7d852e7c60641c2c`  
		Last Modified: Tue, 21 Oct 2025 01:48:40 GMT  
		Size: 7.7 MB (7692029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1895b3861d497a754f77085690a46cc8ddc49ba295a2a9940469b045c2afce`  
		Last Modified: Tue, 21 Oct 2025 01:48:47 GMT  
		Size: 76.7 MB (76652724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f24b65d8dec75be45ffbae4e68f04f096f2000091d0766eec0e21e0beafa08`  
		Last Modified: Tue, 21 Oct 2025 01:48:39 GMT  
		Size: 392.7 KB (392700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d801aaabd0aa70a3ef10379e047ab4cefe8a9dae46c5119341e03d62f7fcb6`  
		Last Modified: Tue, 21 Oct 2025 01:48:40 GMT  
		Size: 99.5 KB (99462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c62e1afce1ee387d8b513aeb417f5d2923b3c8effc353a803236d2997d6dbbc`  
		Last Modified: Tue, 21 Oct 2025 01:48:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd698eb5dda21c64b725fc1f35382a140e35d2a8fcd394d2581666c65a5b4d8`  
		Last Modified: Tue, 21 Oct 2025 01:48:42 GMT  
		Size: 42.3 MB (42338433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a57ac6ba65a5db293fad3d0b56087e40b78f646d98984b94b4c80e6ef53118`  
		Last Modified: Tue, 21 Oct 2025 01:48:39 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:b3bfa3c9b78f805d794ed3b6cef47e55f6e156ae0c1c433975c0b2175ee95880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1faf9bfd155669dd6d67d932b17cee107705c6bf761944d1d9b886c24dddf5d2`

```dockerfile
```

-	Layers:
	-	`sha256:a86901657a28f2106c4989414d4464b32b17948db61b1fc52565b28bcc88c496`  
		Last Modified: Tue, 21 Oct 2025 10:33:37 GMT  
		Size: 3.7 MB (3656725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:270b30851a2520992933292b5593e150437a79030176d467eb46b7b015c8032d`  
		Last Modified: Tue, 21 Oct 2025 10:33:38 GMT  
		Size: 24.7 KB (24745 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:e4c1cf464286a900ce86d7096170b79c191b0074671bbe641daeb58da6f1ac72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150084594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6dc22a341d88212c87b94678a78c8dbf8254d5dce3e2650d1438777fd86356c`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 03:18:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Nov 2025 03:18:35 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 04 Nov 2025 03:18:40 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:18:50 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:18:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 04 Nov 2025 03:18:53 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Nov 2025 03:18:57 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:18:57 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 04 Nov 2025 03:19:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.0~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 04 Nov 2025 03:19:10 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 04 Nov 2025 03:19:10 GMT
VOLUME [/opt/nouveau/data]
# Tue, 04 Nov 2025 03:19:10 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 04 Nov 2025 03:19:10 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7536539bf1ad715cf2dd300635c28f289b63af1cbb92522e91502eef246923`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526e0a76fba7a4a90e9f82e82a2d36b1fb986318a85518bfc9635401a95de3e9`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 7.4 MB (7398078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce039d7896ebedadc57a51103ebe71649e42dcf66503771ad322910999b1c820`  
		Last Modified: Tue, 04 Nov 2025 03:19:46 GMT  
		Size: 73.1 MB (73142672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5a2015e06dd327a6fa19c3c6249a4fce7b4de27b48d0ffe99bd89193cdc50d`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 394.4 KB (394429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2edba20a7c1a1e969e4475b2647e6299aa0a17f5c863767efe6b0eba76bd8b9`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 99.6 KB (99633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758223be14bf6c71052fd32d6b25ffd5166b527a06b436acc6588a71754d8256`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a42ee912410feb134c1beae3caa7a5819b26a2805c5f5788a2f1c752a05596`  
		Last Modified: Tue, 04 Nov 2025 03:19:45 GMT  
		Size: 42.2 MB (42163353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28b2decc0bdb622a25486a906d92d47c9957614b0b2ddb085d111ec24b66527`  
		Last Modified: Tue, 04 Nov 2025 03:19:41 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:11dfbbe0f26655b6dfe5283f838c837702a2801997b244b3a58e3a1ec15d5fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6db580cd46bc75bb51312e6ea0a2dfb655c8e7fe65b7510b23417a1d0c73e9`

```dockerfile
```

-	Layers:
	-	`sha256:1d791db3ab66f5870c8b313ea2a48f5fdf410625cdd00d14b2c3fe7fd8f612da`  
		Last Modified: Tue, 04 Nov 2025 08:33:32 GMT  
		Size: 3.6 MB (3648582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:908d204e4b43581a218031a0ded371c1bfa2b0e497370e7987e87a5c61463cfd`  
		Last Modified: Tue, 04 Nov 2025 08:33:32 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json
