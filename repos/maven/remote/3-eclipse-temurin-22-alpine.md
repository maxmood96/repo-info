## `maven:3-eclipse-temurin-22-alpine`

```console
$ docker pull maven@sha256:afc6bd249f957beaa982a411c9ed9ff09d023aebed1c4b3e97b5b30a32bc0a47
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-eclipse-temurin-22-alpine` - linux; amd64

```console
$ docker pull maven@sha256:933407864e22b16e8a79035ee8aea007e2faa22baa603b36b5ed8c664ea4dba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.8 MB (187761342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e942fab4fa3dfb48b347b64b85cf119ec2dfe5c760ff5b65092fffa7496eea4`
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
	-	`sha256:34c98b5ab7b96fc483a1a02aa1165f9731a145bfed5f72598d4beb4cbaab2837`  
		Last Modified: Tue, 17 Sep 2024 03:01:21 GMT  
		Size: 4.2 MB (4243027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24aed51fd085928af8975da486b0bff0fbd9a993d17dd2ac768d7ef9c5ecd94`  
		Last Modified: Tue, 17 Sep 2024 03:01:22 GMT  
		Size: 9.2 MB (9170434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f624c78c4db029012e81d82b94c32fa6b450621b3036b8542e8b7c5a0c40063`  
		Last Modified: Tue, 17 Sep 2024 03:01:21 GMT  
		Size: 859.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d19963e4a4f1c7d2ec4a44a7c497f67a1ad162c79b7af4b80787423d62e31e1`  
		Last Modified: Tue, 17 Sep 2024 03:01:21 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-22-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:7de52a5899ab87bb7a3f8c57f5e3c46e1d218c20e5e5186fc18cb295e83d1bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **994.8 KB (994824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f97ca270c929183472c4c03608e1aea3e4208ae38ba66a9306abda54c174c8e`

```dockerfile
```

-	Layers:
	-	`sha256:2b4cc654983eb079f5cd60b02c7be27288c6a224d745c371bcccbcc592844c87`  
		Last Modified: Tue, 17 Sep 2024 03:01:21 GMT  
		Size: 975.5 KB (975466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dcca7cf8ad82294213bdfedd25c870b91c7937202a66ba6a5a17a705a053a16`  
		Last Modified: Tue, 17 Sep 2024 03:01:21 GMT  
		Size: 19.4 KB (19358 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-22-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:23c4f5354b6a85d3a5216ba159b6469f5667b784053dd68d8c2bc5135d2062bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.4 MB (186449947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f252a3ef629c6b71d250e3c10cf24faa1bbf22c161847abee834e9ef89627dd6`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 19 Aug 2024 08:57:28 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8a2d3622211b600f84f1b27f8913afa35a6719e1ddde90ee5afb4bc8b95868`  
		Last Modified: Fri, 06 Sep 2024 23:28:36 GMT  
		Size: 14.4 MB (14361804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094715011aeed129ffc8ee3a3f6a66d001c2c3efddadd367324fa7b309468b27`  
		Last Modified: Fri, 06 Sep 2024 23:29:21 GMT  
		Size: 154.5 MB (154451673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd96d9d855f0efc9062857cd2bb01daca27563089131929d7c8106ed40f85bc`  
		Last Modified: Fri, 06 Sep 2024 23:29:11 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4d5e72eab1f277450299cf89cb0e1fdd45bdc188be802931b56acc33836ea0`  
		Last Modified: Fri, 06 Sep 2024 23:29:11 GMT  
		Size: 2.1 KB (2106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de088245cf0a276937db1a7ddf504435aec7843f120ec6c7afd94bfc22bc9f3`  
		Last Modified: Sat, 07 Sep 2024 12:24:14 GMT  
		Size: 4.4 MB (4375074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3317ba56bfc39a880bfe63c102a6f930de17c920a86c26b56febab9d0b4da0`  
		Last Modified: Sat, 07 Sep 2024 12:24:14 GMT  
		Size: 9.2 MB (9170440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7c776a1d3e3a5ba0aa06ea850db2e6dbb7381fe11dd801596ddc495a550fde`  
		Last Modified: Sat, 07 Sep 2024 12:24:13 GMT  
		Size: 858.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef42cafe24292f9c744a8bf62d90ff1e04441805b93a3447b8d7bd0c79a91064`  
		Last Modified: Sat, 07 Sep 2024 12:24:13 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-22-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:c94466d594e4d9c8fcbb391c13fcfc673f7b3579cc2c98ed0077b9315229b856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1100782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd0e8be33244bf98021691142bfcdca3bd8e5abfa0f50c9284cf50cf48a0489`

```dockerfile
```

-	Layers:
	-	`sha256:4b8928ed8e89e79fb191d6343f6a38b0e2256e0ae01b162cb7ada00d217be45a`  
		Last Modified: Sat, 07 Sep 2024 12:24:14 GMT  
		Size: 1.1 MB (1080766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3f5e2cce17f091268e4c97fb3b824acdd84d9bbed7f0f539a5e9295284fd004`  
		Last Modified: Sat, 07 Sep 2024 12:24:13 GMT  
		Size: 20.0 KB (20016 bytes)  
		MIME: application/vnd.in-toto+json
