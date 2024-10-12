## `maven:3-eclipse-temurin-23-noble`

```console
$ docker pull maven@sha256:5ddc23a764108682937064c4da1ed510f8e07ebe244935807a37bcd687f53fb1
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
$ docker pull maven@sha256:0e08a2ca44eb7cd72580e7cfcc58a9947ff9808c2c577b0a8e2a8616022cd0b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (245969619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cda6de28b64ce97d9d19d69b97bf938fd7da0843fe8f2f0b44d11872790db893`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:55 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:58 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Mon, 16 Sep 2024 06:23:59 GMT
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
	-	`sha256:43cc87cb0cd1fc1c0b6c8670fa2a07f84e6af2cd95bce48b7909b42cca8e5fc1`  
		Last Modified: Fri, 20 Sep 2024 15:05:59 GMT  
		Size: 30.0 MB (29952705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212edad047af411595279704a7b7bfe372a0db6ebb7cc2a85203e432a918a984`  
		Last Modified: Wed, 02 Oct 2024 01:28:48 GMT  
		Size: 19.0 MB (19005121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c235ecc5e3f1c16307d00226877dc3cead92325fe52503dcffb8eace7b32e5a`  
		Last Modified: Wed, 02 Oct 2024 01:28:56 GMT  
		Size: 163.3 MB (163256295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e481e76c03a4158171b8c316cff1e3c3a84920b7a53da5bc1dd02579bbb794`  
		Last Modified: Wed, 02 Oct 2024 01:28:45 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1febdc356d2517295f94b4b249a10845f51e58baef035dd29198f61e712eb5b`  
		Last Modified: Wed, 02 Oct 2024 01:28:45 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdb888ce97d972b5cfbc2e9a5c7d7dc1d00c025310a6463cb6530e69bfc1b49`  
		Last Modified: Wed, 02 Oct 2024 06:48:48 GMT  
		Size: 24.6 MB (24581764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0573586549a5d14fed7bfa8ba28274a429c8747fad6e490bbed71ed348b3c2b2`  
		Last Modified: Wed, 02 Oct 2024 06:48:48 GMT  
		Size: 9.2 MB (9170442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4174fa27f37dcecfe829ccb48b2cca28828a91d40b9b870da622646313d877`  
		Last Modified: Wed, 02 Oct 2024 06:48:47 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764b51d491e29f5bd85cf1a396af80561a73d14bc90e2c65bf3c4bfb29f3e37e`  
		Last Modified: Wed, 02 Oct 2024 06:48:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-23-noble` - unknown; unknown

```console
$ docker pull maven@sha256:1b21a58dc43a0438c1c15d28cf6a81f6f20df0235d22529a97926fafbf3fa405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4892836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f92d5867d72243de872791f4b9ccb2324739518742576bafe460c2f94c0e16d`

```dockerfile
```

-	Layers:
	-	`sha256:b321163fa5608cb29cd2fdde96ee852fbd0c5ab5243147648b4a410b06aa0880`  
		Last Modified: Wed, 02 Oct 2024 06:49:44 GMT  
		Size: 4.9 MB (4873034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ee738a75453daea656d5754b60fe9bca0f4572dbf759a101a8bbcbf06b0c9fc`  
		Last Modified: Wed, 02 Oct 2024 06:49:44 GMT  
		Size: 19.8 KB (19802 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-23-noble` - linux; ppc64le

```console
$ docker pull maven@sha256:22102fda8a8929771e4780cdf182a436ac58707d8545ef524d16721190d52c08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.8 MB (256755824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c92fbbe4412755bfeaa4aac746e965aac029612e974215ea02dfb6557dc55ef`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 16 Sep 2024 06:25:02 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:25:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:25:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:25:02 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:25:05 GMT
ADD file:5fe4accfd69653c9efcd106650478901cff305ef72427da563b841cc55cd5df4 in / 
# Mon, 16 Sep 2024 06:25:05 GMT
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
	-	`sha256:d3b933ab36d7d3de2d3d18b1141e06a388bb6b545afd828222778b868adbc114`  
		Last Modified: Wed, 02 Oct 2024 01:55:43 GMT  
		Size: 35.5 MB (35517922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c6be8ab4a8decb4dc1814ecfbf2eab0826a3950f3ccc9782df5b5e1e99f1b7`  
		Last Modified: Wed, 02 Oct 2024 02:10:04 GMT  
		Size: 17.8 MB (17768333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3573e037bcdcd23f2aebb73cc5ae98e9ca3335515537d96a4bd33a45801ee0`  
		Last Modified: Wed, 02 Oct 2024 02:10:16 GMT  
		Size: 165.2 MB (165157590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591c46d4c12e2daf606a01d91aa9b65ff04e44964e7e3b189a008fa7b53b5e73`  
		Last Modified: Wed, 02 Oct 2024 02:10:01 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437508c5f1e2f8a8ed78dc3fdd94ef1eb583e1411a750b7e62b15ccff80182a9`  
		Last Modified: Wed, 02 Oct 2024 02:10:00 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb921b2e6660bb7e22c753f0f1f1ae2fb9180b52a61ec614be1a9b76cca06217`  
		Last Modified: Wed, 02 Oct 2024 04:58:31 GMT  
		Size: 29.1 MB (29138235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3079d4e53c8df09fe22f178b4219063e3a57c0614e874820ecfd3a6e662569fa`  
		Last Modified: Wed, 02 Oct 2024 04:58:31 GMT  
		Size: 9.2 MB (9170450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c07f56369354e05d2a69b3734698ef11e3eecd914fff8e9389f9406ef2e430`  
		Last Modified: Wed, 02 Oct 2024 04:58:30 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99dfbf83023df6fadfd8eabeaa47c28f97d4a26345999346c30e32637bb26ff1`  
		Last Modified: Wed, 02 Oct 2024 04:58:30 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-23-noble` - unknown; unknown

```console
$ docker pull maven@sha256:4afb85cf788ad0c0b7400a8c45688e1caae0678727c3e43ccae584134b1d41fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4806042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a41dfc5da49eb22e649db37fa371873dacddd04daeade7b5d8e948aedec25ddc`

```dockerfile
```

-	Layers:
	-	`sha256:c2d8de455eebe0df2ba333e4404aee6b1d7966a02ce0a7adb37e27a2f740dbbb`  
		Last Modified: Wed, 02 Oct 2024 04:58:53 GMT  
		Size: 4.8 MB (4786323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82a38d1b9e9a37e1c19f4baf48a556ff02681e03ffe976d3099013cebc8a94ce`  
		Last Modified: Wed, 02 Oct 2024 04:58:52 GMT  
		Size: 19.7 KB (19719 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-23-noble` - linux; s390x

```console
$ docker pull maven@sha256:621f50f781d452f63a92bb6963ce6f3f700dd3fbcd1316b10a563684bef903d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.8 MB (236766642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea1497c1b0b06c3a741ae6fad6a9b2f614c4d8bbddb5049eddfcb5ff1959641d`
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
ADD file:ed84c120e781b2f48856752e1e38d21db0bed5e09a2a64f961f004a4906abcb6 in / 
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
	-	`sha256:220da50193dc0598aa4f0418f3c1f89ed396983e85b2032ceeac1e4e044e443a`  
		Last Modified: Sat, 12 Oct 2024 00:18:34 GMT  
		Size: 30.7 MB (30663130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811c74b4ed884b0b9b22d6b2e8ff8d4190ccc9741918d6d9b522bca8f78dc3e0`  
		Last Modified: Sat, 12 Oct 2024 00:27:18 GMT  
		Size: 16.7 MB (16696966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2559b893b398119f20de285710274fc95b4ac51d3989e54ac09b6f95abaebd35`  
		Last Modified: Sat, 12 Oct 2024 00:27:31 GMT  
		Size: 154.4 MB (154375350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cfbd731c33f5b9f9015a53830e7971b2b68268abf26606b4b3a738b1d8b7e4`  
		Last Modified: Sat, 12 Oct 2024 00:27:15 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349d4007d0d1eb7bcc4400b9a360cd9df21f41cc504957ff50ef8878327611ed`  
		Last Modified: Sat, 12 Oct 2024 00:27:15 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9cc01d05967d7b2ea93bb6076373999a94d2bf6dab30420222a768b29898a7`  
		Last Modified: Sat, 12 Oct 2024 01:59:02 GMT  
		Size: 25.9 MB (25857476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51eb8b7691d82436e523c191fe68823c1a81b91364ee389bf88fafa52170f5b`  
		Last Modified: Sat, 12 Oct 2024 01:59:01 GMT  
		Size: 9.2 MB (9170430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f67892dc8ec58e39097b404d180769b035d258128c2454d1440e0c4cd7d5c8`  
		Last Modified: Sat, 12 Oct 2024 01:59:01 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2c527349abe56c441cfb3a4c0f099f2152a0f33814ef4d5dc10e8f2e326212`  
		Last Modified: Sat, 12 Oct 2024 01:59:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-23-noble` - unknown; unknown

```console
$ docker pull maven@sha256:5ef53f3662f903313559168c17b80150647eac5c9787f5081514fb9581eb4543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4701602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5f5f01791bdf05ebc13ed849c059b6cbbff18ffc8ee2cf9099d6796442ee97`

```dockerfile
```

-	Layers:
	-	`sha256:1a4e412d0e77217969bd5072ed9ebacfad6a916c15ccbcab77be241d5f816799`  
		Last Modified: Sat, 12 Oct 2024 01:59:30 GMT  
		Size: 4.7 MB (4681894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c685f1e070118af29475ea7491e4c6ff212644eb3f7dd563e9c1dd3252e4dc4`  
		Last Modified: Sat, 12 Oct 2024 01:59:30 GMT  
		Size: 19.7 KB (19708 bytes)  
		MIME: application/vnd.in-toto+json
