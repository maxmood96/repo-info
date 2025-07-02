## `groovy:4-jdk17-noble`

```console
$ docker pull groovy@sha256:75767444fb1833dece66977585504d0d3d60a5f31d6c0a8526a81ed263e0e526
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `groovy:4-jdk17-noble` - linux; amd64

```console
$ docker pull groovy@sha256:80aa20ae830568184ef09fc563c32fe0c497dcc82a55fd33da95afced2769b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227751617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5020c0dc707cfc7a5a3578ee90a643476d9c0364ed580985824b4a23117d40cf`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9616877c733c9249328ea9bd83a5c8c30e0f9a7af180cac8ffda9034161c2df2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='0db0d6cbe33238f33aa52837b1dc8fc6067b34d206b3e0f9243c7f8c9b9539a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='8a3c859355f898c119d154e4caf867263e0e4c8065a91d63ae10666c19bc1108';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='0823d92d9537fcdd56952abc450d1f9585b4d329f8f884dcb230a2e08db6bf5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        riscv64)          ESUM='1a9a532a6c3e591c5eb72ef875d0f5825961bf8cb0eeea876d7f1e198575ed49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='0033ef81d9c1d30782c5638c20bd7ce3681ebf4b8a68cbc750bb15d613e76e67';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
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
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bf331549f652756582afefc2ee7c09a64ab25e34d1ed06cced226ce3d8077a7`  
		Last Modified: Wed, 02 Jul 2025 03:10:26 GMT  
		Size: 23.0 MB (22954979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7116e2803008c88f3e0a01f8794d3f2d2cb4ced6873e1cbb1508f0ca3dbfa720`  
		Last Modified: Wed, 02 Jul 2025 04:11:17 GMT  
		Size: 144.6 MB (144646724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40062f2f076600e1a5ca4f053337dde667071b23dd75d99803999e13a422bfef`  
		Last Modified: Wed, 02 Jul 2025 03:10:24 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a023b21e1d611c552afa7c4c7b7112fca2b91d703f849cf0388c5f572c201088`  
		Last Modified: Wed, 02 Jul 2025 03:10:24 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56321d973e092e9730e44dd871f8a84aa5ed1d8e7e3ab21d0a6a6af17f87dcd`  
		Last Modified: Wed, 02 Jul 2025 16:57:54 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b452836297496ae16d6bed9c3549c4b8838fca2681593fcf189cf3787d40f1c1`  
		Last Modified: Wed, 02 Jul 2025 16:57:54 GMT  
		Size: 242.0 KB (241988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969f9368770f18e67d014edc8302013e8f3b9d43633e81f2654a284c82349298`  
		Last Modified: Wed, 02 Jul 2025 16:57:57 GMT  
		Size: 30.2 MB (30185642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4c81909207013ffd6f335d743f6f7bbf8a5fea812305f32280ef3d1b0bd481`  
		Last Modified: Wed, 02 Jul 2025 16:57:51 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:4-jdk17-noble` - unknown; unknown

```console
$ docker pull groovy@sha256:d447832c62daaf18da171e470df18c5725a0d24432eed5d1f2cdda506d005baa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3643638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba23cf2d12d824f165045e7e1cab98b3ba7846876963c891515ab8292ed87524`

```dockerfile
```

-	Layers:
	-	`sha256:7e1b885d454a1dea434c3e3b418ea9c987a3c859dc50e04a2ffc832512a0db9a`  
		Last Modified: Wed, 02 Jul 2025 17:21:10 GMT  
		Size: 3.6 MB (3617182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbdf3621c9d4fdee95d29475ef88a38d37ef814bc1908f18183b5181437226d4`  
		Last Modified: Wed, 02 Jul 2025 17:21:11 GMT  
		Size: 26.5 KB (26456 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:4-jdk17-noble` - linux; arm variant v7

```console
$ docker pull groovy@sha256:a43682b5bfb60f023026b088b228d5ec7cd7e256ef765fcde9137f42d1ae0602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220764629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20600a6e18a5e95f39fded29072aac31fa76cc1a43cb7576ffcef9c5caf64ab`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:88b7ca184cec1707b10b6b543ddfa7abfcacc2605cdd5919877294ff5290aa3e in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9616877c733c9249328ea9bd83a5c8c30e0f9a7af180cac8ffda9034161c2df2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='0db0d6cbe33238f33aa52837b1dc8fc6067b34d206b3e0f9243c7f8c9b9539a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='8a3c859355f898c119d154e4caf867263e0e4c8065a91d63ae10666c19bc1108';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='0823d92d9537fcdd56952abc450d1f9585b4d329f8f884dcb230a2e08db6bf5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        riscv64)          ESUM='1a9a532a6c3e591c5eb72ef875d0f5825961bf8cb0eeea876d7f1e198575ed49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='0033ef81d9c1d30782c5638c20bd7ce3681ebf4b8a68cbc750bb15d613e76e67';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
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
	-	`sha256:149362fdfa6e6a5d9f009b896da3be3172c395ba2287b57d4969f3f46e573055`  
		Last Modified: Fri, 20 Jun 2025 10:02:42 GMT  
		Size: 26.8 MB (26844462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cfaf12232242b87f25dec6171b42156051f497afc56f52d638d96fe75bff4ff`  
		Last Modified: Wed, 02 Jul 2025 10:32:16 GMT  
		Size: 21.4 MB (21380467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899d32690173ee4fc3a964ce395bb5f3707e1be2f1365a1e3cdebf37236cc6cf`  
		Last Modified: Wed, 02 Jul 2025 12:15:40 GMT  
		Size: 142.1 MB (142121653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ac8c05608633c569d9e7a98a67c410af18c4ca14e333c73e9a4ae2c351b690`  
		Last Modified: Wed, 02 Jul 2025 10:32:15 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ec5d566d7157f23f8ac971e1be533694fa7c38bd313ea133d2e8a46f441de5`  
		Last Modified: Wed, 02 Jul 2025 10:32:16 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1bd0046da90be6ee55d9b10fe2b27f594f02e3665f82c8605b07b36c8394d5`  
		Last Modified: Wed, 02 Jul 2025 16:55:27 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b99e6205dc6bb1dbe3d8f8c9419926faf0beea5921bbf1f668a9c1b569d1e4`  
		Last Modified: Wed, 02 Jul 2025 16:55:27 GMT  
		Size: 228.5 KB (228494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904af24c1999d66538fabbad02cebdf51658a3520c2fcf989495896065621723`  
		Last Modified: Wed, 02 Jul 2025 16:55:28 GMT  
		Size: 30.2 MB (30185635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610c0e925a2cf6aa53b307c1fd016a32ffde111da8e4d23c49d1dd01c49a2834`  
		Last Modified: Wed, 02 Jul 2025 16:55:26 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:4-jdk17-noble` - unknown; unknown

```console
$ docker pull groovy@sha256:eaf15f95f31f7ab3c3ec23b9409678ca5084bd85c2fbf818c520baf46e2ea9f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6546a3dc1c126a8c39135a8f96daf27516160102b211d894e302a7aec94d4246`

```dockerfile
```

-	Layers:
	-	`sha256:559789286159daef1b19da6573c79a4e2bd947ba99bbfb1471af18a3e5bedc1f`  
		Last Modified: Wed, 02 Jul 2025 17:21:16 GMT  
		Size: 3.6 MB (3556699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8735a07b075da74005214c1580ef0c78043d736e2b42569161848711d8feda3`  
		Last Modified: Wed, 02 Jul 2025 17:21:16 GMT  
		Size: 26.6 KB (26603 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:4-jdk17-noble` - linux; ppc64le

```console
$ docker pull groovy@sha256:e95f05ea4af851131e98d1ad844bf5b5a22717a2ab09bbd5b831f8d80b0dd223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233175627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68312cc6cbe69fe22e685e118bfc881b7fbf2ceac1305d653e85087ad359c5d7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:fca9cbe6eff6a6982a26900c08b4e2c5a46057e9e5386288e826ac4f2cb17b32 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9616877c733c9249328ea9bd83a5c8c30e0f9a7af180cac8ffda9034161c2df2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='0db0d6cbe33238f33aa52837b1dc8fc6067b34d206b3e0f9243c7f8c9b9539a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='8a3c859355f898c119d154e4caf867263e0e4c8065a91d63ae10666c19bc1108';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='0823d92d9537fcdd56952abc450d1f9585b4d329f8f884dcb230a2e08db6bf5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        riscv64)          ESUM='1a9a532a6c3e591c5eb72ef875d0f5825961bf8cb0eeea876d7f1e198575ed49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='0033ef81d9c1d30782c5638c20bd7ce3681ebf4b8a68cbc750bb15d613e76e67';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
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
	-	`sha256:384c99c6e2b4660fd65fc9823f13a263fb87d4aec3b8f2bd813a7a255bcf46f3`  
		Last Modified: Fri, 20 Jun 2025 09:40:24 GMT  
		Size: 34.3 MB (34321506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1990ab693782ebb597ca9a3a678caa61fcbede21b4aaefc55dc64456936769`  
		Last Modified: Wed, 02 Jul 2025 03:23:39 GMT  
		Size: 24.1 MB (24103453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8199cb24903c2aaa9b6cb5ce65dd1369f792192ce2d2940c36b75367133e77a8`  
		Last Modified: Wed, 02 Jul 2025 06:16:15 GMT  
		Size: 144.3 MB (144289155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871d89e68eb2e5c6245cdc2e1aba3e827444c73f4cdea0122baa417c3b6e6a17`  
		Last Modified: Wed, 02 Jul 2025 03:23:37 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140030445c4bbe89f0898baf4765c19cadd6b435f20b83468654f0b922861754`  
		Last Modified: Wed, 02 Jul 2025 03:23:37 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022c4acc4067f5d26222b631cf3a2d04e3949fedb217fed95d244b989b84d772`  
		Last Modified: Wed, 02 Jul 2025 17:04:35 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cbd1bc1eb1bcc4e88bb6e7f3a63b11c8b6f5318a389ca86c1b8ceb4bbca3a3`  
		Last Modified: Wed, 02 Jul 2025 17:04:35 GMT  
		Size: 272.0 KB (271955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b09a8f619daa9a5f2f2824ab12fca039b3d72c3023807119512a0a6e5f4b04`  
		Last Modified: Wed, 02 Jul 2025 17:04:39 GMT  
		Size: 30.2 MB (30185642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5044f4a3697b3a4e5c093a455cc0d27c6b3e0463bf4e101d918a25f4a45023`  
		Last Modified: Wed, 02 Jul 2025 17:04:35 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:4-jdk17-noble` - unknown; unknown

```console
$ docker pull groovy@sha256:7f2f08ce2036faaeb121302af1da8bb543739659e1cc7dcf1b82c86dd7a3dfaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3691509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:453d12085c4d017dcca563d28c15c437e3afc15d5d2f5d6dc82b9aef0f0331a0`

```dockerfile
```

-	Layers:
	-	`sha256:83d225e2482c2375531f82a90b033d213626f5f3219ae1f0756e4a456dd18317`  
		Last Modified: Wed, 02 Jul 2025 17:21:21 GMT  
		Size: 3.7 MB (3664980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a7022465d58e78518104fb4d14ec3f78154059c69b8654a407d6b2d1c1a32d6`  
		Last Modified: Wed, 02 Jul 2025 17:21:22 GMT  
		Size: 26.5 KB (26529 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:4-jdk17-noble` - linux; riscv64

```console
$ docker pull groovy@sha256:8b2c9aaace508761f66130ae7246189b45a62661461c99c24d6f276dcf1fcec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 MB (220030882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eced4b3b6a1023c5621734e2334db00410efe4ec1a579a064fa98349a21a67aa`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:202c5a7a84e813495c089800398f2ba18952221717db2c10e042ce4179ee6fc0 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9616877c733c9249328ea9bd83a5c8c30e0f9a7af180cac8ffda9034161c2df2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='0db0d6cbe33238f33aa52837b1dc8fc6067b34d206b3e0f9243c7f8c9b9539a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='8a3c859355f898c119d154e4caf867263e0e4c8065a91d63ae10666c19bc1108';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='0823d92d9537fcdd56952abc450d1f9585b4d329f8f884dcb230a2e08db6bf5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        riscv64)          ESUM='1a9a532a6c3e591c5eb72ef875d0f5825961bf8cb0eeea876d7f1e198575ed49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='0033ef81d9c1d30782c5638c20bd7ce3681ebf4b8a68cbc750bb15d613e76e67';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
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
	-	`sha256:4ccdff8fdb11e14b8e0dab6804aeebce5855635c68b20f199dcf0efcd9b4c462`  
		Last Modified: Wed, 02 Jul 2025 01:17:14 GMT  
		Size: 31.0 MB (30951024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f307aa91f43f6bbfb083211438fde83a6415758b82a4c332bd7dd89aec8e99f0`  
		Last Modified: Wed, 02 Jul 2025 03:30:36 GMT  
		Size: 20.1 MB (20140446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e155206757d593b51cc828aae413b3134d21a605888f369c6558e96b4c989e1`  
		Last Modified: Wed, 02 Jul 2025 06:16:55 GMT  
		Size: 138.5 MB (138496014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda3360286ad8073fe54aa6a8dbaa77a5fdecb6625bd6acede9bb97beb4632e4`  
		Last Modified: Wed, 02 Jul 2025 03:30:34 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32dc6966f7c3bd05314e8db30a9ff60d4c908f89aebef592a52956764636704`  
		Last Modified: Wed, 02 Jul 2025 03:30:33 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a7d2fdcae2b6691945f6b5bf79e0862b4e61fcf873f3be4b8023cd551ee7c5`  
		Last Modified: Wed, 02 Jul 2025 17:03:24 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310d01d6b58b43d3f17972f783c78fbe1edfd7ebb890a00790882a85ab6455a7`  
		Last Modified: Wed, 02 Jul 2025 17:03:24 GMT  
		Size: 253.8 KB (253847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a6f9c4ecf0dec4abc8ab1785cf79ce6cdab43c0cbf7582a090649377baaca1`  
		Last Modified: Wed, 02 Jul 2025 17:03:26 GMT  
		Size: 30.2 MB (30185629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e206bf4aad59d3dba3c386a52549893b792a585884d5b4b974c3b3b058a9710c`  
		Last Modified: Wed, 02 Jul 2025 17:03:25 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:4-jdk17-noble` - unknown; unknown

```console
$ docker pull groovy@sha256:3c7be5ac268331d67cc89fad0115713df3cb453b3b3fbbdf29e8076aaac19bfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3749066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7215ea5a1380ba08fad44e679ae9fe3e9aa226edd4cdf7a91bcdd83411ea9873`

```dockerfile
```

-	Layers:
	-	`sha256:942dc6d4d415c7564cb5b605235d9b5347eaa6b83d7463058a9c687f3c11dd91`  
		Last Modified: Wed, 02 Jul 2025 17:21:26 GMT  
		Size: 3.7 MB (3722536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4efcfcd0b7952e4313c93f12bf04f23280186d5ff0951d6f28ee843605fb9794`  
		Last Modified: Wed, 02 Jul 2025 17:21:27 GMT  
		Size: 26.5 KB (26530 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:4-jdk17-noble` - linux; s390x

```console
$ docker pull groovy@sha256:77675e13bdab60b3f72a4c3b43267cb2ced89946640e04ec796fb44abf173383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.2 MB (217181260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e22d230e9a2aa28769c2f38fdb0145efaa43503770170e0895d5b64c59809f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:80b0b0c2a08a762cf6a520d8428a5c769c29e72f4a51630adb2231f2816c50c4 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9616877c733c9249328ea9bd83a5c8c30e0f9a7af180cac8ffda9034161c2df2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='0db0d6cbe33238f33aa52837b1dc8fc6067b34d206b3e0f9243c7f8c9b9539a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='8a3c859355f898c119d154e4caf867263e0e4c8065a91d63ae10666c19bc1108';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='0823d92d9537fcdd56952abc450d1f9585b4d329f8f884dcb230a2e08db6bf5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        riscv64)          ESUM='1a9a532a6c3e591c5eb72ef875d0f5825961bf8cb0eeea876d7f1e198575ed49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='0033ef81d9c1d30782c5638c20bd7ce3681ebf4b8a68cbc750bb15d613e76e67';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
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
	-	`sha256:30d64ca13d9d94eb48bf3fece3e38a4e60931d72f1a8c633dec981e43a0515a4`  
		Last Modified: Fri, 20 Jun 2025 09:40:24 GMT  
		Size: 29.9 MB (29925630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f20e5bf93e1bfddd9097b0ff58228842e801f91f2b972d3a3308109367dee4`  
		Last Modified: Wed, 02 Jul 2025 04:19:29 GMT  
		Size: 22.1 MB (22132438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3636a63d95f0ce5b400df98681c871188b9de0e5574d717f0d6bab59240fdbce`  
		Last Modified: Wed, 02 Jul 2025 06:17:30 GMT  
		Size: 134.7 MB (134681147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69430f396324a2f30f2312f97ed07a2e793797e90d5e9dfb19f276a6f0af49bb`  
		Last Modified: Wed, 02 Jul 2025 04:19:27 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96cd9efedc0dc65cf9345899c568fdb0660526ce1337bc8dcf2ffe55465fc68`  
		Last Modified: Wed, 02 Jul 2025 04:19:27 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6f9f9a5c051ea70e112927ecfe039278ccfe93929bf03539ca6a9e95c81df4`  
		Last Modified: Wed, 02 Jul 2025 16:56:32 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad4e86e86c504c6b25e83132cd6202f22f788cf9ebabedd65abdf4612d35adb`  
		Last Modified: Wed, 02 Jul 2025 16:56:33 GMT  
		Size: 252.5 KB (252486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6230482e0efc2445db9a8fe1f9331f8bc08960de637571340789d75d136420b2`  
		Last Modified: Wed, 02 Jul 2025 16:56:36 GMT  
		Size: 30.2 MB (30185640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cd3a97cc7ec0e18e2f8816ea51a5543e17466816e03308bd980408b794cfc3`  
		Last Modified: Wed, 02 Jul 2025 16:56:32 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:4-jdk17-noble` - unknown; unknown

```console
$ docker pull groovy@sha256:719b4f362994ff58ff6530241b9d5e266fbef91cf2dccd2796c49de170f34447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3589451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef52329996e62055194bd4ea53a1a06d623c6fe93950e4b88e9e846e09459e0`

```dockerfile
```

-	Layers:
	-	`sha256:000405502ac1781e75fe2c0082a714bf9fc071c47590e565e80147483ea2fb7d`  
		Last Modified: Wed, 02 Jul 2025 17:21:31 GMT  
		Size: 3.6 MB (3562995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc99bdefcf94190957481bf44e430e600d39693704e3c4bbf35bf120bc7cffa7`  
		Last Modified: Wed, 02 Jul 2025 17:21:31 GMT  
		Size: 26.5 KB (26456 bytes)  
		MIME: application/vnd.in-toto+json
