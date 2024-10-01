## `gradle:jdk23`

```console
$ docker pull gradle@sha256:cb2cf03cbe3ebdd3ac31c79e94732c0b6c3ab5a33b66b6da0b55484ef92d4539
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `gradle:jdk23` - linux; amd64

```console
$ docker pull gradle@sha256:42aeb9b7851d6efa73cbc522f935d26638b2c85b9bcd2e38fae7644b5f5b8891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.8 MB (418807046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c074813f6a5bcce4cbf115adc34ccd6dce495170eb644b3ed5e96f6d95f69e74`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:01 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:03 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Tue, 27 Aug 2024 15:55:03 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Sep 2024 19:12:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 19:12:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_VERSION=jdk-23+37
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='630c4f3870056e7e005736ec1edc34ee63a9b45e2027582c52f53a9bf44314b8';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_x64_linux_hotspot_23_37.tar.gz';          ;;        arm64)          ESUM='e8043d1bd9c4f42c5cf7883aca1fc3ef6bcccf4a664f378818ac0fd4fb987b7e';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_aarch64_linux_hotspot_23_37.tar.gz';          ;;        ppc64el)          ESUM='4d3b0609c783dea1f6a899bfc8c84b4000d1f48f39e2489d70050bbf2c7f7d9c';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_ppc64le_linux_hotspot_23_37.tar.gz';          ;;        riscv64)          ESUM='d401699a92469de7bfb72909c1d11019537a0a2c21af01a8dce1831f09ef5165';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_riscv64_linux_hotspot_23_37.tar.gz';          ;;        s390x)          ESUM='2f9cb1db72ddc91f0b90904d038bca9314bc0bafedb0efe1233469bf3c934e58';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_s390x_linux_hotspot_23_37.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 18 Sep 2024 19:12:13 GMT
CMD ["jshell"]
# Sat, 28 Sep 2024 00:46:05 GMT
CMD ["gradle"]
# Sat, 28 Sep 2024 00:46:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 28 Sep 2024 00:46:05 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
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
	-	`sha256:32b824d45c6101d459f5d3c13ab8658b6f79713f3bd64e363d3f6bc98faf5d6d`  
		Last Modified: Tue, 27 Aug 2024 21:43:22 GMT  
		Size: 30.6 MB (30611547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d10ed217d47bf9ca7ed4ff10640027072814de6488661774d73baf109c03a0`  
		Last Modified: Tue, 17 Sep 2024 01:12:29 GMT  
		Size: 20.2 MB (20240501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f1b82e6dca90d5ded9bedc221500b61ec8601961fff512d0d14453eff726da4`  
		Last Modified: Wed, 18 Sep 2024 21:24:49 GMT  
		Size: 165.3 MB (165273656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd57c419bb00193e4098bc3828afd4fd0f10fc88fa7657b9a0d4e6205fd1546b`  
		Last Modified: Wed, 18 Sep 2024 21:24:37 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c38f91104db881766ac239926faf86b52974a7f57f655e80bf75e60d719937`  
		Last Modified: Wed, 18 Sep 2024 21:24:37 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e5e9efdcc6d2e0d7d533968e01fe893105ea55ab02bb389410849fec516b44`  
		Last Modified: Mon, 30 Sep 2024 21:56:25 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b6135525a4df4e3878864f9b5c7172cc242c9966a414727d57774af9f3a9d3`  
		Last Modified: Mon, 30 Sep 2024 21:56:28 GMT  
		Size: 65.9 MB (65893240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7079cf2c35a1cf389580ba87983496972985c3cd02047f63f6fc8619083f60d6`  
		Last Modified: Mon, 30 Sep 2024 21:56:29 GMT  
		Size: 136.7 MB (136729638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f273cf0bf469a94c6e89a4506f79b4247d469815c78bb1da4a01ef0d9afb9044`  
		Last Modified: Mon, 30 Sep 2024 21:56:25 GMT  
		Size: 54.9 KB (54890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk23` - unknown; unknown

```console
$ docker pull gradle@sha256:2403d7dfc37e008c0a2688f0e00e5b0df762857f02aa1ce5964588daa6a7aa8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6999747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ef9f7fd180f7a2717b878fdc210bf1cfe7f8427184c302a5c41b492b00d5a9`

```dockerfile
```

-	Layers:
	-	`sha256:88ff61a668af8dc818f0fbc0b6661e92b1a919fef6202fef854df892f34c2f8e`  
		Last Modified: Mon, 30 Sep 2024 21:56:25 GMT  
		Size: 7.0 MB (6976627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3f980403b18feb8334d5959ee35820d7731f9eea4f86c620ffa7f40d7fae29a`  
		Last Modified: Mon, 30 Sep 2024 21:56:25 GMT  
		Size: 23.1 KB (23120 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk23` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:b763bd115431bdfb2f6bb97a4ca51ace64b21de222b12f4e3a9be31a66923bab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.6 MB (416613691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72909ccf4382c56304c01d00a41df5c5007c9663a73fcb7931bd77d02e09d7fb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:18 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:18 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:20 GMT
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
# Tue, 27 Aug 2024 15:55:20 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Sep 2024 19:12:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 19:12:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_VERSION=jdk-23+37
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='630c4f3870056e7e005736ec1edc34ee63a9b45e2027582c52f53a9bf44314b8';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_x64_linux_hotspot_23_37.tar.gz';          ;;        arm64)          ESUM='e8043d1bd9c4f42c5cf7883aca1fc3ef6bcccf4a664f378818ac0fd4fb987b7e';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_aarch64_linux_hotspot_23_37.tar.gz';          ;;        ppc64el)          ESUM='4d3b0609c783dea1f6a899bfc8c84b4000d1f48f39e2489d70050bbf2c7f7d9c';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_ppc64le_linux_hotspot_23_37.tar.gz';          ;;        riscv64)          ESUM='d401699a92469de7bfb72909c1d11019537a0a2c21af01a8dce1831f09ef5165';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_riscv64_linux_hotspot_23_37.tar.gz';          ;;        s390x)          ESUM='2f9cb1db72ddc91f0b90904d038bca9314bc0bafedb0efe1233469bf3c934e58';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_s390x_linux_hotspot_23_37.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 18 Sep 2024 19:12:13 GMT
CMD ["jshell"]
# Sat, 28 Sep 2024 00:46:05 GMT
CMD ["gradle"]
# Sat, 28 Sep 2024 00:46:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 28 Sep 2024 00:46:05 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
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
	-	`sha256:8a9c853c85e5a53a79f6bc6965cf01799f75bd947d761fc492da5738058f87a2`  
		Last Modified: Sat, 31 Aug 2024 18:28:27 GMT  
		Size: 30.0 MB (29953205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f02ad8447dcf59fc9ef25fc568cda52894bb2a96c76b7f358195ad4e5017b2`  
		Last Modified: Tue, 17 Sep 2024 01:41:57 GMT  
		Size: 21.2 MB (21221253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c400e3103ef0396967e9b24e467a87ee04b154df1374c55689d330ad15b2ccf`  
		Last Modified: Wed, 18 Sep 2024 21:43:21 GMT  
		Size: 163.3 MB (163256308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706f0f10a4d7b72d89ff2ecd09a11a772dea6bf751b942c91dba7a7294c9b124`  
		Last Modified: Wed, 18 Sep 2024 21:43:10 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b8975ca679c78b149dcddd8d3becc199289fa1b567c9b88b58482aed7d162c`  
		Last Modified: Wed, 18 Sep 2024 21:43:10 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49908d2754f775ffc384fac6c574ee1a7c89345f87583db7fbbb79b2b135df8b`  
		Last Modified: Mon, 30 Sep 2024 22:08:02 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3dbcc1dbf037bd6dfb781d4368c418b817642e09fcbdd2c151be4319e0d8f41`  
		Last Modified: Mon, 30 Sep 2024 22:08:04 GMT  
		Size: 65.4 MB (65390087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32372cd838e9143bce7005969d4f05805ea7ce600544a29186927fc795969bb`  
		Last Modified: Mon, 30 Sep 2024 22:08:05 GMT  
		Size: 136.7 MB (136729735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bccb8aefbbf5f7c2ead92fb2e6cfe665f0c63388f0a0b2a9793fd364307c5e`  
		Last Modified: Mon, 30 Sep 2024 22:08:02 GMT  
		Size: 59.5 KB (59530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk23` - unknown; unknown

```console
$ docker pull gradle@sha256:1b0c7722761b035a72acf6bd8ac897f89c6b0dd70d987aa9da3029e6b504f607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7137377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a26f9f1007d54fc60e3fd0d9d7bbcb93003b635314e540cb10fc415912b116`

```dockerfile
```

-	Layers:
	-	`sha256:85c852b937f0ebeb630e98193e5d547121d6c76ebff1110b6ec08c156fa615da`  
		Last Modified: Mon, 30 Sep 2024 22:08:02 GMT  
		Size: 7.1 MB (7113892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a84d657050bfd7bae7c92c56dc1ed005b70a81ac5aab440c32260fbbedf57d1`  
		Last Modified: Mon, 30 Sep 2024 22:08:02 GMT  
		Size: 23.5 KB (23485 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk23` - linux; ppc64le

```console
$ docker pull gradle@sha256:28e08d1d11baa3a9fea65f741bf9d03e0a55e9bfb907a55d645581d16b1c8bde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.6 MB (429574248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed8ea50d452693dbeea9cf1213a268f23f69c0494cf2654ecb9a691536a8d15`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 27 Aug 2024 15:56:25 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:56:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:56:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:56:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:56:28 GMT
ADD file:c70c2393dc0404f71d25ae70ab08b5aa65e46753a6169cfd4f5554c942cc0218 in / 
# Tue, 27 Aug 2024 15:56:29 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Sep 2024 19:12:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 19:12:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_VERSION=jdk-23+37
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='630c4f3870056e7e005736ec1edc34ee63a9b45e2027582c52f53a9bf44314b8';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_x64_linux_hotspot_23_37.tar.gz';          ;;        arm64)          ESUM='e8043d1bd9c4f42c5cf7883aca1fc3ef6bcccf4a664f378818ac0fd4fb987b7e';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_aarch64_linux_hotspot_23_37.tar.gz';          ;;        ppc64el)          ESUM='4d3b0609c783dea1f6a899bfc8c84b4000d1f48f39e2489d70050bbf2c7f7d9c';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_ppc64le_linux_hotspot_23_37.tar.gz';          ;;        riscv64)          ESUM='d401699a92469de7bfb72909c1d11019537a0a2c21af01a8dce1831f09ef5165';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_riscv64_linux_hotspot_23_37.tar.gz';          ;;        s390x)          ESUM='2f9cb1db72ddc91f0b90904d038bca9314bc0bafedb0efe1233469bf3c934e58';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_s390x_linux_hotspot_23_37.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 18 Sep 2024 19:12:13 GMT
CMD ["jshell"]
# Sat, 28 Sep 2024 00:46:05 GMT
CMD ["gradle"]
# Sat, 28 Sep 2024 00:46:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 28 Sep 2024 00:46:05 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
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
	-	`sha256:5d340ed979f83f097fa56590781e2ea4e2d63a50fc75b5e5bc616f845d2e2f80`  
		Last Modified: Tue, 17 Sep 2024 00:53:16 GMT  
		Size: 35.5 MB (35518179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e3c5169d6293fd9f3f82b9deaee88fa754271e536ada337866cf56d5926d7b`  
		Last Modified: Tue, 17 Sep 2024 01:11:33 GMT  
		Size: 20.4 MB (20391476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca4be36c80acc6a9157bd5a146d44f7276af37117eb14812125da7c28beb127`  
		Last Modified: Wed, 18 Sep 2024 21:21:29 GMT  
		Size: 165.2 MB (165157620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad7af30e0015be6b1455df1bcdbecd81963f91e6e56b25f249361f49ad4bdec`  
		Last Modified: Wed, 18 Sep 2024 21:21:14 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c99160b149bc032923d35e9f2b90fc0ed86391097938d29a30e7be255edf3cf`  
		Last Modified: Wed, 18 Sep 2024 21:21:14 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9234990d8499dbf9f8b1074f4daef4a55e8362527af9014c24b0d1a65f3b6130`  
		Last Modified: Mon, 30 Sep 2024 22:09:01 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39672aac6217ce8e0547bf96d9fe920c8dc40d21c8f89ded64ac513dd2c66d6a`  
		Last Modified: Mon, 30 Sep 2024 22:09:03 GMT  
		Size: 71.8 MB (71773378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2c4ffb1d78a10a9e613caeae713abd7e5c76b58022781b6d1d1e8033980454`  
		Last Modified: Mon, 30 Sep 2024 22:09:05 GMT  
		Size: 136.7 MB (136729736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9b58e2ebd721e5c4f9774c16afd3d48ed151173b5eb37ae222e3ef7f711c77`  
		Last Modified: Mon, 30 Sep 2024 22:09:01 GMT  
		Size: 290.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk23` - unknown; unknown

```console
$ docker pull gradle@sha256:59dd268bc16112b14b3ad3f54b24458866cc5749d42463839cb8ed097d4094a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7050773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa6e03d4ff779db6dda31ea8594435f4fc257fb6ceb41a75123ca09746b5114`

```dockerfile
```

-	Layers:
	-	`sha256:7ede3be21e7374fe07dfcb061c8fd609296113df6377add6b6eb5a3f90448b05`  
		Last Modified: Mon, 30 Sep 2024 22:09:01 GMT  
		Size: 7.0 MB (7027587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52096abe09f8f7771c1225cd8982be2e7d4381aaf018c4612b76fb145a65bf53`  
		Last Modified: Mon, 30 Sep 2024 22:09:00 GMT  
		Size: 23.2 KB (23186 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk23` - linux; s390x

```console
$ docker pull gradle@sha256:1e81407fc9760b49a0da6729f3e19502c0155d17009b86566c44593c7d22c868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.5 MB (408462497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28cf7775c75afa88557d4998d197164de652c4f981d92f2e6f388c74766d523f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:05 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:08 GMT
ADD file:55ce2834630c73439274688061a6b2ad0d6952c2435dc51250026e14f139275d in / 
# Tue, 27 Aug 2024 15:55:08 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Sep 2024 19:12:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 19:12:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_VERSION=jdk-23+37
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='630c4f3870056e7e005736ec1edc34ee63a9b45e2027582c52f53a9bf44314b8';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_x64_linux_hotspot_23_37.tar.gz';          ;;        arm64)          ESUM='e8043d1bd9c4f42c5cf7883aca1fc3ef6bcccf4a664f378818ac0fd4fb987b7e';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_aarch64_linux_hotspot_23_37.tar.gz';          ;;        ppc64el)          ESUM='4d3b0609c783dea1f6a899bfc8c84b4000d1f48f39e2489d70050bbf2c7f7d9c';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_ppc64le_linux_hotspot_23_37.tar.gz';          ;;        riscv64)          ESUM='d401699a92469de7bfb72909c1d11019537a0a2c21af01a8dce1831f09ef5165';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_riscv64_linux_hotspot_23_37.tar.gz';          ;;        s390x)          ESUM='2f9cb1db72ddc91f0b90904d038bca9314bc0bafedb0efe1233469bf3c934e58';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_s390x_linux_hotspot_23_37.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 18 Sep 2024 19:12:13 GMT
CMD ["jshell"]
# Sat, 28 Sep 2024 00:46:05 GMT
CMD ["gradle"]
# Sat, 28 Sep 2024 00:46:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 28 Sep 2024 00:46:05 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
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
	-	`sha256:1ebdf4a84a853f3e1fae6f15bd5f734d2925697002b9b26792d25b2080fac7e6`  
		Last Modified: Tue, 17 Sep 2024 01:29:05 GMT  
		Size: 30.7 MB (30665390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f1e9a70cd71418919e1bcea64252f1597c713fe3d37f248f75bc8203446cca`  
		Last Modified: Tue, 17 Sep 2024 01:42:07 GMT  
		Size: 18.8 MB (18794257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c330ca7faa3c67223a43b8ae04047fd4aa9e7da7b238dfd3485e5f2d019c5af`  
		Last Modified: Wed, 18 Sep 2024 21:47:46 GMT  
		Size: 154.4 MB (154375397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23016b67da9560d59258eb3b89bf430726c7cf23c306ff9ed3e7a84678ce02b8`  
		Last Modified: Wed, 18 Sep 2024 21:47:35 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf388efc1d595ed62342d22eac061d719af8a40f2a9e1fc5f7327d2ce0b77bb6`  
		Last Modified: Wed, 18 Sep 2024 21:47:35 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9870fad9684bdee2ac994dfec2746f5074ce1859497dc2aef4571784171f0617`  
		Last Modified: Mon, 30 Sep 2024 22:10:04 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ad1bcf98b67b6a13a95b00dfe8b9eaa937ab4f4920233d781b9afd567b2c16`  
		Last Modified: Mon, 30 Sep 2024 22:10:06 GMT  
		Size: 67.9 MB (67893852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c689d3a3829da6c8a452dc52635c4c583432cb9374d8cb5b4fb87e7ab2a915`  
		Last Modified: Mon, 30 Sep 2024 22:10:10 GMT  
		Size: 136.7 MB (136729738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f388dfa67d8a22406dbfd034e78d175a571cdc5b1c9396079f23d6afcb4ba6b`  
		Last Modified: Mon, 30 Sep 2024 22:10:04 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk23` - unknown; unknown

```console
$ docker pull gradle@sha256:e599b90070d0561a8848d4f1a9766cda24246a764da2c17b7eec103fa48c6f13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6944965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee082bd29e701479861b5a2472a3ee2e3a4a3559db447a7390a3380e60cdcf66`

```dockerfile
```

-	Layers:
	-	`sha256:d4cd7e47c5912479358244b92f7f541a1dc5d3adc49621d4e5777e4121aac58c`  
		Last Modified: Mon, 30 Sep 2024 22:10:04 GMT  
		Size: 6.9 MB (6921847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cb7346634228b468c922e27b7f51a68e03fdc20a7a6d17379813f2a8545c06c`  
		Last Modified: Mon, 30 Sep 2024 22:10:04 GMT  
		Size: 23.1 KB (23118 bytes)  
		MIME: application/vnd.in-toto+json
