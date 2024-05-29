## `clojure:temurin-22-lein`

```console
$ docker pull clojure@sha256:a0d1c0f2954e35e64683eb50fc45c42c96bb9a5e1f079fae76508b17e15ba06d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

### `clojure:temurin-22-lein` - linux; amd64

```console
$ docker pull clojure@sha256:14879340d6ff36d991a5ed2cb0858a6c21284f7534d4a2961061b1543bdd7ee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 MB (230011892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6800d58ea69f47a094d87631a083baf4aaa87d0facf6a84bb4f4124e7cef6ef`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_ROOT=1
# Tue, 28 May 2024 15:17:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a3def59c4f8d3f1625eab8567e011fda2691f6a553d8e2bc3527fa097d80aa`  
		Last Modified: Wed, 29 May 2024 19:58:18 GMT  
		Size: 156.7 MB (156715496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018e25adf6fd61214aea9c5ba525ee0866afb059adbfdc389c56e62b5765fa5e`  
		Last Modified: Wed, 29 May 2024 19:58:16 GMT  
		Size: 19.3 MB (19321470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce769c73ce4091e513710c1214369b3f406ea0be3a6bed8eebbd1c19e1a65f19`  
		Last Modified: Wed, 29 May 2024 19:58:15 GMT  
		Size: 4.4 MB (4398104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e4ba233c9b87aa4c993c42d3e3ee534014906f7df288e933777d44892c624f`  
		Last Modified: Wed, 29 May 2024 19:58:15 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:076b1f59b7498a63bb8f5e08ed4d79b85db50b3cc383fabfa414ee6b6fab0392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3967950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db1104418d7028633ad0535de5815098e2419dad1ba7e4773292d407f583420f`

```dockerfile
```

-	Layers:
	-	`sha256:8034cc1847fe6018abd6c5edae668964ea4fa3a6e0d11e7108b7f99f0823f7a7`  
		Last Modified: Wed, 29 May 2024 19:58:15 GMT  
		Size: 3.9 MB (3949320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:884b30e4f8e620a4634c7e69dec3b02e146a872a919aefc9014875f06ae5305f`  
		Last Modified: Wed, 29 May 2024 19:58:15 GMT  
		Size: 18.6 KB (18630 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-lein` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:68ee36922409126e45a561733ece500b4474949fdb5a81bba91fbd87f7a4b431
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.1 MB (228089226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e668ff1335bfb8524dd446cd7341777ae63c2805f191ffe6611b75bebceeacfa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:32 GMT
ADD file:b7c55dda8ded4219a7cdc9fbd91dfb5996c4886d4394b85751c2f956defe3287 in / 
# Tue, 14 May 2024 00:39:33 GMT
CMD ["bash"]
# Tue, 28 May 2024 19:43:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 20:01:49 GMT
COPY dir:8db4aa7d00469f3c784932412aa95caf68b05146a02559362a91df21ce463ad4 in /opt/java/openjdk 
# Tue, 28 May 2024 20:01:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 20:01:53 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 28 May 2024 20:01:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 28 May 2024 20:01:53 GMT
WORKDIR /tmp
# Tue, 28 May 2024 20:02:08 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 28 May 2024 20:02:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 28 May 2024 20:02:09 GMT
ENV LEIN_ROOT=1
# Tue, 28 May 2024 20:02:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj
# Tue, 28 May 2024 20:02:11 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Tue, 28 May 2024 20:02:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 20:02:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:91e301773f03e9e0fabc5c177fe6bfe8daf14e992ab816f151692b814ddc462c`  
		Last Modified: Tue, 14 May 2024 00:42:35 GMT  
		Size: 49.6 MB (49613388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4f8d9754157e574093fa6b6f43b879df60fea9a7884ed7c7b2a17d7afbedf8`  
		Last Modified: Tue, 28 May 2024 20:21:33 GMT  
		Size: 154.7 MB (154737715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:357310f12b34fd2c5da14b86ab3f8c980570f5a67448e7c13d951c1de8254f2f`  
		Last Modified: Tue, 28 May 2024 20:21:24 GMT  
		Size: 19.3 MB (19339614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39bc99722f2e40c5aa0749bfc9d0c6c827adb29edadf1c1c4da48ba42e7b1596`  
		Last Modified: Tue, 28 May 2024 20:21:23 GMT  
		Size: 4.4 MB (4398109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc3f09f251f6fd3479257372c9b6efc79798fdc47bbdda86fd4dcf56cd6d752e`  
		Last Modified: Tue, 28 May 2024 20:21:22 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
