## `maven:3-eclipse-temurin-21-alpine`

```console
$ docker pull maven@sha256:ce356dedc8da6c160d82f241e7bea6977e800e59e39882a1530d68d6a74aa72b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-eclipse-temurin-21-alpine` - linux; amd64

```console
$ docker pull maven@sha256:09896cbce17b926b927a6b308a9b55fcc7649e01ef305fcc242b6f61523414a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196204431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86da43a087647de1c5c85520711bcf248c0a6df565e6af8eecd1e0304b794cf7`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:19:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:19:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:19:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:19:13 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:19:13 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Thu, 05 Feb 2026 22:19:19 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='19eba6c3877612157ef1f46deb92745b4567cfcd64b79f15449c68cd2b7501e3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='8eb39f442c3c603e414af43844b419a9b5d4f3fe221181f323aa4eec1bd20cf8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 22:19:20 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:19:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:19:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:19:20 GMT
CMD ["jshell"]
# Thu, 05 Feb 2026 23:28:20 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Thu, 05 Feb 2026 23:28:20 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 05 Feb 2026 23:28:20 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:28:20 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:28:20 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 05 Feb 2026 23:28:20 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 05 Feb 2026 23:28:20 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 05 Feb 2026 23:28:20 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 05 Feb 2026 23:28:20 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 05 Feb 2026 23:28:21 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 05 Feb 2026 23:28:21 GMT
ARG MAVEN_VERSION=3.9.12
# Thu, 05 Feb 2026 23:28:21 GMT
ARG USER_HOME_DIR=/root
# Thu, 05 Feb 2026 23:28:21 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 05 Feb 2026 23:28:21 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 05 Feb 2026 23:28:21 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf27b2f1dcc34bb3592032d2fca01d720abfd1e6baa1293e287a9ccab686e2c`  
		Last Modified: Thu, 05 Feb 2026 22:19:36 GMT  
		Size: 21.3 MB (21315086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52562347e5095f91dcef07e31744d38da2218e3d68ed36686ee889ef31ae2406`  
		Last Modified: Thu, 05 Feb 2026 22:19:39 GMT  
		Size: 158.1 MB (158118844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0b3aa0fc9566eb09be60af94e6aa6908c7e5e316b531ec5a22f49ee8685b66`  
		Last Modified: Thu, 05 Feb 2026 22:19:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b736977b63e2d08f494efff566b76b53223018ba70ef3f070289f1f0830e61`  
		Last Modified: Thu, 05 Feb 2026 22:19:35 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09793f49c4a5c8b60f51c9c86123b893651ce1f12f3afcc476de4153e7337a4`  
		Last Modified: Thu, 05 Feb 2026 23:28:29 GMT  
		Size: 3.6 MB (3592987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce44b8a7dbadbd8270a2467f8e9a25d4ee6dbfc90a4112c77980cbff3212efd`  
		Last Modified: Thu, 05 Feb 2026 23:28:29 GMT  
		Size: 9.3 MB (9312243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebb16a3639f86e922e0d0637a64a1632abc9903aff6c3fdf31df2143966f1bf`  
		Last Modified: Thu, 05 Feb 2026 23:28:29 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b936a4414022b7be741205895dd096d430279aba4043f7799bc059dd4cd67028`  
		Last Modified: Thu, 05 Feb 2026 23:28:29 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:eb657df363f44d5105fdc7f86bf862099740c6f247eea8234dcb8dc2e1f51c91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1265365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583d1b08728e0385d8bd58a728b68ba60f1e8ace697b89066c9ed2e4b5bbb8a5`

```dockerfile
```

-	Layers:
	-	`sha256:0d1f50a95587fc90f709b138c0f59f62a2bad601fc07f12e540dd75459546779`  
		Last Modified: Thu, 05 Feb 2026 23:28:29 GMT  
		Size: 1.2 MB (1246019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1904cbfb5b276f41405a5353c75dc754c82f9df1fbdcf6c0b85570037a46a17b`  
		Last Modified: Thu, 05 Feb 2026 23:28:29 GMT  
		Size: 19.3 KB (19346 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-21-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:1ecd3060c79dcb93146a5b02994ed3caf773ae5c8417bfb19d5e2698b9280c2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.6 MB (194627454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:474d48f1f5e130f10776a834ac4dd85456113d42ddd37022134f41aaeb875ab6`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:18:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:18:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:18:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:18:10 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:18:10 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Thu, 05 Feb 2026 22:18:17 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='19eba6c3877612157ef1f46deb92745b4567cfcd64b79f15449c68cd2b7501e3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='8eb39f442c3c603e414af43844b419a9b5d4f3fe221181f323aa4eec1bd20cf8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 22:18:18 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:18:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:18:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:18:18 GMT
CMD ["jshell"]
# Thu, 05 Feb 2026 23:39:33 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Thu, 05 Feb 2026 23:39:33 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 05 Feb 2026 23:39:33 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:39:33 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:39:33 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 05 Feb 2026 23:39:33 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 05 Feb 2026 23:39:33 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 05 Feb 2026 23:39:33 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 05 Feb 2026 23:39:33 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 05 Feb 2026 23:39:34 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 05 Feb 2026 23:39:34 GMT
ARG MAVEN_VERSION=3.9.12
# Thu, 05 Feb 2026 23:39:34 GMT
ARG USER_HOME_DIR=/root
# Thu, 05 Feb 2026 23:39:34 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 05 Feb 2026 23:39:34 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 05 Feb 2026 23:39:34 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5089fa766c3c57eb5cdb3a5598c7f03110834ceee51d81992317c110371aff`  
		Last Modified: Thu, 05 Feb 2026 22:18:35 GMT  
		Size: 21.3 MB (21312383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17a1043f9baa0dcfa204d652bd299bd7e2ea6bf633efb9cd52c3f9f54976b7c`  
		Last Modified: Thu, 05 Feb 2026 22:18:38 GMT  
		Size: 156.1 MB (156130023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b7508607faa8f1e571f0bf716125a563c17b8e3883efba109aff61801ae738`  
		Last Modified: Thu, 05 Feb 2026 22:18:34 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f522a964bdc39f18b044b5e8f2817027173df17e2d19e26e356d7ef7c4afa85c`  
		Last Modified: Thu, 05 Feb 2026 22:18:34 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0ddb85aa7a5cc4df1c8d1949aed601068ea1d0da9bad806e577cdc79d90ffd`  
		Last Modified: Thu, 05 Feb 2026 23:39:42 GMT  
		Size: 3.7 MB (3672269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5721d9b4e986547155d6129cb2544da0db857f4c8f0f878bba02ca2d91032f18`  
		Last Modified: Thu, 05 Feb 2026 23:39:42 GMT  
		Size: 9.3 MB (9312235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad719cf494a671970cba232077037e39bccff4b7806ee24f3f4d1f96902909f3`  
		Last Modified: Thu, 05 Feb 2026 23:39:42 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef486c68410676c8ea62a83213e16d3ff41aff56095aadd4f716345d4cba4e13`  
		Last Modified: Thu, 05 Feb 2026 23:39:42 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:079df0bc4cd12235bdded04b44beeed681f69a15781abb84e3d93cbc57146c95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1414851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64f4fad3faf03b5311b098c0ab05adf707ecb9e06f4263f2e1e8c4c81c268cd`

```dockerfile
```

-	Layers:
	-	`sha256:9025443f5eb6d17ef19d86c0333e2eaa706fd7fadd6bf648ecec47bcbdad7148`  
		Last Modified: Thu, 05 Feb 2026 23:39:42 GMT  
		Size: 1.4 MB (1395371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a8eaa554013c8083d01387883c883559e3a2c561b3b9ca766ba541445d78eb8`  
		Last Modified: Thu, 05 Feb 2026 23:39:42 GMT  
		Size: 19.5 KB (19480 bytes)  
		MIME: application/vnd.in-toto+json
