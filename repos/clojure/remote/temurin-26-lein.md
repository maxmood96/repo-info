## `clojure:temurin-26-lein`

```console
$ docker pull clojure@sha256:ce9caa50ff1d86419a6aa49818120d2d97ff031deaf5778304d004a4dd37e2f0
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

### `clojure:temurin-26-lein` - linux; amd64

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

### `clojure:temurin-26-lein` - unknown; unknown

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

### `clojure:temurin-26-lein` - linux; arm64 variant v8

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

### `clojure:temurin-26-lein` - unknown; unknown

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

### `clojure:temurin-26-lein` - linux; ppc64le

```console
$ docker pull clojure@sha256:f67f997644ad0ad8699453da1ead73112bb31755ec6991ba8e1a9041160206dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171096665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51bd6584c15d0caef5001debc98bc66f923acdec5e306efcda107b04408056a9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 08:30:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 08:30:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 08:30:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 08:30:47 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 08:30:47 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 08:30:48 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 08:33:34 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 08:33:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 08:33:34 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 08:33:38 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 08:33:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 08:33:38 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 08:33:38 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:55b0e891f4e8dc14bf4bc7e853254fcf1f3ba5a8e8e3c07c21e7dd5bd6d87882`  
		Last Modified: Wed, 24 Jun 2026 00:27:34 GMT  
		Size: 52.3 MB (52346847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3911fb4790a8a823332a0489f588cce29b003efdc940702ba27434da3da607`  
		Last Modified: Wed, 24 Jun 2026 08:34:16 GMT  
		Size: 93.9 MB (93902051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a60e281587ef9ff81861da0217ed27f3d24ccb1cc1c849597d4427809239f16`  
		Last Modified: Wed, 24 Jun 2026 08:34:14 GMT  
		Size: 20.3 MB (20332150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df58aac8cef729a69a45723cb3b3836420bc99db290d9b2ffaf1fe94ad64fe92`  
		Last Modified: Wed, 24 Jun 2026 08:34:13 GMT  
		Size: 4.5 MB (4515187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2a82ca263372d754a5942009e198ca60f6acea009d8b59c4bc6fc7c4aa897a`  
		Last Modified: Wed, 24 Jun 2026 08:34:13 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:71ec9b6492bb129b2188b704ecce9d24522b1241c535578882eef6891d459351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4253805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab617a2b3baf8fea408eb1af4140c68a6d6265150f7e90b0d1355ed5ba9e4b05`

```dockerfile
```

-	Layers:
	-	`sha256:4ddaf11e63f29846671206a78e028583643f84db41b82c4ac72f3ee5df446708`  
		Last Modified: Wed, 24 Jun 2026 08:34:13 GMT  
		Size: 4.2 MB (4235368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b09f9e7ec6153191ba84a21bac3bbe2c0d66db42bc107180499d37dc8ed62f2`  
		Last Modified: Wed, 24 Jun 2026 08:34:13 GMT  
		Size: 18.4 KB (18437 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein` - linux; s390x

```console
$ docker pull clojure@sha256:4e23848c8d3d3d8579a5168f1a2a4823aab56ff4df8e76dae3bf7e1cbcaa35f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.0 MB (161984436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5e03e8583a604d6162c54bbce3e21faaeb536dc7ff437fcedc4dc0d8e2fc2c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 04:19:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:19:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:19:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:19:34 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 04:19:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 04:19:34 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 04:20:35 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 04:20:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 04:20:35 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 04:20:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 04:20:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 04:20:37 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 04:20:37 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:bdd2e9d83d68023204331dd445067114dbd3500d2d496368624fa7ef81743d4a`  
		Last Modified: Wed, 24 Jun 2026 00:27:09 GMT  
		Size: 47.2 MB (47161675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec0a7bf706ef5f3dfc06370f280188b307fdbd1df1db2cee1e3b1703d342699`  
		Last Modified: Wed, 24 Jun 2026 04:21:03 GMT  
		Size: 90.5 MB (90536980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f0747856b853c7a9d0d78f58cc678e39cfbd37b04d6616e00a468e7af63673`  
		Last Modified: Wed, 24 Jun 2026 04:21:01 GMT  
		Size: 19.8 MB (19770137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82bccf136fa51a96bdec947a5bb316747fc66e7120533cddf609a64d4784bb09`  
		Last Modified: Wed, 24 Jun 2026 04:21:01 GMT  
		Size: 4.5 MB (4515214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77708567a83d02e329d1fe549b28bf0e232bb01977879e0402fe59f9d8431854`  
		Last Modified: Wed, 24 Jun 2026 04:21:01 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:1a98c2d0c18fd2e503a47117de2c2ca3b6bcbe2a4a5aff484d1ab6632c360ad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4244939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce2bf76f1d573ca7e5a4326188804637ef4da01c6559309c7c2f877a46b22387`

```dockerfile
```

-	Layers:
	-	`sha256:f6b89fba8315e4cb343aaf9d52195d4c62c9715e6603610950ea8b4bb85712e4`  
		Last Modified: Wed, 24 Jun 2026 04:21:01 GMT  
		Size: 4.2 MB (4226559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd7c8899a594832f462b1376ca85e125f211787f6825c4b631ec3dcbf0cf42cc`  
		Last Modified: Wed, 24 Jun 2026 04:21:01 GMT  
		Size: 18.4 KB (18380 bytes)  
		MIME: application/vnd.in-toto+json
