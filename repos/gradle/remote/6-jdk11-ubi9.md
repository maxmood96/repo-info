## `gradle:6-jdk11-ubi9`

```console
$ docker pull gradle@sha256:51fbac68a638f5431a99e3c2a9af65b32b2e155d28bd74664091d2c5b54a5e0c
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

### `gradle:6-jdk11-ubi9` - linux; amd64

```console
$ docker pull gradle@sha256:98bce63ebd6b75fbd72a22830f6b79b4c89d6889810915c7ffdb5f74122a0bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.5 MB (357538048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f00551baba4879a18f226ee546e1cdd17aad7895736e2ba5a624f3b21740fa`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 11 May 2026 01:07:55 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 11 May 2026 01:07:55 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 11 May 2026 01:07:55 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 11 May 2026 01:07:55 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 11 May 2026 01:07:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 11 May 2026 01:07:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 11 May 2026 01:07:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:07:55 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:07:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 11 May 2026 01:07:55 GMT
LABEL io.openshift.expose-services=""
# Mon, 11 May 2026 01:07:55 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 11 May 2026 01:07:55 GMT
ENV container oci
# Mon, 11 May 2026 01:07:56 GMT
COPY dir:d396e6c334ec17a1ba4a03f21481f526666f77d114978313ef1df55edd8e1412 in /      
# Mon, 11 May 2026 01:07:56 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 11 May 2026 01:07:56 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 01:07:56 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 11 May 2026 01:07:56 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 11 May 2026 01:07:56 GMT
COPY file:1b5a90f3ed08efd6f44de46e666565e2a9b8e1a168d7a249c016b23dc19bcaac in /usr/share/buildinfo/labels.json      
# Mon, 11 May 2026 01:07:56 GMT
COPY file:1b5a90f3ed08efd6f44de46e666565e2a9b8e1a168d7a249c016b23dc19bcaac in /root/buildinfo/labels.json      
# Mon, 11 May 2026 01:07:57 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1" "org.opencontainers.image.revision"="15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1" "build-date"="2026-05-11T01:07:39Z" "org.opencontainers.image.created"="2026-05-11T01:07:39Z" "release"="1778461551"org.opencontainers.image.revision=15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1,org.opencontainers.image.created=2026-05-11T01:07:39Z
# Tue, 12 May 2026 00:02:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 00:02:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:02:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 00:02:17 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 00:02:17 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 12 May 2026 00:03:10 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 12 May 2026 00:03:11 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 00:03:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 00:03:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 00:03:11 GMT
CMD ["jshell"]
# Tue, 12 May 2026 00:18:38 GMT
CMD ["gradle"]
# Tue, 12 May 2026 00:18:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 May 2026 00:18:38 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 12 May 2026 00:18:38 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 May 2026 00:18:38 GMT
WORKDIR /home/gradle
# Tue, 12 May 2026 00:19:16 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 12 May 2026 00:19:16 GMT
ENV GRADLE_VERSION=6.9.4
# Tue, 12 May 2026 00:19:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Tue, 12 May 2026 00:19:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 12 May 2026 00:19:18 GMT
USER gradle
# Tue, 12 May 2026 00:19:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 12 May 2026 00:19:19 GMT
USER root
```

-	Layers:
	-	`sha256:34f4a557df8123a31168a9ed57304a4ee0a79b26712d1770dcf7c798372b100b`  
		Last Modified: Mon, 11 May 2026 02:10:30 GMT  
		Size: 40.0 MB (39994724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02988dece23c62f932df389247c4a7dbb5bd30626affa1e0e05af09e0aaa800a`  
		Last Modified: Tue, 12 May 2026 00:02:36 GMT  
		Size: 30.4 MB (30368917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:448270b28357eb70a6b3ea11df1fbf593c37a1f3a9d926d0a1df3506402001c4`  
		Last Modified: Tue, 12 May 2026 00:03:29 GMT  
		Size: 142.3 MB (142348805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb0369f003cae910c3757e895b0dc64ff3bbf8e13f3337d49b5e8ce67657be3`  
		Last Modified: Tue, 12 May 2026 00:03:26 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2989132f24daf049696525e32e8a4e0e625aac81cae1ddabc35fd411e825481`  
		Last Modified: Tue, 12 May 2026 00:03:26 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3341eecb38c54ac1679b82e308995d013a9e409fcddc1924d7da8b29b26cae`  
		Last Modified: Tue, 12 May 2026 00:18:58 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00470dd242802f54c1597e01831f68d193f7349897a4e4a20fb3bf861534bd10`  
		Last Modified: Tue, 12 May 2026 00:19:34 GMT  
		Size: 36.7 MB (36693532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ed0d2070adc886c819c8c8e6c25b31441c56852e97fe86cff4dabd3024e882`  
		Last Modified: Tue, 12 May 2026 00:19:36 GMT  
		Size: 107.7 MB (107696639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d710a3212657111bd97ab5a0b8fb873816576aa32a9f0a00bd7e0cb2cf5ec9f3`  
		Last Modified: Tue, 12 May 2026 00:19:33 GMT  
		Size: 431.3 KB (431274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:dd71f603fd3b51b53e6581c9a981e97088fe15afca9700fee0ca23a9f5db94bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5339782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ed2841a0619efabfe6aae57cce6973b7dce9b065869e98084f251ae1466cd4b`

```dockerfile
```

-	Layers:
	-	`sha256:d432cccc868c67fce82c6fee72115de1f22c01ff50fa1b5c1b349a806c22111e`  
		Last Modified: Tue, 12 May 2026 00:19:33 GMT  
		Size: 5.3 MB (5316198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48531bb683ff3bd8d95f1956dcc3c35acc319c318bdf642c3a7f4f67368ca104`  
		Last Modified: Tue, 12 May 2026 00:19:33 GMT  
		Size: 23.6 KB (23584 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk11-ubi9` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:aeb78714688f5ce8ecd4e0de9f4dc0df1c379c7d24207fee0cb063a001f55a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.2 MB (352187601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512b5811a2ebaf1c3777579fc3fd10147bae0f9b6b26964e4857548ffdf7d839`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 11 May 2026 01:10:03 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 11 May 2026 01:10:03 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 11 May 2026 01:10:03 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 11 May 2026 01:10:03 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 11 May 2026 01:10:03 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 11 May 2026 01:10:03 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 11 May 2026 01:10:03 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:10:04 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:10:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 11 May 2026 01:10:04 GMT
LABEL io.openshift.expose-services=""
# Mon, 11 May 2026 01:10:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 11 May 2026 01:10:04 GMT
ENV container oci
# Mon, 11 May 2026 01:10:05 GMT
COPY dir:f96b78a7f24437106ae6a323adf2c06c98f78157637998e58adf24d336fc59f9 in /      
# Mon, 11 May 2026 01:10:05 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 11 May 2026 01:10:05 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 01:10:05 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 11 May 2026 01:10:05 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 11 May 2026 01:10:05 GMT
COPY file:4815587a81c6816403ce960a517de92d74cd550eeda95c6164f5b3614ab4c3fe in /usr/share/buildinfo/labels.json      
# Mon, 11 May 2026 01:10:05 GMT
COPY file:4815587a81c6816403ce960a517de92d74cd550eeda95c6164f5b3614ab4c3fe in /root/buildinfo/labels.json      
# Mon, 11 May 2026 01:10:05 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1" "org.opencontainers.image.revision"="15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1" "build-date"="2026-05-11T01:09:50Z" "org.opencontainers.image.created"="2026-05-11T01:09:50Z" "release"="1778461551"org.opencontainers.image.revision=15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1,org.opencontainers.image.created=2026-05-11T01:09:50Z
# Mon, 11 May 2026 23:59:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 11 May 2026 23:59:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:59:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 11 May 2026 23:59:46 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 11 May 2026 23:59:46 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 12 May 2026 00:01:23 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 12 May 2026 00:01:25 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 00:01:25 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 00:01:25 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 00:01:25 GMT
CMD ["jshell"]
# Tue, 12 May 2026 00:18:01 GMT
CMD ["gradle"]
# Tue, 12 May 2026 00:18:01 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 May 2026 00:18:01 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 12 May 2026 00:18:01 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 May 2026 00:18:01 GMT
WORKDIR /home/gradle
# Tue, 12 May 2026 00:18:05 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 12 May 2026 00:18:05 GMT
ENV GRADLE_VERSION=6.9.4
# Tue, 12 May 2026 00:18:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Tue, 12 May 2026 00:18:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 12 May 2026 00:18:08 GMT
USER gradle
# Tue, 12 May 2026 00:18:09 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 12 May 2026 00:18:09 GMT
USER root
```

-	Layers:
	-	`sha256:07b48350f3398d184075c56877eb97837294903946c9a6c10031807b6c4f549d`  
		Last Modified: Mon, 11 May 2026 02:11:01 GMT  
		Size: 38.2 MB (38205518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd6ab7ec1d6210314e91ddca10dab2e77942a0ef57b3d2cad8094a806f34c10`  
		Last Modified: Tue, 12 May 2026 00:00:08 GMT  
		Size: 30.8 MB (30789492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb49ba83c179e0929abb11e0c17dc2d6e31ab57ae858a0130935ef332153a16e`  
		Last Modified: Tue, 12 May 2026 00:01:44 GMT  
		Size: 139.0 MB (139040657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0135c3623a9391ec4fa8360ef845432a1a444df04cdb3a28ebffb55c25483735`  
		Last Modified: Tue, 12 May 2026 00:01:40 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4baa52ae09ca9dae9c841492bdea16e8327353b95eb219f4fa16af7759db7420`  
		Last Modified: Tue, 12 May 2026 00:01:40 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d89025abb8ec559e1f06c76fd2e4a41d8117a086df285b21e87e01f99429121`  
		Last Modified: Tue, 12 May 2026 00:18:24 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b542be7a0a5f157d749cccc638004bf44619e550a3d5fabaabfb6c45e448d0`  
		Last Modified: Tue, 12 May 2026 00:18:25 GMT  
		Size: 36.0 MB (36026100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12bf5538ba3187298c9c5c66181692b324f9c6c70bade287cf65b1273985bc5`  
		Last Modified: Tue, 12 May 2026 00:18:27 GMT  
		Size: 107.7 MB (107696637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c82c85dd0e038594e373afdb9defd5925e8f7f2b35028dcc8d26a4dfd272435`  
		Last Modified: Tue, 12 May 2026 00:18:24 GMT  
		Size: 425.0 KB (425033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:089601f5d69acc56d1b23a5387ad5876c03e604612ff47bd9e56644852dcecbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5339979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8dcb6d7d3a7cbf2e37b971e0643f645358636f560ebf028f3281157e720908f`

```dockerfile
```

-	Layers:
	-	`sha256:52689ed27feb825556a0afea13ae790cc8b87c355e5f726963e1ff275b14a2d8`  
		Last Modified: Tue, 12 May 2026 00:18:24 GMT  
		Size: 5.3 MB (5316222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54f44bd8ffdd411b1bbf37ccaeec5367095af7662567077e3584fbef06010911`  
		Last Modified: Tue, 12 May 2026 00:18:24 GMT  
		Size: 23.8 KB (23757 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk11-ubi9` - linux; ppc64le

```console
$ docker pull gradle@sha256:7c2df9de643e709f569b3b66fce09e5d45fe25e51c430c701a51b264f5b6aa5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.6 MB (352573022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e074f465c43e062e5737d8c2fc5e8afc1900ca96eda89069d973ed4f46786db`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 06 May 2026 12:56:35 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 06 May 2026 12:56:35 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 06 May 2026 12:56:35 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 06 May 2026 12:56:35 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 06 May 2026 12:56:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 06 May 2026 12:56:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 06 May 2026 12:56:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 12:56:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 12:56:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 06 May 2026 12:56:35 GMT
LABEL io.openshift.expose-services=""
# Wed, 06 May 2026 12:56:35 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 06 May 2026 12:56:35 GMT
ENV container oci
# Wed, 06 May 2026 12:56:36 GMT
COPY dir:80e7e7cac97ce232e3c4b678751f9a2b11cc4a26beaae93a957f83f1fc548f95 in /      
# Wed, 06 May 2026 12:56:36 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 06 May 2026 12:56:36 GMT
CMD ["/bin/bash"]
# Wed, 06 May 2026 12:56:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 06 May 2026 12:56:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 06 May 2026 12:56:36 GMT
COPY file:bffe3875426b01ab6d752ed5055c4e2d920bf40e31b44b873a80786da1d0750b in /usr/share/buildinfo/labels.json      
# Wed, 06 May 2026 12:56:36 GMT
COPY file:bffe3875426b01ab6d752ed5055c4e2d920bf40e31b44b873a80786da1d0750b in /root/buildinfo/labels.json      
# Wed, 06 May 2026 12:56:37 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c" "org.opencontainers.image.revision"="8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c" "build-date"="2026-05-06T12:56:25Z" "org.opencontainers.image.created"="2026-05-06T12:56:25Z" "release"="1778072020"org.opencontainers.image.revision=8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c,org.opencontainers.image.created=2026-05-06T12:56:25Z
# Fri, 08 May 2026 16:18:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 16:18:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 16:18:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 May 2026 16:18:41 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Fri, 08 May 2026 16:18:41 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Fri, 08 May 2026 16:20:40 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 08 May 2026 16:20:43 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 16:20:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 16:20:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 16:20:43 GMT
CMD ["jshell"]
# Fri, 08 May 2026 16:46:19 GMT
CMD ["gradle"]
# Fri, 08 May 2026 16:46:19 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 May 2026 16:46:19 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 08 May 2026 16:46:19 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 May 2026 16:46:19 GMT
WORKDIR /home/gradle
# Fri, 08 May 2026 16:46:28 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 08 May 2026 16:46:28 GMT
ENV GRADLE_VERSION=6.9.4
# Fri, 08 May 2026 16:46:28 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Fri, 08 May 2026 16:51:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 08 May 2026 16:51:13 GMT
USER gradle
# Fri, 08 May 2026 16:51:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 08 May 2026 16:51:14 GMT
USER root
```

-	Layers:
	-	`sha256:e3c3e69dacc2a761a2218333f5a3c6de6e1ae1b3afa56e02bcb3f2e70f91db2c`  
		Last Modified: Wed, 06 May 2026 18:13:19 GMT  
		Size: 44.5 MB (44456866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30e4b2f46114bf6e128a1cbe09e30dd7493dd7f6692477ad27cf63291c7e84f`  
		Last Modified: Fri, 08 May 2026 16:19:19 GMT  
		Size: 32.8 MB (32843917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e9475f98d3e3a0589b1f692f8704ca21321d574cee263d6e3dad76d8d2be1a`  
		Last Modified: Fri, 08 May 2026 16:21:18 GMT  
		Size: 129.6 MB (129614170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141a4747ae4ddf0ac3e44ff352c87c40e83a17ec2057b10a63297c3d9583700b`  
		Last Modified: Fri, 08 May 2026 16:21:14 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7fd931c1ddc1e980d9d7570558a50df519a9b3b27c8969b0f371ec19da3f1b1`  
		Last Modified: Fri, 08 May 2026 16:21:14 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896fb134bcb3bbdfbb888ead553d25ca62e6419c7b592d8bd3f6509db00c782d`  
		Last Modified: Fri, 08 May 2026 16:47:05 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fbbef53a598f0671df6b5e3ea2725536fa3426100f5eff1db548a702e5292b`  
		Last Modified: Fri, 08 May 2026 16:47:07 GMT  
		Size: 37.9 MB (37922330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735f08ad36d06d3d76870e66a3b3612d4f50aaef477c9c61d571247aae4ee7a4`  
		Last Modified: Fri, 08 May 2026 16:51:42 GMT  
		Size: 107.7 MB (107696594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c499ba4747cdedaa99b417a52296fc6566f103dee3da9064f845e7e68987b37c`  
		Last Modified: Fri, 08 May 2026 16:51:39 GMT  
		Size: 35.0 KB (34983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:abbc514a8dd4956a067e065dae4dfe3b6528d12010d52a0abb85766cb6d2f9f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5336549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:998ad836b021ec5c2b9e19a19afbcfc10d37f9ee5c1c934686c7ce41ac30a20c`

```dockerfile
```

-	Layers:
	-	`sha256:cdf2b680997661917aef66f2b266c78ba2e4ca6196c3095a65eba5a338d98e03`  
		Last Modified: Fri, 08 May 2026 16:51:40 GMT  
		Size: 5.3 MB (5312904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:184063d1943040efe6ab82fe5447062464c496c44f24b05fadd4ba5aac63ccbd`  
		Last Modified: Fri, 08 May 2026 16:51:39 GMT  
		Size: 23.6 KB (23645 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk11-ubi9` - linux; s390x

```console
$ docker pull gradle@sha256:329718f17af0034cb7d6c565fa5773f1155058c32c6818ecd77ceb8c218e6b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.6 MB (335641708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdf3cbf85829dd1e0d76e93d4ed987cebb2a55213103a48c575716f1777470db`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 11 May 2026 01:10:09 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 11 May 2026 01:10:09 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 11 May 2026 01:10:09 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 11 May 2026 01:10:09 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 11 May 2026 01:10:09 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 11 May 2026 01:10:09 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 11 May 2026 01:10:09 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:10:09 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:10:09 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 11 May 2026 01:10:09 GMT
LABEL io.openshift.expose-services=""
# Mon, 11 May 2026 01:10:09 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 11 May 2026 01:10:09 GMT
ENV container oci
# Mon, 11 May 2026 01:10:10 GMT
COPY dir:2a2bb91993c7787b85a3cdef17fac2d4a451771711ace3d2f7d4a57df4fd720e in /      
# Mon, 11 May 2026 01:10:10 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 11 May 2026 01:10:10 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 01:10:10 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 11 May 2026 01:10:10 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 11 May 2026 01:10:10 GMT
COPY file:6e6aef2633a1aeb29df36766e5920d63b41f2443841821a183adbf53bfc02d4f in /usr/share/buildinfo/labels.json      
# Mon, 11 May 2026 01:10:10 GMT
COPY file:6e6aef2633a1aeb29df36766e5920d63b41f2443841821a183adbf53bfc02d4f in /root/buildinfo/labels.json      
# Mon, 11 May 2026 01:10:10 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1" "org.opencontainers.image.revision"="15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1" "build-date"="2026-05-11T01:09:59Z" "org.opencontainers.image.created"="2026-05-11T01:09:59Z" "release"="1778461551"org.opencontainers.image.revision=15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1,org.opencontainers.image.created=2026-05-11T01:09:59Z
# Tue, 12 May 2026 00:00:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 00:00:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:00:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 00:00:27 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 00:00:27 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 12 May 2026 00:00:33 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 12 May 2026 00:00:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 00:00:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 00:00:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 00:00:34 GMT
CMD ["jshell"]
# Tue, 12 May 2026 00:14:46 GMT
CMD ["gradle"]
# Tue, 12 May 2026 00:14:46 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 May 2026 00:14:46 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 12 May 2026 00:14:46 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 May 2026 00:14:46 GMT
WORKDIR /home/gradle
# Tue, 12 May 2026 00:14:52 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 12 May 2026 00:14:52 GMT
ENV GRADLE_VERSION=6.9.4
# Tue, 12 May 2026 00:14:52 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Tue, 12 May 2026 00:14:55 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 12 May 2026 00:14:55 GMT
USER gradle
# Tue, 12 May 2026 00:14:55 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 12 May 2026 00:14:55 GMT
USER root
```

-	Layers:
	-	`sha256:9e318380099430c4b5b0b9ce404e5438a459390bacd9fa537031869a73d98e4b`  
		Last Modified: Mon, 11 May 2026 06:12:10 GMT  
		Size: 38.1 MB (38128501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e91c90ce3db8a8b54c33928da91ec2124d42bb6f3f4ce2819ab15e28876fab`  
		Last Modified: Tue, 12 May 2026 00:00:56 GMT  
		Size: 30.4 MB (30382364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fdd346fe27429c1fb96d9dadbbc45919f1c48f833191ff8d1d6250dcccf4e12`  
		Last Modified: Tue, 12 May 2026 00:00:58 GMT  
		Size: 123.1 MB (123061391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0915cbbe3bea543da6754381f5b7df0fb2d759ded18f48e0e85fc490f4530da9`  
		Last Modified: Tue, 12 May 2026 00:00:48 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b475644fe269a833e0f519b3267586f9a84f35558eb35f907c6d864fe9b645c`  
		Last Modified: Tue, 12 May 2026 00:00:56 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c5f6a5e27ffec7f295813e1bf734e54757ce4e1936bac44bf279e72ce30b13`  
		Last Modified: Tue, 12 May 2026 00:15:19 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b655385ae2dc3fa44b92362750df77c1436f3f83e37c796634476078b2b69fbd`  
		Last Modified: Tue, 12 May 2026 00:15:20 GMT  
		Size: 36.3 MB (36333676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0004e22c4b38ce8e7fb93aef0fa56fcde0cf5341457ae4e7ca9bee179df363ad`  
		Last Modified: Tue, 12 May 2026 00:15:21 GMT  
		Size: 107.7 MB (107696636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79a4cb3df45e96200c6e91288f305634f40ed32d4890e92b7c948f69c4b2a4f`  
		Last Modified: Tue, 12 May 2026 00:15:19 GMT  
		Size: 35.0 KB (34977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:618d77d9cf2d64ee468b4f3575333cad5c39a96132ea5825d09e689a9727e89c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5326389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b5532db3b9d61d78e9ac5a32128801006146ecb4be33ecaf94da1caadbba914`

```dockerfile
```

-	Layers:
	-	`sha256:b9bf2d87705019e1ae338444bf013a08c696d6d4e3b21c7ac22b21af78659b92`  
		Last Modified: Tue, 12 May 2026 00:15:19 GMT  
		Size: 5.3 MB (5302807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:626f45cefded42e4925daf20bf7e61fd92238a041ce63d8300634122ab87e723`  
		Last Modified: Tue, 12 May 2026 00:15:19 GMT  
		Size: 23.6 KB (23582 bytes)  
		MIME: application/vnd.in-toto+json
