## `maven:3-eclipse-temurin-17-noble`

```console
$ docker pull maven@sha256:674de0df5a38cfe793a587829a181835f8af3ea1f556be7172e0aa547274bcc9
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
$ docker pull maven@sha256:24f2acc3ce39e5af4431378984cd035be99a7d1e7d19d91303a6b3e4e735f782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230188006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eb4a3be9878e576cd3da128b073573bc6144dd508c0e35516396515ed0747d1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:33:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:33:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:33:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:33:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:33:38 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:33:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='21050b8325b62cb3fca4f871aadbddc04c67e21f3ab57236439aa951cbcb17ae';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='485f49ec3f7048b466c3b8e5b543932c8aae845a1ba95ebb30fc527019371ed4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:33:46 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:33:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:33:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 20:33:46 GMT
CMD ["jshell"]
# Wed, 15 Apr 2026 22:09:05 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:09:10 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 15 Apr 2026 22:09:10 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 22:09:10 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 22:09:10 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 15 Apr 2026 22:09:10 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 15 Apr 2026 22:09:10 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 15 Apr 2026 22:09:10 GMT
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 22:09:10 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
# Wed, 15 Apr 2026 22:09:10 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 15 Apr 2026 22:09:10 GMT
ARG USER_HOME_DIR=/root
# Wed, 15 Apr 2026 22:09:10 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 15 Apr 2026 22:09:10 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 15 Apr 2026 22:09:10 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78dbd4bf6df60adadc649324ed935bca4d910519f68acf374ab030c3c9cb3048`  
		Last Modified: Wed, 15 Apr 2026 20:34:03 GMT  
		Size: 23.0 MB (22965417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f3fd0f1c2176e779aabd80195ebcf9b908f943622f8d916931360b0cbf665b`  
		Last Modified: Wed, 15 Apr 2026 20:34:06 GMT  
		Size: 145.6 MB (145633837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f907e7b2d67743a675319ea202651b65dc9b515430be6018c6fd18bf88461f64`  
		Last Modified: Wed, 15 Apr 2026 20:34:02 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286cf14499d5b0f1da8709959ce97f11188bd32cbb5b46a0892214ccdfc88861`  
		Last Modified: Wed, 15 Apr 2026 20:34:02 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf78702371929e307b7300e4d026bd951512378e1a37fe3776af98ded0d3a3c8`  
		Last Modified: Wed, 15 Apr 2026 22:09:24 GMT  
		Size: 22.5 MB (22541004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425de70ce304e0d33bc652fbf0b0b2ea384970ec81439e358c4ae5ae58dc0955`  
		Last Modified: Wed, 15 Apr 2026 22:09:24 GMT  
		Size: 9.3 MB (9310969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2fc84d249b10d52a642c4152e538d263445539b42b79219550e3505a36a6c5`  
		Last Modified: Wed, 15 Apr 2026 22:09:23 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2956b070321d6189f3e55e83fbaec3dff5a2cad7f6456501767ce167795a9f`  
		Last Modified: Wed, 15 Apr 2026 22:09:23 GMT  
		Size: 356.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:debf58b15d174f6891bd9bd74793c5c6e03e29682a7cb9a8e894fa2e7761f07c`  
		Last Modified: Wed, 15 Apr 2026 22:09:24 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17-noble` - unknown; unknown

```console
$ docker pull maven@sha256:a59034ab9c3ae86a4f380ee97d1337ddbc38f340b984360acfe39f30cc2d70c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5072116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45822de8af34e21a8bffe99b6a46a2cc2196b66bbb472b4332f505f956d8801f`

```dockerfile
```

-	Layers:
	-	`sha256:03fe957793e5281e6319e9054f8482720c21b0f8e0cc09739680bdf340585063`  
		Last Modified: Wed, 15 Apr 2026 22:09:24 GMT  
		Size: 5.0 MB (5046048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75eae14a524506995f629725bf759e0ec2279f76ac1abe51e42e62290a8eeb29`  
		Last Modified: Wed, 15 Apr 2026 22:09:23 GMT  
		Size: 26.1 KB (26068 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17-noble` - linux; arm variant v7

```console
$ docker pull maven@sha256:beb031b973150889005b3a22d5bf6749089695e3641ee387eae4885d38d3bf18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227834247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0517a89a2efb81bd66a0426e75d9b2f6b992856fb30bc558379955ab8338a75`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:30 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:30 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:33 GMT
ADD file:341ecc672c4413d50e9543a8a38e44f8686dbdcc696b241b06e6b5b3a3ad57f6 in / 
# Fri, 10 Apr 2026 06:56:33 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:33:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:33:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:33:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:33:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:33:36 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:33:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='21050b8325b62cb3fca4f871aadbddc04c67e21f3ab57236439aa951cbcb17ae';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='485f49ec3f7048b466c3b8e5b543932c8aae845a1ba95ebb30fc527019371ed4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:33:49 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:33:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:33:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 20:33:49 GMT
CMD ["jshell"]
# Wed, 15 Apr 2026 21:41:24 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:41:28 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 15 Apr 2026 21:41:28 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 21:41:28 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 21:41:28 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 15 Apr 2026 21:41:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 15 Apr 2026 21:41:28 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 15 Apr 2026 21:41:28 GMT
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:41:28 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
# Wed, 15 Apr 2026 21:41:28 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 15 Apr 2026 21:41:28 GMT
ARG USER_HOME_DIR=/root
# Wed, 15 Apr 2026 21:41:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 15 Apr 2026 21:41:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 15 Apr 2026 21:41:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:03a6f28563c3f1bd861a0bd521bea32abc15b3b1362797f0ee963f0cfbe31325`  
		Last Modified: Fri, 10 Apr 2026 09:34:31 GMT  
		Size: 26.9 MB (26859689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7d52ac9b5aabafb39c3240afb9e6a6c108558b6ce7a15af05acd854c4c4106`  
		Last Modified: Wed, 15 Apr 2026 20:34:06 GMT  
		Size: 21.4 MB (21389580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9a8502dfb1d31d6374b08dab38678ee59467e09447d401e19135243b9424da`  
		Last Modified: Wed, 15 Apr 2026 20:34:09 GMT  
		Size: 143.0 MB (142994547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6005608956f43671fb5b0e730ff6d908f35eaacb27076e62c558ee4c38231fa`  
		Last Modified: Wed, 15 Apr 2026 20:34:05 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac8cb2cd45735fb4da63f8ffece72017654a0d2f03cdf3e2bb328cd47402a5e`  
		Last Modified: Wed, 15 Apr 2026 20:33:29 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304182df5f8593fc1b8e7954a97cf609b946353cefda0d0681f2348e527bcf41`  
		Last Modified: Wed, 15 Apr 2026 21:41:41 GMT  
		Size: 27.3 MB (27275679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19523fe7cc3b8b82a0c77ad67028ba10442ff8a128bedce1de2dd8ddfa26650b`  
		Last Modified: Wed, 15 Apr 2026 21:41:40 GMT  
		Size: 9.3 MB (9310952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e131a5dd94b7d6f348eac02127902454489c68ef4b656e2bb20895026852dc1`  
		Last Modified: Wed, 15 Apr 2026 21:41:40 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e664d2d032df99346ff860e241d74c8c05c17f177ac5f26497d1092d42900dd`  
		Last Modified: Wed, 15 Apr 2026 21:41:40 GMT  
		Size: 357.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df53f97d5b11e3f92b6ddcba1c79671cd8384a684c83143f70a5795da0bc9cf`  
		Last Modified: Wed, 15 Apr 2026 21:41:41 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17-noble` - unknown; unknown

```console
$ docker pull maven@sha256:8ccbcdf14ed0c168a085a6296461e1c9e7543307a78381d025148243552a4737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5010526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:916dddde62207379594228a276b81157669484525424f404db311fa2ca2e7e47`

```dockerfile
```

-	Layers:
	-	`sha256:b29b093cc86344eeca9d66c72185cd86fce1cfb1ea5e248bf83fce676b64f64a`  
		Last Modified: Wed, 15 Apr 2026 21:41:40 GMT  
		Size: 5.0 MB (4984295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ed56a35135b748be800caef4208c9146e6cd1348155d453140e95ed2ebe2ebc`  
		Last Modified: Wed, 15 Apr 2026 21:41:40 GMT  
		Size: 26.2 KB (26231 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17-noble` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:0fd2fffeb24c3231625e06110615ca4bae8a2eaace5476a986ffb18e507aa806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.4 MB (229415120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a739878f605737f942b6f8e80d9c53c6dc1235dace5b8df1572bb2a0d4a63491`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:33:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:33:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:33:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:33:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:33:41 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:33:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='21050b8325b62cb3fca4f871aadbddc04c67e21f3ab57236439aa951cbcb17ae';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='485f49ec3f7048b466c3b8e5b543932c8aae845a1ba95ebb30fc527019371ed4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:33:48 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:33:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:33:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 20:33:48 GMT
CMD ["jshell"]
# Wed, 15 Apr 2026 22:20:47 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:20:52 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 15 Apr 2026 22:20:52 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 22:20:52 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 22:20:52 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 15 Apr 2026 22:20:52 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 15 Apr 2026 22:20:52 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 15 Apr 2026 22:20:52 GMT
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 22:20:52 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
# Wed, 15 Apr 2026 22:20:52 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 15 Apr 2026 22:20:52 GMT
ARG USER_HOME_DIR=/root
# Wed, 15 Apr 2026 22:20:52 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 15 Apr 2026 22:20:52 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 15 Apr 2026 22:20:52 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b90980f1e34331b287aa136d58391a04413e0c3ef70e514fffe91df8277db4`  
		Last Modified: Wed, 15 Apr 2026 20:34:06 GMT  
		Size: 24.2 MB (24171216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ce5ce0be8920e36d38d4d52a5fbe8b857120b69ae9d30f30ca91f6b9b1e835`  
		Last Modified: Wed, 15 Apr 2026 20:34:09 GMT  
		Size: 144.4 MB (144444070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6d55f210406fb30d7c905aa44462f96cbfcdd975a2810f6fe56bd1ebae2f61`  
		Last Modified: Wed, 15 Apr 2026 20:34:05 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61786f915b16e31860ac17ff543d4af19a0816a2055db0691007e8fb65c59993`  
		Last Modified: Wed, 15 Apr 2026 20:33:54 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0b186f0ee85180ed77e9605ef8b2231fdaeb2571bde39b64898aec435c079e`  
		Last Modified: Wed, 15 Apr 2026 22:21:05 GMT  
		Size: 22.6 MB (22609302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1206d117c6b5b256d82710b2da538d616b82404fb68148c139f896ab6c0f5333`  
		Last Modified: Wed, 15 Apr 2026 22:21:04 GMT  
		Size: 9.3 MB (9310953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7d7567b1984f3b473fe34a884dac316a3241ece9e56c7f95331ed8c859aeee`  
		Last Modified: Wed, 15 Apr 2026 22:21:04 GMT  
		Size: 846.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb27acd7907590241209fc96de1718e667013396cc6c58689a2f5c4646052521`  
		Last Modified: Wed, 15 Apr 2026 22:21:04 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b48e791d58e5ed6cceecd76f069fb17071caa97ad429f618f106c31d506c53`  
		Last Modified: Wed, 15 Apr 2026 22:21:05 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17-noble` - unknown; unknown

```console
$ docker pull maven@sha256:27aeab6c8f9a8015b109b072feebf27ad6110a617ac7749d3406c66e493b5d3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5209918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096dd5a4e528fdbd5504b45c8c5ef763030bbf5ccedd3c891526663c9a4812f5`

```dockerfile
```

-	Layers:
	-	`sha256:2db0f4bdb1f2afd64d121b2e34ddc53c9014d25dea456948461d9f5c0bb73da9`  
		Last Modified: Wed, 15 Apr 2026 22:21:04 GMT  
		Size: 5.2 MB (5183645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78f47aa96bcd0f1946eda99e7efbfc2560ebf7e8f8ddb113e6bf6cacac2613be`  
		Last Modified: Wed, 15 Apr 2026 22:21:04 GMT  
		Size: 26.3 KB (26273 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17-noble` - linux; ppc64le

```console
$ docker pull maven@sha256:b650c796081f193abee197325c16e03a5318cf255bf14f36b45f4e4ea4f93045
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.8 MB (239755231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf2cea62d9b280c1ef19d564d8ec1f7f8f3ad524f6cf37bc6b73d2f810cfac9`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:18:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 21:18:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:18:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 21:18:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:18:06 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 21:18:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='21050b8325b62cb3fca4f871aadbddc04c67e21f3ab57236439aa951cbcb17ae';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='485f49ec3f7048b466c3b8e5b543932c8aae845a1ba95ebb30fc527019371ed4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 21:18:22 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 21:18:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:18:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 21:18:23 GMT
CMD ["jshell"]
# Thu, 16 Apr 2026 03:23:32 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Apr 2026 03:23:39 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 16 Apr 2026 03:23:39 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 16 Apr 2026 03:23:39 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 16 Apr 2026 03:23:39 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 16 Apr 2026 03:23:39 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 16 Apr 2026 03:23:39 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 16 Apr 2026 03:23:39 GMT
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 16 Apr 2026 03:23:40 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
# Thu, 16 Apr 2026 03:23:40 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 16 Apr 2026 03:23:40 GMT
ARG USER_HOME_DIR=/root
# Thu, 16 Apr 2026 03:23:40 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 16 Apr 2026 03:23:40 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 16 Apr 2026 03:23:40 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053e955f9e814add024b501a8f341ea40f458696ac7204b476dfa5a6086a32ec`  
		Last Modified: Wed, 15 Apr 2026 21:19:07 GMT  
		Size: 24.1 MB (24093352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77153addc62f975cc8aa954a1524baa5e378c08c8d32f03d548bee1e4d4af68`  
		Last Modified: Wed, 15 Apr 2026 21:19:09 GMT  
		Size: 145.4 MB (145442311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155fcd132a483ea0a6bf7fda87aa43e19d52434b14f2640eb98172e6ea94ea76`  
		Last Modified: Wed, 15 Apr 2026 21:19:05 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23b054593aeea5229b95530ae8bc06fdce908c8758936a7c74e3f10b0bc1c18`  
		Last Modified: Wed, 15 Apr 2026 21:19:05 GMT  
		Size: 2.3 KB (2278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6b0e229f77c40067a6a0c00383c187de30f687c7b2db6084614fc932d58938`  
		Last Modified: Thu, 16 Apr 2026 03:24:14 GMT  
		Size: 26.6 MB (26590630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f14bc4fb5ce2b061e7f4d6c5ba7f32ee04d469748ad3afdd21ae21a52bee44`  
		Last Modified: Thu, 16 Apr 2026 03:24:13 GMT  
		Size: 9.3 MB (9310960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c3f91faaf6e951aed4a15c632d024a61b3828776222192ca5a9caf5aa4a105`  
		Last Modified: Thu, 16 Apr 2026 03:24:13 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6409e2e9789a54a96aa0d84542d15d0b622331b0af9c428a02dab2044f1eeab8`  
		Last Modified: Thu, 16 Apr 2026 03:24:13 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1070dcceffd7deb1db592a60725056eea63b80d8b8d21795a1bf7f4893a8f3c`  
		Last Modified: Thu, 16 Apr 2026 03:24:14 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17-noble` - unknown; unknown

```console
$ docker pull maven@sha256:7fbab805639a5afd728cebe3441b14834ff742cd21cc39afec598f3de480f125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5122757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e65c7f16a2ac67fcb92bf51e82173a3b20d28f789ab9ab7ed1e30a0570ab15fa`

```dockerfile
```

-	Layers:
	-	`sha256:60aa6e65822f0a638881491754714aac34743f8d833188338b811efabdb0d990`  
		Last Modified: Thu, 16 Apr 2026 03:24:13 GMT  
		Size: 5.1 MB (5096621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bc4160ff42b5171619ae701e2f2d71e312b16101c5052a2c361ec547333fef8`  
		Last Modified: Thu, 16 Apr 2026 03:24:13 GMT  
		Size: 26.1 KB (26136 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17-noble` - linux; riscv64

```console
$ docker pull maven@sha256:4752ceebf7b5949d7d4f1dc81dbe573f2cca0046a623d500c448ca9e73584cc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234107697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b93d0eddd216374dd55bf5bef5e2680ff1a29d02e287e6eabb3aa470081e2c3`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 10 Apr 2026 09:24:05 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:24:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:24:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 09:24:43 GMT
ADD file:a9a4679e3df2846468311b83a8f6ab86f5a205bab966d3f236c9f30151010c5b in / 
# Fri, 10 Apr 2026 09:24:47 GMT
CMD ["/bin/bash"]
# Thu, 16 Apr 2026 16:46:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 16:46:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 16:46:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Apr 2026 16:46:37 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Apr 2026 16:46:37 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Thu, 16 Apr 2026 16:47:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='21050b8325b62cb3fca4f871aadbddc04c67e21f3ab57236439aa951cbcb17ae';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='485f49ec3f7048b466c3b8e5b543932c8aae845a1ba95ebb30fc527019371ed4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 16 Apr 2026 16:47:46 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 16 Apr 2026 16:47:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 16 Apr 2026 16:47:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 16 Apr 2026 16:47:47 GMT
CMD ["jshell"]
# Sat, 18 Apr 2026 06:50:10 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 18 Apr 2026 06:50:23 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 18 Apr 2026 06:50:23 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 18 Apr 2026 06:50:23 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 18 Apr 2026 06:50:23 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 18 Apr 2026 06:50:23 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 18 Apr 2026 06:50:23 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 18 Apr 2026 06:50:24 GMT
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 18 Apr 2026 06:50:24 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
# Sat, 18 Apr 2026 06:50:24 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 18 Apr 2026 06:50:24 GMT
ARG USER_HOME_DIR=/root
# Sat, 18 Apr 2026 06:50:24 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 18 Apr 2026 06:50:24 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 18 Apr 2026 06:50:24 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a7f0c74374451005259fe6b1b7ef3185055f2b6c419b5ba0ae8e4f55b1e1c31d`  
		Last Modified: Fri, 10 Apr 2026 09:34:45 GMT  
		Size: 31.0 MB (30965327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb43b647117c9f43692f378d47bfa7800d85b1756ada8ad0318423a33c02a7d`  
		Last Modified: Thu, 16 Apr 2026 16:51:32 GMT  
		Size: 20.2 MB (20151745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790484bc5978595764d5d853fe629dd792c406bf4dad318694d851a7f420dc43`  
		Last Modified: Thu, 16 Apr 2026 16:51:51 GMT  
		Size: 142.7 MB (142673710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6845b7c27596bb93e532e175f3a0f9973f871216c83e833790224504db1ff111`  
		Last Modified: Thu, 16 Apr 2026 16:51:25 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513bfa7cd5cd01ddeb5adcaf4ee98bc39a1f5a00cde1c9d808b0a2ff9541b997`  
		Last Modified: Thu, 16 Apr 2026 16:51:26 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472618cbbb090db3d5634c3615604ddae96529b08c6c88162140d4b808c04f02`  
		Last Modified: Sat, 18 Apr 2026 06:53:32 GMT  
		Size: 31.0 MB (31002137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d282bdcb7b1442b37e53e8d93524bf91264d6467b1b94f58714d33553b42f1`  
		Last Modified: Sat, 18 Apr 2026 06:53:29 GMT  
		Size: 9.3 MB (9310968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a4456d46105b072b22580e5348a01f30091ce99f8fd8ed5c2ed6fe37ba1754`  
		Last Modified: Sat, 18 Apr 2026 06:53:26 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ed0db232b8f9fd03b5e0e2d47d03c4d5e76154431d8d3aae002fc4dfd5e12b`  
		Last Modified: Sat, 18 Apr 2026 06:53:26 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423587c320ac85524d21d736d204df867d557e7d46e352aff44579a5d997fa83`  
		Last Modified: Sat, 18 Apr 2026 06:53:28 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17-noble` - unknown; unknown

```console
$ docker pull maven@sha256:0b28d2c02f7c2333e0e6d203565ce17f43b51142ac7c32089871caea7986bea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5173903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f3f63a0ee8bd6f5fc8f3fd86790378db3cc1672f3c3b5f335985cfa1460ca1`

```dockerfile
```

-	Layers:
	-	`sha256:33c95a74d5e9f88d145bef0c5b9d0de0b49f7bdbca6bb34354550642c575ba56`  
		Last Modified: Sat, 18 Apr 2026 06:53:28 GMT  
		Size: 5.1 MB (5147767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ea99839432c326416fc33537cfdba5a4d5ee6b45b6b882e28af53dba862a0f9`  
		Last Modified: Sat, 18 Apr 2026 06:53:26 GMT  
		Size: 26.1 KB (26136 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17-noble` - linux; s390x

```console
$ docker pull maven@sha256:5d377aad5ace0f7cc1fbc7924e630426c1466e0c6bef43789efcaa296062a6b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220656279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e35a9f59a25f5e4c15196110d42aa9bdaf30d6f3522204eaaaf09dba8effb25`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 10 Apr 2026 06:50:27 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:50:29 GMT
ADD file:41defd98c44eed6fc946fd94496a94164879f2ad4f63d66a5c1e213cc2259ad1 in / 
# Fri, 10 Apr 2026 06:50:29 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:45:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:45:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:45:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:45:14 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:45:14 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:45:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        arm64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        armhf)          ESUM='21050b8325b62cb3fca4f871aadbddc04c67e21f3ab57236439aa951cbcb17ae';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64el)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        riscv64)          ESUM='485f49ec3f7048b466c3b8e5b543932c8aae845a1ba95ebb30fc527019371ed4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:45:21 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:45:21 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:45:21 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 20:45:21 GMT
CMD ["jshell"]
# Thu, 16 Apr 2026 00:49:37 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Apr 2026 00:49:41 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 16 Apr 2026 00:49:41 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 16 Apr 2026 00:49:41 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 16 Apr 2026 00:49:41 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 16 Apr 2026 00:49:41 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 16 Apr 2026 00:49:41 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 16 Apr 2026 00:49:41 GMT
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 16 Apr 2026 00:49:41 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
# Thu, 16 Apr 2026 00:49:41 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 16 Apr 2026 00:49:41 GMT
ARG USER_HOME_DIR=/root
# Thu, 16 Apr 2026 00:49:41 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 16 Apr 2026 00:49:41 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 16 Apr 2026 00:49:41 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:ef1c26d09a5f9962879f732e212c4246a41e8473f6120efb435886357c85dd5a`  
		Last Modified: Fri, 10 Apr 2026 09:34:53 GMT  
		Size: 29.9 MB (29912147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f0c98d4f049f66eb7465b6da7d86ea355d897ad8dc0256a5fb63d4e160c164`  
		Last Modified: Wed, 15 Apr 2026 20:45:47 GMT  
		Size: 22.1 MB (22127292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff57945ebac6c8e5e47f7c319a0733b1999db91a2b18c89eeaefe1519b6ce91`  
		Last Modified: Wed, 15 Apr 2026 20:45:50 GMT  
		Size: 135.6 MB (135631508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a024addc9574b299cef48fb71d039145869c81a8409fb75fc63cb2c5840c83`  
		Last Modified: Wed, 15 Apr 2026 20:45:46 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09cd69fccdd9211f3f2a52f4db80f04893c70a26c6f25a59376ba3b39e6f4e7`  
		Last Modified: Wed, 15 Apr 2026 20:45:42 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70dda92552e3ca1a650643dcfcc2d1d8b66010807edf0f0b91ef42f91edeeb0d`  
		Last Modified: Thu, 16 Apr 2026 00:50:00 GMT  
		Size: 23.7 MB (23670572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657491a6f7b3e4ee11b95ea82fa9710e92ac75193d44217846674b3f5dfdedf5`  
		Last Modified: Thu, 16 Apr 2026 00:50:00 GMT  
		Size: 9.3 MB (9310955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6406e043fb37203ffa01988fbaf06e7aa3ff8b36e4064e919248746c24640cba`  
		Last Modified: Thu, 16 Apr 2026 00:50:00 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57792c4b866c42d6b21df4a9476554d999f663a1cf351d55c3d2688d557606c0`  
		Last Modified: Thu, 16 Apr 2026 00:50:00 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6351f956b07c99a293d5b82efdd5ff8986e8a00c6bad562207730d82f8d566`  
		Last Modified: Thu, 16 Apr 2026 00:50:01 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17-noble` - unknown; unknown

```console
$ docker pull maven@sha256:8391a13d7c2b7d8ae0b6d60a701d48ca6868f3572e114f94b2e406bdc7442c46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5017516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f86ed55436b0c21c7642cb78a96d3a47cd766f63754ff11e5a00d7f94a9dcc5c`

```dockerfile
```

-	Layers:
	-	`sha256:3e3573058186df37efd57aaa757e87054949142d3dd9abd9901ebc915f6ff13a`  
		Last Modified: Thu, 16 Apr 2026 00:50:00 GMT  
		Size: 5.0 MB (4991448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0479e78fc88fdb0aa654abe207c0d938bd3ca7eee3f0ebf4cc9e13ebc2ac3a60`  
		Last Modified: Thu, 16 Apr 2026 00:49:59 GMT  
		Size: 26.1 KB (26068 bytes)  
		MIME: application/vnd.in-toto+json
