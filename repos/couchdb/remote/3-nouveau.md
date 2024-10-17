## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:c8e6e619045e67b6f614ba41e24923a53b9a87e5b850ee0f0a832afeffb7ca31
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
$ docker pull couchdb@sha256:69201663158ef27cebf3754503b99930fd9fcba11b9ddca4004fb9ebab880526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156247349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c79aa53ba986a9a9f2923dcff657045fbfeba8b0df43c45b018df4c6b7a175`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Fri, 04 Oct 2024 23:09:59 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 23:09:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 04 Oct 2024 23:09:59 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
VOLUME [/opt/nouveau/data]
# Fri, 04 Oct 2024 23:09:59 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8341a5170e640ab064934f5a16b9ddda0d977e75c8a35a2c0a21624175ff7d55`  
		Last Modified: Thu, 17 Oct 2024 01:13:58 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d614eb0dffb75053d727b3da4345cc10290bedde0592ab11da569f1303d25e1c`  
		Last Modified: Thu, 17 Oct 2024 01:13:59 GMT  
		Size: 7.9 MB (7874325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f47713982a4618c995e645c57ccd25e4bb1a82c7f599781d74ac8beb173c91c`  
		Last Modified: Thu, 17 Oct 2024 01:14:01 GMT  
		Size: 77.2 MB (77212293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b504ad20a2b123b7701b91d47c94fca132bd9b7b0d87a62c98ffe3b0fba7961f`  
		Last Modified: Thu, 17 Oct 2024 01:13:59 GMT  
		Size: 414.9 KB (414915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccc4abaaed860931f8316e29ccaa1e28fb973cf3465f80a72c6bd229418a1b4`  
		Last Modified: Thu, 17 Oct 2024 01:13:59 GMT  
		Size: 99.2 KB (99225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3963ff4981167fb6541aa9d61cf3ca5ceea815cc334f709d7ba28bc35c5664c`  
		Last Modified: Thu, 17 Oct 2024 01:14:00 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d533960cb845281574aa500cd0664a7af2ff3a0d6f0375b9cec594d6c2dbef`  
		Last Modified: Thu, 17 Oct 2024 01:14:02 GMT  
		Size: 41.5 MB (41518425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25cdd0790b455c2f406f8cc76c546a18ae0c354a7cef553c69bd5e3474d2640`  
		Last Modified: Thu, 17 Oct 2024 01:14:00 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:73f91e3d4325120c083b80a024abe041b6d609fe89dab2f33f1af4ca0acba313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3478701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17bd9c4df629543404caa7974aa89adc67ba197f9468d81ede57cf02ff55e70d`

```dockerfile
```

-	Layers:
	-	`sha256:8db47e984c370964cf9a1fe7f608b95199bacd19bd67b8ac7599931763c3f615`  
		Last Modified: Thu, 17 Oct 2024 01:13:59 GMT  
		Size: 3.5 MB (3454275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d85194621739adfae301dd10b86700352c70ef6325d11a0fc4591cd7625a2c41`  
		Last Modified: Thu, 17 Oct 2024 01:13:58 GMT  
		Size: 24.4 KB (24426 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:8a5b77c7118d220a61071998d224249d041f9f74083eb8f3591fbe9ceef936fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155210795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98b353a401f166bb68e575bfd822646a3608e820cc4231fa13464b0683e3e985`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Fri, 04 Oct 2024 23:09:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 23:09:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 04 Oct 2024 23:09:59 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
VOLUME [/opt/nouveau/data]
# Fri, 04 Oct 2024 23:09:59 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Fri, 04 Oct 2024 23:09:59 GMT
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
	-	`sha256:1cfb43d3130dea5b226ee6d3d7a89a1a039708a27401ad55338f9509583bed31`  
		Last Modified: Thu, 17 Oct 2024 08:37:08 GMT  
		Size: 7.7 MB (7653601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e5d718c0a45301c947c0bca060f0ef28d7c83043355da9e77a0804f831f46c`  
		Last Modified: Thu, 17 Oct 2024 08:37:10 GMT  
		Size: 76.5 MB (76508581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7eece477d75c7f105fdd604598ed02f5b1068a219cbe58a2229256b9893b5d3`  
		Last Modified: Thu, 17 Oct 2024 08:37:08 GMT  
		Size: 371.7 KB (371682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7cbcc8c872a854268b654cdb819597d6728167612a8a56425d398b2fe641fb`  
		Last Modified: Thu, 17 Oct 2024 08:37:09 GMT  
		Size: 99.2 KB (99198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e6bc749445a8325728ef17a17221250d734e41f3062355d62748a56c7fc33b`  
		Last Modified: Thu, 17 Oct 2024 08:37:09 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e94d56078b2aa7190091ad8d91efea53f6653876edd7f1f68acc5f36cb423c`  
		Last Modified: Thu, 17 Oct 2024 08:37:10 GMT  
		Size: 41.4 MB (41419520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198e8ef17bfe3703c4efccfe17c5f2e1f4beb2d8e1ca32ea4636edadc5e16b4b`  
		Last Modified: Thu, 17 Oct 2024 08:37:10 GMT  
		Size: 414.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:655485c5c80e437b211a9b7f0151c0b8459ae590de744b1eab9fc57d195b3ef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3477550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4d47175e6d8e0f3339c0bef4902b5f78f1161136c89714e9a9f55dc66212e2`

```dockerfile
```

-	Layers:
	-	`sha256:13a60c99d849a0e9a27b5590f5fd975c20c879523ee7a6ca32fed3c2420d6981`  
		Last Modified: Thu, 17 Oct 2024 08:37:08 GMT  
		Size: 3.5 MB (3452948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dec208ef53f3f257d00c26a0de0714575dc0ed04a9ee0900349e84366c9cccaf`  
		Last Modified: Thu, 17 Oct 2024 08:37:08 GMT  
		Size: 24.6 KB (24602 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:34e4e127c5f9ef485fade28d3f311f0e0c6cbc12a7c2af25afdb08d9c4d4caaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.6 MB (149594813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b07f083ecd69500e12739cee0bfb3d845466964e509d5554f6a5f49be3396e`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Fri, 04 Oct 2024 23:09:59 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 23:09:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 04 Oct 2024 23:09:59 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
VOLUME [/opt/nouveau/data]
# Fri, 04 Oct 2024 23:09:59 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Fri, 04 Oct 2024 23:09:59 GMT
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
	-	`sha256:7b2b747794ac6e71d08c738e803fc7a9e53a96be7f4b2da17fc311c92665edc0`  
		Last Modified: Thu, 17 Oct 2024 05:24:06 GMT  
		Size: 99.3 KB (99349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a453eab34057d928b0e5ff72f73999ad46c3263d20fa80d54147d243cf941591`  
		Last Modified: Thu, 17 Oct 2024 05:24:06 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344df0ea4b3986556ab2689e47053d6f23aafb0939e455160a615261744c971e`  
		Last Modified: Thu, 17 Oct 2024 05:24:07 GMT  
		Size: 41.3 MB (41250686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077039b4df922fb240063f1a67223bc9406740c5e13ae052c295261ab50c2533`  
		Last Modified: Thu, 17 Oct 2024 05:24:07 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:a7c98572f2af51d20a27ac5ecd3d8a1ae45d8bc53fad772fd172b9a519e43393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3472219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fbcbfc99f19034f187721f94a407d269357eeb33e8f3b50f38cf08be226de3b`

```dockerfile
```

-	Layers:
	-	`sha256:1357a127db355bdd98ee39a75190cb56b6661faef478e43e331e35c51fb8686e`  
		Last Modified: Thu, 17 Oct 2024 05:24:05 GMT  
		Size: 3.4 MB (3447794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85650d43777473290fad1f06db62d0cc4ac3f2ad81e6cdd6f3538051ab7ca92e`  
		Last Modified: Thu, 17 Oct 2024 05:24:05 GMT  
		Size: 24.4 KB (24425 bytes)  
		MIME: application/vnd.in-toto+json
