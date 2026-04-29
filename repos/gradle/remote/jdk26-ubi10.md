## `gradle:jdk26-ubi10`

```console
$ docker pull gradle@sha256:53bb0ccd09698f1ba725773d78921d09d9053f6ab1335c9dde450206f5dd6eba
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
$ docker pull gradle@sha256:76239aed5c65aae79b8a870c0db9bf2a7172e3fa77dff68f65d338aa68d6c1de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.6 MB (345570776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a9e398d419cd598d18fb1578d7dcd9dc3d64d8a117aa0ea386bc81d2b8fa950`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 22 Apr 2026 05:17:54 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 22 Apr 2026 05:17:54 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 22 Apr 2026 05:17:54 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 22 Apr 2026 05:17:54 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 22 Apr 2026 05:17:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 22 Apr 2026 05:17:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 22 Apr 2026 05:17:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:17:55 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:17:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 22 Apr 2026 05:17:55 GMT
LABEL io.openshift.expose-services=""
# Wed, 22 Apr 2026 05:17:55 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 22 Apr 2026 05:17:55 GMT
ENV container oci
# Wed, 22 Apr 2026 05:17:55 GMT
COPY dir:dff10165caa8c30a8c2673a95ace4a09e747d1c9e656d37fe7e2593a4192cea1 in /      
# Wed, 22 Apr 2026 05:17:55 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 22 Apr 2026 05:17:55 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 05:17:55 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 22 Apr 2026 05:17:55 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 22 Apr 2026 05:17:55 GMT
COPY file:1096e68e00ce2e3d16a7fbd65fd0781406fccc42abee623e8fa1f8395c75478b in /usr/share/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:17:56 GMT
COPY file:1096e68e00ce2e3d16a7fbd65fd0781406fccc42abee623e8fa1f8395c75478b in /root/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:17:56 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="8f919d0175e713e927f4fc60c8a4a7f7d7d63a58" "org.opencontainers.image.revision"="8f919d0175e713e927f4fc60c8a4a7f7d7d63a58" "build-date"="2026-04-22T05:17:41Z" "org.opencontainers.image.created"="2026-04-22T05:17:41Z" "release"="1776834797"org.opencontainers.image.revision=8f919d0175e713e927f4fc60c8a4a7f7d7d63a58,org.opencontainers.image.created=2026-04-22T05:17:41Z
# Wed, 22 Apr 2026 18:17:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 18:17:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 18:17:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Apr 2026 18:17:32 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 22 Apr 2026 18:17:32 GMT
ENV JAVA_VERSION=jdk-26+35
# Wed, 22 Apr 2026 18:17:38 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e8ff1f23c5acef74d1b4937dadd67286d67be06758f5d9dca5478c35bf404e83';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64le)          ESUM='7396fc32c311429c4b1573ebfc98eca6b82c2735f9f0e23acbccdcb43e0edee9';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='87fcdbbfd0adfd458922d8f8019eda23755aba597e386de2397f84cdf1b58808';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_s390x_linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='68e19ba53b7f1f74635c13f809e5db36cebccf3ae9e752423dd92d2ad7d831ef';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_x64_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 22 Apr 2026 18:17:40 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 22 Apr 2026 18:17:40 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Apr 2026 18:17:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 22 Apr 2026 18:17:40 GMT
CMD ["jshell"]
# Tue, 28 Apr 2026 23:31:24 GMT
CMD ["gradle"]
# Tue, 28 Apr 2026 23:31:24 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 28 Apr 2026 23:31:24 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 28 Apr 2026 23:31:24 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 28 Apr 2026 23:31:24 GMT
WORKDIR /home/gradle
# Tue, 28 Apr 2026 23:31:27 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 28 Apr 2026 23:31:27 GMT
ENV GRADLE_VERSION=9.5.0
# Tue, 28 Apr 2026 23:31:27 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Tue, 28 Apr 2026 23:31:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 28 Apr 2026 23:31:30 GMT
USER gradle
# Tue, 28 Apr 2026 23:31:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 28 Apr 2026 23:31:30 GMT
USER root
```

-	Layers:
	-	`sha256:74bbdc6f81c25b3fa8d6367ec856d92f28db48c1860a008184a1d723c8d399cc`  
		Last Modified: Wed, 22 Apr 2026 06:14:16 GMT  
		Size: 34.6 MB (34590462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:446a0aee2d15aaa238024fc63f6c75ba15856d38e0bbbeff9da1a3a450638639`  
		Last Modified: Wed, 22 Apr 2026 18:17:59 GMT  
		Size: 37.5 MB (37473595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26521de18c0cbd18f0803b3fc2eb45bdac4caf5d55a76e6667743e17bf3dbf1a`  
		Last Modified: Wed, 22 Apr 2026 18:18:00 GMT  
		Size: 94.5 MB (94454047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428dd31459ad2e2514d1b432ff3b6d9a377900bd8e5402d93ac7fd211052cb54`  
		Last Modified: Wed, 22 Apr 2026 18:17:57 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77fa5f504887197cb531aab54ed6d7ad1505c8d5091bf64493e810de2df879d`  
		Last Modified: Wed, 22 Apr 2026 18:17:58 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b3ebd4d4b4efab145400d1d7cda7348f72d4ba980ec0d7713da0093cf431f7`  
		Last Modified: Tue, 28 Apr 2026 23:31:46 GMT  
		Size: 1.6 KB (1590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2655ed821268993bbcbfc1ed0750234b30379f3cec641f17a578efe231d4aa99`  
		Last Modified: Tue, 28 Apr 2026 23:31:48 GMT  
		Size: 38.8 MB (38787113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43fe7167dcb57e14e3196599b1cde1d9fb13f23ea5569f844fabba88c1deb68`  
		Last Modified: Tue, 28 Apr 2026 23:31:50 GMT  
		Size: 140.2 MB (140235905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf29dcb6862e209d71986d08f2184bde2300a40dccecd67dee726733948311a4`  
		Last Modified: Tue, 28 Apr 2026 23:31:46 GMT  
		Size: 25.6 KB (25613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk26-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:5e9ea9355716b3ed31e07f6290e390ac305463973061c4b4c617173035075cea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7045765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:070c96f8ad928768621dae116b84dcbf096864395dfcef714fd83d5f6358e0d4`

```dockerfile
```

-	Layers:
	-	`sha256:793aff5336eb97f30e009c49d2fb8384d35f6a02a7dc6a343594aeaa205e95ba`  
		Last Modified: Tue, 28 Apr 2026 23:31:47 GMT  
		Size: 7.0 MB (7021357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d220f6f35e52984736bcfa2e3ffdca8c6a57468221bfcffd5823a460685c1721`  
		Last Modified: Tue, 28 Apr 2026 23:31:46 GMT  
		Size: 24.4 KB (24408 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk26-ubi10` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:3ce9617ec45e932451fe9c4dd8e5daac1aa639dc85158194b9ff374f46a21b23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.1 MB (342087872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:506d0dfb9ad423c85367d000e20c3dfd8d37b70ddc34b44f05d3ec0502acd44a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 22 Apr 2026 05:20:36 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 22 Apr 2026 05:20:36 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 22 Apr 2026 05:20:37 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 22 Apr 2026 05:20:37 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 22 Apr 2026 05:20:37 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 22 Apr 2026 05:20:37 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 22 Apr 2026 05:20:37 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:20:37 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:20:37 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 22 Apr 2026 05:20:37 GMT
LABEL io.openshift.expose-services=""
# Wed, 22 Apr 2026 05:20:37 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 22 Apr 2026 05:20:37 GMT
ENV container oci
# Wed, 22 Apr 2026 05:20:38 GMT
COPY dir:3a08e309561c3ef0f2f1f503de8f559ee625841311cafaf96b59ce47a8f1ffce in /      
# Wed, 22 Apr 2026 05:20:38 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 22 Apr 2026 05:20:38 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 05:20:38 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 22 Apr 2026 05:20:38 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 22 Apr 2026 05:20:38 GMT
COPY file:70c2dda7fafaa9f54a42bab62bbf07c21fa030503d7cbb51eb7b6ef84bbbba51 in /usr/share/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:20:38 GMT
COPY file:70c2dda7fafaa9f54a42bab62bbf07c21fa030503d7cbb51eb7b6ef84bbbba51 in /root/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:20:38 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="8f919d0175e713e927f4fc60c8a4a7f7d7d63a58" "org.opencontainers.image.revision"="8f919d0175e713e927f4fc60c8a4a7f7d7d63a58" "build-date"="2026-04-22T05:20:21Z" "org.opencontainers.image.created"="2026-04-22T05:20:21Z" "release"="1776834797"org.opencontainers.image.revision=8f919d0175e713e927f4fc60c8a4a7f7d7d63a58,org.opencontainers.image.created=2026-04-22T05:20:21Z
# Wed, 22 Apr 2026 18:16:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 18:16:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 18:16:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Apr 2026 18:16:26 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 22 Apr 2026 18:16:26 GMT
ENV JAVA_VERSION=jdk-26+35
# Wed, 22 Apr 2026 18:17:00 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e8ff1f23c5acef74d1b4937dadd67286d67be06758f5d9dca5478c35bf404e83';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64le)          ESUM='7396fc32c311429c4b1573ebfc98eca6b82c2735f9f0e23acbccdcb43e0edee9';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='87fcdbbfd0adfd458922d8f8019eda23755aba597e386de2397f84cdf1b58808';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_s390x_linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='68e19ba53b7f1f74635c13f809e5db36cebccf3ae9e752423dd92d2ad7d831ef';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_x64_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 22 Apr 2026 18:17:01 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 22 Apr 2026 18:17:01 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Apr 2026 18:17:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 22 Apr 2026 18:17:01 GMT
CMD ["jshell"]
# Tue, 28 Apr 2026 23:32:48 GMT
CMD ["gradle"]
# Tue, 28 Apr 2026 23:32:48 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 28 Apr 2026 23:32:48 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 28 Apr 2026 23:32:48 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 28 Apr 2026 23:32:48 GMT
WORKDIR /home/gradle
# Tue, 28 Apr 2026 23:32:52 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 28 Apr 2026 23:32:52 GMT
ENV GRADLE_VERSION=9.5.0
# Tue, 28 Apr 2026 23:32:52 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Tue, 28 Apr 2026 23:32:54 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 28 Apr 2026 23:32:54 GMT
USER gradle
# Tue, 28 Apr 2026 23:32:55 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 28 Apr 2026 23:32:55 GMT
USER root
```

-	Layers:
	-	`sha256:e8c4c206e9282db63c5bc98a6b172b79a7673404566e305674f0176bf9808f38`  
		Last Modified: Wed, 22 Apr 2026 06:16:01 GMT  
		Size: 32.7 MB (32712089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90cc0cfd04d8bf7d6ccd69d61211a956f29fcaea939aa0703b43a5889945a474`  
		Last Modified: Wed, 22 Apr 2026 18:16:44 GMT  
		Size: 37.4 MB (37416496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165b1e9b2701b27d76f50f8c9d4d5e63fb4450051e2dbc3681742a0cdaa1091a`  
		Last Modified: Wed, 22 Apr 2026 18:17:21 GMT  
		Size: 93.4 MB (93395922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1b22696d4d265096bb53638a3d45272f12e02ea8427fe2f2d5e5b560fd4fa9`  
		Last Modified: Wed, 22 Apr 2026 18:17:16 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa102225f8ac9d4ceb7eed421a4ced0e10149ecbbd758d24277bf6415b4c19c`  
		Last Modified: Wed, 22 Apr 2026 18:17:19 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390b55d6a31fd9ce385d95954094620396ae9ab120d6dec8bed8b2cd8daa5c39`  
		Last Modified: Tue, 28 Apr 2026 23:33:13 GMT  
		Size: 1.6 KB (1588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9748e24dc9ae3196caaad006324ef5df0d27e9df12e302026dfcf53158957f92`  
		Last Modified: Tue, 28 Apr 2026 23:33:15 GMT  
		Size: 38.3 MB (38294059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69cd406c8a35397682bedf07199c91c9f5c4c7637cf00046636a9ec4b6f6aa88`  
		Last Modified: Tue, 28 Apr 2026 23:33:17 GMT  
		Size: 140.2 MB (140235928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393705541e12156c047c411ca03a4f6c48f5bb713492e240d860b139b77eae46`  
		Last Modified: Tue, 28 Apr 2026 23:33:14 GMT  
		Size: 29.3 KB (29339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk26-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:345934b86c3d9b71155999948628b88dcad76a18c107c36fb598231614e2c60a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7044216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f3085ff671c23aaabf2cbea1b00fe7e9ce7bbdd8e36915b3cf376edf46d766`

```dockerfile
```

-	Layers:
	-	`sha256:b13575a63c47f23781c1f06680b1591b7fcb2b2df92a5048b2d00d209df9c11a`  
		Last Modified: Tue, 28 Apr 2026 23:33:14 GMT  
		Size: 7.0 MB (7019610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ebf5f4f64e701ba16bd16b840b9ef40a422604cc206dd3b43421ee13014e5e8`  
		Last Modified: Tue, 28 Apr 2026 23:33:13 GMT  
		Size: 24.6 KB (24606 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk26-ubi10` - linux; ppc64le

```console
$ docker pull gradle@sha256:b88246542f1c5ecf654d0640ffd3b7c867bebf3e4c52a889845f9a8e17293b55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.5 MB (352529947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc274e22f3ec04529a59b40dcb9d42b440ebefd2ac365d583ae793d2eb54b0d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 22 Apr 2026 05:19:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 22 Apr 2026 05:19:25 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 22 Apr 2026 05:19:25 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 22 Apr 2026 05:19:25 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 22 Apr 2026 05:19:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 22 Apr 2026 05:19:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 22 Apr 2026 05:19:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:19:25 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:19:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 22 Apr 2026 05:19:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 22 Apr 2026 05:19:25 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 22 Apr 2026 05:19:25 GMT
ENV container oci
# Wed, 22 Apr 2026 05:19:26 GMT
COPY dir:8ebfd472fb6c3a18db13a69e93e153e014f1bb212fbd41469e95368f33c9855b in /      
# Wed, 22 Apr 2026 05:19:26 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 22 Apr 2026 05:19:26 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 05:19:26 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 22 Apr 2026 05:19:26 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 22 Apr 2026 05:19:26 GMT
COPY file:1be71759ffffc91e186254d5919b2addc4c673e22dcd491b1496fe531cd50a49 in /usr/share/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:19:26 GMT
COPY file:1be71759ffffc91e186254d5919b2addc4c673e22dcd491b1496fe531cd50a49 in /root/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:19:27 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="8f919d0175e713e927f4fc60c8a4a7f7d7d63a58" "org.opencontainers.image.revision"="8f919d0175e713e927f4fc60c8a4a7f7d7d63a58" "build-date"="2026-04-22T05:19:14Z" "org.opencontainers.image.created"="2026-04-22T05:19:14Z" "release"="1776834797"org.opencontainers.image.revision=8f919d0175e713e927f4fc60c8a4a7f7d7d63a58,org.opencontainers.image.created=2026-04-22T05:19:14Z
# Wed, 22 Apr 2026 20:20:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 20:20:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 20:20:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Apr 2026 20:20:47 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 22 Apr 2026 20:20:47 GMT
ENV JAVA_VERSION=jdk-26+35
# Wed, 22 Apr 2026 20:30:35 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e8ff1f23c5acef74d1b4937dadd67286d67be06758f5d9dca5478c35bf404e83';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64le)          ESUM='7396fc32c311429c4b1573ebfc98eca6b82c2735f9f0e23acbccdcb43e0edee9';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='87fcdbbfd0adfd458922d8f8019eda23755aba597e386de2397f84cdf1b58808';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_s390x_linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='68e19ba53b7f1f74635c13f809e5db36cebccf3ae9e752423dd92d2ad7d831ef';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_x64_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 22 Apr 2026 20:30:41 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 22 Apr 2026 20:30:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Apr 2026 20:30:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 22 Apr 2026 20:30:41 GMT
CMD ["jshell"]
# Tue, 28 Apr 2026 23:33:12 GMT
CMD ["gradle"]
# Tue, 28 Apr 2026 23:33:12 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 28 Apr 2026 23:33:12 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 28 Apr 2026 23:33:12 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 28 Apr 2026 23:33:13 GMT
WORKDIR /home/gradle
# Tue, 28 Apr 2026 23:33:30 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 28 Apr 2026 23:33:30 GMT
ENV GRADLE_VERSION=9.5.0
# Tue, 28 Apr 2026 23:33:30 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Tue, 28 Apr 2026 23:33:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 28 Apr 2026 23:33:35 GMT
USER gradle
# Tue, 28 Apr 2026 23:33:37 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 28 Apr 2026 23:33:37 GMT
USER root
```

-	Layers:
	-	`sha256:948a2ed1d2b45707813b0dd77e6a53e4f19eb962b9d9bd8172ed211361568ec7`  
		Last Modified: Wed, 22 Apr 2026 06:16:32 GMT  
		Size: 38.7 MB (38732470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2433584b22c8a5a7b6fce7b912874af7acd3331970ae9ba91fbe6f82ec3637a`  
		Last Modified: Wed, 22 Apr 2026 20:21:23 GMT  
		Size: 39.2 MB (39225692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ffeca0f54815557c025fef421fde73c5fd2349123de6a992deffbb687936e6`  
		Last Modified: Wed, 22 Apr 2026 20:31:22 GMT  
		Size: 93.8 MB (93783038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86523e409a3e8358de2887604c0dfe3f359e638ec0f9cbba8c03006bdac6c00`  
		Last Modified: Wed, 22 Apr 2026 20:31:19 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d98cd615a27de2bbfb195314d5fc2813387dec1bbe7dba15a77d259d53fdcf`  
		Last Modified: Wed, 22 Apr 2026 20:31:20 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23400c8d1c8025ab1bd17ae377a5d9654d141be6426e851c93e6bb0c22d9d82`  
		Last Modified: Tue, 28 Apr 2026 23:34:17 GMT  
		Size: 1.6 KB (1591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80eed60072ce0c33f4f971168f0e58496f135159bafbf485756d0827267c8eda`  
		Last Modified: Tue, 28 Apr 2026 23:34:19 GMT  
		Size: 40.5 MB (40548380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b3faeeb7644d209c96a7ea1d549445480f201314a9c9c306637262458e6a2d`  
		Last Modified: Tue, 28 Apr 2026 23:34:23 GMT  
		Size: 140.2 MB (140235944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a63c93d65e314caa641ba96810745e02d56ed4e0659bb38720b0262aa96430`  
		Last Modified: Tue, 28 Apr 2026 23:34:17 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk26-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:6b847e142f6840e38e0e5428ed17564eb37e157f1619e1098563a6d5f075527a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7021192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13fad32a9ba83d39b86c7d28fb74605f03911361ea7eaa9228bfdb164e2a6232`

```dockerfile
```

-	Layers:
	-	`sha256:d806958f6331b1c7492167bccef7689569865c12f3cfbd600b39a465214d4f4e`  
		Last Modified: Tue, 28 Apr 2026 23:34:17 GMT  
		Size: 7.0 MB (6996711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2567846f4b75c0bc3b40905b420e86aa3714b7f846692f27d141f95c536c02dd`  
		Last Modified: Tue, 28 Apr 2026 23:34:17 GMT  
		Size: 24.5 KB (24481 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk26-ubi10` - linux; s390x

```console
$ docker pull gradle@sha256:0d1d23f93a6b0e1478f86d9f11a0f4237474cb00a4601f7abb36bb79bde35ec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.0 MB (343974682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9128f7112a47ed1fdeefaa58389974b38ca0094e1f9508d4cdd420787d0dd24c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 22 Apr 2026 05:32:39 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 22 Apr 2026 05:32:39 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 22 Apr 2026 05:32:39 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 22 Apr 2026 05:32:39 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 22 Apr 2026 05:32:39 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 22 Apr 2026 05:32:39 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 22 Apr 2026 05:32:39 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:32:39 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:32:39 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 22 Apr 2026 05:32:39 GMT
LABEL io.openshift.expose-services=""
# Wed, 22 Apr 2026 05:32:39 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 22 Apr 2026 05:32:39 GMT
ENV container oci
# Wed, 22 Apr 2026 05:32:40 GMT
COPY dir:98278e95a3e2bb93450b2e648bccc4bc2352556303c23dd62fc4c7b46f277fc9 in /      
# Wed, 22 Apr 2026 05:32:40 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 22 Apr 2026 05:32:40 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 05:32:40 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 22 Apr 2026 05:32:40 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 22 Apr 2026 05:32:40 GMT
COPY file:38c5f0375461f381e5db51646115279e3dad5b3c19eb862207cbc26ede0a9104 in /usr/share/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:32:40 GMT
COPY file:38c5f0375461f381e5db51646115279e3dad5b3c19eb862207cbc26ede0a9104 in /root/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:32:40 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="8f919d0175e713e927f4fc60c8a4a7f7d7d63a58" "org.opencontainers.image.revision"="8f919d0175e713e927f4fc60c8a4a7f7d7d63a58" "build-date"="2026-04-22T05:32:00Z" "org.opencontainers.image.created"="2026-04-22T05:32:00Z" "release"="1776834797"org.opencontainers.image.revision=8f919d0175e713e927f4fc60c8a4a7f7d7d63a58,org.opencontainers.image.created=2026-04-22T05:32:00Z
# Wed, 22 Apr 2026 18:16:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 18:16:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 18:16:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Apr 2026 18:16:22 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 22 Apr 2026 18:16:22 GMT
ENV JAVA_VERSION=jdk-26+35
# Wed, 22 Apr 2026 18:23:18 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e8ff1f23c5acef74d1b4937dadd67286d67be06758f5d9dca5478c35bf404e83';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64le)          ESUM='7396fc32c311429c4b1573ebfc98eca6b82c2735f9f0e23acbccdcb43e0edee9';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='87fcdbbfd0adfd458922d8f8019eda23755aba597e386de2397f84cdf1b58808';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_s390x_linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='68e19ba53b7f1f74635c13f809e5db36cebccf3ae9e752423dd92d2ad7d831ef';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_x64_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 22 Apr 2026 18:23:26 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 22 Apr 2026 18:23:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Apr 2026 18:23:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 22 Apr 2026 18:23:28 GMT
CMD ["jshell"]
# Tue, 28 Apr 2026 23:28:36 GMT
CMD ["gradle"]
# Tue, 28 Apr 2026 23:28:36 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 28 Apr 2026 23:28:36 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 28 Apr 2026 23:28:36 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 28 Apr 2026 23:28:36 GMT
WORKDIR /home/gradle
# Tue, 28 Apr 2026 23:28:51 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 28 Apr 2026 23:28:51 GMT
ENV GRADLE_VERSION=9.5.0
# Tue, 28 Apr 2026 23:28:51 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Tue, 28 Apr 2026 23:28:55 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 28 Apr 2026 23:28:55 GMT
USER gradle
# Tue, 28 Apr 2026 23:28:55 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 28 Apr 2026 23:28:55 GMT
USER root
```

-	Layers:
	-	`sha256:59053ba8a9d1e0e09d61b1f59967bb9ffc4505ef8eebe01b4c6808d9bce8b3a6`  
		Last Modified: Wed, 22 Apr 2026 06:16:12 GMT  
		Size: 34.4 MB (34437922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cf755e7e06afeb41fd368fbfaae8e70f129c645bebe025cef69dbd8ac6c635`  
		Last Modified: Wed, 22 Apr 2026 18:17:40 GMT  
		Size: 37.8 MB (37849869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c1b6cf5c6abec1fd044d444af556f39a98168c58436d794173012a3fc03dec`  
		Last Modified: Wed, 22 Apr 2026 18:24:40 GMT  
		Size: 90.5 MB (90548283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38962e6908118ba21a78df1f30b1440bd0b95de374ded13565d9e4ea7e64bb3`  
		Last Modified: Wed, 22 Apr 2026 18:24:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59b06b7bd118d4f35996e1eef430168586debbafb3cf81a90eb6b29c08cca6b`  
		Last Modified: Wed, 22 Apr 2026 18:24:32 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6219890cb749e447bd7ee356190b21bc94b1fda88c385a622dc2c6cfc24ec363`  
		Last Modified: Tue, 28 Apr 2026 23:29:22 GMT  
		Size: 1.6 KB (1590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66964c9a3ea254f5fc8511272cd56a4925337859fb1a90ab1a3b899dd5bdd2c8`  
		Last Modified: Tue, 28 Apr 2026 23:29:23 GMT  
		Size: 40.9 MB (40898252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95bf7af36a5c6c204f2266b76cf5f088259d00b44e85f405710ddebc80e1cfcd`  
		Last Modified: Tue, 28 Apr 2026 23:29:25 GMT  
		Size: 140.2 MB (140235940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ed50c9e96210b92cf6cd90d19d73eae3e3ee376c265823fa1a0544c143fe54`  
		Last Modified: Tue, 28 Apr 2026 23:29:22 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk26-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:0f189c3e04099c2590e3311ac2c4e7de93212bad62a9187e5a0747323fbddde1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7011597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3193d1515788fd141e9a00ce02b6a1fd40e0cce883dadafdf19eb664f9aca1`

```dockerfile
```

-	Layers:
	-	`sha256:46e3c665140f47ed30887a6256308c79e25eb773a8741a70d08ea59bcab7e77d`  
		Last Modified: Tue, 28 Apr 2026 23:29:22 GMT  
		Size: 7.0 MB (6987190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32478ab69cfa43577f12c7d76a45852496b13584c8c416d8b17459695c3b2704`  
		Last Modified: Tue, 28 Apr 2026 23:29:22 GMT  
		Size: 24.4 KB (24407 bytes)  
		MIME: application/vnd.in-toto+json
