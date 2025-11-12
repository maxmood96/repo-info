## `gradle:jdk25-ubi-minimal`

```console
$ docker pull gradle@sha256:f9dfa1abb26bc759662b43b121b56b48d6f14b7ce45c9b12083b1b15efea7ea9
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

### `gradle:jdk25-ubi-minimal` - linux; amd64

```console
$ docker pull gradle@sha256:a5b11a842b6cccf5a0ee67dbb9534d8c90c44fa5f2df81b43a291a9280bcb498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.5 MB (358505556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed6374409686d485fc298dae622167ca44f6c955e5e175902c9b53ebb0740fba`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 03 Nov 2025 17:11:07 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 17:11:07 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 17:11:07 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 17:11:07 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 03 Nov 2025 17:11:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 17:11:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 03 Nov 2025 17:11:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 17:11:08 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 17:11:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 03 Nov 2025 17:11:08 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 17:11:08 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 03 Nov 2025 17:11:08 GMT
LABEL compose-id="RHEL-10.1-updates-20251031.1"
# Mon, 03 Nov 2025 17:11:09 GMT
ENV container oci
# Mon, 03 Nov 2025 17:11:10 GMT
COPY dir:b2070c3a584696dfa50295995b98f1ca6f69ef03e4ee4a779757baf0b56a1546 in /      
# Mon, 03 Nov 2025 17:11:10 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 17:11:10 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 17:11:10 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 17:11:10 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 17:11:10 GMT
COPY file:e8d237b49ae34a5f140de55c7c082573fef974034e3d7ddb0b43a196c7b15275 in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 17:11:11 GMT
COPY file:e8d237b49ae34a5f140de55c7c082573fef974034e3d7ddb0b43a196c7b15275 in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 17:11:12 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="95310b85c4dfa1ed23494ca51d86f210cb1256bf" "org.opencontainers.image.revision"="95310b85c4dfa1ed23494ca51d86f210cb1256bf" "build-date"="2025-11-03T17:10:18Z" "release"="1762189639"org.opencontainers.image.revision=95310b85c4dfa1ed23494ca51d86f210cb1256bf
# Wed, 12 Nov 2025 18:38:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Nov 2025 18:38:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 18:38:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 12 Nov 2025 18:38:44 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 12 Nov 2025 18:38:44 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Wed, 12 Nov 2025 18:38:49 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5c83b7d2121ed482fd06831a1eba1633dbab818aba6addddf48e075b97e6e9b8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='54fdfbfa2c463863bd0c2c9c19901320d25ca533f31daa0bd866c4104af7ce5b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='1b627ec601998e5450fd1af91ae26a43b4d646403a8938d7efe4dfb2848fd896';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8daf77d1aacffe38c9889689bc224a13557de77559d9a5bb91991e6a298baa0d';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 12 Nov 2025 18:38:51 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 12 Nov 2025 18:38:51 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 12 Nov 2025 18:38:51 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 12 Nov 2025 18:38:51 GMT
CMD ["jshell"]
# Wed, 12 Nov 2025 19:10:32 GMT
CMD ["gradle"]
# Wed, 12 Nov 2025 19:10:32 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 12 Nov 2025 19:10:32 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 12 Nov 2025 19:10:32 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 12 Nov 2025 19:10:32 GMT
WORKDIR /home/gradle
# Wed, 12 Nov 2025 19:10:37 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 12 Nov 2025 19:10:37 GMT
ENV GRADLE_VERSION=9.2.0
# Wed, 12 Nov 2025 19:10:37 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Wed, 12 Nov 2025 19:10:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 12 Nov 2025 19:10:40 GMT
USER gradle
# Wed, 12 Nov 2025 19:10:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 12 Nov 2025 19:10:40 GMT
USER root
```

-	Layers:
	-	`sha256:e2fb7c31c3da29493a9042fb2aac284034d054c3aa5fe92e1f234b9e077ede47`  
		Last Modified: Wed, 12 Nov 2025 00:12:41 GMT  
		Size: 34.2 MB (34167037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b17e08df907561de38c89fac753f2efb43f3183538d8cdf9e4412d52c4c8a8`  
		Last Modified: Wed, 12 Nov 2025 18:39:28 GMT  
		Size: 57.7 MB (57665467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b173e797038fdd6568ab17fe9770ad2369594199d2679cace013d9358baa1da`  
		Last Modified: Wed, 12 Nov 2025 18:39:25 GMT  
		Size: 92.0 MB (92046688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a0f92ed539f23deffb6da5ba699c6baa821a9c2940a0a81b35b4f407cb184f`  
		Last Modified: Wed, 12 Nov 2025 18:39:18 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad3d9fafc51138c38d6fd9e6989a78564125179e3db33f4d5d2f49c75b29c6c`  
		Last Modified: Wed, 12 Nov 2025 18:39:14 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb70f552e5542a8e54cb03c8ca58248bc9fb5913c17b4ebcaf4b5561ca8dff9`  
		Last Modified: Wed, 12 Nov 2025 19:11:18 GMT  
		Size: 1.6 KB (1618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5103033ff6102b3b2d12910376e49827c8603beb3e48d607a38a8d8c871f96`  
		Last Modified: Wed, 12 Nov 2025 19:11:21 GMT  
		Size: 39.0 MB (39045740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c521360bb64d858d71ebcf3f88e6e9320e6638ccee51460f4363e4550fe81c`  
		Last Modified: Wed, 12 Nov 2025 19:11:05 GMT  
		Size: 135.5 MB (135521662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a1097eecc9639439644387c956c50dc3bcb6b1371fad56875d2c979edd92cb`  
		Last Modified: Wed, 12 Nov 2025 19:11:18 GMT  
		Size: 54.9 KB (54895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk25-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:1b6679a7124a493e1a9a4a6bc8321e0c575c1188fd1a2a4f227376d8bbb1c2e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8902854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e1773763e05915a9abd0f2f3ee4043129e757bfa70fb9bbc2b1a008308092b`

```dockerfile
```

-	Layers:
	-	`sha256:00290e71009510ee9c77dffbbc3202429a5b12452ca1a2fee1a8caceb9c775a5`  
		Last Modified: Wed, 12 Nov 2025 21:21:05 GMT  
		Size: 8.9 MB (8877834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09321c6511dcb46a646cf9e0a73a2abf4574221135dd1479e6741391d40893b9`  
		Last Modified: Wed, 12 Nov 2025 21:21:06 GMT  
		Size: 25.0 KB (25020 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk25-ubi-minimal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:e8493365a122731f9217ff49bc552f2892d0df00b9c23e5d96724a3128c9cbf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.9 MB (354872978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b6f3266eeba34a584c6754aa446f9ed88bc6162d9e08fbdbe80ce2c6e03b65`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 03 Nov 2025 17:14:06 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 17:14:06 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 17:14:06 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 17:14:06 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 03 Nov 2025 17:14:06 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 17:14:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 03 Nov 2025 17:14:06 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 17:14:06 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 17:14:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 03 Nov 2025 17:14:06 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 17:14:06 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 03 Nov 2025 17:14:06 GMT
LABEL compose-id="RHEL-10.1-updates-20251031.1"
# Mon, 03 Nov 2025 17:14:06 GMT
ENV container oci
# Mon, 03 Nov 2025 17:14:07 GMT
COPY dir:c8db51b55d4ac263e724340de097ab5a5aa8fea3d84a7bc887161a3f2c5d43d6 in /      
# Mon, 03 Nov 2025 17:14:07 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 17:14:07 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 17:14:07 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 17:14:07 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 17:14:07 GMT
COPY file:fb36c295d366f4dba8ba95e1629c37ca6425e3e98ba006db98d86ebcf2c79b44 in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 17:14:07 GMT
COPY file:fb36c295d366f4dba8ba95e1629c37ca6425e3e98ba006db98d86ebcf2c79b44 in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 17:14:08 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="95310b85c4dfa1ed23494ca51d86f210cb1256bf" "org.opencontainers.image.revision"="95310b85c4dfa1ed23494ca51d86f210cb1256bf" "build-date"="2025-11-03T17:13:46Z" "release"="1762189639"org.opencontainers.image.revision=95310b85c4dfa1ed23494ca51d86f210cb1256bf
# Wed, 12 Nov 2025 19:39:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Nov 2025 19:39:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 19:39:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 12 Nov 2025 19:39:45 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 12 Nov 2025 19:39:45 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Wed, 12 Nov 2025 19:41:01 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5c83b7d2121ed482fd06831a1eba1633dbab818aba6addddf48e075b97e6e9b8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='54fdfbfa2c463863bd0c2c9c19901320d25ca533f31daa0bd866c4104af7ce5b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='1b627ec601998e5450fd1af91ae26a43b4d646403a8938d7efe4dfb2848fd896';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8daf77d1aacffe38c9889689bc224a13557de77559d9a5bb91991e6a298baa0d';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 12 Nov 2025 19:41:02 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 12 Nov 2025 19:41:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 12 Nov 2025 19:41:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 12 Nov 2025 19:41:02 GMT
CMD ["jshell"]
# Wed, 12 Nov 2025 20:09:54 GMT
CMD ["gradle"]
# Wed, 12 Nov 2025 20:09:54 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 12 Nov 2025 20:09:54 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 12 Nov 2025 20:09:54 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 12 Nov 2025 20:09:54 GMT
WORKDIR /home/gradle
# Wed, 12 Nov 2025 20:10:02 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 12 Nov 2025 20:10:02 GMT
ENV GRADLE_VERSION=9.2.0
# Wed, 12 Nov 2025 20:10:02 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Wed, 12 Nov 2025 20:10:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 12 Nov 2025 20:10:06 GMT
USER gradle
# Wed, 12 Nov 2025 20:10:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 12 Nov 2025 20:10:07 GMT
USER root
```

-	Layers:
	-	`sha256:f1037a79a8a82585aa3e6b5df2e6c0a42e2f3def0513fef76cfd1daba7331879`  
		Last Modified: Wed, 12 Nov 2025 00:12:43 GMT  
		Size: 32.2 MB (32192138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad645e777d64c22bd6d9e1aaf6c53b2c654db7b717762911e67109b28d786443`  
		Last Modified: Wed, 12 Nov 2025 19:40:21 GMT  
		Size: 57.5 MB (57456635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae80616e90913cdd3179bdb5cfac3d5ccb52d1967aec7de95dfec9760e21c85`  
		Last Modified: Wed, 12 Nov 2025 19:41:42 GMT  
		Size: 91.1 MB (91056294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc939b8993bf389811fe7021b851509f8a8ac9c3657c35de22aaf332ad31f060`  
		Last Modified: Wed, 12 Nov 2025 19:41:30 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8603d2308be6d8e82bbb6e9b1ce7992bcf34c3c7bb50393a1570dee00485170a`  
		Last Modified: Wed, 12 Nov 2025 19:41:30 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9678dd42cbd1d06a7f4b46e7fca8695911f93c4551e29d0837d5bff88a1c9e3`  
		Last Modified: Wed, 12 Nov 2025 20:10:50 GMT  
		Size: 1.6 KB (1621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a831cafbe24f014ed8af998b44cec660c5aef6fd5377553eff74f1bc31380c8a`  
		Last Modified: Wed, 12 Nov 2025 20:10:53 GMT  
		Size: 38.6 MB (38582639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3adf5b661965fb533fa8e4105183ac847ced379622db72d57ed58ecb6d33484e`  
		Last Modified: Wed, 12 Nov 2025 20:10:32 GMT  
		Size: 135.5 MB (135521666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9874e902db691b1a216bf732f304b491b44d12e510ebb2b5768ad2e7e9ee3e`  
		Last Modified: Wed, 12 Nov 2025 20:10:50 GMT  
		Size: 59.5 KB (59532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk25-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:c9c45ec5eea432e8db10716e06c01ee31f22009e2a7091567dbabb2ad6f3da56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8901416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59d06f33e80b316a11e3ab128619c92443fe71e0a6533b9077fe8f6341b98f5`

```dockerfile
```

-	Layers:
	-	`sha256:8694cc27fbcfc7e04ffbd1d16d929ca49777ab5b5a4c8c04523ec53b3112d4b0`  
		Last Modified: Wed, 12 Nov 2025 21:21:14 GMT  
		Size: 8.9 MB (8876175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9b8e6aa33574fa2304fcfebfb80401bdc86f370b14c27d78f4ea560c4ef9914`  
		Last Modified: Wed, 12 Nov 2025 21:21:15 GMT  
		Size: 25.2 KB (25241 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk25-ubi-minimal` - linux; ppc64le

```console
$ docker pull gradle@sha256:df7b6a77bdb6cf751336247430d7b995b3120842827c10bb838641f4ef72f714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.6 MB (360648169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b4a6cfc3439fea8c3cb0fb6570cb8bc70cbdcbd9270d8c7c956ea99f72fcd46`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 24 Sep 2025 07:41:36 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 24 Sep 2025 07:41:36 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 24 Sep 2025 07:41:36 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 24 Sep 2025 07:41:36 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.0"       cpe="cpe:/o:redhat:enterprise_linux:10.0"       distribution-scope="public"
# Wed, 24 Sep 2025 07:41:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 24 Sep 2025 07:41:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 24 Sep 2025 07:41:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 24 Sep 2025 07:41:36 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 24 Sep 2025 07:41:37 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 24 Sep 2025 07:41:37 GMT
LABEL io.openshift.expose-services=""
# Wed, 24 Sep 2025 07:41:37 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 24 Sep 2025 07:41:37 GMT
ENV container oci
# Wed, 24 Sep 2025 07:41:37 GMT
COPY dir:8763112df95fa3ba21bfe4559d1c3d20c94187edd97f0aa385c49c1a78ac67c8 in /      
# Wed, 24 Sep 2025 07:41:37 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 24 Sep 2025 07:41:37 GMT
CMD ["/bin/bash"]
# Wed, 24 Sep 2025 07:41:37 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 24 Sep 2025 07:41:37 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 24 Sep 2025 07:41:37 GMT
COPY file:9d60118773670fbee148c27ca84d2373a59792c5d57f8118d19be9e19f60f51c in /root/buildinfo/labels.json      
# Wed, 24 Sep 2025 07:41:38 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="1cf4bca0a0a9b1becc90c8497d13ba99950d480a" "org.opencontainers.image.revision"="1cf4bca0a0a9b1becc90c8497d13ba99950d480a" "build-date"="2025-09-24T07:41:26Z" "release"="1758699349"org.opencontainers.image.revision=1cf4bca0a0a9b1becc90c8497d13ba99950d480a
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Sep 2025 19:59:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Sep 2025 19:59:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_VERSION=jdk-25+36
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='95716d04bdfc8b10c94f4448ea8d57a3ba872d98b53c752e4c6b48f1c95bc582';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_aarch64_linux_hotspot_25_36.tar.gz';          ;;        ppc64le)          ESUM='b060bb12b3a192a0599f03ebb9495492f78c48cb61e291e336a8b00e7798ffb0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_ppc64le_linux_hotspot_25_36.tar.gz';          ;;        s390x)          ESUM='3e476e40f920ccfb1915d200bc7a1fba9d68c4adcc0358c5968d15613690b915';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_s390x_linux_hotspot_25_36.tar.gz';          ;;        x86_64)          ESUM='ee04de95ab9da7287d40bd2173076ecc2a6dd662f007bedfc6eb0380c0ef90e8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_x64_linux_hotspot_25_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Sep 2025 19:59:06 GMT
CMD ["jshell"]
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["gradle"]
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 30 Sep 2025 09:31:25 GMT
WORKDIR /home/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_VERSION=9.1.0
# Tue, 30 Sep 2025 09:31:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER gradle
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER root
```

-	Layers:
	-	`sha256:03509b72270b34907502615cd7096986a2eeeff33db581c7c8a4d6e63773a680`  
		Last Modified: Wed, 24 Sep 2025 12:11:54 GMT  
		Size: 36.8 MB (36778911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7594fd32628be065d0a211a204c694db88e721d2972b272697f3be160b1b4984`  
		Last Modified: Wed, 24 Sep 2025 21:32:05 GMT  
		Size: 57.1 MB (57088198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873d189906773da04504ca1b699f0893cd338fca6821944cb18078e73caab3fc`  
		Last Modified: Thu, 25 Sep 2025 21:11:10 GMT  
		Size: 91.6 MB (91608624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb4e497e69e481a933f35e40151aab55ebec66603c8f528e33ff70746ea0b2c`  
		Last Modified: Thu, 25 Sep 2025 21:11:02 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b279e8454cdf4b892bd2a109b64615c6fe30d47e3b5f0e374b9c68c91dbab17`  
		Last Modified: Thu, 25 Sep 2025 21:11:02 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e7d31581661d7869662d93478938943f3670fc314de27eec33e955ffdb1bb1`  
		Last Modified: Tue, 30 Sep 2025 19:55:30 GMT  
		Size: 1.6 KB (1616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe586144c5eb73e9fa8f48d4dcba25cad818d220700a3743c5aade7e3fa2baee`  
		Last Modified: Tue, 30 Sep 2025 19:55:36 GMT  
		Size: 40.6 MB (40618607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d42b40a212feab67ee1c1b180a68bac275445fb6e934e63015a47cde61de7a`  
		Last Modified: Thu, 02 Oct 2025 15:14:11 GMT  
		Size: 134.5 MB (134514750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6723789153752ecbda0aedf89c66e2e70649384925a58a8f3dd97d2b8353eca`  
		Last Modified: Tue, 30 Sep 2025 19:55:31 GMT  
		Size: 35.0 KB (35011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk25-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:d129b1573e3e395ce774981ebd6b3252aeb2a140694383d221a4d1c1366a6568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8879800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a51567f0382bdc7658b2e0dfc428c88e1118de622ddb4f9f0c5395ec2311f2d`

```dockerfile
```

-	Layers:
	-	`sha256:dde29fac0426577b537eb9afd997169bd3e8f2372d534d4d4db2aa2fb72850e6`  
		Last Modified: Wed, 01 Oct 2025 20:25:15 GMT  
		Size: 8.9 MB (8854663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27793fd35029fb42eff27fb25f77b844e55a73e90816620d83b5a7520416dc4d`  
		Last Modified: Wed, 01 Oct 2025 20:25:16 GMT  
		Size: 25.1 KB (25137 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk25-ubi-minimal` - linux; s390x

```console
$ docker pull gradle@sha256:cad864d4418f28e0fbc9deda0b18efa6c6891c4bfc9d075555694718ffe7a4c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.8 MB (352806175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc001a75c7cc37c89f64c1c96e0a4edd52e458a2bebc3b11e90d9428469e8a4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 24 Sep 2025 07:53:07 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 24 Sep 2025 07:53:07 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 24 Sep 2025 07:53:07 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 24 Sep 2025 07:53:07 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.0"       cpe="cpe:/o:redhat:enterprise_linux:10.0"       distribution-scope="public"
# Wed, 24 Sep 2025 07:53:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 24 Sep 2025 07:53:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 24 Sep 2025 07:53:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 24 Sep 2025 07:53:07 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 24 Sep 2025 07:53:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 24 Sep 2025 07:53:07 GMT
LABEL io.openshift.expose-services=""
# Wed, 24 Sep 2025 07:53:07 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 24 Sep 2025 07:53:07 GMT
ENV container oci
# Wed, 24 Sep 2025 07:53:07 GMT
COPY dir:2c1fa1bd656078246346d6555e4507761c570da8e180dc87eb26a8c737f74cd5 in /      
# Wed, 24 Sep 2025 07:53:07 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 24 Sep 2025 07:53:07 GMT
CMD ["/bin/bash"]
# Wed, 24 Sep 2025 07:53:08 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 24 Sep 2025 07:53:08 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 24 Sep 2025 07:53:08 GMT
COPY file:2603c76e37273f3a1d2d759b3376cb903e3b2c81e82bfad6aa27546d2fc0b0c4 in /root/buildinfo/labels.json      
# Wed, 24 Sep 2025 07:53:08 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="1cf4bca0a0a9b1becc90c8497d13ba99950d480a" "org.opencontainers.image.revision"="1cf4bca0a0a9b1becc90c8497d13ba99950d480a" "build-date"="2025-09-24T07:50:56Z" "release"="1758699349"org.opencontainers.image.revision=1cf4bca0a0a9b1becc90c8497d13ba99950d480a
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Sep 2025 19:59:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Sep 2025 19:59:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_VERSION=jdk-25+36
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='95716d04bdfc8b10c94f4448ea8d57a3ba872d98b53c752e4c6b48f1c95bc582';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_aarch64_linux_hotspot_25_36.tar.gz';          ;;        ppc64le)          ESUM='b060bb12b3a192a0599f03ebb9495492f78c48cb61e291e336a8b00e7798ffb0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_ppc64le_linux_hotspot_25_36.tar.gz';          ;;        s390x)          ESUM='3e476e40f920ccfb1915d200bc7a1fba9d68c4adcc0358c5968d15613690b915';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_s390x_linux_hotspot_25_36.tar.gz';          ;;        x86_64)          ESUM='ee04de95ab9da7287d40bd2173076ecc2a6dd662f007bedfc6eb0380c0ef90e8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_x64_linux_hotspot_25_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Sep 2025 19:59:06 GMT
CMD ["jshell"]
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["gradle"]
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 30 Sep 2025 09:31:25 GMT
WORKDIR /home/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_VERSION=9.1.0
# Tue, 30 Sep 2025 09:31:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER gradle
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER root
```

-	Layers:
	-	`sha256:2ef2239186ea9c000a30f781ed39af7418e33d673b592070070773399ccd8411`  
		Last Modified: Wed, 24 Sep 2025 12:11:54 GMT  
		Size: 33.4 MB (33412405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e96d81b8156c358ceeb24f51d3a912a38aae04fedf9060e1f8c03816d669cdf`  
		Last Modified: Wed, 24 Sep 2025 20:38:11 GMT  
		Size: 55.7 MB (55675136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d67a0f289d84d40426a5d667784a56dfdbf64746e610fb6ebc7eb16fd2d4cb`  
		Last Modified: Thu, 25 Sep 2025 21:10:29 GMT  
		Size: 88.2 MB (88209134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baafeb1fba5ea3c93d8e5d2dca10ffe492ba450ab9d32738f2a93a7d4583469f`  
		Last Modified: Thu, 25 Sep 2025 21:10:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0237ddcc03a286cda63dd78be7d946e71a6711cdf52d4de42c1ec1c94420e68f`  
		Last Modified: Thu, 25 Sep 2025 21:10:26 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0152e2d49a86ce751c5e9ee858017f4a546fa7242f7c9e80770e3ced27c5da4`  
		Last Modified: Tue, 30 Sep 2025 23:58:29 GMT  
		Size: 1.6 KB (1614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282a07963dc1d59ba333401c2dec07edbb9ae18bf5c0131ef2443dbfbb36324f`  
		Last Modified: Tue, 30 Sep 2025 23:58:32 GMT  
		Size: 41.0 MB (40955753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611d3ac407094136131b618cea1e7f34e09f203ec07ea35eba3a1ccd9a771a5a`  
		Last Modified: Thu, 02 Oct 2025 14:51:37 GMT  
		Size: 134.5 MB (134514680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81265919eee36212049643413c86668f6023560f50b0c62ec17f522c15fbb794`  
		Last Modified: Tue, 30 Sep 2025 23:58:29 GMT  
		Size: 35.0 KB (35002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk25-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:3644cb48e31068102d36c3183bc98eba202d087714d34a6633a5432fd26a490c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8869797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1deaf733abaef460064f8e2ee9ab79d8689886faf9c84e12ed01aa6df65a6bab`

```dockerfile
```

-	Layers:
	-	`sha256:ef4925dc6f2297f1d85df8b77d82af9e613ed2a0583da379f9dcc728afa292e8`  
		Last Modified: Wed, 01 Oct 2025 20:25:23 GMT  
		Size: 8.8 MB (8844746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4ff81cc0fab7f6c4b8e0d69bd687d4fdc237653820e529554d7c6ff8bdaa303`  
		Last Modified: Wed, 01 Oct 2025 20:25:24 GMT  
		Size: 25.1 KB (25051 bytes)  
		MIME: application/vnd.in-toto+json
