## `clojure:temurin-24-lein-2.11.2-trixie-slim`

```console
$ docker pull clojure@sha256:164041990f4f17ef3bddb1edbb6d24c69a8e7621db1fdba6d3b6a9db83f8a307
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

### `clojure:temurin-24-lein-2.11.2-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d5b688d6524425fb0bb41bcfe74b679da6821bea783bc343e7e0524842797ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.1 MB (178123933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840a295684bf2b15a3ddde4e4792f2646773e31f7813ce28b2d9b44a0cd37163`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f7f88c6d7f710176d487a3ac59c7790f981832a06bfc197dbe4a74d73b1407b7`  
		Last Modified: Tue, 01 Jul 2025 01:14:56 GMT  
		Size: 29.8 MB (29761106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f239cb83a22bdc6a514ec363bf1e5ee9688fab250495fee990d452270fb7e4fe`  
		Last Modified: Wed, 02 Jul 2025 04:17:44 GMT  
		Size: 90.0 MB (89952014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66226b9f976ddfeaa28bfa19f8aab311547b97b642ec0afd3d2e080de5b76708`  
		Last Modified: Wed, 02 Jul 2025 04:17:35 GMT  
		Size: 53.9 MB (53896235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fc92f981d73010c4eb12ce9d473f35e5f0d5005f76d70b8e9022766b424e9a`  
		Last Modified: Wed, 02 Jul 2025 04:17:30 GMT  
		Size: 4.5 MB (4514150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c16847274c3a546ead71730e5e9aa1880d34ec6eecb31865c7bef9e81a3a6b6`  
		Last Modified: Wed, 02 Jul 2025 04:17:29 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-2.11.2-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f76c5739fa6ba9492144993ef799f4286baa9008d140c073c17fa22937fc5c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4246543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc6aea5d135bd857dfd53e2f3875210e0c7e7ec9489408d4d2b7dde481ccb0e7`

```dockerfile
```

-	Layers:
	-	`sha256:5312cdb791ad7637b58fcc993661898a561e9b6c8f66de4a4850b1e0a05d25c4`  
		Last Modified: Wed, 02 Jul 2025 06:41:49 GMT  
		Size: 4.2 MB (4228112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e06299cf6ee44bf621e36ad231e5d7d05ea9e842f4be5b2470d6d33f04e22a14`  
		Last Modified: Wed, 02 Jul 2025 06:41:49 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein-2.11.2-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9c071bae91f5de882434766eb701107ea74afa761a6c83e16d3e1b9104a191cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.6 MB (177571369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a396aea7b9c1d6f302a7cbb6b39c25b7f8dc4cca16dffd9efe25acfe1322fdd0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:dfa10e860e0106510a14bae8331a4dd762d3d3737fdba0dbec102458f9853b71`  
		Last Modified: Tue, 01 Jul 2025 01:18:18 GMT  
		Size: 30.1 MB (30126864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e3b7a4767010fa7ce7cd79c35e00c69d2fb559ce69f151a063ef94a08d5a77c`  
		Last Modified: Wed, 02 Jul 2025 13:00:18 GMT  
		Size: 89.1 MB (89091235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f6d22317bd2bf84ce8ae42be0c404884f7c2a4d261f73dc3cc1faf10dd552b`  
		Last Modified: Wed, 02 Jul 2025 13:00:15 GMT  
		Size: 53.8 MB (53838680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140579e87b8887024a505113ca3b2f5c3f421c8a5374ce53d1c17fb610ed9c45`  
		Last Modified: Wed, 02 Jul 2025 13:00:11 GMT  
		Size: 4.5 MB (4514162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9587ca46d596814c421f400cd9447d188ec2c274fb2bb22a02c4ce9f764c2a7`  
		Last Modified: Wed, 02 Jul 2025 13:00:11 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-2.11.2-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2699089ba97fe3f2ef00a46a618bdaaaa4cd71c04096f7c80a17f13f990b42f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4252362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fff97ff285838272cfa2a2212974d71526d59a80f61563f54556b664fe7f3c06`

```dockerfile
```

-	Layers:
	-	`sha256:829f87ff37cf36ee9be5c5c9f05d351fa5c7ac07cc79c4b89dc394fcc437107e`  
		Last Modified: Wed, 02 Jul 2025 15:42:59 GMT  
		Size: 4.2 MB (4233811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34b17404fc2d16664f826bd9f019e19d1920568c6e38d37b9341040b4fea8294`  
		Last Modified: Wed, 02 Jul 2025 15:43:00 GMT  
		Size: 18.6 KB (18551 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein-2.11.2-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:6905cb193c3cc262024180843263cd94c6f01a5ae21509986ef010ec65b177c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.9 MB (186903046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f79d2c52263ccf98dfb0037a207fe5934b883da60ad395d2493c881304d74e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2adebcab7d76ecb14ead3f70af8ca34e5abca513c2fcbd9f40e3af1e18442ccc`  
		Last Modified: Tue, 01 Jul 2025 01:19:23 GMT  
		Size: 33.6 MB (33586035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7cbb5f9536c9aa24563a8b209f3c1b094fe9b850aa3b8889a2d17239db0d7b`  
		Last Modified: Wed, 02 Jul 2025 14:09:45 GMT  
		Size: 89.9 MB (89920270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2e7e8e4ce348a75672b273ae1fc3d30814adba3458fe52978d828f26877f60`  
		Last Modified: Wed, 02 Jul 2025 14:09:44 GMT  
		Size: 58.9 MB (58882113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9766c4e60efe53d5bde3848e388090051b90b32aee1403d8a78c6cc8b4d98514`  
		Last Modified: Wed, 02 Jul 2025 14:09:37 GMT  
		Size: 4.5 MB (4514198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56fbbe69e73224c17bd8bc6d113d8648a93d1420b9d7d68fbd4aa79860fc7188`  
		Last Modified: Wed, 02 Jul 2025 14:09:37 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-2.11.2-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1e3fa7c58e07b719fa5c39184230ea82b7bcbf0378cfcec0e88b41dc1b25a355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4251950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d20bdf72f693e576a0cd81e6fac8a17c4e63c452a4d29fe083119ddbe58d8c`

```dockerfile
```

-	Layers:
	-	`sha256:0fb06403282ad403e010f7afc29601a8b910b4c05a8de46bd78739fca300b252`  
		Last Modified: Wed, 02 Jul 2025 15:43:05 GMT  
		Size: 4.2 MB (4233476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db07aedcaa653b6fd598a9e3d2a8b3809bb17363d859a053e8877b60db6b3b6e`  
		Last Modified: Wed, 02 Jul 2025 15:43:05 GMT  
		Size: 18.5 KB (18474 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein-2.11.2-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:52d4dae97834ce753a0a1c01bc73c26e2bbc9fb340b062679d7ee7d6a2d05689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.4 MB (173410208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90673995bce26692c0a69a6eeca38ef0d7aa9dfccaefbeafe29e31a70531e07`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:43faa9a2f25436afce0db8221e3c0e223102f73a33b0cd47eb32294e8033b203`  
		Last Modified: Tue, 01 Jul 2025 01:24:44 GMT  
		Size: 28.3 MB (28258970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e419a52d0b7166273c72df76079f5355fbec04834338cef62e248098795964`  
		Last Modified: Tue, 01 Jul 2025 03:38:20 GMT  
		Size: 87.6 MB (87622190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9e35fba85db9cf2adab38d6816c630bbf44081fcdfb956c1ad0ad2c978405c`  
		Last Modified: Tue, 01 Jul 2025 03:38:18 GMT  
		Size: 53.0 MB (53014387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55f04f202e8fb7b2c3eefa427efa370595c9bd386e4acedac3ed8a6225289aa`  
		Last Modified: Tue, 01 Jul 2025 03:38:16 GMT  
		Size: 4.5 MB (4514233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c24fe9cff17cee61d1981e026ad02e027ba950a2efa185719e9f634c1b87c3`  
		Last Modified: Wed, 02 Jul 2025 09:30:29 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-2.11.2-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:999a388d312c05f0c69330fb62d801923cf8f6721757cc8b62af0a408c77209c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc7f756243a5688f894e0d6ee51c2366339fc89648739106b752022951f166f`

```dockerfile
```

-	Layers:
	-	`sha256:313c1aaf5a8e4d604c8a5ed600cf3b8fa5125ba6441059ca79d09796d6403ca5`  
		Last Modified: Wed, 02 Jul 2025 12:40:33 GMT  
		Size: 4.2 MB (4217488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a5b874afe9d35e25ec2f21b16b5d5da5e6c86398adf715903aa74dcc30a1af2`  
		Last Modified: Wed, 02 Jul 2025 12:40:33 GMT  
		Size: 18.5 KB (18475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein-2.11.2-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:550ae49dbcd98f5af7235c6e400f2895e7c82d0384cf4258cab5bfb07503722a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.4 MB (174442952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc4b598f530a4273db341dc2d5a18f73f8672d8f838d79dc5d0758e4f0c54b22`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:728fbd29b8599bd56dcb8703b5c428523bcf0f3d48c5e95804f60267a128a3bc`  
		Last Modified: Tue, 01 Jul 2025 01:19:25 GMT  
		Size: 29.8 MB (29838345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105179baa40c85d8521707990861ebb0b6d40818c639c5026c7c305780a59f4b`  
		Last Modified: Wed, 02 Jul 2025 06:59:58 GMT  
		Size: 85.2 MB (85216920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f851c863ebbe1d818222df7fa0b45c5617b8bbd919590188f7cd161366fc1af5`  
		Last Modified: Wed, 02 Jul 2025 06:59:55 GMT  
		Size: 54.9 MB (54873069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0cb975af94067f866e767794af1a10f458835ec50a058221f7523f6099d4b14`  
		Last Modified: Wed, 02 Jul 2025 06:59:50 GMT  
		Size: 4.5 MB (4514190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321dbc426a17a40279aa3e5cd106efc538a6b33e702e64d03d1bcc37aec3b8f8`  
		Last Modified: Wed, 02 Jul 2025 06:59:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-2.11.2-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1de62d2f37b2ea6457b37f6fe53835b11efe4f7339bd673b763448ea89bb791c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4245070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4695ee56a1624e1a628af560b135ccfd55de582a7767d6a16f40132cdbaa5e2`

```dockerfile
```

-	Layers:
	-	`sha256:0e4f0411fcdfcd77f0fe3478186f572ac4a8527854df77fff021ba1be1e03b2f`  
		Last Modified: Wed, 02 Jul 2025 09:41:09 GMT  
		Size: 4.2 MB (4226639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4bc98dad03edfe98d09f416e2e6697ca1c8cd242371f6814062ca6972dca4cf`  
		Last Modified: Wed, 02 Jul 2025 09:41:09 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json
