## `gradle:jdk-21-and-22-jammy`

```console
$ docker pull gradle@sha256:f42a42d8cb758dad9559139a1375c5551f02ade0a8e88019f761dcd6f7feba22
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk-21-and-22-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:cc4b4392c937f26aae2a162fde3eb2408018ef3f622af8626afe2a6667eb598c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **548.9 MB (548937802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06c2f37e20b7d42a9e66adffbc41b46ad91c85453a1d8d1539f1efdaa80e0f3f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:35 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:37 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Sat, 27 Apr 2024 13:18:37 GMT
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
# Mon, 20 May 2024 22:05:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk22 # buildkit
# Mon, 20 May 2024 22:05:06 GMT
RUN set -o errexit -o nounset     && ln --symbolic /opt/java/openjdk /opt/java/openjdk21 # buildkit
# Mon, 20 May 2024 22:05:06 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk21
# Mon, 20 May 2024 22:05:06 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk22
# Mon, 20 May 2024 22:05:06 GMT
CMD ["gradle"]
# Mon, 20 May 2024 22:05:06 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 20 May 2024 22:05:06 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Mon, 20 May 2024 22:05:06 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 20 May 2024 22:05:06 GMT
WORKDIR /home/gradle
# Mon, 20 May 2024 22:05:06 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 20 May 2024 22:05:06 GMT
ENV GRADLE_VERSION=8.7
# Mon, 20 May 2024 22:05:06 GMT
ARG GRADLE_DOWNLOAD_SHA256=544c35d6bd849ae8a5ed0bcea39ba677dc40f49df7d1835561582da2009b961d
# Mon, 20 May 2024 22:05:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=544c35d6bd849ae8a5ed0bcea39ba677dc40f49df7d1835561582da2009b961d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:4a023cab5400feb5c1ab725beb8345ddb0e3200314004b56677a5eee2e8c86cf`  
		Last Modified: Sat, 27 Apr 2024 20:07:18 GMT  
		Size: 30.4 MB (30439649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5d1bccc5440d3a24f4a620704b9e687b4163c6c872fcc8e812e200c9bbac58`  
		Last Modified: Thu, 02 May 2024 01:18:08 GMT  
		Size: 17.5 MB (17456240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd7ada947ce7661ad85815ab478851ccf7b0d064cde9c9195bafb2bd499b29e`  
		Last Modified: Thu, 02 May 2024 01:19:17 GMT  
		Size: 158.5 MB (158512068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478e5694bb3e0cbd54a331514092737b8a8de5a4fe7069a3f00e6eb1b98fd605`  
		Last Modified: Thu, 02 May 2024 01:19:05 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fa38685928ae1a460299486cb01d7d2db1eff47fbd68c8ac6c936e89af1641`  
		Last Modified: Thu, 02 May 2024 01:19:05 GMT  
		Size: 731.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7919da9e35224232cd4be0182d4cc1a54243e3509d8a29b0aa5e10d6e7ce0ed`  
		Last Modified: Tue, 21 May 2024 23:52:36 GMT  
		Size: 156.7 MB (156715800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2beda9702eb5ab1e2d987c711ed6aaa9cccca8d6e6812846e71a475f4979d449`  
		Last Modified: Tue, 21 May 2024 23:52:34 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6704f99834923b1fbeb9469fb6877852d0db3fa4ce7ded8bb094d66f0aa23c13`  
		Last Modified: Tue, 21 May 2024 23:52:34 GMT  
		Size: 4.4 KB (4420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ec528237a25b2c3625813db3b530515662c65b77690bd5fa99d6983ebc1ceb`  
		Last Modified: Tue, 21 May 2024 23:52:35 GMT  
		Size: 51.5 MB (51545200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678426a570c2a7b301550c29e62317b1c62631151e90c9ab8440fdcbb3b1c871`  
		Last Modified: Tue, 21 May 2024 23:52:36 GMT  
		Size: 134.3 MB (134263331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-21-and-22-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:d9289c4d0219cc07180e4bc60bbfb7226cf0e74fc8a06821b525b27095594ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7167444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d937e32a1092fb575b04d088fe0df37bcdb561f344fbd863535326394ea95d0d`

```dockerfile
```

-	Layers:
	-	`sha256:e6a0438a6e5be94bad8ce4a4df25db9e2231b28f45af6bed64f9b8869fe7304e`  
		Last Modified: Tue, 21 May 2024 23:52:34 GMT  
		Size: 7.1 MB (7134711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3427455a8a6ea1835ab6b9435b6943b35655e65213c788a3e938f8c0b9f1e85`  
		Last Modified: Tue, 21 May 2024 23:52:34 GMT  
		Size: 32.7 KB (32733 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-21-and-22-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:59feab08a3e234217a035cf82b1da6503c7da3b4e3d15dd01811ada9ab86272f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.1 MB (544062377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0b18f0f2e0a693164331f8078a894d242310dd7f0b95469f8fd6da086e55e3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
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
# Mon, 20 May 2024 22:05:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk22 # buildkit
# Mon, 20 May 2024 22:05:06 GMT
RUN set -o errexit -o nounset     && ln --symbolic /opt/java/openjdk /opt/java/openjdk21 # buildkit
# Mon, 20 May 2024 22:05:06 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk21
# Mon, 20 May 2024 22:05:06 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk22
# Mon, 20 May 2024 22:05:06 GMT
CMD ["gradle"]
# Mon, 20 May 2024 22:05:06 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 20 May 2024 22:05:06 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Mon, 20 May 2024 22:05:06 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 20 May 2024 22:05:06 GMT
WORKDIR /home/gradle
# Mon, 20 May 2024 22:05:06 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 20 May 2024 22:05:06 GMT
ENV GRADLE_VERSION=8.7
# Mon, 20 May 2024 22:05:06 GMT
ARG GRADLE_DOWNLOAD_SHA256=544c35d6bd849ae8a5ed0bcea39ba677dc40f49df7d1835561582da2009b961d
# Mon, 20 May 2024 22:05:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=544c35d6bd849ae8a5ed0bcea39ba677dc40f49df7d1835561582da2009b961d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8868eeb30ae6b43fdd3ec11d565b77e83f6c78c86d892957cf1cecb5cc59c9`  
		Last Modified: Thu, 02 May 2024 04:19:45 GMT  
		Size: 18.9 MB (18858238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c4fbd4e9d83ad90ce0ad2f1020e353b63183850d87d2df6bab21ba49e65781`  
		Last Modified: Thu, 02 May 2024 04:20:47 GMT  
		Size: 156.7 MB (156672781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06264556304042e648d17bebdd6326344ccb5c81617ccd6f52ed861a3565cf5a`  
		Last Modified: Thu, 02 May 2024 04:20:37 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0053e5818a6e8d1a15a06441ce5ffc605eb87138e57ddf2a25dcfb6a423afe23`  
		Last Modified: Thu, 02 May 2024 04:20:37 GMT  
		Size: 731.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01feb2199f015b8f69d3368ea0c88e18da401cb82eec1961f847c34df908cbb9`  
		Last Modified: Wed, 22 May 2024 01:45:25 GMT  
		Size: 154.7 MB (154738427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd99a6dca386e3a0308f7d7eb83c5d5ed42e2f938c8879b8a920455082c8b19`  
		Last Modified: Wed, 22 May 2024 01:45:21 GMT  
		Size: 151.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b885a8ce62d471e491460f05c6b863f9231e72ead0915c3f07368afe10635a1f`  
		Last Modified: Wed, 22 May 2024 01:45:21 GMT  
		Size: 4.4 KB (4425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d261734e7dd0e080bf0289cb75da5a1f428879233a3ef3c014076bfca454fcaf`  
		Last Modified: Wed, 22 May 2024 01:45:23 GMT  
		Size: 51.1 MB (51115511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a391c9f3b1ec51233538a94b740ee841ca712f8e82bd6f60d8dc46aad42f415`  
		Last Modified: Wed, 22 May 2024 01:45:25 GMT  
		Size: 134.3 MB (134270725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-21-and-22-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:59f4647a971b965314527ca66907e95240becc11e3ae3c023080fe46d55ec21e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7269072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8d137576f551c93561e86e8066c4de8c5aa7611955a9057eb4510da2ce13203`

```dockerfile
```

-	Layers:
	-	`sha256:969cfbd184a1af23dba0a75325f486377128f60c81dacec8631227fea3f7cf07`  
		Last Modified: Wed, 22 May 2024 01:45:21 GMT  
		Size: 7.2 MB (7237123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:635d28995ad18740120f436d34cf7b0597f6fc8e542fe9e1ef76aae0617aea7b`  
		Last Modified: Wed, 22 May 2024 01:45:20 GMT  
		Size: 31.9 KB (31949 bytes)  
		MIME: application/vnd.in-toto+json
