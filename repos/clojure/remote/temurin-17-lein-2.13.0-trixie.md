## `clojure:temurin-17-lein-2.13.0-trixie`

```console
$ docker pull clojure@sha256:2bff6cf9f961679323a8b7189bef5e8dd41c592409bf515cb421f9edd19f3252
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

### `clojure:temurin-17-lein-2.13.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:00338c42b0898f9e633a91ff994e5880f7a540bf2a6d0d6eb76eeea518444677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 MB (218618566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29c1c87c45d8e485fe453de1f8efdd6399df0c17579b68a2e5a71304e8f3ae1e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:34:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:34:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:34:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:34:56 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:34:56 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:34:56 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:36:11 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:36:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:36:11 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:36:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:36:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:36:13 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:36:13 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8e19437d9443fb412455bbf7dfc36827f9c30e24a4ada4a22d5e867fc49522`  
		Last Modified: Tue, 16 Jun 2026 23:36:32 GMT  
		Size: 145.9 MB (145905445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8fd9d11a5304ed0bd9f1e48c3da5a65790c3c6e9189da2f3a93639783db3e2e`  
		Last Modified: Tue, 16 Jun 2026 23:36:31 GMT  
		Size: 18.9 MB (18880354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83a211291f4963faefad4476101e8b8bbb80bfbdf74d426bc683e432279ab86`  
		Last Modified: Tue, 16 Jun 2026 23:36:29 GMT  
		Size: 4.5 MB (4515217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97752d643fd67cfdaa60ba416a6bd2e54f91d878b53583703dfb8c41c86c4dc0`  
		Last Modified: Tue, 16 Jun 2026 23:36:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.13.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:efa5e2effcd519ae62298adb0ba67172400293480842a62c3aa5b33f0fbf6c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00e3eff4f3e48e2c25df29d1cf5563fabf39ea434ada8b1857cf87e96474636`

```dockerfile
```

-	Layers:
	-	`sha256:36dbdbfc06cd9dc0c6c34d47a688c970d7c1a08d79c2842f2aaf88a9c904548e`  
		Last Modified: Tue, 16 Jun 2026 23:36:30 GMT  
		Size: 3.8 MB (3817820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3ddd2d71bd38c44e74359bdbf58d393c1dfbd0b17eefdb650f3e6eacd1b9619`  
		Last Modified: Tue, 16 Jun 2026 23:36:30 GMT  
		Size: 17.7 KB (17718 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.13.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6c912238a3f4191a97f518a3956a795c1d2cb42f4270281286b456f5f38bfa16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.8 MB (217757641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d819926efac1053a1e7755108b3fd7ed83848e31cdce23e5b75b4797d4e5ad1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:34:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:34:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:34:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:34:39 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:34:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:34:39 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:35:55 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:35:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:35:55 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:35:56 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:35:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:35:56 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:35:56 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694c68a43a3423248186f55d02b8ffebde0d89830cc65dfe7ece4d4c9d9511a0`  
		Last Modified: Tue, 16 Jun 2026 23:36:16 GMT  
		Size: 144.7 MB (144724336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1666b5b694260aed7d4b0309673f01c9a2999db693ab9313f92851a62f3a35dc`  
		Last Modified: Tue, 16 Jun 2026 23:36:14 GMT  
		Size: 18.8 MB (18839498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9a61624cb5f2301f4e01db409c016671cacbae0b28b9213793fdb784354e32`  
		Last Modified: Tue, 16 Jun 2026 23:36:13 GMT  
		Size: 4.5 MB (4515208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1737ad1fe525c06c028b6b7ee563062aa02f3df463b8b91ce65162f03e50e4fc`  
		Last Modified: Tue, 16 Jun 2026 23:36:13 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.13.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:71533397afd09f61d18609f881f39732e382ee90f14152d7818c541a7a00669b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f635222f13b52df7f63b04739eb914022afbbda58c851ac6ae2f513ef5b05b1`

```dockerfile
```

-	Layers:
	-	`sha256:e866fe2dfdc6894364f1c808ff9830a7a75987595e7a6057a31b4cc6338f7b32`  
		Last Modified: Tue, 16 Jun 2026 23:36:13 GMT  
		Size: 3.8 MB (3818060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:175ac7d209666aed9072b0626d6836f6b6ec64e9bd8bc6301621f5dd85d0f5a2`  
		Last Modified: Tue, 16 Jun 2026 23:36:13 GMT  
		Size: 17.8 KB (17839 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.13.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:aa2997ed5d527b015c785a507f06e4b74f387e9f726ab2629013b0295d5ca111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.4 MB (222356303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7de7649106aed0d4a39c75a315a71f49668eff2e7ab135629f8f8f965fef7b9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:48:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:48:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:48:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:48:59 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:48:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:48:59 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:51:36 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:51:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:51:36 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:51:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:51:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:51:39 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:51:39 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:fc2380819f7227178ecd607b245c244d8811737f42c6112caf011a01a3889a8e`  
		Last Modified: Thu, 11 Jun 2026 00:24:43 GMT  
		Size: 53.1 MB (53137939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed3d97dd025f914f8a14a5c18aa1876d5300ef1a094c3a1b87be22f0b189f28`  
		Last Modified: Tue, 16 Jun 2026 23:52:17 GMT  
		Size: 145.8 MB (145766159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe2d8d53d90546a07d8078ed5bde5c357de8b3731118bb2909a6413c662b412f`  
		Last Modified: Tue, 16 Jun 2026 23:52:14 GMT  
		Size: 18.9 MB (18936563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40af2ecc1f5700a277133d1c848bfaccd671494195358e35dc6fe8d8569bb573`  
		Last Modified: Tue, 16 Jun 2026 23:52:13 GMT  
		Size: 4.5 MB (4515212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1c043c4a3f95c192577faa2b1ade03359e0a5ee74602966c09ee8ced6e9a9d`  
		Last Modified: Tue, 16 Jun 2026 23:52:13 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.13.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e2d9c40b23462e9a66e20e920c7021a7da6e3cd65ae658a8464b57b578348716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a60edfb2c6579f4d9f1ab249e3be88010846c0204f63e8d86547dbe96848a293`

```dockerfile
```

-	Layers:
	-	`sha256:50ba15e760aa968678c18bcd85fa6f9d27c2581b8dd9c368b95df1f3398edb72`  
		Last Modified: Tue, 16 Jun 2026 23:52:13 GMT  
		Size: 3.8 MB (3818820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16d5814cfec479d7eab5dc9499377552660deec8a7d7f7b7ac4794dfb0700015`  
		Last Modified: Tue, 16 Jun 2026 23:52:13 GMT  
		Size: 17.8 KB (17762 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.13.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:c586b0b494d0802d6292b15d4e2d45b60e5829f6edfe35b71ed5174bfb584774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.7 MB (208734043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76e15ca3dedb239e6bff8973ece74509bf7954d62b466a08da2538a38b13c04`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:35:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:35:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:35:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:35:07 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:35:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:35:07 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:36:19 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:36:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:36:19 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:36:21 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:36:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:36:21 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:36:21 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0ebf827318debac5b829e4cd5c36e0122490cf2392f532aa02b2b0999d5c1b37`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 49.4 MB (49385897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659a6777b5012e898ab89bb60abb007df6038d89345343823bf1a65797f143ee`  
		Last Modified: Tue, 16 Jun 2026 23:36:50 GMT  
		Size: 135.9 MB (135910370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d34523775f8a25a1eab659d896a379f464279c4a022cb6144c98cd86aca7f60`  
		Last Modified: Tue, 16 Jun 2026 23:36:48 GMT  
		Size: 18.9 MB (18922132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47599e0421247127d4d040ec531ae66b94b1d0383f24cd50bcefe59db8cafe54`  
		Last Modified: Tue, 16 Jun 2026 23:36:47 GMT  
		Size: 4.5 MB (4515214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2125fdf7ffbcd4d8ceb7a31a4626d849f0b7011e6b9d73c646c284d45e954ec1`  
		Last Modified: Tue, 16 Jun 2026 23:36:47 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.13.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ce5bd42f513f9c153a43576143414f43c312f7ee46473a8bbcd8046151861793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3831965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f0eddf103ecb0fb7bdf46a17cbeb56f4e97f7ad649d8971d47f386a6cb91112`

```dockerfile
```

-	Layers:
	-	`sha256:628864c631fb2d9410736af3d56dc665f877e7e074440d3420de6c63f992fbbb`  
		Last Modified: Tue, 16 Jun 2026 23:36:47 GMT  
		Size: 3.8 MB (3814247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a78a5d27dfd9d89271343975eaa0f57705d8914907df8799176ded982b76739`  
		Last Modified: Tue, 16 Jun 2026 23:36:47 GMT  
		Size: 17.7 KB (17718 bytes)  
		MIME: application/vnd.in-toto+json
