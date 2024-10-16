## `maven:3-eclipse-temurin-23-noble`

```console
$ docker pull maven@sha256:7ab00ece517cbfc3e1e1ac10db74581144f18aa886232cc5b7cf1e33b1744e86
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

### `maven:3-eclipse-temurin-23-noble` - linux; amd64

```console
$ docker pull maven@sha256:095b8d01e2db2922c927844495f0817a65df45794aacd4e49bd79cb4be7fa6df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.4 MB (247382024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6e3e62878b6fb79f1d1a069f8a8bcb296372a2f334211f4227a281e91ab261`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 23 Sep 2024 17:02:08 GMT
ARG RELEASE
# Mon, 23 Sep 2024 17:02:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Sep 2024 17:02:08 GMT
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Sep 2024 19:12:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 19:12:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_VERSION=jdk-23+37
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='630c4f3870056e7e005736ec1edc34ee63a9b45e2027582c52f53a9bf44314b8';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_x64_linux_hotspot_23_37.tar.gz';          ;;        arm64)          ESUM='e8043d1bd9c4f42c5cf7883aca1fc3ef6bcccf4a664f378818ac0fd4fb987b7e';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_aarch64_linux_hotspot_23_37.tar.gz';          ;;        ppc64el)          ESUM='4d3b0609c783dea1f6a899bfc8c84b4000d1f48f39e2489d70050bbf2c7f7d9c';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_ppc64le_linux_hotspot_23_37.tar.gz';          ;;        riscv64)          ESUM='d401699a92469de7bfb72909c1d11019537a0a2c21af01a8dce1831f09ef5165';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_riscv64_linux_hotspot_23_37.tar.gz';          ;;        s390x)          ESUM='2f9cb1db72ddc91f0b90904d038bca9314bc0bafedb0efe1233469bf3c934e58';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_s390x_linux_hotspot_23_37.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 18 Sep 2024 19:12:13 GMT
CMD ["jshell"]
# Mon, 23 Sep 2024 17:02:08 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 23 Sep 2024 17:02:08 GMT
ARG USER_HOME_DIR=/root
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 23 Sep 2024 17:02:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:aed300f9456f1ba3649e409619ab8495b52eea254997f9293d3fa2f1a213be79`  
		Last Modified: Thu, 10 Oct 2024 03:03:25 GMT  
		Size: 30.6 MB (30613278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61fab2e8b4527848f1e9a3937408cae252744250c63d4215a03c70d4d7982548`  
		Last Modified: Fri, 11 Oct 2024 23:58:48 GMT  
		Size: 17.8 MB (17834149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ced065f01cb550e27791897f3c8787eb923ae491d0a1ba5db9c6aa4fd8fca62`  
		Last Modified: Fri, 11 Oct 2024 23:58:58 GMT  
		Size: 165.3 MB (165273668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be28238e6394ae0a49c723d3cad8481133a5178f94d22b04b5d81c05d203fb17`  
		Last Modified: Fri, 11 Oct 2024 23:58:45 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163024d7191a7420b9f48bf8c7054d20428023d4220c620c168d06a490c83fa4`  
		Last Modified: Fri, 11 Oct 2024 23:58:45 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14488807fd9cf4670060ee3f252fedd178ab92e2ccae80288244234d5fa596c`  
		Last Modified: Sat, 12 Oct 2024 01:55:41 GMT  
		Size: 24.5 MB (24487215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55a15e18e15965d4d20856684070d8f1699e983e188302577d560a7976e7d85`  
		Last Modified: Sat, 12 Oct 2024 01:55:38 GMT  
		Size: 9.2 MB (9170423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:577532588f8bb2e80e55f14abaa17f39e29a25eba6a6d766f696d2338a452452`  
		Last Modified: Sat, 12 Oct 2024 01:55:37 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952aec8b5089593030e6d778fac6604c333a241009acf441c9747f7f2964abe0`  
		Last Modified: Sat, 12 Oct 2024 01:55:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-23-noble` - unknown; unknown

```console
$ docker pull maven@sha256:86c028b58aa2005ab849dbc77021d77f34f65b3bea351480165910b3d53f22a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4756255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eab6ee5419fc81da4070b7296ba53b8f942341de6b694698a4709317fe119bfa`

```dockerfile
```

-	Layers:
	-	`sha256:a0620ff65eb7926b90fa86e8c29d7371d3401ae7444d7bc77b88b852710b4997`  
		Last Modified: Sat, 12 Oct 2024 01:55:38 GMT  
		Size: 4.7 MB (4736571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f81be18d38eace397659a12be4a550983ab3bc654b10cf7b194175bc4a50503`  
		Last Modified: Sat, 12 Oct 2024 01:55:37 GMT  
		Size: 19.7 KB (19684 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-23-noble` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:d62b9e950346da140d1e21065e588d906bbaaea04b3d9ff32da26ae1298254d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (245978021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7976dd3b8927f46f0ad22657aea4b4e303a0ff25438264172072aefd827e6a1b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 23 Sep 2024 17:02:08 GMT
ARG RELEASE
# Mon, 23 Sep 2024 17:02:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Sep 2024 17:02:08 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Sep 2024 19:12:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 19:12:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_VERSION=jdk-23+37
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='630c4f3870056e7e005736ec1edc34ee63a9b45e2027582c52f53a9bf44314b8';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_x64_linux_hotspot_23_37.tar.gz';          ;;        arm64)          ESUM='e8043d1bd9c4f42c5cf7883aca1fc3ef6bcccf4a664f378818ac0fd4fb987b7e';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_aarch64_linux_hotspot_23_37.tar.gz';          ;;        ppc64el)          ESUM='4d3b0609c783dea1f6a899bfc8c84b4000d1f48f39e2489d70050bbf2c7f7d9c';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_ppc64le_linux_hotspot_23_37.tar.gz';          ;;        riscv64)          ESUM='d401699a92469de7bfb72909c1d11019537a0a2c21af01a8dce1831f09ef5165';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_riscv64_linux_hotspot_23_37.tar.gz';          ;;        s390x)          ESUM='2f9cb1db72ddc91f0b90904d038bca9314bc0bafedb0efe1233469bf3c934e58';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_s390x_linux_hotspot_23_37.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 18 Sep 2024 19:12:13 GMT
CMD ["jshell"]
# Mon, 23 Sep 2024 17:02:08 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 23 Sep 2024 17:02:08 GMT
ARG USER_HOME_DIR=/root
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 23 Sep 2024 17:02:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:ea4ac7c2aed5e8bd05e7fcc8c0cd77ade510c4daf1690cfe93167a634eb81e4f`  
		Last Modified: Fri, 11 Oct 2024 18:11:40 GMT  
		Size: 30.0 MB (29952803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281f222bc79db09e568399b36dc24e86e77da3201df1247524f179e08d4ba074`  
		Last Modified: Wed, 16 Oct 2024 01:19:20 GMT  
		Size: 19.0 MB (19013016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71c086970ddc308820ead7432558cf95fd50099fd3dd67af6b09cfa9056458a`  
		Last Modified: Wed, 16 Oct 2024 01:19:29 GMT  
		Size: 163.3 MB (163256350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe2517f284b51de3e57cfd1d9d7c39fd44968fde73fde95e4c7633515c432c1`  
		Last Modified: Wed, 16 Oct 2024 01:19:18 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8980d81d23a210669113fd708554d9e2fd628112d62110d3b2d73738d0b89d6e`  
		Last Modified: Wed, 16 Oct 2024 01:19:18 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91cc3473ece462a53e3f433b9e9da2478464538c536fa863860344e63fb0951`  
		Last Modified: Wed, 16 Oct 2024 07:17:13 GMT  
		Size: 24.6 MB (24582128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065fcb501612a9e4f4aaa172cc1db4e8834e87d2bdfe3f1c056d6978d89a3342`  
		Last Modified: Wed, 16 Oct 2024 07:17:13 GMT  
		Size: 9.2 MB (9170436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f3a155ce6a5f7419f8556b94e85eb15050bac0f05f4afedb5a6fc068e49f62`  
		Last Modified: Wed, 16 Oct 2024 07:17:12 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5400a3b31a3d588185504c84c4a25cbddc1905c82f44a701e937b4bf5790db41`  
		Last Modified: Wed, 16 Oct 2024 07:17:12 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-23-noble` - unknown; unknown

```console
$ docker pull maven@sha256:b02a3640ddc166018b64210b517f388118a94a16f10cc80495c9a017d37e5ae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4893540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:970bd856521aa11ea77e682c3e230cdf97039a6ac01faa26a0e3f40e95a8b394`

```dockerfile
```

-	Layers:
	-	`sha256:1aa10857bb2e7b067530619febbaeb07bf418a31feefa3681f18ee9bdc9047ed`  
		Last Modified: Wed, 16 Oct 2024 07:18:15 GMT  
		Size: 4.9 MB (4873705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870b1fc029614924b4d742eedf09d75cede9ee36a675378cdb66279ece6abdf7`  
		Last Modified: Wed, 16 Oct 2024 07:18:15 GMT  
		Size: 19.8 KB (19835 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-23-noble` - linux; ppc64le

```console
$ docker pull maven@sha256:75162c1f963728c507c8bdeab99e164a5d102966982f8069131648fbe5b085e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.8 MB (256751362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:249237648fe044033d0a265eddf3114a0f1d3a23df454889f51e50995750d083`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 23 Sep 2024 17:02:08 GMT
ARG RELEASE
# Mon, 23 Sep 2024 17:02:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Sep 2024 17:02:08 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Sep 2024 19:12:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 19:12:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_VERSION=jdk-23+37
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='630c4f3870056e7e005736ec1edc34ee63a9b45e2027582c52f53a9bf44314b8';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_x64_linux_hotspot_23_37.tar.gz';          ;;        arm64)          ESUM='e8043d1bd9c4f42c5cf7883aca1fc3ef6bcccf4a664f378818ac0fd4fb987b7e';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_aarch64_linux_hotspot_23_37.tar.gz';          ;;        ppc64el)          ESUM='4d3b0609c783dea1f6a899bfc8c84b4000d1f48f39e2489d70050bbf2c7f7d9c';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_ppc64le_linux_hotspot_23_37.tar.gz';          ;;        riscv64)          ESUM='d401699a92469de7bfb72909c1d11019537a0a2c21af01a8dce1831f09ef5165';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_riscv64_linux_hotspot_23_37.tar.gz';          ;;        s390x)          ESUM='2f9cb1db72ddc91f0b90904d038bca9314bc0bafedb0efe1233469bf3c934e58';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_s390x_linux_hotspot_23_37.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 18 Sep 2024 19:12:13 GMT
CMD ["jshell"]
# Mon, 23 Sep 2024 17:02:08 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 23 Sep 2024 17:02:08 GMT
ARG USER_HOME_DIR=/root
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 23 Sep 2024 17:02:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:3bfa2652777e83aa1dc3e08ba4b8288b0567c5238e8b9e282751133f1ec79e5b`  
		Last Modified: Wed, 16 Oct 2024 01:44:26 GMT  
		Size: 35.5 MB (35511137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2ec16fbfa0c562f558165cb1c37a388c4a857e64ea51f1be35f118b7cd96e9`  
		Last Modified: Wed, 16 Oct 2024 01:48:33 GMT  
		Size: 17.8 MB (17769811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c548a5fa8697f80dd94cb70e3c91f58929aabc24fc4f85e81de2a441f76e32b6`  
		Last Modified: Wed, 16 Oct 2024 01:48:44 GMT  
		Size: 165.2 MB (165157539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20408ebe163cc495214b403cb95a869ff9b902b420a0ad4e4da68e7b2ac1b668`  
		Last Modified: Wed, 16 Oct 2024 01:48:29 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eecc938213f57a6666562f29e0cd7076803861ebe3e8bbe21bf5648e855c99e`  
		Last Modified: Wed, 16 Oct 2024 01:48:29 GMT  
		Size: 2.1 KB (2105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f496ff6c6b69e4f65f7d7d12e1e2929ade0a90f76bfdb622c14841705e19678`  
		Last Modified: Wed, 16 Oct 2024 07:11:33 GMT  
		Size: 29.1 MB (29139162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff8f691d6a1956800bb0d577900a813a8dab49c178160c5642aafbef4995e71`  
		Last Modified: Wed, 16 Oct 2024 07:11:32 GMT  
		Size: 9.2 MB (9170429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d69ab0fa825e363d1b3a8c7d5b61b1b1b0b6c6871ef690e910ef68d22cdb55`  
		Last Modified: Wed, 16 Oct 2024 07:11:32 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993bb475b5923c2d94f93219cceedfbd83b6a5efc31f3931ac76f37c9157a32b`  
		Last Modified: Wed, 16 Oct 2024 07:11:32 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-23-noble` - unknown; unknown

```console
$ docker pull maven@sha256:1e454a487fed75b40899d9c4e04ad5c267103a5e329675e57ca8be62c94575ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4806742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:963861912d6c829fe47772cffa8ae6d616d48bdd60a73a9e3555d48d8a765bb7`

```dockerfile
```

-	Layers:
	-	`sha256:0bdb50c9a26c9dbb2b21ec7349f9e07b62ac991f16689e69e8511c7ef395a0ac`  
		Last Modified: Wed, 16 Oct 2024 07:11:59 GMT  
		Size: 4.8 MB (4786990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b0a9806d1362aeed124eb409f9a7e29b9336c37dae4536b5863534eb91e62b3`  
		Last Modified: Wed, 16 Oct 2024 07:11:58 GMT  
		Size: 19.8 KB (19752 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-23-noble` - linux; s390x

```console
$ docker pull maven@sha256:dda43ce39b18563abada0f7c5287fba044b3b21b87c2a9e38bdb375e871afb1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.8 MB (236767631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96902a1daa46fc5dc466eec5d1eb949f4f7607f05488bef45f02ed59422be8b8`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 23 Sep 2024 17:02:08 GMT
ARG RELEASE
# Mon, 23 Sep 2024 17:02:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Sep 2024 17:02:08 GMT
ADD file:77ba16e2cf3c210906ec7587ab14314afc15cb73af4337fde69ac35187fdb263 in / 
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Sep 2024 19:12:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 19:12:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_VERSION=jdk-23+37
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='630c4f3870056e7e005736ec1edc34ee63a9b45e2027582c52f53a9bf44314b8';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_x64_linux_hotspot_23_37.tar.gz';          ;;        arm64)          ESUM='e8043d1bd9c4f42c5cf7883aca1fc3ef6bcccf4a664f378818ac0fd4fb987b7e';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_aarch64_linux_hotspot_23_37.tar.gz';          ;;        ppc64el)          ESUM='4d3b0609c783dea1f6a899bfc8c84b4000d1f48f39e2489d70050bbf2c7f7d9c';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_ppc64le_linux_hotspot_23_37.tar.gz';          ;;        riscv64)          ESUM='d401699a92469de7bfb72909c1d11019537a0a2c21af01a8dce1831f09ef5165';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_riscv64_linux_hotspot_23_37.tar.gz';          ;;        s390x)          ESUM='2f9cb1db72ddc91f0b90904d038bca9314bc0bafedb0efe1233469bf3c934e58';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_s390x_linux_hotspot_23_37.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 18 Sep 2024 19:12:13 GMT
CMD ["jshell"]
# Mon, 23 Sep 2024 17:02:08 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 23 Sep 2024 17:02:08 GMT
ARG USER_HOME_DIR=/root
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 23 Sep 2024 17:02:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:fbce550314e6331afd2ad455e770bf99838b047eaec77c6d995b82c2ba1a18ae`  
		Last Modified: Wed, 16 Oct 2024 01:17:45 GMT  
		Size: 30.7 MB (30661606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b2a719ada2500ffda0860c37127f9f294e1dfaca50f689d6806d1eb9331b91`  
		Last Modified: Wed, 16 Oct 2024 01:28:55 GMT  
		Size: 16.7 MB (16699629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff0385fc32817141df8f545502e80e8dec85e1fbc19b2ae029ba6ff16053b40`  
		Last Modified: Wed, 16 Oct 2024 01:29:05 GMT  
		Size: 154.4 MB (154375356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd083d077f27f40b0af456867763272c8ab18f36fb0e9f5ea1705eae89e1ede`  
		Last Modified: Wed, 16 Oct 2024 01:28:52 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0baf8b22bb56b7fe3aaa91fae5eb2b28686f7270d6f3f413156425b038a5b2`  
		Last Modified: Wed, 16 Oct 2024 01:28:52 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a3bd3810971e68edcdd1deaffb8ca05e00cb2c9b42c48a2b19fe0a11e78ebc`  
		Last Modified: Wed, 16 Oct 2024 02:55:02 GMT  
		Size: 25.9 MB (25857308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e2e88f9af036984b189305c75f06a53ee6952eea81296f7b3d5b8ac09565de`  
		Last Modified: Wed, 16 Oct 2024 02:55:01 GMT  
		Size: 9.2 MB (9170441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5b695a13b5e743a916a0f7c79dd015248a25851394c23228e7c9e4a03177da`  
		Last Modified: Wed, 16 Oct 2024 02:55:01 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e850595455592ebc3fb00dae17ab2a72eaa682dd668c89fca8d8e5b0381a89`  
		Last Modified: Wed, 16 Oct 2024 02:55:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-23-noble` - unknown; unknown

```console
$ docker pull maven@sha256:484097f3f212fc807dad09bac0dcf93846f61227693ae30f71cbc72b41b9f472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4701630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a921702072d01859681bf0d491c66b7721b0a773347440ebab336b1f300e543`

```dockerfile
```

-	Layers:
	-	`sha256:1a87164bef0bbd3b393fb705061596b821458db6621946742b39e03cd15efd19`  
		Last Modified: Wed, 16 Oct 2024 02:55:29 GMT  
		Size: 4.7 MB (4681922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a445eb8092d62e1f74ea8b35bf6d9b15cc4ba45b2eba7261e1793978ec9e05c`  
		Last Modified: Wed, 16 Oct 2024 02:55:29 GMT  
		Size: 19.7 KB (19708 bytes)  
		MIME: application/vnd.in-toto+json
