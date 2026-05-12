## `gradle:jdk17-ubi9`

```console
$ docker pull gradle@sha256:59e269fce4af2206c24db65709ec8342d51f6752aa85c3456fb0c5247ebcb5fe
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

### `gradle:jdk17-ubi9` - linux; amd64

```console
$ docker pull gradle@sha256:2285bfb0bbce45fa3b8e559be95cdd7a0859fcd9a99cc17d677e385dc2189812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.2 MB (393239524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56fb2c14de1ece52a6fa6a9cc6c293683759798f3a3471e0db6272384465c9d5`
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
# Tue, 12 May 2026 00:03:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 00:03:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:03:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 00:03:44 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 00:03:44 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Tue, 12 May 2026 00:04:15 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 12 May 2026 00:04:16 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 00:04:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 00:04:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 00:04:16 GMT
CMD ["jshell"]
# Tue, 12 May 2026 20:48:39 GMT
CMD ["gradle"]
# Tue, 12 May 2026 20:48:39 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 May 2026 20:48:39 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 12 May 2026 20:48:39 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 May 2026 20:48:40 GMT
WORKDIR /home/gradle
# Tue, 12 May 2026 20:48:43 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 12 May 2026 20:48:43 GMT
ENV GRADLE_VERSION=9.5.1
# Tue, 12 May 2026 20:48:43 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Tue, 12 May 2026 20:48:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 12 May 2026 20:48:46 GMT
USER gradle
# Tue, 12 May 2026 20:48:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 12 May 2026 20:48:46 GMT
USER root
```

-	Layers:
	-	`sha256:34f4a557df8123a31168a9ed57304a4ee0a79b26712d1770dcf7c798372b100b`  
		Last Modified: Mon, 11 May 2026 02:10:30 GMT  
		Size: 40.0 MB (39994724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38de3c3bb095f10d951999805aae95621256a5093a2e831bab5cf51b603f636`  
		Last Modified: Tue, 12 May 2026 00:04:01 GMT  
		Size: 30.4 MB (30369082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b86bd6f42cf14c928806cd7e8f9f344fffec14dac0d0282d916da5a71c91415`  
		Last Modified: Tue, 12 May 2026 00:04:36 GMT  
		Size: 145.9 MB (145915422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f667e623f2ea931eaa5c1ff8bb73b442fccbacb746401261a83a2c97656c75e4`  
		Last Modified: Tue, 12 May 2026 00:04:32 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88603fea4396eb95833ab2643765f949dff7f97771332ac035e6f1f8311e5ec2`  
		Last Modified: Tue, 12 May 2026 00:04:28 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf131a99357d9b24b9a505f92de36f01175d50f1bcb1f7e731288db98f0de5ee`  
		Last Modified: Tue, 12 May 2026 20:49:03 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993a077c42f3e4135a38e2f5368f12161675657bf2690247b0e3bc7fced7ce52`  
		Last Modified: Tue, 12 May 2026 20:49:05 GMT  
		Size: 36.7 MB (36693545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc6f0bbff723dddb80285d50c84da5c8ccc107b883df70e4ad77ea460cd0754`  
		Last Modified: Tue, 12 May 2026 20:49:08 GMT  
		Size: 140.2 MB (140236986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7221c9263972cee684fa76a64a32063e354ea6f82f795c921f7fc9a1c22ac184`  
		Last Modified: Tue, 12 May 2026 20:49:04 GMT  
		Size: 25.6 KB (25607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:a6dd10e9cd5929360b6be868f7aaa3f869dbfaf2424e42755fc89b509d08663d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5441808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd1294dfbd20eef1982331b3293421ff28b0afb5fe80c3a4faff7b8284849fa`

```dockerfile
```

-	Layers:
	-	`sha256:7ade1bade62a15aa97667b8ae7b4ed14e36daf62022bc3715b27d89683afe39f`  
		Last Modified: Tue, 12 May 2026 20:49:04 GMT  
		Size: 5.4 MB (5418608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dc4e9972741673c1c5394aab3c9908658127ca3c55335a5614c806b0075950f`  
		Last Modified: Tue, 12 May 2026 20:49:04 GMT  
		Size: 23.2 KB (23200 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk17-ubi9` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:9f290df45bc90fbea93681f42d353c3db52b3b601e13bef1f47585adf366a7eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.0 MB (390026411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15347c15372e2a3fe3f1dbcf2c7ac962c9f315e54df0433b6ef8f32fb5e0a7c0`
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
ENV JAVA_VERSION=jdk-17.0.19+10
# Tue, 12 May 2026 00:02:19 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 12 May 2026 00:02:20 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 00:02:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 00:02:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 00:02:20 GMT
CMD ["jshell"]
# Tue, 12 May 2026 20:48:50 GMT
CMD ["gradle"]
# Tue, 12 May 2026 20:48:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 May 2026 20:48:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 12 May 2026 20:48:50 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 May 2026 20:48:50 GMT
WORKDIR /home/gradle
# Tue, 12 May 2026 20:48:54 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 12 May 2026 20:48:54 GMT
ENV GRADLE_VERSION=9.5.1
# Tue, 12 May 2026 20:48:54 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Tue, 12 May 2026 20:48:57 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 12 May 2026 20:48:57 GMT
USER gradle
# Tue, 12 May 2026 20:48:57 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 12 May 2026 20:48:57 GMT
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
	-	`sha256:fce3d89bb3e053337a8d27c538a91703d36ff7eb5d4fe4386d4337b30060120b`  
		Last Modified: Tue, 12 May 2026 00:02:40 GMT  
		Size: 144.7 MB (144734847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8d79a31581103699e8231a9d6742b877a8e18eff34bfb03d63f3ede6d6f64a`  
		Last Modified: Tue, 12 May 2026 00:02:36 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8137005b72e476419d64e1aa73ab87e6702b31836bbc8c9ffa452fe14ccec1f6`  
		Last Modified: Tue, 12 May 2026 00:02:36 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c9a1fe9b6927905f5b65157f7139d5e7ac47c5322f997b26e8c98b035314e5`  
		Last Modified: Tue, 12 May 2026 20:49:14 GMT  
		Size: 1.7 KB (1713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd40cb073d32794e8c5e4f63d4a19c24b611db098104a06590dec1147231a32`  
		Last Modified: Tue, 12 May 2026 20:49:15 GMT  
		Size: 36.0 MB (36026069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34cf5eb943f65095f9e9fe374d154aa3088eadc61f8ef018f94db6f6b81801e2`  
		Last Modified: Tue, 12 May 2026 20:49:17 GMT  
		Size: 140.2 MB (140236988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1710dbad5623de41914c23352255d415e56390b4aaa09c6f0a14a00324fa1f0b`  
		Last Modified: Tue, 12 May 2026 20:49:14 GMT  
		Size: 29.3 KB (29334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:02d4e143437eff10cdbb36f1a67c52fad085c3f500447ccc0abc818ff74badb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5441339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1da2e267381820594e24bbcac05d75c3c80bb7ed4fa479a26469cddc1247d5b`

```dockerfile
```

-	Layers:
	-	`sha256:ea4f57d0dcdb76544cdf907ca2eb9467190ff098481ea95521e1a91f7ef7d095`  
		Last Modified: Tue, 12 May 2026 20:49:14 GMT  
		Size: 5.4 MB (5417990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1b19aac1dc1ee4532264fb579e1cd17f236b7ba8b010411cb8eee4fb1d71ad1`  
		Last Modified: Tue, 12 May 2026 20:49:14 GMT  
		Size: 23.3 KB (23349 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk17-ubi9` - linux; ppc64le

```console
$ docker pull gradle@sha256:f68fd9b94c88c3ab76160a5ec2fd29a0386b54f870443f867b5ba3a5ce7a85ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.3 MB (401254222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdaaee98e6da5125948b1d749f44cd47e5724a27a740271e2dfb24f7de5782c6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 11 May 2026 01:08:39 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 11 May 2026 01:08:39 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 11 May 2026 01:08:39 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 11 May 2026 01:08:39 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 11 May 2026 01:08:39 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 11 May 2026 01:08:39 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 11 May 2026 01:08:39 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:08:39 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:08:39 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 11 May 2026 01:08:39 GMT
LABEL io.openshift.expose-services=""
# Mon, 11 May 2026 01:08:39 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 11 May 2026 01:08:39 GMT
ENV container oci
# Mon, 11 May 2026 01:08:40 GMT
COPY dir:965cbe659c4ef641a7d8453ee3646d27f67083aabd851e0d0e8ae579e1a5219a in /      
# Mon, 11 May 2026 01:08:40 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 11 May 2026 01:08:40 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 01:08:40 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 11 May 2026 01:08:40 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 11 May 2026 01:08:40 GMT
COPY file:5ab8055b01479fa72fe220e6096452a3966616329925346e0d128323be1372ea in /usr/share/buildinfo/labels.json      
# Mon, 11 May 2026 01:08:40 GMT
COPY file:5ab8055b01479fa72fe220e6096452a3966616329925346e0d128323be1372ea in /root/buildinfo/labels.json      
# Mon, 11 May 2026 01:08:41 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1" "org.opencontainers.image.revision"="15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1" "build-date"="2026-05-11T01:08:29Z" "org.opencontainers.image.created"="2026-05-11T01:08:29Z" "release"="1778461551"org.opencontainers.image.revision=15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1,org.opencontainers.image.created=2026-05-11T01:08:29Z
# Tue, 12 May 2026 00:29:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 00:29:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:29:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 00:29:05 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 00:29:05 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Tue, 12 May 2026 00:32:33 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 12 May 2026 00:32:36 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 00:32:37 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 00:32:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 00:32:37 GMT
CMD ["jshell"]
# Tue, 12 May 2026 01:14:04 GMT
CMD ["gradle"]
# Tue, 12 May 2026 01:14:04 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 May 2026 01:14:04 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 12 May 2026 01:14:04 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 May 2026 01:14:05 GMT
WORKDIR /home/gradle
# Tue, 12 May 2026 01:14:17 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 12 May 2026 01:14:17 GMT
ENV GRADLE_VERSION=9.5.1
# Tue, 12 May 2026 01:14:17 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Tue, 12 May 2026 20:52:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 12 May 2026 20:52:25 GMT
USER gradle
# Tue, 12 May 2026 20:52:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 12 May 2026 20:52:27 GMT
USER root
```

-	Layers:
	-	`sha256:63f20427e281fbcfcf4050232e679771a690d7b2cb4885d2fa139012ed9194ac`  
		Last Modified: Mon, 11 May 2026 06:12:17 GMT  
		Size: 44.5 MB (44457236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794d7e1260962e3beb07f3313ca46feec37bccd1dcc87637de2655c117ec19a4`  
		Last Modified: Tue, 12 May 2026 00:29:41 GMT  
		Size: 32.8 MB (32844103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e748976b5ec9d9861c5bc723954d5012c1d896c992ea9973a512b0114ba8563a`  
		Last Modified: Tue, 12 May 2026 00:33:15 GMT  
		Size: 145.8 MB (145788755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6067cd13d4842061a802ba8335168f812915ea4273815821d9834271f485818e`  
		Last Modified: Tue, 12 May 2026 00:33:11 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2d2ee3d0aa76333f18f01b064c0ed8506858818c1f10cec9001929fead046e`  
		Last Modified: Tue, 12 May 2026 00:33:11 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5f9a424618dc79a9d5a2ba673f6fd64b5f9bc40d020e84c3a422a7e22ec859`  
		Last Modified: Tue, 12 May 2026 01:14:56 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564ffc7bb79d109df1d7ce4f6032f242901de841cc5bec78c6522bdcacf413ab`  
		Last Modified: Tue, 12 May 2026 01:14:58 GMT  
		Size: 37.9 MB (37922593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae10cad62dae0b36c922519af5c20ecd3623279b137b9697a6fff127eb70c31`  
		Last Modified: Tue, 12 May 2026 20:53:10 GMT  
		Size: 140.2 MB (140236993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559a0ea6ff2f55c8c39df0c9492db5b4daa2e6b62e2082bb81f05c06c14939c6`  
		Last Modified: Tue, 12 May 2026 20:53:06 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:9ad032e8cfd9e1c5aec61a4006cb6862ba3a30b2b270b07d23e98a3688a17d66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5439201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f60b72e631689c95e853382bf0c8233747cbc48e8b314627879b0fad4224a1d`

```dockerfile
```

-	Layers:
	-	`sha256:2d80500fa277e0c6e85531c0e78c6132b1f91fb6d14563b9f84be9e7e90a9c68`  
		Last Modified: Tue, 12 May 2026 20:53:06 GMT  
		Size: 5.4 MB (5415919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5ca9d6fa710b28e704454185ff9ffd56e6ebddc5f6a61a2a8b9e41f3d150585`  
		Last Modified: Tue, 12 May 2026 20:53:06 GMT  
		Size: 23.3 KB (23282 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk17-ubi9` - linux; s390x

```console
$ docker pull gradle@sha256:61fce1a51f14d39995196535f2310be745aa39764c082e5f4e57370a4b467f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.0 MB (380998445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84e57398ea6ee7ce0a3ff35d810bcabe24fcde8c6e504c3c7f6e2e25fd122bb`
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
ENV JAVA_VERSION=jdk-17.0.19+10
# Tue, 12 May 2026 00:01:38 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 12 May 2026 00:01:39 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 00:01:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 00:01:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 00:01:39 GMT
CMD ["jshell"]
# Tue, 12 May 2026 00:13:45 GMT
CMD ["gradle"]
# Tue, 12 May 2026 00:13:45 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 May 2026 00:13:45 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 12 May 2026 00:13:45 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 May 2026 00:13:45 GMT
WORKDIR /home/gradle
# Tue, 12 May 2026 00:13:49 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 12 May 2026 00:13:49 GMT
ENV GRADLE_VERSION=9.5.1
# Tue, 12 May 2026 00:13:49 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Tue, 12 May 2026 20:48:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 12 May 2026 20:48:14 GMT
USER gradle
# Tue, 12 May 2026 20:48:15 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 12 May 2026 20:48:15 GMT
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
	-	`sha256:534e2781af71b7e89eb71926bd97421e3e621532a58285b07f21b6ac9337a17c`  
		Last Modified: Tue, 12 May 2026 00:02:03 GMT  
		Size: 135.9 MB (135912312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b13e6cae583983971e9bc650c988aa2ee623206888450b91a20203d2aaf74fa`  
		Last Modified: Tue, 12 May 2026 00:02:00 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba09dafbe83c07c0d1235a24b19c6f2151d3f4f7596e1af6d788bbb3c60c91c`  
		Last Modified: Tue, 12 May 2026 00:02:00 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d17ba6a3b075dbb598f774d051ca8cdaa67177905049bc9172681edc4acb34`  
		Last Modified: Tue, 12 May 2026 00:14:18 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e582ce0d0588ceb609b9ce2d12ebef9d374afb25fee10dd442bbb81ff38c03d`  
		Last Modified: Tue, 12 May 2026 00:14:19 GMT  
		Size: 36.3 MB (36333735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ef8459b4d0f2537708c965c0833379c2b3bc44acac617ac7596fc5f1d41bac`  
		Last Modified: Tue, 12 May 2026 20:48:44 GMT  
		Size: 140.2 MB (140236992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d7fc50483348abb544701494fe4516c1bc839ed015a4fb2c70341d86184d12`  
		Last Modified: Tue, 12 May 2026 20:48:40 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:b74788bff1649c78ffb9bb51991a2333b6666f8eed0d51aef63e5d5c0df68e54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5428447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a0dd400aaeedb014d0cbc231b150d084505913fcad75a71dcff74847bf9663`

```dockerfile
```

-	Layers:
	-	`sha256:f2ef0957911e5829bcac8b6b8406c4b41287b0977ca2d92ca8bf415e825e8b89`  
		Last Modified: Tue, 12 May 2026 20:48:40 GMT  
		Size: 5.4 MB (5405213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30785575085b439214d99e6763ec83c1f52fdee04503a8d56f39c33fe32b6730`  
		Last Modified: Tue, 12 May 2026 20:48:40 GMT  
		Size: 23.2 KB (23234 bytes)  
		MIME: application/vnd.in-toto+json
