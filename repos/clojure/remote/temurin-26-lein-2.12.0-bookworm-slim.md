## `clojure:temurin-26-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:aad965e31459087bea2c73b4c06020b8ae5c7c27c95c3fd4ec776e0fa71974c9
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

### `clojure:temurin-26-lein-2.12.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7eabe4d22de8d089b2c8e1eef8298e3c28119743f1e148f12c8a0e3682bf6ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.0 MB (144969686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bfa94a9e46aa2e4db3086695649e5462f7057c927d910b8d1f37240f01a732a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:21:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:21:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:21:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:21:27 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:21:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:21:27 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:21:40 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:21:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:21:40 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:21:42 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:21:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:21:42 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:21:42 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47833512b9e23c9c2dfe8bcdaa25d638496220f7ef8bb021f0cb4964ee3e2a7a`  
		Last Modified: Wed, 22 Apr 2026 02:22:00 GMT  
		Size: 94.5 MB (94455697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14f4a7a994ccb79f2be5d48817d3b56b466cde921fc25d0ed08b8a2f585a389`  
		Last Modified: Wed, 22 Apr 2026 02:22:00 GMT  
		Size: 17.8 MB (17759570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c07948be4a6e571424237623f07a3d55c3f7be3ba761f25d5c8b624a5b4a4d3`  
		Last Modified: Wed, 22 Apr 2026 02:21:57 GMT  
		Size: 4.5 MB (4517739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc77618d7012f579570e7a56ca5e7b59493bd57f1d9075b959b215b65544cbe`  
		Last Modified: Wed, 22 Apr 2026 02:21:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e58585c65b1abe7599df24aa25c9e4e40410cfc1af00481abb8f572732e10509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2713950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ec74332a63e32dd1432f6f80c635b48121eba362dba7645198ed72894b493ca`

```dockerfile
```

-	Layers:
	-	`sha256:d6cd0e2ebc7d41995d5b7c615b58569b6c5c4ae15754a1728d0cad31525bbb01`  
		Last Modified: Wed, 22 Apr 2026 02:21:57 GMT  
		Size: 2.7 MB (2695554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34d10271cf44e073fc0eedc9ca67e57161b230b6179bf7d50a01ec3f30aa1008`  
		Last Modified: Wed, 22 Apr 2026 02:21:56 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:89d63d8e04259e2cbe8e358401df335ed9cc3a2f16c4ce62461c9c8de5ff6d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.6 MB (143622515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18874c4172e088e1a5188e90fc94e7b4677e7cea3e74604b172b6f100f6cf753`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:24:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:24:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:24:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:24:21 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:24:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:24:22 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:24:35 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:24:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:24:35 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:24:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:24:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:24:37 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:24:37 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d60a3acb34a95760fe0accc757f7e75b70257d0264cb0e2ef0b8973574c240`  
		Last Modified: Wed, 22 Apr 2026 02:25:01 GMT  
		Size: 93.4 MB (93395205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a3eaea9f589499698e3d593fbaf666938fdcfef7543c8e4cc33755254022da`  
		Last Modified: Wed, 22 Apr 2026 02:24:54 GMT  
		Size: 17.6 MB (17593038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32237eb58eb4b027a572e85e9a414ab311e4ff7e1897a7da71edc671ff41cb3d`  
		Last Modified: Wed, 22 Apr 2026 02:24:54 GMT  
		Size: 4.5 MB (4517730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ab178e8a2bf3f0ccb825ff4cced384c9e1ced7ad0d34476b084f3811958f81`  
		Last Modified: Wed, 22 Apr 2026 02:24:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b6632d2cf41bec37dc954cb94577c929b80ed052d8abb18d82ed3711629d08ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2713683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071556bdb046850198150c063a6f5144b5385f31e364c082c29021f28975aaa6`

```dockerfile
```

-	Layers:
	-	`sha256:4961fb12c00cb740ca0bdd546ad09b5c9778d9e36a163ffa7e8dbccd94bf9f36`  
		Last Modified: Wed, 22 Apr 2026 02:24:53 GMT  
		Size: 2.7 MB (2695166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e134bf2e518f99f0014cc8efbf1f06ecbac6d254e56c46376e3eae0d7c47cf3d`  
		Last Modified: Wed, 22 Apr 2026 02:24:53 GMT  
		Size: 18.5 KB (18517 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:41812fdbeb0cb18aeaec8fc0da10ac2be5f8554a9a1b9880dad956c590e0cf78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.3 MB (148339446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec588f0dd4538bb2ee7a810e7487032da1a017cf00801a28c52382f78987b1cf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 08:51:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 08:51:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 08:51:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 08:51:10 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 08:51:10 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 08:51:10 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 08:51:40 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 08:51:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 08:51:40 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 08:51:43 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 08:51:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 08:51:44 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 08:51:44 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0bcb46f6315f7a2c8ddde875fca21de96c94e451046e6692f77a99aca489f3be`  
		Last Modified: Wed, 22 Apr 2026 00:15:02 GMT  
		Size: 32.1 MB (32078402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30eb4eb9b2f7105e84346a7caa4be9f9fac688f33aad32bc25bad332349d4d4`  
		Last Modified: Wed, 22 Apr 2026 08:52:19 GMT  
		Size: 93.8 MB (93781481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0216fec632526879e7fefc2055d24b1c95258be4c260ca065844375b199036b3`  
		Last Modified: Wed, 22 Apr 2026 08:52:17 GMT  
		Size: 18.0 MB (17961379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a80ebb5e7b187dac71f7cafd7a33981cf2ba3bfd761ac436e1fdcf1578cda3`  
		Last Modified: Wed, 22 Apr 2026 08:52:16 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a5feab0635dcd3e53ee9aa1fee3412e4cb6f0ece23f3262c051c7317bc702c`  
		Last Modified: Wed, 22 Apr 2026 08:52:16 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7f7b768e907807d103ae4fdfde75f9c6c771aba297a484202dc50b92c2f31526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2699763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ff4e1dbe4605af1c59d1c99fbfbb81796446063f5e16bd4271bd8c15f3f4e6`

```dockerfile
```

-	Layers:
	-	`sha256:d4adc9024c63f83dc79330c8e6c757cbb187ef9ad0ac63bc343778d1bfd30416`  
		Last Modified: Wed, 22 Apr 2026 08:52:16 GMT  
		Size: 2.7 MB (2681323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc9ae2ea7ac798e73c71c810f68e28f80cf940a9660151d0c9c1acca6e5bbebb`  
		Last Modified: Wed, 22 Apr 2026 08:52:16 GMT  
		Size: 18.4 KB (18440 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.12.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:4e896f87f9f98b4243e3328507e5aff5591d9cc0440b17b6dd0868f28bda7ed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139379421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1165580928e14b9f66643af967524f35a7764af4ee3639ff9c7145f1bae73baf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 04:06:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 04:06:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 04:06:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 04:06:50 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 04:06:50 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 04:06:51 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 04:07:02 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 04:07:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 04:07:02 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 04:07:03 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 04:07:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 04:07:03 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 04:07:03 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c6ea417d5ab31a608e273e6f14bf4055de86e0cd7929dfbce786005714ea0c`  
		Last Modified: Wed, 22 Apr 2026 04:07:29 GMT  
		Size: 90.5 MB (90547719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5126e61a64b2e1265c0755ba699d501755ee816bc3e6b4c8fa9d9cf6cee8a6`  
		Last Modified: Wed, 22 Apr 2026 04:07:28 GMT  
		Size: 17.4 MB (17422006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f2bba8300ccd6b7ae52761629d89bf1ae9afb4e4802dd3a9fc25f31e6f8310`  
		Last Modified: Wed, 22 Apr 2026 04:07:27 GMT  
		Size: 4.5 MB (4517705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd57ba50baf3cae0bf506e20c630efc04324cb787d57a094cbd90225f597e7dc`  
		Last Modified: Wed, 22 Apr 2026 04:07:27 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5c86278d2843d0774d1ad051197506cd7c3ce28944c7ae5b05edfc53a920285d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2690949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20dc412fb391b260b37c6c56679d384255bdcdea8d92d3d236b6cacbe4440e95`

```dockerfile
```

-	Layers:
	-	`sha256:a1999f545dbd6f651156511b27cb62b8ec7ca938746164d44446edd98e3adee2`  
		Last Modified: Wed, 22 Apr 2026 04:07:27 GMT  
		Size: 2.7 MB (2672554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5887351e412436155618a5e2cabdcbc0686d19235c513b4e8440d9c80e54d3a`  
		Last Modified: Wed, 22 Apr 2026 04:07:27 GMT  
		Size: 18.4 KB (18395 bytes)  
		MIME: application/vnd.in-toto+json
