## `clojure:temurin-21-lein-trixie-slim`

```console
$ docker pull clojure@sha256:a8581e7480bfb5250fc7871dedeb27c3cff2eaa79bb2e456b1195199fedb753b
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

### `clojure:temurin-21-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d45f50d2a891341b7149c8496e0a730e2472a22a6a41d2b9d60a232e1be65157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.2 MB (209210649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a5ae535e0f7b8fcdd6b6bc095dc24656cfd5ebd696dc6d2a08aaaad6b358fcf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:36:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:36:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:36:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:36:31 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:36:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:36:31 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:37:47 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:37:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:37:47 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:37:49 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:37:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:37:49 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:37:49 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089c9115a1092e7de6fa8be0f3c9c09472a9a1d58be2fc6c8a2ee91b19590bbf`  
		Last Modified: Tue, 16 Jun 2026 23:38:09 GMT  
		Size: 158.2 MB (158166942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b8997257cac476f56068c7cc7814078a71e76e1ab8add569d935c2704485ed`  
		Last Modified: Tue, 16 Jun 2026 23:38:06 GMT  
		Size: 16.7 MB (16742667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2c677318e316d5b705c7845586240dbc768af20c5f9b084d22d446b9798248`  
		Last Modified: Tue, 16 Jun 2026 23:38:06 GMT  
		Size: 4.5 MB (4515194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98f939257681a17d968323cc3015d7fc953ddc8853d4b7c753a58786438fb56`  
		Last Modified: Tue, 16 Jun 2026 23:38:05 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:baa21d9b906a63ba29c88d17c272421131607f1db2bda6ac98940058e1984b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfce45cf132aa233d4c510b632cc9d76fe34df9ab85c3a274b937a24f8c30530`

```dockerfile
```

-	Layers:
	-	`sha256:a842bfe10e04a1e9015ab1c500678f63b73a39e2acfd4a8035a0798d37f4bddf`  
		Last Modified: Tue, 16 Jun 2026 23:38:05 GMT  
		Size: 2.4 MB (2368933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:963baf09a9732f87dce63b3155aff115e936f57f7aa0f8eb91ca446891e13e2a`  
		Last Modified: Tue, 16 Jun 2026 23:38:05 GMT  
		Size: 17.8 KB (17753 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:83dac299bcc91850fb6fd41d9dfd39bf30be549484a819c4d819283f69b55472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.8 MB (207837096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c82d1036235033150de78e9130851d140139a5f40b2660e3352cc1a13368e636`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:36:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:36:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:36:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:36:16 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:36:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:36:16 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:37:31 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:37:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:37:31 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:37:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:37:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:37:33 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:37:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8d444cb22ea01c73038b972783f1024b1d1cf05c6c6ffd6c1a812cba38ed22`  
		Last Modified: Tue, 16 Jun 2026 23:37:54 GMT  
		Size: 156.5 MB (156461291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb662f4493474f148ca90a562d77bd365b9541c2591c827d850ba8074010b8c4`  
		Last Modified: Tue, 16 Jun 2026 23:37:51 GMT  
		Size: 16.7 MB (16711641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69e616e7684e246a89ed031a897fad6f8fb79128519a6812ded8a0aaa37f086`  
		Last Modified: Tue, 16 Jun 2026 23:37:51 GMT  
		Size: 4.5 MB (4515204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3898ac9ce3ddba3490147e42910e53801e1fdfbadf4f1aba20622b8a383a01`  
		Last Modified: Tue, 16 Jun 2026 23:37:50 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ebab59c42b688cac840706f6d14c8caa77e1c7a17a789ffc0d19d1bd2e150bd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e681692249e5853fa5fe31badc08f25d645ebacb926ed78534d3d716c190a8`

```dockerfile
```

-	Layers:
	-	`sha256:5827f520cc35a05862f0f07a9da7aa99b051884192283396a207459816636336`  
		Last Modified: Tue, 16 Jun 2026 23:37:50 GMT  
		Size: 2.4 MB (2368543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a9ef961d89d1ecf05e6c730ac7a129b22c16d44ada0dbd0052d399f660c8ac7`  
		Last Modified: Tue, 16 Jun 2026 23:37:50 GMT  
		Size: 17.9 KB (17873 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:3f0fea328d22611575f458c90fe86bef4de053b5817f343e9591816971371b98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.2 MB (213247590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0dae320f65ea2e165e33a21f74c0cd964133416c8ea39d69d3bca18819856fc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Wed, 17 Jun 2026 00:00:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jun 2026 00:00:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 17 Jun 2026 00:00:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jun 2026 00:00:47 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 17 Jun 2026 00:00:47 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 17 Jun 2026 00:00:47 GMT
WORKDIR /tmp
# Wed, 17 Jun 2026 00:03:27 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 17 Jun 2026 00:03:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 17 Jun 2026 00:03:27 GMT
ENV LEIN_ROOT=1
# Wed, 17 Jun 2026 00:03:31 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 17 Jun 2026 00:03:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 17 Jun 2026 00:03:31 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 17 Jun 2026 00:03:31 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cae30f60cd0ec6ba95234bc9baf8b715de9cca5a8c7483a3f4eebc08e9456b2`  
		Last Modified: Wed, 17 Jun 2026 00:04:10 GMT  
		Size: 158.3 MB (158343250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ecab9349ceb2918e3b2fb0e2a1b9bf4bc3113ebdb9f963e67d351f15e9835c9`  
		Last Modified: Wed, 17 Jun 2026 00:04:06 GMT  
		Size: 16.8 MB (16782386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc85fb5220f648344b5a97a51eda13fd644755fb75eafdd40b1a03353c9f5fe`  
		Last Modified: Wed, 17 Jun 2026 00:04:05 GMT  
		Size: 4.5 MB (4515185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1132a529849969ec5395c2ad6eae1493086320b0c51cb6cab5f46bc82318cb`  
		Last Modified: Wed, 17 Jun 2026 00:04:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:345ceb657462c61ba4033562861c66b475d32e697dcf48d3e3c3a723109c06c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2387710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b2660f96804716029269f3dd562884e338fc3927a05eb920f0f5b86bf6e267`

```dockerfile
```

-	Layers:
	-	`sha256:ffebad513ffb9e99d663b718e0ac3f667f45df028ca486e1523ec2ac93c4a74d`  
		Last Modified: Wed, 17 Jun 2026 00:04:05 GMT  
		Size: 2.4 MB (2369913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:904e8821153289f54d68135bf9d12889f2242249a1def3a88b6f8bca55de4683`  
		Last Modified: Wed, 17 Jun 2026 00:04:05 GMT  
		Size: 17.8 KB (17797 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:80560e952d4f233de843c963e1747a93fbaf8beaa7db1899d36e16008b2834d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.5 MB (198535018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695212a4f4b938a7d61f0a95291b67b7f1c6b795b72c795be987b17366a3a3c3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:38:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:38:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:38:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:38:51 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:38:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:38:51 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:40:04 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:40:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:40:04 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:40:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:40:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:40:06 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:40:06 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e66d9375a62e658d5255a5581f80c6f86b82e7d20e6a5c6878c2e0220d54700`  
		Last Modified: Tue, 16 Jun 2026 23:40:34 GMT  
		Size: 147.4 MB (147388338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a591815a1c96260572f72ad9e7b60e296717e36c2a433c0da2a45d40931e6f5`  
		Last Modified: Tue, 16 Jun 2026 23:40:32 GMT  
		Size: 16.8 MB (16779695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ee544c84d46e11562e572ece00dd9d3a2ba7dc62be33f607f6cf9647d62bd7`  
		Last Modified: Tue, 16 Jun 2026 23:40:32 GMT  
		Size: 4.5 MB (4515201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e41e633d46d77d12113b18c609b64884cddd36e1eb7c1fd2ef3b8e1d820a1c`  
		Last Modified: Tue, 16 Jun 2026 23:40:31 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:72503063d9686958035058d68a492862af8d2220e3cf276ab38f1454d1fa2416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2383113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea2d16d82510cf69f49efef7cf2aaf9ec7f3dac8d5d32546a630301feb224ad`

```dockerfile
```

-	Layers:
	-	`sha256:274dc9b3539500741f642055e4947d9e91604666b4b3766de5977211efce5dd2`  
		Last Modified: Tue, 16 Jun 2026 23:40:32 GMT  
		Size: 2.4 MB (2365360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09b3c109ef4a910904e52f27b950637a079ba4164be027a84d8bbb2235ec7904`  
		Last Modified: Tue, 16 Jun 2026 23:40:32 GMT  
		Size: 17.8 KB (17753 bytes)  
		MIME: application/vnd.in-toto+json
