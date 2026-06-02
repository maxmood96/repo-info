## `groovy:3-noble`

```console
$ docker pull groovy@sha256:2d22e2653edf7a63def1e90d675cda7982e9c9c73c2ba9c0a114a93a2212aafd
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

### `groovy:3-noble` - linux; amd64

```console
$ docker pull groovy@sha256:15db997e04188a77380095e6b199870b64907a2286fd45da30034d09245b5d46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256159378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff6a9022158c45bfbbc87ab0f41a8937bc2f6c7d7eb42ea755e7a36add84a92d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

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
# Thu, 07 May 2026 23:59:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 May 2026 23:59:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 23:59:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 07 May 2026 23:59:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 May 2026 23:59:55 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 08 May 2026 00:00:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        riscv64)          ESUM='40c6862e6aff63fe9a03856ba0506531b516a17bdb5018464e9006ea7f0f5fe4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 08 May 2026 00:00:03 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 00:00:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 00:00:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 00:00:03 GMT
CMD ["jshell"]
# Fri, 08 May 2026 00:13:43 GMT
CMD ["groovysh"]
# Fri, 08 May 2026 00:13:43 GMT
ENV GROOVY_HOME=/opt/groovy
# Fri, 08 May 2026 00:13:43 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to groovy"     && groupmod --new-name groovy ubuntu     && mkdir /home/groovy     && usermod --login groovy --home /home/groovy --groups groovy ubuntu     && chown groovy /home/groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Fri, 08 May 2026 00:13:43 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Fri, 08 May 2026 00:13:43 GMT
WORKDIR /home/groovy
# Fri, 08 May 2026 00:13:47 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 00:13:47 GMT
ENV GROOVY_VERSION=3.0.25
# Fri, 08 May 2026 00:14:41 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Fri, 08 May 2026 00:14:41 GMT
USER 1000:1000
# Fri, 08 May 2026 00:14:41 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117face21d4999b98333e39f0370ceccc72ca68ac796e6637469537582d5a61f`  
		Last Modified: Fri, 08 May 2026 00:00:22 GMT  
		Size: 23.0 MB (22966995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510ce46061a4b99d147c0b3deedae89dcd096b6c3e74b533cb783d18f9bab2d6`  
		Last Modified: Fri, 08 May 2026 00:00:25 GMT  
		Size: 158.2 MB (158171738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725f3390c4115f24528fbb7be27b2f2b4fc47a10c12ea80ca4d6bbd632155e54`  
		Last Modified: Fri, 08 May 2026 00:00:20 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee78dd6a47528af4f12330b07b6f941bbd217e6278e89ba9875a41a50def41fa`  
		Last Modified: Fri, 08 May 2026 00:00:22 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363575efe9e0a1041c13ee1be06753f02db35b68cc274d776becf31d523c57ee`  
		Last Modified: Fri, 08 May 2026 00:14:50 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9203bd4ec8b5d5660f3f9883ec5b89ae78738475f49a6a42d3e171da97670f`  
		Last Modified: Fri, 08 May 2026 00:14:50 GMT  
		Size: 242.1 KB (242114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a03205aa300b9434ea1c1df1e708def12c6a707dbeb68d4a704692afcbdfc66`  
		Last Modified: Fri, 08 May 2026 00:14:52 GMT  
		Size: 45.0 MB (45041638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f9e9a7f3efc98703e34a8f1ab1e2102242cb1896050401ec8db21feb5c7de8`  
		Last Modified: Fri, 08 May 2026 00:14:51 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:3-noble` - unknown; unknown

```console
$ docker pull groovy@sha256:b1016544beb4e83131d7d8c8f7d46f82c7d6e7aa442ba01e0a6d5685f6ecdf24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3695573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be12286a33610b01f53a4ce54f328fb126d909e9b4cf1db1031bec1724e38474`

```dockerfile
```

-	Layers:
	-	`sha256:1f8eba72fc67eae5a80f1afb44265a6395027a64c7367b7f38acf6d189b6e40f`  
		Last Modified: Fri, 08 May 2026 00:14:51 GMT  
		Size: 3.7 MB (3666110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:792ffb980552c8b6d50697144eed580316baaefbd0186e59071f7edbdeb2c028`  
		Last Modified: Fri, 08 May 2026 00:14:50 GMT  
		Size: 29.5 KB (29463 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:3-noble` - linux; arm64 variant v8

```console
$ docker pull groovy@sha256:58c2887bbcd439b2ebc3a53f810e552df4665682a865f1dbad8dd35dddb4a55a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.8 MB (254809242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c6db5dedb184e0fab53e8a49b3a2f21c3e4de115f223dfb548b3a32ba0fc93c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

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
# Thu, 07 May 2026 23:59:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 May 2026 23:59:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 23:59:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 07 May 2026 23:59:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 May 2026 23:59:34 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Thu, 07 May 2026 23:59:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        riscv64)          ESUM='40c6862e6aff63fe9a03856ba0506531b516a17bdb5018464e9006ea7f0f5fe4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 07 May 2026 23:59:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 07 May 2026 23:59:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 07 May 2026 23:59:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 07 May 2026 23:59:42 GMT
CMD ["jshell"]
# Fri, 08 May 2026 00:16:57 GMT
CMD ["groovysh"]
# Fri, 08 May 2026 00:16:57 GMT
ENV GROOVY_HOME=/opt/groovy
# Fri, 08 May 2026 00:16:57 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to groovy"     && groupmod --new-name groovy ubuntu     && mkdir /home/groovy     && usermod --login groovy --home /home/groovy --groups groovy ubuntu     && chown groovy /home/groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Fri, 08 May 2026 00:16:57 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Fri, 08 May 2026 00:16:57 GMT
WORKDIR /home/groovy
# Fri, 08 May 2026 00:17:04 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 00:17:04 GMT
ENV GROOVY_VERSION=3.0.25
# Fri, 08 May 2026 00:18:28 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Fri, 08 May 2026 00:18:28 GMT
USER 1000:1000
# Fri, 08 May 2026 00:18:28 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84fa2a514a5307491f5de1145b4702ac1bbd0e4e8c13ab659b3326714f6ec4b3`  
		Last Modified: Fri, 08 May 2026 00:00:00 GMT  
		Size: 24.2 MB (24172696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce21ee5c0e78f9798c236abe913341fbf00efbf30ffc203c0d0882e4a39d6f9c`  
		Last Modified: Fri, 08 May 2026 00:00:04 GMT  
		Size: 156.5 MB (156473515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c774b8a7e68a4d73adc475392932ee24fa0bffa64087021207a11e6dad3d0043`  
		Last Modified: Thu, 07 May 2026 23:59:59 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6c40c3516540503092334eba702c60474cf1e29c9c196eef302b94935ce434`  
		Last Modified: Thu, 07 May 2026 23:59:59 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d26746c5f04952c69a27c078d40cc734c37043fdde46617d6817978965c3c6b`  
		Last Modified: Fri, 08 May 2026 00:18:40 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6e1d874cb5669af8ea286400d05d4526bd186f045ca48e28d5c3ae1da687a0`  
		Last Modified: Fri, 08 May 2026 00:18:40 GMT  
		Size: 241.7 KB (241710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163784cbe6917bd22d6d15ee8efffd22098914c5d8256e86d620708184335879`  
		Last Modified: Fri, 08 May 2026 00:18:42 GMT  
		Size: 45.0 MB (45041617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f1c3bd750364e43d9d278d5b2363ec32e6da74e2025810f6720dffa9467aa2`  
		Last Modified: Fri, 08 May 2026 00:18:40 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:3-noble` - unknown; unknown

```console
$ docker pull groovy@sha256:eebc06214fbe6b1998113dddf85a19f3e654c54fbf6b1cb7d121c849f1646c68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3827579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8373743dfe70fa3041d3e21bfa7de4801bd13c31ccaac9b717f2b79ed082361`

```dockerfile
```

-	Layers:
	-	`sha256:9ecf481d5e49e40181e7e6b43020d9c3008b9da4ccf5510c6e758af2e2faf6ab`  
		Last Modified: Fri, 08 May 2026 00:18:40 GMT  
		Size: 3.8 MB (3797799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3347b31b18fa96ec2ac6b17555860e6b667165185f0b43efbf4469186753e34`  
		Last Modified: Fri, 08 May 2026 00:18:39 GMT  
		Size: 29.8 KB (29780 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:3-noble` - linux; ppc64le

```console
$ docker pull groovy@sha256:576a3b55860b567f1ba762b6e12fecba4a786fa5be5493791ae9cabc3c002345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.1 MB (262073630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe230f233e767d06906df66a937f366c875f7ad5f211a0f87439dda1aab7ce3d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Wed, 20 May 2026 01:37:26 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:26 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:29 GMT
ADD file:25dad72762cb0d82bbf57f17b8713b1ca4d35e813d99be37e61090f10acd5d92 in / 
# Wed, 20 May 2026 01:37:30 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:12:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:12:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:12:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:12:24 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:12:24 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 02 Jun 2026 08:12:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        riscv64)          ESUM='40c6862e6aff63fe9a03856ba0506531b516a17bdb5018464e9006ea7f0f5fe4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:12:51 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:12:51 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:12:51 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 08:12:51 GMT
CMD ["jshell"]
# Tue, 02 Jun 2026 09:18:32 GMT
CMD ["groovysh"]
# Tue, 02 Jun 2026 09:18:32 GMT
ENV GROOVY_HOME=/opt/groovy
# Tue, 02 Jun 2026 09:18:32 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to groovy"     && groupmod --new-name groovy ubuntu     && mkdir /home/groovy     && usermod --login groovy --home /home/groovy --groups groovy ubuntu     && chown groovy /home/groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Tue, 02 Jun 2026 09:18:32 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Tue, 02 Jun 2026 09:18:32 GMT
WORKDIR /home/groovy
# Tue, 02 Jun 2026 09:18:38 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:18:38 GMT
ENV GROOVY_VERSION=3.0.25
# Tue, 02 Jun 2026 09:56:30 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Tue, 02 Jun 2026 09:56:30 GMT
USER 1000:1000
# Tue, 02 Jun 2026 09:56:32 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c1670fe2f067637ded122a0663c456ca6091e763c878866bd1996f0f3852f7`  
		Last Modified: Tue, 02 Jun 2026 08:13:11 GMT  
		Size: 24.1 MB (24096040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f99ed93216c409ce80de40299956c411fe8d5580c1e4effe74d64e94d62449`  
		Last Modified: Tue, 02 Jun 2026 08:13:29 GMT  
		Size: 158.3 MB (158345909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038eb3036bf5ea5a468b49c2e5dd73daa411d2c8d6810020e7332228fd980030`  
		Last Modified: Tue, 02 Jun 2026 08:13:24 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64bbf3baca588841b50b9d867afee68ac3fa864c9ec5ee9c6ad293dacbfd78d`  
		Last Modified: Tue, 02 Jun 2026 08:13:25 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4081d47c3c726dc8a0ad08b296d341ff14f191320b82b92e19e28cf8af7a41cf`  
		Last Modified: Tue, 02 Jun 2026 09:28:41 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b6aa94580ca54d32643e2c8c8f64c60ca3dd2df2960fefe74a15dc1f3de35d`  
		Last Modified: Tue, 02 Jun 2026 09:28:41 GMT  
		Size: 272.0 KB (272021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb78f4fd596889658e216a8b07f572def4cd9153267bcdc5be3e059e77fa4434`  
		Last Modified: Tue, 02 Jun 2026 09:56:53 GMT  
		Size: 45.0 MB (45041636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5300cc01b762d4a4877310a5bbf711262ca73844a6e582be40d0f396d18ba1b`  
		Last Modified: Tue, 02 Jun 2026 09:56:51 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:3-noble` - unknown; unknown

```console
$ docker pull groovy@sha256:7cc74b63722e2ee9c958c634f0785dadc9f2d823e891697a240553dcf451397f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3743577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d58a1e14a35cdca1b9575c7b7df37a963af5bd63e5a2eea8251d905e9465354`

```dockerfile
```

-	Layers:
	-	`sha256:e4e88f92a4b2d0cb34b6213a1e8aabfd4ebb8092672a321fc1d8e062f73b81dd`  
		Last Modified: Tue, 02 Jun 2026 09:56:51 GMT  
		Size: 3.7 MB (3713980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5c65bc372263b23fd9ac895547721561eb0225ce00828241e839cd07b02f9fe`  
		Last Modified: Tue, 02 Jun 2026 09:56:51 GMT  
		Size: 29.6 KB (29597 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:3-noble` - linux; riscv64

```console
$ docker pull groovy@sha256:74ace26a7d3163851c6c9062b58755f1fc932301fbb83f7e7bdeef89d84de3e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.9 MB (253887131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741fce44d6311a8442ddc905d389c7ec1a7f2d49cd38ffd5a923b8a0be889f4d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

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
# Thu, 16 Apr 2026 16:46:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 16:46:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 16:46:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Apr 2026 16:46:37 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Apr 2026 16:46:37 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Sat, 09 May 2026 05:35:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        riscv64)          ESUM='40c6862e6aff63fe9a03856ba0506531b516a17bdb5018464e9006ea7f0f5fe4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 09 May 2026 05:36:09 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 09 May 2026 05:36:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 09 May 2026 05:36:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 09 May 2026 05:36:10 GMT
CMD ["jshell"]
# Mon, 11 May 2026 02:03:21 GMT
CMD ["groovysh"]
# Mon, 11 May 2026 02:03:21 GMT
ENV GROOVY_HOME=/opt/groovy
# Mon, 11 May 2026 02:03:21 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to groovy"     && groupmod --new-name groovy ubuntu     && mkdir /home/groovy     && usermod --login groovy --home /home/groovy --groups groovy ubuntu     && chown groovy /home/groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Mon, 11 May 2026 02:03:21 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Mon, 11 May 2026 02:03:21 GMT
WORKDIR /home/groovy
# Mon, 11 May 2026 02:04:07 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 02:04:07 GMT
ENV GROOVY_VERSION=3.0.25
# Mon, 11 May 2026 02:18:49 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Mon, 11 May 2026 02:18:49 GMT
USER 1000:1000
# Mon, 11 May 2026 02:18:59 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:a7f0c74374451005259fe6b1b7ef3185055f2b6c419b5ba0ae8e4f55b1e1c31d`  
		Last Modified: Fri, 10 Apr 2026 09:34:45 GMT  
		Size: 31.0 MB (30965327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb43b647117c9f43692f378d47bfa7800d85b1756ada8ad0318423a33c02a7d`  
		Last Modified: Thu, 16 Apr 2026 16:51:32 GMT  
		Size: 20.2 MB (20151745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7744a8e7488dc516bb6d47c7ea19cc1cc8087874207376f53fc91d01f640f2c`  
		Last Modified: Sat, 09 May 2026 05:40:31 GMT  
		Size: 157.5 MB (157470542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a7b1609f38192706f02657d6f791cce4d7b5ded85109015497bda93efe8371`  
		Last Modified: Sat, 09 May 2026 05:40:05 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3937815dcfefc380c6a8d84f2cb4791cbc731324ff9c24383b54c07f79707907`  
		Last Modified: Sat, 09 May 2026 05:40:06 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f044a99227643839ae34343d79353120a950049b6a40d76826e4f82b333244`  
		Last Modified: Mon, 11 May 2026 02:06:55 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021e6c3df33610a1665f778187c3cf5bf7237a81f00b071ea196810d986c25a5`  
		Last Modified: Mon, 11 May 2026 02:06:55 GMT  
		Size: 253.9 KB (253948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81993c87b4480ef71c2904a55f88ba43893740aee20cd8dc73ec128429081c5b`  
		Last Modified: Mon, 11 May 2026 02:21:45 GMT  
		Size: 45.0 MB (45041645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e931431a543e3eb2811262723e281e87a873899909e2b90aeab01e9bcb952f70`  
		Last Modified: Mon, 11 May 2026 02:21:37 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:3-noble` - unknown; unknown

```console
$ docker pull groovy@sha256:a8267b1fdb53328c9426ac810206112f54564a49faa3665a8cdf5bded20c1132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3803038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3301ab879a9ced1958988e9d48e8e5a818141bff1bbc0d8f436153ed04ac205`

```dockerfile
```

-	Layers:
	-	`sha256:5c2799f7b4b89e02223996cc99072e0cff45af37096ae5ca9bd4a295a20a5c8d`  
		Last Modified: Mon, 11 May 2026 02:21:38 GMT  
		Size: 3.8 MB (3773441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f48f6e8b1a77b588f425b8410dfe792e64b454f39f64f57c7034aa37ed1cc87`  
		Last Modified: Mon, 11 May 2026 02:21:37 GMT  
		Size: 29.6 KB (29597 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:3-noble` - linux; s390x

```console
$ docker pull groovy@sha256:214785c64e6990bd8b6e5f6ad68fc4ed1586f0a087a3e23f1433db6a1a695398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.7 MB (244740578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abce97eff39ed2a40db71a2fb7fc3351a90782102e1b4e0395b3e1045cce3ce9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Wed, 20 May 2026 01:37:09 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:11 GMT
ADD file:b574b1e436c2db4e4d66f69c75e47a9aebf0da1ad375147eb2c0b7ff76c6ab7e in / 
# Wed, 20 May 2026 01:37:11 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:11:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:11:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:11:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:11:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:11:03 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 02 Jun 2026 08:11:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        riscv64)          ESUM='40c6862e6aff63fe9a03856ba0506531b516a17bdb5018464e9006ea7f0f5fe4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:11:09 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:11:09 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:11:09 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 08:11:09 GMT
CMD ["jshell"]
# Tue, 02 Jun 2026 09:14:07 GMT
CMD ["groovysh"]
# Tue, 02 Jun 2026 09:14:07 GMT
ENV GROOVY_HOME=/opt/groovy
# Tue, 02 Jun 2026 09:14:07 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to groovy"     && groupmod --new-name groovy ubuntu     && mkdir /home/groovy     && usermod --login groovy --home /home/groovy --groups groovy ubuntu     && chown groovy /home/groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Tue, 02 Jun 2026 09:14:07 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Tue, 02 Jun 2026 09:14:07 GMT
WORKDIR /home/groovy
# Tue, 02 Jun 2026 09:14:11 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:14:11 GMT
ENV GROOVY_VERSION=3.0.25
# Tue, 02 Jun 2026 09:30:15 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Tue, 02 Jun 2026 09:30:15 GMT
USER 1000:1000
# Tue, 02 Jun 2026 09:30:16 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:c8ebd0a624851e8502e41ee64db2b6a45537554969784d82ebbc91c905cbc2ef`  
		Last Modified: Wed, 20 May 2026 02:16:00 GMT  
		Size: 29.9 MB (29912835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161ab83b783a70ac7e335f06f868087878d7a3e67ada1ea2ed592d86b5ed002d`  
		Last Modified: Tue, 02 Jun 2026 08:11:34 GMT  
		Size: 22.1 MB (22130533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5ba65f654f079fa940ba38ee6ace3fac70039f845c9b29befdb2d4219f8e9a`  
		Last Modified: Tue, 02 Jun 2026 08:11:37 GMT  
		Size: 147.4 MB (147398857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76a6cebb1e74b0c202e5830c582ceb4a363c946651341977e28df6e3c678e23`  
		Last Modified: Tue, 02 Jun 2026 08:11:33 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43a9502fe3bc0ed260d6f31186168220db755450056002c0f96394792b89dc0`  
		Last Modified: Tue, 02 Jun 2026 08:11:33 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f23537f9fcc5726715141fbd732d19ff279e7d37176ca72fb093ae7d9b3d915`  
		Last Modified: Tue, 02 Jun 2026 09:21:42 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c5b90f9c554fc4f08b72e9b34931f76a0360b7b2c771f2d85e7685f7b45e67`  
		Last Modified: Tue, 02 Jun 2026 09:21:42 GMT  
		Size: 252.8 KB (252812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c496b021c52c51ca8c313c040eb448a5c7f690041287eaeaba82362df2efe819`  
		Last Modified: Tue, 02 Jun 2026 09:30:32 GMT  
		Size: 45.0 MB (45041620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b506a506dae50ae057f06ca61c0ae577ab21c45a4b01391e943b8f90e6f9cba4`  
		Last Modified: Tue, 02 Jun 2026 09:30:31 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:3-noble` - unknown; unknown

```console
$ docker pull groovy@sha256:bf3ce98c0e18d9efd87cb7ec23766b25bb9c5788d7415e4d665fd2b6927f14a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2735c3de83c674cf5ef626943e9068f80baf52c30c6049efc1ecdbc1d2bd0c9`

```dockerfile
```

-	Layers:
	-	`sha256:941d973d4851afb49a936daea8bf1f2d53969486097a7bb7b192bb7124353e91`  
		Last Modified: Tue, 02 Jun 2026 09:30:31 GMT  
		Size: 3.6 MB (3611939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:681cf4f65f1a45b96f98d1ff148e5001719a1a2529c2e63fda5e940d6615e357`  
		Last Modified: Tue, 02 Jun 2026 09:30:31 GMT  
		Size: 29.5 KB (29463 bytes)  
		MIME: application/vnd.in-toto+json
