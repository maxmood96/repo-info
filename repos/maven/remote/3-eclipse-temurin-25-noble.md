## `maven:3-eclipse-temurin-25-noble`

```console
$ docker pull maven@sha256:65e73dbed6813dadbf1b20b98f7f4d6bab01a0e3e7a1b027f709dd6d2839d735
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

### `maven:3-eclipse-temurin-25-noble` - linux; amd64

```console
$ docker pull maven@sha256:ac0d69a365a9f4e7bb882b5a82a07a99b14d2ce1b30e9e816bdd3c201c6f73ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.1 MB (173115208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daad458da47d2d6ddb865bc7e7c076944f04e78078acf8d2747bd2deee86ca83`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751f17092206e57f1a1a273a304c3391c6b5e525e3b827f8f98aa95c6617ee0d`  
		Last Modified: Thu, 09 Oct 2025 21:14:36 GMT  
		Size: 17.5 MB (17458339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5f352694d8627292c2cf79e310b418dcabbc90dc635644e82f51bd9a986132`  
		Last Modified: Thu, 09 Oct 2025 21:14:38 GMT  
		Size: 92.2 MB (92168040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd412807b1d854d10ba7ed722cb2db269bdae28795b00a69549388cab7b9ea2`  
		Last Modified: Thu, 09 Oct 2025 21:14:34 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06281d3d4057bce7915359c5b1e8e879edcb2ca6e37558020b004c3b6217cffa`  
		Last Modified: Thu, 09 Oct 2025 22:50:05 GMT  
		Size: 24.5 MB (24519748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d1b346bb4d90275835afa4ff8cf21b951d026a831f54a91630bfcfb03cd207`  
		Last Modified: Thu, 09 Oct 2025 22:50:01 GMT  
		Size: 9.2 MB (9242590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7404dfe70a4e611d0c2fc17019201eae9073bba7728cd4826ad57f5b1d91f8`  
		Last Modified: Thu, 09 Oct 2025 22:50:01 GMT  
		Size: 845.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b9fce27afe99f62bd8f0d908c5983b84ee6c2becdce434344186716fa03660`  
		Last Modified: Thu, 09 Oct 2025 22:50:01 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-25-noble` - unknown; unknown

```console
$ docker pull maven@sha256:30944168058034ac211bbbbe9f62cdd55b8b53b0d6d4790e0df3042adbc1eaad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4886794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c6f44535e176e5a584c307de558791c7b6fbe2c837d424c5f7b40fc078d594`

```dockerfile
```

-	Layers:
	-	`sha256:2eba92df60cf40e426efcfac06329e31222d53d231ecd384b72e6825a641bcdf`  
		Last Modified: Fri, 10 Oct 2025 05:27:24 GMT  
		Size: 4.9 MB (4863633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af3ff69b3291e6d73ea4bfedc8ac3a97cfc794b974d2c8b5ec4c3fb343ae6a4d`  
		Last Modified: Fri, 10 Oct 2025 05:27:25 GMT  
		Size: 23.2 KB (23161 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-25-noble` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:0fcc49f3a1269eeef1ea8a901185a7a2e7902f75cbb3a0c1c4d008ae9c6cbbe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.5 MB (172546223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60e77b46f87bd8d676f9e6f4ed935edb711d6be573f62dc0240b6bf653ea1e98`
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
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
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
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f534f212b81280f9bb38024333dd966c72c7b4f9e4e38e47ce52ac0db5a8630`  
		Last Modified: Thu, 09 Oct 2025 21:16:05 GMT  
		Size: 18.7 MB (18652075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a019a5e915bc01822b117e3ff7b8cb7467c0c157494660a51b69c9ecea351a3`  
		Last Modified: Thu, 09 Oct 2025 21:16:16 GMT  
		Size: 91.2 MB (91175671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c052dc0d5069685926780974e4c16a48da1ad8e760614f991e98d260844156d`  
		Last Modified: Thu, 09 Oct 2025 21:14:59 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e8b6129ab61246d972ccd1e355e0387c3ecc89a966a045a31d92b0b8776e7a`  
		Last Modified: Thu, 09 Oct 2025 22:54:05 GMT  
		Size: 24.6 MB (24610828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3893a4867c21a0a7ad644c1aeedce4c755c0d43d7f71e33d43c79056f4f0bdd`  
		Last Modified: Thu, 09 Oct 2025 22:54:04 GMT  
		Size: 9.2 MB (9242585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23a277884049caff84c02ca2c6d2922953d19a8012fa6263ff22f863ea79ab4`  
		Last Modified: Thu, 09 Oct 2025 22:54:03 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1c15b80e2e4903dc90e63d15069dede962c4735f70b555e442d7aea633d107`  
		Last Modified: Thu, 09 Oct 2025 22:54:03 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-25-noble` - unknown; unknown

```console
$ docker pull maven@sha256:9454dcc1e951e69dddf04823bc510b58b54a5ca94afc9c5651bce4ec66d52add
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5024745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48364fa2a4cae5acb47c388065edabb6ebdb11ce0c5f7827f812baf262c5383e`

```dockerfile
```

-	Layers:
	-	`sha256:01c0cb8854bb483951138e0701cc9e8fca2d861751865f423f7b05fc18657c9d`  
		Last Modified: Fri, 10 Oct 2025 05:27:30 GMT  
		Size: 5.0 MB (5001319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9595f7f3fa190987ed6a8374743b4e7868ca2e866dbbdc1210351091dd96e751`  
		Last Modified: Fri, 10 Oct 2025 05:27:31 GMT  
		Size: 23.4 KB (23426 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-25-noble` - linux; ppc64le

```console
$ docker pull maven@sha256:60fe40a5f929d8b0df945f1501c91a8b9bdbb766744452cea4a20c48ec8d3094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.3 MB (184284287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:166211ec3f1d814794be1ce4f2f1fdb249eaefceaebd22bc67cc9fa1a5c59ec8`
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
ADD file:c654664ccaf1c501c787c924fddcfab7f9cdc324325d45748f97ee6d5ad63cec in / 
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
	-	`sha256:15a6b79c4fd2f3417787ba4c0a8161183cf898454880102c719eb0c91671c218`  
		Last Modified: Tue, 30 Sep 2025 17:28:16 GMT  
		Size: 34.3 MB (34303547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef3087348d873fc22dc527e45fa54c984032543f2f1f33aa78865409275e9e7`  
		Last Modified: Thu, 02 Oct 2025 01:43:05 GMT  
		Size: 20.0 MB (19959869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df90dfa18ef28f4c6576c88e6f03a4226c79dd798d044233107fbc60880fff6f`  
		Last Modified: Thu, 02 Oct 2025 03:22:27 GMT  
		Size: 91.7 MB (91734544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c98e49febfac2808c20d9baf1030602882fe657bb52e0e09adff76a95489ef`  
		Last Modified: Thu, 02 Oct 2025 01:43:03 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e37b1d34676a07f9a87fb9389eafc11fda0f291793cf1a5d8c42f3658e7416`  
		Last Modified: Thu, 02 Oct 2025 15:39:14 GMT  
		Size: 29.0 MB (29040389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4000f60fbd1e31ddb4bab3709b9d9ca853a0ca5fbdc8de30a65861971038d177`  
		Last Modified: Thu, 02 Oct 2025 15:39:07 GMT  
		Size: 9.2 MB (9242585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173b09486e15e8218156e5934f1e172d65bc81f84c70012829de99c205ba92f4`  
		Last Modified: Thu, 02 Oct 2025 15:39:03 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25afd6bb113c6bcb3377f6782080808fe940248ef5dae08852939960c563661`  
		Last Modified: Thu, 02 Oct 2025 15:39:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-25-noble` - unknown; unknown

```console
$ docker pull maven@sha256:6e7d9feeeeb1d5cbc50bd6e06c1cee2a9a7c644d119f75b59a7b8b744a0dd769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4938799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1caeadda88df2d667e36937e2a3c2e9536e4a7bb3db79f5e04f62d3fde72b92`

```dockerfile
```

-	Layers:
	-	`sha256:fb0a7c0871fa2a8b94d07b9e9f7c8cc5eea7434e7b49d6634f0090cf80f108b7`  
		Last Modified: Thu, 02 Oct 2025 17:27:27 GMT  
		Size: 4.9 MB (4915522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac993ef5286bdd5e50e6801a5aebfdcb796c3bdc4c6e7d5a911c7edb9bc90c39`  
		Last Modified: Thu, 02 Oct 2025 17:27:28 GMT  
		Size: 23.3 KB (23277 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-25-noble` - linux; riscv64

```console
$ docker pull maven@sha256:664cdf46aa903f7a6d06a6e88086c4584cdcd1a513a2196d1321e03d75838378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.2 MB (180156906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd899928394297496fe1d3cb56ef6447f3f3ad3c4ef0922ed83f0ebe5c71f55`
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
ADD file:13e2355f84c9f5f1ba6aa2fa1db4359cbe23312f7b2905fc8b976899a09fdfef in / 
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
	-	`sha256:2d699e6bd7ed3cc40f40b8118f763dc4303b0e97b911de163cabf78f19b5d434`  
		Last Modified: Thu, 02 Oct 2025 23:21:18 GMT  
		Size: 31.0 MB (30950446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681226ecf08b5ed0c7a2ddb14b0aa1fa5dd9f08ee2ddf669cc5331ece21ce750`  
		Last Modified: Fri, 03 Oct 2025 19:54:08 GMT  
		Size: 16.0 MB (15954979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cca09b62c92482cb6874f3bf24b3ee869acb89243f8e34c1e3d93064fb6662e`  
		Last Modified: Sat, 04 Oct 2025 01:08:28 GMT  
		Size: 90.9 MB (90881850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f03e987e085b9325bfc3fbe514c2b59872211194c96856a70cd7ade9ff7c816`  
		Last Modified: Fri, 03 Oct 2025 19:54:04 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d92d61f5d4f25988023db94a38a419b2a19f2ff47df5021dd539540ef8cdd0`  
		Last Modified: Tue, 07 Oct 2025 13:00:25 GMT  
		Size: 33.1 MB (33123702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc798b045918cf6d152c8fdfa8d558091723d26ce3831e379f7300b6b87b3d07`  
		Last Modified: Tue, 07 Oct 2025 13:00:23 GMT  
		Size: 9.2 MB (9242577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef8fe793eabb2632e5a0b69111afbddd1683a00910467815afd0290a6881b58`  
		Last Modified: Tue, 07 Oct 2025 13:00:22 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4c6a5e93a168297ad6bd89b60511ecf83dbf0fd9560659fe396e17b0b57619`  
		Last Modified: Tue, 07 Oct 2025 13:00:22 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-25-noble` - unknown; unknown

```console
$ docker pull maven@sha256:5051970379036609fd48e322eb93466950dcc959d72d35dcea9582a8d8ef6b96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4990579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5966065ebc351526a59f352cee568c451410112227496aa85f577b96d9ab4004`

```dockerfile
```

-	Layers:
	-	`sha256:0cf6dc73bd0b025187992cc23a0ecbf7bd1ec9cdd7ee64714b714abd6d1dedb3`  
		Last Modified: Tue, 07 Oct 2025 14:27:35 GMT  
		Size: 5.0 MB (4967302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:998eb5d6189585608badad4bfc1be6b2ccd038265ccb668969d39e5f9acd63c5`  
		Last Modified: Tue, 07 Oct 2025 14:27:36 GMT  
		Size: 23.3 KB (23277 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-25-noble` - linux; s390x

```console
$ docker pull maven@sha256:1d18a2305a92596efe7475692622cf11c56c8239050c42bfc8c06b05992a82a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.6 MB (171621064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:401da5d9e5f23800c96a645932b0712ce7535b226c67ce785b64643921b862d5`
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
ADD file:2df9e8bc7cd2e879b1bb1d4b43960e570cf8bf039e9c92e1b3599d2ec12b6674 in / 
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
	-	`sha256:e9a7df0c6e08fd0434347bd07ecdade7cc5d006c086084ec4347cd24546ee1a5`  
		Last Modified: Tue, 30 Sep 2025 17:14:38 GMT  
		Size: 29.9 MB (29906146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64786075c80c5cf3380d304f4b2eb63f2b70da7a2d07030cae11b04b31f8571`  
		Last Modified: Thu, 02 Oct 2025 01:27:00 GMT  
		Size: 18.4 MB (18405738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9385a51ae5a37291a486c9fa1fb53c54c75f5877066d8de5670915ef840578e1`  
		Last Modified: Thu, 02 Oct 2025 01:27:10 GMT  
		Size: 88.3 MB (88331722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc83c2d261e2cfee32ec6e7652d90c98b920b8ef0676bf7163ff24278e93e6ba`  
		Last Modified: Thu, 02 Oct 2025 01:26:56 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550d8fc8db457e07be662a2edaf7facfd130f4fa348528585ab08cd0bf7521bc`  
		Last Modified: Thu, 02 Oct 2025 08:00:30 GMT  
		Size: 25.7 MB (25731528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337037f3d709d6f9308b501de7d68844704e7e31e4e412f090e09fca05419a4c`  
		Last Modified: Thu, 02 Oct 2025 08:00:30 GMT  
		Size: 9.2 MB (9242582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea5a6cd27aec5a2e79fbb2e3ac678f990f6f7eee2a90108a731409be6207f0e`  
		Last Modified: Thu, 02 Oct 2025 08:00:29 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9999dda90bf1574a4658e607e95df8e2ec9f866251905c6b6a527108aff648a9`  
		Last Modified: Thu, 02 Oct 2025 08:00:29 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-25-noble` - unknown; unknown

```console
$ docker pull maven@sha256:b95d95aedb379b6744d619524c3f702e2f82b29afe79263ca770a7c2e92236cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4834748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc0abf0de8e250beecee0ad3676cd2cb88ecbce1b120380db5b9efeab4224b5`

```dockerfile
```

-	Layers:
	-	`sha256:1b56ccab92984c4f99e7d6b22c5fc157ab0893c4f07fcca976ebf688c1b28293`  
		Last Modified: Thu, 02 Oct 2025 08:28:07 GMT  
		Size: 4.8 MB (4811587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc3f8a377a2145fe94b548a4ec76eb8967118ccde7018f13e598819b5f16d8f6`  
		Last Modified: Thu, 02 Oct 2025 08:28:08 GMT  
		Size: 23.2 KB (23161 bytes)  
		MIME: application/vnd.in-toto+json
