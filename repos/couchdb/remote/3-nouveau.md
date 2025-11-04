## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:62892a06582cc1217e9acd9fecfdec72987a0663535b4669eeb6d527c07ea007
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
$ docker pull couchdb@sha256:ba14630b9dad2c142c905ef78d836e2a2b4da23b5111409617461f45f4cfbed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156452722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f64a3eafb3b15d9df4b97709f73460df419e811a21c8ef8431619fcf11bc1a8`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:28:37 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Nov 2025 00:28:37 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 04 Nov 2025 00:28:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:28:51 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:28:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 04 Nov 2025 00:28:54 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Nov 2025 00:28:58 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:28:58 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 04 Nov 2025 00:29:04 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.0~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 04 Nov 2025 00:29:04 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 04 Nov 2025 00:29:04 GMT
VOLUME [/opt/nouveau/data]
# Tue, 04 Nov 2025 00:29:04 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 04 Nov 2025 00:29:04 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d04d9845fcfae593ae1808345251e428ef4fb3c8dd5f936e2446654cd2b276`  
		Last Modified: Tue, 04 Nov 2025 00:29:35 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0506dd93f2a5bc85ebf11a68aeaf5867c2ee4da3388c033286d544826e20ccc3`  
		Last Modified: Tue, 04 Nov 2025 00:29:38 GMT  
		Size: 7.9 MB (7881727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2644b8fa1680ae0db4ec90781ea2109d5e050f351aa461c5cc0cc22132e6407b`  
		Last Modified: Tue, 04 Nov 2025 00:29:45 GMT  
		Size: 77.4 MB (77380720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102078526bd9fb9e43df333c808651969972b027d7eb66c8dd51668ee8a1097b`  
		Last Modified: Tue, 04 Nov 2025 00:29:36 GMT  
		Size: 424.1 KB (424085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6a356dbdef6d588ef7a563556455518fdca30553aa2a94c3d9c895ff04ff33`  
		Last Modified: Tue, 04 Nov 2025 00:29:36 GMT  
		Size: 99.5 KB (99457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded44638d74930968683be2aae1b76ec4cf3ed2decf48ed338ebe322b2a600d0`  
		Last Modified: Tue, 04 Nov 2025 00:29:36 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b195a0de37f8a6313fe015f14ee4d812e2f3879ad65179950f570e1ffc4dd5d3`  
		Last Modified: Tue, 04 Nov 2025 00:29:43 GMT  
		Size: 42.4 MB (42436290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c48c9f3441b02ccdf5cce0efdff38a15396af514fd4a27d9229f4913f911c2`  
		Last Modified: Tue, 04 Nov 2025 00:29:36 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:909d65395179abe79e89f3bec366cdf7f4c4efd475bd4c4ccb8cfbf8cb58a2f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21c3978ba58ac3b5a46b5e03229658606e1b452f418e98a6c4c568d2cca7b7a`

```dockerfile
```

-	Layers:
	-	`sha256:ddf9955211f3b768c9af16b3d291532c4824ced4fbc85599ea5535c6e722bb3e`  
		Last Modified: Tue, 04 Nov 2025 11:33:32 GMT  
		Size: 3.7 MB (3658053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:401aa995221ea5ba3da1571644b255e038ca4ba73a7a873e393aaabe799708d4`  
		Last Modified: Tue, 04 Nov 2025 11:33:33 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:9b87ffe96a19f23609df806fe5d59f941aa3ae2718e83b12900b53c9a43dbf4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155318406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:983a9ddc781a9ce172e99b3bd96a5bee58e893ed58250131b314e1cb6e687007`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:30:39 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 04 Nov 2025 00:30:39 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 04 Nov 2025 00:30:45 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:30:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:30:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 04 Nov 2025 00:30:55 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 04 Nov 2025 00:30:59 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:30:59 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 04 Nov 2025 00:31:06 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.0~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 04 Nov 2025 00:31:06 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 04 Nov 2025 00:31:06 GMT
VOLUME [/opt/nouveau/data]
# Tue, 04 Nov 2025 00:31:06 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 04 Nov 2025 00:31:06 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d877567f4df604047f2eb226f625f3982f2115bb2483d6d9b54c784180f0fa92`  
		Last Modified: Tue, 04 Nov 2025 00:31:36 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4389d9e835eca1b8a7d6fb5a57c30dfaafa356b6861319e0eab3ee2774f07e7`  
		Last Modified: Tue, 04 Nov 2025 00:31:36 GMT  
		Size: 7.7 MB (7692036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eac257402c7ebe43ddf0fdd7dc6aa64da069f70515ce198c8674a629da30c1f`  
		Last Modified: Tue, 04 Nov 2025 00:31:47 GMT  
		Size: 76.7 MB (76691526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6a872f09b98f342372c3aac87e69ad3985bf34255863d62d313794e5a7a8c0`  
		Last Modified: Tue, 04 Nov 2025 00:31:37 GMT  
		Size: 392.7 KB (392688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621a0a38dc0a23e5f952219453939772d44d91fee2698b97ddadd10e51d9e803`  
		Last Modified: Tue, 04 Nov 2025 00:31:36 GMT  
		Size: 99.4 KB (99412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064dd1e307fee62fe335c8689346442ed37b02b4eace00c7948e7d449ca9c724`  
		Last Modified: Tue, 04 Nov 2025 00:31:36 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d722788c47ca1e7eab00963a5546fe2f9ac6be08a16a51beed0c50b10a85368`  
		Last Modified: Tue, 04 Nov 2025 00:31:42 GMT  
		Size: 42.3 MB (42338491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dfaaa9b14c9b02f5bac8c6408e2210c4f8e3fa2f35097de8a33f44a06061754`  
		Last Modified: Tue, 04 Nov 2025 00:31:37 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:68319b39ca1f6a8aeff03f16a32261d92d9b813588f9d89ba56980315b7244ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5767697258fffa5fda2b7790ecec01420248faa53fc27c0cca598875e3354057`

```dockerfile
```

-	Layers:
	-	`sha256:aa4478f273f0982f31978c0f8fe94ca2d1ed57a7fe9c58caee50c37f36cf4064`  
		Last Modified: Tue, 04 Nov 2025 11:33:37 GMT  
		Size: 3.7 MB (3656729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b86d89e8aa3be9f669ace6674a11e46c52bb794e184182dd6113be09aed2971`  
		Last Modified: Tue, 04 Nov 2025 11:33:38 GMT  
		Size: 24.7 KB (24702 bytes)  
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
