## `gradle:9-jdk21-ubi`

```console
$ docker pull gradle@sha256:2a6c819bc7d386a61be9ecf3d6a8bfe06ed2cdfdf46b42c025c0900f9d72072a
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

### `gradle:9-jdk21-ubi` - linux; amd64

```console
$ docker pull gradle@sha256:9db11e58221314a1d708d40a9f03119819fe0333ee62a30b3c1b70014dfe9d4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.1 MB (401129241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9124740849baff8d7bbbdbab349e90912a8a659160229779495cc5b5a66e06c7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 12 Nov 2025 14:07:22 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 12 Nov 2025 14:07:22 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 12 Nov 2025 14:07:22 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 12 Nov 2025 14:07:22 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 12 Nov 2025 14:07:22 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 12 Nov 2025 14:07:23 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 12 Nov 2025 14:07:23 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 14:07:23 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 14:07:23 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 12 Nov 2025 14:07:23 GMT
LABEL io.openshift.expose-services=""
# Wed, 12 Nov 2025 14:07:23 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 12 Nov 2025 14:07:23 GMT
ENV container oci
# Wed, 12 Nov 2025 14:07:24 GMT
COPY dir:fd8f02dabe7ae9790ce0638d1f9e9f60d460b3580843d39cb4dee8e471c106cc in /      
# Wed, 12 Nov 2025 14:07:24 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 12 Nov 2025 14:07:24 GMT
CMD ["/bin/bash"]
# Wed, 12 Nov 2025 14:07:24 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 12 Nov 2025 14:07:24 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 12 Nov 2025 14:07:24 GMT
COPY file:b446d7ec96d8598bdd079305b40e4e5a0c1e0d484658876cab87a4393ac52954 in /usr/share/buildinfo/labels.json      
# Wed, 12 Nov 2025 14:07:24 GMT
COPY file:b446d7ec96d8598bdd079305b40e4e5a0c1e0d484658876cab87a4393ac52954 in /root/buildinfo/labels.json      
# Wed, 12 Nov 2025 14:07:24 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="09400c6ea1039bbeb186633c5815980c077ced2a" "org.opencontainers.image.revision"="09400c6ea1039bbeb186633c5815980c077ced2a" "build-date"="2025-11-12T14:07:06Z" "release"="1762956380"org.opencontainers.image.revision=09400c6ea1039bbeb186633c5815980c077ced2a
# Fri, 14 Nov 2025 01:13:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 01:13:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:13:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 14 Nov 2025 01:13:20 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Fri, 14 Nov 2025 01:13:20 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Fri, 14 Nov 2025 01:13:28 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 14 Nov 2025 01:13:29 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 14 Nov 2025 01:13:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 14 Nov 2025 01:13:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 01:13:29 GMT
CMD ["jshell"]
# Mon, 17 Nov 2025 19:59:04 GMT
CMD ["gradle"]
# Mon, 17 Nov 2025 19:59:04 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 17 Nov 2025 19:59:04 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 17 Nov 2025 19:59:04 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 17 Nov 2025 19:59:04 GMT
WORKDIR /home/gradle
# Mon, 17 Nov 2025 19:59:09 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 17 Nov 2025 19:59:09 GMT
ENV GRADLE_VERSION=9.2.1
# Mon, 17 Nov 2025 19:59:09 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Mon, 17 Nov 2025 19:59:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 17 Nov 2025 19:59:11 GMT
USER gradle
# Mon, 17 Nov 2025 19:59:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 17 Nov 2025 19:59:11 GMT
USER root
```

-	Layers:
	-	`sha256:179ba4be1de0701de7b39988f2989858194723f60b56b12f8d9438358e471a73`  
		Last Modified: Wed, 12 Nov 2025 15:07:23 GMT  
		Size: 40.0 MB (40048414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf0892ca9c17b1c1d03f4e21610a2e428db9a5539a8422e0e61e1f3b611d6e1`  
		Last Modified: Fri, 14 Nov 2025 01:13:59 GMT  
		Size: 30.6 MB (30635354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5cbd75d5f83f1cac1b68184e34a26ef8531e76a9b1d29416d57ade3d98627e0`  
		Last Modified: Fri, 14 Nov 2025 02:17:41 GMT  
		Size: 157.8 MB (157828920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d08b160ba258654e124d865a930f7fd39763f216cf56b4ed27d15b35c7d98b8`  
		Last Modified: Fri, 14 Nov 2025 01:13:56 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07152ac26477194c362e7fac694a5ed39cff0dfbb97006e44fb3d69150cd614`  
		Last Modified: Fri, 14 Nov 2025 01:13:56 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7cd28a356a3d9655f010dd4683f4611ba8a9be8533f85f6fb4f6d865368fcc`  
		Last Modified: Mon, 17 Nov 2025 19:59:39 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b0cc329973170e778f93d3bfcb7898dbafa5502f3a70cbc72e8cbba6f8d33d`  
		Last Modified: Mon, 17 Nov 2025 19:59:42 GMT  
		Size: 37.0 MB (37035524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4916258dfb2c8d3896a0539af3d212efe63070eda66dd82d3c073bb86655bf`  
		Last Modified: Mon, 17 Nov 2025 21:48:41 GMT  
		Size: 135.5 MB (135521970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9785c0244bc24adf927816e78e4f08575b9b7f394ccc296c25c849b7fa4542e1`  
		Last Modified: Mon, 17 Nov 2025 19:59:39 GMT  
		Size: 54.9 KB (54897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:bcc32d2212f27db11303cd008e4b9081fa2d24b2edfadb60673c072358202cae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5425158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e72c595a3a5c4d6b87cae3e29fd9640ed40e6514c786818b4f1db639e7f3e723`

```dockerfile
```

-	Layers:
	-	`sha256:700cb1d0d8ffa935f2487718a4e5e549ee9dd197d6ed0ddc4abc2e7794218caa`  
		Last Modified: Mon, 17 Nov 2025 21:25:25 GMT  
		Size: 5.4 MB (5400666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37fe61eaff7d49b5ace9e2eb6335a89619d740a74fb25d506978736f786715dc`  
		Last Modified: Mon, 17 Nov 2025 21:25:26 GMT  
		Size: 24.5 KB (24492 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk21-ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:df3f460d0068f304b9f426a92b362419470425d62f1ab5ae397e242770f622dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.2 MB (397229213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce770887fbdab4e1b30d0454a6183c6620d08b14c36f36cef73fb6e11bbaf75a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 12 Nov 2025 14:10:10 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 12 Nov 2025 14:10:10 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 12 Nov 2025 14:10:10 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 12 Nov 2025 14:10:10 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 12 Nov 2025 14:10:10 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 12 Nov 2025 14:10:10 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 12 Nov 2025 14:10:10 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 14:10:11 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 14:10:11 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 12 Nov 2025 14:10:11 GMT
LABEL io.openshift.expose-services=""
# Wed, 12 Nov 2025 14:10:11 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 12 Nov 2025 14:10:11 GMT
ENV container oci
# Wed, 12 Nov 2025 14:10:11 GMT
COPY dir:306690a4b33e0c2c47cf50b466ed471eb7ab206a490a8f74fd060934dfe49241 in /      
# Wed, 12 Nov 2025 14:10:12 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 12 Nov 2025 14:10:12 GMT
CMD ["/bin/bash"]
# Wed, 12 Nov 2025 14:10:12 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 12 Nov 2025 14:10:12 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 12 Nov 2025 14:10:12 GMT
COPY file:0fb7b120ef84051a76f1b80ab468bcf42e6749f2d4faca4621e99b2ad0f6bb9a in /usr/share/buildinfo/labels.json      
# Wed, 12 Nov 2025 14:10:12 GMT
COPY file:0fb7b120ef84051a76f1b80ab468bcf42e6749f2d4faca4621e99b2ad0f6bb9a in /root/buildinfo/labels.json      
# Wed, 12 Nov 2025 14:10:12 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="09400c6ea1039bbeb186633c5815980c077ced2a" "org.opencontainers.image.revision"="09400c6ea1039bbeb186633c5815980c077ced2a" "build-date"="2025-11-12T14:09:54Z" "release"="1762956380"org.opencontainers.image.revision=09400c6ea1039bbeb186633c5815980c077ced2a
# Fri, 14 Nov 2025 01:28:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 01:28:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:28:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 14 Nov 2025 01:28:20 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Fri, 14 Nov 2025 01:28:20 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Fri, 14 Nov 2025 01:29:12 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 14 Nov 2025 01:29:14 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 14 Nov 2025 01:29:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 14 Nov 2025 01:29:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 01:29:14 GMT
CMD ["jshell"]
# Mon, 17 Nov 2025 19:58:49 GMT
CMD ["gradle"]
# Mon, 17 Nov 2025 19:58:49 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 17 Nov 2025 19:58:49 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 17 Nov 2025 19:58:49 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 17 Nov 2025 19:58:49 GMT
WORKDIR /home/gradle
# Mon, 17 Nov 2025 19:58:54 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 17 Nov 2025 19:58:54 GMT
ENV GRADLE_VERSION=9.2.1
# Mon, 17 Nov 2025 19:58:54 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Mon, 17 Nov 2025 19:58:57 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 17 Nov 2025 19:58:57 GMT
USER gradle
# Mon, 17 Nov 2025 19:58:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 17 Nov 2025 19:58:58 GMT
USER root
```

-	Layers:
	-	`sha256:e01bb2a7f0e8ff512f86254e984d1cf0bdc9b357f1e0f0f61d352832dc12a646`  
		Last Modified: Wed, 12 Nov 2025 15:16:35 GMT  
		Size: 38.2 MB (38221043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48960c34ddbfa8b8e131fd6a7e92f7db1b2656e9ee8ed3d0004706df37396894`  
		Last Modified: Fri, 14 Nov 2025 01:28:56 GMT  
		Size: 30.9 MB (30885195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6555b47ac9e6b738b216a461b7d5987c4fd5e4c7779e554d944532547fb1c7c7`  
		Last Modified: Fri, 14 Nov 2025 02:21:10 GMT  
		Size: 156.1 MB (156111819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e24df88e7ef6b5a5ef4640d96d9516cf7a8331d206bd8196f92977b0a9882b`  
		Last Modified: Fri, 14 Nov 2025 01:29:40 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7592d68359cb83f907db6e711fafd9e5a615c48de2011368fa7e42e918dbb95`  
		Last Modified: Fri, 14 Nov 2025 01:29:39 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075b5297d191ead5e887acccc53bafb65c531b241d330c5914cfb1cb11ef83e2`  
		Last Modified: Mon, 17 Nov 2025 19:59:26 GMT  
		Size: 1.7 KB (1713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5e746f2f1407702349062d454f5b651f869c666e5da75a8e5e234f98262bd9`  
		Last Modified: Mon, 17 Nov 2025 19:59:28 GMT  
		Size: 36.4 MB (36425479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021fcf2caf62ee5586a9ff2b4287fae688d5c2debef2e88ce55935132f0de14f`  
		Last Modified: Mon, 17 Nov 2025 22:07:34 GMT  
		Size: 135.5 MB (135521974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ccf80d40c0953b47902b14ab3b77f5555c7ce8b2d57170b538b2f2e5ebd9f29`  
		Last Modified: Mon, 17 Nov 2025 19:59:26 GMT  
		Size: 59.5 KB (59540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:138b01ca633c9d5612e0f43b4ef85e9e6caa6e067d89a53358ad8e647383ac3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5424785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:843be1284407a710a4e90efc486ab51a1c6b29a171bc5e56dcf3ec3792f465c4`

```dockerfile
```

-	Layers:
	-	`sha256:976a42c67a0c552b6ba2e0650032d5152991f3234ab998c10801468403bd6c7f`  
		Last Modified: Mon, 17 Nov 2025 21:25:32 GMT  
		Size: 5.4 MB (5400096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90071bfa9d298a4dd18bef7ec091642c558db2d24dd36e2e83469810c09aa645`  
		Last Modified: Mon, 17 Nov 2025 21:25:33 GMT  
		Size: 24.7 KB (24689 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk21-ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:88b32f8ac3772dfb060eb9f60ff41c63ba76c7cf931a94520a2c395b2f7b121e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **409.5 MB (409474914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9fe37feaddc3265f8b1f5aeea05c9c1d1f4eac890fe9a2a811bef6056d21c4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 12 Nov 2025 14:16:19 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 12 Nov 2025 14:16:19 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 12 Nov 2025 14:16:19 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 12 Nov 2025 14:16:19 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 12 Nov 2025 14:16:19 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 12 Nov 2025 14:16:19 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 12 Nov 2025 14:16:19 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 14:16:19 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 14:16:19 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 12 Nov 2025 14:16:19 GMT
LABEL io.openshift.expose-services=""
# Wed, 12 Nov 2025 14:16:19 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 12 Nov 2025 14:16:19 GMT
ENV container oci
# Wed, 12 Nov 2025 14:16:20 GMT
COPY dir:b82b42d48fe8d3e110150627be797446b78337654b9b58113dd416e573c5a220 in /      
# Wed, 12 Nov 2025 14:16:20 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 12 Nov 2025 14:16:20 GMT
CMD ["/bin/bash"]
# Wed, 12 Nov 2025 14:16:20 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 12 Nov 2025 14:16:20 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 12 Nov 2025 14:16:20 GMT
COPY file:64a778769303615894b65a7e1f48ca07c19f426b240dc8585547e487e79b9119 in /usr/share/buildinfo/labels.json      
# Wed, 12 Nov 2025 14:16:20 GMT
COPY file:64a778769303615894b65a7e1f48ca07c19f426b240dc8585547e487e79b9119 in /root/buildinfo/labels.json      
# Wed, 12 Nov 2025 14:16:21 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="09400c6ea1039bbeb186633c5815980c077ced2a" "org.opencontainers.image.revision"="09400c6ea1039bbeb186633c5815980c077ced2a" "build-date"="2025-11-12T14:16:09Z" "release"="1762956380"org.opencontainers.image.revision=09400c6ea1039bbeb186633c5815980c077ced2a
# Fri, 14 Nov 2025 02:05:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 02:05:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 02:05:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 14 Nov 2025 02:05:53 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Fri, 14 Nov 2025 02:05:53 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Fri, 14 Nov 2025 02:21:02 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 14 Nov 2025 02:21:04 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 14 Nov 2025 02:21:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 14 Nov 2025 02:21:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 02:21:05 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 08:05:13 GMT
CMD ["gradle"]
# Fri, 14 Nov 2025 08:05:13 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 14 Nov 2025 08:05:13 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 14 Nov 2025 08:05:13 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 14 Nov 2025 08:05:13 GMT
WORKDIR /home/gradle
# Mon, 17 Nov 2025 19:58:44 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 17 Nov 2025 19:58:44 GMT
ENV GRADLE_VERSION=9.2.1
# Mon, 17 Nov 2025 19:58:44 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Mon, 17 Nov 2025 19:58:51 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 17 Nov 2025 19:58:51 GMT
USER gradle
# Mon, 17 Nov 2025 19:58:53 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 17 Nov 2025 19:58:53 GMT
USER root
```

-	Layers:
	-	`sha256:179a593a6a9b7d7a22e6d6775d4ba55276bcd89646d198335c7dc5df13535e72`  
		Last Modified: Wed, 12 Nov 2025 18:10:57 GMT  
		Size: 44.5 MB (44458676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4bd2e498d81706e50aadabea204732bf19ba120b5389dc6dfedc310c13bcf4`  
		Last Modified: Fri, 14 Nov 2025 02:06:55 GMT  
		Size: 33.2 MB (33208505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c980495aa2fa67a0f40767948937b258c1fe39bc30aeb53c96dadc991d9d4b6e`  
		Last Modified: Fri, 14 Nov 2025 13:23:48 GMT  
		Size: 157.9 MB (157943395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f9d4c6d7ec61d25b7a0a9f0d6a9ac0eb736079a25df2fd6f361f1cf0f714db`  
		Last Modified: Fri, 14 Nov 2025 02:22:04 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2abf17a7dc1f9c30e9eefdec3e9e26b64b525361e166bfc2f0087effcbe0029`  
		Last Modified: Fri, 14 Nov 2025 02:22:04 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5214d77cbddf94f2a16e8bea1db91d211e0057c99c7885c5580016825274f3`  
		Last Modified: Fri, 14 Nov 2025 08:07:27 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b10761414a9cdb8ba28711a44b4669ed7fc7158b51dff24f379733571113ac`  
		Last Modified: Mon, 17 Nov 2025 19:59:57 GMT  
		Size: 38.3 MB (38303185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2072f651b1faef2b9f21e2a7c48da7d95c3aba9db42986dcc0368333753546ca`  
		Last Modified: Mon, 17 Nov 2025 23:40:04 GMT  
		Size: 135.5 MB (135521973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0f5187a01c5253cb98c0d13db794a12d93c3215a32a167450975e9599d1c47`  
		Last Modified: Mon, 17 Nov 2025 19:59:55 GMT  
		Size: 35.0 KB (35019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:a6570682674352836e532e08ea536f5f44e530fe0af6dbc51777b55776ca4398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5422603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc73366db5a1a06c84bc5a730ec2503dffaf0d14d044e22e9dcd3ef7c74d737`

```dockerfile
```

-	Layers:
	-	`sha256:4b1aa472dfc52ed0ed094b4c69c2bc107ecce42f0c3b227fe7e1d0438de43e6c`  
		Last Modified: Mon, 17 Nov 2025 21:25:39 GMT  
		Size: 5.4 MB (5398001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80aa5eb00908c39bb829643c35da05929353f3cf709587c76f263fb49c1d4912`  
		Last Modified: Mon, 17 Nov 2025 21:25:39 GMT  
		Size: 24.6 KB (24602 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk21-ubi` - linux; s390x

```console
$ docker pull gradle@sha256:d816e4503bd2f07769bd25dfb6146cf34f6a6c8ec6bd8a3823b27aa6a656cadc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.7 MB (387660769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c02c8bd22f3b96b5d2901d747a3343f5abde42c8a308bba97c886fd34ba33b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 12 Nov 2025 14:23:14 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 12 Nov 2025 14:23:14 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 12 Nov 2025 14:23:14 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 12 Nov 2025 14:23:14 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 12 Nov 2025 14:23:14 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 12 Nov 2025 14:23:14 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 12 Nov 2025 14:23:14 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 14:23:14 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 14:23:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 12 Nov 2025 14:23:15 GMT
LABEL io.openshift.expose-services=""
# Wed, 12 Nov 2025 14:23:15 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 12 Nov 2025 14:23:15 GMT
ENV container oci
# Wed, 12 Nov 2025 14:23:15 GMT
COPY dir:8fb28e41f0652f38250d50e7c8b787f823f9c655088e3095ff5bb5e88ff8abdb in /      
# Wed, 12 Nov 2025 14:23:15 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 12 Nov 2025 14:23:15 GMT
CMD ["/bin/bash"]
# Wed, 12 Nov 2025 14:23:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 12 Nov 2025 14:23:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 12 Nov 2025 14:23:15 GMT
COPY file:871581d6a37c5961759af7dee95b7002ef35c09f77e017243a464bb731d06145 in /usr/share/buildinfo/labels.json      
# Wed, 12 Nov 2025 14:23:15 GMT
COPY file:871581d6a37c5961759af7dee95b7002ef35c09f77e017243a464bb731d06145 in /root/buildinfo/labels.json      
# Wed, 12 Nov 2025 14:23:16 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="09400c6ea1039bbeb186633c5815980c077ced2a" "org.opencontainers.image.revision"="09400c6ea1039bbeb186633c5815980c077ced2a" "build-date"="2025-11-12T14:23:04Z" "release"="1762956380"org.opencontainers.image.revision=09400c6ea1039bbeb186633c5815980c077ced2a
# Fri, 14 Nov 2025 01:40:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 01:40:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:40:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 14 Nov 2025 01:40:01 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Fri, 14 Nov 2025 01:40:01 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Fri, 14 Nov 2025 01:40:06 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 14 Nov 2025 01:40:07 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 14 Nov 2025 01:40:07 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 14 Nov 2025 01:40:07 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 01:40:07 GMT
CMD ["jshell"]
# Mon, 17 Nov 2025 19:56:20 GMT
CMD ["gradle"]
# Mon, 17 Nov 2025 19:56:20 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 17 Nov 2025 19:56:20 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 17 Nov 2025 19:56:20 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 17 Nov 2025 19:56:20 GMT
WORKDIR /home/gradle
# Mon, 17 Nov 2025 19:56:39 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 17 Nov 2025 19:56:39 GMT
ENV GRADLE_VERSION=9.2.1
# Mon, 17 Nov 2025 19:56:39 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Mon, 17 Nov 2025 19:56:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 17 Nov 2025 19:56:43 GMT
USER gradle
# Mon, 17 Nov 2025 19:56:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 17 Nov 2025 19:56:46 GMT
USER root
```

-	Layers:
	-	`sha256:d163f17b10d9f2c2fb3a866ba5330a41136f00b32975ee3b44f80939989d11e6`  
		Last Modified: Wed, 12 Nov 2025 18:10:56 GMT  
		Size: 38.1 MB (38137296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc6ad800512727eaead634a70032a4ad768f37bd18ae03ba4ceb9ecf331d4f8`  
		Last Modified: Fri, 14 Nov 2025 01:40:42 GMT  
		Size: 30.3 MB (30256406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4325f70aba5ca5f7d0ecec4862e43fb02145fe1eedce5bda232bf7ee93e34416`  
		Last Modified: Fri, 14 Nov 2025 03:05:49 GMT  
		Size: 147.1 MB (147068416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123f1eb9ab667c2b5b7febf2d1d45f8b2be4a545b9ea3c4586bf0f957a269865`  
		Last Modified: Fri, 14 Nov 2025 01:40:40 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c3da9afb6729cf1fef240ea7a2cdf4f5b88246089f5e2280d26f3488388de1`  
		Last Modified: Fri, 14 Nov 2025 01:40:40 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66a867a05f866e2fd868d0078eaf5cf987a784411f7291ef77bb2d09525daa1`  
		Last Modified: Mon, 17 Nov 2025 19:57:46 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b81507cc919890d994291b64e55f55db4a224d12c9cd396af18d64ac92f947`  
		Last Modified: Mon, 17 Nov 2025 19:57:49 GMT  
		Size: 36.6 MB (36637478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84589b3b22b25e5eb495275b08c5584b53d03fbc82ccedf5becebcd3b7b46ff3`  
		Last Modified: Mon, 17 Nov 2025 19:57:41 GMT  
		Size: 135.5 MB (135521999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b5842bb024b6c407eac0579210f1d463e332b42a428a482ea6f79344b27dd5`  
		Last Modified: Mon, 17 Nov 2025 19:57:46 GMT  
		Size: 35.0 KB (35006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:95c341459f99d40f5447c412741edcd5044bde83f64bea4638e8548970c5ac87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5411799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f44f37b2e8b37281f854832aff49acb694e5c5ea533c7cafce8deb1426c6b4fe`

```dockerfile
```

-	Layers:
	-	`sha256:59610f6dfd7a53671f4a6ecc7ff40768d6f12c615373d8877071ba9326557648`  
		Last Modified: Mon, 17 Nov 2025 21:25:45 GMT  
		Size: 5.4 MB (5387271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d252a5f3464918d963e07374691006e57daf9f64b45ba7956abaf6fba4dfe2b7`  
		Last Modified: Mon, 17 Nov 2025 21:25:46 GMT  
		Size: 24.5 KB (24528 bytes)  
		MIME: application/vnd.in-toto+json
