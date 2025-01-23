## `groovy:jdk21-jammy`

```console
$ docker pull groovy@sha256:d2702b0c4049cd7f675a1fd0c07d2aad40d6c6aad1110481cb1b972eccfd0ed7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `groovy:jdk21-jammy` - linux; amd64

```console
$ docker pull groovy@sha256:7a2b28df17515013ebf049eb2fe2b4744fdfb93c272efe352c903cd423d3616d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.0 MB (238041224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae1abad79de7e79a0f5ccd3ddc7888c3409987b353b6f339932792982fd10612`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Sat, 09 Nov 2024 02:52:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 Nov 2024 02:52:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Nov 2024 02:52:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 09 Nov 2024 02:52:58 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 Nov 2024 02:52:58 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Sat, 09 Nov 2024 02:52:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='3c654d98404c073b8a7e66bffb27f4ae3e7ede47d13284c132d40a83144bfd8c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_x64_linux_hotspot_21.0.5_11.tar.gz';          ;;        arm64)          ESUM='6482639ed9fd22aa2e704cc366848b1b3e1586d2bf1213869c43e80bca58fe5c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.5_11.tar.gz';          ;;        ppc64el)          ESUM='3c6f4c358facfb6c19d90faf02bfe0fc7512d6b0e80ac18146bbd7e0d01deeef';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.5_11.tar.gz';          ;;        s390x)          ESUM='51a7ca42cc2e8cb5f3e7a326c28912ee84ff0791a1ca66650a8c53af07510a7c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 09 Nov 2024 02:52:58 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 09 Nov 2024 02:52:58 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 09 Nov 2024 02:52:58 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 09 Nov 2024 02:52:58 GMT
CMD ["jshell"]
# Sat, 09 Nov 2024 02:52:58 GMT
CMD ["groovysh"]
# Sat, 09 Nov 2024 02:52:58 GMT
ENV GROOVY_HOME=/opt/groovy
# Sat, 09 Nov 2024 02:52:58 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Sat, 09 Nov 2024 02:52:58 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Sat, 09 Nov 2024 02:52:58 GMT
WORKDIR /home/groovy
# Sat, 09 Nov 2024 02:52:58 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Sat, 09 Nov 2024 02:52:58 GMT
ENV GROOVY_VERSION=4.0.24
# Sat, 09 Nov 2024 02:52:58 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Sat, 09 Nov 2024 02:52:58 GMT
USER 1000:1000
# Sat, 09 Nov 2024 02:52:58 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff6889381574881f25a2c4711dfef10388ff02f47974301a6613cb2449709c7`  
		Last Modified: Wed, 22 Jan 2025 18:28:13 GMT  
		Size: 20.7 MB (20693776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d58567494e63efa6f164ddc431f30d7c047f02d2bf58de85d07294f0c2428dc`  
		Last Modified: Wed, 22 Jan 2025 18:28:15 GMT  
		Size: 157.6 MB (157585504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be9d5d5d7e5d8f5738d840a2e1adf5dcbcf619e7ca85a30f95243522b6930fb`  
		Last Modified: Wed, 22 Jan 2025 18:28:13 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0da6393fd47cfa1a49b58091b48da741160efaefb8c68549b15e6d93ed3547`  
		Last Modified: Wed, 22 Jan 2025 18:28:01 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a61bcd30020a0ab41dad797d5e06a0d4684ac43b7ba050291ea2f12946f0c6`  
		Last Modified: Wed, 22 Jan 2025 19:36:00 GMT  
		Size: 4.3 KB (4334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be4929d92a856553319063435417c54f801d1fe534c0fe97aa95c9b6ac9fc7e`  
		Last Modified: Wed, 22 Jan 2025 19:36:01 GMT  
		Size: 247.0 KB (246958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40db0d2fee237b7ff4cdab934dc6c19a7bd5e1b54c0e6736ca66814ce35c0d56`  
		Last Modified: Wed, 22 Jan 2025 19:36:02 GMT  
		Size: 30.0 MB (29972352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d722af0b9224938e3964ffcb2e820470a58989f238a42a6a18cbb979d75a919`  
		Last Modified: Wed, 22 Jan 2025 19:36:00 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk21-jammy` - unknown; unknown

```console
$ docker pull groovy@sha256:21d96cc96fe429cc9201828f1824c546e36db1fb7583690ac506c643b967b475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4069254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc0f199a394a1bcc776610e079574c06b2df08c6a78c337a3c03780ff83a161`

```dockerfile
```

-	Layers:
	-	`sha256:d6f9fffd21fc58f579186fada398bfdade6bb4a36fdaa9d9c68d16c3e07e5bb6`  
		Last Modified: Wed, 22 Jan 2025 19:36:00 GMT  
		Size: 4.0 MB (4043641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b34ed19842037214fc597524c8ebad1cd24e45b460fc02efbb8c20119a3c499`  
		Last Modified: Wed, 22 Jan 2025 19:36:00 GMT  
		Size: 25.6 KB (25613 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:jdk21-jammy` - linux; arm64 variant v8

```console
$ docker pull groovy@sha256:9dfabd11c7bc1cd10abc3a13352d023447ecd1e1b6c7ba98498644c50eb391cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.5 MB (235458321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c915c84b19bada5717f6c82c7159b4cb853f60e58d2a29e24031663ced8f75aa`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='3c654d98404c073b8a7e66bffb27f4ae3e7ede47d13284c132d40a83144bfd8c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_x64_linux_hotspot_21.0.5_11.tar.gz';          ;;        arm64)          ESUM='6482639ed9fd22aa2e704cc366848b1b3e1586d2bf1213869c43e80bca58fe5c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.5_11.tar.gz';          ;;        ppc64el)          ESUM='3c6f4c358facfb6c19d90faf02bfe0fc7512d6b0e80ac18146bbd7e0d01deeef';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.5_11.tar.gz';          ;;        s390x)          ESUM='51a7ca42cc2e8cb5f3e7a326c28912ee84ff0791a1ca66650a8c53af07510a7c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["jshell"]
# Sat, 09 Nov 2024 02:52:58 GMT
CMD ["groovysh"]
# Sat, 09 Nov 2024 02:52:58 GMT
ENV GROOVY_HOME=/opt/groovy
# Sat, 09 Nov 2024 02:52:58 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Sat, 09 Nov 2024 02:52:58 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Sat, 09 Nov 2024 02:52:58 GMT
WORKDIR /home/groovy
# Sat, 09 Nov 2024 02:52:58 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Sat, 09 Nov 2024 02:52:58 GMT
ENV GROOVY_VERSION=4.0.24
# Sat, 09 Nov 2024 02:52:58 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Sat, 09 Nov 2024 02:52:58 GMT
USER 1000:1000
# Sat, 09 Nov 2024 02:52:58 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd1f22a9dd7228be27e706b25f1b3429d02ca813b8c0e0263edaa65a05911c8`  
		Last Modified: Thu, 24 Oct 2024 01:09:29 GMT  
		Size: 22.1 MB (22072026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769c454e4083771448c1ca566548905f47f1628bcd3d645e5486a44156028a57`  
		Last Modified: Thu, 24 Oct 2024 01:15:08 GMT  
		Size: 155.8 MB (155805359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6fa8b0f1fe6e6b10b29a94eda5f2f8685322a6a9a25fcdf3aa25f40dd28d31`  
		Last Modified: Thu, 24 Oct 2024 01:15:04 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795abbf1e836cd5e5bbe1b004ef8374ccd5b8067cf7902905f2776353abd5423`  
		Last Modified: Thu, 24 Oct 2024 01:15:04 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1844f73523b3eb3b194bef77af3751ef9e8505d6b3429706ade5e90759b684da`  
		Last Modified: Mon, 11 Nov 2024 19:01:28 GMT  
		Size: 4.3 KB (4338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960b01f0083a163bf772781118d8a6c806f2e615d028b766316f23a4fbdbb57c`  
		Last Modified: Mon, 11 Nov 2024 19:01:29 GMT  
		Size: 243.3 KB (243327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa84f401d0e802db4cbe9d7d3bc410ddbbc3f85b67c92679447249c29bbbf1a`  
		Last Modified: Mon, 11 Nov 2024 19:01:30 GMT  
		Size: 30.0 MB (29972329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a669ee97d2e03b0fb7690e6325ecb5117c8234d60fea7d515bd745e50b406b5c`  
		Last Modified: Mon, 11 Nov 2024 19:01:29 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk21-jammy` - unknown; unknown

```console
$ docker pull groovy@sha256:7d897a3cf0666d76d541f7799027f0fc3ec4861217aba8556181aa834819131d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4169751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b09cf3b7eb54a7183d7e8a7343bdc2d27be9a3e94f8b2d9ea5af6640602e84`

```dockerfile
```

-	Layers:
	-	`sha256:5e9346936055069c14079315f6a93af282f07122391f7f11b45fb7441e583ef6`  
		Last Modified: Mon, 11 Nov 2024 19:01:29 GMT  
		Size: 4.1 MB (4143966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccdcdaa59f412442132df41e21f0e1bc681bc1bd475d45005fa43708b425824d`  
		Last Modified: Mon, 11 Nov 2024 19:01:28 GMT  
		Size: 25.8 KB (25785 bytes)  
		MIME: application/vnd.in-toto+json
