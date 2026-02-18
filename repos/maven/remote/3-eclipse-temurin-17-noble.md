## `maven:3-eclipse-temurin-17-noble`

```console
$ docker pull maven@sha256:55fac3153d579bdb7c7d7e684bdc9e35ef93ecb547100bf56e675dcef112f29c
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

### `maven:3-eclipse-temurin-17-noble` - linux; amd64

```console
$ docker pull maven@sha256:22e5056a4cd1e09d0373044e1a8f5f47711878cb5803b11c97729b856571a52e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230180469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:897d798fb52cd9312a97f1e3542c0f00acb9ba6a700d7ab734da0ab148c38dcf`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:19:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:19:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:19:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:19:39 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:19:39 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 17 Feb 2026 20:19:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='21050b8325b62cb3fca4f871aadbddc04c67e21f3ab57236439aa951cbcb17ae';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='485f49ec3f7048b466c3b8e5b543932c8aae845a1ba95ebb30fc527019371ed4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:19:46 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:19:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:19:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Feb 2026 20:19:46 GMT
CMD ["jshell"]
# Tue, 17 Feb 2026 21:46:33 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:46:33 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Feb 2026 21:46:33 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 21:46:33 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 21:46:33 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Feb 2026 21:46:33 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Feb 2026 21:46:33 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Feb 2026 21:46:33 GMT
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 21:46:33 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
# Tue, 17 Feb 2026 21:46:33 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Feb 2026 21:46:33 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 17 Feb 2026 21:46:33 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Feb 2026 21:46:33 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Feb 2026 21:46:33 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Feb 2026 21:46:33 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10f3ac7b458bcc0853b8cddf5bb91d305f64732b5e46f7897402e9104a2b6c7`  
		Last Modified: Tue, 17 Feb 2026 20:20:03 GMT  
		Size: 23.0 MB (22962446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bbcf5688c1943d868111317459775672c2eb59c07b04633f4653e36deaac799`  
		Last Modified: Tue, 17 Feb 2026 20:20:05 GMT  
		Size: 145.6 MB (145633930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78395afbc5ebce60b7dff0200af60f0f3df93dd724ebb8f148212ed7d9b243e7`  
		Last Modified: Tue, 17 Feb 2026 20:20:02 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd88562ce968f9f2742decb2b41610942b1696ea2c5e3d23e5a6d4d60c881435`  
		Last Modified: Tue, 17 Feb 2026 20:20:02 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae2e4a8370e72a1a6d344f3327ebc25ccd1efe410907e73e2a07439045b9982`  
		Last Modified: Tue, 17 Feb 2026 21:46:45 GMT  
		Size: 22.5 MB (22540659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0315dd7c027c164b61f78af3ace6a5fa4e4d25d18b2406bda298deb0c729ed5b`  
		Last Modified: Tue, 17 Feb 2026 21:46:45 GMT  
		Size: 9.3 MB (9312019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea46ab8f938aedf7388a5b43650520877c63c631ca9bd9d9492b92a27b0a0a2`  
		Last Modified: Tue, 17 Feb 2026 21:46:44 GMT  
		Size: 846.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c73c7e6cdbd7b9d1acbbdba324d2b71d4e1874ab56a9a362a5956f160e14c1d`  
		Last Modified: Tue, 17 Feb 2026 21:46:44 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a2ab1a3a0b3fc26424d804d6fb1e0291ff0c96b0157c89d03da35c46d61b0e`  
		Last Modified: Tue, 17 Feb 2026 21:46:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17-noble` - unknown; unknown

```console
$ docker pull maven@sha256:f227c5303dde0bfc58ce198c9415dab9d066d03931775699712f4eb6040a3aee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5072120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a087fad25968a51354de93f927d7d0a0efda3a99ab1202dc934a143068a251c9`

```dockerfile
```

-	Layers:
	-	`sha256:c74a8312dafa455c54f292aa3af34fe099f9e8f27fece986ce6d853a13b28970`  
		Last Modified: Tue, 17 Feb 2026 21:46:45 GMT  
		Size: 5.0 MB (5046016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8831fc103ff0b5cbb79c275e918906af10e2b25d09a432d708c6b235319ec7a`  
		Last Modified: Tue, 17 Feb 2026 21:46:44 GMT  
		Size: 26.1 KB (26104 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17-noble` - linux; arm variant v7

```console
$ docker pull maven@sha256:7510de16c07e79b3398bafcbfa4046cf8660bc8129e4d3546c1722e34b284479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227828377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b394f5fdd7f753ea56282768942ec033ce781ed2095d5d93ce4b5bbb24742a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 10 Feb 2026 16:51:23 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:51:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:51:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:51:24 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:51:27 GMT
ADD file:9633092e110ed5475e9e31841bcc6e288ca09c116e102d75694089f384f549b3 in / 
# Tue, 10 Feb 2026 16:51:28 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:12:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:12:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:12:19 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 17 Feb 2026 20:12:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='21050b8325b62cb3fca4f871aadbddc04c67e21f3ab57236439aa951cbcb17ae';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='485f49ec3f7048b466c3b8e5b543932c8aae845a1ba95ebb30fc527019371ed4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:12:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:12:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Feb 2026 20:12:28 GMT
CMD ["jshell"]
# Tue, 17 Feb 2026 21:19:46 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:19:49 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Feb 2026 21:19:49 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 21:19:49 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 21:19:49 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Feb 2026 21:19:49 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Feb 2026 21:19:49 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Feb 2026 21:19:49 GMT
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 21:19:49 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
# Tue, 17 Feb 2026 21:19:49 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Feb 2026 21:19:49 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 17 Feb 2026 21:19:49 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Feb 2026 21:19:49 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Feb 2026 21:19:49 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Feb 2026 21:19:49 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:dd135084b7c993802b7c1ba97d192c201727ddf710812c361d5441cb729f5c20`  
		Last Modified: Tue, 10 Feb 2026 17:41:49 GMT  
		Size: 26.9 MB (26855457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fcf9b8e1cf1354d2dbfb4f075947902a906cf11806654d5a7e9467e1b157df`  
		Last Modified: Tue, 17 Feb 2026 20:12:47 GMT  
		Size: 21.4 MB (21388491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f9e2e780b0aa077f01393ee70cf2f3770c67ab0b46fbb5560dd426b9e2e478`  
		Last Modified: Tue, 17 Feb 2026 20:12:50 GMT  
		Size: 143.0 MB (142994251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09246bf376973b8111f425f0e02ade8256ddf0a4af240469af19f84a16ab193c`  
		Last Modified: Tue, 17 Feb 2026 20:12:46 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad87b751ce78aadaaec52a961e84cefb97575caf040d8f1cf18e8a186ebaabeb`  
		Last Modified: Tue, 17 Feb 2026 20:12:46 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0b63782acf0d108505b2423dc7ec4add71452b9ab5cdcfb086ed9f9c3bd1ee`  
		Last Modified: Tue, 17 Feb 2026 21:20:01 GMT  
		Size: 27.3 MB (27274359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6fb445adbcec1e3771e4fb1e84990abba5bef6b3dbff65d1f4da88d532fd1eb`  
		Last Modified: Tue, 17 Feb 2026 21:20:00 GMT  
		Size: 9.3 MB (9312020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2ffeef4d32dc8be0977608bdd9e308ff5976fe2c60212e08e936e14871870e`  
		Last Modified: Tue, 17 Feb 2026 21:20:00 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deeca0ab6fa1ed3e7cb1a2b40ab5e4676d5c56c29f61e96088a0e6e01f471562`  
		Last Modified: Tue, 17 Feb 2026 21:20:00 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c82a1cef04a899bb46a4ec5fc442d9f04ec0220faf6176210127bc04c7c4dbb`  
		Last Modified: Tue, 17 Feb 2026 21:20:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17-noble` - unknown; unknown

```console
$ docker pull maven@sha256:0f60dec2ede79eb3309637715b978f07a1b4853c442470c963d6f46f99fe9b5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5010532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce6f318ff1b8cbe321930fe2db699adc0d26230d42467f1b4932ed4150eaece`

```dockerfile
```

-	Layers:
	-	`sha256:f681a124c92973b32e216f17d96dbc57555200d67d9af332f2a409526079d4f6`  
		Last Modified: Tue, 17 Feb 2026 21:20:00 GMT  
		Size: 5.0 MB (4984265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd3461e466d1ccf7ac5ea0a245305ac21340621d253f2187c6177eaf49df82dc`  
		Last Modified: Tue, 17 Feb 2026 21:20:00 GMT  
		Size: 26.3 KB (26267 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17-noble` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:e5070a6d02d64e87af7b52c21f682ae6f24c92948819b8eb9cf7e0953ada82c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.4 MB (229401783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd6d811d846b39b425eb28d6fd2b33e2b85ef4bd25dc33b56da341671c93b05`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:19:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:19:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:19:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:19:10 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:19:10 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 17 Feb 2026 20:19:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='21050b8325b62cb3fca4f871aadbddc04c67e21f3ab57236439aa951cbcb17ae';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='485f49ec3f7048b466c3b8e5b543932c8aae845a1ba95ebb30fc527019371ed4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:19:18 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:19:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:19:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Feb 2026 20:19:18 GMT
CMD ["jshell"]
# Tue, 17 Feb 2026 21:46:11 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:46:16 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Feb 2026 21:46:16 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 21:46:16 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 21:46:16 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Feb 2026 21:46:16 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Feb 2026 21:46:16 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Feb 2026 21:46:16 GMT
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 21:46:16 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
# Tue, 17 Feb 2026 21:46:16 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Feb 2026 21:46:16 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 17 Feb 2026 21:46:16 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Feb 2026 21:46:16 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Feb 2026 21:46:16 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Feb 2026 21:46:16 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03eac264d5df3e5eb1611554c669ffd726b07509669fe4411c456ad62c8b7c56`  
		Last Modified: Tue, 17 Feb 2026 20:19:36 GMT  
		Size: 24.2 MB (24167692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55071af2ac506944e21770c81b651f5847488178ff0b8c1a20af67215fa4af2f`  
		Last Modified: Tue, 17 Feb 2026 20:19:38 GMT  
		Size: 144.4 MB (144444038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1777e35d8796120890d06a7d8a9a53285fb384b677055548643f669b12f7a58`  
		Last Modified: Tue, 17 Feb 2026 20:19:35 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9731669689e82e918ab1cb1cbda39d05b6eb9bc7544f6f9d0ea3e41a4955015`  
		Last Modified: Tue, 17 Feb 2026 20:19:35 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e934bbfb3775053be63e5124de3b1e0cfd2b7a0952e4fa6b46e17dea35d29f`  
		Last Modified: Tue, 17 Feb 2026 21:46:31 GMT  
		Size: 22.6 MB (22609095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a701ba1e133c7ae732139a77ae81256a4852aeb7da9ce48eb182416f51d35aba`  
		Last Modified: Tue, 17 Feb 2026 21:46:31 GMT  
		Size: 9.3 MB (9312031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d717464f6e3a45cf21ddfef23d135d624e0787a2f11a4f9f2100cd7a97a31c3`  
		Last Modified: Tue, 17 Feb 2026 21:46:30 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b865274a2aa82efcc98dda565b90a05b3ed19345303af959aa9560cd988078`  
		Last Modified: Tue, 17 Feb 2026 21:46:30 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124a23849ab3fd8419f85473733f3d8b60c8c1d9867e6539e2048b76ce49baa6`  
		Last Modified: Tue, 17 Feb 2026 21:46:31 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17-noble` - unknown; unknown

```console
$ docker pull maven@sha256:ed5708384eef3dfd213952bb0037a1b5f000dc590a2b0375b74df7ade2d14514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5209922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d6f4e5a0ec43f89079975ceb29352fbf3fa3a136f9080c4019a10846d64df0`

```dockerfile
```

-	Layers:
	-	`sha256:093992351437746f7ad342ac25c90dcf4ab36f63a885be8418d5f9ed118030fc`  
		Last Modified: Tue, 17 Feb 2026 21:46:30 GMT  
		Size: 5.2 MB (5183613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a37f0ae27eb7dca9ce0b2ed906d5b5cf99110c31da4a26ba8bdfce2e1ad76105`  
		Last Modified: Tue, 17 Feb 2026 21:46:30 GMT  
		Size: 26.3 KB (26309 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17-noble` - linux; ppc64le

```console
$ docker pull maven@sha256:48bf45c36bd077e6866406b09e8537a613f606a056d92b0a9905d60e8c0b1ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.8 MB (239758543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa7a8a5b79f7e3da69c58395fdfd3af875bc6da9c31b899bf28cda46eab462e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:35 GMT
ADD file:993db8d05f03953198d71fcb66f9a9dca68dcfd7ca7b3e4a866954aa297b35ce in / 
# Tue, 10 Feb 2026 16:50:35 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:18:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:18:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:18:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:18:26 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:18:26 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 17 Feb 2026 20:18:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='21050b8325b62cb3fca4f871aadbddc04c67e21f3ab57236439aa951cbcb17ae';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='485f49ec3f7048b466c3b8e5b543932c8aae845a1ba95ebb30fc527019371ed4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:18:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:18:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:18:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Feb 2026 20:18:42 GMT
CMD ["jshell"]
# Wed, 18 Feb 2026 00:07:47 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Feb 2026 00:07:53 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 18 Feb 2026 00:07:53 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 18 Feb 2026 00:07:53 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 18 Feb 2026 00:07:53 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 18 Feb 2026 00:07:53 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 18 Feb 2026 00:07:53 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 18 Feb 2026 00:07:54 GMT
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 18 Feb 2026 00:07:55 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
# Wed, 18 Feb 2026 00:07:56 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 18 Feb 2026 00:07:56 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 18 Feb 2026 00:07:56 GMT
ARG USER_HOME_DIR=/root
# Wed, 18 Feb 2026 00:07:56 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 18 Feb 2026 00:07:56 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 18 Feb 2026 00:07:56 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6703b8ece0ce217ed67aed2176638b1c0350e7c03037dcb896534a4ce5717701`  
		Last Modified: Tue, 17 Feb 2026 20:19:22 GMT  
		Size: 24.1 MB (24105013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b51b4d285c18057ca2953badeb4295cedd2dbb9de0040649b364e75308c449`  
		Last Modified: Tue, 17 Feb 2026 20:19:25 GMT  
		Size: 145.4 MB (145442153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56e0d963cecc750cd56528c0fdc8dca07e42a8c364451325464e5634c550806`  
		Last Modified: Tue, 17 Feb 2026 20:19:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f373d81525a1ef425261ca57b59de8a8b189e892f1e63410a0f33e22a80829e8`  
		Last Modified: Tue, 17 Feb 2026 20:19:21 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26ca8e53a61c40e805bc1d34a73b6d87c9691f1b894e7e8424e14886cf2d22d`  
		Last Modified: Wed, 18 Feb 2026 00:08:28 GMT  
		Size: 26.6 MB (26588643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948d4cffcd7921120257780bac7ae1f4e87c8b293bb9d229bf404e1129108be0`  
		Last Modified: Wed, 18 Feb 2026 00:08:30 GMT  
		Size: 9.3 MB (9312019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5f364199daa3e7c3ebf448684dad57e88925473f7e9f0491d85da7afb9e786`  
		Last Modified: Wed, 18 Feb 2026 00:08:27 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efcb2177806d6495a060e3d5726789b627e8d1cf9300aa6bc95d08958a786d64`  
		Last Modified: Wed, 18 Feb 2026 00:08:27 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b376d3d698175bd1a6b76c7a4d49732c197f7355dd19f6f39dfd3ace615b48a5`  
		Last Modified: Wed, 18 Feb 2026 00:08:28 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17-noble` - unknown; unknown

```console
$ docker pull maven@sha256:111718aa77d44c00bfe1021b55b9a2287e9af49da4ec8139c75a284a08ebe9e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5122763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a51fe6e2076deef4621edc7c1e44c88ba9a66f79bae55748e49a8ad28a079f8`

```dockerfile
```

-	Layers:
	-	`sha256:852bd77204b1b7d21b683b51d26116a999956d1b6fc0d90ea2d7cbc01e2741b4`  
		Last Modified: Wed, 18 Feb 2026 00:08:27 GMT  
		Size: 5.1 MB (5096591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c724897c900a83959819e599c96727a04f30118da45af8a243f38a839212e893`  
		Last Modified: Wed, 18 Feb 2026 00:08:27 GMT  
		Size: 26.2 KB (26172 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17-noble` - linux; riscv64

```console
$ docker pull maven@sha256:3f14fa1ac329bea3c8293ef7a997b1a499bde2221d3e0e834feac9128c27bb0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234088790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3bef92fb0adc4f4dd9f55fc2f947fadd2d8d5e9044cd6384cb889f3d475b907`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 13 Jan 2026 06:14:56 GMT
ARG RELEASE
# Tue, 13 Jan 2026 06:14:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 06:14:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 06:14:58 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 06:15:46 GMT
ADD file:8d0655de001e92042901c645c76202ac355acb6fa186561e7344a0829ffd983d in / 
# Tue, 13 Jan 2026 06:15:51 GMT
CMD ["/bin/bash"]
# Mon, 19 Jan 2026 18:08:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 19 Jan 2026 18:08:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 Jan 2026 18:08:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 19 Jan 2026 18:08:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Jan 2026 18:08:38 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Sun, 08 Feb 2026 00:07:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='21050b8325b62cb3fca4f871aadbddc04c67e21f3ab57236439aa951cbcb17ae';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='485f49ec3f7048b466c3b8e5b543932c8aae845a1ba95ebb30fc527019371ed4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 08 Feb 2026 00:07:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 08 Feb 2026 00:07:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 08 Feb 2026 00:07:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 08 Feb 2026 00:07:38 GMT
CMD ["jshell"]
# Mon, 09 Feb 2026 13:31:55 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 13:32:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 09 Feb 2026 13:32:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 09 Feb 2026 13:32:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 09 Feb 2026 13:32:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 09 Feb 2026 13:32:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 09 Feb 2026 13:32:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 09 Feb 2026 13:32:09 GMT
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 09 Feb 2026 13:32:09 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
# Mon, 09 Feb 2026 13:32:09 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 09 Feb 2026 13:32:09 GMT
ARG MAVEN_VERSION=3.9.12
# Mon, 09 Feb 2026 13:32:09 GMT
ARG USER_HOME_DIR=/root
# Mon, 09 Feb 2026 13:32:09 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 09 Feb 2026 13:32:09 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 09 Feb 2026 13:32:09 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f151392858868452ec0f1f8d2947624e8dcdecf23bce587cfbd7c38a3264f9df`  
		Last Modified: Tue, 13 Jan 2026 06:36:06 GMT  
		Size: 31.0 MB (30953090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70a79886c4402a76ef90814a79e96c424cf0e215bb8c0b7d7f29e0d0acc7bd0`  
		Last Modified: Mon, 19 Jan 2026 18:13:27 GMT  
		Size: 20.1 MB (20146747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3365fc6e81443b39ba1db08593be084a9f6b6aee019bf65ba03980478e75ad`  
		Last Modified: Sun, 08 Feb 2026 00:11:48 GMT  
		Size: 142.7 MB (142673677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca0e603c1d8c618ddf30d3eb7ed10b80f44e8237ad5e30b39c8c6072e59a5124`  
		Last Modified: Sun, 08 Feb 2026 00:11:27 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62a9782326449af4166ece38402261ba1a953a160b1acca2fa294eb0210bad9`  
		Last Modified: Sun, 08 Feb 2026 00:11:27 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf02b772a3a92e3d02d309f3286001a3a47d12aa61326afb7620d1e9c146a1d3`  
		Last Modified: Mon, 09 Feb 2026 13:35:26 GMT  
		Size: 31.0 MB (30999439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e161e61980b57c5a55c1d4d19d16da4b9d023fc0cbc12aa981c70a4613a31865`  
		Last Modified: Mon, 09 Feb 2026 13:35:23 GMT  
		Size: 9.3 MB (9312024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d113381e0f0b371e4e6216249be7974f54d95241c0acc59612a377080a21d3d3`  
		Last Modified: Mon, 09 Feb 2026 13:35:20 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc8e69241c6797a56790703ae69d35c9b50a85c04746b33a533f124bd31293de`  
		Last Modified: Mon, 09 Feb 2026 13:35:20 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52070d19f1b2d31534cee82ab22190fb4984d1257269fb99e50cb05c0f39a48f`  
		Last Modified: Mon, 09 Feb 2026 13:35:22 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17-noble` - unknown; unknown

```console
$ docker pull maven@sha256:055f23746ac99980d3f12d118ea16f0fc1abf98e9fa0a09ce0bf1b404399ee97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5173901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa752da002d67b4751d8d0f6e061c824e513ccea17bade16afb31f61956c96e7`

```dockerfile
```

-	Layers:
	-	`sha256:74fc2fdbe300ea8672d93a4be856086d7d999704326cf58440b667e37c0ef0cd`  
		Last Modified: Mon, 09 Feb 2026 13:35:22 GMT  
		Size: 5.1 MB (5147729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eb5350b789d5df8f8c7936d00e34a791dda9d21e28d4ccc67e6796628e5af7b`  
		Last Modified: Mon, 09 Feb 2026 13:35:20 GMT  
		Size: 26.2 KB (26172 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17-noble` - linux; s390x

```console
$ docker pull maven@sha256:d7d3002ef050490dab410d7f73530a1e17b5f2ed50ec488b5fa9d3c03bbec8f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220656363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06373901f294a696841599c10546a3398519ee7d0b5e42db51126bcf2ad371ca`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:51 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:51 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:52 GMT
ADD file:be1799101a7a15f881e3aebea1e86fa6a156760dc7688b1affe179e948814a3b in / 
# Tue, 10 Feb 2026 16:50:52 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:13:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:13:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:13:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:13:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:13:16 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 17 Feb 2026 20:13:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='21050b8325b62cb3fca4f871aadbddc04c67e21f3ab57236439aa951cbcb17ae';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='485f49ec3f7048b466c3b8e5b543932c8aae845a1ba95ebb30fc527019371ed4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:13:23 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:13:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:13:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Feb 2026 20:13:23 GMT
CMD ["jshell"]
# Tue, 17 Feb 2026 22:20:43 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 22:20:49 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Feb 2026 22:20:49 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:20:49 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:20:49 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Feb 2026 22:20:49 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Feb 2026 22:20:49 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Feb 2026 22:20:49 GMT
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 22:20:51 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
# Tue, 17 Feb 2026 22:20:52 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Feb 2026 22:20:52 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 17 Feb 2026 22:20:52 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Feb 2026 22:20:52 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Feb 2026 22:20:52 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Feb 2026 22:20:52 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:8b6ba492713239cba0554ce53d24405e1285684fa64bcfb05df4af8037ba5836`  
		Last Modified: Tue, 10 Feb 2026 17:42:12 GMT  
		Size: 29.9 MB (29909784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c61c0dceff600fa73a9e5c4c1e6b5bd67c056a803cadf4663f05f037f3b413`  
		Last Modified: Tue, 17 Feb 2026 20:13:59 GMT  
		Size: 22.1 MB (22132300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a2b165a5fba8af9a2e977c81f301b9d7c5419451e10e73cac02e889467deae`  
		Last Modified: Tue, 17 Feb 2026 20:14:01 GMT  
		Size: 135.6 MB (135631870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd81daff4e2f95b8488e3f8a8b906c21526856272c6e595a95f9e11f7e2b324`  
		Last Modified: Tue, 17 Feb 2026 20:13:58 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520c3dd95c98dc1182338a43a3c388dcf56e1e4ab3a398575d60aa93eaf9fe7e`  
		Last Modified: Tue, 17 Feb 2026 20:13:58 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523cad7f980cb24b99ed3fe3958a65ec754c755cae3d94940655115d8a06bfd7`  
		Last Modified: Tue, 17 Feb 2026 22:21:27 GMT  
		Size: 23.7 MB (23666584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4006db8f1f096c9b8ae9afbd11b1830802e8ac7e83ea099bea2573504a23b4cf`  
		Last Modified: Tue, 17 Feb 2026 22:21:27 GMT  
		Size: 9.3 MB (9312020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae83a8d758b7d98713f4a2671ba6cd6f78726cdc4ad9022da2279bda2fafe61a`  
		Last Modified: Tue, 17 Feb 2026 22:21:27 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf338f375dcc2e9dea8024edb45b27866da1591976493650eb2b566b0d1bd04c`  
		Last Modified: Tue, 17 Feb 2026 22:21:27 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef89c7f1030c4295d3e47abb4aacd0a25eab3c4da049215160a017ec1d749272`  
		Last Modified: Tue, 17 Feb 2026 22:21:28 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17-noble` - unknown; unknown

```console
$ docker pull maven@sha256:7da056065d249491575c44c95ce6f305ebeb1f660ccb2248f72ef04f601a1ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5017521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f0312c7c4170615575518b09b93618aee096facd37743d2bd5de7754e8a4d2d`

```dockerfile
```

-	Layers:
	-	`sha256:35b3df47b480b2a9d92ab5e51a6cab398eaa9bf8da6c30c9b7b2060e0091abf9`  
		Last Modified: Tue, 17 Feb 2026 22:21:27 GMT  
		Size: 5.0 MB (4991418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:084c32ecc918a345d4e0773421194eee24674f7f9e99a9081dc0610a295d98c5`  
		Last Modified: Tue, 17 Feb 2026 22:21:27 GMT  
		Size: 26.1 KB (26103 bytes)  
		MIME: application/vnd.in-toto+json
