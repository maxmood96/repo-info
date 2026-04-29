## `gradle:ubi`

```console
$ docker pull gradle@sha256:6e168bf977566830282376b5a9d58ef958e6b7f65f18bc2bb45ba585d3702d4a
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

### `gradle:ubi` - linux; amd64

```console
$ docker pull gradle@sha256:4a2919cea294f0389dd9bad098c6fb38386a258dd9a5f180e40418c0b3231f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.4 MB (343374754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512301fe8bd73515c8b0d4588b2a32f2c2b25a9882c0672ed676f60210c18637`
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
# Wed, 22 Apr 2026 18:16:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 18:16:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 18:16:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Apr 2026 18:16:15 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 22 Apr 2026 18:16:15 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Wed, 22 Apr 2026 18:17:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='a9d73e711d967dc44896d4f430f73a68fd33590dabc29a7f2fb9f593425b854c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64le)          ESUM='b262b735b215173003766da36588d5f717dceada0286db41b439f93fb2ada468';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='15e5cbcadcf3d43623c31b825063cdc2817b9f1ba840b51dc6ef70e5d33c84e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='987387933b64b9833846dee373b640440d3e1fd48a04804ec01a6dbf718e8ab8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 22 Apr 2026 18:17:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 22 Apr 2026 18:17:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Apr 2026 18:17:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 22 Apr 2026 18:17:28 GMT
CMD ["jshell"]
# Tue, 28 Apr 2026 23:27:43 GMT
CMD ["gradle"]
# Tue, 28 Apr 2026 23:27:43 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 28 Apr 2026 23:27:43 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 28 Apr 2026 23:27:43 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 28 Apr 2026 23:27:43 GMT
WORKDIR /home/gradle
# Tue, 28 Apr 2026 23:27:48 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 28 Apr 2026 23:27:48 GMT
ENV GRADLE_VERSION=9.5.0
# Tue, 28 Apr 2026 23:27:48 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Tue, 28 Apr 2026 23:27:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 28 Apr 2026 23:27:50 GMT
USER gradle
# Tue, 28 Apr 2026 23:27:51 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 28 Apr 2026 23:27:51 GMT
USER root
```

-	Layers:
	-	`sha256:74bbdc6f81c25b3fa8d6367ec856d92f28db48c1860a008184a1d723c8d399cc`  
		Last Modified: Wed, 22 Apr 2026 06:14:16 GMT  
		Size: 34.6 MB (34590462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f685e5b87dd061925558e3c45ed769f2548d459f3d91eca60df9d864c51b411`  
		Last Modified: Wed, 22 Apr 2026 18:16:37 GMT  
		Size: 37.5 MB (37473579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd8c2c5a03638a9e12ba8211191883cc1fdfb202e4f7582ed793d8edbf51cb2`  
		Last Modified: Wed, 22 Apr 2026 18:17:48 GMT  
		Size: 92.3 MB (92257956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200e3b851b2c95f4bbae8b1a4c5b978410b5af8e66db0658205c1d7bf8155d7a`  
		Last Modified: Wed, 22 Apr 2026 18:17:45 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32604a7fe743873c814493cb57a6fcf12041cc45ba109e273908ca0b7d3e62c`  
		Last Modified: Wed, 22 Apr 2026 18:17:45 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbd0c9a950fa091a7729e142f8be412cb6efbd944210034a21eaabf5050aa09`  
		Last Modified: Tue, 28 Apr 2026 23:28:08 GMT  
		Size: 1.6 KB (1587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d722fb805b49f43430aea1b26803c86cbbabb4090d465dcf6aee373fcca17a`  
		Last Modified: Tue, 28 Apr 2026 23:28:10 GMT  
		Size: 38.8 MB (38787159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28d13c933a6c80dfbfc150121d89aa48be9160081b8cb65bce220ee8d86a0a4`  
		Last Modified: Tue, 28 Apr 2026 23:28:12 GMT  
		Size: 140.2 MB (140235944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef6e0e4cca1a902bbd896e8667ff5fa4e9446281943d48aac9fcb4a1212f6bc`  
		Last Modified: Tue, 28 Apr 2026 23:28:08 GMT  
		Size: 25.6 KB (25616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:32eab2f814c7e06549b1f338a7bc79c0d61180f2c87604728c2dd05d2b976027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7048852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46e13d36a980b3684f82a70c477948e38f512c4c7e7e306dd9dcde96eda7ab1`

```dockerfile
```

-	Layers:
	-	`sha256:d4250f39261f01a6c1191fccd1cf18d339777d15926cfb267dc2fbb6779611e9`  
		Last Modified: Tue, 28 Apr 2026 23:28:08 GMT  
		Size: 7.0 MB (7023839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17605d2fbc9041c5f6b7c5eb93c211205e5d83593e067aa3530850154d847d5e`  
		Last Modified: Tue, 28 Apr 2026 23:28:08 GMT  
		Size: 25.0 KB (25013 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:c11b647dd94ab74a18ea359ed0e22271d2a15cbd3369bd6551af7839b861480e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.0 MB (339989855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82be595dd0855dfde1ed9a5e9db0b197b2f0fe6b7debdb9a345af27e6d9909f9`
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
# Wed, 22 Apr 2026 18:16:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 18:16:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 18:16:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Apr 2026 18:16:05 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 22 Apr 2026 18:16:05 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Wed, 22 Apr 2026 18:16:47 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='a9d73e711d967dc44896d4f430f73a68fd33590dabc29a7f2fb9f593425b854c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64le)          ESUM='b262b735b215173003766da36588d5f717dceada0286db41b439f93fb2ada468';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='15e5cbcadcf3d43623c31b825063cdc2817b9f1ba840b51dc6ef70e5d33c84e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='987387933b64b9833846dee373b640440d3e1fd48a04804ec01a6dbf718e8ab8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 22 Apr 2026 18:16:48 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 22 Apr 2026 18:16:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Apr 2026 18:16:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 22 Apr 2026 18:16:48 GMT
CMD ["jshell"]
# Tue, 28 Apr 2026 23:28:01 GMT
CMD ["gradle"]
# Tue, 28 Apr 2026 23:28:01 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 28 Apr 2026 23:28:01 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 28 Apr 2026 23:28:01 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 28 Apr 2026 23:28:01 GMT
WORKDIR /home/gradle
# Tue, 28 Apr 2026 23:28:07 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 28 Apr 2026 23:28:07 GMT
ENV GRADLE_VERSION=9.5.0
# Tue, 28 Apr 2026 23:28:07 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Tue, 28 Apr 2026 23:28:09 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 28 Apr 2026 23:28:09 GMT
USER gradle
# Tue, 28 Apr 2026 23:28:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 28 Apr 2026 23:28:10 GMT
USER root
```

-	Layers:
	-	`sha256:e8c4c206e9282db63c5bc98a6b172b79a7673404566e305674f0176bf9808f38`  
		Last Modified: Wed, 22 Apr 2026 06:16:01 GMT  
		Size: 32.7 MB (32712089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51fe502eb3aa9412ac47fe447396fc11182e0577ef6af51affcc47ddd8eecc1`  
		Last Modified: Wed, 22 Apr 2026 18:16:31 GMT  
		Size: 37.4 MB (37416384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67239b7e94133c6266c97025276fdaf228e2d0414024ff567d65cf5ec037dc2`  
		Last Modified: Wed, 22 Apr 2026 18:17:12 GMT  
		Size: 91.3 MB (91297852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83d062b34b0541447c3679bf8706409bf22cc5bf3fdfb6fceb061c076b103b4`  
		Last Modified: Wed, 22 Apr 2026 18:17:04 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6af4fe7d6c9798de1d3a8f03d373d7e2062e422265fb2d04dcefe9f2a07a780`  
		Last Modified: Wed, 22 Apr 2026 18:17:04 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e547e31da148f575c1369d3907ecf2711e37202f0cfcf15174130229aa7a35f9`  
		Last Modified: Tue, 28 Apr 2026 23:28:29 GMT  
		Size: 1.6 KB (1588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5bd69ac17396480d7b646d717a3afa573b64560641a36e0e1e4ba62f6f8459`  
		Last Modified: Tue, 28 Apr 2026 23:28:31 GMT  
		Size: 38.3 MB (38294206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f8e64d21fc044e472b05010e781813fa273fad04027e493452103e6aafa5f8`  
		Last Modified: Tue, 28 Apr 2026 23:28:33 GMT  
		Size: 140.2 MB (140235945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24b9f6d0f1634dd55baf687d3f1c485ffa9c02ff0ce6a066e50f7bae9d779ab`  
		Last Modified: Tue, 28 Apr 2026 23:28:29 GMT  
		Size: 29.3 KB (29340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:ab66ea8f01388ac5be3329d2a10ce6048fc9feb68ea2e778b7a62ec19ffa53e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7047350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ec8ccead2c4c163b01012f84e513a3ff86c01856477b45a90ac3c9478baa676`

```dockerfile
```

-	Layers:
	-	`sha256:6270bae1d3ce3d0d915f521e02f26e88a56d70c18912853959f66428dd924ff0`  
		Last Modified: Tue, 28 Apr 2026 23:28:30 GMT  
		Size: 7.0 MB (7022116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16f3b877615e7ae7fe68ff1aff560aa5574196cf015ccc6bbe4189fe8ea17363`  
		Last Modified: Tue, 28 Apr 2026 23:28:29 GMT  
		Size: 25.2 KB (25234 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:afc7ec39b01bdc1d9bcd35de44d042cf9b3c7ac90fe6812ed33d0b2340e3fdc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.4 MB (350381961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a32a589fc2d3823ed0ce48acf6e9fd49e604a0a61f82f80e0e58f7454ad5330`
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
ENV JAVA_VERSION=jdk-25.0.2+10
# Wed, 22 Apr 2026 20:29:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='a9d73e711d967dc44896d4f430f73a68fd33590dabc29a7f2fb9f593425b854c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64le)          ESUM='b262b735b215173003766da36588d5f717dceada0286db41b439f93fb2ada468';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='15e5cbcadcf3d43623c31b825063cdc2817b9f1ba840b51dc6ef70e5d33c84e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='987387933b64b9833846dee373b640440d3e1fd48a04804ec01a6dbf718e8ab8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 22 Apr 2026 20:29:39 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 22 Apr 2026 20:29:40 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Apr 2026 20:29:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 22 Apr 2026 20:29:40 GMT
CMD ["jshell"]
# Tue, 28 Apr 2026 23:22:36 GMT
CMD ["gradle"]
# Tue, 28 Apr 2026 23:22:36 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 28 Apr 2026 23:22:36 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 28 Apr 2026 23:22:36 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 28 Apr 2026 23:22:36 GMT
WORKDIR /home/gradle
# Tue, 28 Apr 2026 23:23:11 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 28 Apr 2026 23:23:11 GMT
ENV GRADLE_VERSION=9.5.0
# Tue, 28 Apr 2026 23:23:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Tue, 28 Apr 2026 23:23:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 28 Apr 2026 23:23:16 GMT
USER gradle
# Tue, 28 Apr 2026 23:23:17 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 28 Apr 2026 23:23:17 GMT
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
	-	`sha256:5e476fe2a08b821d36fdeac5aeccd645207e9c025b7739dc9884852e908d237d`  
		Last Modified: Wed, 22 Apr 2026 20:30:17 GMT  
		Size: 91.6 MB (91634919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db25e3a380a314c5c8e575e1a5937963d6f20af316098de9dbf0d72e058dffa`  
		Last Modified: Wed, 22 Apr 2026 20:30:14 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf000b2e7bef536bd617a44880e9ea502ff1958adaf7b5c6f526ea5e1dc76399`  
		Last Modified: Wed, 22 Apr 2026 20:30:14 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8c9a19f019d247cdbf37cce7f10972645cc6cdcd434e0ac2eea37d8e4441f1`  
		Last Modified: Tue, 28 Apr 2026 23:23:54 GMT  
		Size: 1.6 KB (1594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69166904437d7d0d136e0ea68bde8231bc76a0cdbab15604f1d6f68755805362`  
		Last Modified: Tue, 28 Apr 2026 23:23:56 GMT  
		Size: 40.5 MB (40548515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7265e8fc43586a6600507d27dc2a5f772dc04b61894d1a0941f7a8283517612f`  
		Last Modified: Tue, 28 Apr 2026 23:23:58 GMT  
		Size: 140.2 MB (140235943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d4992b42b4e04b9e4b82839651b8f748269de06c4a4c034390e5f9350a7e14`  
		Last Modified: Tue, 28 Apr 2026 23:23:54 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:0c1f8841fb0f61eae3b38004e25234342851efe1eb67135fb5562adf3c168087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7023678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d663f43ede087181ed56f80963a83f940794b35556fef340ec3ea5e6401fdd`

```dockerfile
```

-	Layers:
	-	`sha256:a066c701b221a1467dd888751137fd840babd8bf1826faed5e28eb1a3e9e8523`  
		Last Modified: Tue, 28 Apr 2026 23:23:54 GMT  
		Size: 7.0 MB (6998581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c45ad4f780bfb548be7e7aad4a1956062bbd8735d6f63424f05e0e3f1a9d9ef`  
		Last Modified: Tue, 28 Apr 2026 23:23:54 GMT  
		Size: 25.1 KB (25097 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:ubi` - linux; s390x

```console
$ docker pull gradle@sha256:37754e737c662a2ceca6da46f4d25c36b166d7ec17f6003c66f0a35b1d53b6b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.7 MB (341661689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f86374dbbdbeb27bc43d41ce6cf08732338ba207d993dd2cb53f3c39843e49d2`
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
# Wed, 22 Apr 2026 18:16:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 18:16:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 18:16:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Apr 2026 18:16:25 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 22 Apr 2026 18:16:25 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Wed, 22 Apr 2026 18:23:07 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='a9d73e711d967dc44896d4f430f73a68fd33590dabc29a7f2fb9f593425b854c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64le)          ESUM='b262b735b215173003766da36588d5f717dceada0286db41b439f93fb2ada468';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='15e5cbcadcf3d43623c31b825063cdc2817b9f1ba840b51dc6ef70e5d33c84e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='987387933b64b9833846dee373b640440d3e1fd48a04804ec01a6dbf718e8ab8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 22 Apr 2026 18:23:14 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 22 Apr 2026 18:23:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Apr 2026 18:23:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 22 Apr 2026 18:23:16 GMT
CMD ["jshell"]
# Tue, 28 Apr 2026 23:34:50 GMT
CMD ["gradle"]
# Tue, 28 Apr 2026 23:34:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 28 Apr 2026 23:34:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 28 Apr 2026 23:34:50 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 28 Apr 2026 23:34:50 GMT
WORKDIR /home/gradle
# Tue, 28 Apr 2026 23:35:00 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 28 Apr 2026 23:35:00 GMT
ENV GRADLE_VERSION=9.5.0
# Tue, 28 Apr 2026 23:35:00 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Tue, 28 Apr 2026 23:35:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 28 Apr 2026 23:35:04 GMT
USER gradle
# Tue, 28 Apr 2026 23:35:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 28 Apr 2026 23:35:04 GMT
USER root
```

-	Layers:
	-	`sha256:59053ba8a9d1e0e09d61b1f59967bb9ffc4505ef8eebe01b4c6808d9bce8b3a6`  
		Last Modified: Wed, 22 Apr 2026 06:16:12 GMT  
		Size: 34.4 MB (34437922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f5f9f574b3daeca8f4702cc891ece0285c63d8e300411023f5895f380e9f97`  
		Last Modified: Wed, 22 Apr 2026 18:18:11 GMT  
		Size: 37.9 MB (37850017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9bee2882d5bf8e9711abff0b03dd91bbf2c83b0379310359746482c004c855`  
		Last Modified: Wed, 22 Apr 2026 18:24:41 GMT  
		Size: 88.2 MB (88235374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2deb2a87434b7a512841e3629f9f397f9917718327fbaf10e1ad29a256735b`  
		Last Modified: Wed, 22 Apr 2026 18:24:32 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28d75aefef7ee3db12ac9f022fc2909bc5790ba1bd22d59b4791428e0da1395`  
		Last Modified: Wed, 22 Apr 2026 18:24:33 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecc8c19e85025016f0a4db40178a7cf1ae26b4e45d2d1ed8fae1b2a5b1a05f1`  
		Last Modified: Tue, 28 Apr 2026 23:35:30 GMT  
		Size: 1.6 KB (1589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be47ddae7a2ef7644755927dc45fb0de453f992f2d0f59175ab4612132e7e3d8`  
		Last Modified: Tue, 28 Apr 2026 23:35:31 GMT  
		Size: 40.9 MB (40898026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3712a758cc9153f59d569625611b5ca0b9f88644ff43f9eb3c1ea993022f7e17`  
		Last Modified: Tue, 28 Apr 2026 23:35:33 GMT  
		Size: 140.2 MB (140235934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8a57e2fec35e7896e57311d6c61eae550498b6a4bfb842b4c2edd9063faf88`  
		Last Modified: Tue, 28 Apr 2026 23:35:30 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:1e094564546366791cf5923f93b346f77511a34c33d36c97479ec327624cca7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7014059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed3e77e9ac9583e46f5eb692fe5088626ce5cc76e17b4a1164f1c557a62133c`

```dockerfile
```

-	Layers:
	-	`sha256:d3642903fa2707aa416fc80cffabcd7e49ef2a6aa344ec2ddcecb22eba8e450b`  
		Last Modified: Tue, 28 Apr 2026 23:35:30 GMT  
		Size: 7.0 MB (6989048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7d0588b012820999762a2e5add03da6941bffd50d31f054896e5990613d36d7`  
		Last Modified: Tue, 28 Apr 2026 23:35:30 GMT  
		Size: 25.0 KB (25011 bytes)  
		MIME: application/vnd.in-toto+json
