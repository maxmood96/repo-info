## `clojure:temurin-11-lein-2.13.0-trixie`

```console
$ docker pull clojure@sha256:9c2335eceedd7f555d34c785fd3848bf2aba32bc6bf29ca5e79a93f1ad358a2c
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

### `clojure:temurin-11-lein-2.13.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:44d7edd90e454d56762abefed0179117a5e34269bf28915312bc63b8607b4248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 MB (218598426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7ec3236273269c1596366b1bfc28dcccf90ab7bffbed79f295fec6c2c8dc02d`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:15:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:15:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:15:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:15:25 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:15:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:15:25 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:16:38 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:16:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:16:38 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:16:40 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:16:40 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d51e24fcd2b8eb4381a7eb3e25cdea53484cf080b331b32f4321d2df244e059`  
		Last Modified: Fri, 19 Jun 2026 02:17:00 GMT  
		Size: 145.9 MB (145886162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa889d620626569ff6b7d4f99b1504abd34a0c6b8621a9c7c6c0fe0a2f06d660`  
		Last Modified: Fri, 19 Jun 2026 02:16:56 GMT  
		Size: 18.9 MB (18879895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b343bdb05a68b6b50d9dec1d4f386adfa6ea5157f6d8080c86c9e910f2529e59`  
		Last Modified: Fri, 19 Jun 2026 02:16:55 GMT  
		Size: 4.5 MB (4515216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.13.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:689e0373314c86c6b784f3a0eb2b91e0951938f2b794389bf72282b2c8bd3758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3853070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cc2834c21428c60474f30efda9226cd519d131cef26145a7e94a5aba0920b2a`

```dockerfile
```

-	Layers:
	-	`sha256:9128f2a7f5c9a6db48e015297400db6ca5184c35d1e1a56ad8c6ef368b933861`  
		Last Modified: Fri, 19 Jun 2026 02:16:55 GMT  
		Size: 3.8 MB (3837336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4e77d4d2761932917fedd38227b5f19423854690571a2ecc3086e617658287b`  
		Last Modified: Fri, 19 Jun 2026 02:16:55 GMT  
		Size: 15.7 KB (15734 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.13.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:02898182d91196e7bca0e90a07a22a13a2aed1a30427210ee5a2861b831ffa4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.6 MB (215615138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0ae04841617fcb3c75b6ffd82e75037609df7df8e407652bca8f577fc02058`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:15:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:15:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:15:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:15:52 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:15:52 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:15:52 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:17:08 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:17:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:17:08 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:17:10 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:17:10 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8b76aaab1e87ab47f1275b0bc7769c7561073f2123c9db7ef3f81b0159ac3f`  
		Last Modified: Fri, 19 Jun 2026 02:16:31 GMT  
		Size: 142.6 MB (142582158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b4a7f07b97e458a493d757de066f2189413e0d425292046aa2f2c84da98b50`  
		Last Modified: Fri, 19 Jun 2026 02:17:27 GMT  
		Size: 18.8 MB (18839551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea79a91f792378bd42f51cc7ed2085e009802ef5c5f83d91f0f77309f6fcdabe`  
		Last Modified: Fri, 19 Jun 2026 02:17:26 GMT  
		Size: 4.5 MB (4515228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.13.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:bf3f9594964e1f572aa576e637768681d74d87f005e941e6010a5388073d523a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3854049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a713ae1e7db0014327536da62d680f7349277b61f1123bbb462da8074799670a`

```dockerfile
```

-	Layers:
	-	`sha256:cb2d10cc760107a92ec453795dda61d13a4c4e5a1151782ebb723f0fae83a4b5`  
		Last Modified: Fri, 19 Jun 2026 02:17:26 GMT  
		Size: 3.8 MB (3838194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e9178920b8c0f3a7121ddec710b9def2f36dea7524cb97fd0a55a54610bf638`  
		Last Modified: Fri, 19 Jun 2026 02:17:26 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.13.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:296fc97ceb29a73c8c3e0f5c0acfd0b658045ed3aa1576c3b907c95fb23bf005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.7 MB (209700181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0cf6605387afd92c734944f1f7efa819cb79341e576bb2debc5e9110a6d29ac`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:28:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:28:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:28:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:28:46 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:28:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:28:47 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:32:01 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:32:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:32:01 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:32:05 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:32:05 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:fc2380819f7227178ecd607b245c244d8811737f42c6112caf011a01a3889a8e`  
		Last Modified: Thu, 11 Jun 2026 00:24:43 GMT  
		Size: 53.1 MB (53137939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c757e25eae7c582cfef76c30181fc527b42e7b29239bda1a4edb72b6b1ee22ff`  
		Last Modified: Fri, 19 Jun 2026 02:32:44 GMT  
		Size: 133.1 MB (133110616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705138ea13377438f3eb070b2fae51c0dd70212ec3066aa3293c3499cd87534c`  
		Last Modified: Fri, 19 Jun 2026 02:32:40 GMT  
		Size: 18.9 MB (18936379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79dfcbafe8f03f8d9a2c90d261fb14d29dffe52de4f921cd6c9ba8617ab63019`  
		Last Modified: Fri, 19 Jun 2026 02:32:40 GMT  
		Size: 4.5 MB (4515215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.13.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:dc5520ac888f7da2f69f00c5403e5e97bc0cd7490b6222d342d99a507cf68210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3853499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e539417113b6f688c6b18f54439aa2cd316f236dea2faf0db1b5c9f20b2c1497`

```dockerfile
```

-	Layers:
	-	`sha256:c64da1b2afdb8ac383a9f04114ce7d0ac6bb49ef2f31e1388159d84f32098d1c`  
		Last Modified: Fri, 19 Jun 2026 02:32:40 GMT  
		Size: 3.8 MB (3837721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49614cbe7baf3af07c853e56adf559b8a27de824b7b06e6ffdfb9f8dabd15ca2`  
		Last Modified: Fri, 19 Jun 2026 02:32:39 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.13.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:84f7d0116e4d5229c14e1b483d3c3ec578c6b954c3a906e630672c7ebf8bffb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.5 MB (199475405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc7c5e0602273f6d9fc0f40faff7f0b08ab1cb75db802581f68f500c8c20142`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:13:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:13:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:13:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:13:59 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:13:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:13:59 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:15:29 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:15:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:15:29 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:15:31 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:15:31 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:0ebf827318debac5b829e4cd5c36e0122490cf2392f532aa02b2b0999d5c1b37`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 49.4 MB (49385897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a393e938c4fde8ef93dc40c992c3d1e85ca370fd167d582340e3b1c41dfbca85`  
		Last Modified: Fri, 19 Jun 2026 02:15:56 GMT  
		Size: 126.7 MB (126652563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b9722e8d9a31919cbef0bfef3f6dc2997f93a29893848f058c63a2dd83cd0e`  
		Last Modified: Fri, 19 Jun 2026 02:15:53 GMT  
		Size: 18.9 MB (18921706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e005ebf1f79c61705e83b4acb40975a6c90a51845386d7894b0d4ab2f7473ad5`  
		Last Modified: Fri, 19 Jun 2026 02:15:53 GMT  
		Size: 4.5 MB (4515207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.13.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f8db6b3c9dcc538e066f18d890ac5563f65d6f543affe2ab96e8c7b5fea23f37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3849501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55643af825ebbaf2cd3661481d895fcf922d4b0416b17a5b59936a017a08e321`

```dockerfile
```

-	Layers:
	-	`sha256:d8afc1f84acec75424080494e81adfafa60f9c4ca73f5e6b985f4477a00bfe28`  
		Last Modified: Fri, 19 Jun 2026 02:15:53 GMT  
		Size: 3.8 MB (3833767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f1b7741d75f92d96b110aaa229dedc1dccc5e0d3c3539bcb50e78aa5cccfba4`  
		Last Modified: Fri, 19 Jun 2026 02:15:53 GMT  
		Size: 15.7 KB (15734 bytes)  
		MIME: application/vnd.in-toto+json
