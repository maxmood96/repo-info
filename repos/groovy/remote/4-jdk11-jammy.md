## `groovy:4-jdk11-jammy`

```console
$ docker pull groovy@sha256:0d6d998dbdcdd64aa71e2bd75877854b86f949b3d750eada0c7d64c9f3c98d6f
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

### `groovy:4-jdk11-jammy` - linux; amd64

```console
$ docker pull groovy@sha256:02ec488e68811f6e3e5deab2cd805a118fa695c9c26633a1b0a586c2b44840bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 MB (221793737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc68c24b268d9dfda32d0c2f0017d2efdd112b4fd1ebe8977146795c197281e`
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
LABEL org.opencontainers.image.version=22.04
# Wed, 02 Jul 2025 04:24:55 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Wed, 02 Jul 2025 04:24:55 GMT
CMD ["/bin/bash"]
# Wed, 02 Jul 2025 04:24:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Jul 2025 04:24:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Jul 2025 04:24:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Jul 2025 04:24:55 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7dfd551795a8884b26cbb02e0301da95db40160bb194f48271dc2ef9367f50c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_x64_linux_hotspot_11.0.28_6.tar.gz';          ;;        arm64)          ESUM='32c316cb3998a9c9dee2829fbb577ea1c0ed666700cec73e049d44c342bb19af';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.28_6.tar.gz';          ;;        armhf)          ESUM='b33c99068804bbd7e4aa4bd1c5419ae88ec77833e5e5339ab06a00546a2b0711';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_arm_linux_hotspot_11.0.28_6.tar.gz';          ;;        ppc64el)          ESUM='e272abd162b3de68093630929453feba3e63a5ab1bbb912379f6a4aa968ef06a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.28_6.tar.gz';          ;;        s390x)          ESUM='ac3f94fdcc5372e90f44fad9cd03ec0e3fd3535fea06c120f85e4a7534c6de04';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
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
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626e0066814941272596c597780bba5c1c5946777688734462b04050bbfc86aa`  
		Last Modified: Mon, 01 Sep 2025 23:08:54 GMT  
		Size: 16.2 MB (16150578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5af6814b849fd03f35bb04c172c54aed74a2f1b2c0874ee0d0a741afb248ab`  
		Last Modified: Tue, 02 Sep 2025 00:11:15 GMT  
		Size: 145.7 MB (145669093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481ed921877fec7fe7c67ad46baaa417fd72c7d23bdc6947ad207f016f9a0c76`  
		Last Modified: Mon, 01 Sep 2025 23:08:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04773f58314fb5a8e58a12dcc9f230f3bd11368c661df5d942a2db056acb31c`  
		Last Modified: Mon, 01 Sep 2025 23:08:44 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72725e5459b6c4b30741903a250882d35be325db678fd2917984cf1d106233a7`  
		Last Modified: Tue, 02 Sep 2025 01:44:22 GMT  
		Size: 4.3 KB (4327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c62806c6fc62881c3f8f941729a6aeb33d56e080a995dc06a25ae419421f13`  
		Last Modified: Tue, 02 Sep 2025 01:44:23 GMT  
		Size: 244.6 KB (244552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8794d76e6c1b15920bfcfe3c182754e813733e02e5aeea70a3aba65836ef29`  
		Last Modified: Tue, 02 Sep 2025 01:44:27 GMT  
		Size: 30.2 MB (30185642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc3257fda35819eea263058da8ee4587aa1ce542b3d3aadcaa6dc3a01be641e`  
		Last Modified: Tue, 02 Sep 2025 01:44:28 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:4-jdk11-jammy` - unknown; unknown

```console
$ docker pull groovy@sha256:6473cda795b9e08c45b407b7461e13fee9585fcc33158348ef2b0ddccaa0ecf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4110787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d07516ab95b8e8e1a20f9bb0288a1bf8cb05120b156a1bfe43fd12f3c3eb6b2f`

```dockerfile
```

-	Layers:
	-	`sha256:d8cb483c11b1195a3d0a31e33aa5a4af13ae7f00709c5006ddcd41b6968e536b`  
		Last Modified: Tue, 02 Sep 2025 02:20:40 GMT  
		Size: 4.1 MB (4082111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e28ff8af06f32157481765d805601b7431a008a9837bad0b2261d22616ae600`  
		Last Modified: Tue, 02 Sep 2025 02:20:41 GMT  
		Size: 28.7 KB (28676 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:4-jdk11-jammy` - linux; arm variant v7

```console
$ docker pull groovy@sha256:4d16fd2710c9acae736230ebed794c7f0856184e621577e802dab59f65729be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211098446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67e6a3ad1ce173dc8cd467ace95b41653a2f7c1d3ab7d40e15d6a35ea33572bf`
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
LABEL org.opencontainers.image.version=22.04
# Wed, 02 Jul 2025 04:24:55 GMT
ADD file:1b718ac25471aa07aabcef27ec2e737bdbf36fd950c8d6e6103ad3dfeacd8e98 in / 
# Wed, 02 Jul 2025 04:24:55 GMT
CMD ["/bin/bash"]
# Wed, 02 Jul 2025 04:24:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Jul 2025 04:24:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Jul 2025 04:24:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Jul 2025 04:24:55 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7dfd551795a8884b26cbb02e0301da95db40160bb194f48271dc2ef9367f50c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_x64_linux_hotspot_11.0.28_6.tar.gz';          ;;        arm64)          ESUM='32c316cb3998a9c9dee2829fbb577ea1c0ed666700cec73e049d44c342bb19af';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.28_6.tar.gz';          ;;        armhf)          ESUM='b33c99068804bbd7e4aa4bd1c5419ae88ec77833e5e5339ab06a00546a2b0711';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_arm_linux_hotspot_11.0.28_6.tar.gz';          ;;        ppc64el)          ESUM='e272abd162b3de68093630929453feba3e63a5ab1bbb912379f6a4aa968ef06a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.28_6.tar.gz';          ;;        s390x)          ESUM='ac3f94fdcc5372e90f44fad9cd03ec0e3fd3535fea06c120f85e4a7534c6de04';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
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
	-	`sha256:9e6391cf5a380a152971ee67d9bbbdd494023e7e2a2da9c7b92dd6d51593fee6`  
		Last Modified: Mon, 01 Sep 2025 23:13:56 GMT  
		Size: 26.6 MB (26642908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0cf151b513ce2784601808e6c9ca1a399d393f9a94a6bc7e7157b64d4f3a05`  
		Last Modified: Tue, 02 Sep 2025 00:14:16 GMT  
		Size: 15.9 MB (15889744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b2786ca22c280ab4c2494d1f927563b0d6f1111a1a7f8db50a163a7da1e1c1`  
		Last Modified: Tue, 02 Sep 2025 02:15:51 GMT  
		Size: 138.1 MB (138142357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ebfd754e5405482f66042b258dc90d0bc06f1d4c9488b01b925a002bc23600`  
		Last Modified: Tue, 02 Sep 2025 00:17:08 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d41dd975b0b5227a57f89fa2df1d00b96589e357921052327bf82952e1c4ac`  
		Last Modified: Tue, 02 Sep 2025 00:17:08 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac5c17db85d25821ded2fa52d8ba671458ca56586fed3f2f7542b973e9a9bf0`  
		Last Modified: Tue, 02 Sep 2025 01:26:51 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f528a5f02344ab052b568cbb8057cf7a9b6b30fc13766fbcb1e8705e9cf384`  
		Last Modified: Tue, 02 Sep 2025 01:26:51 GMT  
		Size: 230.9 KB (230866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b382a0be9d049c323d6f0974e0e9a4b399c89be2fdf88fd8e105e6ec37f0827`  
		Last Modified: Tue, 02 Sep 2025 01:26:56 GMT  
		Size: 30.2 MB (30185644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e291f66fa3367d66af2f8e20a7432da00de0d1d68e948a66c7e6bbe066fc024b`  
		Last Modified: Tue, 02 Sep 2025 01:26:51 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:4-jdk11-jammy` - unknown; unknown

```console
$ docker pull groovy@sha256:fc378d0ae9995509c210b78724381574285da9fe80dd105316f7ddd3a2fc17fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09966838ea0b9639d8e29980c3333cc9ee68444e070ad1bdbffd6e9885133055`

```dockerfile
```

-	Layers:
	-	`sha256:161bb1dcc2237a3c847d0600d905513231cc14b6a6e2a8a675b7365706673ab8`  
		Last Modified: Tue, 02 Sep 2025 02:20:46 GMT  
		Size: 4.1 MB (4083270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24ea682c10f139a6d9f484ac10067fbe735eae7ca79dde9b3996da7d95bbc191`  
		Last Modified: Tue, 02 Sep 2025 02:20:47 GMT  
		Size: 28.9 KB (28888 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:4-jdk11-jammy` - linux; arm64 variant v8

```console
$ docker pull groovy@sha256:e2a453719f22850a7e7d15bd67c6c6d52bd51683076621facb6c03ab1389f3a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.3 MB (216320628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d37fa01420e1a49110ac4b40774ee5010b1f3d8a74b136e8bfc3ca5ce02504d`
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
LABEL org.opencontainers.image.version=22.04
# Wed, 02 Jul 2025 04:24:55 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 02 Jul 2025 04:24:55 GMT
CMD ["/bin/bash"]
# Wed, 02 Jul 2025 04:24:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Jul 2025 04:24:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Jul 2025 04:24:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Jul 2025 04:24:55 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7dfd551795a8884b26cbb02e0301da95db40160bb194f48271dc2ef9367f50c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_x64_linux_hotspot_11.0.28_6.tar.gz';          ;;        arm64)          ESUM='32c316cb3998a9c9dee2829fbb577ea1c0ed666700cec73e049d44c342bb19af';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.28_6.tar.gz';          ;;        armhf)          ESUM='b33c99068804bbd7e4aa4bd1c5419ae88ec77833e5e5339ab06a00546a2b0711';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_arm_linux_hotspot_11.0.28_6.tar.gz';          ;;        ppc64el)          ESUM='e272abd162b3de68093630929453feba3e63a5ab1bbb912379f6a4aa968ef06a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.28_6.tar.gz';          ;;        s390x)          ESUM='ac3f94fdcc5372e90f44fad9cd03ec0e3fd3535fea06c120f85e4a7534c6de04';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
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
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b5bc71170396faf6c1c291a060d5d6b6d6700719a4f7f1f47d7e8a843b7a6d`  
		Last Modified: Tue, 12 Aug 2025 18:31:02 GMT  
		Size: 16.1 MB (16063741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a534e1f6cdf5da1af1d2d4342de0176cfbe458ca1d323955a852587ce3a548`  
		Last Modified: Tue, 12 Aug 2025 22:59:40 GMT  
		Size: 142.5 MB (142463709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490f693a645e7ed96e223d23d1b38132cd2394b67c567bb1ea6cffd2c05ffb56`  
		Last Modified: Tue, 12 Aug 2025 19:04:32 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35e4135fa2779838a8c8cb6276e6719ad1243eecedd278088d4961cb9f8b878`  
		Last Modified: Tue, 12 Aug 2025 19:04:31 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c3812013fd289aba60aedf1df5be35165ed9b79cc913552dc4f16346fb8cf0`  
		Last Modified: Tue, 12 Aug 2025 22:54:48 GMT  
		Size: 4.3 KB (4332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ce5dbd5b5d0415bf7105f006987dd73818aefa91ec9de831f0b050f7a15b27`  
		Last Modified: Tue, 12 Aug 2025 22:54:48 GMT  
		Size: 241.4 KB (241367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6360cee0eb583b93fb70dc4a411b4ad8bea9bfed6a4ef2aa72fdb80c6093f0`  
		Last Modified: Tue, 12 Aug 2025 22:54:53 GMT  
		Size: 30.2 MB (30185626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d819ea792f392f6dc272ad1a75987e6a1842bfe33b6db59837c23be74481e44`  
		Last Modified: Tue, 12 Aug 2025 22:54:49 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:4-jdk11-jammy` - unknown; unknown

```console
$ docker pull groovy@sha256:39e3bde302490317ae5e8473bae60bd9448eadf9c4bb549ecd8e36d8d50da18a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4111507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54bb591be9036f13c81f6a5310efe125e58cda36c6be08344dc5e16f07de9303`

```dockerfile
```

-	Layers:
	-	`sha256:4eeaee6063e5c7b1d2daafc182f369dd620b02abaa6e3ee23553954026c63ae7`  
		Last Modified: Tue, 12 Aug 2025 23:20:43 GMT  
		Size: 4.1 MB (4082537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53501d39f5804c8055e050bb74e16b81f9ca7bbdd89125f9c74c8d551ef74e28`  
		Last Modified: Tue, 12 Aug 2025 23:20:44 GMT  
		Size: 29.0 KB (28970 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:4-jdk11-jammy` - linux; ppc64le

```console
$ docker pull groovy@sha256:3983bb4f64df8aa526a11dd88e95c98b1a499470fff19b96f1131f0f325b9c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215402239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16ff3feb612358711f2a03ecaa40bf893d8acfe2ce50ddd1aee8dff70a1d5b03`
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
LABEL org.opencontainers.image.version=22.04
# Wed, 02 Jul 2025 04:24:55 GMT
ADD file:8e490d6aa7e352ca02bf6249fe59c9445bd10be61e8a31e7d8219d7f34f3df1e in / 
# Wed, 02 Jul 2025 04:24:55 GMT
CMD ["/bin/bash"]
# Wed, 02 Jul 2025 04:24:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Jul 2025 04:24:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Jul 2025 04:24:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Jul 2025 04:24:55 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7dfd551795a8884b26cbb02e0301da95db40160bb194f48271dc2ef9367f50c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_x64_linux_hotspot_11.0.28_6.tar.gz';          ;;        arm64)          ESUM='32c316cb3998a9c9dee2829fbb577ea1c0ed666700cec73e049d44c342bb19af';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.28_6.tar.gz';          ;;        armhf)          ESUM='b33c99068804bbd7e4aa4bd1c5419ae88ec77833e5e5339ab06a00546a2b0711';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_arm_linux_hotspot_11.0.28_6.tar.gz';          ;;        ppc64el)          ESUM='e272abd162b3de68093630929453feba3e63a5ab1bbb912379f6a4aa968ef06a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.28_6.tar.gz';          ;;        s390x)          ESUM='ac3f94fdcc5372e90f44fad9cd03ec0e3fd3535fea06c120f85e4a7534c6de04';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
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
	-	`sha256:9e0049f176947659afd8c14b3a33c239a7d2fb1bdcbab338270e4d28b95b3a1d`  
		Last Modified: Tue, 12 Aug 2025 17:03:41 GMT  
		Size: 34.4 MB (34443145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10c50520b2833414582dcec4e87265a64dd9e5acd7b3ec03378e25ec51523b3`  
		Last Modified: Tue, 12 Aug 2025 17:29:14 GMT  
		Size: 17.6 MB (17624214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a6cdc48b64479e6917dde7b6550af7c51adfa53eeba27a0786368995116b45`  
		Last Modified: Wed, 13 Aug 2025 02:12:12 GMT  
		Size: 132.9 MB (132862811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b11773663267f7ddb7d368fd4918e6bf44a563a7603dda1c5fb6011569f0e6`  
		Last Modified: Tue, 12 Aug 2025 17:33:36 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60ba88d28d12ee48c6f0e528dafaedab24d8ea3bf981070059ec979d3e6ad6e`  
		Last Modified: Tue, 12 Aug 2025 17:33:35 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca8dbd351b8a577815085bb731a1c740ed5245cee4c18e4913cfe56e01ba01e`  
		Last Modified: Wed, 13 Aug 2025 00:57:33 GMT  
		Size: 4.3 KB (4331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72d18f9f1f043debf7581f6f03a212528eda33bb4603c5eb7c85172d00adf0d`  
		Last Modified: Wed, 13 Aug 2025 00:57:33 GMT  
		Size: 279.5 KB (279493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f784270807264b5d64e9fcda2973bdca760f6b12b229b721b04228eea3b054f`  
		Last Modified: Wed, 13 Aug 2025 00:57:38 GMT  
		Size: 30.2 MB (30185632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a85b70a8789376d56809f3b8014657d2f2c341346854306543365e95511d654`  
		Last Modified: Wed, 13 Aug 2025 00:57:34 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:4-jdk11-jammy` - unknown; unknown

```console
$ docker pull groovy@sha256:6480d9e6036a6b27e76de413ec563b9e0acd5a67175ec21556141a55973ca102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03005f99d38984163fa5b5eccc122d5813e00d824d8b1f39c1f629225684b5b`

```dockerfile
```

-	Layers:
	-	`sha256:4053bfd5198247c6f032b259472f057f82962be6643a4e305acaafc70953fefb`  
		Last Modified: Wed, 13 Aug 2025 02:20:40 GMT  
		Size: 4.1 MB (4083718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f721b396e1e5357448a63b0317b130364b71eccc6cc244fffa5ef816243894b4`  
		Last Modified: Wed, 13 Aug 2025 02:20:41 GMT  
		Size: 28.8 KB (28799 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:4-jdk11-jammy` - linux; s390x

```console
$ docker pull groovy@sha256:4616b4c31d225b759e691bda8b0ddeee850045c3d556b505f2da24ccf036d839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.2 MB (200224683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf13b0a540947a12148ed4f7f8c211a4d95d959bf3f88a40cae639313947427e`
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
LABEL org.opencontainers.image.version=22.04
# Wed, 02 Jul 2025 04:24:55 GMT
ADD file:29917512cc6cafe60268e67a6ab4ee1e581cd8f4c2bca9a228ba5a680375b746 in / 
# Wed, 02 Jul 2025 04:24:55 GMT
CMD ["/bin/bash"]
# Wed, 02 Jul 2025 04:24:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Jul 2025 04:24:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Jul 2025 04:24:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Jul 2025 04:24:55 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Wed, 02 Jul 2025 04:24:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7dfd551795a8884b26cbb02e0301da95db40160bb194f48271dc2ef9367f50c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_x64_linux_hotspot_11.0.28_6.tar.gz';          ;;        arm64)          ESUM='32c316cb3998a9c9dee2829fbb577ea1c0ed666700cec73e049d44c342bb19af';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.28_6.tar.gz';          ;;        armhf)          ESUM='b33c99068804bbd7e4aa4bd1c5419ae88ec77833e5e5339ab06a00546a2b0711';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_arm_linux_hotspot_11.0.28_6.tar.gz';          ;;        ppc64el)          ESUM='e272abd162b3de68093630929453feba3e63a5ab1bbb912379f6a4aa968ef06a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.28_6.tar.gz';          ;;        s390x)          ESUM='ac3f94fdcc5372e90f44fad9cd03ec0e3fd3535fea06c120f85e4a7534c6de04';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
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
	-	`sha256:2109104756ac117958527cffddc193d2cf33d0621953649a7d5800a93fa86665`  
		Last Modified: Mon, 01 Sep 2025 22:59:18 GMT  
		Size: 28.0 MB (28003668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd9a055cccbd579a3774f2095602ffe4afd51473766e809ce2a67b5cfb09608`  
		Last Modified: Mon, 01 Sep 2025 23:11:44 GMT  
		Size: 16.1 MB (16149951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed6a5707be8fa02908801c16ce329216fe3caf3c4e0857c8b0fa6906ce2a7af`  
		Last Modified: Mon, 01 Sep 2025 23:11:54 GMT  
		Size: 125.6 MB (125635785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc0b2e58e4773ddbf85f262b6892a8a44e260ecc60407d16cad8262b7cdb563`  
		Last Modified: Mon, 01 Sep 2025 23:11:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559ea82e93f86715103b708a7fcad7ff84b7ad6298854f0b63cf242cf55fe8a4`  
		Last Modified: Mon, 01 Sep 2025 23:11:43 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf11fbbbecdf22355108d9d556510af52734d6fc2547cd43a335138f80e37733`  
		Last Modified: Tue, 02 Sep 2025 01:24:37 GMT  
		Size: 4.3 KB (4330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed52a5d788a7c158b0d35cdd26f6159cab111995304af9be7ca20c429db18e84`  
		Last Modified: Tue, 02 Sep 2025 01:24:37 GMT  
		Size: 242.7 KB (242720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8cd2b2918ca6b0dd6bb0e800d14ba34b4aa91813132b61609db6ffb3ff3041`  
		Last Modified: Tue, 02 Sep 2025 00:38:07 GMT  
		Size: 30.2 MB (30185619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b370cffcc8b5acab9a298d0082dfc204e10431ed29d6b6bdafab2763a2440c67`  
		Last Modified: Tue, 02 Sep 2025 01:24:36 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:4-jdk11-jammy` - unknown; unknown

```console
$ docker pull groovy@sha256:1a7bb45e81003913926fa5fb4154af137f9ae9c77cd69fc78054dd462d343788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4107984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc147c07b5968ce81eb612821b26a4935c5e871b1c9c5001c7870b47249509b`

```dockerfile
```

-	Layers:
	-	`sha256:bcba1db4649b60c0ce274094e17769ad9b41bc09eb76ef81cd54e9412d1d5113`  
		Last Modified: Tue, 02 Sep 2025 02:21:00 GMT  
		Size: 4.1 MB (4079307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04c07ed3843dd1dd9c08948893aa71e251afcd7d281bc5d5218ad4c0b23fffdf`  
		Last Modified: Tue, 02 Sep 2025 02:21:01 GMT  
		Size: 28.7 KB (28677 bytes)  
		MIME: application/vnd.in-toto+json
