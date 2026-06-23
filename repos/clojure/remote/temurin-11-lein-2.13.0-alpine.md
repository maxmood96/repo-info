## `clojure:temurin-11-lein-2.13.0-alpine`

```console
$ docker pull clojure@sha256:43064d72d0bc79f735eea65731d1a96ae4d83d6b2ba5912deeb17b3529b9d1db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-11-lein-2.13.0-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:dcbffe20d33275b25a6e5f4c8e08380f257a5b379e4ba024a7458a65817a1515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181520207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f90fa6fe844a15f888fd0090bc7cf41442238d323e1a848cfad48aa9489a62`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:56:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jun 2026 19:56:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:56:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Jun 2026 19:56:34 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 22 Jun 2026 19:56:34 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Mon, 22 Jun 2026 19:56:41 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='ed06a4b8381786a6e8091c10539856675497d2b821cd2d0200cc5b65f453b982';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 22 Jun 2026 19:56:43 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 22 Jun 2026 19:56:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:56:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 22 Jun 2026 19:56:43 GMT
CMD ["jshell"]
# Mon, 22 Jun 2026 20:24:28 GMT
ENV LEIN_VERSION=2.13.0
# Mon, 22 Jun 2026 20:24:28 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 22 Jun 2026 20:24:28 GMT
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
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f9b522ef6226b5e762f07b84e312e749c4ff9762d64fb0a0e6a0f08d3dadc9`  
		Last Modified: Mon, 22 Jun 2026 19:56:57 GMT  
		Size: 16.8 MB (16815695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82edf31c58962a79b82269852db50864e5e46165fd344f4918a80796db584951`  
		Last Modified: Mon, 22 Jun 2026 19:57:00 GMT  
		Size: 141.1 MB (141074581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6857b309472f9776411dbc577858d377ec37fa81f85b3d973ce4c495a1a72e`  
		Last Modified: Mon, 22 Jun 2026 19:56:57 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2ca25c879ff73f76024b21ff3fcdcae040cc01923ae1d2bf184bd72f35d3bf`  
		Last Modified: Mon, 22 Jun 2026 19:56:57 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5483046e803594298c5345d561d7d09254c8c358a99d6e670ee0c5f8a736dd3`  
		Last Modified: Mon, 22 Jun 2026 20:25:21 GMT  
		Size: 15.3 MB (15267845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f79e80b0f92c7128490d63b76cea2a40d6564b100ae7193f9b2487c23c2756`  
		Last Modified: Mon, 22 Jun 2026 20:25:21 GMT  
		Size: 4.5 MB (4515223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.13.0-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:fd7f3abf046ec4b4c80a2e319d557ee938bf2ea518b76bed497ab2e4fb08536f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **977.8 KB (977793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a5b3ff6b6669b7c14f85db54195dc3db00a8179d1fdeca6e3d2aa5ddb62402`

```dockerfile
```

-	Layers:
	-	`sha256:fd6e67b230470b9bf12dba1a5554ac042999ee8b99bcc81aedec8cf96e94a0d4`  
		Last Modified: Mon, 22 Jun 2026 20:25:21 GMT  
		Size: 962.9 KB (962858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70e82d2c713ddfc9908f8dfd9f7d4018acaa8999c42b12df2d3b42b237f51957`  
		Last Modified: Mon, 22 Jun 2026 20:25:20 GMT  
		Size: 14.9 KB (14935 bytes)  
		MIME: application/vnd.in-toto+json
