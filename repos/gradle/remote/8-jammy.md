## `gradle:8-jammy`

```console
$ docker pull gradle@sha256:5a150cde8c34e7812fd4a5ee5fc682ce417356d9de5741ff5288966291a641cc
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

### `gradle:8-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:b198cbacfa943581680fd882190dd8ae016abed1fa35fd22238293c42219c1f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.3 MB (396331268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dbe659ac01ee9c4ec3af86b29b2d345bc3ed441bba377d8dd547023238709d3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:59:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:59:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:59:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:59:25 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:59:25 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 17:59:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:59:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:59:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:59:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 17:59:33 GMT
CMD ["jshell"]
# Sat, 08 Nov 2025 18:23:03 GMT
CMD ["gradle"]
# Sat, 08 Nov 2025 18:23:03 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 08 Nov 2025 18:23:03 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 08 Nov 2025 18:23:03 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 08 Nov 2025 18:23:03 GMT
WORKDIR /home/gradle
# Sat, 08 Nov 2025 18:23:19 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 08 Nov 2025 18:23:19 GMT
ENV GRADLE_VERSION=8.14.3
# Sat, 08 Nov 2025 18:23:19 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Sat, 08 Nov 2025 18:23:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 08 Nov 2025 18:23:21 GMT
USER gradle
# Sat, 08 Nov 2025 18:23:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 08 Nov 2025 18:23:22 GMT
USER root
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2c69c2ae48b8dfa0e7524b6becae3735db162948d108f0f293ba8c0c645027`  
		Last Modified: Sat, 08 Nov 2025 18:00:00 GMT  
		Size: 20.7 MB (20700810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e364f712170579a1c9e3826e1c557039053c032b290407de83752f0040166e`  
		Last Modified: Sat, 08 Nov 2025 18:21:17 GMT  
		Size: 157.8 MB (157838996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be52b6f65f24d5d42beccb02b074c489b7fd7c6b6750076ce407d5919750ce3c`  
		Last Modified: Sat, 08 Nov 2025 17:59:58 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965340c1c3650258de014358d65dec0f58b3393c7ceae99ece6a3b275a9d9129`  
		Last Modified: Sat, 08 Nov 2025 17:59:58 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d3deee813e20ca36ff19f44789a7733ef8483bc53f7b44a523c34cfb8129d0`  
		Last Modified: Sat, 08 Nov 2025 18:23:50 GMT  
		Size: 4.3 KB (4310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a60e51379d18aa7ea01b8822811fc2531360c63d79e7844e9fb51dcc2bebd2`  
		Last Modified: Sat, 08 Nov 2025 18:23:52 GMT  
		Size: 50.8 MB (50797766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bacea1a64d688a70ba11f5af2d016e677050548269776a3b4d29600e9ec876cd`  
		Last Modified: Sat, 08 Nov 2025 18:23:47 GMT  
		Size: 137.4 MB (137395198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a03bde3286d6fc6c981543b4c7e68de44809b1bfe82a41a5cff3f961743043e`  
		Last Modified: Sat, 08 Nov 2025 18:23:50 GMT  
		Size: 54.9 KB (54898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:eb731be6f42cc6a215a5356a64bcea6edae81f35ff71051b9303a5c99a5eaa5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7890384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61dd33c4107901fc129e1de70948bdc87d2b040b74d05b59405732070e7f5108`

```dockerfile
```

-	Layers:
	-	`sha256:07aa6947bcf2ece9189567ebb7d1f4576708bfb1dfda09303d82e5f1084cd284`  
		Last Modified: Sat, 08 Nov 2025 21:25:23 GMT  
		Size: 7.9 MB (7865639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:686e61d67b104350907e48ad3bafbb909ba173bb812f8b7d4cb84a3b294c14f4`  
		Last Modified: Sat, 08 Nov 2025 21:25:24 GMT  
		Size: 24.7 KB (24745 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:ce2cba6fb1810b24402f5efcf18a2597dd1f35a9c7fa55d12a95d56c07bb06f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.4 MB (393394901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324d025908a9d1ead24b2f24c784465f38f2bfd579022abb6097c8427b121e24`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:58:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:58:55 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 17:59:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:59:04 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:59:04 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:59:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 17:59:04 GMT
CMD ["jshell"]
# Sat, 08 Nov 2025 18:23:08 GMT
CMD ["gradle"]
# Sat, 08 Nov 2025 18:23:08 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 08 Nov 2025 18:23:08 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 08 Nov 2025 18:23:08 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 08 Nov 2025 18:23:09 GMT
WORKDIR /home/gradle
# Sat, 08 Nov 2025 18:23:29 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 08 Nov 2025 18:23:29 GMT
ENV GRADLE_VERSION=8.14.3
# Sat, 08 Nov 2025 18:23:29 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Sat, 08 Nov 2025 18:23:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 08 Nov 2025 18:23:32 GMT
USER gradle
# Sat, 08 Nov 2025 18:23:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 08 Nov 2025 18:23:32 GMT
USER root
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1702c590aa52cc1a55100ef3a2722295a0e836a36483904b5ad835785fb649cf`  
		Last Modified: Sat, 08 Nov 2025 17:59:32 GMT  
		Size: 22.1 MB (22092877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70e708deb4dc5c197b7da39ba74f46ccb4672b33ed04677b073f7a62a9446a2`  
		Last Modified: Sat, 08 Nov 2025 18:20:32 GMT  
		Size: 156.1 MB (156107664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b560d7769af500a8625c4b0f3df581ee0ac48df555449344862c489442f4cf`  
		Last Modified: Sat, 08 Nov 2025 17:59:30 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582e8ef109503a10a17c82887e33e0d6b683860c18c2a59552922ceac6af9fb0`  
		Last Modified: Sat, 08 Nov 2025 17:59:30 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36c079c6257bdc6f8f1d700a20196701ca65bb572e8e62748a0a3c7ba4a8f63`  
		Last Modified: Sat, 08 Nov 2025 18:24:03 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9afc83822c6416e9aa3856bf84fdf37ca7b3a9e0aa6889b558d50ebcd8b8ca10`  
		Last Modified: Sat, 08 Nov 2025 18:24:19 GMT  
		Size: 50.3 MB (50349744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e515103506a4a0fa6aeb82e7e04a41f33442f7ac7fe9caebe3ca4e2b114cdd2e`  
		Last Modified: Sat, 08 Nov 2025 18:23:56 GMT  
		Size: 137.4 MB (137395201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f975d0950e5e92c7f3ba7485aae117527dfe5832df61f9423f011fa8c3f8364e`  
		Last Modified: Sat, 08 Nov 2025 18:24:04 GMT  
		Size: 59.5 KB (59521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:53b7c8b97f89dbab98832f349b68aa1c74369c6138b0fe103ca3c673956ad292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7992279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1701faa8d9d0a54905a7fb442a96545279ff3be37091d4c6af1a8e2c6298814e`

```dockerfile
```

-	Layers:
	-	`sha256:fbc4476b069b1cdc0f124c7179fc859052b55f4652d37c928fc3d2b07ed910c6`  
		Last Modified: Sat, 08 Nov 2025 21:25:31 GMT  
		Size: 8.0 MB (7967326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a184da88a3391487c4e107d11deec89b1b80811f7e15bdbaa34d2207816b797e`  
		Last Modified: Sat, 08 Nov 2025 21:25:32 GMT  
		Size: 25.0 KB (24953 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jammy` - linux; ppc64le

```console
$ docker pull gradle@sha256:6b3ba23b379cafc9402963ba0dececf98acad48a58c78a6a9463ee2473da6b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.2 MB (407168439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3126a7876bd4c9f03099c221e40b19aac258037d1904bbc165ab40efa820afad`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 01 Oct 2025 07:06:37 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:06:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:06:42 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Wed, 01 Oct 2025 07:06:43 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 18:10:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:10:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:10:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 18:10:07 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:10:07 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 18:19:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:19:51 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:19:52 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:19:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:19:52 GMT
CMD ["jshell"]
# Sat, 08 Nov 2025 20:17:53 GMT
CMD ["gradle"]
# Sat, 08 Nov 2025 20:17:53 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 08 Nov 2025 20:17:53 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 08 Nov 2025 20:17:53 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 08 Nov 2025 20:17:53 GMT
WORKDIR /home/gradle
# Sat, 08 Nov 2025 20:18:17 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 08 Nov 2025 20:18:17 GMT
ENV GRADLE_VERSION=8.14.3
# Sat, 08 Nov 2025 20:18:17 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Sat, 08 Nov 2025 20:18:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 08 Nov 2025 20:18:22 GMT
USER gradle
# Sat, 08 Nov 2025 20:18:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 08 Nov 2025 20:18:24 GMT
USER root
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b28c0af977be1fa691f47aa085a5dcbdecf883fed43be25218a980c6df57a94`  
		Last Modified: Sat, 08 Nov 2025 18:11:13 GMT  
		Size: 22.6 MB (22582810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b1fd71cedac2e56f2090a401ddd6149a8d12b93dfa03f7954ec5c8d47033ca`  
		Last Modified: Sat, 08 Nov 2025 22:28:21 GMT  
		Size: 157.9 MB (157949062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058a5944b46248f0426c5a065fa203efb4789f8a23a270f19c25c7e77bd22004`  
		Last Modified: Sat, 08 Nov 2025 18:20:38 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a08963ed388b1968fe1d059cbd5cfbc2e389494b500781003efef987fa0e81a`  
		Last Modified: Sat, 08 Nov 2025 18:20:38 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5d63cd014a8a5a0996d75c63970edf9a29cc952bd204dd60dbb08bb68105f0`  
		Last Modified: Sat, 08 Nov 2025 20:19:20 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a543d8410bca8f09bb9369f8f9be2225a2d56858c183263b8e024dcbdd1585`  
		Last Modified: Sat, 08 Nov 2025 20:19:24 GMT  
		Size: 54.8 MB (54752853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f15ae1b7a9d356c93584297f0b11a69c9300231d4705e902cc0e930fd42fc12`  
		Last Modified: Sat, 08 Nov 2025 20:19:14 GMT  
		Size: 137.4 MB (137395131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a37afb3f829d88561ec891a60e2e80e1297bbd09026ac378def169e188fa2ca`  
		Last Modified: Sat, 08 Nov 2025 20:19:20 GMT  
		Size: 35.0 KB (35007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:e979c35a6098742e365b7c82bdf10327d00edfab9ee93af19cdbc94e098ba91a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7921344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b11fe5398114832697d73c58b46b2cc339e78ab27a02d1f69c1cb3846e058da`

```dockerfile
```

-	Layers:
	-	`sha256:26bd418a2035c7c586904d6142b0b6506c265def5fbe3edbc597b87fecd33fd5`  
		Last Modified: Sat, 08 Nov 2025 21:25:38 GMT  
		Size: 7.9 MB (7896519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ad2bd4883a16b868f8bdf50ebb1fc2b7497d13076e2ac6422e9ecfc325ddb27`  
		Last Modified: Sat, 08 Nov 2025 21:25:39 GMT  
		Size: 24.8 KB (24825 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jammy` - linux; s390x

```console
$ docker pull gradle@sha256:9ecbdb67a3dac56400f974cc44b40019921b846823880c6a2f8d87a224e0d82f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.4 MB (383434755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:027f15909159810ceb6eefc8891ec39126240cd16e84062d46a4bcd444c9adfd`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:26 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:26 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:28 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Wed, 01 Oct 2025 07:05:28 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 18:00:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:00:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:00:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 18:00:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:00:27 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 18:07:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:07:41 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:07:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:07:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:07:41 GMT
CMD ["jshell"]
# Sat, 08 Nov 2025 18:23:23 GMT
CMD ["gradle"]
# Sat, 08 Nov 2025 18:23:23 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 08 Nov 2025 18:23:23 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 08 Nov 2025 18:23:23 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 08 Nov 2025 18:23:24 GMT
WORKDIR /home/gradle
# Sat, 08 Nov 2025 18:27:29 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 08 Nov 2025 18:27:29 GMT
ENV GRADLE_VERSION=8.14.3
# Sat, 08 Nov 2025 18:27:29 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Sat, 08 Nov 2025 18:27:36 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 08 Nov 2025 18:27:36 GMT
USER gradle
# Sat, 08 Nov 2025 18:27:37 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 08 Nov 2025 18:27:37 GMT
USER root
```

-	Layers:
	-	`sha256:e4a5a322dd65d010805129ca793d5d5e6b07872cbc2f41d566a84091b39c794e`  
		Last Modified: Thu, 02 Oct 2025 00:25:04 GMT  
		Size: 28.0 MB (28003413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e5bc38b02c86e51438b090eda672cdcfe861be42a8e425cca1357b01c1cf44`  
		Last Modified: Sat, 08 Nov 2025 18:01:13 GMT  
		Size: 20.4 MB (20416886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0945fbf93d219085934e1f0059553c8990c39c0212288d47505cca86b3ff0cf`  
		Last Modified: Sat, 08 Nov 2025 19:35:03 GMT  
		Size: 147.1 MB (147080347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf4c9828b8c1af0710bb3dd43e6b385ba511b73f66a9f9c1c38207741ecd594`  
		Last Modified: Sat, 08 Nov 2025 18:08:14 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e512b4b632fd4506a5bb581356c60c34d7706c0f395e1f2cf99d4fb6cb8ec18d`  
		Last Modified: Sat, 08 Nov 2025 18:08:14 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd0a437bc52e412cd99ce49c875f681a3468f6824c6793bd3c6d07a8f55d70a`  
		Last Modified: Sat, 08 Nov 2025 18:28:32 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebfb0099227bcef2ca200c5f379dee30715070e2f97ca89f3c41595c61879df6`  
		Last Modified: Sat, 08 Nov 2025 18:28:37 GMT  
		Size: 50.5 MB (50497122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b2d0aa80eff6363d23145c456e4d8fb8d9489fee56008b872021c747f3c1a3`  
		Last Modified: Sat, 08 Nov 2025 18:28:20 GMT  
		Size: 137.4 MB (137395197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a31bb911090559cf090953e2f428037a3f0262dbc77ba32afd9125551e148f7`  
		Last Modified: Sat, 08 Nov 2025 18:28:33 GMT  
		Size: 35.0 KB (35003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:1dcbfd2ca7ba3c44242ede5ecfa6b8a937225c7a31cec159c431ba43a776afc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7814064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f57acf27dea24220be10076f5953e10d6ced3ebe95509cd8396eb7dc9223c84a`

```dockerfile
```

-	Layers:
	-	`sha256:1cc726b6219b815d04a4103d6d1a38af0d03638e54fcef1938c184a63bf866ff`  
		Last Modified: Sat, 08 Nov 2025 21:25:45 GMT  
		Size: 7.8 MB (7789319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f6fcf02ec42ca362ddae11d77746f15a5a6a17c51340245767e661a745d356e`  
		Last Modified: Sat, 08 Nov 2025 21:25:45 GMT  
		Size: 24.7 KB (24745 bytes)  
		MIME: application/vnd.in-toto+json
