## `groovy:jdk21-jammy`

```console
$ docker pull groovy@sha256:29c170253aaf8c1cb535d112998fc350202b5ba5a44afda5480879bc31b23b00
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `groovy:jdk21-jammy` - linux; amd64

```console
$ docker pull groovy@sha256:2675b1612418b48aa2728490c4760924c3d7064a364f57b356047cab5585c032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.8 MB (239805460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b1b31f6e276ae0b5086e3f02b1e0d0620eaa07564cc1aa26a8e914fdb90dd74`
-	Entrypoint: `["\/bin\/bash","\/__cacert_entrypoint.sh"]`
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
ENV JAVA_VERSION=jdk-21.0.4+7
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:482fbf153ddc486288887c925609aba1a06123ef449197541916204000b32be3`  
		Last Modified: Sat, 17 Aug 2024 01:14:02 GMT  
		Size: 158.6 MB (158587052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880c2e95b386c797a96f9abf3551e5738cf995742285d5f45314d75676ed6d7a`  
		Last Modified: Sat, 17 Aug 2024 01:13:50 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d374cf93eba985e32df69f0d66d0f96d62292e4de04a8adf60ea4ab943bf0a9f`  
		Last Modified: Sat, 17 Aug 2024 01:13:50 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ea6f8ae9821defcce5572c14a2aade7b29108a3ec5d8068fba70f6226891f5`  
		Last Modified: Sat, 17 Aug 2024 02:00:59 GMT  
		Size: 4.3 KB (4326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b4193b8efe7ad8eb1264199bfe38c1ca52eefc196be08136c2aca87d9fca95`  
		Last Modified: Sat, 17 Aug 2024 02:00:59 GMT  
		Size: 3.5 MB (3503769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0531d2bfb1216eb140b80cdb0ebc564bb5e815cb5f7ee2f22f2c4639d83697fb`  
		Last Modified: Sat, 17 Aug 2024 02:01:00 GMT  
		Size: 29.9 MB (29851959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15570c03b55d2ec88afb87f0e190a366cb54cf9392e00ed9f25090cfb59aaab4`  
		Last Modified: Sat, 17 Aug 2024 02:00:59 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk21-jammy` - unknown; unknown

```console
$ docker pull groovy@sha256:368b2abdcd5d6d90f5dc3f14685a8de72739ac8247d0ec24e53d42238fae8ec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3889477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b21e08d28a0095355c5a47a6373fe12e795abf5f4754eb64e9076fdbb7f253c`

```dockerfile
```

-	Layers:
	-	`sha256:cb0cf38550d79ba974b4d735525e90a279f0a2966703adff5b90c0f8cac1ee03`  
		Last Modified: Sat, 17 Aug 2024 02:00:59 GMT  
		Size: 3.9 MB (3863892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca44594de7f450e8cd3838455c2dba8b172c0afb5b138a506f2f71e842196821`  
		Last Modified: Sat, 17 Aug 2024 02:00:58 GMT  
		Size: 25.6 KB (25585 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:jdk21-jammy` - linux; arm64 variant v8

```console
$ docker pull groovy@sha256:8149c32af08443ed89cb772b7460aa73dbc0d3c32fe9df1bb9af1db881986439
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.3 MB (237313074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba8c2b6a0c959d48988389808d3f25935ea53788d3e5fc2bb9aaea15eff9fb1`
-	Entrypoint: `["\/bin\/bash","\/__cacert_entrypoint.sh"]`
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
ENV JAVA_VERSION=jdk-21.0.4+7
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 30 Jun 2024 17:46:17 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:844625103df5730b175530991cf1aa8bfc1484eb61d967e68c9eb7c0fb721310`  
		Last Modified: Sat, 17 Aug 2024 01:36:44 GMT  
		Size: 156.8 MB (156756765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99d21c2f2420d3cb394597a37125582947b7c6843676a6725f3d8b0705b26f3`  
		Last Modified: Sat, 17 Aug 2024 01:36:33 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb7fa3a20c4143387f406802257a1692743970d394f68ff253d8203ba1ef6a6`  
		Last Modified: Sat, 17 Aug 2024 01:36:33 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ccd9bb9befc37a26b94f6771552162677a488cf4cd474901529ec17c198083`  
		Last Modified: Sat, 17 Aug 2024 07:23:16 GMT  
		Size: 4.3 KB (4336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950bc070e13127ab51f02e270da0282d88f593217aad4320bb5d5fd708544696`  
		Last Modified: Sat, 17 Aug 2024 07:23:17 GMT  
		Size: 3.5 MB (3472674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e938bd36b8af7eeab37f9f22eb69cd04b6cf72d60e2e446432a62b968696fa8`  
		Last Modified: Sat, 17 Aug 2024 07:23:18 GMT  
		Size: 29.9 MB (29851960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe885c73f36ceeb2412a861a3684c60be51570f4deded7c69b00a391accfc92f`  
		Last Modified: Sat, 17 Aug 2024 07:23:17 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk21-jammy` - unknown; unknown

```console
$ docker pull groovy@sha256:33669aed351d65578ae58640a9716f3a55f79588a148d41221d485267989b97e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3986058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1e9c2582402850b99c1cac5d8c5c39fbe7be6d8c3bd6374deb87c1a144bad28`

```dockerfile
```

-	Layers:
	-	`sha256:7f69f415c6114d7e0b2026a13712c1c6b5fd7a6eb0dcd8f1e0ed314b75d81927`  
		Last Modified: Sat, 17 Aug 2024 07:23:17 GMT  
		Size: 4.0 MB (3960132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:240c080f9a45b53d1d0284420f5e8ed0bf2b1429467acdefe1ee52c1edf9eaa7`  
		Last Modified: Sat, 17 Aug 2024 07:23:16 GMT  
		Size: 25.9 KB (25926 bytes)  
		MIME: application/vnd.in-toto+json
