## `gradle:focal`

```console
$ docker pull gradle@sha256:22a28e07e71fbf4577ed37f05e97393c0a8885fd2aa0406bfefb93f5d13531e6
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

### `gradle:focal` - linux; amd64

```console
$ docker pull gradle@sha256:4b918d7def69152fd55c916f0b453dc0424d8980c428542a3b73048e243109ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.1 MB (397063043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbea746428da32b898a5fab24438a2e32ae2f10e05d8ca2538bc360c67699789`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 13 Aug 2024 09:26:46 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:26:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:26:48 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 13 Aug 2024 09:26:48 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["jshell"]
# Sat, 28 Sep 2024 00:46:05 GMT
CMD ["gradle"]
# Sat, 28 Sep 2024 00:46:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 28 Sep 2024 00:46:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 28 Sep 2024 00:46:05 GMT
WORKDIR /home/gradle
# Sat, 28 Sep 2024 00:46:05 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
ENV GRADLE_VERSION=8.10.2
# Sat, 28 Sep 2024 00:46:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
# Sat, 28 Sep 2024 00:46:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
USER gradle
# Sat, 28 Sep 2024 00:46:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
USER root
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5aedc0e1fdb7b1e0021df89491ab1ecb1d06f9ed9029843e236b44cc81d167`  
		Last Modified: Wed, 05 Jun 2024 05:00:16 GMT  
		Size: 20.7 MB (20672189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460b26a845b3dacac3596a292cd7a4fc0b933f99c647ae88429fdb474e1b5705`  
		Last Modified: Tue, 23 Jul 2024 01:07:03 GMT  
		Size: 145.2 MB (145178336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e3f73af39d0d03cfbec4869402d3c3b955717f2cc4c435e1a262c4769ce07e`  
		Last Modified: Tue, 23 Jul 2024 01:06:52 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef392037e06aafa4695d1001b88a5a52b9d9eea67a8cf2126beeaebaf33d24b4`  
		Last Modified: Fri, 23 Aug 2024 19:26:53 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732e3713539c29793e0d76190048bd56331becfe384cce4f33cb4fe6b3721d92`  
		Last Modified: Mon, 30 Sep 2024 21:56:11 GMT  
		Size: 4.3 KB (4323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e1098cacfd3909b0273abf8fba80b2f2f4d9d8cd5ba206f3b3ce5b50947971`  
		Last Modified: Mon, 30 Sep 2024 21:56:12 GMT  
		Size: 65.8 MB (65837023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2343645f079d41d6d45fec086d1efb868bc7857181d8e30dd4bd9cc34f6d62ab`  
		Last Modified: Mon, 30 Sep 2024 21:56:13 GMT  
		Size: 136.7 MB (136729733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d691c1478afc29338c9b880741aac3372be5befedc3a25ad3c3137a3e18d5485`  
		Last Modified: Mon, 30 Sep 2024 21:56:11 GMT  
		Size: 54.9 KB (54900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:focal` - unknown; unknown

```console
$ docker pull gradle@sha256:7c1d1ddfac7f1aea45b19590a70607325d11e650a5c6e3371ac9be95bc50e90b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7808975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:823f7b6c14807609dade669aa81dabbd5c5b1579982ad263c22c221aa8b6959b`

```dockerfile
```

-	Layers:
	-	`sha256:cd4f6ed9648d65ece5aa46b0e1f15e8f966d3d898796ab4e35f74bdef84c327f`  
		Last Modified: Mon, 30 Sep 2024 21:56:11 GMT  
		Size: 7.8 MB (7784818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5de912b974265dd6b16372ff2d5504f5a35b08dbb9fa6b54c486a64c35eb2eb`  
		Last Modified: Mon, 30 Sep 2024 21:56:11 GMT  
		Size: 24.2 KB (24157 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:focal` - linux; arm variant v7

```console
$ docker pull gradle@sha256:97aac160261dc669946fe81c8455d2a66d53da81bdff5d086302a319f30a2d24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.4 MB (384406384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a9d61a927076c983fd43b701b2545b2467530623c7a6d83a8ba2c964e1187f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 13 Aug 2024 09:29:35 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:29:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:29:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:29:35 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:29:37 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Tue, 13 Aug 2024 09:29:38 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["jshell"]
# Sat, 28 Sep 2024 00:46:05 GMT
CMD ["gradle"]
# Sat, 28 Sep 2024 00:46:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 28 Sep 2024 00:46:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 28 Sep 2024 00:46:05 GMT
WORKDIR /home/gradle
# Sat, 28 Sep 2024 00:46:05 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
ENV GRADLE_VERSION=8.10.2
# Sat, 28 Sep 2024 00:46:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
# Sat, 28 Sep 2024 00:46:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
USER gradle
# Sat, 28 Sep 2024 00:46:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
USER root
```

-	Layers:
	-	`sha256:fdbafd70c97f0cd921335e769caece4ff9a54483363cd205543860fb1e1cc94e`  
		Last Modified: Wed, 05 Jun 2024 03:30:49 GMT  
		Size: 24.6 MB (24603821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7727e8480ab0d546c03e272641ac75e49de4204e0ca2ce79b0c85c1b50fd9407`  
		Last Modified: Wed, 05 Jun 2024 04:01:52 GMT  
		Size: 20.0 MB (19957955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a261ac4799d19425c98a8958ce356429a185b155daaa3ccd9c52c064bf9eff`  
		Last Modified: Tue, 23 Jul 2024 03:17:00 GMT  
		Size: 142.6 MB (142645314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303476b7ea40a2ba3c3fe0d37faa3537ff10fc69cfd923597b5a4ce4e098f697`  
		Last Modified: Tue, 23 Jul 2024 03:16:43 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f7693dcee5cc72604371f974af463906fac6f607d18105e8655c4d8fded38b`  
		Last Modified: Fri, 23 Aug 2024 19:00:14 GMT  
		Size: 2.1 KB (2106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4135b805f71fe8c9f35394dccad66e5ffc18ca12bc9e5793bc3968d31274773e`  
		Last Modified: Mon, 30 Sep 2024 22:04:11 GMT  
		Size: 4.3 KB (4301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23b0a49d2c7e056c20f8d8f75299162bf1552ef696213574bfc53ff8ba8f180`  
		Last Modified: Mon, 30 Sep 2024 22:04:13 GMT  
		Size: 60.5 MB (60462751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4bafb49b0ef59241cbcc5d1eb8dcf8e5d0b82e0d810c3a7b0195cb322c93a72`  
		Last Modified: Mon, 30 Sep 2024 22:04:15 GMT  
		Size: 136.7 MB (136729639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe439014d296f294e97cfb28125057838d93d849a5b4b078715c10e0e3ebbac2`  
		Last Modified: Mon, 30 Sep 2024 22:04:11 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:focal` - unknown; unknown

```console
$ docker pull gradle@sha256:d11f7ba52cff4090817cbbe0da1f0f3db9870f95dd175764b6a2c7cb52f3c44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7729851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b6b3b102c27d55d59df86662b8f062123f87575669fdb329d556a1aa1def24`

```dockerfile
```

-	Layers:
	-	`sha256:cd7c99bcfcb3906afaf1a66fbe7aba1867119e5d73ff930988c975abfdb41d41`  
		Last Modified: Mon, 30 Sep 2024 22:04:11 GMT  
		Size: 7.7 MB (7705523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d13c3c612bcad57068e54936634307415738c03488959c091204786c1f0b0b1`  
		Last Modified: Mon, 30 Sep 2024 22:04:11 GMT  
		Size: 24.3 KB (24328 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:focal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:b5962928247840254504dff3025ef83723ceb1e588446e86134359c7ad152226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.0 MB (394982312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb08bce83b0acdbd016fb92269769d98803efc720193e5bf8853e7485a7ed92`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:56 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:27:58 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Tue, 13 Aug 2024 09:27:58 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["jshell"]
# Sat, 28 Sep 2024 00:46:05 GMT
CMD ["gradle"]
# Sat, 28 Sep 2024 00:46:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 28 Sep 2024 00:46:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 28 Sep 2024 00:46:05 GMT
WORKDIR /home/gradle
# Sat, 28 Sep 2024 00:46:05 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
ENV GRADLE_VERSION=8.10.2
# Sat, 28 Sep 2024 00:46:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
# Sat, 28 Sep 2024 00:46:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
USER gradle
# Sat, 28 Sep 2024 00:46:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
USER root
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3947aac99c3e7c1d43015a496d42024cac8967a86cab89aef36ae800c0272bdd`  
		Last Modified: Wed, 05 Jun 2024 04:56:48 GMT  
		Size: 21.4 MB (21375371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867b3de9f22fc9a80b614795706d0ab9b418935a0fc119bb4b08b2c3c09e0d0e`  
		Last Modified: Tue, 23 Jul 2024 04:12:42 GMT  
		Size: 144.0 MB (143967215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d51a74b88c1cc6131458a8bab48a7327f44645d9c1ed2e5ada16eed7c9eb376`  
		Last Modified: Tue, 23 Jul 2024 04:12:33 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ac5324d0374acc083f98dfb116395b5d4b00e109ef960660805724e06fc5d1`  
		Last Modified: Fri, 23 Aug 2024 19:44:29 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1d0785176cd58c6f1dcc840828d4954ccaf72f946329a7019b80600ca20746`  
		Last Modified: Mon, 30 Sep 2024 22:01:51 GMT  
		Size: 4.3 KB (4318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575ce1e4707ebe0dfa1a307a873019d0a547dcb92a9de26f22443446a41b522b`  
		Last Modified: Mon, 30 Sep 2024 22:01:54 GMT  
		Size: 65.6 MB (65638676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4960356925335f2e24072abaaba0a33eb8d18332fe3fe2dcd69be040b8e704`  
		Last Modified: Mon, 30 Sep 2024 22:01:55 GMT  
		Size: 136.7 MB (136729644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6ab2c49c1a833b9f9e64c9372540eec57a03d0df44bdd476302f088a6851e5`  
		Last Modified: Mon, 30 Sep 2024 22:01:52 GMT  
		Size: 59.5 KB (59531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:focal` - unknown; unknown

```console
$ docker pull gradle@sha256:c4e6768e4bcf71a3a72bff9577eab2158b931378e9a2317dc7adb4633f2d2dde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7911236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dcc9198651739d208b494c8710e3e5ba5abd65541d35787d8d346819f01cd94`

```dockerfile
```

-	Layers:
	-	`sha256:e94e76004d19088093272054cd11f827220d7074b8a6102f3a8676aaf4a595a7`  
		Last Modified: Mon, 30 Sep 2024 22:01:52 GMT  
		Size: 7.9 MB (7886666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abee594881192b2206e25af3b6fde414d6f78261b209321d2e2d0ea6389b9546`  
		Last Modified: Mon, 30 Sep 2024 22:01:51 GMT  
		Size: 24.6 KB (24570 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:focal` - linux; ppc64le

```console
$ docker pull gradle@sha256:907f6905c7dbc779719c222e3ba8cbe9a9955dd65f08f87be5c1e802a0600c1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.9 MB (411881636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d430d401b5387f7cd5e7483ad9a17b258937e5396a95fcb238777d64f77f06ee`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 13 Aug 2024 09:30:49 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:30:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:30:52 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Tue, 13 Aug 2024 09:30:52 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["jshell"]
# Sat, 28 Sep 2024 00:46:05 GMT
CMD ["gradle"]
# Sat, 28 Sep 2024 00:46:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 28 Sep 2024 00:46:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 28 Sep 2024 00:46:05 GMT
WORKDIR /home/gradle
# Sat, 28 Sep 2024 00:46:05 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
ENV GRADLE_VERSION=8.10.2
# Sat, 28 Sep 2024 00:46:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
# Sat, 28 Sep 2024 00:46:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
USER gradle
# Sat, 28 Sep 2024 00:46:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
USER root
```

-	Layers:
	-	`sha256:eb386e2cea8559613691083e515b5dad445536487242267707f4a8aec6a17286`  
		Last Modified: Wed, 05 Jun 2024 03:47:07 GMT  
		Size: 33.3 MB (33316120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7279313aa43260c90e56081f2f0fa3737f14cb0dce37ae46dc81d4ec4f561e1f`  
		Last Modified: Wed, 05 Jun 2024 04:02:27 GMT  
		Size: 22.7 MB (22715832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71a9f0efdba1b837a77b11e9c5274d8531a6731f0c76cfe5f2ae2252c69dc86`  
		Last Modified: Tue, 23 Jul 2024 01:42:34 GMT  
		Size: 144.9 MB (144864837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07bbaa65568bf9a4164ed7225cf03fb884535018c25b038d738f6efdb3308dc`  
		Last Modified: Tue, 23 Jul 2024 01:42:20 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a247b447125a2e53ddd142a6a49dc0c7166b99023a99576d90592c47ddf30975`  
		Last Modified: Fri, 23 Aug 2024 19:23:32 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb10255113b44bf8e0eab02c832008e6742e3882163da4eb16f554f39ec08d8d`  
		Last Modified: Mon, 30 Sep 2024 22:05:16 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90e48ebe0208e21f08af3be70d6458497db7a04dc8b62106d97b2d1035e2291`  
		Last Modified: Mon, 30 Sep 2024 22:05:19 GMT  
		Size: 74.2 MB (74248270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d03598922caf55fd2664ec5da9b37d2ace8110f649ab3861406f13b86cb24bd`  
		Last Modified: Mon, 30 Sep 2024 22:05:21 GMT  
		Size: 136.7 MB (136729662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb934f8d65d7d199813f500dff73e5577318d1869f8905d4544cbfdc1b5c8548`  
		Last Modified: Mon, 30 Sep 2024 22:05:17 GMT  
		Size: 289.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:focal` - unknown; unknown

```console
$ docker pull gradle@sha256:171706626ee1cf005078fe86932995a161c6b5b797d0138a2352239f1141be30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7839846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8353b97aa1f057db30dd2393415a644fee57de829754ee3106e2b9b4de7371e`

```dockerfile
```

-	Layers:
	-	`sha256:049941a37e87d3e4ecaebfdf42f04323fc1c00b06835ba7ed172f12c72c77492`  
		Last Modified: Mon, 30 Sep 2024 22:05:17 GMT  
		Size: 7.8 MB (7815600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32e6d1cbe1092cac91a13f33dc2cd0dc2c73b8b3e4289d6807d9b88d64ad210b`  
		Last Modified: Mon, 30 Sep 2024 22:05:16 GMT  
		Size: 24.2 KB (24246 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:focal` - linux; s390x

```console
$ docker pull gradle@sha256:2aa83b77cf90339bf0e0ea80f11e181e230b44dc6bf89c117b3fdb00fa082b07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.5 MB (383466143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:591a7a095999c7e1b9d9a528f0b532cb88b3d137caa757eedf5c7bed142093d6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 13 Aug 2024 09:29:15 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:29:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:29:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:29:15 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:29:17 GMT
ADD file:39767f0b13dc17d01020c3b8f88f8738a789fa7a5b27336e218ba44a42cbb60c in / 
# Tue, 13 Aug 2024 09:29:18 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["jshell"]
# Sat, 28 Sep 2024 00:46:05 GMT
CMD ["gradle"]
# Sat, 28 Sep 2024 00:46:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 28 Sep 2024 00:46:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 28 Sep 2024 00:46:05 GMT
WORKDIR /home/gradle
# Sat, 28 Sep 2024 00:46:05 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
ENV GRADLE_VERSION=8.10.2
# Sat, 28 Sep 2024 00:46:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
# Sat, 28 Sep 2024 00:46:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
USER gradle
# Sat, 28 Sep 2024 00:46:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
USER root
```

-	Layers:
	-	`sha256:ef41535c40f05e4212ae6933472799342ac3f01e687718bc7f1bb59e7eb40810`  
		Last Modified: Wed, 05 Jun 2024 03:12:18 GMT  
		Size: 27.0 MB (27013418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4616fbef706655b2aec3e9799581587b3d48a3bfca23b4984ec604fc5fba9135`  
		Last Modified: Wed, 05 Jun 2024 03:13:21 GMT  
		Size: 20.1 MB (20142321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0509cee5fbe81fbad90fc9f8fcd22d5d43e0dd5ad8811944795e2e163472d1b`  
		Last Modified: Tue, 23 Jul 2024 02:42:35 GMT  
		Size: 134.4 MB (134408626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a389f88882a2715261fb14b2fd7190d2782317e71d242f74c0802f230750e3d`  
		Last Modified: Tue, 23 Jul 2024 02:42:24 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab48a4285204310c09a8de68a3895f5c4e2c7a8ab8e2a5a23747f513aafa1ac0`  
		Last Modified: Fri, 23 Aug 2024 19:47:19 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43acb4f78b3d63fe3a980ba8319a88f319009b7e815a584daa19af1159895789`  
		Last Modified: Mon, 30 Sep 2024 22:05:18 GMT  
		Size: 4.3 KB (4324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3cdb289aee0a75a8015da80bf146567139453a32fc1e55074aeb2320ca1440`  
		Last Modified: Mon, 30 Sep 2024 22:05:20 GMT  
		Size: 65.2 MB (65165119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6073031b13105458426336911a2dee54aa9b24debf6269ff205e4e179806820d`  
		Last Modified: Mon, 30 Sep 2024 22:05:21 GMT  
		Size: 136.7 MB (136729733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd03a8cc3b2a1929da6a212155bea051f6c3acb10c54bc3c5003544883669fe7`  
		Last Modified: Mon, 30 Sep 2024 22:05:18 GMT  
		Size: 289.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:focal` - unknown; unknown

```console
$ docker pull gradle@sha256:f56e23eb46fe41a4a2d1390ecbd5d6efa39210142d64ae5545ed2f7c3c98b552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7731736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0b0426aaf4082fc4a5240218d2ed2cb5203d77682a75df04fd0bbf4a4ac7e3`

```dockerfile
```

-	Layers:
	-	`sha256:c9250c1047aab888c54f558f485949aee1d6371eb6a98616da2d475cf918bea5`  
		Last Modified: Mon, 30 Sep 2024 22:05:18 GMT  
		Size: 7.7 MB (7707581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ca427d32c66cc32e0fc21d9d30473433ba63f63ead595848e319014ce2e8c9e`  
		Last Modified: Mon, 30 Sep 2024 22:05:18 GMT  
		Size: 24.2 KB (24155 bytes)  
		MIME: application/vnd.in-toto+json
