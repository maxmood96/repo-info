## `clojure:lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:751daeed41fbe416d0f697c401685987ddaf032d6a3699da9a5634a39624b457
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:lein-2.12.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:061352188b95c863bf107963cb4f54bf39269a278ed93a8060801f22d3cae51c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.4 MB (164432606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4e84e9114db84e2567e81f3268b6706c62d2287448ba4c238b0de7b0af79f0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:56:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:56:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:56:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:56:21 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 08 Dec 2025 23:56:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 08 Dec 2025 23:56:21 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:56:39 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 08 Dec 2025 23:56:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 08 Dec 2025 23:56:39 GMT
ENV LEIN_ROOT=1
# Mon, 08 Dec 2025 23:56:41 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 08 Dec 2025 23:56:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 23:56:41 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 23:56:41 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2981f7e8980b9f4b6605026e1c5f99b4971ebba15f626e46904554de09f324f4`  
		Last Modified: Mon, 08 Dec 2025 22:17:46 GMT  
		Size: 49.3 MB (49289520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67dfbc97782bb4ef5510715f43433bb0a8145e3caa8d14c9d55f353cb09197b0`  
		Last Modified: Mon, 08 Dec 2025 23:57:12 GMT  
		Size: 92.0 MB (92045289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7496780c46a8b1c45c45913b9599bb3e20f17e2ab2177d1bbea134d007c6174a`  
		Last Modified: Mon, 08 Dec 2025 23:57:04 GMT  
		Size: 18.6 MB (18579626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3542c124ff0fa2dad100ddf83daa43639f31557744a962dfbce30677543378`  
		Last Modified: Mon, 08 Dec 2025 23:57:02 GMT  
		Size: 4.5 MB (4517743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6eb0eae1f2cd85f9c568d6f1f5b5b29457a64d7ec6efcb8cb66261c55674d9`  
		Last Modified: Mon, 08 Dec 2025 23:57:02 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:13092e19f031a7eaf7c31832c7b88eabefc73cad26d517fc1a6e0d726f3b2a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3783655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9454c1ae516e03a1f3cb663dababb8d30ae52830b19abc85017c413aaa4d0017`

```dockerfile
```

-	Layers:
	-	`sha256:cd326f1b5957670be91e087d9f537e7da3288205dd7d1593c06e9cdabdfc3f52`  
		Last Modified: Tue, 09 Dec 2025 04:35:27 GMT  
		Size: 3.8 MB (3764676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4680877aa8a6e028af32f8a75131d1db47f9870409ea60b002aad02193e9bce7`  
		Last Modified: Tue, 09 Dec 2025 04:35:28 GMT  
		Size: 19.0 KB (18979 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:349e10acff26c8f4c4de8ecf222ce39394eb799f007a6791977d51e7cf901ed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.8 MB (163761529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60e92bacaf608b4c74d42b8da77f2b8cb419c4855ff40a1824760891a4117239`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:03:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 00:03:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 00:03:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:03:34 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 09 Dec 2025 00:03:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 09 Dec 2025 00:03:34 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 00:03:50 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 09 Dec 2025 00:03:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 09 Dec 2025 00:03:50 GMT
ENV LEIN_ROOT=1
# Tue, 09 Dec 2025 00:03:51 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 09 Dec 2025 00:03:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 00:03:51 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 00:03:51 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6a828f739420ec96bad6123094a07f3f234998f6cf772e34e0ba733aa8e2b347`  
		Last Modified: Mon, 08 Dec 2025 22:17:28 GMT  
		Size: 49.7 MB (49650226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ded3e94cebf7c49c4b3114eccb4f0e5700860cf7718bf8bb46ff7cfad8c753`  
		Last Modified: Tue, 09 Dec 2025 00:04:26 GMT  
		Size: 91.1 MB (91052515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10d4ddd291ef32e620d512c7aa74b85ed56e52ba5273e2c1f884dea5e6107ff`  
		Last Modified: Tue, 09 Dec 2025 00:04:18 GMT  
		Size: 18.5 MB (18540648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f32b891aad765c8fb8db347922d87ca92c67c1c3f91a915676420e88f0ad78`  
		Last Modified: Tue, 09 Dec 2025 00:04:17 GMT  
		Size: 4.5 MB (4517713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7de20cec84fc848d32c1ec60878a77cf99da22182a66f2748d7ecaaa6a50a06`  
		Last Modified: Tue, 09 Dec 2025 00:04:17 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f1ef0ec8434e3c10ae4b77daf7d0c89648bfb452ea0489ab9df9693af2e37259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739e0461b7006d4b1d736874170c914795b358a82297d5d3e64215eab6fb7be1`

```dockerfile
```

-	Layers:
	-	`sha256:08f5853ce6aec7ea76da07792141f8aca47f9ec11c068160936257902530642c`  
		Last Modified: Tue, 09 Dec 2025 04:35:32 GMT  
		Size: 3.8 MB (3765574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b38fc4dfa872d5848f4cd88bb73d5ce0344dfad44d9ad442a3a5a942724e548`  
		Last Modified: Tue, 09 Dec 2025 04:35:33 GMT  
		Size: 19.1 KB (19124 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:dfbdb39e93080809f7649f501b8e3a16632a2ac32c001aa81c25406114fa767d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.9 MB (167874391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8cec03c916c4606cef348c0f89f4b5e05815860409a729b54131be00ecce9c0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:32:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:32:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:32:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:32:22 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 08 Dec 2025 23:32:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 08 Dec 2025 23:32:23 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:32:59 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 08 Dec 2025 23:32:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 08 Dec 2025 23:32:59 GMT
ENV LEIN_ROOT=1
# Mon, 08 Dec 2025 23:33:03 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 08 Dec 2025 23:33:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 23:33:03 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 23:33:03 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:fb00391cdf4b5dc5fe2e67e0bee3770076e9af9efed48ba15cb306902e36c78c`  
		Last Modified: Mon, 08 Dec 2025 22:52:23 GMT  
		Size: 53.1 MB (53108478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe3513d576a2d4d2badd58f02126058233abf53aea816262c3b7f313a199d32`  
		Last Modified: Mon, 08 Dec 2025 23:34:05 GMT  
		Size: 91.6 MB (91610745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c064ef854103108d83a9ae52a541816f78b57be63c6013a782fd1fb6cfb5d1e`  
		Last Modified: Mon, 08 Dec 2025 23:33:59 GMT  
		Size: 18.6 MB (18636980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dab2bed772505ca5c1244fce5f8fd0305aa95dc1211041086ee2249481eda9d`  
		Last Modified: Mon, 08 Dec 2025 23:33:56 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf073c5fd283726ad3c6a2c6ec0622260bf0795410e15ba25360e11de790251`  
		Last Modified: Mon, 08 Dec 2025 23:33:56 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:eaaa5ecc07c96acccc65a5cf39692f6be06db5e62d110150205f5430061c68bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3786019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248332e4858b43a0f68270568262db02b5574c66fd0216eb2debaebebc8732e8`

```dockerfile
```

-	Layers:
	-	`sha256:2c53f932aee35c19b6bad803559fbe3873587344ed3f2e1c3472501aac4e2dab`  
		Last Modified: Tue, 09 Dec 2025 01:35:08 GMT  
		Size: 3.8 MB (3766984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8a577328e35352062b6d1fd57841894b66717d321a1ace3dfd8ce0f468e0ea9`  
		Last Modified: Tue, 09 Dec 2025 01:35:08 GMT  
		Size: 19.0 KB (19035 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:4ce46e71633c2c6d1ebe99802e724b59d87dfecdb8cf492c09e26556ba57bbf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161573968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dea8bf6ac389362b63b559a9b1b8c141464d14f0085f737cde7afe0c4f5cdd7e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Sat, 13 Dec 2025 19:08:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 13 Dec 2025 19:08:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 13 Dec 2025 19:08:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Dec 2025 19:08:58 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 13 Dec 2025 19:08:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 13 Dec 2025 19:08:58 GMT
WORKDIR /tmp
# Sat, 13 Dec 2025 19:10:29 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 13 Dec 2025 19:10:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 13 Dec 2025 19:10:29 GMT
ENV LEIN_ROOT=1
# Sat, 13 Dec 2025 19:10:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 13 Dec 2025 19:10:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 13 Dec 2025 19:10:45 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 13 Dec 2025 19:10:45 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e8961870af39130e72e5dc66bd3574bb074dffc7989fd5e909f55fefadae8a30`  
		Last Modified: Tue, 09 Dec 2025 02:05:05 GMT  
		Size: 47.8 MB (47771135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e7a81485ab6b126c740ed6e6342f4229b7a854be769f1f6488cea63fad4ccc`  
		Last Modified: Sat, 13 Dec 2025 19:14:48 GMT  
		Size: 90.8 MB (90752902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ee7f0cd4b7ec5b54511c33f297e076335a395a58b58baa99b3ed4247ea6f56`  
		Last Modified: Sat, 13 Dec 2025 19:14:40 GMT  
		Size: 18.5 MB (18531715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc8a2d0c366f0d803ceaf00ebc9aaca05d5ba4a1167f118e9cdf3dd68a0a395`  
		Last Modified: Sat, 13 Dec 2025 19:14:39 GMT  
		Size: 4.5 MB (4517785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfeedf80562237ed0f2b0daca668a048e0c742829ad4307a08998e366881330`  
		Last Modified: Sat, 13 Dec 2025 19:14:38 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c366f23e5d509ea29615c58f4a6f6f0083830e3d081e0ca374cd139f557a6032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b3e074e60a0a0ab3b90a639527e2e84fe22e0d182177777756719a3225dbee0`

```dockerfile
```

-	Layers:
	-	`sha256:f3df6610dddf019db643622c8fd87b96d1b5580c0aec7a3b6f9d0385199a6551`  
		Last Modified: Sat, 13 Dec 2025 22:34:37 GMT  
		Size: 3.8 MB (3755160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b77e31d924141965d71a11408b3075c2476fb2f066403b7553875f5376248118`  
		Last Modified: Sat, 13 Dec 2025 22:34:37 GMT  
		Size: 19.0 KB (19035 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:ff08ee63407ba1cd7203669fbccf58a83133f4f7254f90c51fd4854706ffd16a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160695443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbba5576adf5a36d8aedb3517a373f2a987e90860b645e6037c9b251eef74b46`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 01:33:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 01:33:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 01:33:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:33:33 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 09 Dec 2025 01:33:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 09 Dec 2025 01:33:33 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 01:33:47 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 09 Dec 2025 01:33:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 09 Dec 2025 01:33:47 GMT
ENV LEIN_ROOT=1
# Tue, 09 Dec 2025 01:33:49 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 09 Dec 2025 01:33:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 01:33:49 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 01:33:49 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3f8967bef2f6a8ec916f7d3a0d528a6724093176621c5758addeeece50e41dec`  
		Last Modified: Mon, 08 Dec 2025 22:16:15 GMT  
		Size: 49.3 MB (49345908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561af1fd1f572f4dbfb628c0a027acc23b1d8a0d6465efff545b43e36426f3e6`  
		Last Modified: Tue, 09 Dec 2025 01:34:33 GMT  
		Size: 88.2 MB (88210717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e02da8ac4c8f6d0d286e414ee3e14da8f79625da1e3ddf6f898c1a0f2ac671a`  
		Last Modified: Tue, 09 Dec 2025 01:34:24 GMT  
		Size: 18.6 MB (18620638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d1d1173d764a5f06f84884dcb10f8558dccafafbc07acc8aa4e09af3137b5a`  
		Last Modified: Tue, 09 Dec 2025 01:34:23 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcdb5e17ebf5df584356ee9e155132c5b0f2c4b194260fd7215c77283bbc5b80`  
		Last Modified: Tue, 09 Dec 2025 01:34:23 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:750e758330c56aba588f45c1337e4a2f7be85ca296d468a64c5c70d77dc00ff1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3782630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e9c68b3d860968944c1ee588501b619fe44286e48a06276e5e8ead4467c6f49`

```dockerfile
```

-	Layers:
	-	`sha256:88bde6bedbc7d509a7e9e4f329eabf3be7c5b31f7e0862bb1909c65c886421dc`  
		Last Modified: Tue, 09 Dec 2025 04:35:43 GMT  
		Size: 3.8 MB (3763651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55d8e5e2faea10025d2b9d0c2f38de270568daecb88d0150e6355d0f7e3ed6d6`  
		Last Modified: Tue, 09 Dec 2025 04:35:43 GMT  
		Size: 19.0 KB (18979 bytes)  
		MIME: application/vnd.in-toto+json
