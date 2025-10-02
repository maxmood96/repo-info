## `gradle:jdk-jammy`

```console
$ docker pull gradle@sha256:2ea1a66486c64d4492227a554817dc637f1e7284acfc1c86e943b8041d83c838
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

### `gradle:jdk-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:82e9b13e22797f7fa8e6e751398494089770f64d05ed6ac442df2dd8fa7cccd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.9 MB (393887108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa8f1981ee5388bf694cb46438c54a1276cabf8ade3dc8476e401096ba97e71`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["gradle"]
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 30 Sep 2025 09:31:25 GMT
WORKDIR /home/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_VERSION=9.1.0
# Tue, 30 Sep 2025 09:31:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER gradle
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER root
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6db01968dec5422143ca20241b7e6c8ad46caee949abf4078c57f6b57a3ea9b`  
		Last Modified: Mon, 01 Sep 2025 23:09:00 GMT  
		Size: 20.7 MB (20700719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b60e486d958e30feaa19f7611bf1eabbc9b58f02a923ba54d78244b20398c1a`  
		Last Modified: Tue, 02 Sep 2025 00:11:14 GMT  
		Size: 157.8 MB (157809326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6120984b6f35ac69dd1cd2a895fa2a353eef3edb8dad7539e1b796fe8a97757`  
		Last Modified: Mon, 01 Sep 2025 23:08:58 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e4d5608b5d0f1473f670c627420caef94f8c549b943262ab5a6301b0b9160c`  
		Last Modified: Mon, 01 Sep 2025 23:08:55 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fa419028967a90c7de6064146c6fd323f8175bce51e62036bb683344fbc8ac`  
		Last Modified: Tue, 30 Sep 2025 16:57:15 GMT  
		Size: 4.3 KB (4309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074c95918dfdf5b64e55d27959737e5d9a627564ba256274fb297975b86ec543`  
		Last Modified: Tue, 30 Sep 2025 16:57:21 GMT  
		Size: 51.3 MB (51263766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e1f77aa24c85572a31c1189289c1fe5cfbf5a9ea8ba1aa879f6706975fe3dc`  
		Last Modified: Wed, 01 Oct 2025 14:22:17 GMT  
		Size: 134.5 MB (134514680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bacc0d95e72bf07af4a5255cbc0927ffb3e4bd4b529bac09eb4d9b3df2319cec`  
		Last Modified: Tue, 30 Sep 2025 16:57:15 GMT  
		Size: 54.9 KB (54898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:4ea32a2564297885a98ab091e260f0cbee0256e148d1bcc1b998575a6bfa118c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7879866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c40a9291e0b887e5f8ae1f08a8bf5c7a9b5fe816841b6cb353bb34a3fca0a2aa`

```dockerfile
```

-	Layers:
	-	`sha256:c77c10f9d4fd7bb20632886ee1b2b527fb45da646480ad7df802a2824cc04bb8`  
		Last Modified: Wed, 01 Oct 2025 14:20:53 GMT  
		Size: 7.9 MB (7853974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d41b050e26763eac99a9afc63b451b18721d67b48079e87a1f67a013e5586621`  
		Last Modified: Wed, 01 Oct 2025 14:20:54 GMT  
		Size: 25.9 KB (25892 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:a7bf376922679fc4393c253d7621bac36081f2a6dfe4286e961c07c40d86c484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.5 MB (390480982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ffa9c21be54b0aacc8e83b3b8566172b9142a6d3c979bc1ec4f6cbb297bfb7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["gradle"]
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 30 Sep 2025 09:31:25 GMT
WORKDIR /home/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_VERSION=9.1.0
# Tue, 30 Sep 2025 09:31:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER gradle
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER root
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17471f93170246329b5bfbfd198178e5f2e63ad2df8453e4e914a2f743c3723`  
		Last Modified: Thu, 02 Oct 2025 01:18:02 GMT  
		Size: 22.1 MB (22078740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a949ce1ff73dcc7be415c57ebd6b5cb643191c5104da87ad00b767ed6f9145b`  
		Last Modified: Thu, 02 Oct 2025 02:16:27 GMT  
		Size: 156.1 MB (156088616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a69383b5d8b8b65fa827eeb67703a8fea52697943c1a8e09da2e630d3192a5a`  
		Last Modified: Thu, 02 Oct 2025 01:18:00 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa20f6fcb0a53f726b3966db3c3dc597c9db0d2937e209787702548ead4f06b3`  
		Last Modified: Thu, 02 Oct 2025 01:18:00 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c7ded6b963a72e43b84c111d1e2a4e9a9af0a420ed8ff3849e58ff3e091173`  
		Last Modified: Thu, 02 Oct 2025 02:17:17 GMT  
		Size: 4.3 KB (4312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8bf1dff89fa4304c22dccaf18e5f2919bd602196c32a78fead5f79664becb7`  
		Last Modified: Thu, 02 Oct 2025 02:17:20 GMT  
		Size: 50.3 MB (50349469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba96c241b9e2c4f9a2dceb1b9b2f2a4f126ded8d165353ec2a24086911d2075`  
		Last Modified: Thu, 02 Oct 2025 06:09:56 GMT  
		Size: 134.5 MB (134514745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0be8cff0e28f5433eccfe8dd8bdc494516a072ee3efc08e5e3d1a0335ac23c`  
		Last Modified: Thu, 02 Oct 2025 02:17:17 GMT  
		Size: 59.5 KB (59522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:14bc63a6db5d9bf38b5a5ebacf3c51f8348422993a3a5d0de4719be36f779237
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7981834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2c9117da057e20f9a33142044afdff0f95dc62d1eb84f892fb0f51de78bac1`

```dockerfile
```

-	Layers:
	-	`sha256:9aea4de556866fb3d18f86d0cd5f5516d07425f51f55bc6615f18ea7b42eb71b`  
		Last Modified: Thu, 02 Oct 2025 05:29:07 GMT  
		Size: 8.0 MB (7955697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1b66fcc4eb170101edb8d7114f0f67baa5cdfa0edfc3d3f32d26497c202b24e`  
		Last Modified: Thu, 02 Oct 2025 05:29:08 GMT  
		Size: 26.1 KB (26137 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-jammy` - linux; ppc64le

```console
$ docker pull gradle@sha256:25c088071628155105ccb51d68dedddf287f57cf89657d3e9d84295602ad2e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.3 MB (404307459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac321e5dc03a8a8d551f29fdfcaa14ff99fae6d01bdf57cc652b53ded98a9062`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["gradle"]
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 30 Sep 2025 09:31:25 GMT
WORKDIR /home/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_VERSION=9.1.0
# Tue, 30 Sep 2025 09:31:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER gradle
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER root
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ac4f459c7226effc55c25655a772ab01a4267f689ebfa8bfb3d1cb2820e159`  
		Last Modified: Thu, 02 Oct 2025 01:29:24 GMT  
		Size: 22.6 MB (22582015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b28e7f96838afb2f94a133cd33ad92f7069e5ca6cc1099d0b87534e332dc03`  
		Last Modified: Thu, 02 Oct 2025 03:20:52 GMT  
		Size: 158.0 MB (157969717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5133e4db74a2fdebebb8b8d6a438425bfe7011a3adaf6093710bb0a7ca5f083`  
		Last Modified: Thu, 02 Oct 2025 01:35:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e75afe318af8bab2be7d8da2068aec101eb9437edbe04e7c76a7a4d577b517`  
		Last Modified: Thu, 02 Oct 2025 01:35:19 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e887a50ab2abdecbbd070782e5ad6629e95afe1df3143688fc781f250565ff6`  
		Last Modified: Thu, 02 Oct 2025 05:19:06 GMT  
		Size: 4.3 KB (4312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61acf0e8ce8f37e2e1dbf81a89be02fd36e798f63a49623ceb639e8758daefcf`  
		Last Modified: Thu, 02 Oct 2025 06:12:17 GMT  
		Size: 54.8 MB (54752465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402662be4c7021618d35bf28e58e529c5a3c3c3f3742206b8207d70a25c6839e`  
		Last Modified: Thu, 02 Oct 2025 06:12:27 GMT  
		Size: 134.5 MB (134514676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e9bb1ac44ba26ccd54356ace50eef6647abfbfe4a2578e908d01224f316ce3`  
		Last Modified: Thu, 02 Oct 2025 05:19:10 GMT  
		Size: 35.0 KB (35011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:b5821890f50946393d0d331b10cdd935614e043dbf39c779bce5bb379b53f633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7910861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:148fe01ae23eb5e7dc4be25b5d08294b9f8dc8a1e843d7a7af2a93768e504144`

```dockerfile
```

-	Layers:
	-	`sha256:90a4448aaa0e55d56ad2ce3b1acde8d03115c7b0fbd2bdaa7ec815d662ceeb9b`  
		Last Modified: Thu, 02 Oct 2025 08:25:10 GMT  
		Size: 7.9 MB (7884872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f1475f7d81a201424a48a1046a9493d5fb78f3e4b53e50a65d353f12704d8f4`  
		Last Modified: Thu, 02 Oct 2025 08:25:10 GMT  
		Size: 26.0 KB (25989 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-jammy` - linux; s390x

```console
$ docker pull gradle@sha256:b9e1641151bb97521e375b1617a7409de6e7f1b8d4386eb7318e093853b56884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.5 MB (380509015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369443f51e28ffc30fbb454970ec334fb12fdf8877294f9ec87f54ad68a9b86c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["gradle"]
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 30 Sep 2025 09:31:25 GMT
WORKDIR /home/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_VERSION=9.1.0
# Tue, 30 Sep 2025 09:31:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER gradle
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER root
```

-	Layers:
	-	`sha256:e4a5a322dd65d010805129ca793d5d5e6b07872cbc2f41d566a84091b39c794e`  
		Last Modified: Thu, 02 Oct 2025 00:25:04 GMT  
		Size: 28.0 MB (28003413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5db983e1437101247e4457123304ebfed1b2f5bda55689e0208bb26f3ad06dd`  
		Last Modified: Thu, 02 Oct 2025 01:18:11 GMT  
		Size: 20.4 MB (20415506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16e37acb1b2c44cc09a24ba3c22be7be7d4cf3cc202a620d974ef303854aa65`  
		Last Modified: Thu, 02 Oct 2025 03:16:49 GMT  
		Size: 147.0 MB (147036660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05399d9e93b8f796f2926196440e859fbe1ca4a4a013513fdfa855890a0c9dcb`  
		Last Modified: Thu, 02 Oct 2025 01:21:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01967decf688d77bed000140aefe8b8cad2c7f0ad32257c6718e29272edc767`  
		Last Modified: Thu, 02 Oct 2025 01:21:59 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a5b2d3ef5af8d4aa254a371ba5217ae2732a14e1d4b964c8a9fa42c8550cd3`  
		Last Modified: Thu, 02 Oct 2025 02:47:06 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88715cbbbfa858f09e56d3874f6ee247630287be63fb032da3e6826aaf8b8fc1`  
		Last Modified: Thu, 02 Oct 2025 02:47:18 GMT  
		Size: 50.5 MB (50496971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6d1cfb52499aa8313ab65f17aa323b4d7b8c654d2aa466ad40050455969d88`  
		Last Modified: Thu, 02 Oct 2025 03:16:44 GMT  
		Size: 134.5 MB (134514673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318934f43313cc71212b7d11305b2b862f08bd08ec2fa320dabd5e104e780605`  
		Last Modified: Thu, 02 Oct 2025 02:47:05 GMT  
		Size: 35.0 KB (35009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:e6062fc0865e0809b55fb481bdbc28d7391b5c54de411d4231312fdae1bd5a49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7803546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d260e7b350984408eb7fcc73f76be4118c799d4e1a7afb6078acc7f2e84fe8`

```dockerfile
```

-	Layers:
	-	`sha256:949ed32f9aa6359f60eb897f000b724356e417deff31867c0ba2d79623bc0fc2`  
		Last Modified: Thu, 02 Oct 2025 05:29:19 GMT  
		Size: 7.8 MB (7777654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a763d1bcc7c184f2f734a3edd93e63402a56e0da39b8152f9b706b87dff8ade`  
		Last Modified: Thu, 02 Oct 2025 05:29:19 GMT  
		Size: 25.9 KB (25892 bytes)  
		MIME: application/vnd.in-toto+json
