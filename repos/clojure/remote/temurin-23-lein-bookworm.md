## `clojure:temurin-23-lein-bookworm`

```console
$ docker pull clojure@sha256:ea5a8cacff0212f0d80478163885c6c4b4c259a77c0269707a90ece9df7865f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:2065ab79a7ccf7e98c4b51cda5d2af412add8ace3857f11e4acd1650a5f32ec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.4 MB (281387432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90e30b6b19bef1c63c7d88f67f97670b5feb2cf4e59b556bc28dcf3daece7a2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:19 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Fri, 27 Sep 2024 04:29:20 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_VERSION=2.11.2
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_ROOT=1
# Thu, 03 Oct 2024 17:49:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9784b681dc81ea7dbfe4d42eb4bc032c73f5ee0058a7e9789044e3f498e716cb`  
		Last Modified: Thu, 03 Oct 2024 19:00:36 GMT  
		Size: 165.3 MB (165267635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5254fad88d40a6867cfb10e8b3b657e6188d1fbba0459c028163f8daba103362`  
		Last Modified: Thu, 03 Oct 2024 19:00:39 GMT  
		Size: 62.1 MB (62050170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3740662341314964c81770d251a4a2f30c76d07fa2d2f536c00f902e4bd2e905`  
		Last Modified: Thu, 03 Oct 2024 19:00:38 GMT  
		Size: 4.5 MB (4514150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f99134b9ece5b12c606b3483ab16e2fba446d8700dc63e6da332d4fb6b415f4`  
		Last Modified: Thu, 03 Oct 2024 19:00:37 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:bb6888fea348b8187e40f02be46ad4941865dd7129ded46a9eb6f2e73c616e73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6545075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad1b0268a9ec30d90a6d25dbc5f33078c32f17370c2aedc615b89dd0ced5a95`

```dockerfile
```

-	Layers:
	-	`sha256:8fbb3762c538c400bcb9df91ebf6dbb66c7946505011d5dd5f9f9288f4862509`  
		Last Modified: Thu, 03 Oct 2024 19:00:38 GMT  
		Size: 6.5 MB (6526378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe6cef4aedb87aac751513c8fd0a028a9c133c743c05007f259e424f3812a5bb`  
		Last Modified: Thu, 03 Oct 2024 19:00:38 GMT  
		Size: 18.7 KB (18697 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:87acfe5c9d43da36e2cec522d37dbd9097fd5d60112792be92258411faf60c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.4 MB (279382557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9a80fa5713702eb6fcfffc2a694afffa3212661caa623067deac1a7d8016d1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:09 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Fri, 27 Sep 2024 04:38:10 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_VERSION=2.11.2
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_ROOT=1
# Thu, 03 Oct 2024 17:49:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd4646320d386687be33160a1cb9db47c711fe0f46f942c4f39ee5d54f71bf8`  
		Last Modified: Thu, 03 Oct 2024 19:00:47 GMT  
		Size: 163.3 MB (163252821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ec4d9128a73b2846c74245133ee499a654f9771ba7dee895d833181b1a56c2`  
		Last Modified: Thu, 03 Oct 2024 19:00:45 GMT  
		Size: 62.0 MB (62030229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76e9251eb26d033097059d204319376b451f649a9cfb8aac50bdec4c0430f1f`  
		Last Modified: Thu, 03 Oct 2024 19:00:44 GMT  
		Size: 4.5 MB (4514193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7244261cd2ba1693a7bb71265819681929622294871b7f2e11cc84468215d6`  
		Last Modified: Thu, 03 Oct 2024 19:00:44 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8a162337447cbe19cc27d44264782280b9872f3bcf56c9f67f4b638cf94eb0f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6550309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5b6109feb22f85b0681264918c70141020f525cc7b9d8a8d8b1bcb6a6e5d6f6`

```dockerfile
```

-	Layers:
	-	`sha256:44ffafeb09b0d7a201747e90c4811b9e5da920c66d647273d5a0678c87e8d6f4`  
		Last Modified: Thu, 03 Oct 2024 19:00:44 GMT  
		Size: 6.5 MB (6531479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0b061862baef93fa78f309408fa15d94c35b1e08a7f7624e9cd99ccd406c0cf`  
		Last Modified: Thu, 03 Oct 2024 19:00:44 GMT  
		Size: 18.8 KB (18830 bytes)  
		MIME: application/vnd.in-toto+json
