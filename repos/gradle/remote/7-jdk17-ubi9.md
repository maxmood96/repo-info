## `gradle:7-jdk17-ubi9`

```console
$ docker pull gradle@sha256:41cf8623c321b0e9b8f7ca11137b737dc52b9c405b241ae9d3967796d3808c8d
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

### `gradle:7-jdk17-ubi9` - linux; amd64

```console
$ docker pull gradle@sha256:597cdbedfd4efc9cc05febeb0b96039eb51828636f3b70e69681f16eb36932a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.2 MB (381212114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf540eb8bbbf40ee2334d45d7a214a61bd802b228e3b09c75a694b8fd30aaec`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Apr 2026 04:52:35 GMT
ENV container oci
# Wed, 08 Apr 2026 04:52:35 GMT
COPY dir:7e1fa46f22db9f15d490572bbe30fedb301ac6c3ea9196eda6f29556472de21e in /      
# Wed, 08 Apr 2026 04:52:35 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 08 Apr 2026 04:52:35 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /usr/share/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /root/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="470b852dce8e880416927445bd12327938b329e2" "org.opencontainers.image.revision"="470b852dce8e880416927445bd12327938b329e2" "build-date"="2026-04-08T04:52:24Z" "org.opencontainers.image.created"="2026-04-08T04:52:24Z" "release"="1775623882"org.opencontainers.image.revision=470b852dce8e880416927445bd12327938b329e2,org.opencontainers.image.created=2026-04-08T04:52:24Z
# Wed, 08 Apr 2026 17:25:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 08 Apr 2026 17:25:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2026 17:25:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 08 Apr 2026 17:25:32 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 08 Apr 2026 17:25:32 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 08 Apr 2026 17:26:23 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 08 Apr 2026 17:26:24 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 08 Apr 2026 17:26:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 08 Apr 2026 17:26:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 08 Apr 2026 17:26:24 GMT
CMD ["jshell"]
# Wed, 08 Apr 2026 18:12:44 GMT
CMD ["gradle"]
# Wed, 08 Apr 2026 18:12:44 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 08 Apr 2026 18:12:44 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 08 Apr 2026 18:12:44 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 08 Apr 2026 18:12:44 GMT
WORKDIR /home/gradle
# Wed, 08 Apr 2026 18:12:48 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 08 Apr 2026 18:12:48 GMT
ENV GRADLE_VERSION=7.6.6
# Wed, 08 Apr 2026 18:12:48 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Wed, 08 Apr 2026 18:12:51 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 08 Apr 2026 18:12:51 GMT
USER gradle
# Wed, 08 Apr 2026 18:12:51 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 08 Apr 2026 18:12:51 GMT
USER root
```

-	Layers:
	-	`sha256:d70a90fdfb362fd73aa4eb84ad1d7bb2a584e2d13f7e6f51200923818455d13e`  
		Last Modified: Wed, 08 Apr 2026 05:42:00 GMT  
		Size: 40.0 MB (39982647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79584430aa583bd660ed7237fef3731db66561c908aba01292610eadce03ff8f`  
		Last Modified: Wed, 08 Apr 2026 17:26:01 GMT  
		Size: 30.4 MB (30368915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee8665dff770e5a43caabaa7663060d9b9e5a3d10dac406064e037997063289`  
		Last Modified: Wed, 08 Apr 2026 17:26:43 GMT  
		Size: 145.6 MB (145637117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b89eacd207f972373357dad4d3c7468f258faf42cb4448baf367319c7b43851`  
		Last Modified: Wed, 08 Apr 2026 17:26:39 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc006677dcd77f18ffed0eeb29b67006e72615132f9b1cc7b8832606c5164e8c`  
		Last Modified: Wed, 08 Apr 2026 17:26:40 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156d853902817b4d8d9e1fe2e684ab6dfad9276d81aa2e14aec51170bda4f683`  
		Last Modified: Wed, 08 Apr 2026 18:13:08 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a647fca7720c9d2fba56f1d7135bb7627f3f686e361699625f017a7c8110c685`  
		Last Modified: Wed, 08 Apr 2026 18:13:11 GMT  
		Size: 36.7 MB (36694953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07502aa0ba32f98afb6510bba4522945c9480c705aeea3add0196c7ccfe8635`  
		Last Modified: Wed, 08 Apr 2026 18:13:13 GMT  
		Size: 128.5 MB (128469420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024a510e810f8ccf99b05a059957ff4ca263c0b099cdfdbc78a225b010e2fb26`  
		Last Modified: Wed, 08 Apr 2026 18:13:09 GMT  
		Size: 54.9 KB (54902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:05eadab0523d93020afadfafe1e6039e89eb8165f5601cdc559d54b287c6f12e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5338093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43e971a5d5041ec2cf443b47dc1f42878f402b993911f96b63f9f796525b656a`

```dockerfile
```

-	Layers:
	-	`sha256:2e4fc778ea0f7727240e5712c1e8a2f4007bf720883203d9c9e09c13967536a2`  
		Last Modified: Wed, 08 Apr 2026 18:13:09 GMT  
		Size: 5.3 MB (5314550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be68285dc8e3f0addb1c30d3fcd7822c4dccbe7fe3de558dcef01b84080854db`  
		Last Modified: Wed, 08 Apr 2026 18:13:08 GMT  
		Size: 23.5 KB (23543 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk17-ubi9` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:1d3da76fedd41210c6cbfd7a3a5aa564aeb8f534986b7753987225d70014e9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.0 MB (378005273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f74fbf846bbd300066b19387ee6c314315302b16a7be4dcb7e8586f8c6febec4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Apr 2026 04:55:31 GMT
ENV container oci
# Wed, 08 Apr 2026 04:55:32 GMT
COPY dir:e3968b666ccf8b1da827a1f934e7d66b38ad6335b0bf20a2a01583a6f9f3fdaa in /      
# Wed, 08 Apr 2026 04:55:32 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 08 Apr 2026 04:55:32 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 04:55:32 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 08 Apr 2026 04:55:32 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 08 Apr 2026 04:55:32 GMT
COPY file:696dd319730ed197429cabc840fe5bc51d4286962e2bde67f5d48480e8cbdd7b in /usr/share/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:55:32 GMT
COPY file:696dd319730ed197429cabc840fe5bc51d4286962e2bde67f5d48480e8cbdd7b in /root/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:55:33 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="470b852dce8e880416927445bd12327938b329e2" "org.opencontainers.image.revision"="470b852dce8e880416927445bd12327938b329e2" "build-date"="2026-04-08T04:55:18Z" "org.opencontainers.image.created"="2026-04-08T04:55:18Z" "release"="1775623882"org.opencontainers.image.revision=470b852dce8e880416927445bd12327938b329e2,org.opencontainers.image.created=2026-04-08T04:55:18Z
# Wed, 08 Apr 2026 17:27:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 08 Apr 2026 17:27:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2026 17:27:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 08 Apr 2026 17:27:14 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 08 Apr 2026 17:27:14 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 08 Apr 2026 17:27:44 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 08 Apr 2026 17:27:46 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 08 Apr 2026 17:27:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 08 Apr 2026 17:27:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 08 Apr 2026 17:27:46 GMT
CMD ["jshell"]
# Wed, 08 Apr 2026 18:12:42 GMT
CMD ["gradle"]
# Wed, 08 Apr 2026 18:12:42 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 08 Apr 2026 18:12:42 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 08 Apr 2026 18:12:42 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 08 Apr 2026 18:12:42 GMT
WORKDIR /home/gradle
# Wed, 08 Apr 2026 18:12:46 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 08 Apr 2026 18:12:46 GMT
ENV GRADLE_VERSION=7.6.6
# Wed, 08 Apr 2026 18:12:46 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Wed, 08 Apr 2026 18:12:49 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 08 Apr 2026 18:12:49 GMT
USER gradle
# Wed, 08 Apr 2026 18:12:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 08 Apr 2026 18:12:50 GMT
USER root
```

-	Layers:
	-	`sha256:1ffb0d1826b0600c6d4836c7ada23756af4c1475452e12ce1bed713d58738262`  
		Last Modified: Wed, 08 Apr 2026 05:41:58 GMT  
		Size: 38.2 MB (38200278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f84dfe3f54e12d5e46be4489a23625ea95818f60b31a88025af82da048b7b1f`  
		Last Modified: Wed, 08 Apr 2026 17:27:31 GMT  
		Size: 30.8 MB (30795542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a35da8ea1e7acf19b0c6f00c6f9b201f8d6593f89f230f9b224f860272d1647`  
		Last Modified: Wed, 08 Apr 2026 17:28:05 GMT  
		Size: 144.4 MB (144446588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a88c5dc6c7e403a2ac70a778b84badbfee0a3f0c283b23c75f1dc34ed0a862`  
		Last Modified: Wed, 08 Apr 2026 17:28:01 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18a4085ba4afea9e40c6a9cea5fa654091056c1d8993fcc84613e899a1fe879`  
		Last Modified: Wed, 08 Apr 2026 17:28:01 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0317666dbc71b47c760352120bec700210d99c3b34462735ce7f2eb429e426`  
		Last Modified: Wed, 08 Apr 2026 18:13:07 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e84c96daa20dd2df83e1af2482d423bb72cf6653b7862953475a5e0ec04a17`  
		Last Modified: Wed, 08 Apr 2026 18:13:09 GMT  
		Size: 36.0 MB (36029758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296ed0f4bf0e096018a0f905db155fcb18ab915eee0e4d8b288944063ad2de2f`  
		Last Modified: Wed, 08 Apr 2026 18:13:12 GMT  
		Size: 128.5 MB (128469423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0514f0a42ecfa6e5abcd7cad3309ad265237a7f3f0a917e1653779bc771e715b`  
		Last Modified: Wed, 08 Apr 2026 18:13:07 GMT  
		Size: 59.5 KB (59524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:e20d52149cc00b10b07c9ada107e2c8ffcec8a133efa8b4c59634dab50853775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5337672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f500819d688a17864bc05b04740ac11892f3cee5b023cfc1b7874732e7177198`

```dockerfile
```

-	Layers:
	-	`sha256:e7c9acd53bfbc3fab86aa2f590a63161f55664597d3baf4688fd44587d93cf40`  
		Last Modified: Wed, 08 Apr 2026 18:13:07 GMT  
		Size: 5.3 MB (5313956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e03d5a9f977326775a48f485f4d2e22d1dd692001060eb24152285ea1ba013c`  
		Last Modified: Wed, 08 Apr 2026 18:13:06 GMT  
		Size: 23.7 KB (23716 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk17-ubi9` - linux; ppc64le

```console
$ docker pull gradle@sha256:c43a8fc09c743fe8f57682b11c52a7948bbbc979b2f23c2a71ce77206b409875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.2 MB (389205309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:378effdad0c334d9919965576e7db1b6222b0505bcb87e2d3ab69a851032255e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 08 Apr 2026 04:54:19 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Apr 2026 04:54:19 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Apr 2026 04:54:19 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 08 Apr 2026 04:54:19 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 08 Apr 2026 04:54:19 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Apr 2026 04:54:19 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Apr 2026 04:54:19 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:54:19 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:54:19 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Apr 2026 04:54:19 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Apr 2026 04:54:19 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Apr 2026 04:54:19 GMT
ENV container oci
# Wed, 08 Apr 2026 04:54:20 GMT
COPY dir:436d133f1cdcc884037448e774a24a829aca74f2e3df9ed98967bc293872db72 in /      
# Wed, 08 Apr 2026 04:54:20 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 08 Apr 2026 04:54:20 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 04:54:20 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 08 Apr 2026 04:54:20 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 08 Apr 2026 04:54:20 GMT
COPY file:3d096e486f3f704f5a85bb466b49e2b6383b940a165abc05b73dce12cd4502bf in /usr/share/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:54:20 GMT
COPY file:3d096e486f3f704f5a85bb466b49e2b6383b940a165abc05b73dce12cd4502bf in /root/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:54:21 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="470b852dce8e880416927445bd12327938b329e2" "org.opencontainers.image.revision"="470b852dce8e880416927445bd12327938b329e2" "build-date"="2026-04-08T04:54:09Z" "org.opencontainers.image.created"="2026-04-08T04:54:09Z" "release"="1775623882"org.opencontainers.image.revision=470b852dce8e880416927445bd12327938b329e2,org.opencontainers.image.created=2026-04-08T04:54:09Z
# Wed, 08 Apr 2026 17:40:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 08 Apr 2026 17:40:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2026 17:40:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 08 Apr 2026 17:40:59 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 08 Apr 2026 17:40:59 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 08 Apr 2026 17:43:21 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 08 Apr 2026 17:43:24 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 08 Apr 2026 17:43:25 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 08 Apr 2026 17:43:25 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 08 Apr 2026 17:43:25 GMT
CMD ["jshell"]
# Wed, 08 Apr 2026 21:33:40 GMT
CMD ["gradle"]
# Wed, 08 Apr 2026 21:33:40 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 08 Apr 2026 21:33:40 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 08 Apr 2026 21:33:40 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 08 Apr 2026 21:33:41 GMT
WORKDIR /home/gradle
# Wed, 08 Apr 2026 21:35:39 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 08 Apr 2026 21:35:39 GMT
ENV GRADLE_VERSION=7.6.6
# Wed, 08 Apr 2026 21:35:39 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Wed, 08 Apr 2026 21:38:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 08 Apr 2026 21:38:23 GMT
USER gradle
# Wed, 08 Apr 2026 21:38:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 08 Apr 2026 21:38:24 GMT
USER root
```

-	Layers:
	-	`sha256:3e558ab952e7353c7098da86d39e696cc812d91e36d37e1b280a09e42c0fa29e`  
		Last Modified: Wed, 08 Apr 2026 06:11:41 GMT  
		Size: 44.5 MB (44454533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d97b379fb6e65b4bc7725a2774f0be6887b1d49a462c3f3f788e88ffa70763`  
		Last Modified: Wed, 08 Apr 2026 17:41:37 GMT  
		Size: 32.8 MB (32849831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45349c02214a449648812ca576385d451e9efafd2d6852a245b7a609c7ee6753`  
		Last Modified: Wed, 08 Apr 2026 17:44:15 GMT  
		Size: 145.5 MB (145459994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fe6c229d31545553a55a9dad6fbb5a67736f91c97fad962ad762a03ef0c4c8`  
		Last Modified: Wed, 08 Apr 2026 17:44:10 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff7c6fce0d08204bc928cb397e0335186e227bfe7b543e91656385a061fb668`  
		Last Modified: Wed, 08 Apr 2026 17:44:11 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3ff4e0ca970cb543b98bba2fb292d9d4ad7f49c1aeb238512ed59043cdbd7b`  
		Last Modified: Wed, 08 Apr 2026 21:34:53 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70480291641f01f7c4fcf9c3388d84b7ed47db5bb82dfb9c20fab35ea5a71989`  
		Last Modified: Wed, 08 Apr 2026 21:36:30 GMT  
		Size: 37.9 MB (37932363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d682b6f3ebc437b1ae2694f54d60bb50293083962cd151daadb3a665d173c54`  
		Last Modified: Wed, 08 Apr 2026 21:39:04 GMT  
		Size: 128.5 MB (128469421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4836eac660321408272e2dd486cec850807ca578177c97da32cac2d5caa1f7e`  
		Last Modified: Wed, 08 Apr 2026 21:39:00 GMT  
		Size: 35.0 KB (35006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:59a082c6bbf4af4fa1ffbd4e162f53a44f586467ec0ade7284f36dcd089ff8f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5335510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3600333e0ec1f48a08247d25a17930f8e64e5f496041988716086350a8e082f4`

```dockerfile
```

-	Layers:
	-	`sha256:eda21001b8e2732b2b4808560868866f55c072972f6f42c879045db201a258b2`  
		Last Modified: Wed, 08 Apr 2026 21:39:01 GMT  
		Size: 5.3 MB (5311869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:163d6de15f8721de8ca39ff7b1e593c9a4e2ab2bc195057689e75d723293ac2a`  
		Last Modified: Wed, 08 Apr 2026 21:39:00 GMT  
		Size: 23.6 KB (23641 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk17-ubi9` - linux; s390x

```console
$ docker pull gradle@sha256:6f1d6e7c075ae4f1bf817f84703c97e3997b66374df6b9b45c77e42c7002a909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.0 MB (368953207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8004d9a1e071b6e5374498ef72af44e5aad66d221f6f808fabbadfb13267136`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 08 Apr 2026 04:57:30 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Apr 2026 04:57:30 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Apr 2026 04:57:30 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 08 Apr 2026 04:57:30 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 08 Apr 2026 04:57:30 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Apr 2026 04:57:30 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Apr 2026 04:57:30 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:57:30 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:57:30 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Apr 2026 04:57:30 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Apr 2026 04:57:30 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Apr 2026 04:57:30 GMT
ENV container oci
# Wed, 08 Apr 2026 04:57:31 GMT
COPY dir:df6bb403ebf6f62a05d743be5f30411253e036d1b5e6d5fe4a30348c86682080 in /      
# Wed, 08 Apr 2026 04:57:31 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 08 Apr 2026 04:57:31 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 04:57:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 08 Apr 2026 04:57:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 08 Apr 2026 04:57:31 GMT
COPY file:c085a9f1d8e36293754a8d06efb027a09ad650ab224af3e4a6fe83d436836064 in /usr/share/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:57:31 GMT
COPY file:c085a9f1d8e36293754a8d06efb027a09ad650ab224af3e4a6fe83d436836064 in /root/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:57:31 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="470b852dce8e880416927445bd12327938b329e2" "org.opencontainers.image.revision"="470b852dce8e880416927445bd12327938b329e2" "build-date"="2026-04-08T04:57:20Z" "org.opencontainers.image.created"="2026-04-08T04:57:20Z" "release"="1775623882"org.opencontainers.image.revision=470b852dce8e880416927445bd12327938b329e2,org.opencontainers.image.created=2026-04-08T04:57:20Z
# Wed, 08 Apr 2026 17:20:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 08 Apr 2026 17:20:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2026 17:20:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 08 Apr 2026 17:20:58 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 08 Apr 2026 17:20:58 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 08 Apr 2026 17:21:19 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 08 Apr 2026 17:21:21 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 08 Apr 2026 17:21:21 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 08 Apr 2026 17:21:21 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 08 Apr 2026 17:21:21 GMT
CMD ["jshell"]
# Wed, 08 Apr 2026 18:36:22 GMT
CMD ["gradle"]
# Wed, 08 Apr 2026 18:36:22 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 08 Apr 2026 18:36:22 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 08 Apr 2026 18:36:22 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 08 Apr 2026 18:36:22 GMT
WORKDIR /home/gradle
# Wed, 08 Apr 2026 18:37:51 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 08 Apr 2026 18:37:51 GMT
ENV GRADLE_VERSION=7.6.6
# Wed, 08 Apr 2026 18:37:51 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Wed, 08 Apr 2026 18:37:55 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 08 Apr 2026 18:37:55 GMT
USER gradle
# Wed, 08 Apr 2026 18:37:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 08 Apr 2026 18:37:56 GMT
USER root
```

-	Layers:
	-	`sha256:54db3bbd8a20aa62ac98659e9789851e1e6fd4f38d510a6df422467c1f72259e`  
		Last Modified: Wed, 08 Apr 2026 06:11:32 GMT  
		Size: 38.1 MB (38110884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e956f6d9c01a4c9871911b8e1ba556a77304520b107c16d8b2331d0f058b25`  
		Last Modified: Wed, 08 Apr 2026 17:21:34 GMT  
		Size: 30.4 MB (30388530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f8591ba316d118d498010a551540addc1cf6a1e5200337c6e2e01ccf0320e2`  
		Last Modified: Wed, 08 Apr 2026 17:21:59 GMT  
		Size: 135.6 MB (135629113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9028706f0dbae495441d1b4a54bc9333e80dc21994a046dcdc1103bd846dd08f`  
		Last Modified: Wed, 08 Apr 2026 17:21:55 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52323b27e992dbc9c92d11a1fabb39f77a16ade141c9f5141d5a42ff9495dbe7`  
		Last Modified: Wed, 08 Apr 2026 17:21:55 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2c8699cd129daea05630aeb30c5f506a015490d972576c18d47461dfa3ca62`  
		Last Modified: Wed, 08 Apr 2026 18:37:18 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af83ef0844337d361b3c5fccb624fedaa80974f193c3ab1b8ea28ee56518a2cd`  
		Last Modified: Wed, 08 Apr 2026 18:38:26 GMT  
		Size: 36.3 MB (36316095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa0a3d1fc3f580fe8ef58687ae536c3d9b60baaf6a034ef685afe2e850e872c`  
		Last Modified: Wed, 08 Apr 2026 18:38:28 GMT  
		Size: 128.5 MB (128469419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7330e828344826898bf44cc0522229ab71491765aad5290779197f89a74b1166`  
		Last Modified: Wed, 08 Apr 2026 18:38:24 GMT  
		Size: 35.0 KB (35010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:e633d139b64aaeb8988548b8f91a7091768d521a2ee85d2f4a136156be8642b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5324730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ab92346ea1c97b5c1af75af7f6fb8eb0bae6966e1743caf1ea04ac2690c19f`

```dockerfile
```

-	Layers:
	-	`sha256:975fa11700f3519b59b7a57c993a45d36248ec245223535d1dcada0b2e7e4bcf`  
		Last Modified: Wed, 08 Apr 2026 18:38:25 GMT  
		Size: 5.3 MB (5301151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f01e10d6257c8e12500cdcc71ef151d3b011a7eeba4615ae1b32e9f15f6c781`  
		Last Modified: Wed, 08 Apr 2026 18:38:24 GMT  
		Size: 23.6 KB (23579 bytes)  
		MIME: application/vnd.in-toto+json
