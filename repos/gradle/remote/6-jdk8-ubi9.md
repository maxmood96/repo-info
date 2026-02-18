## `gradle:6-jdk8-ubi9`

```console
$ docker pull gradle@sha256:eb02ee7fe977aa4923649a0b763470966cdfd986d47083e45c7158e43421c152
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `gradle:6-jdk8-ubi9` - linux; amd64

```console
$ docker pull gradle@sha256:fbf616b6b5cff8c4c07e08e1cbcf9c03a2ad0281da70667df9f07d737bec919a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.4 MB (270440365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71bb06474935deafa8b463b33ad47ac7cfa26977b60fc20812bae877da706c9f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 17 Feb 2026 16:42:45 GMT
ENV container oci
# Tue, 17 Feb 2026 16:42:46 GMT
COPY dir:a84da6f36b88f4eb0d6c411f65b34c1a9d85150d3035dd516db4ece0c2569465 in /      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 17 Feb 2026 16:42:46 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:6326b4becf4dcc53eab9a0e80efe304ada5421165d0586862d969cb5fa826bd8 in /usr/share/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:6326b4becf4dcc53eab9a0e80efe304ada5421165d0586862d969cb5fa826bd8 in /root/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:42:46 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0ced2bbee24d5463d4530756a57f8db895246c48" "org.opencontainers.image.revision"="0ced2bbee24d5463d4530756a57f8db895246c48" "build-date"="2026-02-17T16:42:34Z" "org.opencontainers.image.created"="2026-02-17T16:42:34Z" "release"="1771346502"org.opencontainers.image.revision=0ced2bbee24d5463d4530756a57f8db895246c48,org.opencontainers.image.created=2026-02-17T16:42:34Z
# Wed, 18 Feb 2026 19:19:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Feb 2026 19:19:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 19:19:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Feb 2026 19:19:45 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 18 Feb 2026 19:19:45 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Wed, 18 Feb 2026 19:19:50 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        ppc64le)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        x86_64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Wed, 18 Feb 2026 19:19:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 18 Feb 2026 19:19:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Feb 2026 19:19:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 18 Feb 2026 20:12:00 GMT
CMD ["gradle"]
# Wed, 18 Feb 2026 20:12:00 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 18 Feb 2026 20:12:00 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 18 Feb 2026 20:12:00 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 18 Feb 2026 20:12:00 GMT
WORKDIR /home/gradle
# Wed, 18 Feb 2026 20:12:04 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 18 Feb 2026 20:12:04 GMT
ENV GRADLE_VERSION=6.9.4
# Wed, 18 Feb 2026 20:12:04 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Wed, 18 Feb 2026 20:12:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 18 Feb 2026 20:12:06 GMT
USER gradle
# Wed, 18 Feb 2026 20:12:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 18 Feb 2026 20:12:07 GMT
USER root
```

-	Layers:
	-	`sha256:4638e3415987f378f2d6dd70f9c6a2869dd5ebd09e3510ba45e46bbb6ec1a3dd`  
		Last Modified: Tue, 17 Feb 2026 18:08:54 GMT  
		Size: 40.0 MB (40033596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:448edd91b2ee4fa896bbb5c9b0e4e94d03cdbdd696ee3168e86e22d01889136e`  
		Last Modified: Wed, 18 Feb 2026 19:20:04 GMT  
		Size: 30.4 MB (30395441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0093472000e75d143a9bba1922dcacbc43fc2b08d29d37b640c53190b1bde6e5`  
		Last Modified: Wed, 18 Feb 2026 19:20:05 GMT  
		Size: 55.2 MB (55170652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49372b1fd3e98495425454d32a17572821e2cb4ed8610236127e00c8d3f4bcf2`  
		Last Modified: Wed, 18 Feb 2026 19:20:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75367c40b6ba5d783b172f35c1cc4fddef850db8a776e3abab5e12e5c6f8171a`  
		Last Modified: Wed, 18 Feb 2026 19:20:03 GMT  
		Size: 2.3 KB (2313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc70607eac0e31a5f615ee7064613d7215b4807b204d020fa59bc592bd371d7`  
		Last Modified: Wed, 18 Feb 2026 20:12:21 GMT  
		Size: 1.7 KB (1701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872e11530dfd0450a647beafbf423ea49c197e20dd63040d446fc41f68bef0da`  
		Last Modified: Wed, 18 Feb 2026 20:12:23 GMT  
		Size: 36.7 MB (36708565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2127b1b8e6b6ad2e2645d596caacb9ec53a096d8cc1500366f95468f10c5d3af`  
		Last Modified: Wed, 18 Feb 2026 20:12:24 GMT  
		Size: 107.7 MB (107696663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47bc2e2ec74c590d91d4517abb722d63305f1db8477799030be7497653591dc5`  
		Last Modified: Wed, 18 Feb 2026 20:12:22 GMT  
		Size: 431.3 KB (431276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:4833604f00ba9279a26da34757062e0efc07a0452ff16cd19373b5689e9df6e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5441144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76e20f6714dbfecb8f4ea189721b8ddac88867bdcdb2e4a1e0d6ebbc83b9ad33`

```dockerfile
```

-	Layers:
	-	`sha256:b4ca597a416a2b9ac3e2fd2aa7df03e300ec2cf367a7dd5cbd32ca5df240faf2`  
		Last Modified: Wed, 18 Feb 2026 20:12:22 GMT  
		Size: 5.4 MB (5417625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:214af60c1b5e186721030742ba231a75a8737f8659b5178df1205168b6db7da2`  
		Last Modified: Wed, 18 Feb 2026 20:12:21 GMT  
		Size: 23.5 KB (23519 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk8-ubi9` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:61e0dc81c7d24690eb8f6be673a1e49c332dad9560e8aa93a0fc40f1e4337ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.5 MB (267463731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c1b0e533f33c0ec31fb7f59017a7826315a09aa2151576f082ec3583b2bc796`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 17 Feb 2026 16:45:44 GMT
ENV container oci
# Tue, 17 Feb 2026 16:45:45 GMT
COPY dir:ac0ab1292a52ccb276077ed994531e1a3deef7d271c3502d95032264a0448d19 in /      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 17 Feb 2026 16:45:45 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:b6e9611fd18f4ab100ec73ea6037b1118108a414096af83dfb78d47ad0a2b249 in /usr/share/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:b6e9611fd18f4ab100ec73ea6037b1118108a414096af83dfb78d47ad0a2b249 in /root/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:45:46 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0ced2bbee24d5463d4530756a57f8db895246c48" "org.opencontainers.image.revision"="0ced2bbee24d5463d4530756a57f8db895246c48" "build-date"="2026-02-17T16:45:31Z" "org.opencontainers.image.created"="2026-02-17T16:45:31Z" "release"="1771346502"org.opencontainers.image.revision=0ced2bbee24d5463d4530756a57f8db895246c48,org.opencontainers.image.created=2026-02-17T16:45:31Z
# Wed, 18 Feb 2026 19:16:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Feb 2026 19:16:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 19:16:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Feb 2026 19:16:40 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 18 Feb 2026 19:16:40 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Wed, 18 Feb 2026 19:16:45 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        ppc64le)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        x86_64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Wed, 18 Feb 2026 19:16:45 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 18 Feb 2026 19:16:45 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Feb 2026 19:16:45 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 18 Feb 2026 20:11:29 GMT
CMD ["gradle"]
# Wed, 18 Feb 2026 20:11:29 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 18 Feb 2026 20:11:29 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 18 Feb 2026 20:11:29 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 18 Feb 2026 20:11:29 GMT
WORKDIR /home/gradle
# Wed, 18 Feb 2026 20:11:33 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 18 Feb 2026 20:11:33 GMT
ENV GRADLE_VERSION=6.9.4
# Wed, 18 Feb 2026 20:11:33 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Wed, 18 Feb 2026 20:11:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 18 Feb 2026 20:11:35 GMT
USER gradle
# Wed, 18 Feb 2026 20:11:36 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 18 Feb 2026 20:11:36 GMT
USER root
```

-	Layers:
	-	`sha256:063fbd5fac6af91f4042bbe66bae69795aa46675d5b0c800ed195ad79ed8fb02`  
		Last Modified: Tue, 17 Feb 2026 18:09:11 GMT  
		Size: 38.2 MB (38202534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a2646c40d44a7a462d59bb0a2fca3186042f1c52ec9253b267e1e7b03cc022`  
		Last Modified: Wed, 18 Feb 2026 19:16:59 GMT  
		Size: 30.8 MB (30825760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593901ccb9b963f69431c18cdd5322db76066e8bf866594012010290895a8473`  
		Last Modified: Wed, 18 Feb 2026 19:17:00 GMT  
		Size: 54.3 MB (54252023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b6cf9ca8b65d2d2161a1909f44e9a4ce669ea909320c3b0875dddfd6fc869e`  
		Last Modified: Wed, 18 Feb 2026 19:16:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686770abfeeda2e9394da5fc001a3e655d967de1858c422d92822a8d109925f1`  
		Last Modified: Wed, 18 Feb 2026 19:16:59 GMT  
		Size: 2.3 KB (2314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89da490100b3b5963976beb82a22c9ee470dc4dae31ef02705e73ada7c8ba9c7`  
		Last Modified: Wed, 18 Feb 2026 20:11:50 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b536e7fb3c2cf5423ba5a5518b4c523fe8b1580c939e4afed0c88d110f554e3e`  
		Last Modified: Wed, 18 Feb 2026 20:11:52 GMT  
		Size: 36.1 MB (36057537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc398cd23bf890886573d2a79816272822fb9144964f35a090db46541796a71`  
		Last Modified: Wed, 18 Feb 2026 20:11:53 GMT  
		Size: 107.7 MB (107696667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df3a5cf3b43997af5d4a0057540a9091f2754bc313f09effb7198d903b76892`  
		Last Modified: Wed, 18 Feb 2026 20:11:50 GMT  
		Size: 425.0 KB (425033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:c578ebeddbd76fd7056e9373178bad2718be11508ebc135d93450059ddd82269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5441423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c27ebaf6bc78af35c752ed4e27e5b867ffa65df82a9c652914c28613a3ceb0a`

```dockerfile
```

-	Layers:
	-	`sha256:49a73d2fd236914c2e160522cf7ede3d89e62edaaa0ad3868c3b3e068882cdc9`  
		Last Modified: Wed, 18 Feb 2026 20:11:50 GMT  
		Size: 5.4 MB (5417731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:367a5aa92e14e96dc88bbe4f93424423a03b881324f54b1b137ac08cfcb55d30`  
		Last Modified: Wed, 18 Feb 2026 20:11:50 GMT  
		Size: 23.7 KB (23692 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk8-ubi9` - linux; ppc64le

```console
$ docker pull gradle@sha256:cd75a2b1e3fb110f790ce732b820040d0332fd7daae15a40cb5919b5e0884de4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.7 MB (275662105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8f9df2b24189b264af2b96923ab2623ec13fb0bb12627a65562ad2b6d4f203e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 17 Feb 2026 17:14:47 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Feb 2026 17:14:47 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 17 Feb 2026 17:14:47 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 17 Feb 2026 17:14:47 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 17 Feb 2026 17:14:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Feb 2026 17:14:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 17 Feb 2026 17:14:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 17:14:47 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 17:14:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 17 Feb 2026 17:14:47 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Feb 2026 17:14:47 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 17 Feb 2026 17:14:47 GMT
ENV container oci
# Tue, 17 Feb 2026 17:14:48 GMT
COPY dir:3a75322911f167c45a527d249b8b7a1bb61960bd0414c69e2c48ff05f3aaaa64 in /      
# Tue, 17 Feb 2026 17:14:48 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 17 Feb 2026 17:14:48 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 17:14:48 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 17 Feb 2026 17:14:48 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 17 Feb 2026 17:14:48 GMT
COPY file:4d5fe83a4c701a100e1eaed18157926865f67ffe30ea0c801e48164ab289c12d in /usr/share/buildinfo/labels.json      
# Tue, 17 Feb 2026 17:14:48 GMT
COPY file:4d5fe83a4c701a100e1eaed18157926865f67ffe30ea0c801e48164ab289c12d in /root/buildinfo/labels.json      
# Tue, 17 Feb 2026 17:14:48 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="0ced2bbee24d5463d4530756a57f8db895246c48" "org.opencontainers.image.revision"="0ced2bbee24d5463d4530756a57f8db895246c48" "build-date"="2026-02-17T17:14:36Z" "org.opencontainers.image.created"="2026-02-17T17:14:36Z" "release"="1771346502"org.opencontainers.image.revision=0ced2bbee24d5463d4530756a57f8db895246c48,org.opencontainers.image.created=2026-02-17T17:14:36Z
# Wed, 18 Feb 2026 19:22:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Feb 2026 19:22:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 19:22:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Feb 2026 19:22:09 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 18 Feb 2026 19:22:09 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Wed, 18 Feb 2026 19:22:19 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        ppc64le)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        x86_64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Wed, 18 Feb 2026 19:22:23 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 18 Feb 2026 19:22:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Feb 2026 19:22:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 18 Feb 2026 20:12:48 GMT
CMD ["gradle"]
# Wed, 18 Feb 2026 20:12:48 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 18 Feb 2026 20:12:48 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 18 Feb 2026 20:12:48 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 18 Feb 2026 20:12:48 GMT
WORKDIR /home/gradle
# Wed, 18 Feb 2026 20:13:03 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 18 Feb 2026 20:13:03 GMT
ENV GRADLE_VERSION=6.9.4
# Wed, 18 Feb 2026 20:13:03 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Wed, 18 Feb 2026 20:16:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 18 Feb 2026 20:16:22 GMT
USER gradle
# Wed, 18 Feb 2026 20:16:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 18 Feb 2026 20:16:23 GMT
USER root
```

-	Layers:
	-	`sha256:722693878ac364b9d2ee6aa4d50e67ce459b9548beed24d0bb6ff115844b6e5d`  
		Last Modified: Tue, 17 Feb 2026 18:09:24 GMT  
		Size: 44.5 MB (44450261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bee69fcb88d423dd51b4ae1e9aa4be9eb53f1df38695a23566fd8e316cd932`  
		Last Modified: Wed, 18 Feb 2026 19:22:54 GMT  
		Size: 32.9 MB (32872323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a32074c16ad1eada72d118b6ff88d43c2837ed9781570bd502d736c7942dd43`  
		Last Modified: Wed, 18 Feb 2026 19:22:55 GMT  
		Size: 52.7 MB (52650909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c4681e2903c0151fcf3561763631bb95af198bc96f947a0f3306764bd36b60`  
		Last Modified: Wed, 18 Feb 2026 19:22:51 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec67d5ae7a94e339b76acee07d4574af40c15762f4885d46a49e509e2c38a180`  
		Last Modified: Wed, 18 Feb 2026 19:22:53 GMT  
		Size: 2.3 KB (2314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4003812106810ac8eb63d0261e659f4a7e317b89a8aae89170d98d0b02b8e83`  
		Last Modified: Wed, 18 Feb 2026 20:13:53 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f71b7b3247335e5081cf94a81cdaea9508aa19287a58bdf96e0aead3e03792`  
		Last Modified: Wed, 18 Feb 2026 20:13:55 GMT  
		Size: 38.0 MB (37952780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77fe0dfc70e60b1313a823ac66ac71ac328a213971f960286454c8d02f8eb58d`  
		Last Modified: Wed, 18 Feb 2026 20:17:06 GMT  
		Size: 107.7 MB (107696669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b847eff809818d0597bffc4502af0a1cf8c6865eca529412688016d482499ad`  
		Last Modified: Wed, 18 Feb 2026 20:17:03 GMT  
		Size: 35.0 KB (34984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:64d733f2e43455246788cf7e911e6aca924ddd2624e947d73da32f38347ebc20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5439159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db1d9ad5865fca8d10087a98b3877dba5f38234603ebcfefbb1ee886b9f4fede`

```dockerfile
```

-	Layers:
	-	`sha256:c1f191f2f09336f59c712862d698bc219cddec9773ad5273bc6f14fc8561e1ef`  
		Last Modified: Wed, 18 Feb 2026 20:17:03 GMT  
		Size: 5.4 MB (5415543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ad72d904d3b586b082fa6bedf0f0964952ac5a1951d3e7a5b393b7132a0e454`  
		Last Modified: Wed, 18 Feb 2026 20:17:03 GMT  
		Size: 23.6 KB (23616 bytes)  
		MIME: application/vnd.in-toto+json
