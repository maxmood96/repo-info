## `groovy:jdk8-jammy`

```console
$ docker pull groovy@sha256:09ec9df84d4339ce755f2a79c213e6d2933b221a1b2bbab6242036807366cd81
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `groovy:jdk8-jammy` - linux; amd64

```console
$ docker pull groovy@sha256:21e99d282d904c1a8d2102210d142cd77ea653441aca10cf30935d35add1d17f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131640310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938411f4ba6fe234a8fcca15027cf2fef381a2292c2ca3be076440e4efaa17b1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:32:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:32:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:32:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:32:21 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:32:21 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Wed, 15 Apr 2026 20:32:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='1d0d16394e2fe637f9eb8e73e63ea6fe9ceee98337c0527aa058cee777ad638a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Wed, 15 Apr 2026 20:32:25 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:32:25 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:32:25 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 21:33:07 GMT
CMD ["groovysh"]
# Wed, 15 Apr 2026 21:33:07 GMT
ENV GROOVY_HOME=/opt/groovy
# Wed, 15 Apr 2026 21:33:07 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Wed, 15 Apr 2026 21:33:07 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Wed, 15 Apr 2026 21:33:07 GMT
WORKDIR /home/groovy
# Wed, 15 Apr 2026 21:33:13 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:33:13 GMT
ENV GROOVY_VERSION=4.0.30
# Wed, 15 Apr 2026 21:33:20 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
USER 1000:1000
# Wed, 15 Apr 2026 21:33:20 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b699ac82f8f4bc202667b93bb403fa63a9d1637ce1f8fa60f2e6adceb8bf6be8`  
		Last Modified: Wed, 15 Apr 2026 20:32:38 GMT  
		Size: 16.2 MB (16150818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dfae8fec46c3d37535117b69a93963943ff3e3de751e2aa89287f69ec47171a`  
		Last Modified: Wed, 15 Apr 2026 20:32:39 GMT  
		Size: 55.2 MB (55172941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d393a668fd7abdb353104b0fce5968b214d5ac3ff3cbb65251bdfe6116b21b`  
		Last Modified: Wed, 15 Apr 2026 20:32:33 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2b0e71db5598e689453f02b98ac96955ee8ed91cbe61b6272a4122020be927`  
		Last Modified: Wed, 15 Apr 2026 20:32:37 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0938881418eda9bbea733b9161817f014fcf46018a1091a41500eb1e62a6dde2`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 4.3 KB (4333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b53b64601ff613635947f9f1be293251c9deac83155615ad19199d5c58e6f3f`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 244.6 KB (244593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1158b188b8202bd62a59ed466b5865cc7926f0e667b2553b2b8de7f6a6de2c`  
		Last Modified: Wed, 15 Apr 2026 21:33:31 GMT  
		Size: 30.3 MB (30328524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5290c8fafcaa0c86fc2b898095aa234997de418d217ea172f800116fe39ee666`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk8-jammy` - unknown; unknown

```console
$ docker pull groovy@sha256:f11a1f32c01d35fbb316af249f553550a70cc318dc5b3e757b0f9fea56f8e4af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4207261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5691ba938d231383b6930bd39fa82933a1edae95bc4212b5d60da85df29ebb3`

```dockerfile
```

-	Layers:
	-	`sha256:a5f2d1f809cc4e4f199b61bec3e3d2fbc0dc821027ec3547858cd1a3b06542a8`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 4.2 MB (4181761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb8d9513e8568cabb1856c9a64308c02f6dc2f11d20c6c1c01b70b8a3821c4f5`  
		Last Modified: Wed, 15 Apr 2026 21:33:30 GMT  
		Size: 25.5 KB (25500 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:jdk8-jammy` - linux; arm variant v7

```console
$ docker pull groovy@sha256:9996c83da397f1a376de1a88db970d81a7a07583f1024ca81821595b071303d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123841139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfcd07f08a7ffc4f1d70da4d71413af1e55bb697bbba6a314fdc8a6677c12833`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Fri, 10 Apr 2026 09:44:44 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:44:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:44:44 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:44:47 GMT
ADD file:cf79b3b81bc9aa60d93ec4cfb803894aca6ed3d1e7c9ed02435158c6c0de400b in / 
# Fri, 10 Apr 2026 09:44:47 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:32:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:32:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:32:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:32:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:32:02 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Wed, 15 Apr 2026 20:32:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='1d0d16394e2fe637f9eb8e73e63ea6fe9ceee98337c0527aa058cee777ad638a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Wed, 15 Apr 2026 20:32:14 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:32:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:32:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 21:35:00 GMT
CMD ["groovysh"]
# Wed, 15 Apr 2026 21:35:00 GMT
ENV GROOVY_HOME=/opt/groovy
# Wed, 15 Apr 2026 21:35:00 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Wed, 15 Apr 2026 21:35:00 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Wed, 15 Apr 2026 21:35:00 GMT
WORKDIR /home/groovy
# Wed, 15 Apr 2026 21:35:07 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:35:07 GMT
ENV GROOVY_VERSION=4.0.30
# Wed, 15 Apr 2026 21:35:25 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy # buildkit
# Wed, 15 Apr 2026 21:35:25 GMT
USER 1000:1000
# Wed, 15 Apr 2026 21:35:26 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:f1c61368409f262f2b51173bb83056489f63f356da65ec1d7227c4451afc7ff0`  
		Last Modified: Fri, 10 Apr 2026 11:01:03 GMT  
		Size: 26.8 MB (26841687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f750b5c6da26ec8a09bcce448a8aebc0a81b55b292a25188f051c044915fca50`  
		Last Modified: Wed, 15 Apr 2026 20:32:27 GMT  
		Size: 15.9 MB (15891805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e09588e5014699965a92b7a01371ef9cf79045200bf24ea5b76f4f43ebbdff6`  
		Last Modified: Wed, 15 Apr 2026 20:32:28 GMT  
		Size: 50.5 MB (50540900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411ddcc9a3dfc4a57e42925f5f96c4900bd02674ed5dd63edca20ce92fc63cfb`  
		Last Modified: Wed, 15 Apr 2026 20:32:26 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae031066b3a5e6b7433292761ddf81f944533e2d172fb207fb5f90dc35b2288b`  
		Last Modified: Wed, 15 Apr 2026 20:32:26 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d1f06a054d7408ee19a43fd87e4e835a00cee1a320170d413cfea09d8b47ba`  
		Last Modified: Wed, 15 Apr 2026 21:35:35 GMT  
		Size: 4.3 KB (4315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66a004bdfc38f7bba2b8bc57c5082e5b0b1e4f8f1f44fb6bcb10fd3ae20f9d7`  
		Last Modified: Wed, 15 Apr 2026 21:35:35 GMT  
		Size: 231.3 KB (231305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d8c300f2fa8eecd6905ea59f899064e418288f61aef22040447042b30bd1ba`  
		Last Modified: Wed, 15 Apr 2026 21:35:35 GMT  
		Size: 30.3 MB (30328525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f575415b0764ca37883f95d3d93ca0ceacb29c7dd637c8d8f58468702db2042`  
		Last Modified: Wed, 15 Apr 2026 21:35:35 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk8-jammy` - unknown; unknown

```console
$ docker pull groovy@sha256:c361587a577f362b3aa1410873166bda42918b24be8c65d3d7e568e4d87102c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4211452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6179756e88ac805fce2a3a98a4200cef74fdff05ffbcca06dcf0f50364b1720`

```dockerfile
```

-	Layers:
	-	`sha256:ccb20bac423164dbbe727375024866b85367204691f7976b5e981fe368ab303c`  
		Last Modified: Wed, 15 Apr 2026 21:35:35 GMT  
		Size: 4.2 MB (4185800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbbd142f5ae3bd44fd54027e5fed4520b354175653d3170213a9143bda9f1aac`  
		Last Modified: Wed, 15 Apr 2026 21:35:35 GMT  
		Size: 25.7 KB (25652 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:jdk8-jammy` - linux; arm64 variant v8

```console
$ docker pull groovy@sha256:a8e16f1f622aa12f5abda47b9e0b669365efe72f01c6b2a70c68752582552226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128519808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ea95168b8718dfed95416fde464ddb559b2c76dff01522c1f4d85f2ad431d6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:32:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:32:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:32:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:32:43 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:32:43 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Wed, 15 Apr 2026 20:32:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='1d0d16394e2fe637f9eb8e73e63ea6fe9ceee98337c0527aa058cee777ad638a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Wed, 15 Apr 2026 20:32:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:32:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:32:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 21:46:16 GMT
CMD ["groovysh"]
# Wed, 15 Apr 2026 21:46:16 GMT
ENV GROOVY_HOME=/opt/groovy
# Wed, 15 Apr 2026 21:46:16 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Wed, 15 Apr 2026 21:46:16 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Wed, 15 Apr 2026 21:46:16 GMT
WORKDIR /home/groovy
# Wed, 15 Apr 2026 21:46:23 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:46:23 GMT
ENV GROOVY_VERSION=4.0.30
# Wed, 15 Apr 2026 21:46:30 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy # buildkit
# Wed, 15 Apr 2026 21:46:30 GMT
USER 1000:1000
# Wed, 15 Apr 2026 21:46:31 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a116ac60a9bda7df2aa8d5f8c599e43b76fc505884b313fa5a950252ed9b69`  
		Last Modified: Wed, 15 Apr 2026 20:33:00 GMT  
		Size: 16.1 MB (16075202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53614aca3bb32d1a5095ef396c08b4a7292999ad4a296c5ef9f8a53222ae5e3b`  
		Last Modified: Wed, 15 Apr 2026 20:33:01 GMT  
		Size: 54.3 MB (54261216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88e93f626800c3e743b24f70c0f766f3debe0ba6f4fe4007f364e298391e35b`  
		Last Modified: Wed, 15 Apr 2026 20:32:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f626c4297327dd6abfea8f0acb8ea0be823687a7a4e4f87e1cceb14b277b937e`  
		Last Modified: Wed, 15 Apr 2026 20:32:59 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85b48256fe9bc1d6d430d4fb8fdbd299eab36db56c32ef09987f57eae3f315c`  
		Last Modified: Wed, 15 Apr 2026 21:46:40 GMT  
		Size: 4.3 KB (4333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35214c93d824ed0f1bde095070a0725a8cb135318ad869ac18f50f36ab099e82`  
		Last Modified: Wed, 15 Apr 2026 21:46:40 GMT  
		Size: 241.4 KB (241387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a1b4f12d9585cd337f3ac27dfe7a351788db688f8d9065ec6b5af001d6862c`  
		Last Modified: Wed, 15 Apr 2026 21:46:41 GMT  
		Size: 30.3 MB (30328523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf77d50fa23eeac377d7a8cd31d203a810c565d25dcadc79176685c9d119ff2`  
		Last Modified: Wed, 15 Apr 2026 21:46:40 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk8-jammy` - unknown; unknown

```console
$ docker pull groovy@sha256:71887c59c60bc7a9880cded823a88acdb829bfff0e295583fb5f9e894ed4c7d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4207887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf3aa9ed874e6ff6a32c0b1894c5d60a98a95b54f6a2704d2613d6ecd053388`

```dockerfile
```

-	Layers:
	-	`sha256:ad0e06bf956b09c0c75f3576ee96733b02d10c6046318a626b756782c407fb14`  
		Last Modified: Wed, 15 Apr 2026 21:46:41 GMT  
		Size: 4.2 MB (4182189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dd85280c452a80f8521578745af948f4421a7dc8fd5e7b2a26b96a8a2d44fa3`  
		Last Modified: Wed, 15 Apr 2026 21:46:40 GMT  
		Size: 25.7 KB (25698 bytes)  
		MIME: application/vnd.in-toto+json

### `groovy:jdk8-jammy` - linux; ppc64le

```console
$ docker pull groovy@sha256:f7b9a735ee8fc5ddf428275d17da8ec1e7c976fa0fcb743759fc6d01e8d76d23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135539055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba76a1b1dcc80838e25964eda8c28b5143d4ae4fc1d9e60c0a8e4a3d57b6e890`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:14:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 21:14:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:14:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 21:14:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:14:32 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Wed, 15 Apr 2026 21:14:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='1d0d16394e2fe637f9eb8e73e63ea6fe9ceee98337c0527aa058cee777ad638a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Wed, 15 Apr 2026 21:14:40 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 21:14:40 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:14:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 16 Apr 2026 00:40:44 GMT
CMD ["groovysh"]
# Thu, 16 Apr 2026 00:40:44 GMT
ENV GROOVY_HOME=/opt/groovy
# Thu, 16 Apr 2026 00:40:44 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy # buildkit
# Thu, 16 Apr 2026 00:40:44 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Thu, 16 Apr 2026 00:40:44 GMT
WORKDIR /home/groovy
# Thu, 16 Apr 2026 00:40:50 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/* # buildkit
# Thu, 16 Apr 2026 00:40:50 GMT
ENV GROOVY_VERSION=4.0.30
# Thu, 16 Apr 2026 00:40:59 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy # buildkit
# Thu, 16 Apr 2026 00:40:59 GMT
USER 1000:1000
# Thu, 16 Apr 2026 00:41:01 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version # buildkit
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fb6b0270a1e57e97f5a37840672246e903f6d765edf38fbdc976c403a8074e`  
		Last Modified: Wed, 15 Apr 2026 21:15:05 GMT  
		Size: 17.6 MB (17623543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d080b0776c5470b9b7363d562845f4a2d108db9584306e033d1804ec07e66b2`  
		Last Modified: Wed, 15 Apr 2026 21:15:07 GMT  
		Size: 52.7 MB (52652114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bafc2f71390ebd72287a79ba7403ca6f74221fa90f85089aeb5edad1228491d4`  
		Last Modified: Wed, 15 Apr 2026 21:15:04 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52426cfe78887257801b6b7d1a0152e3cddaa78d880186fc6a1a042b1b6445c9`  
		Last Modified: Wed, 15 Apr 2026 21:15:04 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9815599c27571454729c83ac3a04385dbaf198bb0fe48ec2e24c390715e0dc31`  
		Last Modified: Thu, 16 Apr 2026 00:41:23 GMT  
		Size: 4.3 KB (4330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61875d8bd4585b700c31f461436de6fa6536a96d5d911fbb29c28151f668024`  
		Last Modified: Thu, 16 Apr 2026 00:41:24 GMT  
		Size: 279.5 KB (279544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a630829f2243738fdd13f0d3fbccdc40409a29198ca985c1eb21b5341b0f5c80`  
		Last Modified: Thu, 16 Apr 2026 00:41:26 GMT  
		Size: 30.3 MB (30328526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4566b56fc2515c162f3e57c8ae7a9333a7302d5bf32051998238c940e47b527`  
		Last Modified: Thu, 16 Apr 2026 00:41:24 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `groovy:jdk8-jammy` - unknown; unknown

```console
$ docker pull groovy@sha256:f9bd84ca01811b2312346747dca27cc79c1a1d10ee4e66a8ab27a08be5e1aa4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4210121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce6dcf9eedd1eb22b8bca64e176da8de8912537aecaaca4fe9ece4ae6ddbfbf`

```dockerfile
```

-	Layers:
	-	`sha256:411307ac660a9ab703d74cc8a6bc921d46565cdec3f0a2f028a56410b28691cf`  
		Last Modified: Thu, 16 Apr 2026 00:41:24 GMT  
		Size: 4.2 MB (4184546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:154299cb1eddb36df32fd05638d4b03b9b0b9933188a7dc8d53e4aaea07f6556`  
		Last Modified: Thu, 16 Apr 2026 00:41:23 GMT  
		Size: 25.6 KB (25575 bytes)  
		MIME: application/vnd.in-toto+json
