## `gradle:7-jdk11-jammy`

```console
$ docker pull gradle@sha256:e708a7b43ebbffa17a5123a30d9319ad5dcae672cf200ff5d0a2b0be1b371069
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

### `gradle:7-jdk11-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:421b1f778db5b93ccd5906c3bb9e25dcae4bd15ec823df8bdd2688953025c25e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.2 MB (363197749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6be5815cf0a50647e4825897aba33d8abf35b30ed43c6dde3a6ef5f09e9a5a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 05 Feb 2024 22:05:50 GMT
ARG RELEASE
# Mon, 05 Feb 2024 22:05:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Feb 2024 22:05:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Feb 2024 22:05:50 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Feb 2024 22:05:50 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 05 Feb 2024 22:05:50 GMT
CMD ["/bin/bash"]
# Mon, 05 Feb 2024 22:05:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 05 Feb 2024 22:05:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Feb 2024 22:05:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e00476a7be3c4adfa9b3d55d30768967fd246a8352e518894e183fa444d4d3ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='23e47ea7a3015be3240f21185fd902adebdcf76530757c9b482c7eb5bd3417c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='8077edc07a57d846c3d11286a7caf05ed6ca6d6c1234bf0e03611f18e187f075';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f56068bb64c6bf858894f75c2bc261f54db32932422eb07527f36ae40046e9a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf06c3e41acfaeda77112ac04f5a711cafe9fa9ac04dff758696fe7e8d66a0ea';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 05 Feb 2024 22:05:50 GMT
CMD ["jshell"]
# Mon, 05 Feb 2024 22:05:50 GMT
CMD ["gradle"]
# Mon, 05 Feb 2024 22:05:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 05 Feb 2024 22:05:50 GMT
WORKDIR /home/gradle
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENV GRADLE_VERSION=7.6.4
# Mon, 05 Feb 2024 22:05:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Mon, 05 Feb 2024 22:05:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
USER gradle
# Mon, 05 Feb 2024 22:05:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
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
	-	`sha256:48af12c3bc389429b16f89a66c1010ae6980bfcb957ecbdca073d31d7fdf085b`  
		Last Modified: Wed, 05 Jun 2024 06:12:30 GMT  
		Size: 4.3 KB (4310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a911584895566ace994bdac61a8d65e75d914e3172eed323d96bf74f324646b1`  
		Last Modified: Wed, 05 Jun 2024 06:12:31 GMT  
		Size: 51.6 MB (51553849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224a12d1ea06571b59db177353cd4a67a1b15f38ea79ac9746dad05ac6a27bcc`  
		Last Modified: Wed, 05 Jun 2024 06:12:32 GMT  
		Size: 122.7 MB (122730487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501d613da856ba26b4b3bb5f8b97356b335d2ed536e3450f5a47aff16cd9bac6`  
		Last Modified: Wed, 05 Jun 2024 06:12:30 GMT  
		Size: 54.9 KB (54886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:43b4fc11823da0069d49720c0fd04901c405677140a05732c5c7f81b582b186d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6967597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc654a5daa5190cfe21cdf7084c38f740ae2f775dd352680b9593b9d6d439e41`

```dockerfile
```

-	Layers:
	-	`sha256:656ba39a6cde539195299deca6e24ec909f5a55babdffa07771cbc3b8f5df8c5`  
		Last Modified: Wed, 05 Jun 2024 06:12:30 GMT  
		Size: 6.9 MB (6945366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18ba0860831c4cfde192c1bcfcf38df1a542236a344c56256741171dc234dd0d`  
		Last Modified: Wed, 05 Jun 2024 06:12:30 GMT  
		Size: 22.2 KB (22231 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk11-jammy` - linux; arm variant v7

```console
$ docker pull gradle@sha256:47b7f5908d4ff062805c35e101fb67a4ba85f647267557361015532ef685be3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.7 MB (354687226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806664fd31b6e8dc3cbc447d294b5892380e192455b8102e2e9cc8cf21a63d55`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 05 Feb 2024 22:05:50 GMT
ARG RELEASE
# Mon, 05 Feb 2024 22:05:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Feb 2024 22:05:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Feb 2024 22:05:50 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Feb 2024 22:05:50 GMT
ADD file:76d606bb5f897ff3ffe149c5d3d049c7ace15da77a61a7df4e558eceebd8d2bd in / 
# Mon, 05 Feb 2024 22:05:50 GMT
CMD ["/bin/bash"]
# Mon, 05 Feb 2024 22:05:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 05 Feb 2024 22:05:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Feb 2024 22:05:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e00476a7be3c4adfa9b3d55d30768967fd246a8352e518894e183fa444d4d3ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='23e47ea7a3015be3240f21185fd902adebdcf76530757c9b482c7eb5bd3417c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='8077edc07a57d846c3d11286a7caf05ed6ca6d6c1234bf0e03611f18e187f075';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f56068bb64c6bf858894f75c2bc261f54db32932422eb07527f36ae40046e9a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf06c3e41acfaeda77112ac04f5a711cafe9fa9ac04dff758696fe7e8d66a0ea';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 05 Feb 2024 22:05:50 GMT
CMD ["jshell"]
# Mon, 05 Feb 2024 22:05:50 GMT
CMD ["gradle"]
# Mon, 05 Feb 2024 22:05:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 05 Feb 2024 22:05:50 GMT
WORKDIR /home/gradle
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENV GRADLE_VERSION=7.6.4
# Mon, 05 Feb 2024 22:05:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Mon, 05 Feb 2024 22:05:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
USER gradle
# Mon, 05 Feb 2024 22:05:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
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
	-	`sha256:44accc0f9a14f1dcd22d4cec09f821e3c6e0d783e24c288278b4b916c1144001`  
		Last Modified: Wed, 05 Jun 2024 06:53:40 GMT  
		Size: 122.7 MB (122730527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57874a008de29ac5982258e142d996dfed1bedd57d1d9917f6d0dd9329f246d2`  
		Last Modified: Wed, 05 Jun 2024 06:53:36 GMT  
		Size: 31.3 KB (31295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:5f61fba2b8c351552470030111717ff6b7358fbb1c3f6ebb2ef47d22c74d7d14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6968072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0715a7e1ef727352a04cd2a0c2438572420865871c67b8fb3e3a078e5a83d738`

```dockerfile
```

-	Layers:
	-	`sha256:4b1fe59a3560b5db723a463f0a40c8e3f97a1d95284e06c3adeb6c86ceff3b75`  
		Last Modified: Wed, 05 Jun 2024 06:53:37 GMT  
		Size: 6.9 MB (6945715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79e8c9f105470ffba64dae2be5e404e6fe2987b2a78f7d65b0d2b9eb8689a865`  
		Last Modified: Wed, 05 Jun 2024 06:53:36 GMT  
		Size: 22.4 KB (22357 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk11-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:d3b6e8970ee68f7a5a606115bcea6113a1c1a80cef2f1e64f29f4cc2c6986af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.5 MB (357467475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9e66160b0eb8a001df28be5d2397728ac0b287e4223c414b560bbd289b882cc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 05 Feb 2024 22:05:50 GMT
ARG RELEASE
# Mon, 05 Feb 2024 22:05:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Feb 2024 22:05:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Feb 2024 22:05:50 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Feb 2024 22:05:50 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Mon, 05 Feb 2024 22:05:50 GMT
CMD ["/bin/bash"]
# Mon, 05 Feb 2024 22:05:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 05 Feb 2024 22:05:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Feb 2024 22:05:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e00476a7be3c4adfa9b3d55d30768967fd246a8352e518894e183fa444d4d3ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='23e47ea7a3015be3240f21185fd902adebdcf76530757c9b482c7eb5bd3417c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='8077edc07a57d846c3d11286a7caf05ed6ca6d6c1234bf0e03611f18e187f075';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f56068bb64c6bf858894f75c2bc261f54db32932422eb07527f36ae40046e9a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf06c3e41acfaeda77112ac04f5a711cafe9fa9ac04dff758696fe7e8d66a0ea';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 05 Feb 2024 22:05:50 GMT
CMD ["jshell"]
# Mon, 05 Feb 2024 22:05:50 GMT
CMD ["gradle"]
# Mon, 05 Feb 2024 22:05:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 05 Feb 2024 22:05:50 GMT
WORKDIR /home/gradle
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENV GRADLE_VERSION=7.6.4
# Mon, 05 Feb 2024 22:05:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Mon, 05 Feb 2024 22:05:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
USER gradle
# Mon, 05 Feb 2024 22:05:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
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
	-	`sha256:ddf7f71528cd9d5243a6f4473c72b5a7eed8097164b6edbc3f97c32aaa4d4786`  
		Last Modified: Thu, 16 May 2024 22:32:33 GMT  
		Size: 4.3 KB (4319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8788684e08a247d428297d42d6a8f87aebf71b128dca6f5fcfcdafdc768fc2`  
		Last Modified: Thu, 16 May 2024 22:32:34 GMT  
		Size: 51.1 MB (51112799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2665fad9f2e9ddf34350e166838c6832deb7a344d9834a4951331b45404a8fe`  
		Last Modified: Thu, 16 May 2024 22:44:11 GMT  
		Size: 122.7 MB (122730530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41693b0bbcad40d13cc35b6b1e373a9510eaadb191c6bb6905cb0987a7fb7a4b`  
		Last Modified: Thu, 16 May 2024 22:44:08 GMT  
		Size: 59.5 KB (59529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:cda41628614fcbf134916d59d6b2b5a37144ccf3e42a2025f5761ac09211ba9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6973949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f057bda2ae1b8288d591538936a7f3cfd6a4069fac4c59e0bf7a504ce15a05d5`

```dockerfile
```

-	Layers:
	-	`sha256:f4ca494fbc0104dfe59668be1779927d0f0aee2dfba176266195f6e1ee3c8532`  
		Last Modified: Thu, 16 May 2024 22:44:08 GMT  
		Size: 7.0 MB (6951703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0e1f5b1451b55f876eb15de35466dae29586577816afa321c1d68dcce4e4220`  
		Last Modified: Thu, 16 May 2024 22:44:08 GMT  
		Size: 22.2 KB (22246 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk11-jammy` - linux; ppc64le

```console
$ docker pull gradle@sha256:76014e72142489889bda2957a42b2aeefefb261c59e6c6b821bddd9962f6399d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.5 MB (360512604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9160b2cdacb07df254979f6ee8ed494b64e2a0fb26dfbe79f3969be24a49b9b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 05 Feb 2024 22:05:50 GMT
ARG RELEASE
# Mon, 05 Feb 2024 22:05:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Feb 2024 22:05:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Feb 2024 22:05:50 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Feb 2024 22:05:50 GMT
ADD file:3ab2760f4e449111dcca3f0816583c72999e1ce2ec20beac068dccfd6c9d8b81 in / 
# Mon, 05 Feb 2024 22:05:50 GMT
CMD ["/bin/bash"]
# Mon, 05 Feb 2024 22:05:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 05 Feb 2024 22:05:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Feb 2024 22:05:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e00476a7be3c4adfa9b3d55d30768967fd246a8352e518894e183fa444d4d3ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='23e47ea7a3015be3240f21185fd902adebdcf76530757c9b482c7eb5bd3417c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='8077edc07a57d846c3d11286a7caf05ed6ca6d6c1234bf0e03611f18e187f075';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f56068bb64c6bf858894f75c2bc261f54db32932422eb07527f36ae40046e9a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf06c3e41acfaeda77112ac04f5a711cafe9fa9ac04dff758696fe7e8d66a0ea';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 05 Feb 2024 22:05:50 GMT
CMD ["jshell"]
# Mon, 05 Feb 2024 22:05:50 GMT
CMD ["gradle"]
# Mon, 05 Feb 2024 22:05:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 05 Feb 2024 22:05:50 GMT
WORKDIR /home/gradle
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENV GRADLE_VERSION=7.6.4
# Mon, 05 Feb 2024 22:05:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Mon, 05 Feb 2024 22:05:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
USER gradle
# Mon, 05 Feb 2024 22:05:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
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
	-	`sha256:ab7272bffab70395814a1481ae55cc0c2a9ce0b820298c5a2b35f292ea1f9c2f`  
		Last Modified: Fri, 17 May 2024 00:14:29 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b7d20516c48adeef3ab78f3d39c2c2f06786deb4724d629fa3fe58d0656bfb`  
		Last Modified: Fri, 17 May 2024 00:14:32 GMT  
		Size: 55.7 MB (55666826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9c0f614b3dc5214890d696ed5d315e3fec31c6413a4944bf5dd07d1a02981f`  
		Last Modified: Fri, 17 May 2024 02:36:39 GMT  
		Size: 122.7 MB (122730530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0dcd0c0076b12cfb034535eab70489b30d0b02b398fc360323597a98acd25b`  
		Last Modified: Fri, 17 May 2024 02:36:35 GMT  
		Size: 35.0 KB (35002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:66993802ac9837febc75d4b8a8b9f9859dd12a9e8e368a78a8912dc9841bbf73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6975398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67e4cb8a13c5cd5794696400942be0913eab258c50a7db5cf03ff06a7e0474dd`

```dockerfile
```

-	Layers:
	-	`sha256:f5dba71f21fb76cd07f6706e28d2b1c0cfb67328172c41fff6fcc5a714d1c4c5`  
		Last Modified: Fri, 17 May 2024 02:36:36 GMT  
		Size: 7.0 MB (6953110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6973265f2eba99646be790093e7a4316b67889fb3112bd851469d525eb26eea2`  
		Last Modified: Fri, 17 May 2024 02:36:35 GMT  
		Size: 22.3 KB (22288 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk11-jammy` - linux; s390x

```console
$ docker pull gradle@sha256:2129ac306656124a684f6fc069d0ea0d465e8bb8d43ea7c13eb5580a960af6f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.2 MB (341166965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:836e42ee7edef8ee5730b98303a4ac60a92824e2178ff37163fbf3dc6d8d3ffc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 05 Feb 2024 22:05:50 GMT
ARG RELEASE
# Mon, 05 Feb 2024 22:05:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Feb 2024 22:05:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Feb 2024 22:05:50 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Feb 2024 22:05:50 GMT
ADD file:4fb908f3bd908a7abc338d7e2006cb2c97aa7f83aca415f3b86c0ae86d61fed1 in / 
# Mon, 05 Feb 2024 22:05:50 GMT
CMD ["/bin/bash"]
# Mon, 05 Feb 2024 22:05:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 05 Feb 2024 22:05:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Feb 2024 22:05:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e00476a7be3c4adfa9b3d55d30768967fd246a8352e518894e183fa444d4d3ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='23e47ea7a3015be3240f21185fd902adebdcf76530757c9b482c7eb5bd3417c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='8077edc07a57d846c3d11286a7caf05ed6ca6d6c1234bf0e03611f18e187f075';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f56068bb64c6bf858894f75c2bc261f54db32932422eb07527f36ae40046e9a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf06c3e41acfaeda77112ac04f5a711cafe9fa9ac04dff758696fe7e8d66a0ea';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 05 Feb 2024 22:05:50 GMT
CMD ["jshell"]
# Mon, 05 Feb 2024 22:05:50 GMT
CMD ["gradle"]
# Mon, 05 Feb 2024 22:05:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 05 Feb 2024 22:05:50 GMT
WORKDIR /home/gradle
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
ENV GRADLE_VERSION=7.6.4
# Mon, 05 Feb 2024 22:05:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Mon, 05 Feb 2024 22:05:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
USER gradle
# Mon, 05 Feb 2024 22:05:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
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
	-	`sha256:b3ff8e70ea2ec06e8951a0c388625d42321a7f3847541571d43af650abfbf103`  
		Last Modified: Wed, 05 Jun 2024 07:35:56 GMT  
		Size: 122.7 MB (122730529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343194177ad5afdd9967f7d2919b9381d7ad0c388fef9bb8ccd76380d5f5c14a`  
		Last Modified: Wed, 05 Jun 2024 07:35:53 GMT  
		Size: 35.0 KB (35011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:f6b8a1674d9da0ca58f11d3304d743203ac68f013471b23b76a6e99bc8531631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6967475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb028d8a24ea3df20db5545460130998737b9e1f7a36e5e3733b4490bcec408`

```dockerfile
```

-	Layers:
	-	`sha256:a7bdc3b393f43348332781901d0bd908b1476703f732a5fc959caf2fa5d4f274`  
		Last Modified: Wed, 05 Jun 2024 07:35:53 GMT  
		Size: 6.9 MB (6945243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6d08678dc1305f0ca2e3645e12395a1b54b1f734c7a5c7b7625569a5940cc7a`  
		Last Modified: Wed, 05 Jun 2024 07:35:52 GMT  
		Size: 22.2 KB (22232 bytes)  
		MIME: application/vnd.in-toto+json
