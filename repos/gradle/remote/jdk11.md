## `gradle:jdk11`

```console
$ docker pull gradle@sha256:d8ef6604ef9969bb48b260e828fabb3a5e72867cf8c4463bcd0f3c3790060ba7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `gradle:jdk11` - linux; amd64

```console
$ docker pull gradle@sha256:af97cc8d5e2ceb4091c98564c8592c97ab45ee0544be84354ca387784cab9130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.5 MB (378529301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:921444103ecc0f9950011a565fe50c0173fd1636c2cbb037ce400fbe62922cb8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 01 Jun 2024 15:03:05 GMT
ARG RELEASE
# Sat, 01 Jun 2024 15:03:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Jun 2024 15:03:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Jun 2024 15:03:05 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 01 Jun 2024 15:03:05 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Sat, 01 Jun 2024 15:03:05 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e00476a7be3c4adfa9b3d55d30768967fd246a8352e518894e183fa444d4d3ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='23e47ea7a3015be3240f21185fd902adebdcf76530757c9b482c7eb5bd3417c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='8077edc07a57d846c3d11286a7caf05ed6ca6d6c1234bf0e03611f18e187f075';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f56068bb64c6bf858894f75c2bc261f54db32932422eb07527f36ae40046e9a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf06c3e41acfaeda77112ac04f5a711cafe9fa9ac04dff758696fe7e8d66a0ea';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Sat, 01 Jun 2024 15:03:05 GMT
CMD ["gradle"]
# Sat, 01 Jun 2024 15:03:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 01 Jun 2024 15:03:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 01 Jun 2024 15:03:05 GMT
WORKDIR /home/gradle
# Sat, 01 Jun 2024 15:03:05 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
ENV GRADLE_VERSION=8.8
# Sat, 01 Jun 2024 15:03:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
# Sat, 01 Jun 2024 15:03:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
USER gradle
# Sat, 01 Jun 2024 15:03:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
USER root
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab7f202453ac8b8def634e399240ab2bd7247e2f125fbddd2dbaaa8fa4ce555`  
		Last Modified: Wed, 05 Jun 2024 04:58:06 GMT  
		Size: 12.9 MB (12904817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69865e71a9cfb01a2ad202d7db1341b49a92b426e46706bad26149092c0acb33`  
		Last Modified: Wed, 05 Jun 2024 04:59:26 GMT  
		Size: 145.5 MB (145509176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02b970a522c41c71d86ecd9b628a5bb6338994f4ff33b187bbe317968966b5c`  
		Last Modified: Wed, 05 Jun 2024 04:59:15 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd1135e66d0e77a22a5893e962088e398b99d9b3f0286206707bbb76aa75be1`  
		Last Modified: Wed, 05 Jun 2024 04:59:15 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6d289623c1d721ffcc24fdd75d324684da528b2f981db380ce47bfb20a0c9c`  
		Last Modified: Wed, 05 Jun 2024 06:12:36 GMT  
		Size: 4.3 KB (4306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2bb4b2719df70fdb96fa51f7bee655e47a94ac68a914ec1f1a0db1970f3639`  
		Last Modified: Wed, 05 Jun 2024 06:12:37 GMT  
		Size: 51.6 MB (51553304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d38fe90c83b791a9b98e339a4e4a51bd0e31687b9085b55e828b758afde91f`  
		Last Modified: Wed, 05 Jun 2024 06:12:39 GMT  
		Size: 138.1 MB (138062576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1903d5a3afe551f30d472ec237c0508ec2c0d47c7f5eca7f94cf22ecfe00cf2e`  
		Last Modified: Wed, 05 Jun 2024 06:12:36 GMT  
		Size: 54.9 KB (54898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11` - unknown; unknown

```console
$ docker pull gradle@sha256:15f55ec74e65138a5a53a88263ae2c0e2ec6a5a04b9c7328140a80c4f25915b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6998718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f553a77844f9337da093f9730f24337152d0feb226118854421a73211a6f42bf`

```dockerfile
```

-	Layers:
	-	`sha256:cd0734c0e21c2248496537eb8b9f06f651ddf3a6cc40486e1f86e9788ae0b955`  
		Last Modified: Wed, 05 Jun 2024 06:12:37 GMT  
		Size: 7.0 MB (6975891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5511434073f13e2d886fe64ca48696baefb2307b9dfd77c0184029299bdd82ed`  
		Last Modified: Wed, 05 Jun 2024 06:12:36 GMT  
		Size: 22.8 KB (22827 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk11` - linux; arm variant v7

```console
$ docker pull gradle@sha256:6822e9c44daeda5053b495ca73711b3c13ec38550b66c370efd325a31a515e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.0 MB (369988244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2969d22afadcc5d34d0e1df12a4e788904630a8f2a7e1432032e735097075c1c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 01 Jun 2024 15:03:05 GMT
ARG RELEASE
# Sat, 01 Jun 2024 15:03:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Jun 2024 15:03:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Jun 2024 15:03:05 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 01 Jun 2024 15:03:05 GMT
ADD file:76d606bb5f897ff3ffe149c5d3d049c7ace15da77a61a7df4e558eceebd8d2bd in / 
# Sat, 01 Jun 2024 15:03:05 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e00476a7be3c4adfa9b3d55d30768967fd246a8352e518894e183fa444d4d3ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='23e47ea7a3015be3240f21185fd902adebdcf76530757c9b482c7eb5bd3417c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='8077edc07a57d846c3d11286a7caf05ed6ca6d6c1234bf0e03611f18e187f075';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f56068bb64c6bf858894f75c2bc261f54db32932422eb07527f36ae40046e9a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf06c3e41acfaeda77112ac04f5a711cafe9fa9ac04dff758696fe7e8d66a0ea';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Sat, 01 Jun 2024 15:03:05 GMT
CMD ["gradle"]
# Sat, 01 Jun 2024 15:03:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 01 Jun 2024 15:03:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 01 Jun 2024 15:03:05 GMT
WORKDIR /home/gradle
# Sat, 01 Jun 2024 15:03:05 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
ENV GRADLE_VERSION=8.8
# Sat, 01 Jun 2024 15:03:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
# Sat, 01 Jun 2024 15:03:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
USER gradle
# Sat, 01 Jun 2024 15:03:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
USER root
```

-	Layers:
	-	`sha256:bb2b4ba5ac52e5e8a83a1f8dc3c79ed1f5409e3bc349a8c36b2cd4b9d3f6cb23`  
		Last Modified: Tue, 04 Jun 2024 01:38:51 GMT  
		Size: 27.5 MB (27534888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2e7d8e2026f154f12e834d8b72426c2f71c8a555d373336fddba91616868b7`  
		Last Modified: Wed, 05 Jun 2024 03:59:49 GMT  
		Size: 12.5 MB (12493203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463ed2419e5a3d33f88d49daac8b666c92a96a76a7a61459c49c34fcd3e6a9f1`  
		Last Modified: Wed, 05 Jun 2024 04:01:10 GMT  
		Size: 138.0 MB (138004561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ece81701fa181139e9fcefd2eedd9d1736df1692a74f866d31a164d40a548e3`  
		Last Modified: Wed, 05 Jun 2024 04:00:55 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed363f50e5e6714fd4c28aa4be93d0aac96e086f7e2a3aa187353c0af702b20`  
		Last Modified: Wed, 05 Jun 2024 04:00:55 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f4c5f60e9b8e36b6eebadb7011d346d2aca1862f79ed881d22fbba88f12f9f`  
		Last Modified: Wed, 05 Jun 2024 06:45:41 GMT  
		Size: 4.3 KB (4299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16dc7cad752a3896504a2f9456cc20feb33c72a98468b52f64e23084148e7deb`  
		Last Modified: Wed, 05 Jun 2024 06:45:44 GMT  
		Size: 53.9 MB (53887512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30fcfe5d6811c52097d49aa70537c2265a05804ad40395e68902d05f12bbe707`  
		Last Modified: Wed, 05 Jun 2024 06:45:46 GMT  
		Size: 138.1 MB (138062555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094e2105cdde0c86528993a497e90024f5f272ec666972b506512260d1de3f4e`  
		Last Modified: Wed, 05 Jun 2024 06:45:42 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11` - unknown; unknown

```console
$ docker pull gradle@sha256:a06d78ffb153665637f0c1b535263bf3679962a43ebf8af51f70b107399e965d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6999363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b07814e9d066ddad6c97c1a4dcc6499a948a9a2f7e6d3b33ad58f195bcdf66`

```dockerfile
```

-	Layers:
	-	`sha256:f92a4a5c099059a4805e5e6400401a45b119c617c1c8ec526bb9ef60925a69b6`  
		Last Modified: Wed, 05 Jun 2024 06:45:42 GMT  
		Size: 7.0 MB (6976396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8044975f789909868077b89e61cb355f4f77f85068145a94dfcffc611f44969`  
		Last Modified: Wed, 05 Jun 2024 06:45:41 GMT  
		Size: 23.0 KB (22967 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk11` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:190d0066a57e850fcb171d47f09a22bafa19e6ae70024cd6dc4196bf17694173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.8 MB (372825743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c9ee87f75082c6aee78570e44b5156f1876dd5e0569e582f7eb4bbec563cd80`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e00476a7be3c4adfa9b3d55d30768967fd246a8352e518894e183fa444d4d3ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='23e47ea7a3015be3240f21185fd902adebdcf76530757c9b482c7eb5bd3417c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='8077edc07a57d846c3d11286a7caf05ed6ca6d6c1234bf0e03611f18e187f075';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f56068bb64c6bf858894f75c2bc261f54db32932422eb07527f36ae40046e9a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf06c3e41acfaeda77112ac04f5a711cafe9fa9ac04dff758696fe7e8d66a0ea';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Sat, 01 Jun 2024 15:03:05 GMT
CMD ["gradle"]
# Sat, 01 Jun 2024 15:03:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 01 Jun 2024 15:03:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 01 Jun 2024 15:03:05 GMT
WORKDIR /home/gradle
# Sat, 01 Jun 2024 15:03:05 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
ENV GRADLE_VERSION=8.8
# Sat, 01 Jun 2024 15:03:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
# Sat, 01 Jun 2024 15:03:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
USER gradle
# Sat, 01 Jun 2024 15:03:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
USER root
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2472ac6840da0115175cae8b0be8d1b8c2b6b74acb5fc6bf185b0c9333b8a3`  
		Last Modified: Thu, 02 May 2024 04:17:28 GMT  
		Size: 12.8 MB (12847034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e0e8dbe77354ae4322c793be6d479bf2968d7a89c33a1fa305f402462eba8d`  
		Last Modified: Thu, 02 May 2024 04:18:41 GMT  
		Size: 142.3 MB (142311142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c2698f9483bfc599181902f9f470180ac5c9df9afa0cefb3e0b6561ed506b2`  
		Last Modified: Thu, 02 May 2024 04:18:32 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1600df7cb3218474629c2527afa2b3ee549558a582701c372c017e56f6529c3c`  
		Last Modified: Thu, 02 May 2024 04:18:32 GMT  
		Size: 731.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd06c06d2bf9623fc6d613baa5e8ca9ea478153225c95e579e4587b571a15487`  
		Last Modified: Tue, 04 Jun 2024 02:43:59 GMT  
		Size: 4.3 KB (4319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0652636030481a546c2031bc3fed50f5ca001aa0a45e88f3d6ff2241f45e516c`  
		Last Modified: Tue, 04 Jun 2024 02:44:01 GMT  
		Size: 51.1 MB (51139052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f72189ecbbb646e3ee52cf983570587398d20047670a356d1376ba843cfa9ce`  
		Last Modified: Tue, 04 Jun 2024 02:44:06 GMT  
		Size: 138.1 MB (138062554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8d72750644c7ef030c414113280c9d0f4a25cbc600953d3df6e9653093504f`  
		Last Modified: Tue, 04 Jun 2024 02:44:00 GMT  
		Size: 59.5 KB (59520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11` - unknown; unknown

```console
$ docker pull gradle@sha256:cd3ab66283d0787820c9cf40c4b74ef8b076a00816d0ee9526f404b70f0c9ad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7005578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f9bbe6102a99bd496328831caf66f9ee9dbbf8a864694a3bd40f07505f9888`

```dockerfile
```

-	Layers:
	-	`sha256:94d247c14fa3dbc2b69bfcd9c44ae9c1112eb14b7a55ada30672f41932aab202`  
		Last Modified: Tue, 04 Jun 2024 02:44:00 GMT  
		Size: 7.0 MB (6982385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f56f0ad9574a847cf5269bc4ea080d48d632824689935817ce0d0248990c8a0`  
		Last Modified: Tue, 04 Jun 2024 02:43:59 GMT  
		Size: 23.2 KB (23193 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk11` - linux; ppc64le

```console
$ docker pull gradle@sha256:c28f559e212e3d2660aa087b7cf881eb417dbb335f6b2d2c5f6778b0103e5918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.8 MB (375815009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5acdaf339f9a9ed87530ef4cc58d45b2f14f07f72210f52aece551f5a183571a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:13 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:13 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:17 GMT
ADD file:3ab2760f4e449111dcca3f0816583c72999e1ce2ec20beac068dccfd6c9d8b81 in / 
# Sat, 27 Apr 2024 13:18:17 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e00476a7be3c4adfa9b3d55d30768967fd246a8352e518894e183fa444d4d3ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='23e47ea7a3015be3240f21185fd902adebdcf76530757c9b482c7eb5bd3417c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='8077edc07a57d846c3d11286a7caf05ed6ca6d6c1234bf0e03611f18e187f075';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f56068bb64c6bf858894f75c2bc261f54db32932422eb07527f36ae40046e9a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf06c3e41acfaeda77112ac04f5a711cafe9fa9ac04dff758696fe7e8d66a0ea';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Sat, 01 Jun 2024 15:03:05 GMT
CMD ["gradle"]
# Sat, 01 Jun 2024 15:03:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 01 Jun 2024 15:03:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 01 Jun 2024 15:03:05 GMT
WORKDIR /home/gradle
# Sat, 01 Jun 2024 15:03:05 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
ENV GRADLE_VERSION=8.8
# Sat, 01 Jun 2024 15:03:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
# Sat, 01 Jun 2024 15:03:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
USER gradle
# Sat, 01 Jun 2024 15:03:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
USER root
```

-	Layers:
	-	`sha256:ef1313ed517c6def5644ab70e25cc66f1c4cd52b1e81c07fb33bfb8850b39c25`  
		Last Modified: Thu, 02 May 2024 01:40:15 GMT  
		Size: 35.6 MB (35588524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615a40d637191fd38e803d020c6fd9ef07a75d9c895faae5c0a3a02afa988fbc`  
		Last Modified: Thu, 02 May 2024 01:51:41 GMT  
		Size: 13.8 MB (13767451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157b579cb4fb1d0582c6c57618de44788a5b5dc513b26afcb67320c1e020409f`  
		Last Modified: Thu, 02 May 2024 01:53:05 GMT  
		Size: 132.7 MB (132719018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e7abaf0f8b4d8d6d8cb5d4d9725ee0d8d835017b4a62d31d50954fb198d519`  
		Last Modified: Thu, 02 May 2024 01:52:53 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c8d386e21c30c0454765311f15c9c047dba7222013efa1c749e45fcf3fbf65`  
		Last Modified: Thu, 02 May 2024 01:52:53 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35aa2630d9c9f68e8032435f720b2706624a72a6e893ce47da4044ebe027c8b`  
		Last Modified: Mon, 03 Jun 2024 19:41:55 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90bff657dc0767b74f10700d41eaa636115a91038e0db9fb8f84c83d2a0d709`  
		Last Modified: Mon, 03 Jun 2024 19:41:57 GMT  
		Size: 55.7 MB (55671925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00070f1f380b398070280296ce1f998c5a47d0e3c60e61d9e873f24a26fd15b`  
		Last Modified: Mon, 03 Jun 2024 19:42:00 GMT  
		Size: 138.1 MB (138062550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ada7af4a17cae171c277358275584967ac38dcfe374e3f7879e6c3d543d651c`  
		Last Modified: Mon, 03 Jun 2024 19:41:56 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11` - unknown; unknown

```console
$ docker pull gradle@sha256:ec1cd97c624f3b67e59c7a83c5972253355f0b6b8e55a4a835039420eb102df7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7006602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72b004ec9dfc8b3e5d910541a90f6689be65009486db8a498ea87a61005b937a`

```dockerfile
```

-	Layers:
	-	`sha256:13396e706f6a93e935167eb76749771f3157aede71ec858c57362513e1a21e85`  
		Last Modified: Mon, 03 Jun 2024 19:41:56 GMT  
		Size: 7.0 MB (6983708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb12fa36bdca5694a09d23943e3a1fc68db51d4b991d3369a7a9a61bf74c6012`  
		Last Modified: Mon, 03 Jun 2024 19:41:55 GMT  
		Size: 22.9 KB (22894 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk11` - linux; s390x

```console
$ docker pull gradle@sha256:68b8b13e6eccbf6cbef99e079898d3f404d0d1835f0f7f5eb9abbcd4744d49d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.5 MB (356464263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991bb7c8591c76930d51a30076836d2ec62776f1ae8ccd8206e16bbb04bab117`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 01 Jun 2024 15:03:05 GMT
ARG RELEASE
# Sat, 01 Jun 2024 15:03:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Jun 2024 15:03:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Jun 2024 15:03:05 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 01 Jun 2024 15:03:05 GMT
ADD file:4fb908f3bd908a7abc338d7e2006cb2c97aa7f83aca415f3b86c0ae86d61fed1 in / 
# Sat, 01 Jun 2024 15:03:05 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e00476a7be3c4adfa9b3d55d30768967fd246a8352e518894e183fa444d4d3ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='23e47ea7a3015be3240f21185fd902adebdcf76530757c9b482c7eb5bd3417c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='8077edc07a57d846c3d11286a7caf05ed6ca6d6c1234bf0e03611f18e187f075';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f56068bb64c6bf858894f75c2bc261f54db32932422eb07527f36ae40046e9a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf06c3e41acfaeda77112ac04f5a711cafe9fa9ac04dff758696fe7e8d66a0ea';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Sat, 01 Jun 2024 15:03:05 GMT
CMD ["gradle"]
# Sat, 01 Jun 2024 15:03:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 01 Jun 2024 15:03:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 01 Jun 2024 15:03:05 GMT
WORKDIR /home/gradle
# Sat, 01 Jun 2024 15:03:05 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
ENV GRADLE_VERSION=8.8
# Sat, 01 Jun 2024 15:03:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
# Sat, 01 Jun 2024 15:03:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
USER gradle
# Sat, 01 Jun 2024 15:03:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
USER root
```

-	Layers:
	-	`sha256:0424de0056677a3a1d049300220cb3d875fb304aae1fa90f7b0292500716e5ed`  
		Last Modified: Wed, 05 Jun 2024 03:12:35 GMT  
		Size: 28.6 MB (28637399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87504bacc983be102c1f56d585bd6aeb2fba4f402fc20a73671274561ac7e98b`  
		Last Modified: Wed, 05 Jun 2024 03:12:32 GMT  
		Size: 13.0 MB (12986422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e374406e8bee25824b499de36dfba887dda16ea6af784e60a74d29117fe5bf`  
		Last Modified: Wed, 05 Jun 2024 03:12:45 GMT  
		Size: 125.5 MB (125501678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f014b0093e858ac799fbb568f1106a0e13e2ff49e82660c9f4c67467cee1c75`  
		Last Modified: Wed, 05 Jun 2024 03:12:30 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc69886f6a87f60a8646873e31032dd4b2966f47a53494f91ec9ca1391d66602`  
		Last Modified: Wed, 05 Jun 2024 03:12:31 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c1bc0cba73cb8ee34f9a8d663ee2b85432ace3f66edc6db607672b2a6a2996`  
		Last Modified: Wed, 05 Jun 2024 07:27:58 GMT  
		Size: 4.3 KB (4317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e83940ab52d94922096b731c7504c3254641bdff68d7f39bc14e2a1852764c5e`  
		Last Modified: Wed, 05 Jun 2024 07:28:01 GMT  
		Size: 51.3 MB (51270671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d776192c99d8d24ea0b8d68655db37014ce9220f1e0cd3fbc7be84a7099879f2`  
		Last Modified: Wed, 05 Jun 2024 07:28:02 GMT  
		Size: 138.1 MB (138062552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbcb2a323cfe07dcddca4d0765c96a439abae233e0e9625fa931680598b9fbfe`  
		Last Modified: Wed, 05 Jun 2024 07:27:58 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11` - unknown; unknown

```console
$ docker pull gradle@sha256:b71fbbc57f58a29f5b6e2878b7e1d157783a53b247edbaea56b559275c96a618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6998660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea3bd4ac8bfc533304e01b8423bbb43163bb4e2ba9d6796821358a1419200bd4`

```dockerfile
```

-	Layers:
	-	`sha256:0947a25e419e4f558efe7753b029abfb046caafc96e8f04b99864ea7ddea3f62`  
		Last Modified: Wed, 05 Jun 2024 07:27:58 GMT  
		Size: 7.0 MB (6975835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:191d1ef529549af24ca766c3790f3b6ed1a678a71f5044ce1dfb2a65282bcd76`  
		Last Modified: Wed, 05 Jun 2024 07:27:58 GMT  
		Size: 22.8 KB (22825 bytes)  
		MIME: application/vnd.in-toto+json
