## `maven:3-eclipse-temurin-25-alpine`

```console
$ docker pull maven@sha256:403a1b0eeab426743a6f2cd5cafede426e8e45b945462efdaa67f2ad09bacca0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-eclipse-temurin-25-alpine` - linux; amd64

```console
$ docker pull maven@sha256:32b2df5c68fa9e8ee62bae672692201fd46eb7f62155aef367a92d367881d451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123650797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d94e34622a92bf2f440d05c343f54f16d06b917e3bb46e166510c36f4914108`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

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
# Mon, 22 Jun 2026 20:27:08 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Mon, 22 Jun 2026 20:27:14 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 22 Jun 2026 20:27:14 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 22 Jun 2026 20:27:14 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 22 Jun 2026 20:27:14 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 22 Jun 2026 20:27:14 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 22 Jun 2026 20:27:14 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 22 Jun 2026 20:27:14 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 22 Jun 2026 20:27:14 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 22 Jun 2026 20:27:14 GMT
ARG USER_HOME_DIR=/root
# Mon, 22 Jun 2026 20:27:14 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 22 Jun 2026 20:27:14 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 22 Jun 2026 20:27:14 GMT
CMD ["mvn"]
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
	-	`sha256:33d4e431b4eac694a534910202d55df4ec427b7577308cd88e62f8783d3b063d`  
		Last Modified: Mon, 22 Jun 2026 20:27:21 GMT  
		Size: 4.6 MB (4559183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0caced839db8130094cc28aa4a57f4ee56ed290b9df5398e9c76585ec7c9a15b`  
		Last Modified: Mon, 22 Jun 2026 20:27:21 GMT  
		Size: 9.4 MB (9359956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47661399478766a851c4cf5dc1c1ce21ea35b07c2e1df5dceaf76e39f64b400`  
		Last Modified: Mon, 22 Jun 2026 20:27:21 GMT  
		Size: 859.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a82839824a70adec957346088bf2758a25a8ee0bf8b7335beec8d60d56c1c4`  
		Last Modified: Mon, 22 Jun 2026 20:27:21 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-25-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:fc4c2898fd796741587efcc77931e99162c94c11c403d9adde27779b5344e6c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1141400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22adafa249118f105841c10c16239353c7e736d508d46ca0b4b08ebe2b5380d5`

```dockerfile
```

-	Layers:
	-	`sha256:f133d50241fb8a43347e55b8a6b7af9cc18863560c380f6ea78fef4e4f7ff0d5`  
		Last Modified: Mon, 22 Jun 2026 20:27:21 GMT  
		Size: 1.1 MB (1124364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8c7333c2cb21b1a632f04fe3a67719c440b7eb3c0c092e758b4c5ae92d33066`  
		Last Modified: Mon, 22 Jun 2026 20:27:20 GMT  
		Size: 17.0 KB (17036 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-25-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:7a2a170aa5f5a59c5520a15c7cfbab14ba36038d8788f847b60c63431007e28b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123079154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b5df504739200f67087260e426a6b682753f536d49be515d7cbce551152973a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

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
# Mon, 22 Jun 2026 21:53:27 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Mon, 22 Jun 2026 21:53:27 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 22 Jun 2026 21:53:27 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 22 Jun 2026 21:53:27 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 22 Jun 2026 21:53:27 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 22 Jun 2026 21:53:27 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 22 Jun 2026 21:53:27 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 22 Jun 2026 21:53:27 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 22 Jun 2026 21:53:27 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 22 Jun 2026 21:53:27 GMT
ARG USER_HOME_DIR=/root
# Mon, 22 Jun 2026 21:53:27 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 22 Jun 2026 21:53:27 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 22 Jun 2026 21:53:27 GMT
CMD ["mvn"]
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
	-	`sha256:0f6729cebc12476b8509417b6fc148a554f9b3598aae2d71813c137283893539`  
		Last Modified: Mon, 22 Jun 2026 21:53:35 GMT  
		Size: 4.6 MB (4641918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1bbc9260870d6f7982840e3ee6cbb69da5ab98e65dd23ee288f3d9e6873742`  
		Last Modified: Mon, 22 Jun 2026 21:53:35 GMT  
		Size: 9.4 MB (9359968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d69f2445201ce6a365d9cf6517c9d27867c7c3bad9662a9562ce9ce6dcb0d5`  
		Last Modified: Mon, 22 Jun 2026 21:53:35 GMT  
		Size: 859.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7646c5babcc03efa8771fd32f41f415d4a0f2b3cc34ee605db5f4782b6c33890`  
		Last Modified: Mon, 22 Jun 2026 21:53:35 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-25-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:f12ca41e31716d15a8cdb4f661cad6920b49c8e85819864237c6ee3d94eea057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29c75ea395f2399c52a5ed1d0c31b4c1cb5aac04bcd88ede70ce4873f296a12b`

```dockerfile
```

-	Layers:
	-	`sha256:9b4d725c91ddc92410b1c02129b8631a765885463eb16ab2e89aec383dfe83d4`  
		Last Modified: Mon, 22 Jun 2026 21:53:35 GMT  
		Size: 1.3 MB (1273713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21906eb9dad9ac5bf0d4869dbbc894da4e5bb11e4b91a1f4b841ff332380f03d`  
		Last Modified: Mon, 22 Jun 2026 21:53:35 GMT  
		Size: 17.2 KB (17169 bytes)  
		MIME: application/vnd.in-toto+json
