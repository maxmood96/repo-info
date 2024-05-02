## `gradle:7-jdk8-focal`

```console
$ docker pull gradle@sha256:ddc6f8c4c0c2516a89f77b66259fcc40ab7d607a7e7a38f7ce1faa0628cdbd41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `gradle:7-jdk8-focal` - linux; amd64

```console
$ docker pull gradle@sha256:a51e43230c76e162df711f6b37fd574bb6b8d72e10c420bae9e823c724f3caa0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.3 MB (337308079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0f6580c14be11008b26e50d8a33cce4c3d3d37c92c4f0c937f861de5a2eb932`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
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
ENV JAVA_VERSION=jdk8u412-b08
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3504d748a93f23cac8c060bd33231bd51e90dcb620f38dadc6239b6cd2a5011c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b9884a96f78543276a6399c3eb8c2fd8a80e6b432ea50e87d3d12d495d1d2808';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='be4aff6fa7bf6515f16f93dcaf9fdc61853fe1ef0d25b08a1bb1cf6e3d047391';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='6b7ed7996788075e182dd33349288346240fbce540e50fd77aecfc309a5ada19';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 02 May 2024 01:22:22 GMT
CMD ["gradle"]
# Thu, 02 May 2024 01:22:22 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 02 May 2024 01:22:23 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Thu, 02 May 2024 01:22:23 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 02 May 2024 01:22:23 GMT
WORKDIR /home/gradle
# Thu, 02 May 2024 01:23:02 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Thu, 02 May 2024 01:28:37 GMT
ENV GRADLE_VERSION=7.6.4
# Thu, 02 May 2024 01:28:37 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Thu, 02 May 2024 01:28:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Thu, 02 May 2024 01:28:42 GMT
USER gradle
# Thu, 02 May 2024 01:28:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Thu, 02 May 2024 01:28:43 GMT
USER root
```

-	Layers:
	-	`sha256:c83baea2d576c50e5cabbc3c34a47fbbbbd18a9230362ba713d603c9686181fb`  
		Last Modified: Sat, 27 Apr 2024 19:03:26 GMT  
		Size: 28.6 MB (28584299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15eb874ca572c30548f8b3ccb6743465ceb027c1547a6159c7e8c0cfd9d2990c`  
		Last Modified: Thu, 02 May 2024 01:15:11 GMT  
		Size: 16.9 MB (16921162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c97ff698c6773943407778d54d3fd482ef05d0c082590a368e1c4c682d1e069`  
		Last Modified: Thu, 02 May 2024 01:15:17 GMT  
		Size: 103.6 MB (103602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b636a3c2676bd576551066e1f4c6c8fbef247a3ac757a4598054ca5a622eb5`  
		Last Modified: Thu, 02 May 2024 01:15:08 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2e733962399af478465628910ec2e68b8830634df5d3b15c39ded1b1e6bbdc`  
		Last Modified: Thu, 02 May 2024 01:15:08 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf71ba2cb70241ab33e2c584e04f576987d6590031f4b04f3454ef1afce8594`  
		Last Modified: Thu, 02 May 2024 01:32:33 GMT  
		Size: 4.4 KB (4358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b456c5b1b83008f7fc6be38d4faeabec80e11a53c351fd1486de0c21da07b7c`  
		Last Modified: Thu, 02 May 2024 01:32:43 GMT  
		Size: 65.5 MB (65464311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c883ae55ef41f672fa2daedc06de41ca2c3e1aedac1013673e453057dd61476`  
		Last Modified: Thu, 02 May 2024 01:38:45 GMT  
		Size: 122.7 MB (122730235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea867b5fbb7be0fe4e87eebebf58ade21d1e64e0d9b05c1910df65526757ac83`  
		Last Modified: Thu, 02 May 2024 01:38:40 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:7-jdk8-focal` - linux; arm variant v7

```console
$ docker pull gradle@sha256:64788a837746497f256a0a13fe6e6e33b53d867a2ed5963eef31871b0109d9a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.4 MB (322385732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d64cbd5970cb899411f2f915d6225c2ab535e690b29e1708c27b868aa18367c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 27 Apr 2024 14:42:50 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:42:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:42:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:42:50 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:43:02 GMT
ADD file:5789980ed37544805bfc38f68255149cf4ceac7689ffcbcf606720b1b7170733 in / 
# Sat, 27 Apr 2024 14:43:03 GMT
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
ENV JAVA_VERSION=jdk8u412-b08
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3504d748a93f23cac8c060bd33231bd51e90dcb620f38dadc6239b6cd2a5011c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b9884a96f78543276a6399c3eb8c2fd8a80e6b432ea50e87d3d12d495d1d2808';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='be4aff6fa7bf6515f16f93dcaf9fdc61853fe1ef0d25b08a1bb1cf6e3d047391';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='6b7ed7996788075e182dd33349288346240fbce540e50fd77aecfc309a5ada19';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 02 May 2024 02:28:34 GMT
CMD ["gradle"]
# Thu, 02 May 2024 02:28:34 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 02 May 2024 02:28:35 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Thu, 02 May 2024 02:28:35 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 02 May 2024 02:28:35 GMT
WORKDIR /home/gradle
# Thu, 02 May 2024 02:28:59 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Thu, 02 May 2024 02:31:27 GMT
ENV GRADLE_VERSION=7.6.4
# Thu, 02 May 2024 02:31:28 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Thu, 02 May 2024 02:31:33 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Thu, 02 May 2024 02:31:33 GMT
USER gradle
# Thu, 02 May 2024 02:31:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Thu, 02 May 2024 02:31:34 GMT
USER root
```

-	Layers:
	-	`sha256:8bc6554297d271d6d4b2d1b92b5a4a9fc067e28e04c1d749f5fa99295fe0b1d9`  
		Last Modified: Thu, 02 May 2024 01:27:40 GMT  
		Size: 24.6 MB (24604686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2646dc3617a1a156c1e540ddc70a7d0d4da53563679b00f5098c31f95b7609fe`  
		Last Modified: Thu, 02 May 2024 01:27:38 GMT  
		Size: 15.7 MB (15666334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:639bb70fcee56a135eb05b4b207880ff40d6cd5f32be388d40572f583e92cee8`  
		Last Modified: Thu, 02 May 2024 01:27:45 GMT  
		Size: 99.2 MB (99230882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18dc2a8b3f5694a21d859662437eb3910560d1b9103c9d96cde8a3dd65a1e697`  
		Last Modified: Thu, 02 May 2024 01:27:36 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d31c90b020369770698de4034057774695e6a0bea221c1882bc9e8953ca9b3c`  
		Last Modified: Thu, 02 May 2024 01:27:36 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83da900bb4f3fd14891a5ce8e2d072cb0f4107936f3d38c6476c3a94d810720b`  
		Last Modified: Thu, 02 May 2024 02:34:45 GMT  
		Size: 4.3 KB (4350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2867a6d8e53381c179d31c66c8a832ddcd9174e2782835dcf1d2a15dfff52d7f`  
		Last Modified: Thu, 02 May 2024 02:34:56 GMT  
		Size: 60.1 MB (60148157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81146ce78968def5e080082bdfd0d74492be0042fc8b5d476e53893cb7a88c1c`  
		Last Modified: Thu, 02 May 2024 02:37:47 GMT  
		Size: 122.7 MB (122730261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457ec766291c7c598c376c8e315ba21e8fff5d1c548b660ea1f45c0bfdf540e1`  
		Last Modified: Thu, 02 May 2024 02:37:41 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:7-jdk8-focal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:f885ce2c5c4eed1fa028dadf1bf4e582e57b5100b06fc87310ef7f4e508fb6e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.7 MB (334693143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6309fd39f88b8607923d92020cd2a234e568bba47ea0a3533e340a632b305ec`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 27 Apr 2024 14:42:15 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:42:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:42:24 GMT
ADD file:d1a4a31f5a3aea1e130c7e173da2ed506ba19e91be74ab9700d398774d0ace22 in / 
# Sat, 27 Apr 2024 14:42:24 GMT
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
ENV JAVA_VERSION=jdk8u412-b08
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3504d748a93f23cac8c060bd33231bd51e90dcb620f38dadc6239b6cd2a5011c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b9884a96f78543276a6399c3eb8c2fd8a80e6b432ea50e87d3d12d495d1d2808';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='be4aff6fa7bf6515f16f93dcaf9fdc61853fe1ef0d25b08a1bb1cf6e3d047391';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='6b7ed7996788075e182dd33349288346240fbce540e50fd77aecfc309a5ada19';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 02 May 2024 06:01:53 GMT
CMD ["gradle"]
# Thu, 02 May 2024 06:01:53 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 02 May 2024 06:01:54 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Thu, 02 May 2024 06:01:54 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 02 May 2024 06:01:54 GMT
WORKDIR /home/gradle
# Thu, 02 May 2024 06:02:35 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Thu, 02 May 2024 06:05:02 GMT
ENV GRADLE_VERSION=7.6.4
# Thu, 02 May 2024 06:05:02 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Thu, 02 May 2024 06:05:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Thu, 02 May 2024 06:05:06 GMT
USER gradle
# Thu, 02 May 2024 06:05:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Thu, 02 May 2024 06:05:07 GMT
USER root
```

-	Layers:
	-	`sha256:83049506c6eb6b11ef1a8774b3486a01a1804f7d13bd230b44788bc63248282d`  
		Last Modified: Mon, 29 Apr 2024 19:12:05 GMT  
		Size: 27.2 MB (27206145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a3510597c9954b37f646e357b476e00ba683391a190199312f9fd3f1344ca2d`  
		Last Modified: Thu, 02 May 2024 04:17:12 GMT  
		Size: 16.8 MB (16777842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eeb42b0c56e081b2510de6a96e0a733cf30196e8e26b7c2383fb2c551d9d66c`  
		Last Modified: Thu, 02 May 2024 04:17:17 GMT  
		Size: 102.7 MB (102704789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ea52a9111bee9997a521418a9f4c35734be36f6aaecc2e1085c3704b32e98b`  
		Last Modified: Thu, 02 May 2024 04:17:09 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad0201e4c3dba9cfc6fdaa94646913498e950a742d31b32be009fb40620ee60`  
		Last Modified: Thu, 02 May 2024 04:17:10 GMT  
		Size: 731.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505dde10679deceb9f82b0f93ea7c7f3c7fa299883d1b5ba426f566a8a820df0`  
		Last Modified: Thu, 02 May 2024 06:08:05 GMT  
		Size: 4.4 KB (4364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:831988e4a30fb5f92f4576cd17881369d8893d4ca448192eefc3c9dd1d27d856`  
		Last Modified: Thu, 02 May 2024 06:08:13 GMT  
		Size: 65.3 MB (65268688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d208724cad4d9dec3230058f918013b618da020ffd11b79303ee1fa7e8ae2d`  
		Last Modified: Thu, 02 May 2024 06:11:47 GMT  
		Size: 122.7 MB (122730253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6029733755b7e3d71731b268dfc2b9948617349912aa5f1d4a6cd01e34fe64ec`  
		Last Modified: Thu, 02 May 2024 06:11:42 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:7-jdk8-focal` - linux; ppc64le

```console
$ docker pull gradle@sha256:05e632ef4411e232b14aafb7e26d0c79fab4b8b4bb9f315d4f0a007576d07c8f
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.2 MB (349182799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ed63f70b067609e35c31820c1a8e73741555a96c6029764bb6002568176460e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 27 Apr 2024 13:33:02 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:33:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:33:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:33:02 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 13:33:06 GMT
ADD file:de463dcd7b30faec6d782106816b443697c99747238015d4d992786da4888987 in / 
# Sat, 27 Apr 2024 13:33:06 GMT
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
ENV JAVA_VERSION=jdk8u412-b08
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3504d748a93f23cac8c060bd33231bd51e90dcb620f38dadc6239b6cd2a5011c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b9884a96f78543276a6399c3eb8c2fd8a80e6b432ea50e87d3d12d495d1d2808';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='be4aff6fa7bf6515f16f93dcaf9fdc61853fe1ef0d25b08a1bb1cf6e3d047391';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='6b7ed7996788075e182dd33349288346240fbce540e50fd77aecfc309a5ada19';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 02 May 2024 05:18:04 GMT
CMD ["gradle"]
# Thu, 02 May 2024 05:18:04 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 02 May 2024 05:18:06 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Thu, 02 May 2024 05:18:06 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 02 May 2024 05:18:07 GMT
WORKDIR /home/gradle
# Thu, 02 May 2024 05:19:21 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Thu, 02 May 2024 05:25:03 GMT
ENV GRADLE_VERSION=7.6.4
# Thu, 02 May 2024 05:25:03 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Thu, 02 May 2024 05:25:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Thu, 02 May 2024 05:25:13 GMT
USER gradle
# Thu, 02 May 2024 05:25:15 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Thu, 02 May 2024 05:25:16 GMT
USER root
```

-	Layers:
	-	`sha256:842f501e2541cf3af2b2c183cb8bc0e8ee178240b7a31e44ca04a5741c69410b`  
		Last Modified: Thu, 02 May 2024 01:51:19 GMT  
		Size: 33.3 MB (33316011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a680bfbe33125da457ff9d39f64548e1fcd6e34c4da44faa1039f934edc56adc`  
		Last Modified: Thu, 02 May 2024 01:51:19 GMT  
		Size: 18.2 MB (18222362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2282a3d984cbc48aa5e0e69a5f04f0de00834ace608b91a4d5a667991fa360c7`  
		Last Modified: Thu, 02 May 2024 01:51:24 GMT  
		Size: 101.1 MB (101070867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74381d03e491a12ca4fbcbd4330710e7d1aa44d372e7e021b133242fec74c2d9`  
		Last Modified: Thu, 02 May 2024 01:51:13 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71d3200a48ac93b5369f004ea67c074dec405ad5954b6b736725ff626fda556`  
		Last Modified: Thu, 02 May 2024 01:51:13 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19821c7e136a0ba4881b8c5fdc8c0179baaf1d86678b4b08e68a2cfb6a2b49f4`  
		Last Modified: Thu, 02 May 2024 05:29:56 GMT  
		Size: 4.4 KB (4361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676a3cf23c966f4f45b077c1654ea7d061f54f1d07cf337ecf0abe9a055044b1`  
		Last Modified: Thu, 02 May 2024 05:30:10 GMT  
		Size: 73.8 MB (73837870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dfd685fe3ce5e16648a52d2b9cec0eee95d82d32825514a778f6dc72f1c6c0f`  
		Last Modified: Thu, 02 May 2024 05:33:13 GMT  
		Size: 122.7 MB (122730262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42593eab4025f7d7702c7bb29293ab6baa46ac7d6d6e6c30fe3a9156fd63db67`  
		Last Modified: Thu, 02 May 2024 05:33:06 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
