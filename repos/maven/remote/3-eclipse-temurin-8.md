## `maven:3-eclipse-temurin-8`

```console
$ docker pull maven@sha256:1d0fbe0484d2b6f71d4eff2e3a527a26283747379479276b321597d17dc75a12
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `maven:3-eclipse-temurin-8` - linux; amd64

```console
$ docker pull maven@sha256:60615f0d31517214054e99b05970821d29890d83e7c5f1089ecd1ef4dfd3affb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133295503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f4ec6862911ed3a007d346bcd36cd0998f0ae3c0059b26d5815d98524db318`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:18:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:18:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:18:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:18:24 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:18:24 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Thu, 15 Jan 2026 22:18:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 15 Jan 2026 22:18:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:18:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:18:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Jan 2026 02:42:21 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 02:42:21 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 16 Jan 2026 02:42:21 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 02:42:21 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 02:42:21 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 16 Jan 2026 02:42:21 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 16 Jan 2026 02:42:21 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 16 Jan 2026 02:42:21 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 16 Jan 2026 02:42:21 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 16 Jan 2026 02:42:21 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 16 Jan 2026 02:42:21 GMT
ARG MAVEN_VERSION=3.9.12
# Fri, 16 Jan 2026 02:42:21 GMT
ARG USER_HOME_DIR=/root
# Fri, 16 Jan 2026 02:42:21 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 16 Jan 2026 02:42:21 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 16 Jan 2026 02:42:21 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a72c85106ae9a2885d2aab3a7c757b40d4b5915c54193b935f37111828dcf3`  
		Last Modified: Thu, 15 Jan 2026 22:18:50 GMT  
		Size: 17.0 MB (16975926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8532bae8ee50cd24b239a6fa063eb19526cff6782f6f74ae026a2178cda0a6e6`  
		Last Modified: Thu, 15 Jan 2026 22:18:49 GMT  
		Size: 54.7 MB (54742663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94376c6c055750f8b9c88f96b456f10b0ae030a3b44755a6e278c38518a9034d`  
		Last Modified: Thu, 15 Jan 2026 22:18:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc7e5b7949d54912db3f6da36540adee01df91f2667cdda51997344cba74339`  
		Last Modified: Thu, 15 Jan 2026 22:18:45 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d017f427a11767d419539a5677d466d9bf16bcfa0406de23deb886fb8221574`  
		Last Modified: Fri, 16 Jan 2026 02:42:41 GMT  
		Size: 22.5 MB (22535195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbd25018ee9f8689ffe073f0aace8a7e4ebd952293cccd94429a5ce4a5ba969`  
		Last Modified: Fri, 16 Jan 2026 02:42:39 GMT  
		Size: 9.3 MB (9312235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dda40d310c645b0f399fdbdb565e511dfc4bf24dddeee0f0c4373223628e02`  
		Last Modified: Fri, 16 Jan 2026 02:42:38 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3037dc559031c2f2d16ff97ed02038637eb64cc1f27dd7a915629c6835a83d5`  
		Last Modified: Fri, 16 Jan 2026 02:42:38 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-8` - unknown; unknown

```console
$ docker pull maven@sha256:2423222a854c0d5ed7876b3b09583f8892422ccba768757e13ab61cf0ff78678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5034672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d912aef9391eae3f97a573edc1e6435473e8754f2cf16c868ea77d0b20f6d88b`

```dockerfile
```

-	Layers:
	-	`sha256:70f95d19971d40f1cfa9f52f026e8d9df603e66c7734a6737d91ef9a3cf62858`  
		Last Modified: Fri, 16 Jan 2026 03:31:34 GMT  
		Size: 5.0 MB (5014007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc42b4615974eacc3bce546cfc2dc59ee910439673a930d8dd8460d66deba9b7`  
		Last Modified: Fri, 16 Jan 2026 03:31:35 GMT  
		Size: 20.7 KB (20665 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-8` - linux; arm variant v7

```console
$ docker pull maven@sha256:aceed04acef57db7f6a054afee28d8cdd8b515c787cfb426c1d9bb8f674fecac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.9 MB (129891240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:437c35a05182bd0931acdd3773c14d66f10092ec3e1969cf331dc98fe4d7ed20`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:59 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:59 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:02 GMT
ADD file:9e6534a5b837dcbcc4b9596878a4feeb07210fb34c7385aeee0217ff03c2460e in / 
# Tue, 13 Jan 2026 05:40:03 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:09:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:09:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:09:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:09:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:09:28 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Thu, 15 Jan 2026 22:09:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 15 Jan 2026 22:09:37 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:09:37 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:09:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 23:35:09 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:35:09 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 15 Jan 2026 23:35:09 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 15 Jan 2026 23:35:09 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 15 Jan 2026 23:35:09 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 15 Jan 2026 23:35:09 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 15 Jan 2026 23:35:09 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 15 Jan 2026 23:35:09 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 15 Jan 2026 23:35:09 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 15 Jan 2026 23:35:09 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 15 Jan 2026 23:35:09 GMT
ARG MAVEN_VERSION=3.9.12
# Thu, 15 Jan 2026 23:35:09 GMT
ARG USER_HOME_DIR=/root
# Thu, 15 Jan 2026 23:35:09 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 15 Jan 2026 23:35:09 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 15 Jan 2026 23:35:09 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a56277e49d30e9a430d5cefad3038f88470a8681e48b806fff292791ed54f1fc`  
		Last Modified: Tue, 13 Jan 2026 10:01:35 GMT  
		Size: 26.9 MB (26853837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9794ead862662ff877148f78c6a954afced26c3e80c70a689e42810257024568`  
		Last Modified: Thu, 15 Jan 2026 22:10:01 GMT  
		Size: 16.3 MB (16306643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f506d761ce6244c87ee0dfce86be439b17d5c712ef27b8a0a3ac3b4b5104180b`  
		Last Modified: Thu, 15 Jan 2026 22:10:05 GMT  
		Size: 50.1 MB (50144725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437dc824101437c30cc541a61762b87fdec86e527873aef7b68985de95fc7d84`  
		Last Modified: Thu, 15 Jan 2026 22:09:59 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13345ac4a0f33ab5d5bdf99805b68a8b4aafa373cab3e4997b4c691724de7f75`  
		Last Modified: Thu, 15 Jan 2026 22:09:59 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f0265c23e0e77d86fc03d49a0a2ac4c63dc46b24f1cc3be81e244a3a941aae`  
		Last Modified: Thu, 15 Jan 2026 23:35:29 GMT  
		Size: 27.3 MB (27270325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085fe75fb16cec5e6bf7fb972e0265ebecac61cb96754420e828b15c69bd77ab`  
		Last Modified: Thu, 15 Jan 2026 23:35:27 GMT  
		Size: 9.3 MB (9312237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9594d4142cfb44404bcc5e44e094a03651fcbfb327fa847a9662cba4c5baf4d5`  
		Last Modified: Thu, 15 Jan 2026 23:35:27 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2279a87ee4604c93e1cc30d2710224cc9645e54511885d5e8412fe2c5ec6be16`  
		Last Modified: Thu, 15 Jan 2026 23:35:26 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-8` - unknown; unknown

```console
$ docker pull maven@sha256:772146f95bba183f069b657f404bac0a9924a3ba864add0c25e601519a219495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5037549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:268dbf522cef2dfed60be0210c7ff9335d9941472fd1dc5c3f20df1814131716`

```dockerfile
```

-	Layers:
	-	`sha256:a2eb069bc7fd7d9318a4fefdd6e2f01aa63ee1e5133a7239fb6be33d147a0a8f`  
		Last Modified: Fri, 16 Jan 2026 00:30:39 GMT  
		Size: 5.0 MB (5016753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5fda9a8371d82c1febde1787a9ed8ffe484f89c798915376a4b75831776ec5e`  
		Last Modified: Fri, 16 Jan 2026 00:30:40 GMT  
		Size: 20.8 KB (20796 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:d080a0f669c4a2d27576519cdb0968d19ad5d5188320b4a98d71d07c8beb61ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131589471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7357875904b84484fd97c42f06a1f28e81189e54ced9e539e1dd9eac40b542`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:19:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:19:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:19:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:19:45 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:19:45 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Thu, 13 Nov 2025 23:19:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 13 Nov 2025 23:19:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:19:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:19:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 17 Dec 2025 20:08:09 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 20:08:09 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 17 Dec 2025 20:08:09 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:08:09 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:08:09 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 17 Dec 2025 20:08:09 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 17 Dec 2025 20:08:09 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 17 Dec 2025 20:08:09 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 17 Dec 2025 20:08:09 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 17 Dec 2025 20:08:09 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 17 Dec 2025 20:08:09 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 17 Dec 2025 20:08:09 GMT
ARG USER_HOME_DIR=/root
# Wed, 17 Dec 2025 20:08:09 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 17 Dec 2025 20:08:09 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 17 Dec 2025 20:08:09 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09820b8e59aef8e82bd8c719b6aeb1f6355bb3e879c512f6a3a90e1c5341895`  
		Last Modified: Tue, 13 Jan 2026 01:00:28 GMT  
		Size: 17.0 MB (16989094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8bb96a4c61ded17e086db424a1acc02dec156d5a17ccfa08cec010cae101343`  
		Last Modified: Tue, 13 Jan 2026 01:00:31 GMT  
		Size: 53.8 MB (53819233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0260625ec9c439cb3c3745021eb1ae1259198471f12aed961bb5ab6b0fa6dd7b`  
		Last Modified: Tue, 13 Jan 2026 01:00:26 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1621d881ada784b6bb5ed5254ade826b77e98df260f81febda258566e422f079`  
		Last Modified: Tue, 13 Jan 2026 01:00:26 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3b6b0f0e1d46cc203ed41860c1c66cdc96fea32297e17669b77ac40e5edab7`  
		Last Modified: Wed, 17 Dec 2025 20:08:30 GMT  
		Size: 22.6 MB (22603475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb11da1f8c5ba24b55f72414657f4e8e9c8ec4fca9e11baf7132fd8f16d6885b`  
		Last Modified: Wed, 17 Dec 2025 20:08:29 GMT  
		Size: 9.3 MB (9312238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1ebe772058c83715cd73ddd4cef248a51cc4d5a262a5bdfab4e3a830e29140`  
		Last Modified: Wed, 17 Dec 2025 20:08:28 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554d4601a2f7ba985b2805a9453b40b982e815b883371585a409f84400901816`  
		Last Modified: Wed, 17 Dec 2025 20:08:28 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-8` - unknown; unknown

```console
$ docker pull maven@sha256:beb0f259864c00bcd7bc24b8f2183b34f71492e415bc8c0c0853fd3c9029ba5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5042074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ebea61bf2405901dd9288388772e0133cba27f70689f726f8e9282c57d5d1f3`

```dockerfile
```

-	Layers:
	-	`sha256:fb8ca7df4a88331face666ef90dd0561da49909efe9b3d1cb2b3e8fb406299a8`  
		Last Modified: Wed, 17 Dec 2025 21:33:09 GMT  
		Size: 5.0 MB (5021240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db9c9dde2e653d497863012b3b9113d772de425256c10e5991bca219ed39cee9`  
		Last Modified: Wed, 17 Dec 2025 21:33:10 GMT  
		Size: 20.8 KB (20834 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-8` - linux; ppc64le

```console
$ docker pull maven@sha256:8a7fea069e9d469a4d96d05f9f099ff249adafe967502a9148490c8c5e53c4e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141199301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d9f86cddc734ee174482266fe290aeaa6b6c7f2d7861d6a3083a4b927ab873e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:12:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:12:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:12:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:12:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:12:31 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Thu, 13 Nov 2025 23:12:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        arm64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        armhf)          ESUM='184d3f914f1e41476449043382cb81bd8086214acef7353ed1b456b49b8ac9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u472b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 13 Nov 2025 23:12:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:12:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:12:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 17 Dec 2025 20:17:27 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 20:17:28 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 17 Dec 2025 20:17:28 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:17:28 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:17:28 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 17 Dec 2025 20:17:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 17 Dec 2025 20:17:28 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 17 Dec 2025 20:17:30 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 17 Dec 2025 20:17:31 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 17 Dec 2025 20:17:32 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 17 Dec 2025 20:17:32 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 17 Dec 2025 20:17:32 GMT
ARG USER_HOME_DIR=/root
# Wed, 17 Dec 2025 20:17:32 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 17 Dec 2025 20:17:32 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 17 Dec 2025 20:17:32 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Tue, 16 Dec 2025 00:07:47 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0cf872bdb9578adf029cccb893ea39b7d62a1717f6f08db17d402977875a8b`  
		Last Modified: Tue, 13 Jan 2026 02:35:41 GMT  
		Size: 18.8 MB (18814748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224a2003935b5dcdb1f56ae6ff2cae1b3690473d82d6ac0e132782ae0aec50b0`  
		Last Modified: Tue, 13 Jan 2026 05:30:59 GMT  
		Size: 52.2 MB (52180233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e9549873261a8ef868fa9e7606eb1029e30a926b5f39928c4f2e665ee8f44a`  
		Last Modified: Tue, 13 Jan 2026 05:30:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5598e1714061db699fc5bfe5500bc460e3ed9c7098e1fa71daf04ce0ae5fe3`  
		Last Modified: Tue, 13 Jan 2026 05:30:54 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274f3cd41bac3c4d7759d1e8142ee46374caee2bebf82b204ad58f0529b8a989`  
		Last Modified: Wed, 17 Dec 2025 20:18:14 GMT  
		Size: 26.6 MB (26584174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc848f422c11cc3f7c625e964f340fbd25284ac731402221562e35b306bf48e7`  
		Last Modified: Wed, 17 Dec 2025 20:18:11 GMT  
		Size: 9.3 MB (9312252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b06c5aded634be2478922cc255bf1fb6aad4356b1fd429f2f271fd74eb30c3`  
		Last Modified: Wed, 17 Dec 2025 20:18:10 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab8091dc29b64c3eea9828cfdd3c05fa088f1177d763602c09a0e9e80c733b2`  
		Last Modified: Wed, 17 Dec 2025 20:18:10 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-8` - unknown; unknown

```console
$ docker pull maven@sha256:8030beb6d9c22f2af236ab09951c0961948e2fd07443e32e7f4cf844a63e0877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5040271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8262f3b5e4a90334d786e63aa56e028175490522eb54c3c71b133864630522a`

```dockerfile
```

-	Layers:
	-	`sha256:5beec37c83e3ecfaf38c8e14febbe60182de6493dd5af26f1c167d2a279e76f4`  
		Last Modified: Wed, 17 Dec 2025 21:33:15 GMT  
		Size: 5.0 MB (5019538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1766b01ac5afee1cc5659eecc6a723a145bd758ed0e3c42d4344ffff58fe26a2`  
		Last Modified: Wed, 17 Dec 2025 21:33:16 GMT  
		Size: 20.7 KB (20733 bytes)  
		MIME: application/vnd.in-toto+json
