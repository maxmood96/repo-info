## `clojure:temurin-26-lein-bookworm`

```console
$ docker pull clojure@sha256:fb8927c31d8cb5117753931ba260c52fb9be724cd8922e9a07d1dd8ee05f171b
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

### `clojure:temurin-26-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:2bba909ee56e6f635b5288d470073785395185b817c416b3746c2e9aa0397d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.6 MB (167649812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6aa81cd3f1a3a13ccd2246efbbe1ca23d67bc61358d18f6dd6561180062c3db`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:37:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:37:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:37:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:37:58 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:37:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:37:58 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:39:06 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:39:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:39:06 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:39:08 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:39:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:39:08 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:39:08 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ddf23a54af8a95e072edd510bc9c9d0aa39ae811a3035c9a552bad9f848b881`  
		Last Modified: Tue, 16 Jun 2026 23:39:28 GMT  
		Size: 94.5 MB (94524364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633d6e77637141544ee66295d8c84a16b61e27e6615ac20e6c68b42731f712ca`  
		Last Modified: Tue, 16 Jun 2026 23:39:26 GMT  
		Size: 20.1 MB (20107762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e31addbe33761344b89763a85df8d759067acb1c7fbda8d2f6991658772fad`  
		Last Modified: Tue, 16 Jun 2026 23:39:25 GMT  
		Size: 4.5 MB (4515214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43c345887397b28a328364093becf0c52a8b8a29eb0503f2075c5095b77e95c`  
		Last Modified: Tue, 16 Jun 2026 23:39:25 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:62c20f0dad1926586de59546fe0f170f7032f82c1463dd0dbb605c253dc6be16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4267940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49d8988d5c0672621ed1df95386f2751fc01f4f138e3ff36375bc8349f0c7ae`

```dockerfile
```

-	Layers:
	-	`sha256:055e6be0be951508e874351adb9c54919b685fbbbca12a44f90c33717dc5b719`  
		Last Modified: Tue, 16 Jun 2026 23:39:25 GMT  
		Size: 4.2 MB (4249559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc9684db4fd66fe78d8c38812be3b5dcd647cab52bde12c8d5a6bbb5aa5db3e7`  
		Last Modified: Tue, 16 Jun 2026 23:39:25 GMT  
		Size: 18.4 KB (18381 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c6c2905061cd6b3b25a0b2953d499222345b518b8f816837349b01e3344e92eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.3 MB (166349466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b797d4301dc426b8f45e55b0bb6979390e59b8a4ef0937c91ba5ba857de8157d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:38:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:38:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:38:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:38:00 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:38:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:38:00 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:39:05 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:39:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:39:05 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:39:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:39:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:39:07 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:39:07 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49db32c834b5ef1de7f24acd9899a23f673349b681fa0b68c5927664e5b62f74`  
		Last Modified: Tue, 16 Jun 2026 23:39:26 GMT  
		Size: 93.5 MB (93504348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802886cfb0da5d75646b79cb9c5f4df25ffb7469167c4d5ce89ffe671a180cb5`  
		Last Modified: Tue, 16 Jun 2026 23:39:24 GMT  
		Size: 19.9 MB (19940506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae76a5bf29000015f0e999b520c2486938a73e9f56c59fa3a142436567e802be`  
		Last Modified: Tue, 16 Jun 2026 23:39:23 GMT  
		Size: 4.5 MB (4515167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3ca8360162359e8ed1d4ff325160c60676a62b77d5594c3190f40d5b800ab8`  
		Last Modified: Tue, 16 Jun 2026 23:39:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4e3d898551178ae94c0abf575dfe4233ade429ec600b48114f0f8515e98b862b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4267721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3b6a68b213c025cc3e24f2a116323281c9d5cffc3d6dcf4ecb99e32fd66911`

```dockerfile
```

-	Layers:
	-	`sha256:83fb9ada127289fd1a50caa558e343bab59f49c76f9e2d884f85f7b180d3c082`  
		Last Modified: Tue, 16 Jun 2026 23:39:23 GMT  
		Size: 4.2 MB (4249195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3577a953d63217410f959b6e1e5f579a493b357f5559c732c638aa93c6dd9283`  
		Last Modified: Tue, 16 Jun 2026 23:39:23 GMT  
		Size: 18.5 KB (18526 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:cf2188181dcf085141f0988e4ed1768372cf6945a5b59b21b2d1b7fa430f9210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171096405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab40800dbcc4110b9702abd3947ce9d6bcccee5261793d8f5d46d04c5f07b15`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Wed, 17 Jun 2026 00:07:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jun 2026 00:07:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 17 Jun 2026 00:07:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jun 2026 00:07:21 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 17 Jun 2026 00:07:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 17 Jun 2026 00:07:21 GMT
WORKDIR /tmp
# Wed, 17 Jun 2026 00:10:01 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 17 Jun 2026 00:10:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 17 Jun 2026 00:10:01 GMT
ENV LEIN_ROOT=1
# Wed, 17 Jun 2026 00:10:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 17 Jun 2026 00:10:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 17 Jun 2026 00:10:04 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 17 Jun 2026 00:10:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:88b94a58fac236a778527a3293ccd0ff4d309bff0bf314017ea5af603908fa2e`  
		Last Modified: Thu, 11 Jun 2026 00:21:34 GMT  
		Size: 52.3 MB (52346670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4759a87d2ab24b2fac4a2500d8d0888984823a78af74fea7debdc9f59a4aa41`  
		Last Modified: Wed, 17 Jun 2026 00:10:39 GMT  
		Size: 93.9 MB (93902050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438cc53d9667f2fae2cf6b81e25d13181a80615b69a51ecb6af55b0ce07dbfc4`  
		Last Modified: Wed, 17 Jun 2026 00:10:37 GMT  
		Size: 20.3 MB (20332041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724f86330d8c7e704aa8121678a6898fba98afa1958fdf22addd0c9fc1b01869`  
		Last Modified: Wed, 17 Jun 2026 00:10:36 GMT  
		Size: 4.5 MB (4515215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4d010da56d491c545e90064f0b0222259c84c59bcb739d6bb5e16079fabf8b`  
		Last Modified: Wed, 17 Jun 2026 00:10:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8a27a7e28c2cbf3c6d0d71fbadc94fce4a5a3fc7a47c563568c1e9c6dfbcb8fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4253805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf8c5d6de97f357f924c7dfa5b33b5edf1bae8b4470d5662faf22e82a2b9f20`

```dockerfile
```

-	Layers:
	-	`sha256:4404ed54a041981967840f561d6a6e39ee29e2e1c63668aa40e358a64b6778b6`  
		Last Modified: Wed, 17 Jun 2026 00:10:36 GMT  
		Size: 4.2 MB (4235368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce86c040bf1f8ade49b9547f6dbf68501575d8732382ee7819d5a59a120e21e0`  
		Last Modified: Wed, 17 Jun 2026 00:10:36 GMT  
		Size: 18.4 KB (18437 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:3e7a1064212ef9efd3b3019b838ceffb1c71049470544166c92994fbe7fecc71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.0 MB (161985309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b2a832ab6c1900942354697ff63ab20aad46e9e4cdedd7dfec6366a5adc3c69`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:41:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:41:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:41:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:41:21 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:41:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:41:21 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:42:25 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:42:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:42:25 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:42:27 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:42:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:42:27 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:42:27 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b041a55a85cc0e47dd570746852cc1b0fee042f3a03eb250b9f896ac4aa74a3d`  
		Last Modified: Wed, 10 Jun 2026 23:41:01 GMT  
		Size: 47.2 MB (47161500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aaf4ab9205bb640a8f57d3d886d8b4e29f83e17eef854c8f31a6f6915511560`  
		Last Modified: Tue, 16 Jun 2026 23:42:55 GMT  
		Size: 90.5 MB (90536964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5086737cab11dccf6d2be92cd75ddc69be9b1882dbe429513ceeeb9f34d816f8`  
		Last Modified: Tue, 16 Jun 2026 23:42:54 GMT  
		Size: 19.8 MB (19771208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa34c2d09a6e759329cd59a4b5c681ca0f0da391cd04d5df4487fdad5856c3d`  
		Last Modified: Tue, 16 Jun 2026 23:42:53 GMT  
		Size: 4.5 MB (4515207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174b0ad226f512069ce01e6d4b50682b002d8a2320ec01de8d2b306e7eeba53a`  
		Last Modified: Tue, 16 Jun 2026 23:42:53 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:12dbb77903d8ad6a96c22ea035ee1080da7de1840fa76ae8b9521cb88771e8db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4244940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd1ca687a9a26aa3ea91238c8be4efe5b0ade03d237eeab7f41021ee619ab87`

```dockerfile
```

-	Layers:
	-	`sha256:e6418b6a0107887d6ae01ce7dc0059be046ccf1075afe12a3d73ae0f39753e10`  
		Last Modified: Tue, 16 Jun 2026 23:42:53 GMT  
		Size: 4.2 MB (4226559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42cc755c2d6daac7ec670494e9626160e383c4f0577c3fa5012c2577a8d300aa`  
		Last Modified: Tue, 16 Jun 2026 23:42:53 GMT  
		Size: 18.4 KB (18381 bytes)  
		MIME: application/vnd.in-toto+json
