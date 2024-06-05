## `groovy:4-jammy`

```console
$ docker pull groovy@sha256:9359ff1a3cd39d9dd186a5dad7b80c57163874174368721e6606f6bf1d27b648
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

### `groovy:4-jammy` - linux; amd64

```console
$ docker pull groovy@sha256:2ed4a9991524684836a0234f65967665bae42b26ee3cf501d48a4a298adff3aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226316791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1eb6438d99f740ce77e6e61480658d30529305d5af85a501a42a3e944e673cf`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Sun, 17 Mar 2024 02:31:45 GMT
ARG RELEASE
# Sun, 17 Mar 2024 02:31:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 17 Mar 2024 02:31:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 17 Mar 2024 02:31:45 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 17 Mar 2024 02:31:45 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Sun, 17 Mar 2024 02:31:45 GMT
CMD ["/bin/bash"]
# Sun, 17 Mar 2024 02:31:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 17 Mar 2024 02:31:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 17 Mar 2024 02:31:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 17 Mar 2024 02:31:45 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a900acf3ae56b000afc35468a083b6d6fd695abec87a8abdb02743d5c72f6d6d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='aa7fb6bb342319d227a838af5c363bfa1b4a670c209372f9e6585bd79da6220c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='9b5c375ed7ce654083c6c1137d8daadebaf8657650576115f0deafab00d0f1d7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='44bdd662c3b832cfe0b808362866b8d7a700dd60e6e39716dee97211d35c230f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='af3f33c14ed3e2fcd85a390575029fbf92a491f60cfdc274544ac8ad6532de47';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 17 Mar 2024 02:31:45 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 17 Mar 2024 02:31:45 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 17 Mar 2024 02:31:45 GMT
CMD ["jshell"]
# Sun, 17 Mar 2024 02:31:45 GMT
CMD ["groovysh"]
# Sun, 17 Mar 2024 02:31:45 GMT
ENV GROOVY_HOME=/opt/groovy
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Sun, 17 Mar 2024 02:31:45 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Sun, 17 Mar 2024 02:31:45 GMT
WORKDIR /home/groovy
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Sun, 17 Mar 2024 02:31:45 GMT
ENV GROOVY_VERSION=4.0.20
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Sun, 17 Mar 2024 02:31:45 GMT
USER 1000:1000
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
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
	-	`sha256:db39646274eacde3e8c4abd5a34bb608b52c0be1ec92c51c6a57e3e6cc682b9f`  
		Last Modified: Wed, 05 Jun 2024 05:00:45 GMT  
		Size: 145.1 MB (145101545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7948178b4c26a03ca48c677e56865ee5d754d9f7ef612c9e91dc15c239d4dca8`  
		Last Modified: Wed, 05 Jun 2024 05:00:34 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee390ebec53ec7588055b27080fcc66d4244ff2f4b46eb409c0fe768f70b16a`  
		Last Modified: Wed, 05 Jun 2024 05:00:34 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cded1f453949a147173cb5b2135825fe13b70496b297ff8c08d8fc4183d7eede`  
		Last Modified: Wed, 05 Jun 2024 06:12:52 GMT  
		Size: 4.3 KB (4328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5a1d8c1e61ad24476e254d95906c1532e9e90cc86585ad64653069b0fb2763`  
		Last Modified: Wed, 05 Jun 2024 06:12:52 GMT  
		Size: 3.5 MB (3503574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae55279767822f5c95e6bfa77ae783c018ab9a3668cfe8e5b43b543a13561b8`  
		Last Modified: Wed, 05 Jun 2024 06:12:54 GMT  
		Size: 29.8 MB (29810620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7ca45e7abeb361b49bed51c8e2ba22a67af8e5f9b614bd054d8ccff32142a6`  
		Last Modified: Wed, 05 Jun 2024 06:12:52 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:4-jammy` - unknown; unknown

```console
$ docker pull groovy@sha256:c6b85df2a84a7c0814ae07208e64c28f03cae09cc4034ffa81ae90c99cc03843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3858148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:161d84fcbab79742d996e4953289374f77bd8b035734a13e4af3cead513e1867`

```dockerfile
```

-	Layers:
	-	`sha256:8ff9f6e5bc2b9977d4973a178a475d9f6feb71f07274c04a6fada6f70309fb9e`  
		Last Modified: Wed, 05 Jun 2024 06:12:52 GMT  
		Size: 3.8 MB (3828395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:411832bd4e5ac53f8548b4dc4eb1b25b0edef1e2ca4d28923d29558e5973fbf0`  
		Last Modified: Wed, 05 Jun 2024 06:12:52 GMT  
		Size: 29.8 KB (29753 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:4-jammy` - linux; arm variant v7

```console
$ docker pull groovy@sha256:053a543a6a35b349388ca5d8a1376cd650a8bf2a95d2b512e4c5e617e39b2f9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.2 MB (221162499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:822dfcd3391bd796592174113306d6a0ea5bb88c8fa55796184c24b8214fb36e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Sun, 17 Mar 2024 02:31:45 GMT
ARG RELEASE
# Sun, 17 Mar 2024 02:31:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 17 Mar 2024 02:31:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 17 Mar 2024 02:31:45 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 17 Mar 2024 02:31:45 GMT
ADD file:76d606bb5f897ff3ffe149c5d3d049c7ace15da77a61a7df4e558eceebd8d2bd in / 
# Sun, 17 Mar 2024 02:31:45 GMT
CMD ["/bin/bash"]
# Sun, 17 Mar 2024 02:31:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 17 Mar 2024 02:31:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 17 Mar 2024 02:31:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 17 Mar 2024 02:31:45 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a900acf3ae56b000afc35468a083b6d6fd695abec87a8abdb02743d5c72f6d6d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='aa7fb6bb342319d227a838af5c363bfa1b4a670c209372f9e6585bd79da6220c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='9b5c375ed7ce654083c6c1137d8daadebaf8657650576115f0deafab00d0f1d7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='44bdd662c3b832cfe0b808362866b8d7a700dd60e6e39716dee97211d35c230f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='af3f33c14ed3e2fcd85a390575029fbf92a491f60cfdc274544ac8ad6532de47';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 17 Mar 2024 02:31:45 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 17 Mar 2024 02:31:45 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 17 Mar 2024 02:31:45 GMT
CMD ["jshell"]
# Sun, 17 Mar 2024 02:31:45 GMT
CMD ["groovysh"]
# Sun, 17 Mar 2024 02:31:45 GMT
ENV GROOVY_HOME=/opt/groovy
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Sun, 17 Mar 2024 02:31:45 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Sun, 17 Mar 2024 02:31:45 GMT
WORKDIR /home/groovy
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Sun, 17 Mar 2024 02:31:45 GMT
ENV GROOVY_VERSION=4.0.20
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Sun, 17 Mar 2024 02:31:45 GMT
USER 1000:1000
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:bb2b4ba5ac52e5e8a83a1f8dc3c79ed1f5409e3bc349a8c36b2cd4b9d3f6cb23`  
		Last Modified: Tue, 04 Jun 2024 01:38:51 GMT  
		Size: 27.5 MB (27534888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8437ec41aa58662737f55f9b8113ffbf0970e08792586413197c289856ed6a7f`  
		Last Modified: Wed, 05 Jun 2024 04:02:13 GMT  
		Size: 17.6 MB (17589786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febc86426ce602e96ae4f75e9fc39481018a326db48c70308966865f7cdeb60d`  
		Last Modified: Wed, 05 Jun 2024 04:02:23 GMT  
		Size: 142.6 MB (142578037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbdfd9f96c9b22fa29e9eb1146207896d2f3fdb79bebe2e6b8f480007be6f51`  
		Last Modified: Wed, 05 Jun 2024 04:02:10 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95fdbb24f25556c5784811f4921bd9e9b5e655af9e63d60014bcc781454f773f`  
		Last Modified: Wed, 05 Jun 2024 04:02:10 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0d72bc818c4d01cb0b96dbe3a52bdc461f26e277a4f7eef4505e7569b44687`  
		Last Modified: Wed, 05 Jun 2024 07:05:17 GMT  
		Size: 4.3 KB (4316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff2946622b09f1ec7231ba7deaa20dcd6b1dcdc417290eb36d6ae0f21d6092b`  
		Last Modified: Wed, 05 Jun 2024 07:05:18 GMT  
		Size: 3.6 MB (3643761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6cbe8fa9096d1bd44e430ebd7c4260a732475121ff7c44f1e598d50621b2186`  
		Last Modified: Wed, 05 Jun 2024 07:05:19 GMT  
		Size: 29.8 MB (29810631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a66b3cfd9d3540e782858a818efc0b4c4865e942fab315c8099bbcda411e01`  
		Last Modified: Wed, 05 Jun 2024 07:05:18 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:4-jammy` - unknown; unknown

```console
$ docker pull groovy@sha256:13fcc63f66de4cc8ff2e40506c7a170db82774e5ee4a93e086ef770a45125d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3778642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a08ba9953cab77f18399682feda2ab6863dedd5acbd5c50bf07af97c998ee9d6`

```dockerfile
```

-	Layers:
	-	`sha256:19201d6473a44773679bb2d9adc52b841a4696cd909c77902240eb8e7f9ceacf`  
		Last Modified: Wed, 05 Jun 2024 07:05:18 GMT  
		Size: 3.7 MB (3748653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab99159df5ec893bda7fe78d0befce64dba5d6067cb3a4769586dc10074a561a`  
		Last Modified: Wed, 05 Jun 2024 07:05:17 GMT  
		Size: 30.0 KB (29989 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:4-jammy` - linux; arm64 variant v8

```console
$ docker pull groovy@sha256:016520ad4a1db53ebb0bea3c9ed0e5e460835bfae56e7397e8149f9a56330201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.4 MB (224447470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dbf13a3001b8761ec21b38a9625a77aa9e6c0a975e2bac485417447d12cd052`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Sun, 17 Mar 2024 02:31:45 GMT
ARG RELEASE
# Sun, 17 Mar 2024 02:31:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 17 Mar 2024 02:31:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 17 Mar 2024 02:31:45 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 17 Mar 2024 02:31:45 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Sun, 17 Mar 2024 02:31:45 GMT
CMD ["/bin/bash"]
# Sun, 17 Mar 2024 02:31:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 17 Mar 2024 02:31:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 17 Mar 2024 02:31:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 17 Mar 2024 02:31:45 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a900acf3ae56b000afc35468a083b6d6fd695abec87a8abdb02743d5c72f6d6d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='aa7fb6bb342319d227a838af5c363bfa1b4a670c209372f9e6585bd79da6220c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='9b5c375ed7ce654083c6c1137d8daadebaf8657650576115f0deafab00d0f1d7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='44bdd662c3b832cfe0b808362866b8d7a700dd60e6e39716dee97211d35c230f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='af3f33c14ed3e2fcd85a390575029fbf92a491f60cfdc274544ac8ad6532de47';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 17 Mar 2024 02:31:45 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 17 Mar 2024 02:31:45 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 17 Mar 2024 02:31:45 GMT
CMD ["jshell"]
# Sun, 17 Mar 2024 02:31:45 GMT
CMD ["groovysh"]
# Sun, 17 Mar 2024 02:31:45 GMT
ENV GROOVY_HOME=/opt/groovy
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Sun, 17 Mar 2024 02:31:45 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Sun, 17 Mar 2024 02:31:45 GMT
WORKDIR /home/groovy
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Sun, 17 Mar 2024 02:31:45 GMT
ENV GROOVY_VERSION=4.0.20
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Sun, 17 Mar 2024 02:31:45 GMT
USER 1000:1000
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
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
	-	`sha256:1398cf47b652b314c15a999a812a61f17fe942d81d04191d3d45d6ce2b2eda28`  
		Last Modified: Wed, 05 Jun 2024 04:57:14 GMT  
		Size: 143.9 MB (143896065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e06ec5e75f9ec89d5ed374dbd73b32bb895a5449612015dcd41982831677ad7`  
		Last Modified: Wed, 05 Jun 2024 04:57:05 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a70e026c3ed5fb90e5ecd734c8b8356832ee8f09fca572444ed2008dc56cd9`  
		Last Modified: Wed, 05 Jun 2024 04:57:05 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7085e835b3a471e0a7b82bd4d70541e3e0bfbaa46f05b0cc6dd172eee874c50e`  
		Last Modified: Wed, 05 Jun 2024 15:32:29 GMT  
		Size: 4.3 KB (4334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10a668c3047ae9440cd28d5552dc363520256abf1b99ccc4c960308b981b341`  
		Last Modified: Wed, 05 Jun 2024 15:32:30 GMT  
		Size: 3.5 MB (3473980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e14c0df33786b98b42a8e84b5b75cba3fecb4f2f57ed645c57481a38b2ee09`  
		Last Modified: Wed, 05 Jun 2024 15:32:30 GMT  
		Size: 29.8 MB (29810624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93112154edac5883eab0feb87de86c2a767844ef567dc14cbcdbc64ca5f1615b`  
		Last Modified: Wed, 05 Jun 2024 15:32:30 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:4-jammy` - unknown; unknown

```console
$ docker pull groovy@sha256:05b6cbcd6cd2b6a5b186f5043b4cc90cf4dea30fc3a863716ddf724ceba984a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3955065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f440efe1218b317d86a41bdb67cf89b8540b96fe9bc717ac4d6a7fdfdbbebfe`

```dockerfile
```

-	Layers:
	-	`sha256:a00002d1fe8e5d1febf042dcb87bc1cc02d02622691ad7211d420e86dc26fab2`  
		Last Modified: Wed, 05 Jun 2024 15:32:29 GMT  
		Size: 3.9 MB (3924803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dd675261a850d6d9b18063eaacee05f825a8cf2682f63f0afd6e725f3861c79`  
		Last Modified: Wed, 05 Jun 2024 15:32:29 GMT  
		Size: 30.3 KB (30262 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:4-jammy` - linux; ppc64le

```console
$ docker pull groovy@sha256:7244063827bef0cf5213368c94aefd4e8143da443474ba8afa08f71796b88ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233122767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7c2731c9ed2ac6d603714c26ec3b9cad4c1627a50ad0efc900cf8c638383162`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Sun, 17 Mar 2024 02:31:45 GMT
ARG RELEASE
# Sun, 17 Mar 2024 02:31:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 17 Mar 2024 02:31:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 17 Mar 2024 02:31:45 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 17 Mar 2024 02:31:45 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Sun, 17 Mar 2024 02:31:45 GMT
CMD ["/bin/bash"]
# Sun, 17 Mar 2024 02:31:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 17 Mar 2024 02:31:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 17 Mar 2024 02:31:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 17 Mar 2024 02:31:45 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a900acf3ae56b000afc35468a083b6d6fd695abec87a8abdb02743d5c72f6d6d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='aa7fb6bb342319d227a838af5c363bfa1b4a670c209372f9e6585bd79da6220c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='9b5c375ed7ce654083c6c1137d8daadebaf8657650576115f0deafab00d0f1d7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='44bdd662c3b832cfe0b808362866b8d7a700dd60e6e39716dee97211d35c230f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='af3f33c14ed3e2fcd85a390575029fbf92a491f60cfdc274544ac8ad6532de47';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 17 Mar 2024 02:31:45 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 17 Mar 2024 02:31:45 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 17 Mar 2024 02:31:45 GMT
CMD ["jshell"]
# Sun, 17 Mar 2024 02:31:45 GMT
CMD ["groovysh"]
# Sun, 17 Mar 2024 02:31:45 GMT
ENV GROOVY_HOME=/opt/groovy
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Sun, 17 Mar 2024 02:31:45 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Sun, 17 Mar 2024 02:31:45 GMT
WORKDIR /home/groovy
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Sun, 17 Mar 2024 02:31:45 GMT
ENV GROOVY_VERSION=4.0.20
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Sun, 17 Mar 2024 02:31:45 GMT
USER 1000:1000
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:391f04f7f495cb5fc20be69876c8638cb8f316a2cddac5d48d77ca39244e6dea`  
		Last Modified: Wed, 05 Jun 2024 03:48:14 GMT  
		Size: 35.6 MB (35588332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5071b706d3bd7ec8e211755f3aac7b7183e30aa4f50d72c97b830028c346d4af`  
		Last Modified: Wed, 05 Jun 2024 04:02:49 GMT  
		Size: 18.7 MB (18722020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1658ce6a09dc3e1f29ff12cc424df525f941f95bac688d068775e36e344ab82e`  
		Last Modified: Wed, 05 Jun 2024 04:02:58 GMT  
		Size: 144.8 MB (144793374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b797f2971266e3c5addcb5ee4d0d01a5b4d633502c29950bb643775f7527c0`  
		Last Modified: Wed, 05 Jun 2024 04:02:44 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637066a03fba580770ae878d8129316e16f0697486dfa9741b5751b05e316576`  
		Last Modified: Wed, 05 Jun 2024 04:02:44 GMT  
		Size: 731.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f4a418e76b79e9279deab8fa10b456585bb81fb85d104233f9cc6ff4debf00`  
		Last Modified: Wed, 05 Jun 2024 14:23:37 GMT  
		Size: 4.3 KB (4331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08674748a0852e92e0844cf9078f2ba01fc6fcdad3280b58d2e1c31badd1e508`  
		Last Modified: Wed, 05 Jun 2024 14:23:38 GMT  
		Size: 4.2 MB (4203012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14aee259935d01f68b00351a6c3a87bf180cc00806769010b3315e31fd69830b`  
		Last Modified: Wed, 05 Jun 2024 14:23:38 GMT  
		Size: 29.8 MB (29810623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:598edf7f442cff4fad14ea2e7572a797235662622c0d2cf0f92a1a4bd2412ffa`  
		Last Modified: Wed, 05 Jun 2024 14:23:37 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:4-jammy` - unknown; unknown

```console
$ docker pull groovy@sha256:f9c5711e7282c805f4cb1d60819ae1bd13c71e672cda8c3538bc2ac517f45818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3888343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed75142ca4f16d32ba755623db46206ae5f5a8348c83df8fd6f5318f6989747`

```dockerfile
```

-	Layers:
	-	`sha256:57ad5ec7223f38bbf26b0e7de2b1aaaabf84f0857cd0130c1f9fbe58dd817a8a`  
		Last Modified: Wed, 05 Jun 2024 14:23:37 GMT  
		Size: 3.9 MB (3858450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe2d322425d1a26b7adfdc188e2dae2db239173403c6a9096eb1e20b0f500c7d`  
		Last Modified: Wed, 05 Jun 2024 14:23:37 GMT  
		Size: 29.9 KB (29893 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:4-jammy` - linux; s390x

```console
$ docker pull groovy@sha256:a76329768647f1c981dceb0cdd7f9f8251d091bbeee4373112795d5061b83378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.5 MB (213461326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99686322689ca71c29b87fb9531cebbbcb56dc69fbd78d1c1a3afdb7b97e37ae`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Sun, 17 Mar 2024 02:31:45 GMT
ARG RELEASE
# Sun, 17 Mar 2024 02:31:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 17 Mar 2024 02:31:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 17 Mar 2024 02:31:45 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 17 Mar 2024 02:31:45 GMT
ADD file:4fb908f3bd908a7abc338d7e2006cb2c97aa7f83aca415f3b86c0ae86d61fed1 in / 
# Sun, 17 Mar 2024 02:31:45 GMT
CMD ["/bin/bash"]
# Sun, 17 Mar 2024 02:31:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 17 Mar 2024 02:31:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 17 Mar 2024 02:31:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 17 Mar 2024 02:31:45 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a900acf3ae56b000afc35468a083b6d6fd695abec87a8abdb02743d5c72f6d6d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='aa7fb6bb342319d227a838af5c363bfa1b4a670c209372f9e6585bd79da6220c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='9b5c375ed7ce654083c6c1137d8daadebaf8657650576115f0deafab00d0f1d7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='44bdd662c3b832cfe0b808362866b8d7a700dd60e6e39716dee97211d35c230f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='af3f33c14ed3e2fcd85a390575029fbf92a491f60cfdc274544ac8ad6532de47';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 17 Mar 2024 02:31:45 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 17 Mar 2024 02:31:45 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 17 Mar 2024 02:31:45 GMT
CMD ["jshell"]
# Sun, 17 Mar 2024 02:31:45 GMT
CMD ["groovysh"]
# Sun, 17 Mar 2024 02:31:45 GMT
ENV GROOVY_HOME=/opt/groovy
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Sun, 17 Mar 2024 02:31:45 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Sun, 17 Mar 2024 02:31:45 GMT
WORKDIR /home/groovy
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Sun, 17 Mar 2024 02:31:45 GMT
ENV GROOVY_VERSION=4.0.20
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Sun, 17 Mar 2024 02:31:45 GMT
USER 1000:1000
# Sun, 17 Mar 2024 02:31:45 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:0424de0056677a3a1d049300220cb3d875fb304aae1fa90f7b0292500716e5ed`  
		Last Modified: Wed, 05 Jun 2024 03:12:35 GMT  
		Size: 28.6 MB (28637399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b04c46ec817e6a2a43d4ca0a0487d915cc9831867279ce9b11b41408d280205`  
		Last Modified: Wed, 05 Jun 2024 03:13:39 GMT  
		Size: 17.3 MB (17259370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53bdafbde9a20650510fe076ebdd8b09082d938bf55e16c8d1f494841ad5267`  
		Last Modified: Wed, 05 Jun 2024 03:13:47 GMT  
		Size: 134.3 MB (134336433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d942fb5d7b27a11eb02473ae5bd8b12cc1c63e7692b7087aa3c596a01fc5df`  
		Last Modified: Wed, 05 Jun 2024 03:13:37 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afde48d23b648eb745ea3c9e732f1e6a7d54f277d865d94a70a625e268238c59`  
		Last Modified: Wed, 05 Jun 2024 03:13:37 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c339557afc1c75a9dea849151b7abd633c4cbc1103a2af3071143bb1f6e48f36`  
		Last Modified: Wed, 05 Jun 2024 07:46:24 GMT  
		Size: 4.3 KB (4335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0670597c916c66f3888af853e3e0fec889bcc845f14d2a5e6788f04068c8b74`  
		Last Modified: Wed, 05 Jun 2024 07:46:24 GMT  
		Size: 3.4 MB (3412091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba0c2dc2234ca37472542c7b7f9a79f699c96c593b9eccf2f6f4c63834315cfe`  
		Last Modified: Wed, 05 Jun 2024 07:46:25 GMT  
		Size: 29.8 MB (29810620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23f0086f419bc753fababa30b2c434ebd1819a20bb264826e38d0e1393d3c31`  
		Last Modified: Wed, 05 Jun 2024 07:46:24 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:4-jammy` - unknown; unknown

```console
$ docker pull groovy@sha256:fd9aa57fb4d5680844f6ecc6a633b7cefbb59be971ae76c0329caaf37070881b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3787123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aefc3260c6bc621d96da7b746a4af638e9237b85d75d57337eab81177acc8f4`

```dockerfile
```

-	Layers:
	-	`sha256:4fe4b9c2bb33a089bb5328a7691453f3ff1f14b200daf11c0b933e9636a37ab7`  
		Last Modified: Wed, 05 Jun 2024 07:46:24 GMT  
		Size: 3.8 MB (3757370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afe69df9437ea4a14f36041dc0449e4aafb1e5a03d43883b448eae4af3a60582`  
		Last Modified: Wed, 05 Jun 2024 07:46:24 GMT  
		Size: 29.8 KB (29753 bytes)  
		MIME: application/vnd.in-toto+json
