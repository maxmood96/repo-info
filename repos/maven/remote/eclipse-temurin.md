## `maven:eclipse-temurin`

```console
$ docker pull maven@sha256:401dc96d1b75109d71d2668f66ca589f50a055b0684607133c95d3ff76d179dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `maven:eclipse-temurin` - linux; amd64

```console
$ docker pull maven@sha256:b437d2ed152e471d453843f9bcdab5e80f25f61ce6ad750f185fb22dbb75fa39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.1 MB (173117431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98d7cbb8ddfd788cba3e19d756b88792905c96460e96083ef9c88aa791a03dc2`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 18:00:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:00:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:00:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 18:00:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:00:16 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Sat, 08 Nov 2025 18:00:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8daf77d1aacffe38c9889689bc224a13557de77559d9a5bb91991e6a298baa0d';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        arm64)          ESUM='5c83b7d2121ed482fd06831a1eba1633dbab818aba6addddf48e075b97e6e9b8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64el)          ESUM='54fdfbfa2c463863bd0c2c9c19901320d25ca533f31daa0bd866c4104af7ce5b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        riscv64)          ESUM='6c11dfbe07ec0eb9e8c23f302dcd57c7e26f3fc7b62e15533c5e6640900e497b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_riscv64_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='1b627ec601998e5450fd1af91ae26a43b4d646403a8938d7efe4dfb2848fd896';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:00:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:00:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:00:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:00:34 GMT
CMD ["jshell"]
# Sat, 08 Nov 2025 19:21:51 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 19:21:51 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 08 Nov 2025 19:21:51 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:21:51 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:21:51 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 08 Nov 2025 19:21:51 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 08 Nov 2025 19:21:51 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 08 Nov 2025 19:21:51 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 08 Nov 2025 19:21:51 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 08 Nov 2025 19:21:51 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 08 Nov 2025 19:21:51 GMT
ARG MAVEN_VERSION=3.9.11
# Sat, 08 Nov 2025 19:21:51 GMT
ARG USER_HOME_DIR=/root
# Sat, 08 Nov 2025 19:21:51 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 08 Nov 2025 19:21:51 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 08 Nov 2025 19:21:51 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48f960b380d0e91fbb0ac7b8af4dd6b5bdc7cd499dd7f68bca3fe0c18b96e76`  
		Last Modified: Sat, 08 Nov 2025 18:01:01 GMT  
		Size: 17.5 MB (17459042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58424d8c3e86de038eb279c8e9b7e9f39ee0e6d1ac133febea8040448315728c`  
		Last Modified: Sat, 08 Nov 2025 18:01:05 GMT  
		Size: 92.2 MB (92168982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b61783688937e5a3c8dd096e5f4f3386e25aa4ca054d50974e3fa8eb07f9e1`  
		Last Modified: Sat, 08 Nov 2025 18:00:58 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff37fca1b55f96d563e8add703a0725a5b2f4551a3cf639afa4de7df7157be48`  
		Last Modified: Sat, 08 Nov 2025 19:22:11 GMT  
		Size: 24.5 MB (24520308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4e25639add12773959b2735f48ea1931d0b5078c822b36b61078ace5052260`  
		Last Modified: Sat, 08 Nov 2025 19:22:11 GMT  
		Size: 9.2 MB (9242603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96bcf7b2759042bb200a1c135844e7c9a2ede7a8832c77904eaeab5c7409492`  
		Last Modified: Sat, 08 Nov 2025 19:22:09 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d462037946b4b6fcd0c2f4b345d57ed8627c22401facbfd4986ee4c85fd5217`  
		Last Modified: Sat, 08 Nov 2025 19:22:09 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:eclipse-temurin` - unknown; unknown

```console
$ docker pull maven@sha256:0fb7bb85acc45a3fc755697905b0d473e8693b256ccce62db6dae7585f4c6cc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4886771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f325cafc89cd38cba7d75d241cdbaea3332d7079c45bd978921d3ab95adab9`

```dockerfile
```

-	Layers:
	-	`sha256:719b1458662c15e939f26c7d0725d2be47527742d6c070b5b118e18250057813`  
		Last Modified: Sat, 08 Nov 2025 21:27:29 GMT  
		Size: 4.9 MB (4863647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:648f4b3a64ec39ef157e4dbadb4e056c9706ee59f0f09c0c1ceb367ce3595cf0`  
		Last Modified: Sat, 08 Nov 2025 21:27:29 GMT  
		Size: 23.1 KB (23124 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:eclipse-temurin` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:f927cbb3e166e7a5bfd98dd3f73f1cb656449af75b28e0e6e47da15872308ecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172550287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1a8c4a20bd2c13b1d2eacc44ae8982a6a056d649fb3c69f8d907cb548372328`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:59:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:59:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:59:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:59:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:59:48 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Sat, 08 Nov 2025 18:00:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8daf77d1aacffe38c9889689bc224a13557de77559d9a5bb91991e6a298baa0d';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        arm64)          ESUM='5c83b7d2121ed482fd06831a1eba1633dbab818aba6addddf48e075b97e6e9b8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64el)          ESUM='54fdfbfa2c463863bd0c2c9c19901320d25ca533f31daa0bd866c4104af7ce5b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        riscv64)          ESUM='6c11dfbe07ec0eb9e8c23f302dcd57c7e26f3fc7b62e15533c5e6640900e497b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_riscv64_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='1b627ec601998e5450fd1af91ae26a43b4d646403a8938d7efe4dfb2848fd896';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:00:08 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:00:08 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:00:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:00:08 GMT
CMD ["jshell"]
# Sat, 08 Nov 2025 19:21:33 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 19:21:33 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 08 Nov 2025 19:21:33 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:21:33 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:21:33 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 08 Nov 2025 19:21:33 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 08 Nov 2025 19:21:33 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 08 Nov 2025 19:21:33 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 08 Nov 2025 19:21:33 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 08 Nov 2025 19:21:33 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 08 Nov 2025 19:21:33 GMT
ARG MAVEN_VERSION=3.9.11
# Sat, 08 Nov 2025 19:21:33 GMT
ARG USER_HOME_DIR=/root
# Sat, 08 Nov 2025 19:21:33 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 08 Nov 2025 19:21:33 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 08 Nov 2025 19:21:33 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a316c91d5a75591ae187745caf6d54121af46048fac51111ef95d54d9676424f`  
		Last Modified: Sat, 08 Nov 2025 18:00:35 GMT  
		Size: 18.6 MB (18649062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e9ee746c90730e83ae70a0652c862fbfb1961dc4ddb579e488925476a2957f`  
		Last Modified: Sat, 08 Nov 2025 18:00:48 GMT  
		Size: 91.2 MB (91182725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c251c454a3653110f677e97bf2a41fe4d956f424c20d8a168a6b8b56f998c1`  
		Last Modified: Sat, 08 Nov 2025 18:00:33 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510e2810d571a4c99e0c8ef6d1de3b345486ad9278adde9bfa76a41f463d75b6`  
		Last Modified: Sat, 08 Nov 2025 19:21:53 GMT  
		Size: 24.6 MB (24610858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337bccd479ab3bf4e54ab5ff9208deb984bd167b6cac7ae8c65b5f30d342b486`  
		Last Modified: Sat, 08 Nov 2025 19:21:52 GMT  
		Size: 9.2 MB (9242577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b794e5a123cafb0677f37cade478d76259ec52509e94a7348804eefe25f32e6`  
		Last Modified: Sat, 08 Nov 2025 19:21:51 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472f5b7a004b9f75d928dc2207dbba1443ffdcec5e96f7f5746bd5ad7e216d3d`  
		Last Modified: Sat, 08 Nov 2025 19:21:51 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:eclipse-temurin` - unknown; unknown

```console
$ docker pull maven@sha256:23f9cd636f4a77b59ed03b959dc38402cae8800f44711efe9817612dec57cdf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5024722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9082c8e1838d60a136d237338186969cefa498021a5b13f2777e2eebff6913`

```dockerfile
```

-	Layers:
	-	`sha256:aa7ac2db9005d0250ed77fe3eeee03690d6acc8675580f6aa62f041d840d041e`  
		Last Modified: Sat, 08 Nov 2025 21:27:34 GMT  
		Size: 5.0 MB (5001333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f42d96ea176cf74f1dc7f23c7dfe16ae39bdaa01e47847d622176d424303858d`  
		Last Modified: Sat, 08 Nov 2025 21:27:35 GMT  
		Size: 23.4 KB (23389 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:eclipse-temurin` - linux; ppc64le

```console
$ docker pull maven@sha256:8aa64732682b9021d15a51265552ba77b0e0d96d5f993196183eee4020ab8285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.7 MB (181663924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:858b3ecf934c37e24e8046f8ab179edc2e010fdef71adeaa1d552a401e911c9e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 25 Sep 2025 19:59:06 GMT
ARG RELEASE
# Thu, 25 Sep 2025 19:59:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 19:59:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 19:59:06 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 25 Sep 2025 19:59:06 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Thu, 25 Sep 2025 19:59:06 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Sep 2025 19:59:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Sep 2025 19:59:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_VERSION=jdk-25+36
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='ee04de95ab9da7287d40bd2173076ecc2a6dd662f007bedfc6eb0380c0ef90e8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_x64_linux_hotspot_25_36.tar.gz';          ;;        arm64)          ESUM='95716d04bdfc8b10c94f4448ea8d57a3ba872d98b53c752e4c6b48f1c95bc582';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_aarch64_linux_hotspot_25_36.tar.gz';          ;;        ppc64el)          ESUM='b060bb12b3a192a0599f03ebb9495492f78c48cb61e291e336a8b00e7798ffb0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_ppc64le_linux_hotspot_25_36.tar.gz';          ;;        riscv64)          ESUM='3fc35759502b620f010a9cd2b3da8454f8a49a156ceaebb00de1fd8335682d40';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_riscv64_linux_hotspot_25_36.tar.gz';          ;;        s390x)          ESUM='3e476e40f920ccfb1915d200bc7a1fba9d68c4adcc0358c5968d15613690b915';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_s390x_linux_hotspot_25_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Sep 2025 19:59:06 GMT
CMD ["jshell"]
# Fri, 26 Sep 2025 11:21:48 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Sep 2025 11:21:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 26 Sep 2025 11:21:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 26 Sep 2025 11:21:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 26 Sep 2025 11:21:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 26 Sep 2025 11:21:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 26 Sep 2025 11:21:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 26 Sep 2025 11:21:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 26 Sep 2025 11:21:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 26 Sep 2025 11:21:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 26 Sep 2025 11:21:48 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 26 Sep 2025 11:21:48 GMT
ARG USER_HOME_DIR=/root
# Fri, 26 Sep 2025 11:21:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 26 Sep 2025 11:21:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 26 Sep 2025 11:21:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3abef86328361e6a8fca4e97e2725838182e487a709b1cd23bd0d865c03378c`  
		Last Modified: Thu, 09 Oct 2025 21:20:21 GMT  
		Size: 17.3 MB (17340059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa97d42bf6d5c3b33aceb7ed3328b51ee36d1b9c1e84af0c37cc4e26510a06c6`  
		Last Modified: Thu, 09 Oct 2025 21:20:35 GMT  
		Size: 91.7 MB (91734228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a1d4febf2b7aa769213c87b6ec5db4c41302b34879891f6660fe2e9a11f5cb`  
		Last Modified: Thu, 09 Oct 2025 21:20:20 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f00f55dc6a99f281f8a2ae14195b872c72bef1e8bc3cb89d439d66a62aa93f`  
		Last Modified: Fri, 10 Oct 2025 09:28:27 GMT  
		Size: 29.0 MB (29040187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce292721038cbb5bf41a14c2ff25aa3aa30e181012f57d526f569780e573409f`  
		Last Modified: Fri, 10 Oct 2025 09:28:24 GMT  
		Size: 9.2 MB (9242575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753c6d639881a7004bdaccfae59803a46b26e00310347647b3c324421eed8f09`  
		Last Modified: Fri, 10 Oct 2025 09:28:24 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ad4bc4643ca03c45053b1ebf05a688f37967267e5ed7b1a20fbae9c1496864`  
		Last Modified: Fri, 10 Oct 2025 09:28:24 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:eclipse-temurin` - unknown; unknown

```console
$ docker pull maven@sha256:431dc807ba691ceba86e382e215c64fb3b2cf92ff33545844350e6f696e3b30a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4938799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d6cb5d3a316b06bd1e6ad9e76516cb26f2f809d36745533ea4010417820e4c2`

```dockerfile
```

-	Layers:
	-	`sha256:a28315b5219563525a028dbf12f3917bc9af918dc8c6574cae8e723470d5567b`  
		Last Modified: Fri, 10 Oct 2025 11:27:26 GMT  
		Size: 4.9 MB (4915522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4289412bb88ab07ae7828db5972dc0d0ccf79502ee4745296de7d7adc17953eb`  
		Last Modified: Fri, 10 Oct 2025 11:27:27 GMT  
		Size: 23.3 KB (23277 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:eclipse-temurin` - linux; riscv64

```console
$ docker pull maven@sha256:e6095faeac0ff1c7b8464eda15d4c52c0ad4c39b22d5e3b1e7cd3afef100d69a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.0 MB (178046625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9525289c0e0fda9bdabbb4a9fc3847f26325266e7225af626ad974f1fad6b8`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 25 Sep 2025 19:59:06 GMT
ARG RELEASE
# Thu, 25 Sep 2025 19:59:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 19:59:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 19:59:06 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 25 Sep 2025 19:59:06 GMT
ADD file:857dc87fbafae31881cff8c69aed267a033f5df226dd351ee89de918ad5678ce in / 
# Thu, 25 Sep 2025 19:59:06 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Sep 2025 19:59:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Sep 2025 19:59:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_VERSION=jdk-25+36
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='ee04de95ab9da7287d40bd2173076ecc2a6dd662f007bedfc6eb0380c0ef90e8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_x64_linux_hotspot_25_36.tar.gz';          ;;        arm64)          ESUM='95716d04bdfc8b10c94f4448ea8d57a3ba872d98b53c752e4c6b48f1c95bc582';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_aarch64_linux_hotspot_25_36.tar.gz';          ;;        ppc64el)          ESUM='b060bb12b3a192a0599f03ebb9495492f78c48cb61e291e336a8b00e7798ffb0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_ppc64le_linux_hotspot_25_36.tar.gz';          ;;        riscv64)          ESUM='3fc35759502b620f010a9cd2b3da8454f8a49a156ceaebb00de1fd8335682d40';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_riscv64_linux_hotspot_25_36.tar.gz';          ;;        s390x)          ESUM='3e476e40f920ccfb1915d200bc7a1fba9d68c4adcc0358c5968d15613690b915';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_s390x_linux_hotspot_25_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Sep 2025 19:59:06 GMT
CMD ["jshell"]
# Fri, 26 Sep 2025 11:21:48 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Sep 2025 11:21:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 26 Sep 2025 11:21:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 26 Sep 2025 11:21:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 26 Sep 2025 11:21:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 26 Sep 2025 11:21:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 26 Sep 2025 11:21:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 26 Sep 2025 11:21:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 26 Sep 2025 11:21:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 26 Sep 2025 11:21:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 26 Sep 2025 11:21:48 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 26 Sep 2025 11:21:48 GMT
ARG USER_HOME_DIR=/root
# Fri, 26 Sep 2025 11:21:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 26 Sep 2025 11:21:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 26 Sep 2025 11:21:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:ff47a256ba51b80e9880bc96be4ac2f094c47e0fcd7eec71bab85787cfa54b8b`  
		Last Modified: Mon, 13 Oct 2025 04:10:18 GMT  
		Size: 31.0 MB (30951381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5cec5b487e18a19c40c1e960973c17f029e6b9c8aa5730824281240a3f8086`  
		Last Modified: Wed, 15 Oct 2025 07:05:50 GMT  
		Size: 13.8 MB (13842473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea2ed334f0d37e197c8fd587d56a032c08c3ad111ced1ca412d18eb5db538d1`  
		Last Modified: Wed, 15 Oct 2025 07:06:02 GMT  
		Size: 90.9 MB (90882461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfb6b3c494bb4b635907a18100b50663f9c45b28ed5dc11f9e9600f6b5bd9e2`  
		Last Modified: Wed, 15 Oct 2025 07:05:49 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae5574906f79b5436f3c54cb97ed3dfaf59d090f101fd3940312bbb83f42019`  
		Last Modified: Thu, 16 Oct 2025 12:04:50 GMT  
		Size: 33.1 MB (33124380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a143214c504eb5e92b9d26807817b988a2c5700f0bfa73153126186a38162d2`  
		Last Modified: Thu, 16 Oct 2025 12:04:49 GMT  
		Size: 9.2 MB (9242578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f842263e9672fcea3a2fbd4c7e6a9cc31cc1ab7efce93d4f8a617d4275e705f2`  
		Last Modified: Thu, 16 Oct 2025 12:04:47 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eec4346cd50d83632d8299b3cf4e6c5decf3852da2eaceca5b8b61e128fb898`  
		Last Modified: Thu, 16 Oct 2025 12:04:47 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:eclipse-temurin` - unknown; unknown

```console
$ docker pull maven@sha256:8416b8f5e8d1c15c3423de4dac50723480f861509ff80929d30a560573feb23e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4990579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09ff548b143ba12028519d86619e477102e723fe3afe351c5fef12c4ba986879`

```dockerfile
```

-	Layers:
	-	`sha256:a8188741376955aaf1c9ddada03a90d740689bb9626031f6eca43b155e5d27f0`  
		Last Modified: Thu, 16 Oct 2025 14:27:32 GMT  
		Size: 5.0 MB (4967302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80947840a670b768679ff6030ba8b538496d9d9efa24f05fc7757c0c21912de3`  
		Last Modified: Thu, 16 Oct 2025 14:27:33 GMT  
		Size: 23.3 KB (23277 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:eclipse-temurin` - linux; s390x

```console
$ docker pull maven@sha256:6528360505d7491c1e8e79473f44e18d91738d77eb52211087919dc7518dd91c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169540429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c917ed50aa940d92a5fe5fc67cc2e2b3947278398fcd6349eb12e341fe5f6fe`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:05 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:06 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:07 GMT
ADD file:1c921a1d937949898d3d4ba499ce8d41425fe6dd2c8fdbcddd0070f2699f05b2 in / 
# Wed, 01 Oct 2025 13:02:07 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 18:15:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:15:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:15:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 18:15:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:15:54 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Sat, 08 Nov 2025 18:16:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='8daf77d1aacffe38c9889689bc224a13557de77559d9a5bb91991e6a298baa0d';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        arm64)          ESUM='5c83b7d2121ed482fd06831a1eba1633dbab818aba6addddf48e075b97e6e9b8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64el)          ESUM='54fdfbfa2c463863bd0c2c9c19901320d25ca533f31daa0bd866c4104af7ce5b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        riscv64)          ESUM='6c11dfbe07ec0eb9e8c23f302dcd57c7e26f3fc7b62e15533c5e6640900e497b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_riscv64_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='1b627ec601998e5450fd1af91ae26a43b4d646403a8938d7efe4dfb2848fd896';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:16:11 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:16:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:16:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:16:11 GMT
CMD ["jshell"]
# Sat, 08 Nov 2025 21:06:27 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 21:06:27 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 08 Nov 2025 21:06:27 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 21:06:27 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 21:06:27 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 08 Nov 2025 21:06:27 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 08 Nov 2025 21:06:27 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 08 Nov 2025 21:06:27 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 08 Nov 2025 21:06:28 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 08 Nov 2025 21:06:28 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 08 Nov 2025 21:06:28 GMT
ARG MAVEN_VERSION=3.9.11
# Sat, 08 Nov 2025 21:06:28 GMT
ARG USER_HOME_DIR=/root
# Sat, 08 Nov 2025 21:06:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 08 Nov 2025 21:06:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 08 Nov 2025 21:06:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:67735b72a65d308a2c2c9505d0d6e8419b7f2654a16cbd56963d88e01202d507`  
		Last Modified: Wed, 01 Oct 2025 15:43:10 GMT  
		Size: 29.9 MB (29906151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198889c35755625a18c85ae4f589aa70dbc1cf34f173f74b40ade94637489345`  
		Last Modified: Sat, 08 Nov 2025 18:16:41 GMT  
		Size: 16.3 MB (16311011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7af96f0bcccc437046c0e7d9abc76730385b1b9577fd68e71376d35605fdf4b`  
		Last Modified: Sat, 08 Nov 2025 18:16:56 GMT  
		Size: 88.3 MB (88345848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f648e871bc26c47ced9815518316545060aa9b16f498623100fdf79f5ce382`  
		Last Modified: Sat, 08 Nov 2025 18:16:42 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861a4db5f4fc6774796ed846d34a6e4a1d234eb40bbcad4b146ba9082df4b1ef`  
		Last Modified: Sat, 08 Nov 2025 21:06:57 GMT  
		Size: 25.7 MB (25731491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c0d4f291b86b20652694d4535c1af64c6342ee8a26ca6abbe68164ea53744f`  
		Last Modified: Sat, 08 Nov 2025 21:06:54 GMT  
		Size: 9.2 MB (9242574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92fd4d4de4aa3537df01bb6cf67275ff45c7ce3922e501f8e43c4bc95005d2e5`  
		Last Modified: Sat, 08 Nov 2025 21:06:52 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e5a85f46aa5d063c6a00a85d259b0747bab9eb06a2bd6c29f038e6d94bca4d`  
		Last Modified: Sat, 08 Nov 2025 21:06:52 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:eclipse-temurin` - unknown; unknown

```console
$ docker pull maven@sha256:f48743b2a934dc73e5ab7e10d14ddf404a602f3f214497d1143a5b83a4d9a002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4834724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64efd1dd278c6f9a4bf12efa22a20f680d426ef916cf26cd9f5dac75a3b0be38`

```dockerfile
```

-	Layers:
	-	`sha256:967a9da4fc4fdea91676715a946c5ffc2b72e757dc4983771e1d2cd4b5e39c37`  
		Last Modified: Sat, 08 Nov 2025 21:27:47 GMT  
		Size: 4.8 MB (4811601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f1e0b14d0452408b928a15ad590fc919be6dd429c4ffcf4445039cf3eb54d8a`  
		Last Modified: Sat, 08 Nov 2025 21:27:48 GMT  
		Size: 23.1 KB (23123 bytes)  
		MIME: application/vnd.in-toto+json
