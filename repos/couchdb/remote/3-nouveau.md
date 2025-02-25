## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:e1c90b9e841242efe15e03f531a241ea963cc2ae33e74661b96e437ba35ee561
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
$ docker pull couchdb@sha256:bf9d15a52b4a4159de6f776059a1fc43fe6f0db3fdfdbdfd21f288ec2be77b0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155539446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c77c33bbbb0871a28c6df842259e0a2350a2c45d8b4ca305783b06ca1fce57e`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bf3493e51923e21aca2e6b0ed8bdd6c7397432e6a9216e30f2b60a2a7a74b1`  
		Last Modified: Tue, 25 Feb 2025 02:26:33 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c154d442b26e68a8569c856e9c65fc07ad78e6e22587a621336df375c0c37a`  
		Last Modified: Tue, 25 Feb 2025 02:26:33 GMT  
		Size: 7.9 MB (7874871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45c389dd0343a2e240f3dc400e9a571a5dd89785d86095d6d9c017b92dcf94f`  
		Last Modified: Tue, 25 Feb 2025 02:26:34 GMT  
		Size: 77.3 MB (77297471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618a4159279c674042f1505eb309bb61ad6e735ddf7fea3786d1ab4ef547b1fb`  
		Last Modified: Tue, 25 Feb 2025 02:26:33 GMT  
		Size: 415.0 KB (414956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50377d11c2cfc8d00bfb06284f9d90303501c7e8591acc20594dd3e7a1cd5d0`  
		Last Modified: Tue, 25 Feb 2025 02:26:34 GMT  
		Size: 99.3 KB (99279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5306fe2cf1e4820646b4c399391cc240a8572242d28718420e89286b264528b3`  
		Last Modified: Tue, 25 Feb 2025 02:26:34 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f219b56b995df8101c472c812043e14b1e66a089de47c712964fc9520948cba`  
		Last Modified: Tue, 25 Feb 2025 02:26:35 GMT  
		Size: 41.6 MB (41631688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2f811beb79d2150fe05b012e87da5ee1ef9e84e8daa89b1cf1f268cc4de1d3`  
		Last Modified: Tue, 25 Feb 2025 02:26:34 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:d47b2188df79dcf9dca0d53660a2bdd44f613a9b2bb59b20d387f08a669292e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3486634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc925911c466003c1dcb05333360af3fe74198da7ac0e26c85aedbe617d9d1c5`

```dockerfile
```

-	Layers:
	-	`sha256:acb1dc572371d0464b91b652afac79b1800022d27bf82bc6ae8b3ec439d41868`  
		Last Modified: Tue, 25 Feb 2025 02:26:33 GMT  
		Size: 3.5 MB (3462070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:635c35ed0a747f6dd5e0cc352dda4f32f8ba8df49ca711a277477ae6e7d45ed9`  
		Last Modified: Tue, 25 Feb 2025 02:26:33 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:46b7e16a02d458f58bb7f7e6e33439bc5a79efd5738fc1dba3ec515c17760c3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.3 MB (154327757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47acd08b258e314193a79ae54980bfb9aadaca06679af9fed998ecf27912d1a`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23e32040e94a467fba782c3c70d6b960930dd220a32afc9518070319e716e71`  
		Last Modified: Tue, 25 Feb 2025 05:46:57 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6198e0660a0211f3dfd8d86fe024630c661447399f6b1c1bcd9ddfe284c99a`  
		Last Modified: Tue, 25 Feb 2025 05:46:58 GMT  
		Size: 7.7 MB (7654528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5647f475f201681ceb2a8dbe35d9f91132ebe44ca55f72c4498980a3921f4b`  
		Last Modified: Tue, 25 Feb 2025 05:47:00 GMT  
		Size: 76.6 MB (76624219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc897d478950fe35ec176037d9cebbaef9c01f5d46a179ffacb3ff46d01ff011`  
		Last Modified: Tue, 25 Feb 2025 05:46:58 GMT  
		Size: 371.7 KB (371693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb85f5d159a6ed60007c738749a405199940d7f65da6322b8f386e13c9a52a0d`  
		Last Modified: Tue, 25 Feb 2025 05:46:59 GMT  
		Size: 99.2 KB (99249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b349509f6a1e7abf35c94990d6356a595b541f9ffd3ad610f822666aab5b1a2`  
		Last Modified: Tue, 25 Feb 2025 05:46:59 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a5ba1126c04e2d1c71bd3e1f4ea54203f16c3b574cea56c39efd5b435f62f3`  
		Last Modified: Tue, 25 Feb 2025 05:47:01 GMT  
		Size: 41.5 MB (41527762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a087379c72dcde45cfe30709070d2deb11aa3e64b1e03caad85bd66cf73660a3`  
		Last Modified: Tue, 25 Feb 2025 05:47:00 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:428f842fa4beb6d48ffee7e417502d3ec8ee8cf03aa0aaf57855f7b644a4c66c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3485492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca09c6e8bec8a0c13c980f1ddbed9fa7fe5f186f2122b64ae468cf3e04d59c6d`

```dockerfile
```

-	Layers:
	-	`sha256:3e8b1eeb300bd7e51f3faa5dda0f9de5d08831f4017f28c8f4002ef7f2a11682`  
		Last Modified: Tue, 25 Feb 2025 05:46:58 GMT  
		Size: 3.5 MB (3460746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5d140cf18f642d211e340a1b5dd6138007dadeeddfefe699e6160d13d2c1733`  
		Last Modified: Tue, 25 Feb 2025 05:46:57 GMT  
		Size: 24.7 KB (24746 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:90bfb19c1a3db8c4f68500a6fac9bd402fb039c8206b4e3cad1852ce33769ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149148959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24593b163730d5783917485605f7744caeb681a77c233c347868f5f304b56eb7`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
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
	-	`sha256:6d4d169c55c2ee02478b6705c4ba9e6795bffbbb872a22adfd95fb2484f2e85c`  
		Last Modified: Tue, 25 Feb 2025 01:30:03 GMT  
		Size: 26.9 MB (26864838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b727432b08dc53c299c29d0e1180458231688d633ab5fcc58c42ef288f9b33c`  
		Last Modified: Tue, 25 Feb 2025 04:09:01 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc1911e4d16dd8b248344768c9a45626cf2912d545de7c0c3b61d153eed6f7b`  
		Last Modified: Tue, 25 Feb 2025 04:09:02 GMT  
		Size: 7.4 MB (7387912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59dfb66040d2c2540d72bf1adfa2b3f30ea287e27bfeee50becffb3e8a1e5b69`  
		Last Modified: Tue, 25 Feb 2025 04:09:03 GMT  
		Size: 73.1 MB (73065184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0849999b446a0c2b8705bdeab4302d3d5aa3be979baa97ca133827931ac868d`  
		Last Modified: Tue, 25 Feb 2025 04:09:01 GMT  
		Size: 378.0 KB (378004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e1079eee2c1bbc3ef50a34cbad2955f10c4cfc749a7d6e2dce8d691f657fd0`  
		Last Modified: Tue, 25 Feb 2025 04:09:01 GMT  
		Size: 99.4 KB (99389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2bf2e65979d48d7255b35c892402899d216dc8d2ec4a4253f2070419817eb4`  
		Last Modified: Tue, 25 Feb 2025 04:09:02 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701f1d42140a93cba865e9b00567ff857e6b3e170d519fc1ff85a371dfd36930`  
		Last Modified: Tue, 25 Feb 2025 04:09:04 GMT  
		Size: 41.4 MB (41351750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e56e072d1d222f16d8a89d5145f779889c84127b56407c511d2f087226538d`  
		Last Modified: Tue, 25 Feb 2025 04:09:03 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:53631756e39d6b7f106a6a81ed54579011b38c2e623f5658a07c81901c4d6e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3480055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a51f1394f7060f9e98e24b5738ae72f02baa7519400f3b0adb01dcf10a755e1`

```dockerfile
```

-	Layers:
	-	`sha256:3fb6241ebd57d30869463d1b73b9a53dab62ca5e0c6674ffc3a22bd6b1a404f6`  
		Last Modified: Tue, 25 Feb 2025 04:09:01 GMT  
		Size: 3.5 MB (3455491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8116d21e02603b6c30c163d9b6497675b325b08ce3576f3ee96a8ad826c4ad45`  
		Last Modified: Tue, 25 Feb 2025 04:09:01 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json
