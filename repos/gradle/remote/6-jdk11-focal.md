## `gradle:6-jdk11-focal`

```console
$ docker pull gradle@sha256:5205b7a8b5051a19a52b3a7b9d8d84712e3a704d43dbed53bc825d28f9cd4680
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

### `gradle:6-jdk11-focal` - linux; amd64

```console
$ docker pull gradle@sha256:a8c1284e7e5296e882724b85784118cdea10d8b357ce64860d1e1c32580860a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.8 MB (366819625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6461718e825ff08e284e95a15bcda7230537724314db6977359d4487349d162`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 18 Jan 2024 04:04:59 GMT
ARG RELEASE
# Thu, 18 Jan 2024 04:04:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jan 2024 04:04:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jan 2024 04:04:59 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jan 2024 04:04:59 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Thu, 18 Jan 2024 04:04:59 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 04:04:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 18 Jan 2024 04:04:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jan 2024 04:04:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='191baa2e052627614022171400a917d28f0987dc54da48aaf07b06f552bb9884';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='f2087cc3abdd509b74facf8e43e81e36244d14c70dec080b8f3a662695417ca7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6bdd7da08c9f8fedded8da0411b6566c16cb9a904d164b68a0b7f11c8376673a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='0014ffdae26d2b8f840b4842e3f9d4edc3576b4a961770708273d8ecc86ba5b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='5fb661da82943f42a14bed94beda6d4dd3188987bd13b77e8b6f907054a73e9d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 18 Jan 2024 04:04:59 GMT
CMD ["jshell"]
# Thu, 18 Jan 2024 04:04:59 GMT
CMD ["gradle"]
# Thu, 18 Jan 2024 04:04:59 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 18 Jan 2024 04:04:59 GMT
WORKDIR /home/gradle
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
ENV GRADLE_VERSION=6.9.4
# Thu, 18 Jan 2024 04:04:59 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Thu, 18 Jan 2024 04:04:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
USER gradle
# Thu, 18 Jan 2024 04:04:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
USER root
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e1ffd97a5d2efe1747865cafbf6f27b0831ab7c5fca5e5b30f294c77fa3f08`  
		Last Modified: Wed, 22 Jan 2025 18:28:00 GMT  
		Size: 20.3 MB (20257650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0824a1e0d26cf9fd3a1b25aca5139fef86fbdc0cf2038d1dd06adb63a56db06`  
		Last Modified: Wed, 22 Jan 2025 18:28:03 GMT  
		Size: 145.6 MB (145609201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56cc89cf5c6035f271890a38ddb01f91f8998bd7b89e96a10f49cc4bf565b04`  
		Last Modified: Wed, 22 Jan 2025 18:28:00 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea5b328bd6917817d973f1c3a6d3c4819c5c02196244f4eb05983ee0a4128ea`  
		Last Modified: Wed, 22 Jan 2025 18:28:02 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b86d798d0f258f54edcfdf9882f686ffec99be20a1aa4b411eb62478166036`  
		Last Modified: Wed, 22 Jan 2025 19:35:16 GMT  
		Size: 4.3 KB (4309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46331a25a8ba0df02f88a9e64c4f2efe8c0119bc434782e78c060475773a609`  
		Last Modified: Wed, 22 Jan 2025 19:35:17 GMT  
		Size: 65.3 MB (65307001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f8881783ee1b1e36b682c5473f9c8f9d90a79bc32a1f69227266610a159dee`  
		Last Modified: Wed, 22 Jan 2025 19:35:18 GMT  
		Size: 107.7 MB (107696660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0dc273b2c63721ccb4591df218fa8f6127c2310422984fd0e6b98bf23cd2fee`  
		Last Modified: Wed, 22 Jan 2025 19:35:16 GMT  
		Size: 431.3 KB (431270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:30f811dc704a81186943785aefb17fbb7d1dea8433338a2a2f62255461046783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7753926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cca540ca94bb5f3dcef679e0779e7254bf117cb53d6ccad67baa59439a2a727`

```dockerfile
```

-	Layers:
	-	`sha256:05d5b06962c4cc4899e6de4991293c3aa8d59631af2d7fcc4b61b99dcdcab8b8`  
		Last Modified: Wed, 22 Jan 2025 19:35:16 GMT  
		Size: 7.7 MB (7732515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd5d071c62c98adb3caa07beb5e3749360b2e2da9670e01a097fb59e97796184`  
		Last Modified: Wed, 22 Jan 2025 19:35:16 GMT  
		Size: 21.4 KB (21411 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk11-focal` - linux; arm variant v7

```console
$ docker pull gradle@sha256:6b665af70ec845678be4392a9d7c5c7d10dbea7364c0236d73c42d1da3fdb101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.9 MB (347897292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4958a797a4946a2e89a63933b86c5fcc74770c627b8e2981726b1a1cf945a07`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 18 Jan 2024 04:04:59 GMT
ARG RELEASE
# Thu, 18 Jan 2024 04:04:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jan 2024 04:04:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jan 2024 04:04:59 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jan 2024 04:04:59 GMT
ADD file:f76c848564adfa0c782654cd9423feee0ffacccd95abfe3e4e696203d5e61fbf in / 
# Thu, 18 Jan 2024 04:04:59 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 04:04:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 18 Jan 2024 04:04:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jan 2024 04:04:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='191baa2e052627614022171400a917d28f0987dc54da48aaf07b06f552bb9884';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='f2087cc3abdd509b74facf8e43e81e36244d14c70dec080b8f3a662695417ca7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6bdd7da08c9f8fedded8da0411b6566c16cb9a904d164b68a0b7f11c8376673a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='0014ffdae26d2b8f840b4842e3f9d4edc3576b4a961770708273d8ecc86ba5b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='5fb661da82943f42a14bed94beda6d4dd3188987bd13b77e8b6f907054a73e9d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 18 Jan 2024 04:04:59 GMT
CMD ["jshell"]
# Thu, 18 Jan 2024 04:04:59 GMT
CMD ["gradle"]
# Thu, 18 Jan 2024 04:04:59 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 18 Jan 2024 04:04:59 GMT
WORKDIR /home/gradle
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
ENV GRADLE_VERSION=6.9.4
# Thu, 18 Jan 2024 04:04:59 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Thu, 18 Jan 2024 04:04:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
USER gradle
# Thu, 18 Jan 2024 04:04:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
USER root
```

-	Layers:
	-	`sha256:10b337d353b3ceaf6823ab2d8696989401feed741b22eb313c8a0cd378762d39`  
		Last Modified: Fri, 11 Oct 2024 04:41:36 GMT  
		Size: 23.6 MB (23620412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf7dfa91dfefd2d38b8ffd98f5296dec749e2c8b186d41439b07e2e8ade5eba`  
		Last Modified: Thu, 24 Oct 2024 00:57:44 GMT  
		Size: 18.5 MB (18475795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d2dcf9df32fee9f809c1050ce15e96f5d322b50182156296e27828360db18b`  
		Last Modified: Thu, 23 Jan 2025 01:31:31 GMT  
		Size: 138.1 MB (138079763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcc3e9f0308f0307d1146e989aa3e8b38e70c6ea01bd0ab76a56107386afc1b`  
		Last Modified: Thu, 23 Jan 2025 01:31:27 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0c6b6feb1851eaf7207ab612bb6b72f2b396f10ea32efdcc85b66729c1615a`  
		Last Modified: Thu, 23 Jan 2025 01:31:27 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be5fc4ab158cffee862c077ec247cff867aa1b7b9273e9399aa2256584ae337`  
		Last Modified: Thu, 23 Jan 2025 04:19:14 GMT  
		Size: 4.3 KB (4296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80752486143954d57aa7815aaf918c2f241ab942f3b54cfc7538e8ab47113ead`  
		Last Modified: Thu, 23 Jan 2025 04:19:16 GMT  
		Size: 60.0 MB (59986622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9fbb7b435a3df3c6f5d651da6fb75b535843a64fa1c6c0aae485ebd3d6a9878`  
		Last Modified: Thu, 23 Jan 2025 04:31:46 GMT  
		Size: 107.7 MB (107696661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4134aac0adc25678a10e694bc36c2a7b1e32552a8dedfb01fcb8e35b41226a`  
		Last Modified: Thu, 23 Jan 2025 04:31:43 GMT  
		Size: 31.3 KB (31269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:82e9b1dfd469cb6a0dc93797447be2ac3b98bbfd9a02c2775acebd3d9d59ae28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7758413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:910c5dc88b65a88ce01ef01f86fc0cc7ab8e4e3c80a9d07f6228b018f82abbe5`

```dockerfile
```

-	Layers:
	-	`sha256:1e4b0512e25b8786a66bbf4932cb74689001196ae8cf59e1112ec45f6789fa08`  
		Last Modified: Thu, 23 Jan 2025 04:31:43 GMT  
		Size: 7.7 MB (7736893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bff03eeb62af86407f990bc0050b4bceeb6da3ebe7e8414f4c9b97e25533674f`  
		Last Modified: Thu, 23 Jan 2025 04:31:42 GMT  
		Size: 21.5 KB (21520 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk11-focal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:37a9194ee9b92166b17611ef01ac8892bbd1522f0dd729a7aaa2d035516177b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.7 MB (361658210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5150a583fd455dde8bffcdf81182a4518f54a8810ad2a1c27c4d59f84d25f0a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 18 Jan 2024 04:04:59 GMT
ARG RELEASE
# Thu, 18 Jan 2024 04:04:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jan 2024 04:04:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jan 2024 04:04:59 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jan 2024 04:04:59 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Thu, 18 Jan 2024 04:04:59 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 04:04:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 18 Jan 2024 04:04:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jan 2024 04:04:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='191baa2e052627614022171400a917d28f0987dc54da48aaf07b06f552bb9884';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='f2087cc3abdd509b74facf8e43e81e36244d14c70dec080b8f3a662695417ca7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6bdd7da08c9f8fedded8da0411b6566c16cb9a904d164b68a0b7f11c8376673a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='0014ffdae26d2b8f840b4842e3f9d4edc3576b4a961770708273d8ecc86ba5b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='5fb661da82943f42a14bed94beda6d4dd3188987bd13b77e8b6f907054a73e9d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 18 Jan 2024 04:04:59 GMT
CMD ["jshell"]
# Thu, 18 Jan 2024 04:04:59 GMT
CMD ["gradle"]
# Thu, 18 Jan 2024 04:04:59 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 18 Jan 2024 04:04:59 GMT
WORKDIR /home/gradle
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
ENV GRADLE_VERSION=6.9.4
# Thu, 18 Jan 2024 04:04:59 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Thu, 18 Jan 2024 04:04:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
USER gradle
# Thu, 18 Jan 2024 04:04:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
USER root
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623d12075ed7a05b064c5e3f3efe3b64669e0176900a7b195c750eec83f6f79`  
		Last Modified: Wed, 22 Jan 2025 20:50:38 GMT  
		Size: 20.1 MB (20094632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f4b72dcbb6206c43fe45c55101d1e9488f00e6908563d57ded36365e8f11e5`  
		Last Modified: Wed, 22 Jan 2025 20:56:53 GMT  
		Size: 142.4 MB (142386629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea9da366dca0f6592ba69e8a5b9560a31595ca67e7df454bdb5656b03d833d6`  
		Last Modified: Wed, 22 Jan 2025 20:56:48 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef5e6ad774f07f40e295b3f3aa2a431acc33b9ba03bbac13fda900c76835adc`  
		Last Modified: Wed, 22 Jan 2025 20:56:49 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16b64a7fee66fdf96c6767fc618a3f59f70822442e8ec62a96f4633bdcb8cea`  
		Last Modified: Thu, 23 Jan 2025 00:01:35 GMT  
		Size: 4.3 KB (4319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c347d3bfa4dd957f88232456700f535c53bda6d06dbd31a6a7309051a2464f8`  
		Last Modified: Thu, 23 Jan 2025 00:01:40 GMT  
		Size: 65.1 MB (65074643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd18f04eb705a64beeef1b3e79d0e3a939abd701314a372e37b0d2e201226c52`  
		Last Modified: Thu, 23 Jan 2025 00:13:42 GMT  
		Size: 107.7 MB (107696666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83d79d3ef8a901cee6791464b47a8dc4f8ba8b0f47077ff1ea1fff4dcffa30c`  
		Last Modified: Thu, 23 Jan 2025 00:13:39 GMT  
		Size: 425.0 KB (425019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:faaba9fe461c52cd49029e9eb0edc5b781657ecb44ac120e590334065c0db3c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7760504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e85e729930dbb1774792466760c113be610adf67313776c256dc724f86308e86`

```dockerfile
```

-	Layers:
	-	`sha256:e34bacd495179217f7f164ec9326c876b7352fce76843c0c3e3b3dc63b64ea54`  
		Last Modified: Thu, 23 Jan 2025 00:13:39 GMT  
		Size: 7.7 MB (7738953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee383ebb82e2215540976d5d69a501d5f2daf6746ba643e770c5a1631b7828a1`  
		Last Modified: Thu, 23 Jan 2025 00:13:38 GMT  
		Size: 21.6 KB (21551 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk11-focal` - linux; ppc64le

```console
$ docker pull gradle@sha256:cc9b268d40d84bc40c60fdf7a0b6cbefa39260439ad99910e58570beeabcade0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.7 MB (368679448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c7c869b4c6035d800e9dd2c5a607166b32b65023d98a92f2f95972699415d9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 18 Jan 2024 04:04:59 GMT
ARG RELEASE
# Thu, 18 Jan 2024 04:04:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jan 2024 04:04:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jan 2024 04:04:59 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jan 2024 04:04:59 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Thu, 18 Jan 2024 04:04:59 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 04:04:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 18 Jan 2024 04:04:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jan 2024 04:04:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='191baa2e052627614022171400a917d28f0987dc54da48aaf07b06f552bb9884';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='f2087cc3abdd509b74facf8e43e81e36244d14c70dec080b8f3a662695417ca7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6bdd7da08c9f8fedded8da0411b6566c16cb9a904d164b68a0b7f11c8376673a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='0014ffdae26d2b8f840b4842e3f9d4edc3576b4a961770708273d8ecc86ba5b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='5fb661da82943f42a14bed94beda6d4dd3188987bd13b77e8b6f907054a73e9d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 18 Jan 2024 04:04:59 GMT
CMD ["jshell"]
# Thu, 18 Jan 2024 04:04:59 GMT
CMD ["gradle"]
# Thu, 18 Jan 2024 04:04:59 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 18 Jan 2024 04:04:59 GMT
WORKDIR /home/gradle
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
ENV GRADLE_VERSION=6.9.4
# Thu, 18 Jan 2024 04:04:59 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Thu, 18 Jan 2024 04:04:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
USER gradle
# Thu, 18 Jan 2024 04:04:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
USER root
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f87c2fb3d121a254124d3a3171cab48a218a493e68f9620a9d15f0bd3bfc103`  
		Last Modified: Wed, 22 Jan 2025 18:28:55 GMT  
		Size: 22.4 MB (22419717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647dd706bf46127c3b8908591869e8c72d0a319ab3309ebb1e22031e83077496`  
		Last Modified: Wed, 22 Jan 2025 18:35:47 GMT  
		Size: 132.8 MB (132794223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52372f2ccaa017974db97b217cbbe3ec81487dba4374c7335d1207322456db41`  
		Last Modified: Wed, 22 Jan 2025 18:35:43 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c329ab171bded5f635dc05ecc786e1910d65e12f5a5292ca737b496e2ef85e3`  
		Last Modified: Wed, 22 Jan 2025 18:35:43 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5313ce96dc239c888ad7de2aa049f21942a2a4bcd6325b184ec9db9cfd7354fe`  
		Last Modified: Wed, 22 Jan 2025 19:37:53 GMT  
		Size: 4.3 KB (4312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aef5618e54800a70abc210502753d39c675a11a3a5031a10497fb485a93c374`  
		Last Modified: Wed, 22 Jan 2025 19:37:56 GMT  
		Size: 73.7 MB (73650568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0c40d2fb2ceb168de740b491849942f28bae72cb948435c2e79c12e2a48c42`  
		Last Modified: Wed, 22 Jan 2025 19:56:28 GMT  
		Size: 107.7 MB (107696664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e994469db6e44948d40d2c152cbdd43b54aa5ba1487b363a5557ae1630cc40df`  
		Last Modified: Wed, 22 Jan 2025 19:56:25 GMT  
		Size: 35.0 KB (34982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:086c409b3676b03fb1ffa3edca4a37ff2d462553b4c0cfc9c35ff77ff8dc04f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7758707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:496a5dc75f15ce0e64225e9ed603d7857454120182690b22cdd1e4bcefc28a1e`

```dockerfile
```

-	Layers:
	-	`sha256:c5557194ca645c453923f96320fea5b58511982280ed2a9289ec9fb3e289d896`  
		Last Modified: Wed, 22 Jan 2025 19:56:25 GMT  
		Size: 7.7 MB (7737251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a1e6b34fe9128ca8685297276f0e0f6804980cd636cbaa76b4e78f07c4968a3`  
		Last Modified: Wed, 22 Jan 2025 19:56:24 GMT  
		Size: 21.5 KB (21456 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk11-focal` - linux; s390x

```console
$ docker pull gradle@sha256:53afd311b33e92e58614f7b90b46e4a93f9dd9cb24d5da001d21d6b623a3c53d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.2 MB (344196920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:017830cf9f821a5aeb12f7afea750a828e7b7b3942826cc6e1c769cc7f9d5938`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 18 Jan 2024 04:04:59 GMT
ARG RELEASE
# Thu, 18 Jan 2024 04:04:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jan 2024 04:04:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jan 2024 04:04:59 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jan 2024 04:04:59 GMT
ADD file:e3e9bad1c3576edf8ddea2dd7af2ed8ecac1ad0b15d714dd9c51f679d44d13b6 in / 
# Thu, 18 Jan 2024 04:04:59 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 04:04:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 18 Jan 2024 04:04:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jan 2024 04:04:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='191baa2e052627614022171400a917d28f0987dc54da48aaf07b06f552bb9884';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='f2087cc3abdd509b74facf8e43e81e36244d14c70dec080b8f3a662695417ca7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6bdd7da08c9f8fedded8da0411b6566c16cb9a904d164b68a0b7f11c8376673a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='0014ffdae26d2b8f840b4842e3f9d4edc3576b4a961770708273d8ecc86ba5b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='5fb661da82943f42a14bed94beda6d4dd3188987bd13b77e8b6f907054a73e9d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 18 Jan 2024 04:04:59 GMT
CMD ["jshell"]
# Thu, 18 Jan 2024 04:04:59 GMT
CMD ["gradle"]
# Thu, 18 Jan 2024 04:04:59 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 18 Jan 2024 04:04:59 GMT
WORKDIR /home/gradle
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
ENV GRADLE_VERSION=6.9.4
# Thu, 18 Jan 2024 04:04:59 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Thu, 18 Jan 2024 04:04:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
USER gradle
# Thu, 18 Jan 2024 04:04:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
USER root
```

-	Layers:
	-	`sha256:f6b14778eb4fed5cbb0bd80eea19d48526571f3b2dfa0196faf63f42fdb8c6c2`  
		Last Modified: Fri, 11 Oct 2024 04:41:53 GMT  
		Size: 26.4 MB (26365979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb249cf2bb79e7c454a96cbf6cd56dc7ed7161f5a8b48921c7a48c6ae4882f2`  
		Last Modified: Wed, 22 Jan 2025 21:41:39 GMT  
		Size: 19.9 MB (19901189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed3376c2bb7aca7c91e26dc867be4ee5dfa3fc2463933a96b2a7d9d1b906658`  
		Last Modified: Wed, 22 Jan 2025 21:41:40 GMT  
		Size: 125.6 MB (125574059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0e0d603cd2e92a2daee2d56c23b2cf949a19a5bda27dd45e68c8157ba7f4a6`  
		Last Modified: Wed, 22 Jan 2025 21:41:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac98141a33ad2ff098f4433313e9878a3eaa65e0d8fbb2d2b7594a393f67d961`  
		Last Modified: Wed, 22 Jan 2025 21:41:39 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1741d94cdc2955c11bbf4e27c218ac59624b759e107b1397ec2e1e1e08f86c62`  
		Last Modified: Thu, 23 Jan 2025 02:06:17 GMT  
		Size: 4.3 KB (4315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc217498e8a90cc50c3259b8ee95b500dc1ed28b8f326d26ca20d1989f8f88c`  
		Last Modified: Thu, 23 Jan 2025 02:06:18 GMT  
		Size: 64.6 MB (64617263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81aa0dce461e9509b91f2dfa62b686542bfb26fd2a17564a7bc6f66881efdd0`  
		Last Modified: Thu, 23 Jan 2025 02:18:21 GMT  
		Size: 107.7 MB (107696662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0351408650daed19df9c2981f2e2286d4229718d56bd29773efbe61af4c5ae`  
		Last Modified: Thu, 23 Jan 2025 02:18:19 GMT  
		Size: 35.0 KB (34978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:ffdf79b1365593c3c1b0f5d9175fbca70eb210d0a8425eee68f63d56f3a21e0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7748982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63be50802232c1917f6ed1c7863b759ecfac350184e2ea7b4354d344ab43763`

```dockerfile
```

-	Layers:
	-	`sha256:5aa72dcff4229e7874ae04fc38dbc0d9f4206bbb8728ffebc66248615c42697d`  
		Last Modified: Thu, 23 Jan 2025 02:18:19 GMT  
		Size: 7.7 MB (7727569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd4b37f2539acbd0c77711e947bb88ca97154aadcb27acdc32646f6389b60f9e`  
		Last Modified: Thu, 23 Jan 2025 02:18:19 GMT  
		Size: 21.4 KB (21413 bytes)  
		MIME: application/vnd.in-toto+json
