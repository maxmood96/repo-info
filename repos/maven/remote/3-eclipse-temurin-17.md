## `maven:3-eclipse-temurin-17`

```console
$ docker pull maven@sha256:b9fc7a802745f5f4dec3007d7668c8c9da845ac41d37737ec6442a35b853c258
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `maven:3-eclipse-temurin-17` - linux; amd64

```console
$ docker pull maven@sha256:d3a2f2e4f66a94f9316e38fc08dc14e56be3594015c73e53fc2f255dfd8f78d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.4 MB (231385210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0d18266725b1161af875fa62a985b72b14afd460c716127018a6c9fe59b075`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 26 Oct 2024 17:22:34 GMT
ARG RELEASE
# Sat, 26 Oct 2024 17:22:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 26 Oct 2024 17:22:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 26 Oct 2024 17:22:34 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 26 Oct 2024 17:22:34 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Sat, 26 Oct 2024 17:22:34 GMT
CMD ["/bin/bash"]
# Sat, 26 Oct 2024 17:22:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 26 Oct 2024 17:22:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 26 Oct 2024 17:22:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 26 Oct 2024 17:22:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Sat, 26 Oct 2024 17:22:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='d7ba818b1417b67f1f3cdcf7c5fac5e179998469dce7448349f24175eb9b2871';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 26 Oct 2024 17:22:34 GMT
CMD ["jshell"]
# Sat, 26 Oct 2024 17:22:34 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 26 Oct 2024 17:22:34 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 26 Oct 2024 17:22:34 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 26 Oct 2024 17:22:34 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 26 Oct 2024 17:22:34 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 26 Oct 2024 17:22:34 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
ARG MAVEN_VERSION=3.9.9
# Sat, 26 Oct 2024 17:22:34 GMT
ARG USER_HOME_DIR=/root
# Sat, 26 Oct 2024 17:22:34 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 26 Oct 2024 17:22:34 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 26 Oct 2024 17:22:34 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ff804eb32a079e6f9a54eb31c0f43d9d6c56fc09c7735ec59e2ad948fc6af6`  
		Last Modified: Tue, 04 Feb 2025 04:40:05 GMT  
		Size: 22.9 MB (22942779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5768705e3b7e7e3c61f95a6ed0478a61076d084e1adedfe24e09ce95d5c433`  
		Last Modified: Tue, 04 Feb 2025 04:40:07 GMT  
		Size: 144.6 MB (144576191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4fff2c206cae13745f200704b38134105ac3a4bcf862dc0d04d08f6aa9d2ce`  
		Last Modified: Tue, 04 Feb 2025 04:40:04 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2700d3f64bcbf1b67ccf65a715330aa34cb16c0c1e8c9146c15011233d6fc4`  
		Last Modified: Tue, 04 Feb 2025 04:40:04 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e90a69f846403fabce7149b4bad565ecef1f1417c8e0b7ff9db353b0989030`  
		Last Modified: Tue, 04 Feb 2025 05:28:36 GMT  
		Size: 24.9 MB (24937930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2428cc0bc9962489b4f844c031147cd2a26138a661a1c87f35c8e5aaba7451`  
		Last Modified: Tue, 04 Feb 2025 05:28:35 GMT  
		Size: 9.2 MB (9170220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd7ffb9ce7e3971835aec1219589100b1350fe7de3e5746d4351774779e3878`  
		Last Modified: Tue, 04 Feb 2025 05:28:35 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bfdaeea3607e3711f21496bbce3a91d5f4bf545e67f4761d276c7e562091c4`  
		Last Modified: Tue, 04 Feb 2025 05:28:35 GMT  
		Size: 357.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec08daa9cf227a7f42c64629c5055fee090b4048ead7cfa51821caffcf0c7768`  
		Last Modified: Tue, 04 Feb 2025 05:28:36 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17` - unknown; unknown

```console
$ docker pull maven@sha256:74f0139112a2fa7130f608d6928285865e1ed4e2d9fa32a53c95ad486b32e0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4879311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c1b8be913bbde87fe371bdab34946a5cf8d07535701204cf6ba8935cbec2f57`

```dockerfile
```

-	Layers:
	-	`sha256:c7d4c46f02d6041f4de339cd7c0a10c4a588896bf931e793734493c2f8dd1220`  
		Last Modified: Tue, 04 Feb 2025 05:28:35 GMT  
		Size: 4.9 MB (4854794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd34402ebc78bb6ff09b2748b7cb9361a302eee5f82988e210e747837b8909b9`  
		Last Modified: Tue, 04 Feb 2025 05:28:35 GMT  
		Size: 24.5 KB (24517 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17` - linux; arm variant v7

```console
$ docker pull maven@sha256:daf84d9b0870c9293b4b47b5415a749264dcf40a93771d0f822e568e173df214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228885205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0fefc768afe17190e54cc4c145b45a553a3e4e459cbe9b593ea58f883d9ccc`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 26 Oct 2024 17:22:34 GMT
ARG RELEASE
# Sat, 26 Oct 2024 17:22:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 26 Oct 2024 17:22:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 26 Oct 2024 17:22:34 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 26 Oct 2024 17:22:34 GMT
ADD file:22301ffa2fa465db7a0f07e0c3ddc488f07cc6a745c39e6f450fdbe37da97418 in / 
# Sat, 26 Oct 2024 17:22:34 GMT
CMD ["/bin/bash"]
# Sat, 26 Oct 2024 17:22:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 26 Oct 2024 17:22:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 26 Oct 2024 17:22:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 26 Oct 2024 17:22:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Sat, 26 Oct 2024 17:22:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='d7ba818b1417b67f1f3cdcf7c5fac5e179998469dce7448349f24175eb9b2871';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 26 Oct 2024 17:22:34 GMT
CMD ["jshell"]
# Sat, 26 Oct 2024 17:22:34 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 26 Oct 2024 17:22:34 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 26 Oct 2024 17:22:34 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 26 Oct 2024 17:22:34 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 26 Oct 2024 17:22:34 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 26 Oct 2024 17:22:34 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
ARG MAVEN_VERSION=3.9.9
# Sat, 26 Oct 2024 17:22:34 GMT
ARG USER_HOME_DIR=/root
# Sat, 26 Oct 2024 17:22:34 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 26 Oct 2024 17:22:34 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 26 Oct 2024 17:22:34 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:3492abb11babfb77cfc5a8904e67b22f4e4fd68c8d8a7fe1119861ed6503b36f`  
		Last Modified: Mon, 27 Jan 2025 05:10:02 GMT  
		Size: 26.9 MB (26874983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a5feca48d6d52ff9ef30651ab2fd330f7df213f49a2e8c1d802233ca080dc8`  
		Last Modified: Tue, 04 Feb 2025 11:00:12 GMT  
		Size: 21.4 MB (21372885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833c6bc8f928a67ecef0b46f949f694a60a7e196f6f0704a06a727e12abadfbc`  
		Last Modified: Tue, 04 Feb 2025 11:00:15 GMT  
		Size: 142.1 MB (142054855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396068d15b13caa66c2782b7168c539c408e5b5b1538cb708f9da8a8f00648de`  
		Last Modified: Tue, 04 Feb 2025 11:00:12 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aaa9004b1c56b65f3255b579cd72d29c9582472fb986711f92dff3ae1f0c3c6`  
		Last Modified: Tue, 04 Feb 2025 11:00:11 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf390de01c365f0add0174011e8259a55f19d1f615b33a74bc4855685948303`  
		Last Modified: Tue, 04 Feb 2025 22:17:56 GMT  
		Size: 29.4 MB (29408468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b420690dc9701700a517c5e026e8a96e8acba7ccb4f139557f731836e3b15a90`  
		Last Modified: Tue, 04 Feb 2025 22:17:56 GMT  
		Size: 9.2 MB (9170213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acec65203ff2933e0f03332488dbe72757b706ef06a956f4fe9d6042936e72e`  
		Last Modified: Tue, 04 Feb 2025 22:17:55 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f776bca99836f3d4752c5d62608504c56be2417c024db862dd500e8e18305b23`  
		Last Modified: Tue, 04 Feb 2025 22:17:56 GMT  
		Size: 358.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27497fdae6f8a073e7ccc8cabbe92966ca625b7a5126cb1de9b540bc78261033`  
		Last Modified: Tue, 04 Feb 2025 22:17:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17` - unknown; unknown

```console
$ docker pull maven@sha256:636d97072f7430b0ba543bd8e716191d614fbdccb1d0e21463bd8e3b39cb3cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4818070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2331bcfcf595a8fe30212fb4e1364e2cd1109d97bc979fee3fd9e1609eac8c5f`

```dockerfile
```

-	Layers:
	-	`sha256:7f6076f5e30ce73c462984f0f49dbd4162e546d81af0aa91029d69851743b53c`  
		Last Modified: Tue, 04 Feb 2025 22:17:55 GMT  
		Size: 4.8 MB (4793421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:770502c535dc6a729b2c2c5278b353f7026da378157ed2eaa8897dfbc5defb66`  
		Last Modified: Tue, 04 Feb 2025 22:17:55 GMT  
		Size: 24.6 KB (24649 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:fa820dc755f828b28e6845ac5d269615d877a3f090ddc545266091c957188bc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230670941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74dbe0f3cf994fb505669bf6bb6860081367b32cb9698efb6ff208cb796bfb1e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 26 Oct 2024 17:22:34 GMT
ARG RELEASE
# Sat, 26 Oct 2024 17:22:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 26 Oct 2024 17:22:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 26 Oct 2024 17:22:34 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 26 Oct 2024 17:22:34 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Sat, 26 Oct 2024 17:22:34 GMT
CMD ["/bin/bash"]
# Sat, 26 Oct 2024 17:22:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 26 Oct 2024 17:22:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 26 Oct 2024 17:22:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 26 Oct 2024 17:22:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Sat, 26 Oct 2024 17:22:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='d7ba818b1417b67f1f3cdcf7c5fac5e179998469dce7448349f24175eb9b2871';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 26 Oct 2024 17:22:34 GMT
CMD ["jshell"]
# Sat, 26 Oct 2024 17:22:34 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 26 Oct 2024 17:22:34 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 26 Oct 2024 17:22:34 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 26 Oct 2024 17:22:34 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 26 Oct 2024 17:22:34 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 26 Oct 2024 17:22:34 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
ARG MAVEN_VERSION=3.9.9
# Sat, 26 Oct 2024 17:22:34 GMT
ARG USER_HOME_DIR=/root
# Sat, 26 Oct 2024 17:22:34 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 26 Oct 2024 17:22:34 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 26 Oct 2024 17:22:34 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc2f1e9953cd78876e5c047eaef6baf6407597113cd49d27cbee3d3eb57d11e`  
		Last Modified: Tue, 04 Feb 2025 09:22:21 GMT  
		Size: 24.2 MB (24153905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f5f70da64d3cfa33a66961fee477351b067301f124a76aec3532966a7fb1f8`  
		Last Modified: Tue, 04 Feb 2025 09:22:24 GMT  
		Size: 143.5 MB (143461842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b835032ff5a4a87eeb8c35796ca4985bc225bee2a303c6363d38dfbb8cc3004`  
		Last Modified: Tue, 04 Feb 2025 09:22:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08000320ad8b126a6e08ce05141beb6870c3289fbf0d83b0427c71da2e26200`  
		Last Modified: Tue, 04 Feb 2025 09:22:20 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d74a3d679c6229c4c095bc9860ab241abfceacc88519fcf750380d0c599a7c`  
		Last Modified: Wed, 05 Feb 2025 00:31:45 GMT  
		Size: 25.0 MB (24987569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f702f0fc708b6e87c5d998a07584d09bbdcd5ff9d509662f689e0c0f42088e`  
		Last Modified: Wed, 05 Feb 2025 00:31:45 GMT  
		Size: 9.2 MB (9170221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d71a27b749638888cfba053b67e90ac66acaee7b4ec58e29e12d2f09bf17286`  
		Last Modified: Wed, 05 Feb 2025 00:31:44 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708e4c9edb525a4386cb8e53fee660a9e91b6961524128d03e2c8956bee070b7`  
		Last Modified: Wed, 05 Feb 2025 00:31:44 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002f68e2a92d9da1a634c989735c9ea98c8002c17b46c9519221dacf3f7ca48d`  
		Last Modified: Wed, 05 Feb 2025 00:31:45 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17` - unknown; unknown

```console
$ docker pull maven@sha256:1a3be2ccb892e7943a0bf6b86e3ba25f60a56c44d85f76653bb1aedf2222cac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5017037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a30d9a499038bbd7eb82525ed2436a645dcd642d9af8605ebc8e9cc8ffc28989`

```dockerfile
```

-	Layers:
	-	`sha256:610a6c6c547ca58ebe7f18040afe55ce10a9e5890b2c59a606f2b319f4a991a4`  
		Last Modified: Wed, 05 Feb 2025 00:31:45 GMT  
		Size: 5.0 MB (4992354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2c08cb62a36e0bfa82fc5fce96dea09e0b61b6ad94566440172a385c78d1aab`  
		Last Modified: Wed, 05 Feb 2025 00:31:44 GMT  
		Size: 24.7 KB (24683 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17` - linux; ppc64le

```console
$ docker pull maven@sha256:c1488b63dd704f0ad00a194fc457cf7385646dbf484d212a6d9d9b668a2a9b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (241030529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e853e1c90eece9c2b47b798e7f7dd46ec72c6e9b41184a50fa603d86510bc604`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 26 Oct 2024 17:22:34 GMT
ARG RELEASE
# Sat, 26 Oct 2024 17:22:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 26 Oct 2024 17:22:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 26 Oct 2024 17:22:34 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 26 Oct 2024 17:22:34 GMT
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
# Sat, 26 Oct 2024 17:22:34 GMT
CMD ["/bin/bash"]
# Sat, 26 Oct 2024 17:22:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 26 Oct 2024 17:22:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 26 Oct 2024 17:22:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 26 Oct 2024 17:22:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Sat, 26 Oct 2024 17:22:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='d7ba818b1417b67f1f3cdcf7c5fac5e179998469dce7448349f24175eb9b2871';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 26 Oct 2024 17:22:34 GMT
CMD ["jshell"]
# Sat, 26 Oct 2024 17:22:34 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 26 Oct 2024 17:22:34 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 26 Oct 2024 17:22:34 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 26 Oct 2024 17:22:34 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 26 Oct 2024 17:22:34 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 26 Oct 2024 17:22:34 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
ARG MAVEN_VERSION=3.9.9
# Sat, 26 Oct 2024 17:22:34 GMT
ARG USER_HOME_DIR=/root
# Sat, 26 Oct 2024 17:22:34 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 26 Oct 2024 17:22:34 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 26 Oct 2024 17:22:34 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dd9d1b7ea01dff2ab580e6320a587b1adc67cea22a1f4d2e67127ca693646d`  
		Last Modified: Tue, 04 Feb 2025 07:43:05 GMT  
		Size: 24.1 MB (24107411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b935de70b38f6190f9e9edf6b409ffe906868fe431405592a2f5ffc916c991`  
		Last Modified: Tue, 04 Feb 2025 07:43:08 GMT  
		Size: 144.2 MB (144219941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f048f8a18afbd7593ac0f1982333c47d71cfe39c1909972382be413e96fafe`  
		Last Modified: Tue, 04 Feb 2025 07:43:04 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e059096bbd194b86c37274409ecff5a58c8ab3f2f843f0fc6e6486f199b7b5`  
		Last Modified: Tue, 04 Feb 2025 07:43:04 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eff6daf10b56d305272c3209bcc8bcc630a4bf230429e18558c5b409ea1676d`  
		Last Modified: Tue, 04 Feb 2025 20:42:37 GMT  
		Size: 29.1 MB (29139343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a8a2f22e4c2ced3cc0109affa8361c6a0461656cc55670b72b9eb94d94771e`  
		Last Modified: Tue, 04 Feb 2025 20:42:36 GMT  
		Size: 9.2 MB (9170203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2d6e9ebf4746526f1f1846cbf1a9b3f7294793560bd18adb2109e007a492cb`  
		Last Modified: Tue, 04 Feb 2025 20:42:35 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced950340f8b94c1e54ccb2501dea7c5df261e84242b648aad828fca3a6e024a`  
		Last Modified: Tue, 04 Feb 2025 20:42:35 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf3419ce5f513df924cf3dae6e17f601f575123bf698de01df592b9731ea808`  
		Last Modified: Tue, 04 Feb 2025 20:42:36 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17` - unknown; unknown

```console
$ docker pull maven@sha256:3de2f163d7caa0f2b4b08b14eff195a0daa7559378b4eca78a2a804725b733fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4930146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e87caa5cd0cb28613cf56f69b62d89081cffdfeac091d017ed4c710504ae8b`

```dockerfile
```

-	Layers:
	-	`sha256:a1abbf06f0ad47104104826fa9aa7e2c0a4ca1da3d5415569fd5daeae437e4ba`  
		Last Modified: Tue, 04 Feb 2025 20:42:36 GMT  
		Size: 4.9 MB (4905581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b998d424e2d05c8cb17f5fd73a643d822ac0afa055097712208a86ed0a1a56d`  
		Last Modified: Tue, 04 Feb 2025 20:42:35 GMT  
		Size: 24.6 KB (24565 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17` - linux; riscv64

```console
$ docker pull maven@sha256:c5146c6476e17b0df975c9038c6ac424982607cc1857b52f41d66fc427744f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232092187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f6d8f94a60487cc649178947eecffa4944d2740b77ffd6b37cdb2cfe96819b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 26 Oct 2024 17:22:34 GMT
ARG RELEASE
# Sat, 26 Oct 2024 17:22:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 26 Oct 2024 17:22:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 26 Oct 2024 17:22:34 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 26 Oct 2024 17:22:34 GMT
ADD file:69c46ae9666e78c27ca5b5f25cec1a5536ff16f17cb00104e5c77e722bd8d643 in / 
# Sat, 26 Oct 2024 17:22:34 GMT
CMD ["/bin/bash"]
# Sat, 26 Oct 2024 17:22:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 26 Oct 2024 17:22:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 26 Oct 2024 17:22:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 26 Oct 2024 17:22:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Sat, 26 Oct 2024 17:22:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='d7ba818b1417b67f1f3cdcf7c5fac5e179998469dce7448349f24175eb9b2871';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 26 Oct 2024 17:22:34 GMT
CMD ["jshell"]
# Sat, 26 Oct 2024 17:22:34 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 26 Oct 2024 17:22:34 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 26 Oct 2024 17:22:34 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 26 Oct 2024 17:22:34 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 26 Oct 2024 17:22:34 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 26 Oct 2024 17:22:34 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
ARG MAVEN_VERSION=3.9.9
# Sat, 26 Oct 2024 17:22:34 GMT
ARG USER_HOME_DIR=/root
# Sat, 26 Oct 2024 17:22:34 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 26 Oct 2024 17:22:34 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 26 Oct 2024 17:22:34 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6e1053d729cc1718daa9369927cf6ddfbf892a846041de0e610d1c77ade136c5`  
		Last Modified: Mon, 27 Jan 2025 05:10:15 GMT  
		Size: 31.0 MB (30983910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a116124a0e7b20219e18554d3546d2013703e5da91b9df632ebcd5e027f6af4`  
		Last Modified: Tue, 04 Feb 2025 04:55:11 GMT  
		Size: 20.1 MB (20135431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409a5a118bdeaf726687041177a60f88ac756ae930a777e38b432687113ba20e`  
		Last Modified: Tue, 04 Feb 2025 04:55:28 GMT  
		Size: 138.4 MB (138437583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5cc4ae66fc71e58d63974f1129907240137a19c2184aed63e360e8599e16ff0`  
		Last Modified: Tue, 04 Feb 2025 04:55:08 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feca01857b497f12c8c5d068ef46bad5efb49fdc819d84a213285db3d23415e2`  
		Last Modified: Fri, 31 Jan 2025 01:53:19 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b185e2e317d563c8815cad55b60e251ee7508edb14e7ee4870ce573b7c50113`  
		Last Modified: Tue, 04 Feb 2025 09:15:54 GMT  
		Size: 33.4 MB (33361228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c8e6ba61a91f5cff4e70de9dc88851b4438d4852272c589cac056be8bf2327`  
		Last Modified: Tue, 04 Feb 2025 09:15:51 GMT  
		Size: 9.2 MB (9170227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d9917f64b78e4c5b4aa5ed42eb9bbf5fdb16230d989cea741d81cebd366268`  
		Last Modified: Tue, 04 Feb 2025 09:15:49 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691fa8a58882f7e234985c917c2d68fd2360e001d02175f02a0b51ee76805353`  
		Last Modified: Tue, 04 Feb 2025 09:15:50 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302c63139ba0889106b3c7abf0050318cde462c200cf9c139e121f0e6cd33334`  
		Last Modified: Tue, 04 Feb 2025 09:15:50 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17` - unknown; unknown

```console
$ docker pull maven@sha256:05c76a0caee99214ae22300269a30f29bdc8db3a93171d3df0b157aa73196465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4981585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6156d0164b7a33a04802df4ff533c1a6177793e6ffa06bdc98594a8342ece552`

```dockerfile
```

-	Layers:
	-	`sha256:703556dfdb8a6399f67b79b47e54dc48a44985ab3f6288e65b3e77e5af97c954`  
		Last Modified: Tue, 04 Feb 2025 09:15:50 GMT  
		Size: 5.0 MB (4957023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26eceb1a416ae44807da379e77bdd97c50b4c72d97b74eb3ee26d39f753d81a7`  
		Last Modified: Tue, 04 Feb 2025 09:15:49 GMT  
		Size: 24.6 KB (24562 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17` - linux; s390x

```console
$ docker pull maven@sha256:79e97b75a41a895fac7f66b30fa1fbd7b44ca87fba4c42df03350b0da3b6031b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.2 MB (222249036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d46693ab0557d1fcc0d8df89d20c2bc0fea505ad333acb12cc06120ce9614e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 26 Oct 2024 17:22:34 GMT
ARG RELEASE
# Sat, 26 Oct 2024 17:22:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 26 Oct 2024 17:22:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 26 Oct 2024 17:22:34 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 26 Oct 2024 17:22:34 GMT
ADD file:1a65bb049384da7e51a2b1e9180f11d6ec22b1427da7ca5682814abd261ba57e in / 
# Sat, 26 Oct 2024 17:22:34 GMT
CMD ["/bin/bash"]
# Sat, 26 Oct 2024 17:22:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 26 Oct 2024 17:22:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 26 Oct 2024 17:22:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 26 Oct 2024 17:22:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Sat, 26 Oct 2024 17:22:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='d7ba818b1417b67f1f3cdcf7c5fac5e179998469dce7448349f24175eb9b2871';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 26 Oct 2024 17:22:34 GMT
CMD ["jshell"]
# Sat, 26 Oct 2024 17:22:34 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 26 Oct 2024 17:22:34 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 26 Oct 2024 17:22:34 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 26 Oct 2024 17:22:34 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 26 Oct 2024 17:22:34 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 26 Oct 2024 17:22:34 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 26 Oct 2024 17:22:34 GMT
ARG MAVEN_VERSION=3.9.9
# Sat, 26 Oct 2024 17:22:34 GMT
ARG USER_HOME_DIR=/root
# Sat, 26 Oct 2024 17:22:34 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 26 Oct 2024 17:22:34 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 26 Oct 2024 17:22:34 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:8e1d25585ef2d346b71072d258a697a9d190e3c5754512c7cb978dbbe80911e6`  
		Last Modified: Mon, 27 Jan 2025 05:10:30 GMT  
		Size: 30.0 MB (30027563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e861bff15ace5229469756101c0dfe916c9eb38c8a5cd02670f910ae5f61ca43`  
		Last Modified: Tue, 04 Feb 2025 07:46:14 GMT  
		Size: 22.1 MB (22132598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66edfe61b7bee16cfe328c7c38f7e2bff79edcdacf57f6b0b978ced78df727b`  
		Last Modified: Tue, 04 Feb 2025 07:46:16 GMT  
		Size: 134.6 MB (134623288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d432f939d5dba41c58721164d5612144df12ed5f24b53cf8538d16028d364a4`  
		Last Modified: Tue, 04 Feb 2025 07:46:13 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b6199f471cb128d3009b41eb5f6bedeb97eeba0612c58a6e0a5e35b280d6d8`  
		Last Modified: Tue, 04 Feb 2025 07:46:13 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9b4b2c65fcea05a3c366e5950d3c5b4d4d2401b164a7ba605aedc3c6bf1de6`  
		Last Modified: Tue, 04 Feb 2025 21:08:05 GMT  
		Size: 26.3 MB (26291556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b918377d28ccd291d2924a73885968ce0f14031513f4400423c76f094b7993`  
		Last Modified: Tue, 04 Feb 2025 21:08:04 GMT  
		Size: 9.2 MB (9170226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a082b0819cc422a3c12ebe9194be12f3c58d1d90202c8f4953c17d047e824c9`  
		Last Modified: Tue, 04 Feb 2025 21:08:03 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5630eee9ef2a88616076beb28e6b346f891a2d9660ab066854d0239842837f3`  
		Last Modified: Tue, 04 Feb 2025 21:08:04 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158f7207b6ec52142ceec633095af63d1a46659cbb2eb6a563ffbe42db2fe521`  
		Last Modified: Tue, 04 Feb 2025 21:08:04 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17` - unknown; unknown

```console
$ docker pull maven@sha256:2e129257b4fe4bd61b228d33dfa4a45c8a873c26afb3618bba14cc76f2662c9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4825119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff15cb296eea213b252c9c07e4a411075f169145840dc4b5442b7a1ca9b31262`

```dockerfile
```

-	Layers:
	-	`sha256:b19984ce84792d3b467bf7c930866c3bbd7188027b36a35a3b7b2a94666ec8a3`  
		Last Modified: Tue, 04 Feb 2025 21:08:04 GMT  
		Size: 4.8 MB (4800602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:310b69b1923e2610899111a42a00c31c5f3085c029974650a6325887cc4bf790`  
		Last Modified: Tue, 04 Feb 2025 21:08:03 GMT  
		Size: 24.5 KB (24517 bytes)  
		MIME: application/vnd.in-toto+json
