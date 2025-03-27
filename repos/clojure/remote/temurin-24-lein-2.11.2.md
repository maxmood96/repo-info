## `clojure:temurin-24-lein-2.11.2`

```console
$ docker pull clojure@sha256:4cc94ea1bfb4640e285e3f7d19f7d40f4a05ae5d5eccc4519f9eb598a8f53325
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-lein-2.11.2` - linux; amd64

```console
$ docker pull clojure@sha256:52af4c0049edbd0e957f463416e72506858546c406efb541de4e536381fd7bd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (204995228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8b3236932a7177261d2fdb20a344ff6dcfff0460db3ff4a38d0b6db0d5cdd2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_ROOT=1
# Wed, 26 Mar 2025 16:17:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7cd785773db44407e20a679ce5439222e505475eed5b99f1910eb2cda51729ab`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.5 MB (48467838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1331ccb5110c1f1a1136c66bd6c574898c3c34f8e94f27c996b5beed83d27fc3`  
		Last Modified: Thu, 27 Mar 2025 17:53:35 GMT  
		Size: 89.9 MB (89949053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d698d0131f32814c9bf16ecc83b8bf1ff63b8b17b52a8e11b867abe2236fa717`  
		Last Modified: Thu, 27 Mar 2025 17:53:34 GMT  
		Size: 62.1 MB (62063758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cc35cb6af3d63cf3de2daebe2b00fa8c8fae70f4c9295d43ff6f952481d86c`  
		Last Modified: Thu, 27 Mar 2025 17:53:33 GMT  
		Size: 4.5 MB (4514149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ad0a589e8373270ab3398e76177db7029f0110b3e56ccb95ce2f847cdaef9d`  
		Last Modified: Thu, 27 Mar 2025 17:53:33 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-2.11.2` - unknown; unknown

```console
$ docker pull clojure@sha256:cad3ba8c4f8b22919a47e0219aad6c9003fea0c42d426d0c6fbf145dc1d6fa16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6504622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cc7f1cfe15f78dfdc38fd13092380d567c45de03f63d9ead89fbc648ed26f90`

```dockerfile
```

-	Layers:
	-	`sha256:3973af195cf08e9f91defba13570182c5a36e6f9b176a70c05e1de76d293aeb7`  
		Last Modified: Thu, 27 Mar 2025 17:53:33 GMT  
		Size: 6.5 MB (6485557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3550baeeb3b02caf9e143356ded1ac3fdfab3566fed03bfc59a8376c974f9a51`  
		Last Modified: Thu, 27 Mar 2025 17:53:33 GMT  
		Size: 19.1 KB (19065 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein-2.11.2` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:20c879812b6cdac76665de2c761678afa46d1ab5f4ad1cbc5e508477ca173cdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.9 MB (203949475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb457a81e754460e4444a204b1a8ce5578f65b1d73c2002bc41aa406e58f68f1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_ROOT=1
# Wed, 26 Mar 2025 16:17:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32f1d4584a0aa49d6c0f2a0d382f28e60f4fc57ebb8548010197c1a8c2e0418`  
		Last Modified: Thu, 27 Mar 2025 17:53:16 GMT  
		Size: 89.1 MB (89092702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fde553ad6587f93b17d85aeac55a0ce2588a0690076b0c8fa32da97afebaedb`  
		Last Modified: Thu, 27 Mar 2025 17:53:15 GMT  
		Size: 62.0 MB (62037302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146ceac137cf3a1a3359378670d27469f7b534d34405824dfa01a31acff1de16`  
		Last Modified: Thu, 27 Mar 2025 17:53:13 GMT  
		Size: 4.5 MB (4514187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2380bc6bc38217d9639c8d03fc6f055636dd143f663c374715c6caf471389b`  
		Last Modified: Thu, 27 Mar 2025 17:53:13 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-2.11.2` - unknown; unknown

```console
$ docker pull clojure@sha256:020b3c6b01079ad62afae4ae86a7a86659e9e3d8fa7e054016eaa11f3fee8b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6510481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c89fb0ecb3dbad70d4c5969bb2a48cec36ce26eb201c1286bd71ea64c4eb0a19`

```dockerfile
```

-	Layers:
	-	`sha256:94366e0d12f8c4565e2da74073186002db1e059cfb1a36b3bff83c2c5cfed5c1`  
		Last Modified: Thu, 27 Mar 2025 17:53:13 GMT  
		Size: 6.5 MB (6491272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:533a930b89aff6cecc3032983aacf720cf9daee0351183081bf8e9aceccb45a9`  
		Last Modified: Thu, 27 Mar 2025 17:53:13 GMT  
		Size: 19.2 KB (19209 bytes)  
		MIME: application/vnd.in-toto+json
