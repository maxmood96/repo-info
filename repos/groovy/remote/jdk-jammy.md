## `groovy:jdk-jammy`

```console
$ docker pull groovy@sha256:1c66a031a89ce50bf33bf953f5d36d45fbfb5f74e11d3abc2d9af90b67f29046
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

### `groovy:jdk-jammy` - linux; amd64

```console
$ docker pull groovy@sha256:0ae78f6fe1cc26fb354a09a3112c1017b80c3cf953d801e33a41ae82a4841597
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.4 MB (226395767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a63f54b5c54962c5491a8c7812d7c81e45e2d1934a477fb74a3b20eb31b9f44`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Sun, 30 Jun 2024 17:46:17 GMT
ARG RELEASE
# Sun, 30 Jun 2024 17:46:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 30 Jun 2024 17:46:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 30 Jun 2024 17:46:17 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 30 Jun 2024 17:46:17 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Sun, 30 Jun 2024 17:46:17 GMT
CMD ["/bin/bash"]
# Sun, 30 Jun 2024 17:46:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 30 Jun 2024 17:46:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 30 Jun 2024 17:46:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 30 Jun 2024 17:46:17 GMT
CMD ["jshell"]
# Sun, 30 Jun 2024 17:46:17 GMT
CMD ["groovysh"]
# Sun, 30 Jun 2024 17:46:17 GMT
ENV GROOVY_HOME=/opt/groovy
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Sun, 30 Jun 2024 17:46:17 GMT
WORKDIR /home/groovy
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
ENV GROOVY_VERSION=4.0.22
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
USER 1000:1000
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:762bedf4b1b784c3de6c5022c5307d63123d3b7cdd59211317e37e9d477deaa0`  
		Last Modified: Fri, 09 Aug 2024 01:22:05 GMT  
		Size: 30.4 MB (30440714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d2822c71e1c49e3b52ca63c8ad15833449ee66e6c398a302eb046c556826e0`  
		Last Modified: Sat, 17 Aug 2024 01:12:37 GMT  
		Size: 17.4 MB (17415429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df78e45a4823d233088ec6cd712ed594c80f424c18e6459122bdb252ed130119`  
		Last Modified: Sat, 17 Aug 2024 01:12:45 GMT  
		Size: 145.2 MB (145177168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bb97986468c82fd074135d909c3d21add2e80b83458fc4c73c3b77824519d2`  
		Last Modified: Sat, 17 Aug 2024 01:12:34 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e931d838d2e474afb231e2950ac78bca102cc55e3e52436a5f77c0886f35ab9`  
		Last Modified: Fri, 23 Aug 2024 19:27:01 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7941be0a85cd6d0bd3a1f9ce95c5e2f0eecc3416b24af1be0ea27197f9c30173`  
		Last Modified: Fri, 23 Aug 2024 20:02:52 GMT  
		Size: 4.3 KB (4330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039aa3fef62ae3bed93e10608a63e0ca31647b1467b68a9436251e80849754f7`  
		Last Modified: Fri, 23 Aug 2024 20:02:52 GMT  
		Size: 3.5 MB (3503726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36511aef1068098e56913b25ba09a05faaa95944d1757cee7858e1c5590a18c8`  
		Last Modified: Fri, 23 Aug 2024 20:02:52 GMT  
		Size: 29.9 MB (29851948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba4a85690b7c5c12883b0e41b1910adfbf6d0e9878dac90f637889f87c17aa7`  
		Last Modified: Fri, 23 Aug 2024 20:02:52 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk-jammy` - unknown; unknown

```console
$ docker pull groovy@sha256:1b6a1502bae5cc8f4068fe2ed8658db121c4c5cf7215095055eedf5cb3bb4fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3897908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d928cf81f5b8a9c660dd8cb264b65197a9d98b2b7574394615ac956b948383d2`

```dockerfile
```

-	Layers:
	-	`sha256:59dba75ab4b65f6cc7a61bb120c86afd7d19debc7a0b5640fa866ee4a7618b7a`  
		Last Modified: Fri, 23 Aug 2024 20:02:52 GMT  
		Size: 3.9 MB (3868100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f88be9172c6895fd88d8a12fa1cbd3246b25214a976301f3979202a2fa94984c`  
		Last Modified: Fri, 23 Aug 2024 20:02:52 GMT  
		Size: 29.8 KB (29808 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:jdk-jammy` - linux; arm variant v7

```console
$ docker pull groovy@sha256:f22dc99050e669d1a4f9547a914090aebc1e3771da3de5d83e9aa7e63fbf95f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.2 MB (221247412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b429a00be54cb058d735905b35032736d65589ea2c6a0162d9ed4e33eac69a29`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Sun, 30 Jun 2024 17:46:17 GMT
ARG RELEASE
# Sun, 30 Jun 2024 17:46:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 30 Jun 2024 17:46:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 30 Jun 2024 17:46:17 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 30 Jun 2024 17:46:17 GMT
ADD file:ef971273c60fcf0d0b0a4e71a5e5421060cd7c316f1d9af068a193c23dc81d31 in / 
# Sun, 30 Jun 2024 17:46:17 GMT
CMD ["/bin/bash"]
# Sun, 30 Jun 2024 17:46:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 30 Jun 2024 17:46:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 30 Jun 2024 17:46:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 30 Jun 2024 17:46:17 GMT
CMD ["jshell"]
# Sun, 30 Jun 2024 17:46:17 GMT
CMD ["groovysh"]
# Sun, 30 Jun 2024 17:46:17 GMT
ENV GROOVY_HOME=/opt/groovy
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Sun, 30 Jun 2024 17:46:17 GMT
WORKDIR /home/groovy
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
ENV GROOVY_VERSION=4.0.22
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
USER 1000:1000
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:f2a599e193acb4c0e6567f9f5e0b191f59e170d5062a49d73761ee20623e6788`  
		Last Modified: Fri, 09 Aug 2024 02:12:36 GMT  
		Size: 27.5 MB (27535050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff66fc029b6f8bf50d1f45a1d3c46a35f7283ef6380b744f45979482bc8bcc6e`  
		Last Modified: Sat, 17 Aug 2024 01:38:32 GMT  
		Size: 17.6 MB (17566676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61e3aadb99e5b45ff83ab2891aeeadf95b833d2341f254de2c9217f64b6a576`  
		Last Modified: Sat, 17 Aug 2024 01:38:42 GMT  
		Size: 142.6 MB (142643911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bee8596b18afa899f01be0d7354c343c9d91c94896e086e8cd0ae8866bda30`  
		Last Modified: Sat, 17 Aug 2024 01:38:29 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94cd8fb4a99bea3664ffe3078f895ead49cbe7a48b68a89b55f93cab111f7bb9`  
		Last Modified: Fri, 23 Aug 2024 19:00:22 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a053dd185f2128cc8af9520f03ad279339af9d0d5867a80115921662ba8286bc`  
		Last Modified: Fri, 23 Aug 2024 20:30:50 GMT  
		Size: 4.3 KB (4320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b76182aa7e45eeb186cba5a1907f585914a6c5ad2ff7134caced393b616328`  
		Last Modified: Fri, 23 Aug 2024 20:30:51 GMT  
		Size: 3.6 MB (3643011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb04b20e48c08fd55cc188cc8017f7a0ed13495dd307ab76be816dd2ecb17fc`  
		Last Modified: Fri, 23 Aug 2024 20:30:52 GMT  
		Size: 29.9 MB (29851991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50e9e06dddaa585c297c0df632aba1b90d3d2e4e793d40afdfb8fb1f37e1ab4`  
		Last Modified: Fri, 23 Aug 2024 20:30:50 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk-jammy` - unknown; unknown

```console
$ docker pull groovy@sha256:4ed1fec80859f6785b8f72f6551f14c99815756c8ae019c152117d3d3102b831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3818260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c26412ca3c1f2b00340916b1797becd2b9380274eb6283a8ff4c17c9cf52c71`

```dockerfile
```

-	Layers:
	-	`sha256:854f444ac3e4e3b0ac2de9562c74599c3daa5045a1982ad27cfee73354b05e52`  
		Last Modified: Fri, 23 Aug 2024 20:30:51 GMT  
		Size: 3.8 MB (3788215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:214c52a5f766586a0c415cb181de3b2d672c0accafa3a19c270b4a9a0932ed75`  
		Last Modified: Fri, 23 Aug 2024 20:30:50 GMT  
		Size: 30.0 KB (30045 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:jdk-jammy` - linux; arm64 variant v8

```console
$ docker pull groovy@sha256:aadeb71ca3fe33530154ca7c00ba6fce599093c24a32fe37fd2d18567fa8da37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.5 MB (224523604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e3569356802c83d2e7877a9afd74eba65ef09e6ea9af7e96df503111b625642`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Sun, 30 Jun 2024 17:46:17 GMT
ARG RELEASE
# Sun, 30 Jun 2024 17:46:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 30 Jun 2024 17:46:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 30 Jun 2024 17:46:17 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 30 Jun 2024 17:46:17 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Sun, 30 Jun 2024 17:46:17 GMT
CMD ["/bin/bash"]
# Sun, 30 Jun 2024 17:46:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 30 Jun 2024 17:46:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 30 Jun 2024 17:46:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 30 Jun 2024 17:46:17 GMT
CMD ["jshell"]
# Sun, 30 Jun 2024 17:46:17 GMT
CMD ["groovysh"]
# Sun, 30 Jun 2024 17:46:17 GMT
ENV GROOVY_HOME=/opt/groovy
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Sun, 30 Jun 2024 17:46:17 GMT
WORKDIR /home/groovy
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
ENV GROOVY_VERSION=4.0.22
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
USER 1000:1000
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:f99601f39010ba98f3cb03ebfcc356cf14d93d5f585f680a3651901dce700f45`  
		Last Modified: Fri, 09 Aug 2024 02:12:50 GMT  
		Size: 28.4 MB (28397110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19a41cbd65bedaea8ec6506f879288194980af2b58962cdbb7a3f74472ba89d1`  
		Last Modified: Sat, 17 Aug 2024 01:35:29 GMT  
		Size: 18.8 MB (18828020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f15f4e96b72848492ea70c24924c663daaabc66056b4c79e20c49bcaa0281b`  
		Last Modified: Sat, 17 Aug 2024 01:35:36 GMT  
		Size: 144.0 MB (143967117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db77bfc4ba1ffc9a51529c131b219fd7c8b0cbb0453787159c83766555ef58f`  
		Last Modified: Sat, 17 Aug 2024 01:35:26 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4adffa105451616dea2c4d9cf0d90302d4b6712e88d24a96f440284bd2bed24`  
		Last Modified: Fri, 23 Aug 2024 19:44:36 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813616a23a3cc17a6fa11d34a6497fd703f2dcd0be25bb02b36a8dd3b1538c7d`  
		Last Modified: Fri, 23 Aug 2024 22:43:54 GMT  
		Size: 4.3 KB (4340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273e5c2b736227a87d7475222f5e1c47ac27b88ea363ce301c9920e6d2795de5`  
		Last Modified: Fri, 23 Aug 2024 22:43:55 GMT  
		Size: 3.5 MB (3472602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ba724641eac0e21805bbe1ce6cd4788db7e070823be1e243c4ad661b106058`  
		Last Modified: Fri, 23 Aug 2024 22:43:56 GMT  
		Size: 29.9 MB (29851963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb08f9ecd2ad1429f1bda805b9765ed2af77563a03d088555783bf619b858e00`  
		Last Modified: Fri, 23 Aug 2024 22:43:54 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk-jammy` - unknown; unknown

```console
$ docker pull groovy@sha256:8964b2ed3083fa8340741fece7f3c48c04503be990188fce1e51b2a4361f5886
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3994825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d90baed7944e1da0e10ab8560fa1fa39d35f7a208f29e8106faaa400be42ef`

```dockerfile
```

-	Layers:
	-	`sha256:77c2c842e8e54da704753cb8a339fbbb0af64533a201dfa4cc4dbb1f1efee569`  
		Last Modified: Fri, 23 Aug 2024 22:43:55 GMT  
		Size: 4.0 MB (3964508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df234250fa017e7e1c63646f6b47b695ce1fca118121924bac341d24d2c56da6`  
		Last Modified: Fri, 23 Aug 2024 22:43:54 GMT  
		Size: 30.3 KB (30317 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:jdk-jammy` - linux; ppc64le

```console
$ docker pull groovy@sha256:d024e40a04e344b6e47b5366c0dd528caa4296ecba3593801f96a62b039e6d51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233189657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9af0847175d917b831fb4af8bb381c8ddb62aff218cf27b137c145db82fc54`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Sun, 30 Jun 2024 17:46:17 GMT
ARG RELEASE
# Sun, 30 Jun 2024 17:46:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 30 Jun 2024 17:46:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 30 Jun 2024 17:46:17 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 30 Jun 2024 17:46:17 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Sun, 30 Jun 2024 17:46:17 GMT
CMD ["/bin/bash"]
# Sun, 30 Jun 2024 17:46:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 30 Jun 2024 17:46:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 30 Jun 2024 17:46:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 30 Jun 2024 17:46:17 GMT
CMD ["jshell"]
# Sun, 30 Jun 2024 17:46:17 GMT
CMD ["groovysh"]
# Sun, 30 Jun 2024 17:46:17 GMT
ENV GROOVY_HOME=/opt/groovy
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Sun, 30 Jun 2024 17:46:17 GMT
WORKDIR /home/groovy
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
ENV GROOVY_VERSION=4.0.22
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
USER 1000:1000
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:80c625afbf07d8c6d2718c777f706ddee78a027c79596515653025fb506d8670`  
		Last Modified: Sat, 17 Aug 2024 00:46:53 GMT  
		Size: 35.6 MB (35587644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0693fdc769b35059bf46757710f7d052660918503e58a5fb55e877e19ecee155`  
		Last Modified: Sat, 17 Aug 2024 01:01:59 GMT  
		Size: 18.7 MB (18677262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc7958a546eccffac8f590c1a80d8ab8afaaddb533401a9225d360d4c830813`  
		Last Modified: Sat, 17 Aug 2024 01:02:10 GMT  
		Size: 144.9 MB (144862961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa478c61eda2baedae493052ff4a84316a19a1c8bb23fdae75733a80297a162`  
		Last Modified: Sat, 17 Aug 2024 01:01:54 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8843b5b94c772d8f22dc0486fb135cce9a4e4047a21085f59110b7f5332630c8`  
		Last Modified: Fri, 23 Aug 2024 19:23:44 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f223ccf0fc390babd7000a39a0c645bd3dce3fa92b5d0639c29f67bb1473d9e`  
		Last Modified: Fri, 23 Aug 2024 20:42:50 GMT  
		Size: 4.3 KB (4329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1768a10de2e483fa992f67e4071dc5a9f08b0a5709b3b111a9729690b43d0ec2`  
		Last Modified: Fri, 23 Aug 2024 20:42:50 GMT  
		Size: 4.2 MB (4203045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca74978a1035ca28887adc030fd534b972942dea9616e58bb63079ffafe113d`  
		Last Modified: Fri, 23 Aug 2024 20:42:51 GMT  
		Size: 29.9 MB (29851961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0855792baf4b440087e2f749e99973d5786b86453081cef2c6b2c1bb58e1add4`  
		Last Modified: Fri, 23 Aug 2024 20:42:50 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk-jammy` - unknown; unknown

```console
$ docker pull groovy@sha256:64ac55f815f40f4718f4490cee9d1ce4df145952c42ad8dbace519009668fbc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3928102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9c3095f82fdfffe0d3562c855f2a3bd09a9ad44082eaa6acfc995199c8871c`

```dockerfile
```

-	Layers:
	-	`sha256:9b198a7d099eba29a8736c73b9ffeb919036a552afaccf179ed1b27f1041b92b`  
		Last Modified: Fri, 23 Aug 2024 20:42:50 GMT  
		Size: 3.9 MB (3898155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51a960878a40dfd8231737ee6b1a71c6d98170fb476094de0eb43f8280906f45`  
		Last Modified: Fri, 23 Aug 2024 20:42:50 GMT  
		Size: 29.9 KB (29947 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:jdk-jammy` - linux; s390x

```console
$ docker pull groovy@sha256:a76ceebcec8cdefca486b52cdf7568255f23c529988b0a8170447642402abc79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.5 MB (213546437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8befee982d032d7fde42046554ff65b3aff3cb9cd5952cdeba84f5a325277dd`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Sun, 30 Jun 2024 17:46:17 GMT
ARG RELEASE
# Sun, 30 Jun 2024 17:46:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 30 Jun 2024 17:46:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 30 Jun 2024 17:46:17 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 30 Jun 2024 17:46:17 GMT
ADD file:560440017e541c07ad2788f24ed9fd81ef2e2966bd15d8bdd9726934a79c5242 in / 
# Sun, 30 Jun 2024 17:46:17 GMT
CMD ["/bin/bash"]
# Sun, 30 Jun 2024 17:46:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 30 Jun 2024 17:46:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 30 Jun 2024 17:46:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 30 Jun 2024 17:46:17 GMT
CMD ["jshell"]
# Sun, 30 Jun 2024 17:46:17 GMT
CMD ["groovysh"]
# Sun, 30 Jun 2024 17:46:17 GMT
ENV GROOVY_HOME=/opt/groovy
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Sun, 30 Jun 2024 17:46:17 GMT
WORKDIR /home/groovy
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
ENV GROOVY_VERSION=4.0.22
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
USER 1000:1000
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:9a6ca8a36259241f44c15c84a37ed8ab040ccfe0f554bcfa04c618e1afbe5c0b`  
		Last Modified: Sat, 17 Aug 2024 01:32:21 GMT  
		Size: 28.6 MB (28638503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a4353a8eb4f285ecb7c45d930598defa46de85e4d28e5771f4f8c7a0fa8740`  
		Last Modified: Sat, 17 Aug 2024 01:33:24 GMT  
		Size: 17.2 MB (17229109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283379d6e95b5ccbfca83e42f61928b8d764e99730fcb0f34c412f734c6c0cfe`  
		Last Modified: Sat, 17 Aug 2024 01:33:32 GMT  
		Size: 134.4 MB (134407920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c672b651946102611784b8a3aadd925df7ce1b1207aac153c80db72c2bb9308`  
		Last Modified: Sat, 17 Aug 2024 01:33:21 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ba57a48c18623b72489d99e2581d0739d60702caee3c58c7c5d421c9a28093`  
		Last Modified: Fri, 23 Aug 2024 19:47:24 GMT  
		Size: 2.1 KB (2106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e83688ad4e70424b9b42e469042b970d58888c4b6a8db3a5410caab414e5ac`  
		Last Modified: Sat, 24 Aug 2024 00:10:30 GMT  
		Size: 4.3 KB (4332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f285d6eecf527bd235c56fa44ed89d01b2deb225a3d3073c41fd33754d1d1c`  
		Last Modified: Sat, 24 Aug 2024 00:10:31 GMT  
		Size: 3.4 MB (3412162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e85ee12ddd567e88346c517e3ce17acf4882bce0491da0b11a310c39df188ec`  
		Last Modified: Sat, 24 Aug 2024 00:10:31 GMT  
		Size: 29.9 MB (29851961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc8f435bb6c79ad6a306831da822c04f693ab1cb4d9bfcf402430a4cfc5eccf`  
		Last Modified: Sat, 24 Aug 2024 00:10:30 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk-jammy` - unknown; unknown

```console
$ docker pull groovy@sha256:a87cd302ac8f1f75eada3e22056b0df74f678a271523483cf4ac5d7dc41dc5d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3826740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf3ad4840dfe3d6d4217e549c6754b929a61591c51b2f77571294570f0817b7`

```dockerfile
```

-	Layers:
	-	`sha256:59b240233f27b7ae4fbcf543cf3faad524bddae19fc3578f232deeabc5448ffa`  
		Last Modified: Sat, 24 Aug 2024 00:10:30 GMT  
		Size: 3.8 MB (3796932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac0d394fea2616dd946105266c28b80faa448481c40ff1c459c4fe50b8aaa27f`  
		Last Modified: Sat, 24 Aug 2024 00:10:30 GMT  
		Size: 29.8 KB (29808 bytes)  
		MIME: application/vnd.in-toto+json
