## `clojure:latest`

```console
$ docker pull clojure@sha256:c1ec7c266539a4a9312882b562542c11edf1091ebffb9628ea80aaa18f300b41
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

### `clojure:latest` - linux; amd64

```console
$ docker pull clojure@sha256:b3b4ebd83d378f96085e194fa7101e7bef8657d1fd7faf9b5540207051ef4800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233911379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:404667e0c23c7f7a4b9911d966f057354a928c3de20e5f198e9987e5b1807e6c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:13:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:13:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:13:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:13:48 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:13:48 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:13:49 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:14:56 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:14:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:14:56 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:14:57 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:14:57 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:14:57 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:15:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:15:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:15:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:15:09 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:15:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:425befdf76e52426879d2abe42093a00dca59a893e7b4fa2a7679b0180b71d4b`  
		Last Modified: Wed, 24 Jun 2026 00:27:40 GMT  
		Size: 48.5 MB (48502210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fadfeea07f1d91ff6abe5f0dd692dc356dafa1c2b993a09cef62bd0bc0165d1`  
		Last Modified: Wed, 24 Jun 2026 02:15:32 GMT  
		Size: 92.6 MB (92574611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe020da3fa0d6b1b3de0b3805a4cdf191b6113c96166d6db835680b7719bbb3`  
		Last Modified: Wed, 24 Jun 2026 02:15:30 GMT  
		Size: 20.1 MB (20107678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45d3d226a3e992b1baa6461a010cdf8380da344afa6a7139bc94c2a8d1bd6dd`  
		Last Modified: Wed, 24 Jun 2026 02:15:29 GMT  
		Size: 4.5 MB (4515172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c141b1a8331c177f0ea22de4aa0836c7aa52e2cc6f04ebef37e6d9649dc91765`  
		Last Modified: Wed, 24 Jun 2026 02:15:32 GMT  
		Size: 68.2 MB (68210638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56538fee4a382268f1b834c79b7b232766c48230761de3962887dcd378655298`  
		Last Modified: Wed, 24 Jun 2026 02:15:31 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a532e15561e243fe13e9977d26dc6970c6641159ce0b744ed482be97f52d1982`  
		Last Modified: Wed, 24 Jun 2026 02:15:31 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:6967f07ee40915160ace3c3a3ba42a571395f9aca233ad0b1780d4d5a05dfc01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7460886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8da7f50c0dcb1b94bc43baf3dac7149bdd291eb7fac2d3b389a4e89c960c336`

```dockerfile
```

-	Layers:
	-	`sha256:8fc6c72cecb273026a7d1d55f24ccc860e94fc95f47581750f1720f7ba1209f6`  
		Last Modified: Wed, 24 Jun 2026 02:15:29 GMT  
		Size: 7.4 MB (7435911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f769a3f0eab2cff86d585ead9a971a56cf3330831c9058281f8c5bb85bb88897`  
		Last Modified: Wed, 24 Jun 2026 02:15:29 GMT  
		Size: 25.0 KB (24975 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ac973e04736feee41e72fb8f55f34c571bd23d0650c7acd66ce7a0096bda504e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.7 MB (232741995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:674e1d620c43085e1a00ab0a117a24b6db84b44f7707df18e8e043e76c7b82fa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:20:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:20:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:20:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:37 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:20:37 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:20:37 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:21:46 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:21:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:21:46 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:21:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:21:48 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:21:48 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:22:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:22:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:22:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:22:01 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:22:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0fb1189398e2e4b474d43aac6502510d0da0318e70137a377c21087f198814db`  
		Last Modified: Wed, 24 Jun 2026 00:27:19 GMT  
		Size: 48.4 MB (48389201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb1a01d07618944a985d757fbc70e42a6482ac039ae2c717de78405b7f027c1`  
		Last Modified: Wed, 24 Jun 2026 02:22:27 GMT  
		Size: 91.5 MB (91542238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37605868edcf4aab62142310c232461d0d3b85eb2971e439bf210d1a193c5fa9`  
		Last Modified: Wed, 24 Jun 2026 02:22:24 GMT  
		Size: 19.9 MB (19940269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b1e7c55a7f84b0c40e21b688651813e22b09d143a2d211e7232555e3ea6e05`  
		Last Modified: Wed, 24 Jun 2026 02:22:23 GMT  
		Size: 4.5 MB (4515226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3057e759002dece13ef188d36bbc79ec610e865f2eb50ce55c6f36b9338328d6`  
		Last Modified: Wed, 24 Jun 2026 02:22:27 GMT  
		Size: 68.4 MB (68353988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dfd8c5e4281c356439860c71976001111ced95c7535ca500f8f8cb4ca83eb8e`  
		Last Modified: Wed, 24 Jun 2026 02:22:25 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c451a1da3f23dd8512c6565c7815a12a3502efb7ee3efb0596ea5426138fe4`  
		Last Modified: Wed, 24 Jun 2026 02:22:26 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:3052021c1ddf328891e0f576cd750876dbd0cab2133771ba351e06d0a02944ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7466746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1188a623333279bf61303058335841458c17d40ffe36538501e99cb33a466bb6`

```dockerfile
```

-	Layers:
	-	`sha256:2b2f3a83698879abb46f91f8a2b324b4431705521b3c7baa9da499b99d7a87b8`  
		Last Modified: Wed, 24 Jun 2026 02:22:24 GMT  
		Size: 7.4 MB (7441647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27a7eb695040280fddb2e810038102ef7a60e9607b2e434bb02cf9b3932bb629`  
		Last Modified: Wed, 24 Jun 2026 02:22:23 GMT  
		Size: 25.1 KB (25099 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; ppc64le

```console
$ docker pull clojure@sha256:9f776d596afe3cbf652635270972a95a9588bbf9fa915ffc8d713e11c4f655b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242920865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd9b110ac059606dad89cfe16fa0b1f0ffc1f400f7fca7df54d7b44895fbd203`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:30:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:30:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:30:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:30:21 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:30:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:30:22 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:33:52 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:33:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:33:52 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:33:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:33:55 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Tue, 16 Jun 2026 23:33:55 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:34:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 16 Jun 2026 23:34:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 16 Jun 2026 23:34:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:34:32 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:34:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:88b94a58fac236a778527a3293ccd0ff4d309bff0bf314017ea5af603908fa2e`  
		Last Modified: Thu, 11 Jun 2026 00:21:34 GMT  
		Size: 52.3 MB (52346670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af2d7bc5e0f6f23b949f449ec38352dcc13ff43d0d262dab584e4f344eec386`  
		Last Modified: Tue, 16 Jun 2026 23:35:12 GMT  
		Size: 91.9 MB (91914009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68947c24a5e1c48feb5dfc5d4e28fe4f56550fcd7d0ffdaf1322d3ddb36f090a`  
		Last Modified: Tue, 16 Jun 2026 23:35:09 GMT  
		Size: 20.3 MB (20331869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7f1d5b8d6bc4ae48b7364827721c152758155257cfff4b80279cd72f3d6bf1`  
		Last Modified: Tue, 16 Jun 2026 23:35:08 GMT  
		Size: 4.5 MB (4515191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681ca53a2ea5923857d7bd3046b8635776ac9327e93b8476b7862b1690ae8527`  
		Last Modified: Tue, 16 Jun 2026 23:35:12 GMT  
		Size: 73.8 MB (73812052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ce5bc08975d0e839671137a7c2bb51320b950433317790cdd8ac9cb14ca325`  
		Last Modified: Tue, 16 Jun 2026 23:35:10 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb72dd97a652b682ba689394204a9a87d775b1aba31696034959d9216435764`  
		Last Modified: Tue, 16 Jun 2026 23:35:11 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:482b0cb47789ba3acb6369cd32c1937c328bcf80b3291764d636c6ca47f4ba61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7449442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55fc002db4352b59ff325a0cb2c315ee618054f28b5cd48cdc471b2a04592db`

```dockerfile
```

-	Layers:
	-	`sha256:aa8ba60eaf34e6e37a39d62b7ca53296bdd9bf57983acea1d0cca0dd7696ea81`  
		Last Modified: Fri, 19 Jun 2026 02:21:08 GMT  
		Size: 7.4 MB (7424427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a786af90727536f6091ae493bc5f1f7cbd2abb4b6f0f2631c25fa8970c9991b9`  
		Last Modified: Fri, 19 Jun 2026 02:21:08 GMT  
		Size: 25.0 KB (25015 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; s390x

```console
$ docker pull clojure@sha256:c3accfc5eeca746f7a2e5f4db03a7fa81baca5b7fad22dcb46813d68b1668962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.2 MB (227211061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf97c5a8f5bd5fbe2059faf2ce456017f4226856f68da7d1504a08bd2b90dfb4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 04:07:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:07:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:07:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:07:44 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 04:07:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 04:07:44 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 04:09:00 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 04:09:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 04:09:00 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 04:09:02 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 04:09:02 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 04:09:02 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 04:09:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 04:09:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 04:09:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 04:09:14 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 04:09:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bdd2e9d83d68023204331dd445067114dbd3500d2d496368624fa7ef81743d4a`  
		Last Modified: Wed, 24 Jun 2026 00:27:09 GMT  
		Size: 47.2 MB (47161675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42b02c985ff427f09da77745bd5599ec265500d0ffe9217e4629e6e410d74c2`  
		Last Modified: Wed, 24 Jun 2026 04:09:44 GMT  
		Size: 88.4 MB (88420330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5807e04f5849dd283ff540b02d07b6683180964ed3837e17d4bb24c987c5b6`  
		Last Modified: Wed, 24 Jun 2026 04:09:43 GMT  
		Size: 19.8 MB (19770663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1030fac02fc7fb6c91fdb9664b2131408274d0bb6c4fd223c0b7b0635b4163`  
		Last Modified: Wed, 24 Jun 2026 04:09:42 GMT  
		Size: 4.5 MB (4515219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9015e1c11b8997d8cb3a6ebedcfb018146cb209a3849670829e5525ec1915f`  
		Last Modified: Wed, 24 Jun 2026 04:09:44 GMT  
		Size: 67.3 MB (67342102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb1a924ce57071d0aa21998f1938fcd17aa979341d62eb0a21b63a4ecc350c6`  
		Last Modified: Wed, 24 Jun 2026 04:09:43 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b795bfa2d893b28e53bebe3048356b44ed1a82c1401d21e2baa249fded73a970`  
		Last Modified: Wed, 24 Jun 2026 04:09:44 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:c3a9070d51f0a2ffebafda788f1c027714d94fac20216e80f3d0857ab66652c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7436767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1645f75ab70fbde19b54a6c212370d5b128a00fec579768249f7078c32ea0c16`

```dockerfile
```

-	Layers:
	-	`sha256:5465bc1e007e16afde5c4dbdd195cf5c17d462fcdf7d1c34aece15b6b164bba8`  
		Last Modified: Wed, 24 Jun 2026 04:09:42 GMT  
		Size: 7.4 MB (7411792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98d427ee5ae228e816ed9d69d7535a21bb448c04d02cb6e4dbd21598133d3ce9`  
		Last Modified: Wed, 24 Jun 2026 04:09:42 GMT  
		Size: 25.0 KB (24975 bytes)  
		MIME: application/vnd.in-toto+json
