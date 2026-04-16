## `clojure:temurin-26-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:545ca73ae92ace2c6375eed656640640fc92a9a90225fc1442fa4b2d6a4cb313
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8f8bf3b841fd76100c1fec601abed919b8db56963f522464d9c2002f446aabfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144570668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98d71423a86550bff35491a3bf7c95a735a0b0a7f3de776804dd5a60c1fa0b96`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:07:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:07:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:07:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:07:38 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:07:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:07:38 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:07:51 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:07:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:07:51 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:07:52 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:07:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:07:52 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:07:52 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ee5c1e0cf15be378f920dd7b97d319143a378c0648feb3aa1ae350aea61e87`  
		Last Modified: Wed, 15 Apr 2026 22:08:11 GMT  
		Size: 94.5 MB (94455691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6334d7c38a03c496eecc06cd077fb239aae81c71240dd556cafd436f8af4d2e6`  
		Last Modified: Wed, 15 Apr 2026 22:08:09 GMT  
		Size: 15.3 MB (15338783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22309687b23b5942f5f381b8c380b991ceef4febe5b6530c9aa72da6aa06955a`  
		Last Modified: Wed, 15 Apr 2026 22:08:08 GMT  
		Size: 4.5 MB (4517746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd44d81282ef930d6a64b0c13bccbab20b2ab66e48d07c085c7e04948a5b62c`  
		Last Modified: Wed, 15 Apr 2026 22:08:08 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:456c362756ff43e4b19d3034c43208cd45dae07c0c0dea538e5113e95e0759d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3011482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304bda714516a75506cb7e0e2f0d4eea588ca031a18cc50cd4833e1c37c41939`

```dockerfile
```

-	Layers:
	-	`sha256:d0793fdf3b5272bcadfe5c2594dee28588ba78e5810a64dcf436a4e896811756`  
		Last Modified: Wed, 15 Apr 2026 22:08:08 GMT  
		Size: 3.0 MB (2993086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba6dad34a4bd60167667b68002f3d3fbffa6a403ce3489e2e6f05754b39f2f8b`  
		Last Modified: Wed, 15 Apr 2026 22:08:07 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e62a6f3f6113554b3a2aa0a8fb3df306e7c3ba3c2401f47356e3eb1b700fc580
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (141985323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae1b70c82d5338c2fec93ae6a51bf22c5a4991652fd8575f3e9b57d4b9c92db`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:19:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:19:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:19:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:19:09 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:19:09 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:19:09 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:19:24 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:19:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:19:24 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:19:26 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:19:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:19:26 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:19:26 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce1ec8f5e97e57e9f06c82a701697bb4e123379ac62bbdcee88f06c81b5ab60`  
		Last Modified: Wed, 15 Apr 2026 22:19:45 GMT  
		Size: 93.4 MB (93395224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de87f9d5f6b00404962caf041ac99c981ba37a5ce17393f18882eb573f6c4b9`  
		Last Modified: Wed, 15 Apr 2026 22:19:43 GMT  
		Size: 15.3 MB (15327238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdff6c19938c1e8ffd641152be3c1e7b0cc142e35c87fc99c618e5935ea039d`  
		Last Modified: Wed, 15 Apr 2026 22:19:48 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e9f251a6e1de62d0f74a7d1297f3e19033463c9aa27750f35ffc346479242f`  
		Last Modified: Wed, 15 Apr 2026 22:19:42 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f61fd68dd32b36fab01b5d6f7162dbe47bd53eafd3457a874fd4a52032aa4f25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3011208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb6bda616c184a615fe695f049ea389609397b6b6f1576a87233a65f6c8af08`

```dockerfile
```

-	Layers:
	-	`sha256:06133efab03a9a4ed19666ddddfcec6fd0f0e54ec57a617cb2fd91e8e01a0875`  
		Last Modified: Wed, 15 Apr 2026 22:19:43 GMT  
		Size: 3.0 MB (2992692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa16c163937665068f5edf9c05c4029f8549483e729d7146bdfe6a4ffff3c98a`  
		Last Modified: Wed, 15 Apr 2026 22:19:42 GMT  
		Size: 18.5 KB (18516 bytes)  
		MIME: application/vnd.in-toto+json
