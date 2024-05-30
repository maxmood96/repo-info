## `groovy:jdk17`

```console
$ docker pull groovy@sha256:c4ef9b4ef54ded6d3eeb6313b703bd23be46ed1dcd4dc7279cee40b4b9126eb7
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

### `groovy:jdk17` - linux; amd64

```console
$ docker pull groovy@sha256:fd335e183f9a63cf712f7c50b9ce9a99f04491a6e84f3b85c6fc949b3ac94e3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226315755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295c13175cd33f8d6f039200915ae15330ed483159c1ce923a8dc6b457890193`
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
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
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
	-	`sha256:4a023cab5400feb5c1ab725beb8345ddb0e3200314004b56677a5eee2e8c86cf`  
		Last Modified: Sat, 27 Apr 2024 20:07:18 GMT  
		Size: 30.4 MB (30439649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5d1bccc5440d3a24f4a620704b9e687b4163c6c872fcc8e812e200c9bbac58`  
		Last Modified: Thu, 02 May 2024 01:18:08 GMT  
		Size: 17.5 MB (17456240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59fd278c1b4ffe1727be6ccba42125e8f4db57e660e795cce19889d2c776457`  
		Last Modified: Thu, 02 May 2024 01:18:17 GMT  
		Size: 145.1 MB (145100254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97285723537ab7921fca4d081c256e501adfdaa8992d04637992075f4cea392`  
		Last Modified: Thu, 02 May 2024 01:18:05 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ba11f7aaaedad962216812fe84aee9061aeabac6932f0274a1d204eb96e8e8`  
		Last Modified: Thu, 02 May 2024 01:18:05 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1cff7593b41fc94ecbd169b032e4779cffa4de27b98480840ebbf761a6f4e9`  
		Last Modified: Wed, 29 May 2024 19:59:24 GMT  
		Size: 4.3 KB (4331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19cdd1cd435a1fba86cc471036a817c773716e5b4f501fd112c7971ef127269`  
		Last Modified: Wed, 29 May 2024 19:59:25 GMT  
		Size: 3.5 MB (3503584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38666734b4476e906aa01028fb890860be5a1f7558923eaec3573ef785a25d36`  
		Last Modified: Wed, 29 May 2024 19:59:25 GMT  
		Size: 29.8 MB (29810621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db7048457f3d0e77a5352495bcf009763f99d89832fe1189a3348704bdfe7a1`  
		Last Modified: Wed, 29 May 2024 19:59:24 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk17` - unknown; unknown

```console
$ docker pull groovy@sha256:b59e69d8268e9c59ad588abfaea6e867ac9e24aa5bb75ab9bf2ffa47b02aac4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3858149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d9647738c0b7704d1aa58a605ff181461c207fe2e52dc8dfc1e5b70b09b6051`

```dockerfile
```

-	Layers:
	-	`sha256:1a88570c590058ad34e00f12a997cb82bbfb82730f693b044cfb2a75a9e1261a`  
		Last Modified: Wed, 29 May 2024 19:59:24 GMT  
		Size: 3.8 MB (3828396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6353d4e1dd5ac2f1338014bc82144250ff95a1cdd796a322e458f641aa390ff6`  
		Last Modified: Wed, 29 May 2024 19:59:24 GMT  
		Size: 29.8 KB (29753 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:jdk17` - linux; arm variant v7

```console
$ docker pull groovy@sha256:c3869930ec6120264583c710c5ed94e7cd9ff4750305ed06daf1281faddbc770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.2 MB (221165691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7927c8c2eb69490ba9441b2e0969483d3dc9e0a9e8a2524def74cc1953a3687`
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
ADD file:ab2e95a123b006ac900aaaf0d1858b88941c8d319f47e41733db6f0f5fe98b87 in / 
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
	-	`sha256:b7e19bb2918236ac8ccf2faf405ff5a9521a86762ef07ef60917aa41d6dc8155`  
		Last Modified: Mon, 29 Apr 2024 07:54:39 GMT  
		Size: 27.5 MB (27536224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b3f73c192c90e17e2d0c62653322b55508663f76bd4f376e3f404d5117dbed`  
		Last Modified: Thu, 02 May 2024 01:30:27 GMT  
		Size: 17.6 MB (17591102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12f1f6abdb613617941a12fdd4a42598b8523f7d5b182ac4fa4660ddfba933c`  
		Last Modified: Thu, 02 May 2024 01:30:37 GMT  
		Size: 142.6 MB (142578026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effae5a6ff12fa462f0d7ca8324f93268c4a4b100097c168bb53283313b98797`  
		Last Modified: Thu, 02 May 2024 01:30:24 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f39a96c1b10f751b301b1d5576fa736097494d4083e06460132966c89f06cf`  
		Last Modified: Thu, 02 May 2024 01:30:24 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771e2215622a2a276eca9ec120d7a719155f50273616e88f93cf4afc2b8c805f`  
		Last Modified: Wed, 29 May 2024 20:15:09 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746bac0b2490b544b08a596a8de345b366ae4a334b02733407bafe3fd9196779`  
		Last Modified: Wed, 29 May 2024 20:15:10 GMT  
		Size: 3.6 MB (3644320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53cde7791751f66ac89cef51f0758ec8443cd8ffe95b77d62ef55db3371237d7`  
		Last Modified: Wed, 29 May 2024 20:15:11 GMT  
		Size: 29.8 MB (29810627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a66d2dd98940e3a66591f106f14f08f3de4f601266ebb213fd3a3342d432b8`  
		Last Modified: Wed, 29 May 2024 20:15:09 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk17` - unknown; unknown

```console
$ docker pull groovy@sha256:fcd2de4635de3e05eb1daa27b381e9bea5b1f58a9fdccb435e46985a3ad64279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3778644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ed57edd47365827c0c4e3bdd325c58a6c4556cd0e0eddf538dc23f52e3bc2c9`

```dockerfile
```

-	Layers:
	-	`sha256:5c41dbea1326d4cfcfe528d129c5e918f831b0c3cff6effe40f97930a86526d9`  
		Last Modified: Wed, 29 May 2024 20:15:09 GMT  
		Size: 3.7 MB (3748654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05c526d9d4d943361d1557cb1028eb39a8243681cc15264972ef16aa057d6769`  
		Last Modified: Wed, 29 May 2024 20:15:09 GMT  
		Size: 30.0 KB (29990 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:jdk17` - linux; arm64 variant v8

```console
$ docker pull groovy@sha256:280dd930742cb6196e780e33f4ce5011cad16ed44401fa0bda67d226ba930c02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.4 MB (224444243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0966496adcb4ab220e6fe8ad7d1d0be43f910425d925e496e9f9e985eb625e21`
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
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
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
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8868eeb30ae6b43fdd3ec11d565b77e83f6c78c86d892957cf1cecb5cc59c9`  
		Last Modified: Thu, 02 May 2024 04:19:45 GMT  
		Size: 18.9 MB (18858238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c5f0f638087f0231a157f7deba2d5494e0cd15dfc56fab26293430ccccd3d2`  
		Last Modified: Thu, 02 May 2024 04:19:53 GMT  
		Size: 143.9 MB (143896056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b7d030db882e91686c67d5a7c655905f45b24a3e131c15eacc276f3033475c`  
		Last Modified: Thu, 02 May 2024 04:19:43 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00ec0bc677d0cfff04f78636ce68c4815766fc7560ceb0c5f031e84ffb38607`  
		Last Modified: Thu, 02 May 2024 04:19:43 GMT  
		Size: 731.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f45a09b8260059a5786b38fcc323759dad24a5b4e5c4259c6bc8b73c7e2efcb`  
		Last Modified: Thu, 30 May 2024 02:11:45 GMT  
		Size: 4.3 KB (4339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d574c60a83b637bb91378b89fa717976e8606428d5a9cfa5e62164a01046dd`  
		Last Modified: Thu, 30 May 2024 02:11:45 GMT  
		Size: 3.5 MB (3472728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4bae6d1784467ea5306c7e8bc82f8e908400c36fcc49523a997404eb735a6b8`  
		Last Modified: Thu, 30 May 2024 02:11:46 GMT  
		Size: 29.8 MB (29810624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7d6b173e4ee2e06b578326690afa4894949945f3c0d5b65da2fbb61fc5cb87`  
		Last Modified: Thu, 30 May 2024 02:11:45 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk17` - unknown; unknown

```console
$ docker pull groovy@sha256:bbe899db40cfb8d091f7135633402c0d8b58ee25ef556b68b102da77d550f36f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3955066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7889dfd1db73950770d70f25db3db7bb8c7a830971743fe72a62b0defec62084`

```dockerfile
```

-	Layers:
	-	`sha256:b5f4448d9d897a09a7a9a024b1564643cefb2f1b83bad06fb670104aa73b3652`  
		Last Modified: Thu, 30 May 2024 02:11:45 GMT  
		Size: 3.9 MB (3924804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:971d3a34c3e9e05cb7a480b24b18d8fb9d284e62f2f1ecd25ab57f60f45c0c6f`  
		Last Modified: Thu, 30 May 2024 02:11:45 GMT  
		Size: 30.3 KB (30262 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:jdk17` - linux; ppc64le

```console
$ docker pull groovy@sha256:e1733a0414790903b0b4871206624c8547dccea3a80d68c1cdaaddb432f12585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233124713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6159a11959f051242bdc29227eeaf5863e05e77c9b9afe2768130bd8ee9d5d60`
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
ADD file:3ab2760f4e449111dcca3f0816583c72999e1ce2ec20beac068dccfd6c9d8b81 in / 
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
	-	`sha256:ef1313ed517c6def5644ab70e25cc66f1c4cd52b1e81c07fb33bfb8850b39c25`  
		Last Modified: Thu, 02 May 2024 01:40:15 GMT  
		Size: 35.6 MB (35588524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce34360d55ae028192392c25f1a7ba3e34d2877f439114b2769039b5dfa13b9d`  
		Last Modified: Thu, 02 May 2024 01:54:21 GMT  
		Size: 18.7 MB (18722864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42849840e3a90a8ebdf702470b466cc65476a789891097b66680eec53aaae4f8`  
		Last Modified: Thu, 02 May 2024 01:54:30 GMT  
		Size: 144.8 MB (144794148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7017e34365e5f6c03867bf5a507591b84dc8bae09179ec3e4dbba6029e32dcc`  
		Last Modified: Thu, 02 May 2024 01:54:15 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22fdf18c8ebf0a6672e6f5a0eb29814e5e40afedc235495b684f13aebea2c159`  
		Last Modified: Thu, 02 May 2024 01:54:15 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a89d351fadd7b54d284b68bb01ddc0abfcdb2fd1c4cf4018c6e4ad49636219f`  
		Last Modified: Wed, 29 May 2024 20:16:48 GMT  
		Size: 4.3 KB (4329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5afbed6c3d7028725bab6e5e7bfcbf6bbb03d0c1a80f14199a19c7cfac6b6566`  
		Last Modified: Wed, 29 May 2024 20:16:49 GMT  
		Size: 4.2 MB (4203138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1a68607941dbc92ba651f1cf7de1d1b492d2565c06c421ced56ef92444881b`  
		Last Modified: Wed, 29 May 2024 20:16:49 GMT  
		Size: 29.8 MB (29810630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aeadbc7a63d454ea8ef3edfa31927f9c755ffd771dfc559d99e452f64cfdd0c`  
		Last Modified: Wed, 29 May 2024 20:16:48 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk17` - unknown; unknown

```console
$ docker pull groovy@sha256:97485a2931bebc2ba2527d8207343cf560af3ebe33320a64cf245c2a7a9d4e2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3888344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7e4b06466d098b7dfa937aaa1752c4e96a4e853a3e4472e0a8b47806741eb9b`

```dockerfile
```

-	Layers:
	-	`sha256:3db5a23316cdaf758d7084066230279232e835fad34c3cc927ad13c30a3c932c`  
		Last Modified: Wed, 29 May 2024 20:16:48 GMT  
		Size: 3.9 MB (3858451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32d35fe495ac81737a2520d85b1213bdb8419a8f9b5d68a2277522021bbb6893`  
		Last Modified: Wed, 29 May 2024 20:16:48 GMT  
		Size: 29.9 KB (29893 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:jdk17` - linux; s390x

```console
$ docker pull groovy@sha256:34e45b46f1fecfd875b99848cae444c5aaba4ebd0341f2539fce3a9d300fcb95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.5 MB (213461290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:627b070ba65b17b8f5ef76a98f1d8b0f3b469b8f1cb754b8da84d9108de5380a`
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
ADD file:7d693ab3b1f45d4992a119ec94444efc96c176ad954375f3bc1299ab813a46a0 in / 
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
	-	`sha256:ffda8878ec88daab976ebae63a8dc770c7ff669cb06828bf12b1a5acca67f1f8`  
		Last Modified: Thu, 02 May 2024 01:13:50 GMT  
		Size: 28.6 MB (28637522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9390685e0a430de7796df7df6993f29237307d1119a049ee83b14acf2ef63598`  
		Last Modified: Thu, 02 May 2024 01:46:04 GMT  
		Size: 17.3 MB (17259595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3932a8168eb0d977840fcf3b0a5973fa148307408ab58b28429e4a0958df0b9`  
		Last Modified: Thu, 02 May 2024 01:46:12 GMT  
		Size: 134.3 MB (134336102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dff6182059ff647ff16317ba774b54aef922781cb97918338f4c8043f733353`  
		Last Modified: Thu, 02 May 2024 01:46:01 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593147e9c25b096fbfc816d950ebb6914d4f3558a44dd7391e5065dbcf729696`  
		Last Modified: Thu, 02 May 2024 01:46:01 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c3536d4b9c7f140c190d62d77efec8ef93e034bf1d3b2b2e143a7a10779afc`  
		Last Modified: Wed, 29 May 2024 20:13:22 GMT  
		Size: 4.3 KB (4335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8831874afabf5964f0c6c98e52d08154e88c7537a4837b90638e3e3f13b829`  
		Last Modified: Wed, 29 May 2024 20:13:22 GMT  
		Size: 3.4 MB (3412032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6384b9d13b5746b7a85d60656a8bb5a04b3d77815f625b1ec96a72d06c86f60c`  
		Last Modified: Wed, 29 May 2024 20:13:22 GMT  
		Size: 29.8 MB (29810625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acaa17ce5802be5056c7e73b786a9915eae7f3b63c91c6e6c9bdf79729bfdea`  
		Last Modified: Wed, 29 May 2024 20:13:22 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk17` - unknown; unknown

```console
$ docker pull groovy@sha256:e892aa4ae5f6e4141a9cb9f8873bc8fb3a4d603cc9bc819dee12e06325b7ca97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3787122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f6fa9a23071364a8b89c469220e2bbae53c2e69c22b3055ba7919bae283614`

```dockerfile
```

-	Layers:
	-	`sha256:ab9c0609931cb693097ad695700f9787db8d937d1634b574302fcbb9f2b70cc8`  
		Last Modified: Wed, 29 May 2024 20:13:22 GMT  
		Size: 3.8 MB (3757371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22c3c1790722383e5bf47f6495dc0456778c417da3a52c57174e4856dfef23bd`  
		Last Modified: Wed, 29 May 2024 20:13:21 GMT  
		Size: 29.8 KB (29751 bytes)  
		MIME: application/vnd.in-toto+json
