## `gradle:9-jdk17-ubi10`

```console
$ docker pull gradle@sha256:99222b43e84028892b3f5917d268bea0757e93378b89cbb215d07aef780f7ea9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `gradle:9-jdk17-ubi10` - linux; amd64

```console
$ docker pull gradle@sha256:4a2bf08cca6b1ff68054218dcf23111f2e6aa3754059f9f615d2557e3a112c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.1 MB (397137143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c91b141fce069965402e6881426aa7463e80c790526d1bdf4eaea4b2b4837ebf`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 06 May 2026 09:10:13 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 06 May 2026 09:10:13 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 06 May 2026 09:10:13 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 06 May 2026 09:10:13 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 06 May 2026 09:10:13 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 06 May 2026 09:10:13 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 06 May 2026 09:10:13 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 09:10:13 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 09:10:13 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 06 May 2026 09:10:13 GMT
LABEL io.openshift.expose-services=""
# Wed, 06 May 2026 09:10:13 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 06 May 2026 09:10:13 GMT
ENV container oci
# Wed, 06 May 2026 09:10:13 GMT
COPY dir:c68dbe05133c31f8fd9f151252a4a29ce3fdd8d44060b74e88191790dd574dbf in /      
# Wed, 06 May 2026 09:10:13 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 06 May 2026 09:10:14 GMT
CMD ["/bin/bash"]
# Wed, 06 May 2026 09:10:14 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 06 May 2026 09:10:14 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 06 May 2026 09:10:14 GMT
COPY file:878ce3a57b93d24e6852d17b3cb65931afbc773f95f9596e50dac7b8ef938cc4 in /usr/share/buildinfo/labels.json      
# Wed, 06 May 2026 09:10:14 GMT
COPY file:878ce3a57b93d24e6852d17b3cb65931afbc773f95f9596e50dac7b8ef938cc4 in /root/buildinfo/labels.json      
# Wed, 06 May 2026 09:10:14 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="bf211293690f866639ec8b5930bb28589978ee3f" "org.opencontainers.image.revision"="bf211293690f866639ec8b5930bb28589978ee3f" "build-date"="2026-05-06T09:09:57Z" "org.opencontainers.image.created"="2026-05-06T09:09:57Z" "release"="1778058333"org.opencontainers.image.revision=bf211293690f866639ec8b5930bb28589978ee3f,org.opencontainers.image.created=2026-05-06T09:09:57Z
# Fri, 08 May 2026 16:20:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 16:20:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 16:20:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 May 2026 16:20:55 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 08 May 2026 16:20:55 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 08 May 2026 16:21:01 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 08 May 2026 16:21:02 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 16:21:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 16:21:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 16:21:02 GMT
CMD ["jshell"]
# Fri, 08 May 2026 16:37:57 GMT
CMD ["gradle"]
# Fri, 08 May 2026 16:37:57 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 May 2026 16:37:57 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 08 May 2026 16:37:57 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 May 2026 16:37:57 GMT
WORKDIR /home/gradle
# Fri, 08 May 2026 16:38:02 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 08 May 2026 16:38:02 GMT
ENV GRADLE_VERSION=9.5.0
# Fri, 08 May 2026 16:38:02 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Fri, 08 May 2026 16:38:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 08 May 2026 16:38:05 GMT
USER gradle
# Fri, 08 May 2026 16:38:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 08 May 2026 16:38:05 GMT
USER root
```

-	Layers:
	-	`sha256:92d62aafb6a18663d52e4aabc1138a75b2e6994c38e927e9099cb078cc22e6b7`  
		Last Modified: Wed, 06 May 2026 10:14:33 GMT  
		Size: 34.6 MB (34621721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212c78130b95b82c3274218b7f781c8de8a6ddd9044ed3cbacccd8daf28fa9be`  
		Last Modified: Fri, 08 May 2026 16:21:19 GMT  
		Size: 37.5 MB (37499076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70232a01b7df5c229991f7f63a3efc90b11ed5493ffcc18471c43931afcb68e2`  
		Last Modified: Fri, 08 May 2026 16:21:21 GMT  
		Size: 145.9 MB (145915482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc89d4ef50a24e910eb18cb626bffbcb96f91274cdcda23fa0a60be79b131710`  
		Last Modified: Fri, 08 May 2026 16:21:17 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fdfcf0272b56443ff95d00943eda92e4eebb32cd51f0273ee21f603a7200a8d`  
		Last Modified: Fri, 08 May 2026 16:21:02 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4723424810ba9ae0ab565b519a31320f286128d48f6c2367ac73e98f39721160`  
		Last Modified: Fri, 08 May 2026 16:38:24 GMT  
		Size: 1.6 KB (1584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d7ad45af33cab3c4b2a7ac279915a17b5a7346f25f77a823565b62c4270893`  
		Last Modified: Fri, 08 May 2026 16:38:26 GMT  
		Size: 38.8 MB (38835271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ad0bd3322de4e140e011327207e6b7955e771a981a7c93ba7273813197a0aa`  
		Last Modified: Fri, 08 May 2026 16:38:29 GMT  
		Size: 140.2 MB (140235941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355bb27293044e708491e011b7d5c588ee429cc163cad990bbe2eb58b714771e`  
		Last Modified: Fri, 08 May 2026 16:38:24 GMT  
		Size: 25.6 KB (25615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:05b399c45d4488cc28da0d0b27a9207d63da4c4f89a81d2d71b2d4ffad51a313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7080983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c39639a04e49d1fed49aa8bcf0e704f8f29812680eec50667f0e940f178e3f5c`

```dockerfile
```

-	Layers:
	-	`sha256:f5d39859ec98d7f1eac959568e3776472c0ed1030dfee59e8fbe86e41f40a58e`  
		Last Modified: Fri, 08 May 2026 16:38:24 GMT  
		Size: 7.1 MB (7056528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c49353619f3c9313896ba19598162e399a4b8e6fe473406f93fa3b15abb30a6`  
		Last Modified: Fri, 08 May 2026 16:38:24 GMT  
		Size: 24.5 KB (24455 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-ubi10` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:85526a42b143832f8b751df1389a682374cae7f76c1b1b23091a7ea83a1fc739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.5 MB (393515975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6529ade9b49d24d822dddab25b6273ddac464a2c4efb63a6f2dfa79cca15d84f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 06 May 2026 09:13:03 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 06 May 2026 09:13:03 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 06 May 2026 09:13:03 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 06 May 2026 09:13:03 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 06 May 2026 09:13:03 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 06 May 2026 09:13:03 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 06 May 2026 09:13:03 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 09:13:03 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 09:13:03 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 06 May 2026 09:13:03 GMT
LABEL io.openshift.expose-services=""
# Wed, 06 May 2026 09:13:03 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 06 May 2026 09:13:03 GMT
ENV container oci
# Wed, 06 May 2026 09:13:04 GMT
COPY dir:750bbe41da49fc0c3224e4824b23b1c35d4c73f39652b46f248f5dd9cad107de in /      
# Wed, 06 May 2026 09:13:04 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 06 May 2026 09:13:04 GMT
CMD ["/bin/bash"]
# Wed, 06 May 2026 09:13:04 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 06 May 2026 09:13:04 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 06 May 2026 09:13:05 GMT
COPY file:2221d5e6d5258b2c2c2c5ff82716a8550cb92905efa9801612122423d38aec35 in /usr/share/buildinfo/labels.json      
# Wed, 06 May 2026 09:13:05 GMT
COPY file:2221d5e6d5258b2c2c2c5ff82716a8550cb92905efa9801612122423d38aec35 in /root/buildinfo/labels.json      
# Wed, 06 May 2026 09:13:05 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="bf211293690f866639ec8b5930bb28589978ee3f" "org.opencontainers.image.revision"="bf211293690f866639ec8b5930bb28589978ee3f" "build-date"="2026-05-06T09:12:48Z" "org.opencontainers.image.created"="2026-05-06T09:12:48Z" "release"="1778058333"org.opencontainers.image.revision=bf211293690f866639ec8b5930bb28589978ee3f,org.opencontainers.image.created=2026-05-06T09:12:48Z
# Fri, 08 May 2026 16:20:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 16:20:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 16:20:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 May 2026 16:20:47 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 08 May 2026 16:20:47 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 08 May 2026 16:20:53 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 08 May 2026 16:20:55 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 16:20:55 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 16:20:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 16:20:55 GMT
CMD ["jshell"]
# Fri, 08 May 2026 16:35:17 GMT
CMD ["gradle"]
# Fri, 08 May 2026 16:35:17 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 May 2026 16:35:17 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 08 May 2026 16:35:17 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 May 2026 16:35:17 GMT
WORKDIR /home/gradle
# Fri, 08 May 2026 16:35:21 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 08 May 2026 16:35:21 GMT
ENV GRADLE_VERSION=9.5.0
# Fri, 08 May 2026 16:35:21 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Fri, 08 May 2026 16:35:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 08 May 2026 16:35:24 GMT
USER gradle
# Fri, 08 May 2026 16:35:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 08 May 2026 16:35:24 GMT
USER root
```

-	Layers:
	-	`sha256:e82aa3f29d1a9f34361831d6ff7b3f84cfd92ed1421ee638f165e55be85bd238`  
		Last Modified: Wed, 06 May 2026 10:17:34 GMT  
		Size: 32.7 MB (32746638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb229b21115571024cf10391b3d37329f493fc4acec7902a11cf112807262fa`  
		Last Modified: Fri, 08 May 2026 16:21:14 GMT  
		Size: 37.4 MB (37443950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8432e60f9084dcc3ac13e0a267fe3f1803144d357232f101356ff8e0377c14e9`  
		Last Modified: Fri, 08 May 2026 16:21:16 GMT  
		Size: 144.7 MB (144734896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640c14ac4a681cc9c2c2bc523b790e24ab26323620b8c56775d09e61ca8c4bde`  
		Last Modified: Fri, 08 May 2026 16:21:12 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3688fc0d3d5fbba7aba3728cb64720a1b3725df82c7bf053035215547b6da445`  
		Last Modified: Fri, 08 May 2026 16:20:46 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4921c962acdbf7d2075bcb9a6358a80b9ec5a55a63148a5374c28fb3f3719592`  
		Last Modified: Fri, 08 May 2026 16:35:41 GMT  
		Size: 1.6 KB (1588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59fc004f13dc9668dec961fe0884bb93899adf606cb9ef9e7faa158b32139f14`  
		Last Modified: Fri, 08 May 2026 16:35:43 GMT  
		Size: 38.3 MB (38321213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da7691ab942e2d08d1b92580da6aca258859de7ba402c511a543a133e262bfd`  
		Last Modified: Fri, 08 May 2026 16:35:46 GMT  
		Size: 140.2 MB (140235902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c710df9533f21ce3ef3c97131df0235c275f11ca38657e9be077346374a298a0`  
		Last Modified: Fri, 08 May 2026 16:35:41 GMT  
		Size: 29.3 KB (29337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:a01847350751d92d7a2840d135ea90ffe14bd73f3b0ddb0bc78cdf5be76292e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7079436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0dd1f1810bf50f7f4f8decfc824f4997d62bb85deebd187a5944dd5c953db79`

```dockerfile
```

-	Layers:
	-	`sha256:85953e9eaac332ad4890fe6677c8c7190f73ef18d14817f96979053bb4a825a4`  
		Last Modified: Fri, 08 May 2026 16:35:42 GMT  
		Size: 7.1 MB (7054784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c56b0bbfff2bb1d0b7837e8ea1bfaeb90cbdb5c90c92124c9330ebb6384a0e57`  
		Last Modified: Fri, 08 May 2026 16:35:41 GMT  
		Size: 24.7 KB (24652 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-ubi10` - linux; ppc64le

```console
$ docker pull gradle@sha256:97f1a782d7b1bb61c2e5178f942288e4c7829859072f130181a3ee0456337354
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.6 MB (404613982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa6dd9ebdd4fae86399a785c8806c13f4453c2189ad87a1b61345f47885197e8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 06 May 2026 09:10:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 06 May 2026 09:10:53 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 06 May 2026 09:10:53 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 06 May 2026 09:10:53 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 06 May 2026 09:10:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 06 May 2026 09:10:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 06 May 2026 09:10:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 09:10:53 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 09:10:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 06 May 2026 09:10:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 06 May 2026 09:10:53 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 06 May 2026 09:10:53 GMT
ENV container oci
# Wed, 06 May 2026 09:10:53 GMT
COPY dir:158c3f0cb7ce24639f61426b68518af6eac4aaf0de71f58d18f634631d8ec0f0 in /      
# Wed, 06 May 2026 09:10:53 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 06 May 2026 09:10:53 GMT
CMD ["/bin/bash"]
# Wed, 06 May 2026 09:10:53 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 06 May 2026 09:10:54 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 06 May 2026 09:10:54 GMT
COPY file:fa10e966ee7289b238e615643b46ea2d8e307515115a0ea9e2b102df79fabf33 in /usr/share/buildinfo/labels.json      
# Wed, 06 May 2026 09:10:54 GMT
COPY file:fa10e966ee7289b238e615643b46ea2d8e307515115a0ea9e2b102df79fabf33 in /root/buildinfo/labels.json      
# Wed, 06 May 2026 09:10:54 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="bf211293690f866639ec8b5930bb28589978ee3f" "org.opencontainers.image.revision"="bf211293690f866639ec8b5930bb28589978ee3f" "build-date"="2026-05-06T09:10:41Z" "org.opencontainers.image.created"="2026-05-06T09:10:41Z" "release"="1778058333"org.opencontainers.image.revision=bf211293690f866639ec8b5930bb28589978ee3f,org.opencontainers.image.created=2026-05-06T09:10:41Z
# Fri, 08 May 2026 16:18:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 16:18:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 16:18:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 May 2026 16:18:44 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 08 May 2026 16:18:44 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 08 May 2026 16:22:52 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 08 May 2026 16:22:56 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 16:22:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 16:22:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 16:22:56 GMT
CMD ["jshell"]
# Fri, 08 May 2026 16:42:27 GMT
CMD ["gradle"]
# Fri, 08 May 2026 16:42:27 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 May 2026 16:42:27 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 08 May 2026 16:42:27 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 May 2026 16:42:28 GMT
WORKDIR /home/gradle
# Fri, 08 May 2026 16:42:48 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 08 May 2026 16:42:48 GMT
ENV GRADLE_VERSION=9.5.0
# Fri, 08 May 2026 16:42:48 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Fri, 08 May 2026 16:42:52 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 08 May 2026 16:42:52 GMT
USER gradle
# Fri, 08 May 2026 16:42:54 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 08 May 2026 16:42:54 GMT
USER root
```

-	Layers:
	-	`sha256:8fabb2dd484322746fc4d1ed7e1fbca1a0509bc14f76029832e436bbc2825a8d`  
		Last Modified: Wed, 06 May 2026 12:15:25 GMT  
		Size: 38.8 MB (38751685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b7c362fde3ba2e4cb3c58a05618ebaafb430e3fbe1631353247827620d8d0d`  
		Last Modified: Fri, 08 May 2026 16:19:23 GMT  
		Size: 39.3 MB (39256885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4766b0025ba582f7dfd72034c4d565fc1bdd413cf3c9d7373c36c3e88d7572df`  
		Last Modified: Fri, 08 May 2026 16:23:36 GMT  
		Size: 145.8 MB (145788810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f235744ab698cc77e82ab9752c01b22e373ae623322cc810738428022345f5`  
		Last Modified: Fri, 08 May 2026 16:23:30 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61245b8f39e1938f2b5909f8cc46b699f69f6bb8ac5c28e618b00eef36e0c67c`  
		Last Modified: Fri, 08 May 2026 16:23:30 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7c630006ba31a4db9b5b42bc8ebfea4a126ca6d040757b059f0ab649334b13`  
		Last Modified: Fri, 08 May 2026 16:43:47 GMT  
		Size: 1.6 KB (1589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5dc30096790363a5852542cfc491cbefe8a2ee36653f8abeacf3a24a298142d`  
		Last Modified: Fri, 08 May 2026 16:43:51 GMT  
		Size: 40.6 MB (40576279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9874f523cba17d98dc52445cc0ce2f4650b3bcda3a8714b39be1b566621f4457`  
		Last Modified: Fri, 08 May 2026 16:43:52 GMT  
		Size: 140.2 MB (140235905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17820b34144c0fcbe943d208a77827500e25e425e64ca1b246edf2e7b3b25479`  
		Last Modified: Fri, 08 May 2026 16:43:47 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:e0d08e9cd58cc597fd4aa8cfadce1d2f07f50e190930f5e58a6204c73abdbd38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7072472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248e12818ee3ba6f0b6edff110c7a3cfc2e07d0c1379733a8fe2c0d535fe4563`

```dockerfile
```

-	Layers:
	-	`sha256:f09fd11d5aad99ac5a56c979009a2d061979fa1cf5e67effa12e507aec30139f`  
		Last Modified: Fri, 08 May 2026 16:43:48 GMT  
		Size: 7.0 MB (7047946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7281a6a001a976b1d2a6dba89bf29ee6f9450c840e100503b80d04df61b31ebd`  
		Last Modified: Fri, 08 May 2026 16:43:47 GMT  
		Size: 24.5 KB (24526 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-ubi10` - linux; s390x

```console
$ docker pull gradle@sha256:c96986f5233f3754e2416da3fa89474c73dd248a69081c40432b98f7dc9b1027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.4 MB (389406318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12d64771d4a88b4291cbaa38e2a11fe069fec5d27a5bda378a5df2abe5188b7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 06 May 2026 09:18:23 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 06 May 2026 09:18:23 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 06 May 2026 09:18:23 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 06 May 2026 09:18:23 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 06 May 2026 09:18:23 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 06 May 2026 09:18:23 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 06 May 2026 09:18:23 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 09:18:23 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 09:18:23 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 06 May 2026 09:18:23 GMT
LABEL io.openshift.expose-services=""
# Wed, 06 May 2026 09:18:23 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 06 May 2026 09:18:23 GMT
ENV container oci
# Wed, 06 May 2026 09:18:24 GMT
COPY dir:2de320d13d9374da0da9c93af8654c20620deef9fb77e0789c2dd217c1731ec0 in /      
# Wed, 06 May 2026 09:18:24 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 06 May 2026 09:18:24 GMT
CMD ["/bin/bash"]
# Wed, 06 May 2026 09:18:24 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 06 May 2026 09:18:24 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 06 May 2026 09:18:24 GMT
COPY file:de510b2b1ef76ab831f854dfe5fc4dc2d485ce06def44bc72ced35b5d05e629e in /usr/share/buildinfo/labels.json      
# Wed, 06 May 2026 09:18:24 GMT
COPY file:de510b2b1ef76ab831f854dfe5fc4dc2d485ce06def44bc72ced35b5d05e629e in /root/buildinfo/labels.json      
# Wed, 06 May 2026 09:18:24 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="bf211293690f866639ec8b5930bb28589978ee3f" "org.opencontainers.image.revision"="bf211293690f866639ec8b5930bb28589978ee3f" "build-date"="2026-05-06T09:17:45Z" "org.opencontainers.image.created"="2026-05-06T09:17:45Z" "release"="1778058333"org.opencontainers.image.revision=bf211293690f866639ec8b5930bb28589978ee3f,org.opencontainers.image.created=2026-05-06T09:17:45Z
# Fri, 08 May 2026 16:18:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 16:18:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 16:18:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 May 2026 16:18:48 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 08 May 2026 16:18:48 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 08 May 2026 16:19:45 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 08 May 2026 16:19:47 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 16:19:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 16:19:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 16:19:47 GMT
CMD ["jshell"]
# Fri, 08 May 2026 16:26:23 GMT
CMD ["gradle"]
# Fri, 08 May 2026 16:26:23 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 May 2026 16:26:23 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 08 May 2026 16:26:23 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 May 2026 16:26:23 GMT
WORKDIR /home/gradle
# Fri, 08 May 2026 16:26:28 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 08 May 2026 16:26:28 GMT
ENV GRADLE_VERSION=9.5.0
# Fri, 08 May 2026 16:26:28 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Fri, 08 May 2026 16:26:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 08 May 2026 16:26:32 GMT
USER gradle
# Fri, 08 May 2026 16:26:33 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 08 May 2026 16:26:33 GMT
USER root
```

-	Layers:
	-	`sha256:59eaf6b643faaa0a9b84bfb511ee7041d5f1d45b964283eb78c164d14435bcf6`  
		Last Modified: Wed, 06 May 2026 12:15:13 GMT  
		Size: 34.4 MB (34447291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c567288b6c22b0aca367e6871184062ac6fdc0793ecbbf0f93c4ec5dd3e5e8ee`  
		Last Modified: Fri, 08 May 2026 16:19:20 GMT  
		Size: 37.9 MB (37882211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359515b368daf15da35343d6459939c5e0199af38159c936fa1fbef47de8bcd1`  
		Last Modified: Fri, 08 May 2026 16:20:23 GMT  
		Size: 135.9 MB (135912375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c70d8e16ebbcaabf646a151f3e3104fff2413e9c082876288e400e81c118be`  
		Last Modified: Fri, 08 May 2026 16:20:20 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2321588e706970a946ed49326c88f4caf50c99b6acfc786f4b16e61a90da13a4`  
		Last Modified: Fri, 08 May 2026 16:20:20 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5002971b0b412f68dc1c1b20a3a526fd7ee65eeaa066924dab57af3f0940afad`  
		Last Modified: Fri, 08 May 2026 16:27:07 GMT  
		Size: 1.6 KB (1585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24488a25251623ff20dabd1a1b10b387ca375bccbdb155aca67f6513d656bf6`  
		Last Modified: Fri, 08 May 2026 16:27:09 GMT  
		Size: 40.9 MB (40924096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f937b2edbbe41549a9ec5916ca6bb747775dc9a59558b0d8f5e6df48015ad2d`  
		Last Modified: Fri, 08 May 2026 16:27:11 GMT  
		Size: 140.2 MB (140235932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa1589fcb31c72267db8a78ed189f71109bfd27db283a145a70bac27c8c96ce`  
		Last Modified: Fri, 08 May 2026 16:27:07 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:4421434a4c98e22723b6eabc9cdfa2330c31be70443c353a1902bbee8d03c161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7061628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fc0725ee215b4affe7014ad1a16a7016210cc826103108560534943a1b8b35`

```dockerfile
```

-	Layers:
	-	`sha256:53bc682c59e6d229505b42d20ca60ec0ee8774be618631b69074f027358e5799`  
		Last Modified: Fri, 08 May 2026 16:27:08 GMT  
		Size: 7.0 MB (7037175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df323f2403a52c0f686e933463891ae1b8cb7ab824f3c716c414a5f2f6812c0b`  
		Last Modified: Fri, 08 May 2026 16:27:07 GMT  
		Size: 24.5 KB (24453 bytes)  
		MIME: application/vnd.in-toto+json
