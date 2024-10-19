## `gradle:7-jdk11-focal`

```console
$ docker pull gradle@sha256:bdb2fe77bc36f757b4a0d24711499e68466c1922e1d301d42a12ad78038c5a26
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

### `gradle:7-jdk11-focal` - linux; amd64

```console
$ docker pull gradle@sha256:ac05833f72c8f26419bcb3cf8117bd19b9abd1138562fc456c414e51ee0fac76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.3 MB (378290004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d88ade5c3cb376cc54e9dd8b3df1e5bd01db881d8f79da872e919a32f3732000`
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
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Feb 2024 22:05:50 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
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
ENV JAVA_VERSION=jdk-11.0.24+8
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e71a01563a5c7b9988a168b0c4ce720a6dff966b3c27bb29d1ded461ff71d0e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='04e21301fedc76841fb03929ac6cacfbbda30b5693acfd515a8f34d4a0cdeb28';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='9d14a076d1440161ab4c9736644e8e9f4719eb8e9f44c03470640960c3cd5e00';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='4dfdc498938a159c592a2f094576f09c94999e17327c1f5ff81794694992054d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='7f049af5d3ff8794d07da1c31752e18e204653930f1d422e2d42905c90c1c408';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d73e7b18f39c1ce533e99dc4bb9197d29ad9b0848e2ac07b0d6f26210e9956d`  
		Last Modified: Sat, 19 Oct 2024 02:06:44 GMT  
		Size: 16.9 MB (16931683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bacfb683a3291c3373af19d24e4a4ef71d347e5e04276609553f0f7b0713d88`  
		Last Modified: Sat, 19 Oct 2024 02:06:46 GMT  
		Size: 145.6 MB (145558068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf33e4fcca9d478292b083ea7add7e2a9f46e4a3a7bf25ac8debdfc39c0a3fed`  
		Last Modified: Sat, 19 Oct 2024 02:06:44 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe65af51e61751d7c21a8a50cd1d1e8470bbbe64a8483b21fa5ff42a94621bd`  
		Last Modified: Sat, 19 Oct 2024 02:06:44 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d107534a5aac84f3540642e1ec27edf97d3db3134f961f27caae6b9ca35fd3`  
		Last Modified: Sat, 19 Oct 2024 02:53:24 GMT  
		Size: 4.3 KB (4308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7e9031dc4d61e2d5b0b4e947897fb0e9f9620fe419f64fec0410a13da1a2d7`  
		Last Modified: Sat, 19 Oct 2024 02:53:26 GMT  
		Size: 65.5 MB (65497157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d3980e889b2d8accbcec58da0d54c9dc067bfa8f76847f7581d34e3151ee90`  
		Last Modified: Sat, 19 Oct 2024 02:53:26 GMT  
		Size: 122.7 MB (122730525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fdb6eacc767796e58245581df63e313391e7b2668f1636b4c730f868aa66e8`  
		Last Modified: Sat, 19 Oct 2024 02:53:24 GMT  
		Size: 54.9 KB (54905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:98e06fc36592b91d5f7708086dace943abb2408cc8383ccfb1fb7777a73b2cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7646939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67f7636330294f8e2bc2e22bcfbfbde649e9f4a9d6d560c51bfa45d8c133b87c`

```dockerfile
```

-	Layers:
	-	`sha256:26469af534faee7ec4e2d579d3201c9ba0a32a7ceefdc3da1747b570d8bc7ce0`  
		Last Modified: Sat, 19 Oct 2024 02:53:25 GMT  
		Size: 7.6 MB (7625526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74b20b7ffd10b565d2a2c3a5eb4b6527e8e075651592711ef61945ab7a326aaa`  
		Last Modified: Sat, 19 Oct 2024 02:53:24 GMT  
		Size: 21.4 KB (21413 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk11-focal` - linux; arm variant v7

```console
$ docker pull gradle@sha256:bb48c3f11e43cbdb332a5516ea3e11975e2025e1e7efeb12fd5bd3277ff73588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.3 MB (360256657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5300484c424612e09b38f31467b23cab0955994ed8eb723b0da7369a886323`
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
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Feb 2024 22:05:50 GMT
ADD file:f76c848564adfa0c782654cd9423feee0ffacccd95abfe3e4e696203d5e61fbf in / 
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
ENV JAVA_VERSION=jdk-11.0.24+8
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e71a01563a5c7b9988a168b0c4ce720a6dff966b3c27bb29d1ded461ff71d0e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='04e21301fedc76841fb03929ac6cacfbbda30b5693acfd515a8f34d4a0cdeb28';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='9d14a076d1440161ab4c9736644e8e9f4719eb8e9f44c03470640960c3cd5e00';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='4dfdc498938a159c592a2f094576f09c94999e17327c1f5ff81794694992054d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='7f049af5d3ff8794d07da1c31752e18e204653930f1d422e2d42905c90c1c408';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
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
	-	`sha256:10b337d353b3ceaf6823ab2d8696989401feed741b22eb313c8a0cd378762d39`  
		Last Modified: Fri, 11 Oct 2024 04:41:36 GMT  
		Size: 23.6 MB (23620412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f6da1c0cd70ff8def0afc476602312ab72c48c692e501fb298e735407a9759`  
		Last Modified: Sat, 19 Oct 2024 06:49:10 GMT  
		Size: 15.7 MB (15678763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b6dd8f752a4d3fc36fcd071a726fcd782ccd1b4a486432c99b0b56aae2e81d4`  
		Last Modified: Sat, 19 Oct 2024 06:56:40 GMT  
		Size: 138.0 MB (138037300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad0c1fc2efe23da4f6ed03dc2735941940fcfc5a79bce51bb2f559e3c437096`  
		Last Modified: Sat, 19 Oct 2024 06:56:36 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8885286648abdf89e6de89e8d6cecd9cfe94535828f09dc114d972575fece803`  
		Last Modified: Sat, 19 Oct 2024 06:56:36 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9324d78e97c9c932c005dafe0ba231014368bb4289d35f537aa0ff5bf5e70e1e`  
		Last Modified: Sat, 19 Oct 2024 08:34:22 GMT  
		Size: 4.3 KB (4297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2c5a5201b65831e70885ead1dda48362c812171ad4b603236dfa507500dfd3`  
		Last Modified: Sat, 19 Oct 2024 08:34:24 GMT  
		Size: 60.2 MB (60151757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76bc32055ace9a2317909ba7916592f51da6fa1398ca761aadd4522dee1d325`  
		Last Modified: Sat, 19 Oct 2024 08:45:39 GMT  
		Size: 122.7 MB (122730527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7601cf1cad0e42e9b8e19789773d3c1e2054d5ff9e480cad5638b0739cb58c21`  
		Last Modified: Sat, 19 Oct 2024 08:45:35 GMT  
		Size: 31.3 KB (31301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:218a0ab9c8f6ce14cba13bf57f7a10b71f1d0ff9e650b97ce259c91d2928beb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7649584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b5943df67249aafc96c289ee558decb1db4b0b5d8d27fc55d4b7711adf26cd`

```dockerfile
```

-	Layers:
	-	`sha256:12be2c10f2984af03984421280be042307a42423335a2c7c93b42a0d4db05b29`  
		Last Modified: Sat, 19 Oct 2024 08:45:36 GMT  
		Size: 7.6 MB (7628064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ebdf3d85c3a30412dea242ad88408a86e0a5de1eaa8d606e2f03654646133e6`  
		Last Modified: Sat, 19 Oct 2024 08:45:35 GMT  
		Size: 21.5 KB (21520 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk11-focal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:ecea36e1bdf38ea9b35178c0138f3f4a085b8d52cd76c55ed52df5f3e1edf7fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.2 MB (373211771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1ab4516b332d1be05fb5cc2b8d86b589c85033f7f5c0ab8abfeee5723090d5`
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
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Feb 2024 22:05:50 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
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
ENV JAVA_VERSION=jdk-11.0.24+8
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e71a01563a5c7b9988a168b0c4ce720a6dff966b3c27bb29d1ded461ff71d0e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='04e21301fedc76841fb03929ac6cacfbbda30b5693acfd515a8f34d4a0cdeb28';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='9d14a076d1440161ab4c9736644e8e9f4719eb8e9f44c03470640960c3cd5e00';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='4dfdc498938a159c592a2f094576f09c94999e17327c1f5ff81794694992054d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='7f049af5d3ff8794d07da1c31752e18e204653930f1d422e2d42905c90c1c408';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711fd1dcf6308def8083b3a50d8d51b4c2287f2541f89a3d1f81037c6175a179`  
		Last Modified: Sat, 19 Oct 2024 05:26:18 GMT  
		Size: 16.8 MB (16787577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb347cf060800f2ae143ecdf8db248fe6b7922c17df1a63816727e9f345c5e82`  
		Last Modified: Sat, 19 Oct 2024 05:30:35 GMT  
		Size: 142.4 MB (142359212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11cdb3693501bd1bef7e0e2eccba152770f16b0798f4cd1174990f3f8b7a576`  
		Last Modified: Sat, 19 Oct 2024 05:30:32 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9c50221555aebf819e22346186c997339b31ce9647bcaa9761fb732756ed6e`  
		Last Modified: Sat, 19 Oct 2024 05:30:32 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951957d396d331085b51191462e397adc07de121965640bdcf79d764cb9a8a00`  
		Last Modified: Sat, 19 Oct 2024 07:05:02 GMT  
		Size: 4.3 KB (4312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d34ce686ac3ae0494a45aacdb6ad512ec7b66f5ca0ec82d3269a942ac7a9a5`  
		Last Modified: Sat, 19 Oct 2024 07:05:04 GMT  
		Size: 65.3 MB (65294481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8cc8ef580df2c3afee076dffcdb7fa87876097aa230df38e232ec2a1a211ee9`  
		Last Modified: Sat, 19 Oct 2024 07:17:54 GMT  
		Size: 122.7 MB (122730529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08e7456962f390c4efb0f41098e9f31ebd68b7ec9065f66585dc9bedd8ef889`  
		Last Modified: Sat, 19 Oct 2024 07:17:51 GMT  
		Size: 59.5 KB (59533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:c1878daa5866f494251bd63d63299c9dec010b9827fe4ae59861d1eab0d47452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7653513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72c9f630ff2db2083567f132964c5ba6829f3762b7b909c65a25eefbc556a698`

```dockerfile
```

-	Layers:
	-	`sha256:810d52da58f2659e38480bb19f05e09552bfd91a534c362a9dbc5cd1955c08b4`  
		Last Modified: Sat, 19 Oct 2024 07:17:51 GMT  
		Size: 7.6 MB (7631963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59c7be7a346dd8daab778ce45762f7891c8d1c52f9d7ff8b1d8f6525dd1708d8`  
		Last Modified: Sat, 19 Oct 2024 07:17:51 GMT  
		Size: 21.6 KB (21550 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk11-focal` - linux; ppc64le

```console
$ docker pull gradle@sha256:c01c1cd2ef5571674ba4dc31b4d28bb029da7aaf1c50b7104be85a504fcd7532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.7 MB (379701952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de606208df2f914c57d7206cbfcd115a5f69a56b4384c35e4d7d016adc1ccb21`
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
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Feb 2024 22:05:50 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
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
ENV JAVA_VERSION=jdk-11.0.24+8
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e71a01563a5c7b9988a168b0c4ce720a6dff966b3c27bb29d1ded461ff71d0e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='04e21301fedc76841fb03929ac6cacfbbda30b5693acfd515a8f34d4a0cdeb28';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='9d14a076d1440161ab4c9736644e8e9f4719eb8e9f44c03470640960c3cd5e00';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='4dfdc498938a159c592a2f094576f09c94999e17327c1f5ff81794694992054d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='7f049af5d3ff8794d07da1c31752e18e204653930f1d422e2d42905c90c1c408';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
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
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d82d180d2a71e9810b37a59c605f26d958a89f42ca8d64d57bdd44918cac352`  
		Last Modified: Sat, 19 Oct 2024 04:17:06 GMT  
		Size: 18.2 MB (18240226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8136cfba792a2034d3e8b941392f8405e8239517c53656c956008c705025e0c8`  
		Last Modified: Sat, 19 Oct 2024 04:24:03 GMT  
		Size: 132.8 MB (132755707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0545ac649da533aa5ffe02a79fb387a7da1b96edb0bade9d6c9df823b2084ae`  
		Last Modified: Sat, 19 Oct 2024 04:24:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9670aafd68ca88b2976dac91ce904bd9c932d30bd62f0a11db3fa37858acd07d`  
		Last Modified: Sat, 19 Oct 2024 04:24:00 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f98d927c1ab74142f0ceaa50150eb3b5e1288269d29dcdf3727fa10409d0ce7`  
		Last Modified: Sat, 19 Oct 2024 08:44:17 GMT  
		Size: 4.3 KB (4305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2991f08500cd53632e3ad7548e28307a4d47a8205cf57bf7d6ac52548c1abd1`  
		Last Modified: Sat, 19 Oct 2024 08:44:20 GMT  
		Size: 73.9 MB (73857369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44907ec095b6ceb79784860c8003b4aa612d21e36e4f3e75160ce9d08c65484`  
		Last Modified: Sat, 19 Oct 2024 09:03:58 GMT  
		Size: 122.7 MB (122730530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ee1ae64e9f3c27dffd492e0fdd4b4eebae4069e98fcb2535c835dd94f72844`  
		Last Modified: Sat, 19 Oct 2024 09:03:54 GMT  
		Size: 35.0 KB (35008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:4577ac007ed0e1c8427a63f5f3ddbe9489838af05514d3b9ded2517e63927143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7651693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ce6c10407acbbf0a09862800f5e59289b1568fc782ec3eeff4bb54cb45e51f3`

```dockerfile
```

-	Layers:
	-	`sha256:f01157b3939b4479b2ba32e8f2ad81868e10cde439ed2e608312ded44fe7df11`  
		Last Modified: Sat, 19 Oct 2024 09:03:55 GMT  
		Size: 7.6 MB (7630236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71005d44d75d63532cad41a53b722aaead58d9aee8eabc52a4b683d2e58fb1f3`  
		Last Modified: Sat, 19 Oct 2024 09:03:54 GMT  
		Size: 21.5 KB (21457 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk11-focal` - linux; s390x

```console
$ docker pull gradle@sha256:671bc2579d706f3edca74359c41e7871fceb06de86e383ab14835feb80f0b47b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.2 MB (356160722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089c9caf950e09395b0fd89d402f079fcb8d9b94968e13eb59a41480a988737d`
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
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Feb 2024 22:05:50 GMT
ADD file:e3e9bad1c3576edf8ddea2dd7af2ed8ecac1ad0b15d714dd9c51f679d44d13b6 in / 
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
ENV JAVA_VERSION=jdk-11.0.24+8
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e71a01563a5c7b9988a168b0c4ce720a6dff966b3c27bb29d1ded461ff71d0e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='04e21301fedc76841fb03929ac6cacfbbda30b5693acfd515a8f34d4a0cdeb28';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='9d14a076d1440161ab4c9736644e8e9f4719eb8e9f44c03470640960c3cd5e00';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='4dfdc498938a159c592a2f094576f09c94999e17327c1f5ff81794694992054d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='7f049af5d3ff8794d07da1c31752e18e204653930f1d422e2d42905c90c1c408';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 05 Feb 2024 22:05:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
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
	-	`sha256:f6b14778eb4fed5cbb0bd80eea19d48526571f3b2dfa0196faf63f42fdb8c6c2`  
		Last Modified: Fri, 11 Oct 2024 04:41:53 GMT  
		Size: 26.4 MB (26365979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f788a32fd814318b0a9245d8d09c2dd8cf3432170360599689d82fc11b2ef1`  
		Last Modified: Sat, 19 Oct 2024 03:54:05 GMT  
		Size: 16.7 MB (16666958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f08449fe12d165058b114705e73615cdca877777929b0abeeaced9e7be7445`  
		Last Modified: Sat, 19 Oct 2024 03:54:07 GMT  
		Size: 125.5 MB (125526993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e33eb458e77e4a2be194c24262d5d7936d831e4df8996030fe599a5d78edecf`  
		Last Modified: Sat, 19 Oct 2024 03:54:05 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0608f8bdc9929a574e1c0251035a21d3816c1dbc12049d396cbbcd85095c6461`  
		Last Modified: Sat, 19 Oct 2024 03:54:05 GMT  
		Size: 2.1 KB (2110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf7c48141ddb6b08293a6f2128865a59dc3c739e5cfd7ba6ef1706b91f36357`  
		Last Modified: Sat, 19 Oct 2024 05:21:28 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0a69412a0775fa9195b7a95437857e28934f2017e602d0065dce3e829d8d03`  
		Last Modified: Sat, 19 Oct 2024 05:21:29 GMT  
		Size: 64.8 MB (64828648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8808638f8696ef6bccb0d65565fc6613e992832ec9c925508eefa4def109f7eb`  
		Last Modified: Sat, 19 Oct 2024 05:37:32 GMT  
		Size: 122.7 MB (122730530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e4e47393eca62a410944467ce2d44da581d202a86765fb305dfa8e576d821af`  
		Last Modified: Sat, 19 Oct 2024 05:37:30 GMT  
		Size: 35.0 KB (35002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:793fb81612953be25ec95824b5e7c70cd2c269c4e625d1723feb363989bc36da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7641990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ba348f88a5a059706e38e47b0c597191b12e111511b25f1f6604d926e459ca`

```dockerfile
```

-	Layers:
	-	`sha256:1c2a34df7dc44b5a5569fc48fbe57184ff6952139d5e10a2fb5bc1d7e9a046a9`  
		Last Modified: Sat, 19 Oct 2024 05:37:30 GMT  
		Size: 7.6 MB (7620577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dfc143ab06380801a0ce0ae08966779ded299d6cc654ee075379eca9620fd9b`  
		Last Modified: Sat, 19 Oct 2024 05:37:30 GMT  
		Size: 21.4 KB (21413 bytes)  
		MIME: application/vnd.in-toto+json
