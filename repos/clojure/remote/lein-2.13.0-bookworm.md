## `clojure:lein-2.13.0-bookworm`

```console
$ docker pull clojure@sha256:6e35789a8faf65b829c7928cc4599967363f4c80af3d7a201b87471be9e40ef0
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

### `clojure:lein-2.13.0-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:521912e5db675ce11b9fa44574f674ec9cf2469016c7bd4e785eee1e48904d02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.7 MB (165700106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d27123fa630f2d481470dd7d72eca5634df932fe673714dd84d89bea58c64e49`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:19:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:19:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:19:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:19:36 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:19:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:19:36 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:20:41 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:20:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:20:41 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:20:42 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:20:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:20:42 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:20:42 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5303faae136b6b32b318285ca3b597b4b6413e22072bf32893cc91fae33a7c7e`  
		Last Modified: Fri, 19 Jun 2026 02:21:01 GMT  
		Size: 92.6 MB (92574585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bad772c456f37699592659d0d9592e6595e23619e3dda4b61e5356c64dc5e27`  
		Last Modified: Fri, 19 Jun 2026 02:20:58 GMT  
		Size: 20.1 MB (20107848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1387fd4797cd69de53c75da1d19224a46df3275d2bbee76f774d2546d4ef6d4b`  
		Last Modified: Fri, 19 Jun 2026 02:20:58 GMT  
		Size: 4.5 MB (4515201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc85fec9288c4277852e2fb9e4ee8b932fc39383edc5008415ed43f31c8b8fd2`  
		Last Modified: Fri, 19 Jun 2026 02:20:57 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.13.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a5125a7746d78b085b67a56bfaf69521a58f8e286720351902afbe3b467696cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4272939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7a592b030f0337a1e2ea16b0be9c9f584c4a32798f00d6c4e06417661493ac`

```dockerfile
```

-	Layers:
	-	`sha256:993555914c93c3e919a9ffaa3ae271e4c2b234f2298c397e9b7ce72028910684`  
		Last Modified: Fri, 19 Jun 2026 02:20:58 GMT  
		Size: 4.3 MB (4253310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b88708c77555ecba4261d042d53cb68e9e34d53413c2c4fe8e9bc9a0bfb31ea1`  
		Last Modified: Fri, 19 Jun 2026 02:20:57 GMT  
		Size: 19.6 KB (19629 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.13.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7d137bc4ab6f278656db152fde9c093c09da477f67c889ddc543660e3d9c3faf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.4 MB (164387312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04534612865b68ee03e183b92c45febb13874a445a835b06c1d97c7e72fb092e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:14:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:14:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:14:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:14:39 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:14:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:14:39 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:15:47 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:15:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:15:47 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:15:49 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:19:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:19:57 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:19:57 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9403891d67e1401d668b8a82f359cd7e2b122c6a957c5225435b27e2dd007c06`  
		Last Modified: Fri, 19 Jun 2026 02:16:25 GMT  
		Size: 91.5 MB (91542250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412ba610ae37b075f51dee929048718ab44872c60b4805808e35cf2d24f8402c`  
		Last Modified: Fri, 19 Jun 2026 02:16:22 GMT  
		Size: 19.9 MB (19940404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65aaacdd6b9a95c2ff9e783864d0998999986f6e4d088575a487c8a12bfd9338`  
		Last Modified: Fri, 19 Jun 2026 02:16:21 GMT  
		Size: 4.5 MB (4515217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277cb3b5adc819cd517683ca9c8ec9efec3afd0f9d20960f8c8d7e19455c33e6`  
		Last Modified: Fri, 19 Jun 2026 02:20:05 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.13.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:532e310a5df581b0d3f104b9a12b73d80174074285b12c6506adeb25250355cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4272816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a6cc2c0605ba38eda6e0766873b1d9cb5ae23997c1f125b52de7312dd5abe72`

```dockerfile
```

-	Layers:
	-	`sha256:323f2b89f2c4811233abe761667cfc819fd99b43a238d722836d142c6d624a7e`  
		Last Modified: Fri, 19 Jun 2026 02:20:05 GMT  
		Size: 4.3 MB (4252994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2c8c0f405169cee66d98fa0a2d9c1410f67bf4c381cb44de03889e9e2a69a0b`  
		Last Modified: Fri, 19 Jun 2026 02:20:05 GMT  
		Size: 19.8 KB (19822 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.13.0-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:f179e58df2450e746ddbdae5f18eca4312365a9247d0830d85d58c0aec72f210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.1 MB (169108168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0946dc73b9cec62a85ec1814ad55485ea17f60420920f3824e70b66d7cc323f9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

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
# Wed, 17 Jun 2026 00:02:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 17 Jun 2026 00:02:47 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 17 Jun 2026 00:02:47 GMT
CMD ["repl"]
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
	-	`sha256:bf89a28de7a2761db3b1d45bf3c00b21c7ab706a0db5122da20022d327e92acf`  
		Last Modified: Wed, 17 Jun 2026 00:03:01 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.13.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2cadce95d8e923b6153bd02c9f9dcce3f6787e1419d4e0d885a5c92a7d268afa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4258228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95253a85c927dae803396fff97931566b21def29e53435e55c9f705145327753`

```dockerfile
```

-	Layers:
	-	`sha256:c01440eecd04d82a4e45f97594bb7a0f49f23f1333d4b3ea97ffc3dc2bf1f775`  
		Last Modified: Fri, 19 Jun 2026 02:54:17 GMT  
		Size: 4.2 MB (4238519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2561dd60319cd3da789732cdeac71965020c1b35cfd067ecd01e79569ff7829`  
		Last Modified: Fri, 19 Jun 2026 02:54:17 GMT  
		Size: 19.7 KB (19709 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.13.0-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:4cfcadd0572b5b444e9799569faa3e136dfe4a4e297cf010dbf3a8d6ffe85c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159867763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a87b10344ab2fedf822731fbb050f9dd174f5625565366c8e21a366e47f5854`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:30:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:30:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:30:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:30:16 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:30:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:30:16 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:31:32 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:31:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:31:32 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:31:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:20:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:20:53 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:20:53 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b041a55a85cc0e47dd570746852cc1b0fee042f3a03eb250b9f896ac4aa74a3d`  
		Last Modified: Wed, 10 Jun 2026 23:41:01 GMT  
		Size: 47.2 MB (47161500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14907b0f682b8ecfba5edca7e3ae44505f908a9f5163eb33cb4b2d568ad948ea`  
		Last Modified: Tue, 16 Jun 2026 23:32:19 GMT  
		Size: 88.4 MB (88420320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e7043565b34b7284c7fa5d693843e5ece45dbcaec9986711d409c32de70cec`  
		Last Modified: Tue, 16 Jun 2026 23:32:17 GMT  
		Size: 19.8 MB (19770336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987739cc204bb874386b889d6cc4fae0c385eb47a370889b6f322604802cc162`  
		Last Modified: Tue, 16 Jun 2026 23:32:16 GMT  
		Size: 4.5 MB (4515179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4aaa912ff704d061d44d23769c8be07901fe41f606472834ea209de6b20d73e`  
		Last Modified: Fri, 19 Jun 2026 02:21:04 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.13.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f5068281eb06bbdfea22c7b322d7be432eeee3f9c10404cd1c88dd0748b8462d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4249315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d27786433f82ddfeef171bc59fd2f17d00e1c80f284cb4ac561c26186eb46330`

```dockerfile
```

-	Layers:
	-	`sha256:ee98f5f42ece53f4711549f487ad2a4086af1382044b6054b6d3c987fc2574e7`  
		Last Modified: Fri, 19 Jun 2026 02:21:04 GMT  
		Size: 4.2 MB (4229686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80bf930ce76771bd72b8f2feaf0c88d0776e651c0deaeb7f818d36e4f1812595`  
		Last Modified: Fri, 19 Jun 2026 02:21:04 GMT  
		Size: 19.6 KB (19629 bytes)  
		MIME: application/vnd.in-toto+json
