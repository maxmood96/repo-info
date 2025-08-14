## `gradle:7-jdk17-jammy`

```console
$ docker pull gradle@sha256:d687ceaa4588e6de7a866c1212128f449dd17ca0dfee5efeb8acb46d7561fa8b
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

### `gradle:7-jdk17-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:5529585d4650a78d2db3cb80c47f1a07c158ced3ea1fc9447401b66eceb16597
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.3 MB (374279140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09cc2f9c5b2ed30f63ef54dae938a6ce8ce423c74f999e77de2b376f241206b1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 05 Jul 2025 02:17:41 GMT
ARG RELEASE
# Sat, 05 Jul 2025 02:17:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 05 Jul 2025 02:17:41 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Sat, 05 Jul 2025 02:17:41 GMT
CMD ["/bin/bash"]
# Sat, 05 Jul 2025 02:17:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Jul 2025 02:17:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Jul 2025 02:17:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 05 Jul 2025 02:17:41 GMT
CMD ["jshell"]
# Sat, 05 Jul 2025 02:17:41 GMT
CMD ["gradle"]
# Sat, 05 Jul 2025 02:17:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 05 Jul 2025 02:17:41 GMT
WORKDIR /home/gradle
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENV GRADLE_VERSION=7.6.6
# Sat, 05 Jul 2025 02:17:41 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Sat, 05 Jul 2025 02:17:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
USER gradle
# Sat, 05 Jul 2025 02:17:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
USER root
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21202b7a8c26c2998366846f3a160592b48eb0b123d5f5e9e6a2481f88666d9e`  
		Last Modified: Tue, 12 Aug 2025 17:24:51 GMT  
		Size: 20.7 MB (20700721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf6bd137d7e53909afa1fa74eec54838d28d7b60eca08f028e99b74a138af93`  
		Last Modified: Tue, 12 Aug 2025 17:51:57 GMT  
		Size: 144.7 MB (144708996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683cfeb3a822b48ef3ed0fb42bceca40d5e8471cddd312dd748cb341fbbe073c`  
		Last Modified: Tue, 12 Aug 2025 17:24:47 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c1a22f4ef06a888c9067bc5259de406cb36f5b3e4802fb9111091151eca5dc`  
		Last Modified: Tue, 12 Aug 2025 17:24:48 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c8e3470ed15db342308e3af76d34387b403da0802165fc891b94d5936cf09f`  
		Last Modified: Tue, 12 Aug 2025 19:36:43 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941a041771d628b4c2039bd2c9d75e24adce1de46cc21c8563de72d45dc0dcf1`  
		Last Modified: Wed, 13 Aug 2025 01:01:47 GMT  
		Size: 50.8 MB (50801334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8624b89b517a3aa172aa6701707c3bcf64c1a0660c64c053c68260036118cd24`  
		Last Modified: Wed, 13 Aug 2025 01:02:00 GMT  
		Size: 128.5 MB (128469415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877d7c354a1cf61c91751f6e8c36f8dd2d1880ec79d374903e7b1338d3d1a700`  
		Last Modified: Tue, 12 Aug 2025 19:36:41 GMT  
		Size: 54.9 KB (54897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:a122409eefe65e859a7b968ace2e49840b8f5fdfa1c9a2ec7c9140ad58755486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7797752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e25b30447e9c5d395e36cd67213a333fffd6c6443893b5fa21e387be8abd87b`

```dockerfile
```

-	Layers:
	-	`sha256:6355dcad865c3bc702d476eaf97e4c74eb743fa0e95f96893d15ce9d18bdb6f9`  
		Last Modified: Tue, 12 Aug 2025 20:19:21 GMT  
		Size: 7.8 MB (7773120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15891b94dc4651c881318a2550f70429ede8c0922e3271d4c7b24d6ec9a6a823`  
		Last Modified: Tue, 12 Aug 2025 20:19:21 GMT  
		Size: 24.6 KB (24632 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk17-jammy` - linux; arm variant v7

```console
$ docker pull gradle@sha256:f09f84369891d917a964bdfb77b327a15d3e2c1c781b7d65381589e8cc79ffa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.6 MB (371587976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e3fa532646e677f979af8d1e85d12ff50173fba9ef82b8ca7bbcd7a822ebe6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 05 Jul 2025 02:17:41 GMT
ARG RELEASE
# Sat, 05 Jul 2025 02:17:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 05 Jul 2025 02:17:41 GMT
ADD file:56dd1608fa49343c3815b8373825d581303e97b21994ce0e1d099bf09251caea in / 
# Sat, 05 Jul 2025 02:17:41 GMT
CMD ["/bin/bash"]
# Sat, 05 Jul 2025 02:17:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Jul 2025 02:17:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Jul 2025 02:17:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 05 Jul 2025 02:17:41 GMT
CMD ["jshell"]
# Sat, 05 Jul 2025 02:17:41 GMT
CMD ["gradle"]
# Sat, 05 Jul 2025 02:17:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 05 Jul 2025 02:17:41 GMT
WORKDIR /home/gradle
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENV GRADLE_VERSION=7.6.6
# Sat, 05 Jul 2025 02:17:41 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Sat, 05 Jul 2025 02:17:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
USER gradle
# Sat, 05 Jul 2025 02:17:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
USER root
```

-	Layers:
	-	`sha256:6530e67fdf3958f32e486561f05a1170b5fbcd419c51eb435b13993ecadad7b3`  
		Last Modified: Tue, 12 Aug 2025 17:02:44 GMT  
		Size: 26.6 MB (26642919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6231663ad997fed039ebb761b08d8e1b3af186213bff219a7809bed21ff3d5`  
		Last Modified: Tue, 12 Aug 2025 17:31:48 GMT  
		Size: 21.0 MB (20989087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b75b2fdb124472de91a09f0da51a8dfb02d68a4f3e935ba1eeb30cc3b4fb402`  
		Last Modified: Tue, 12 Aug 2025 18:30:29 GMT  
		Size: 142.2 MB (142180924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31758fc0f894b5d7b8820e167887440edc1824d60afbc59b0f4f630b5583b939`  
		Last Modified: Tue, 12 Aug 2025 17:31:44 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360de63dad622573a9faa24ebc245999e0df940ec9b1b035a804e5ca0a9d0f92`  
		Last Modified: Tue, 12 Aug 2025 17:31:45 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d01c05832b79d93fc61866539d4213abc686ecb4844bd4dead0b9d1139e9e72`  
		Last Modified: Tue, 12 Aug 2025 18:11:49 GMT  
		Size: 4.3 KB (4300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68ae917d95ec059a19032afbadda002a70d6f1e1ccb0b44773e615996aae4c2`  
		Last Modified: Tue, 12 Aug 2025 18:12:03 GMT  
		Size: 53.3 MB (53267552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916a9df7224fbe934a4be05152b520580c4bc9eb1c9e61ea2e2242b0ea556bdc`  
		Last Modified: Tue, 12 Aug 2025 19:02:29 GMT  
		Size: 128.5 MB (128469421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a920a04a59731cbfb40d29aaffe35e83afe9cc0c866398e571719829ab122ac`  
		Last Modified: Tue, 12 Aug 2025 18:17:49 GMT  
		Size: 31.3 KB (31300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:4ed06621bf6dfb3764e76a1495a8e33377c8780dc5adbc363cb50574f5b39143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7716245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9604507efe21dd9b452a735f7531f7ffbded60b44e22f5bbf199f7a26a2d34`

```dockerfile
```

-	Layers:
	-	`sha256:73f594cd2dff263bc617482578f895ebd91cef9ed2b0970c986a681362e7d0b7`  
		Last Modified: Tue, 12 Aug 2025 20:19:29 GMT  
		Size: 7.7 MB (7691458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ac3398348e036357ba3b6d2f0886ae3ed262b82eab273df8a264b78ba35c961`  
		Last Modified: Tue, 12 Aug 2025 20:19:30 GMT  
		Size: 24.8 KB (24787 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk17-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:587b3fd793a42733fe2475e9b29a6fc8ab310b6557c88f4365730743359318f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.9 MB (371860443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e98e226574eaa7cc580d6200b0ca0f06104231a61daad31c19762735f0541814`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 05 Jul 2025 02:17:41 GMT
ARG RELEASE
# Sat, 05 Jul 2025 02:17:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 05 Jul 2025 02:17:41 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Sat, 05 Jul 2025 02:17:41 GMT
CMD ["/bin/bash"]
# Sat, 05 Jul 2025 02:17:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Jul 2025 02:17:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Jul 2025 02:17:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 05 Jul 2025 02:17:41 GMT
CMD ["jshell"]
# Sat, 05 Jul 2025 02:17:41 GMT
CMD ["gradle"]
# Sat, 05 Jul 2025 02:17:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 05 Jul 2025 02:17:41 GMT
WORKDIR /home/gradle
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENV GRADLE_VERSION=7.6.6
# Sat, 05 Jul 2025 02:17:41 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Sat, 05 Jul 2025 02:17:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
USER gradle
# Sat, 05 Jul 2025 02:17:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
USER root
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd64f9c0cf3ec5f7ce785ff4584071b2ec4640f7044349e337bfe3cce57c33ed`  
		Last Modified: Tue, 12 Aug 2025 18:35:46 GMT  
		Size: 22.1 MB (22075031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cdcf689f1acf4099a10761af720e6ba34e73c75171e3957c82295f4821a4fb`  
		Last Modified: Tue, 12 Aug 2025 19:17:04 GMT  
		Size: 143.6 MB (143550964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5921f25c735b6df8445caa9d0522f11fd276b4e4a2d4e4d0612a6c2d1e41a04`  
		Last Modified: Tue, 12 Aug 2025 18:35:44 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99da9c053b020127129a6b8a600b45f24567f545cbb8b4657a0cb5d637ba7393`  
		Last Modified: Tue, 12 Aug 2025 18:35:45 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32729d7f88d70dc028a045da4956975b507073c88146503db4aafab57621acf`  
		Last Modified: Tue, 12 Aug 2025 22:42:15 GMT  
		Size: 4.3 KB (4309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6602b14a7defbb9d3ebbc33152e33f349f53e4fa916b93744861dcfdbeef891`  
		Last Modified: Tue, 12 Aug 2025 22:42:08 GMT  
		Size: 50.3 MB (50339483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1268816201655fd56fa3b2f9d5545e9f54b3f26beed0951c607e4a4f590069`  
		Last Modified: Tue, 12 Aug 2025 23:22:55 GMT  
		Size: 128.5 MB (128469416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87be5afcc7f72d00f3b80674ddbf8dd7378d9046bf637c0c4a824d801b9882e8`  
		Last Modified: Tue, 12 Aug 2025 22:50:55 GMT  
		Size: 59.5 KB (59520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:23b71e1b175df1d6267a45b5186ddddfb7671c7f1d6e5b10dfa90fabf76294f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7899652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c0d225fa44a644e359ab6dbeb8db7b8a690a878ca84d92b5fa69eca78f50a8`

```dockerfile
```

-	Layers:
	-	`sha256:40e3cdf379a1b1ddd0f58671ebfb8b5a04c09a33fa69d98d6547126df2fb4d97`  
		Last Modified: Tue, 12 Aug 2025 23:18:37 GMT  
		Size: 7.9 MB (7874811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6b3f3b1c59fdb06cc8253bcc9972096bd638117c07268ee5de75f9062dfb276`  
		Last Modified: Tue, 12 Aug 2025 23:18:38 GMT  
		Size: 24.8 KB (24841 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk17-jammy` - linux; ppc64le

```console
$ docker pull gradle@sha256:e2a49bf5188418ad2fcd622720b3a832d4570e599aea191acb840a4fc6a9a22c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.7 MB (384669846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ff05a5b46b68f34247085861c211b9ae52fc664b091cb9f3275da5729cf6edc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 05 Jul 2025 02:17:41 GMT
ARG RELEASE
# Sat, 05 Jul 2025 02:17:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 05 Jul 2025 02:17:41 GMT
ADD file:8e490d6aa7e352ca02bf6249fe59c9445bd10be61e8a31e7d8219d7f34f3df1e in / 
# Sat, 05 Jul 2025 02:17:41 GMT
CMD ["/bin/bash"]
# Sat, 05 Jul 2025 02:17:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Jul 2025 02:17:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Jul 2025 02:17:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 05 Jul 2025 02:17:41 GMT
CMD ["jshell"]
# Sat, 05 Jul 2025 02:17:41 GMT
CMD ["gradle"]
# Sat, 05 Jul 2025 02:17:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 05 Jul 2025 02:17:41 GMT
WORKDIR /home/gradle
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENV GRADLE_VERSION=7.6.6
# Sat, 05 Jul 2025 02:17:41 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Sat, 05 Jul 2025 02:17:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
USER gradle
# Sat, 05 Jul 2025 02:17:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
USER root
```

-	Layers:
	-	`sha256:9e0049f176947659afd8c14b3a33c239a7d2fb1bdcbab338270e4d28b95b3a1d`  
		Last Modified: Tue, 12 Aug 2025 17:03:41 GMT  
		Size: 34.4 MB (34443145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea246dccf5d245b72648d22d4739d134fafd91ec98d1602a6933020bd17bf36d`  
		Last Modified: Tue, 12 Aug 2025 17:37:46 GMT  
		Size: 22.6 MB (22582240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7651a1059ec050d25c5bf470477743abd9029d2e2883d00d34c5124130f5a0`  
		Last Modified: Tue, 12 Aug 2025 18:30:25 GMT  
		Size: 144.4 MB (144376291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c990c09a3e1608a660c763ce498aa2de5118af50f511ab99b4dd4c51b58dc986`  
		Last Modified: Tue, 12 Aug 2025 17:37:44 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef404c17a68be785d25e8ac3de31837b488fc4b26dfaabb75341a0d7ff4151d7`  
		Last Modified: Tue, 12 Aug 2025 17:37:45 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b01ab49f4289fcd142572f53e6ba64c16c905fa5b5e45c307659360d88f5949`  
		Last Modified: Tue, 12 Aug 2025 23:32:54 GMT  
		Size: 4.3 KB (4309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36bc2ffae1af1a4caf7c28d00eedee3e490b0197e2512263ac9bfce84fb48881`  
		Last Modified: Tue, 12 Aug 2025 23:33:04 GMT  
		Size: 54.8 MB (54756967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69884868a704197d73a660dfa9cc5a893e867b5b95e74ca47258bd78381c6802`  
		Last Modified: Tue, 12 Aug 2025 23:47:54 GMT  
		Size: 128.5 MB (128469417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb177ca285489ce14a2edc77826fb4e2db65094f3c597153129eebb5a5523c8`  
		Last Modified: Tue, 12 Aug 2025 23:48:05 GMT  
		Size: 35.0 KB (35004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:1a5a3468398303c780713ccfdb0391c632ace019487968f69ee6ec1f913a25e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7828712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6103911fc26573ce76da5e5b94752f29555a0345a7fa3ac5545b327a7ad59e08`

```dockerfile
```

-	Layers:
	-	`sha256:7dd98547a3dbe52695fe6c7900f4915ed52a6b0fc99b0ce6fee16ecd6c62c97f`  
		Last Modified: Wed, 13 Aug 2025 02:18:52 GMT  
		Size: 7.8 MB (7804000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a7998d16606cde179a6cb53d3cb6fc619ef5728a333e10fb408211c9cbf989d`  
		Last Modified: Wed, 13 Aug 2025 02:18:52 GMT  
		Size: 24.7 KB (24712 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk17-jammy` - linux; s390x

```console
$ docker pull gradle@sha256:c7ea2d12638e0d3e03eef1d38cffd5180fef0917cb83333f2e2a9b617aad01a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.2 MB (362156731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a1f1deefec046eb3a68906591f444d8a6f0f939fbe194cfdd8cd7137ef643b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 05 Jul 2025 02:17:41 GMT
ARG RELEASE
# Sat, 05 Jul 2025 02:17:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 05 Jul 2025 02:17:41 GMT
ADD file:e0994d65dd44d220b4a55ce1033f7309688125fc54c99056866a92caff4bce78 in / 
# Sat, 05 Jul 2025 02:17:41 GMT
CMD ["/bin/bash"]
# Sat, 05 Jul 2025 02:17:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Jul 2025 02:17:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Jul 2025 02:17:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 05 Jul 2025 02:17:41 GMT
CMD ["jshell"]
# Sat, 05 Jul 2025 02:17:41 GMT
CMD ["gradle"]
# Sat, 05 Jul 2025 02:17:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 05 Jul 2025 02:17:41 GMT
WORKDIR /home/gradle
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENV GRADLE_VERSION=7.6.6
# Sat, 05 Jul 2025 02:17:41 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Sat, 05 Jul 2025 02:17:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
USER gradle
# Sat, 05 Jul 2025 02:17:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
USER root
```

-	Layers:
	-	`sha256:9c54d9d5bd2c16422a2ac0653717d2ef3d3e03f04fb894713d9682ff2fb1a339`  
		Last Modified: Tue, 12 Aug 2025 17:29:30 GMT  
		Size: 28.0 MB (28003219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f69f96d672e6f24790d41532552580e7a8a6c59a2383dc2e4f9873fdcda9ed2`  
		Last Modified: Tue, 12 Aug 2025 17:30:43 GMT  
		Size: 20.4 MB (20416263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6372e078d83c1bc9f2f68055108c3f76a521f2d59ef1d34a68393bcef9672c`  
		Last Modified: Tue, 12 Aug 2025 18:30:37 GMT  
		Size: 134.7 MB (134729909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053da4b9ae8ab5d8fade3a7996551a5bedeba29454ebed12466b749c29c82c5f`  
		Last Modified: Tue, 12 Aug 2025 17:30:41 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c229fee676ac9cb17e9ae341161d8ffebe1b4fffb8f416de4c2bfa98a6d0fa4`  
		Last Modified: Tue, 12 Aug 2025 17:30:43 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce18458669a7464b87a9adc86f0bd4e7eb294a15a6a593a3f95bda9471e5067b`  
		Last Modified: Tue, 12 Aug 2025 18:58:52 GMT  
		Size: 4.3 KB (4322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8064ac1d510008cd0f4cdef7fb4b873a62aca92011b714ba64d0fe105bde3fb0`  
		Last Modified: Tue, 12 Aug 2025 18:59:11 GMT  
		Size: 50.5 MB (50496104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779d973ef353d5ddb3c5f7b651770dc47f6d0b4b6c61c14cb51735af1649a26d`  
		Last Modified: Tue, 12 Aug 2025 21:27:53 GMT  
		Size: 128.5 MB (128469440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71853f35b4dc7c98482fb2e763767727a20d62236a0c53acec35f89396fea39`  
		Last Modified: Tue, 12 Aug 2025 19:09:08 GMT  
		Size: 35.0 KB (35002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:6d435c57fe7b92f9a58b97a0e3ef3a1a507c988fdfe50404721c11e80d80593e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7721436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:564f8d996fb2a2cd641e892cf33eff56b1f65e44e8896ca2445fac18b3703f5a`

```dockerfile
```

-	Layers:
	-	`sha256:9117185a6a971ee1e61b706eb3b6da8c8c5597961b792224d57c3e5915930dde`  
		Last Modified: Tue, 12 Aug 2025 20:19:50 GMT  
		Size: 7.7 MB (7696804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c0ed79fdac09c7e57ea0308d0afb2ac8e419161a7b07cc6e25bdc609907ef79`  
		Last Modified: Tue, 12 Aug 2025 20:19:51 GMT  
		Size: 24.6 KB (24632 bytes)  
		MIME: application/vnd.in-toto+json
