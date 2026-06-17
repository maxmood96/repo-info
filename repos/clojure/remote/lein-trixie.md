## `clojure:lein-trixie`

```console
$ docker pull clojure@sha256:36048ed7f1044c28b1541fabebc064eb779911171adfe882e8afbe42a916da1c
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

### `clojure:lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:de18cf507cc944172190c2469b61cb3634448b1126a92f3e54a3214a35561b8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.3 MB (165287630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:959615b69679b14d3da7f6e840ffe3d02440a447e2d2ae96da734478a889cd37`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:37:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:37:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:37:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:37:48 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:37:48 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:37:48 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:39:08 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:39:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:39:08 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:39:09 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:39:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:39:09 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:39:09 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f740cf368b291b568578883b29c230c7e6b82ad914b0ec1f08f12b10c71c3708`  
		Last Modified: Tue, 16 Jun 2026 23:39:29 GMT  
		Size: 92.6 MB (92574574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef958fa0dd440c7e8dbd57dccc6210a4bdac115cb2d1585489ecf93e98a8e91`  
		Last Modified: Tue, 16 Jun 2026 23:39:27 GMT  
		Size: 18.9 MB (18880330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163474895f89848e2aa81151e288936dc6aa7e366620d798cd888bc8bf8c0ce7`  
		Last Modified: Tue, 16 Jun 2026 23:39:27 GMT  
		Size: 4.5 MB (4515176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1829704d6e4557c143fbdba2dab079974e8029a79b480718baf469f2dea338`  
		Last Modified: Tue, 16 Jun 2026 23:39:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:65002a9d7627ecfb44c8453079944d259ab7525fbefad6747eebfb97120fa76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3804193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e87816a444c9c83931932b827e83e53be2e2b0e78d39a01e814a8bc270fcd712`

```dockerfile
```

-	Layers:
	-	`sha256:09e9a90758caf491d060c845be04d09b725d09006498ab3f6ca678fc45a0c7cd`  
		Last Modified: Tue, 16 Jun 2026 23:39:27 GMT  
		Size: 3.8 MB (3785848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a516032ab120fdeeb23547330eee4880d2bfdb879c0bf9e8ab9daebbea9bc27c`  
		Last Modified: Tue, 16 Jun 2026 23:39:26 GMT  
		Size: 18.3 KB (18345 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4d84b8901eb4624082699fa413b3ff92db8b852be44e1c0c399b53520d2b3e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.6 MB (164575653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a06fbdae81336461f7de14d38fd5af3030cc11dd661dee89c930fd2fb01960b8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:37:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:37:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:37:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:37:31 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:37:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:37:31 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:38:46 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:38:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:38:46 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:38:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:38:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:38:48 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:38:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487c8b34b6435ec7c409bdba9232d21f391cbe49ec8bb95863062407d5eaaca3`  
		Last Modified: Tue, 16 Jun 2026 23:39:06 GMT  
		Size: 91.5 MB (91542253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de7bd7df56aeb00a58514db21e28243441e2e3663182f307a06951221f20062`  
		Last Modified: Tue, 16 Jun 2026 23:39:04 GMT  
		Size: 18.8 MB (18839624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e27c3de256ac76ba67a188a7d9e5ead825b11721dcda33114a740bb3c94411c`  
		Last Modified: Tue, 16 Jun 2026 23:39:04 GMT  
		Size: 4.5 MB (4515178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8674c19bc3593b4b7530f46caef6204694a8575845a996aefc0c6374aad47d`  
		Last Modified: Tue, 16 Jun 2026 23:39:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9f8d6574b97d27f2c63a5ac84805d6f1c73134bd7459a1c4d45bebc823ab7c45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3804598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def7b704d77fb239556b2dee60206cf74cff029a72b6cc06ffff21993c48ec2d`

```dockerfile
```

-	Layers:
	-	`sha256:059719f55483da456cfeb9200ba91fd13d89a1554c70cf2d152d1f844b5fc0ed`  
		Last Modified: Tue, 16 Jun 2026 23:39:04 GMT  
		Size: 3.8 MB (3786109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6456d304b6c6a88048ce32c935e2cfad97f6d49cbd070fd91a20118b5bd5f06b`  
		Last Modified: Tue, 16 Jun 2026 23:39:04 GMT  
		Size: 18.5 KB (18489 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:f5ba3c4ab925d437bbf1890ee2ee837f8f79dfde6782c740e3f3353eaa8687cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168504056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc7af32c2b409e0c04012fcac01cd73d7684dd9608423c672b5d84e756015a3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Wed, 17 Jun 2026 00:11:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jun 2026 00:11:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 17 Jun 2026 00:11:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jun 2026 00:11:00 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 17 Jun 2026 00:11:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 17 Jun 2026 00:11:00 GMT
WORKDIR /tmp
# Wed, 17 Jun 2026 00:13:43 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 17 Jun 2026 00:13:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 17 Jun 2026 00:13:43 GMT
ENV LEIN_ROOT=1
# Wed, 17 Jun 2026 00:13:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 17 Jun 2026 00:13:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 17 Jun 2026 00:13:47 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 17 Jun 2026 00:13:47 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:fc2380819f7227178ecd607b245c244d8811737f42c6112caf011a01a3889a8e`  
		Last Modified: Thu, 11 Jun 2026 00:24:43 GMT  
		Size: 53.1 MB (53137939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc6e91230e9fcb06c48eef2eae63696efc222edfdf9387e828c0e8a79c0a8c9`  
		Last Modified: Wed, 17 Jun 2026 00:14:23 GMT  
		Size: 91.9 MB (91914030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545271dc17cd609e72c45c99cc2b4c230217501733bc396ea85bb6cff9be56e8`  
		Last Modified: Wed, 17 Jun 2026 00:14:21 GMT  
		Size: 18.9 MB (18936466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c816ddc4d5518aa88e3295640163da90bcf82a13d4b932d4a76c10753cb825`  
		Last Modified: Wed, 17 Jun 2026 00:14:20 GMT  
		Size: 4.5 MB (4515191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70de2f92949336d91b0ec75fa618b27498fcb6a8e3610fabf898d448df7b34d2`  
		Last Modified: Wed, 17 Jun 2026 00:14:20 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f2436e33b829ded8fc19aec62855b3b3153a649098615f27a824940663b41be5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3788573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce69ebda287cd3054dbce6cb4a5f50d2014f5a13430656cba8ce01143e22b6d`

```dockerfile
```

-	Layers:
	-	`sha256:506a4e1cc354a4a439cac4422a22035095f3df51ed7885011f5ebbac5c295642`  
		Last Modified: Wed, 17 Jun 2026 00:14:20 GMT  
		Size: 3.8 MB (3770172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0666a0a5225e014a5c2341b46e7b339b642124a7ba8e4957c38a03a008955909`  
		Last Modified: Wed, 17 Jun 2026 00:14:20 GMT  
		Size: 18.4 KB (18401 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:560c14959e1fceeb842be3d8cabdc354d4a42576da15ab73c979ea46e4385a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161244095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb0da4677d4a9846c8d9938b9d4e0d93933f1cc49e33d9989c491f67d35983c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:41:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:41:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:41:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:41:05 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:41:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:41:05 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:42:20 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:42:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:42:20 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:42:21 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:42:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:42:22 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:42:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0ebf827318debac5b829e4cd5c36e0122490cf2392f532aa02b2b0999d5c1b37`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 49.4 MB (49385897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e141af4c3ca44d66006c21b5229d05180427e764c0a36b8e43c72eabd028a0d`  
		Last Modified: Tue, 16 Jun 2026 23:42:49 GMT  
		Size: 88.4 MB (88420336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a733018c6226522d055d969779733c42428ba813866bb1cb361a3f8c0a3f14`  
		Last Modified: Tue, 16 Jun 2026 23:42:47 GMT  
		Size: 18.9 MB (18922250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f130159aac0d382537808c6188680825a9450faa7e535b7ad3cdd2c6c2ca3d0`  
		Last Modified: Tue, 16 Jun 2026 23:42:47 GMT  
		Size: 4.5 MB (4515183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5195836d6f7c75fd166bd459a5b54291255f0c6464e19a557cb79372885af406`  
		Last Modified: Tue, 16 Jun 2026 23:42:47 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1ac400087de8a650eaa3d6e690b41d49d388a5daacc32196ad83c52295a52602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3785182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854ee0eaf548d618896faf3c36e2908a8878902de02030c4eb138356eb2254f1`

```dockerfile
```

-	Layers:
	-	`sha256:ccd89e0edccc7e44708737ca0eb7710d3f3a7cd555fc212413321365f03a066c`  
		Last Modified: Tue, 16 Jun 2026 23:42:47 GMT  
		Size: 3.8 MB (3766837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a9e651c0c468a48150aa9de1e437047d6bd3fe732b59091aa7df14a02eec4cd`  
		Last Modified: Tue, 16 Jun 2026 23:42:47 GMT  
		Size: 18.3 KB (18345 bytes)  
		MIME: application/vnd.in-toto+json
