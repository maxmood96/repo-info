## `gradle:jdk26-ubi10`

```console
$ docker pull gradle@sha256:22b5de2f2e313cdb7219d7ee72027aa846a1e7857f7e4baebbf8a6dcf7a2f760
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

### `gradle:jdk26-ubi10` - linux; amd64

```console
$ docker pull gradle@sha256:441f0b4285ad89f75b7af8519408030147a12b6d33babaaa32fddb513fd16840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.7 MB (345675561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a693406479d207705a876a6ad5cd5bf3f85940bcc499c08ef2dbab526544ba`
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
# Fri, 08 May 2026 16:21:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 16:21:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 16:21:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 May 2026 16:21:29 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 08 May 2026 16:21:29 GMT
ENV JAVA_VERSION=jdk-26+35
# Fri, 08 May 2026 16:21:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e8ff1f23c5acef74d1b4937dadd67286d67be06758f5d9dca5478c35bf404e83';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64le)          ESUM='7396fc32c311429c4b1573ebfc98eca6b82c2735f9f0e23acbccdcb43e0edee9';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='87fcdbbfd0adfd458922d8f8019eda23755aba597e386de2397f84cdf1b58808';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_s390x_linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='68e19ba53b7f1f74635c13f809e5db36cebccf3ae9e752423dd92d2ad7d831ef';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_x64_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 08 May 2026 16:21:35 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 16:21:35 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 16:21:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 16:21:35 GMT
CMD ["jshell"]
# Fri, 08 May 2026 16:38:29 GMT
CMD ["gradle"]
# Fri, 08 May 2026 16:38:29 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 May 2026 16:38:29 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 08 May 2026 16:38:29 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 May 2026 16:38:29 GMT
WORKDIR /home/gradle
# Fri, 08 May 2026 16:38:32 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 08 May 2026 16:38:32 GMT
ENV GRADLE_VERSION=9.5.0
# Fri, 08 May 2026 16:38:32 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Fri, 08 May 2026 16:38:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 08 May 2026 16:38:35 GMT
USER gradle
# Fri, 08 May 2026 16:38:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 08 May 2026 16:38:35 GMT
USER root
```

-	Layers:
	-	`sha256:92d62aafb6a18663d52e4aabc1138a75b2e6994c38e927e9099cb078cc22e6b7`  
		Last Modified: Wed, 06 May 2026 10:14:33 GMT  
		Size: 34.6 MB (34621721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda4854c408a43867d5c0c1618c8447f4cbd053d867526d19e5bcb517c49d290`  
		Last Modified: Fri, 08 May 2026 16:21:53 GMT  
		Size: 37.5 MB (37498920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7472831ebad11064e68ef8ae12896f8fcacf7c149c330f18ceaf65c03b6c2d`  
		Last Modified: Fri, 08 May 2026 16:21:55 GMT  
		Size: 94.5 MB (94454023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b36e144fa27c673d358c153e40fef4815b30af7118298af85f77ae76fb0cd1`  
		Last Modified: Fri, 08 May 2026 16:21:51 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad7bcd80ae3a99b62e29399dc53c07ffd11d2aea85161501905bb0069c02dde`  
		Last Modified: Fri, 08 May 2026 16:21:51 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ddd623120c7bb61cee39f342c9df478b8dc194afe5d0000c77c636ee167f50`  
		Last Modified: Fri, 08 May 2026 16:38:54 GMT  
		Size: 1.6 KB (1585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f05f5d939dbcdb6b6c1f0c1822f4a2245ae8596ff53a027c9fbf9e8aa9c78a7`  
		Last Modified: Fri, 08 May 2026 16:38:56 GMT  
		Size: 38.8 MB (38835304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5004d7a276808d076b096012addb3b7a2774da19331d87a4645d898264618cd7`  
		Last Modified: Fri, 08 May 2026 16:38:58 GMT  
		Size: 140.2 MB (140235944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e885aee313646aed069d57bdee6d603b0af0fb04821fe409918fe3caf57c8a`  
		Last Modified: Fri, 08 May 2026 16:38:54 GMT  
		Size: 25.6 KB (25612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk26-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:cd80fe2441a9a2636b81957487de548f34fab5d4b6a6ff278092d11f236ba88f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7045813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47655b0b6ef81b1cec9d1299e04c4676a7fc37134944158eece49a1b475fa66b`

```dockerfile
```

-	Layers:
	-	`sha256:2b7171e80184f1b7a24be68496334e4afb0d4b9f135ecc08d482a702ce590ba0`  
		Last Modified: Fri, 08 May 2026 16:38:54 GMT  
		Size: 7.0 MB (7021405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:975c09ebc1d4db1e7da53b0965ce16cde820833203a5b7c0b266e482b99284db`  
		Last Modified: Fri, 08 May 2026 16:38:53 GMT  
		Size: 24.4 KB (24408 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk26-ubi10` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:c6eb2d515d2e0fdfb167b6ffc54d628ac36d6acc4dc421896568dbc35e00cf9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.2 MB (342177454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b3de7123e00f758dd2d6891432a387a9ade9e2ca42cd3e91a00c40c1385ec20`
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
# Fri, 08 May 2026 16:20:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 16:20:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 16:20:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 May 2026 16:20:34 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 08 May 2026 16:20:34 GMT
ENV JAVA_VERSION=jdk-26+35
# Fri, 08 May 2026 16:21:17 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e8ff1f23c5acef74d1b4937dadd67286d67be06758f5d9dca5478c35bf404e83';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64le)          ESUM='7396fc32c311429c4b1573ebfc98eca6b82c2735f9f0e23acbccdcb43e0edee9';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='87fcdbbfd0adfd458922d8f8019eda23755aba597e386de2397f84cdf1b58808';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_s390x_linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='68e19ba53b7f1f74635c13f809e5db36cebccf3ae9e752423dd92d2ad7d831ef';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_x64_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 08 May 2026 16:21:19 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 16:21:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 16:21:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 16:21:19 GMT
CMD ["jshell"]
# Fri, 08 May 2026 16:35:33 GMT
CMD ["gradle"]
# Fri, 08 May 2026 16:35:33 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 May 2026 16:35:33 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 08 May 2026 16:35:33 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 May 2026 16:35:33 GMT
WORKDIR /home/gradle
# Fri, 08 May 2026 16:35:37 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 08 May 2026 16:35:37 GMT
ENV GRADLE_VERSION=9.5.0
# Fri, 08 May 2026 16:35:37 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Fri, 08 May 2026 16:35:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 08 May 2026 16:35:40 GMT
USER gradle
# Fri, 08 May 2026 16:35:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 08 May 2026 16:35:40 GMT
USER root
```

-	Layers:
	-	`sha256:e82aa3f29d1a9f34361831d6ff7b3f84cfd92ed1421ee638f165e55be85bd238`  
		Last Modified: Wed, 06 May 2026 10:17:34 GMT  
		Size: 32.7 MB (32746638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d9bb7ed98a0c3af6f8d4b5c97f12821da96943bf413573741d84a78165a4e5`  
		Last Modified: Fri, 08 May 2026 16:21:00 GMT  
		Size: 37.4 MB (37443890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf17db2324897a742d43fd86f031b0baf2e1082beaa3b3103261a7ddb1a536d`  
		Last Modified: Fri, 08 May 2026 16:21:38 GMT  
		Size: 93.4 MB (93395916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ccead134754096b84ebc83a14286cfc996c4228ea6d94338480d6ea4fb1266`  
		Last Modified: Fri, 08 May 2026 16:21:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc896a24fb6fc5cbb129a4a07081650a1a3fdba1b3aed29ad71a48663fe9bf4`  
		Last Modified: Fri, 08 May 2026 16:21:29 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b963bdf50e5bca6f39b4d5c0eda4f33e1fab7af886298298fcf73f45df1a5d`  
		Last Modified: Fri, 08 May 2026 16:36:00 GMT  
		Size: 1.6 KB (1585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2097b2688fef4ac5e848adc32ed773fe58f8f0bf589218385f3b2aa49b9ffe09`  
		Last Modified: Fri, 08 May 2026 16:36:02 GMT  
		Size: 38.3 MB (38321694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87306570b942e0e34d3babbeaabe82ee96b1f342f756a5900ccc8c0155692e9`  
		Last Modified: Fri, 08 May 2026 16:36:04 GMT  
		Size: 140.2 MB (140235941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a182dedf81c534b6051b39e9f56bc1e070223b58e78c46d8fc84608af9b2c1`  
		Last Modified: Fri, 08 May 2026 16:36:00 GMT  
		Size: 29.3 KB (29338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk26-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:5657dcd1af844b50fcf17cae868f5985c10f337d675a32f2e4fff77820f51118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7044264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0caacf1ee959171652ce1c40c0c52f9a5e5980071c6e6649d7660182692715`

```dockerfile
```

-	Layers:
	-	`sha256:e3abbd4ce0b92b403ffafde4a31743af3be977bc7713fd28627d0e8a7a72d68f`  
		Last Modified: Fri, 08 May 2026 16:36:00 GMT  
		Size: 7.0 MB (7019658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31d762dbba99a37594a3e8c0d35403d102c17564c70b3b77bfff9dddab6f6b63`  
		Last Modified: Fri, 08 May 2026 16:36:00 GMT  
		Size: 24.6 KB (24606 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk26-ubi10` - linux; ppc64le

```console
$ docker pull gradle@sha256:b36577f60420f3175ddfb8a17468366a8d25eb6c860910095afcdaab07a206e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.6 MB (352608034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb880fee8c53088464f556a25d98f07cd75d88401be64fb918ad3c3ce287bb3`
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
ENV JAVA_VERSION=jdk-26+35
# Fri, 08 May 2026 16:28:13 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e8ff1f23c5acef74d1b4937dadd67286d67be06758f5d9dca5478c35bf404e83';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64le)          ESUM='7396fc32c311429c4b1573ebfc98eca6b82c2735f9f0e23acbccdcb43e0edee9';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='87fcdbbfd0adfd458922d8f8019eda23755aba597e386de2397f84cdf1b58808';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_s390x_linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='68e19ba53b7f1f74635c13f809e5db36cebccf3ae9e752423dd92d2ad7d831ef';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_x64_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 08 May 2026 16:28:16 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 16:28:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 16:28:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 16:28:16 GMT
CMD ["jshell"]
# Fri, 08 May 2026 20:04:17 GMT
CMD ["gradle"]
# Fri, 08 May 2026 20:04:17 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 May 2026 20:04:17 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 08 May 2026 20:04:17 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 May 2026 20:04:17 GMT
WORKDIR /home/gradle
# Fri, 08 May 2026 20:04:31 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 08 May 2026 20:04:31 GMT
ENV GRADLE_VERSION=9.5.0
# Fri, 08 May 2026 20:04:31 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Fri, 08 May 2026 20:04:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 08 May 2026 20:04:35 GMT
USER gradle
# Fri, 08 May 2026 20:04:37 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 08 May 2026 20:04:37 GMT
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
	-	`sha256:6ccb666aa29fab53ce9c55739d1f7ecc862b64eae3cc013891861bfcfc9dbba0`  
		Last Modified: Fri, 08 May 2026 16:28:57 GMT  
		Size: 93.8 MB (93783018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465dbba4a7849d53e8b6518ae8e34ecfc968774129bf53e88cd008765377aaba`  
		Last Modified: Fri, 08 May 2026 16:28:54 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb122caac2957cae35506249ff49963a96e8b69230b0c89826f042b7056faf1`  
		Last Modified: Fri, 08 May 2026 16:28:54 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38434e51a8b77e0d82b7ec2a785621b91d76002b1f288789c1120e6925093611`  
		Last Modified: Fri, 08 May 2026 20:05:11 GMT  
		Size: 1.6 KB (1585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0d35a081e18b51f879420bf5ecfd00713a4ff9a2511feb46b8471f6cbbcc03`  
		Last Modified: Fri, 08 May 2026 20:05:14 GMT  
		Size: 40.6 MB (40576103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e65fc7de2ea5ef1bdfae5b95053d702cc4eff8ec6247f088ec9a75b67115fc5`  
		Last Modified: Fri, 08 May 2026 20:05:16 GMT  
		Size: 140.2 MB (140235927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8e1ae9218de51b055c3e541b0406dbd40e3009e6cc40e2d29a2677c850fc17`  
		Last Modified: Fri, 08 May 2026 20:05:12 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk26-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:a8b16ff0922c1ae16707fc39dbf1d323f41b23a3eebf1d741f0d9ec94597d10f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7021240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33d55fe8e6cc32ae4edd100efa1023d0065b691e7e43fd1933236b4f9e37963`

```dockerfile
```

-	Layers:
	-	`sha256:2d3640dd57cee91133433d48bcf990044732cdedca0ea2d0c792649656f5affe`  
		Last Modified: Fri, 08 May 2026 20:05:12 GMT  
		Size: 7.0 MB (6996759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbc389a63ed29ea16dd390a38c96d7f3f49266b893f782c55aeaca79d6108187`  
		Last Modified: Fri, 08 May 2026 20:05:11 GMT  
		Size: 24.5 KB (24481 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk26-ubi10` - linux; s390x

```console
$ docker pull gradle@sha256:9082bb6373e7016bb2af3e05e3d5504f0928928d0eef52098c52e6fdc5ea102d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.0 MB (344041908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e9aaa12904fb333fc0597553911aa2e00bf0197f546532806407c3568cffab`
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
# Fri, 08 May 2026 16:18:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 16:18:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 16:18:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 May 2026 16:18:54 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 08 May 2026 16:18:54 GMT
ENV JAVA_VERSION=jdk-26+35
# Fri, 08 May 2026 16:22:02 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e8ff1f23c5acef74d1b4937dadd67286d67be06758f5d9dca5478c35bf404e83';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64le)          ESUM='7396fc32c311429c4b1573ebfc98eca6b82c2735f9f0e23acbccdcb43e0edee9';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='87fcdbbfd0adfd458922d8f8019eda23755aba597e386de2397f84cdf1b58808';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_s390x_linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='68e19ba53b7f1f74635c13f809e5db36cebccf3ae9e752423dd92d2ad7d831ef';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_x64_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 08 May 2026 16:22:04 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 16:22:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 16:22:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 16:22:05 GMT
CMD ["jshell"]
# Fri, 08 May 2026 16:27:29 GMT
CMD ["gradle"]
# Fri, 08 May 2026 16:27:29 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 May 2026 16:27:29 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 08 May 2026 16:27:29 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 May 2026 16:27:29 GMT
WORKDIR /home/gradle
# Fri, 08 May 2026 16:27:35 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 08 May 2026 16:27:35 GMT
ENV GRADLE_VERSION=9.5.0
# Fri, 08 May 2026 16:27:35 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Fri, 08 May 2026 16:27:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 08 May 2026 16:27:39 GMT
USER gradle
# Fri, 08 May 2026 16:27:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 08 May 2026 16:27:40 GMT
USER root
```

-	Layers:
	-	`sha256:59eaf6b643faaa0a9b84bfb511ee7041d5f1d45b964283eb78c164d14435bcf6`  
		Last Modified: Wed, 06 May 2026 12:15:13 GMT  
		Size: 34.4 MB (34447291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11063d83193319cb5980b0a40bb11387764f3db57700e2f877ca5b9f024b5c7f`  
		Last Modified: Fri, 08 May 2026 16:19:32 GMT  
		Size: 37.9 MB (37882115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e4f896ad10269d72dcb784cc1827780eb5edf9e2ef18b68d325868cd394a3da`  
		Last Modified: Fri, 08 May 2026 16:22:35 GMT  
		Size: 90.5 MB (90548242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab11a755d6ec1b68c548e5668506bf4b76178c99d7d963b36cee3862b417a7ed`  
		Last Modified: Fri, 08 May 2026 16:22:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8a1727cb63268018955fff323f07faf418c62c1bfcef7e482649325223feee`  
		Last Modified: Fri, 08 May 2026 16:22:31 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae056e926e6e37b6fa49bac57a01f2a261a472ed5f7e640e541dbc3fd239350`  
		Last Modified: Fri, 08 May 2026 16:28:15 GMT  
		Size: 1.6 KB (1584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c27a606feeffe35a505e6013ea7ade51cfc96c7ef447ec88f7c3bdf25e3e72f`  
		Last Modified: Fri, 08 May 2026 16:28:17 GMT  
		Size: 40.9 MB (40923907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a43896ce6cecdeac7b1c4de7c8b75bdf68f8b7bb3ad3c0e76dcd15b30d83ed46`  
		Last Modified: Fri, 08 May 2026 16:28:19 GMT  
		Size: 140.2 MB (140235942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38658fae29d251daf33a89ad7414192417d21756661beb6509b1b80428d1396d`  
		Last Modified: Fri, 08 May 2026 16:28:16 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk26-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:a085a85f0a4a2e252a05618af0cbdd04bd0d4667993e15b6d3fb2aed46721957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7011645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2432510bb530d4c2696d98f10ac31af8340cae4b0c397bdaf3740cbb5fdd3b5c`

```dockerfile
```

-	Layers:
	-	`sha256:1a3fc5cb5004573696fa9a011514d664c726889f6fdb3b4cd35fad72b4413b9f`  
		Last Modified: Fri, 08 May 2026 16:28:16 GMT  
		Size: 7.0 MB (6987238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e090aac5dd92bf6fdf97b75f36cf1d1fd31ff5abb1816b49200454a010c343ec`  
		Last Modified: Fri, 08 May 2026 16:28:15 GMT  
		Size: 24.4 KB (24407 bytes)  
		MIME: application/vnd.in-toto+json
