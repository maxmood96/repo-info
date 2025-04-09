## `groovy:jdk11-jammy`

```console
$ docker pull groovy@sha256:15bfcdee90d5db4566801a3a204007883322e6ae6754da91fe8457ee7665c62d
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

### `groovy:jdk11-jammy` - linux; amd64

```console
$ docker pull groovy@sha256:6f39d1f2367c3c2098a2f5d7716eac5b8996a4deb075925b5564e253024f924e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.6 MB (221554177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f14420f441c5f2e6496fb48ab558b6f23f50cfd5f4f0d87855f40f813b1e9f9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Tue, 28 Jan 2025 19:12:40 GMT
ARG RELEASE
# Tue, 28 Jan 2025 19:12:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Jan 2025 19:12:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Jan 2025 19:12:40 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 28 Jan 2025 19:12:40 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Tue, 28 Jan 2025 19:12:40 GMT
CMD ["/bin/bash"]
# Tue, 28 Jan 2025 19:12:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 Jan 2025 19:12:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 19:12:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7def4c5807b38ef1a7bb30a86572a795ca604127cc8d1f5b370abf23618104e6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='e7b3d37c347fe7af2a53711f16da8b9b164748ce4a84e47bb0739c3be7f1c421';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='79d574328f6960d40349996ef8c5949581f9e533dc76f134857c4125c78558ff';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='42c63651125a149cee2ba781300d75ffa67a25032f95038d50ee6d6177cb2e41';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='0da13d990da34ecc666399cf0efa72a4b4e295f05c0686ea25a4a173a6f4414b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 28 Jan 2025 19:12:40 GMT
CMD ["jshell"]
# Tue, 28 Jan 2025 19:12:40 GMT
CMD ["groovysh"]
# Tue, 28 Jan 2025 19:12:40 GMT
ENV GROOVY_HOME=/opt/groovy
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Tue, 28 Jan 2025 19:12:40 GMT
WORKDIR /home/groovy
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
ENV GROOVY_VERSION=4.0.25
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
USER 1000:1000
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54506c4838ad6d3a8d9661ee544a95d91e851847b40c2ee85c693921a6cc43d`  
		Last Modified: Wed, 09 Apr 2025 01:15:37 GMT  
		Size: 16.1 MB (16146031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473f219e2b1687296fe069312830215bd77cada5bf111769b7a9c085e8b73edb`  
		Last Modified: Wed, 09 Apr 2025 01:15:41 GMT  
		Size: 145.6 MB (145607790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef971a82f787d0c6600e2d79528604ee94829c5094e62fd488a16503ae709c1`  
		Last Modified: Wed, 09 Apr 2025 01:15:36 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178c66146304559b5b9efecae9527ce1f43c667d4c402a00cdf5e15a8ffe3cbd`  
		Last Modified: Wed, 09 Apr 2025 01:15:20 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b185163cd4c8f3c4aceb5c7bc69c089a307cc10cdba3195519002a9ee3de370`  
		Last Modified: Wed, 09 Apr 2025 02:12:35 GMT  
		Size: 4.3 KB (4325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9929bcc3efaa5cb3470af6a66abbe1fc68a6ee0fcfcb86d7707b67fae30dba`  
		Last Modified: Wed, 09 Apr 2025 02:12:35 GMT  
		Size: 244.6 KB (244568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa1e219f57fec24afbca4eee6df53b27e0641dfebfeb0c23c8272daa74bf9b4`  
		Last Modified: Wed, 09 Apr 2025 02:12:36 GMT  
		Size: 30.0 MB (30016489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39fc19d44204e2c8c504e997b345239bf6cab785d42ef320f637a4381fc0eac9`  
		Last Modified: Wed, 09 Apr 2025 02:12:35 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk11-jammy` - unknown; unknown

```console
$ docker pull groovy@sha256:24fe003ae8b2238884dd23a01618325130fabfa428c0aa0a510b274bb980f851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f1e92a56272a4a13c3bab742e92ef696c25fc78eb4c7c88c6c3aafb9bdfcfae`

```dockerfile
```

-	Layers:
	-	`sha256:0d888a8a58c9e72cdf9a0a175e433da46dd50d6e78bc47cb5c7ec2953875a882`  
		Last Modified: Wed, 09 Apr 2025 02:12:35 GMT  
		Size: 3.9 MB (3904680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29c3be6c8882a3c2f844308785f0a15c8025b20287edecb5364b9a2f9fc5124e`  
		Last Modified: Wed, 09 Apr 2025 02:12:35 GMT  
		Size: 25.6 KB (25613 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:jdk11-jammy` - linux; arm variant v7

```console
$ docker pull groovy@sha256:8bdfbfdee168630f47d08dfda791fd1a4b0619d66df272937d8fbb1d5018bf69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.9 MB (210876784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ffd2d781478b8fa82304404eb96e50e0b4d9f21194845cb962376c39c3eb0c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Tue, 28 Jan 2025 19:12:40 GMT
ARG RELEASE
# Tue, 28 Jan 2025 19:12:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Jan 2025 19:12:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Jan 2025 19:12:40 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 28 Jan 2025 19:12:40 GMT
ADD file:b27bdc0157c0d964026ea411ed5874766d804b491dfc3d5ac10188c76746bbb0 in / 
# Tue, 28 Jan 2025 19:12:40 GMT
CMD ["/bin/bash"]
# Tue, 28 Jan 2025 19:12:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 Jan 2025 19:12:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 19:12:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7def4c5807b38ef1a7bb30a86572a795ca604127cc8d1f5b370abf23618104e6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='e7b3d37c347fe7af2a53711f16da8b9b164748ce4a84e47bb0739c3be7f1c421';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='79d574328f6960d40349996ef8c5949581f9e533dc76f134857c4125c78558ff';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='42c63651125a149cee2ba781300d75ffa67a25032f95038d50ee6d6177cb2e41';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='0da13d990da34ecc666399cf0efa72a4b4e295f05c0686ea25a4a173a6f4414b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 28 Jan 2025 19:12:40 GMT
CMD ["jshell"]
# Tue, 28 Jan 2025 19:12:40 GMT
CMD ["groovysh"]
# Tue, 28 Jan 2025 19:12:40 GMT
ENV GROOVY_HOME=/opt/groovy
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Tue, 28 Jan 2025 19:12:40 GMT
WORKDIR /home/groovy
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
ENV GROOVY_VERSION=4.0.25
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
USER 1000:1000
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:f3e10eb95482b14d0f5a969fafb71afd541d5efd38890d551e27c957ed3ae84e`  
		Last Modified: Mon, 07 Apr 2025 08:26:39 GMT  
		Size: 26.6 MB (26640334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c38f06e215a1fbf49c830181d7341b1b395e52f4245dca30239c9be2d76548`  
		Last Modified: Wed, 09 Apr 2025 11:39:21 GMT  
		Size: 15.9 MB (15890794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dab56717d9c63fc09a056e74d0d20609e134d1d6c8bacf5b27ffd995ce5c44e`  
		Last Modified: Wed, 09 Apr 2025 11:43:58 GMT  
		Size: 138.1 MB (138091447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d3cc5c7097625a3d050e08dff633f8dc74d91da5025219228f3779ce6de3fb`  
		Last Modified: Wed, 09 Apr 2025 11:43:54 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46cb39aca12c5c2cd333563f232f059b96f8c09010100f7ab9bda16900d9db6b`  
		Last Modified: Wed, 09 Apr 2025 11:43:54 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6a9d3d410d11437497163aafef2d11da2e112284cd6035675a4833ede0ad67`  
		Last Modified: Wed, 09 Apr 2025 12:42:45 GMT  
		Size: 4.3 KB (4310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f420f5501d7fe9b088ec858695fd4bccffb26cff6b12711e5cea4fe5a0e557d8`  
		Last Modified: Wed, 09 Apr 2025 12:42:46 GMT  
		Size: 230.8 KB (230812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb46921d16faf55bef547abee30eebcfad128dfea18e7fbbd60baa7894ac3e1`  
		Last Modified: Wed, 09 Apr 2025 12:42:47 GMT  
		Size: 30.0 MB (30016475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef25902d9bce947eb6425bcee0f60f8c1f60bc462553d6eed7b1826c2bfdd9d3`  
		Last Modified: Wed, 09 Apr 2025 12:42:46 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk11-jammy` - unknown; unknown

```console
$ docker pull groovy@sha256:868eb710ee691f2e3c1ccf0851e3ce3691b062b1fe77976f498c91bb75e96d51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3931503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb6fcf981f7d1fb5571cf0a38fa7dca7af15b01bdf51864446769f09c19c6af`

```dockerfile
```

-	Layers:
	-	`sha256:bf93ae5f8b8ee7d7802b7839e48051c1bba3a818dde9a32c2235ea77e64499b7`  
		Last Modified: Wed, 09 Apr 2025 12:42:46 GMT  
		Size: 3.9 MB (3905759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e77ebc236ced5448fa5005d572d023c227d26074a3b565d101f38d1f742f2d84`  
		Last Modified: Wed, 09 Apr 2025 12:42:45 GMT  
		Size: 25.7 KB (25744 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:jdk11-jammy` - linux; arm64 variant v8

```console
$ docker pull groovy@sha256:4230413ceb53bab575e755675777ac8e7d4fc546b79c08a3e2f829285bc2801d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.1 MB (216065950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f783504ebb4b5dac82c33697567a76fd2bfa6a4f944660795b2a96ec8fbf720f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Tue, 28 Jan 2025 19:12:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 Jan 2025 19:12:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 19:12:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7def4c5807b38ef1a7bb30a86572a795ca604127cc8d1f5b370abf23618104e6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='e7b3d37c347fe7af2a53711f16da8b9b164748ce4a84e47bb0739c3be7f1c421';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='79d574328f6960d40349996ef8c5949581f9e533dc76f134857c4125c78558ff';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='42c63651125a149cee2ba781300d75ffa67a25032f95038d50ee6d6177cb2e41';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='0da13d990da34ecc666399cf0efa72a4b4e295f05c0686ea25a4a173a6f4414b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 28 Jan 2025 19:12:40 GMT
CMD ["jshell"]
# Tue, 28 Jan 2025 19:12:40 GMT
CMD ["groovysh"]
# Tue, 28 Jan 2025 19:12:40 GMT
ENV GROOVY_HOME=/opt/groovy
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Tue, 28 Jan 2025 19:12:40 GMT
WORKDIR /home/groovy
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
ENV GROOVY_VERSION=4.0.25
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
USER 1000:1000
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b542dd916502bedf4dd14bd9610d5843b919aed4757a473c4043de50c9ba83`  
		Last Modified: Tue, 04 Feb 2025 09:16:50 GMT  
		Size: 16.1 MB (16052648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35eff08bbe9698d6aba2dd294dbfeffe3aebd362e4ee73eb556e23d37c34ace4`  
		Last Modified: Tue, 04 Feb 2025 09:19:11 GMT  
		Size: 142.4 MB (142390417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4338c4fa92a386a1654e5969d3c1ea1d50cb1e3e1cc3f232fd2800018bebb4`  
		Last Modified: Tue, 04 Feb 2025 09:19:07 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5041ccdf179c4ec0e4a63f2f9eb342e2a05b3ea24d215a3049e83fa7c225a0a7`  
		Last Modified: Tue, 04 Feb 2025 09:19:07 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93cd2397507e857828ad4cfd2e30dc3922e630d28ac634c369fb59467942afcf`  
		Last Modified: Tue, 04 Feb 2025 20:09:30 GMT  
		Size: 4.3 KB (4338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e6e2a92c754dbee4fd219d110e086fa6d569de2d9def011287fb011d597af7`  
		Last Modified: Tue, 04 Feb 2025 20:09:31 GMT  
		Size: 241.3 KB (241265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26318626bba74620e0d0f420f70f17212ab78580d92689539be4d2606ee1ec8b`  
		Last Modified: Tue, 04 Feb 2025 20:09:32 GMT  
		Size: 30.0 MB (30016490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c68303bb1d19747ca50b5b2e0c6d7ca363ca17cfeef79de30fbb925bea7af6`  
		Last Modified: Tue, 04 Feb 2025 20:09:31 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk11-jammy` - unknown; unknown

```console
$ docker pull groovy@sha256:85259ea76dea654c4dee7c1ab4479801e5f197b7f7fe9eb6f58c984f11dd7587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3928210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d85b9d75210c4efe9efc2169937dc33c391950d86d2405c4916a5e9e2dcc91aa`

```dockerfile
```

-	Layers:
	-	`sha256:af25c0e17b815338d31e9db5bb559f64ee783986f059de348f0ccc9231c0d9cd`  
		Last Modified: Tue, 04 Feb 2025 20:09:31 GMT  
		Size: 3.9 MB (3902424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2241b00e800051bd99fb57637aad5c9daf531eebfae2506b922a65aa8ed177cd`  
		Last Modified: Tue, 04 Feb 2025 20:09:30 GMT  
		Size: 25.8 KB (25786 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:jdk11-jammy` - linux; ppc64le

```console
$ docker pull groovy@sha256:5cab269a8864850f013f4b95582127e761e950d28e0364fa4f1f2cc2307db5f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.2 MB (215151005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac150bbc87126bd9e73024418b05f84f7aab112168a81309778358a07eaf46b4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Tue, 28 Jan 2025 19:12:40 GMT
ARG RELEASE
# Tue, 28 Jan 2025 19:12:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Jan 2025 19:12:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Jan 2025 19:12:40 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 28 Jan 2025 19:12:40 GMT
ADD file:b1634c9c9ee669b835ef39787fc71f78267fab0678a8e8c5547ba2339762e075 in / 
# Tue, 28 Jan 2025 19:12:40 GMT
CMD ["/bin/bash"]
# Tue, 28 Jan 2025 19:12:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 Jan 2025 19:12:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 19:12:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7def4c5807b38ef1a7bb30a86572a795ca604127cc8d1f5b370abf23618104e6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='e7b3d37c347fe7af2a53711f16da8b9b164748ce4a84e47bb0739c3be7f1c421';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='79d574328f6960d40349996ef8c5949581f9e533dc76f134857c4125c78558ff';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='42c63651125a149cee2ba781300d75ffa67a25032f95038d50ee6d6177cb2e41';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='0da13d990da34ecc666399cf0efa72a4b4e295f05c0686ea25a4a173a6f4414b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 28 Jan 2025 19:12:40 GMT
CMD ["jshell"]
# Tue, 28 Jan 2025 19:12:40 GMT
CMD ["groovysh"]
# Tue, 28 Jan 2025 19:12:40 GMT
ENV GROOVY_HOME=/opt/groovy
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Tue, 28 Jan 2025 19:12:40 GMT
WORKDIR /home/groovy
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
ENV GROOVY_VERSION=4.0.25
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
USER 1000:1000
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:220e8fedb927c1ecfafdf1e8cd0a85977de62e4afd95df2c5a27a70d3bdf34b0`  
		Last Modified: Mon, 07 Apr 2025 08:26:45 GMT  
		Size: 34.4 MB (34442696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8c38ec2b4ee36ca93f19596eb065a396e648e65a58e52db4e0886be5ded596`  
		Last Modified: Wed, 09 Apr 2025 04:35:13 GMT  
		Size: 17.6 MB (17617815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcbee5d493c15f21ec8ede9dc23a5f672c0955dfedaf2be3468514d6ba603278`  
		Last Modified: Wed, 09 Apr 2025 04:40:42 GMT  
		Size: 132.8 MB (132787532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f297de1cdb64851d733bf1d7a3f3a4a4154009ec5de2036c047f0d52cf022b5`  
		Last Modified: Wed, 09 Apr 2025 04:40:37 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e134bddf72bcb2c001c1d09efb7d740a9b7033a6b43957d6817c1a0a99905b`  
		Last Modified: Wed, 09 Apr 2025 04:40:37 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd3cdb1c9856203a49f367648592a7de65d7b54544f9742d98cfd69ebfdf709`  
		Last Modified: Wed, 09 Apr 2025 08:18:59 GMT  
		Size: 4.3 KB (4334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca4e86163c69f60ff854d3dcf09f361c88f984a83fe1dcb1c55a0855be8116b`  
		Last Modified: Wed, 09 Apr 2025 08:19:00 GMT  
		Size: 279.5 KB (279529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd5b9fe8e76437017f0a840f562b4e69ec5948e2e33e787da411f2652e20bb2`  
		Last Modified: Wed, 09 Apr 2025 08:19:01 GMT  
		Size: 30.0 MB (30016486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30cd70e3524a132a5acfd13cb17f73a92e525a25233c8e0971b7dcbb178c05d0`  
		Last Modified: Wed, 09 Apr 2025 08:19:00 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk11-jammy` - unknown; unknown

```console
$ docker pull groovy@sha256:34250e978a9e2e7e198bd5f1b49cf4a4fe900ccf9d9404656877ebb92a181101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3931768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90effedda9be987818ec7da98f9cb1896b99a7bd1f193e6adeadd1703b94c73a`

```dockerfile
```

-	Layers:
	-	`sha256:9326d0e827138ea5b6ba80a332d06a4b1c2e016dd5f01460224cfd21d2281feb`  
		Last Modified: Wed, 09 Apr 2025 08:19:00 GMT  
		Size: 3.9 MB (3906093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5547fd0b0ad462427503a5de0ddf6bf6df1523d5b143c084660e4295a50d53aa`  
		Last Modified: Wed, 09 Apr 2025 08:18:59 GMT  
		Size: 25.7 KB (25675 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:jdk11-jammy` - linux; s390x

```console
$ docker pull groovy@sha256:67a3850c943fbe5a8f37909af9b27161229dff5ece1c6b61ddceb617da0bced0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.0 MB (199985868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:149773d99a211b0aca3c7a0fce49a937e292fd888dfceb5683a3e04d51899a82`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Tue, 28 Jan 2025 19:12:40 GMT
ARG RELEASE
# Tue, 28 Jan 2025 19:12:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Jan 2025 19:12:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Jan 2025 19:12:40 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 28 Jan 2025 19:12:40 GMT
ADD file:5d8d436f6811fd1894d694e7df7d347b9bd021b38bd57e01718331911c43a656 in / 
# Tue, 28 Jan 2025 19:12:40 GMT
CMD ["/bin/bash"]
# Tue, 28 Jan 2025 19:12:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 Jan 2025 19:12:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 19:12:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7def4c5807b38ef1a7bb30a86572a795ca604127cc8d1f5b370abf23618104e6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        arm64)          ESUM='e7b3d37c347fe7af2a53711f16da8b9b164748ce4a84e47bb0739c3be7f1c421';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        armhf)          ESUM='79d574328f6960d40349996ef8c5949581f9e533dc76f134857c4125c78558ff';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_arm_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64el)          ESUM='42c63651125a149cee2ba781300d75ffa67a25032f95038d50ee6d6177cb2e41';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='0da13d990da34ecc666399cf0efa72a4b4e295f05c0686ea25a4a173a6f4414b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 28 Jan 2025 19:12:40 GMT
CMD ["jshell"]
# Tue, 28 Jan 2025 19:12:40 GMT
CMD ["groovysh"]
# Tue, 28 Jan 2025 19:12:40 GMT
ENV GROOVY_HOME=/opt/groovy
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Tue, 28 Jan 2025 19:12:40 GMT
WORKDIR /home/groovy
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
ENV GROOVY_VERSION=4.0.25
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy" # buildkit
# Tue, 28 Jan 2025 19:12:40 GMT
USER 1000:1000
# Tue, 28 Jan 2025 19:12:40 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:25cf79adc8d2979d397edb23d9d8f0127bc0edfd1addfa501b8a0cc74338576b`  
		Last Modified: Mon, 07 Apr 2025 08:26:58 GMT  
		Size: 28.0 MB (28000118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939ffac1a60b6cb80417a2deaa826c5568b388878415c01490d46c373b76b9af`  
		Last Modified: Wed, 09 Apr 2025 04:16:19 GMT  
		Size: 16.1 MB (16143553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4852f34e12568b8cc124f8e686c47b54b55a08e450d54d6bd585cd1c14d6c707`  
		Last Modified: Wed, 09 Apr 2025 04:16:21 GMT  
		Size: 125.6 MB (125576016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f42b567c5a6c9e3cf2b0c7a8073853c1dfcb62f6e4e96a06dbc6f999d2d211d`  
		Last Modified: Wed, 09 Apr 2025 04:16:18 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e56b3843eb65dbdc6c20db47c42483431f4c5975c902bcecf6548bd47461d03`  
		Last Modified: Wed, 09 Apr 2025 04:16:18 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f230ea54039a23cc3b1e4755435ab3c84bcff40f53ddcdfd46f33f925571a567`  
		Last Modified: Wed, 09 Apr 2025 05:48:08 GMT  
		Size: 4.3 KB (4332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbbedd52c448c1cbf3b6a89fd065212544a52c6dae6dc54d7a7c5b1e5d8c8496`  
		Last Modified: Wed, 09 Apr 2025 05:48:08 GMT  
		Size: 242.8 KB (242752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a079502922132a9c7fa90633929c60ac098d7e294004c4e5c5666143d52fa26`  
		Last Modified: Wed, 09 Apr 2025 05:48:09 GMT  
		Size: 30.0 MB (30016487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0840ea70fdfb49d052852c3770b7c825c316a46da37cebd0beaf7d9e906ff1ed`  
		Last Modified: Wed, 09 Apr 2025 05:48:08 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk11-jammy` - unknown; unknown

```console
$ docker pull groovy@sha256:36e90c1370ba11f1453ff15839be9c29f79e574010861bbee8163ba326534969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3927489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d4fb8c4a3e7dfcd9fac86bfbfcbbce329adb750a66db50a1c4835f4f1e362b9`

```dockerfile
```

-	Layers:
	-	`sha256:8471e393be85c888280eed32ad62d1723ebd6bbc4d9d877b7d9f8855dc311d09`  
		Last Modified: Wed, 09 Apr 2025 05:48:08 GMT  
		Size: 3.9 MB (3901876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72c6265ecf7ba8d37616b012ffbdcf311712b46df66da91312f51e7be76edeef`  
		Last Modified: Wed, 09 Apr 2025 05:48:08 GMT  
		Size: 25.6 KB (25613 bytes)  
		MIME: application/vnd.in-toto+json
