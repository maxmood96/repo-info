## `clojure:temurin-11-lein-2.13.0-bookworm`

```console
$ docker pull clojure@sha256:8f8b893da7425f6a5cbc278e14e381523f66d594e21fe26e5f6bae7ded022d35
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

### `clojure:temurin-11-lein-2.13.0-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:8b423192d49421a014c66c7fc60ca41dd1f8e0afa93885467de1f71111943d94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.0 MB (219010984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c5297424100d7c4769ee39ba69eb1c4a00a05ef4dd5eab94aa1b16d85a84994`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:15:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:15:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:15:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:15:14 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:15:14 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:15:14 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:16:22 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:16:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:16:22 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:16:24 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:16:24 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66243f6dbbbf14b7bdd6b32388826658f9b1823512e9aa7c060474fbec90544d`  
		Last Modified: Fri, 19 Jun 2026 02:16:45 GMT  
		Size: 145.9 MB (145886182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7206883157e6164baa6e5853d6c7bf58894cc8afafc02224216d317ac1f3432`  
		Last Modified: Fri, 19 Jun 2026 02:16:42 GMT  
		Size: 20.1 MB (20107523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8f4b32fcd7af598271d7a411563ba10f208f2f3a51bb8564b2162bc80cb3ea`  
		Last Modified: Fri, 19 Jun 2026 02:16:41 GMT  
		Size: 4.5 MB (4515205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.13.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4e7f70990f6fae8fe6614b50a008b6cb5d5729531a56e54fc10c3a4a286ca452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4319282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55262a949da3adc46611d63b564f22e67173c507b524f0dbe91c21e962e69eea`

```dockerfile
```

-	Layers:
	-	`sha256:cc5b7450f8415c7e840cee5a204c503a345b441c0ba16d9ab8cf45a39bc9f09d`  
		Last Modified: Fri, 19 Jun 2026 02:16:41 GMT  
		Size: 4.3 MB (4303534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91e145d14d43b83b7cb5fe69835a54e9801dc9c9a4c73a75d5b2e49a0924f922`  
		Last Modified: Fri, 19 Jun 2026 02:16:41 GMT  
		Size: 15.7 KB (15748 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.13.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:78a51d66e6daa2e92c3919637ca22527436c65aad1db18173cf5a9e3685144be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215426683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fa4be1ee1b4d3fbeb015ddeb08437c11a557b6de8eab900cc9b2e70d5904e53`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:15:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:15:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:15:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:15:26 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:15:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:15:26 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:16:33 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:16:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:16:33 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:16:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:16:35 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f01604b5de02872c46c120b82ba320961aaeff605bc17c0398b14b9375b811`  
		Last Modified: Fri, 19 Jun 2026 02:16:55 GMT  
		Size: 142.6 MB (142582158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46ac8548bee780440bd382155976cc97057bc1bae78a04a8dd5c01d50a7d41e`  
		Last Modified: Fri, 19 Jun 2026 02:16:52 GMT  
		Size: 19.9 MB (19940276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2588f7a1dd348f6e3aefb57e75652444bd2d7508703836f8b1750633aab24f98`  
		Last Modified: Fri, 19 Jun 2026 02:16:51 GMT  
		Size: 4.5 MB (4515201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.13.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5a37924131bbdaceeb7cc2ec2c2a70bcb17d00589d62549e60b401fb80414421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4319636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec2e26dc9e1d1b91488fd0127a1a43c40eb043304310b795c69a463bcc442471`

```dockerfile
```

-	Layers:
	-	`sha256:e70ba72a53f20f63293c359a689ed800fb7859cc277b79eb64d1d684abfcf026`  
		Last Modified: Fri, 19 Jun 2026 02:16:51 GMT  
		Size: 4.3 MB (4303767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cc04e167b12f41c257e3dcc50850f0ec1843ae52dd259ea5733c0fc6afee26f`  
		Last Modified: Fri, 19 Jun 2026 02:16:51 GMT  
		Size: 15.9 KB (15869 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.13.0-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:25836bde1dce43263a8b18df2614937dc1443fbf0c964b6f5df12ac9aa8c4161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.3 MB (210304543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4384e4dd70f06e0a280ee9f85b3f8f728344967724b820a1006ada7c8c48c595`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:24:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:24:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:24:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:24:25 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:24:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:24:25 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:27:46 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:27:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:27:46 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:27:51 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:27:51 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:88b94a58fac236a778527a3293ccd0ff4d309bff0bf314017ea5af603908fa2e`  
		Last Modified: Thu, 11 Jun 2026 00:21:34 GMT  
		Size: 52.3 MB (52346670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fc64daf9c9f118fbcba656767bc8dbba78b223045b626eb61d82cdc3a433d8`  
		Last Modified: Fri, 19 Jun 2026 02:28:29 GMT  
		Size: 133.1 MB (133110739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc85b9e1ec0d23773963d5ecc2fd33f11242ce5e5959a8f1deaaca08521a3f3`  
		Last Modified: Fri, 19 Jun 2026 02:28:26 GMT  
		Size: 20.3 MB (20331864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26a3d1cac191f049dea600f0e191f736278f738f222cdc99b2ee5f04b4fe2c7`  
		Last Modified: Fri, 19 Jun 2026 02:28:26 GMT  
		Size: 4.5 MB (4515238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.13.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:017799ee5e164e9fec5fce5f156edec0e46113e0007d41f766409fefb7363d24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4320572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da2065137edd6437e32b9ea08630419229258c9c232059940ea7d8b980865bb5`

```dockerfile
```

-	Layers:
	-	`sha256:4a6c270b4f8f4bb93e3e63f440ebb42b8c91879421e6c4965daf4a7642784e75`  
		Last Modified: Fri, 19 Jun 2026 02:28:26 GMT  
		Size: 4.3 MB (4304780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e43375b6cbcaacea554df3798b38f95c1450d0bf67f0de25b9769d1ac4b8c59a`  
		Last Modified: Fri, 19 Jun 2026 02:28:25 GMT  
		Size: 15.8 KB (15792 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.13.0-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:7499fd22373d673bdd46683afc0575e19f8a06fab316853f145d20ba86d50b88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.1 MB (198099858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a6b2a47c3d0545da5c06c2f50886abd79f4975ba39a56eb7178da89775fed4c`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:13:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:13:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:13:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:13:19 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:13:19 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:13:19 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:14:42 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:14:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:14:42 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:14:44 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:14:44 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:b041a55a85cc0e47dd570746852cc1b0fee042f3a03eb250b9f896ac4aa74a3d`  
		Last Modified: Wed, 10 Jun 2026 23:41:01 GMT  
		Size: 47.2 MB (47161500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec01773c1e8ae5aa1b17b3f9ed96fe3b2db5b42fdb8cb8ff5e6dac16b5f5027`  
		Last Modified: Fri, 19 Jun 2026 02:15:08 GMT  
		Size: 126.7 MB (126652584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a89087ba486ffad94dcc2e50a64f60d79cd5af1fdd9dffa931229ae8e3bb15`  
		Last Modified: Fri, 19 Jun 2026 02:15:06 GMT  
		Size: 19.8 MB (19770528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4890de5c461ee10a21a177103e688dcbff81f188c8f73318491fdb0ed665c2`  
		Last Modified: Fri, 19 Jun 2026 02:15:06 GMT  
		Size: 4.5 MB (4515214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.13.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c9c60a82baab7402e00449afb8ccdfff33a8dd32af9c5b4207d758efc4c1d8c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4311100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10bd025b8a7a4f44ffaf9a5b27590cf58e78dcf01315f9a4eb31a69edebb5ccc`

```dockerfile
```

-	Layers:
	-	`sha256:2a7f36d1f38f078fab0a0b92ad732d5ed62d27ab0afcbf8f9d7747f128244b3c`  
		Last Modified: Fri, 19 Jun 2026 02:15:06 GMT  
		Size: 4.3 MB (4295352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:492aabd781b4e5457959ac65c3ac2f77222f7b971f4fe91d82c15c2458da86ab`  
		Last Modified: Fri, 19 Jun 2026 02:15:06 GMT  
		Size: 15.7 KB (15748 bytes)  
		MIME: application/vnd.in-toto+json
