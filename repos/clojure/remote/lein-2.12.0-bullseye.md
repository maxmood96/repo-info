## `clojure:lein-2.12.0-bullseye`

```console
$ docker pull clojure@sha256:974d0d1e1dc9c75012be4e48b34ab1c6141e2178b4a41ec8e697eec6c962c44e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:lein-2.12.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:232deb545e714f2c40488c5e0da0e5c253075bfc25d4f0fbd4bd6f4802d3ed6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167485673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:367e421458beee6007cde05d3df511bdd3e42f64bb037fc5fbd9777e0466cdb9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:19:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:19:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:19:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:19:01 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:19:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:19:01 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:19:15 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:19:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:19:15 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:19:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:19:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:19:17 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:19:17 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1c662d8f6b122c4f09d6ae1b210df55a5ba6e7b529807c0757ccba0c1ac508e0`  
		Last Modified: Fri, 08 May 2026 18:23:06 GMT  
		Size: 53.8 MB (53763343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1100a9ace8dcbc40a26712ecee68a42394613c9b46b75f051f35098c1ca07482`  
		Last Modified: Fri, 08 May 2026 20:19:36 GMT  
		Size: 92.6 MB (92574572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e5613812cfd641a41e6d67e69c1c75a42b29a1560ae7a39e528a631729dcdb`  
		Last Modified: Fri, 08 May 2026 20:19:34 GMT  
		Size: 16.6 MB (16629587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81431ccb00a4afd644ad912e58a2084f68bef22ccf6c4bacc1df943df0710004`  
		Last Modified: Fri, 08 May 2026 20:19:34 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ec6a131edf189b318ab9a76ae50dd0c631fcdab91cb7a3dac1aa5fc0305a4d`  
		Last Modified: Fri, 08 May 2026 20:19:34 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:5a7490826813a2412bd5771028fddaf339ce17a9b97b850f16eaffd96f557832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4473682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e3a06232c847c092ec5553cb5d0431bee41671bfeb1c9b64c24082b3ed6282`

```dockerfile
```

-	Layers:
	-	`sha256:6a33a7a963f6826650130d6cb053bf4034e7ba96775713a33c9389f9013161d2`  
		Last Modified: Fri, 08 May 2026 20:19:34 GMT  
		Size: 4.5 MB (4454525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88b41e63d01f5185fc1465b0bde175c667634bae1ea585cd2c157fb3303b97f6`  
		Last Modified: Fri, 08 May 2026 20:19:34 GMT  
		Size: 19.2 KB (19157 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b00200dfaa08545b6201d4dad3aa3e9ecc5a4f42a216963415c3f2c8ee07cacf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.9 MB (164930220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8b2d6140ad536d45232bc8214f4056af66aef7cb1bdbbd86d572284bc5e1b0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:23:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:23:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:23:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:23:17 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:23:17 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:23:18 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:23:31 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:23:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:23:31 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:23:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:23:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:23:33 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:23:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec372cebf34e7d29e5bbefb83ba0144c0fa2146cbbd2b693c6ab81b2e16175cd`  
		Last Modified: Fri, 08 May 2026 20:23:51 GMT  
		Size: 91.5 MB (91542294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491c3f96b5fc3f898e620d724e9a035c99fe2d7ef80c816db0bf09228350f809`  
		Last Modified: Fri, 08 May 2026 20:23:50 GMT  
		Size: 16.6 MB (16616536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19031063864965ed2ca9ffd09fdd3524ac9ffa77a4bd307742b4c9e8c142c38f`  
		Last Modified: Fri, 08 May 2026 20:23:49 GMT  
		Size: 4.5 MB (4517751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c95423ae34beb4952ccb7da6b0ad647d582aaf8eb2667f194ae125f7c1ddd0`  
		Last Modified: Fri, 08 May 2026 20:23:49 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:74905a47771acb1874f0f34a6b32611ede768a3ec6b1c231bf770f0cf5560f88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4472822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa98e0544505bad32a2f9d8930aed0ffeb0794516a39d3524d5ee4eb498050c4`

```dockerfile
```

-	Layers:
	-	`sha256:43988e130e8f8f18066265d8af7b3cccd09054122d5257f2800315ca2b033743`  
		Last Modified: Fri, 08 May 2026 20:23:49 GMT  
		Size: 4.5 MB (4453520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76685d844b487e82aceeca910504c39635a4977f9da9624ffd074efadc218de6`  
		Last Modified: Fri, 08 May 2026 20:23:49 GMT  
		Size: 19.3 KB (19302 bytes)  
		MIME: application/vnd.in-toto+json
