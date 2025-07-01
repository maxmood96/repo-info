## `clojure:temurin-11-lein-trixie`

```console
$ docker pull clojure@sha256:964a7d943c93fc0a0b57aee3c882e4333e4b8c13f1cd56254c2f98383a084c7b
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

### `clojure:temurin-11-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:9f287530486074032fa024508f6449165cacb176ba6723ca4d9f7b448c8ecf95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.9 MB (265929393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86d4cff1a133acba4f558b9531ca1b8c7972e03179079db42eeb31a6203895d4`
-	Default Command: `["lein","repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:b72fed6e2775feec9291a4bd4b416f996dfc503eda11eaa00def55711302b4ce`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 49.3 MB (49263877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4525ddd3b1b4809613bb25e581220f86b167f9d6a95de80f5f6b7f6bd019fde7`  
		Last Modified: Tue, 01 Jul 2025 02:39:01 GMT  
		Size: 145.6 MB (145635639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8ed794f17da86f71cf2303b9a089b1e53234401554685d36d1561051669c82`  
		Last Modified: Tue, 01 Jul 2025 02:39:54 GMT  
		Size: 66.5 MB (66515703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de297d19106b45b43d36f91c55ea124e26d9f49ad5bfdb93ca2db9451e32fbb`  
		Last Modified: Tue, 01 Jul 2025 02:39:29 GMT  
		Size: 4.5 MB (4514142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9d4de96bbb0bcf84fc95bee61f62a9abc30802a6770889d45234715304f37bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6484467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3fec8f9fbea0dfcc6061ac95e343412940bc0a616bfc2156aefb66a56d66f5e`

```dockerfile
```

-	Layers:
	-	`sha256:684935ccfa043d52b75d3092e491c6a307622dc7017995d4749b730817f7eaca`  
		Last Modified: Tue, 01 Jul 2025 06:35:57 GMT  
		Size: 6.5 MB (6468048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7db038db59caa674134c6498769b6ea3f1afa04384120820fc7b6367532ebaf3`  
		Last Modified: Tue, 01 Jul 2025 06:35:58 GMT  
		Size: 16.4 KB (16419 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9aa3b6dcf9b049199c5f6a5d00b0c2de55bc327a717a81cd450d535499eb970c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.0 MB (263041136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d00d2426917b4da6b4eddad65eb6a1bd2a3876876a9d3052eae371c65cdd037`
-	Default Command: `["lein","repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:546a427a0109bbde3a869c6a4ff1ed90ec74768e7fd82dd00441608d83416632`  
		Last Modified: Tue, 10 Jun 2025 22:52:49 GMT  
		Size: 49.6 MB (49621528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d780a3a01a9b1dea561cdbd6b3757dc17dc751380a900c5d002fde515f87636a`  
		Last Modified: Sat, 14 Jun 2025 09:10:31 GMT  
		Size: 142.4 MB (142420640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec990e752ebe8bf800a373932f7d5dfd93ab2a44ef48a94c3d369ffc5ecd2af`  
		Last Modified: Sat, 14 Jun 2025 09:27:29 GMT  
		Size: 66.5 MB (66484726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e3c432574323b040cbb8983d1227d81b010d9fc0f0e1d769e62f2d0a9d8d15`  
		Last Modified: Fri, 13 Jun 2025 00:40:59 GMT  
		Size: 4.5 MB (4514210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:03bc5004c1a9c23f1f2b174383f7e8aea6b2bcac134a9f42d81f899cffbc600f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6492165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:711d1d4d0f30c31dba14bcbbb63ca08b5a91bd324b6e8b52ad896a055e5807f3`

```dockerfile
```

-	Layers:
	-	`sha256:8962ea783b21da098f0152a6ab3c217b8e53ff6679df117ed6dee7a4e7fc1545`  
		Last Modified: Wed, 11 Jun 2025 09:36:16 GMT  
		Size: 6.5 MB (6475625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03830437d200e8d0b8ee2eac9f92ac864f7de01e101424bd4c269a846dd18630`  
		Last Modified: Wed, 11 Jun 2025 09:36:16 GMT  
		Size: 16.5 KB (16540 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:8d33af077d0e5819e9e13fae3e3f418d88728a48b9aa88346d58b91194b95b6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.9 MB (261943674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc3887b59bd92a780868ff912959e4eb4077eff6e461890dd88f9fc2536d54e`
-	Default Command: `["lein","repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:5c6a246a80c20351fe842a314b6b3f8561a5ceaea736decf36fe380b29e53224`  
		Last Modified: Tue, 01 Jul 2025 01:18:57 GMT  
		Size: 53.1 MB (53097236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85a969def2863a9e85601ef2d4f2e86efa8ff38674c223fec6a8890f4ca131a`  
		Last Modified: Tue, 01 Jul 2025 08:32:36 GMT  
		Size: 132.8 MB (132810557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ea19e210ebeb638eb42bf6bd8ca04743654049831c1f6f5a946518caa10383`  
		Last Modified: Tue, 01 Jul 2025 08:32:49 GMT  
		Size: 71.5 MB (71521667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d3d8266928cc8ba1eb68b99b8e8e108c66ef8d4dbf373644330a7c00ffcb5e`  
		Last Modified: Tue, 01 Jul 2025 08:32:43 GMT  
		Size: 4.5 MB (4514182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4fa99365b01de2d1084d70bb095d5be35ccb9d12433ecd5a227e58a68295aa20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6488004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569c75249ce5efe425e8527692a00ab4bf267ca0f4de84dfdd5293a8b24b6454`

```dockerfile
```

-	Layers:
	-	`sha256:7961bb6e1257e02d9c8ea44bbc10b9d05e5375c3c692473c5a33923cfcb434d0`  
		Last Modified: Tue, 01 Jul 2025 09:36:07 GMT  
		Size: 6.5 MB (6471541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35a1cf72f2f7e1214edbb1d87cf6f63d31b8e8bdc157f389196c6c546d04892e`  
		Last Modified: Tue, 01 Jul 2025 09:36:08 GMT  
		Size: 16.5 KB (16463 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:7bb1199c21b2276fb285a1c151b15feb1739e76c03cb110095cb7cf54f7ca216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.9 MB (246936482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa574e09add40d7d0bb10bd11d7bacef8610654eafbac519d7dc872451a8796`
-	Default Command: `["lein","repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:48de1d8f52c0a2a00375babc11bf69628b8225862d3b6ebbb2205e4ae2f3e96a`  
		Last Modified: Tue, 01 Jul 2025 01:19:00 GMT  
		Size: 49.3 MB (49343660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51563ad6f8cf46e75e2593bfc2fa766379abde52fc9f681453ba8ac4cdcd264`  
		Last Modified: Tue, 01 Jul 2025 08:04:07 GMT  
		Size: 125.6 MB (125585349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11193e56de1d7b263b2f9bf7710728a8b24ee51d7ea9767d0011a920aafbd9fa`  
		Last Modified: Tue, 01 Jul 2025 08:04:04 GMT  
		Size: 67.5 MB (67493227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65cfda55e34e585c91312afa93471f62068d484f6f70aeda3e64c2d64ee7c5d4`  
		Last Modified: Tue, 01 Jul 2025 08:03:59 GMT  
		Size: 4.5 MB (4514214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6ba0f8bdabc49c29facdf54cbcb8c903a57a9e501203a7fa5fdd1847ee208563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6480448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8b77673178757ef733f05026c3702a71f6b45e3e253e9dbe30cc8a16b2849fe`

```dockerfile
```

-	Layers:
	-	`sha256:ea45908ba2c136e1eaddc1fdd6fb4ac4df7c1e97a6e7e6a914d63beb62d9f160`  
		Last Modified: Tue, 01 Jul 2025 09:36:13 GMT  
		Size: 6.5 MB (6464029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58b288b3f61ed38b4141083f9af8537ae80f9fad80b551e44ac31f4e05657ac3`  
		Last Modified: Tue, 01 Jul 2025 09:36:13 GMT  
		Size: 16.4 KB (16419 bytes)  
		MIME: application/vnd.in-toto+json
