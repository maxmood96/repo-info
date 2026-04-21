## `gradle:jdk26-ubi`

```console
$ docker pull gradle@sha256:ca1dcc411ec717e1fec09ae060d27ef69d9da59b37e5c70aa0dc399c410eff94
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

### `gradle:jdk26-ubi` - linux; amd64

```console
$ docker pull gradle@sha256:f14d60e9740658b4debae7391cc18b716dd1160c9860754ddf678e15c4f777b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.2 MB (343158582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3640907e5d5d968e7f12f0de1dac8819644d569842c95379870bf512103b4167`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 20 Apr 2026 01:02:16 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 20 Apr 2026 01:02:16 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 20 Apr 2026 01:02:16 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 20 Apr 2026 01:02:16 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 20 Apr 2026 01:02:16 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 20 Apr 2026 01:02:16 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 20 Apr 2026 01:02:16 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 01:02:16 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 01:02:16 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 20 Apr 2026 01:02:16 GMT
LABEL io.openshift.expose-services=""
# Mon, 20 Apr 2026 01:02:16 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 20 Apr 2026 01:02:16 GMT
ENV container oci
# Mon, 20 Apr 2026 01:02:16 GMT
COPY dir:dd0e1195353ed5dffd0360f7175a32413cb31b4b787f27413cf4ea2f98d12b5d in /      
# Mon, 20 Apr 2026 01:02:16 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 20 Apr 2026 01:02:16 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 01:02:16 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 20 Apr 2026 01:02:17 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 20 Apr 2026 01:02:17 GMT
COPY file:fbdadfc291bf0e40ec3c74e36ea45cd6d320a19b5da8cb1d3fdb33930ac6a4c0 in /usr/share/buildinfo/labels.json      
# Mon, 20 Apr 2026 01:02:17 GMT
COPY file:fbdadfc291bf0e40ec3c74e36ea45cd6d320a19b5da8cb1d3fdb33930ac6a4c0 in /root/buildinfo/labels.json      
# Mon, 20 Apr 2026 01:02:17 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="32540b060e1a63cad21d656f09cff9da51482dc3" "org.opencontainers.image.revision"="32540b060e1a63cad21d656f09cff9da51482dc3" "build-date"="2026-04-20T01:02:00Z" "org.opencontainers.image.created"="2026-04-20T01:02:00Z" "release"="1776646707"org.opencontainers.image.revision=32540b060e1a63cad21d656f09cff9da51482dc3,org.opencontainers.image.created=2026-04-20T01:02:00Z
# Mon, 20 Apr 2026 23:06:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Apr 2026 23:06:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 23:06:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Apr 2026 23:06:50 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:06:50 GMT
ENV JAVA_VERSION=jdk-26+35
# Mon, 20 Apr 2026 23:06:55 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e8ff1f23c5acef74d1b4937dadd67286d67be06758f5d9dca5478c35bf404e83';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64le)          ESUM='7396fc32c311429c4b1573ebfc98eca6b82c2735f9f0e23acbccdcb43e0edee9';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='87fcdbbfd0adfd458922d8f8019eda23755aba597e386de2397f84cdf1b58808';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_s390x_linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='68e19ba53b7f1f74635c13f809e5db36cebccf3ae9e752423dd92d2ad7d831ef';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_x64_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 20 Apr 2026 23:06:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Apr 2026 23:06:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Apr 2026 23:06:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Apr 2026 23:06:57 GMT
CMD ["jshell"]
# Tue, 21 Apr 2026 00:00:22 GMT
CMD ["gradle"]
# Tue, 21 Apr 2026 00:00:22 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 21 Apr 2026 00:00:22 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 21 Apr 2026 00:00:22 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 21 Apr 2026 00:00:22 GMT
WORKDIR /home/gradle
# Tue, 21 Apr 2026 00:00:26 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 21 Apr 2026 00:00:26 GMT
ENV GRADLE_VERSION=9.4.1
# Tue, 21 Apr 2026 00:00:26 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Tue, 21 Apr 2026 00:00:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 21 Apr 2026 00:00:29 GMT
USER gradle
# Tue, 21 Apr 2026 00:00:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 21 Apr 2026 00:00:29 GMT
USER root
```

-	Layers:
	-	`sha256:9ea0f884ebdb006c6d06f1f86307c899f549c7d238971fe657c84c93f6b38191`  
		Last Modified: Mon, 20 Apr 2026 11:13:13 GMT  
		Size: 34.6 MB (34611060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be016dfd83668fda58f66807c20467f96b033d037049d206b336f51d8a9f75c0`  
		Last Modified: Mon, 20 Apr 2026 23:07:15 GMT  
		Size: 37.5 MB (37463316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed4c14506c987d700cd15c32ea6ba760b1574fbb70feb0ff4c1031ea5f7e4b1`  
		Last Modified: Mon, 20 Apr 2026 23:07:16 GMT  
		Size: 94.5 MB (94454029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29eeedebe20dfb246751f32c44386500ac0f95c47b447e67d1e6f5feb89e2b1c`  
		Last Modified: Mon, 20 Apr 2026 23:07:13 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067cadd24f9069eb560945531ead12d72ced10368628b081ceb7ded0267c7f05`  
		Last Modified: Mon, 20 Apr 2026 23:07:10 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd939ab86606c0329e96ed87654c7acb47ab299227aa949779dc4a74844b8a26`  
		Last Modified: Tue, 21 Apr 2026 00:00:46 GMT  
		Size: 1.6 KB (1588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e095874dc7fc6da0a61b9015e3994bba6ac1d049d0b188b147ca6eeaf8c842`  
		Last Modified: Tue, 21 Apr 2026 00:00:48 GMT  
		Size: 38.8 MB (38792189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3232b33967f2163958162f8049362ae3076ec66c5de331206dc3fb10d0d0c9c`  
		Last Modified: Tue, 21 Apr 2026 00:00:51 GMT  
		Size: 137.8 MB (137808338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5516fd65bc1f47c6b3371cdf8710df8979369c8b7ef84f794038b6f1a3d864c`  
		Last Modified: Tue, 21 Apr 2026 00:00:46 GMT  
		Size: 25.6 KB (25611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk26-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:859525cf5089b8574f0f535cedb206801f0e8c940b94db032ce4b551d6306774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7016857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:908fecdda76df8928c58ea678b31461ca409d7d242ee6bb2b75dad2cb2241100`

```dockerfile
```

-	Layers:
	-	`sha256:693c7c6cb77beb2ebfd3fe8155aa11fcc11c57dd584759736d6a351548d61ff7`  
		Last Modified: Tue, 21 Apr 2026 00:00:46 GMT  
		Size: 7.0 MB (6992448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79e3c45d5d8377d5c27fc321dc2fbbc04e63b75e12a155b315a6106f5902c2db`  
		Last Modified: Tue, 21 Apr 2026 00:00:46 GMT  
		Size: 24.4 KB (24409 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk26-ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:e9081da3ed9fbabdf513d7250c110b59ff7f231a27106ad5da0e5f359339142c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.6 MB (339628990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a2fceced36b37bd19b8c47672db27691f8fe1c12b69c1779b7c363bd9195dbc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 20 Apr 2026 01:04:42 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 20 Apr 2026 01:04:42 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 20 Apr 2026 01:04:42 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 20 Apr 2026 01:04:43 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 20 Apr 2026 01:04:43 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 20 Apr 2026 01:04:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 20 Apr 2026 01:04:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 01:04:43 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 01:04:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 20 Apr 2026 01:04:43 GMT
LABEL io.openshift.expose-services=""
# Mon, 20 Apr 2026 01:04:43 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 20 Apr 2026 01:04:43 GMT
ENV container oci
# Mon, 20 Apr 2026 01:04:43 GMT
COPY dir:3dce53cd7f9d7326227f9f135d7cd4905e49967e75fffdb7305248967fd08ecb in /      
# Mon, 20 Apr 2026 01:04:44 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 20 Apr 2026 01:04:44 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 01:04:44 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 20 Apr 2026 01:04:44 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 20 Apr 2026 01:04:44 GMT
COPY file:47b968046aebceb7e689b8f162b1d58465b394d88fb7d588f40ffa5eb8594d57 in /usr/share/buildinfo/labels.json      
# Mon, 20 Apr 2026 01:04:44 GMT
COPY file:47b968046aebceb7e689b8f162b1d58465b394d88fb7d588f40ffa5eb8594d57 in /root/buildinfo/labels.json      
# Mon, 20 Apr 2026 01:04:44 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="32540b060e1a63cad21d656f09cff9da51482dc3" "org.opencontainers.image.revision"="32540b060e1a63cad21d656f09cff9da51482dc3" "build-date"="2026-04-20T01:04:27Z" "org.opencontainers.image.created"="2026-04-20T01:04:27Z" "release"="1776646707"org.opencontainers.image.revision=32540b060e1a63cad21d656f09cff9da51482dc3,org.opencontainers.image.created=2026-04-20T01:04:27Z
# Mon, 20 Apr 2026 23:03:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Apr 2026 23:03:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 23:03:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Apr 2026 23:03:48 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:03:48 GMT
ENV JAVA_VERSION=jdk-26+35
# Mon, 20 Apr 2026 23:04:30 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e8ff1f23c5acef74d1b4937dadd67286d67be06758f5d9dca5478c35bf404e83';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64le)          ESUM='7396fc32c311429c4b1573ebfc98eca6b82c2735f9f0e23acbccdcb43e0edee9';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='87fcdbbfd0adfd458922d8f8019eda23755aba597e386de2397f84cdf1b58808';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_s390x_linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='68e19ba53b7f1f74635c13f809e5db36cebccf3ae9e752423dd92d2ad7d831ef';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_x64_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 20 Apr 2026 23:04:31 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Apr 2026 23:04:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Apr 2026 23:04:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Apr 2026 23:04:31 GMT
CMD ["jshell"]
# Mon, 20 Apr 2026 23:14:16 GMT
CMD ["gradle"]
# Mon, 20 Apr 2026 23:14:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 20 Apr 2026 23:14:16 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 20 Apr 2026 23:14:16 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 20 Apr 2026 23:14:16 GMT
WORKDIR /home/gradle
# Mon, 20 Apr 2026 23:14:20 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 20 Apr 2026 23:14:20 GMT
ENV GRADLE_VERSION=9.4.1
# Mon, 20 Apr 2026 23:14:20 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Mon, 20 Apr 2026 23:14:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 20 Apr 2026 23:14:25 GMT
USER gradle
# Mon, 20 Apr 2026 23:14:26 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 20 Apr 2026 23:14:26 GMT
USER root
```

-	Layers:
	-	`sha256:8aaf81d11ba9b2394d31694793b5dabaf4eed2f5a356c7de160384c76fcf3161`  
		Last Modified: Mon, 20 Apr 2026 12:17:52 GMT  
		Size: 32.7 MB (32690247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed296aa7f07597047f5286ee9ca2f7e6be1c2cba92dda8f3d62ccba13b950ce`  
		Last Modified: Mon, 20 Apr 2026 23:04:15 GMT  
		Size: 37.4 MB (37402032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d30e3d4ffc42c532d4807aae55703d4f501fef0e89fd6171feb03288252f3ce`  
		Last Modified: Mon, 20 Apr 2026 23:04:50 GMT  
		Size: 93.4 MB (93395906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ac919073e134675293bf4c365e2af8fe47d4c98e62e1aee8b84f4fee5562bf`  
		Last Modified: Mon, 20 Apr 2026 23:04:48 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b5bb791f909a4d48414b08b0496c9d88c22f9283b870237c57b5e8a45de2b3`  
		Last Modified: Mon, 20 Apr 2026 23:04:48 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6484a00fc192034ef19d7047fcc6b51e794ce92eac26f7c1a2284d346608ecb5`  
		Last Modified: Mon, 20 Apr 2026 23:14:46 GMT  
		Size: 1.6 KB (1582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e39b6407248dd9fb00a257469620647bdc933195123ff1c0a7e0755c2877f7`  
		Last Modified: Mon, 20 Apr 2026 23:14:48 GMT  
		Size: 38.3 MB (38299096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01413fe4c33da039f557c88c3029fdebb02981fc9009baf3660abb4717a1683`  
		Last Modified: Mon, 20 Apr 2026 23:14:50 GMT  
		Size: 137.8 MB (137808337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ba37981457faffc632b5ee3b7a569b28f9fe8605fac9035ec55513014e8b58`  
		Last Modified: Mon, 20 Apr 2026 23:14:46 GMT  
		Size: 29.3 KB (29339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk26-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:09aad905aa5da12f8c10debb7fa6ac0763361c4bc5803ebdec11fc9f7e09dfc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7015307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb5ed99bf35262cc063a05db5c52297b44fb5121fc5d254d8307d35b5a300f0b`

```dockerfile
```

-	Layers:
	-	`sha256:00383b6f1bb8920ce7f3de80d439010c1647b921fb666665493b2f5d7b07f2e9`  
		Last Modified: Mon, 20 Apr 2026 23:14:46 GMT  
		Size: 7.0 MB (6990701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56112866a757802dcb2a96e31c5162a27261cf96a8f347cc6d41ad6089fbca66`  
		Last Modified: Mon, 20 Apr 2026 23:14:46 GMT  
		Size: 24.6 KB (24606 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk26-ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:2047176c154dcf889d97444159a214f0ea225670b5613ae992d561c7b37caa37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.0 MB (350043427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5fb3a65be60abc50fa48e1ce3b1b62dc70ee92fc9263002c2979464acf9e4f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 20 Apr 2026 01:03:47 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 20 Apr 2026 01:03:47 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 20 Apr 2026 01:03:47 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 20 Apr 2026 01:03:47 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 20 Apr 2026 01:03:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 20 Apr 2026 01:03:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 20 Apr 2026 01:03:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 01:03:47 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 01:03:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 20 Apr 2026 01:03:47 GMT
LABEL io.openshift.expose-services=""
# Mon, 20 Apr 2026 01:03:47 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 20 Apr 2026 01:03:47 GMT
ENV container oci
# Mon, 20 Apr 2026 01:03:48 GMT
COPY dir:56f7e656d3890224e75a1a16ae5067199386e27e9adfa336ba5808545546cc9e in /      
# Mon, 20 Apr 2026 01:03:48 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 20 Apr 2026 01:03:48 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 01:03:48 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 20 Apr 2026 01:03:48 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 20 Apr 2026 01:03:48 GMT
COPY file:7bbce3df91c54303354eb2bfc2cec747cbe675dbc724bafe59b7a5adbf9432ea in /usr/share/buildinfo/labels.json      
# Mon, 20 Apr 2026 01:03:48 GMT
COPY file:7bbce3df91c54303354eb2bfc2cec747cbe675dbc724bafe59b7a5adbf9432ea in /root/buildinfo/labels.json      
# Mon, 20 Apr 2026 01:03:49 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="32540b060e1a63cad21d656f09cff9da51482dc3" "org.opencontainers.image.revision"="32540b060e1a63cad21d656f09cff9da51482dc3" "build-date"="2026-04-20T01:03:36Z" "org.opencontainers.image.created"="2026-04-20T01:03:36Z" "release"="1776646707"org.opencontainers.image.revision=32540b060e1a63cad21d656f09cff9da51482dc3,org.opencontainers.image.created=2026-04-20T01:03:36Z
# Mon, 20 Apr 2026 23:00:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Apr 2026 23:00:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 23:00:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Apr 2026 23:00:58 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:00:58 GMT
ENV JAVA_VERSION=jdk-26+35
# Mon, 20 Apr 2026 23:10:04 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e8ff1f23c5acef74d1b4937dadd67286d67be06758f5d9dca5478c35bf404e83';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64le)          ESUM='7396fc32c311429c4b1573ebfc98eca6b82c2735f9f0e23acbccdcb43e0edee9';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='87fcdbbfd0adfd458922d8f8019eda23755aba597e386de2397f84cdf1b58808';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_s390x_linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='68e19ba53b7f1f74635c13f809e5db36cebccf3ae9e752423dd92d2ad7d831ef';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_x64_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 20 Apr 2026 23:10:08 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Apr 2026 23:10:09 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Apr 2026 23:10:09 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Apr 2026 23:10:09 GMT
CMD ["jshell"]
# Tue, 21 Apr 2026 00:00:49 GMT
CMD ["gradle"]
# Tue, 21 Apr 2026 00:00:49 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 21 Apr 2026 00:00:49 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 21 Apr 2026 00:00:49 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 21 Apr 2026 00:00:50 GMT
WORKDIR /home/gradle
# Tue, 21 Apr 2026 00:01:19 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 21 Apr 2026 00:01:19 GMT
ENV GRADLE_VERSION=9.4.1
# Tue, 21 Apr 2026 00:01:19 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Tue, 21 Apr 2026 00:01:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 21 Apr 2026 00:01:28 GMT
USER gradle
# Tue, 21 Apr 2026 00:01:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 21 Apr 2026 00:01:31 GMT
USER root
```

-	Layers:
	-	`sha256:6d2ce28440d2316b24b69c4ac9181a2021fc4fbcccd08e544cb55b3f85789742`  
		Last Modified: Mon, 20 Apr 2026 12:18:07 GMT  
		Size: 38.7 MB (38691389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55d8a467e0af186e4504fef70fa25944d04fcadf33d89978c86033d4efabe13`  
		Last Modified: Mon, 20 Apr 2026 23:01:39 GMT  
		Size: 39.2 MB (39213371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0d355788d029f5eb9a704b03869fb3d9a1ad73b1dfd25f03722691cdf346a6`  
		Last Modified: Mon, 20 Apr 2026 23:10:52 GMT  
		Size: 93.8 MB (93783012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3217065b5268d515a7cfd8aad88a5358e851d5ecc6cc562a1f89ff5c58ffceb`  
		Last Modified: Mon, 20 Apr 2026 23:10:48 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b9e52a32e7b7ba081138be3b8a2f80b9e51eaad134af741521c1fb5e2f7d30`  
		Last Modified: Mon, 20 Apr 2026 23:10:49 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6fee521705b672773f88c6f9d2667f0b01eefe83c027c2fb59b5641df6653aa`  
		Last Modified: Tue, 21 Apr 2026 00:02:10 GMT  
		Size: 1.6 KB (1584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812a77d2bc630743d0652667f2fc1ef38acddaf648c15dcfac8c87a61cbc9647`  
		Last Modified: Tue, 21 Apr 2026 00:02:12 GMT  
		Size: 40.5 MB (40542904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb1d0176847682d99ba51877a69a8bd358b5b1de66942f4df92f9c05283f80d`  
		Last Modified: Tue, 21 Apr 2026 00:02:16 GMT  
		Size: 137.8 MB (137808338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5588ced13db41c7fc561e341479550aac67f7fe04efa5196c06e8a5b613034`  
		Last Modified: Tue, 21 Apr 2026 00:02:10 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk26-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:95458d809a0f20ddd67802dad9318399872662c9c5caee5c8fe0dcefdfbdbc45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6992283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a30c062eb941050e5e3b64862c57985e353bd29c952bd1d60f39f8daba312a`

```dockerfile
```

-	Layers:
	-	`sha256:91ec72a4cfa4a2c8a1208fbe40b1d9e264542ed5883689128ab9287680e9df47`  
		Last Modified: Tue, 21 Apr 2026 00:02:11 GMT  
		Size: 7.0 MB (6967802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:931e797b27f6c6d6db40ee3d5efa7c33327f472b97b6016dc1a73048f54978d1`  
		Last Modified: Tue, 21 Apr 2026 00:02:10 GMT  
		Size: 24.5 KB (24481 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk26-ubi` - linux; s390x

```console
$ docker pull gradle@sha256:0fe61a906860d168a94e96cebc0e7126f0d5fa9754eb7d3c2a75297792717703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.6 MB (341558217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:889a1049922fd154ee83ef01e160b12fda4eec788760b1f80338682796145575`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 20 Apr 2026 01:16:10 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 20 Apr 2026 01:16:10 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 20 Apr 2026 01:16:10 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 20 Apr 2026 01:16:10 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 20 Apr 2026 01:16:10 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 20 Apr 2026 01:16:10 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 20 Apr 2026 01:16:10 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 01:16:10 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 01:16:10 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 20 Apr 2026 01:16:10 GMT
LABEL io.openshift.expose-services=""
# Mon, 20 Apr 2026 01:16:10 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 20 Apr 2026 01:16:10 GMT
ENV container oci
# Mon, 20 Apr 2026 01:16:10 GMT
COPY dir:4e87af2731f02be78cfc1976cd162db8d3f5c4fdd7c727c77a82a99e955d0442 in /      
# Mon, 20 Apr 2026 01:16:10 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 20 Apr 2026 01:16:10 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 01:16:10 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 20 Apr 2026 01:16:10 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 20 Apr 2026 01:16:10 GMT
COPY file:a467820b7ca76dd041fea2ae09e903a742727218438d9088812b788d84b3bf37 in /usr/share/buildinfo/labels.json      
# Mon, 20 Apr 2026 01:16:10 GMT
COPY file:a467820b7ca76dd041fea2ae09e903a742727218438d9088812b788d84b3bf37 in /root/buildinfo/labels.json      
# Mon, 20 Apr 2026 01:16:11 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="32540b060e1a63cad21d656f09cff9da51482dc3" "org.opencontainers.image.revision"="32540b060e1a63cad21d656f09cff9da51482dc3" "build-date"="2026-04-20T01:15:28Z" "org.opencontainers.image.created"="2026-04-20T01:15:28Z" "release"="1776646707"org.opencontainers.image.revision=32540b060e1a63cad21d656f09cff9da51482dc3,org.opencontainers.image.created=2026-04-20T01:15:28Z
# Mon, 20 Apr 2026 23:04:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Apr 2026 23:04:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 23:04:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Apr 2026 23:04:17 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:04:17 GMT
ENV JAVA_VERSION=jdk-26+35
# Mon, 20 Apr 2026 23:16:49 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e8ff1f23c5acef74d1b4937dadd67286d67be06758f5d9dca5478c35bf404e83';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64le)          ESUM='7396fc32c311429c4b1573ebfc98eca6b82c2735f9f0e23acbccdcb43e0edee9';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='87fcdbbfd0adfd458922d8f8019eda23755aba597e386de2397f84cdf1b58808';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_s390x_linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='68e19ba53b7f1f74635c13f809e5db36cebccf3ae9e752423dd92d2ad7d831ef';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_x64_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 20 Apr 2026 23:16:59 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Apr 2026 23:17:04 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Apr 2026 23:17:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Apr 2026 23:17:04 GMT
CMD ["jshell"]
# Tue, 21 Apr 2026 00:04:59 GMT
CMD ["gradle"]
# Tue, 21 Apr 2026 00:04:59 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 21 Apr 2026 00:04:59 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 21 Apr 2026 00:04:59 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 21 Apr 2026 00:04:59 GMT
WORKDIR /home/gradle
# Tue, 21 Apr 2026 00:06:27 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 21 Apr 2026 00:06:27 GMT
ENV GRADLE_VERSION=9.4.1
# Tue, 21 Apr 2026 00:06:27 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Tue, 21 Apr 2026 00:07:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 21 Apr 2026 00:07:38 GMT
USER gradle
# Tue, 21 Apr 2026 00:07:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 21 Apr 2026 00:07:42 GMT
USER root
```

-	Layers:
	-	`sha256:04715052fbc06c0056775e78575e0b8f757abb3e43e5f7db21d195f303d81dc7`  
		Last Modified: Mon, 20 Apr 2026 12:17:59 GMT  
		Size: 34.4 MB (34449818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634ad98208e9fa699c94890ad966ce076aba8c7dd5d326a137e414df039960d5`  
		Last Modified: Mon, 20 Apr 2026 23:07:01 GMT  
		Size: 37.8 MB (37842246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed555e8ce9643f75fd3dbdef1aa79bb9e5f15deadafdc7c04f52b1ba3dac6040`  
		Last Modified: Mon, 20 Apr 2026 23:19:12 GMT  
		Size: 90.5 MB (90548283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be605ec32b71ba1556107d59abbcd4bcb45c91ca896d4194e2fbae06915621e`  
		Last Modified: Mon, 20 Apr 2026 23:19:00 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6697bc5827987e99bfdb03a43ae8a0b0200b3d1bce4bb4c3a01cc4db11011ae3`  
		Last Modified: Mon, 20 Apr 2026 23:19:04 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e3bcec0f3d8c3a4897904bc2e1bce7ff978b87b37d67dcc783930e3965d5db`  
		Last Modified: Tue, 21 Apr 2026 00:09:11 GMT  
		Size: 1.6 KB (1596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfcd0155d96edfe17f9e76b301a49f1a1f4d32a3f08746c68095dbb9b2162142`  
		Last Modified: Tue, 21 Apr 2026 00:09:17 GMT  
		Size: 40.9 MB (40905102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5661632ee40c9fe5dfa65a805bae2af9db92035a7fc9627943f33edd719371`  
		Last Modified: Tue, 21 Apr 2026 00:09:21 GMT  
		Size: 137.8 MB (137808341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3802bfff122ecc068294d62a43fe16b0f0a0dd865da900f68b9db535aef82d`  
		Last Modified: Tue, 21 Apr 2026 00:09:11 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk26-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:d9bafebfe20a27c87267ef6c3de8c1a8a2ee496c41083973e812cf1c9d7c444d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6982688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c31936647b7cc505428f73b25a9ebd4beca468c2e7c50b9e452c1674795c62a3`

```dockerfile
```

-	Layers:
	-	`sha256:226712c85107d16d56f0176f3a1829220a3ace7a12e7d39c92247089d0efdefe`  
		Last Modified: Tue, 21 Apr 2026 00:09:14 GMT  
		Size: 7.0 MB (6958281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e5f6b106aad1368d1970664a49dc6be09c895a33c7dba81813d723db5ec51c6`  
		Last Modified: Tue, 21 Apr 2026 00:09:10 GMT  
		Size: 24.4 KB (24407 bytes)  
		MIME: application/vnd.in-toto+json
