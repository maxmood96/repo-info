## `clojure:temurin-22-lein-2.11.2-bullseye-slim`

```console
$ docker pull clojure@sha256:d944d04b2d58b90c45aba04ec749d3b3c3cc76fbf97f0973eb6f5cfee5b32937
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-lein-2.11.2-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0072f7e7cd06901b4c887928d69721f5d8cef97c5cf53bb1945b84e1938508bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235685034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0fd8120742f536c85b18194dbe7c12ee15f8dcb52f4297c23d3bc66593c64a1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 04 Sep 2024 22:31:09 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Wed, 04 Sep 2024 22:31:09 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV LEIN_VERSION=2.11.2
# Fri, 06 Sep 2024 16:59:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 06 Sep 2024 16:59:26 GMT
ENV LEIN_ROOT=1
# Fri, 06 Sep 2024 16:59:26 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f6c29c4ea598c3e9e0162aa1162c954a77be00423bf0f347267585eebbd216`  
		Last Modified: Tue, 17 Sep 2024 01:59:08 GMT  
		Size: 156.5 MB (156481658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8863540121ec444f97bf355ffa966d7dbc71929de06a3cf583f30ebc9ba767c5`  
		Last Modified: Tue, 17 Sep 2024 01:59:05 GMT  
		Size: 43.3 MB (43260130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b250218a82f3db5c83db26b89b00cbd1e81d73867906ad840cc80d14184e0d`  
		Last Modified: Tue, 17 Sep 2024 01:59:04 GMT  
		Size: 4.5 MB (4514139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfb1b4da0edafef03f3248038d88d761f1f8bcb398712fc9f32caaa6a7ec54b`  
		Last Modified: Tue, 17 Sep 2024 01:59:03 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-lein-2.11.2-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b5a86b16d370809ec6e53a8115feb0052eec3a3436cf6a9dda0fe321005e5877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4420338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f7e3f9091a798ca49df8bb1b212ad83af2effad374571df96b820111964258`

```dockerfile
```

-	Layers:
	-	`sha256:01787cd937c0c34830acb074b25e13102eb08613cbd6756631863c7af09b594a`  
		Last Modified: Tue, 17 Sep 2024 01:59:04 GMT  
		Size: 4.4 MB (4402246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:233c0ffe360ea12bee369593438b5b63dfa0e9194375b8f02d06812a2f9e3b6e`  
		Last Modified: Tue, 17 Sep 2024 01:59:04 GMT  
		Size: 18.1 KB (18092 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-lein-2.11.2-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:011d0986a1db257b43d42ab05ee37912398f0bb1a319e2590a0d34d5807a1b3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232401906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc197eda8e92c0e5c4c63b0b682067d2fd806de66a48db724f548cd849950be5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 04 Sep 2024 21:40:08 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Wed, 04 Sep 2024 21:40:08 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV LEIN_VERSION=2.11.2
# Fri, 06 Sep 2024 16:59:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 06 Sep 2024 16:59:26 GMT
ENV LEIN_ROOT=1
# Fri, 06 Sep 2024 16:59:26 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50350f2974c0417f312abfa4209238a88e094d8f3d7ce45496c26f6a51b902d2`  
		Last Modified: Tue, 17 Sep 2024 04:54:51 GMT  
		Size: 154.5 MB (154503758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e19160b4ca7ecf171473b7fa89466687661a391be2821272fa9c043d0630bb1`  
		Last Modified: Tue, 17 Sep 2024 04:54:48 GMT  
		Size: 43.3 MB (43309214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c4888ecfbded5c718dc9492ac3ab4275d14e016b57741d10bd2ee45aa81fff`  
		Last Modified: Tue, 17 Sep 2024 04:54:48 GMT  
		Size: 4.5 MB (4514140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a7ce05ee1e9c7e9a3c89c8ce9d4d7239445a2def1d5dae086cb3878fcf6af8`  
		Last Modified: Tue, 17 Sep 2024 04:54:47 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-lein-2.11.2-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e333128dfcd9f7602f095b38226ceeb897f32ef03c391fd042f21fb219ab5c9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4427155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a6eca1f4574bc2e5d0884d6a0f68e029ddd9e6249012dd9519f9486b2d1107`

```dockerfile
```

-	Layers:
	-	`sha256:8ca86c92deaa33a77647c1ca5b4b106b7a6dcae1078f892e71bc7ea7caa53456`  
		Last Modified: Tue, 17 Sep 2024 04:54:47 GMT  
		Size: 4.4 MB (4408534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3ee021e8c7e1c28df759c763303ab19bd2cfbb79e82a8582f9aed9096151a86`  
		Last Modified: Tue, 17 Sep 2024 04:54:47 GMT  
		Size: 18.6 KB (18621 bytes)  
		MIME: application/vnd.in-toto+json
