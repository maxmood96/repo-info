## `groovy:4-jdk11-jammy`

```console
$ docker pull groovy@sha256:8ac95972ea2f456bc196f41d108c5d0a3acfe084fb8bb5360da5c840312b9fed
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
$ docker pull groovy@sha256:ed0f00339786b48609098151081e0714afb331aeecb77b219a90d87f241b1989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211097981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11296681722840de76f33b36a3cc4e7ed1a43be4af599d0f973f8ccd9baeec61`
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
ADD file:7939f961de8cf091ed251aa1d8e432c16ec7506130ed39a1db4028efdad8fbfe in / 
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
	-	`sha256:33392950d914bf1e16e980fc0bbcec6367a2d2b8ecbd726dc5fc65b4c96ce79f`  
		Last Modified: Wed, 01 Oct 2025 18:17:15 GMT  
		Size: 26.6 MB (26643435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407ee8a10b899fca8fa52a65c4066d12c175b603f0afa2b6c4b98f1ab7a597ef`  
		Last Modified: Thu, 02 Oct 2025 01:12:25 GMT  
		Size: 15.9 MB (15888947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac2b5bd03fa85c3c69533d9c5342dcb00a0016f097f42b228cee6998dac4538`  
		Last Modified: Thu, 02 Oct 2025 02:15:12 GMT  
		Size: 138.1 MB (138142188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ab839ec8293ae8ffa8946539e0fcb607ef4f6822037c5e91278891e4e9071e`  
		Last Modified: Thu, 02 Oct 2025 01:12:22 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83bc4dd9c54d2ffadd2ff1db237009dcfea98c65a8ec903afefbdaf3d18aec0`  
		Last Modified: Thu, 02 Oct 2025 01:12:14 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72190f6a7e52fe6e28f06f08c002e7196594953e49e41b6753fdeaa67fa5631a`  
		Last Modified: Thu, 02 Oct 2025 02:17:16 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc74fa54d94f18b5719a7911ba3964a2da654870e2fd5aff9e27dd3b3f909055`  
		Last Modified: Thu, 02 Oct 2025 02:17:16 GMT  
		Size: 230.8 KB (230848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d7866e80ff1ce57d8d58be5e43cf1d198ddc748d3461baafde4ff49d2c0741`  
		Last Modified: Thu, 02 Oct 2025 02:17:19 GMT  
		Size: 30.2 MB (30185641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb19f352b8e76b2fb72b5b7db8832504bbc5f82374c588aba1f07a3baa3b2bba`  
		Last Modified: Thu, 02 Oct 2025 02:17:17 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:4-jdk11-jammy` - unknown; unknown

```console
$ docker pull groovy@sha256:8121e374e1c1e29a98d9a6bd438f39244ea91204bb1c50d149075ca0b8e4a641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad33013fcb6d95299577b7f1e444b5a5acab2224c6f249c4a32a4166c2281a9a`

```dockerfile
```

-	Layers:
	-	`sha256:cc1602159019dcf60cf19fe34e56f9897fb9854a51fc57ee7901112b8d5cb6ee`  
		Last Modified: Thu, 02 Oct 2025 05:20:48 GMT  
		Size: 4.1 MB (4083270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c92f6d2e21b33cae95cf9afedfc7a32c37dc07eeb97d8b2a68d4e9201c51093`  
		Last Modified: Thu, 02 Oct 2025 05:20:50 GMT  
		Size: 28.9 KB (28892 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:4-jdk11-jammy` - linux; arm64 variant v8

```console
$ docker pull groovy@sha256:6107c043c603f643db5029ae97fda450c70275da888cb005bde02b5295d7c61f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.3 MB (216348601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83cf9cc77e7c5806f3e8166a00524bc92a04e61dd62217068359efdd2dcf4e7`
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
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467d494d86601559a7c580a845a24d7c3c4e03397a8e6172f73c42ceaea86b78`  
		Last Modified: Thu, 02 Oct 2025 01:17:23 GMT  
		Size: 16.1 MB (16065710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d19d17ce5c4e5ce5c7d830f1dd4a97f39bf68e94135f8e8e0a6024458084e5a`  
		Last Modified: Thu, 02 Oct 2025 02:18:00 GMT  
		Size: 142.5 MB (142465824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fcddd67e29121d270d27c5165775ac884460e37aabce793d45897440c6bcad`  
		Last Modified: Thu, 02 Oct 2025 01:17:22 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a32ba3c9242b8d0bbaf28bbfa687c3c8646d14b23cb160dc3be8e414c6b3ffa`  
		Last Modified: Thu, 02 Oct 2025 01:17:22 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9a6fc571c83bbbf9479354654019f74c460e0d9badcbb34e124517eb7fda17`  
		Last Modified: Thu, 02 Oct 2025 02:20:07 GMT  
		Size: 4.3 KB (4331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02d949d971d599c32701d0608431cbbbdb73b6d7d8a3f678b673595ed4349a6`  
		Last Modified: Thu, 02 Oct 2025 02:20:07 GMT  
		Size: 241.4 KB (241384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c635f10c462af653e7f0ea4b91315802f0d7ba61ec732b93ff5e8672fe8932`  
		Last Modified: Thu, 02 Oct 2025 02:20:09 GMT  
		Size: 30.2 MB (30185635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ecd153db81260fd5ae7ea9bc96754326fc546384eec43295fa5ac7cf63125fa`  
		Last Modified: Thu, 02 Oct 2025 02:20:07 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:4-jdk11-jammy` - unknown; unknown

```console
$ docker pull groovy@sha256:a612d60d4c5f9897a943b47af145cb1e1600450b51bbc99b02e1cae0680fb19b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4111523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77b477418fa6f5a278b2fb260c46a2f54455738da024b91dfde4a3dbcbdd5f9`

```dockerfile
```

-	Layers:
	-	`sha256:f43d717e210ad2bde81a4fe902e2ede4cd92654fc90cc282f79b39df473712cd`  
		Last Modified: Thu, 02 Oct 2025 05:20:55 GMT  
		Size: 4.1 MB (4082553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c53d8a4c242fe628513d310547851954bf7bc39dbd3bc532a7837629d7feba4a`  
		Last Modified: Thu, 02 Oct 2025 05:20:56 GMT  
		Size: 29.0 KB (28970 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:4-jdk11-jammy` - linux; ppc64le

```console
$ docker pull groovy@sha256:cd46fb3078aab08e1d0b716db3db2e171eda8b3c11d7da7cff58c38288081737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215402647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a6143beebcc2e502810dd160ed3fac37bcb32fdd56b869e43d9470f1bc9279`
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
ADD file:da179546f976792ede40255758ecaed39b1e36eacf91ef3899fb0ec36863ccd6 in / 
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
	-	`sha256:f898542d1cc6dfc233b10b2c9c711f920b80c44eb0a9c8b0df300ebedc3f27fd`  
		Last Modified: Mon, 01 Sep 2025 23:16:55 GMT  
		Size: 34.4 MB (34443224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fb8a6a11d6a8aa6cb1265b04b48ac3ea54c5e642546199e4ec643364cc84fb`  
		Last Modified: Tue, 02 Sep 2025 00:15:21 GMT  
		Size: 17.6 MB (17624314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875ad18bcf69d0dbbd676132276146b2ba758ce550d4e14bd46b6c372bbc1ab9`  
		Last Modified: Tue, 02 Sep 2025 06:10:41 GMT  
		Size: 132.9 MB (132862983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a06d51daae232b5675e8196c551098aac5e132c5933d3e1638e96fe16d0490`  
		Last Modified: Tue, 02 Sep 2025 00:19:02 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283447e9860e6ae3158a8ac804dece435236a3ce1b26eafe3798f57b9441f68a`  
		Last Modified: Tue, 02 Sep 2025 00:19:03 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2da3c33aea1e83ea0faeab6493bd2c79fae79ad06bad2af62e32b746f6a647d`  
		Last Modified: Tue, 02 Sep 2025 05:54:16 GMT  
		Size: 4.3 KB (4337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4cf562f466e8187025fc28612723f29ed9f9947791b0fa315eb0e29b7be33e`  
		Last Modified: Tue, 02 Sep 2025 05:54:16 GMT  
		Size: 279.6 KB (279550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b21b27d8baf6e87e1e11f2bd7c41ac04564b75655afa0370d8b44e2a7d2598`  
		Last Modified: Tue, 02 Sep 2025 05:54:19 GMT  
		Size: 30.2 MB (30185627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d98ed57e2980ba4346f1cf35e92d20f3f25e40caacffcd3ffac20241cd4c75`  
		Last Modified: Tue, 02 Sep 2025 05:54:16 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:4-jdk11-jammy` - unknown; unknown

```console
$ docker pull groovy@sha256:fff8cb012c74154be435e4473ea10e6032fb09b32b32b602bf275217a29cc1d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a14f5f754afe08e78f8086ebcec2b06d32d4c2b9cb0d8956ceb2461a3e7a71`

```dockerfile
```

-	Layers:
	-	`sha256:a7e7e2cdc3f8a62ce8a5932575ef59f44710bec733fd2116e30d6e6850bf628c`  
		Last Modified: Tue, 02 Sep 2025 08:20:35 GMT  
		Size: 4.1 MB (4083734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7795bde1de81fccdd33d6c391e67d73cfaf63474a4f0c149b742debcc0a64953`  
		Last Modified: Tue, 02 Sep 2025 08:20:35 GMT  
		Size: 28.8 KB (28799 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:4-jdk11-jammy` - linux; s390x

```console
$ docker pull groovy@sha256:acfa513c23b144ad77abc8858476ef5d30f86e84a39bb96e0225092a65fa1dd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.2 MB (200224147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0480a01f8c6eae08b554d7c3785ffa1e80948a5ddbdea75f651b8201985931f5`
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
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
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
	-	`sha256:e4a5a322dd65d010805129ca793d5d5e6b07872cbc2f41d566a84091b39c794e`  
		Last Modified: Thu, 02 Oct 2025 00:25:04 GMT  
		Size: 28.0 MB (28003413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa057040468c4605ce5fb8ed262a9f172e925905b6ab54206a3c9fdecdb0775`  
		Last Modified: Thu, 02 Oct 2025 01:15:00 GMT  
		Size: 16.1 MB (16149615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce49dfda43688a09d6cf57c439418b5ebf83ba65fe87ad84e43093b3ad955a7`  
		Last Modified: Thu, 02 Oct 2025 01:15:09 GMT  
		Size: 125.6 MB (125635817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c2f272f782d172ccb24591764848b655840ac584e767fede4811ae81ee64c4`  
		Last Modified: Thu, 02 Oct 2025 01:14:59 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fab53f9096bfacc6f2d85373844bdabfadc8db1a3f895ad350813072708fd0c`  
		Last Modified: Thu, 02 Oct 2025 01:14:59 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fbd63445bd64ba1f30047bf0851c1e3d96d305fd522c0c53bd943653496bde`  
		Last Modified: Thu, 02 Oct 2025 03:03:55 GMT  
		Size: 4.3 KB (4328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec09c359b14d5dd47c55520a297b9d3434feb1de754451a4653eaca5983d60fb`  
		Last Modified: Thu, 02 Oct 2025 03:03:55 GMT  
		Size: 242.7 KB (242735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:761f8d0942fb97f1607a5eaac31e045081ee36aeae095a673278272652f4a9e6`  
		Last Modified: Thu, 02 Oct 2025 03:03:58 GMT  
		Size: 30.2 MB (30185630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954991d5a3dc79e01dc312dadbf94d5f984c8c22e39f04b6ff4a2ac78c13a78f`  
		Last Modified: Thu, 02 Oct 2025 03:03:55 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:4-jdk11-jammy` - unknown; unknown

```console
$ docker pull groovy@sha256:1b633b400fd8bbe52dc472e7b5792907642199f91ad8a8af649f6cce96216d44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4107984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c148e0d243105825b639c66e3480de4ade08e59641ae33c59b2403c75c7283e`

```dockerfile
```

-	Layers:
	-	`sha256:19267b1a73deabb5a3547797ffe1c252489cf2d7324862be9f7d584d868decc8`  
		Last Modified: Thu, 02 Oct 2025 05:21:06 GMT  
		Size: 4.1 MB (4079307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:854c017db5d8fed92b1287afbb2a674697c2c8518ecd9a710f85ae4182f56b61`  
		Last Modified: Thu, 02 Oct 2025 05:21:07 GMT  
		Size: 28.7 KB (28677 bytes)  
		MIME: application/vnd.in-toto+json
