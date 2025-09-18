## `clojure:temurin-17-lein-trixie`

```console
$ docker pull clojure@sha256:db1c4c753db6c7e7a128f6afcaf1f5fdf61e7dd3cc25db2bda72d2b1181995e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:f6e089eb4b99167b96fb9ed50b081eda5d6b5c06237cfcde5e76fd70bb4947a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.1 MB (217069718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6a59345568b4e8c96f02d1c2181b0744cc28c6e371ef4702c9f37451e5db428`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:15b1d8a5ff03aeb0f14c8d39a60a73ef22f656550bfa1bb90d1850f25a0ac0fa`  
		Last Modified: Mon, 08 Sep 2025 21:12:52 GMT  
		Size: 49.3 MB (49279531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e01a5c69623831c03190ea685c20b9716912a66ff309f4a0dd6c32f2121568a`  
		Last Modified: Wed, 17 Sep 2025 02:37:31 GMT  
		Size: 144.7 MB (144693569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9331dbe69c3453e7f90c5605ca3e9f784dda17f18b222f82802b0af4a3f426`  
		Last Modified: Mon, 15 Sep 2025 23:26:43 GMT  
		Size: 18.6 MB (18578443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8fb39a8a962b5d244ab140ed555bc5416364168e3d700eb39512ac4bda8c685`  
		Last Modified: Mon, 15 Sep 2025 23:26:42 GMT  
		Size: 4.5 MB (4517747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d34e449d2ae7e6cb77420d615fc686c665131489f377fabe6c6457d5c9d1d786`  
		Last Modified: Mon, 15 Sep 2025 23:26:41 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:cc2b09ddd1d54465a4afd223f323de5bc65ed50991b4a43f81548704394beaa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3831725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f892bb8e9f6facfb5314f8821b548ffc4cab371bbda11571b77ff2750f949b8`

```dockerfile
```

-	Layers:
	-	`sha256:31805023d5ef1a94082c9b7c95ee6709e420137174dd82e636c77027eec80b1b`  
		Last Modified: Tue, 16 Sep 2025 00:40:01 GMT  
		Size: 3.8 MB (3813330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90ebf5160e4ef744d568503cb21590e0225a080467f09ba89d9c3ef4c63400d3`  
		Last Modified: Tue, 16 Sep 2025 00:40:03 GMT  
		Size: 18.4 KB (18395 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:33fa4cc878808c384ba22cb7f6e6fd858dfc3d897a55ee986ea5021f51beec37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.2 MB (216243187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a20d98e0fa83fff040df4bf8bef099f96411092521fc2ba711a761fd37a11e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:37b49b813d9cadbc816aea22a15ef76898c66b4db015fea88b8f15bf213d5004`  
		Last Modified: Mon, 08 Sep 2025 21:13:28 GMT  
		Size: 49.6 MB (49643746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f4037ca81d388986f8e0f47079ab3cd764f0f8e0f9714e33d8819c4e30d675`  
		Last Modified: Wed, 17 Sep 2025 02:38:17 GMT  
		Size: 143.5 MB (143542107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66dd20e6f50b0a42ec5e98bb61cb0ac056614f575d58c528df6fae34b217c46a`  
		Last Modified: Mon, 15 Sep 2025 23:26:50 GMT  
		Size: 18.5 MB (18539210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc695506f6157d6c66ef7efeb9c98b3cce740813f06cecc09a33805cca9c6cbd`  
		Last Modified: Mon, 15 Sep 2025 23:26:50 GMT  
		Size: 4.5 MB (4517695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9448a08830148b5e72e5be5e83cf0db8b3f38e98fa977036d5dcede6828e6a54`  
		Last Modified: Mon, 15 Sep 2025 23:26:49 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:60b1a1069b5ab68327f354af4c5dd196a6b825e31fee820740f9366c76355c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3832723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66cd926820f49fbfc3e7f6d508b581a0c58e17358d9b976835f28919b70b52dc`

```dockerfile
```

-	Layers:
	-	`sha256:cec47baf9713bb0af4547b8225191d7b28746ca50e2e57ddbbee75b1ae84f8fe`  
		Last Modified: Tue, 16 Sep 2025 00:40:07 GMT  
		Size: 3.8 MB (3814207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02c49278e896e147b37a23e6ed8fb4abfce8cf1a609b73105439da3e2e5f05e5`  
		Last Modified: Tue, 16 Sep 2025 00:40:08 GMT  
		Size: 18.5 KB (18516 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:c6de3425a7caefccf1617eb706084d6988cf0925bf29620af16c54d16f32ce37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 MB (220631382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d2351b99b9db11b33f515f4821dd6dfd554565d939c6fb71338c58b92132eed`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4cb8224e7ffc22512c71f1cfc1042cb22342df02312e61cb1ab0c492c3369711`  
		Last Modified: Mon, 08 Sep 2025 21:18:07 GMT  
		Size: 53.1 MB (53104433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bec9658ed8acc29c1f6bd15375c46e562b9e85a845ad8ba358ea676bd106fa2`  
		Last Modified: Thu, 18 Sep 2025 19:48:33 GMT  
		Size: 144.4 MB (144372823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e2eae33088e0ed6097ba7a5af188488ae6e1634c922521346adf12d5778245`  
		Last Modified: Tue, 16 Sep 2025 01:02:41 GMT  
		Size: 18.6 MB (18635994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:308707ec2d4e091018686aaccd388283a42cdbc53b4011ab52cd85cc5067c9ec`  
		Last Modified: Tue, 16 Sep 2025 01:02:40 GMT  
		Size: 4.5 MB (4517704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f3a9cb209aff19f2ce067c0b95e7678c4dd94623d7641e34711694e648c938`  
		Last Modified: Tue, 16 Sep 2025 01:02:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e92e8abf6f08579485fc472914888e67f056aa4039bb953e89aa9e7eb0ae5ce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3832767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb1ac608c08593a226bc0c95853c1f738de68e94ab66c17b932fcc7da2520885`

```dockerfile
```

-	Layers:
	-	`sha256:33a20249fb0f2fe0525baf65d8cf94d1ebc68c4a2380a265028a79bcf0d3b2f6`  
		Last Modified: Tue, 16 Sep 2025 03:38:42 GMT  
		Size: 3.8 MB (3814328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7b75344ae7f175f681df1ba275a9f5c698a1e2c9b53139356144f6553952287`  
		Last Modified: Tue, 16 Sep 2025 03:38:42 GMT  
		Size: 18.4 KB (18439 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:1f5d04ddbc1455e9599d4d96535872d1c5988372dcd597731daa3301af8f4d02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.4 MB (209389623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b59e5733cb3ec81875ea1c17ba4cb9a3ae867740791cdb631c0d0fb1b4538f9d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8f913be5ecadf79e3ee9792194aaab366421c7e066487d572f285b293ff78a7a`  
		Last Modified: Tue, 09 Sep 2025 00:25:27 GMT  
		Size: 47.8 MB (47765447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3ae21fa5b4d30371a66ca687e7c73e5de6887104c1d0ede9bca919214a08b0`  
		Last Modified: Thu, 18 Sep 2025 19:48:28 GMT  
		Size: 138.6 MB (138575662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d98e84da4628b26fe6d3341d392e6f6b3081609241420318318fb17a23bc9bc`  
		Last Modified: Wed, 17 Sep 2025 19:30:44 GMT  
		Size: 18.5 MB (18530295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b21e131e2b6878ba6f7fef7962bc44c18a4f9517bf567673c04f275897754d78`  
		Last Modified: Wed, 17 Sep 2025 19:30:41 GMT  
		Size: 4.5 MB (4517790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0daf36afdaca591b76aa920075dc88d96dd8569159bdb3e8d90761a1fd82f4`  
		Last Modified: Wed, 17 Sep 2025 19:30:41 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:557dd3580535e4ef7a84bed645d6f01cad7595b0db45edcefcdbbc0d72a3502b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3820325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a1cb00d0ced464938bee785c39a0af217388285aa2a624ad1ab47731b8b7088`

```dockerfile
```

-	Layers:
	-	`sha256:389663a3019e8b783411836f7ff31f690dbe875863b89ecffeca41971fe5ff36`  
		Last Modified: Wed, 17 Sep 2025 21:35:42 GMT  
		Size: 3.8 MB (3801886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ec49afd2438120098d4245ebdb25c881082e9a63e6237a4301c893e28755c1f`  
		Last Modified: Wed, 17 Sep 2025 21:35:43 GMT  
		Size: 18.4 KB (18439 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:6f5db1489c32400c8e18a8d6c8de546987cba1bbd56c8bcd9b2a2c56fbddf17f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.2 MB (207208747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0c6154fbdd3dc80f43d6046ed737b82fe4115768635c929acd372cb873ac85f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:28eee642962fd09c10ecf87da2d4b65d208f3d5c1bf3fcca21c105c0213f558a`  
		Last Modified: Mon, 08 Sep 2025 21:32:18 GMT  
		Size: 49.3 MB (49346327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07421808cb5a906dc7375ab5693a2be92a79fe93308030ecd8c387a14adda9d5`  
		Last Modified: Tue, 16 Sep 2025 00:35:20 GMT  
		Size: 134.7 MB (134724367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6a795274d3e7794ee8d2a68b380f0dd1f21e025a58bd93d7530a31190f6de8`  
		Last Modified: Tue, 16 Sep 2025 00:35:39 GMT  
		Size: 18.6 MB (18619913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255917a85d1bd35864b63332b5c2b50cd83aefcc9bcea2fd204f82189cc886f6`  
		Last Modified: Tue, 16 Sep 2025 00:35:37 GMT  
		Size: 4.5 MB (4517709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32491285f3904dfe88c64ba2cb02d8483650d59480205f468d73fac32b907f23`  
		Last Modified: Tue, 16 Sep 2025 00:35:36 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:112fcdb5bc1158d6f23cb362ae8740a29e511c5ea2c387a772e8bc5de57f6f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3828151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc75e5758166620c0d386d298ea80d33e4fc7bef479f16a87d54a0ae8ef719bd`

```dockerfile
```

-	Layers:
	-	`sha256:5db5e8ef6cbcd805b1d9229b6f249c72992c5f9c479d2cbb6bb306742cd67439`  
		Last Modified: Tue, 16 Sep 2025 03:38:49 GMT  
		Size: 3.8 MB (3809757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28e1549781d6ca21c7daf63c4d20a4da87914c402c9f29886e2e52fee2c5ef09`  
		Last Modified: Tue, 16 Sep 2025 03:38:50 GMT  
		Size: 18.4 KB (18394 bytes)  
		MIME: application/vnd.in-toto+json
