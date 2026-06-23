## `clojure:temurin-25-lein-alpine`

```console
$ docker pull clojure@sha256:9992f4154951bafa893f4f318e85eeca842e25bb20acb82ea4ef9e63bfe18da3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-lein-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:cf0d8697253ef580d964dfab4f0fff9a18d2b0f95d5f9c8329338251e2131bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.7 MB (129700706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15985108dc25262b520af82a2656ed7bd05e4e93e3d363c4fbf66c53b953f90a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:57:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jun 2026 19:57:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:57:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Jun 2026 19:57:28 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 22 Jun 2026 19:57:28 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Mon, 22 Jun 2026 19:57:35 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='6ed368e93049d3b188c045fce0b20953bbea92fe0614dbbf4d3fd8daad7be3b2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='51c2415b370aac7c3796b0c4663c8fcf91bc22d76f03df95b25fa5667cb5fdd8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Mon, 22 Jun 2026 19:57:36 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 22 Jun 2026 19:57:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:57:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 22 Jun 2026 19:57:36 GMT
CMD ["jshell"]
# Mon, 22 Jun 2026 20:25:01 GMT
ENV LEIN_VERSION=2.13.0
# Mon, 22 Jun 2026 20:25:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 22 Jun 2026 20:25:01 GMT
WORKDIR /tmp
# Mon, 22 Jun 2026 20:25:33 GMT
RUN set -eux; apk add --no-cache ca-certificates bash maven git gnupg && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apk del ca-certificates maven git gnupg # buildkit
# Mon, 22 Jun 2026 20:25:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 22 Jun 2026 20:25:33 GMT
ENV LEIN_ROOT=1
# Mon, 22 Jun 2026 20:25:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 22 Jun 2026 20:25:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Jun 2026 20:25:34 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Jun 2026 20:25:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95dd7d1a57040850aa18d8f120a347787a853ddadfc0e04c01ba359687f83037`  
		Last Modified: Mon, 22 Jun 2026 19:57:55 GMT  
		Size: 14.3 MB (14259376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586ae85e2c68546c53c9b39b13ad3a217cff435d3f4ed14c0808da512b593ea2`  
		Last Modified: Mon, 22 Jun 2026 19:58:08 GMT  
		Size: 91.6 MB (91624437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1580feaf93ee040ffb3f5ef134e5cc50ea4a1357ecdd98270885a7563d2b8e21`  
		Last Modified: Mon, 22 Jun 2026 19:57:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84edc40c41dfe07d6b44bf4c0fa58803f7070a8fb7ec3f9603d8cb0e50ac8058`  
		Last Modified: Mon, 22 Jun 2026 19:57:50 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4c108365ab9a70ddc8250c4ff16f4da75669d255eed577cb465b2c62d4247a`  
		Last Modified: Mon, 22 Jun 2026 20:25:43 GMT  
		Size: 15.5 MB (15454445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a85e5b212b017a4e063de8a629d4135e11ed9f24b2ef3d8457f12ddbfe97585`  
		Last Modified: Mon, 22 Jun 2026 20:25:42 GMT  
		Size: 4.5 MB (4515180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5b58777b676063fe3851e82cf8664dc5c355bf984c45995c1a3f6e57f00c8d`  
		Last Modified: Mon, 22 Jun 2026 20:25:42 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:d8d965e93e3d737937e313f667716b3d4c6b17e89b274f9fa6f3985f626d41c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1050004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96b0a14661766926a7e7a2096a3ba20fb163a2147927030c852ae6796403b5e9`

```dockerfile
```

-	Layers:
	-	`sha256:25fd66d558b90e03820df79bfeb46c607f18436faff8f22d40135eb87b001a13`  
		Last Modified: Mon, 22 Jun 2026 20:25:42 GMT  
		Size: 1.0 MB (1032614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77c088df9cf97fedacac6efd93a959f3501ef1defc59cb418f2740b00d81a98d`  
		Last Modified: Mon, 22 Jun 2026 20:25:42 GMT  
		Size: 17.4 KB (17390 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-alpine` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b0c5a8f6b45aa9d44a1055a6e17ac1da653946150f583caf496bd5ee890b3007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.1 MB (129122217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c62bef61a254d43bac3458c60673a720814ed1ea73906d463d1186d7833480e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:12:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jun 2026 20:12:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 20:12:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Jun 2026 20:12:39 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 22 Jun 2026 20:12:39 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Mon, 22 Jun 2026 20:12:45 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='6ed368e93049d3b188c045fce0b20953bbea92fe0614dbbf4d3fd8daad7be3b2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='51c2415b370aac7c3796b0c4663c8fcf91bc22d76f03df95b25fa5667cb5fdd8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Mon, 22 Jun 2026 20:12:46 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 22 Jun 2026 20:12:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 22 Jun 2026 20:12:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 22 Jun 2026 20:12:46 GMT
CMD ["jshell"]
# Mon, 22 Jun 2026 21:53:21 GMT
ENV LEIN_VERSION=2.13.0
# Mon, 22 Jun 2026 21:53:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 22 Jun 2026 21:53:21 GMT
WORKDIR /tmp
# Mon, 22 Jun 2026 21:54:09 GMT
RUN set -eux; apk add --no-cache ca-certificates bash maven git gnupg && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apk del ca-certificates maven git gnupg # buildkit
# Mon, 22 Jun 2026 21:54:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 22 Jun 2026 21:54:09 GMT
ENV LEIN_ROOT=1
# Mon, 22 Jun 2026 21:54:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 22 Jun 2026 21:54:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Jun 2026 21:54:11 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Jun 2026 21:54:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff532a92b2635da709828a163e9a5ed2f5149ecbe38b06fce240f8fb7104afca`  
		Last Modified: Mon, 22 Jun 2026 20:13:02 GMT  
		Size: 14.3 MB (14320296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de05b5f3adafc3ef06ed696a78315ea4e1caf24c78e679cc659d636c92fbdd77`  
		Last Modified: Mon, 22 Jun 2026 20:13:06 GMT  
		Size: 90.6 MB (90571688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a582b2da42ce858dfb28843505bc7c46dab8db82854a593f73fe11f4abc3d085`  
		Last Modified: Mon, 22 Jun 2026 20:13:01 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2881aa8c3290ef38ec53319eae6c5498e1f555bf0142e50a1dd91eb8728d60dd`  
		Last Modified: Mon, 22 Jun 2026 20:13:01 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8b2fcbfa297e539b73740e168f266d1be2327e1cb796c66d0b18efaa5e0777`  
		Last Modified: Mon, 22 Jun 2026 21:54:20 GMT  
		Size: 15.5 MB (15530349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da304ea75fdb2f6d6c94e1195397de3a790682f9553eeaacc7a0a68a9d870f17`  
		Last Modified: Mon, 22 Jun 2026 21:54:20 GMT  
		Size: 4.5 MB (4515178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0247ebe0b617f061f3aee00ac8442da944f184c71d3dd7f950a6c9a86f186263`  
		Last Modified: Mon, 22 Jun 2026 21:54:20 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:b682e5de8546f372017c69ec035a0a2b9a3e3ae36ea411e46665bf18de9b60bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1199436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32cc86d8333744d5336adbf6f2b91b2dc140c74662f348cbab891d2f95f708ef`

```dockerfile
```

-	Layers:
	-	`sha256:579d389a7b9f4496e16d9821098f9bf5fa57dd41273c32fd45db54e569545579`  
		Last Modified: Mon, 22 Jun 2026 21:54:20 GMT  
		Size: 1.2 MB (1181951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7e36358bdb4d59b768e3156017d5997cf2de23c35c72a62b46d33418f0d7dcc`  
		Last Modified: Mon, 22 Jun 2026 21:54:19 GMT  
		Size: 17.5 KB (17485 bytes)  
		MIME: application/vnd.in-toto+json
