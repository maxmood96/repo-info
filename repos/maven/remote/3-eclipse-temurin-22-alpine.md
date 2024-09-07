## `maven:3-eclipse-temurin-22-alpine`

```console
$ docker pull maven@sha256:159cf7ea3da7ffd3b87378f099a8d2c325ef8a07006b6a6afb92140e4a9d10ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-eclipse-temurin-22-alpine` - linux; amd64

```console
$ docker pull maven@sha256:7c4189d50fc8c62394e315086f7b1fe13373600bcb57990bbbeb19e3ccdd847f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.8 MB (187761345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79c22cad528e22841884f1b25f7641840f57ffa858847f46134a73e4adf6dfa3`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 19 Aug 2024 08:57:28 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["/bin/sh"]
# Mon, 19 Aug 2024 08:57:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 19 Aug 2024 08:57:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 Aug 2024 08:57:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 19 Aug 2024 08:57:28 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ENV JAVA_VERSION=jdk-22.0.2+9
# Mon, 19 Aug 2024 08:57:28 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='8ac93a2d5a55aabbc0f7156c2f9032026e87c185689d628ef8a4184b6e9ab006';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_aarch64_alpine-linux_hotspot_22.0.2_9.tar.gz';          ;;        x86_64)          ESUM='49f73414824b1a7c268a611225fa4d7ce5e25600201e0f1cd59f94d1040b5264';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_x64_alpine-linux_hotspot_22.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["jshell"]
# Mon, 19 Aug 2024 08:57:28 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 19 Aug 2024 08:57:28 GMT
ARG USER_HOME_DIR=/root
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 19 Aug 2024 08:57:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591c34627c847892ee87160ccb0488eb4484039dd04d400e9e86561f15459495`  
		Last Modified: Fri, 06 Sep 2024 22:44:13 GMT  
		Size: 14.0 MB (14032627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559b8137bd4921c799557192bcefdb6c2f1832441cf79262428b2a1c59d17813`  
		Last Modified: Fri, 06 Sep 2024 22:45:43 GMT  
		Size: 156.7 MB (156688135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00c325b8130f16dc6563e15cd93765be1f9170d7cb6aa5c0a8e02719526393d`  
		Last Modified: Fri, 06 Sep 2024 22:45:31 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7d061fa70b7ad0d36e9fc85adeddd91a56155fd7b7f74805d65ec02d86c723`  
		Last Modified: Fri, 06 Sep 2024 22:45:31 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8847d0a326fd6aeeda41fa50aeb8f7272d39123efe284975cb39a073e952f845`  
		Last Modified: Sat, 07 Sep 2024 00:11:34 GMT  
		Size: 4.2 MB (4243026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8908f4441af97286eab522e13337dde9a89e756c57144f0249af4c9936f423`  
		Last Modified: Sat, 07 Sep 2024 00:11:34 GMT  
		Size: 9.2 MB (9170440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf87a5b7ff5cad7a9d1ab14635477c9589fb8f6df838bad0a5683168c95da95`  
		Last Modified: Sat, 07 Sep 2024 00:11:33 GMT  
		Size: 858.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a52054710c0a48205ab1e54cdf2bac03676083ddd4a83a821b636eb11a0f51b`  
		Last Modified: Sat, 07 Sep 2024 00:11:33 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-22-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:fb02ea5759450b77a9042a803e4e634b8f6b4de54efc03969e81713b6bd95a2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **994.8 KB (994824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ccecf8cd92d047c5771971aebcd954de864fa8cd07238408a9363d20252b8b`

```dockerfile
```

-	Layers:
	-	`sha256:bf5a0d53b43e1d6f102cf76eb55b450e6bfe8cfb1c7452d5693e200b74853f6a`  
		Last Modified: Sat, 07 Sep 2024 00:11:33 GMT  
		Size: 975.5 KB (975466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04301820926325c1e54d6d1c928ee3b40102aeabb301960952b65f4027e9568d`  
		Last Modified: Sat, 07 Sep 2024 00:11:33 GMT  
		Size: 19.4 KB (19358 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-22-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:fe7e0628a2689a8a2d278ad7d144fc57fda28a1681b276f3fc7f779176377bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.5 MB (186456308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b528be828cb8b44d69ace1fe93292e1c842fd2b90d90b8fbbf49f9b79c7b18`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Mon, 19 Aug 2024 08:57:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 19 Aug 2024 08:57:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 Aug 2024 08:57:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 19 Aug 2024 08:57:28 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ENV JAVA_VERSION=jdk-22.0.2+9
# Mon, 19 Aug 2024 08:57:28 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='8ac93a2d5a55aabbc0f7156c2f9032026e87c185689d628ef8a4184b6e9ab006';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_aarch64_alpine-linux_hotspot_22.0.2_9.tar.gz';          ;;        x86_64)          ESUM='49f73414824b1a7c268a611225fa4d7ce5e25600201e0f1cd59f94d1040b5264';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_x64_alpine-linux_hotspot_22.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["jshell"]
# Mon, 19 Aug 2024 08:57:28 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 19 Aug 2024 08:57:28 GMT
ARG USER_HOME_DIR=/root
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 19 Aug 2024 08:57:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2478f4a9466e915a5997ded853c525c23643a703902fa3b4e95b2c80136f5c87`  
		Last Modified: Thu, 25 Jul 2024 17:46:42 GMT  
		Size: 14.4 MB (14369016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15272a94a5cba129ac4e863de378ce4664fb3369cd14db2139a70584c1af3223`  
		Last Modified: Thu, 25 Jul 2024 17:48:10 GMT  
		Size: 154.5 MB (154451742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a151e7b51b09f040c06d05d09617ee7592bcd9f2e74ce173126bc8324b54101e`  
		Last Modified: Thu, 25 Jul 2024 17:48:00 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b1bd3bcf9378572c3d574289461b590c70f5430c82f6ccf5fd311245e4dac3`  
		Last Modified: Fri, 23 Aug 2024 19:46:57 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2265252ec2b7433633d8f491ff23959d366daea97c28dd53c7a851cb6d3b16b`  
		Last Modified: Sat, 24 Aug 2024 03:11:11 GMT  
		Size: 4.4 MB (4374871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a081043e076a37e1c537760c8561db72db4a60fc724319355a7e5ea1840b6109`  
		Last Modified: Sat, 24 Aug 2024 03:11:11 GMT  
		Size: 9.2 MB (9170439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40acbd2fb390ce1a1bfca139e18dbbf28e9e93a5371a2cef4bda69b4a917bcae`  
		Last Modified: Sat, 24 Aug 2024 03:11:11 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34de6fc51f47e4eeb4a11f9180e915cce92bfe1299553f0fc226c351843ba2e9`  
		Last Modified: Sat, 24 Aug 2024 03:11:11 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-22-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:3f508a30f141f18a38c9a648c2d8d9b8944783a70ccedeae5e13c42ccfb12a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1100782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c356b414c207614ea1b6987bde412bd89b19ee539bfa6efe6c20763c8911f69a`

```dockerfile
```

-	Layers:
	-	`sha256:906aaf9623338774a279f25298efe21231dba49a165b646aad9f298fceaf6994`  
		Last Modified: Sat, 24 Aug 2024 03:11:11 GMT  
		Size: 1.1 MB (1080766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd5a2e8197b3ada962ac331160d8b4c58225fdcfcf9a9a1fbbfdc560f2fb422b`  
		Last Modified: Sat, 24 Aug 2024 03:11:10 GMT  
		Size: 20.0 KB (20016 bytes)  
		MIME: application/vnd.in-toto+json
