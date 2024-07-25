## `gradle:8-jdk22-jammy`

```console
$ docker pull gradle@sha256:6a499abef5e40019f7643e2bb9f9a22ad056454d6c411ad8475a3769e6f86fca
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

### `gradle:8-jdk22-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:a976e5ec1635202ef6e1979a86ea9d7e56e27600af4d3f39f946ba38510bbb44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.6 MB (391625190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92037d1dd6b808878ff75ba1dd481acffc13ed91ba364c3b81f64ad6bda091af`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Fri, 12 Jul 2024 03:13:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Jul 2024 03:13:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 03:13:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
ENV JAVA_VERSION=jdk-22.0.2+9
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='05cd9359dacb1a1730f7c54f57e0fed47942a5292eb56a3a0ee6b13b87457a43';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_x64_linux_hotspot_22.0.2_9.tar.gz';          ;;        arm64)          ESUM='dac62747b5158c4bf4c4636432e3bdb9dea47f80f0c9d1d007f19bd5483b7d29';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_aarch64_linux_hotspot_22.0.2_9.tar.gz';          ;;        ppc64el)          ESUM='1d678752d58e33ff951e75736b8415d6d7ae136b2421ca02e993f2603e9b259b';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_ppc64le_linux_hotspot_22.0.2_9.tar.gz';          ;;        s390x)          ESUM='46527cfc560552f05c0462520d69d438f144a3dc8206687952387c910cdd4c40';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_s390x_linux_hotspot_22.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 12 Jul 2024 03:13:38 GMT
CMD ["jshell"]
# Fri, 12 Jul 2024 03:13:38 GMT
CMD ["gradle"]
# Fri, 12 Jul 2024 03:13:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 12 Jul 2024 03:13:38 GMT
WORKDIR /home/gradle
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
ENV GRADLE_VERSION=8.9
# Fri, 12 Jul 2024 03:13:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
# Fri, 12 Jul 2024 03:13:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
USER gradle
# Fri, 12 Jul 2024 03:13:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
USER root
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec46f3f6db860434ad19e35ce03fbc32ac970c970f807ba59885aeae242df05`  
		Last Modified: Tue, 02 Jul 2024 06:03:12 GMT  
		Size: 16.3 MB (16312426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265d1e38c473ebf4f2334ee4d02c19cae77c73ca72d6f686ca037a51e10c5d37`  
		Last Modified: Wed, 24 Jul 2024 01:30:00 GMT  
		Size: 156.5 MB (156487168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833703801e8effc9ec7da5656b6ae1056ae83d9202a938a270c1cf290c8d9674`  
		Last Modified: Wed, 24 Jul 2024 01:29:48 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356b4efde96c349d219007c025553b09af29dfaab8cf58da5f9714d2e9f9a806`  
		Last Modified: Wed, 24 Jul 2024 01:29:48 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c157561fc244f37cd50015054486c23e0630eb66c111a963b21e3e8044201fc`  
		Last Modified: Wed, 24 Jul 2024 03:04:43 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db008f6f7acd3b58442aac45bf6aa0700c1c10f0c56860cba38354de2fc85daf`  
		Last Modified: Wed, 24 Jul 2024 03:04:44 GMT  
		Size: 52.2 MB (52192867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3701051dccfa850adfd8794d64d947acb89007c3c981f407c4af20203c21b8a`  
		Last Modified: Wed, 24 Jul 2024 03:04:45 GMT  
		Size: 136.1 MB (136132040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fac927eb11c90486620d3fbf1c8daee0b21215907c3da6f87ba329f9a442d8`  
		Last Modified: Wed, 24 Jul 2024 03:04:43 GMT  
		Size: 54.9 KB (54896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk22-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:04a53f2e3f3fd07f132954c45d72ce4b4c41e8b1d7e80f383e7088d8a85034e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7256169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79cfdf19856e185c2396bbb49de443e2f9e90065cf24f76882c213d814bd7b8f`

```dockerfile
```

-	Layers:
	-	`sha256:a809dd5f9ca71c8f748a00ffb307e4b52d23ab0b4ea14e092b3c2290715c6fe9`  
		Last Modified: Wed, 24 Jul 2024 03:04:43 GMT  
		Size: 7.2 MB (7233290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f680692dc463edc16f932a122c8dbea2aa490f52444562c9d84625bc41d399be`  
		Last Modified: Wed, 24 Jul 2024 03:04:43 GMT  
		Size: 22.9 KB (22879 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk22-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:396746b08012784ec51596ad009a0d7e33c2e8a7532962a0fc29ee74a5cb7d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.6 MB (388600368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a79981959715f064f6284fb74c7c7be09846858a09fe4d15a43fab0e4707e296`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Fri, 12 Jul 2024 03:13:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Jul 2024 03:13:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 03:13:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
ENV JAVA_VERSION=jdk-22.0.2+9
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='05cd9359dacb1a1730f7c54f57e0fed47942a5292eb56a3a0ee6b13b87457a43';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_x64_linux_hotspot_22.0.2_9.tar.gz';          ;;        arm64)          ESUM='dac62747b5158c4bf4c4636432e3bdb9dea47f80f0c9d1d007f19bd5483b7d29';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_aarch64_linux_hotspot_22.0.2_9.tar.gz';          ;;        ppc64el)          ESUM='1d678752d58e33ff951e75736b8415d6d7ae136b2421ca02e993f2603e9b259b';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_ppc64le_linux_hotspot_22.0.2_9.tar.gz';          ;;        s390x)          ESUM='46527cfc560552f05c0462520d69d438f144a3dc8206687952387c910cdd4c40';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_s390x_linux_hotspot_22.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 12 Jul 2024 03:13:38 GMT
CMD ["jshell"]
# Fri, 12 Jul 2024 03:13:38 GMT
CMD ["gradle"]
# Fri, 12 Jul 2024 03:13:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 12 Jul 2024 03:13:38 GMT
WORKDIR /home/gradle
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
ENV GRADLE_VERSION=8.9
# Fri, 12 Jul 2024 03:13:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
# Fri, 12 Jul 2024 03:13:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
USER gradle
# Fri, 12 Jul 2024 03:13:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
USER root
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac50ae6767d4a91ada9d54209c76b3645963c6e1b649e0894bcfbc75cf1e0877`  
		Last Modified: Tue, 02 Jul 2024 04:36:41 GMT  
		Size: 17.7 MB (17721806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccb33b6e6156bf3bae7feb6806afcc4d2c0fe9235dfbb29068ff2855c4cb5ae`  
		Last Modified: Wed, 24 Jul 2024 00:53:07 GMT  
		Size: 154.5 MB (154500947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16094ccf4532f9f5a492b45dba12cf96fef5f6df808bd1fb8116edb76befaf85`  
		Last Modified: Wed, 24 Jul 2024 00:52:57 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531cd8411c715aa45c9476585be9bffc10507b58b0be8ebd6fd57e5b12e77a8d`  
		Last Modified: Wed, 24 Jul 2024 00:52:57 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30521460b24a5bc31b61292411541136dbd36f7ecbc32738b27d2d063a4eaea2`  
		Last Modified: Wed, 24 Jul 2024 12:40:18 GMT  
		Size: 4.3 KB (4316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0cb7475f907c25eeccde498851f89106543dc1ab321d4341af5480c006980f`  
		Last Modified: Wed, 24 Jul 2024 12:40:20 GMT  
		Size: 51.8 MB (51778995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0c2fe43910b83506d732a2b05719af8ec516bc48bded78a422e9a3cc17bc28`  
		Last Modified: Wed, 24 Jul 2024 12:40:22 GMT  
		Size: 136.1 MB (136132042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874b9df483c42008bfea97f945932388f1fce34785fa8212e066507a96b4c13d`  
		Last Modified: Wed, 24 Jul 2024 12:40:18 GMT  
		Size: 59.5 KB (59523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk22-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:7db0ad1ebdaa1847c1a9971d8ff674a7bcadde0fa5e346bd21b88ea03278703d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7358952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c71567a2db7c45aa7ef9af508ef77db34ecb1f5def4ff180713b04aa2717419`

```dockerfile
```

-	Layers:
	-	`sha256:18c7b0757d0ab79c529b648341574ec748c94117c5273402d31893635344580d`  
		Last Modified: Wed, 24 Jul 2024 12:40:19 GMT  
		Size: 7.3 MB (7335708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2402c70c40267acd5694d0d051be852a7af87bb105f300c4cee42ca6ddc9a72f`  
		Last Modified: Wed, 24 Jul 2024 12:40:18 GMT  
		Size: 23.2 KB (23244 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk22-jammy` - linux; ppc64le

```console
$ docker pull gradle@sha256:861d5e249f948e399b5f09279550649e5b15c21db407f2174eec3b0b8f8ff522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.9 MB (401929688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c79ae8ca5780e2f92f68889273c06fdc1867c6ba9ed8d014b73b823c9751853`
-	Entrypoint: `["\/bin\/bash","\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Fri, 12 Jul 2024 03:13:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Jul 2024 03:13:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 03:13:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
ENV JAVA_VERSION=jdk-22.0.2+9
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='05cd9359dacb1a1730f7c54f57e0fed47942a5292eb56a3a0ee6b13b87457a43';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_x64_linux_hotspot_22.0.2_9.tar.gz';          ;;        arm64)          ESUM='dac62747b5158c4bf4c4636432e3bdb9dea47f80f0c9d1d007f19bd5483b7d29';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_aarch64_linux_hotspot_22.0.2_9.tar.gz';          ;;        ppc64el)          ESUM='1d678752d58e33ff951e75736b8415d6d7ae136b2421ca02e993f2603e9b259b';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_ppc64le_linux_hotspot_22.0.2_9.tar.gz';          ;;        s390x)          ESUM='46527cfc560552f05c0462520d69d438f144a3dc8206687952387c910cdd4c40';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_s390x_linux_hotspot_22.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Fri, 12 Jul 2024 03:13:38 GMT
CMD ["jshell"]
# Fri, 12 Jul 2024 03:13:38 GMT
CMD ["gradle"]
# Fri, 12 Jul 2024 03:13:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 12 Jul 2024 03:13:38 GMT
WORKDIR /home/gradle
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
ENV GRADLE_VERSION=8.9
# Fri, 12 Jul 2024 03:13:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
# Fri, 12 Jul 2024 03:13:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
USER gradle
# Fri, 12 Jul 2024 03:13:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
USER root
```

-	Layers:
	-	`sha256:8abbcd57d9001f5aade9e7c1c7cf47fea659efa1b67f1bf51c65e0f66569df0d`  
		Last Modified: Tue, 02 Jul 2024 02:09:14 GMT  
		Size: 35.6 MB (35588321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9464c0d74292e9000dcfd35c7f43f3a5a15d1ec6fbc80e60c46baed7cc7d133d`  
		Last Modified: Tue, 02 Jul 2024 05:06:49 GMT  
		Size: 17.3 MB (17277959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2cd7eaa61fbb3b5a3a59a3789a6ec7ed8d063a66555a365bbf9e7bfd1ece34`  
		Last Modified: Wed, 24 Jul 2024 04:14:20 GMT  
		Size: 156.5 MB (156469928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0172b907817b8412f745253664a5943b7534cd6559a4a207187fc2cf0f57e89e`  
		Last Modified: Wed, 24 Jul 2024 04:14:05 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab200aa5997c01381e84a27a1d370d6d7cd98b2dfa159a98f888b23de59a813a`  
		Last Modified: Thu, 25 Jul 2024 17:26:33 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e24963bf5fe6e8e23413e431233841d1adbf39f00718c5cda5e1b776fec683`  
		Last Modified: Thu, 25 Jul 2024 19:26:03 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe14d6814cffed96b94a94bb4a0debd1fa45ebf403a1fa5ae4f81bdd5c44fd5`  
		Last Modified: Thu, 25 Jul 2024 19:26:05 GMT  
		Size: 56.5 MB (56454790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c642bb6c733ff8c43af50dff90af55fde778d8567fb7837887ec541eb1b8ed35`  
		Last Modified: Thu, 25 Jul 2024 19:26:07 GMT  
		Size: 136.1 MB (136132043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca965029cdc460bda236b19fbf69d75d5e06eefb36a6fc6ad95b50788e6adaa`  
		Last Modified: Thu, 25 Jul 2024 19:26:04 GMT  
		Size: 291.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk22-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:c0a314fc98b7d8c7be92de8754414b01c491e30ba56d0140350c47aae0b2f9d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7289453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc740d4d42654a17d057182be52fbc3c3659c4fc258b1f41475b0c379eb223e0`

```dockerfile
```

-	Layers:
	-	`sha256:b08269c587336710f411e177e0c10e37429dfa449d997ca71af2bb4e18b76c01`  
		Last Modified: Thu, 25 Jul 2024 19:26:03 GMT  
		Size: 7.3 MB (7266508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb48f299334b09ec8fae573b1a3155852135185916cfec7312ef4b32a90871c1`  
		Last Modified: Thu, 25 Jul 2024 19:26:03 GMT  
		Size: 22.9 KB (22945 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk22-jammy` - linux; s390x

```console
$ docker pull gradle@sha256:5ba33b5a212fa1598554c629f90448931304db6cb550d0edfc9fbaab8ffab038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.3 MB (378349947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7520469ef53f679cce3e393c77f11708d52b53174d8f82bfa5f76220d918c9`
-	Entrypoint: `["\/bin\/bash","\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 27 Jun 2024 19:26:47 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:26:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:26:50 GMT
ADD file:160bc105c5c70c3239daf08894bd8a2311ea04a965b30820eebf28573143f86b in / 
# Thu, 27 Jun 2024 19:26:50 GMT
CMD ["/bin/bash"]
# Fri, 12 Jul 2024 03:13:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Jul 2024 03:13:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 03:13:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
ENV JAVA_VERSION=jdk-22.0.2+9
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='05cd9359dacb1a1730f7c54f57e0fed47942a5292eb56a3a0ee6b13b87457a43';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_x64_linux_hotspot_22.0.2_9.tar.gz';          ;;        arm64)          ESUM='dac62747b5158c4bf4c4636432e3bdb9dea47f80f0c9d1d007f19bd5483b7d29';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_aarch64_linux_hotspot_22.0.2_9.tar.gz';          ;;        ppc64el)          ESUM='1d678752d58e33ff951e75736b8415d6d7ae136b2421ca02e993f2603e9b259b';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_ppc64le_linux_hotspot_22.0.2_9.tar.gz';          ;;        s390x)          ESUM='46527cfc560552f05c0462520d69d438f144a3dc8206687952387c910cdd4c40';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jdk_s390x_linux_hotspot_22.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Fri, 12 Jul 2024 03:13:38 GMT
CMD ["jshell"]
# Fri, 12 Jul 2024 03:13:38 GMT
CMD ["gradle"]
# Fri, 12 Jul 2024 03:13:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 12 Jul 2024 03:13:38 GMT
WORKDIR /home/gradle
# Fri, 12 Jul 2024 03:13:38 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
ENV GRADLE_VERSION=8.9
# Fri, 12 Jul 2024 03:13:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
# Fri, 12 Jul 2024 03:13:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
USER gradle
# Fri, 12 Jul 2024 03:13:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=d725d707bfabd4dfdc958c624003b3c80accc03f7037b5122c4b1d0ef15cecab
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 12 Jul 2024 03:13:38 GMT
USER root
```

-	Layers:
	-	`sha256:4870604a2dd3e1b2f1a9f9dc1f8d02b548d030f0680887506b32aaee40747aa4`  
		Last Modified: Tue, 02 Jul 2024 03:47:54 GMT  
		Size: 28.6 MB (28637470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb585e50f43f29df0c0719456a8a2828ccc7b6cc9c1a57fbb50c79af66e4735`  
		Last Modified: Tue, 02 Jul 2024 03:56:27 GMT  
		Size: 16.1 MB (16124387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa6c55cecab382b53ea639d0af8a8b9f9234e336b9da61d3e7666cf9c23bb60`  
		Last Modified: Wed, 24 Jul 2024 00:58:13 GMT  
		Size: 145.6 MB (145550056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee051be6bedd2129807bd6058166e3591d9f91d61d36f17a0a3901bf474f426e`  
		Last Modified: Wed, 24 Jul 2024 00:58:02 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05acba51a259a952fbdc5dbc796feea1f580340f992ae5731433d312101d017f`  
		Last Modified: Thu, 25 Jul 2024 17:49:43 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c43cd36ef9a9fd71a0d147fe1ee5a16503ba2a1dc0103064377f8976c6d2de4`  
		Last Modified: Thu, 25 Jul 2024 19:12:13 GMT  
		Size: 4.3 KB (4319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886b1a384b6f9b5ce423f0b01d98c6f198735d4bf5071c12cfacc51b2694bc98`  
		Last Modified: Thu, 25 Jul 2024 19:12:14 GMT  
		Size: 51.9 MB (51899343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31961b54d1b728ea29db8ba9e1b8b8dd1eccc9c5216c9399e3a86ea8963eb57`  
		Last Modified: Thu, 25 Jul 2024 19:12:17 GMT  
		Size: 136.1 MB (136132041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b1ce345151762faaaa3611c04ffa9a5fb042e87e6833a6f3ee5297777c5186`  
		Last Modified: Thu, 25 Jul 2024 19:12:14 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk22-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:0d98052452681de07abd24f4c7c17994714c318801304aa1430350d86c25f782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7183688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:162ee620e15ff4fcd9830c96978ba31dd1113ace6afc5f25d9a3e023375c0a51`

```dockerfile
```

-	Layers:
	-	`sha256:050cefbda0f133562a82cc89fe9523256ef9ba4bb28a0de7bdb18f3a39d431e5`  
		Last Modified: Thu, 25 Jul 2024 19:12:13 GMT  
		Size: 7.2 MB (7160811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eee9e05f764af8857a44c2bfc9f043e45facb5ed4bad5486913963b06b0af9e3`  
		Last Modified: Thu, 25 Jul 2024 19:12:13 GMT  
		Size: 22.9 KB (22877 bytes)  
		MIME: application/vnd.in-toto+json
