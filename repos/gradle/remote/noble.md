## `gradle:noble`

```console
$ docker pull gradle@sha256:482cfc026939e7e7bf70d12640f8e10b3527268d4167e9e3a908c56c2987dc39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `gradle:noble` - linux; amd64

```console
$ docker pull gradle@sha256:b83c536704ab3117c957a1b5884abaf1c76d271604163e328ca1e81cf880b3bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.4 MB (411402812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcabd3d31c13ac3183d3a47d57152c555a373c7b0be2ea73ac7211fddc9160b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='974d3acef0b7193f541acb61b76e81670890551366625d4f6ca01b91ac152ce0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='31dba70ba928c78c20d62049ac000f79f7a7ab11f9d9c11e703f52d60aa64f93';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='2ddc0dc14b07d9e853875aac7f84c23826fff18b9cea618c93efe0bcc8f419c2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        riscv64)          ESUM='d75f33ee7f9e5532bce263db83443ffed7d9bae7ff3ed41e48d137808adfe513';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='216edbccab2d677639c90d2cb09dfa39c257788a62b8b83d879528c447b9ad33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
# Thu, 05 Jun 2025 16:04:16 GMT
CMD ["gradle"]
# Thu, 05 Jun 2025 16:04:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 05 Jun 2025 16:04:16 GMT
WORKDIR /home/gradle
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
ENV GRADLE_VERSION=8.14.2
# Thu, 05 Jun 2025 16:04:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
# Thu, 05 Jun 2025 16:04:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
USER gradle
# Thu, 05 Jun 2025 16:04:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
USER root
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380ab39b4f9f66f5491f1e6c6e1b00af781c9e67017d5194267c1eb1b1ea9d61`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 23.0 MB (22954920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf9441e6dddb8defe5d23ab009dd1a3d91ad4f953b4d53d9e904e1adcae03de`  
		Last Modified: Tue, 03 Jun 2025 13:30:23 GMT  
		Size: 157.6 MB (157648066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ea0157e6cfd88563f52f3de2252f96d1de76755323a4e666dc06bfdc169362`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f05f209f6fd19181ffd50612236193ad46991100ff9ffc79e5b5d7f15f0e06`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c8c8e4baffaa489525d18c87d5126ac2bf3a15034480af95f726561197d9a9`  
		Last Modified: Thu, 05 Jun 2025 20:01:49 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f03d8f591aec04e25be8805b4e27dfd361ef322c7e33429cd4150886434d753`  
		Last Modified: Thu, 05 Jun 2025 20:01:55 GMT  
		Size: 63.6 MB (63630333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bedb1dc74d25744b62b71db8a08ab785d9bb05193226c89c93a7215595499b1`  
		Last Modified: Thu, 05 Jun 2025 20:20:00 GMT  
		Size: 137.4 MB (137395504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3401624ce27ffecc7a0d7cb7e7d07c27b289c51321375db6b1dcb5e60e9a2080`  
		Last Modified: Thu, 05 Jun 2025 20:01:49 GMT  
		Size: 54.9 KB (54895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:noble` - unknown; unknown

```console
$ docker pull gradle@sha256:df8d8bab2ffb1a1cceaff1322a8b2f163a1d06ad1ab27dc99adaf4823736d8d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7209593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66dc05c02bd44862ff0069849d8ac3e80003c158dbbd5a3ef7905f4959abd24a`

```dockerfile
```

-	Layers:
	-	`sha256:62fe07dca400519729e6e05234668c7c439011c7d78c7e268c7610253efeea0c`  
		Last Modified: Thu, 05 Jun 2025 20:19:30 GMT  
		Size: 7.2 MB (7180068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4449b562f95674afaec84a535606e0e2583f56c913abeee537a53f5d9eb5f479`  
		Last Modified: Thu, 05 Jun 2025 20:19:31 GMT  
		Size: 29.5 KB (29525 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:noble` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:c6bcb863c094ac6338eb03602a38b528b2980fdf8b9f2dba51c54a3f5649073d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **409.5 MB (409489643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c39ffa6ec22b0e99ba5cfe07e11170bf084ca4c39ee1b9a34a2acd54aecb97fc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='974d3acef0b7193f541acb61b76e81670890551366625d4f6ca01b91ac152ce0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='31dba70ba928c78c20d62049ac000f79f7a7ab11f9d9c11e703f52d60aa64f93';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='2ddc0dc14b07d9e853875aac7f84c23826fff18b9cea618c93efe0bcc8f419c2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        riscv64)          ESUM='d75f33ee7f9e5532bce263db83443ffed7d9bae7ff3ed41e48d137808adfe513';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='216edbccab2d677639c90d2cb09dfa39c257788a62b8b83d879528c447b9ad33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
# Thu, 05 Jun 2025 16:04:16 GMT
CMD ["gradle"]
# Thu, 05 Jun 2025 16:04:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 05 Jun 2025 16:04:16 GMT
WORKDIR /home/gradle
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
ENV GRADLE_VERSION=8.14.2
# Thu, 05 Jun 2025 16:04:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
# Thu, 05 Jun 2025 16:04:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
USER gradle
# Thu, 05 Jun 2025 16:04:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
USER root
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d25aa6c570ac3eb2e6b67b6b415a041c1abc67be71cd7980de88555abccc2d7`  
		Last Modified: Tue, 03 Jun 2025 13:30:34 GMT  
		Size: 24.2 MB (24164086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f9050394cd65db7bd682aa204a01c362d8d2d363adf985a50957840cff4d7e`  
		Last Modified: Tue, 03 Jun 2025 13:30:39 GMT  
		Size: 155.9 MB (155931692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06e006ec58303e7beba0209f43f756637b1ba897201c22052d0e46037217c36`  
		Last Modified: Tue, 03 Jun 2025 13:30:30 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8128e0116aa02398c453c60b880bc13aeab791c1527d27e53b77f6af03bc9201`  
		Last Modified: Tue, 03 Jun 2025 13:30:29 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244814d5d4ce3e33c3b2701f4d54236ae31f174e7b86231a9f0e38bba2ffd2d7`  
		Last Modified: Tue, 03 Jun 2025 13:37:24 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4990c92f289180e10fc42c9c73d9a4315792cadee1ad9d435a8c85b3405728b`  
		Last Modified: Tue, 03 Jun 2025 13:37:53 GMT  
		Size: 63.1 MB (63083151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9ceb5ec68ab583ec87b84d4bc58cc3c6f30508501c982bb1a4a49ef97db044`  
		Last Modified: Thu, 05 Jun 2025 23:25:30 GMT  
		Size: 137.4 MB (137395511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e723f7bab15e967f1da437a3ec74e3bfd1e17e8ae9a5a37701950a318741eb7`  
		Last Modified: Thu, 05 Jun 2025 20:08:42 GMT  
		Size: 59.5 KB (59543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:noble` - unknown; unknown

```console
$ docker pull gradle@sha256:fa73fedda387c9bf581ba84fe1421e624b570c3eacb99ac5472f5a7c4fc6dfd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7347895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac0ca9573f10a71a39a203dc4ea235825ab2b8f8974758df0f757563e96589a8`

```dockerfile
```

-	Layers:
	-	`sha256:4d0b8c9908a144cda9d0796ef2051005c5e7151891b764c1300a0327ccb86b19`  
		Last Modified: Thu, 05 Jun 2025 23:19:27 GMT  
		Size: 7.3 MB (7317981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b098373c8abfc66b64204af8507538f078a341e7a117a8259f2010ce3e69013`  
		Last Modified: Thu, 05 Jun 2025 23:19:28 GMT  
		Size: 29.9 KB (29914 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:noble` - linux; ppc64le

```console
$ docker pull gradle@sha256:8ffefed7f6ba0e94100921e7820e8580176097924d48b61106bb9eea97b7137d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.6 MB (422557343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed460760430a77af3813263f8b35a16d1469995b4c659192c12ae35cdde74a7c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:5b5c63079c35f826dfba60892de9b0b4108ed6547a12101193a481b991b1add9 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='974d3acef0b7193f541acb61b76e81670890551366625d4f6ca01b91ac152ce0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='31dba70ba928c78c20d62049ac000f79f7a7ab11f9d9c11e703f52d60aa64f93';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='2ddc0dc14b07d9e853875aac7f84c23826fff18b9cea618c93efe0bcc8f419c2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        riscv64)          ESUM='d75f33ee7f9e5532bce263db83443ffed7d9bae7ff3ed41e48d137808adfe513';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='216edbccab2d677639c90d2cb09dfa39c257788a62b8b83d879528c447b9ad33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
# Thu, 05 Jun 2025 16:04:16 GMT
CMD ["gradle"]
# Thu, 05 Jun 2025 16:04:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 05 Jun 2025 16:04:16 GMT
WORKDIR /home/gradle
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
ENV GRADLE_VERSION=8.14.2
# Thu, 05 Jun 2025 16:04:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
# Thu, 05 Jun 2025 16:04:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
USER gradle
# Thu, 05 Jun 2025 16:04:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
USER root
```

-	Layers:
	-	`sha256:9f6c4197b204ad8fd01f03e4a049c781a2075478303fbfa660f581b019365dab`  
		Last Modified: Tue, 03 Jun 2025 13:31:13 GMT  
		Size: 34.3 MB (34325210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68873b9ea7e686832e413229ce9ce7a4388079a8479fc2f14002ac9fab91ed30`  
		Last Modified: Tue, 03 Jun 2025 13:37:41 GMT  
		Size: 24.1 MB (24103472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438dd66d44158843e7b3a58a446d1e00f1554645d6d5a1540f6766d538f8d717`  
		Last Modified: Tue, 03 Jun 2025 14:45:39 GMT  
		Size: 157.8 MB (157818284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827895e70c4a48f386a7a468f8222c5f71a1870c9f82a9924f0629cbf7e5cd45`  
		Last Modified: Tue, 03 Jun 2025 13:37:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee588969b11e60b08f02103dcd1f6d3d7f110b194c52f2bd3b9c31fc86ad933`  
		Last Modified: Tue, 03 Jun 2025 13:37:28 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bc5d37891e101fd7a581557b15c56eb489fa97c0adcbd7b1e7068a60d3d98b`  
		Last Modified: Tue, 03 Jun 2025 13:37:30 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84560e6d057e959c257811cde78912027806e8776f37293f3a071e8e8ce16e9`  
		Last Modified: Tue, 03 Jun 2025 15:32:48 GMT  
		Size: 68.9 MB (68876089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662693bc987f4bfd26242fedc490894df58834aa16820917e36d5b3d520639df`  
		Last Modified: Fri, 06 Jun 2025 00:07:20 GMT  
		Size: 137.4 MB (137395512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28891395db4dfb001f7cd67821896c2e1e964ac8e33d21ed13ecf8cd8a0c3445`  
		Last Modified: Thu, 05 Jun 2025 20:12:17 GMT  
		Size: 35.0 KB (35018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:noble` - unknown; unknown

```console
$ docker pull gradle@sha256:bd3463ae171681633b65e8abbe53f5d29c3769c3a327b791af9d62d8c873c7c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7260986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d8ba9dc479c425258840fcc0be94778240d8848b64bf6b28c18e513a3a27f74`

```dockerfile
```

-	Layers:
	-	`sha256:3cfa266048e520f6eeee42a64905c3f2eb419f994080f93a69a7759f1418b6cd`  
		Last Modified: Thu, 05 Jun 2025 23:19:35 GMT  
		Size: 7.2 MB (7231291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaa4917657e7a21e676f2117afa973614863548f1e8a4d36cf47f6f64e683605`  
		Last Modified: Thu, 05 Jun 2025 23:19:35 GMT  
		Size: 29.7 KB (29695 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:noble` - linux; riscv64

```console
$ docker pull gradle@sha256:b84777695aad186a8e6fd490845e0d983eeae52cf89a373a5045cb08fb5e0235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.6 MB (413602594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:708e363e15971d5580e8175400f4609dc45c2b4b484bbfdfc6a819199f8b416a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:f68263cf915d0f5d61ab9caa83da511fc9ef55d936429cb8fb542906fc38a8fa in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='974d3acef0b7193f541acb61b76e81670890551366625d4f6ca01b91ac152ce0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='31dba70ba928c78c20d62049ac000f79f7a7ab11f9d9c11e703f52d60aa64f93';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='2ddc0dc14b07d9e853875aac7f84c23826fff18b9cea618c93efe0bcc8f419c2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        riscv64)          ESUM='d75f33ee7f9e5532bce263db83443ffed7d9bae7ff3ed41e48d137808adfe513';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='216edbccab2d677639c90d2cb09dfa39c257788a62b8b83d879528c447b9ad33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
# Thu, 05 Jun 2025 16:04:16 GMT
CMD ["gradle"]
# Thu, 05 Jun 2025 16:04:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 05 Jun 2025 16:04:16 GMT
WORKDIR /home/gradle
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
ENV GRADLE_VERSION=8.14.2
# Thu, 05 Jun 2025 16:04:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
# Thu, 05 Jun 2025 16:04:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
USER gradle
# Thu, 05 Jun 2025 16:04:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
USER root
```

-	Layers:
	-	`sha256:4ac2db62b9f8401057b5c4ebae4764d70573ec599f6a1f0b5dc2c4491ed8e39a`  
		Last Modified: Tue, 03 Jun 2025 13:37:40 GMT  
		Size: 30.9 MB (30947484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35acbe10412254f3364c6f1d25b017d5adb3a767bf8074b34180643aaabd3a2a`  
		Last Modified: Tue, 03 Jun 2025 13:37:42 GMT  
		Size: 20.1 MB (20140173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138876a674c762e721ede8dbb50320c7830e29573f49e90bf6ec7e6172133423`  
		Last Modified: Tue, 03 Jun 2025 14:46:59 GMT  
		Size: 153.5 MB (153461483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df0cee5d9bfb8c6536fa6e0b0e650deacbd1bd9bb24c450915fce9616d5b75e`  
		Last Modified: Tue, 03 Jun 2025 13:37:31 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d30e50399898371eb099b2aa5d967b6a3841a7b2fa71365c15cc9e73d047b3`  
		Last Modified: Tue, 03 Jun 2025 13:37:33 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02d98eb3c94073e13cd2fd1fdfc13ea613d34dc701381b57464d4c53c7c9235`  
		Last Modified: Tue, 03 Jun 2025 13:37:34 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59451047b5b1164e4f7dca0bff5db6598d73a7dff0462ee925d25becb1380aa`  
		Last Modified: Tue, 03 Jun 2025 13:37:54 GMT  
		Size: 71.6 MB (71619160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2107148cb2ddd4b4d37c719a019b4ba4afe245415fefb9bb6aa8ae9f3d1b95ca`  
		Last Modified: Fri, 06 Jun 2025 00:08:00 GMT  
		Size: 137.4 MB (137395509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385ea45f91730ffec021cb7b4dac6c0b06ca724442528b14650f22673254b473`  
		Last Modified: Thu, 05 Jun 2025 21:21:27 GMT  
		Size: 35.0 KB (35024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:noble` - unknown; unknown

```console
$ docker pull gradle@sha256:5754c6478c8d3e0a338e3fba04ee98075706dedfeae09481740ca2ca77a9be54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7313651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5843ce29067fbe8c839417f1773bcfcf0bba56d8c273584fca4ca82b5458e5ed`

```dockerfile
```

-	Layers:
	-	`sha256:be581387496cb2092959c44d9390d06615db99ea7e071830a61d4c0354dc75da`  
		Last Modified: Thu, 05 Jun 2025 23:19:41 GMT  
		Size: 7.3 MB (7283956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f9c1329ac31cee34472e36099caa0c867562f5770ec5d76c700cbae65aed137`  
		Last Modified: Thu, 05 Jun 2025 23:19:42 GMT  
		Size: 29.7 KB (29695 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:noble` - linux; s390x

```console
$ docker pull gradle@sha256:86d7ad61e8fae1c49bd3ddd38872a402fb7e08195b4ff164e0c1e70010f0d79a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.8 MB (401760460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b7f3100805698b531a3baf1bdcf60351059501eff5e52086e24d07f982035b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:b6b8557b3fef6c06eb943ce735f649cf7033ab3925e70e6b43901f1f29b4d5e9 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='974d3acef0b7193f541acb61b76e81670890551366625d4f6ca01b91ac152ce0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='31dba70ba928c78c20d62049ac000f79f7a7ab11f9d9c11e703f52d60aa64f93';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='2ddc0dc14b07d9e853875aac7f84c23826fff18b9cea618c93efe0bcc8f419c2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        riscv64)          ESUM='d75f33ee7f9e5532bce263db83443ffed7d9bae7ff3ed41e48d137808adfe513';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='216edbccab2d677639c90d2cb09dfa39c257788a62b8b83d879528c447b9ad33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
# Thu, 05 Jun 2025 16:04:16 GMT
CMD ["gradle"]
# Thu, 05 Jun 2025 16:04:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 05 Jun 2025 16:04:16 GMT
WORKDIR /home/gradle
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
ENV GRADLE_VERSION=8.14.2
# Thu, 05 Jun 2025 16:04:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
# Thu, 05 Jun 2025 16:04:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
USER gradle
# Thu, 05 Jun 2025 16:04:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
USER root
```

-	Layers:
	-	`sha256:7fa55ab2f467363da0197dee4a8e5af9e7ba7ef5686c6f0951bc509c387b765c`  
		Last Modified: Tue, 03 Jun 2025 13:31:43 GMT  
		Size: 29.9 MB (29930056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7307db90fb2df8b2bec66d8ccfe619edd2c08ee266d3b6bb1483618c2a2afb`  
		Last Modified: Tue, 03 Jun 2025 13:37:51 GMT  
		Size: 22.1 MB (22132536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f767c347faf42229797a051c73ddd3a7e5093ca053278c3e2a78fb883c5777e6`  
		Last Modified: Tue, 03 Jun 2025 13:37:57 GMT  
		Size: 146.9 MB (146922986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda1253453eabb6e12e981c782ac9548d6190f311180344ddc4e9c4b6d1fe3c9`  
		Last Modified: Tue, 03 Jun 2025 13:37:40 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c06bc5cc48d3edcb92446966a7d31e6389c130c19697c66372e2739abf03c9`  
		Last Modified: Tue, 03 Jun 2025 13:37:42 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989cfada602969884867f746c637d45c227f35e2c1e2c932afc69f3ed2a764c0`  
		Last Modified: Tue, 03 Jun 2025 13:37:44 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbbbd715da054c215df6e18f37e6ee2dc420095442213438df924e154be208b`  
		Last Modified: Tue, 03 Jun 2025 13:37:55 GMT  
		Size: 65.3 MB (65340600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81d8b1f6b33eb36b6f297a3bb1a53a098479ad7295be6a8e8e276a8df328436`  
		Last Modified: Fri, 06 Jun 2025 00:08:32 GMT  
		Size: 137.4 MB (137395512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dabe0dc3a245a7a859abf0d4e0b0d36cac946ec40b7c244954de37182fd3ad0`  
		Last Modified: Thu, 05 Jun 2025 20:34:37 GMT  
		Size: 35.0 KB (35013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:noble` - unknown; unknown

```console
$ docker pull gradle@sha256:f195556e1ea3a80e97218615e3c1cfc7c44afab3d9b4501b4c10f69c0ec46b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7154895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71bcedfc7fe3727f045be3463b797543b28f1647ac8f73219c8cf13084f38b8c`

```dockerfile
```

-	Layers:
	-	`sha256:3aee7cf0c85dc7e92d0b7265a2c864575cb5d59d3c9443ab062b1e291a72d108`  
		Last Modified: Thu, 05 Jun 2025 23:19:48 GMT  
		Size: 7.1 MB (7125370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cd00cc063fa99e1b44729b1848c50217a598ba4da801cf9dd48b09aadb5802c`  
		Last Modified: Thu, 05 Jun 2025 23:19:49 GMT  
		Size: 29.5 KB (29525 bytes)  
		MIME: application/vnd.in-toto+json
