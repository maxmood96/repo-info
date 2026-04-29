## `gradle:9-jdk-lts-and-current-noble`

```console
$ docker pull gradle@sha256:2d3db697a76830975e375a1a0a6393dc57af39855c7ac4a5c6c4e9c81a15f7f6
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

### `gradle:9-jdk-lts-and-current-noble` - linux; amd64

```console
$ docker pull gradle@sha256:7b3b93ec6d76ec37eea2e487ce8e44a82f42ddd22f79586d98c595c7f8557639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.3 MB (441293385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a711f81a80d092de9084aeb0ef0788f4d8f05982f3c6f416fce8a24da25f91`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:34:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:34:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:34:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:34:26 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:34:26 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Wed, 15 Apr 2026 20:34:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='987387933b64b9833846dee373b640440d3e1fd48a04804ec01a6dbf718e8ab8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='a9d73e711d967dc44896d4f430f73a68fd33590dabc29a7f2fb9f593425b854c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='b262b735b215173003766da36588d5f717dceada0286db41b439f93fb2ada468';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        riscv64)          ESUM='168119e4fba350f4e6b3ca92450a2b90a8502b89a235a04415e9adf9f5d3164e';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_riscv64_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='15e5cbcadcf3d43623c31b825063cdc2817b9f1ba840b51dc6ef70e5d33c84e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:34:47 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 20:34:47 GMT
CMD ["jshell"]
# Tue, 28 Apr 2026 23:31:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk26 # buildkit
# Tue, 28 Apr 2026 23:31:30 GMT
RUN set -o errexit -o nounset     && ln --symbolic /opt/java/openjdk /opt/java/openjdk25 # buildkit
# Tue, 28 Apr 2026 23:31:30 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk25
# Tue, 28 Apr 2026 23:31:30 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk26
# Tue, 28 Apr 2026 23:31:30 GMT
CMD ["gradle"]
# Tue, 28 Apr 2026 23:31:30 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 28 Apr 2026 23:31:30 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Tue, 28 Apr 2026 23:31:30 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 28 Apr 2026 23:31:31 GMT
WORKDIR /home/gradle
# Tue, 28 Apr 2026 23:31:51 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 28 Apr 2026 23:31:51 GMT
ENV GRADLE_VERSION=9.5.0
# Tue, 28 Apr 2026 23:31:51 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Tue, 28 Apr 2026 23:31:54 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 28 Apr 2026 23:31:54 GMT
USER gradle
# Tue, 28 Apr 2026 23:31:54 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 28 Apr 2026 23:31:54 GMT
USER root
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6278b6d85f88f131710db43937ce991b11cd7dab1ca01c4cca26d2c8b6a05b`  
		Last Modified: Wed, 15 Apr 2026 20:35:03 GMT  
		Size: 17.5 MB (17462574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b037921f813c98a3d0b72a394a53d1037fbc29374a9ac4d1980ea85981d5a6`  
		Last Modified: Wed, 15 Apr 2026 20:35:05 GMT  
		Size: 92.4 MB (92388672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:456eee9f1cc21d140a5661456cf0038e5a125c7cb15f61a78bee9a0defab79b7`  
		Last Modified: Wed, 15 Apr 2026 20:35:02 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7390f13498b52b655175291ff4a9967d9b205667926883778c6e789d3f302d95`  
		Last Modified: Tue, 28 Apr 2026 23:32:20 GMT  
		Size: 94.5 MB (94456145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e6246dcb609a5fb9a8ba07146eccda4d1ad23b5d865e6c9f7fb60927c47b00`  
		Last Modified: Tue, 28 Apr 2026 23:32:15 GMT  
		Size: 152.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70112f201a4965f20f042031d2da23486b75037286a8bb3c299c0749e9ed689d`  
		Last Modified: Tue, 28 Apr 2026 23:32:15 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635ddc83689d5b72ae4ff96eb2dd2c043697e2f2bb3b6a32ea17f8e7c8a20283`  
		Last Modified: Tue, 28 Apr 2026 23:32:19 GMT  
		Size: 67.0 MB (66987560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266bccc203c263aa104d4dee99ce29406c6bca03015b739278994c0a5ffc6aea`  
		Last Modified: Tue, 28 Apr 2026 23:32:22 GMT  
		Size: 140.2 MB (140235939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e4ffcd27f825598dd8cc4d6fa6c4f19c82ff35178d06380cf9202d51c3827e`  
		Last Modified: Tue, 28 Apr 2026 23:32:17 GMT  
		Size: 25.6 KB (25607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-lts-and-current-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:35acc59e3750a2d2e328ba921f1c37f5fc1a4aaaa3937e7d2beee86dfd47776b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7439149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5f1201212e9db29158d97a48953baf3b99237967b5b9c26b6ddc437bf6b0295`

```dockerfile
```

-	Layers:
	-	`sha256:db8eb84d7a2dbd0b77e77c38a0e6290b13300223c5f6f8f3ae6544bc9b2c99e8`  
		Last Modified: Tue, 28 Apr 2026 23:32:16 GMT  
		Size: 7.4 MB (7402984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f34ad237bd2ea9e3fa3f4f70424d6f9e08d41925acad8223ba20c10b4364711`  
		Last Modified: Tue, 28 Apr 2026 23:32:15 GMT  
		Size: 36.2 KB (36165 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk-lts-and-current-noble` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:b12142a5b6e6e531e33215b6bdca7591f5a44911ebd711792a306292d439a4d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **439.1 MB (439089421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79ede5cb0cc42a4357b15212bde0964fa1b1e89dad6ed9853092821835d4af79`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:34:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:34:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:34:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:34:40 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:34:40 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Wed, 15 Apr 2026 20:35:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='987387933b64b9833846dee373b640440d3e1fd48a04804ec01a6dbf718e8ab8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='a9d73e711d967dc44896d4f430f73a68fd33590dabc29a7f2fb9f593425b854c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='b262b735b215173003766da36588d5f717dceada0286db41b439f93fb2ada468';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        riscv64)          ESUM='168119e4fba350f4e6b3ca92450a2b90a8502b89a235a04415e9adf9f5d3164e';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_riscv64_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='15e5cbcadcf3d43623c31b825063cdc2817b9f1ba840b51dc6ef70e5d33c84e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:35:04 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:35:04 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:35:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 20:35:04 GMT
CMD ["jshell"]
# Tue, 28 Apr 2026 23:32:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk26 # buildkit
# Tue, 28 Apr 2026 23:32:55 GMT
RUN set -o errexit -o nounset     && ln --symbolic /opt/java/openjdk /opt/java/openjdk25 # buildkit
# Tue, 28 Apr 2026 23:32:55 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk25
# Tue, 28 Apr 2026 23:32:55 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk26
# Tue, 28 Apr 2026 23:32:55 GMT
CMD ["gradle"]
# Tue, 28 Apr 2026 23:32:55 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 28 Apr 2026 23:32:55 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Tue, 28 Apr 2026 23:32:55 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 28 Apr 2026 23:32:55 GMT
WORKDIR /home/gradle
# Tue, 28 Apr 2026 23:33:18 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 28 Apr 2026 23:33:18 GMT
ENV GRADLE_VERSION=9.5.0
# Tue, 28 Apr 2026 23:33:18 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Tue, 28 Apr 2026 23:33:20 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 28 Apr 2026 23:33:20 GMT
USER gradle
# Tue, 28 Apr 2026 23:33:20 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 28 Apr 2026 23:33:20 GMT
USER root
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712e80e9f1d62b2cdcb8742bb9be50b820684464408bf3b0e6618b72e27643e7`  
		Last Modified: Wed, 15 Apr 2026 20:35:21 GMT  
		Size: 18.7 MB (18654626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b0772df217f1503b8b46878f21bbc935f1e56b398f70466738b9d19744bc6b7`  
		Last Modified: Wed, 15 Apr 2026 20:35:23 GMT  
		Size: 91.4 MB (91424614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f8e32194280b1dd1c489a9156e4186ec96e53ffa29124387db8c3f02336eb6`  
		Last Modified: Wed, 15 Apr 2026 20:35:21 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108e0db4499b47e581e3add30c12d7afef68f936dc9f1ab9aca696c6e148a57b`  
		Last Modified: Tue, 28 Apr 2026 23:33:48 GMT  
		Size: 93.4 MB (93394867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2a73a6c65113633bc7d52436738193899c27287783a8ac7c29e4cda9d8434f`  
		Last Modified: Tue, 28 Apr 2026 23:33:43 GMT  
		Size: 152.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2a7e078e321476caa6963b0279f332e9dc83e909d8586d0315870ed5ad7a2e`  
		Last Modified: Tue, 28 Apr 2026 23:33:43 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f3b60fd388c61432dd3dd092bd44e4eb31fe7866212611d45d1f0ce5659922`  
		Last Modified: Tue, 28 Apr 2026 23:33:47 GMT  
		Size: 66.5 MB (66470414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6c062225bf3ea61155242bb8a3218be1e919e954b5c848134bd38b2554eab4`  
		Last Modified: Tue, 28 Apr 2026 23:33:49 GMT  
		Size: 140.2 MB (140235878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f98c62ccdde84ab2ced88246ff272b243175bf7e49c83ba16310f71d232336`  
		Last Modified: Tue, 28 Apr 2026 23:33:44 GMT  
		Size: 29.3 KB (29326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-lts-and-current-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:4a85cec63b25cb7ac44cafc9d3f5312b3f366750f812aa76e7d3bc69586de117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7576673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8574e63d5f48b70827d14ac9c6ac00c9a392e533a8c53147532c08cf34c44a`

```dockerfile
```

-	Layers:
	-	`sha256:4c9e1b9eb70ad83957ed74621590057eede57b1116c9e3d0c50aba754e13d10a`  
		Last Modified: Tue, 28 Apr 2026 23:33:44 GMT  
		Size: 7.5 MB (7540175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59bf968324f502ba62b3e7e6307cfb71fa33b02549e586bb0263bb10059d39b1`  
		Last Modified: Tue, 28 Apr 2026 23:33:43 GMT  
		Size: 36.5 KB (36498 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk-lts-and-current-noble` - linux; ppc64le

```console
$ docker pull gradle@sha256:c391e0d3eba4fc8c272338720c4b23e2c5926f83188258b43f3661f0c742ab0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **450.3 MB (450345965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b43ddab75f7fdc44dd1385c8fe4bb5eb3c8233f1c142704cddd75d276df088d0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:23:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 21:23:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:23:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 21:23:17 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:23:17 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Wed, 15 Apr 2026 21:23:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='987387933b64b9833846dee373b640440d3e1fd48a04804ec01a6dbf718e8ab8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='a9d73e711d967dc44896d4f430f73a68fd33590dabc29a7f2fb9f593425b854c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='b262b735b215173003766da36588d5f717dceada0286db41b439f93fb2ada468';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        riscv64)          ESUM='168119e4fba350f4e6b3ca92450a2b90a8502b89a235a04415e9adf9f5d3164e';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_riscv64_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='15e5cbcadcf3d43623c31b825063cdc2817b9f1ba840b51dc6ef70e5d33c84e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 21:23:59 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 21:23:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:23:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 21:23:59 GMT
CMD ["jshell"]
# Tue, 28 Apr 2026 23:33:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk26 # buildkit
# Tue, 28 Apr 2026 23:33:45 GMT
RUN set -o errexit -o nounset     && ln --symbolic /opt/java/openjdk /opt/java/openjdk25 # buildkit
# Tue, 28 Apr 2026 23:33:45 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk25
# Tue, 28 Apr 2026 23:33:45 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk26
# Tue, 28 Apr 2026 23:33:45 GMT
CMD ["gradle"]
# Tue, 28 Apr 2026 23:33:45 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 28 Apr 2026 23:33:45 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Tue, 28 Apr 2026 23:33:45 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 28 Apr 2026 23:33:46 GMT
WORKDIR /home/gradle
# Tue, 28 Apr 2026 23:34:28 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 28 Apr 2026 23:34:28 GMT
ENV GRADLE_VERSION=9.5.0
# Tue, 28 Apr 2026 23:34:28 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Tue, 28 Apr 2026 23:34:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 28 Apr 2026 23:34:32 GMT
USER gradle
# Tue, 28 Apr 2026 23:34:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 28 Apr 2026 23:34:34 GMT
USER root
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e58bb41e4edbeb34c365caaecd193fe9139b7eb17a5567d506790db84c8c38`  
		Last Modified: Wed, 15 Apr 2026 21:24:42 GMT  
		Size: 17.3 MB (17329160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1344210c0bbe09bafe05fd9c366be46d0433428f8673fefe368a838c43cccf8f`  
		Last Modified: Wed, 15 Apr 2026 21:24:47 GMT  
		Size: 91.8 MB (91757173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f93ab63d3deb35ce1e62c3eb126ac85439e4ae8ee1e73eb5972b7bc860c6697`  
		Last Modified: Wed, 15 Apr 2026 21:24:42 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33d30d10304e0c29746b106b636cf6d1eb835abcc6c75f9bdc81d5ff7bcaa90`  
		Last Modified: Tue, 28 Apr 2026 23:35:22 GMT  
		Size: 93.8 MB (93782510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d8dffd10753ab61e6723e4cb6543bece9c31b1b0a1f4ec97222e49618170ee`  
		Last Modified: Tue, 28 Apr 2026 23:35:17 GMT  
		Size: 151.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf55ae7ca2dcc86f4650e03e0439fff8f1282a3ac4f6c34b5ad6d8693336f39`  
		Last Modified: Tue, 28 Apr 2026 23:35:17 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed72fa463d46739fe38da49db90ef192e2bc57b899e6841fd7468f74becb3fdf`  
		Last Modified: Tue, 28 Apr 2026 23:35:21 GMT  
		Size: 72.9 MB (72922760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad8b02c1de9eec75d14194a469508fc856860af6f13789bb4a7ebbbbd97552c`  
		Last Modified: Tue, 28 Apr 2026 23:35:24 GMT  
		Size: 140.2 MB (140235899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8571c0e5825b0f1eca2531cf9fbe8ecb75f92b0d8c5dea859fadf4babe198bc6`  
		Last Modified: Tue, 28 Apr 2026 23:35:18 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-lts-and-current-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:e0e52411a26d3194b2dbb793395cb15a3c2b24c8b7bb4ee9454f7226cc30fb44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7455101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da75e615c1f3f416cafe4a6f2942edb2fe09079f37cbe71ee0bbd8341836f59`

```dockerfile
```

-	Layers:
	-	`sha256:0e47890900cb451c0be0f37a8622c95ee6dd9ea3b1e4067a7da916bd6f29b2d5`  
		Last Modified: Tue, 28 Apr 2026 23:35:18 GMT  
		Size: 7.4 MB (7418804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38e22820e9e6ba9fedb3e817597e00ec4e20cde6739d263775423e698f6285f4`  
		Last Modified: Tue, 28 Apr 2026 23:35:17 GMT  
		Size: 36.3 KB (36297 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk-lts-and-current-noble` - linux; riscv64

```console
$ docker pull gradle@sha256:710a419e5d56172015b82c67bdf1041fe76e3740f96b5920eec829cd45745b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **444.1 MB (444093743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e662f45400584c2e8d7ab7cc853aaec830588f1e2801fdcdcfdc4b6cd8d25e4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 10 Apr 2026 09:24:05 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:24:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:24:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 09:24:43 GMT
ADD file:a9a4679e3df2846468311b83a8f6ab86f5a205bab966d3f236c9f30151010c5b in / 
# Fri, 10 Apr 2026 09:24:47 GMT
CMD ["/bin/bash"]
# Thu, 16 Apr 2026 17:08:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 17:08:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 17:08:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Apr 2026 17:08:13 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Apr 2026 17:08:13 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Thu, 16 Apr 2026 17:10:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='987387933b64b9833846dee373b640440d3e1fd48a04804ec01a6dbf718e8ab8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='a9d73e711d967dc44896d4f430f73a68fd33590dabc29a7f2fb9f593425b854c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='b262b735b215173003766da36588d5f717dceada0286db41b439f93fb2ada468';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        riscv64)          ESUM='168119e4fba350f4e6b3ca92450a2b90a8502b89a235a04415e9adf9f5d3164e';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_riscv64_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='15e5cbcadcf3d43623c31b825063cdc2817b9f1ba840b51dc6ef70e5d33c84e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 16 Apr 2026 17:10:53 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 16 Apr 2026 17:10:53 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 16 Apr 2026 17:10:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 16 Apr 2026 17:10:53 GMT
CMD ["jshell"]
# Tue, 28 Apr 2026 23:54:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk26 # buildkit
# Tue, 28 Apr 2026 23:54:18 GMT
RUN set -o errexit -o nounset     && ln --symbolic /opt/java/openjdk /opt/java/openjdk25 # buildkit
# Tue, 28 Apr 2026 23:54:19 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk25
# Tue, 28 Apr 2026 23:54:19 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk26
# Tue, 28 Apr 2026 23:54:19 GMT
CMD ["gradle"]
# Tue, 28 Apr 2026 23:54:19 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 28 Apr 2026 23:54:19 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Tue, 28 Apr 2026 23:54:19 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 28 Apr 2026 23:54:19 GMT
WORKDIR /home/gradle
# Tue, 28 Apr 2026 23:57:07 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 28 Apr 2026 23:57:07 GMT
ENV GRADLE_VERSION=9.5.0
# Tue, 28 Apr 2026 23:57:07 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Tue, 28 Apr 2026 23:57:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 28 Apr 2026 23:57:35 GMT
USER gradle
# Tue, 28 Apr 2026 23:57:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 28 Apr 2026 23:57:42 GMT
USER root
```

-	Layers:
	-	`sha256:a7f0c74374451005259fe6b1b7ef3185055f2b6c419b5ba0ae8e4f55b1e1c31d`  
		Last Modified: Fri, 10 Apr 2026 09:34:45 GMT  
		Size: 31.0 MB (30965327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59c00ed68c0deac84fc02e3dccd68f9b3efc658291d07dc8acc15381618a993`  
		Last Modified: Thu, 16 Apr 2026 17:14:12 GMT  
		Size: 13.8 MB (13849642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494961261766df20fa128cd32f5a03dc9a4e4159c45011018b6fa033ab7806a4`  
		Last Modified: Thu, 16 Apr 2026 17:14:23 GMT  
		Size: 90.9 MB (90910216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19682376bf9d3ed5e5a640faaeb58f115949c155581e720e0b6872728dd1c28`  
		Last Modified: Thu, 16 Apr 2026 17:14:08 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ca163079226955d05d4b409b25aa680547cf52acee3840edfb5ec5e7535446`  
		Last Modified: Wed, 29 Apr 2026 00:04:35 GMT  
		Size: 93.0 MB (93008236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8432b77f8b3e12bdb672c3cff6b71a7f098132a2f9f9c39ea01d8bc075203a4`  
		Last Modified: Wed, 29 Apr 2026 00:03:57 GMT  
		Size: 151.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af83bce2788c01cd315191e4288b84d8d925a5f8070f46396ed887b45e8553e5`  
		Last Modified: Wed, 29 Apr 2026 00:03:57 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780ce7102736c9c5bac1b7b23c7f802e9703791b9ed098682f41c18f514f9570`  
		Last Modified: Wed, 29 Apr 2026 00:04:30 GMT  
		Size: 75.1 MB (75120088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50d168d89a49c61bb11953857beea9c283493c44661c0248154f2dafa46356b`  
		Last Modified: Wed, 29 Apr 2026 00:04:42 GMT  
		Size: 140.2 MB (140235941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e512e662fd2a5f7003673215625bd1f8de99c66ea9c84900c09e7889b3ae14`  
		Last Modified: Wed, 29 Apr 2026 00:04:00 GMT  
		Size: 383.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-lts-and-current-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:f5aac307df77b223f425e2473babbb4025e7621ae3211a382024938f54b7810b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7505835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d883501b8cc8308be32d8b870e48e4c2584fab88176b31dd3dad308900346f2`

```dockerfile
```

-	Layers:
	-	`sha256:483dd3525914d937c6361bee375bca78e3acd393b89e23b3ead923e9e6c83738`  
		Last Modified: Wed, 29 Apr 2026 00:04:00 GMT  
		Size: 7.5 MB (7469538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa8f21a2e4a150f8b6590e8727aad3f8873aa1d42f28c1d5dfe03569313f139d`  
		Last Modified: Wed, 29 Apr 2026 00:03:57 GMT  
		Size: 36.3 KB (36297 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk-lts-and-current-noble` - linux; s390x

```console
$ docker pull gradle@sha256:8e5339471516a79ae7bd7f242614e8cb8154c9ea54215d014a145ced9c30ee13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.2 MB (434237881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b09ffb9b00854a10f4b7b8669560821d55f030c224bf46d6170617a08910d1b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 10 Apr 2026 06:50:27 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:50:29 GMT
ADD file:41defd98c44eed6fc946fd94496a94164879f2ad4f63d66a5c1e213cc2259ad1 in / 
# Fri, 10 Apr 2026 06:50:29 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:46:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:46:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:46:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:46:45 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:46:45 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Wed, 15 Apr 2026 20:47:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='987387933b64b9833846dee373b640440d3e1fd48a04804ec01a6dbf718e8ab8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='a9d73e711d967dc44896d4f430f73a68fd33590dabc29a7f2fb9f593425b854c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='b262b735b215173003766da36588d5f717dceada0286db41b439f93fb2ada468';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        riscv64)          ESUM='168119e4fba350f4e6b3ca92450a2b90a8502b89a235a04415e9adf9f5d3164e';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_riscv64_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='15e5cbcadcf3d43623c31b825063cdc2817b9f1ba840b51dc6ef70e5d33c84e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:47:02 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:47:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:47:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 20:47:03 GMT
CMD ["jshell"]
# Tue, 28 Apr 2026 23:29:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk26 # buildkit
# Tue, 28 Apr 2026 23:29:28 GMT
RUN set -o errexit -o nounset     && ln --symbolic /opt/java/openjdk /opt/java/openjdk25 # buildkit
# Tue, 28 Apr 2026 23:29:28 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk25
# Tue, 28 Apr 2026 23:29:28 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk26
# Tue, 28 Apr 2026 23:29:28 GMT
CMD ["gradle"]
# Tue, 28 Apr 2026 23:29:28 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 28 Apr 2026 23:29:28 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Tue, 28 Apr 2026 23:29:28 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 28 Apr 2026 23:29:28 GMT
WORKDIR /home/gradle
# Tue, 28 Apr 2026 23:29:42 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make         curl         wget         tar                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 28 Apr 2026 23:29:42 GMT
ENV GRADLE_VERSION=9.5.0
# Tue, 28 Apr 2026 23:29:42 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Tue, 28 Apr 2026 23:29:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 28 Apr 2026 23:29:46 GMT
USER gradle
# Tue, 28 Apr 2026 23:29:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 28 Apr 2026 23:29:47 GMT
USER root
```

-	Layers:
	-	`sha256:ef1c26d09a5f9962879f732e212c4246a41e8473f6120efb435886357c85dd5a`  
		Last Modified: Fri, 10 Apr 2026 09:34:53 GMT  
		Size: 29.9 MB (29912147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92fdffb4b8be9329fc8e55398dbf1e46076dfc2dbfd017d977bf741df531d683`  
		Last Modified: Wed, 15 Apr 2026 20:47:28 GMT  
		Size: 16.3 MB (16310154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621f771242c7d42a5cdde1fe6dc16d1d1e571a73faea0ce558aaa3d8b92c0ebe`  
		Last Modified: Wed, 15 Apr 2026 20:47:30 GMT  
		Size: 88.4 MB (88369931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323c1c373ca7689cbc16b36f6d476bf6b21084f479f754e135d108bba362a86d`  
		Last Modified: Wed, 15 Apr 2026 20:47:28 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec60b6250e48742481e026cc91776ba36f733d15606478959e382050ff5f1b0`  
		Last Modified: Tue, 28 Apr 2026 23:30:22 GMT  
		Size: 90.5 MB (90547712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9aa52dcd236e31901a5502f46d2dbe5f22872953bd08e5de1091325b634c80`  
		Last Modified: Tue, 28 Apr 2026 23:30:19 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc64549b3273102130050e67a421a857023f8bee5dd7ae97c24fec927f304b3`  
		Last Modified: Tue, 28 Apr 2026 23:30:19 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5721d1f1e116c5b5c572baca104b691ff8103aae2ef94cc6bd0784abd5dc56d`  
		Last Modified: Tue, 28 Apr 2026 23:30:21 GMT  
		Size: 68.9 MB (68857712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0258fd1654c0c652e7a1d7b9f3b9beea7b168a6ce29285416c50fe92006de2`  
		Last Modified: Tue, 28 Apr 2026 23:30:23 GMT  
		Size: 140.2 MB (140235936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1134403ed025ce8ca325b9d1959685ebfafef74231a0b48a9e773314b8b92769`  
		Last Modified: Tue, 28 Apr 2026 23:30:20 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-lts-and-current-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:43924d259a776ef8d0d1bb46a76bf0d9f091ff3de7749d2abbc04024792552bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7349113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb2dd59c39401918da8a5c77cec98c4d69777c13d990ebf13f024579df862e44`

```dockerfile
```

-	Layers:
	-	`sha256:4d2127b1bf2726a6411526b7a75850d0b6e83ff50185b86d4366460403fba8d4`  
		Last Modified: Tue, 28 Apr 2026 23:30:19 GMT  
		Size: 7.3 MB (7312950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebc3d785f993055f23c5dd27374a2a141f932bf62081063039a73e6b2d817926`  
		Last Modified: Tue, 28 Apr 2026 23:30:19 GMT  
		Size: 36.2 KB (36163 bytes)  
		MIME: application/vnd.in-toto+json
