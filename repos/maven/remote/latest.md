## `maven:latest`

```console
$ docker pull maven@sha256:ac54e1d8310a08b48981e866a903e42a669605ef2de989f223a292db3fd8c533
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

### `maven:latest` - linux; amd64

```console
$ docker pull maven@sha256:6847cbbf21e159f97819f18336cf6bbc24a89f9eb6439317520d93f904e9a916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.8 MB (238847965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0443f2bd5577a33156d65c2838b120d7a67c4301cb19d0d779a7465aec0091ed`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Jun 2024 09:17:07 GMT
ARG RELEASE
# Thu, 27 Jun 2024 09:17:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 27 Jun 2024 09:17:07 GMT
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Jun 2024 09:17:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 09:17:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 27 Jun 2024 09:17:07 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 27 Jun 2024 09:17:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["jshell"]
# Thu, 27 Jun 2024 09:17:07 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ARG MAVEN_VERSION=3.9.8
# Thu, 27 Jun 2024 09:17:07 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:eb993dcd6942ffcb7633f2cb271bd4b0a275fc9bdc8f5100c5b4d24694cacf50`  
		Last Modified: Fri, 02 Aug 2024 03:03:23 GMT  
		Size: 30.6 MB (30567306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6d67df44ebaf68af30549648235de86e15355c7fc9afc496d8d73df71a7a3d`  
		Last Modified: Sat, 17 Aug 2024 01:12:58 GMT  
		Size: 19.8 MB (19765195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6557c86db85bcea2deb397076ac9076aae2b78362428ad52fe54491c58e4d5d`  
		Last Modified: Sat, 17 Aug 2024 01:14:24 GMT  
		Size: 158.6 MB (158587319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef80f85cafa0c73b350e8d0691bf54ea5fa4c2d1f41a1a8e89a6aba60f24b413`  
		Last Modified: Sat, 17 Aug 2024 01:14:11 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9481abb396227b94fd676537f4d4ed59e5ecb5ad290fc65747a1a486b728632a`  
		Last Modified: Sat, 17 Aug 2024 01:14:11 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a2de45a682650608a1f10479cecd6d81ffd103720167e5ff95965681878c07`  
		Last Modified: Sat, 17 Aug 2024 04:08:43 GMT  
		Size: 20.8 MB (20763252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b457da0d7e9457e0b7203460d9aed0d518be49d9edb68ae076834ff4071e246`  
		Last Modified: Sat, 17 Aug 2024 04:08:43 GMT  
		Size: 9.2 MB (9161815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abcef9ce1b7d8e6771eb958d51a3458e5ed8ceb4b2b3e079eabc968fee3fe19`  
		Last Modified: Sat, 17 Aug 2024 04:08:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a90bef484dfc3800ceb493d84709e99662575ffa0ac386606db98ad38ad06b6`  
		Last Modified: Sat, 17 Aug 2024 04:08:42 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:latest` - unknown; unknown

```console
$ docker pull maven@sha256:452bf2f47095cc7151abb3c86e447f0bec48ef1fa6abc0415e781913e8e048eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4543808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb3eeca477e826db5ed84feb7118449b043cfeb4b1bc1a21e0c742cc6b0b6c8d`

```dockerfile
```

-	Layers:
	-	`sha256:e31419e88d4aa7781cc2141e69b066e1c337c972aa9e4d630f886c0ee8ce68a0`  
		Last Modified: Sat, 17 Aug 2024 04:08:42 GMT  
		Size: 4.5 MB (4521825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdb5a46d045e5525ebee0dd4bb177813373ee926bf30977703a394f19b480540`  
		Last Modified: Sat, 17 Aug 2024 04:08:42 GMT  
		Size: 22.0 KB (21983 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:latest` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:87efcb976c5b4cff764ff2abe58ff3e74ec4f1412d18f0c92149bef76342b776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.6 MB (237635314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf83bb67c4b13d1095d425d0670488047a9362840dce9071531717ed3993ccd`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Jun 2024 09:17:07 GMT
ARG RELEASE
# Thu, 27 Jun 2024 09:17:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 27 Jun 2024 09:17:07 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Jun 2024 09:17:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 09:17:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 27 Jun 2024 09:17:07 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 27 Jun 2024 09:17:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["jshell"]
# Thu, 27 Jun 2024 09:17:07 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ARG MAVEN_VERSION=3.9.8
# Thu, 27 Jun 2024 09:17:07 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1567e7ea90b67fc95ccdeeec39bdc3045098dee7e0c604975b957a9f8c0e9616`  
		Last Modified: Fri, 02 Aug 2024 07:40:09 GMT  
		Size: 29.9 MB (29910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d730088f68183e8bde2999ed48782fec63b9dea3c9a5d270fdede5082140ac57`  
		Last Modified: Sat, 17 Aug 2024 01:35:47 GMT  
		Size: 21.0 MB (20962516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4105de25af7c03489996034670f466dddb57ca45b7dad87b2d26c92eb1db1a22`  
		Last Modified: Sat, 17 Aug 2024 01:37:02 GMT  
		Size: 156.8 MB (156756895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbee7ce321c46b65f54436cd5e6a6a60aa3507db38e8c83946e2b0de0bcede5`  
		Last Modified: Sat, 17 Aug 2024 01:36:52 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7d3bb90c425cffd4d0b14e1cc0212955f363af879db11b3eef07061e5c34b2`  
		Last Modified: Sat, 17 Aug 2024 01:36:52 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95df2dffda18a1c8f26bc26e45b340c318100a95616923ce3471fd79e067c721`  
		Last Modified: Sat, 17 Aug 2024 12:00:58 GMT  
		Size: 20.8 MB (20840984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d27e2099982f752db63cfab1366326c4886db8a468cf6fe65e81b821b47c687`  
		Last Modified: Sat, 17 Aug 2024 12:00:58 GMT  
		Size: 9.2 MB (9161813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e123277fa9517c93bdb8e130026d690a1c4abf974c14f730d94d970f8bb6d8`  
		Last Modified: Sat, 17 Aug 2024 12:00:57 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39162e6c29d96cac195a85e3a9eacf29ac38e85b839b786b4eb3103362baa572`  
		Last Modified: Sat, 17 Aug 2024 12:00:57 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:latest` - unknown; unknown

```console
$ docker pull maven@sha256:e13ec8b49db0fed2a34fb0a6917e7ddeb3b56e1ee66f57d5f3f0b9695b1c1119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4682984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06403a905eb43dec23fed54a290b5b83715efe9476a3930511f46010c0afdd42`

```dockerfile
```

-	Layers:
	-	`sha256:f6604f53cd8574b4a52113e7cafc4c13855618ee0f7d85191c8bca03a168ec1c`  
		Last Modified: Sat, 17 Aug 2024 12:00:57 GMT  
		Size: 4.7 MB (4660260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49f62e71de22d804373e60f0e24bbfac12a00831380a71a67df3420ae728b4f1`  
		Last Modified: Sat, 17 Aug 2024 12:00:57 GMT  
		Size: 22.7 KB (22724 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:latest` - linux; ppc64le

```console
$ docker pull maven@sha256:1103e21a4398ef3c3364ef60564e3a00ba337a84500b0917ea9ca502d2dd68c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.6 MB (250608465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0bfab86090c3cc4733821ca6a3120846bac2e594698a78325892d69c51b655`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 01 Aug 2024 14:23:51 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:23:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:23:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:23:51 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:23:55 GMT
ADD file:f6dda5643c6c5671bba452213beef0fdd84c17bc5e733964b8b6d98a44d522a3 in / 
# Thu, 01 Aug 2024 14:23:55 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Wed, 24 Jul 2024 22:19:06 GMT
CMD ["jshell"]
# Mon, 19 Aug 2024 08:57:28 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:6e87eba78bda982d63d6dcd89b529540108dd7b3549a594cdc780cc6e61b5b37`  
		Last Modified: Tue, 06 Aug 2024 02:06:20 GMT  
		Size: 35.6 MB (35627737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba790d65beede6367e6ad44a964053b08c93678b7b635f447b2dd3a94207b532`  
		Last Modified: Sat, 17 Aug 2024 01:02:23 GMT  
		Size: 20.2 MB (20224418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ee3e473b36e7cc775738c613afd12f88077106b67f1ae2517980634585711e`  
		Last Modified: Sat, 17 Aug 2024 01:04:01 GMT  
		Size: 158.8 MB (158827535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9ffed7ae83d4cb72dcae37ba5d9fe3f15803b9eb24794e9e7c6b1733071b07`  
		Last Modified: Sat, 17 Aug 2024 01:03:46 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e81457b1518296186f1c4f7a60430f4a71f33353b39030ef6295b6cac0344ee`  
		Last Modified: Sat, 17 Aug 2024 01:03:46 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e916c81d01a62a10d99f4a9af11048a26cab3cdf387c3806665493cc2b53ad1`  
		Last Modified: Mon, 19 Aug 2024 19:16:17 GMT  
		Size: 26.8 MB (26755250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1570d0bb2d704ca3b824b7b00555738e7cf45613bc9726a424e97c355b15e8fa`  
		Last Modified: Mon, 19 Aug 2024 19:16:16 GMT  
		Size: 9.2 MB (9170443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8180a345e1f9ccdd5830215ae65cdd67611085b860ec4f5b9408a16277710429`  
		Last Modified: Mon, 19 Aug 2024 19:16:15 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435b57167160da3d19776a5f02dc219e163beb7cd049713d82206af92fd56784`  
		Last Modified: Mon, 19 Aug 2024 19:16:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:latest` - unknown; unknown

```console
$ docker pull maven@sha256:bd6f7d661d85864b2f68e493b561af339cc35747fe5476f02797c699a6df1f4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4656101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f557d065ac0341e0f95717032ece4e02ecdf239dcb77585efc5ded53ec510f12`

```dockerfile
```

-	Layers:
	-	`sha256:f364386e2b31f97adb36be5b9945090bc49c75201e4abda8ba0926e8571ffc03`  
		Last Modified: Mon, 19 Aug 2024 19:16:16 GMT  
		Size: 4.6 MB (4633967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9070084324b0d8b6507ad9f3874b273fbbdb1d7000474ae7361fce97ad02a4a5`  
		Last Modified: Mon, 19 Aug 2024 19:16:15 GMT  
		Size: 22.1 KB (22134 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:latest` - linux; s390x

```console
$ docker pull maven@sha256:d0c3aed8073d540e86a7f9757d0dcaaf405f0c1bd0a4b26e297347a2d3028d16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229535183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3063e19d9211071815845f7c6443e53c2cb325e1d429de3cb4f99248351f1003`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 01 Aug 2024 14:23:53 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:23:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:23:55 GMT
ADD file:1b967f5f96a2f9507c47196cb40249f8528c5dc5b92a0a49c22dd65046aaa6a7 in / 
# Thu, 01 Aug 2024 14:23:56 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Wed, 24 Jul 2024 22:19:06 GMT
CMD ["jshell"]
# Mon, 19 Aug 2024 08:57:28 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:c3604fa4febf99b39355be32e35ede051ab4df81ab153df330fa3128ef1e3dfd`  
		Last Modified: Tue, 06 Aug 2024 02:06:09 GMT  
		Size: 30.7 MB (30692324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1865b66d283cd0d67208fbdcd7cf8d1e3e7cc81fb2051cb503e196b949326e`  
		Last Modified: Sat, 17 Aug 2024 01:33:41 GMT  
		Size: 18.8 MB (18753945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce5e7c7683da72103e8e43607fa3ab1515fd5f8c3167b77ea79a85ff1fac768`  
		Last Modified: Sat, 17 Aug 2024 01:34:50 GMT  
		Size: 147.1 MB (147066981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4174539e54a62bcc97cc94bdef47eb2be864a86d660c7fcbe41c41a3a04ff81`  
		Last Modified: Sat, 17 Aug 2024 01:34:39 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2791f4f7fea6817cc84dce984d8aab9acbe4dfe9fdbdc775b13ff0fd5e9433e3`  
		Last Modified: Sat, 17 Aug 2024 01:34:39 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831ea9bdfffc2fd991a62d070989b268d7bc95adf7d4f9f0988beb34de57d016`  
		Last Modified: Mon, 19 Aug 2024 19:15:34 GMT  
		Size: 23.8 MB (23848414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd01c58553d7ce50570c59f80f8adf20011b4a5e0a0cf1437e8380d2327f2967`  
		Last Modified: Mon, 19 Aug 2024 19:15:34 GMT  
		Size: 9.2 MB (9170440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79fc947fccb345702f09b2d1a5dca55dfd2eb5507d0593fe66bc5763f044676`  
		Last Modified: Mon, 19 Aug 2024 19:15:33 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70e7880c3b71f34d90a25f65e81fe521b8f8729f82999a12329e9f4a1bc3e5d`  
		Last Modified: Mon, 19 Aug 2024 19:15:33 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:latest` - unknown; unknown

```console
$ docker pull maven@sha256:50f4eb88d6f03a9cbc9d210fefd81237e3f896b8c07eccaa06c5608a6aa083df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4552275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2766c36fbd6aac6b5dcb112f2e369f89d77dc55f53c6e47c790089811e8dbb5`

```dockerfile
```

-	Layers:
	-	`sha256:dc178dd7e691b25ea6a1a2885b57242ac62dc20203117958a618bd153457b780`  
		Last Modified: Mon, 19 Aug 2024 19:15:33 GMT  
		Size: 4.5 MB (4530233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86446d28518e110a9cbfc5bf9fe72ea446d655942971515d902085e6c34c7700`  
		Last Modified: Mon, 19 Aug 2024 19:15:33 GMT  
		Size: 22.0 KB (22042 bytes)  
		MIME: application/vnd.in-toto+json
