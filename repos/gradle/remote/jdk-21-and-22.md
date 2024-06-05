## `gradle:jdk-21-and-22`

```console
$ docker pull gradle@sha256:0ddfdec8ec84c266d69f37a961bedcbf95548469f1bbb19cb929c7dce7578902
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk-21-and-22` - linux; amd64

```console
$ docker pull gradle@sha256:807eb9abbacfade5757d01f2b3153a1e59939a9a85d79c5f78cffb3287b7a604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **552.8 MB (552808221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8404d5a6ab089ced5789c3aebd583bd2de4620a9ddd36276a73873c062a9cbf`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7d3ab0e8eba95bd682cfda8041c6cb6fa21e09d0d9131316fd7c96c78969de31';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.3_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fffa52c22d797b715a962e6c8d11ec7d79b90dd819b5bc51d62137ea4b22a340';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.3_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9a1079d7f0fc72951fdc9a0029e49a15f6ba114683aee626f882ee2c761f1d57';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.3_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f57a078d417614e5d78c07c77a6d8a04701058cf692c8e2868d593582be92768';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Tue, 04 Jun 2024 20:56:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk22 # buildkit
# Tue, 04 Jun 2024 20:56:32 GMT
RUN set -o errexit -o nounset     && ln --symbolic /opt/java/openjdk /opt/java/openjdk21 # buildkit
# Tue, 04 Jun 2024 20:56:32 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk21
# Tue, 04 Jun 2024 20:56:32 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk22
# Tue, 04 Jun 2024 20:56:32 GMT
CMD ["gradle"]
# Tue, 04 Jun 2024 20:56:32 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 04 Jun 2024 20:56:32 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Tue, 04 Jun 2024 20:56:32 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 04 Jun 2024 20:56:32 GMT
WORKDIR /home/gradle
# Tue, 04 Jun 2024 20:56:32 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 04 Jun 2024 20:56:32 GMT
ENV GRADLE_VERSION=8.8
# Tue, 04 Jun 2024 20:56:32 GMT
ARG GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
# Tue, 04 Jun 2024 20:56:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c930bd25dd53355206fb22462e8fbde127b1d43483ca67962d2bf2bb4a534c0`  
		Last Modified: Wed, 05 Jun 2024 05:00:37 GMT  
		Size: 17.5 MB (17456370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae78fb28ee8ad64497b830c9c46950ab9448341cbdb14f4710d143671487c61`  
		Last Modified: Wed, 05 Jun 2024 05:01:45 GMT  
		Size: 158.5 MB (158511802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2b2709c988772d4f722fa842b200b424f5873a64a9b4c5cfaeb86a6293a3b1`  
		Last Modified: Wed, 05 Jun 2024 05:01:33 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e071b974f417bebf03dcba8690670bce9d7d83d647b1775d42f720b2813da09d`  
		Last Modified: Wed, 05 Jun 2024 05:01:33 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9a15a04e4bd8a42f2d9e5f74023856a81143502e7c6fa291dcf93711cc2be9`  
		Last Modified: Wed, 05 Jun 2024 17:06:14 GMT  
		Size: 156.7 MB (156715797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2122872be42c5a3bf7d7b6bd2f56c683c740663dced25400775eed39b2d40c`  
		Last Modified: Wed, 05 Jun 2024 17:06:12 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bede4d092b917e1312c7e130be7e74a9d2b8c911b3de0e3dccc3c3c089b76e8`  
		Last Modified: Wed, 05 Jun 2024 17:06:11 GMT  
		Size: 4.4 KB (4420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06cf645583f2c5895e8bbc0ed5dbe9ac48ac37a972d3011b4090baf1c31d128`  
		Last Modified: Wed, 05 Jun 2024 17:06:13 GMT  
		Size: 51.6 MB (51560802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814eb9fd4e197dc124d51b8702946f77414b2eb2f4ff362ebe6cc65284d36871`  
		Last Modified: Wed, 05 Jun 2024 17:06:15 GMT  
		Size: 138.1 MB (138118652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-21-and-22` - unknown; unknown

```console
$ docker pull gradle@sha256:7b857f14765c1ab1547b3f09a8cbd84802f9a4d5a158a1ba418fb1a116e74ddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7168212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64d34ccdbc7669c5f2997ac590ad7c78870515bf6f1e8a9db492786f60be5a1`

```dockerfile
```

-	Layers:
	-	`sha256:2fcfa50a921e6940f5bc217e98e052c15fd48dcb78a43b57acfd833aa2acf4c0`  
		Last Modified: Wed, 05 Jun 2024 17:06:12 GMT  
		Size: 7.1 MB (7137159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:374a4ba28fda8dc76a91ad414dd7194af86ba5b2c4112812e55acfca5d6b19ce`  
		Last Modified: Wed, 05 Jun 2024 17:06:12 GMT  
		Size: 31.1 KB (31053 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-21-and-22` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:9840ad9e70f2093e2cd2752762b63b09130f1fa897f4131ab3fc2c42f22b00b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.9 MB (547942013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d884d30ab08e33c1612efcb9395f564b9f183742144802988ad3502a487e8a4d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7d3ab0e8eba95bd682cfda8041c6cb6fa21e09d0d9131316fd7c96c78969de31';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.3_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fffa52c22d797b715a962e6c8d11ec7d79b90dd819b5bc51d62137ea4b22a340';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.3_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9a1079d7f0fc72951fdc9a0029e49a15f6ba114683aee626f882ee2c761f1d57';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.3_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f57a078d417614e5d78c07c77a6d8a04701058cf692c8e2868d593582be92768';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Tue, 04 Jun 2024 20:56:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk22 # buildkit
# Tue, 04 Jun 2024 20:56:32 GMT
RUN set -o errexit -o nounset     && ln --symbolic /opt/java/openjdk /opt/java/openjdk21 # buildkit
# Tue, 04 Jun 2024 20:56:32 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk21
# Tue, 04 Jun 2024 20:56:32 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk22
# Tue, 04 Jun 2024 20:56:32 GMT
CMD ["gradle"]
# Tue, 04 Jun 2024 20:56:32 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 04 Jun 2024 20:56:32 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Tue, 04 Jun 2024 20:56:32 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 04 Jun 2024 20:56:32 GMT
WORKDIR /home/gradle
# Tue, 04 Jun 2024 20:56:32 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 04 Jun 2024 20:56:32 GMT
ENV GRADLE_VERSION=8.8
# Tue, 04 Jun 2024 20:56:32 GMT
ARG GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
# Tue, 04 Jun 2024 20:56:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd5d7dbc0eb75f9bc71643e6dcfed8b6cef6295e5c7d5f5ba90aa14f0d9cc6f`  
		Last Modified: Wed, 05 Jun 2024 04:57:07 GMT  
		Size: 18.9 MB (18859083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0a2a7710d9d7d0f88f9f13ede1b7ff2f89343d79308778db178dc4f312ae4a`  
		Last Modified: Wed, 05 Jun 2024 04:58:04 GMT  
		Size: 156.7 MB (156672853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e96aef1e76c15d9c20747e43105bca90537c6bb652ea98bc96ef69728de212`  
		Last Modified: Wed, 05 Jun 2024 04:57:54 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a3dedce6ac6bb05c0e8a5dbdcc1f91df5880b0dd7eb1e077172730f1f2322e`  
		Last Modified: Wed, 05 Jun 2024 04:57:54 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093a3f0cf087f64c80e6d22e5ecf2cf4a9d5bae049d6be04c219003214512e2a`  
		Last Modified: Wed, 05 Jun 2024 15:16:00 GMT  
		Size: 154.7 MB (154738464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec7733dd1a1c8e5c61c60e701e16c5f3c2852a2c0e26649fd11ccb0a6a7a8e2`  
		Last Modified: Wed, 05 Jun 2024 15:15:55 GMT  
		Size: 152.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f9a094ae43dddc366ac9ee49603098248d558059d4b8f97c3fdad855e149f6`  
		Last Modified: Wed, 05 Jun 2024 15:15:55 GMT  
		Size: 4.4 KB (4425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5642f080addeade41f530f1cc3cff25a17f292eb8ccf4dd1dc5e6c0439076e96`  
		Last Modified: Wed, 05 Jun 2024 15:15:57 GMT  
		Size: 51.1 MB (51143119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb09be6dab2e1387de684b2a8c030f8b72d1b3256014b4a21abb96c79acfa27`  
		Last Modified: Wed, 05 Jun 2024 15:16:00 GMT  
		Size: 138.1 MB (138120672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-21-and-22` - unknown; unknown

```console
$ docker pull gradle@sha256:ab9b644290c93b3f59c5f7090beff62ed0a69c09d110165468e3017e4df8e9ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7271436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:228c92badc09b7878bf0971e14f81bc3394a640f79c09041dea18eca822208e7`

```dockerfile
```

-	Layers:
	-	`sha256:08814d83406f5c1e84d30c9d37e5212c66100ba114235a53975cb668ba2d5162`  
		Last Modified: Wed, 05 Jun 2024 18:36:58 GMT  
		Size: 7.2 MB (7239668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a429dbc0d02c823ef1d077483fb676f70090ff36e4400424d7f7b958299fc9af`  
		Last Modified: Wed, 05 Jun 2024 18:36:58 GMT  
		Size: 31.8 KB (31768 bytes)  
		MIME: application/vnd.in-toto+json
