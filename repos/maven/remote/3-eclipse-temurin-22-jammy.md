## `maven:3-eclipse-temurin-22-jammy`

```console
$ docker pull maven@sha256:2e088e1b70559006905f933b3023b8d64c86e205cbefd4e7ec4b6d4506c3f833
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

### `maven:3-eclipse-temurin-22-jammy` - linux; amd64

```console
$ docker pull maven@sha256:add031850a1a13d9fcacfabf3ea7e3e2922a0c816e2b5cb2acbd380b04350278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232501008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2756a5c2a23c643c7660346ad49d0dca1fb6091fd6e979545b7b2cb202e76d49`
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
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 09:17:07 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-22.0.1+8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d8488fa1e4e8c1e318cef4c0fc3842a7f15a4cf52b27054663bb94471f54b3fa';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_aarch64_linux_hotspot_22.0.1_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='e59c6bf801cc023a1ea78eceb5e6756277f1564cd0a421ea984efe6cb96cfcf8';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_x64_linux_hotspot_22.0.1_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4113606ba65044a3cbd7678e1c0d41881d24a2441c8ab8b658b4ac58da624de5';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_ppc64le_linux_hotspot_22.0.1_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM="9f648abfa8ae82a1138bf069f498bc73d5ed0463b3f5d79e5d0988d28f9ffcc5";          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1.1%2B1/OpenJDK22U-jdk_s390x_linux_hotspot_22.0.1.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
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
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec46f3f6db860434ad19e35ce03fbc32ac970c970f807ba59885aeae242df05`  
		Last Modified: Tue, 02 Jul 2024 06:03:12 GMT  
		Size: 16.3 MB (16312426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd99df117edf9123ecb0467c6bf31b368c1614bc3251677326653d507ea5f2`  
		Last Modified: Tue, 02 Jul 2024 06:03:21 GMT  
		Size: 156.7 MB (156718135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a97d8e5b8802cd18a7d7b06f812320dc477a5b91103beb7ff3260a8025be229`  
		Last Modified: Tue, 02 Jul 2024 06:03:09 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea02da09984464a1fc4abb1bcd41040d077b17344e55e8f75bd9270e022a6d8d`  
		Last Modified: Tue, 02 Jul 2024 06:03:09 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36863d7235a89da6d4ea904c49f26a034afb32eb2170ee24c19991ccf24a4ad`  
		Last Modified: Tue, 02 Jul 2024 09:09:31 GMT  
		Size: 19.9 MB (19866849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed9d997dfd936ba9a7d18a07ef8610509c0939798c9f2ee64427f7b6666a3e1`  
		Last Modified: Tue, 02 Jul 2024 09:09:31 GMT  
		Size: 9.2 MB (9161815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a10d5d211969d42d93aec01df81eb5feacba30d7d22cdfa10cc553bd870a364`  
		Last Modified: Tue, 02 Jul 2024 09:09:30 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d89d858a4a1933e263aea13b2eafc5b7a3c7a16b6f983b8ddaf8dcea9dfd03c`  
		Last Modified: Tue, 02 Jul 2024 09:09:30 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-22-jammy` - unknown; unknown

```console
$ docker pull maven@sha256:f7ddebfc9791330768fddacfeb764eb289fef60ad268b02fe08dc4769e5b01f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5047859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abcf75a676d7368d36c3040a6bebf6870eaa5063c477d5107f10d15d0338f4e0`

```dockerfile
```

-	Layers:
	-	`sha256:a0c1dbffe0ee5bc6e047350f6c9d6f470738f6c840570cb620475f0d66e0cd03`  
		Last Modified: Tue, 02 Jul 2024 09:09:30 GMT  
		Size: 5.0 MB (5028249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e59ddd8879b420974f39465ea9f01f9d3d6445dd573527a6aa619d1240c1e76`  
		Last Modified: Tue, 02 Jul 2024 09:09:30 GMT  
		Size: 19.6 KB (19610 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-22-jammy` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:89c6a93312719442e59416459900c551377f5d33ce82dd2f9ad036b76e25bdd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229891152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a24850f7f92f2a3e96e48e8253c12bb62ab94b3b4369a8ee041fe3135d897b`
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
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 09:17:07 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-22.0.1+8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d8488fa1e4e8c1e318cef4c0fc3842a7f15a4cf52b27054663bb94471f54b3fa';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_aarch64_linux_hotspot_22.0.1_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='e59c6bf801cc023a1ea78eceb5e6756277f1564cd0a421ea984efe6cb96cfcf8';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_x64_linux_hotspot_22.0.1_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4113606ba65044a3cbd7678e1c0d41881d24a2441c8ab8b658b4ac58da624de5';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_ppc64le_linux_hotspot_22.0.1_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM="9f648abfa8ae82a1138bf069f498bc73d5ed0463b3f5d79e5d0988d28f9ffcc5";          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1.1%2B1/OpenJDK22U-jdk_s390x_linux_hotspot_22.0.1.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
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
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac50ae6767d4a91ada9d54209c76b3645963c6e1b649e0894bcfbc75cf1e0877`  
		Last Modified: Tue, 02 Jul 2024 04:36:41 GMT  
		Size: 17.7 MB (17721806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1934a9dfa0c67fd2797e54204df0600093bd8994a12644c6fbee8ce8fbf09f6`  
		Last Modified: Tue, 02 Jul 2024 04:36:50 GMT  
		Size: 154.7 MB (154738637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6cc3dd379d9c1d398278f013a00629e21f4dbd44fe3a4d3d876d28c6e16b244`  
		Last Modified: Tue, 02 Jul 2024 04:36:39 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830995778c8c0e67880a719c34e2889cbe66cd4ada1eb5f4376df14540fa9d08`  
		Last Modified: Tue, 02 Jul 2024 04:36:39 GMT  
		Size: 732.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9dcefb1094e604092776fb6cbc8639ca30e68d51faabb01c9aa38b4a9c3855`  
		Last Modified: Wed, 03 Jul 2024 10:26:25 GMT  
		Size: 19.9 MB (19865883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b66a92e55d97d28b3fda0f98d7280ff94a717291afc574f160379940332506a`  
		Last Modified: Wed, 03 Jul 2024 10:26:25 GMT  
		Size: 9.2 MB (9161778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442f1c03ca567059cb3f8daaf9ef25568c9f1319a94e5e14c4fa7d57355d8520`  
		Last Modified: Wed, 03 Jul 2024 10:26:24 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6130e5157508d28439b05b480d4d1777f603a21a8aa149d87d61c2b935599dd`  
		Last Modified: Wed, 03 Jul 2024 10:26:25 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-22-jammy` - unknown; unknown

```console
$ docker pull maven@sha256:85951b50b3a6ba41951262fb461222b4c6ab6d11c178ddb0bee69bb1cfef92ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5150753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b1e8423e8e8083cc173432df3b2b5b331fc68d9502e757101e067229ebc6ee`

```dockerfile
```

-	Layers:
	-	`sha256:6118e1bffda1b38a710fa002bd4a82fe31c1cfe3237e3aece5582038cb3662cc`  
		Last Modified: Wed, 03 Jul 2024 10:27:08 GMT  
		Size: 5.1 MB (5130492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:485bd2c03d43021793ae266b39a9e17f81eb29d6b7685c38eea260061953f79b`  
		Last Modified: Wed, 03 Jul 2024 10:27:08 GMT  
		Size: 20.3 KB (20261 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-22-jammy` - linux; ppc64le

```console
$ docker pull maven@sha256:90318a50169dbca510ab05c1cd15d4b4bdb2a4cf7ad7aba528248b2c59f1d920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.0 MB (242019828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea0cf22006b4c8b48d9e5de2a4e8adf4cad5b560e224e9b26ede0886c3236ae4`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 03 Jun 2024 10:34:18 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:34:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:34:22 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 03 Jun 2024 10:34:22 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-22.0.1+8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d8488fa1e4e8c1e318cef4c0fc3842a7f15a4cf52b27054663bb94471f54b3fa';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_aarch64_linux_hotspot_22.0.1_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='e59c6bf801cc023a1ea78eceb5e6756277f1564cd0a421ea984efe6cb96cfcf8';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_x64_linux_hotspot_22.0.1_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4113606ba65044a3cbd7678e1c0d41881d24a2441c8ab8b658b4ac58da624de5';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_ppc64le_linux_hotspot_22.0.1_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM="9f648abfa8ae82a1138bf069f498bc73d5ed0463b3f5d79e5d0988d28f9ffcc5";          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1.1%2B1/OpenJDK22U-jdk_s390x_linux_hotspot_22.0.1.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
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
	-	`sha256:391f04f7f495cb5fc20be69876c8638cb8f316a2cddac5d48d77ca39244e6dea`  
		Last Modified: Wed, 05 Jun 2024 03:48:14 GMT  
		Size: 35.6 MB (35588332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4bf6932beb9296640196fd39ef77a8cbc68154fd9c83c1ce930c76881fc4166`  
		Last Modified: Wed, 05 Jun 2024 04:04:30 GMT  
		Size: 17.3 MB (17330237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f1c25cb08549cf72c0af669d2222f3486cfec0c5c7c41783cafec439878df7`  
		Last Modified: Wed, 05 Jun 2024 04:04:40 GMT  
		Size: 156.7 MB (156694995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafd2c9aff158aa3dcce52c4b0f5cfc5d1dd818c18b8755de5951d09a92402d6`  
		Last Modified: Wed, 05 Jun 2024 04:04:26 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08d7575cd1e5c3d47e31d2405358abff1e92854b10ad9ea0eaff9b661a8414c`  
		Last Modified: Wed, 05 Jun 2024 04:04:26 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9fb1fe0621051ad3b410060f52edf2465cc2928dae93cd16d1c0347553f40c`  
		Last Modified: Thu, 27 Jun 2024 19:00:28 GMT  
		Size: 23.2 MB (23242560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92404ae37a56bc20ff619e126bfe10d2f4ab0255ebb135d5fdacf0087f62c560`  
		Last Modified: Thu, 27 Jun 2024 19:00:28 GMT  
		Size: 9.2 MB (9161782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ae4467e6dbbfef02c70d7bc45cae52518a48f1c681db138364169d9cdacb49`  
		Last Modified: Thu, 27 Jun 2024 19:00:27 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28fbb13c4e1f8880c0711ae331b49a5ff4d17339b1db141a33ba0b90f4fe95e8`  
		Last Modified: Thu, 27 Jun 2024 19:00:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-22-jammy` - unknown; unknown

```console
$ docker pull maven@sha256:8b856af4615dcaabb1c583bbf3d1e876dd979dc2d3a9da32751f44371ed92294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5080532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9c82ae4a8969239b00823fafbdf996ee3eefa77e9d5b69a057abaa20e9e0ed`

```dockerfile
```

-	Layers:
	-	`sha256:fd2fe62fa60bf9f668a8641ea49697f95d7851ac136e50b44de9eba898e7abb5`  
		Last Modified: Thu, 27 Jun 2024 19:00:54 GMT  
		Size: 5.1 MB (5060854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecc9f269a953028383f5e21b544c3c5cf10f992a36f3fd25c6a89c0475d0dbcf`  
		Last Modified: Thu, 27 Jun 2024 19:00:53 GMT  
		Size: 19.7 KB (19678 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-22-jammy` - linux; s390x

```console
$ docker pull maven@sha256:6940ffba2839c40661d585c8914e6415abc1d7ccf4dea1d6444c0a3d04f8dff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.8 MB (219783511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ebc944c597bdde6ac9b3f2584a2bcf3fe6d6febd9cb4f27a8bcb0d8fdd91b18`
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
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 09:17:07 GMT
ADD file:160bc105c5c70c3239daf08894bd8a2311ea04a965b30820eebf28573143f86b in / 
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-22.0.1+8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d8488fa1e4e8c1e318cef4c0fc3842a7f15a4cf52b27054663bb94471f54b3fa';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_aarch64_linux_hotspot_22.0.1_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='e59c6bf801cc023a1ea78eceb5e6756277f1564cd0a421ea984efe6cb96cfcf8';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_x64_linux_hotspot_22.0.1_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4113606ba65044a3cbd7678e1c0d41881d24a2441c8ab8b658b4ac58da624de5';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_ppc64le_linux_hotspot_22.0.1_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM="9f648abfa8ae82a1138bf069f498bc73d5ed0463b3f5d79e5d0988d28f9ffcc5";          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1.1%2B1/OpenJDK22U-jdk_s390x_linux_hotspot_22.0.1.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
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
	-	`sha256:4870604a2dd3e1b2f1a9f9dc1f8d02b548d030f0680887506b32aaee40747aa4`  
		Last Modified: Tue, 02 Jul 2024 03:47:54 GMT  
		Size: 28.6 MB (28637470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb585e50f43f29df0c0719456a8a2828ccc7b6cc9c1a57fbb50c79af66e4735`  
		Last Modified: Tue, 02 Jul 2024 03:56:27 GMT  
		Size: 16.1 MB (16124387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd37b9cdce40a3173ca9ebf6edb0583baf0c24825fd9d50760b16f2da653a089`  
		Last Modified: Tue, 02 Jul 2024 03:56:41 GMT  
		Size: 145.8 MB (145776704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de263ba84b8bf02ee83eeb6529017af699e427662354537458f0bcec40b178e`  
		Last Modified: Tue, 02 Jul 2024 03:56:24 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0fa7933ce5691c666277fc05704ad554d9d6a7a035c4fc61d7b9ae1bd1152d`  
		Last Modified: Tue, 02 Jul 2024 03:56:24 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ebf0e0fb95646b0bd703f5ac7827c2689101e7556770bc1936d23f86a84b2d`  
		Last Modified: Wed, 03 Jul 2024 10:38:13 GMT  
		Size: 20.1 MB (20081220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e7b6cbc08fc7ea7af125450bc38fd826bd862a271712decdaeb6bb73a90daa`  
		Last Modified: Wed, 03 Jul 2024 10:38:12 GMT  
		Size: 9.2 MB (9161813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d992990bba98db30edb5042fbeb8130ab429b74d79be1dd0b6c77c5bf407964`  
		Last Modified: Wed, 03 Jul 2024 10:38:12 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa01d0a3c0746d09b987754e6dfecfcff54f63d7ba988c7df82eb4cbd36357c`  
		Last Modified: Wed, 03 Jul 2024 10:38:12 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-22-jammy` - unknown; unknown

```console
$ docker pull maven@sha256:d79f0c857f44a21733f92e56b03a5cebc844a86b8c3138471ef91968f591b720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4975654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acbbe128839c22063469b7041a7b50851de2e8ba9f94217d2fcb5ed872757715`

```dockerfile
```

-	Layers:
	-	`sha256:cbf9d67a0bfe5b12050a00326e11c5cd0319162a2e932a412ccb1ee02afeab3f`  
		Last Modified: Wed, 03 Jul 2024 10:38:53 GMT  
		Size: 5.0 MB (4956022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1124c257b15fe5722c2fc68feb5a816cd5837722d57e76260ba5ea7630eed9cd`  
		Last Modified: Wed, 03 Jul 2024 10:38:53 GMT  
		Size: 19.6 KB (19632 bytes)  
		MIME: application/vnd.in-toto+json
