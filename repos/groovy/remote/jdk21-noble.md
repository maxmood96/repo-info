## `groovy:jdk21-noble`

```console
$ docker pull groovy@sha256:d106bfbbdf4b7aa4c66fe791fe78f5a3d3b72f38939add71c15d6e62ce2d1b33
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

### `groovy:jdk21-noble` - linux; amd64

```console
$ docker pull groovy@sha256:1525d92e1acfe7beccb515c20c1d13da363716369e0c57b3e118ed66dd4a4c29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240922942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38dca3ea2fef0733f1ab552f71c8df2f8a163bedccec1eb2ca21a2daa31cd131`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Wed, 02 Jul 2025 04:24:55 GMT
ARG RELEASE
# Wed, 02 Jul 2025 04:24:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 02 Jul 2025 04:24:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 02 Jul 2025 04:24:55 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 02 Jul 2025 04:24:55 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 02 Jul 2025 04:24:55 GMT
CMD ["/bin/bash"]
# Wed, 02 Jul 2025 04:24:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Jul 2025 04:24:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Jul 2025 04:24:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Jul 2025 04:24:55 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='8171d95189e675e297b5cb96c7ac6247ab4e9f48da82b13f491fc46ef5d97836';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 02 Jul 2025 04:24:55 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 02 Jul 2025 04:24:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 02 Jul 2025 04:24:55 GMT
CMD ["jshell"]
# Wed, 02 Jul 2025 04:24:55 GMT
CMD ["groovysh"]
# Wed, 02 Jul 2025 04:24:55 GMT
ENV GROOVY_HOME=/opt/groovy
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to groovy"     && groupmod --new-name groovy ubuntu     && mkdir /home/groovy     && usermod --login groovy --home /home/groovy --groups groovy ubuntu     && chown groovy /home/groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Wed, 02 Jul 2025 04:24:55 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Wed, 02 Jul 2025 04:24:55 GMT
WORKDIR /home/groovy
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Wed, 02 Jul 2025 04:24:55 GMT
ENV GROOVY_VERSION=4.0.27
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Wed, 02 Jul 2025 04:24:55 GMT
USER 1000:1000
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51d8cf184477166509f3db9216fce57ab67d94b9b882f2f10ff2891baba2550`  
		Last Modified: Tue, 12 Aug 2025 17:24:54 GMT  
		Size: 23.0 MB (22958720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9e2e04796b2ee0ed28666a3def2a846c561134cbd2d024b273991f8c85936f`  
		Last Modified: Tue, 12 Aug 2025 17:51:57 GMT  
		Size: 157.8 MB (157809399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9967391d7d212b197d98e34a983091c6878b25ce3fb014d6f01065f6f6167096`  
		Last Modified: Tue, 12 Aug 2025 17:24:49 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9246e450bedd7659121fadbb2365286bed2c7be3365f401ba6cf042289bd63e0`  
		Last Modified: Tue, 12 Aug 2025 17:24:50 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa11348a9c82c0438da9db9ad8b8a77a9204e9eb2c536406ba9eb1e4c583395c`  
		Last Modified: Tue, 12 Aug 2025 17:53:01 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8675de741eb6c1aafe4803e641d37022fff83aedce5cc8d437fbf3e18cdd4c`  
		Last Modified: Tue, 12 Aug 2025 17:53:03 GMT  
		Size: 242.0 KB (242042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9488d46335a5940bee90b6b30130e6a3b867137d73abf463bc4b7787335e28f5`  
		Last Modified: Tue, 12 Aug 2025 17:53:08 GMT  
		Size: 30.2 MB (30185645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9723529e0fde2de2a25e4f6c203f0561d2089bcf89191c8805ff5dc58570bdc0`  
		Last Modified: Tue, 12 Aug 2025 17:53:06 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk21-noble` - unknown; unknown

```console
$ docker pull groovy@sha256:d2b45eff70623785d29c19bac8dc6664ad9e067708cb00ecbba48a66b605e435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3656402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a325aaefaf3c8cab048e7ab74df3e2b53cbca44dfe32668c1ef9d57a2df32eb`

```dockerfile
```

-	Layers:
	-	`sha256:a0e4426b51b3d15a2fe119b230adc01b100a1ae4ddcfad91609f7f3613badbc5`  
		Last Modified: Tue, 12 Aug 2025 20:20:25 GMT  
		Size: 3.6 MB (3625128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0219ea17c727c7bf9389c5bb2bc05e96825b16aa3a0cce3767e19fd7fb7e4b97`  
		Last Modified: Tue, 12 Aug 2025 20:20:26 GMT  
		Size: 31.3 KB (31274 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:jdk21-noble` - linux; arm64 variant v8

```console
$ docker pull groovy@sha256:f243213466f171e628f4add1d936195a265afff5ac8aac5c157be30c2976f1c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.5 MB (239546069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:585d79b80ff000225764102d1e6206eed421079db4a3495451f74ef946362f51`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Wed, 02 Jul 2025 04:24:55 GMT
ARG RELEASE
# Wed, 02 Jul 2025 04:24:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 02 Jul 2025 04:24:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 02 Jul 2025 04:24:55 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 02 Jul 2025 04:24:55 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 02 Jul 2025 04:24:55 GMT
CMD ["/bin/bash"]
# Wed, 02 Jul 2025 04:24:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Jul 2025 04:24:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Jul 2025 04:24:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Jul 2025 04:24:55 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='8171d95189e675e297b5cb96c7ac6247ab4e9f48da82b13f491fc46ef5d97836';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 02 Jul 2025 04:24:55 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 02 Jul 2025 04:24:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 02 Jul 2025 04:24:55 GMT
CMD ["jshell"]
# Wed, 02 Jul 2025 04:24:55 GMT
CMD ["groovysh"]
# Wed, 02 Jul 2025 04:24:55 GMT
ENV GROOVY_HOME=/opt/groovy
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to groovy"     && groupmod --new-name groovy ubuntu     && mkdir /home/groovy     && usermod --login groovy --home /home/groovy --groups groovy ubuntu     && chown groovy /home/groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Wed, 02 Jul 2025 04:24:55 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Wed, 02 Jul 2025 04:24:55 GMT
WORKDIR /home/groovy
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Wed, 02 Jul 2025 04:24:55 GMT
ENV GROOVY_VERSION=4.0.27
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Wed, 02 Jul 2025 04:24:55 GMT
USER 1000:1000
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5ce41d5de7afb59affbe0233d7397418d2e57ed330589e31f1678f08a6fa5e`  
		Last Modified: Tue, 12 Aug 2025 18:36:42 GMT  
		Size: 24.2 MB (24165644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf34575c4e3b3b166c464edf4e5028e3cfc1c601ff17cfbbf1e7acdee8e50ad`  
		Last Modified: Tue, 12 Aug 2025 20:03:06 GMT  
		Size: 156.1 MB (156088917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1966e7bdaa805e2a3fb4d7f8bd3b8b696ad43a80ee23c4e497b0c806325e31`  
		Last Modified: Tue, 12 Aug 2025 18:38:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc5dbd963a682bc03f830ef4c292f4d1afbbc2fe50658fe169297a94fa1dac9`  
		Last Modified: Tue, 12 Aug 2025 18:38:43 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d160a9226c81345f7e1977bdf93bad9b96c901a6b454df893bad7a62621c9f`  
		Last Modified: Tue, 12 Aug 2025 22:53:35 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901ba693e810ecc745098dbf6e5cb7b6e587fca50b889e87d20bc99bcd11a1bc`  
		Last Modified: Tue, 12 Aug 2025 22:53:34 GMT  
		Size: 241.6 KB (241582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5f799a2adb0ddf501e439904af051db51c6b2980dd4de05c6ffdc10203cf43`  
		Last Modified: Tue, 12 Aug 2025 22:53:32 GMT  
		Size: 30.2 MB (30185630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01426ea74652848507cefc603b190d57054810e54e76d30d162bd2fb43fb2480`  
		Last Modified: Tue, 12 Aug 2025 22:53:30 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk21-noble` - unknown; unknown

```console
$ docker pull groovy@sha256:68860ea8b30da78c3e931372607926947cd910a748c08501ee1b8117abc17e5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3788552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e8a34434795ddd06c161b3332adcfc1467530c2697b500b372c61d8ec7140be`

```dockerfile
```

-	Layers:
	-	`sha256:aae4cbad5048fb1668200447a855193a68b74c283f90b4317a803b8664a4eabd`  
		Last Modified: Tue, 12 Aug 2025 23:20:35 GMT  
		Size: 3.8 MB (3756889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cef91964cb7daba6717e9ed971e2c961e6d7389a6939febc8c861f4830858909`  
		Last Modified: Tue, 12 Aug 2025 23:20:36 GMT  
		Size: 31.7 KB (31663 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:jdk21-noble` - linux; ppc64le

```console
$ docker pull groovy@sha256:655d3e7d492b6d4e951bd7638ee0e3246b9b97989331fa7c55868b715c83a293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.9 MB (246862692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2339707ae1a60643ad20a4824897bef23720d3761361fbe0024f3cadc4086b97`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Wed, 02 Jul 2025 04:24:55 GMT
ARG RELEASE
# Wed, 02 Jul 2025 04:24:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 02 Jul 2025 04:24:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 02 Jul 2025 04:24:55 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 02 Jul 2025 04:24:55 GMT
ADD file:e2ae399c3aa36bf07b7d3562a21b9ad89f66ae6e03733ed0edcdcda5bd391c60 in / 
# Wed, 02 Jul 2025 04:24:55 GMT
CMD ["/bin/bash"]
# Wed, 02 Jul 2025 04:24:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Jul 2025 04:24:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Jul 2025 04:24:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Jul 2025 04:24:55 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='8171d95189e675e297b5cb96c7ac6247ab4e9f48da82b13f491fc46ef5d97836';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 02 Jul 2025 04:24:55 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 02 Jul 2025 04:24:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 02 Jul 2025 04:24:55 GMT
CMD ["jshell"]
# Wed, 02 Jul 2025 04:24:55 GMT
CMD ["groovysh"]
# Wed, 02 Jul 2025 04:24:55 GMT
ENV GROOVY_HOME=/opt/groovy
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to groovy"     && groupmod --new-name groovy ubuntu     && mkdir /home/groovy     && usermod --login groovy --home /home/groovy --groups groovy ubuntu     && chown groovy /home/groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Wed, 02 Jul 2025 04:24:55 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Wed, 02 Jul 2025 04:24:55 GMT
WORKDIR /home/groovy
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Wed, 02 Jul 2025 04:24:55 GMT
ENV GROOVY_VERSION=4.0.27
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Wed, 02 Jul 2025 04:24:55 GMT
USER 1000:1000
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:403b01240f845337685ead3abfb0228bb1d1b78b076d609aa20f4733d260f58f`  
		Last Modified: Wed, 30 Jul 2025 11:30:48 GMT  
		Size: 34.3 MB (34329650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44dac22db2acf299562658bdbfc8f885fd4929a06be6ed9a37bc4736330fe91b`  
		Last Modified: Tue, 12 Aug 2025 17:39:59 GMT  
		Size: 24.1 MB (24101582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e917ebf66df5f21e8f8a6fcb5fed8b8aae52537f9a9f89c75c0290510ce1a6b2`  
		Last Modified: Tue, 12 Aug 2025 18:46:20 GMT  
		Size: 158.0 MB (157969889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07ca97c37923f60b48017e671652f8ec10759b3245737ebab3d46e45bde8932`  
		Last Modified: Tue, 12 Aug 2025 17:58:35 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08dafcc6f3cf8a0ab22e0589729586dc5636b06c81225f289939204617ecb117`  
		Last Modified: Tue, 12 Aug 2025 17:58:38 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4879cc6e50ece24c6fe21a123d1b12fea5a88b7ccc6f6a42d4a6ef8fd1763319`  
		Last Modified: Tue, 12 Aug 2025 23:53:10 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6da6aa78f9a5b9a90ef52bd5dfeb681b7baa3203a60ae578d4d95db82c6f23`  
		Last Modified: Tue, 12 Aug 2025 23:53:11 GMT  
		Size: 272.0 KB (272017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367cc8c693ae1eb30f1093551502bd0abf7340c5395a5cbe3608198466493e3d`  
		Last Modified: Tue, 12 Aug 2025 23:53:14 GMT  
		Size: 30.2 MB (30185630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e398318bde77c1744fe3fe868afca04d8a8b3093c26782680ad1014210fd38a`  
		Last Modified: Tue, 12 Aug 2025 23:53:10 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk21-noble` - unknown; unknown

```console
$ docker pull groovy@sha256:9ae1f4d11dc33e9bf743a3038082f1f8b152e97eef9cf96eda097ac57491b96d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3704466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b3f5c40d2ef012c579b920edfc091b08c1ef284382ba0b76f772e8933dcc58`

```dockerfile
```

-	Layers:
	-	`sha256:802b36f29dc9353858eed8bcf3c31cff2328afa22135aa2638ede1fffea567b2`  
		Last Modified: Wed, 13 Aug 2025 02:20:29 GMT  
		Size: 3.7 MB (3673022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4732921e752cc80e919c85a1952c88416e05797ff4586e153fcfa6bd06c84b79`  
		Last Modified: Wed, 13 Aug 2025 02:20:30 GMT  
		Size: 31.4 KB (31444 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:jdk21-noble` - linux; riscv64

```console
$ docker pull groovy@sha256:815df79d4f9fe58464cebdbf9f28520ef6ec434b0c0b1071505982488e6d0754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235139319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4df468f6a1572c2d14ec93e275ee56c8fe3f7e662b1b8868d1fa67cd9ab5f5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Wed, 02 Jul 2025 04:24:55 GMT
ARG RELEASE
# Wed, 02 Jul 2025 04:24:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 02 Jul 2025 04:24:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 02 Jul 2025 04:24:55 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 02 Jul 2025 04:24:55 GMT
ADD file:07f3c32dd2b7f6af0f399701257442794654b72aa96759b98cb033a715461739 in / 
# Wed, 02 Jul 2025 04:24:55 GMT
CMD ["/bin/bash"]
# Wed, 02 Jul 2025 04:24:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Jul 2025 04:24:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Jul 2025 04:24:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Jul 2025 04:24:55 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='8171d95189e675e297b5cb96c7ac6247ab4e9f48da82b13f491fc46ef5d97836';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 02 Jul 2025 04:24:55 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 02 Jul 2025 04:24:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 02 Jul 2025 04:24:55 GMT
CMD ["jshell"]
# Wed, 02 Jul 2025 04:24:55 GMT
CMD ["groovysh"]
# Wed, 02 Jul 2025 04:24:55 GMT
ENV GROOVY_HOME=/opt/groovy
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to groovy"     && groupmod --new-name groovy ubuntu     && mkdir /home/groovy     && usermod --login groovy --home /home/groovy --groups groovy ubuntu     && chown groovy /home/groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Wed, 02 Jul 2025 04:24:55 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Wed, 02 Jul 2025 04:24:55 GMT
WORKDIR /home/groovy
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Wed, 02 Jul 2025 04:24:55 GMT
ENV GROOVY_VERSION=4.0.27
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Wed, 02 Jul 2025 04:24:55 GMT
USER 1000:1000
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:b12e9b07091787c99b29dd2be63680c86c47e8be60a46566329007fb82cee41d`  
		Last Modified: Tue, 12 Aug 2025 17:05:53 GMT  
		Size: 31.0 MB (30951577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad34db99b8b6d3689c6e8a55f34d183fc435ecd3c12cf99054a4e88b66485262`  
		Last Modified: Tue, 12 Aug 2025 18:16:38 GMT  
		Size: 20.1 MB (20142191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ed77a84631ddb22d11797ed16369a4012b54722b11977b17b1c5735ce60cf6`  
		Last Modified: Tue, 12 Aug 2025 19:58:57 GMT  
		Size: 153.6 MB (153602021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c685ab3f81c4315d1b9d1a6a0a258e682da0586cba6f45d6504d6600701410f`  
		Last Modified: Tue, 12 Aug 2025 17:49:59 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c1ee18ad5ca7c547af330fcdd24445fee1c86fdbf70d30ea5020e8fb367b2b`  
		Last Modified: Tue, 12 Aug 2025 17:50:01 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6564300d14e13ff47671aeba2e782d9b5221b8bb4c11a67766b45a5b3a01c806`  
		Last Modified: Tue, 12 Aug 2025 23:22:38 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f0c2e0c4a423844e57284da0018de6d3de8a786d1333feb62beb8e1cdc2bfb`  
		Last Modified: Tue, 12 Aug 2025 23:22:38 GMT  
		Size: 254.0 KB (253991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d0311d253c44c233fbeedd7f43816c0c1b8db29e0dc16b1933ab75c7e2ca89`  
		Last Modified: Tue, 12 Aug 2025 23:22:36 GMT  
		Size: 30.2 MB (30185618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee4e12e6c9ce4d2818ab375859cad7c3896f8d381959b8b324213f90aa81094`  
		Last Modified: Tue, 12 Aug 2025 23:22:33 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk21-noble` - unknown; unknown

```console
$ docker pull groovy@sha256:8a7495fdbb1b3a2f34b5223e5e4ff0b07eb83e72d766d8629f0770eb29f39a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3763941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982c62cfaddc75d1c8263e24a64445b40904b57a8f2301bdc49b6331034037e1`

```dockerfile
```

-	Layers:
	-	`sha256:1bb74b634d723eacbac114ea1bb28c9f289497292558ce80c14b832244e02fa2`  
		Last Modified: Wed, 13 Aug 2025 02:20:34 GMT  
		Size: 3.7 MB (3732497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4da1317319863d445bc0d74746a8a909c6379559195614cc6f7cd2fcbacf8339`  
		Last Modified: Wed, 13 Aug 2025 02:20:35 GMT  
		Size: 31.4 KB (31444 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:jdk21-noble` - linux; s390x

```console
$ docker pull groovy@sha256:4376602450cfd6324ecb01fd04775ac5550059149fa961dd5ea01ffa73ae9e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229540363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7eb2904e32ace2678a0d26dfe62ab66adee35906891add2c2af88e3d828b32`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Wed, 02 Jul 2025 04:24:55 GMT
ARG RELEASE
# Wed, 02 Jul 2025 04:24:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 02 Jul 2025 04:24:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 02 Jul 2025 04:24:55 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 02 Jul 2025 04:24:55 GMT
ADD file:f751959e6b8dae58a35017dc82c7271708f085c111710b59527373699b0784b5 in / 
# Wed, 02 Jul 2025 04:24:55 GMT
CMD ["/bin/bash"]
# Wed, 02 Jul 2025 04:24:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Jul 2025 04:24:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Jul 2025 04:24:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Jul 2025 04:24:55 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='8171d95189e675e297b5cb96c7ac6247ab4e9f48da82b13f491fc46ef5d97836';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 02 Jul 2025 04:24:55 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 02 Jul 2025 04:24:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 02 Jul 2025 04:24:55 GMT
CMD ["jshell"]
# Wed, 02 Jul 2025 04:24:55 GMT
CMD ["groovysh"]
# Wed, 02 Jul 2025 04:24:55 GMT
ENV GROOVY_HOME=/opt/groovy
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to groovy"     && groupmod --new-name groovy ubuntu     && mkdir /home/groovy     && usermod --login groovy --home /home/groovy --groups groovy ubuntu     && chown groovy /home/groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Wed, 02 Jul 2025 04:24:55 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Wed, 02 Jul 2025 04:24:55 GMT
WORKDIR /home/groovy
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Wed, 02 Jul 2025 04:24:55 GMT
ENV GROOVY_VERSION=4.0.27
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Wed, 02 Jul 2025 04:24:55 GMT
USER 1000:1000
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:1c5d0b18c745fadd2e177b54d4df793f25b01437577bc09c72ae52a0f3f9aeb3`  
		Last Modified: Wed, 30 Jul 2025 11:30:49 GMT  
		Size: 29.9 MB (29932680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca1d3019421a7aa66519824ce0e982b25db3c4e4004543099d050378dee3b89`  
		Last Modified: Tue, 12 Aug 2025 17:31:44 GMT  
		Size: 22.1 MB (22128620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dde20cb1cc0afeadd58455ba9b92aa1d948a128d674b17c9a766205c845fa85`  
		Last Modified: Tue, 12 Aug 2025 19:59:19 GMT  
		Size: 147.0 MB (147036882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110ad87a33b450be1a83bae10a1e154b38f8d28b2a410cd79573a7581552ed69`  
		Last Modified: Tue, 12 Aug 2025 17:34:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d993136b80279c45bf94985aada87e93498dd4d46b42e123b919c7ed1c4f63d0`  
		Last Modified: Tue, 12 Aug 2025 17:34:45 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3568fb376fe0be0429ad595e9cc58590b34b7f660f790920a0857b18e7e0d66`  
		Last Modified: Tue, 12 Aug 2025 19:12:44 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb1040c44348ce847cfed4be80d43bf2f3223d22ba418691190f09915164e0a`  
		Last Modified: Tue, 12 Aug 2025 19:12:44 GMT  
		Size: 252.6 KB (252638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12f1976d7a8f37ba501dd944ce0cba8d439f1daef5f78e40b3b9b62bfd1eacf`  
		Last Modified: Tue, 12 Aug 2025 19:12:46 GMT  
		Size: 30.2 MB (30185626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e81b0a5eded25637e404158bdc1056a5355328e096f2720494338ffcc1bb9fb`  
		Last Modified: Tue, 12 Aug 2025 19:12:43 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk21-noble` - unknown; unknown

```console
$ docker pull groovy@sha256:7c19c3651b2168a00e70fc4b8b1478e937f37c9c4c4e67da38d241a0ca75aa06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3602215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f8c7e03b467fc54f36c0b79dd156d4b062d70b0617c3a71ea62eca30d6902c`

```dockerfile
```

-	Layers:
	-	`sha256:49485e6e048a08fce87ad79d37c8eab84e9de85da1479dcf8e4976a7c8181f63`  
		Last Modified: Tue, 12 Aug 2025 20:20:47 GMT  
		Size: 3.6 MB (3570941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:036cc2d87bd73901fa39920f2da20682e1e0b86ac65659d3c3773386fca2e8a7`  
		Last Modified: Tue, 12 Aug 2025 20:20:48 GMT  
		Size: 31.3 KB (31274 bytes)  
		MIME: application/vnd.in-toto+json
