## `maven:3-eclipse-temurin-8`

```console
$ docker pull maven@sha256:4a5513acee5d1da132d45adcc747084421e3b26d99a321ef4d5a7287001c42e5
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

### `maven:3-eclipse-temurin-8` - linux; amd64

```console
$ docker pull maven@sha256:f4b699fa67057fe696e4829f90f303fc3d5e33ed36d8a17daa41fc7f2aa7b5d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133740360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f96b0f8edc5846c3e9f9361b21b2b8a376795d607cc531101f26f23d72ff97bf`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:51:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 01:51:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:51:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:51:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:51:28 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 07 Apr 2026 01:51:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='1d0d16394e2fe637f9eb8e73e63ea6fe9ceee98337c0527aa058cee777ad638a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 07 Apr 2026 01:51:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 01:51:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:51:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 05:06:35 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:06:35 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 07 Apr 2026 05:06:35 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:06:35 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:06:35 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 07 Apr 2026 05:06:35 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 07 Apr 2026 05:06:35 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 07 Apr 2026 05:06:35 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 07 Apr 2026 05:06:35 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 07 Apr 2026 05:06:36 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 07 Apr 2026 05:06:36 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 07 Apr 2026 05:06:36 GMT
ARG USER_HOME_DIR=/root
# Tue, 07 Apr 2026 05:06:36 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 07 Apr 2026 05:06:36 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 07 Apr 2026 05:06:36 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df075017d15135f960163de725cc6ee6f3dff47ddd56d95e2cc4211fd70f8d09`  
		Last Modified: Tue, 07 Apr 2026 01:51:45 GMT  
		Size: 17.0 MB (16983570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4ed7a05f34e2ef36cf7507be1c1e7dfcb1af10176a7b75e7d53ce5f5bdee56`  
		Last Modified: Tue, 07 Apr 2026 01:51:46 GMT  
		Size: 55.2 MB (55173034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1ae502b02605c95e2c151a6ec6dd824cf02ee8982afe38501277f9fd6cab87`  
		Last Modified: Tue, 07 Apr 2026 01:51:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616f3967b6044708defa9338a4f6e7fc39f76bb62094c84c83729d4f76e7e892`  
		Last Modified: Tue, 07 Apr 2026 01:51:44 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779d0471d2e6db5b257ef369b1a07501d6e4f76fee0f1da610013629741d4c56`  
		Last Modified: Tue, 07 Apr 2026 05:06:46 GMT  
		Size: 22.5 MB (22535637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0052024213d0d7e42a456b5535bd6d821af2e9e35d782d2f1e69625f1da3dd57`  
		Last Modified: Tue, 07 Apr 2026 05:06:46 GMT  
		Size: 9.3 MB (9311190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3ab5f1baec8ae435871a67645de0931cceba7098c8c6edef3513055d07c71f`  
		Last Modified: Tue, 07 Apr 2026 05:06:45 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8900ff78abd00b0803794304f81123c00af9c46a34a545c3d7378637c58d23f8`  
		Last Modified: Tue, 07 Apr 2026 05:06:46 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-8` - unknown; unknown

```console
$ docker pull maven@sha256:f768231917f3cc034ac4b051cb458ba99651bcf90986454abecabea5690f642e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5035326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aa48f4f40c4fbacd2a2d4b28d1e624099ccaf76c896a8533cffd0274ab34db8`

```dockerfile
```

-	Layers:
	-	`sha256:8eee5f5610e7d51df2d8a857566e11385d4250b0b68372389b6dcc10e66c3fe7`  
		Last Modified: Tue, 07 Apr 2026 05:06:46 GMT  
		Size: 5.0 MB (5014662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1461c1306be055a5736df1f28c55f880eb26dd397690fd7de336947e80564dd`  
		Last Modified: Tue, 07 Apr 2026 05:06:45 GMT  
		Size: 20.7 KB (20664 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-8` - linux; arm variant v7

```console
$ docker pull maven@sha256:26c7c2d4e336325e84fff38151468d1240459035ab8ea7ab5299bae2725f71e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.3 MB (130288672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f8be57a22eb98b344e1e88b696926d58b1e4c61b3d6956253745a0967973fb4`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 03 Apr 2026 15:14:30 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:14:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:14:31 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:14:34 GMT
ADD file:68e3febb1e8418fa8ce83073bfbf6ec7236d81e7c8781177d7295e5adce34436 in / 
# Fri, 03 Apr 2026 15:14:34 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:06:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 02:06:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:06:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 02:06:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:06:09 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 07 Apr 2026 02:06:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='1d0d16394e2fe637f9eb8e73e63ea6fe9ceee98337c0527aa058cee777ad638a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 07 Apr 2026 02:06:24 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 02:06:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 02:06:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 04:36:32 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:36:33 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 07 Apr 2026 04:36:33 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 04:36:33 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 04:36:33 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 07 Apr 2026 04:36:33 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 07 Apr 2026 04:36:33 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 07 Apr 2026 04:36:33 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 07 Apr 2026 04:36:33 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 07 Apr 2026 04:36:33 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 07 Apr 2026 04:36:33 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 07 Apr 2026 04:36:33 GMT
ARG USER_HOME_DIR=/root
# Tue, 07 Apr 2026 04:36:33 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 07 Apr 2026 04:36:33 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 07 Apr 2026 04:36:33 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d7d21bc3f0364f0d98c41b0bcda87b8f2bfbf1688f75f6322ed679752a149163`  
		Last Modified: Fri, 03 Apr 2026 15:56:43 GMT  
		Size: 26.9 MB (26858365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3d545bd3a100e6b840cfe6a8546189d669abd93c99329b5cd3553567986cb7`  
		Last Modified: Tue, 07 Apr 2026 02:06:36 GMT  
		Size: 16.3 MB (16309786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb15d10aa0c606cc3c8eaf3216083668265fca997db4982ec5f965ec20c8fb6`  
		Last Modified: Tue, 07 Apr 2026 02:06:39 GMT  
		Size: 50.5 MB (50534176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26252a58ff8b82b7cff7ac1300a386d64a7abf44630add6927841898d08f5fe`  
		Last Modified: Tue, 07 Apr 2026 02:06:35 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6491bc4ad2141a89cd72872182dbe361742ecbe1f5802dcd8bc8f46c64e126fa`  
		Last Modified: Tue, 07 Apr 2026 02:06:36 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f9eda3a53e914a6b1cce90221d72aeb28d9badf8d34b2eeca0ff13b0ffe7db`  
		Last Modified: Tue, 07 Apr 2026 04:36:47 GMT  
		Size: 27.3 MB (27271698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e9453500224e24981f1da23bcc7c256e013a88f229c296af41fa75ed9e4ddc`  
		Last Modified: Tue, 07 Apr 2026 04:36:46 GMT  
		Size: 9.3 MB (9311179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e3dbb693b51fda734f22bd1500bff16efa557035d7eb57467c99f0689d92b3`  
		Last Modified: Tue, 07 Apr 2026 04:36:46 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695c742c12d7878bf23ac548a7fd5f71a3116c23a0d58f934a94298155203d50`  
		Last Modified: Tue, 07 Apr 2026 04:36:46 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-8` - unknown; unknown

```console
$ docker pull maven@sha256:292731e9d7ce601c2ad38a25bd2c5e82858e29753e25763223e658add4825556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5038208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d704d68390b1b9a170598f57bfc5b848e6084dbf23ff47a1c7abc612ac7a019c`

```dockerfile
```

-	Layers:
	-	`sha256:405f98f1fcd607867744709ac808d566472c2ba697d435fe70c2c1a56193fdb1`  
		Last Modified: Tue, 07 Apr 2026 04:36:46 GMT  
		Size: 5.0 MB (5017414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b976357627ed5ed8cf703043e4bafd1ad42c3846b7a8594a903fcecf3969fe35`  
		Last Modified: Tue, 07 Apr 2026 04:36:46 GMT  
		Size: 20.8 KB (20794 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:26ed3ba0deb6cef84379de9ffd399eaacbfe5437b81aa464fc2559033abd3ec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132051552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:277dc7ea5fe2a84a41a7e18975ff7a1662f965cdd73422eec66c172f20db6915`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:54:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 01:54:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:54:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:54:52 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:54:52 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 07 Apr 2026 01:54:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='1d0d16394e2fe637f9eb8e73e63ea6fe9ceee98337c0527aa058cee777ad638a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 07 Apr 2026 01:54:55 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 01:54:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:54:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 05:12:07 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:12:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 07 Apr 2026 05:12:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:12:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:12:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 07 Apr 2026 05:12:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 07 Apr 2026 05:12:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 07 Apr 2026 05:12:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 07 Apr 2026 05:12:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 07 Apr 2026 05:12:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 07 Apr 2026 05:12:08 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 07 Apr 2026 05:12:08 GMT
ARG USER_HOME_DIR=/root
# Tue, 07 Apr 2026 05:12:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 07 Apr 2026 05:12:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 07 Apr 2026 05:12:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0738e80beda892add763f8343b2d18f0db5b9faee5a996058a9edfd5f7705a`  
		Last Modified: Tue, 07 Apr 2026 01:55:08 GMT  
		Size: 17.0 MB (16996230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbda5becb75a3625bbff099e0aeafb79c9cebee747aa564170617e51a803e4b`  
		Last Modified: Tue, 07 Apr 2026 01:55:09 GMT  
		Size: 54.3 MB (54261010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1ce28e9fc87f52ed90bd740f3a80449a8e5d78ab2814fd0015e43ab0c78a87`  
		Last Modified: Tue, 07 Apr 2026 01:55:06 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b285e0b7720e0fcc67055866167f744eb6708aef8d94536dea3273cd76a0027a`  
		Last Modified: Tue, 07 Apr 2026 01:55:07 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0312668ca1bf85d8532f8d4d22808aeaaa469dfc8569bb02b72e6d71281b3ebd`  
		Last Modified: Tue, 07 Apr 2026 05:12:20 GMT  
		Size: 22.6 MB (22605583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0d414e3a8526f4cff550aaab3da62355c08b98593bc39bf537c6300e4d6178`  
		Last Modified: Tue, 07 Apr 2026 05:12:20 GMT  
		Size: 9.3 MB (9311185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10192f6dd04a2c2ca7a5a50ce0a9945bce1feaf0430b9b1ed041d6152c2097f5`  
		Last Modified: Tue, 07 Apr 2026 05:12:19 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74fb9a11604b7aa437a1847ac004de4b0f22a60e13548734ebb08d733d2bfc2a`  
		Last Modified: Tue, 07 Apr 2026 05:12:19 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-8` - unknown; unknown

```console
$ docker pull maven@sha256:48fce5e527d58aee6e966f57af10be37bceb2ffd77834b94762b43a5f3482037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5042743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d005a7e1b4a62b086327165e7c3bdec57fdc9866263bfa5bab5d06a4fc9601`

```dockerfile
```

-	Layers:
	-	`sha256:effca0e1635e117abf3e6e65648331137b263773d7d03ae764c9428c8492832b`  
		Last Modified: Tue, 07 Apr 2026 05:12:20 GMT  
		Size: 5.0 MB (5021909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d19265bfaf95047014923ba6ca768bcbf6d4d9e25758e9a23cf509dd7d48dd3`  
		Last Modified: Tue, 07 Apr 2026 05:12:19 GMT  
		Size: 20.8 KB (20834 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-8` - linux; ppc64le

```console
$ docker pull maven@sha256:ff32c47b07837af573fc57d77832542ffb47de90defe870d2dc9f847f43104d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141675826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ba0837761a56bb84e99f6740e9901ae97d55e0643283581699bfb2f6d4649d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 23 Feb 2026 17:18:33 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:18:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:18:36 GMT
ADD file:2a89eb67bf550d9680999e3ff99dbaa17c251b6c343a241318e879a26da53fca in / 
# Mon, 23 Feb 2026 17:18:37 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 08:29:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 08:29:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 08:29:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 08:29:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 08:29:49 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 17 Mar 2026 08:29:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='1d0d16394e2fe637f9eb8e73e63ea6fe9ceee98337c0527aa058cee777ad638a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 17 Mar 2026 08:29:54 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 08:29:55 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 08:29:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Mar 2026 22:05:00 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 22:05:01 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Mar 2026 22:05:01 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 22:05:01 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 22:05:01 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Mar 2026 22:05:01 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Mar 2026 22:05:01 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Mar 2026 22:05:01 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 22:05:02 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Mar 2026 22:05:02 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Mar 2026 22:05:02 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 17 Mar 2026 22:05:02 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Mar 2026 22:05:02 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Mar 2026 22:05:02 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Mar 2026 22:05:02 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f826c9b754a00ada9d9335ffdf3ffd40f6925a3223caac76cc429823b8621f9e`  
		Last Modified: Mon, 23 Feb 2026 17:51:39 GMT  
		Size: 34.3 MB (34310051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c602d6d5b3bff268e7b1f1815099c69255c8fca8953f0d22e169ed8acd2c409c`  
		Last Modified: Tue, 17 Mar 2026 08:30:26 GMT  
		Size: 18.8 MB (18813047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96aec3e5db94d0faab4622f1d80bab547ecb0d60f584ca842375a83e99952830`  
		Last Modified: Tue, 17 Mar 2026 08:30:27 GMT  
		Size: 52.7 MB (52652123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a066d0afd44ccebf44530b4221ac6fa866c3f7b71f100815137c14a0c0d409d`  
		Last Modified: Tue, 17 Mar 2026 08:30:24 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5e40d2ab2cccf9a8444d933642f74171d202e74cbbcc770d1e70095f842bca`  
		Last Modified: Tue, 17 Mar 2026 08:30:25 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c0f48482a03ee03dfe7afa924666743df96d019c8acbdd2b491775bace4fc7`  
		Last Modified: Tue, 17 Mar 2026 22:05:31 GMT  
		Size: 26.6 MB (26585957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0acd081442ec5f4a33f04122517baa7192d280e5ee4ab295cb647b62105cdb5`  
		Last Modified: Tue, 17 Mar 2026 22:05:31 GMT  
		Size: 9.3 MB (9311176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7f0b888af0cf4d3c4c7412ede572936bac7b47e19ddc958c76b8034d3ea715`  
		Last Modified: Tue, 17 Mar 2026 22:05:30 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b893c8555d73fbf71f6c798826bc0dbe1975389a277ba1615152ef96e860b6`  
		Last Modified: Tue, 17 Mar 2026 22:05:30 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-8` - unknown; unknown

```console
$ docker pull maven@sha256:2724ee4ebdd0038c84530ea13ceb4251c73cb7b6487fb699da5cbfe1ffbcc09b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5040940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c4dbad2a4598b83e9dcb7e5d8c01fc963fd4d616987d7ba508dd1b7b119e6d6`

```dockerfile
```

-	Layers:
	-	`sha256:cea20b25e5c66773bd6a7e148a5270182826579f93aa8dfead9778dc23fa39e3`  
		Last Modified: Tue, 17 Mar 2026 22:05:30 GMT  
		Size: 5.0 MB (5020207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:434fb83853534f6ff75274ac443513ca0a9bbe5aa6a6f155c398429a64636670`  
		Last Modified: Tue, 17 Mar 2026 22:05:30 GMT  
		Size: 20.7 KB (20733 bytes)  
		MIME: application/vnd.in-toto+json
