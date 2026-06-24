## `clojure:temurin-26-lein-2.13.0-bookworm`

```console
$ docker pull clojure@sha256:42952446a40599fcc22e40e24108f54a17f531eebf32d6ae113a517a378235ca
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

### `clojure:temurin-26-lein-2.13.0-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:e64a288b088ed334ec2d4617568f594ffec27fb739168cfc41619ad805f6f72d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.6 MB (167649777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b19dfd7e9c30072c0d6214a66e690a180422c28bf8779ea50fc77271928a5b71`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:22:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:22:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:22:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:22:11 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:22:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:22:11 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:23:12 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:23:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:23:12 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:23:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:23:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:23:13 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:23:13 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:425befdf76e52426879d2abe42093a00dca59a893e7b4fa2a7679b0180b71d4b`  
		Last Modified: Wed, 24 Jun 2026 00:27:40 GMT  
		Size: 48.5 MB (48502210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7af060bab959327c8f4893ea4dbe9c988889d4744f339ad962cb35938aeba3`  
		Last Modified: Wed, 24 Jun 2026 02:23:34 GMT  
		Size: 94.5 MB (94524361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095cc37eaee476ab01d318a21ac026f9cc19c24dc48c6a11defc4a677da58f51`  
		Last Modified: Wed, 24 Jun 2026 02:23:32 GMT  
		Size: 20.1 MB (20107603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a47cf4fc39da5f7abbceffa18643ae1e2af70659eaa4e197d8c968abba89e6b`  
		Last Modified: Wed, 24 Jun 2026 02:23:31 GMT  
		Size: 4.5 MB (4515174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c47162149b6edad8f855ac5a33c09107873db28ab49b5249c989663ef87785`  
		Last Modified: Wed, 24 Jun 2026 02:23:31 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.13.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7c303c8c293c3b3970d5bc285e3e4957d94392f01be4c9b65d5bc204dd3f09eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4267940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a632f494ca0ff5ab16847d9710c84bb6d04c18c07a5557e684890553ed5b455e`

```dockerfile
```

-	Layers:
	-	`sha256:a4c2a04775da02290c7cd3c1e91643c085417679d65c755542969a9bc7adab14`  
		Last Modified: Wed, 24 Jun 2026 02:23:31 GMT  
		Size: 4.2 MB (4249559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b229d20d98f697d354628e069ccca0286a44cb1b6b76893a6ad8e6fc71983435`  
		Last Modified: Wed, 24 Jun 2026 02:23:30 GMT  
		Size: 18.4 KB (18381 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.13.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5e22791413c061653cae95693f688662663ebdea8ff19d2c56456c746489382b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.3 MB (166349370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f4d269f950b9c20e4bee43c27d591c290abf260a04ec445e10112bb5dacb9f5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:28:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:28:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:28:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:28:59 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:28:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:28:59 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:30:08 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:30:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:30:08 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:30:10 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:30:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:30:10 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:30:10 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0fb1189398e2e4b474d43aac6502510d0da0318e70137a377c21087f198814db`  
		Last Modified: Wed, 24 Jun 2026 00:27:19 GMT  
		Size: 48.4 MB (48389201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b05c1b63abec778c95a72be7e0b16e93d099bb72000d6308e40b683c5d5072`  
		Last Modified: Wed, 24 Jun 2026 02:30:30 GMT  
		Size: 93.5 MB (93504335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37bac0db20755644dc732418c2b46f9a92f1c908edc5049b8d255432d976bb55`  
		Last Modified: Wed, 24 Jun 2026 02:30:28 GMT  
		Size: 19.9 MB (19940200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8074be5c7d0d3537ef62005c97772493e133f4b0958d038f538d932b6da6385f`  
		Last Modified: Wed, 24 Jun 2026 02:30:27 GMT  
		Size: 4.5 MB (4515204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cb496ddc76eeda52786423498b2f051b9e62c9edd511be0b8e6595b8287095`  
		Last Modified: Wed, 24 Jun 2026 02:30:27 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.13.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d380314f048f0e8845b3550262d860a1f8f066a2d1860ff540f26ad24f1eb6b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4267721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89ac46d61c82d929fa3bddf480002a44b3e999d5fd700faacf9e55730dce6ba1`

```dockerfile
```

-	Layers:
	-	`sha256:98aee59e0a03c22c3dbb84457eed3869009b450d8fc04acd21185e6ad94bad6d`  
		Last Modified: Wed, 24 Jun 2026 02:30:27 GMT  
		Size: 4.2 MB (4249195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9e90ddd79022ceb7ec318b5f9379f5001f37782862c5108edd06b3d23c5274e`  
		Last Modified: Wed, 24 Jun 2026 02:30:27 GMT  
		Size: 18.5 KB (18526 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.13.0-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:f425df151a5487c4e7e275fe3ccb766e8953adc5bd37e02b8fb42a3195397136
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

### `clojure:temurin-26-lein-2.13.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2ae5a09d535af18f63527a2bbb7e56a736dc0060fb1c218647a7e20e4f3da06d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4253805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2187a0793c003965ce0bed1ac56564a8ebb39b46c611989f229e0e85086f3d9f`

```dockerfile
```

-	Layers:
	-	`sha256:44d6f25d070f9b0e0e0e7186232d68987e89e58d0392edc98719e635675138cb`  
		Last Modified: Fri, 19 Jun 2026 02:58:39 GMT  
		Size: 4.2 MB (4235368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a498a1cfb1ed15102f9bbfe73d4e939d7229777f04a5adfb76dde81b30a828dd`  
		Last Modified: Fri, 19 Jun 2026 02:58:39 GMT  
		Size: 18.4 KB (18437 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.13.0-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:eb692e872b14f7a42f7664e40c37bb558c4fe80d55a29e1bf334df1c4d6728bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.0 MB (161984418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca1abd3cbc255d895e8493c4a2e27c4fc5403078a9fd250fae8b099f5efa470a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:22:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:22:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:22:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:22:54 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:22:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:22:54 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:23:59 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:23:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:23:59 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:24:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:24:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:24:01 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:24:01 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b041a55a85cc0e47dd570746852cc1b0fee042f3a03eb250b9f896ac4aa74a3d`  
		Last Modified: Wed, 10 Jun 2026 23:41:01 GMT  
		Size: 47.2 MB (47161500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93dffac2f0aa26f15bbfc00b26f8e00f41d28e225af70af77c70295cf7b0a6c`  
		Last Modified: Fri, 19 Jun 2026 02:24:28 GMT  
		Size: 90.5 MB (90536936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b2ba4cbbb6a84ff9134b153722a1d1cdb79ff03db443f015b0ff4a087dee98`  
		Last Modified: Fri, 19 Jun 2026 02:24:26 GMT  
		Size: 19.8 MB (19770341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf36d5b55df0ad38c1a8ac0fc544db96c4b3b52fd843aa16f758e1b62e143b07`  
		Last Modified: Fri, 19 Jun 2026 02:24:25 GMT  
		Size: 4.5 MB (4515212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa226d21a8c685abca41d8e6535188edd0e44c1827dc1e1f208fc637fad2748c`  
		Last Modified: Fri, 19 Jun 2026 02:24:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.13.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:641760ae5648d3600ac42e9d1fa9e5272b3173548b3d543ea76a1934ec563b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4244940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffef27a05901899601f498eae7f84be15fdef005c0cafc7d7e0f60153cba9500`

```dockerfile
```

-	Layers:
	-	`sha256:c6cb7c2fece12f8f790fe4b597da5d678bfb47e7f4100be4a459fa714d897a79`  
		Last Modified: Fri, 19 Jun 2026 02:24:25 GMT  
		Size: 4.2 MB (4226559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a082585c1b2c28d5978b3e29326b5da8c0bfe276181867110fc101e2ed706cf5`  
		Last Modified: Fri, 19 Jun 2026 02:24:25 GMT  
		Size: 18.4 KB (18381 bytes)  
		MIME: application/vnd.in-toto+json
