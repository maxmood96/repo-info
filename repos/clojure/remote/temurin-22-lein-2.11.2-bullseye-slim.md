## `clojure:temurin-22-lein-2.11.2-bullseye-slim`

```console
$ docker pull clojure@sha256:7250de704e6097671fbdae8a7c7fd623e891882c6d1655043a7d955860f4aace
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-lein-2.11.2-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6311a5d3130d768ce209a9f31815792bbc1f4a416465471d16e2193ae0876368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235446184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:458e001b131277833bfc5aeedf616b890f4154e06eacd71445e8d906a80eb565`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_ROOT=1
# Wed, 07 Aug 2024 18:04:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283eea0701513305f2815579e5b6de979e8daf039986de743a5b1f555efe33d4`  
		Last Modified: Tue, 13 Aug 2024 01:11:39 GMT  
		Size: 156.5 MB (156481636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd601be371f71e025c5472a9a033bb24eaacb26aec9a0028fe06c83598039978`  
		Last Modified: Tue, 13 Aug 2024 01:11:38 GMT  
		Size: 43.1 MB (43137795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4d1c601cc106ff1a30f45a3cd16b728952f8c1aea0cfbb109d6f10962a5110`  
		Last Modified: Tue, 13 Aug 2024 01:11:37 GMT  
		Size: 4.4 MB (4398037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdfb0cd33dd315574741a916c3ad3a7f52f6b3c9312c73e636b5878406f0378a`  
		Last Modified: Tue, 13 Aug 2024 01:11:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-lein-2.11.2-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e0b090ab57e63c8584a2159bca605e68c9113c2eea429a6451e1ce5fd266f25a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4419172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab8bffd1b0ac5aa802a3cf86a4093baab0508c23b9d9da389140edd003fa2e6`

```dockerfile
```

-	Layers:
	-	`sha256:af28bd68c9d977888a1261b9826b79ac891eb76c56b064718761ab11430cd114`  
		Last Modified: Tue, 13 Aug 2024 01:11:37 GMT  
		Size: 4.4 MB (4401080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2d78bc96c4ebecb94d88c643c0051959f76285e139ad68d31d5121fd09754d9`  
		Last Modified: Tue, 13 Aug 2024 01:11:37 GMT  
		Size: 18.1 KB (18092 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-lein-2.11.2-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4cf8cd31230df753d6054a21c4d1c152b616bc4f7a386dbfdf46017acdd01df7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232135747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:216ddf89c1c355b6b4cf9251c20aa56c8ba29ff16bbe7ad6f52849cd8703072e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jul 2024 04:18:06 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Tue, 23 Jul 2024 04:18:07 GMT
CMD ["bash"]
# Thu, 25 Jul 2024 20:19:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jul 2024 20:19:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jul 2024 20:19:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jul 2024 20:19:09 GMT
ENV LEIN_VERSION=2.11.2
# Thu, 25 Jul 2024 20:19:09 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 25 Jul 2024 20:19:09 GMT
WORKDIR /tmp
# Thu, 25 Jul 2024 20:19:09 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 25 Jul 2024 20:19:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 25 Jul 2024 20:19:09 GMT
ENV LEIN_ROOT=1
# Thu, 25 Jul 2024 20:19:09 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 25 Jul 2024 20:19:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 25 Jul 2024 20:19:09 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 25 Jul 2024 20:19:09 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3578437e84830a360777bae87ddcde03bf7d0e3d58f2b9884bb3105e4bf361b2`  
		Last Modified: Thu, 25 Jul 2024 21:30:07 GMT  
		Size: 154.5 MB (154503703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f37e66df6c205d6e7b653c4a4a8c8f905187f0ad744c8e35ea92f9972539723`  
		Last Modified: Thu, 25 Jul 2024 21:30:05 GMT  
		Size: 43.2 MB (43157481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef6fa461af6584ab905e443a8c98fdd9e71b45a19cb85ed3024a58e55854875`  
		Last Modified: Thu, 25 Jul 2024 21:30:04 GMT  
		Size: 4.4 MB (4398050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6ea50a92cb54ba1d2472e1aa3c507cfd047fe72517658960b6fb985b7d595f`  
		Last Modified: Thu, 25 Jul 2024 21:30:04 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-lein-2.11.2-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ee027ac754d7227d93ac303c59b2fc20076899ab76babe360104ca03ddbbac1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4425998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e85b35fc1bc622443ad106ae916823fe1e7a0c2024c1fb5129a78659b37ace2a`

```dockerfile
```

-	Layers:
	-	`sha256:051af64cc83a6cedf50a31528a3d4792a567d1aa8314adb83d31b72bcf8c81b9`  
		Last Modified: Thu, 25 Jul 2024 21:30:04 GMT  
		Size: 4.4 MB (4407378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be1f5a9bce914981345ec2caedea62ac4d432fa32c04150e9741a0bdd08f2737`  
		Last Modified: Thu, 25 Jul 2024 21:30:04 GMT  
		Size: 18.6 KB (18620 bytes)  
		MIME: application/vnd.in-toto+json
