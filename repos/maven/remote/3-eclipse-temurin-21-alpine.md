## `maven:3-eclipse-temurin-21-alpine`

```console
$ docker pull maven@sha256:e45339e025dd9df4d256b54133507495ce59d5473600bba1aff8a73bbaaed42b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-eclipse-temurin-21-alpine` - linux; amd64

```console
$ docker pull maven@sha256:6548adf065bc5d94e6d6e4fe38c2e2d02524f3270e72ba84c631f1b3ea9e1bae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.8 MB (195750661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:313447cc796120ec10c50ae712d89e9aea471a68ea236c2a970e196105efc366`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:59:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:59:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:59:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:59:09 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:59:09 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 17:59:14 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='6d3c2b956d6b837bfdc992e58488fb16c96e5852820e9feaa42a8672bbca9c7b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='52e30d3157432e87ee464b656f776f0a22946f1f3182eea779258284bc6f55da';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Sat, 08 Nov 2025 17:59:16 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:59:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:59:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 17:59:16 GMT
CMD ["jshell"]
# Wed, 17 Dec 2025 20:06:55 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Wed, 17 Dec 2025 20:06:55 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 17 Dec 2025 20:06:55 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:06:55 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:06:55 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 17 Dec 2025 20:06:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 17 Dec 2025 20:06:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 17 Dec 2025 20:06:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 17 Dec 2025 20:06:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 17 Dec 2025 20:06:56 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 17 Dec 2025 20:06:56 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 17 Dec 2025 20:06:56 GMT
ARG USER_HOME_DIR=/root
# Wed, 17 Dec 2025 20:06:56 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 17 Dec 2025 20:06:56 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 17 Dec 2025 20:06:56 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604c946e03558d5b63598812078583a7cacf7c19412e2c71732c6c7e972a09e0`  
		Last Modified: Sat, 08 Nov 2025 17:59:43 GMT  
		Size: 21.1 MB (21112184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34da1dc78644035d0dc76bd344bb33911551088d2c35e5eae20ee0883291ece`  
		Last Modified: Sat, 08 Nov 2025 18:21:14 GMT  
		Size: 158.1 MB (158102933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a3991c44d0e9016c97a7a16b122fc35778b7bf3abb694a7acabc5f8e6551c8`  
		Last Modified: Sat, 08 Nov 2025 17:59:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8cb030eff3c05fd59aaea4464781aa26b800aef5bdbe8b20be44289a6d4fde7`  
		Last Modified: Sat, 08 Nov 2025 17:59:41 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d4bb48abc550441689f66036660c15cc73cedaae309d02293279322af70c04`  
		Last Modified: Wed, 17 Dec 2025 20:07:10 GMT  
		Size: 3.4 MB (3417393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06447ddb9b0991a431ca17cf8624223ee932c1c2800e5e4a759c30076dd5cd9`  
		Last Modified: Wed, 17 Dec 2025 20:07:11 GMT  
		Size: 9.3 MB (9312244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b711ac569788305973ba4f7f8d7388fc12bb7f87e9460bfc91ddeb4a0d4e5e48`  
		Last Modified: Wed, 17 Dec 2025 20:07:10 GMT  
		Size: 860.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7193942e7c3eafbd08c654371d90542145a59c681dd2f23d15e1aa300ddffa9b`  
		Last Modified: Wed, 17 Dec 2025 20:07:10 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:14bba28f473d86dd1f9b981f3461072947101b7ff927a79593bab477bd0c3cf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1258181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227ad45615dff21fe642c820df87e80ac114e3357db99e05c70eecdc31d1d991`

```dockerfile
```

-	Layers:
	-	`sha256:771c60498ba7a0f079b84db037014454780a1bed5c7a402cc38322025fbab29d`  
		Last Modified: Wed, 17 Dec 2025 21:32:10 GMT  
		Size: 1.2 MB (1238834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9f41faa6a86ce40d7877b1f0fe9f6d2a7d51bea9255f5531e60894f9114d242`  
		Last Modified: Wed, 17 Dec 2025 21:32:11 GMT  
		Size: 19.3 KB (19347 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-21-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:918ffe9d3cf5ad173e10e1bdd587ff0ac8c7f08df6a616bf89d82697f082b06b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.2 MB (194192298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d26799ef92deff6568b7c846f6337157647ad87d0b67726ae44c76e5c9db54b3`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:58:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:30 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:58:30 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 17:58:37 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='6d3c2b956d6b837bfdc992e58488fb16c96e5852820e9feaa42a8672bbca9c7b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='52e30d3157432e87ee464b656f776f0a22946f1f3182eea779258284bc6f55da';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Sat, 08 Nov 2025 17:58:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 17:58:38 GMT
CMD ["jshell"]
# Wed, 17 Dec 2025 20:07:34 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Wed, 17 Dec 2025 20:07:34 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 17 Dec 2025 20:07:34 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:07:34 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:07:34 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 17 Dec 2025 20:07:34 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 17 Dec 2025 20:07:34 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 17 Dec 2025 20:07:34 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 17 Dec 2025 20:07:34 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 17 Dec 2025 20:07:34 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 17 Dec 2025 20:07:34 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 17 Dec 2025 20:07:34 GMT
ARG USER_HOME_DIR=/root
# Wed, 17 Dec 2025 20:07:34 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 17 Dec 2025 20:07:34 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 17 Dec 2025 20:07:34 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534675d10f4caa61d314d425f92d547712626251f89901c5d58eac317205e1c5`  
		Last Modified: Sat, 08 Nov 2025 17:59:06 GMT  
		Size: 21.2 MB (21164202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac0dd9c7e27c9284c00f27ca9959b156926e12010ba8683e583ff6811916f12`  
		Last Modified: Sat, 08 Nov 2025 18:22:14 GMT  
		Size: 156.1 MB (156097412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c7361609fe55d3eb9a77ca907ab0d5f394b754ecf497fbd624cd8fe359a6db`  
		Last Modified: Sat, 08 Nov 2025 17:59:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867c03b825a35a5db0249203ef051f7e12f2bc4c110f281f6de68072d3c55bab`  
		Last Modified: Sat, 08 Nov 2025 17:58:49 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419c0f76fbcee788fc1a3aa1d65fa0f0159a74ee8afe282ca865f98738bf8dc5`  
		Last Modified: Wed, 17 Dec 2025 20:07:51 GMT  
		Size: 3.5 MB (3476918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086d557641bcc2b18bcadc18c2e990b0d89f3ea0d17fc60ed71504f27f78d916`  
		Last Modified: Wed, 17 Dec 2025 20:07:52 GMT  
		Size: 9.3 MB (9312245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a4ec7cc6c77f4cd3f3f64bb0917b80988ca2355acd9b73e643aeaaff935214`  
		Last Modified: Wed, 17 Dec 2025 20:07:50 GMT  
		Size: 859.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb590ac98fcde366e9fa42ce4277ae6ca466f15593132841cc6e840e384e92a`  
		Last Modified: Wed, 17 Dec 2025 20:07:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:86da04e8bf72650dfe1439ef5c316a953a4464777beffb079ef29b7c696a872d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1408315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76b552420f9921a1937a4410783d116435d3a4cb1984ce5264e164a0d27be8e8`

```dockerfile
```

-	Layers:
	-	`sha256:c4594e5202125606ac02986860a8b34f12c7146e28c4910d9a6cbfabaaccd600`  
		Last Modified: Wed, 17 Dec 2025 21:32:23 GMT  
		Size: 1.4 MB (1388836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73ef2db571a1c38ea72ca324c142ba65008023bb3578fa869070fda764b32f42`  
		Last Modified: Wed, 17 Dec 2025 21:32:24 GMT  
		Size: 19.5 KB (19479 bytes)  
		MIME: application/vnd.in-toto+json
