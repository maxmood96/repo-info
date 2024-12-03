## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:0601f22d55569e387670df07bb40314793af5b5d2c32d39a34de5ba59e144414
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
$ docker pull couchdb@sha256:ee3c19ed84984c039b2aed6c9778f961d9d93f68e527d7430ddecad8f3a1e6bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155342527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303b5c2e55f983b7ee77545598858abd612b8be35e8f84bd91fd671257dfa9f8`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b98581970ff034bd529aa26ca12985e1754b525da12b09d70af3afd68237dec`  
		Last Modified: Tue, 03 Dec 2024 02:30:12 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad44d7c547c5b4af935adb2d65f110daa2908d5e03b73bf0ab7586b3d9508055`  
		Last Modified: Tue, 03 Dec 2024 02:30:13 GMT  
		Size: 7.7 MB (7680091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56274944153676d0005183f9e215ec98e6e7472eddc5cf21529268cdd42779ac`  
		Last Modified: Tue, 03 Dec 2024 02:30:14 GMT  
		Size: 77.3 MB (77283848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2ce4fc68f42259f450845e7d641d1dacce777d2e5a8e84f4c962ce84b1d317`  
		Last Modified: Tue, 03 Dec 2024 02:30:13 GMT  
		Size: 415.0 KB (414979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3369ef73f7e71d1762b7655789406b41950edaa9d021d59fcbcd99437c9290b1`  
		Last Modified: Tue, 03 Dec 2024 02:30:13 GMT  
		Size: 99.3 KB (99275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2357ef9f7a1531b8f41bbb206494d4830505a15cb69eb5692cd61b76c0e54d`  
		Last Modified: Tue, 03 Dec 2024 02:30:15 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279b904e61f002e3c6e6a1291643a131b5e7baa407204a1b3cd7d0a1b3c93389`  
		Last Modified: Tue, 03 Dec 2024 02:30:16 GMT  
		Size: 41.6 MB (41630870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec70c3c80f6e9ae7f7a2020188828dc2c2126616bf7f67a70f2abc6c5a57e984`  
		Last Modified: Tue, 03 Dec 2024 02:30:14 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:cf1cbbc70dcd900a27e44cbca90120d8ec57695a3ca1d26e28182a6f3edc5b60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3498401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b307ee6fcc8d74c05f3f3c53b8e833866b239892d62ed652b73dc79de86b0c`

```dockerfile
```

-	Layers:
	-	`sha256:6d4feac5f0676816359cf6e4ed69fef2b22e74a88f239b1beda607fb80e24a5a`  
		Last Modified: Tue, 03 Dec 2024 02:30:12 GMT  
		Size: 3.5 MB (3473837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44ddb8926a39928e1bef08870795effae205dc9ba496060f6eed74d82a1799eb`  
		Last Modified: Tue, 03 Dec 2024 02:30:12 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:8942db81adbc28f1fae9ee53f4a75aec44b215f23c8616d47d05f96b44266256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154104676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53f52e3c61a04d822a4a604526aff4b8c10a77108d81b1a53b151b965cd29aaf`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59fa0ff3b45cefb3103f5e899f172aaaa27b2ab60a9d1ef3bd7dd01ff16e12ea`  
		Last Modified: Tue, 03 Dec 2024 05:45:33 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc3470d203ab1a35bfc7d8bd4ef72d9a65e5247ce73ac203185a06bd083e727`  
		Last Modified: Tue, 03 Dec 2024 05:45:34 GMT  
		Size: 7.5 MB (7462106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0401d1709d755f04bcea81d9b5cdd0a77efdd6dde82cf30b47bd5a2def2777`  
		Last Modified: Tue, 03 Dec 2024 05:45:36 GMT  
		Size: 76.6 MB (76584007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13876dd1a77393914e5b20839014d085dde093d4e004822af8a575e9a9745dcc`  
		Last Modified: Tue, 03 Dec 2024 05:45:34 GMT  
		Size: 371.7 KB (371736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52abd970df5381ceaed2fca3ad95b05b97770409f067dacc1bdc3cd75cd66c5`  
		Last Modified: Tue, 03 Dec 2024 05:45:34 GMT  
		Size: 99.3 KB (99279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dabbce0fb524bef360cde9c3f60602e16ec73ffc27d54fe8227c55ec2e54040`  
		Last Modified: Tue, 03 Dec 2024 05:45:35 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a31c70cb72384eecb7996330667c2f809cf7c6b96c8b5d36f375149bf17035`  
		Last Modified: Tue, 03 Dec 2024 05:45:37 GMT  
		Size: 41.5 MB (41526859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72db8ec1b5095f36f5272d4fad08832ccde0655898cf92be98a51ba7ee188173`  
		Last Modified: Tue, 03 Dec 2024 05:45:35 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:3fb399da5c7d605ab9e7206949de7ca3fbd19b93d877a3a7751863f4cf112fb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3497256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a30806cc9d901dc4609e9055d409ae002ea59ef87be6302ed3ca196997535b`

```dockerfile
```

-	Layers:
	-	`sha256:452706c3aca6de462aea88d06e394ea434477af051089d19bb82d900be0e9381`  
		Last Modified: Tue, 03 Dec 2024 05:45:34 GMT  
		Size: 3.5 MB (3472510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5901f02c0f4926d683628766d3eaa00767267e18b39ecc8076d8aee1807951b`  
		Last Modified: Tue, 03 Dec 2024 05:45:33 GMT  
		Size: 24.7 KB (24746 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:78b2608987f018fac2cd4759f3c5f66568433802fbea35b0f2ee4cbf946d5d42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (148967286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1882582f22070e4df3f0856060c2cc693cf367b521c6f911633590a8ce060b72`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
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
	-	`sha256:9378ae44108012049addde60d193467e2b15a247b2f953ad5c27e073c4573d42`  
		Last Modified: Tue, 03 Dec 2024 01:28:18 GMT  
		Size: 26.9 MB (26878971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd2d074f21bdd203a2fd183cffe3e3815c3d9d940d57fed8bc55c74741e400e`  
		Last Modified: Tue, 03 Dec 2024 04:14:04 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354a85114ee6eb212fc2c26419f60433aa0ef174d027d581cf3702301d73f88c`  
		Last Modified: Tue, 03 Dec 2024 04:14:04 GMT  
		Size: 7.2 MB (7194578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1071a9e3021abb79a6c6b4da3028cbb55bc209fabbf7d15d78c44b418261b076`  
		Last Modified: Tue, 03 Dec 2024 04:14:07 GMT  
		Size: 73.1 MB (73064424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ac56c18e58424283065b984082e48f090c2bc9760fc9c888a6bfa2154bb70b`  
		Last Modified: Tue, 03 Dec 2024 04:14:04 GMT  
		Size: 378.1 KB (378058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142d0b872098335016954848d7bb541f1aaa55f65761a42e4530519237a19f0d`  
		Last Modified: Tue, 03 Dec 2024 04:14:05 GMT  
		Size: 99.4 KB (99374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b4ba328975dc41fbbd97e521fa416f0ba61388e06215adac680d504b8c110e`  
		Last Modified: Tue, 03 Dec 2024 04:14:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84c9850d59b3c32b0060fcebf8e5a86123aeccb9f5d4f2ee4dd4d8d35951ead`  
		Last Modified: Tue, 03 Dec 2024 04:14:06 GMT  
		Size: 41.4 MB (41350001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d567022c96a29e59c406eadd309fde18ada5e8c173f57053f873875f8f7930d`  
		Last Modified: Tue, 03 Dec 2024 04:14:06 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:5c691120bc9ec3e23b564749cc4083f48ef2a5e46d50490cab818af0966512a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3491814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0eb85fc081723015864f739973269bec9c437e614167fe8f4094eae370b8a10`

```dockerfile
```

-	Layers:
	-	`sha256:7350fb0515b510d03ca20474209976a6034d8599c0254f86d3077c05b563e25f`  
		Last Modified: Tue, 03 Dec 2024 04:14:04 GMT  
		Size: 3.5 MB (3467250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe5189496a205fc0b5adab44ba885a919654391a96b68ef7f895ffb3cbb91c9e`  
		Last Modified: Tue, 03 Dec 2024 04:14:04 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json
