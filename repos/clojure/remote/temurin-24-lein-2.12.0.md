## `clojure:temurin-24-lein-2.12.0`

```console
$ docker pull clojure@sha256:0abbc862f582c34e12ea1e0b90b9c18b4f95f54cd60c99c91ff493c5fee6f3c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-24-lein-2.12.0` - linux; amd64

```console
$ docker pull clojure@sha256:a335232bda33f988f2692b1c3fac76ebfa9ba93b0f5dd95293c66eec392ae5cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.8 MB (162773901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8d38d4a479c0b54726cdb3403ffcad8d42d66a23c9356310fd82db38dea4ce7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e270b91fc58d47e2bfbc5e8671ca695eb69147e8bcd0a0a55cbd165f48ebd768`  
		Last Modified: Sat, 13 Sep 2025 00:10:59 GMT  
		Size: 90.0 MB (89975233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2622de2a2f6bdd133e358970b6c0b3862fff98b25293e54389e96c9ceb9841`  
		Last Modified: Sat, 13 Sep 2025 00:10:50 GMT  
		Size: 19.8 MB (19799915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199d7aabd6111dc4a894b4ac0d20198f493569f9e3e702a0cc25d15e3380e96d`  
		Last Modified: Sat, 13 Sep 2025 00:10:50 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cbc99ec2164484189674774293a7a33720138c1f31174a1e89e156e7ecb3f8`  
		Last Modified: Sat, 13 Sep 2025 00:10:49 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-2.12.0` - unknown; unknown

```console
$ docker pull clojure@sha256:68a15f8c449e256b7991259807313b0e2e4c6b5dec280f2f6c3e6fde67e0781f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4250184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8631efd745b77731a890ffb3dfc5894ed6b404de72259fad43127b01181e38d6`

```dockerfile
```

-	Layers:
	-	`sha256:102b466f5c76348e741c47e0ee80de9bf2c514d107be938d46e3297902378b06`  
		Last Modified: Sat, 13 Sep 2025 00:41:52 GMT  
		Size: 4.2 MB (4231132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3f621d99bc2b59ea44220f06baeee65f0fe2518caf20a1653ac511fd43a66db`  
		Last Modified: Sat, 13 Sep 2025 00:41:53 GMT  
		Size: 19.1 KB (19052 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein-2.12.0` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ded45b32539e4e2f67e92b96b89f768de6b8659b8143614ebb725467c20e437c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161598447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f192be09f44050d24d0c75769a5193b5177d313e30ca450f84722019d5a82ec`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912388ad7a0726fd6e3d60ab58c85a57d937ca58e038e6da3e3ddca40ebc3fa4`  
		Last Modified: Sat, 13 Sep 2025 00:16:46 GMT  
		Size: 89.1 MB (89092551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0c7dd8f2d55b350fd67c6ff032f1e93b8e32383db5de499e8606a3e8ce06fa`  
		Last Modified: Sat, 13 Sep 2025 00:16:38 GMT  
		Size: 19.6 MB (19628704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55dd6d9f527513314962962adbbdc7f7ef3a6cc44fbab8c00c4ebc753223290`  
		Last Modified: Sat, 13 Sep 2025 00:16:37 GMT  
		Size: 4.5 MB (4517743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dded61bc75d406a3879c493fb52c552f406610881d5a94defe53a2e6157f696`  
		Last Modified: Sat, 13 Sep 2025 00:16:37 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-2.12.0` - unknown; unknown

```console
$ docker pull clojure@sha256:9c4a51af030c5869e39f1c63dd4996c69f4b29d7deafd737f129efadaaec7889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4249967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c699e5906d21184779a702f9265c1f9c6ebc65254da357e9ed1d2521f13b68`

```dockerfile
```

-	Layers:
	-	`sha256:020c9813b7d49fb409f52c414034fd572489697c5043682375682adb7fb8ab83`  
		Last Modified: Sat, 13 Sep 2025 03:40:10 GMT  
		Size: 4.2 MB (4230768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e46719aa7e0c5f8d9283ca2f0e5ee3708342237466ad0f40b9766791c24e3c00`  
		Last Modified: Sat, 13 Sep 2025 03:40:11 GMT  
		Size: 19.2 KB (19199 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein-2.12.0` - linux; ppc64le

```console
$ docker pull clojure@sha256:58dc3ba55aa8a5dcef2890f586cbe9d0d7271ea6d6bdb22e51782d4ff9cc7c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166782086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a1e2fa1c184f802d4a818414a461a1378ed7111f64c4e9a4f44fe9d0ae111f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:64b8116dd43c29a2a4aa3131cb4895af0a7267cc5883e3761556e54c369be9af`  
		Last Modified: Mon, 08 Sep 2025 21:22:08 GMT  
		Size: 52.3 MB (52326822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86172f15372b948e9acf8523414dcea949da4bf6c2e68bc45159e62ddfee9e65`  
		Last Modified: Sat, 13 Sep 2025 03:50:01 GMT  
		Size: 89.9 MB (89918193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce460708a68b774dbfc92194e99eeb64a0630abc10d6cf2943c50013f2100c4e`  
		Last Modified: Sat, 13 Sep 2025 03:49:56 GMT  
		Size: 20.0 MB (20018899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a44cedbf857430e9cbb01c877d807a28dfa45ba7eaa0fe60e79e8ba5c4fe533`  
		Last Modified: Sat, 13 Sep 2025 03:49:55 GMT  
		Size: 4.5 MB (4517743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09dfcd114cafa04d8b3210e383d3af1713df269f0e9f5c3ee8c25cd89a3637ab`  
		Last Modified: Sat, 13 Sep 2025 03:49:55 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-2.12.0` - unknown; unknown

```console
$ docker pull clojure@sha256:243bae58f59f0813b08777c9c6912b69f7d8305b61f3d9bdd83b9b951921e56e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4253411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35c842d3817df71a9399fd758a7d0b47a2138884e5c2a19654195365b972290c`

```dockerfile
```

-	Layers:
	-	`sha256:0a1440afd46633d2444c535dc9ae69aec59abac07cd3de4b5e8863c8f10c0c02`  
		Last Modified: Sat, 13 Sep 2025 06:39:33 GMT  
		Size: 4.2 MB (4234301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18b0b1d2fd874002998b799ff9b5138406ffa963c02213938d056fc0fd992ec0`  
		Last Modified: Sat, 13 Sep 2025 06:39:34 GMT  
		Size: 19.1 KB (19110 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein-2.12.0` - linux; s390x

```console
$ docker pull clojure@sha256:9156373cbbde99c1a78e27d757a70da2826f8cd7b96dea535f0931ee20e6220f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.3 MB (156340780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c8cd139e42fd45e90510fee91492b9f699a36c75f31bd9c76171fb7f71472f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:67e2d91fae4fd9af13e4e364bf8120dcca7856e8273995cc0651acae70b27e8e`  
		Last Modified: Mon, 08 Sep 2025 21:18:01 GMT  
		Size: 47.1 MB (47137539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a194a3e86b38170126e14a8a4967e24dd619d46e1914dcccc96f552585ef697`  
		Last Modified: Sat, 13 Sep 2025 00:02:32 GMT  
		Size: 85.2 MB (85226409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc7f98252ddbbe9ce0a554cccae922c275a91c9bc607e80bf734f73a2b46c1d`  
		Last Modified: Sat, 13 Sep 2025 03:17:38 GMT  
		Size: 19.5 MB (19458699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2429fd5de59dc3a94badf917dcd48456691afaf99e673927924be2725e4c52c8`  
		Last Modified: Sat, 13 Sep 2025 03:17:37 GMT  
		Size: 4.5 MB (4517706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254d679e43a16ce1a5e0094a796e699998f5856219050e0563aa0daaeff14805`  
		Last Modified: Sat, 13 Sep 2025 03:17:37 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-2.12.0` - unknown; unknown

```console
$ docker pull clojure@sha256:2443693255efda898924e0acca91fe800c6439bbfe88ce851da21c42e55d9651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4244548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20b521390aeb526a7ef22b498b4f3f22d32a8518099329a2b0a0fd60c1735881`

```dockerfile
```

-	Layers:
	-	`sha256:d0c4d319c82a85983594feda62c1091a957df331cbe95c17936810124558237f`  
		Last Modified: Sat, 13 Sep 2025 06:39:38 GMT  
		Size: 4.2 MB (4225494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a829d778511703b8aa3e975ef5dff8b4402adfb1d6fd461ff4a42a8ba838c09`  
		Last Modified: Sat, 13 Sep 2025 06:39:38 GMT  
		Size: 19.1 KB (19054 bytes)  
		MIME: application/vnd.in-toto+json
