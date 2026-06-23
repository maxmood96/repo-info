## `clojure:temurin-17-lein-2.13.0-alpine`

```console
$ docker pull clojure@sha256:c3098bb2bed6cc3814ae6bbb19f55f2735fb7648c464f1befb25dc365dbbc8bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-17-lein-2.13.0-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:6c79772881024c31c944a47a771c05c2403e80a8a12b8a70c9ec8bf643857729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (189977630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b3dddcaa715b89b8191f8282f496f5e3421f8b567c263302e63770929e3c05`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:56:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jun 2026 19:56:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:56:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Jun 2026 19:56:53 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 22 Jun 2026 19:56:53 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Mon, 22 Jun 2026 19:57:01 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='960b4090b75a887bb21a915a294bee3a97cd11876967c95e5bd29d9ec4812e17';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 22 Jun 2026 19:57:02 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 22 Jun 2026 19:57:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:57:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 22 Jun 2026 19:57:02 GMT
CMD ["jshell"]
# Mon, 22 Jun 2026 20:24:38 GMT
ENV LEIN_VERSION=2.13.0
# Mon, 22 Jun 2026 20:24:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 22 Jun 2026 20:24:38 GMT
WORKDIR /tmp
# Mon, 22 Jun 2026 20:25:12 GMT
RUN set -eux; apk add --no-cache ca-certificates bash maven git gnupg && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apk del ca-certificates maven git gnupg # buildkit
# Mon, 22 Jun 2026 20:25:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 22 Jun 2026 20:25:12 GMT
ENV LEIN_ROOT=1
# Mon, 22 Jun 2026 20:25:14 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 22 Jun 2026 20:25:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Jun 2026 20:25:14 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Jun 2026 20:25:14 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb24b7abeaf5ce9e23187de02071382730c0873637800e8a9adcb59301992717`  
		Last Modified: Mon, 22 Jun 2026 19:57:16 GMT  
		Size: 21.3 MB (21290166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9a403ef070b145efc0a24ea5ea18c62cf96257bfefd784d70237ec8671df1f`  
		Last Modified: Mon, 22 Jun 2026 19:57:19 GMT  
		Size: 145.1 MB (145051633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8954f1747c4e5c426ae38631e95b0494950eb78209f25ea413a0d591f5bfd8b0`  
		Last Modified: Mon, 22 Jun 2026 19:57:15 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f47b51787bf9ee6cbfe3b6ad72acc64ab2cd047c11d06a156720b184193e59`  
		Last Modified: Mon, 22 Jun 2026 19:57:15 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674575d7d3737c490f6b57a1772143df6bd27904c84bc2e6027182dd21742907`  
		Last Modified: Mon, 22 Jun 2026 20:25:22 GMT  
		Size: 15.3 MB (15273337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf87918a4b8a76e20cf10a9aeb9a2a771b43b5ead46514e898f2cbb6513309df`  
		Last Modified: Mon, 22 Jun 2026 20:25:22 GMT  
		Size: 4.5 MB (4515229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694dfc7cf5495dce4e091173cccef3c1f5bd14d6493c2f061b21a0f2cb2900f9`  
		Last Modified: Mon, 22 Jun 2026 20:25:21 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.13.0-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:f58870bc948068e74793a5142cf9139bcdb87b6781fcc0108ad1fc03f897e8c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1082619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b26061e12b57e3f62569820163868b6cb5664337a83902f31c0682aa28d5e73`

```dockerfile
```

-	Layers:
	-	`sha256:611363860ad809dcda138067a74cf56d1ef56eb5a7d1549eb23bab495a3c9b23`  
		Last Modified: Mon, 22 Jun 2026 20:25:21 GMT  
		Size: 1.1 MB (1065220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0c2a539097a93ca229a698d79c85005c6d612432241ad5939728ae8133220f6`  
		Last Modified: Mon, 22 Jun 2026 20:25:21 GMT  
		Size: 17.4 KB (17399 bytes)  
		MIME: application/vnd.in-toto+json
