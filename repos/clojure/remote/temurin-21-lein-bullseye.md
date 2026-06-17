## `clojure:temurin-21-lein-bullseye`

```console
$ docker pull clojure@sha256:93d9461b7589b6177e68e328c080f6bbc970e2224d0f47ed2a1f4eee5b187cec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:954e4ca8602138360bcacd90f5c1c5a97e67f6cd1cdfabe9793cc19449794de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.4 MB (233382868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fb46a43dcff50d3fb4a99b5cfed855f972259b7a1398650fb4a02937651c989`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Tue, 16 Jun 2026 23:36:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:36:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:36:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:36:09 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:36:09 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:36:09 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:37:17 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:37:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:37:17 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:37:19 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:37:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:37:19 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:37:19 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:af48a3e7696e07f88a02f9674e541901b65eadb5cf0f62e566b1d895099a1e9e`  
		Last Modified: Wed, 10 Jun 2026 23:40:09 GMT  
		Size: 53.8 MB (53771769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:448fbd65f09d59091a3a4b3821d9f46a058b535e7b75d08a6c6af4444d7bdb02`  
		Last Modified: Tue, 16 Jun 2026 23:37:41 GMT  
		Size: 158.2 MB (158166957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32afbef26e45b823d8e6626ccc1691da1327bc216658b03b4df85e453c413cc7`  
		Last Modified: Tue, 16 Jun 2026 23:37:37 GMT  
		Size: 16.9 MB (16928488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4e3eb5fdf57cf101d26cc7d2742b8a302981f5572fd0629555ee4c20faf26f`  
		Last Modified: Tue, 16 Jun 2026 23:37:37 GMT  
		Size: 4.5 MB (4515223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ab56251350f6ea2cf9d5034dc8ebc6b1ab6cda03f594eb8ac7ef7ecd2b9199`  
		Last Modified: Tue, 16 Jun 2026 23:37:37 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:68b15afb10226f33df7b2de9029efcd21c1a8e6dbcc34298256061efc0e7d26b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4522241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae5688b8de28d33a4dd5d06ee62cb13cf4b7628171669d08f58f7ba8c2b4d802`

```dockerfile
```

-	Layers:
	-	`sha256:4ae1e9986e112ae1aee148f1f8dd0ddcca8c6a280a7ab39dab1930cc2971cf2f`  
		Last Modified: Tue, 16 Jun 2026 23:37:37 GMT  
		Size: 4.5 MB (4504503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d15a1e0e9ff5c33e5e1f96fd2c5939fb5b6f334d5223af8c3f0c274a22933cff`  
		Last Modified: Tue, 16 Jun 2026 23:37:37 GMT  
		Size: 17.7 KB (17738 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5b5eb9a85cd8b52ef8259a922509fb36b9767aabc869259d5b3f99e29b8153b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230158796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb9e191688f33f99c56189dd6691dda3b51fd8608ed29f9fd45abbfe4d5d9441`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Tue, 16 Jun 2026 23:35:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:35:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:35:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:35:57 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:35:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:35:57 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:37:05 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:37:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:37:05 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:37:07 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:37:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:37:07 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:37:07 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7c21e59e753cb91625909251110d6e4cc4a5411b4b7b37f74a62e56b927b7f1e`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 52.3 MB (52264114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed860c84f19ac38d5140912d3aff9f0d870d865e2e9e881b39c94b7daeeab040`  
		Last Modified: Tue, 16 Jun 2026 23:37:28 GMT  
		Size: 156.5 MB (156461282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d674ea0a468a4ca361bb28bb283df209228d1025c248c99a124cae041ef4f1`  
		Last Modified: Tue, 16 Jun 2026 23:37:25 GMT  
		Size: 16.9 MB (16917770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b21bd56aee83d21de31d515a39dce0ea27d84c6d2cac0b8bdaefb1e46368fc64`  
		Last Modified: Tue, 16 Jun 2026 23:37:24 GMT  
		Size: 4.5 MB (4515199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32316f72787deeef433d95138addace198ec8cc78b7dba6138dc3ed792d7d3d6`  
		Last Modified: Tue, 16 Jun 2026 23:37:24 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:9a57f0742e9898ac90ba13dce191852cddb8360031fcc0a800ec35a7ce1a479d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4521336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa6132ab38201dae949a4cc2bee3fdfd3c5715a497ef331bd821746d9dd758b4`

```dockerfile
```

-	Layers:
	-	`sha256:90a4c3ce36e23a5a63e1ebd822e0674e7477cdfb567272b79719b27026d64ee0`  
		Last Modified: Tue, 16 Jun 2026 23:37:24 GMT  
		Size: 4.5 MB (4503477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d5858781b6a8ad75a06831716f018ed1dfcd5799f2bd88bece5ed23f3e11c06`  
		Last Modified: Tue, 16 Jun 2026 23:37:24 GMT  
		Size: 17.9 KB (17859 bytes)  
		MIME: application/vnd.in-toto+json
