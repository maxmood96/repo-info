## `clojure:temurin-17-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:1d270e3340c7d356061d537f36df6796de3e102752ee2b24711e828b8ce7c086
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:717a26a70f48e8e4e1b213e1d14d5d995fddaec1279793c857af65803385c922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.6 MB (222617153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77eadd8215c0898bec69be9d11bc8fec68099d12039a7bba47005850c43efdf5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
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
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
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
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4440d80ddfdc65dbdc71afaa5ca86a749466dbb5b74d5887174ad814a092b6`  
		Last Modified: Wed, 09 Apr 2025 02:18:54 GMT  
		Size: 144.6 MB (144566536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84192075a7123f7a8d7384b32cdb739c5dfe4388d6920d5118b1616c60169c2`  
		Last Modified: Wed, 09 Apr 2025 02:18:52 GMT  
		Size: 43.3 MB (43278561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1292174cc675e3353daee9a098b9ec251865aefd1b2d5e3858a96fd698b323fd`  
		Last Modified: Wed, 09 Apr 2025 02:18:51 GMT  
		Size: 4.5 MB (4514208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a7aa2384df6c14996d3f7636190cbb1477e9baadc2daf57663f108cc73c321`  
		Last Modified: Wed, 09 Apr 2025 02:18:51 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a3601306b9438e3db80044f13487a697151db61ba30de728b013a7d0f276fad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4588572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1550b5fab7e93e7213473be44110705d5493baca0bcf4620265b6816a7d91ca4`

```dockerfile
```

-	Layers:
	-	`sha256:959e1660c0c12bad9150a9e69ff9d3c7e07a2d4c4e22bfbd7e5efdce8e8e54b6`  
		Last Modified: Wed, 09 Apr 2025 02:18:51 GMT  
		Size: 4.6 MB (4570115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1543c394c81ca2c6e3906f04adcfbb78a09e3469c34c0668a0bfa0bc41e654c4`  
		Last Modified: Wed, 09 Apr 2025 02:18:51 GMT  
		Size: 18.5 KB (18457 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:85eafbf9f06536bb7cd6f4b420e10c87490cf496d834d60c889785e013e720f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 MB (220032963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e412d33f8a3c5f0bbb27c13177b318df7b5891e6da1ea4d553dba89c7690f84`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
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
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
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
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdc61d01d3c1907bedb7211a2ec04da2c97e8407d17c661dbb3fccaf3036cfc`  
		Last Modified: Wed, 09 Apr 2025 15:18:21 GMT  
		Size: 143.5 MB (143454624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8c38f767eb4c56058827e5885f47b2e25fcdb42975bd0abbdfef129c560ae2`  
		Last Modified: Wed, 09 Apr 2025 17:32:16 GMT  
		Size: 43.3 MB (43314254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619f4398364d3b3e3dad32534b1d1a23ddddc66fa778cd8bc8acad88e5e50b51`  
		Last Modified: Wed, 09 Apr 2025 17:32:15 GMT  
		Size: 4.5 MB (4514157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97621b4bf89a88338ca74ecddee4ad5be3d991d96c1881ecc7a7617f625e32cc`  
		Last Modified: Wed, 09 Apr 2025 17:32:14 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f481136f14032d29fa29b24d88c2cb8c4bcaa9a81efd9d6fbaf5b19beedbd79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4594358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac056ea10c75c025666cbe3b36ac1cddde5b8f6a4c369dd8fd8bd8164d7e8e0`

```dockerfile
```

-	Layers:
	-	`sha256:6b5048235b7d6702360d13db8553e758eb642a9586a2e275d26ef5debc781950`  
		Last Modified: Wed, 09 Apr 2025 17:32:15 GMT  
		Size: 4.6 MB (4575779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c79f4efe0438a6f5d1115148aa93993dd29b05b4fe0144a94f18129c38a7ed86`  
		Last Modified: Wed, 09 Apr 2025 17:32:14 GMT  
		Size: 18.6 KB (18579 bytes)  
		MIME: application/vnd.in-toto+json
