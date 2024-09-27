## `maven:3-eclipse-temurin-23`

```console
$ docker pull maven@sha256:a325c4ca0e3d99b7f19e163ed3f6511d2d655880c6da9ca2fcca0343f7cb847c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `maven:3-eclipse-temurin-23` - linux; amd64

```console
$ docker pull maven@sha256:059fb2ba6170fa13a56609dc8732f90ce6fe12b32c06f75a9b8466589d292280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.8 MB (249786159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9c534cb08ee6512a8d9f95fcaafed0c258d5fb8bf1bd040d0283d6998110bc`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:01 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:03 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Tue, 27 Aug 2024 15:55:03 GMT
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
	-	`sha256:32b824d45c6101d459f5d3c13ab8658b6f79713f3bd64e363d3f6bc98faf5d6d`  
		Last Modified: Tue, 27 Aug 2024 21:43:22 GMT  
		Size: 30.6 MB (30611547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d10ed217d47bf9ca7ed4ff10640027072814de6488661774d73baf109c03a0`  
		Last Modified: Tue, 17 Sep 2024 01:12:29 GMT  
		Size: 20.2 MB (20240501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f1b82e6dca90d5ded9bedc221500b61ec8601961fff512d0d14453eff726da4`  
		Last Modified: Wed, 18 Sep 2024 21:24:49 GMT  
		Size: 165.3 MB (165273656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd57c419bb00193e4098bc3828afd4fd0f10fc88fa7657b9a0d4e6205fd1546b`  
		Last Modified: Wed, 18 Sep 2024 21:24:37 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c38f91104db881766ac239926faf86b52974a7f57f655e80bf75e60d719937`  
		Last Modified: Wed, 18 Sep 2024 21:24:37 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deedde955f8b149bc21abaeedee203fb5d8227780934da3e68b2e1ce45f09a16`  
		Last Modified: Fri, 27 Sep 2024 19:55:47 GMT  
		Size: 24.5 MB (24486727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c05d22c783dc938cc42ea0a582dad1abf455edcc4a1bcd0bd0199766cdc1d2`  
		Last Modified: Fri, 27 Sep 2024 19:55:47 GMT  
		Size: 9.2 MB (9170439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592653002b441dd8623e2dc91b0d177a473d1135618b3d0571b2909a652cc72c`  
		Last Modified: Fri, 27 Sep 2024 19:55:47 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5f0338b3fad72a3a92ca4a0839526ceb5497ec9cd77e7231fc1247c9276431`  
		Last Modified: Fri, 27 Sep 2024 19:55:48 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-23` - unknown; unknown

```console
$ docker pull maven@sha256:594551636dcfd3644ca0d34da38010d2e9b0963796f1baa1158efdffc2afdeed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4755462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc75d7853a62455282e407c9dff2850da5d9a11aad49a09e466f80060a52baa`

```dockerfile
```

-	Layers:
	-	`sha256:5a92170d2afe5be09f4aa79351ea005aec6d1f0d0c0748504c97dcf70a9b66eb`  
		Last Modified: Fri, 27 Sep 2024 19:55:47 GMT  
		Size: 4.7 MB (4735896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8befe00bd926b812ece3fdfd78ade7505b50e0f341f854a17c41b293b0cad297`  
		Last Modified: Fri, 27 Sep 2024 19:55:46 GMT  
		Size: 19.6 KB (19566 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-23` - linux; s390x

```console
$ docker pull maven@sha256:bc77e7ad331f825ee690cef749653f9bb62cb2c66f75651178448a5966f672a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.9 MB (238865953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc5bac918e7ed5e96438af54d23fbf57d908d092e107e9e1c2bd161805c00da`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:05 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:08 GMT
ADD file:55ce2834630c73439274688061a6b2ad0d6952c2435dc51250026e14f139275d in / 
# Tue, 27 Aug 2024 15:55:08 GMT
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
	-	`sha256:1ebdf4a84a853f3e1fae6f15bd5f734d2925697002b9b26792d25b2080fac7e6`  
		Last Modified: Tue, 17 Sep 2024 01:29:05 GMT  
		Size: 30.7 MB (30665390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f1e9a70cd71418919e1bcea64252f1597c713fe3d37f248f75bc8203446cca`  
		Last Modified: Tue, 17 Sep 2024 01:42:07 GMT  
		Size: 18.8 MB (18794257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c330ca7faa3c67223a43b8ae04047fd4aa9e7da7b238dfd3485e5f2d019c5af`  
		Last Modified: Wed, 18 Sep 2024 21:47:46 GMT  
		Size: 154.4 MB (154375397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23016b67da9560d59258eb3b89bf430726c7cf23c306ff9ed3e7a84678ce02b8`  
		Last Modified: Wed, 18 Sep 2024 21:47:35 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf388efc1d595ed62342d22eac061d719af8a40f2a9e1fc5f7327d2ce0b77bb6`  
		Last Modified: Wed, 18 Sep 2024 21:47:35 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3276f2173eace2e11f4eb0b7d6ad4a261318eb4f0c40553bfe091d10ccd5b385`  
		Last Modified: Fri, 27 Sep 2024 19:58:04 GMT  
		Size: 25.9 MB (25857175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7802d32ec9d61953e9d1df584f1ff685ed6cf81bc471823bc58e29803a998ce7`  
		Last Modified: Fri, 27 Sep 2024 19:58:04 GMT  
		Size: 9.2 MB (9170442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa35a797382b47e7579b873033b9c00dd99b780203a2e158e28d1cc04abba476`  
		Last Modified: Fri, 27 Sep 2024 19:58:04 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e656ee9cf8955d0ab766226038a68396dea9c886b8971992e21f7717ac097e0`  
		Last Modified: Fri, 27 Sep 2024 19:58:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-23` - unknown; unknown

```console
$ docker pull maven@sha256:96f3e564f8f01c6615bb8cee2319494192c47cb3e430926e6e3636fe8de00f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4700809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26110b18b2a68a82e080df5fcf936bcc13e295161b053d49e7050fcdb9359bcb`

```dockerfile
```

-	Layers:
	-	`sha256:ef5d909274b4840b3531c67c035713a8928afa1f80d817b52375680270fc5050`  
		Last Modified: Fri, 27 Sep 2024 19:58:03 GMT  
		Size: 4.7 MB (4681219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66405cadb1884881218e43a929ab0964bd23b84f596ba137521ccfdd39ed7c9d`  
		Last Modified: Fri, 27 Sep 2024 19:58:03 GMT  
		Size: 19.6 KB (19590 bytes)  
		MIME: application/vnd.in-toto+json
