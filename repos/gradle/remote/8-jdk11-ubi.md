## `gradle:8-jdk11-ubi`

```console
$ docker pull gradle@sha256:5e360c316464b86caa6c8fe8d560d192bac9cd3227baba360131341cf8fc2cc3
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

### `gradle:8-jdk11-ubi` - linux; amd64

```console
$ docker pull gradle@sha256:53bfdd3faece80669ad353bcaf6550fb3ce76cb2f18359b598ad45b29b94ade5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.0 MB (389982823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb028e4cd310bb8c08b974bec1d64ea1a9348615c7b46cdb9be6d7353e2fcbb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL io.openshift.expose-services=""
# Mon, 29 Jun 2026 04:51:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 29 Jun 2026 04:51:29 GMT
ENV container oci
# Mon, 29 Jun 2026 04:51:29 GMT
COPY dir:739d9f5e7f28cc70aad7ae94223fd7338511092b65f74c794a7b61ab61297289 in /      
# Mon, 29 Jun 2026 04:51:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 29 Jun 2026 04:51:29 GMT
CMD ["/bin/bash"]
# Mon, 29 Jun 2026 04:51:30 GMT
COPY dir:0d9e9fcd450f7954ea82dd60c01a9062c55769458d716bb966e758775cf44d8c in /usr/share/buildinfo/      
# Mon, 29 Jun 2026 04:51:30 GMT
COPY dir:0d9e9fcd450f7954ea82dd60c01a9062c55769458d716bb966e758775cf44d8c in /root/buildinfo/      
# Mon, 29 Jun 2026 04:51:30 GMT
LABEL "org.opencontainers.image.created"="2026-06-29T04:50:08Z" "org.opencontainers.image.revision"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "build-date"="2026-06-29T04:50:08Z" "architecture"="x86_64" "vcs-ref"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "vcs-type"="git" "release"="1782708562"org.opencontainers.image.created=2026-06-29T04:50:08Z,org.opencontainers.image.revision=b0536a5d45ebd046bef183288a4f1cd5e6d68f66
# Tue, 30 Jun 2026 00:10:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Jun 2026 00:10:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:10:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 30 Jun 2026 00:10:33 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 30 Jun 2026 00:10:33 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 30 Jun 2026 00:11:06 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 30 Jun 2026 00:11:07 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 30 Jun 2026 00:11:07 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 30 Jun 2026 00:11:07 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 30 Jun 2026 00:11:07 GMT
CMD ["jshell"]
# Tue, 30 Jun 2026 01:11:26 GMT
CMD ["gradle"]
# Tue, 30 Jun 2026 01:11:26 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Jun 2026 01:11:26 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 30 Jun 2026 01:11:26 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 30 Jun 2026 01:11:26 GMT
WORKDIR /home/gradle
# Tue, 30 Jun 2026 01:11:30 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 30 Jun 2026 01:11:30 GMT
ENV GRADLE_VERSION=8.14.5
# Tue, 30 Jun 2026 01:11:30 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Tue, 30 Jun 2026 01:11:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 30 Jun 2026 01:11:32 GMT
USER gradle
# Tue, 30 Jun 2026 01:11:33 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 30 Jun 2026 01:11:33 GMT
USER root
```

-	Layers:
	-	`sha256:49d891c4faa7e711f5655dc8fb5604fa8b30c65842b722ab503bcb4a08c3f5cc`  
		Last Modified: Mon, 29 Jun 2026 06:11:20 GMT  
		Size: 40.7 MB (40686817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf863bfad5c865bbca7848dc24c7d66181ab857c5ce404e8e90bea2c793f983`  
		Last Modified: Tue, 30 Jun 2026 00:10:52 GMT  
		Size: 30.9 MB (30877463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254a6c28a47971a2901caeefecafabaf3447fbe15d9411e63adcc07c35f8722d`  
		Last Modified: Tue, 30 Jun 2026 00:11:25 GMT  
		Size: 142.3 MB (142348846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9156149acd67a6882a337c074262c6177be7d036d4672e60f4f09461842a3605`  
		Last Modified: Tue, 30 Jun 2026 00:11:22 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d2d0c5181f4a11fc786c2e22aec262b725f5cead33d701871f7028eb960c16`  
		Last Modified: Tue, 30 Jun 2026 00:11:22 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5608e2bf2918b6a00f318e9eea463f8c517ff6890640ee46792b69c1134f6e83`  
		Last Modified: Tue, 30 Jun 2026 01:11:50 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f80180a8e95660ed87631cb3d3fc9688ac012ed62b6fcc819e4378424edef32`  
		Last Modified: Tue, 30 Jun 2026 01:11:51 GMT  
		Size: 37.9 MB (37942092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e09d42fa1c9b1de3cf9ea4bd1d9451f9904fe861584b103179cd05df3a4c54`  
		Last Modified: Tue, 30 Jun 2026 01:11:54 GMT  
		Size: 138.1 MB (138068538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f59f02698eae51097c3cefa08f7725eb3e61e701069bb9247a95731babba476`  
		Last Modified: Tue, 30 Jun 2026 01:11:50 GMT  
		Size: 54.9 KB (54907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:899a6c78ad7649891e0ab6ebf10353ac3c3f194f99bda6cecde7f87f44473525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5451050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6fa12984ebd858ee5256b8833256ff4fbd4c5d30db1bc534406c19b6443fa0f`

```dockerfile
```

-	Layers:
	-	`sha256:8e17d2aab187e24702949d871fa77a2978ecbf0ea37996fc5d38f97b54376936`  
		Last Modified: Tue, 30 Jun 2026 01:11:50 GMT  
		Size: 5.4 MB (5426597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:360a546392c3c6b3df88daf5b8547c6ae867c4992d07d7c418c67bbc4f7fa538`  
		Last Modified: Tue, 30 Jun 2026 01:11:50 GMT  
		Size: 24.5 KB (24453 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk11-ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:5c625946a4c7827d6ab4f165a063831c7e93b917d53f856e40b25a83e3bd5af7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.0 MB (384013864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8963294f21b2a46f76f415a01b90626ad0e0e61f3494cfb74148bda196b0e055`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:52:40 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 29 Jun 2026 04:52:40 GMT
LABEL io.openshift.expose-services=""
# Mon, 29 Jun 2026 04:52:40 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 29 Jun 2026 04:52:40 GMT
ENV container oci
# Mon, 29 Jun 2026 04:52:40 GMT
COPY dir:e6026d5a9734bc68758c885a994b1d95fd048fb5657a86e6b5e51129e847f4d9 in /      
# Mon, 29 Jun 2026 04:52:40 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 29 Jun 2026 04:52:40 GMT
CMD ["/bin/bash"]
# Mon, 29 Jun 2026 04:52:40 GMT
COPY dir:f71705f172541ee791b12a4ded058a688a198aeab58382823b47b8b83bf77d5d in /usr/share/buildinfo/      
# Mon, 29 Jun 2026 04:52:41 GMT
COPY dir:f71705f172541ee791b12a4ded058a688a198aeab58382823b47b8b83bf77d5d in /root/buildinfo/      
# Mon, 29 Jun 2026 04:52:41 GMT
LABEL "org.opencontainers.image.created"="2026-06-29T04:52:17Z" "org.opencontainers.image.revision"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "build-date"="2026-06-29T04:52:17Z" "architecture"="aarch64" "vcs-ref"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "vcs-type"="git" "release"="1782708562"org.opencontainers.image.created=2026-06-29T04:52:17Z,org.opencontainers.image.revision=b0536a5d45ebd046bef183288a4f1cd5e6d68f66
# Tue, 30 Jun 2026 00:09:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Jun 2026 00:09:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:09:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 30 Jun 2026 00:09:19 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 30 Jun 2026 00:09:19 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 30 Jun 2026 00:09:26 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 30 Jun 2026 00:09:27 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 30 Jun 2026 00:09:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 30 Jun 2026 00:09:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 30 Jun 2026 00:09:27 GMT
CMD ["jshell"]
# Tue, 30 Jun 2026 01:11:04 GMT
CMD ["gradle"]
# Tue, 30 Jun 2026 01:11:04 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Jun 2026 01:11:04 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 30 Jun 2026 01:11:04 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 30 Jun 2026 01:11:04 GMT
WORKDIR /home/gradle
# Tue, 30 Jun 2026 01:11:08 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 30 Jun 2026 01:11:08 GMT
ENV GRADLE_VERSION=8.14.5
# Tue, 30 Jun 2026 01:11:08 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Tue, 30 Jun 2026 01:11:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 30 Jun 2026 01:11:11 GMT
USER gradle
# Tue, 30 Jun 2026 01:11:12 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 30 Jun 2026 01:11:12 GMT
USER root
```

-	Layers:
	-	`sha256:6415421793d9d3697d4a730b8a3f7869954a938b640547194c623cb3a001e6c2`  
		Last Modified: Mon, 29 Jun 2026 06:11:28 GMT  
		Size: 38.8 MB (38819449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b1b1c78ab8f21d1fa459b695ee710fd1707a6fd973eb46e33b021b354b5bab`  
		Last Modified: Tue, 30 Jun 2026 00:09:44 GMT  
		Size: 30.8 MB (30794514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c05f0544cfb1b05acda219db7444f8841e8e483a33ed4fe792734b435b8b536`  
		Last Modified: Tue, 30 Jun 2026 00:09:46 GMT  
		Size: 139.0 MB (139040621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b488efd005394a794774d2caa03ee435f7fd3363133096c6bcb9bb41d692676e`  
		Last Modified: Tue, 30 Jun 2026 00:09:43 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce03c521360f23c468865b7411267472b82d348238405399230a92a9f70521f4`  
		Last Modified: Tue, 30 Jun 2026 00:09:43 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cbb380eb3a472f498c33a5b44411f267ed8c5c7e41d4287fe1c0138ada57e67`  
		Last Modified: Tue, 30 Jun 2026 01:11:28 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08ec7f790e6666059f4e112fbdcbf844c69ab47e77087e2e01553adbffe4f2a`  
		Last Modified: Tue, 30 Jun 2026 01:11:30 GMT  
		Size: 37.2 MB (37227031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46ed2238fe18ffef9a073bcc77d0866874f7b0bf16e5b99011d7bb2236f2d60`  
		Last Modified: Tue, 30 Jun 2026 01:11:32 GMT  
		Size: 138.1 MB (138068541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cffff75b7e02429f33527cbdbc2fb839f9601a42ca3808543969bfd7c11e4dc`  
		Last Modified: Tue, 30 Jun 2026 01:11:28 GMT  
		Size: 59.5 KB (59548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:5b36aeb9c6ea0613169cbea0c7b985ebda2c4c467adf47b868638bfa366522bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5449512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07336a2190be91ec43e62829547a3f98f9f2ee6470e67ba97d79b5d32f94d6b5`

```dockerfile
```

-	Layers:
	-	`sha256:01334f8a869fcfc321b64e77ff7d785fd5780e5d08364da25515c3c574a66fb6`  
		Last Modified: Tue, 30 Jun 2026 01:11:28 GMT  
		Size: 5.4 MB (5424863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e9b803a7a0a4155ae0e9032d88cc447a1d56e93e401e5004942532df011179f`  
		Last Modified: Tue, 30 Jun 2026 01:11:28 GMT  
		Size: 24.6 KB (24649 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk11-ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:3ccdef2bdbb33b9fb831774209e0279497953a94f40c66a9bfbf5e2e04bb1c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.1 MB (382074700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b42da9f52285376bdca110e5f85bdf0bf451cedf00d555778f05c30f229e24d9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 29 Jun 2026 04:51:43 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 29 Jun 2026 04:51:43 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 29 Jun 2026 04:51:43 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 29 Jun 2026 04:51:43 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 29 Jun 2026 04:51:43 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 29 Jun 2026 04:51:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 29 Jun 2026 04:51:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:51:43 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:51:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 29 Jun 2026 04:51:43 GMT
LABEL io.openshift.expose-services=""
# Mon, 29 Jun 2026 04:51:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 29 Jun 2026 04:51:43 GMT
ENV container oci
# Mon, 29 Jun 2026 04:51:44 GMT
COPY dir:4c1c925f52e2bf94f6f51ed2040707135dad2469062fae485083f1e3880aa690 in /      
# Mon, 29 Jun 2026 04:51:44 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 29 Jun 2026 04:51:44 GMT
CMD ["/bin/bash"]
# Mon, 29 Jun 2026 04:51:44 GMT
COPY dir:b37bcc35410383d4962d130d7f52524a29de2416d65cdbb7496d3441baade925 in /usr/share/buildinfo/      
# Mon, 29 Jun 2026 04:51:44 GMT
COPY dir:b37bcc35410383d4962d130d7f52524a29de2416d65cdbb7496d3441baade925 in /root/buildinfo/      
# Mon, 29 Jun 2026 04:51:44 GMT
LABEL "org.opencontainers.image.created"="2026-06-29T04:51:26Z" "org.opencontainers.image.revision"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "build-date"="2026-06-29T04:51:26Z" "architecture"="ppc64le" "vcs-ref"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "vcs-type"="git" "release"="1782708562"org.opencontainers.image.created=2026-06-29T04:51:26Z,org.opencontainers.image.revision=b0536a5d45ebd046bef183288a4f1cd5e6d68f66
# Tue, 30 Jun 2026 00:11:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Jun 2026 00:11:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:11:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 30 Jun 2026 00:11:34 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 30 Jun 2026 00:11:34 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 30 Jun 2026 00:12:32 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 30 Jun 2026 00:12:35 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 30 Jun 2026 00:12:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 30 Jun 2026 00:12:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 30 Jun 2026 00:12:36 GMT
CMD ["jshell"]
# Tue, 30 Jun 2026 01:10:49 GMT
CMD ["gradle"]
# Tue, 30 Jun 2026 01:10:49 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Jun 2026 01:10:49 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 30 Jun 2026 01:10:49 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 30 Jun 2026 01:10:49 GMT
WORKDIR /home/gradle
# Tue, 30 Jun 2026 01:11:03 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 30 Jun 2026 01:11:03 GMT
ENV GRADLE_VERSION=8.14.5
# Tue, 30 Jun 2026 01:11:03 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Tue, 30 Jun 2026 01:11:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 30 Jun 2026 01:11:07 GMT
USER gradle
# Tue, 30 Jun 2026 01:11:09 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 30 Jun 2026 01:11:09 GMT
USER root
```

-	Layers:
	-	`sha256:cab5e0c171012774531d882f585d3be1eb8a97b88a5126afe48b35169caafc50`  
		Last Modified: Mon, 29 Jun 2026 06:11:46 GMT  
		Size: 45.1 MB (45078234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3383a7a24164308cd34dd0b3f319e45e2be49008abc404e48fcc73abdb8e02b0`  
		Last Modified: Tue, 30 Jun 2026 00:12:08 GMT  
		Size: 30.1 MB (30082685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d916e13ecd6f632d8b6e84239ec1235cb9716ee7006bd42bd33fc895891ed3d`  
		Last Modified: Tue, 30 Jun 2026 00:13:08 GMT  
		Size: 129.6 MB (129614219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14a8a1e985d064492815dc5170c5b2d0f6eeed2e94efad4f743315ea5c82bf3`  
		Last Modified: Tue, 30 Jun 2026 00:13:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34e324b1bc2384c5927c27b374dd786590c7afebd80edbeec8bc95c05ec5f52`  
		Last Modified: Tue, 30 Jun 2026 00:13:04 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b009a4bbc0b76a8b7761480ae3779fd2a4d919273f61bd2caef9bdbbf2c33607`  
		Last Modified: Tue, 30 Jun 2026 01:11:41 GMT  
		Size: 1.7 KB (1713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beed182ae28ac552047284d250282e8ec856a212dc1a14c7ababa2ced1badb2c`  
		Last Modified: Tue, 30 Jun 2026 01:11:43 GMT  
		Size: 39.2 MB (39191853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b183f7f181492e5259c1b100e11b3e135afe448b0097c47d7a28a8f01ed9089`  
		Last Modified: Tue, 30 Jun 2026 01:11:46 GMT  
		Size: 138.1 MB (138068535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b00d7d19a51f9fee78e753bbe114ecf47977626191dfe482ad7caab75862341`  
		Last Modified: Tue, 30 Jun 2026 01:11:41 GMT  
		Size: 35.0 KB (35009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:d2da34187222d7e577f94e3b626bb3afcbbdd456f62b219e79d80900f66a8a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5446137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:465cc53703affbf92d9e86d306ea3cbc6bd8144d9a7f9275de11fadc1684e731`

```dockerfile
```

-	Layers:
	-	`sha256:e2912bb6d1db0b2e4a8f2d0dd3f4127db09cb39bc72f39959b9de08f6a33061b`  
		Last Modified: Tue, 30 Jun 2026 01:11:42 GMT  
		Size: 5.4 MB (5421573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24509cc00efb7009bdd7674f6252b5857017f71bbeaec232b3bf8e5eba0d613f`  
		Last Modified: Tue, 30 Jun 2026 01:11:41 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk11-ubi` - linux; s390x

```console
$ docker pull gradle@sha256:337bd32ef349ebe829bd8c6b409e5ac70900b54bb8fa3f4a26fd67afd02ed8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.9 MB (367877373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e811893c39f838dd8aaca7842cd7b0c81a8aff7680c1a9056af0de9dce82fbcb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 29 Jun 2026 04:54:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 29 Jun 2026 04:54:01 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 29 Jun 2026 04:54:01 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 29 Jun 2026 04:54:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 29 Jun 2026 04:54:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 29 Jun 2026 04:54:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 29 Jun 2026 04:54:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:54:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:54:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 29 Jun 2026 04:54:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 29 Jun 2026 04:54:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 29 Jun 2026 04:54:01 GMT
ENV container oci
# Mon, 29 Jun 2026 04:54:02 GMT
COPY dir:bef74dcd4da475c586b5111f5945e8f6c9f80ccf9a44e3148ec57db13ecb6f76 in /      
# Mon, 29 Jun 2026 04:54:02 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 29 Jun 2026 04:54:02 GMT
CMD ["/bin/bash"]
# Mon, 29 Jun 2026 04:54:02 GMT
COPY dir:b86703d2983643457ac1d15b6653c2433af6c84ce9ec066326faf8d778c83033 in /usr/share/buildinfo/      
# Mon, 29 Jun 2026 04:54:02 GMT
COPY dir:b86703d2983643457ac1d15b6653c2433af6c84ce9ec066326faf8d778c83033 in /root/buildinfo/      
# Mon, 29 Jun 2026 04:54:02 GMT
LABEL "org.opencontainers.image.created"="2026-06-29T04:53:12Z" "org.opencontainers.image.revision"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "build-date"="2026-06-29T04:53:12Z" "architecture"="s390x" "vcs-ref"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "vcs-type"="git" "release"="1782708562"org.opencontainers.image.created=2026-06-29T04:53:12Z,org.opencontainers.image.revision=b0536a5d45ebd046bef183288a4f1cd5e6d68f66
# Tue, 30 Jun 2026 00:09:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Jun 2026 00:09:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:09:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 30 Jun 2026 00:09:34 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 30 Jun 2026 00:09:34 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 30 Jun 2026 00:09:41 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 30 Jun 2026 00:09:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 30 Jun 2026 00:09:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 30 Jun 2026 00:09:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 30 Jun 2026 00:09:42 GMT
CMD ["jshell"]
# Tue, 30 Jun 2026 01:09:55 GMT
CMD ["gradle"]
# Tue, 30 Jun 2026 01:09:55 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Jun 2026 01:09:55 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 30 Jun 2026 01:09:55 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 30 Jun 2026 01:09:55 GMT
WORKDIR /home/gradle
# Tue, 30 Jun 2026 01:09:59 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 30 Jun 2026 01:09:59 GMT
ENV GRADLE_VERSION=8.14.5
# Tue, 30 Jun 2026 01:09:59 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Tue, 30 Jun 2026 01:10:03 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 30 Jun 2026 01:10:03 GMT
USER gradle
# Tue, 30 Jun 2026 01:10:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 30 Jun 2026 01:10:04 GMT
USER root
```

-	Layers:
	-	`sha256:2b76546ac3454fac1865108cd9899827c06545a83bd476481d8bd3017de72774`  
		Last Modified: Mon, 29 Jun 2026 06:11:36 GMT  
		Size: 38.8 MB (38768635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47c019bbc5bf5fafae88fde703fb08f23e7357ff980fee2471235e2e7902fb1`  
		Last Modified: Tue, 30 Jun 2026 00:09:56 GMT  
		Size: 30.4 MB (30413888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a39c1c39137a249524a7008c6e5973b6fb0ac79a7819cd4b1cd589f0570000`  
		Last Modified: Tue, 30 Jun 2026 00:10:06 GMT  
		Size: 123.1 MB (123061371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce46e58a246c3a5d261e820a083fa79c04885ff83361e8e3bff934fb30d4b02`  
		Last Modified: Tue, 30 Jun 2026 00:10:04 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c276bf1d611d02f5ec3b30ac07d43e5355c8d3ff94ca724e3d413c3cade752`  
		Last Modified: Tue, 30 Jun 2026 00:10:04 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e979ddf0dad191fbbf6061ab2343eee7ee22249673bf3a1e1ebfb3fa8cf51b`  
		Last Modified: Tue, 30 Jun 2026 01:10:27 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08dd5a92bbe2188db406906d2cb13b958ac442dafd0a66f20471c060d86be2f9`  
		Last Modified: Tue, 30 Jun 2026 01:10:28 GMT  
		Size: 37.5 MB (37525733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd23584cf96e39fc21b54451d11bf713344508c54a7a63fea9c4659db29c6e0`  
		Last Modified: Tue, 30 Jun 2026 01:10:30 GMT  
		Size: 138.1 MB (138068577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299fbd5cba7dec4fd2ee51916b16072282db8580b7eec1eaa3dbb0442f6ea6e9`  
		Last Modified: Tue, 30 Jun 2026 01:10:27 GMT  
		Size: 35.0 KB (35011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:729d57b6728d798f5c9ffc632b010daaa2c70945279b73b62c694f8afc492081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5435914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72ea27222c9e8de364185b5d3e8aed48d1e1efa2ce5b6f600f5f52149458cdb9`

```dockerfile
```

-	Layers:
	-	`sha256:4c9a0ea148efcde56a1af7740a8df9d9761b6c32444df6d20828a88298aa8411`  
		Last Modified: Tue, 30 Jun 2026 01:10:27 GMT  
		Size: 5.4 MB (5411424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1af9784af37bd24ed0066b5b5181d1c4a95b6781e9d7e6a5b7b04c2a3e97ee9`  
		Last Modified: Tue, 30 Jun 2026 01:10:27 GMT  
		Size: 24.5 KB (24490 bytes)  
		MIME: application/vnd.in-toto+json
