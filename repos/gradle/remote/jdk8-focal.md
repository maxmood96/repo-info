## `gradle:jdk8-focal`

```console
$ docker pull gradle@sha256:837c4c0e6ce69de647a9dc1adb7af39ce8062ea510b6a3dc8f15c1d2dc06eba9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `gradle:jdk8-focal` - linux; amd64

```console
$ docker pull gradle@sha256:33eab35bf0146ed7158bf7ab5c758ca067259d43c26a9567777cb8fbd97f402a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.4 MB (351419945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441301fff5f6ec88ab510fbe8bc2da95f1d761cb7c62aed78bff0a6ae2c1d244`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:32 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:34 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Wed, 18 Sep 2024 04:18:34 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:708f64f82dd88cf1254c197fe8a812ffc7c3ebf200e9ac71f489d96160efa1d6`  
		Last Modified: Wed, 18 Sep 2024 06:52:54 GMT  
		Size: 28.6 MB (28583886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b774bb3b629182074f56c4fd66bcbe6c07f5e0078a79dc1520e6715111a73e0`  
		Last Modified: Wed, 02 Oct 2024 02:20:32 GMT  
		Size: 16.9 MB (16934012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dcfdc2e6cd95129b7c303e478b6aa1e5a821d4ca25a07e155766a61c052101e`  
		Last Modified: Wed, 02 Oct 2024 02:20:38 GMT  
		Size: 103.6 MB (103616439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8c65217c75fe0f01024023748acffa174da1ae08416fda739efa124ec766e6`  
		Last Modified: Wed, 02 Oct 2024 02:20:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f3afb445a6b2ca770250fad69d6e9e6862dda9b969404f4a3b740d4e41e26e`  
		Last Modified: Wed, 02 Oct 2024 02:20:29 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ba94a4a872b263c506ea4e7a2ed3cf3397eaef89e8c896b2441e91e953fdde`  
		Last Modified: Wed, 02 Oct 2024 03:56:33 GMT  
		Size: 4.3 KB (4312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73424071095821da9303ef6ddd21ae4083cbc670f86f3c12712253e398f31d79`  
		Last Modified: Wed, 02 Oct 2024 03:56:33 GMT  
		Size: 65.5 MB (65494372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c17a9272616b0b6f5042661e41af09c1f66739798b8a97db236f4766c8f217e`  
		Last Modified: Wed, 02 Oct 2024 03:56:35 GMT  
		Size: 136.7 MB (136729731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce416a8daffc7038c9c3cd5e905a910f1f2915fb1dc175d707b33c9d14880a0`  
		Last Modified: Wed, 02 Oct 2024 03:56:33 GMT  
		Size: 54.9 KB (54903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk8-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:5bc0768dc45dda1dd2ab7e71fb4f8d110104129fe07d43cc0f4d2251350ac4fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4fdcdea653a2c3bb5d3da85e6eedebeebaf5751822333f872b02f70c37dd307`

```dockerfile
```

-	Layers:
	-	`sha256:e2d5ec5348ca507fa614a95d8cc7e0f703a86c77440ca7d11695dda49e1c7cb3`  
		Last Modified: Wed, 02 Oct 2024 03:56:33 GMT  
		Size: 7.8 MB (7753589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17958ad00b22097a845839d43f5b30922923e0daba6c135764399340efc7b7ab`  
		Last Modified: Wed, 02 Oct 2024 03:56:33 GMT  
		Size: 21.7 KB (21687 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk8-focal` - linux; arm variant v7

```console
$ docker pull gradle@sha256:6d13e2eda9c523e3961bd6235cb33ecd4f06e210641dc622f6785c340627d211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.4 MB (336414472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92cd456d345c73479371d9bf6d3b5543a64f1c4e82361da0d9839866ce4f3623`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 28 Sep 2024 00:46:05 GMT
ARG RELEASE
# Sat, 28 Sep 2024 00:46:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 28 Sep 2024 00:46:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 28 Sep 2024 00:46:05 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 28 Sep 2024 00:46:05 GMT
ADD file:f76c848564adfa0c782654cd9423feee0ffacccd95abfe3e4e696203d5e61fbf in / 
# Sat, 28 Sep 2024 00:46:05 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:7474977cdbc1bb838c947dfdfa420a17f877727196fdf929b5bbfb57ddc59d1e`  
		Last Modified: Wed, 16 Oct 2024 01:27:36 GMT  
		Size: 24.6 MB (24600743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5720df978cd4898f2d30c9e693b05c5bfe028f17db83a2a8ebb5ba1a181de336`  
		Last Modified: Wed, 16 Oct 2024 01:33:27 GMT  
		Size: 15.7 MB (15678736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2fe902e12b264c8fa1d4b42703d8c077b9ed6a9c105eebc438ecbd2c142418c`  
		Last Modified: Wed, 16 Oct 2024 01:33:32 GMT  
		Size: 99.2 MB (99249612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6a2a8af8b167e3110f27b9e4ee3f0dfb31137fb0fd1ee329d2e291537a72cf`  
		Last Modified: Wed, 16 Oct 2024 01:33:23 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced787b8eead4a2d70ce19923a82df35bb77a4c35facfcd2f5c056febe3912e8`  
		Last Modified: Wed, 16 Oct 2024 01:33:23 GMT  
		Size: 2.1 KB (2131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af7d6507afa81b2412c7827b1e483e8325d269d17c895daf1d34cb913b7ff85`  
		Last Modified: Wed, 16 Oct 2024 02:11:44 GMT  
		Size: 4.3 KB (4294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d591e12ed3ea2ab1b2b1308462378538bae1d723ed0ba442e9f34590aa7cfe`  
		Last Modified: Wed, 16 Oct 2024 02:11:46 GMT  
		Size: 60.1 MB (60148776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e08c4c5b198d743b282f1f78cfdcdfbde6a630b4d542c7241137976802aaa6`  
		Last Modified: Wed, 16 Oct 2024 02:11:48 GMT  
		Size: 136.7 MB (136729734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a11e19ffb0307c5204926b9f53099de0cfa309f0cac9bc3f2a79f70ad5e2bc4`  
		Last Modified: Wed, 16 Oct 2024 02:11:45 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk8-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:3daa0df8cccd876fd73de703451a3c0c42a9539346cf6652ff3fdf52bd3b3181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7780509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09c6e6b6ae5a50f3bbe818096433af0c3df3efeac421f16676de13fe2f56d55`

```dockerfile
```

-	Layers:
	-	`sha256:beedf540430ea4a9e0ddbd4037650a66566ecd7e4fbbb3b867ea2be69d06ed03`  
		Last Modified: Wed, 16 Oct 2024 02:11:43 GMT  
		Size: 7.8 MB (7758687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51f4b18700f5ad3b66e2d04632748bf6cc2b24a28983e6de84f6df1a17f8d635`  
		Last Modified: Wed, 16 Oct 2024 02:11:43 GMT  
		Size: 21.8 KB (21822 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk8-focal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:9326498e96fc8651074c258e8bf88d0093bc0ee16ab2f6c2d0593aa383028677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.8 MB (348813585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be87c0dc562bc49a45c1daa464b7050b294e749a665d0aa2086c98a9cba91f9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 28 Sep 2024 00:46:05 GMT
ARG RELEASE
# Sat, 28 Sep 2024 00:46:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 28 Sep 2024 00:46:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 28 Sep 2024 00:46:05 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 28 Sep 2024 00:46:05 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Sat, 28 Sep 2024 00:46:05 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:963ceec6c2ca13b343a25d3157e3e30ffa80fc297ad5e3f78d8f43087427b2d3`  
		Last Modified: Sat, 12 Oct 2024 07:30:30 GMT  
		Size: 27.2 MB (27204259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d2e9d896341dc2470e5877241905d4df074cef3aed1d0a5b7c9b27fcfb590a`  
		Last Modified: Wed, 16 Oct 2024 01:15:36 GMT  
		Size: 16.8 MB (16789035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fde0d98287038c3305255d715400951b85049ada5a8e85ec1f010acba0f16b`  
		Last Modified: Wed, 16 Oct 2024 01:15:41 GMT  
		Size: 102.7 MB (102733745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18de9c40ac0ad1ca090ddc9d6355157141f85bd4ecd1a50d7e9c0c71e4df3fd`  
		Last Modified: Wed, 16 Oct 2024 01:15:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f1576606d840849742fa033f5bac5b9d25aaf202cd019094c8e9c1411e6ac1`  
		Last Modified: Wed, 16 Oct 2024 01:15:34 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3a45efb68d3493a6419ae71c80b2673128373cca6535b5a749f3105f66f579`  
		Last Modified: Wed, 16 Oct 2024 02:50:14 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eaec6c1451f761b86cc5ad20f274862452362ab5805ec0e6754bcb6cd02b38b`  
		Last Modified: Wed, 16 Oct 2024 02:50:16 GMT  
		Size: 65.3 MB (65290707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7193d2ef925c305be37604675381a36193576ee1e086c70c29ac9bbedf5a51f3`  
		Last Modified: Wed, 16 Oct 2024 02:50:18 GMT  
		Size: 136.7 MB (136729714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b53ea661c699a5155826c1b88e479931059a8f797e23e1501cab6afa9d47b0f`  
		Last Modified: Wed, 16 Oct 2024 02:50:15 GMT  
		Size: 59.5 KB (59521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk8-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:453352f19944d118d3edc21497dc41624581f58f22ba060f3ea379122826adcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7781986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10287c14c90768b871dbec9b2287bfbcc7ec119e9ed09842cd22ab6abf5605f2`

```dockerfile
```

-	Layers:
	-	`sha256:8b30123c26840dc0afdf2ec2b1dc10846acf3ae8b229e59254b594de8697f7b1`  
		Last Modified: Wed, 16 Oct 2024 02:50:13 GMT  
		Size: 7.8 MB (7760122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7047fdd4d2f2e1917df21f9c9b392158a47c3899f3df0bd9ba17902349554ca5`  
		Last Modified: Wed, 16 Oct 2024 02:50:13 GMT  
		Size: 21.9 KB (21864 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk8-focal` - linux; ppc64le

```console
$ docker pull gradle@sha256:fc145c6b386de10c09f08a5f27a937e02bb320f22cc66dee3686de7ba1bf5d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.2 MB (363231501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e00ce223104cebe58b232a20294b6e558519fc3bddd7912fb2f018f64071a1e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 18 Sep 2024 04:19:24 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:19:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:19:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:19:24 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:19:28 GMT
ADD file:c6515e5ea6494efa348e1177d50c0c28bb8236a5d2b518388f13b7d5a528d4fd in / 
# Wed, 18 Sep 2024 04:19:28 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:92ebc0bf195e4cfb272e0c863b69e6327a1601581a197046391e118d61fc5c6c`  
		Last Modified: Wed, 02 Oct 2024 01:54:32 GMT  
		Size: 33.3 MB (33315563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94e066e8839b320e9bf6923305661b21e2687d1563b765f6651d10de2cd3666`  
		Last Modified: Wed, 02 Oct 2024 02:05:33 GMT  
		Size: 18.2 MB (18241400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec7e669827e4c05a43259153afee370330fdd0375d272bdaa136da33f90ad3e`  
		Last Modified: Wed, 02 Oct 2024 02:05:37 GMT  
		Size: 101.1 MB (101080054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea743d760842be0902d4a393b64121784ef42be950894a5fcff565d036d122f`  
		Last Modified: Wed, 02 Oct 2024 02:05:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f90a7926c67c9766ecdcb4380d8e90e93f2fa477239305d4e2548f7deb874d`  
		Last Modified: Wed, 02 Oct 2024 02:05:28 GMT  
		Size: 2.1 KB (2130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec2127b436f6c174e01c80d096e1ef9f3ab8f065cad1f65d9f12b0f38706b58`  
		Last Modified: Wed, 02 Oct 2024 03:32:11 GMT  
		Size: 4.3 KB (4309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62dc71735b6a3a1dbe08d1ff37f0f5340ee8421bc0f447efa07dcb811a9ddd34`  
		Last Modified: Wed, 02 Oct 2024 03:32:14 GMT  
		Size: 73.9 MB (73857883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c233c2453e5c0860bc53ab31b3cb0dd93d2ae8db3a6bef9e5292d612fef44a`  
		Last Modified: Wed, 02 Oct 2024 03:32:16 GMT  
		Size: 136.7 MB (136729712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df76aeec4ee9354ece2e54c0080f1642b79a3b193b285c33ad61c768dbddb73`  
		Last Modified: Wed, 02 Oct 2024 03:32:12 GMT  
		Size: 290.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk8-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:cf67f6a5792661e6d3ec1ba0008da2f54631e462a7ec854e22a2925adf07e7db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7781256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce393dfc332ea3c0b739099ed3d1c4ca738725503a68fad977892730976bc03f`

```dockerfile
```

-	Layers:
	-	`sha256:d2c3c2d215b09aa23f083f9bdb710b7a16820ebbc8eaa9496418a7298c753861`  
		Last Modified: Wed, 02 Oct 2024 03:32:10 GMT  
		Size: 7.8 MB (7759526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e806bc5f65649298f0cac9fd5d6400d4bfffac002fdadf41f5b7e7315aba897e`  
		Last Modified: Wed, 02 Oct 2024 03:32:09 GMT  
		Size: 21.7 KB (21730 bytes)  
		MIME: application/vnd.in-toto+json
