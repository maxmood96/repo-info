## `clojure:temurin-17-lein-trixie-slim`

```console
$ docker pull clojure@sha256:48a79cfe549108841be55bed81cc22a3da52c969048a06783d1e93c4f2c49e30
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

### `clojure:temurin-17-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:537156b992045d7c664cd716550ae7e4ccd3ed2bfebf09c7e67ac5abd080d85d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.9 MB (196949005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:401708fb61e01f13d206e541632f690a9a251b76f035f5448a1d8262e236c41b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:34:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:34:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:34:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:34:55 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:34:55 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:34:55 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:36:11 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
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
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8e19437d9443fb412455bbf7dfc36827f9c30e24a4ada4a22d5e867fc49522`  
		Last Modified: Tue, 16 Jun 2026 23:36:32 GMT  
		Size: 145.9 MB (145905445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e7a1eef5080d4ff236bb6659b9a11255e7e0b45e240aa296c4d0a6739edc05`  
		Last Modified: Tue, 16 Jun 2026 23:36:30 GMT  
		Size: 16.7 MB (16742499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83a211291f4963faefad4476101e8b8bbb80bfbdf74d426bc683e432279ab86`  
		Last Modified: Tue, 16 Jun 2026 23:36:29 GMT  
		Size: 4.5 MB (4515217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97752d643fd67cfdaa60ba416a6bd2e54f91d878b53583703dfb8c41c86c4dc0`  
		Last Modified: Tue, 16 Jun 2026 23:36:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:aed0c6901514f811f7cf4d4162be4b3c5f111e9459f536f3a90603551dd409f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6937f897e0c5c340339536311e7d85f476c863b9e18600fc80173fc328acb09`

```dockerfile
```

-	Layers:
	-	`sha256:24c3bad36eb53c5058d5d0d5be0fbbfc66fdddfe49a2277c7cb6576da399201c`  
		Last Modified: Tue, 16 Jun 2026 23:36:29 GMT  
		Size: 2.4 MB (2367081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d8d16c7c17e63dabe9e7ad280ee3a97a9c21e6fc01fb708a82810ab5b90a1d8`  
		Last Modified: Tue, 16 Jun 2026 23:36:29 GMT  
		Size: 17.8 KB (17753 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:aff0706cb1a0281cef49e2a00666fc655028df75f2b384099495d4ca67777caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.1 MB (196099974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583bd7b210393502c38af40e29fdf1a076ed43d897ba5ed84db470e162593230`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:34:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:34:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:34:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:34:47 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:34:47 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:34:47 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:36:02 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:36:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:36:02 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:36:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:36:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:36:04 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:36:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7fc41172e4ccfd7a5b29d28be147dc3fdaf27fee745cd388dffd0f1097e4aa`  
		Last Modified: Tue, 16 Jun 2026 23:36:23 GMT  
		Size: 144.7 MB (144724358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8e5b992bb250e26567564c8010b2eef94d1e2af4651b4c4958c5fd408ee9bd`  
		Last Modified: Tue, 16 Jun 2026 23:36:21 GMT  
		Size: 16.7 MB (16711462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8287041f444bd84472fd96a664dd3e7376db9ad31710bd181fe72bcc7aeb9217`  
		Last Modified: Tue, 16 Jun 2026 23:36:20 GMT  
		Size: 4.5 MB (4515194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af22a9b884c471e850d2ce5d331ca7e6e9c8dc8106af287ad262ece713b1bd7`  
		Last Modified: Tue, 16 Jun 2026 23:36:20 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fdaa934afc684c9987261f5fdfe0c3f29066112e43d4df252a4eed5984dbc2cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2758e089691aa43f7e2126de360b98273fd331db749ed3593ea1de398443acbf`

```dockerfile
```

-	Layers:
	-	`sha256:72ab210ad564198d26cbaaa122e98c4caf83cf7861afa6a0fa3dcb1445f4384d`  
		Last Modified: Tue, 16 Jun 2026 23:36:20 GMT  
		Size: 2.4 MB (2366691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd8cc857b53511851212e08ab01deb390657da61cd1251f7b816ba288f4be61c`  
		Last Modified: Tue, 16 Jun 2026 23:36:20 GMT  
		Size: 17.9 KB (17873 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:42e2d9cd776b8f9acb9659e0ee49b7ce7bcbe7fb3da7f98d1c67330a21daa131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.7 MB (200670400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e94c1ba0874e5b3189497178d02bc15fffd72ef5f43feddc6e384958ee73006`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:50:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:50:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:50:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:50:49 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:50:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:50:49 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:53:33 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:53:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:53:33 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:53:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069cd8d0e7627fec8f8f8e70662122bbb64ff72da415feca098cfc3cc453477c`  
		Last Modified: Tue, 16 Jun 2026 23:54:11 GMT  
		Size: 145.8 MB (145766113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab7a9f7ff159abf583263142d63ddc1cc86679dc968bb0b869468d272e484b2`  
		Last Modified: Tue, 16 Jun 2026 23:54:08 GMT  
		Size: 16.8 MB (16782296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3ef8c71852c8367b32ce99bd0ea48223da3468d6e713e4214cf49bd00aa521`  
		Last Modified: Tue, 16 Jun 2026 23:54:07 GMT  
		Size: 4.5 MB (4515222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f0e4c28b39acc441467c338d88cd6c7f4f31e8b3ab0a17f6901e30c062d1ff`  
		Last Modified: Tue, 16 Jun 2026 23:54:07 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:03ce3a14c1814a49730420c926faacfaf55c0115b1a77e5ab53842d92ea94d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e957ab04acb4ba5ae912e189a9e9bbdce263179d273b7a875a68dfdc313c274`

```dockerfile
```

-	Layers:
	-	`sha256:5d7fcc6e031459194efbef51959b8c9269e56c8abb19cd6570e77115a385a96a`  
		Last Modified: Tue, 16 Jun 2026 23:54:07 GMT  
		Size: 2.4 MB (2368061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46049faec973a6ebdf83b409ac6460fc836080fd8bb434e03f58626dbe04a455`  
		Last Modified: Tue, 16 Jun 2026 23:54:07 GMT  
		Size: 17.8 KB (17797 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:d6656c5bd14b3bdf1aa4ee1946dd5984035209ac0053cd18bde59209ad7167f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187057525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:013e63ed95f4174f4d2461539e80b11abb43408699098ddd5df8e8a3d77f3b8b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:35:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:35:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:35:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:35:49 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:35:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:35:49 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:37:01 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:37:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:37:01 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:37:02 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:37:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:37:02 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:37:02 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a444f5af1920c9789e670823ec9c5edc2487cf979dc8f1838a28788c7ba04a0`  
		Last Modified: Tue, 16 Jun 2026 23:37:30 GMT  
		Size: 135.9 MB (135910410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6660a1da4b910083847373cd781fc578cd8ba49ef59c36cf301b247f71dfe18e`  
		Last Modified: Tue, 16 Jun 2026 23:37:28 GMT  
		Size: 16.8 MB (16780141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1256405baefa8e72184f4f2110ba0b77dad4408f7ea517ea1e921b92f502181`  
		Last Modified: Tue, 16 Jun 2026 23:37:27 GMT  
		Size: 4.5 MB (4515189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e0e424b0111e6eb57e6fa8c03b97944da4b5006ec301b70ac53cf6f24743cb`  
		Last Modified: Tue, 16 Jun 2026 23:37:27 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:836edf0d57cd728e8fc84a66b5e861d20c10f75450fb265088af6bd59517af03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9651b635e284e6f6a2a74d4325a44410f5035028b9e9446891ca234fdd88562c`

```dockerfile
```

-	Layers:
	-	`sha256:b9f80741e139119b5835647875287a07bf6aa4c959528a549fdcae1bbd17f779`  
		Last Modified: Tue, 16 Jun 2026 23:37:27 GMT  
		Size: 2.4 MB (2363508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02181b9eaeae9700a2d7fc93f544c4aaa997a7114e0322a688b98da971b86408`  
		Last Modified: Tue, 16 Jun 2026 23:37:27 GMT  
		Size: 17.8 KB (17753 bytes)  
		MIME: application/vnd.in-toto+json
