## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:857efe68d371236f1bdc898da343175868b5efeb9cf9934a13c8e173e786a354
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
$ docker pull couchdb@sha256:d73248e18a72d47573e1dea801a54fb37b52dd63e8e119bc0e3c42652bd75250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156452958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3109071ca4993e06ad0d4d6b1e786c48365329326ee7287ede57b68d35188d51`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 11 Nov 2025 20:12:39 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 11 Nov 2025 20:12:39 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 11 Nov 2025 20:12:45 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:12:52 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:12:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 11 Nov 2025 20:12:55 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 11 Nov 2025 20:12:58 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:12:58 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 11 Nov 2025 20:13:04 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 11 Nov 2025 20:13:04 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 11 Nov 2025 20:13:04 GMT
VOLUME [/opt/nouveau/data]
# Tue, 11 Nov 2025 20:13:04 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 11 Nov 2025 20:13:04 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4753a07d81ae29a1f5c07d626bbc1509aee278e77e3aaab375ab94890e9aeb9`  
		Last Modified: Tue, 11 Nov 2025 20:13:26 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605d123a589ba69a28cfc4dc492c43c5442935e8f6f784dc9144946ed0ff830e`  
		Last Modified: Tue, 11 Nov 2025 20:13:27 GMT  
		Size: 7.9 MB (7881782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1870aa4ea49712c48611828f9cc0d818149d5a1fb397d52253c79553ba04011b`  
		Last Modified: Tue, 11 Nov 2025 20:13:37 GMT  
		Size: 77.4 MB (77380766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fc3432c653b53a299e44685232f09f7b0809334dee2657458cc70fc82018ed`  
		Last Modified: Tue, 11 Nov 2025 20:13:27 GMT  
		Size: 424.1 KB (424112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894fa5b8d29848991cf9186656a612b7126749b77dafddb9091cafd934f3f14a`  
		Last Modified: Tue, 11 Nov 2025 20:13:27 GMT  
		Size: 99.5 KB (99510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f414fe051f965c8439ad7dd45b3d5e0f60fde782301d3d8b39b11063417be90`  
		Last Modified: Tue, 11 Nov 2025 20:13:26 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3341fb5bd5d5a909f909eea6e9a7411f41de72e5fdb5eb82b5cec97a2e247671`  
		Last Modified: Tue, 11 Nov 2025 20:13:31 GMT  
		Size: 42.4 MB (42436337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a6603e804abc967e250d9c8e5ea60352fb09cd05188ab4a0e930148cef296b`  
		Last Modified: Tue, 11 Nov 2025 20:13:27 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:d7b9a35fd9a8869c1c492ed858d55401fc8c539a4ecbb224d91f32a7796d7c49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:568857b4ebfd0100253c3aa4b17612124b10b5097410fd4cf6ea9e76a13db09c`

```dockerfile
```

-	Layers:
	-	`sha256:5beab407beb102095b5ffab57cf238fe0f9a40f8695b2a9d63b3960f912bb269`  
		Last Modified: Tue, 11 Nov 2025 23:33:37 GMT  
		Size: 3.7 MB (3658053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9ca515fdb2f9e12bf53a92941f03d3aec40b3cccf1d47c1b93e54f7f324c4f7`  
		Last Modified: Tue, 11 Nov 2025 23:33:38 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:09aba0fd985d41d85997a5812bc01ea3a6a4bab791e2a00f65fcbef473eee634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155318900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7782988f3e89e74a895aaec8f4fa216315d467dc79ab413ad89b9b1b097ff7dd`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 11 Nov 2025 20:11:10 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 11 Nov 2025 20:11:10 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 11 Nov 2025 20:11:16 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:11:24 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:11:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 11 Nov 2025 20:11:27 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 11 Nov 2025 20:11:31 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:11:31 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 11 Nov 2025 20:11:38 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 11 Nov 2025 20:11:38 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 11 Nov 2025 20:11:38 GMT
VOLUME [/opt/nouveau/data]
# Tue, 11 Nov 2025 20:11:38 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 11 Nov 2025 20:11:38 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7dd6974ccd35b0cb52781f6c8f38ebeac7a5d6260ac6ede11f3f8c9f7fc215`  
		Last Modified: Tue, 11 Nov 2025 20:12:17 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1f8a4ee6f68ed0ad0430ff95a0098ace6d81921806883704460db6aa1dfd1e`  
		Last Modified: Tue, 11 Nov 2025 20:12:18 GMT  
		Size: 7.7 MB (7692012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a18649a57bbd3cbc1c2fda4ecaf7696bada3bac421f257241f528509e9a1ee`  
		Last Modified: Tue, 11 Nov 2025 20:12:27 GMT  
		Size: 76.7 MB (76691503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42568529e1e6429a35c8c262d9019007ac5da91fabf5742ecd65afee0e60e85`  
		Last Modified: Tue, 11 Nov 2025 20:12:17 GMT  
		Size: 392.7 KB (392686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c20c9f876f0937864841173cc872d0b40ab7e4b1e874fd150bed14e316c8737`  
		Last Modified: Tue, 11 Nov 2025 20:12:17 GMT  
		Size: 99.4 KB (99415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a781ab25ac737fdef9c06353f09faae1dbbd846aa22e6257e1df72655b817015`  
		Last Modified: Tue, 11 Nov 2025 20:12:17 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88308c4f015c5ccafa012b61f255673fca6103af1fcadce254a335a1cc4c0ce1`  
		Last Modified: Tue, 11 Nov 2025 20:12:21 GMT  
		Size: 42.3 MB (42339027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ffc13d91d0ca731e7f6fcf4b27cb78c9e080738696cfcbc946b53d3b4b1c7b`  
		Last Modified: Tue, 11 Nov 2025 20:12:17 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:954d2c3f512a1932c0826eaf32a7cafce8d74f498b88dcf002d9dc150d9ffbc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a396232965fc39a5cef33e08c673a46005c9b24d8261d634c6669a512cea77`

```dockerfile
```

-	Layers:
	-	`sha256:93e8cb72952640bb24278dc2766189898940a409f998cc1523f49e1aa7a3ab04`  
		Last Modified: Tue, 11 Nov 2025 23:33:42 GMT  
		Size: 3.7 MB (3656729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:685e6f2cdaccaf4f44cc143d00ca81ec0005d0e2f61758c9ab557db887643f85`  
		Last Modified: Tue, 11 Nov 2025 23:33:43 GMT  
		Size: 24.7 KB (24703 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:2a59bc3eeaf33c611e6d20198a2d11c347ab3a09cc5f2a194ece87d4cd6917a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150086583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4df85d89689b925f7108cc12b037e552e41f9ce93759a791748679d571f57a`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 11 Nov 2025 20:14:55 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 11 Nov 2025 20:14:55 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 11 Nov 2025 20:15:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:15:32 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:15:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 11 Nov 2025 20:15:37 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 11 Nov 2025 20:15:47 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 20:15:47 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 11 Nov 2025 20:16:02 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 11 Nov 2025 20:16:03 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 11 Nov 2025 20:16:03 GMT
VOLUME [/opt/nouveau/data]
# Tue, 11 Nov 2025 20:16:03 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 11 Nov 2025 20:16:03 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3c6f64be9bdd3c2601d8e4c2d7c4354853fff0c19e8f7bdf9b09e8860c24e6`  
		Last Modified: Tue, 11 Nov 2025 20:17:13 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f243593476a0cede547d1c765b50ea8bc5efa48cb91301386dcac9c5051b81`  
		Last Modified: Tue, 11 Nov 2025 20:17:14 GMT  
		Size: 7.4 MB (7398148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0404524878fe3bbf61b798a9732c238278ceef6c536623058c409670c9c43acb`  
		Last Modified: Tue, 11 Nov 2025 20:17:21 GMT  
		Size: 73.1 MB (73143081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e5e1d70ec4cd7686fe1f025560584c71bd57c0d3c71a06189f1017d9bea5e6`  
		Last Modified: Tue, 11 Nov 2025 20:17:13 GMT  
		Size: 394.5 KB (394458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b4a7c215085507f09d210801f506b21c980a71e6e0d6dbd25e7b1f030c6046`  
		Last Modified: Tue, 11 Nov 2025 20:17:13 GMT  
		Size: 99.7 KB (99676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e9e3fba2322c92147365dab7fb2e4fee6e9a6fb98242badffe51b399fdd0dc`  
		Last Modified: Tue, 11 Nov 2025 20:17:13 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef31665d30c90ec5abf16e6d176c05980f28aa8a8a3ac0a2b120622b616d813`  
		Last Modified: Tue, 11 Nov 2025 20:17:18 GMT  
		Size: 42.2 MB (42164789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f743239c3077bc286d9a3930ffc95cabb89849d4301bbd7067f7a6f28a7526`  
		Last Modified: Tue, 11 Nov 2025 20:17:12 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:5c5b1bddcc346bbcf0737d83ff70de2b0e7a7ea0e9c8368bdd623d334bf5d05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a8b0a83d57b365c00a69979a736bd7e27430a4d90e6a47d46120b3f05e3b0e6`

```dockerfile
```

-	Layers:
	-	`sha256:9f369884d273c2e87ce29b44b7345886fdda1a13af7ab4872dce6501aad619bc`  
		Last Modified: Tue, 11 Nov 2025 23:33:47 GMT  
		Size: 3.6 MB (3648582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c740ff0a68a3faca5335b5543295da9494445384b911e1d54d362c5a109dc315`  
		Last Modified: Tue, 11 Nov 2025 23:33:48 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json
