## `gradle:6-jdk-jammy`

```console
$ docker pull gradle@sha256:29b3c6e0445e821372e0c9fb4d70ee64a1f7aff4726109f72cd6f263a9e8e1ab
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

### `gradle:6-jdk-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:c1da6da9902339a311978210e44dc6ab76b34f282b1f4d63b1c8e0b9de796dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.6 MB (366598842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dcd97ac58c2009942c5741598cd8c8940d054ffd0847755889bc38c245eac5d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a2650fba422283fbed20d936ce5d2a52906a5414ec17b2f7676dddb87201dbae';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='04fe1273f624187d927f1b466e8cdb630d70786db07bee7599bfa5153060afd3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='163724b70b86d5a8461f85092165a9cc5a098ed900fee90d1b0c0be9607ae3d2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='5ba742c87d48fcf564def56812699f6499a1cfd3535ae43286e94e74b8165faf';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
# Tue, 18 Feb 2025 21:10:38 GMT
CMD ["gradle"]
# Tue, 18 Feb 2025 21:10:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 18 Feb 2025 21:10:38 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 18 Feb 2025 21:10:38 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 18 Feb 2025 21:10:38 GMT
WORKDIR /home/gradle
# Tue, 18 Feb 2025 21:10:38 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 18 Feb 2025 21:10:38 GMT
ENV GRADLE_VERSION=6.9.4
# Tue, 18 Feb 2025 21:10:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Tue, 18 Feb 2025 21:10:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 18 Feb 2025 21:10:38 GMT
USER gradle
# Tue, 18 Feb 2025 21:10:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 18 Feb 2025 21:10:38 GMT
USER root
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9ce665314df6489df49d894b81a8b7d89dcbb3916abb4b8f2d9f04f7f30fba`  
		Last Modified: Tue, 04 Feb 2025 04:40:16 GMT  
		Size: 20.7 MB (20684621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c63f325f81a44cbc524343f5cdcec789fb188c2333543d3238cdac7cfeafb7`  
		Last Modified: Tue, 04 Feb 2025 04:40:18 GMT  
		Size: 157.6 MB (157591234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864a83d54ff514b209c491364b5476319cda130d7de9e481c432148668d4f0ab`  
		Last Modified: Tue, 04 Feb 2025 04:40:16 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8df0decf9d7f3577a33fb03b83ae0fc1cb904ea030014ac9bc7a5954ccbfec`  
		Last Modified: Tue, 04 Feb 2025 04:40:16 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3111ba799f3d278b6762d4679f17be7131bf1791ad1d290dfd1ae785f302e272`  
		Last Modified: Wed, 19 Feb 2025 21:30:33 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8132c7ede71d66c6d5c9844b75b0df3eefa7d07138c70a8929974e74eb4188`  
		Last Modified: Wed, 19 Feb 2025 21:30:34 GMT  
		Size: 50.7 MB (50652329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e980dcd4d579990afa902e87c71b4669e02bd2e01f90d0dabc1ba688bd742b`  
		Last Modified: Wed, 19 Feb 2025 21:30:35 GMT  
		Size: 107.7 MB (107696663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bea2b722503009f9fc19aff070ad023e3ae79e3493a19ae56c42052d5fcdff0`  
		Last Modified: Wed, 19 Feb 2025 21:30:33 GMT  
		Size: 431.3 KB (431270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:b06f96126648a4206be3cedd1a6a5359d836264d09f5ee68ec9b6ba94d4b98e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7511599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daac6fb6c3cc27211119ce5743dac431ca41b89d3632750051d41ba6e9073e2f`

```dockerfile
```

-	Layers:
	-	`sha256:09fc6943df3221be699c9712384d231ad24bead8aab07d64376b7e2b1877d960`  
		Last Modified: Wed, 19 Feb 2025 21:30:33 GMT  
		Size: 7.5 MB (7488341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69fcbb09d6d63c214e5523d4c8f21e53065968b8779d8446669a9d0a7d9a0e68`  
		Last Modified: Wed, 19 Feb 2025 21:30:33 GMT  
		Size: 23.3 KB (23258 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:8e90cdcef487e995f9885ee2f115c4fbd1f1b85d0d8328c63c1eece344e981e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.6 MB (363645525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa8e03dfada81d8b6314c93d5e8c7779dae03dc3a54f681e970e141e520d30b8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a2650fba422283fbed20d936ce5d2a52906a5414ec17b2f7676dddb87201dbae';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='04fe1273f624187d927f1b466e8cdb630d70786db07bee7599bfa5153060afd3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='163724b70b86d5a8461f85092165a9cc5a098ed900fee90d1b0c0be9607ae3d2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='5ba742c87d48fcf564def56812699f6499a1cfd3535ae43286e94e74b8165faf';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
# Tue, 18 Feb 2025 21:10:38 GMT
CMD ["gradle"]
# Tue, 18 Feb 2025 21:10:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 18 Feb 2025 21:10:38 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 18 Feb 2025 21:10:38 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 18 Feb 2025 21:10:38 GMT
WORKDIR /home/gradle
# Tue, 18 Feb 2025 21:10:38 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 18 Feb 2025 21:10:38 GMT
ENV GRADLE_VERSION=6.9.4
# Tue, 18 Feb 2025 21:10:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Tue, 18 Feb 2025 21:10:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 18 Feb 2025 21:10:38 GMT
USER gradle
# Tue, 18 Feb 2025 21:10:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 18 Feb 2025 21:10:38 GMT
USER root
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917805cfb6502c189ce3cf996ddbc16ac349000799293570d30f8455b5182667`  
		Last Modified: Tue, 04 Feb 2025 09:21:30 GMT  
		Size: 22.1 MB (22066656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59234f8844652c8c120816e45f1ec1e0a572df42dc02216a900effd642bcaa7a`  
		Last Modified: Tue, 04 Feb 2025 09:24:12 GMT  
		Size: 155.9 MB (155867873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1bc701a616a1c3a463bab5785d49f63264c0d90e7b71527b22f03f2acdfc402`  
		Last Modified: Tue, 04 Feb 2025 09:24:07 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c78c35442c357eb9d11a68f29737b48872f43824c72b85021cf5bd4dd1726d7`  
		Last Modified: Tue, 04 Feb 2025 09:24:07 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f0dad0af645df8668cb4e15b1cde17a8cbf61b2b48ffba400233d60c719991`  
		Last Modified: Wed, 19 Feb 2025 21:38:17 GMT  
		Size: 4.3 KB (4318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638d6e5c95a6ecc71556c82068d65289644b3f46a9ea50e53ddf1a443eb0b2fb`  
		Last Modified: Wed, 19 Feb 2025 21:38:19 GMT  
		Size: 50.2 MB (50224328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b389388f4127cb8dfea196fc14ff5538227ba4e2a043539098693103407a415`  
		Last Modified: Wed, 19 Feb 2025 22:33:27 GMT  
		Size: 107.7 MB (107696668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609b9551fec2351b543de7606d70e49d2c6d722ec6b4c64671ecea81086b5239`  
		Last Modified: Wed, 19 Feb 2025 22:33:24 GMT  
		Size: 425.0 KB (425026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:135a0a1ddfd4cf416fd13a9ffd1a0afa3ea9948b9bf6eb1a2a13e457bb87429f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7613493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e94e758a91273c7b4c898c09609ca2b0f129e56577a1574dc34e44022820ee`

```dockerfile
```

-	Layers:
	-	`sha256:f8e306923616ce8059d1612cab6435bb9edf577e3f80348bde0aed66d10011da`  
		Last Modified: Wed, 19 Feb 2025 22:33:24 GMT  
		Size: 7.6 MB (7590027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36a8a92302c4959563c83e4c77bcb7fea8bd49646185160a90b7b322a322a2f1`  
		Last Modified: Wed, 19 Feb 2025 22:33:23 GMT  
		Size: 23.5 KB (23466 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk-jammy` - linux; ppc64le

```console
$ docker pull gradle@sha256:90de2afae5c851975671ecceb1461922269e3079452f9cd55c3e58fd25890598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.1 MB (377130713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5497a20512bb4585fece84faef8db12e533a995f253c17bbf65e1c4d428fcf70`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:49 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:54 GMT
ADD file:378a1f28ba6d12429f01a1e40af6c7964a243df3db0827fc9d3841a0e7e3730d in / 
# Sun, 26 Jan 2025 05:31:54 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a2650fba422283fbed20d936ce5d2a52906a5414ec17b2f7676dddb87201dbae';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='04fe1273f624187d927f1b466e8cdb630d70786db07bee7599bfa5153060afd3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='163724b70b86d5a8461f85092165a9cc5a098ed900fee90d1b0c0be9607ae3d2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='5ba742c87d48fcf564def56812699f6499a1cfd3535ae43286e94e74b8165faf';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
# Tue, 18 Feb 2025 21:10:38 GMT
CMD ["gradle"]
# Tue, 18 Feb 2025 21:10:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 18 Feb 2025 21:10:38 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 18 Feb 2025 21:10:38 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 18 Feb 2025 21:10:38 GMT
WORKDIR /home/gradle
# Tue, 18 Feb 2025 21:10:38 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 18 Feb 2025 21:10:38 GMT
ENV GRADLE_VERSION=6.9.4
# Tue, 18 Feb 2025 21:10:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Tue, 18 Feb 2025 21:10:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 18 Feb 2025 21:10:38 GMT
USER gradle
# Tue, 18 Feb 2025 21:10:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 18 Feb 2025 21:10:38 GMT
USER root
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c160352719b7340e76a313ad80f511c074773ef617a01e4bcc9435ed413bc462`  
		Last Modified: Tue, 04 Feb 2025 07:41:30 GMT  
		Size: 22.6 MB (22603358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ab2518913c7f986954af54671e54121a09b63eb8adf6aac7850946948e3e84`  
		Last Modified: Tue, 04 Feb 2025 07:46:28 GMT  
		Size: 157.8 MB (157756827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ade24f7ca1e93a21e6daec603239d600a2692b3f5e352aaac7a2473d449f0b7`  
		Last Modified: Tue, 04 Feb 2025 07:46:21 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89c7cc768596b27af6ae26b94884960f2ef136a0e4352176506507562948258`  
		Last Modified: Tue, 04 Feb 2025 07:46:21 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f23b41a730e497c647d550fa9be3d6dc7054d0f4505cd0cf466b7221fedfd2`  
		Last Modified: Wed, 19 Feb 2025 21:38:28 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfc09ea50200d9ade008126185b9466265bc957f0548487c07bf04c7f03b927`  
		Last Modified: Wed, 19 Feb 2025 21:38:30 GMT  
		Size: 54.6 MB (54584157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427321c95878bb790731e6c1d388b9b833e9c65bc9f413a74824ea238b80fae9`  
		Last Modified: Wed, 19 Feb 2025 22:08:23 GMT  
		Size: 107.7 MB (107696665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e956e891c0b01303fa17a92f357f0d73d531f643a825b73f1cbe5f218ee88f0`  
		Last Modified: Wed, 19 Feb 2025 22:08:19 GMT  
		Size: 35.0 KB (34983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:aa125d58a07f110b39316a068d3b1575a728acea3ed1974624cdfa6ee86fe349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7542361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:406061cb3c404927b610b212778a56999826a4d4408615578c34f30eb745c4dd`

```dockerfile
```

-	Layers:
	-	`sha256:f7a1c980f9f718d0df4d3e8f38dc690e03883679d33c3495c3bd2478576ae08c`  
		Last Modified: Wed, 19 Feb 2025 22:08:20 GMT  
		Size: 7.5 MB (7519024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bd9dda055050dddff3aecf8c1dc26cde5f4286a1d34804c0f887c097f6b7a0b`  
		Last Modified: Wed, 19 Feb 2025 22:08:19 GMT  
		Size: 23.3 KB (23337 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk-jammy` - linux; s390x

```console
$ docker pull gradle@sha256:2c1b92d17f19cb7ed052ff0affdb57526657f0e7a728de457139341cd0d2b607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.4 MB (353365926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e25c0087fd4edc489edd34a63109ecd37180afb745cc172c1370a19ed410cd6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:03 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:03 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:05 GMT
ADD file:39a6583c8b71c00e0ea7562cadb2b343caf5c0c274178520c7476e53faed2e3e in / 
# Sun, 26 Jan 2025 05:32:05 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a2650fba422283fbed20d936ce5d2a52906a5414ec17b2f7676dddb87201dbae';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='04fe1273f624187d927f1b466e8cdb630d70786db07bee7599bfa5153060afd3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='163724b70b86d5a8461f85092165a9cc5a098ed900fee90d1b0c0be9607ae3d2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='5ba742c87d48fcf564def56812699f6499a1cfd3535ae43286e94e74b8165faf';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
# Tue, 18 Feb 2025 21:10:38 GMT
CMD ["gradle"]
# Tue, 18 Feb 2025 21:10:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 18 Feb 2025 21:10:38 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 18 Feb 2025 21:10:38 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 18 Feb 2025 21:10:38 GMT
WORKDIR /home/gradle
# Tue, 18 Feb 2025 21:10:38 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 18 Feb 2025 21:10:38 GMT
ENV GRADLE_VERSION=6.9.4
# Tue, 18 Feb 2025 21:10:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Tue, 18 Feb 2025 21:10:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 18 Feb 2025 21:10:38 GMT
USER gradle
# Tue, 18 Feb 2025 21:10:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 18 Feb 2025 21:10:38 GMT
USER root
```

-	Layers:
	-	`sha256:7ed94a91c4e77c2e320a028b45fcefc9419c4df2b3d6494bf92ab5d08bba4d77`  
		Last Modified: Sun, 26 Jan 2025 07:02:32 GMT  
		Size: 28.0 MB (28000931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09541f0a7d4a9736c68565b6e960293f3fc483af161c0194cfc64127082d6baf`  
		Last Modified: Tue, 04 Feb 2025 07:44:52 GMT  
		Size: 20.4 MB (20404458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef520f734172c35c7b01cb703ede04fe6d525142c7020388d35dbe4893011a69`  
		Last Modified: Tue, 04 Feb 2025 07:48:40 GMT  
		Size: 146.9 MB (146871490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef02e15e8ea5ff67ec5789806560db2847978910283def158b9607e6feb1900d`  
		Last Modified: Tue, 04 Feb 2025 07:48:37 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96a7f46e96fd18348ca0cc0868e26ec7a6e6dfe6a8c38aa7d452d01f1dd1362`  
		Last Modified: Tue, 04 Feb 2025 07:48:37 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f3b49d678ffb96797952b6b58e103097f46dacc1f6e4aeb5e20127d162b90a`  
		Last Modified: Wed, 19 Feb 2025 21:35:17 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda3bb079b88ce1cc3d53d59b83de789d0293e7a8fd531e725b02422e5a8f0fe`  
		Last Modified: Wed, 19 Feb 2025 21:35:18 GMT  
		Size: 50.4 MB (50350605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe9f666a00cacb4f8232f4df5c23e655145139562ee78b1808ddc6ec82da7ec`  
		Last Modified: Wed, 19 Feb 2025 21:52:58 GMT  
		Size: 107.7 MB (107696668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9946a0ad4881e3e41163929cecf09fbf0e5a943cc3929379ff2e85c01de47b59`  
		Last Modified: Wed, 19 Feb 2025 21:52:56 GMT  
		Size: 35.0 KB (34989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:276d4adad70f43315f1085f7f78e50f78488cacd6026f2db32bf6677244b1ed2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0297c011cce1537190a33ce8ce1e2225096c65e9e3021eb97565f311a2099550`

```dockerfile
```

-	Layers:
	-	`sha256:061ecfd456ea54363663f58bc7d93fdf5af589624b7521cf93b86fa66d1e6f21`  
		Last Modified: Wed, 19 Feb 2025 21:52:56 GMT  
		Size: 7.4 MB (7412022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73524d75a2fd488843f8ec163bd299bd40c55e09587b49556d742890b1008557`  
		Last Modified: Wed, 19 Feb 2025 21:52:55 GMT  
		Size: 23.3 KB (23257 bytes)  
		MIME: application/vnd.in-toto+json
