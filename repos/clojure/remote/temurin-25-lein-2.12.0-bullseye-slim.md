## `clojure:temurin-25-lein-2.12.0-bullseye-slim`

```console
$ docker pull clojure@sha256:a5f1cfa921427ebf5c3e7cd5d051ac7803ebb98efb3879f9277569afe709e13c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-lein-2.12.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:56747b51c1ecd3197c34b097796e2a80c7b8a2de666a5ba9a2bdced6d109997e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.4 MB (142351443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e677fb93e3789968910cd45c539fe16fe6f1de666899e97c1ef04ea03149dd4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Thu, 05 Feb 2026 23:07:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:07:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:07:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:07:26 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 05 Feb 2026 23:07:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 05 Feb 2026 23:07:26 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:19:40 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 05 Feb 2026 23:19:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 05 Feb 2026 23:19:40 GMT
ENV LEIN_ROOT=1
# Thu, 05 Feb 2026 23:19:42 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 05 Feb 2026 23:19:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:19:42 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:19:42 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f849f6fab95a2fae2e243609862b99fe205cdea0cebbdfe822150caf8290d2f8`  
		Last Modified: Thu, 05 Feb 2026 23:08:01 GMT  
		Size: 92.3 MB (92256283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:747bfa1174d00185b86cfc573c6129343251a97a5af7eb2825188c5812bbbd0f`  
		Last Modified: Thu, 05 Feb 2026 23:19:50 GMT  
		Size: 15.3 MB (15318697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74476e4bf8f9e39e0b740a90cd96ca1660b1263a050a990a54aa6ac5a06f63a`  
		Last Modified: Thu, 05 Feb 2026 23:19:50 GMT  
		Size: 4.5 MB (4517748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc489b4fd50a0f39ca6db4ce5726c3e08f24905710d323ced4399bca20807995`  
		Last Modified: Thu, 05 Feb 2026 23:19:50 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:72c29f4169a61f8bd0a120cac556a29c7490795c40bc0a69328e2638c5a9eb30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3005481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa39fe1d516249633ab3584959ed4d360647776e63d70b1e1f3a17891cce63fc`

```dockerfile
```

-	Layers:
	-	`sha256:18ae2d0a85a7ca4b453af7b291fafdc12086487596bd35cf059b6f652bd154b5`  
		Last Modified: Thu, 05 Feb 2026 23:19:50 GMT  
		Size: 3.0 MB (2987222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bded1348545fadf1f639678de03c1d82cb2f50b55ab87d803c77f9e43188cd55`  
		Last Modified: Thu, 05 Feb 2026 23:19:50 GMT  
		Size: 18.3 KB (18259 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c466fc383f5f85b4f026aa21e1435e1d7151d05e3e929be8b12ddc9ff60688d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139856694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27f03b88e7b059605a875194b7852fe536573b36e6cb500fab8bdb35ec7cf68`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Thu, 05 Feb 2026 23:08:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:08:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:08:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:08:06 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 05 Feb 2026 23:08:06 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 05 Feb 2026 23:08:06 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:08:22 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 05 Feb 2026 23:08:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 05 Feb 2026 23:08:22 GMT
ENV LEIN_ROOT=1
# Thu, 05 Feb 2026 23:08:23 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 05 Feb 2026 23:08:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:08:23 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:08:23 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db83787367b31e098f6d47e4c2c06bc3ba1162a253d9298308bd675943336ba5`  
		Last Modified: Thu, 05 Feb 2026 23:08:42 GMT  
		Size: 91.3 MB (91288274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd8c966089c3d6066c63d0c8b02f3815cbb2547f3837f815b0123ad3cacae08`  
		Last Modified: Thu, 05 Feb 2026 23:08:41 GMT  
		Size: 15.3 MB (15305840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49516fbd05435097c9dbf612c7884ad25c129de6c2ada6257a98f9e2412f462b`  
		Last Modified: Thu, 05 Feb 2026 23:08:40 GMT  
		Size: 4.5 MB (4517713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3efe3800b148fb4b3ebea5133aec72da7e521dec367bdc26a26882d15c1cbe`  
		Last Modified: Thu, 05 Feb 2026 23:08:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:82607cf7eb572aab65ca69eb8fc2714a6ee21c8611a3c5a1464d32408e2cab62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3006055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a472e28db7644bcab1bba4028e531a5d8fbd828de31f1a85f27b2fadb97bc1a3`

```dockerfile
```

-	Layers:
	-	`sha256:89143de602737b801d03a85b47a60bd4ab0131b13882769b0238bd6517b4a3c9`  
		Last Modified: Thu, 05 Feb 2026 23:08:40 GMT  
		Size: 3.0 MB (2986852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78c20c2c0844034473afd9fc3367da53e41b191eb9e9bb467dbbf3d254a858fe`  
		Last Modified: Thu, 05 Feb 2026 23:08:40 GMT  
		Size: 19.2 KB (19203 bytes)  
		MIME: application/vnd.in-toto+json
