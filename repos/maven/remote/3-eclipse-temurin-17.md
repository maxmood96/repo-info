## `maven:3-eclipse-temurin-17`

```console
$ docker pull maven@sha256:254280209db3b7a9c4256c5e71fa03ef3d8157379e141b52eba0a15b76d908f5
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
$ docker pull maven@sha256:8217c6b9a589a7c98769c3d75bfbc2572cde1673731057b7e4f85cae73f6dc62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228957024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e95f40eeea843f84e4718be0fc260913b37318cbf658d5b3c6e119ced54ae13c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ARG RELEASE
# Thu, 30 Jan 2025 14:32:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 Jan 2025 14:32:57 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='d7ba818b1417b67f1f3cdcf7c5fac5e179998469dce7448349f24175eb9b2871';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
# Thu, 27 Mar 2025 16:03:48 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Mar 2025 16:03:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
ARG MAVEN_VERSION=3.9.9
# Thu, 27 Mar 2025 16:03:48 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Mar 2025 16:03:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Mar 2025 16:03:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89e30e15697dc232f3654f9e157d3b28ca771ecac2c0967492c7f89f64b2f4b`  
		Last Modified: Wed, 09 Apr 2025 01:15:53 GMT  
		Size: 23.0 MB (22952728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75915a4c1fbb50377dd6825b9e1cf0b7f02d18043c67736b7b010bc6c2266c6e`  
		Last Modified: Wed, 09 Apr 2025 01:15:56 GMT  
		Size: 144.6 MB (144576259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5282e02cf084d971bf51a730f375efbdae60bb5467dc2a47bd58e3ab58aeec4b`  
		Last Modified: Wed, 09 Apr 2025 01:15:53 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef04ceb2e7f7d5fd3b358054d518735e3c16709b068a6afcd8340a03a88f3ea6`  
		Last Modified: Wed, 09 Apr 2025 01:15:53 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d986f8d1aa9ad4a1c06ab20bc16457972ea9de45a35c6ddb3f9769cdd809d27d`  
		Last Modified: Wed, 09 Apr 2025 02:19:16 GMT  
		Size: 22.5 MB (22536386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f2c20316a5b06ab18381be62cac8da0b39e11621fc7c20a8c0bad8c2acc0e5`  
		Last Modified: Wed, 09 Apr 2025 02:19:16 GMT  
		Size: 9.2 MB (9170200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133596226fb8541ce23ca8843280437823efd824ce467ddc32d843f4872218e0`  
		Last Modified: Wed, 09 Apr 2025 02:19:16 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb0c3bcb0c6cf7476727c01cec3ae5b62a73e8c0f0144d318298d7a9a294ec5`  
		Last Modified: Wed, 09 Apr 2025 02:19:16 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d62f3118f9a4663a1bd537b80219cd59095f8558ecd69d702a3ae955433ecf`  
		Last Modified: Wed, 09 Apr 2025 02:19:17 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17` - unknown; unknown

```console
$ docker pull maven@sha256:77fca4bc834f1345232ef04d67b10a1c562b06ec6f79f624ee018532fdb2dd35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4876950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f5c2152dbab5efe4f318b27612b2180bfa8ac804a40b8eed81e27905305323`

```dockerfile
```

-	Layers:
	-	`sha256:36a583aea5b1239569d2bc5dc8ad3e90eefd56d56ff368b270cc2a302478ac5a`  
		Last Modified: Wed, 09 Apr 2025 02:19:16 GMT  
		Size: 4.9 MB (4852433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54d6d7d17a230354c246bfedbfd6ddede4993c4ec11518b52f8872de9aa5d3b4`  
		Last Modified: Wed, 09 Apr 2025 02:19:16 GMT  
		Size: 24.5 KB (24517 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17` - linux; arm variant v7

```console
$ docker pull maven@sha256:d748d0e912f20920a11a333201756346df9335ac396f864c3ba701611cea67a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.7 MB (226718478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c81a41e00fde4b3f0fda82ac1e1117088a6527449e30e514b638ec9040fcd36`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ARG RELEASE
# Thu, 30 Jan 2025 14:32:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 Jan 2025 14:32:57 GMT
ADD file:0c96eee5fced5e61820b5d18bd668a362ad0e5b3fc04c115f9023e8c295e7000 in / 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='d7ba818b1417b67f1f3cdcf7c5fac5e179998469dce7448349f24175eb9b2871';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
# Thu, 27 Mar 2025 16:03:48 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Mar 2025 16:03:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
ARG MAVEN_VERSION=3.9.9
# Thu, 27 Mar 2025 16:03:48 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Mar 2025 16:03:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Mar 2025 16:03:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:34560582cc6246fb88c88648a1db5ef09d8b65d143991211ba2abe7378aee811`  
		Last Modified: Tue, 08 Apr 2025 11:53:53 GMT  
		Size: 26.8 MB (26837532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52af7d61a91c8618daed9064de3fba2a5c4a12355204f464ec965f8dc71e5832`  
		Last Modified: Wed, 09 Apr 2025 11:50:13 GMT  
		Size: 21.4 MB (21380250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f306df9da12f6f5b6dae4337f293fb2cdeadd7d55c3803bc078388cb9ad572`  
		Last Modified: Wed, 09 Apr 2025 11:50:16 GMT  
		Size: 142.1 MB (142054828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909e67b525bb5507a403ea6b2e756dfb505f620cd146d79e0420db961126a31b`  
		Last Modified: Wed, 09 Apr 2025 11:50:12 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2527476b141f1945a5820a6b5a0981b90521e4344b1f2125e66b24914ab008fe`  
		Last Modified: Wed, 09 Apr 2025 11:50:12 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888645cf2e7b1afc6c22c27844c3941aa11860e63ec01e33e8edbb8ea7a4bfea`  
		Last Modified: Wed, 09 Apr 2025 13:05:55 GMT  
		Size: 27.3 MB (27271850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca9faaba4c65e23a19bd66089a919d59ebb28e8e29ff49a265772a1be5ec6a9`  
		Last Modified: Wed, 09 Apr 2025 13:05:54 GMT  
		Size: 9.2 MB (9170218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:208641b1335d7c717f7288d64984a3c4637d881004d08fd72aab7639eae62efa`  
		Last Modified: Wed, 09 Apr 2025 13:05:54 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2700d3f602446ff513f8b20581ec6ade17496bf5db29255f67a3e6154725788b`  
		Last Modified: Wed, 09 Apr 2025 13:05:54 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0054798b1369942c07da085f32737b898a5d6373421c259006e737a3b2a20bd8`  
		Last Modified: Wed, 09 Apr 2025 13:05:55 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17` - unknown; unknown

```console
$ docker pull maven@sha256:775c372a88c6eecc0c5984ad9c916db0f261b8bf9d99bb3cd4c60653fcd445e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4815709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25fa911014ce010df97fdff32a9404585b0fe89db6c460bd2a86ad8e5129b7f5`

```dockerfile
```

-	Layers:
	-	`sha256:8a7f6360d55946778ad186408946af8589212074d8cf36f6737681f966f74d99`  
		Last Modified: Wed, 09 Apr 2025 13:05:54 GMT  
		Size: 4.8 MB (4791060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05bf915c68f0f32594f8054b9164df5467d05bba94856951d10786b0460a7466`  
		Last Modified: Wed, 09 Apr 2025 13:05:54 GMT  
		Size: 24.6 KB (24649 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:ed7b0cd7bc55999dcca3a941a9f3f449c4693ac0bf4dd049f62572d367e6f81e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228253539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ec6c421939ed519f48170f65b97c5b741250c12fa576e0c22976b618dfdd4b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ARG RELEASE
# Thu, 30 Jan 2025 14:32:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 Jan 2025 14:32:57 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='d7ba818b1417b67f1f3cdcf7c5fac5e179998469dce7448349f24175eb9b2871';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
# Thu, 27 Mar 2025 16:03:48 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Mar 2025 16:03:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
ARG MAVEN_VERSION=3.9.9
# Thu, 27 Mar 2025 16:03:48 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Mar 2025 16:03:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Mar 2025 16:03:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6bb4e2189afd83aaf4ebaa5d182e82cf4839444cb97cb855a17178b08a9012`  
		Last Modified: Wed, 09 Apr 2025 07:05:34 GMT  
		Size: 24.2 MB (24163226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27eae8ebab9bae9078a2efc6360aaf360df25465e4387af24def8cada2271b60`  
		Last Modified: Wed, 09 Apr 2025 07:05:36 GMT  
		Size: 143.5 MB (143461784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a89cb7c086c6517d945cb3cd3868f5956cd73c322e7f2b6e9fa291d63579d66`  
		Last Modified: Wed, 09 Apr 2025 07:05:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67c6f03a28df78a73729402169461858f5e39d3928067ad67dc945c97ad8d24`  
		Last Modified: Wed, 09 Apr 2025 07:05:32 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6664feb50b5fc68f06f00dc412afe8bf7ecf80834da5154a14c05ce89c1a7303`  
		Last Modified: Wed, 09 Apr 2025 17:56:47 GMT  
		Size: 22.6 MB (22607564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387dd720eb7787b9ae8811211120534de762565184c92df7488d482d599437da`  
		Last Modified: Wed, 09 Apr 2025 17:56:46 GMT  
		Size: 9.2 MB (9170204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5950071321f86b1b815eaa7bf094fe3fbcf9f05f44162d0abf03e1593e57c3f`  
		Last Modified: Wed, 09 Apr 2025 17:56:46 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5316c073d62a72e1dab88fe88028833371d93c006fbbb2eea54fee4145d239e`  
		Last Modified: Wed, 09 Apr 2025 17:56:46 GMT  
		Size: 358.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d12517e47d0ef943e9fec9925c6fa5cd15cca08c83a4f9de37845a1cabe513`  
		Last Modified: Wed, 09 Apr 2025 17:56:47 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17` - unknown; unknown

```console
$ docker pull maven@sha256:1c141ff9b674e6d089b15ec3afe0e533ca034d2a0f595635f682470dc1834f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5014677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a886336ebcd81909c2a430ebc43d4e481ad79094ba604fd081d6b4401f48cf`

```dockerfile
```

-	Layers:
	-	`sha256:a44720113fe3d10d14a53dbe6e2e9cc2933674ee5ede5208b5b9e866bf1a62ea`  
		Last Modified: Wed, 09 Apr 2025 17:56:46 GMT  
		Size: 5.0 MB (4989993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6f610215ce7485eedf8d7bfaf037721f2066be3daae3959d793ef19f013c3b3`  
		Last Modified: Wed, 09 Apr 2025 17:56:46 GMT  
		Size: 24.7 KB (24684 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17` - linux; ppc64le

```console
$ docker pull maven@sha256:fa8471a381cafcfc9eb9a9c1b85520574c9da45863dd40e58c45b760fe2806f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.4 MB (238424158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4659f88d62e5252eef19f92bd77bf8cbb98b5404b1be9b13a9b388039d714e0f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ARG RELEASE
# Thu, 30 Jan 2025 14:32:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 Jan 2025 14:32:57 GMT
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='d7ba818b1417b67f1f3cdcf7c5fac5e179998469dce7448349f24175eb9b2871';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
# Thu, 27 Mar 2025 16:03:48 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Mar 2025 16:03:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
ARG MAVEN_VERSION=3.9.9
# Thu, 27 Mar 2025 16:03:48 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Mar 2025 16:03:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Mar 2025 16:03:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7a68004c3056f9c48f386f106b37cd20944506395a2e63cde2f53f63c8cefe`  
		Last Modified: Wed, 09 Apr 2025 04:48:22 GMT  
		Size: 24.1 MB (24101879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0f7493b98cd923092d942aa83a5a10d15ad61bddbccb94dafb9d04a0177263`  
		Last Modified: Wed, 09 Apr 2025 04:48:25 GMT  
		Size: 144.2 MB (144219939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e365f0d6e7ae291b65379b73244eb85c476291819bcf1567ded57eec1eabca9`  
		Last Modified: Wed, 09 Apr 2025 04:48:21 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fd8c4a885d38af30df4ed40cc9d360c15651d3863350d959914c0d2f5a1638`  
		Last Modified: Wed, 09 Apr 2025 04:48:21 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b997f3f4b51e8548618b53418545337baaa44368333ca10ab504a6a3e5abf59`  
		Last Modified: Wed, 09 Apr 2025 13:14:59 GMT  
		Size: 26.6 MB (26587439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a5a140bdadea5ed0b93c4bc14498bb2d0bd6ce84b4bc3036b7b7fbb9fb79e3`  
		Last Modified: Wed, 09 Apr 2025 13:14:58 GMT  
		Size: 9.2 MB (9170227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa78950a0194493f909659786f78fc60f6097fbc0e4a0616649b2e33108bd95`  
		Last Modified: Wed, 09 Apr 2025 13:14:58 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da436f6137f36da978753404f8b3da709aaf17561c176e62f538c98ddd67d778`  
		Last Modified: Wed, 09 Apr 2025 13:14:58 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae4eb51291c74b03f8ff4bc3ee092c8f6a4cc9f6b13c4806e71df179c379d2b`  
		Last Modified: Wed, 09 Apr 2025 13:14:59 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17` - unknown; unknown

```console
$ docker pull maven@sha256:e5f44a3a3e71dfd29de63792938edc123db16c0647a21f022dac4ed083607c5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4927785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83aa70c038487a27658c43a1d5165c3b7cef87bbbd000107b4087c1e91fab3f`

```dockerfile
```

-	Layers:
	-	`sha256:02c2ae1e9e986d6c5f0449b45f9f01d344b72edfb09429d4bb10dc6761c8c3e4`  
		Last Modified: Wed, 09 Apr 2025 13:14:58 GMT  
		Size: 4.9 MB (4903220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97cf03b4e7a152cae4a28c38ac6d6b72b2e4e65f2748b5dd8203530d4dcb9721`  
		Last Modified: Wed, 09 Apr 2025 13:14:57 GMT  
		Size: 24.6 KB (24565 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17` - linux; riscv64

```console
$ docker pull maven@sha256:a3a2102a157b59b0c0d029f2f566e9c182aacc8a070d60f5d2f007c9aa98d768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.7 MB (229691321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384fe72f2daa647746cd434df79f52cb11a7688a8c964369c665c15000142eeb`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ARG RELEASE
# Thu, 30 Jan 2025 14:32:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 Jan 2025 14:32:57 GMT
ADD file:ef7c97f5dd8d665aae899afe52c54f7acaf71fa51e9d7f26e13ed6073141c666 in / 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='d7ba818b1417b67f1f3cdcf7c5fac5e179998469dce7448349f24175eb9b2871';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
# Thu, 27 Mar 2025 16:03:48 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Mar 2025 16:03:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
ARG MAVEN_VERSION=3.9.9
# Thu, 27 Mar 2025 16:03:48 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Mar 2025 16:03:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Mar 2025 16:03:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:ba2f284f7444fb0b78fa804d74c44dee4b397610267539e4a6e9c41ae41e06a1`  
		Last Modified: Tue, 08 Apr 2025 11:54:06 GMT  
		Size: 30.9 MB (30943202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a0a50be59d3ec9789c221036fd2b3d92425c1bfefea86a92dde587c25389798`  
		Last Modified: Wed, 09 Apr 2025 05:32:53 GMT  
		Size: 20.1 MB (20139738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2937aa47d2ee517157e45dbef91c58ed26c8c3b59317dfd543418b35ea26f42`  
		Last Modified: Wed, 09 Apr 2025 05:33:11 GMT  
		Size: 138.4 MB (138437611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9637a34b95f2ee6c1e8efdb8564f954ca0b8d5acccbaa1bac2cce9f7720a0509`  
		Last Modified: Wed, 09 Apr 2025 05:32:49 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d24565919e034fa0cff1432b455b9bfb867ec107c08ebc00489ffbb426127c8`  
		Last Modified: Wed, 09 Apr 2025 05:32:50 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43c1019ddb5a4f6124b87548c071352837876ceaa4a656d68382f2978805b5c`  
		Last Modified: Wed, 09 Apr 2025 10:26:43 GMT  
		Size: 31.0 MB (30996741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621bcf3f0a44a14ace970f1ffd817d3f18d29aab57bd5de5810797c7e095871f`  
		Last Modified: Wed, 09 Apr 2025 10:26:40 GMT  
		Size: 9.2 MB (9170220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb1685030eda9f407cdbaa265eb885a648967a00b7515300e71c5c1891fb5a8`  
		Last Modified: Wed, 09 Apr 2025 10:26:38 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7a4481a660e4a2e2b92d9a1dd2f5f76fa3b2e7e84e9af58088c0d6c4cef3eb`  
		Last Modified: Wed, 09 Apr 2025 10:26:38 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e20eecb5af9017ef9fc7f2ca8ea78d284e8500bffe0fea01d18756c175c05e3`  
		Last Modified: Wed, 09 Apr 2025 10:26:39 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17` - unknown; unknown

```console
$ docker pull maven@sha256:f6fa0a795661ad91ed8243f740f1796d672199656a5c7c8814c30a496051f668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4979227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b204239eeaabddee28a7dc00494d43ce95a4c77a43845f671d24729d93f17d0f`

```dockerfile
```

-	Layers:
	-	`sha256:bce9cfb78348b558c490a53a6e689415632d913af416ec5b10f2a1397bb20efb`  
		Last Modified: Wed, 09 Apr 2025 10:26:39 GMT  
		Size: 5.0 MB (4954662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c75121832f1f2cd6037bc282a414723b3823e2ce88af16c940d37c39347ef1bf`  
		Last Modified: Wed, 09 Apr 2025 10:26:38 GMT  
		Size: 24.6 KB (24565 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17` - linux; s390x

```console
$ docker pull maven@sha256:1db554ba67c09033e13bd9e014c447d9fee5148d79ff0b67f03ee47f0b07db2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.5 MB (219549809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0bd16c3be5976163e214d043b10621db90c3676d944f5633d28a3e225af5e3d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ARG RELEASE
# Thu, 30 Jan 2025 14:32:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 Jan 2025 14:32:57 GMT
ADD file:8f287f40ca940c9bd87c8706751f5f1c5bbd0a83fd75f7d938832b226fdb936d in / 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a3af83983fb94dd7d11b13ba2dba0fb6819dc2caaf87e6937afd22ad4680ae9a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='62efc3e83fc9bcd08db7c4f02977328cb3559a54519078d8337314cf025d19b7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='f43986385403c0f08bd3512c9d11a51c49044a7c8a0a39cf4e2e3731ca0db229';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='f4cb9ee5906a44d110fa381310cd7181d95498d27087d449e7e9b74bddd9def2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='d7ba818b1417b67f1f3cdcf7c5fac5e179998469dce7448349f24175eb9b2871';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3a1d896eb3a737020e5ec95ec3206b1ca36cb365538382289d3fb46d14303648';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
# Thu, 27 Mar 2025 16:03:48 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Mar 2025 16:03:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
ARG MAVEN_VERSION=3.9.9
# Thu, 27 Mar 2025 16:03:48 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Mar 2025 16:03:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Mar 2025 16:03:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e5722f32c6281fa87f1e5f7ebe307864b50aa95a116496a205ce47478bc9b52c`  
		Last Modified: Tue, 08 Apr 2025 11:54:12 GMT  
		Size: 30.0 MB (29956206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb189e60bbcde72b84226fc53fd9434eb3ccfe9d1a1f63d415033557e3d9e60e`  
		Last Modified: Wed, 09 Apr 2025 04:22:02 GMT  
		Size: 22.1 MB (22131159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8e1db2ce9610974294701315fe23bdc8c99763909de6883dd09e5fa6c76593`  
		Last Modified: Wed, 09 Apr 2025 04:22:04 GMT  
		Size: 134.6 MB (134623314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7670e42f01d9c8521521d195c0c2f5fbed4fb8e9d04c79194e30d703227479`  
		Last Modified: Wed, 09 Apr 2025 04:22:01 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852e2a6b31eec10bc097e4d23cd1ea732666e14f22790dbfbb54260e59e02b19`  
		Last Modified: Wed, 09 Apr 2025 04:22:01 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd2e696305e64d0f8d89814d9076ddfcbacc67d844229983ac9f05562f93edb`  
		Last Modified: Wed, 09 Apr 2025 06:44:17 GMT  
		Size: 23.7 MB (23665106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827530d1914a814126b8792e52f117133a8af8c7d7acc80f36f688961f673045`  
		Last Modified: Wed, 09 Apr 2025 06:44:16 GMT  
		Size: 9.2 MB (9170219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd360f58fbb45017d1250ba81f08370f6ea6d6a8a5946677e0e0dd0125489fe`  
		Last Modified: Wed, 09 Apr 2025 06:44:16 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1a581b565a28c5f877447d471d51a8a74cd4cef383e48e7fdcf88ce4ec8e88`  
		Last Modified: Wed, 09 Apr 2025 06:44:16 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a4a1a69372ac1af11378bdd4679728e99049a1458a07e9580c7e5010715d9e`  
		Last Modified: Wed, 09 Apr 2025 06:44:17 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17` - unknown; unknown

```console
$ docker pull maven@sha256:ddd7d758be9dc90c06a867e6263aef693825ff6a1733219646dd1b78aa9abc12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4822758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e3ba4c5a3377a60fcaaef56ca86faa366ffce4ce059d53b215e90700e503019`

```dockerfile
```

-	Layers:
	-	`sha256:5f05cf0a084818c2ced515058ad06652dd2c989f0cab0863149ad43e08b205b4`  
		Last Modified: Wed, 09 Apr 2025 06:44:16 GMT  
		Size: 4.8 MB (4798241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17a8c5e9c5ddcafeccb40d3a3f70bd2e2a8ca511a11f412a95a4f9e418986198`  
		Last Modified: Wed, 09 Apr 2025 06:44:16 GMT  
		Size: 24.5 KB (24517 bytes)  
		MIME: application/vnd.in-toto+json
