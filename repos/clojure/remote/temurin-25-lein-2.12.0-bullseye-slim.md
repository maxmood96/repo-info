## `clojure:temurin-25-lein-2.12.0-bullseye-slim`

```console
$ docker pull clojure@sha256:e9a158097fcc62c6740387512f6992af6c61ad3a89bd297873441feef23fc5d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-lein-2.12.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e018286037d32c5e0025cd4763e8a48cf5e1e518913353699019fad2c14a21a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142131303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25ba5e3e6c5f8ced0ab82ccde4d91392a7df852045f8f23f109711cc9bac3d85`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_ROOT=1
# Fri, 26 Sep 2025 15:53:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d207cc66da44f4d060efb9a20dc200ca0e6b10c76276d0c1db9c735eaee1d506`  
		Last Modified: Tue, 21 Oct 2025 00:19:22 GMT  
		Size: 30.3 MB (30258365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7338424571835aa04d0820414e0d3e74e47ac2f68bc1be561bf5fe7b6daa98d`  
		Last Modified: Tue, 21 Oct 2025 02:24:23 GMT  
		Size: 92.0 MB (92036044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5acc3284dd2529a561b34d9abd970f8ab1bb5a51e8a7a5ca84eff5d70de5cd04`  
		Last Modified: Tue, 21 Oct 2025 02:24:16 GMT  
		Size: 15.3 MB (15318729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0bc519889c518ca20a241ce82f1491507e84320ca8ef376c9bea6af3073151`  
		Last Modified: Tue, 21 Oct 2025 02:24:15 GMT  
		Size: 4.5 MB (4517737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204db2ac86d3d198a2bbf7291c7ce6be526b5672dcf6200e65535c934e61d272`  
		Last Modified: Tue, 21 Oct 2025 02:24:14 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:342f3f1b0899d48184ad4e58d7ce9ea695c21ba0f00a27bd976e89660eb82b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2988321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af21e791cc970e7b314b6bcb075ff46e276e29e003d56aa197f839a8cc0143c5`

```dockerfile
```

-	Layers:
	-	`sha256:27502e50aa5881d7bacd2d3ebe4af80432eac400ffc99c053d0f4d2aff26a0d6`  
		Last Modified: Tue, 21 Oct 2025 09:35:02 GMT  
		Size: 3.0 MB (2969220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91f44f8adcc3bf041700455297899fb03a19132bfa6f5b926a1620a57bea9d67`  
		Last Modified: Tue, 21 Oct 2025 09:35:02 GMT  
		Size: 19.1 KB (19101 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a66f3a5390d4738d220f0771ca3af70b75a4c8de2c74270ed8aca096552915de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139617608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb257fcb32bde0807db59e16c4c94253705d938a260cada62840ce48c844dbc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_ROOT=1
# Fri, 26 Sep 2025 15:53:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:40bdde71139ce202a6b0b5346000bda907331b21efec94960489d60568d26752`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.7 MB (28748401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d134483f4cb7c1f258c4d0596badb97fae9c6ea83fb7468b2688761a12affd`  
		Last Modified: Tue, 21 Oct 2025 02:29:38 GMT  
		Size: 91.0 MB (91045228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44ba097f64e31fbe7793e24fdc224d83a821965af52c27f43fa126e2691dfb2`  
		Last Modified: Tue, 21 Oct 2025 02:29:34 GMT  
		Size: 15.3 MB (15305797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55b64ee10268b5148a34befc864b4ce9b7d740956390591402123f3873db41e`  
		Last Modified: Tue, 21 Oct 2025 02:29:33 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d03804fce6eb8e6e44b85ef0058c7928a46217b7e2839c14cf4adfa8b45547`  
		Last Modified: Tue, 21 Oct 2025 02:29:32 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a123bd03b426289e6c39bbb164e3d86e711f482aa89acb5f393517ed47f22adf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2988096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3945b94dfda493745fa7fb7500902a03a1022fcd94e8457c019d5d53c3d5030d`

```dockerfile
```

-	Layers:
	-	`sha256:0335ef674e5a76ef2aa77bc793240973037192cc64c7ad30bfb0b046860271f2`  
		Last Modified: Tue, 21 Oct 2025 09:35:07 GMT  
		Size: 3.0 MB (2968850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dac8b4011a68bfe32cea3e7e0251370aa134f57caac71c122243a99fc8b42e01`  
		Last Modified: Tue, 21 Oct 2025 09:35:07 GMT  
		Size: 19.2 KB (19246 bytes)  
		MIME: application/vnd.in-toto+json
